# Valundersökningen 1982

## Källa

Statistiska centralbyrån (SCB). 1984. *Allmänna valen 1982. Del 3, Specialundersökningar* (General elections 1982. Vol 3, Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. LiberFörlag/Allmänna Förlaget. ISBN 91-7142-025-8, ISSN 0347-8106. Civiltryck AB, Stockholm 1984. Resultaten från 1982 års valundersökning publicerades även i serien Valundersökningar: *Väljare i förändring 1982* av Sören Holmberg.

Källmaterialet återfinns i avsnitt 6, sidan 91:

- **Tabell 8** (s. 91), ”Röstförändringar 1979–1982: Vart gick 1979 års väljare?”: **radprocent** och publicerat antal intervjupersoner per kategori 1979 (summa **2 821**).
- **Tabell 9** (s. 91), ”Röstförändringar 1979–1982: Varifrån kom 1982 års väljare?”: **kolumnprocent** och publicerat antal intervjupersoner per kategori 1982 (summa **2 826**).

Enligt text och källhänvisningar bygger resultaten till hälften på paneldata från 1979–1982 och till hälften på uppgifter som insamlats 1982. Valdeltagandet har kontrollerats mot de officiella röstlängderna. Icke-röstande redovisas som *ej röstande 1979* respektive *ej röstande 1982*, och förstagångsväljare som *ej röstberättigad 1979*.

### Partibeteckningar i tabellen

- **VPK:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **FP:** Folkpartiet (nuvarande L)
- **M:** Moderata samlingspartiet
- **KDS:** Kristen demokratisk samling (nuvarande KD)
- **MP:** Miljöpartiet de gröna (ställde upp i riksdagsvalet för första gången 1982)
- **Blankt:** Blankröstare
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigad 1979:** Förstagångsväljare 1982 (som inte uppnått rösträttsålder 1979)

## Rekonstruktion

[Partival 1979 × 1982](rd1979_rd1982_partival.md) har **publicerade radmarginaler** från tabell 8 (**126, 1 103, 469, 242, 500, 39, 21, 153, 168**, summa **2 821**) och **publicerade kolumnmarginaler** från tabell 9 (**131, 1 222, 389, 158, 609, 65, 46, 24, 182**, summa **2 826**). Skillnaden på 5 svarande beror på att fem personer med känd röstning 1982 saknade uppgift om partival 1979 i tabell 8.

För att harmonisera de två marginalerna och möjliggöra biproportionell anpassning har radmarginalerna justerats proportionellt till totalen **2 826** (+2 för S, +1 för C, FP och M: **126, 1 105, 470, 243, 501, 39, 21, 153, 168**).

Cellantalen är **rekonstruerade heltal** anpassade till båda tabellerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent och kolumnprocent som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där $p_{ij}$ är radprocent ur tabell 8 och $q_{ij}$ kolumnprocent ur tabell 9.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella kolumnmarginalerna (summa 2 826) och de harmoniserade radmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras. Samtliga 14 celler med 0 % i båda källtabellerna förblir exakt 0.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Se [metodanteckningarna](../METOD.md).
