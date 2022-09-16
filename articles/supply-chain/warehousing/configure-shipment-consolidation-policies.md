---
title: Saadetise konsolideerimispoliitikate konfigureerimine
description: See artikkel selgitab, kuidas seadistada saadetise vaike- ja kohandatud konsolideerimispoliitikaid.
author: Mirzaab
ms.date: 09/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0312d425d2ebc5311e894030423a916b90f1881a
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427978"
---
# <a name="configure-shipment-consolidation-policies"></a>Saadetise konsolideerimispoliitikate konfigureerimine

[!include [banner](../includes/banner.md)]

Saadetise konsolideerimisprotsess, mis kasutab saadetise konsolideerimispoliitikaid, lubab automatiseeritud saadetise konsolideerimist automaatsel ja käsitsi väljastamisel lattu. Pärast selle funktsiooni sisselülitamist peate konfigureerima oma algsed poliitikad. Kui ühtegi poliitikat ei konfigureerita, loob iga müügirida eraldi saadetise, millel on üksik koormuse rida.

Selles artiklis esitatud stsenaariumid näitavad, kuidas seadistada vaike- ja kohandatud saadetise konsolideerimispoliitikaid.

> [!WARNING]
> Kui täiendate Microsofti Dynamics 365 Supply Chain Management süsteemi, kus olete kasutanud pärandsaadetiste konsolideerimise funktsiooni, võib konsolideerimine lõpetada töötamise nii, nagu te eeldate, kui te ei järgi siin antud soovitust.
>
> Tarneahela halduse installides, kus *saadetise* konsolideerimispoliitika funktsioon on välja lülitatud, lubate saadetise konsolideerimise **,** kasutades iga üksiku lao puhul sätet Konsolideeri saadetis vabastamisel lattu. See funktsioon on kohustuslik versiooni 10.0.29 puhul. Kui see on sisse lülitatud, **·** *muutub* säte Konsolideeri saadetis lattu vabastamisel peidetud ja funktsioon asendatakse selles artiklis kirjeldatud saadetise konsolideerimispoliitikatega. Iga poliitika kehtestab konsolideerimisreeglid ja sisaldab päringut selle poliitika rakendumise juhtimise kohta. Kui lülitate funktsiooni esimest korda sisse, ei määratleta saadetise konsolideerimispoliitikaid saadetise **konsolideerimispoliitikate lehel**. Kui poliitikaid pole määratletud, kasutab süsteem pärandkäitumist. Seetõttu järgib iga olemasolev ladu lao sätet **Konsolideeri saadetis lattu** vabastamisel, kuigi see säte on nüüd peidetud. Kuid pärast vähemalt ühe saadetise konsolideerimispoliitika loomist ei **ole laosätetes saadetise konsolideerimine enam mõjul ja poliitikad kontrollivad täielikult konsolideerimisfunktsioone**.
>
> Kui olete määratlenud vähemalt ühe saadetise konsolideerimispoliitika, kontrollib süsteem konsolideerimispoliitikaid iga kord, kui tellimus lattu välja lastakse. Süsteem töötleb poliitikaid, kasutades iga poliitika poliitika järjestamise väärtusega määratud **reitingut**. See rakendab esimest poliitikat, kus päring vastab uuele tellimusele. Kui ükski päringu ei ühti tellimusega, loob iga tellimuse rida eraldi saadetise, mis omab ühte koormarida. Seetõttu soovitame varuna luua vaikepoliitika, mis rakendub kõikidele ladudele ja gruppidele tellimuse numbri järgi. Andke sellele varupoliitikale kõrgeim **poliitika järjestuse** väärtus, nii et seda viimati töödeldakse.
>
> Pärandkäitumise loomiseks peate looma poliitika, mis ei grupeeri tellimuse numbri järgi ja sellel on päringukriteeriumid, mis hõlmavad kõiki asjakohaseid ladusid.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Saadetise konsolideerimispoliitikate funktsiooni sisselülitamine

Saadetise konsolideerimispoliitika *funktsiooni kasutamiseks* peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis *on*[vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides Funktsioonihalduse tööruumis saadetise konsolideerimispoliitika](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsiooni.

## <a name="set-up-your-initial-consolidation-policies"></a><a name="initial-policies"></a> Algsete konsolideerimispoliitikate häälestamine

Kui töötate uue süsteemi või süsteemiga, kus te olete saadetise *konsolideerimispoliitika* funktsiooni esmakordselt sisse lülitanud, järgige neid samme algse saadetise konsolideerimispoliitikate häälestamiseks.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Järgmiste poliitikate loomiseks valige Toimingupaanil **Loo vaikeseadistus**.

    - Poliitika, mille nimi *on Müügitellimuste* poliitika *tüübi vaikeväärtus*.
    - Poliitika, mille nimi on vaikimisi *probleemi* ülekandmise *poliitika* tüübi jaoks.
    - Poliitika, mille nimi on Üleviimise *väljaminek poliitika* tüübi *crossOrder*. (See poliitika luuakse ainult siis, kui teil oli vähemalt üks ladu, kus pärand **Konsolideeri saadetis lattu vabastamise sätte** lubamisel.)
    - Müügitellimuse poliitikatüübi jaoks *poliitika, mille nimi* on *CrossOrder*. (See poliitika luuakse ainult siis, kui teil oli vähemalt üks ladu, kus pärand **Konsolideeri saadetis lattu vabastamise sätte** lubamisel.)

    > [!NOTE]
    > - Mõlemad *CrossOrderi* poliitikad peavad sama väljade komplekti kui varasemat loogikat. Samas arvestavad nad ka tellimuse numbri välja. (Seda välja kasutatakse ridade konsolideerimiseks saadetisteks, mis põhinevad sellistel teguritel, nagu ladu, transpordiliik ja aadress.)
    > - Mõlemad *vaikepoliitikad* peavad sama väljade komplekti kui varasemat loogikat. Samas arvestavad nad ka tellimuse numbri välja. (Seda välja kasutatakse ridade konsolideerimiseks saadetisteks, mis põhinevad sellistel teguritel, nagu tellimuse number, ladu, tarne transpordiviis ja aadress.)

1. Kui süsteem on *loonud müügitellimuste poliitika* *tüübile crossOrderi* poliitika, valige see ja seejärel valige tegevuspaanil suvand Redigeeri **päringut**. Päringuredaktoris näete, milliste ladude puhul oli eelnevalt lubatud säte Konsolideeri saadetis **lattu** vabastamisel. Seetõttu kordab see poliitika teie eelnevaid sätteid nende ladude jaoks.
1. Kohandage uusi vaikepoliitikaid vastavalt vajadusele, lisades või eemaldades välju ja/või redigeerides päringuid. Saate lisada ka nii palju uusi poliitikaid, kui vaja. Näiteid, mis näitavad, kuidas oma poliitikaid kohandada ja konfigureerida, vaadake näite stsenaariumi selles artiklis allpool.

## <a name="scenario-configure-custom-shipment-consolidation-policies"></a>Stsenaarium: kohandatud saadetise konsolideerimispoliitikate konfigureerimine

See stsenaarium annab näite, mis näitab, kuidas seadistada kohandatud saadetise konsolideerimispoliitikaid ja seejärel katsetada neid demoandmete abil. Kohandatud poliitikad toetavaid keerukaid ärivajadusi, kus saadetise konsolideerimine sõltub mitmest tingimusest. Selles stsenaariumis on hiljem iga näidispoliitika kohta toodud selle ärijuhtumi lühikirjeldus. Need näidispoliitikad tuleks seadistada sellises järjestuses, mis tagab päringute püramiidilaadse hindamise. (Teisisõnu, poliitikaid, millel on kõige rohkem tingimusei, tuleb hinnata kõrgeima prioriteediga.)

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

See stsenaarium viitab väärtustele ja kirjetele, mis sisalduvad tarneahela [halduses](../../fin-ops-core/fin-ops/get-started/demo-data.md) antud standardsetes demoandmetes. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks *USMF*.

### <a name="prepare-master-data-for-this-scenario"></a>Valmista selle stsenaariumi jaoks ette koondandmed

Enne kui saate selles stsenaariumis teostada koormusi, peate valmistama ette koondandmed, mis on filtreerimiseks vajalikud, nagu kirjeldatud järgmistes alamjaotistes. (Need eeltingimused kehtivad ka stsenaariumide puhul, mis on loetletud [Näide stsenaariumid saadetise konsolideerimispoliitikate jaotise kasutamise](#example-scenarios) kohta.)

#### <a name="create-two-new-product-filter-codes"></a>Kahe uue tootefiltri koodi loomine

1. Avage jaotis **Laohaldus \> Häälestus \> Tootefiltrid \> Tootefiltrid** ja lisage kaks järgmist tootefiltrit.

    - Tootefilter 1.

        - **Filtri kood:** *Kergsüttiv*
        - **Filtri pealkiri:** *Kood 4*

    - Tootefilter 2.

        - **Filtri kood:** *Lõhkeaine*
        - **Filtri pealkiri:** *Kood 4*

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted**.
1. Avage toode, mille kaubakood on *M9200*. (Valitud toode peab olema lubatud täpsemate laoprotsesside \[WMS\] jaoks lubatud ja see toode peab olema eelnevalt lubatud WMS-protsesside jaoks demoandmetes **USMF**.)
1. Määrake kiirkaardi **Ladu** välja **Kood 4** väärtuseks *Kergsüttiv*.
1. Sulgege leht.
1. Avage toode, mille kaubakood on *M9201*. (See toode on ka eelnevalt lubatud WMS-protsesside jaoks demoandmetes **USMF**.)
1. Määrake kiirkaardi **Ladu** välja **Kood 4** väärtuseks *Lõhkeaine*.
1. Sulgege leht.

#### <a name="create-a-new-transportation-mode-of-delivery"></a>Uue transpordiliigi loomine

1. Tehke valik **Transpordi haldus \> Seadistus \> Vedajad \> Kättetoimetajad**.
1. Looge transpordiliik, mida kasutatakse konsolideerimise päringutes ja pange sellele nimeks *Lennutransport*.
1. Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Kättetoimetajad**.
1. Looge järgmiste sätetega vedaja.

    - **Kättetoimetaja:** *Lennutransport*
    - **Nimi:** *Lennutransport*
    - **Režiim:** *Lennutransport*

1. Lisage uue vedaja kiirkaardil **Teenused** järgmiste sätetega rida.

    - **Vedaja teenus:** *Õhk*
    - **Transpordiviis:** *Õhk*

1. Valige toimingupaanil nupp **Salvesta**.

    > [!NOTE]
    > Uue vedaja salvestamisel määratakse ruudustiku **Teenused** uue rea välja **Tarneviis** väärtuseks automaatselt *Airwa-Air*. Kui kasutate müügitellimuses tarneviisi *Airwa-Air*, kasutatakse seostatud saadetiste puhul transpordiliiki *Lennutransport*.

#### <a name="create-an-order-pool"></a>Tellimuse kaustade loomine

1. Avage jaotis **Müük ja turundus \> Seadistamine \> Müügitellimused \> Tellimuse kaustad**.
1. Looge tellimuse kaust, mida kasutatakse konsolideerimise päringu jaoks. Sellel tellimuse kaustal peaksid olema järgmised sätted.

    - **Kaust:** sisestage täisarv, mida ükski teine kaust veel ei kasuta.
    - **Nimi:** *ShipCons*

1. Avage jaotis **Müük ja turundus \> Kliendid \> Kõik kliendid**.
1. Avage klient, kelle konto number on *US-003*.
1. Määrake kiirkaardi **Müügitellimuse vaikendmed** väljale **Müügitellimuste kaust** äsja loodud tellimuse kaust.
1. Sulgege leht ja korrake seejärel samme 4 ja 5 kliendi puhul, kelle kontonumber on *US-004*.

### <a name="create-example-policy-1"></a>Näidispoliitika 1 loomine

Selles näites loote poliitika *Klient+režiim*, mida saab kasutada järgmise ärijuhtumi korral.

- Poliitika esitab päringu konkreetse kliendi konto (*US-001*) ja kindla tarneviisi (*Airwa-Air*) kohta.
- Avatud saadetistega konsolideerimine on välja lülitatud.
- Konsolideerimist tehakse tellimuse ID põhiselt. (Teisisõnu tehakse eraldi saadetised tellimuse, lao jne kohta.)

Järgige neid etappe selle ärijuhtumi jaoks saadetise konsolideerimispoliitika loomiseks.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Määrake välja **Poliitika tüüp** väärtuseks *Müügitellimused*.
1. Valige Toimingupaanil suvand **Uus**, et luua järgmiste sätetega poliitika.

    - **Poliitika nimi:** *CustomerMode*
    - **Poliitika kirjeldus:** *Kliendi konto ja tarneviis*

1. Jätke suvandi **Avatud saadetistega konsolideerimine** väärtuseks *Ei*.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardi **Konsolideerimise väljad** loendist **Järelejäänud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tarneviis*.
1. Valige nupp **Lisa** ![Pparem nool.](media/forward-button.png) Klõpsake , et teisaldada **valitud väli** loendisse .
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Otsige päringuredaktori dialoogiaknas vahekaardil **Vahemik** ruudustikust üles rida, kus välja **Väli** väärtuseks on seatud *Kliendi konto* ja seadke selle rea välja **Kriteeriumid** väärtuseks *US-001*.
1. Valige **Lisa**, et lisada ruudustikule järgmiste sätetega rida.

    - **Tabel:** *Tellimuse read*
    - **Tuletatud tabel:** *Tellimuse read*
    - **Väli:** *Tarneviis*
    - **Kriteeriumid:** *Airwa-Air*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.

> [!NOTE]
> Selle ärijuhtumi puhul ei konsolideerita kõigile tellimustele kliendi *US-001* tellimuse ridu, mis kasutavad tarneviisi *Airwa-Air*. See poliitika on mõeldud kasutamiseks kõige esimesena olukorras, kus selle kliendi jaoks konsolideeritakse kõik teiste tarneviiside saadetised.

### <a name="create-example-policy-2"></a>Näidispoliitika 2 loomine

Selles näites loote poliitika *Ohtlikud kaubad*, mida saab kasutada järgmise ärijuhtumi korral.

- Poliitika esitab päringu konkreetse filtri koodi (*ohtlik*) ja kindla tarneviisi (*Airwa-Air*) kohta.
- Avatud saadetistega konsolideerimine on sisse lülitatud.
- Konsolideerimist tehakse kõigile tellimustele. (Teisisõnu luuakse eraldi saadetised konto, lao jne kohta, kuid ainult päringus määratletud kaubagrupi piires.)

Järgige neid etappe selle ärijuhtumi jaoks saadetise konsolideerimispoliitika loomiseks.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Määrake välja **Poliitika tüüp** väärtuseks *Müügitellimused*.
1. Valige Toimingupaanil suvand **Uus**, et luua järgmiste sätetega poliitika.

    - **Poliitika nimi:** *Kauba tüüp*
    - **Poliitika kirjeldus:** *Sama tüüpi kauba konsolideerimine kõigis tellimustes*

1. Määrake suvandi **Avatud saadetistega konsolideerimine** väärtuseks *Jah*.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardi **Konsolideerimise väljad** loendist **Järelejäänud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tarneviis*.
1. Valige nupp **Lisa** ![Pparem nool.](media/forward-button.png) Klõpsake , et teisaldada **valitud väli** loendisse .
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Laiendage ja valige päringuredaktori dialoogiakna vahekaardil **Liitmised** puu valikut **Tabelid \> Koormuse üksikasjad**.
1. Valige **Lisa tabeli liitmine**.
1. Kuvatavate seoste ruudustikus otsige üles ja valige rida, kus välja **Seos** väärtuseks on seatud *Lao kaubakood (kaubakood)* ja seejärel valige **Vali**. 
1. Valige vahekaardil **Vahemik** suvand **Lisa**, et lisada ruudustikule järgmiste sätetega rida.

    - **Tabel:** *Lao kaubakood*
    - **Tuletatud tabel:** *Lao kaubakood*
    - **Väli:** *Kood 4*
    - **Kriteeriumid:** *Kergsüttiv*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.

> [!NOTE]
> Selle ärijuhtumi puhul konsolideeritakse kõik tellimuse read, kus kaubal on kindel filtri kood (st filtri kood, mille välja **Kood 4** väärtuseks on seatud *Kergsüttiv*), koos teiste sama tüüpi kaupadega kõigis tellimustes. Kui samal kontol, laol ja kaupade grupil on avatud saadetis, lisatakse sellele uued read.

### <a name="create-example-policy-3"></a>Näidispoliitika 3 loomine

Selles näites loote poliitika *Kliendi nõuded*, mida saab kasutada järgmise ärijuhtumi korral.

- Poliitika esitab päringu konkreetse kliendi konto kohta.
- Avatud saadetistega konsolideerimine on sisse lülitatud.
- Konsolideerimist tehakse kõigile tellimustele, kuid see põhineb kliendi ostutellimustel. (Teisisõnu grupeeritakse mitu tellimust saadetisteks sama kliendi ostutellimuse number ja lao põhjal.)

Järgige neid etappe selle ärijuhtumi jaoks saadetise konsolideerimispoliitika loomiseks.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Määrake välja **Poliitika tüüp** väärtuseks *Müügitellimused*.
1. Valige Toimingupaanil suvand **Uus**, et luua järgmiste sätetega poliitika.

    - **Poliitika nimi:** *CustomerOrderNo*
    - **Poliitika kirjeldus:** *Ridade konsolideerimine kliendi OT alusel*

1. Määrake suvandi **Avatud saadetistega konsolideerimine** väärtuseks *Jah*.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardi **Konsolideerimise väljad** loendist **Järelejäänud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Kliendi ostutellimus*.
1. Valige nupp **Lisa** ![Pparem nool.](media/forward-button.png) Klõpsake , et teisaldada **valitud väli** loendisse .
1. Valige loendist **Järelejäänud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tarneviis*.
1. Valige nupp **Lisa** ![Pparem nool.](media/forward-button.png) Klõpsake , et teisaldada **valitud väli** loendisse .
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Otsige päringuredaktori dialoogiaknas vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Kliendi konto* ja seadke selle rea välja **Kriteeriumid** väärtuseks *US-001*.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.

> [!NOTE]
> Selle ärijuhtumi puhul konsolideeritakse kõik tellimuse read, kus müügitellimustel on sama kliendi ostutellimuse number, üheks saadetiseks, sõltumata müügitellimuse numbrist. (Kliendi ostutellimuse numbrit kasutatakse kliendi ostutellimuse \[OT\] numbrina.) Kui samal kontol, laol ja kliendi ostutellimusel on avatud saadetis, lisatakse sellele uued read. Seda poliitikat saab kasutada juhul, kui klient saadab ühe päeva jooksul mitu täiendavat sama OT-numbriga tellimuse rida ja soovib kõik read üheks saadetideks grupeerida. (Teisisõnu koostatakse üks veokiri ja üks saateleht.)

### <a name="create-example-policy-4"></a>Näidispoliitika 4 loomine

Selles näites loote poliitika *Konsolideerimist lubavad kliendid*, mida saab kasutada järgmise ärijuhtumi korral.

- Poliitika esitab päringu kindla tellimuse kausta kohta, et tuvastada kliendid, kes lubavad konsolideeritud saadetisi.
- Avatud saadetistega konsolideerimine on välja lülitatud.
- Konsolideerimine toimub kõigis tellimustes väljade abil, mille valis vaikimisi poliitika CrossOrder (varasema märkeruudu **Konsolideeri saadetis lattu väljastamisel** kopeerimiseks).

- Saate müügitellimuses selle reegli alistada, valides mõne muu tellimuse kausta.

Järgige neid etappe selle ärijuhtumi jaoks saadetise konsolideerimispoliitika loomiseks.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Määrake välja **Poliitika tüüp** väärtuseks *Müügitellimused*.
1. Valige Toimingupaanil suvand **Uus**, et luua järgmiste sätetega poliitika.

    - **Poliitika nimi:** *Tellimuse kaust*
    - **Poliitika kirjeldus:** *Kõigi tellimuste konsolideerimine tellimuse kausta põhjal*

1. Jätke suvandi **Avatud saadetistega konsolideerimine** väärtuseks *Ei*.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardi **Konsolideerimise väljad** loendist **Järelejäänud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tarneviis*.
1. Valige nupp **Lisa** ![Pparem nool.](media/forward-button.png) Klõpsake , et teisaldada **valitud väli** loendisse .
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Valige päringu redaktori dialoogiboksis vahekaardil **Vahemik** suvand **Lisa**, et lisada järgmiste sätetega rida ruudustikule.

    - **Tabel:** *Müügitellimused*
    - **Tuletatud tabel:** *Müügitellimused*
    - **Väli:** *Kaust*
    - **Kriteeriumid:** *ShipCons*

1. Valige dialoogiboksi sulgemiseks suvand **OK**.

> [!NOTE]
> Selle ärijuhtumi puhul konsolideeritakse kõik tellimuse read, kus müügitellimused kuuluvad samasse tellimuse kausta, ühte saadetisse sama konto, lao ja transpordiliigi kõigi müügitellimuste jaoks. Tellimuse kausta asemel saate kasutada mis tahes muud välja, et eristada kliendigruppi ja kasutada vaikimisi müügitellimuse päist. Seda lähenemisviisi saate kasutada juhul, kui konsolideerimise vajadust juhib klient, mitte ladu. (Varasemas konsolideerimise loogikas juhtis konsolideerimise vajadust ladu.)

### <a name="create-example-policy-5"></a>Näidispoliitika 5 loomine

Selles näites loote poliitika *Konsolideerimist lubavad laod*, mida saab kasutada järgmise ärijuhtumi korral.

- Poliitika esitab päringu kindla tellimuse kausta kohta, et tuvastada laod, mis konsolideerivad saadetisi.
- Avatud saadetistega konsolideerimine on välja lülitatud.
- Konsolideerimine toimub kõigis tellimustes väljade abil, mille valis vaikimisi poliitika CrossOrder (varasema märkeruudu **Konsolideeri saadetis lattu väljastamisel** kopeerimiseks).

Tavaliselt saab seda ärijuhtumi käsitleda, kasutades vaikepoliitikaid [, mille lõite oma algse konsolideerimispoliitikate häälestamisel](#initial-policies). Kuid saate järgmiste etappide abil sarnaseid poliitikaid ka käsitsi luua.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Määrake välja **Poliitika tüüp** väärtuseks *Müügitellimused*.
1. Valige Toimingupaanil suvand **Uus**, et luua järgmiste sätetega poliitika.

    - **Poliitika nimi:** *Risttellimus*
    - **Poliitika kirjeldus:** *ristttellimuste konsolideerimine konkreetsete ladude puhul*

1. Jätke suvandi **Avatud saadetistega konsolideerimine** väärtuseks *Ei*.
1. Valige toimingupaanil nupp **Salvesta**.
1. Valige kiirkaardi **Konsolideerimise väljad** väljalt **Järelejäänud väljad** rida, mille välja **Välja nimi** väärtuseks on seatud *Tarneviis*.
1. Valige nupp **Lisa** ![Pparem nool.](media/forward-button.png) Klõpsake , et teisaldada **valitud väli** loendisse .
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Otsige päringuredaktori dialoogiaknas vahekaardil **Vahemik** üles rida, kus välja **Väli** väärtuseks on seatud *Ladu* ja seadke selle rea välja **Kriteeriumid** väärtuseks *61, 63*.
1. Valige dialoogiboksi sulgemiseks suvand **OK**.

### <a name="set-the-order"></a>Tellimuse määramine

Kui olete kõik oma poliitikad loonud, tuleb teil määrata nende rakendamise järjekord. Püramiidilaadse lähenemisviisi kasutamiseks, kus kõige suurema hulga tingimustega poliitikad hinnatakse kõige kõrgema prioriteediga, toimige järgmiselt.

1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Määrake välja **Poliitika tüüp** väärtuseks *Müügitellimused*.
1. Valige iga vasakus veerus loetletud poliitika ja seejärel kasutage Toimingupaani nuppe **Nihuta üles** ja **Nihuta alla**, et seada poliitikaid järgmisse järjestusse.

    1. CustomerMode
    1. Kauba tüüp
    1. CustomerOrderNo
    1. Tellimuse kaust
    1. Risttellimus
    1. Vaikimisi

## <a name="example-scenarios-of-how-to-use-shipment-consolidation-policies"></a><a name="example-scenarios"></a> Näidisstsenaariumid saadetise konsolideerimispoliitikate kasutamiseks

Järgmised stsenaariumid illustreerivad, kuidas kasutada saadetise konsolideerimispoliitikaid, mille selle artikli lugemise ajal lõite. Iga stsenaarium selgitab saadetise konsolideerimisprotsessi, mis kasutab saadetise konsolideerimispoliitikaid automaatsel või käsitsi väljastamisel lattu.

- 1. stsenaarium: [saadetiste konsolideerimine, kui need on müügitellimuste automaatse väljastamise abil lattu väljastatud](../warehousing/consolidate-shipments-automatic.md)
- 2. stsenaarium: [saadetiste konsolideerimine, kui saadetise konsolideerimispoliitika alistatakse lattu väljastamise lehe kaudu](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- 3. stsenaarium: [saadetiste konsolideerimine, kasutades lattu väljastamist koorma planeerimise töölaua kaudu](../warehousing/consolidate-shipments-load-planning-workbench.md)
- 4. stsenaarium: [saadetiste konsolideerimine saadetise konsolideerimise töölaua abil](../warehousing/consolidate-shipments-manual-workbench.md)
- 5. stsenaarium: [saadetiste käsitsi konsolideerimine saadetiste konsolideerimise lehe kaudu](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikate ülevaade](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
