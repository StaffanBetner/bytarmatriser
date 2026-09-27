# Novus väljarbarometer juli 2026

## Källor och urval

- [Novus, *L lägsta nivån någonsin samt stödet för V sjunker*](https://novus.se/valjarbarometer-arkiv/2026-07-novus-valjarbarometer/): **5 726** röstberättigade svarande 6–9 juli 2026, efterstratifiering efter kön, ålder, utbildning, region och riksdagsvalet 2022. **1,3 %** redovisas som osäkra partiväljare.
- [Globeknot, *Fördelning religion Novus väljarbarometer juli 2026*, arkiverad 14 september](https://web.archive.org/web/20260914063708/https://globeknot.com/fordelning-religion-novus-valjarbarometer-juli-2026/): Torbjörn Sjöströms [procenttabell](https://web.archive.org/web/20260914063708im_/https://i0.wp.com/globeknot.com/wp-content/uploads/2026/08/VB-fordelat-pa-religion.png?resize=1024%2C283&ssl=1) över religionsgruppernas andelar, total partisympati och partisympati per religion. Fråga: ”Oavsett hur troende du är. Tillhör du någon religion?”
- [Globeknots nuvarande sida](https://globeknot.com/fordelning-religion-novus-valjarbarometer-juli-2026/) avser också en senare analys, **maj–augusti 2026 med 22 926 intervjuer**. Här används enbart den arkiverade julitabellen.

## Modellberäknad korstabell

[Religion × partisympati i juli 2026](religion_partisympati.md) redovisar **modellberäknade heltal på skalan 5 652**, inte observerade cellantal. Raderna är självangiven religion, kolumnerna partisympati – inte valresultat.

Globeknots partiprocent saknar kolumn för osäkra. Skalan uppskattas därför från hela Novus-urvalet: $\operatorname{avrunda}(5\,726\times(1-0{,}013))=5\,652$. Avdraget **74** är beräknat, inte publicerat. Det förutsätter att den avrundade, efterstratifierade andelen osäkra och religionsandelarna kan tillämpas på hela urvalet. **Antalet som besvarade båda frågorna är okänt**; 5 652 är inte den observerade korstabellens $N$ och cellerna duger inte för stickprovsfelmarginaler. Judendom, buddhism och annan religion får särskilt små modellmarginaler.

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

**Marginaler i samma procenttabell:** religion, i radordning: **63,9; 2,7; 0,2; 0,7; 1,2; 29,8; 1,5 %**; partisympati, i kolumnordning: **17,3; 1,8; 6,6; 6,1; 31,8; 7,8; 7,2; 20,4; 1,0 %**. [Sektordiagrammet](https://web.archive.org/web/20260914063708im_/https://i0.wp.com/globeknot.com/wp-content/uploads/2026/08/Fordelning-religion-grupper-juli-2026-1.png?resize=1024%2C787&ssl=1) anger i stället **2,6 % islam och 1,6 % ”vet ej”**. Modellen använder tabellens marginaler; skillnaden på 0,1 procentenhet är olöst.

### Beräkning och osäkerhet

1. Skala båda marginalserierna till **5 652** med största restens metod (lika rest: publicerad ordning). Radmarginaler: **3 612, 153, 11, 39, 68, 1 684, 85**; kolumnmarginaler: **978, 102, 373, 345, 1 797, 441, 407, 1 153, 56**.
2. Radnormalisera partiprocenten som startmatris; ersätt 0,0 % med **0,025 % enbart i startmatrisen** eftersom det inte är en säker strukturell nolla. Anpassa till båda marginalerna med iterative proportional fitting (IPF).
3. Avrunda anpassade celler uppåt eller nedåt med exakta marginaler och minsta sammanlagda kvadratiska avrundningsfel.

Källprocenten är avrundade och **inte helt förenliga**: gruppandelarna ger cirka **20,8 % SD**, mot publicerade **20,4 %** totalt. IPF justerar därför cellandelarna. I små grupper kan en enda modellpost motsvara flera procentenheter. Se [metodanteckningarna](../METOD.md).