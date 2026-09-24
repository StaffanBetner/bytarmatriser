Återskapat till stickprovsantal med hjälp av t.ex. Gemini 3.8 Flash. Dubbelraking med biproportionell avrundning


# Metodbeskrivning: Rekonstruktion av bytarmatriser till stickprovsantal

### Syfte
Att ur Valforskningsprogrammets/SCB:s publicerade procenttabeller (övergångsmatriser och balansräkningar) rekonstruera den underliggande diskreta kontingenstabellen i **antal svarande individer ($N$)** så att:
1. Samtliga radsummor matchar stickprovets kända antal per kategori vid val $t-1$.
2. Samtliga kolumnsummor matchar stickprovets kända antal per kategori vid val $t$.
3. Oddskvoterna och övergångssannolikheterna från grundmaterialet bevaras med minimal informationsförlust.
4. Strukturella nollor bevaras ($0{,}0\,\% \to 0$ observationer).
5. Tabellen avrundas till heltal utan att bryta marginalsummorna.

---

### Databehov (två typfall i källmaterialet)

* **Typfall A (Standard, t.ex. 2014/2018 och 2018/2022):**
  * **Tabell 1 (Radvis):** *"Vart tog väljarna vägen?"* – ger övergångsprocenten $P(\text{val}_t \mid \text{val}_{t-1})$ samt radmarginalerna ($n_{\text{rad}}$).
  * **Tabell 2 (Kolumnvis):** *"Varifrån kom väljarna?"* – ger inflödesprocenten $P(\text{val}_{t-1} \mid \text{val}_t)$ samt kolumnmarginalerna ($n_{\text{kol}}$).
* **Typfall B (Enkel övergångstabell, t.ex. 2006/2010):**
  * **Tabell 1:** Radvis övergångstabell med radmarginaler ($n_{\text{rad}}$).
  * **Tabell 2 (eller bilaga/A.1):** Urvalsfördelningen i stickprovet vid val $t$, vilken etablerar kolumnmarginalerna ($n_{\text{kol}}$).

---

### Den matematiska algoritmen

#### Steg 1: Dubbel raking (Iterative Proportional Fitting, IPF)
När två procenttabeller finns tillgängliga skalas de först till initiala antalsmatriser:
$$T_{1,ij} = P_{\text{rad}, ij} \times \frac{R_i}{100}, \qquad T_{2,ij} = P_{\text{kol}, ij} \times \frac{C_j}{100}$$
Därefter körs **IPF (raking)** separat på båda matriserna mot de kända marginalerna $R$ (radsummor) och $C$ (kolumnsummor) tills konvergens uppnås:
* $M_1 = \text{IPF}(T_1, R, C)$
* $M_2 = \text{IPF}(T_2, R, C)$

*IPF minimerar Kullback-Leibler-divergensen mot utgångsmatrisen, vilket garanterar att den inre associativa strukturen (oddskvoterna) förblir opåverkad.*

#### Steg 2: Medelvärdesbildning (Syntes)
Eftersom tabellerna i rapporterna är tryckta med avrundade procenttal (ofta 1 decimal, ibland heltal) har de oberoende avrundningsbrus. Genom att ta medelvärdet elimineras detta brus:
$$M_{\text{medel}} = \frac{M_1 + M_2}{2}$$
*(Om bara en procenttabell fanns, som 2010, sätts $M_{\text{medel}} = M_1$).*

#### Steg 3: Slutlig raking
$M_{\text{medel}}$ rakas en sista gång mot $R$ och $C$ för att säkerställa fullständig numerisk överensstämmelse mot marginalerna ner till maskinprecision ($< 10^{-12}$).

#### Steg 4: Biproportionell heltalsavrundning (Controlled Rounding)
Vanlig avrundning av cellerna till närmaste heltal leder oundvikligen till att marginalsummorna diffar med $\pm 1$ till $3$ personer. För att lösa detta formuleras avrundningen som ett linjärt transportproblem:

$$\min_{X} \sum_{i,j} (X_{ij} - M_{ij})^2$$
under bivillkoren:
$$\sum_j X_{ij} = R_i, \quad \sum_i X_{ij} = C_j, \quad \lfloor M_{ij} \rfloor \le X_{ij} \le \lceil M_{ij} \rceil$$

Tack vare total unimodularitet i transportproblemet ger LP-lösningen strikta heltal som garanterar:
1. Att **varje enskild cell** hamnar på antingen golvet eller taket av sitt reella värde.
2. Att **samtliga rad- och kolumnsummor stämmer exakt** mot stickprovet.
3. Att strukturella nollor bevaras intakta.

---

# Promptmall för en ren session

När du startar en ny chatt (och laddar upp bilderna/tabellerna för ett nytt valpar, t.ex. 2002/2006 eller 1998/2002), klistra bara in följande prompt:

```text
Här är underlag över väljarströmmarna mellan två val, t.ex. riksdagsvalen [ÅR 1] och [ÅR 2] från exempelvis Valundersökningen eller VALU.

Målet är att ta fram den underliggande korstabellen (bytarmatrisen) i faktiskt antal svarande individer (stickprovsantal) via kalibrering (IPF) och (bi)proportionell heltalsavrundning.

GRUNDREGEL ("LÖS PROBLEMET MED DET SOM FINNS"):
Om underlaget är ofullständigt (t.ex. om den ena marginalen helt saknas), stanna INTE upp och be om mer data. Genomför istället beräkningen pragmatiskt genom att härleda saknade värden matematiskt ur det befintliga materialet enligt instruktionerna nedan.

1. Identifiera underlagstyp och fastställ marginalerna (R och C):
   Identifiera först vilken typ av underlag som givits:
   - TYP A (Två korstabeller, t.ex. rad- och kolumnprocent):
     Hämta radmarginalerna R från radtabellen och kolumnmarginalerna C från kolumntabellen.
   - TYP B (En korstabell + separat marginalfördelning):
     Hämta tabellens kända basmarginal (t.ex. R) och hämta den andra marginalen (C) från den separata stickprovsredovisningen (omvandla från % till heltal mot N om nödvändigt).
   - TYP C (Enbart EN korstabell och inga externa marginaler alls):
     1. Ta tabellens kända basmarginal (t.ex. R) och dess total N.
     2. Kompensera för tryckta procentavrundningar genom att beräkna initiala cellvärden som M_ij = R_i × (p_ij / ∑_j p_ij), så att raderna summerar exakt till R_i.
     3. Härled de implicita kolumnmarginalerna som kolumnsummorna: C_j_float = ∑_i M_ij.
     4. Avrunda C_j_float till heltal (C_j) med största restens metod (Hamilton) så att ∑C_j = N.

   Harmonisering: Säkerställ alltid att ∑R = ∑C = N. Vid små diskrepanser mellan källor, harmonisera mot det senaste valets totala N.

2. IPF-kalibrering (Iterative Proportional Fitting):
   - Vid Typ A (Två tabeller): Tillämpa trestegsraketen (raka tabell 1 och tabell 2 separat mot R och C, beräkna medelvärdet av de två kalibrerade matriserna, och raka slutmatrisen en sista gång mot R och C).
   - Vid Typ B och C (En tabell): Raka startmatrisen M iterativt mot marginalerna R och C tills full numerisk konvergens uppnås mot bägge marginaler samtidigt.

3. Slutlig heltalsmatris (Controlled Rounding):
   - Utför en biproportionell heltalsavrundning (controlled rounding via transportproblem/LP) så att varje enskild rad- och kolumnsumma matchar marginalerna R och C exakt på heltalet.
   - Strukturella nollor (0 % eller tomma celler i källan) SKA bevaras som exakta nollor (0).

Leverera:
1. Identifierad underlagstyp (A, B eller C) och de fastställda marginalerna R och C.
2. Den slutliga heltalskorstabellen som en Markdown-tabell samt Markdowntabellen i ett rått kodblock.

