# Sundbusserne IT Infrastrktur
# Maj 2026.

Sundbussernes IT infrastruktur består I overskrifter af følgende systemer, som hver især er en del af den nuværende infrastruktur, nogle af tingene er kritiske/lovpligtige og andre er instrumentale i at relativt-få medarbejdere kan holde et overblik. 

Shopbox POS Systemet -eg. kasseapperaterne. Shopbox håndterer salg i SB både i land og på skibene. Alt salg der har varer associeret overførest øjeblikkeligt til Lagersystemet således at lagersystem altid er et øjebliksbillede af tilgængelige varer (tobak, shopvarer etc.). Dagsomsætning bliver samlet og overført til economics hver nat. Shopbox leveres af virksomeheden Shopbox.dk.

Lagersystemet (lager over alle told/frie varer, både på land og i skibene). Dette system, der hostes af Asvig er tæt integreret med både Shopbox og Econmics. Der ligger også funktionalitet rundt om lagersystem, eksempelvis bliver alle leverancer fra RFS automatisk lagerført (Automatisk lagermodtagelse fra RFS). RFS leverer hovedparten af varer til SB,  varer fra andre leverandører bliver håndteret at cateringafdelingen. Lagersystemet benyttes også som dataleverandør til Toldbog, kommerciel-rapportering og Sundbusbanken. Sundbus-Bank & kommerciel-rapport. er baseret på spreadsheets hvor data kommer fra Lagersystemet og Shopbox. Der er også udviklet Halvtimes-rapporter (moms fordeling DK/SE) som balacerer momsbetalingen mellem Danmark og Sverige. Dette ser dog ud til at være stoppet efter man har skiftet regnskabsleverandør.
Lagersystemet leveres af Asvig hvor det er hosted, bliver backed-up og serviceret.

Den nye billetautomat er en del af et sammenhængene billetsystem hvor billetsalg [kan] håndteres i lokalvaluta for både Helsingør og Helsingbørg. Ydermere er dette koblet sammen med webshoppen: book.sundbussenre.dk således at billetterne der udstedes både kommercielt og med hensyn til validering er samme model. Eg. kommercielt samlet alle betalinger for både billetautomat og webshop salg i ePay, og billetterne er samme "type" så når de skal verificeres gøres dette med samme funktionalitet. Billetsystemet er leveret af Asvig, som hoster server(ne), backer systemet op og administrerer samme. 
Betalingerne for Billetsystemet hånderes af henholdsvis ePay og Softpay.

Economics (Regnskabssystem) - Der er udviklet forskellige funktioner for integration, som overfører daglig omsætningen fra alle POS kasserne, websalg, billetsalg osv. til Economics.

Toldbøger / lagerkontrol (data), dette gøres via advancerede regneark udviklet af HFR, data til disse kommer fra henholdsvis shopbox og lagersystemet.

ISM / ISPS (systemer). Systemerne for både ISM og ISPS er udviklet af Honnimar og hosted i Microsoft 365. Dette projekt har været et udviklingsprojekt og implementeringen er langt, men der mangler områder som endnu ikke er færdig implementeret.

Videoovervågning (ISPS). Som krav for ISPS godkendelserne er videoovervågnigen en samlet overvågning hvor man via en APP kan se alle/nogle kameraer. Der er pt. ingen overvågning på Pernille og SB burde også udvide overvågningen på forskellige områder.

MiWire kommunikationen til/fra skibene. Dette system er også et delvis udviklingsprojekt hvor der har været et tæt samarbejde mellem MiWire og SB. Man burde overveje fremtiden for dette system. Enten skal det opdateres (komponenterne er for en dels vedkommende ret gamle), alternativt burde man overveje en sattelitløsnisng for specifikt Jeppe og Pernille da stabiliteten af MiWire er svingenede, omend der også er lange perioder hvor det har været stabilt. Systemet leveres MiWire som i Lyngby.

Infrastruktur på land & skibene. Dette er et projekt som blev startet på Jeppe i 2026, for at højne stabiliteten og opdatere en generel aldrene infrastuktur. Strategien har været at færdiggøre Jeppe (WIFI) og herefter Helsingør som er begyndt, men ikke fuldendt. 

Sharepoint, filer, emails etc. Alt dette kører Office365 (Microsoft) og er i dag håndteret af Asvig.

Backup af data, dette dækker alle systemer er hosted/håndteret af Asvig.

Domainnavne, websider etc. - Dette er desværre splitet mellem forskellige leverandører. Asvig har nogle af domainerne, Thorn har nogle og måske ligger der også nogle hos one.com

Fremtidige prioriteter: Afhængigt af strategien for rederiet, bør infrastrukturen i Helsingør og Helsingborg være prioriteter, da det lige nu giver daglige udfordringer for pernsonellet. Det er krydret med at internet forbindelserne i både Helsingør og Helsingborg ikke er særligt stabile (5G).




