# Valundersökningen 1994

## Källa

Statsvetenskapliga institutionen vid Göteborgs universitet och Statistiska centralbyrån (SCB). 1995. *Allmänna valen 1994. Del 3, Specialundersökningar* (General elections in 1994. Vol 3, Special Studies). Sveriges officiella statistik. Stockholm: Statistiska centralbyrån. ISBN 91-618-0798-2, ISSN 0347-8106.

De tillhandahållna bilderna visar följande tabeller på sidan 127:

- **Tabell 5.14**, ”Vart gick 1991 års väljare? (procent)” (Where did the voters in 1991 go? per cent): **radprocent** och antal personer per kategori 1991 (summa **2 554**).
- **Tabell 5.15**, ”Varifrån kom 1994 års väljare? (procent)” (From where did the voters in 1994 come? per cent): **kolumnprocent** och antal personer per kategori 1994 (summa **2 554**).

Enligt tabellkommentaren (s. 127) bygger resultaten på uppgifter från **2 554 intervjupersoner**. Information om partivalet 1991 kommer för halva urvalet från minnesuppgifter insamlade 1994 och för andra halvan från paneldata insamlade 1991. Valdeltagandet har kontrollerats mot de officiella röstlängderna. Icke-röstning betecknas som *Ej röstande* i båda tabellerna.

## Rekonstruktion

[Partival 1991 × 1994](rd1991_rd1994_partival.md) har **både publicerade radmarginaler** från tabell 5.14 (**71, 786, 168, 234, 473, 111, 67, 117, 26, 39, 257, 205**) och **publicerade kolumnmarginaler** från tabell 5.15 (**153, 1 059, 195, 176, 472, 95, 118, 25, 8, 46, 207**). Båda marginalerna summerar exakt till **2 554**.

Cellantalen är **rekonstruerade heltal** anpassade till båda marginalerna:

1. **Startmatris:** Beräknad utifrån publicerade radprocent och kolumnprocent som $M^{(0)}_{ij} = \frac{1}{2}\left(\frac{R_i p_{ij}}{100} + \frac{C_j q_{ij}}{100}\right)$, där $p_{ij}$ är radprocent ur tabell 5.14 och $q_{ij}$ kolumnprocent ur tabell 5.15.
2. **Marginalanpassning (IPF):** Matrisen anpassades iterativt med iterative proportional fitting till de officiella rad- och kolumnmarginalerna.
3. **Heltalsavrundning:** De anpassade cellerna avrundades med kontrollerad heltalsavrundning (min-cost network flow) så att varje radsumma $R_i$ och varje kolumnsumma $C_j$ bevaras exakt, samtidigt som det sammanlagda kvadratiska avrundningsfelet minimeras.

Resultatet är uppskattade cellantal och inte verifierade individsvar. Avrundade procent i källan kan dölja enskilda svarande (särskilt i små grupper som Övriga partier 1994 med $N=8$, där varje individ motsvarar $12{,}5\ \%$). Se [metodanteckningarna](../METOD.md).
