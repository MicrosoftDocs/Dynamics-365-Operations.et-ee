---
title: Komplekteerimisridade grupeerimine
description: See teema annab ülevaate komplekteerimisridade grupeerimisest.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4b9cd7dac680c1691fb4c6dd4078f109254be784
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215590"
---
# <a name="pick-line-grouping"></a>Komplekteerimisridade grupeerimine

[!include [banner](../includes/banner.md)]

Komplekteerimisridade grupeerimisel saab mitut töörida, millel on sama üksus ja asukoht, kombineerida üheks komplekteerimiseks, mis edastatakse mobiilse seadme kasutajale. Seega saavad laotöötajad võtta vastu kõige tõhusamad võimalikud juhiseid, kuid samal ajal säilitatakse nõutav süsteemi tööridade eraldamine (nt erinevate konteinerite ja tellimuste jaoks).

## <a name="set-up-pick-line-grouping"></a>Komplekteerimisridade grupeerimise seadistamine

### <a name="create-a-mobile-device-menu-item"></a>Mobiilse seadme menüü-üksuse loomine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused** ja looge uus menüü-üksus, mille nimi on **Müügigrupi rea komplekteerimine – kasutaja suunatud**.
2. Määrake jaotises **Mobiilse seadme menüü-üksused** järgmised väärtused.

    - Väljale **Menüü-üksuse nimi** sisestage **Müügi komplekteerimine – grupi rida**.
    - Väljale **Pealkiri** sisestage **Müügi komplekteerimine – grupi rida**.
    - Valige väljal **Režiim** suvand **Töö**.
    - Valige suvandi **Kasuta olemasolevat tööd** sätteks **Jah**.

3. Kiirkaardil **Üldine** saate määrata järgmised väärtused.

    - Väljale **Juhtija** valige **Kasutaja suunatud**.
    - Määrake suvand **Loo litsentsiplaat** valikule **Jah**.
    - Määrake suvand **Grupi komplekteerimine** valikule **Jah**.

4. Kiirkaardil **Töö klassid** järgige neid etappe, et konfigureerida mobiilse seadme menüü-üksuse kehtivad töö klassid.

    1. Valige suvand **Uus**.
    2. Väljal **Töö klassi ID** valige **Müük** või **SO komplekteerimine**, olenevalt kasutatavast laost.
    3. Valige väljal **Töökäsu tüüp** suvand **Müügitellimused**.

### <a name="set-up-a-mobile-device-menu"></a>Mobiilse seadme menüü seadistamine

1. Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü**. 
1. Lisage menüü-üksus, mille just lõite, soovitud menüüsse.

### <a name="set-up-a-work-template"></a>Töömalli häälestamine

1. Avage **Laohaldus \> Seadistus \> Töö \> Töömallid**.
1. Leidke selle funktsiooniga kasutatav töömall. Selle näite puhul valige standardne **51 Ettevalmistamiseks komplekteerimine** Contoso töömall.
1. Valige menüüs käsk **Redigeeri päringut**.
1. Vahekaardil **Sortimine** valige suvand **Lisa** ja seejärel seadke järgmised väärtused.

    - Valige väljal **Tabel** suvand **Ajutised töökanded**.
    - Valige väljal **Tuletatud tabel** suvand **Ajutised töökanded**.
    - Valige väljal **Väli** suvand **Kaubakood**.
    - Valige väljal **Otsingu suund** suvand **Kasvav**.

> [!NOTE]
> Komplekteerimisrea grupeerimise funktsiooni töötamiseks peavad töö read olema sorditud kauba ID järgi. Kui samu üksuseid sisaldavad read ei ole üksteise järel järjestatud, siis neid ei grupeerita.

## <a name="example"></a>Näide

### <a name="create-picking-work"></a>Komplekteerimistöö loomine

Enne kogumi komplekteerimise seadistamist peate looma mõne sobiliku väljamineva töö.

1. Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.
2. Müügitellimuse loomiseks valige **Uus**. 
3. Valige väljalt **Kliendi konto** mis tahes klient. 
4. Kiirkaardi **Üldine** väljal **Ladu** valige **51**. Seejärel valige **OK**.
5. Lisage jaotises **Müügitellimuse read** järgmised kuus rida:

    - **1. rida:** valige väljal **Kaubakood** väärtus **M9200**. Sisestage väljale **Kogus** väärtus **3**.
    - **2. rida:** valige väljal **Kaubakood** väärtus **M9201**. Sisestage väljale **Kogus** väärtus **3**. 
    - **3. rida:** valige väljal **Kaubakood** väärtus **M9202**. Sisestage väljale **Kogus** väärtus **2**. 
    - **4. rida:** valige väljal **Kaubakood** väärtus **M9200**. Sisestage väljale **Kogus** väärtus **1**. 
    - **5. rida:** valige väljal **Kaubakood** väärtus **M9200**. Sisestage väljale **Kogus** väärtus **3**.
    - **6. rida:** valige väljal **Kaubakood** väärtus **M9202**. Sisestage väljale **Kogus** väärtus **7**. 

    Siin on iga üksuse üldkoguste kokkuvõte.

    - **Üksus M9200:** igat 7
    - **Üksus M9201:** igat 3
    - **Üksus M9202:** igat 9

6. Enne tellimuste lattu vabastamist peate veenduma, et komplekteerimise asukohtadel on kõikide tellimuste kõigi üksuste jaoks piisavalt varusid. Vaadake üle seadistus **Asukoha korraldus**, et määratleda, milliseid komplekteerimise asukohti müügitellimuse komplekteerimiseks kasutatakse.
7. Reserveerige varud ja vabastage need lattu. Luuakse töö ID, millel on kuus rida. Read sorditakse kaubakoodi alusel.

### <a name="run-the-mobile-device-flow"></a>Mobiilse seadme voo käitamine

1. Valige mobiilses seadmes menüü, mis sisaldab uut mobiilse seadme menüü-üksust.
1. Valige menüü-üksus **Müügi komplekteerimine – grupi rida** ja käivitage komplekteerimine.

    Pärast menüü valimist ja töö ID sisestamist näete komplekteerimise etappi, kus kõik üksuse M9200 komplekteerimisread on grupeeritud. Saate juhise komplekteerida üksust M9200 seitse tükki.

1. Kinnitage komplekteerimise etapp. 
1. Avage poolelioleva töö kliendi ekraan ja pange tähele, et kõik kolm üksuse M9200 komplekteerimisrida suleti samaaegselt.

    Esitatakse töö rida 4.

1. Kinnitage komplekteerimise etapp.

    Viimane komplekteerimise etapp mobiilsel seadmel koondab töökäsu viimased kaks komplekteerimisrida.

1. Viige lõpule kõik üheksa üksuse M9202 komplekteerimise sammu.
1. Kinnitage võtmise etapp ja mis tahes täiendavad komplekteerimise/võtmise paarid töö lõpetamiseks.

> [!NOTE]
> - Tööridu saab grupeerida ainult siis, kui need on järjekorras.
> - Järgmisi funktsioone ei toetata.
>
>    - Tegeliku kaaluga kaubad. Kui töös sisalduvad tegeliku kaaluga kaubad, kuvatakse teile enne komplekteerimise alustamist tõrketeade.
>    - Osade komplekteerimine.
>    - Töö read, millel on lõpetamata täiendamise töö.
>    - Ülekomplekteerimine.
