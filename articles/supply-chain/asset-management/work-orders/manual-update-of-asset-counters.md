---
title: Varaloendurite käsitsi värskendamine
description: Selles teemas kirjeldatakse varaloendurite käsitsi värskendust varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875611"
---
# <a name="manual-update-of-asset-counters"></a>Varaloendurite käsitsi värskendamine

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Loendureid kasutatakse vara registreeringute loomiseks näiteks seoses töös olnud tundide või toodetud koguste arvuga.

Kui loendurile valitud loenduri tüüp on määratud loenduri väärtusi pärima (**Varahaldus** > **Seadistus** > **Vara tüübid** > **Loendurid** > **Üldine** kiirkaart > tumblernupp **Päri vara loenduri väärtused** määratud väärtusele "Jah"), siis värskendatakse automaatselt iga sama loenduri tüüpi kasutav alamvara, kui loote uue sama tüüpi loenduri rea.

Jaotises **Kõik varad** loote varale tundide või koguse loenduri registreeringud vara näitude põhjal.

1. Klõpsake **Varahaldus** > **Üldine** > **Varad** > **Kõik varad**.

2. Valige loendist vara ja klõpsake valikul **Loendurid**. Vormil **Vara loendurid** näete loendit kõigist valitud vara eelmistest loenduri registreeringust.

3. Uue registreeringu loomiseks klõpsake **Uus**. Vara ID sisestatakse automaatselt.

4. Valige asjakohane loendur väljal **Loendur**. Saadaval on ainult varale valitud vara tüübiga seotud loendurid. Seotud ühik sisestatakse automaatselt väljale **Ühik**.

5. Valige loenduri registreeringuks kuupäev ja kellaaeg.

6. Sisestage väljale **Väärtus** arv alates viimasest loenduri registreeringust või sisestage loenduri koguarv väljale **Koondväärtus**.

- Kui paigaldate füüsiliselt varale uue loenduri, peate registreerima vara muudatuse jaotises **Vara loendurid**. Järgmisena peate looma kaks registreeringu rida identsete ajatemplitega ja uue loenduriga seotud reale valite märkeruudu **Loenduri lähtestamine**. Kahe registreeringurea loomisel peab esimene rida olema asendatavale loendurile. Väljal **Kogusummad** on loenduri koguarvuks kõigi selle loenduritüübi registreeritud väärtuste loenduri kogusumma.  
- Kui varale on valitud märkeruut **Loenduri lähtestamine** kasutades hoolduskava invervallitüübiga "Üks kord alates..." või "Üks kord ületades...", on loendur uuel loenduri real ikka aktiivne, sest loote eraldi loenduri rea ja alustate uue loenduriga algusest peale.

![Joonis 1](media/11-work-orders.png)


Kui peate tegema loenduri registreeringuid mitmele varale, saab seda teha jaotises **Varahaldus** > **Päringud** > **Varad** > **Vara loendurid**.

>[!NOTE]
>Võite seadistada vahemiku kõrvalekallete määraltemiseks käsitsi loenduri registreeringutele ja selle, millist sõnumit kuvatakse, kui registreering on määratud vahemikust väljaspool. Loendurite seadistamise kohta vaadake teemat [Loendurid](../setup-for-objects/counters.md).
