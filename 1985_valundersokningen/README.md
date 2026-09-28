# Valundersökningen 1985

## Källa

Statistiska centralbyrån (SCB). 1987. *Allmänna valen 1985. Del 3, Specialundersökningar* (General elections 1985. Vol 3, Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. ISBN 91-618-0161-5, ISSN 0347-8106. ALLF 410 6 132. Civiltryck AB, Stockholm 1987. Författare: Lis Berling-Agståhl, Sören Holmberg, Olle Johansson och Leif Lemon. Resultaten från 1985 års valundersökning publicerades även som rapport nr 10 i serien Valundersökningar: *Väljare och val i Sverige*.

Källmaterialet återfinns i avsnitt 6, sidan 95:

- **Tabell 9** (s. 95), ”Röstförändringar 1982–1985: Vart gick 1982 års väljare?”: **radprocent** och publicerat antal intervjuade personer per kategori 1982 (summa **2 802**).
- **Tabell 10** (s. 95), ”Röstförändringar 1982–1985: Varifrån kom 1985 års väljare?”: **kolumnprocent** och publicerat antal intervjuade personer per kategori 1985 (summa **2 802**).

Enligt tabellkommentaren (s. 95) bygger resultaten i tabellerna 8–10 till hälften på paneldata från 1982–1985 och till hälften på uppgifter som insamlats 1985. Valdeltagandet har kontrollerats mot röstlängden. Centerväljare har delats upp på Centerpartiet (C) och KDS med hjälp av en intervjufråga om de röstade på en centerpartilista eller en KDS-lista i riksdagsvalet (med anledning av valsamverkan Centern i valet 1985).

### Partibeteckningar i tabellen

- **VPK:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **FP:** Folkpartiet (nuvarande L)
- **M:** Moderata samlingspartiet
- **KDS:** Kristen demokratisk samling (nuvarande KD)
- **MP:** Miljöpartiet de gröna
- **Blankt:** Blankröstare
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigad 1982:** Förstagångsväljare 1985 (som inte uppnått rösträttsålder 1982)

## Rekonstruktion

[Partival 1982 × 1985](rd1982_rd1985_partival.md) har **både publicerade radmarginaler** från tabell 9 (**121, 1 120, 357, 189, 549, 47, 39, 24, 172, 184**) och **publicerade kolumnmarginaler** från tabell 10 (**134, 1 150, 277, 415, 517, 60, 45, 27, 177**). Båda marginalerna summerar exakt till **2 802**.

Cellantalen är **rekonstruerade heltal** anpassade till båda marginalerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent och kolumnprocent som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där $p_{ij}$ är radprocent ur tabell 9 och $q_{ij}$ kolumnprocent ur tabell 10.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella rad- och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras. Samtliga 10 celler med 0 % i båda källtabellerna förblir exakt 0.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Se [metodanteckningarna](../METOD.md).
