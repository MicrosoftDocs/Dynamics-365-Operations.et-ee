---
title: Varade ja varatüüpide garantiid
description: Selles teemas selgitatakse, kuidas varahalduses seadistada varade ja varatüüpide garantiisid.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
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
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6e69b471af0853159ba807af5f39db64dbbb04f8
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569704"
---
# <a name="warranties-on-assets-and-asset-types"></a>Varade ja varatüüpide garantiid

[!include [banner](../../includes/banner.md)]

 


Selles teemas selgitatakse, kuidas varahalduses seadistada varade ja varatüüpide garantiisid.

## <a name="set-up-a-warranty-on-an-asset-type"></a>Varatüübi garantii seadistamine

1. Valige **Varade haldus** \> **Seadistus** \> **Varatüübid** \> **Varatüübid**.
2. Valige vasakul paanil varatüüp, et lisada sellele hankija garantiileping, ja seejärel valige **Varatüübi vaikeväärtused**.
3. Valige leping FastTabi **Üldine** väljal **Hankija garantii**.

## <a name="set-up-a-warranty-on-an-asset"></a>Varale garantii seadistamine

1. Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**.
2. Valige vara ja seejärel suvand **Redigeeri**.
3. Valige garantiileping FastTabi **Hankija** jaotise **Hankija garantii** väljas **Garantii**.
4. Valige väljal **Garantii algus** ja **Garantii lõpp** algus-ja lõppkuupäevad.

    > [!IMPORTANT]
    > Kui töökäsu väljal **Garantii algus** on valitud kuupäev, muutub garantii sellel kuupäeval töökäsule kehtivaks. Töökäsu loomisel seatakse väli **Garantii alguskuupäev** automaatselt loomise kuupäevale. Samas saate kuupäeva muuta nii, et see vastaks näiteks garantiilepingu alguskuupäevale.
    >
    > ![Töökäsu leht](media/02-warranty.png)

> [!NOTE]
> Hankija garantiiga kaetud varale töökäsu loomisel, kui töökäsul on garantiiaja jooksul eeldatav alguskuupäev, saate garantiilepingu kohta teatise. Seejärel saate töökäsu vastavalt vajadusele tühistada.
