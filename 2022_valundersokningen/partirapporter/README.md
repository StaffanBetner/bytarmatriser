# Valforskningsprogrammets partirapporter – Valet 2022

## Källa och bakgrund

Valforskningsprogrammet vid Statsvetenskapliga institutionen, Göteborgs universitet, publicerar en rapportserie med fördjupade partirapporter för riksdagsvalet 2022. Rapporterna bygger på data från den stora Valundersökningen 2022 och analyserar partiernas väljarprofil, partiledarförtroende, profilfrågor samt väljarnas sakpolitiska preferenser.

Till skillnad från tabellerna i [2022_valundersokningen](../README.md) (som återger oviktade stickprovsantal ur bilaga A.1 till *Väljarna och valet 2022*) redovisar partirapporterna **viktade procentandelar** kalibrerade mot det officiella valresultatet 2022.

## Tabellernas struktur och påbyggnad

Tabellerna i denna undermapp är samlade korstabeller där kolumnerna motsvarar de åtta riksdagspartierna:

$$\text{V}, \quad \text{S}, \quad \text{MP}, \quad \text{C}, \quad \text{L}, \quad \text{KD}, \quad \text{M}, \quad \text{SD}$$

samt en referenskolumn för **Samtliga väljare** (där sådan redovisas i källan). Tabellerna byggs på successivt med nya kolumner allteftersom partirapporter för respektive parti tillhandahålls. Värden som ännu inte är inlagda markeras med `–`.

### Heltal respektive publicerade andelar (enligt METOD.md)
I enlighet med principerna i [METOD.md](../../METOD.md) antas aldrig ett hypotetiskt $N$ när källan redovisar ett urvalsintervall:
- **Rekonstruerade råtabeller (stickprovsantal i heltal):** Endast för tabeller där frågans basurval $n$ är entydigt och exakt redovisat och direkt mappar mot svarsfördelningen ([A1](partiomdome_rd2022.md), [A2](partiledaromdome_rd2022.md), [A3](vanster_hoger_partier_rd2022.md), [A4](flyktingpolitik_partier_rd2022.md) samt [A9](partianhangarskap_rd2022.md)) redovisas heltalsantal beräknade med största restens metod, åtföljda av de ursprungliga källprocenten i en separat sektion.
- **Publicerade andelar (procent):** För tabeller där urvalsstorleken $n$ är redovisad som ett intervall, eller där flervalsfrågor/batterier saknar entydig mappning per rad ([A5](profilfragor_partier_rd2022.md), [A6a](brapolitik_partier_rd2022.md), [A6b](daligpolitik_partier_rd2022.md), [A7](demografi_partivaljare_rd2022.md), [A8](politiska_faktorer_rd2022.md), [A10](rostningsagerande_rd2022.md), [A11](skal_for_partival_rd2022.md), [A12](viktiga_fragor_rd2022.md), [A13](framtida_samhalle_rd2022.md), [A14](sakfragor_rd2022.md)) härleds **inga** råtabeller. Istället behålls de publicerade viktade procentandelarna direkt i tabellen.

### Registrerade rapporter i serien (samtliga riksdagspartier)
- **Vänsterpartiet (V)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Vänsterpartiet. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:8.
- **Socialdemokraterna (S)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Socialdemokraterna. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:11.
- **Miljöpartiet (MP)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Miljöpartiet. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:5.
- **Centerpartiet (C)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Centerpartiet. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:7.
- **Liberalerna (L)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Liberalerna. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:4.
- **Kristdemokraterna (KD)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Kristdemokraterna. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:6.
- **Moderaterna (M)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Moderaterna. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:9.
- **Sverigedemokraterna (SD)**: Bäckstedt, Felix & Richard Karlsson (2025). *Valet 2022 – Sverigedemokraterna. Partiets profil och väljarsammansättning*. Valforskningsprogrammets rapportserie 2025:10.

---

## Tabellförteckning

### 1. Hela väljarkårens uppfattning om partierna och partiledarna
| Tabell | Område och frågeställning | Fil |
| :--- | :--- | :--- |
| **A1** | Partiomdöme på skalan -5 (”Ogillar starkt”) till +5 (”Gillar starkt”) | [partiomdome_rd2022.md](partiomdome_rd2022.md) |
| **A2** | Partiledaromdöme på skalan -5 till +5 | [partiledaromdome_rd2022.md](partiledaromdome_rd2022.md) |
| **A3** | Placering av partierna på vänster–högerskalan (0–10) | [vanster_hoger_partier_rd2022.md](vanster_hoger_partier_rd2022.md) |
| **A4** | Placering av partiernas flyktingpolitik (0 restriktiv till 10 generös) | [flyktingpolitik_partier_rd2022.md](flyktingpolitik_partier_rd2022.md) |
| **A5** | Partiernas profilfrågor (vilka frågor partiet ansågs prioritera) | [profilfragor_partier_rd2022.md](profilfragor_partier_rd2022.md) |
| **A6a** | Bra politik på 18 olika politikområden | [brapolitik_partier_rd2022.md](brapolitik_partier_rd2022.md) |
| **A6b** | Dålig politik på 18 olika politikområden | [daligpolitik_partier_rd2022.md](daligpolitik_partier_rd2022.md) |

### 2. Partiväljarnas sammansättning, agerande och åsikter
| Tabell | Område och frågeställning | Fil |
| :--- | :--- | :--- |
| **A7** | Demografi (kön, ålder, inkomstkvintiler, yrkesgrupp, utbildningsnivå, boendeort) | [demografi_partivaljare_rd2022.md](demografi_partivaljare_rd2022.md) |
| **A8** | Politiska faktorer (politiskt intresse, förtroende för politiker, kunskap, självplacering vänster–höger) | [politiska_faktorer_rd2022.md](politiska_faktorer_rd2022.md) |
| **A9** | Partianhängarskap (starkt/svagt övertygad anhängare, oberoende, anhängare till annat parti) | [partianhangarskap_rd2022.md](partianhangarskap_rd2022.md) |
| **A10** | Röstningsagerande (beslutstidpunkt, röstningssätt samt personröstning) | [rostningsagerande_rd2022.md](rostningsagerande_rd2022.md) |
| **A11** | Skäl för partival (18 olika skäl: ideologi, kompetens, program, litet/stort parti m.m.) | [skal_for_partival_rd2022.md](skal_for_partival_rd2022.md) |
| **A12** | Viktiga frågor för partivalet (öppen fråga kodad i 22 sakområden) | [viktiga_fragor_rd2022.md](viktiga_fragor_rd2022.md) |
| **A13** | Framtida samhällsinriktningar (inställning till 14 olika samhällsmål/visioner) | [framtida_samhalle_rd2022.md](framtida_samhalle_rd2022.md) |
| **A14** | Politiska sakfrågor (inställning till 42 sakpolitiska förslag) | [sakfragor_rd2022.md](sakfragor_rd2022.md) |
