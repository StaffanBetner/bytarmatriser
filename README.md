# Korstabeller från svenska valundersökningar

Det här repot samlar **korstabeller i stickprovsantal** från svenska valundersökningar: partival vid olika val och korsningar med exempelvis demografi, social bakgrund, intresse och kunskap.

Tabellerna innehåller heltal på två sätt:

- **Publicerade antal:** cellerna har förts över från källan, exempelvis bilaga A.1 till Valundersökningen 2022.
- **Rekonstruerade antal:** cellerna har uppskattats från procent och marginaler; de är inte observerade individsvar. Se [metodanteckningarna](METOD.md).

Antalen avser undersökningens svarande, inte väljare i befolkningen. En tabell kan också vara **syntetiska heltal på en antagen skala** om antalet som besvarat båda frågorna är okänt. Urval, bortfall och viktning kan skilja sig mellan tabeller; jämför därför deras marginaler mot respektive studienotering.

## Studier och tabeller

| Studie | Källa och tabellernas status | Korstabeller |
| :--- | :--- | :--- |
| Valundersökningen 2006 | [Oscarsson & Holmberg (2008), tabell 2.1](2006_valundersokningen/README.md) | [Partival 2002 × 2006](2006_valundersokningen/rd2002_rd2006_partival.md) – uppskattade heltal från radprocent och publicerade radantal. |
| Valundersökningen 2010 | [Oscarsson & Holmberg (2011), tabell 14 och A.1](2010_valundersokningen/README.md) | [Partival 2006 × 2010](2010_valundersokningen/rd2006_rd2010_partival.md) |
| Valundersökningen 2014 | [Oscarsson (2016), tabell 2–3](2014_valundersokningen/README.md) | [Partival 2010 × 2014](2014_valundersokningen/rd2010_rd2014_partival.md) |
| Valundersökningen 2018 | [Oscarsson (2020), tabell 5–6](2018_valundersokningen/README.md) | [Partival 2014 × 2018](2018_valundersokningen/rd2014_rd2018_partival.md) |
| Nationella SOM-undersökningen 2018 | [Berg, Erlingsson & Oscarsson (2019), tabell 5](2018_som_undersokningen/README.md) | [Riksdagsval 2018 × kommunval 2018](2018_som_undersokningen/rd2018_kommun2018_partival.md) – heltal uppskattade från radprocent och publicerade radantal. |
| Valundersökningen 2022 | [Oscarsson m.fl. (2024): källa och tabellförteckning](2022_valundersokningen/README.md) | [Partival 2018 × 2022](2022_valundersokningen/rd2018_rd2022_partival.md); fler korsningar ur bilaga A.1 listas i studienoteringen. |
| Novus väljarbarometer juli 2026 | [Studienotering: Globeknot/Novus, julimätningen](2026-07_novus_valjarbarometer/README.md) | [Religion × partisympati](2026-07_novus_valjarbarometer/religion_partisympati.md) – syntetiska heltal på uppskattad skala 5 652 efter avdrag för osäkra partiväljare, **inte** observerade cellantal. |
| VALU 2026 | [SVT:s seminarieunderlag och väljarströmsgrafik](2026_valu/README.md) | [Partival 2022 × 2026, 12 × 9](2026_valu/rd2022_rd2026_partival.md) – rekonstruerade heltal på skalan **13 709 insamlade enkäter**, härledda ur PDF-radprocent och rådatamarginal; antalet som besvarade båda frågorna är inte publicerat. |

## Organisation och dokumentation

En mapp per studie och källa namnges `<studieår>_<källa>` (med månad för månadsmätningar). Studiemappens README anger källa, originaltabell, status och avgränsningar; varje annan Markdownfil i mappen innehåller **en korstabell**. Filnamnet anger först radvariabeln, sedan kolumnvariabeln: `rd2018_rd2022_partival.md` har 2018 på raderna och 2022 på kolumnerna. Mappens år avser undersökningen, inte nödvändigtvis båda variablerna.

När bättre underlag finns för **samma korstabell**, ersätt den i samma fil och uppdatera studienoteringen; Git-historiken bevarar äldre versioner. Använd en ny fil för en annan korsning eller ett annat urval. Redovisa okända källor och metodsteg öppet.

