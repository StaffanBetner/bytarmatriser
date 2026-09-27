# Novus väljarbarometer juli 2026

## Källor och urval

- [Novus, *L lägsta nivån någonsin samt stödet för V sjunker*](https://novus.se/valjarbarometer-arkiv/2026-07-novus-valjarbarometer/): väljarbarometern genomfördes **6–9 juli 2026** med totalt **5 726** röstberättigade svarande. Novus anger efterstratifiering efter kön, ålder, utbildning, region och riksdagsvalet 2022. Osäkra partiväljare redovisas separat (1,3 %).
- [Globeknot, *Fördelning religion Novus väljarbarometer juli 2026*, arkiverad 14 september 2026](https://web.archive.org/web/20260914063708/https://globeknot.com/fordelning-religion-novus-valjarbarometer-juli-2026/): Torbjörn Sjöströms redovisning av religion × partisympati. [Den arkiverade procenttabellen](https://web.archive.org/web/20260914063708im_/https://i0.wp.com/globeknot.com/wp-content/uploads/2026/08/VB-fordelat-pa-religion.png?resize=1024%2C283&ssl=1) ger religionsgruppernas andelar, partiandelar totalt och **partiandel inom varje religionsgrupp**. Frågan lyder: ”Oavsett hur troende du är. Tillhör du någon religion?”
- [Den aktuella Globeknot-sidan](https://globeknot.com/fordelning-religion-novus-valjarbarometer-juli-2026/) har senare uppdaterats med en analys för **maj–augusti 2026, 22 926 intervjuer**. Den analysens diagram avser ett annat underlag och används **inte** här; arkivkopian knyter procenttabellen till julimätningen med 5 726 intervjuer.

## Modellberäknad korstabell

[Religion × partisympati i juli 2026](religion_partisympati.md) är **heltal på en uppskattad skala om 5 652**, inte publicerade cellantal eller verifierade antal som har besvarat båda frågorna. Raderna avser självangiven religiös tillhörighet och kolumnerna uppgiven partisympati vid mätningen, **inte ett valresultat 2026**.

Novus anger **5 726 intervjuer i hela väljarbarometern** och **1,3 % osäkra partiväljare**. Eftersom Globeknots partiprocent summerar till 100 % över de angivna partierna, utan kolumn för osäkra, uppskattas skalan som $\operatorname{avrunda}(5\,726\times(1-0{,}013))=\operatorname{avrunda}(5\,651{,}562)=5\,652$. Det motsvarar ett *beräknat* avdrag om 74 modellposter; **74 är inte ett publicerat antal osäkra svarande**. Uppskattningen förutsätter att Novus andel osäkra kan tillämpas på samtliga 5 726 intervjuer och att de publicerade religionsandelarna kan användas även efter detta avdrag. Andelen osäkra är avrundad och mätningen efterstratifierad, och källan anger inte hur många som besvarade *både* religionsfrågan och partifrågan eller hur de osäkra fördelar sig mellan religionsgrupperna. Därför kan **inte heller 5 652 tolkas som den observerade korstabellens $N$**. Använd inte cellerna som exakta oviktade respondentantal eller som underlag för vanliga stickprovsfelmarginaler. Särskilt judendom, buddhism och annan religion får små modellmarginaler.

### Publicerade procent som använts

Följande är **partiprocent inom varje religionsgrupp** från Globeknots julitabell, omorienterade till samma axlar som heltalstabellen (avrundning i källan: en decimal):

| Religion | M | L | C | KD | S | V | MP | SD | Annat parti |
| :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Kristen | 19,4 | 1,5 | 8,0 | 8,1 | 31,8 | 3,9 | 5,9 | 21,0 | 0,4 |
| Islam | 2,1 | 0,2 | 0,6 | 1,5 | 61,6 | 18,7 | 4,9 | 10,4 | 0,0 |
| Judendom | 11,4 | 0,0 | 7,7 | 17,3 | 29,1 | 4,8 | 3,0 | 26,8 | 0,0 |
| Buddhist | 18,5 | 2,6 | 6,7 | 6,9 | 30,1 | 6,2 | 9,4 | 18,3 | 1,2 |
| Annan religion | 6,8 | 0,3 | 0,2 | 0,0 | 23,0 | 14,5 | 5,8 | 43,0 | 6,3 |
| Ingen religion | 14,9 | 2,4 | 4,9 | 2,9 | 30,6 | 14,4 | 9,1 | 19,3 | 1,5 |
| Vet ej (religion) | 11,6 | 0,0 | 0,3 | 0,4 | 32,1 | 1,0 | 6,8 | 42,4 | 5,5 |

I **samma procenttabell** anges religionsgruppernas andelar i ordningen ovan som **63,9; 2,7; 0,2; 0,7; 1,2; 29,8; 1,5 %** och partiernas totalandelar i kolumnordningen ovan som **17,3; 1,8; 6,6; 6,1; 31,8; 7,8; 7,2; 20,4; 1,0 %**. [Sektordiagrammet i arkivet](https://web.archive.org/web/20260914063708im_/https://i0.wp.com/globeknot.com/wp-content/uploads/2026/08/Fordelning-religion-grupper-juli-2026-1.png?resize=1024%2C787&ssl=1) anger i stället **2,6 % islam och 1,6 % ”vet ej”**. Här används uttryckligen marginalerna i *procenttabellen* för att hålla samma underlag som de korsade partiprocenten; skillnaden på 0,1 procentenhet är olöst.

### Beräkning och osäkerhet

1. Skala båda publicerade marginalprocentserierna separat till **5 652 modellposter** och avrunda med största restens metod (lika rest bryts i publicerad ordning). Detta ger radmarginaler **3 612, 153, 11, 39, 68, 1 684, 85** och kolumnmarginaler **978, 102, 373, 345, 1 797, 441, 407, 1 153, 56**.
2. Använd de avrundade partiprocenten inom varje religionsgrupp som startmatris, normaliserade per rad. Ersätt tryckt 0,0 % **i startmatrisen** med 0,025 % före normalisering; ett avrundat nollvärde antas inte vara en strukturell nolla. Anpassa startmatrisen till båda antagna marginalerna med iterative proportional fitting (IPF).
3. Heltalsavrunda varje anpassad cell uppåt eller nedåt så att båda marginalerna uppfylls exakt, med minsta sammanlagda kvadratiska avrundningsavvikelse.

Källprocenten är redan avrundade och **inte helt inbördes förenliga**: religionsandelarna viktade med partiandelarna inom respektive grupp ger exempelvis cirka **20,8 % SD**, medan publicerad partitotal är **20,4 %**. IPF måste därför ändra de inre andelarna något. För grupper med ett tiotal modellposter kan en enda cell innebära flera procentenheters skillnad. Det går inte att återskapa faktiska respondentantal ur dessa procentuppgifter ens när marginalerna är heltal. [Allmänna metodbegränsningar](../METOD.md).