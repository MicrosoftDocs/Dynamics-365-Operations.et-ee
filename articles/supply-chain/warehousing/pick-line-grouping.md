---
title: Komplekteerimisridade grupeerimine
description: See teema annab ülevaate komplekteerimisridade grupeerimisest.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 076a4dfdc49525eef616d1008073371be1dd4a248cd6f16d395b544ae70e7531
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757490"
---
# <a name="pick-line-grouping"></a>Komplekteerimisridade grupeerimine

[!include [banner](../includes/banner.md)]

Komplekteerimisridade grupeerimine võimaldab mitu töörida, millel on sama üksus ja asukoht, kombineerida üheks komplekteerimiseks, mis edastatakse mobiilse seadme kasutajale. Seega saavad laotöötajad võtta vastu kõige tõhusamad võimalikud juhiseid, kuid nõutav nõutav süsteemi tööridade eraldamine (nt erinevate konteinerite ja tellimuste jaoks) on võimalik säilitada.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Komplekteerimisrea grupeerimise funktsiooni sisselülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *laohaldus*
- **Funktsiooni nimi:** *Komplekteerimisridade grupeerimine*

## <a name="set-up-pick-line-grouping"></a>Komplekteerimisridade grupeerimise seadistamine

### <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüükäsud**.
1. Valige toimingupaanil nupp **Uus**.
1. Väljale **Menüü-üksuse nimi** sisestage *Müügigrupi rea komplekteerimine*.
1. Väljale **Pealkiri** sisestage *Müügigrupi rea komplekteerimine*. See pealkiri kuvatakse mobiilse seadme menüüs.
1. Valige väljal **Režiim** suvand *Töö*.
1. Valige suvandi **Kasuta olemasolevat tööd** sätteks *Jah*.
1. Määrake kiirkaardil **Üldine** järgmised väärtused.

    - Väljale **Juhtija** valige *Kasutaja suunatud*.
    - Määrake suvand **Loo litsentsiplaat** valikule *Jah*.
    - Määrake suvand **Grupi komplekteerimine** valikule *Jah*.
    - Võtke vastu ülejäänud väljade vaikesuvandid.

1. Järgige neid etappe, et konfigureerida mobiilse seadme menüü-üksuse kehtivad töö klassid.

    1. Valige kiirkaardil **Tööklassid** suvand **Uus**.
    2. Väljal **Töö klassi ID** saate valida kas suvandi *Müük* või *SO komplekteerimine*, olenevalt kasutatavast laost. Valige selle stsenaariumi jaoks *SO-komplekteerimine*.

        Väli **Töökäsu tüüp** seatakse automaatselt valikule *Müügitellimused*.

### <a name="set-up-a-mobile-device-menu"></a>Mobiilse seadme menüü seadistamine

Järgige neid samme äsja loodud menüükäsu lisamiseks menüüsse **Väljastus**.

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**.
1. Valige Toimingupaanil nupp **Redigeeri**.
1. Loendi paan kuvab kõik olemasolevad mobiilse seadme menüüd. Valige loendist *Väljastus*.
1. Otsige üles loendist üles suvand **Saadaolevad menüüd ja menüü-üksused**, leidke ja valige loodud menüü-üksus *Müügigrupi rea komplekteerimine*.
1. Valige parempoolne noolenupp, et nihutada menüü-üksus *Müügigrupi rea komplekteerimine* loendisse **Menüüstruktuur**.
1. Kasutage üles ja alla noolenuppe, et teisaldada menüü-üksus soovitud asukohta menüüstruktuuris.
1. Valige toimingupaanil nupp **Salvesta**.

### <a name="set-up-a-work-template"></a>Töömalli häälestamine

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Valige väljal **Töökäsu tüüp** suvand *Müügitellimused*.
1. Ruudustikus **Ülevaade** leidke ja valige töömall, mida tuleks selle funktsiooniga kasutada. Valige selle stsenaariumi jaoks mall *51 Ettevalmistamiseks komplekteerimine*.
1. Valige Toimingupaanil nupp **Päringu redigeerimine**.
1. Valige päringuredaktori dialoogiboksis vahekaardil **Sortimine** suvand **Lisa** ja määrake siis järgmised uue rea väärtused.

    - Valige veerus **Tabel** suvand *Ajutised töökanded*.
    - Valige veerus **Tuletatud tabel** suvand *Ajutised töökanded*.
    - Valige veerus **Väli** suvand *Kaubakood*.
    - Valige veerus **Otsingu suund** suvand *Kasvav*.

1. Valige **OK**, et sulgeda dialoogiboks ja salvestada oma sätted.
1. Teile kuvatakse järgmine teade: „Grupeerimine lähtestatakse, kas soovite jätkata?” Jätkamiseks valige **Jah**.

> [!IMPORTANT]
> Komplekteerimisrea grupeerimise funktsiooni töötamiseks peavad töö read olema sorditud kauba ID järgi. Kui samu üksuseid sisaldavad read ei ole üksteise järel järjestatud, siis neid ei grupeerita.

## <a name="example"></a>Näide

### <a name="create-picking-work"></a>Komplekteerimistöö loomine

Enne kogumi komplekteerimise seadistamist peate looma mõne sobiliku väljamineva töö.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
1. Müügitellimuse loomiseks valige **Uus**.
1. Valige *US-004* väljalt **Kliendi konto**.
1. Kiirkaardi **Üldine** väljal **Ladu** valige *51*.
1. Valige nupp **OK**.
1. Lisage kiirkaardil **Müügitellimuse read** järgmised kuus rida:

    - **1. rida:** valige väljal **Kaubakood** väärtus *M9200*. Sisestage väljale **Kogus** väärtus *3*.
    - **2. rida:** valige väljal **Kaubakood** väärtus *M9201*. Sisestage väljale **Kogus** väärtus *3*.
    - **3. rida:** valige väljal **Kaubakood** väärtus *M9202*. Sisestage väljale **Kogus** väärtus *2*.
    - **4. rida:** valige väljal **Kaubakood** väärtus *M9200*. Sisestage väljale **Kogus** väärtus *1*.
    - **5. rida:** valige väljal **Kaubakood** väärtus *M9200*. Sisestage väljale **Kogus** väärtus *3*.
    - **6. rida:** valige väljal **Kaubakood** väärtus *M9202*. Sisestage väljale **Kogus** väärtus *7*.

    Siin on iga üksuse üldkoguste kokkuvõte.

    - **Üksus M9200:** igat *7*
    - **Üksus M9201:** igat *3*
    - **Üksus M9202:** igat *9*

1. Enne tellimuste lattu vabastamist peate veenduma, et komplekteerimise asukohtadel on kõikide tellimuste kõigi üksuste jaoks piisavalt varusid. Vaadake üle seadistus **Asukoha korraldus**, et määratleda, milliseid komplekteerimise asukohti müügitellimuse komplekteerimiseks kasutatakse. Kui kasutate Contoso demo andmekeskkonda laole *51*, veenduge, et varud oleks olemas.

    Peate nüüd reserveerima iga rea laovaru.

1. Kiirkaardil **Müügitellimuse read** valige üks ridadest, mis tuleb reserveerida.
1. Valige ruudustiku kohal olevast menüüst **Varud** suvand **Reserveerimine**.
1. Valige toimingupaani lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et rakendada reserveering. Seejärel sulgege leht.
1. Korrake samme 8 kuni 10 ülejäänud ridade puhul, mis tuleb reserveerida.

    Peate nüüd vabastama müügitellimuse lattu.

1. Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.

    Saate teate, mis ütleb, et saadetis ja voog on loodud ning et voog on esitatud partiina käitamiseks.

    Kui voog ja kõik allavoolu tööd on lõpetatud, luuakse kuue reaga töö jaoks töö ID. Read sorditakse kaubakoodi alusel.

1. Avage **Laohaldus \> Töö \> Kõik töö**, et vaadata loodud tööd. Märkige üles **Töö ID** väärtus, kuna vajate seda järgmises protseduuris.

### <a name="initiate-picking-from-the-mobile-device"></a>Komplekteerimise käivitamine mobiilsest seadmest

1. Logige mobiilsesse seadmesse sisse kasutajana, kes on seadistatud lao *51* jaoks.
1. Valige mobiilses seadmes menüü, mis sisaldab uut mobiilse seadme menüü-üksust. Valige selle stsenaariumi jaoks **Väljastav**.
1. Valige menüü-üksus **Müügigrupi rea komplekteerimine** ja käivitage komplekteerimine.
1. Sisestage **Töö ID** väärtus, mille eelmises protseduuris kindlaks tegite.

    Peaksite nägema komplekteerimise etappe, kus kauba *M9200* kõik komplekteeritud read on grupeeritud ja teil tuleks saada juhis *7* iga kauba *M9200* komplekteerimiseks.

    > [!IMPORTANT]
    > Mobiilses seadmes on kolme komplekteerimise töörea komplekteerimistöö koondatud kasutaja üheks komplekteerimissammuks.

1. Kinnitage komplekteerimise etapp.
1. Avage töö ID töö leht ja pange tähele, et kõik kolm üksuse *M9200* komplekteerimisrida suleti samaaegselt.
1. Minge tagasi mobiilsesse seadmesse ja jätkake komplekteerimisega. Esitada tuleks kauba *M9201* töörida 4. Kuna tellimusel oli ainult üks töörida, ei ole midagi liita.
1. Kinnitage komplekteerimise etapp.
1. Viimane komplekteerimise etapp mobiilsel seadmel koondab töökäsu viimased kaks komplekteerimisrida.
1. Viige lõpule kõik *üheksa* eseme *M9202* komplekteerimise sammu.
1. Kinnitage võtmise etapp ja mis tahes täiendavad komplekteerimise/võtmise paarid töö lõpetamiseks.

> [!IMPORTANT]
>
> - Tööridu saab grupeerida ainult siis, kui need on järjekorras.
> - Järgmisi funktsioone ei toetata.
>
>   - Tegeliku kaaluga kaubad
>
>    Kui töös sisalduvad tegeliku kaaluga kaubad, kuvatakse teile enne komplekteerimise alustamist tõrketeade.
>
>   - Osade komplekteerimine
>   - Töö read, millel on lõpetamata täiendamise töö
>   - Ülekomplekteerimine
>   - Kiirelt komplekteeritava kauba ümberjaotamine


[!INCLUDE[footer-include](../../includes/footer-banner.md)]