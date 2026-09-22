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
Här är tabeller över väljarströmmarna mellan riksdagsvalen [ÅR 1] och [ÅR 2] från Valundersökningen.

Jag vill ta fram den underliggande korstabellen (bytarmatrisen) i faktiskt antal svarande individer (stickprovsantal) i en trestegsraket med biproportionell heltalsavrundning:

1. Marginaler:
   - Identifiera radmarginalerna (R = antal svarande per kategori val [ÅR 1]).
   - Identifiera kolumnmarginalerna (C = antal svarande per kategori val [ÅR 2] i stickprovet, ej valresultatet).
   - Om det finns en liten diskrepans i N mellan tabellerna, harmonisera radmarginalerna proportionellt mot kolumntotalen.

2. Trestegsraketen (IPF):
   - Steg 1: Raka de bägge tabellerna (radvis och kolumnvis) separat mot de kända marginalerna R och C med Iterative Proportional Fitting.
   - Steg 2: Ta det aritmetiska medelvärdet av de två kalibrerade matriserna för att minimera avrundningsfel från källans tryckta procenttal.
   - Steg 3: Raka den resulterande matrisen en sista gång mot marginalerna för fullständig numerisk konvergens.
   (Om endast en övergångstabell finns, raka den direkt mot rad- och kolumnmarginalerna).

3. Slutlig heltalsmatris:
   - Gör en biproportionell heltalsavrundning (controlled rounding / transportproblem) så att varje enskild radsumma och kolumnsumma matchar marginalerna exakt på heltalet, och strukturella nollor (0,0 %) bevaras som 0.

Leverera:
1. Den beräknade matrisen med 1 decimal.
2. Den slutliga heltalskorstabellen formaterad som en snygg Markdown-tabell (samt i ett rått kopierbart kodblock).
```
