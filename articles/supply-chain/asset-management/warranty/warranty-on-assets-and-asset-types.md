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
ms.openlocfilehash: 3b13f8aba7e1d2448495f97a4772eb573e08c025
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874597"
---
# <a name="warranty-on-assets-and-asset-types"></a>Varade ja varatüüpide garantii

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


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
    > ![Joonis 1](media/02-warranty.png)

> [!NOTE]
> Hankija garantiiga kaetud varale töökäsu loomisel, kui töökäsul on garantiiaja jooksul eeldatav alguskuupäev, saate garantiilepingu kohta teatise. Seejärel saate töökäsu vastavalt vajadusele tühistada.
