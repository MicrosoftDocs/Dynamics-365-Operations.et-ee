---
title: Store Commerce’i rakenduse funktsioonid
description: See artikkel kirjeldab funktsioone, mis on saadaval rakenduse Store Commerce rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2022-09-30
ms.openlocfilehash: 58f2ab1f913d3629de7971c8eeb2d1821161e44f
ms.sourcegitcommit: 29d9a7573bdac004726da88a9d7b2cc9c383e9ca
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/18/2022
ms.locfileid: "9788508"
---
# <a name="store-commerce-app-capabilities"></a>Store Commerce’i rakenduse funktsioonid

[!include [banner](includes/banner.md)]

Store Commerce’i rakendus on tänapäevane kassakogemus Microsoft Dynamics 365 Commerce. See võimaldab ettevõtetel töödelda kauplusekandeid ja hallata kontoris toiminguid, nt varusid ja tellimuste toiminguid. Rakendus võimaldab äril hallata kliendisuhteid püsikliendi ja klientrakendusega. 

Commerce Scale Uniti (CSU) toidena pakub Store Commerce’i rakendus täielikku kanalilahendust. Näiteks saab klient osta toodet võrgus ja võtta selle vastu lähedalasuvasse kauplusesse, jätkates seega oma ostuteed läbi kanalite ilma andmeid kaotamata. 

See artikkel annab ülevaate Store Commerce’i rakenduse võimalustest.

## <a name="platform"></a>Platvorm

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Kanal. | Dynamics 365 Commerce pakub laias laastmiskanali lahenduse, mis on ühene kontori-, kaupluse-, kõnekeskuse- ja digitaalkogemus. | [Ülevaade](index.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/dynamics-365-commerce-overview-november-2-2020) |
| Kaugadministreeritav Commerce | Commerce Scale Unit majutab peakontori ärimootorit. Peakontori mootor on keskne punkt kogu äriloogika ja äriloogika ning kogu ärikanali täieliku lahenduse läbi viimiseks. | <p>[Arhitektuuri ülevaade](commerce-architecture.md)</p><p>[Peakontori ülesehitus](dev-itpro/retail-server-architecture.md)</p> | [Tech](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-commerce-architecture-overview-december-4-2020) |
| Commerce Headquarters | Commerce headquarters pakub peakontori võimalusi, mis võimaldavad toodete, töötajate, äriprotsesside, hinnakujunduse ja muude äritegevuse jaoks vajalike funktsioonide konfigureerimist. | [Arhitektuuri ülevaade](commerce-architecture.md) | |
| Kassa | Store Commerce’i rakendus on kassakogemus Dynamics 365 Commerce. See pakub funktsiooni-rikast ja ulatuslikku müügikoha võimalusi, mis aitavad müügitöötajaid, kassapidajaid ja halduriid pakkuda kõrgemat klienditeenindust. Lisaks pakub see jaemüüjatele mitmeid juurutusvalikuid, aitab parandada jõudlust ja pakub rakenduse elutsükli halduse täiustatud haldust (SALVESTATUD). | [Store Commerce App](dev-itpro/store-commerce.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/modernize-the-dynamics-365-commerce-in-store-technology-using-the-new-store-commerce-app-march-30-2022)</p><p>[Video](https://youtu.be/7B332XH_zfs)</p><p>[Siirdamine MPOS-ist kaupluse ärisse](dev-itpro/pos-extension/migrate-mpos-store-commerce.md)</p> |
| Pilvjuurutus | Koormuse ja asukoha läheduse jaoks saab juurutada mitu Commerce Scale Unitsi eksemplari. | [Pilvejuurutus](../fin-ops-core/dev-itpro/deployment/cloud-deployment-overview.md) | |
| Ettevõttes olevad juurutused | Kasutades kohaliku äriandmete juurutamist, võivad Commerce’i kliendid omada suuremat omavastutust ja Dynamics 365 keskkondade haldust. | [Asutusesisene juurutus](../fin-ops-core/dev-itpro/deployment/deploy-retail-onprem.md) | |

## <a name="device-management"></a>Seadmehaldus

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Mitu vormitegurit | Programmi Store Commerce rakendust toetab mitu seadme vormitegurit, nt arvutid, tahvelarvutid ja mobiilsed seadmed. Rakenduste kasutajaliidese (UI) abil saab kavandi suurust automaatselt muuta ja korrigeerida vastavalt ekraani suurusele. | [Visuaalsed konfiguratsioonid](pos-screen-layouts.md) |  |
| Platvormiülene | Programmi Store Commerce rakendust toetatakse veebis, Windowsis, iOS-is ja platvormides Android . | [Platvormid](dev-itpro/hybridapp.md) | |
| Kaubamärgi kasutamine | Ekraani kujundaja võimaldab teil ekraanipaigutusi kohandada nii, et need vastaksid teie äritegevuse nõuetele. Lisaks saab töötaja rollide põhjal luua kujundusi, kujundusi, värve ja pilte ning seejärel saab neid kaubamärgi ühtsuse ja kasutus lihtsustamise jaoks jagada kõigi kasutajate vahel. | [Visuaalsed konfiguratsioonid](pos-screen-layouts.md) | [Video](https://www.youtube.com/watch?v=ldqCw2wf5fY) |
| Topoloogia | Toetatud on erinevad kaupluses olevad topologid, mis põhinevad võrgu saadavusel. | <p>[Topoloogia](dev-itpro/retail-modern-pos-architecture.md)</p><p>[Teabegraafiline](dev-itpro/retail-in-store-topology.md)</p> | |
| Mitme seadme haldus | Mitut kauplust üle kogu kaupluse saab hõlpsalt hallata commerce headquartersi kaudu. | [Aktiveerimine](set-up-activation-accounts-validate-devices-hq.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/commerce-mass-deployment-with-sccm-system-center-configuration-manager-october-6-2022) |

## <a name="employee-management"></a>Töötajate haldus

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Sisselogimine | Igal kaupluse töötajal võib olla eraldi sisselogimine. Sisselogimistüübid hõlmavad kasutajanime, vöötkoodi, magnetribalugejat (MSR), biomeetrilisi andmeid ja Azure Active Directory (Azure AD). | <p>[Azure AD](aad-pos-logon.md)</p><p>[Laiendatud sisselogimine](extended-logon.md)</p> | |
| Õigused | Töötajatele toetatakse õiguste erinevaid tasemeid, nt tellimuste loomise luba ja tellimuste redigeerimise õigust. | [Õigused](tasks/create-pos-permission-groups.md) | |
| Kellaaja ja kohalviibimise haldus | Kohalolekut saab hallata kellafunktsiooni abil. Kohaloleku andmeid saab rakenduse abil palgaarvestusse Dynamics 365 Human Resources töödelda. | [Ajahaldus](retail-time-attendance.md) | |
| Müügi komisjonitasu | Müügiesindaja võib jälgida müüke, et arvutada komisjonitasusid või muid preemiaid. | [Komisjonitasu](pos-sales-groups-track-commissions.md) | |

## <a name="merchandising"></a>Kaubastamine

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Sortimendi haldus | Tootejuhid saavad tooteid sortida nii, et nad on müügiks kindlas kanalis ja kindlal perioodil. | [Sortimendid](assortments.md) | |
| Kataloogid | Tootejuhid saavad hallata katalooge, et tuvastada tooteid, mida soovite kataloogipõhise hinnakujundusega pakkuda. | [Kataloogid](/dynamicsax-2012/appuser-itpro/about-retail-product-catalogs) | |
| Toote- ja kategooriahaldus | Tootejuhid saavad Commerce Headquartersis luua tooteid, mille atribuudid on variandid, mõõtühik jne. Samuti võivad nad määratleda kategooriahierarhia toodete korraldamiseks. | [Toode](retail-hierarchies.md) | |
| Kogumid | Tootejuhid saavad tooteid grupeerida nii, et neid müüakse kogumisse või komplektina. | [Komplektid](/dynamicsax-2012/appuser-itpro/about-setting-up-retail-product-kits) | |
| Teabekoodid | Teabekoodide abil saate kassapidajalt kassas erinevate toimingute (nt kauba müük, kauba tagastused või kliendi valimine) käigus teavet sisestada. | [Teabekoodid](/dynamicsax-2012/appuser-itpro/about-info-codes-retail) | |
| Lingitud kaubad | Lingitud kaupade abil saate tooteid üles müüa, kui kaup lisatakse kandesse. | [Lingitud kaubad](/dynamicsax-2012/appuser-itpro/set-up-products-for-cross-selling-and-up-selling) | |
| Garantiid | Laiendatud garantiisid saab müüa koos toodetega. | [Garantii](extended-warranty.md) | |
| Sildi printimine | Silte saab luua, mis sisaldavad tooteteavet (nt partiinumber, seerianumber ja aegumiskuupäev). | [Sildi printimine](/dynamicsax-2012/appuser-itpro/create-and-print-labels-overview) | |

## <a name="assisted-selling"></a>Abiline müük

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Toodete sirvimine | Sirvida tooteid kategooria alusel. | [Tootehierarhia](retail-hierarchies.md) | |
| Toote otsing | Otsige tooteid nime järgi ja täpsustage otsingud, kasutades tooteatribuudid nagu kaubamärk, hind ja materjal. Seda võimsust kasutab Azure’i cotive otsing. | [Pilve powered otsing](cloud-powered-search-overview.md) | |
| Leht Toote üksikasjad | Rikas toote üksikasjade leht võib sisaldada pilte, kirjeldust, toote atribuute ja soovitatud tooteid. Soovitused on soovituste teenuse toide. | | |
| Toote võrdlus | Saate võrrelda mitut toodet ja aidata klientidel valida ühe ja lisada need kandesse. | | |
| Lõpplaos | Saate hõlpsalt otsida teiste kaupluste kaubavarusid ja luua tellimusi. | [Otsing varudest](pos-inventory-lookup-operation.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Soovitused | Toodete üles müümine ja edasi müümine soovituste teenuse abil. Teenus kasutab patenteeritud tehnoloogiat soovituste soovitamiseks, mis põhinevad ostutrenditel ja omadustel, nagu näiteks uuesti saabunud, sarnane väljaminek ja hinnatud. Need soovitused on saadaval toote üksikasjade lehtedel, kliendi **üksikasjade** lehel ja kannete **lehel** . | [Soovitused](product-recommendations.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-recommendations-march-2-2021) |

## <a name="customer-relationship"></a>Kliendisuhe

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Klientide haldus | Saate luua, redigeerida ja hallata kliendikontosid. Kliendikontosid saab reaalajas töötlemise vältimiseks hallata asynci režiimis. | [Haldamise](customer-mgmt-stores.md) | |
| Kliendi atribuudid | Kliendi atribuutide raamistik võimaldab hõivata täiendavad kliendiga seotud andmed ärinõuete alusel. | [Atribuudid](dev-itpro/customer-attributes.md) | |
| Kliendi üksikasjade leht | Rikas kliendi üksikasjade leht pakubkirjet kliendi suhtluse kohta kõigis kanalites. Need suhtlused hõlmavad oste, soovinimekirju ja boonuspunkte. | | |
| Pilvepõhine kliendiotsing | Otsige kliente nime, telefoninumbri, meiliaadressi, kliendikaardi, aadressi jne järgi. | [Pilve powered otsing](pos-search-improvements.md#customer-search) | |
| Püsikliendid ja preemiad | Kliendid saavad liituda püsikliendiprogrammiga ning teenida ja lunastada boonuspunkte läbi kanalite. | [Püsiklient](set-up-customer-loyalty-program.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5c2wW) |
| Kliendisuhtlus | Hallake võtmekliente, kasutades kliendiraamatut ning jälgige tegevusi ja märkmeid kliendiprofiilil. Dynamics 365 Customer Insights integratsioon lubab kaupluse töötajatel saada vihjeid iga kliendi järgmise parima tegevuse kohta. | [Kliendisuhtlus](clienteling-overview.md#activities-and-notes) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSP) |

## <a name="pricing-and-discounts"></a>Hinnad ja allahindlused

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Kaubanduslepped | Hinnakujundusjuhid saavad kasutada kaubandusleppeid kindlate hindade määratlemiseks, mis põhinevad kindlate klientide pikaajalistel müügilepingutel. | [Hinnakujundus](price-management.md)| [Video](https://www.youtube.com/watch?v=r2VD8IxHesM) |
| Müügilepingud | Hinnajuhid saavad kasutada müügilepinguid lepingupõhiste hindade määratlemiseks ettevõtete-põhises (B2B) äristsenaariumis. | [Hinnakujundus](price-management.md) | |
| Hinna korrigeerimised | Hinnakujundusjuhid saavad kasutada hinnakorrektsioonide võimalusi oma toodete aja jooksul hinnaalkirjade loomiseks, jälgimiseks ja haldamiseks. | [Hinna korrigeerimised](price-adjustments-discounts.md) | |
| Allahindlused | Hinnakujundusjuhid saavad erinevate kampaaniahindade käivitamiseks häälestada mitut tüüpi allahindlusi. Need allahindlused hõlmavad lihtsaid allahindlusi, koguse allahindlusi, läve allahindlusi, segamise ja sobitamise allahindlusi, maksevahendipõhiseid allahindlusi ja saadetise allahindlusi. | [Allahindlused](retail-discounts-overview.md) | |
| Kupongid | Hinnakujundusjuhid saavad häälestada kupongikoode või vöötkoode, linkida neid allahindlustega ja jaotada neid klientidele. Müügiesindajad saavad lisada müügikannetele kuponge või neid eemaldada. | [Kupongid](coupons.md) | |
| Hinnagrupid | Hinnajuhid saavad kasutada hinnagrupi võimalusi kontekstipõhiste hindade määratlemiseks kanalite, kataloogide, kuuluvuste või püsikliendi programmide alusel. | [Hinnakujundus](price-management.md) | |
| Saadaolevad kampaaniahinnad | Müügiesindajad saavad kergesti otsida saadaolevaid kampaaniahinnad kaupluses toodetele, kandele lisatud toodetele jne. | [Hinnakujunduse funktsioonid](pos-pricing-functions.md) | |
| Hinnakontrollid | Müügiesindajad saavad kiiresti kontrollida kaupluses toodete aktiivseid müügihindu. | [Hinnakujunduse funktsioonid](pos-pricing-functions.md) | |
| Hinnaalistused | Nõutavate õigustega müügiseosed saavad süsteemi konfigureeritud või arvutatud hinnad alistada. | [Hinnakujunduse funktsioonid](pos-pricing-functions.md) | |
| Käsitsi allahindlused | Nõutavate õigustega müügiesindajad saavad rakendada müügikandele või müügiridadele käsitsi allahindlusi. | [Hinnakujunduse funktsioonid](pos-pricing-functions.md) | |

## <a name="electronic-payments"></a>Elektroonilised maksed

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Deebet ja kreedit | Store Commerce’i rakendus toetab PayPali kaudu suuri krediit- ja deebetkaardimakseid Portaali makseportaali ja tellimuse täitmise kaudu. Maksete SDK võimaldab välislüüsiühendusi, mida toetavad sõltumatu tarkvara hankija (ISV) integratsioonid. | <p>[Adyen](dev-itpro/adyen-connector.md?tabs=10-0-23)</p><p>[Paypal](paypal.md)</p><p>[Maksed](payment-methods.md)</p> | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-configuration-february-9-2021)</p><p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-omni-channel-payment-overview-processing-february-4-2021)</p> |
| Digitaalse toe | Rakendus Store Commerce toetab makseid digitaalsete makseviiside kaudu, mis ei kasuta panga ID-koodi (BIN) vahemikke nagu tavalised kreedit- ja deebetkaardid. Makseviise saab vastendada digitaalsete maksetega, nt Sisestajaga. | [Rahakott](wallets.md) | |
| Kinkekaardi tugi | Panga ID-kood Dynamics 365 kinkekaart, salvestatud väärtuse lahendused (SVS) ja Givex kinkekaardid. Kinkekaarte saab tellimuses osta ja lunastada. | [Kinkekaardid](dev-itpro/gift-card.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/d365-commerce-internal-gift-cards-november-16-2021) |
| Fraud Protection | Dynamics 365 Fraud Protection aitab teil petturlikku tegevust vältida ja tuvastada kohad, kus pettus võib olla nimetamata. | [Kaitse pettuse eest](dev-itpro/dfp.md) | [Video](https://www.youtube.com/watch?v=j_1nEiq3LfM) |

## <a name="taxes-and-charges"></a>Maksud ja tasud

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Maksud | Rakendus Store Commerce toetab mitmeid kaudsete maksude tüüpe, nt käibemaksu, käibemaksu (VAT), kaupu ja teenuste maksu (GST), ühikupõhiseid tasusid ja kinnipeetavat maksu. | [Maksud](/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json) | |
| Tasud | Tasusid saab konfigureerida rea tasemel, päise tasemel automaatsete tasudena, kanali jne järgi. | [Tasud](omni-auto-charges.md) | |

## <a name="order-processing-and-fulfillment"></a>Tellimuse töötlemine ja täitmine

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Tellimuse loomine | Tellimust saab luua lähetamiseks või peale lähetusks lähedalasumis kauplusesse. Peale võtta saab ajapesasid. | [Ülevaade](customer-orders-overview.md) | |
| Tellimuse muutmine | Tellimust saab muuta, tagastada, tühistada jne. | <p>[Tühista](customer-orders-overview.md#cancel-a-customer-order)</p><p>[Tagastused](pos-returns.md)</p> | |
| Tellimuste otsing | Otsige ja filtreerige tellimusi tellimuspõhise teabe abil. | [Tellimuste otsing](enhancedorderrecall.md) | |
| Tellimuse atribuudid | Tellimuse atribuudi raamistik võimaldab täiendava tellimusega seotud teabe hõivamist ärinõuete alusel. | [Atribuudid](dev-itpro/order-attributes.md) | |
| Otsetarne | Kaubad saab hankijalt otsetarnele kliendi aadressile märkida. Seda nimetatakse ka otsetarneks. | [Otsetarne](/dynamics365/supply-chain/sales-marketing/tasks/ship-orders-direct-deliveries) | |
| Pakkumine | Kaupluse töötajad saavad luua klientidele pakkumisi ning määrata spetsiaalse hinna, käsitsi allahindlused ja pakkumise kehtivuse kuupäeva. | [Pakkumine](/dynamics365/supply-chain/sales-marketing/tasks/create-edit-sales-quotations) | |
| Täitmine | Kauplused saavad komplekteeritud, pakkida ja saata tellimusi. Saatelehte saab lisada lähetusvalmis pakenditele. | [Täitmine](order-fulfillment-overview.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/unlock-the-power-of-dynamics-365-commerce-supporting-buy-online-pickup-in-store-curbside-with-dynamics-365-commerce-pos-february-3-2021)</p> <p>[Video](https://www.microsoft.com/videoplayer/embed/RE5bRXE)</p>|
| Hajutatud tellimuste haldamine | Store Commerce’i rakendus toetab nutikat tellimuse täitmise optimeerimist, kus äristrateegiaid saab konfigureerida äri olemuse, kliendi tüübi, tellimuse päritolu ja tellimuse tarneviisi alusel. | [DOM](dom.md) | [Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bRYl)|

## <a name="inventory-management"></a>Varud

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Jaotus kesklaost | Jaotage vabade varude jaotus jaotus jaotuskeskusest mitmesse kauplusse või ladu. | [Jaotus kesklaost](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Ristlaadimine | Jaotada sissetulevatel ostutellimustel lao jaotust mitmesse kauplusse või ladu. | [Ristlaadimine](tasks/set-up-rules-parameters-cross-docking-buyers-push.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021) |
| Sissetulevad varud | Laovarud saab hankijalt vastu võtta ostutellimuse kaudu või üleviimistellimuse kaudu muust laost. Looge sissetulev ostutellimus või üleviimistellimuse taotlus. | [Sissetulev](pos-inbound-inventory-operation.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Väljaminevad varud | Saate üleviimistellimuse kaudu lähetada varud teise lattu ja luua väljamineva üleviimistellimuse taotluse. | [Väljaminev](pos-outbound-inventory-operation.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p>  <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Otsing varudest | Kontrollige kaupluste ja ladude toodete vaba kaubavaru ning kontrollige ladu, mis on saadaval lubaduse andmiseks (ATP) tulevastel kuupäevadel. | [Otsing varudest](pos-inventory-lookup-operation.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |
| Varude korrigeerimine | Korrigeerige ladu kaupluse lattu või sellest väljas, et need vastaksid kindlatele ärinõuetele ilma müüki, sissetulekut või ülelugemist ilma. | [Varude korrigeerimine](work-with-store-inventory.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p>|
| Laoinventuurid | Loendage füüsilised varud ja korrigeerige süsteemi raamatupidamislik laovaru nii, et need sobiksid sellega. | [Inventuur](work-with-store-inventory.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)<p> |
| Lao liikumine | Teisaldage varud kaupluse asukohtade vahel. | [Liikumine](work-with-store-inventory.md) | <p>[Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-dynamics-365-commerce---store-inventory-may-13-2021)</p> <p>[Video](https://www.microsoft.com/en-us/videoplayer/embed/RE5bMSx)</p> |

## <a name="financials"></a>Finantsid

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Sularahahaldus | Store Commerce’i rakendus toetab sularaha ja muude kaupluses määratud maksesüsteemide haldust. Lisaks saab vahetuse vastavusseviimist kaupluses lubada täpsemate sularahahalduse võimaluste jaoks. | [Sularaha](cash-mgmt.md) | |
| Finantsaruanded ja vastavusseviimine | Kaupluse sularaha- ja kandekanded kirjendatakse Commerce Headquartersis väljavõtte sisestusprotsesside kaudu. | [Väljavõtted](retail-statements.md) | |
| Tulu- ja kulukanded | Töödelge pisiraha kandeid kaupluses ja registreerige sissetulek, mis ei ole traditsioonilise, nt kaotatud ja leitud raha, teie äris oleva coffee shopi tulu jakandekandeid. | [Väljavõtted](retail-statements.md) | |
| Arve maksed | Saate hõivada maksete arveid. | [Arve](payinvoice.md) | |

## <a name="employee-productivity"></a>Töötaja tööviljakus

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Ülesande haldus | Looge ülesannete loendeid ja ülesandeid ning määrake need kauplustele ja töötajatele. Jälgige ülesannete olekut läbi kaupluste. Ladu on tõrgeteta Microsoft Teams integreerimine. | <p>[Ülesandehaldus](task-mgmt-overview.md)</p><p>[Microsoft Teams](commerce-teams-integration.md)</p> | [Video](https://www.youtube.com/watch?v=ES1whB4C2lU) |

## <a name="hardware-and-peripherals"></a>Riistvara ja välisseadmed

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Ühenda välisseadmed | Ühendage välisseadmed, nt printerid, sularahasahtlid, skannerid ja makseseadmed kassaterminaliga. | [Välisseadmed](retail-peripherals-overview.md) ||
| Jaga välisseadmeid | Kviitungiprintereid, sularahasahtliid ja makseseadmeid saab mitme terminali vahel jagada, ühendades need ühiskasutatava riistvarajaamaga. | <p>[Riistvarajaam](retail-peripherals-overview.md) ||
| Kassa ja välis simulaator | Perifeerne simulaator toetab stsenaariumite testimist, mis nõuavad tavaliselt kassa füüsilisi seadmeid. See sisaldab ka kassa simulaator, mida saab kasutada füüsiliste perifeerseadmete ühilduvuse testimiseks ilma kassa kliendi juurutamist nõudmata. | [Simulator](dev-itpro/retail-peripheral-simulator.md) | |

## <a name="receipts"></a>Sissetulekud

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Prindi sissetulekud | Erinevat tüüpi kviitungeid, nt müügikviitungeid, krediitkaardikviitungeid, kingikviitungeid ja arveid, saab printida vaikimisi või pärast kassapidaja kinnitust väljaregistreerimise ajal. Samuti saab neid töölehelt uuestiprintida. | [Printimine](receipt-templates-printing.md) | |
| Kviitungi saatmine meilitsi | Kviitungid saab kassast meilide teel saata pärast väljaregistreerimise lõpetamist. | [E-post](email-receipts.md) | |
| Sissetulekute kujundamine | Kaupluse kviitungeid saab kohandada nii, et nad kuvaksid andmeid ja paigutusi, mis sobivad jaemüüja ja kande tüübiga. Kviitungeid saab laiendada ka nii, et need näitavad kohandatud andmeid, mida jaemüüja nõutud on. | [Kujundus](receipt-templates-printing.md) | |

## <a name="offline-support"></a>Võrguühenduseta tugi

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Sujuv võrguühenduseta | Ladumatu võrguühenduseta võimaldab teil jätkata transactimist ka siis, kui Interneti-ühenduvus on piiratud või puudub. Andmee välistus aitab teil vähendada võrguühenduseta andmebaaside andmemahtu ja suurendada jõudlust. | [Ühenduseta](pos-operations.md) | |
| Jõudlusepõhine lülitus | Lülituge võrguühenduseta, kui tuvastati jõudluse ülesseadmine. | [Ühenduseta](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI) |
| Võrguühenduseta armatuurlaud | Võrguühenduseta **oleku** armatuurlaud näitab iga seadme võrguühenduseta olekut, tõrkeid ja andmete üksikasju. Seega on mitme seadme oleku haldamine lihtne. | [Ühenduseta](dev-itpro/implementation-considerations-offline.md) | [Video](https://youtu.be/sQU-2pgHToI)|

## <a name="extensibility"></a>Laiendatavus

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Commerce Headquarters | Äriprotsesse lisades või muutes saab äri peakontori lahendusi kohandada. Commerce headquarters toetab metaandmete ja koodipõhise laiendusmudeli kasutamist kohandatud funktsioonide lisamiseks. Seda saab hõlpsalt integreerida väliste lahendustega. | [Ülevaade](dev-itpro/extend-customer-cdx-package.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-unlock-the-power-of-dynamics-365-commerce-commerce-extensibility-overview-february-23-2021) |
| Peakontor | Extensible Lisamise API raamistikku saab kasutada äriloogika kohandamiseks ja lisamiseks. API-d, kus on nõudeohjureid ning eel triggeri ja päästikujärgseid laiendusmustreid. | [CsU](dev-itpro/retail-server-customer-consumer-api.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Äri SDK | Commerce SDK hõlmab koodi, koodinäidiseid, malle ja tööriistu, mida on vaja funktsioonide laiendamiseks või kohandamiseks Dynamics 365 Commerce . SDK avaldatakse GitHub-is erinevates hoidlates (taasposeerimisel), sõltuvalt laienduskomponentidest. | [SDK](dev-itpro/retail-sdk/sdk-github.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |
| Kassa | Rakendust Store Commerce saab rakenduse Commerce SDK laiendusfunktsiooni abil sõltumatult laiendada. Raamistik toetab kasutajakogemuse (UX), töövoogude ja äriloogika kohandamist. | [POS](dev-itpro/pos-extension/pos-extension-overview.md) | [Tech](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/techtalk-series-commerce-extensions) |

## <a name="reporting"></a>Aruandlus

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Müügiaruanded | Müügiaruanded töötajate, registri, makse tüübi, tagastuste, toote jms alusel on kaupluse juhatajatele saadaval. Juhatajad saavad neid aruandeid vaadata ja kasutada neid komisjonitasu eraldamiseks ja tootetrendide tuvastamiseks. | | |

## <a name="diagnostics"></a>Diagnostika

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Tegevusülevaated | Poe curated teenuse tervisekindluse ja jõudluse mõõdikutega on saadaval kliendi kordustellimuses Application Insights . Saadaval on täpsemad teatise- ja seirevõimalused. | | |
| Seisundikontroll | Kassaga ühendatud välisseadmete saadavust saab kontrollida tervisekontrolli toimingut käivitades. Üksikuid välisprobleeme saab seejärel parandada ja kontrollida. | [Seisundikontroll](pos-healthcheck.md) | [Video](https://www.youtube.com/watch?v=RfPDNmnqYvY) |

## <a name="globalization"></a>Globaliseerimine

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Mitme turu tugi | Turuspetsiifilisi funktsioone, nagu fiskaalintegratsioon, GST, täpsem arveldamine ja ettemaksed, toetatakse väljast. See võimalus katab mitut euroopa turud, Ameerikat, Venemaad, Aasiat, Saudi-Araabiat jne. | [Globaliseerimine](localizations/fiscal-integration-for-retail-channel.md) | |

## <a name="compliance"></a>Vastavus

| Võimalus | Kirjeldus | Dokumentatsioon | Lisasisu |
|---|---|---|---|
| Microsofti standardid | Rakendus Store Commerce vastab Microsofti standardile turvalisuse, privaatsuse, juurdepääsu, üldise andmekaitse määruse (GDPR), Euroopa Liidu (EL) andmepiiri jms osas. | | |

