---
title: Voo täitmise teatised
description: See artikkel kirjeldab voo käivitamise teatisi ja selgitab nende seadistamist.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: a6a554965c11eea3b4fa53fe4dbc4bac04624026
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9336571"
---
# <a name="wave-execution-notifications"></a>Voo täitmise teatised

[!include [banner](../includes/banner.md)]

*Voo käivitamisteatised* funktsioon kasutab ärisündmusi ja tegevuskeskust voo käivitamisega seotud teatiste esitamiseks. See võimaldab teil määratleda teatisi loovad sündmuste tüübid, neid loovad laod ja neid saavad kasutajad.

**Teadete näitamise** nupp (kellukesümbol) navigeerimisriba paremal pool näitab, millal tegevuskeskuse sõnum on praegusele kasutajale saadaval. Kasutaja saab tegevuskeskuse avamiseks ja sõnumite ülevaatamiseks valida nupu **Näita teateid**.

Ärisündmused toimuvad äriprotsesside käivitamisel. Äriprotsessid valmistatud ülesannetest. Äriprotsessi ajal sooritavad seda osalevad kasutajad nende ülesannete täitmiseks äritoiminguid. Ärisündmused on mehhanism, mis võimaldab välissüsteemidel võtta vastu teatisi finants- ja operatsioonide rakendustelt. Sel viisil saavad süsteemid sooritada äritoiminguid ja reageerida ärisündmustele. Lisateavet leiate teemast [Ärisündmuste ülevaade](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>Voo käivitamise teatiste funktsiooni sisse- või väljalülitamine

Selle funktsiooni kasutamiseks peab see olema teie süsteemi jaoks sisse lülitatud. Tarneahela halduse versiooni 10.0.25 puhul lülitatakse funktsioon vaikimisi sisse. Tarneahela halduse versiooni 10.0.29 puhul on see funktsioon kohustuslik ja seda ei saa välja lülitada. Kui käitate versiooni, mis on *vanem kui 10.0.29, saavad administraatorid selle funktsiooni sisse või välja lülitada, otsides Funktsioonihalduse tööruumis*[voo käivitamise teatiste](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) funktsiooni.

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Stsenaarium: voo partii käivitamise teatiste saatmine tegevuskeskusele

See stsenaarium näitab kogu voogu teatiste saatmiseks voo partii käivitamise tõrgete kohta konkreetsele rollile tegevuskeskuse kaudu.

### <a name="make-demo-data-available"></a>Demoandmete kättesaadavaks tegemine

Selle stsenaariumiga töötamiseks peavad teil olema installitud demoandmed ja peate valima juriidilise isiku **USMF**.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Veenduge, et voog oleksid käitatud partiirežiimis

1. Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**.
1. Seadke kiirkaardil **Voo töötlemine** suvandi **Voogude töötlemine partiina** väärtuseks *Jah*.

> [!NOTE]
> Kui soovite keelata voo partii käivitamise teatised, määrake suvandi **Keela voo töötlemise partii teatised** väärtuseks *Jah*.

### <a name="configure-a-wave-notification-policy"></a>Voo teavituspoliitika konfigureerimine

Voo teavituspoliitikad määratlevad saadetavate teatiste tüübid ja teavitatud kasutajad.

1. Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo teavituse poliitikad**.
1. Looge järgmiste sätetega kirje.

    - **Voo teavituspoliitika:** *24BatchError*
    - **Kirjeldus:** *lao 24 voo partii tõrge*
    - **Saada teatis:** *ainult tõrge*
    - **Rollile:** *Süsteemiadministraator*

        > [!NOTE]
        > Kuna see stsenaarium kasutab demoandmeid, valitakse lihtsaks kasutamiseks *süsteemiadministraatori* roll. Kuna olete sisse loginud süsteemiadministraatori kasutajana, saate ka teatisi. Kuid tavaliselt peaksite siiski valima konkreetsema rolli voo partii käivitamise tõrgetest teatamiseks, nt *Laohaldur*.

1. Valige toimingupaanil nupp **Salvesta**.

### <a name="configure-a-wave-template"></a>Voomalli konfigureerimine

Voomallid võimaldavad teil linkida kindlaid voo meetodite eksemplare vastava voo sildi mallidega.

1. Avage **Laohaldus \> Seadistus \> Vood \> Voomallid**.
1. Määrake loendipaanil välja **Voo malli tüüp** väärtuseks *Saatmine* ja seejärel valige laole 24 *24 saadetise vaikimisi* voomall.
1. Määrake kiirkaardi **Üldine** välja **Voo teatise poliitika** väärtuseks *24BatchError*.

### <a name="configure-a-work-template"></a>Töömalli konfigureerimine

Töömalle kasutatakse voo käivitamise ajal töö loomiseks. Selle stsenaariumi korral peaks voo käivitamine käivitama tõrke. Seadistades töömalli päringu kasutama olematut laohoonet, tagate, et voo käivitamine nurjub ja saadab teatise.

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Määrake loendipaanil välja **Töömalli tüüp** väärtuseks *Müügitellimused* ja seejärel valige laole 24 *24 SO olek* töömall.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Redigeerige päringuredaktori dialoogiboksis vahekaardil **Vahemik** järgmist rida (või lisage see, kui seda pole olemas):

    - **Tabel:** *Ajutised töökanded*
    - **Tuletatud tabel:** *Ajutised töökanded*
    - **Väli:** *Ladu*
    - **Kriteerium:** muutke väärtus *24* väärtuseks *Tõrge*.

1. Muutuse kinnitamiseks valige **OK**.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Müügitellimuse loomine ja selle väljastamine lattu

1. Avage jaotis **Müük ja turundus \> Müügitellimus \> Kõik müügitellimused**.
1. Looge järgmiste sätetega müügitellimuse rida.

    - **Kliendi konto:** *US-001*
    - **Ladu:** *24*

1. Lisage kiirkaardil **Müügitellimuse read** järgmiste sätetega müügitellimuse rida.

    - **Kauba kood:** *A0001*
    - **Kogus:** *10*

    > [!NOTE]
    > Need kaubad ja kogused on ainult näited. Määratud ladu peab sisaldama piisavalt varu.

1. Kui uus rida on veel valitud kiirkaardil **Müügitellimus**, valige tööriistaribal **Varu \> Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**. Seejärel sulgege leht.
1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

### <a name="notifications-from-wave-batch-job-execution"></a>Voo partiitöö käivitamise teatised

Olenevalt teie ärisündmuste seadistusest saate te lõpuks teate voo käivitamise tõrke kohta. Tegevuskeskuse teade sarnaneb järgmise näitega ja sisaldab linki nurjunud voole.

> **Tõrge voo käivitamise ajal**  
> Voo USMF-000000001 käitamisel esines tõrge.  
> Viimased teated: voo USMF-000000001 jaoks tööd ei loodud.
>
> **OLEK**  
> Aktiivne
>
> Ava voo üksikasjad

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

