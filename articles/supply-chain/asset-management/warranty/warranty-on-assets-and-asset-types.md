---
title: Varade ja varatüüpide garantiid
description: Selles teemas selgitatakse, kuidas varahalduses seadistada varade ja varatüüpide garantiisid.
author: johanhoffmann
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f05f5af76aeb037d606d38a368a49d011f0d2bd6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825562"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]