# Sundbusserne IT Infrastruktur — Maj 2026

Sundbussernes IT infrastruktur består i overskrifter af følgende systemer, som hver især er en del af den nuværende infrastruktur. Nogle af tingene er kritiske/lovpligtige og andre er instrumentale i at relativt-få medarbejdere kan holde et overblik.

---

## Shopbox POS {#shopbox-pos}

Kasseapparaterne. Shopbox håndterer salg i SB både i land og på skibene. Alt salg der har varer associeret overføres øjeblikkeligt til Lagersystemet, således at lagersystem altid er et øjebliksbillede af tilgængelige varer (tobak, shopvarer etc.). Dagsomsætning bliver samlet og overført til Economics hver nat. Shopbox leveres af virksomheden Shopbox.dk.

## Lagersystem {#lagersystem}

Lager over alle told/frie varer, både på land og i skibene. Dette system, der hostes af Asvig, er tæt integreret med både Shopbox og Economics. Der ligger også funktionalitet rundt om lagersystemet, eksempelvis bliver alle leverancer fra RFS automatisk lagerført (automatisk lagermodtagelse fra RFS). RFS leverer hovedparten af varer til SB; varer fra andre leverandører bliver håndteret af cateringafdelingen.

Lagersystemet benyttes også som dataleverandør til Toldbog, kommerciel-rapportering og Sundbusbanken. Sundbus-Bank & kommerciel-rapport er baseret på spreadsheets hvor data kommer fra Lagersystemet og Shopbox. Der er også udviklet halvtimes-rapporter (momsfordeling DK/SE) som balancerer momsbetalingen mellem Danmark og Sverige. Dette ser dog ud til at være stoppet efter man har skiftet regnskabsleverandør.

Lagersystemet leveres af Asvig, hvor det er hosted, bliver backed-up og serviceret.

## Billetsystem {#billetsystem}

Den nye billetautomat er en del af et sammenhængende billetsystem hvor billetsalg kan håndteres i lokalvaluta for både Helsingør og Helsingborg. Ydermere er dette koblet sammen med webshoppen: book.sundbusserne.dk, således at billetter der udstedes både kommercielt og med hensyn til validering er samme model. Kommercielt samles alle betalinger for både billetautomat og webshop-salg i ePay, og billetterne er samme "type", så når de skal verificeres gøres dette med samme funktionalitet.

Billetsystemet er leveret af Asvig, som hoster server(e), backer systemet op og administrerer samme. Betalingerne for Billetsystemet håndteres af henholdsvis ePay og Softpay.

## Economics {#economics}

Regnskabssystem. Der er udviklet forskellige funktioner for integration, som overfører daglig omsætning fra alle POS-kasserne, websalg, billetsalg osv. til Economics.

## Toldbøger / lagerkontrol {#toldbøger}

Dette gøres via avancerede regneark udviklet af HFR. Data til disse kommer fra henholdsvis Shopbox og Lagersystemet.

## ISM / ISPS {#ism-isps}

Systemerne for både ISM og ISPS er udviklet af Honnimar og hosted i Microsoft 365. Dette projekt har været et udviklingsprojekt, og implementeringen er langt, men der mangler områder som endnu ikke er færdig implementeret.

## Videoovervågning (ISPS) {#videoovervågning}

Som krav for ISPS-godkendelserne er videoovervågningen en samlet overvågning, hvor man via en app kan se alle/nogle kameraer. Der er pt. ingen overvågning på Pernille, og SB burde også udvide overvågningen på forskellige områder.

## MiWire kommunikation {#miwire}

Kommunikation til/fra skibene. Dette system er også et delvist udviklingsprojekt, hvor der har været et tæt samarbejde mellem MiWire og SB. Man burde overveje fremtiden for dette system. Enten skal det opdateres (komponenterne er for en dels vedkommende ret gamle), alternativt burde man overveje en satellitløsning specifikt til Jeppe og Pernille, da stabiliteten af MiWire er svingende, omend der også er lange perioder hvor det har været stabilt. Systemet leveres af MiWire i Lyngby.

## Infrastruktur på land og skibene {#infrastruktur}

Dette er et projekt som blev startet på Jeppe i 2026 for at højne stabiliteten og opdatere en generel aldrende infrastruktur. Strategien har været at færdiggøre Jeppe (WiFi) og herefter Helsingør, som er begyndt men ikke fuldendt.

## Sharepoint, filer, emails (Office 365) {#office365}

Alt dette kører på Office 365 (Microsoft) og er i dag håndteret af Asvig.

## Backup af data {#backup}

Dette dækker alle systemer, hosted/håndteret af Asvig.

## Domænenavne og websider {#domæner}

Dette er desværre splittet mellem forskellige leverandører. Asvig har nogle af domænerne, Thorn har nogle, og måske ligger der også nogle hos one.com.

## Fremtidige prioriteter {#fremtid}

Afhængigt af strategien for rederiet bør infrastrukturen i Helsingør og Helsingborg være prioriteter, da det lige nu giver daglige udfordringer for personalet. Det er krydret med at internetforbindelserne i både Helsingør og Helsingborg ikke er særligt stabile (5G).


