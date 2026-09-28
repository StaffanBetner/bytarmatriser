# Valundersökningen 1979

## Källa

Statistiska centralbyrån (SCB). 1981. *Allmänna valen 1979. Del 3, Specialundersökningar* (General elections 1979. Vol 3, Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. LiberFörlag/Allmänna Förlaget. ISBN 91-38-6591-6, ISSN 0347-8106. Civiltryck AB, Stockholm 1981. Resultaten från 1979 års valundersökning publicerades även i serien Valundersökningar: *Väljarna och valet 1979* (Rapport 2) av Sören Holmberg.

Källmaterialet återfinns i avsnitt 6, sidan 136:

- **Tabell 10** (s. 136), ”Röstförändringar 1976–1979: vart gick 1976 års väljare?”: **radprocent** och publicerat antal intervjuade per kategori 1976 (summa **2 739**).
- **Tabell 11** (s. 136), ”Röstförändringar 1976–1979: varifrån kom 1979 års väljare?”: **kolumnprocent** och publicerat antal intervjuade per kategori 1979 (summa **2 740**).

Enligt undersökningsdesignen bygger materialet på valundersökningens paneldesign kombinerad med registerkontroll av valdeltagandet ur de officiella röstlängderna. Icke-röstande redovisas som *ej röstande 1976* respektive *ej röstande 1979*, och förstagångsväljare som *ej röstberättigade 1976*.

### Partibeteckningar i tabellen

- **VPK:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **FP:** Folkpartiet (nuvarande L)
- **M:** Moderata samlingspartiet
- **Övriga partier / Övr:** Övriga partier (inklusive KDS och övriga småpartier)
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigade 1976:** Förstagångsväljare 1979 (som inte uppnått rösträttsålder 1976)

## Rekonstruktion

[Partival 1976 × 1979](rd1976_rd1979_partival.md) har **publicerade radmarginaler** från tabell 10 (**91, 1 107, 575, 268, 337, 42, 151, 168**, summa **2 739**) och **publicerade kolumnmarginaler** från tabell 11 (**137, 1 170, 437, 287, 516, 52, 141**, summa **2 740**). Skillnaden på 1 svarande beror på en respondent med känd röstning 1979 som saknade uppgift om partival 1976.

För att harmonisera de två marginalerna har radmarginalerna justerats proportionellt till totalen **2 740** via Hamiltons metod (+1 till största gruppen S: **91, 1 108, 575, 268, 337, 42, 151, 168**).

Cellantalen är **rekonstruerade heltal** anpassade till båda tabellerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent och kolumnprocent som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där $p_{ij}$ är radprocent ur tabell 10 och $q_{ij}$ kolumnprocent ur tabell 11.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella kolumnmarginalerna (summa 2 740) och de harmoniserade radmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras. Celler med 0 % i båda källtabellerna (VPK $\to$ C, VPK $\to$ FP, VPK $\to$ M, M $\to$ Ej röstande 1979 samt Övriga partier $\to$ Ej röstande 1979) förblir exakt 0.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Se [metodanteckningarna](../METOD.md).
