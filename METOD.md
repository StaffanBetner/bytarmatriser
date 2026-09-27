# Metodanteckningar för rekonstruktion till stickprovsantal

Detta är ett **möjligt arbetssätt** för tabeller med procent men utan cellantal, inte en beskrivning av hur alla matriser i repot framställdes. Studiens README ska ange faktiskt underlag och kända beräkningssteg. Direkt publicerade cellantal behöver inte rekonstrueras.

## Underlag och begränsningar

- En radvis procentsatt tabell ger $P(\text{kolumn}\mid\text{rad})$ och ibland antal per rad $R_i$. En kolumnvis tabell ger $P(\text{rad}\mid\text{kolumn})$ och ibland antal per kolumn $C_j$.
- En procentsatt tabell utan matchande marginaler kräver **uppskattade** rad- eller kolumnstorlekar. Radprocent får inte fördelas kolumnvis utan antaganden om radstorlekarna.
- Om bara hela undersökningens antal är känt, inte hur många som besvarat **båda** frågorna, är heltal på den totalen en **antagen skala**, inte observerade cellantal. Ett avdrag för osäkra svarande är också en uppskattning: procenten kan vara viktad och avrundad, och ytterligare bortfall kan finnas.
- Marginaler måste gälla **samma urval, kategorier och viktning**. Till exempel är redovisningsgrupper i bilaga A.1 för 2022 inte automatiskt marginaler för 2018 × 2022.
- En tryckt nolla är inte nödvändigtvis en strukturell nolla; lås den bara med stöd i källa eller variabeldefinition.

## Ett sätt att konstruera en heltalsmatris

Med publicerade radantal $R_i$ och radprocent $p_{ij}$ kan startvärden beräknas som $T_{ij}=R_i p_{ij}/100$. Kolumnantal $C_j$ och kolumnprocent $q_{ij}$ ger analogt $U_{ij}=C_j q_{ij}/100$. Finns båda tabellerna och **jämförbara** marginaler kan matriserna anpassas var för sig med iterative proportional fitting (IPF), medelvärdesbildas och anpassas igen. Finns bara en procenttabell måste saknade marginaler anges som uppskattningar.

En matris $M$ med anpassade marginaler kan heltalsavrundas genom att välja $X_{ij}\in\{\lfloor M_{ij}\rfloor,\lceil M_{ij}\rceil\}$ så att $\sum_jX_{ij}=R_i$ och $\sum_iX_{ij}=C_j$. Marginalerna måste vara heltal med samma total, och avrundningen måste vara möjlig även med eventuella verifierade nollor.

Resultatet är **uppskattade cellantal**, inte återvunna individsvar. Viktade källprocent behöver inte motsvara kvoter av oviktade antal; dokumentera sådana avvikelser och metodsteg för varje tabell.