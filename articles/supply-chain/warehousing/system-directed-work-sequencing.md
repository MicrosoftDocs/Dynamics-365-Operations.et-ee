---
title: Süsteemi suunatud tööde järjestus
description: Selles teemas antakse teavet süsteemi suunatud tööde järjestuse kohta. Selle funktsiooni abil saate sortida ja filtreerida töötellimusi, mida süsteem kasutajatele käivitamiseks esitab. See on kasulik olukordades, kus lao komplekteerimise protsessi juhtimiseks on lisakriteeriumid nõutavad.
author: Mirzaab
manager: tfehr
ms.date: 07/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFSystemDirectedWorkSequenceQuery, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-03
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3811486a31d079cac7f7c27ea6323f16de4478d5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4970202"
---
# <a name="system-directed-work-sequencing"></a>Süsteemi suunatud tööde järjestus

[!include [banner](../includes/banner.md)]

Süsteemi suunatud tööde järjestuse abil saate sortida ja filtreerida töötellimusi, mida süsteem kasutajatele käivitamiseks esitab. See on kasulik olukordades, kus lao komplekteerimisprotsessi juhtimiseks on lisakriteeriumid nõutavad (nt saatmise aeg, komplekteerimistsoon, asukohaprofiil või erinevate kriteeriumide kombinatsioon).

See funktsioon laiendab praegust süsteemi suunatud komplekteerimise funktsiooni, lisades süsteemi suunatud päringu järjekorra, kus kasutajad saavad seadistada järjestust ja vähemalt ühe päringu, mis hindab kõiki loodud töökäske. Hõivatakse ja esitatakse ainult need töökäsud, mis vastavad mobiilse seadme menüü-üksuse häälestuses määratud.

Seetõttu võimaldab see funktsioon lao komplekteerimise protsesse täiendavalt optimeerida, kuna see tuvastab määratud kriteeriumidele vastavaid töökäskusid, määrab need õigele mobiilse seadme menüü-üksusele ja esitab need seejärel töötajale kindlate oskuste, komplekteerimisseadmete või muude nõuete põhjal.

> [!NOTE]
> Kui on vaja muid kriteeriume, tuleb kasutada mitut mobiilse seadme menüü-üksust.

## <a name="turn-on-the-organization-wide-system-directed-work-sequencing-feature"></a>Lülitage sisse organisatsiooniülene süsteemi suunatud töö järjestamise funktsioon

Enne süsteemi suunatud tööde järjestamise kasutamist peate selle funktsiooni oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Organisatsiooniülene süsteemi suunatud töö järjestamine*

## <a name="setup"></a>Häälestus

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumi kasutamiseks selles teemas esitletud väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed demoandmed. Peate valima ka juriidilise isiku **USMF**. Stsenaarium kasutab ladu *51* demoandmetest.

> [!IMPORTANT]
> Enne tellimuste lattu vabastamist veenduge, et komplekteerimise asukohtadel on tellimuste kõigi üksuste jaoks piisavalt varusid.
>
> Vaikimisi USMF-andmed peaksid seda stsenaariumi toetama. Kui te ei kasuta demoandmeid, vaadake üle seadistus **Asukohakorraldus**, et teada, milliseid komplekteerimise asukohti müügitellimuse komplekteerimiseks kasutatakse. Kui peate korrigeerima varusid, saate luua käsitsi liikumisi, kasutada täiendamist või kasutada mis tahes muud voogu.

### <a name="set-up-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse seadistamine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.
1. Valige mobiilse seadme menüü-üksuste loendist suvand **Müügi komplekteerimine – süsteem**. Nõutav menüü-üksus peaks juba olema olemas. 
1. Kinnitage järgmised sätted.

    - Määrake kiirkaardi **Üldine** väljal **Suunaja** väärtuseks *Süsteemi suunatud*.
    - Kiirkaardil **Tööklassid** peaksid olema järgmised sätted.

        | Töö klassi ID | Töötellimuse tüüp |
        |---|---|
        | Sales | Müügitellimused |
        | SO-komplekteerimine | Müügitellimused |

1. Valige toimingupaanil **Süsteemi suunatud tööde järjestuse päringud**.
1. Valige suvand **Redigeeri**.
1. Kustutage olemasolev rida ja seejärel kinnitage tegevus, valides **Jah**.
1. Rea loomiseks valige toimingupaanilt suvand **Uus**.
1. Määrake uuel real järgmised väärtused.

    - **Järjekorranumber:** *1*
    - **Kirjelduse väli:** *Töö kogus on alla 20 ja kahaneb*

1. Valige käsk **Salvesta**.
1. Valige toimingupaanil **Päringu redigeerimine**.
1. Laiendage vahekaardil **Liitmised** liitmise hierarhiat, et kuvada tabel **Tööread**.
1. Valige tabeli liitmine **Tööread**.
1. Valige **Lisa tabeli liitmine**.
1. Otsige kuvatavast loendist ja valige järgmiste sätetega rida.

    - **Liitmisrežiim:** *n:1*
    - **Seos:** *Asukohad (asukoht)*

1. Valige käsk **Vali**.

    Asukohad lisatakse tabeli liitmisse.

1. Valige vahekaardil **Sortimine** suvand **Lisa**, et lisada rida.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Töö kogus* (valige kuvatavas teateaknas **Jah**, et lisada sellele väljale sortimine.)
    - **Otsingusuund:** *Kahanev*

1. Valige vahekaart **Vahemik**.

    Kui järjestuses peaksid olema kaasatud ainult kindlad töökriteeriumid, saate need määrata vahekaardil **Vahemik**. Selles näites soovite kaasata ainult töö, kus kogus on väiksem kui 20 ea (madalaim mõõtühik).

    Pange tähele, et osad read on juba kaasatud. Neid ridu ei tohi eemaldada.

1. Rea lisamiseks valige **Lisa**.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Varude töö kogus*
    - **Kriteeriumid:** *\<20* (vähem kui 20)

1. Teise rea lisamiseks valige **Lisa**.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Tööread*
    - **Tuletatud tabel:** *Tööread*
    - **Väli:** *Töö tüüp*
    - **Kriteeriumid:** *Komplekteerimine*

1. Teise rea lisamiseks valige **Lisa**.
1. Määrake uuel real järgmised väärtused.

    - **Tabel:** *Asukohad*
    - **Tuletatud tabel:** *Asukohad*
    - **Väli:** *Asukohaprofiili ID*
    - **Kriteeriumid:** *!ETAPP*

        > [!IMPORTANT]
        > Lisage kindlasti ka hüüumärk (*!*) suvandi *ETAPP* ette.

1. Päringu salvestamiseks ja sulgemiseks valige **OK**.
1. Valige käsk **Salvesta**.
1. Sulgege leht lehele **Mobiilse seadme menüü-üksused** naasmiseks.

> [!NOTE]
> See häälestus määratleb kriteeriumid, mida kasutatakse sobiva töö sisestamiseks mobiilse seadme menüü-üksusesse. Kui lisate päringusse veel kriteeriumide ridu, kasutab süsteem kõigepealt päringu rida, millel on väikseim järjekorranumber. Teisisõnu, kõigepealt esitatajse kasutajale kõik sobivad tööd järjekorranumbriga 1 ja seejärel kõik tööd järjekorranumbriga 2. Seetõttu, kui kindlat vahemikku ja sortimist tuleb kasutada koos, tuleb need määrata samas süsteemi suunatud tööde järjestuse päringus.
>
> See seadistus hõivab mis tahes töö, millel on vähemalt üks rida, kus kogus on väiksem kui 20 ea. Seega, kui töös on rida, kus kogus on täpselt 20 ea või üle selle, on see kehtiv, tingimusel, et sellel on ka vähemalt üks rida, kus kogus on väiksem kui 20 ea.

### <a name="location-directives"></a>Asukohakorraldus

Kui kasutate Contoso vaikeandmeid, ei nõua asukohakorralduse tegevuse päring muudatusi. Kuid veendumaks, et asukohakorraldused hõivaksid müügitellimuste kaubad, kui rakendate funktsiooni mitte-Contoso keskkonnas, looge uus asukohakorraldus. Demokeskkonnas sätete kinnitamiseks toimige järgmiselt.

1. Avage **Laohaldus** \> **Seadistus** \> **Asukohakorraldused**.
1. Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.
1. Valige asukohakorraldus, mille nimi on *51 komplekteerimine*.
1. Valige kiirkaardil **Asukohakorralduse tegevused** toimingu **Komplekteerimine** kohta käiv rida.
1. Valige ruudustiku kohal **Päringu redigeerimine**.
1. Vaadake üle päring **Vahemik**.

    1. Otsige üles rida, kus välja **Väli** väärtuseks on seatud *Asukoht*.
    2. Veenduge, et väli **Kriteerium** oleks tühi (st piiranguid pole).

## <a name="scenario"></a>Stsenaarium

### <a name="create-sales-order-picking-work"></a>Müügitellimuse komplekteerimistöö loomine

Enne süsteemi suunatud komplekteerimise käitamist tuleb luua väljaminevaid töid. Selle stsenaariumi puhul loote neli müügitellimust, mis põhinevad määratud süsteemi suunatud tööde järjestuse päringutel.

Iga müügitellimuse jaoks tuleb reserveerida varude kogused. Seetõttu ei saa reserveeritud varusid laost teiste tellimuste jaoks võtta ilma varude reserveeringu täieliku või osalise tühistamiseta.

Seejärel vabastate iga müügitellimuse lattu, et luua väljaminev töö.

#### <a name="sales-order-1"></a>Müügitellimus 1

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse 1 loomiseks valige toimingupaanilt suvand **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - Määrake jaotise **Klient** välja **Kliendi konto** väärtuseks *US-004*.
    - Määrake jaotise **Üldine** välja **Ladu** väärtuseks *51*.

1. Valige dialoogiboksi sulgemiseks suvand **OK**. Märkige üles müügitellimuse number.
1. Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9200*
    - **Kogus:** *20*

1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige lehel **Reserveerimine** varude reserveerimiseks suvand **Reserveeri saatepartii**.
1. Sulgege leht **Reserveerimine**.
1. Tehke Toimingupaani vahekaardil **Ladu** valik **Lattu väljastamine**, et luua lao jaoks töö.

    Saate teabesõnumid, mis näitavad selle müügitellimuse jaoks loodud voo ID ja saadetise ID-d.

#### <a name="sales-order-2"></a>Müügitellimus 2

1. Müügitellimuse 2 loomiseks valige toimingupaanilt suvand **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-007*
    - **Ladu:** *51*

1. Valige dialoogiboksi sulgemiseks suvand **OK**. Märkige üles müügitellimuse number.
1. Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9200*
    - **Kogus:** *5*

1. Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9201*
    - **Kogus:** *1*

1. Reserveerige varud mõlemale reale.
1. Väljastage tellimus lattu.

#### <a name="sales-order-3"></a>Müügitellimus 3

1. Müügitellimuse 3 loomiseks valige toimingupaanilt suvand **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-009*
    - **Ladu:** *51*

1. Valige dialoogiboksi sulgemiseks suvand **OK**. Märkige üles müügitellimuse number.
1. Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9200*
    - **Kogus:** *7*

1. Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9202*
    - **Kogus:** *8*

1. Reserveerige varud mõlemale reale.
1. Väljastage tellimus lattu.

#### <a name="sales-order-4"></a>Müügitellimus 4

1. Müügitellimuse 4 loomiseks valige toimingupaanilt suvand **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-010*
    - **Ladu:** *51*

1. Valige dialoogiboksi sulgemiseks suvand **OK**. Märkige üles müügitellimuse number.
1. Lisage uuele müügitellimusele rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9200*
    - **Kogus:** *25*

1. Valige **Lisa rida**, et lisada teine rida ja seadke järgmised väärtused.

    - **Kauba kood:** *M9202*
    - **Kogus:** *10*

1. Reserveerige varud mõlemale reale.
1. Väljastage tellimus lattu.

### <a name="get-work-ids-for-the-work-that-was-created"></a>Loodud töö jaoks töö ID-de hankimine

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Filtreerige välja **Ladu**, et kuvatakse ainult lao *51* töö.
1. Neli töö ID-d peaks olema loodud. Märkige üles kõigi müügitellimuste töö ID-d.

    | Müügitellimuse ID | Töö ID | Töö kogus |
    |---|---|---|
    | Müügitellimus 1 | Töö ID 1 | 20 ea |
    | Müügitellimus 2 | Töö ID 2 | 6 ea (mõlema rea summa) |
    | Müügitellimus 3 | Töö ID 3 | 15 ea (mõlema rea summa) |
    | Müügitellimus 4 | Töö ID 4 | 35 ea (mõlema rea summa) |

Enne voo käitamist mobiilses seadmes veenduge, et ainult teie äsja loodud töö olek oleks *Avatud* lao *51* ja töökäsu tüübi *Müügitellimus* jaoks. Vastasel juhul võivad testi tulemused erineda, kuna süsteemi suunatud komplekteerimine sisaldab kõiki sobivaid töid.

1. Avage jaotis **Laohaldus \> Töö \> Väljaminev \> Avatud müügitöö**.
1. Filtreerige ruudustiku **Avatud müügitöö** välja **Ladu**, et kuvatakse ainult lao *51* töö.
1. Kinnitage, et kuvatakse teie varasemalt loodud nelja töö ID-d.
1. Sulgege leht **Töö**.

### <a name="mobile-device-flow-execution"></a>Mobiilse seadme voo käivitamine

Vastavalt seadistusele esitab süsteem kasutajale tööd, mis on sorditud kõrgeimast töörea kogusest madalaimale. Iga rea kogus on väiksem kui 20 ea.

Pidage meeles, et see seadistus hõivab mis tahes töö, millel on vähemalt üks rida, kus kogus on väiksem kui 20 ea. Seega, kui töös on teine rida, kus kogus on täpselt 20 ea või enam, on see samuti kehtiv.

#### <a name="mobile-app"></a>Mobiilirakendus

1. Logige ladustamise rakendusse lao *51* kasutajana sisse.
1. Avage jaotis **Väljaminev \> Müügi komplekteerimine – süsteem**.

    Esitatakse töö ID *4* komplekteerimise etapp. Kõigepealt esitatakse see töö ID selle süsteemi suunatud päringu seadistuse tõttu, kus te määrasite, et töö tuleks järjestada töörea kahaneva koguse põhjal.

1. Viige lõpule nõutav komplekteerimine ja ladustamine töö ID sulgemiseks.

    Järgmisena esitatakse töö ID *3*. Üks selle töörida on järjekorras järgmine selle töörea koguse põhjal.

1. Viige lõpule komplekteerimine ja ladustamine töö ID sulgemiseks.

    Järgmisena esitatakse töö ID *2*. Selle töö komplekteerimise rida on järjekorras järgmine.

1. Viige lõpule komplekteerimine ja ladustamine töö ID sulgemiseks.

    Rohkem töid ei tohiks olla teile esitatud. Töö ID *1* pole selle mobiilse seadme menüü-üksuse jaoks sobilik, kuna päring määrab, et tööpäiseid käsitletakse ainult juhul, kui tööridade kogus on väiksem kui 20 ea.

## <a name="tips"></a>Näpunäited

Süsteemi suunatud tööde järjestuse päringud on *kaasa arvatud*. Seda on oluline meeles pidada osade seadistuste puhul. Kui soovite näiteks, et konkreetne menüü-üksus töötleks ainult tööd, kus tööüksus on *ea* ja määrate selle piirangu päringu vahekaardil **Vahemik**. Sellisel juhul esitatakse töötajale kõik tööd, kus vähemalt ühe töörea üksuseks on seatud *ea*. Seetõttu võib see töö sisaldada ka tööd, kus tööridadel on muu tööüksus kui *ea* (nt *kast* või *kaubaalus*). Päring välistab ainult töö, kus ühelegi tööreale pole määratud tööühikuks *ea*.

Seetõttu hõivas päring selle stsenaariumi näites ka töö ID *4*. Selle loomise ajal lisati kaks rida: üks 25 ea kohta ja teine 10 ea kohta. Töö esitati ikkagi kasutajale, sest vähemalt ühe töörea kogus on väiksem kui 20 ea.

Sõltuvalt stsenaariumist saate seda käitumist vältida tööpauside abil.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]