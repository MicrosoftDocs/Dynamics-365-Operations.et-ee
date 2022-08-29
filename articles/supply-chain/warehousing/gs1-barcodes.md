---
title: GS1 vöötkoodid
description: See artikkel kirjeldab, kuidas seadistada GS1 vöötkoode ja QR-koode nii, et silte saab laos skannida.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: e1c1c274054ed1c14c9b3fc0595baa029bf3124d
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336361"
---
# <a name="gs1-bar-codes"></a>GS1 vöötkoodid

[!include [banner](../includes/banner.md)]

Laotöötajad peavad mobiilse seadme skanneri kasutamisel kauba, paleti või konteineri liikumise registreerimiseks täitma mitu ülesannet. Need ülesanded võivad hõlmata nii vöötkoodide skannimist kui ka teabe käsitsi sisestamist mobiilsesse seadmesse. Vöötkoodid kasutavad ettevõtteomast vormingut, mille määratlete ja haldate Microsoft Dynamics 365 Supply Chain Management abil.

GS1 vöötkoodid saadetisesiltide jaoks töötati välja globaalse standardi pakutavaks ettevõtetevaheliseks andmevahetuseks. Need on saadaval nii lineaarsetes (1D) sümbolites (vöötkoodide vormingutes), nagu GS1-128 ja 2D sümbolid, nagu GS1 DataMatrix ja GS1 QR-koodid. GS1 vöötkoodid mitte ainult ei kodeeritud *andmeid*, vaid lubavad kasutada ka rakenduse ID-de eelmääratletud loendit nende andmete tähenduse määratlemiseks. GS1-standard määrab andmevormingu ja erinevad andmed, mida seda saab kasutada kodeerimiseks. Erinevalt vanematest vöötkoodi standarditest võib GS1 vöötkoodil olla mitu andmeelementi. Seetõttu võib ühe vöötkoodi skannimine hõivada mitut tüüpi tooteteavet, nagu näiteks partiid ja aegumiskuupäeva.

GS1-tugi tarneahela halduses lihtsustab märgatavalt skannimisprotsessi ladudes, kus kaubaalused ja konteinerid on sildistatud vöötkoodide abil GS1-vormingus. Laotöötajad saavad kogu vajaliku teabe ekstraktida ühe GS1 vöötkoodi skannimisega. Eemaldades vajaduse teha mitu skannimist ja/või sisestada teavet käsitsi, aitavad GS1 vöötkoodid vähendada ülesannetega seostatud aega. Ühtlasi aitavad need ka parandada täpsust.

Logistikahaldurid peavad seadistama nõutava rakenduse identifikaatorite loendi ja seostama iga neist sobiva mobiilse seadme menüü-üksustega. Rakenduse identifikaatoreid saab seejärel kasutada läbi ladude globaalse sättena teisaldamisel ja pakkimisel. Seetõttu, on kõigil saadetise siltidel ühtne vorm.

Kui pole teisiti määratud, viitab *see* artikkel termini vöötkoodi abil nii lineaarsele (1D) vöötkoodile kui ka 2D-vöötkoodile.

## <a name="the-gs1-bar-code-format"></a>GS1 vöötkoodi vorming

GS1 üldspetsifikatsioonid määratlevad, milliseid sümboleid saab GS1 vöötkoodide puhul kasutada ja kuidas neid vöötkoodis kodeerida. Selles jaotises antakse lühike sissejuhatus artiklisse. Täielikku teavet vt [GS1 üldistest spetsifikatsioonidest](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf), mille avaldatakse GS1. GS1 spetsifikatsioonide dokumenti uuendatakse regulaarselt ja sellelt saadav teave on uuendatud GS1 üldiste spetsifikatsioonide väljaandega 22.0.

GS1 vöötkoodid kasutavad järgmisi sümboleid:

- **Lineaarne või 1D vöötkoodid** – GS1-128 ja GS1 DataBar
- **2D-vöötkoodid** – GS1 DataMatrix, GS1 QR-kood ja GS1 dotcode

Arvestage, et GS1-128-s on GS1-128 erimärgid, mis on tavalise koodi -128 lineaarse vöötkoodi, GS1 DataMatrixi ja GS1 QR-koodi erijuhtum. Erinevus GS1 versiooni ja mitte-GS1 versiooni vahel on erimärgi (FNC1) olemasolu vöötkoodi andmete esimese märgina. FNC1-märgi olemasolu näitab, et vöötkoodi andmeid tuleb tõlgendada vastavalt GS1-spetsifikatsioonile.

Vöötkoodi andmed koosnevad mitmest andmeelemendist, millest igaüks on identifitseeritud rakenduse ID abil välja alguses. Tavaliselt esitatakse andmed vöötkoodi all inim loetavas vormingus, kus rakenduse ID kuvatakse sulgudes. Näite leiate siit: `(01) 09521101530001 (17) 210119 (10) AB-123`. Vöötkood sisaldab kolme elementi:

- **Rakenduse ID 01** – kauba GS1 kaubanduses kohaldatav globaalne kaubakood (GTIN).
- **Rakenduse ID 17** – aegumiskuupäev.
- **Rakenduse ID 10** – partiinumber.

Iga elemendi puhul võib andmete pikkus olla kas eelmääratletud pikkus või muutuja pikkus. Rakenduskoodide fikseeritud loend on eelmääratletud pikkustega. Kõigil rakenduse ID-tel on muutuja pikkus ning GS1 rakenduse identifikaatorite loend määrab andme maksimaalse pikkuse ja vormingu. Näiteks rakenduse ID 01 eelmääratletud pikkus on 16 märki (kaks rakenduse koodi enda jaoks ja seejärel 14 GTIN-i jaoks) ning rakenduse koodil 17 on eelmääratletud pikkus kaheksa tähemärki (rakenduse ID enda jaoks kaks ja seejärel 6 kuupäeva jaoks). Rakenduse idendil 10 on rakenduse ID enda jaoks kaks numbrit ja seejärel kuni 20 tähe- ja numbrimärgi pikkune.

Kui elemendid on kokku pannakse, kui element järgneb muutuva pikkusega elemendile, peab kasutama eraldajamärki. See eraldaja võib olla kas FNC1 erimärk või grupieraldaja märk (prinditav märk, mille ASCII-kood on 29 ja kuueteistkümnendkood 1D). Eraldajat ei tohi kasutada pärast viimast elementi. Kuigi eraldajat ei tohiks kasutada ka pärast eelmääratletud pikkusega elemente, pole selle olemasolu kriitiline tõrge.

Eelmise näite vöötkoodi andmetes, mis sisaldavad rakenduse koode 01, 17 ja 10, kodeeritud andmed koodis -128, QR-koodis või DataMatrixi sümbolis, kodeeritud järgmiselt (rakenduse ID-d `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` näidatakse paksus kirjas). Hea tava on panna lõppu kõik muutuva pikkusega elemendid, et eemaldada vajadus lisagrupieraldaja märgi järgi. Vöötkoodil võib olla ka erinev elementide järjekord, kus eraldaja on kohustuslik. Siin on näide:`<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Kuupäevad ja kümnendarvud

Kuupäevad on alati esitatud *YYMMDD-vormingus*, kus aasta sajandik määratakse GS1 spetsifikatsioonidega. Esitada saab ainult neid kuupäevi, mis on 49 aastat minevikus kuni 50 aastat (praeguse aasta suhtes).

Mõned andmeelemendid sisaldavad kümnendarve. Näiteks rakenduse ID-d 3100, 3101, ... 3105 esindab netokaalu kilogrammides. Kuna nende rakenduse ID-de eelmääratletud pikkus on 10, on koguse jaoks saadaval kuus numbrit. Kümnendkoha asukoha saab määrata rakenduse ID viimase numbriga. Seetõttu võib seda rakenduse ID-deperet esindada ka *310n*. Kuna GS1-standard määrab, et kümnendkohast vasakul peab alati olema vähemalt üks number, on lubatud kõige rohkem viis komakohta.

Siin on mõned näited, mis *näitavad, kuidas 123456* arvu võib tõlgendada erinevate rakenduse identifikaatorite abil (kuvatud paksus kirjas):

- **`3100`**`123456`&rarr; 123456 (täisarv)
- **`3101`**`123456`&rarr; 12345.6 (üks komakoht)
- **`3102`**`123456`&rarr; 1234,56 (kaks komakohta)
- **`3103`**`123456`&rarr; 123.456 (kolm komakohta)
- **`3104`**`123456`&rarr; 12,3456 (neli komakohta)
- **`3105`**`123456`&rarr; 1.23456 (viis komakohta)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>GS1 vöötkoodide skannimine tarneahela halduses

GS1 vöötkoodide skannimiseks kasutavad laotöötajad skannerit, mis on mobiilsesse seadmesse loodud või sellega ühendatud. Seejärel edastab skanner skannitud vöötkoodi laohalduse mobiilirakendusele klaviatuuri sündmuste seeriana. Seda töörežiimi nimetatakse ka klaviatuuri *wedge* või *wedge*. Mobiilirakendus saadab vastuvõetud teksti nii, nagu see on tarneahela haldusse. Kui süsteem saab sisendandmeid, määrab see kõigepealt, kas andmed algavad ühe konfigureeritud eesliitega, mis näitab, et andmed on tegelikult GS1 vöötkood (vt [globaalse GS1](#set-gs1-options) suvandite jaotist). Kui skannitud andmed algavad ühega neist eesliidetest, kasutab süsteem GS1 parserit, et sõeluda andmeid ja ekstraktida üksikud andmeelemendid vastavalt nende rakenduse identifikaatoritele. Pärast andmete sõelumist sisestatakse skannitud andmed kas praegusele sisendväljale või mitmele väljale.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Vöötkoodiskanneri riistvara ja tarkvara konfigureerimine

Selleks, et tarneahela haldus GS1 vöötkoode õigesti ära tunda ja dekodeerida, peab riistvaraskanner või toetav tarkvara olema konfigureeritud sooritama järgmisi toiminguid:

- Lisage skannitud vöötkoodidele eesliide, et süsteem saaks GS1 vöötkoodi ära tunda.
- Saate teisendada prinditava ASCII-grupi eraldajamärgi (ASCII-kood 29 või kuueteistkümnendkood 1D) prinditavaks märgiks, nagu näiteks prinditav märk (~).

Ehkki saate skannitud vöötkoodile lisada mis tahes eesliite, on üks võimalus lisada ISO/IEC 15424 sümbolite identifikaator, *mida nimetatakse ka ASD-koodiks*. See kolmemärgiline `]` ID algab järgmisega, sel juhul on üks märk, mis tuvastab kasutatava sümbolioudu ja sellel on number, mida kasutatakse täiendava muutujana. Näiteks määrab AS-i `]C1` ID koodi 128 vöötkoodi (`C` märgi tõttu) `1` ning muutja määratleb, et andmete esimeses positsioonis on FNC1-märk. Teiseks on vöötkood `]C0` Code 128, mis on mis tahes muu märgiga kui andmete esimene tähemärk.

Järgmised viis sümbolite identifikaatorit vastavad GS1 vöötkoodile, mille rakenduse ID-elemendid on:

- `]C1`– kood 128 (`C`) koos FNC1 märgiga esimeses positsioonis (`1`), mida nimetatakse ka GS1-128;
- `]e0`: GS1 DataBar.
- `]d2`– DataMatrix (`d`) ECC 200 ja FNC1 esimesel positsioonil (`2`), mida nimetatakse ka GS1 DataMatrixiks.
- `]Q3`– QR-kood (`Q`) Mudeli 2 sümbol FNC1 esimeses positsioonis (`3`), mida nimetatakse ka GS1 QR-koodiks.
- `]J1`: GS1 DotCode.

Kui kasutate neid identifikaatoreid, nõuab mitte-GS1 vöötkoodide ühilduvus, et skannerid või skannimistarkvara oleks konfigureeritud eemaldama mis tahes identifikaatoreid, mis ei vasta GS1-koodidele. Näiteks kui skannite "tavalist" Koodi 39 vöötkoodi, `]A0` lisatakse eesliide. Kuna süsteem ei mõista seda eesliidet ühena GS1 eesliitest, tõlgendab see seda kui andmeid ja annab ootamatuid tulemusi.

> [!NOTE]
> Mugavuse tagamiseks eemaldavad laohalduse 2.0.17.0 ja hilisemad versiooniversioonid KÕIK MINGIDJUHTIMISSÜSTEEMI eesliited, mida eelmises loendis ei ole. Selline käitumine toetab juhtumeid, kus saate konfigureerida skannerit nii, et see lisaks KA PREFIX-eesliidet, kuid mitte soovimatud eesliited.

### <a name="single-and-multiple-field-scanning"></a>Ühe ja mitme välja skannimine

Kui andmed on vöötkoodist sõelutud, toidetakse need mobiilse seadme voo juhtelementidesse. On kaks meetodit, mida omakorda töödeldakse:

- **Ühe välja skannimine** – see meetod täidab ainult välja, mille jaoks vöötkoodi skanniti. Näiteks kui skannite `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`**vöötkoodi** kursori soovitud kaubaväljal, sisestatakse sellele väljale vöötkoodi GTIN`09521101530001`. Kui skannite sama vöötkoodi, kui kursor on **väljal Partii ID**, sisestatakse partiinumber `AB-123` vöötkoodilt. See režiim töötab kõigi voogude kõigi väljade puhul ja nõuab ainult üldise seadistuse GS1 konfigureerimist. Kui vöötkood sisaldab mitut elementi, tuleb seda siiski mitu korda skannida, kuna mobiilse seadme voogu sisestatakse korraga ainult üks vöötkoodi tükk. Seda käitumist kontrollib GS1 üldine seadistus, nagu on kirjeldatud jaotises [Üldise GS1 seadistuse sisseseadmine](#generic-gs1-setup).
- **Mitme välja skannimine** – see meetod täidab mitu välja, kui skannitakse üks vöötkood, lükates lisaandmed mobiilse seadme voo olekusse. Näiteks on poliitika konfigureeritud lükkama väljale rakenduse identifikaatorit 01 `ItemId` juhtelemendile ja rakenduse ID-sse 10`InventBatchId`. Kui skannite vöötkoodi `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, lükatakse mõlema muutuja andmed samaaegselt. Seetõttu ei küsi süsteem teilt voos kauba- ja/või partiinumbrit. Seda käitumist kontrollivad menüü üksustega lingitud GS1 poliitikad, [nagu on kirjeldatud jaotises Seadistage GS1 poliitikad mobiilse seadme menüü-üksuste jaoks](#policies-for-menus).

> [!WARNING]
> Vaikimisi GS1 poliitikaid on testitud töötama ilma ootamatu käitumiseta. Kuid menüü-üksustega lingitud GS1 poliitika kohandamine võib põhjustada ootamatut käitumist, sest voog ei pruugi eeldada, et teatud andmed on teatud ajal saadaval.

## <a name="turn-on-the-gs1-feature"></a>Funktsiooni GS1 sisselülitamine

Enne selle funktsiooni kasutamist tuleb see teie süsteemi jaoks sisse lülitada. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *GS1 vöötkoodide skannimine*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Lülitage GS1 vöötkoodide funktsiooni jaoks sisse täiustatud parser.

Kui kasutate GS1 vöötkoode, on *soovitatav lülitada sisse ka täiustatud parseri funktsioon GS1 vöötkoodide* funktsiooni jaoks. See funktsioon pakub GS1 vöötkoodi parseri täiustamist. See lisab järgmised parendused:

- Järgib GS1 üldspetsifikatsiooni algoritmi sümboliandmete sõelumiseks ja kontrollib, kas sümbolis esitatud andmed kehtivad vastavalt spetsifikatsioonile.
- See ei nõua ID väärtuse **maksimaalse** pikkuse seadistamist ja kasutab pikimat konfigureeritud rakenduse ID-st sobivat eesliidet.
- See võimaldab teil kümnendkoha rakenduse IDENTIFIKAATOReid hõlpsalt konfigureerida, kasutades tähtede *n* mis tahes arvule vastamiseks. Näiteks saate konfigureerida ainult ühe rakenduse ID (*310n*) eraldi rakenduse ID-de (*3101*, *3102*, *3103* jne) asemel.
- See parandab probleemi, kus valesti kodeeritud andmeid tõlgendatakse välja andmetena.
- See on eraldi klass, mida saab muudes kontekstides uuesti kasutada ja võimaldab laiendatavuspunkti kasutamist skannitud andmete manipuleerimiseks enne vooväljade sisestamist.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Globaalsete GS1-i suvandite seadistamine

**Warehouse management parameetrite** lehel on sätted, mis loovad globaalsed GS1-suvandid.

Globaalsete GS1 suvandite seadistamiseks toimige järgmiselt.

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Kiirkaardil **Vöötkoodid** määrake järgmised väljad:

    - **FNC1 tähemärk**, **andmematriksi** märk ja QR-koodi **märk – määratlege tähemärgid,** mida tuleb iga GS1 vöötkoodi tüübi puhul prefiksiks tõlgendada.
    - **Grupieraldaja** : määrake märk, mis asendab ASCII-grupi eraldaja märgi.
    - **Maksimaalne identifikaatori pikkus** – määrake rakenduse ID lubatud maksimaalne märkide arv. See väli pole nõutav, kui täiustatud *GS1 Parseri* funktsioon on teie süsteemi jaoks sisse lülitatud.

> [!NOTE]
> Eesliited ütleb süsteemile, et vöötkood on kodeeritud vastavalt GS1-standardile. Kuni kolme eesliite (**FNC1 märk**, **Andmemaatriksi märk** ja **QR-koodi märk**) ja saab kasutada üheaegselt erinevatel eesmärkidel.

## <a name="gs1-application-identifiers"></a>GS1 rakenduse identifikaatorid

GS1-vormingud mitte ainult ei kodeeri andmeid, vaid lubavad kasutada ka rakenduse identifikaatorite eelmääratletud loendit andmete tähenduse määratlemiseks. Logistikahaldurid peavad seadistama nõutava rakenduse identifikaatorite loendi ja seostama iga neist sobiva mobiilse seadme menüü-üksustega. Rakenduse identifikaatoreid saab seejärel kasutada läbi ladude globaalse sättena teisaldamisel ja pakkimisel. Seetõttu, on kõigil saadetise siltidel ühtne vorm.

Süsteem kasutab andmeid, eriti eelmääratletud rakenduse identifikaatoreid, et kehtestada reeglid, mida tuleks rakendada vastava skannitud teabe tükile.

Iga rakenduse identifikaator annab süsteemile signaali, et skannitud vöötkoodi järgnevaid märke tuleks käsitleda krüptitud teabe blokina. Rakenduse ID seadistus määrab, kuidas süsteem peaks vöötkoodi tõlgendama ja salvestama selle väärtusena süsteemis.

Logistikahaldurid saavad kasutada standardseid rahvusvahelisi rakenduse identifikaatoreid ja/või luua oma identifikaatoreid.

### <a name="load-the-standard-application-identifiers"></a>Laadi rakenduse standardsed identifikaatorid

Kiireks alustamiseks saate laadida ühiste rahvusvaheliste rakenduse idendifikaatorite loendi. Seejärel saate loendit vajaduse korral laiendada või redigeerida.

Rakenduse standardsete ID-de laadimiseks järgige neid samme.

1. Minge **Warehouse management \> seadistuse \> GS1 \> GS1 rakenduse identifikaatoritele**.
1. Valige toimingupaanilt suvand **Loo vaikeseadistus**.

> [!WARNING]
> **Vaikeseadistuse loomise** käsk kustutab kõik praegu määratletud rakenduse ID-d ja asendab need standardloendiga. Kuid pärast vaikeseadistuse laadimist saate loendit vastavalt vajadusele kohandada.

### <a name="set-up-custom-application-identifiers"></a>Kohandatud rakenduse ID-de loomine

Kui mõned või kõik rakenduse identifikaatorid, mida teie ettevõte kasutab, erinevad standardkomplektist, saate luua nullist või kohandada standardikomplekti vastavalt vajadusele.

Oma GS1 rakenduse identifikaatorite häälestamiseks ja kohandamiseks järgige neid samme.

1. Minge **Warehouse management \> seadistuse \> GS1 \> GS1 rakenduse identifikaatoritele**.
1. Järgige üht neist sammudest.

    - Uue identifikaatori loomiseks: valige toimingupaanilt suvand **Uus**.
    - Olemasoleva ID redigeerimiseks: valige ID ja seejärel valige tegevuspaanil käsk **Redigeeri**.

1. Seadke uue või identifikaatori jaoks järgmised väljad:

    - **Rakenduse identifikaator**– sisestage rakenduse ID-kood rakenduse identifikaatorisse. Tavaliselt on see kood kahekohaline täisarv, kuid see võib olla ka pikem. Kümnendkoha puhul näitab viimane number komakohtade arvu. Lisateabe saamiseks vaadake selle loendi hiljem märkeruudu **Koma** kirjeldust. *Kui GS1 vöötkoodide funktsiooni täiustatud parser* on lubatud, saate luua ühe rakenduse identifikaatori kõigi kümnendkoha variantide jaoks, *kasutades tähe n* rakenduse identifikaatori viimase märgina. Näiteks saate rakenduse iga komakohtade arvu (3101, 3102 *,* *3103* jne) jaoks rakenduse eraldi ID asemel konfigureerida ainult ühe rakenduse ID (*310n* *).*
    - **Kirjeldus** – sisestage identifikaatori lühikirjeldus.
    - **Fikseeritud pikkus** – märkige see ruut, kui selle rakenduse ID abil skannitud väärtustel on fikseeritud arv märke. Kui väärtuste pikkus on muutuv, tühjendage see ruut. Sellisel juhul peate määrama väärtuse lõpu, kasutades grupieraldaja märki, mille määrasite **Warehouse management parameetrite** lehel.
    - **Pikkus** - Sisestage maksimaalne märkide arv, mis võivad ilmuda selle rakenduse identifikaatori abil skannitud väärtustes. Kui ruut **Fikseeritud pikkus** on märgitud, eeldatakse täpselt seda märkide arvu.
    - **Tüüp** - valige väärtuse tüüp, mida selle rakenduse ID abil skannitakse (*numbriline*, *täht* või *kuupäev*). Lisateavet selle kohta, kuidas kuupäevad ja numbrid vöötkoodi andmetes on esitatud, vt jaotist Kuupäevad [ja kümnendarvud](#dates-and-decimal-numbers).
    - **Kümnendkoht** - Märkige see ruut, kui väärtus sisaldab kaudset kümnendkohta. Kui see ruut on märgitud, kasutab süsteem rakenduse ID viimast numbrit kümnendkohtade arvu määramiseks. Lisateavet selle kohta, kuidas kuupäevad ja numbrid vöötkoodi andmetes on esitatud, vt jaotist Kuupäevad [ja kümnendarvud](#dates-and-decimal-numbers).

> [!WARNING]
> Kuigi süsteem võimaldab **teil** seada märkeruudu Fikseeritud pikkus mis tahes rakenduse ID jaoks, tuleks seda kasutada ainult nende rakenduse ID-de alamkogumi jaoks, mille eelmääratletud pikkus on GS1 üldspetsifikatsioonide kohta. Täiustatud GS1 parser sisaldab juba kõikide rakenduse identifikaatorite loendit, mille pikkuseks on eelmääratletud pikkus.

> [!NOTE]
> Laohalduse **parameetrite** lehel määratud grupieraldaja väärtus on valikuline, kui rakenduse id abil jälgitav väärtus on **fikseeritud** pikkusega.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Üldise GS1 häälestuse häälestamine

Üldise GS1 häälestus loob ühiste vastenduste kogumi. Need vastendused vastavad igale mobiilirakenduse asjakohasele sisendväljale rakenduse identifikaatoriga, mis kontrollib, kuidas skannitud vöötkoodide väärtusi tuleb sellel väljal tõlgendada ja talletada. Vaikimisi kehtivad need sätted kõigi mobiilse seadme menüü-üksuste skannimise puhul. Ühe või mitme konkreetse välja koodi saab siiski üle kirjutada konkreetsele menüü üksusele määratud GS1 poliitikaga.

Üldise GS1 seadistusega saab korraga skannida ainult üht väärtust. Seega, kui soovite ühe skannimisega laadida mitu väljaväärtust, peate seadistama GS1 poliitika vastavatele menüü-üksustele.

Lisateavet GS1 poliitikate kohta leiate järgmisest jaotisest.

### <a name="load-the-standard-generic-gs1-setup"></a>Laadi standardne üldine GS1 häälestus

**GS1 üldine seadistus** leht võimaldab teil laadida standardse vastenduste komplekti mobiilse seadme väljade ja standardsete rakenduse identifikaatorite vahel, mille on loonud vaikeseadistus.

Üldise GS1 häälestuse loomiseks minge **Warehouse management \> seadistuse \> GS1 \> GS1 üldisesse seadistusse**. Seejärel valige käsk **Loo vaikeseadistus**, et määrata igale mobiiliseadme menüü-üksustes tavaliselt kasutatavale väljale automaatselt sobiv rakenduse ID.

> [!WARNING]
> Kui mõni üldine GS1 seadistus on juba olemas, kustutab **vaikeseadistuse** loomise käsk selle täielikult ja laadib standardseadistuse.

### <a name="customize-the-standard-generic-gs1-setup"></a>Kohandage standardset üldist GS1 häälestust

GS1 üldise seadistuse kohandamiseks järgige neid samme.

1. Minge **Warehouse management \> seadistuse \> GS1 \> GS1 üldine seadistus**.
1. Järgige üht neist sammudest.

    - Uue vastenduse loomiseks: valige toimingupaanilt suvand **Uus**.
    - Olemasoleva vastenduse redigeerimiseks: valige vastendamine ja seejärel valige tegevuspaanil käsk **Redigeeri**.

1. Seadke uue või valitud vastenduse jaoks järgmised väljad:

    - **Väli** - valige või sisestage mobiilirakenduse sisendväli, millele sissetuleva väärtus peaks olema määratud. Väärtus pole kuvatav nimi, mida töötajad näevad. Selle asemel on see võtme nimi, mis määratakse aluseks oleva koodi väljale. Vaikeseadistus annab väljade kogumi, mis on ilmselt kasulik, ning kaasab intuitiivsete võtmenimed igale väljale ja vastavad programmistatud funktsioonid. Teil võib siiski olla vaja oma arenduspartneritele teada saada õigeid valikuid oma rakendusse.
    - **Rakenduse ID** - valige rakendatav rakenduse ID, nagu määratud **GS1 rakenduse ID-d** lehel. Identifikaator määrab, kuidas tuleks vöötkoodi tõlgendada ja salvestada väärtusena nimelise välja jaoks. Pärast rakenduse ID valimist kuvatakse **Kirjeldus** väljal selle kirjeldust.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a> Saate häälestada GS1 poliitikaid mobiilse seadme menüü-üksusteks.

Standardi GS1 eesmärk on võimaldada töötajatel ühe vöötkoodi skannimisel laadida mitu väärtust. Selle eesmärgi saavutamiseks peavad logistikahaldurid seadistama GS1 poliitika, mis teavitab süsteemi mitme väärtusega vöötkoodide tõlgendamisest. Hiljem saate määrata poliitikad mobiilse seadme menüü-üksustele, et kontrollida, kuidas vöötkoodi tuleb tõlgendada, kui töötajad seda skannivad, kui nad kasutavad konkreetset menüükäsku.

Kui menüükäsu jaoks ei ole GS1 poliitikat määratud, saab süsteem hõivata ainult ühe väärtuse. See väärtus rakendatakse mobiilse rakenduse sisenditele, mis valitakse siis, kui töötaja skannib, nagu on määratud üldises GS1 häälestuses. Kui menüü üksusele on määratud GS1 poliitika, kasutab süsteem siiski üldist GS1 häälestust, et vastendada esimene vöötkoodi väärtus valitud väljale. Seejärel saab see hõivata lisaväljaväärtusi, nagu on määratud rakendatava poliitikaga.

### <a name="load-the-standard-specific-gs1-policies"></a>Laadi standardsed konkreetsed GS1-poliitikad

Kiireks alustamiseks saate laadida GS1 poliitikad. Seejärel saate poliitikaid vajaduse korral laiendada või redigeerida.

Rakenduse standardsete ID-de laadimiseks järgige neid samme.

1. Avage **Warehouse management \> Seadistus \> GS1 \> GS1 poliitika**.
1. Valige toimingupaanilt suvand **Loo vaikeseadistus**.

> [!WARNING]
> **Vaikeseadistuse loomise** käsk kustutab kõik praegu määratletud poliitikad ja asendab need standardse poliitikate seadistamisega. Kuid pärast vaikeseadistuse laadimist saate poliitikaid vastavalt vajadusele kohandada.

### <a name="set-up-custom-specific-gs1-policies"></a>Saate häälestada kohandatud konkreetseid GS1-poliitikaid

> [!WARNING]
> Mõned GS1 poliitikad ei pruugi töötada iga mobiilse vooga, mida kasutate. Kui konfigureerite kohandatud GS1-poliitikaid, peate testima mobiilse seadme voogu, kasutades erinevaid teabetükke, mida skannitakse voo erinevates punktides. Sel viisil saate määrata, kas voogu nigastatakse nii, nagu eeldate.

Oma GS1-poliitikate häälestamiseks ja kohandamiseks järgige neid samme.

1. Avage **Warehouse management \> Seadistus \> GS1 \> GS1 poliitika**.
1. Järgige üht neist sammudest.

    - Uue poliitika loomiseks: valige toimingupaanilt suvand **Uus**.
    - Olemasoleva poliitika redigeerimiseks: valige see poliitika loendipaanilt.

1. Määrake uue või valitud poliitika päises järgmised väärtused:

    - **Poliitika nimi** – sisestage poliitikale nimi.
    - **Kirjeldus** – sisestage poliitika lühikirjeldus.

1. Päise all oleval kiirkaardil vastendage väljade nimed rakenduse identifikaatoriga nagu praeguse poliitika puhul on nõutud. Kasutage järgmisi nuppe tööriistaribal, et lisada ja eemaldada kirjeid vastavalt vajadustele. Määrake igas reas järgmised väljad.

    - **Väli** - valige või sisestage mobiilirakenduse sisendväli, millele sissetuleva väärtus peaks olema määratud. Väärtus pole kuvatav nimi, mida töötajad näevad. Selle asemel on see võtme nimi, mis määratakse aluseks oleva koodi väljale. Vaikeseadistus annab väljade kogumi, mis on ilmselt kasulik, ning kaasab intuitiivsete võtmenimed igale väljale ja vastavad programmistatud funktsioonid. Teil võib siiski olla vaja oma arenduspartneritele teada saada õigeid valikuid oma rakendusse.
    - **Rakenduse ID** - valige rakendatav rakenduse ID, nagu määratud **GS1 rakenduse ID-d** lehel. Identifikaator määrab, kuidas tuleks vöötkoodi tõlgendada ja salvestada väärtusena nimelise välja jaoks. Pärast rakenduse ID valimist kuvatakse **Kirjeldus** väljal selle kirjeldust.
    - **Sortimine**– iga mitme väärtusega vöötkood hõlmab rakenduse identifikaatorite seeriat, millest igaühele järgneb väärtus. Rakendatav GS1 poliitika tuvastab, milline rakenduse identifikaator on vastendatud igale andmebaasi väljale. Siiski, kui vöötkood kasutab sama rakenduse ID-d rohkem kui üks kord, kasutab süsteem järjekorda, milles rakenduse ID-d ilmuvad koodis nende vastendamiseks väljadega. Ridade puhul, mis jagavad rakenduse ID-d ühe või mitme reaga, kasutage seda välja ühtivate ridade töötlemise järjestuse loomiseks. Esimesena töödeldakse rida, mille sortimisväärtus on madalaim.

> [!NOTE]
> Vöötkoodide puhul, mis sisaldavad rohkem kui üht ja sama rakenduse ID-d, *peate* kasutama **sortimisel** loomiseks sortimisvälja.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>GS1 poliitikate määramine mobiilse seadme menüü-üksustele

Vaikimisi annavad kõik mobiilse seadme menüü-üksused sisendväljad, kus töötajad saavad üldise GS1 häälestuse kohaselt skannida ühte väärtust. Kui soovite, et töötajad saaksid skannida ühe skannimisel mis tahes mobiilse seadme menüü-üksuse jaoks rohkem kui ühte välja väärtust, peate järgmiste sammude abil määrama GS1 poliitika.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Saate luua või avada menüükäsu.
1. Kiirkaardil **Üldine** seadke **GS1 poliitika** väli rakenduv poliitika menüü üksusele.

## <a name="gs1-setup-example"></a>GS1 seadistuse näide

See näide kehtib süsteemi kohta, kus GS1 valikud on seadistatud viisil:

- **Warehouse management parameetrite** lehel luuakse järgmised globaalsätted:

    - **FNC1 märk:** *\]C1*
    - **Grupi eraldaja:** *\~*

- **GS1 rakenduse ID-d** lehel on selle näite puhul asjakohased järgmised rakenduse ID-d.

    | Rakenduse identifikaator | Kirjeldus | Fikseeritud pikkus | Pikkus | Tüüp | Kümnendkoht |
    |---|---|---|---|---|---|
    | 1 | GTIN | Valitud | 14 | Numbriline | Tühjendatud |
    | 10 | Partii number | Tühjendatud | 20 | Tähtnumbriline | Tühjendatud |
    | 17 | Aegumiskuupäev | Valitud | 6 | Kuupäev | Tühjendatud |
    | 30 | Koguse vastuvõtmine | Tühjendatud | 8 | Numbriline | Tühjendatud |

- **Üldisel GS1 seadistus** lehel on selle näite puhul asjakohased üldise GS1 poliitika järgmised sätted.

    | Field | Rakenduse identifikaator | Kirjeldus |
    |---|---|---|
    | ItemId | 1 | GTIN |

- **GS1 poliitika** lehel on poliitika, kus **poliitika nime** väli on seatud väärtusele *Ostu vastuvõtmine*. Poliitika hõlmab järgmisi ridu.

    | Field | Rakenduse identifikaator | Kirjeldus | Sorteerimine |
    |---|---|---|---|
    | Aegumiskuupäev | 17 | Aegumiskuupäev | 0 |
    | InventariPartiiId | 10 | Partii number | 0 |
    | Kogus | 30 | Koguse vastuvõtmine | 0 |

- **Mobiilse seadme menüü-üksuste** lehel on menüü käsk nimega *Ostu vastuvõtmine*. Selle **GS1 poliitika** väli on seatud väärtusele *Ostu vastuvõtmine*.

Kui ostutellimuse kaubad on lattu saabunud, järgib töötaja neid samme.

1. Valige mobiilse seadme menüüelement **Ostu ladustamine**.
1. Sisestage ostutellimuse number.
1. Valige väli **Kaup** ja skannige järgmine vöötkood: `]C10100000012345678~3030~10b1~17220215`.

Selle näite jaoks loodud sätete tõttu sõelub süsteem skannitud vöötkoodi järgmisel viisil.

| Välja võti | Rakenduse ID | Väärtus | Paberraha |
|---|---|---|---|
| ItemId | 1 | 00000012345678 | Kuna töötaja skanniti väljale **Kaup**, vastendatakse vöötkoodi esimene väärtus selle väljaga. Vastendamine võetakse GS1 üldisest seadistusest. |
| Kogus | 30 | 30 | Kuna ühe skannimisega fikseeritakse mitu välja väärtust, võetakse see vastendamine ja kõik ülejäänud vastendamised GS1 poliitikast, mis on määratud menüükäsu **Ostu vastuvõtt**. See väärtus on saadud kogus. |
| InventariPartiiId | 10 | b1 | See väärtus on vaikesäte. |
| Aegumiskuupäev | 17 | 220215 | Kuupäevavorming on AAKKPP. Seepärast on aegumiskuupäev 15. veebruar 2022. |

Seejärel registreeritakse sissetulek ja pärast üksikut skannimist sisestatakse vastavad andmebaasi väärtused.
