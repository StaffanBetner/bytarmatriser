# Valundersökningen 1991

## Källa

Statistiska centralbyrån (SCB). 1993. *Allmänna valen 1991. Del 3, Specialundersökningar* (General elections 1991. Vol 3, Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. Författare: Mikael Gilljam, Sören Holmberg, Lis Berling-Agståhl, Olle Johansson, Leif Lemon, Michael Nilsson. ISBN 91-618-0356-1, ISSN 0347-8106.

Källmaterialet återfinns på sidorna 127–128:

- **Tabell 11** (s. 127), ”Röstförändringar 1988 – 1991: Vart gick 1988 års väljare?”: **radprocent** och antal intervjuade personer per kategori 1988 (summa **2 597**).
- **Tabell 12** (s. 128), ”Röstförändringar 1988 – 1991: Varifrån kom 1991 års väljare?”: **kolumnprocent** och antal intervjuade personer per kategori 1991 (summa **2 597**).

Enligt tabellkommentaren (s. 127–128) bygger resultaten i tabellerna på uppgifter från **2 607 intervjupersoner** (varav 2 597 med redovisat röstnings- och partival). Information om partivalet 1988 härrör för halva urvalet från minnesuppgifter insamlade 1991 och för andra halvan från paneldata insamlade vid valet 1988. Valdeltagandet har kontrollerats mot de officiella röstlängderna. Icke-röstning betecknas som *Ej röstande* i båda tabellerna.

### Partibeteckningar i tabellen

- **v:** Vänsterpartiet
- **s:** Arbetarepartiet-Socialdemokraterna
- **c:** Centerpartiet
- **fp:** Folkpartiet liberalerna
- **m:** Moderata samlingspartiet
- **kds:** Kristen demokratisk samling
- **mp:** Miljöpartiet de gröna
- **nyd:** Ny demokrati (enbart valbart 1991)
- **övr / övriga partier:** Övriga partier
- **blankt:** Blankröst
- **ej röstande:** Personer som avstod från att rösta i respektive val
- **ej röstberättigade 1988:** Förstagångsväljare 1991 (som inte hade uppnått rösträttsålder 1988)

## Rekonstruktion

[Partival 1988 × 1991](rd1988_rd1991_partival.md) har **både publicerade radmarginaler** från tabell 11 (**103, 974, 249, 252, 373, 55, 112, 8, 24, 267, 180**) och **publicerade kolumnmarginaler** från tabell 12 (**83, 884, 206, 215, 507, 173, 87, 162, 16, 38, 226**). Båda marginalerna summerar exakt till **2 597**.

Cellantalen är **rekonstruerade heltal** anpassade till båda marginalerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent ur tabell 11 och kolumnprocent ur tabell 12 som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där $p_{ij}$ är radprocent och $q_{ij}$ kolumnprocent.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella rad- och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras. Celler med noll procent i båda källtabellerna förblir exakt noll.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Se [metodanteckningarna](../METOD.md).
