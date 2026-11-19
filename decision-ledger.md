# J&J kozmetický salón: decision ledger (interné demo)

Dátum: 2026-11-19. Refero MCP nebol použitý, referencie sú z webového vyhľadávania a priamo otvorených webov.

## Brief

Navrhujem jednostránkový web pre malý kozmetický salón na sídlisku KVP v Košiciach, pre ľudí z okolia, mobil aj desktop.
Cieľ: zavolať a dohodnúť termín. Tón: osobný, čistý, sebavedomý, bez spa klišé.
Riziko: chýbajú overené ceny, hodiny a fotky, preto musí web pôsobiť hotovo aj s označenými ukážkovými položkami.
Čo si zapamätať: telefónne číslo je hlavný typografický prvok stránky.

## Referencie, ktoré som otvoril

| # | Web | Odkaz | Konkrétny vzor |
|---|-----|-------|----------------|
| 1 | Face Space, Albany NY | https://thefacespaceco.com/ | Sýty tmavý slivkový farebný blok položený vedľa veľkého detailu fotky; široko prestrkaný verzálkový sans ako wordmark v hlavičke; fotky v zaoblených dlaždiciach. |
| 2 | Spa by the Square, McDonough GA | https://spabythesquare.com/ | Hero nadpis vymenúva služby ako krátke vety s bodkou ("Laser Treatments. Chemical Peels. Facials."); pod ním lokalita jedným riadkom a jedno tlačidlo. Textový blok prekrýva obrázkovú plochu. |
| 3 | Lineage Skin & Hair Studio, NYC | https://lineagestudionyc.com/ | Cenník ako typografický riadok: NÁZOV, trvanie, cena v jednom riadku verzálkami, bez kariet. |
| 4 | Skin by Gabby | https://skinbygabby.com/ | Služby ako obyčajný zoznam (žiadne karty); prestrkané verzálkové štítky sekcií; tenká čierna linka pod hlavičkou. |
| 5 | Shannon Lee Esthetics, NYC | https://shannonleeesthetics.com/ | Jedno malé tlačidlo objednania priamo v hero a druhé stále v navigácii. |
| 6 | Semra DC | https://semradc.com/ | Výrazná CTA farba použitá len na tlačidle objednania; čierne pozadie hlavičky. |
| 7 | Foundry Salon (One Page Love, archív) | https://onepagelove.com/foundry-salon | Dlhý one-pager s kotvovou navigáciou pre malý kolektív. |

Galérie, cez ktoré som hľadal: colorlib.com/wp/esthetician-website-examples, onepagelove.com, awwwards.com (Hi, Skin, SOTD 2021: veľký verzálkový grotesk).

## Reference lock

- **Primárny smer:** Face Space. Svetlé plátno, jeden sýty slivkový blok ako nosič značky, sans písmo, prestrkané verzálky pre štítky.
- **Zachovať:** (1) slivková ako jediná silná farba, použitá na veľký blok s kontaktom a na hlavné tlačidlo; (2) sans grotesk s kontrastom váh, žiadny serif; (3) veľké obrazové plochy s pevným pomerom strán; (4) prestrkaný verzálkový wordmark textom.
- **Požičať len:** (a) zo Spa by the Square hero nadpis "Kozmetika. Čistenie pleti." ako vymenovanie služieb s bodkami; (b) z Lineage cenník ako riadky s linkami a cenou zarovnanou doprava.
- **Pravidlá rolí:** slivková = značka a hlavná akcia (Zavolať), nikdy nie dekor ani pozadie bežných sekcií. Žltý zvýrazňovač = výhradne štítok "ukážka" (anotácia pre majiteľa), nikde inde. Ružovkastá svetlá = len plocha placeholderov fotiek.
- **Médiá:** fotky nemáme. Placeholdery s pevným pomerom strán (4:5 hero, 3:2 v službách), jemný CSS vzor a popis "fotka salónu" s poznámkou, čo má byť na fotke. Mapa ako statický blok s mriežkou ulíc nakreslenou v CSS a odkazom na Mapy Google.
- **Odmietam:** krémovo-olivovú paletu, serif s kurzívou na jednom slove, mriežku kariet so službami, recenzie a hviezdičky, tmavý režim, fialovú/indigo, emoji ikony, ľavé farebné prúžky.
- **Tokeny:** pozadie #FBF8F6, text #1F1418, slivková #4A1D33 (hover #351424), placeholder plocha #EFE2E3, anotácia #F6E27A s textom #3A3000, linky #D9CDCF, radius 0 pre bloky a 999px len pre tlačidlá a štítok ukážka, bez tieňov.

## Decision ledger

| Rozhodnutie | Zdroj | Pravidlo / rola | Prečo |
|---|---|---|---|
| Svetlé plátno #FBF8F6, nie krémové | Face Space (svetlé plátno), anti-slop pravidlo | pozadie | Studenší, ružovkastý odtieň drží smer bližšie k slivkovej a mimo krémovej šablóny. |
| Slivková #4A1D33 ako jediná silná farba | Face Space | značka + CTA | Primárny smer, zachovaný sýty, nezmäkčený. |
| Písmo Instrument Sans (400 až 700) | Face Space, Hi, Skin (sans grotesk) | celé UI | Má latin-ext pre slovenskú diakritiku, kontrast váh namiesto dvoch rodín. |
| Prestrkané verzálky pre wordmark a štítky | Face Space, Skin by Gabby | wordmark, eyebrow štítky | Meno salónu textom, bez loga, podľa zadania. |
| Hero nadpis "Kozmetika. Čistenie pleti." | Spa by the Square | hero | Máme presne dve overené služby, vymenovanie je pravdivé a priame. |
| Telefónne číslo ako veľká typografia v slivkovom bloku | zadanie (tlačidlo Zavolať) + Face Space blok | hlavná akcia | Salón sa objednáva telefonicky; číslo je to, čo si má človek odniesť. Pamätný prvok stránky. |
| Zavolať v hero aj v hlavičke, na mobile pevná spodná lišta | Shannon Lee, Semra | CTA | Na mobile je hovor jeden ťuk z každého miesta stránky. |
| Služby ako zoznam s linkami, overené hore, ukážkové označené | Skin by Gabby | zoznam | Bez kariet, overené fakty oddelené od doplnkov. |
| Cenník ako riadky: názov, trvanie, cena vpravo | Lineage | cenník | Rýchle čítanie na mobile, žiadne karty ani tabuľka s rámikmi. |
| Štítok "ukážka" žltý zvýrazňovač | zadanie (viditeľné označenie) | len anotácia | Musí byť na prvý pohľad iný než značka, aby nikto nepovažoval ukážku za fakt. |
| Placeholdery fotiek s popisom a smerom | refero pravidlo o médiách, zadanie | médiá | Zachová kompozíciu bez sťahovania cudzích fotiek. |
| Mapa ako statický CSS blok + odkaz na Mapy Google | zadanie (bez embedu) | médiá | Bez externých skriptov, odkaz otvorí navigáciu. |
| Bez recenzií, hviezdičiek, citátov | zadanie | obsah | Nič neoverené. |
| Pätička "Ukážka webu od Esticode, nie je zverejnená." + noindex | zadanie | právne/etické | Web sa nesmie tváriť ako oficiálny. |

## Anti-averaging kontrola

- Slivková ostala sýta, nezjemnila sa do staroružovej. OK.
- Žiadny serif a žiadne zvýraznené slovo v nadpise. OK.
- Karty: žiadne. Služby, cenník aj hodiny sú riadky s linkami. OK.
- Jedna výrazná farba, jedna anotačná farba s presnou rolou. OK.
- Hero nie je "text vľavo, fotka vpravo" ako generický vzor: na desktope je fotka-placeholder vysoká 4:5 a slivkový blok s číslom ju prekrýva (vzor prekrytia zo Spa by the Square). OK.
