---
title: Voo siltide uuesti printimine ja tühistamine
description: Selles teemas selgitatakse olemasolevate voo siltide tühistamist ja printimist.
author: GarmMSFT
manager: PJacobse
ms.date: 07/09/2020
ms.topic: reprint-and-void-wave-labels
ms.service: dynamics-ax-applications
ms.search.form: WHSWaveLabel, WHSWaveLabelTemplate, WHSWaveLabelLayoutRow, WHSWaveTableListPage, WHSWorkException, WHSMobileDisplayWaveLabelListLookup, WHSWaveLabelLayout, WHSWaveLabelType, WHSWaveLabelTemplateGroup
audience: Application User
ms.reviewer: PJacobse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-07-09
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: af92334af28824b3fcebde5f046bd7c6da459885
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016650"
---
# <a name="reprint-and-void-wave-labels"></a>Voo siltide uuesti printimine ja tühistamine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas hallata voo töötlemisel loodud silte. (Üksikasjaliku kirjelduse ja konfigureerimisjuhised leiate teemast [Voo sildi printimise konfigureerimine](../warehousing/configure-wave-label-printing.md).)

Voo silte saate igal ajal uuesti printida. Näiteks võib juhtuda, et peate printima üksiku sildi, kui olemasolev silt on kaotsi läinud või kahjustatud. Lao töötajal või järelevaatajal võib olla vaja tervet siltide rulli uuesti printida, kui terve voo siltide seeria number ja/või koosseis on muutunud (nt varude vähesuse tõttu või muudel põhjustel). Sageli tuleb terve rull uuesti printida isegi juhul, kui ainult pakkide arv on muutunud, et iga sildi jaotises „Pakk X/Y” oleks õige koguarv.

Voo siltide uuesti printimise funktsioon toetab järgmisi funktsioone.

- Saate printida silte uuesti nii laorakenduse kui ka rikka kliendi jaoks.
- Saate samaaegselt tühistada silte ja printida neid uuesti. (Siltide tühistamise võimalus on manustatud näiteks kiire komplekteerimise stsenaariumide puhul.)
- Voo siltide ajaloo puhastamine.

Selles teemas kirjeldatakse hulka stsenaariumeid, mis illustreerivad näidete abil, kuidas töötada voo siltide uuesti printimise funktsiooniga.

> [!IMPORTANT]
> Selles teemas esitatud stsenaariumidega töötamiseks peate esmalt sisse lülitama ja konfigureerima asjakohased voo printimise funktsioonid, mis on kirjeldatud teemas [Voo sildi printimise konfigureerimine](../warehousing/configure-wave-label-printing.md). Mitmed selle teema stsenaariumid nõuavad ka esmalt selle teema stsenaariumide läbitöötamist, et luua eeltingimuseks olevad näidisandmed.

## <a name="scenario-1-reprint-labels-from-the-web-client"></a>1. stsenaarium: siltide uuesti printimine veebikliendist

Saate kuvada ja uuesti printida järgmiste lehtede voo silte. Valige iga lehe toimingupaani vahekaardil **Saadetised** grupis **Seotud teave** suvand **Voo sildid**.

- Kõik saadetised \> Saadetise üksikasjad
- Kõik koormused \> Koormuse üksikasjad
- Kõik vood
- Voo sildid
- Voosildi ajalugu

Voo sildi uuesti printimiseks veebikliendist, toimige järgmiselt.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige voog, kust soovite silte uuesti printida.
1. Valige roimingupaani vahekaardil **Voog** grupis **Printimine** suvand **Voo sildid**.
1. Järgige üht või mõlemat järgmistest etappidest.

    - Sildi uuesti printimiseks valige printer väljal **Printeri nimi**. (Jätke see väli tühjaks, kui soovite lihtsalt uuendada voo sildi üksikasju ilma silti uuesti printimata.)
    - Sildi värskendamiseks märkige ruut **Värskenda voo sildi üksikasju**. (Jätke see märkeruut tühjaks, kui soovite eelmist silti uuesti printida.)

    > [!NOTE]
    > Iga kord, kui voo silti prinditakse või uuesti prinditakse, teisendatakse selle andmed vastava voo sildi paigutuse kaudu ja kõik kohatäited asendatakse tegelike väärtustega. Tulemuseks olev string talletatakse voo sildi ajaloo kirjena. Kui märkeruut **Värskenda voo sildi üksikasju** on tühjendatud, kasutatakse sildi uuesti printimisel salvestatud Zebra programmeerimiskeelt (ZPL). Kui märkeruut **Värskenda voo sildi üksikasju** on märgitud, luuakse uus string. Olemasolevad voo sildid arvutatakse samuti ümber ja üleliigsed sildid (nt kui seotud tööread on tühistatud või muudetud) on märgitud **Tühistatuks** ja neid ei prindita uuesti.

1. Valiku kinnitamiseks valige **OK**.

## <a name="scenario-2-reprint-labels-from-the-warehousing-app"></a>2. stsenaarium: siltide uuesti printimine laorakendusest

See stsenaarium kehtib tavaliselt siis, kui terve siltide rull on kadunud või kahjustatud. Siin on esitatud näide, kuidas häälestada mobiilse seadme menüü-üksuseid, mis võimaldavad töötajatel printida ühte ja mitut silti uuesti. Seejärel näidatakse, kuidas kasutada neid uusi menüü-üksuseid mobiilse seadmega töötades.

### <a name="set-up-the-required-menu-items-and-menu-for-the-mobile-device"></a>Mobiilse seadme jaoks vajalike menüü-üksuste ja menüü seadistamine

Enne, kui töötajad saavad silte mobiilse seadme abil uuesti printida, peate seadistama menüü-üksused selle funktsiooni pakkumiseks ja seejärel lisama need üksused laorakenduse menüüsse.

#### <a name="create-new-mobile-device-menu-items"></a>Uute mobiilse seadme menüü-üksuste loomine

Järgige neid etappe, et luua uus menüü-üksuste kogum siltide uuesti printimiseks laorakendusest.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Looge menüü-üksus ja seadke sellele järgmised väärtused.

    - **Menüü-üksuse nimi:** *Ühe voo sildi uuesti printimine*
    - **Pealkiri:** *Ühe voo sildi uuesti printimine*
    - **Režiim:** *Kaudne*
    - **Tegevuse kood:** *Ühe voo sildi uuesti printimine*

1. Looge teine menüü-üksus ja seadke sellele järgmised väärtused.

    - **Menüü-üksuse nimi:** *Siltide uuesti printimine (kaup)*
    - **Pealkiri:** *Voo siltide uuesti printimine (kaup)*
    - **Režiim:** *Kaudne*
    - **Tegevuse kood:** *Mitme voo sildi uuesti printimine*
    - **Kuva tööloendi grupeerimise filter:** *Jah*
    - **Süsteemi grupeerimise väli:** *ShipmentID*
    - **Süsteemi grupeerimise silt:** *Saadetise ID*
    - **Printimisrežiim:** *Toode*

1. Valige toimingupaanil **Väljaloend** , et avada leht, kus saate valida kuvatavad väljad, mis aitavad töötajatel õiget siltide rulli tuvastada.
1. Saate kuvada kuni seitset välja. Kasutage ripploendit, et valida igas saadaolevas kohas kuvatav väli. Jätke tühjaks väljad, mida te ei vaja. 

    Siin on näide.

    - **Kuva väli:** *LabelItemId*
    - **Kuva väli 2:** *LabelItemName*
    - **Kuva väli 3:** *InventQty*
    - **Kuva väli 4:** *LabelUnitId*

1. Sulgege leht.
1. Looge kolmas menüü-üksus ja seadke sellele järgmised väärtused.

    - **Menüü-üksuse nimi:** *Siltide uuesti printimine (loetelu)*
    - **Pealkiri:** *Voo siltide uuesti printimine (loetelu)*
    - **Režiim:** *Kaudne**
    - **Tegevuse kood:** *Mitme voo sildi uuesti printimine*
    - **Kuva tööloendi grupeerimise filter:** *Jah*
    - **Süsteemi grupeerimise väli:** *ShipmentID*
    - **Süsteemi grupeerimise silt:** *Saadetise ID*
    - **Printimisrežiim:** *Loetelu*

1. Valige toimingupaanil **Väljaloend** ja seejärel kasutage ripploendit, et valida kuvatavad väljad, mis aitavad töötajatel õiget siltide rulli tuvastada (nt *LabelItemId* , *LabelItemName* , *InventQty* , *LabelUnitId* ja *NumberOfLabels* ).
1. Sulgege leht.
1. Looge neljas menüü-üksus ja seadke sellele järgmised väärtused.

    - **Menüü-üksuse nimi:** *Siltide uuesti printimine (viimase järgi)*
    - **Pealkiri:** *Voo siltide uuesti printimine (viimase järgi)*
    - **Režiim:** *Kaudne*
    - **Tegevuse kood:** *Mitme voo sildi uuesti printimine*
    - **Kuva tööloendi grupeerimise filter:** *Jah*
    - **Süsteemi grupeerimise väli:** *ShipmentID*
    - **Süsteemi grupeerimise silt:** *Saadetise ID*
    - **Printimisrežiim:** *Viimase hea voo sildi ID*

1. Valige toimingupaanil **Väljaloend** ja seejärel kasutage ripploendit, et valida kuvatavad väljad, mis aitavad töötajatel õiget siltide rulli tuvastada (nt *LabelItemId* , *LabelItemName* , *InventQty* , *LabelUnitId* ja *NumberOfLabels* ).
1. Sulgege leht.

#### <a name="set-up-the-mobile-device-menu"></a>Mobiilse seadme menüü seadistamine

Järgige neid etape oma uute menüü-üksuste lisamiseks laorakenduse menüüsse.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige olemasolev menüü **Väljaminev**.
1. Otsige vasakpoolsest loendist üles äsja loodud uuesti printimise menüü-üksused ja kasutage seejärel paremnoole nuppu, et lisada need parempoolsesse loendisse.
1. Sulgege leht.

### <a name="use-cases"></a>Kasutusjuhtumid

Siin toodud kasutusjuhtumid annavad näiteid, mis illustreerivad, kuidas kasutada erinevaid mobiilse seadme menüü-üksusi, mille seadistasite, et võimaldada töötajatel voo silte uuesti printida.

Enne nende kasutusjuhtumite läbi töötamist, peavad olema täidetud järgmised eeltingimused.

- Demoandmed peavad olema installitud ja peate valima juriidilise isiku **USMF**.
- Voo sildi printimine peab olema konfigureeritud ja tuleb luua mõned sildid jaotises [Voo sildi printimise konfigureerimine](../warehousing/configure-wave-label-printing.md) kirjeldatud juhiste järgi.

#### <a name="use-case-21-a-single-wave-label-is-scratched-and-must-be-reprinted"></a>Kasutusjuhtum 2.1: ühe voo silt on kriimustatud ja tuleb uuesti printida.

1. Logige laorakendusse sisse kasutajana, kellel on juurdepääs laole *62*. (Standardsete demoandmete korral saate logida sisse, kasutades kasutaja ID-na *62* ja paroolina *1*.)
1. Avage jaotis **Väljaminev \> Ühe voo sildi uuesti printimine**.
1. Sisestage või skannige voo sildi ID.
1. Valige printer, miga soovite uuesti printida.
1. Valige tegevuse kinnitamiseks **OK**.

#### <a name="use-case-22-several-labels-for-boxes-of-the-same-item-were-damaged-and-must-be-reprinted-each-label-has-a-product-bar-code-but-no-enumeration-or-sscc-number"></a>Kasutusjuhtum 2.2: sama kauba kastide mitu silti on kahjustatud ja tuleb uuesti printida. Igal sildil on toote vöötkood, kuid loetelu või SSCC-number puudub.

1. Logige laorakendusse sisse kasutajana, kellel on juurdepääs laole *62*. (Standardsete demoandmete korral saate logida sisse, kasutades kasutaja ID-na *62* ja paroolina *1*.)
1. Avage jaotis **Väljaminev \> Siltide uuesti printimine (kaup)**.
1. Sisestage või skannige saadetise ID.
1. Valige õige sildiga paan, millelt uuesti printida.
1. Skannige olemasolevalt sildilt toote vöötkood, et kinnitada õige rea valik.
1. Sisestage uuesti prinditavate siltide arv.
1. Valige printer, miga soovite uuesti printida.
1. Valige tegevuse kinnitamiseks **OK**.

#### <a name="use-case-23-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-because-the-labels-have-enumeration-you-can-define-the-carton-range-to-reprint"></a>Kasutusjuhtum 2.3: kastide jaoks ei prinditud mitut silti printeriummistuse tõttu. Kuna siltidel on loetelu, saate määrata uuesti prinditavate pakkide vahemiku.

1. Logige laorakendusse sisse kasutajana, kellel on juurdepääs laole *62*. (Standardsete demoandmete korral saate logida sisse, kasutades kasutaja ID-na *62* ja paroolina *1*.)
1. Avage jaotis **Väljaminev \> Siltide uuesti printimine (loetelu)**.
1. Sisestage või skannige saadetise ID.
1. Valige õige sildiga paan, millelt uuesti printida.
1. Sisestage esimene pakk, mille silti soovite uuesti printida.
1. Sisestage viimane pakk, mille silti soovite uuesti printida. Võite selle välja ka tühjaks jätta, et printida uuesti kõik esimesele määratleud pakile järgnevate pakkide sildid.
1. Valige printer, miga soovite uuesti printida.
1. Valige tegevuse kinnitamiseks **OK**.

#### <a name="use-case-24-several-labels-for-boxes-werent-printed-because-of-a-printer-jam-the-last-good-label-has-a-wave-label-id-that-is-printed-as-a-bar-code"></a>Kasutusjuhtum 2.4: kastide jaoks ei prinditud mitut silti printeriummistuse tõttu. Viimasel heal sildil on voo sildi ID, mis prinditakse vöötkoodina.

1. Logige laorakendusse sisse kasutajana, kellel on juurdepääs laole *62*. (Standardsete demoandmete korral saate logida sisse, kasutades kasutaja ID-na *62* ja paroolina *1*.)
1. Avage jaotis **Väljaminev \> Siltide uuesti printimine (viimase järgi)**.
1. Sisestage või skannige saadetise ID.
1. Valige õige sildiga paan, millelt uuesti printida.
1. Sisestage või skannige viimase hea voo sildi voo sildi ID. Rakendus tuvastab seeria järgmise sildi esimese pakina, mille silti uuesti printida.
1. Sisestage viimane pakk, mille silti soovite uuesti printida. Võite selle välja ka tühjaks jätta, et printida uuesti kõik esimesele määratleud pakile järgnevate pakkide sildid.
1. Valige printer, miga soovite uuesti printida.
1. Valige tegevuse kinnitamiseks **OK**.

## <a name="scenario-3-short-pick-and-reprint"></a>3. stsenaarium: kiire komplekteerimine ja uuesti printimine

Enne nende selle stsenaariumi läbi töötamist, peavad olema täidetud järgmised eeltingimused.

- Demoandmed peavad olema installitud ja peate valima juriidilise isiku **USMF**.
- Voo sildi printimine peab olema konfigureeritud ja tuleb luua mõned sildid jaotises [Voo sildi printimise konfigureerimine](../warehousing/configure-wave-label-printing.md) kirjeldatud juhiste järgi.

### <a name="set-up-work-exceptions"></a>Tööerandite häälestamine

Töö erandid juhivad kiire komplekteerimise käitumist. Töö erandi seadistamiseks toimige järgmiselt.

1. Avage jaotis **Laohaldus \> Seadistus \> Töö \> Tööerandid**.
1. Looge järgmiste sätetega kirje.

    - **Töö erandi kood:** *Kiire komplekteerimine ja printimine*
    - **Erandi tüüp:** *Kiire komplekteerimine*
    - **Soovita voo siltide uuesti printimist:** *Jah*

### <a name="void-and-reprint-after-a-short-pick"></a>Tühistamine ja uuesti printimine pärast kiiret komplekteerimist

1. Logige laorakendusse sisse kasutajana, kellel on juurdepääs laole *62*. (Standardsete demoandmete korral saate logida sisse, kasutades kasutaja ID-na *62* ja paroolina *1*.)
1. Avage müügitellimuse töö töötlemise voog, mis loodi voo siltide algsel printimisel.
1. Valige **Kiire komplekteerimine**.
1. Valige selle stsenaariumi jaoks loodud töö erandi kood.
1. Kui valisite õige erandi, peaks olema märkeruut **Tühista ja prindi uuesti** saadaval. Valige see märkeruut ja kinnitage. Kui see on kinnitatud, arvutatakse välja **Sildi kooste ID** abil tuvastatud rulli seeria uuesti muudetud töörea koguse põhjal. Seejärel prinditakse see uuesti määratud printeriga.
