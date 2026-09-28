# Valundersökningen 1976

## Källa

Statistiska centralbyrån (SCB). 1978. *Allmänna valen 1976. Del 3, Specialundersökningar* (General elections 1976. Vol 3, Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. LiberFörlag/Allmänna Förlaget. ISBN 91-38-04295-9, ISSN 0347-8106. Civiltryck AB, Stockholm 1978. Resultaten från 1976 års valundersökning publicerades även i serien Valundersökningar: *Väljarna och valet 1976* (Rapport 2) av Olof Petersson.

Källmaterialet återfinns i avsnitt 6, sidan 136:

- **Tabell 11** (s. 136), ”Röstförändringar 1973–1976: vart gick 1973 års väljare?”: **radprocent** och publicerat antal intervjuade per kategori 1973 (summa **2 522**). Kolumnerna redovisar VPK, S, C, FP, M, Övriga partier samt Ej röstande 1976.
- **Tabell 12** (s. 136), ”Röstförändringar 1973–1976: varifrån kom 1976 års väljare?”: **kolumnprocent** och publicerat antal intervjuade per kategori 1976 för sex grupper: VPK (100), S (1 098), C (550), FP (284), M (326) samt Ej röstande (120), summa **2 478**. Kategorin *Övriga* utelämnades som separat kolumn i Tabell 12.

Skillnaden mellan Tabell 11:s radsumma (2 522) och de sex redovisade kolumnerna i Tabell 12 (2 478) är exakt **44 intervjuade**, vilket motsvarar väljarna för *Övriga partier 1976* (vars förväntade summa utifrån Tabell 11 är 44,4).

Enligt undersökningsdesignen bygger materialet på valundersökningens paneldesign (tvåstegspanel) kombinerad med registerkontroll av valdeltagandet ur de officiella röstlängderna. Icke-röstande redovisas som *ej röstande*, och förstagångsväljare som *ej röstberättigade 1973*.

### Partibeteckningar i tabellen

- **VPK:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **FP:** Folkpartiet (nuvarande L)
- **M:** Moderata samlingspartiet
- **Övriga partier / Övriga:** Övriga partier (inklusive KDS och övriga småpartier)
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigade 1973:** Förstagångsväljare 1976 (som inte uppnått rösträttsålder 1973)

## Rekonstruktion

[Partival 1973 × 1976](rd1973_rd1976_partival.md) har **publicerade radmarginaler** från tabell 11 (**87, 1 023, 521, 195, 248, 46, 174, 228**, summa **2 522**) och **kolumnmarginaler** (**100, 1 098, 550, 284, 326, 44, 120**, summa **2 522**).

Cellantalen är **rekonstruerade heltal** anpassade till båda tabellerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent ur Tabell 11 och kolumnprocent ur Tabell 12 som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där kolumnprocenten för *Övriga partier 1976* härletts ur Tabell 11.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella radmarginalerna och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras. Celler med 0 % i båda källtabellerna (t.ex. VPK $\to$ FP, VPK $\to$ M, FP $\to$ VPK, M $\to$ VPK samt Övriga partier $\to$ Ej röstande) förblir exakt 0.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Se [metodanteckningarna](../METOD.md).
