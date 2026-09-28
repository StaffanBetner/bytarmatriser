# Valundersökningen 1973

## Källa

Statistiska centralbyrån (SCB). 1975. *Allmänna valen 1973. Del 3. Riksdagsvalet. Specialundersökningar* (General Elections 1973. Vol. 3. The election to the Riksdag in 1973. Special Surveys). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. ISBN 91-38-02536-1. Berlingska Boktryckeriet, Lund 1975.

Källmaterialet återfinns i avsnitt 4, sidorna 64–65:

- **Tabell 8** (s. 64), ”Partival och valdeltagande 1970–1973: Partiernas väljare samt ej röstande och ej röstberättigade 1970 fördelade efter röstningssätt vid riksdagsvalet 1973”:
  - **Radprocent** för varje kategori 1970.
  - Officiellt antal intervjupersoner per kategori 1970 (summa för redovisade rader: **2 332**; tillkommer **7** personer för Övriga partier enligt tabell 10, totalt **$N = 2\ 339$**).
- **Tabell 9** (s. 65), ”Partival och valdeltagande 1970–1973: Partiernas väljare samt ej röstande 1973 fördelade efter valdeltagande och partival 1970”:
  - **Kolumnprocent** för varje kategori 1973.
  - Officiellt antal intervjupersoner per kategori 1973 (summa för redovisade kolumner: **2 333**; tillkommer **6** personer för Övriga partier enligt tabell 10, totalt **$N = 2\ 339$**).
- **Tabell 10** (s. 65), ”Partival och valdeltagande 1970–1973”:
  - **Totalprocent** med hela antalet personer i tabellen ($N = 2\ 339$) som bas, avrundat till en decimal, inklusive marginalfördelningar för både 1970 och 1973.

Urvalet omfattar **$N = 2\ 339$** intervjupersoner som ingick i undersökningen och för vilka uppgifter om röstning och partival föreligger för båda valen. Uppgifter om valdeltagande har kontrollerats mot de officiella röstlängderna. Partivalet 1970 bygger på paneldata och minnesuppgifter insamlade i undersökningen.

### Partibeteckningar i tabellen

- **VPK:** Vänsterpartiet kommunisterna (nuvarande V)
- **S:** Arbetarepartiet-Socialdemokraterna
- **C:** Centerpartiet
- **FP:** Folkpartiet (nuvarande L)
- **M:** Moderata samlingspartiet
- **KDS:** Kristen demokratisk samling (nuvarande KD)
- **Övr:** Övriga partier
- **Ej röstande:** Personer som avstod från att rösta i respektive val
- **Ej röstberättigade 1970:** Förstagångsväljare 1973 (som inte hade uppnått rösträttsålder 1970)

## Rekonstruktion

[Partival 1970 × 1973](rd1970_rd1973_partival.md) har **både publicerade radmarginaler** (**65, 1 021, 381, 261, 208, 36, 7, 217, 143**) och **publicerade kolumnmarginaler** (**97, 1 021, 559, 179, 278, 44, 6, 155**). Båda marginalerna summerar exakt till **2 339**.

Cellantalen är **rekonstruerade heltal** anpassade till källans tre samtidiga tabeller (radprocent i tabell 8, kolumnprocent i tabell 9 och totalprocent i tabell 10):

1. **Startmatris:** Beräknad genom vägt medelvärde av estimerade individantal utifrån radprocent ($R_i \times p_{ij} / 100$), kolumnprocent ($C_j \times q_{ij} / 100$) och totalprocent ($N \times t_{ij} / 100$).
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella rad- och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som avrundningsfelet mot källans tabeller minimeras.

Det maximala felet mot tabellernas publicerade procentsatser är minimalt och ryms väl inom källans avrundningsintervall. Se [metodanteckningarna](../METOD.md).
