# Valundersökningen 1970

## Källa

Statistiska centralbyrån (SCB). 1973. *Allmänna valen 1970. Del 3. Riksdagsvalet. Specialundersökningar* (General Elections 1970. Vol. 3. The election to the Riksdag. Special studies). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån.

Källmaterialet återfinns på sidan 69:

- **Tabell 4.7**, ”Partival och valdeltagande 1970 fördelat efter partival och valdeltagande 1968 (procent)”:
  - **4.7 A:** Radprocent (1968 års väljare fördelade på 1970 års valdeltagande och partival).
  - **4.7 B:** Kolumnprocent (1970 års väljare fördelade på 1968 års valdeltagande och partival).
  - **4.7 C:** Totalprocent (procentandel av totalurvalet $N = 4\ 022$, avrundat till en decimal), inklusive officiella radantal och kolumnantal.

Urvalsstorleken i tabellen är **$N = 4\ 022$** intervjupersoner som deltog i undersökningen och för vilka uppgift om röstning föreligger i båda valen. Uppgifter om valdeltagande har kontrollerats mot röstlängderna. Partivalet 1968 bygger delvis på paneluppgifter (från 1968 års undersökning) och delvis på minnesuppgifter insamlade 1970.

### Partibeteckningar i tabellen

- **K:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **F:** Folkpartiet (nuvarande L)
- **B:** Borgerlig samling / Mellanpartierna (gemensamma borgerliga samlingslistor i Skåne och Gotland m.fl. valkretsar)
- **KDS:** Kristen demokratisk samling (nuvarande KD)
- **M:** Moderata samlingspartiet
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigade 1968:** Förstagångsväljare 1970 (som inte hade uppnått rösträttsålder 1968)

## Rekonstruktion

[Partival 1968 × 1970](rd1968_rd1970_partival.md) har **både publicerade radmarginaler** (**68, 1 857, 587, 455, 13, 36, 377, 347, 282**) och **publicerade kolumnmarginaler** (**146, 1 790, 805, 510, 3, 51, 318, 399**). Båda marginalerna summerar exakt till **4 022**.

Cellantalen är **rekonstruerade heltal** anpassade till båda marginalerna:

1. **Startmatris:** Beräknad utifrån publicerade totalprocent ur tabell 4.7 C ($p_{ij} \times 4\ 022 / 100$). Celler med avrundat $0{,}0\ \%$ i kolumner/rader med marginellt restvärde (t.ex. listan B med 3 väljare 1970) tilldelades ett litet positivt startvärde.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella rad- och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som avrundningsfelet minimeras.

Det maximala absoluta felet mellan rekonstruerade cellprocent och tabellens publicerade procent är mindre än $0{,}1$ procentenhet ($0{,}09\ \%$). Se [metodanteckningarna](../METOD.md).
