---
title: Muuda töö töökausta
description: Selles teemas selgitatakse, kuidas saate kasutada tööüksuste nuppu Muuda töökausta olemasoleva töö töökausta muutmiseks.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 344918b77334f9aca11f799f8c031047ad229ee0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426296"
---
# <a name="change-work-pool-on-work"></a>Muuda töö töökausta

[!include [banner](../includes/banner.md)]

Töö korraldamiseks gruppidesse saate kasutada töökaustu. Näiteks saate luua töökausta kindlas laoasukohas toimuva töö klassifitseerimiseks.

Funktsioon *Töö töökausta muutmine* lisab nupu **Muuda töökausta** tööüksuste toimingupaanile. Tänu sellele saavad laohaldurid hõlpsalt muuta olemasoleva töö töökausta. See funktsioon võimaldab halduritel kiiresti reageerida lao kaupluse korruse muudatustele ja see aitab parandada nende võimet kohaneda muutuvate olukordadega ja vajadusega viia töö üle teise töökausta.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Funktsiooni Töö töökausta muutmine sisselülitamine

Enne, kui alustate selle funktsiooni seadistamist või kasutamist, peate veenduma, et see oleks teie süsteemis saadaval. Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Töö töökausta muutmine*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Funktsiooni Töö töökausta muutmine seadistamine

Selle funktsiooni kasutamiseks peavad teil olema seadistatud mõned töökaustad. Samuti võite seadistada töömallid, et need määraksid automaatselt kausta. Kui soovite töötada läbi hiljem selles teemas käsitletava näidisstsenaariumi, seadistage oma süsteem selles jaotises kirjeldatud viisil.

### <a name="set-up-work-pools"></a>Töökaustade seadistamine

Töökaustad võimaldavad teil korraldada tööüksusi tüübi järgi. Funktsiooniga *Töö töökausta muutmine* töötamiseks peab teil olema saadaval vähemalt kaks töökausta. Töökaustade kuvamiseks ja lisamiseks järgige neid juhiseid.

1. Minge jaotisse **Laohaldus \> Seadistus \> Töö \> Töökaustad**.
1. Kui töötate ettevõtte **USMF** demoandmetega ja töötate läbi selles teemas hiljem esitatud näidisstsenaariumi, lisage kaks töökausta, millel on järgmised sätted.

    - Töökaust 1:

        - **Töökausta ID:** *E-pood*
        - **Kirjeldus:** *E-pood*

    - Töökaust 2:

        - **Töökausta ID:** *CallCenter*
        - **Kirjeldus:** *Kõnekeskus*

1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-work-templates"></a>Töömallide häälestamine

Igale oma töömallile saate määrata vaikimisi töökausta vastavalt vajadusele. Iga asjakohase malli jaoks saate määrata töökausta veerus **Töökausta ID**. Sellisel juhul pärivad kõik antud malli abil loodud tööüksused automaatselt määratud töökausta. Kui töötate ettevõtte **USMF** demoandmetega ja töötate läbi selles teemas hiljem esitatud näidisstsenaariumi, järgige neid juhiseid.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Lehe redigeerimisrežiimi panemiseks valige toimingupaanil **Redigeeri**.
1. Redigeerige malli, seadistades järgmised väärtused.

    - **Töömall:** *62 pakendamiseks komplekteerimine*
    - **Töökausta ID:** *E-pood*

1. Valige käsk **Salvesta**.

## <a name="example-scenario"></a>Näidisstsenaarium

Selles stsenaariumis näidatakse, kuidas muuta olemasoleva tööüksuse töötlemisvoogu, muutes selle töökausta. See kasutab ettevõtte **USMF** demoandmeid ja selles teemas eelnevalt soovitatud sätteid.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Müügitellimuse loomine ja selle väljastamine lattu

1. Kinnitage, et kaupadel *A0001* ja *A0002* oleks piisavalt vaba kaubavaru laos *62*. Avage jaotis **Varude haldus \> Päringud ja aruanded \> Vaba kaubavaru loend** ja redigeerige filtreid järgmiste juhiste järgi.

    - Väärtuse **Ladu** alguses on *62*.
    - Väärtus **Kaubakood** on kas *A001* või *A002*.

    Kõigi demoandmete kogus peaks olema 10.

    Järgmisena peate looma müügitellimuse.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Valige toimingupaanil nupp **Uus**.
1. Dialoogiboksis **Müügitellimuse loomine** määrake järgmised väärtused.

    - **Kliendi konto:** *US-007*
    - **Ladu:** *62*

1. Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.
1. Avatakse uus müügitellimus. See peaks sisaldama uut tühja rida kiirkaardi **Müügitellimuse read** ruudustikus. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *A0001*
    - **Kogus:** *2*

1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.
1. Sulgege leht.
1. Valige kiirkaardil **Müügitellimuse read** suvand **Lisa rida**, et lisada teine rida müügitellimusse. Määrake sellel real järgmised väärtused.

    - **Kauba kood:** *A0002*
    - **Kogus:** *2*

1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida varud.
1. Sulgege leht.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.
1. Saate teabesõnumid, mis näitavad sellest väljastamisest loodud voo ID-d ja saadetise ID-d. Märkige üles voo ID.

### <a name="review-the-outbound-wave"></a>Väljamineva voo ülevaatamine

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Otsige ruudustikust voo ID, mis loodi müügitellimuse väljastamisel.
1. Valige voo ID üksikasjade kuvamiseks.
1. Veenduge, et kiirkaardil **Voo read** oleks kuvatud müügitellimuse saadetise ID.

    > [!TIP]
    > Kui suvandi **Töötle voogu lattu vabastamisel** väärtuseks on seatud *Ei* tarnevoo malli häälestuses, peate voogu käsitsi töötlema, valides toimingupaani vahekaardil **Voog** suvandi **Töötlemine**, et luua töö.

1. Veenduge, et voog oleks töödeldud. Töötlemine loob vajaliku töö.

### <a name="view-work-details-and-change-the-work-pool"></a>Töö üksikasjade kuvamine ja töökausta muutmine

Saate kasutada lehte **Töö üksikasjad** loodud töö kuvamiseks ja töökausta haldamiseks.

1. Avage jaotis **Laohaldus \> Töö \> Töö üksikasjad**.
1. Valige äsja loodud töö rida. Veerus **Tellimuse number** kuvatakse müügitellimuse number.

    Väli **Töökausta ID** määratakse töömallis seadistatud töökausta ID jaoks.

    > [!TIP]
    > Kui teile ei kuvata välja **Töökausta ID**, lisage veerg ruudustikku ja värskendage lehte.

1. Töö ID-ga seostatud töökausta muutmiseks, valige toimingupaani vahekaardil **Töö** suvand **Töökausta ID muutmine**.
1. Valige dialoogiboksi **Muuda töökausta** kiirkaardi **Parameetrid** väljal **Töökausta ID** suvand *CallCenter*.
1. Muudatuse rakendamiseks valige **OK**.
1. Pange tähele, et välja **Töökausta ID** väärtuseks on nüüd muudetud *CallCenter*.

> [!IMPORTANT]
> Kui kuvatakse dialoogiboks **Muuda töökausta** võib väli **Töökausta ID** olla vaikimisi tühi. Kui väli on tühi ja valite siis muudatuste rakendamiseks **OK**, eemaldatakse töökaust tööst täielikult.
>
> Lisaks töökaustade vahetamisele, saate kasutada seda protseduuri töökausta lisamiseks mis tahes tööüksusele, millelt see puudub või töökausta eemaldamiseks tööüksusest, millel see on.
