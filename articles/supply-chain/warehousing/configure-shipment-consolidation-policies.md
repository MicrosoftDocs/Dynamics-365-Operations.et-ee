---
title: Saadetise konsolideerimispoliitikate konfigureerimine
description: Selles teemas selgitatakse, kuidas seadistada vaikimisi ja kohandatud saadetise konsolideerimispoliitikaid.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, TMSMode, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 51e66cf025db06d9864ce78ba4118dc95f401acb2d1654fcf785a5649629b7f9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735916"
---
# <a name="configure-shipment-consolidation-policies"></a>Saadetise konsolideerimispoliitikate konfigureerimine

[!include [banner](../includes/banner.md)]

Saadetise konsolideerimisprotsess, mis kasutab saadetise konsolideerimispoliitikaid, lubab automatiseeritud saadetise konsolideerimist automaatsel ja käsitsi väljastamisel lattu. Pärast selle funktsiooni sisselülitamist peate konfigureerima oma algsed poliitikad. Kui ühtegi poliitikat ei konfigureerita, loob iga müügirida eraldi saadetise, millel on üksik koormuse rida.

Selles teemas esitatud stsenaariumid näitavad, kuidas seadistada vaikimisi ja kohandatud saadetise konsolideerimispoliitikaid.

## <a name="turn-on-the-shipment-consolidation-policies-feature"></a>Saadetise konsolideerimispoliitikate funktsiooni sisselülitamine

> [!IMPORTANT]
> Selles teemas kirjeldatud [esimeses stsenaariumis](#scenario-1) seadistate esmalt lao, et see kasutaks varasemat saadetise konsolideerimise funktsiooni. Seejärel teete saadetise konsolideerimispoliitikad kättesaadavaks. Sedasi saate proovida, kuidas täiendamise stsenaarium töötab. Kui kavatsete kasutada esimese stsenaariumi läbimiseks demoandmete keskkonda, ärge lülitage funktsiooni enne stsenaariumi tegemist sisse.

Enne funktsiooni *Saadetise konsolideerimispoliitikad* kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Saadetise konsolideerimine*

## <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle teema iga stsenaarium viitab väärtustele ja kirjetele, mis kuuluvad Microsoft Dynamics 365 Supply Chain Managementile esitatud standardsete demoandmete hulka. Kui soovite kasutada siin esitatud väärtusi harjutuste tegemise ajal, veenduge, et töötate keskkonnas, kuhu on demoandmed installitud ja määrake enne alustamist juriidiliseks isikuks **USMF**.

## <a name="scenario-1-configure-default-shipment-consolidation-policies"></a><a name="scenario-1"></a>1. stsenaarium: saadetise vaikimisi konsolideerimispoliitikate konfigureerimine

Pärast funktsiooni *Saadetise konsolideerimispoliitika* sisselülitamist peate konfigureerima minimaalse arvu vaikepoliitikaid kahel juhul.

- Keskkonna täiendamisel, mis juba sisaldab andmeid.
- Täiesti uue keskkonna seadistamisel.

### <a name="upgrade-an-environment-where-warehouses-are-already-configured-for-cross-order-consolidation"></a>Keskkonna uuendamine, kus laod on juba konfigureeritud risttellimuste konsolideerimiseks

Selle protseduuri käivitamisel peaks funktsioon *Saadetise konsolideerimispoliitika* olema välja lülitatud, et simuleerida keskkonda, kus on juba üldist risttellimuste konsolideerimise funktsiooni kasutatud. Seejärel saate kasutada funktsioonihaldust selle funktsiooni sisselülitamiseks, et saaksite teada, kuidas häälestada saadetise konsolideerimispoliitikaid pärast täiendust.

Järgige neid etappe vaikimisi saadetiste konsolideerimispoliitikate seadistamiseks keskkonnas, kus laod on juba konfigureeritud risttellimuste konsolideerimiseks.

1. Avage **Laohaldus \> Seadistus \> Ladu \> Laod**.
1. Otsige loendist üles ja avage soovitud lao kirje (nt ladu *24* demoandmetes **USMF**).
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Määrake kiirkaardil **Ladu** suvandi **Konsolideeri saadetis lattu väljastamisel** väärtuseks *Jah*.
1. Korrake etappe 2– 4 kõigi teiste ladude puhul, kus konsolideerimist nõutakse.
1. Sulgege leht.
1. Kasutage [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsiooni *Saadetise konsolideerimispoliitikad* sisselülitamiseks. Tööruumis **Funktsioonihaldus** on selle funktsiooni nimeks *Saadetise konsolideerimine*.
1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**. Pärast funktsiooni sisselülitamist uue menüükäsu **Saadetise konsolideerimispoliitikad** kuvamiseks peate tõenäoliselt värskendama oma brauserit.
1. Järgmiste poliitikate loomiseks valige Toimingupaanil **Loo vaikeseadistus**.

    - Poliitika **CrossOrder** poliitika tüübi *Müügitellimused* jaoks (eeldusel, et teil on vähemalt üks ladu, mis on seadistatud varasema konsolideerimisfunktsiooni kasutamiseks)
    - Poliitika **Vaikimisi** poliitika tüübi *Müügitellimused* jaoks
    - Poliitika **Vaikimisi** poliitika tüübi *Edastuse väljaminek* jaoks
    - Poliitika **CrossOrder** poliitika tüübi *Edastuse väljaminek* jaoks (eeldusel, et teil on vähemalt üks ladu, mis on seadistatud varasema konsolideerimisfunktsiooni kasutamiseks)

    > [!NOTE]
    > - Mõlemad poliitikad **CrossOrder** kasutavad sama väljade kogumit varasema loogikana, välja arvatud tellimuse numbri välja. (Seda välja kasutatakse ridade konsolideerimiseks saadetisteks, mis põhinevad sellistel teguritel, nagu ladu, transpordiliik ja aadress.)
    > - Mõlemad poliitikad **Vaikimisi** kasutavad sama väljade kogumit varasema loogikana, sealhulgas tellimuse numbri välja. (Seda välja kasutatakse ridade konsolideerimiseks saadetisteks, mis põhinevad sellistel teguritel, nagu tellimuse number, ladu, tarne transpordiviis ja aadress.)

1. Valige poliitika **CrossOrder** poliitika tüübi *Müügitellimused* jaoks ja seejärel valige Toimingupaanil käsk **Päringu redigeerimine**.
1. Kontrollige, kas päringuredaktori dialoogiboksi loendis on laod, mille suvandi **Konsolideeri saadetis lattu vabastamisel** väärtuseks on seatud *Jah*. Sellisel juhul need kaasatakse päringusse.

### <a name="create-default-policies-for-a-new-environment"></a>Uue keskkonna vaikepoliitikate loomine

Järgige neid etappe uues keskkonnas saadetise vaikimisi konsolideerimispoliitikate seadistamiseks.

1. Kasutage [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsiooni *Saadetise konsolideerimispoliitikad* sisselülitamiseks, kui te veel pole seda teinud. Tööruumis **Funktsioonihaldus** on selle funktsiooni nimeks *Saadetise konsolideerimine*.
1. Avage jaotis **Laohaldus \> Seadistus \> Lattu väljastamine \> Saadetise konsoldeerimispoliitika**.
1. Järgmiste poliitikate loomiseks valige Toimingupaanil **Loo vaikeseadistus**.

    - Poliitika **Vaikimisi** poliitika tüübi *Müügitellimused* jaoks
    - Poliitika **Vaikimisi** poliitika tüübi *Edastuse väljaminek* jaoks

    > [!NOTE]
    > Mõlemad poliitikad **Vaikimisi** kasutavad sama väljade kogumit varasema loogikana, sealhulgas tellimuse numbri välja. (Seda välja kasutatakse ridade konsolideerimiseks saadetisteks, mis põhinevad sellistel teguritel, nagu tellimuse number, ladu, tarne transpordiviis ja aadress.)

## <a name="scenario-2-configure-custom-shipment-consolidation-policies"></a>2. stsenaarium: saadetise kohandatud konsolideerimispoliitikate konfigureerimine

Selles stsenaariumis näidatakse, kuidas seadistada saadetise kohandatud konsolideerimispoliitikaid. Kohandatud poliitikad toetavaid keerukaid ärivajadusi, kus saadetise konsolideerimine sõltub mitmest tingimusest. Selles stsenaariumis on hiljem iga näidispoliitika kohta toodud selle ärijuhtumi lühikirjeldus. Need näidispoliitikad tuleks seadistada sellises järjestuses, mis tagab päringute püramiidilaadse hindamise. (Teisisõnu, poliitikaid, millel on kõige rohkem tingimusei, tuleb hinnata kõrgeima prioriteediga.)

### <a name="turn-on-the-feature-and-prepare-master-data-for-this-scenario"></a>Funktsiooni sisselülitamine ja stsenaariumi jaoks koondandmete ettevalmistamine

Enne, kui saate selle stsenaariumi harjutusi läb teha, peate selle funktsiooni sisse lülitama ja valmistama ette koondandmed, mida on vaja filtreerimiseks, vastavalt järgmistes alamjaotistes kirjeldatule. (Need eeltingimused kehtivad teemas [Saadetise konsolideerimispoliitikate kasutamise näidisstsenaariumid](#example-scenarios) loetletud stsenaariumitele.)

#### <a name="turn-on-the-feature-and-create-the-default-policies"></a>Funktsiooni sisselülitamine ja vaikepoliitikate loomine

Saate kasutada funktsioonihaldust funktsiooni sisselülitamiseks, kui te pole seda veel sisse lülitanud ja luua [stsenaariumis 1](#scenario-1) kirjeldatud vaikimisi konsolideerimispoliitikaid.

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
1. Sulgege leht ja seejärel korrake etappe 4 ja 5 kliendi puhul, kelle konto number on *US-004*.

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

Tavaliselt saab seda ärijuhtumit lahendada [stsenaariumis 1](#scenario-1) loodud vaikepoliitikate abil. Kuid saate järgmiste etappide abil sarnaseid poliitikaid ka käsitsi luua.

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

Järgmised stsenaariumid illustreerivad, kuidas kasutada selle teema lugemise käigus loodud saadetise konsolideerimispoliitikaid. Iga stsenaarium selgitab saadetise konsolideerimisprotsessi, mis kasutab saadetise konsolideerimispoliitikaid automaatsel või käsitsi väljastamisel lattu.

- 1. stsenaarium: [saadetiste konsolideerimine, kui need on müügitellimuste automaatse väljastamise abil lattu väljastatud](../warehousing/consolidate-shipments-automatic.md)
- 2. stsenaarium: [saadetiste konsolideerimine, kui saadetise konsolideerimispoliitika alistatakse lattu väljastamise lehe kaudu](../warehousing/consolidate-shipments-release-to-warehouse-override.md)
- 3. stsenaarium: [saadetiste konsolideerimine, kasutades lattu väljastamist koorma planeerimise töölaua kaudu](../warehousing/consolidate-shipments-load-planning-workbench.md)
- 4. stsenaarium: [saadetiste konsolideerimine saadetise konsolideerimise töölaua abil](../warehousing/consolidate-shipments-manual-workbench.md)
- 5. stsenaarium: [saadetiste käsitsi konsolideerimine saadetiste konsolideerimise lehe kaudu](../warehousing/consolidate-shipments-manual-form.md)


## <a name="additional-resources"></a>Lisaressursid

- [Saadetise konsolideerimispoliitikad](about-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]