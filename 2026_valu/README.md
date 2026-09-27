# VALU 2026

## Källa

[SVT, *SVT:s Vallokalsundersökning: Riksdagsvalet 2026*](https://omoss.svt.se/download/18.c7d6c981a0a583535d1535/1789484134179/Valu%202026%20seminarium%20260915.pdf) är ett **seminarieunderlag från 15 september 2026**, inte en slutrapport. PDF-sida 18 (uppslaget märkt 18–19) redovisar vägda **radprocent** för tolv 2022-rader × nio 2026-kolumner: åtta partier och Övr samt 2022 års blankröstare, ej röstande och ej röstberättigade. **Cellantal och antal svar per rad saknas.** PDF-sidorna 1 och 5 anger **13 709 insamlade enkäter**; sida 6 redovisar ”Valu rådata” som partiprocent 2026 och sida 7 beskriver viktning mot valresultat.

[SVT Nyheters väljarströmsgrafik](https://www.svt.se/nyheter/sa-har-valjarna-rort-sig), uppdaterad 14 september 2026, återges för åtta partier i [Wikipedias tabeller ”Väljarströmmar”](https://sv.wikipedia.org/wiki/Riksdagsvalet_i_Sverige_2026) (avlästa 28 september 2026). De visar procent i **båda riktningarna**, men avser ett snävare, viktat urval än PDF-tabellen: bland annat visas inte förstagångsväljare, blankröstare eller dem som inte röstade 2022. Wikipedia är en sekundär källa för jämförelse, inte för cellantal.

## Rekonstruktion

[Partival 2022 × 2026](rd2022_rd2026_partival.md) är en tillhandahållen **rekonstruktion**, inte publicerade cellantal. Matrisens $N=13\,709$ är det kända antalet insamlade enkäter, **inte ett redovisat antal som besvarat båda frågorna**. Att använda totalen som korstabellens nämnare är ett antagande.

**Sannolik beräkning:** De nio avrundade rådataprocenten på PDF-sida 6 (summa 99,9 %) normaliseras till 100 %, multipliceras med 13 709 och avrundas med största restens metod. Det ger **exakt tabellens kolumnsummor**, men inte verifierade kolumnantal. Om varje kolumnsumma $C_j$ därefter fördelas enligt sida 18:s tolv procenttal $p_{ij}$, fås $x_{ij}=C_j p_{ij}/\sum_{k=1}^{12}p_{kj}$. Kolumnvis avrundning ger **100 av 108 celler exakt**; övriga åtta skiljer ett steg uppåt eller nedåt. Den ursprungliga avrundningsmetoden är inte dokumenterad.

**Begränsning:** PDF-procenten avser $P(2026\mid 2022)$, inte $P(2022\mid 2026)$. Att fördela dem kolumnvis utan kända radstorlekar ändrar därför nämnaren. Exempelvis blir S→S **77,5 %** av S-raden i matrisen mot **73 %** i PDF:en; bland de åtta namngivna 2022-partierna blir S→S **44,5 %** av S-kolumnen mot **75 %** i SVT/Wikipedias snävare redovisning. Jämförelserna är inte exakta felmått eftersom källprocenten är viktade och urvalen delvis skiljer sig. Utan svarandebas och radmarginaler kan de faktiska cellantalen inte bestämmas; ersätt matrisen i samma fil när bättre underlag finns.
