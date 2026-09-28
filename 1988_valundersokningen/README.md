# Valundersökningen 1988

## Källa

Statistiska centralbyrån (SCB). 1990. *Allmänna valen 1988. Del 3, Specialundersökningar* (General elections 1988. Vol 3, Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. ISBN 91-618-0356-1, ISSN 0347-8106. Norstedts Tryckeri, Stockholm 1990. Libergraf 410 0 025. Författare: Lis Berling-Agståhl, Mikael Gilljam, Sören Holmberg, Olle Johansson, Leif Lemon och Michael Nilsson. Resultaten från 1988 års valundersökning publicerades även som rapport nr 12 i serien Valundersökningar: *Rött Blått Grönt*.

Källmaterialet återfinns i avsnitt 6, sidorna 103–104:

- **Tabell 7** (s. 103), ”Röstförändringar 1985–1988: Vart gick 1985 års väljare?”: **radprocent** och publicerat antal intervjuade personer per kategori 1985 (summa **2 657**).
- **Tabell 8** (s. 104), ”Röstförändringar 1985–1988: Varifrån kom 1988 års väljare?”: **kolumnprocent** och publicerat antal intervjuade personer per kategori 1988 (summa **2 657**).

Enligt tabellkommentaren (s. 104) bygger resultaten på uppgifter från **2 657 intervjupersoner**. Information om partivalet 1985 härrör för halva urvalet från minnesuppgifter insamlade 1988 och för andra halvan från paneldata insamlade vid valet 1985. Valdeltagandet har kontrollerats mot de officiella röstlängderna. Icke-röstande redovisas som *ej röstande 1985* respektive *ej röstande 1988*, och förstagångsväljare som *ej röstberättigad 1985*.

### Partibeteckningar i tabellen

- **VPK:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **FP:** Folkpartiet (nuvarande L)
- **M:** Moderata samlingspartiet
- **KDS:** Kristen demokratisk samling (nuvarande KD)
- **MP:** Miljöpartiet de gröna
- **Övr:** Övriga partier
- **Blankt:** Blankröstare
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigad 1985:** Förstagångsväljare 1988 (som inte uppnått rösträttsålder 1985)

## Rekonstruktion

[Partival 1985 × 1988](rd1985_rd1988_partival.md) har **både publicerade radmarginaler** från tabell 7 (**118, 1 071, 261, 335, 451, 36, 55, 3, 19, 129, 179**) och **publicerade kolumnmarginaler** från tabell 8 (**127, 1 081, 277, 277, 395, 63, 141, 8, 33, 255**). Båda marginalerna summerar exakt till **2 657**.

Cellantalen är **rekonstruerade heltal** anpassade till båda marginalerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent och kolumnprocent som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där $p_{ij}$ är radprocent ur tabell 7 och $q_{ij}$ kolumnprocent ur tabell 8. (I tabell 8 summerar kolumnen för VPK till 91 % i trycket, men IPF anpassar cellerna simultant mot båda marginalerna).
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella rad- och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras. Samtliga 27 celler med 0 % i båda källtabellerna förblir exakt 0.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Se [metodanteckningarna](../METOD.md).
