# Korstabeller från svenska valundersökningar

Det här repot samlar **korstabeller i stickprovsantal** från undersökningar om svenska val. Målet är att samla många slags korsningar mellan partival och andra variabler: partival vid två val, demografi, social bakgrund, politiskt intresse, kunskap och andra redovisade grupper. Det är alltså inte enbart ett arkiv över väljarbyten. Nya korsningar läggs till efter hand när användbart källmaterial finns.

Tabellerna innehåller heltal på två sätt:

- **Direkt publicerade antal:** antalen finns i källan och förs över till separata korstabeller. Bilaga A.1 till Valundersökningen 2022 är ett exempel.
- **Rekonstruerade antal:** cellerna uppskattas från publicerade procenttabeller och tillgängliga stickprovsmarginaler. De är **inte** observerade mikrodata, även när de har exakta marginaler. Se [metodanteckningarna](METOD.md).

När källan redovisar stickprovsantal gäller de svarande i det aktuella urvalet, inte antal väljare i befolkningen. Om **den gemensamma svarandebasen saknas** men ett antal för hela undersökningen finns kan en tabell i stället vara **syntetiska heltal på en antagen $N$-skala**; dessa är uttryckligen märkta och är inte faktiska antal svarande på båda frågorna. Olika tabeller, även från samma undersökning, kan ha olika $N$ på grund av urval, frågor eller bortfall. Procent i originalpublikationen kan vara viktade och behöver inte gå att räkna fram genom att dividera dessa heltal. Jämför därför inte tabellernas marginaler som om de avsåg samma respondentgrupp utan att kontrollera studiens källnotering.

## Studier och tabeller

| Studie | Källa och tabellernas status | Korstabeller |
| :--- | :--- | :--- |
| Valundersökningen 2010 | [Studienotering – referens saknas](2010_valundersokningen/README.md) | [Partival 2006 × 2010](2010_valundersokningen/rd2006_rd2010_partival.md) |
| Valundersökningen 2014 | [Studienotering – referens saknas](2014_valundersokningen/README.md) | [Partival 2010 × 2014](2014_valundersokningen/rd2010_rd2014_partival.md) |
| Valundersökningen 2018 | [Oscarsson (2020), tabell 5–6](2018_valundersokningen/README.md) | [Partival 2014 × 2018](2018_valundersokningen/rd2014_rd2018_partival.md) |
| Nationella SOM-undersökningen 2018 | [Berg, Erlingsson & Oscarsson (2019), tabell 5](2018_som_undersokningen/README.md) | [Riksdagsval 2018 × kommunval 2018](2018_som_undersokningen/rd2018_kommun2018_partival.md) – heltal uppskattade från radprocent och publicerade radantal. |
| Valundersökningen 2022 | [Oscarsson m.fl. (2024): källa och tabellförteckning](2022_valundersokningen/README.md) | [Partival 2018 × 2022](2022_valundersokningen/rd2018_rd2022_partival.md); fler korsningar ur bilaga A.1 listas i studienoteringen. |
| Novus väljarbarometer juli 2026 | [Studienotering: Globeknot/Novus, julimätningen](2026-07_novus_valjarbarometer/README.md) | [Religion × partisympati](2026-07_novus_valjarbarometer/religion_partisympati.md) – syntetiska heltal på uppskattad skala 5 652 efter avdrag för osäkra partiväljare, **inte** observerade cellantal. |
| VALU 2026 | [Studienotering – exakt utgåva saknas](2026_valu/README.md) | [Partival 2022 × 2026](2026_valu/rd2022_rd2026_partival.md) |

## Organisation och dokumentation

En mapp per studie och källa namnges `<studieår>_<källa>` (med månad efter årtalet för månadsmätningar). Studiemappens README ger fullständig källhänvisning när den är känd, originaltabell och sida, länk till varje korstabell, om antalen är **publicerade eller rekonstruerade**, samt viktiga avgränsningar. Varje övrig Markdownfil i mappen innehåller **bara en korstabell**. Radernas variabel kommer först i filnamnet, kolumnernas sist: `rd2018_rd2022_partival.md` har partival 2018 på raderna och partival 2022 på kolumnerna. Samma mönster används för andra korsningar, till exempel kön × partival 2022. Studieåret i mappnamnet anger när undersökningen genomfördes, inte nödvändigtvis året i båda variablerna.

Om bättre underlag för **samma korstabell** publiceras ersätts den tidigare tabellen i samma fil. Dokumentera nytt underlag och ändrade beräkningsval i studiemappens README; Git-historiken bevarar äldre rekonstruktioner. Skapa en ny fil för en annan variabelkorsning eller ett annat urval som ska finnas kvar sida vid sida. Där källor eller metoduppgifter ännu inte är kända ska det framgå öppet i studiemappens README.

