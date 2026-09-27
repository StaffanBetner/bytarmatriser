# Metodanteckningar för rekonstruktion till stickprovsantal

Det här dokumentet beskriver ett **möjligt arbetssätt** när källan innehåller procent men inga fullständiga cellantal. Det är inte ett intyg på att alla befintliga matriser har beräknats på detta sätt. Dokumentera faktiskt underlag, marginaler, viktning och beräkning för varje matris i studiens README. Om antalen redan är publicerade (som i bilaga A.1 till Valundersökningen 2022) behövs ingen rekonstruktion.

## Underlag och begränsningar

- En radvis procentsatt tabell ger $P(\text{kolumn}\mid\text{rad})$ och ibland antal per rad $R_i$. En kolumnvis tabell ger $P(\text{rad}\mid\text{kolumn})$ och ibland antal per kolumn $C_j$.
- I andra fall finns en procentsatt tabell plus en separat stickprovsfördelning, eller enbart en procentsatt tabell. Saknade marginaler kan då behöva **uppskattas** och ska inte presenteras som direkt observerade.
- Om bara hela undersökningens antal intervjuer är känt, men antalet som besvarat **båda** korsade frågor saknas, är heltal framräknade på ett antaget $N$ en **syntetisk skala**, inte den observerade korstabellens faktiska stickprovsantal. Även om man drar bort en publicerad andel osäkra partiväljare från totalen är resultatet bara en uppskattning: andelen kan vara viktad och avrundad, och bortfall på den andra frågan är okänt. Redovisa uttryckligen antagandet i studiens README.
- Kontrollera att marginalerna gäller **samma urval, kategorier och viktning**. Om olika källor har skilda urval eller antal svarande går de inte utan vidare att raka mot varandra. Exempelvis gäller bilaga A.1:s redovisningsgrupper inte automatiskt samma urval som en övergångstabell för 2018 × 2022.
- En tryckt nolla (eller tom cell) behöver inte vara en strukturell nolla. Lås den bara om källan eller variabeldefinitionen ger stöd för det.

## Ett sätt att konstruera en heltalsmatris

För en radprocenttabell kan startvärdena beräknas som $T_{ij}=R_i p_{ij}/100$. Motsvarande kolumnprocenttabell ger $U_{ij}=C_j q_{ij}/100$. Om båda tabellerna och jämförbara marginaler finns kan varje startmatris anpassas separat med iterative proportional fitting (IPF) till $R$ och $C$. En möjlig syntes är att medelvärdesbilda de två anpassade matriserna och raka medelvärdet en sista gång. Om bara en procentsatt tabell finns kan dess startmatris användas; eventuell okänd marginal måste då härledas och märkas som uppskattad.

En reell matris $M$ med anpassade marginaler kan därefter heltalsavrundas med kontrollerad avrundning: välj $X_{ij}\in\{\lfloor M_{ij}\rfloor,\lceil M_{ij}\rceil\}$ så att $\sum_jX_{ij}=R_i$ och $\sum_iX_{ij}=C_j$. Kontrollera att marginalerna är heltal, har samma total och att en lösning finns givet eventuella verifierade nollor. Notera hur celler avrundades om detta är känt.

Resultatet är en **uppskattning av cellantal**, inte återvunna individsvar. Tryckta procent kan vara viktade även om redovisade antal avser oviktade svarande; kvoter av rekonstruerade antal behöver då inte reproducera procenttabellen. Exakt rekonstruktionsförfarande för äldre tabeller i repot återstår i flera fall att dokumentera.