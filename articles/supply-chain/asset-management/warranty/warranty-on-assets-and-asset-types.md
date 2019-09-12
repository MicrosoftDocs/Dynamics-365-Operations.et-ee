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
# <a name="warranty-on-assets-and-asset-types"></a><span data-ttu-id="833c7-103">Varade ja varatüüpide garantii</span><span class="sxs-lookup"><span data-stu-id="833c7-103">Warranty on assets and asset types</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="833c7-104">Selles teemas selgitatakse, kuidas varahalduses seadistada varade ja varatüüpide garantiisid.</span><span class="sxs-lookup"><span data-stu-id="833c7-104">This topic explains how to set up warranties on assets and asset types in Asset Management.</span></span>

## <a name="set-up-a-warranty-on-an-asset-type"></a><span data-ttu-id="833c7-105">Varatüübi garantii seadistamine</span><span class="sxs-lookup"><span data-stu-id="833c7-105">Set up a warranty on an asset type</span></span>

1. <span data-ttu-id="833c7-106">Valige **Varade haldus** \> **Seadistus** \> **Varatüübid** \> **Varatüübid**.</span><span class="sxs-lookup"><span data-stu-id="833c7-106">Select **Asset management** \> **Setup** \> **Asset types** \> **Asset types**.</span></span>
2. <span data-ttu-id="833c7-107">Valige vasakul paanil varatüüp, et lisada sellele hankija garantiileping, ja seejärel valige **Varatüübi vaikeväärtused**.</span><span class="sxs-lookup"><span data-stu-id="833c7-107">In the left pane, select the asset type to attach a vendor warranty agreement to, and then select **Asset type defaults**.</span></span>
3. <span data-ttu-id="833c7-108">Valige leping FastTabi **Üldine** väljal **Hankija garantii**.</span><span class="sxs-lookup"><span data-stu-id="833c7-108">On the **General** FastTab, in the **Vendor warranty** field, select the agreement.</span></span>

## <a name="set-up-a-warranty-on-an-asset"></a><span data-ttu-id="833c7-109">Varale garantii seadistamine</span><span class="sxs-lookup"><span data-stu-id="833c7-109">Set up a warranty on an asset</span></span>

1. <span data-ttu-id="833c7-110">Valige **Varahaldus**\>**Ühised**\>**Varad**\>**Kõik varad**.</span><span class="sxs-lookup"><span data-stu-id="833c7-110">Select **Asset management** \> **Common** \> **Assets** \> **All assets**.</span></span>
2. <span data-ttu-id="833c7-111">Valige vara ja seejärel suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="833c7-111">Select the asset, and then select **Edit**.</span></span>
3. <span data-ttu-id="833c7-112">Valige garantiileping FastTabi **Hankija** jaotise **Hankija garantii** väljas **Garantii**.</span><span class="sxs-lookup"><span data-stu-id="833c7-112">On the **Vendor** FastTab, in the **Vendor warranty** section, in the **Warranty** field, select the warranty agreement.</span></span>
4. <span data-ttu-id="833c7-113">Valige väljal **Garantii algus** ja **Garantii lõpp** algus-ja lõppkuupäevad.</span><span class="sxs-lookup"><span data-stu-id="833c7-113">In the **Warranty start** and **Warranty end** fields, select the start and end dates.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="833c7-114">Kui töökäsu väljal **Garantii algus** on valitud kuupäev, muutub garantii sellel kuupäeval töökäsule kehtivaks.</span><span class="sxs-lookup"><span data-stu-id="833c7-114">If a date is selected in the **Warranty start** field on a work order, the warranty becomes valid for the work order on that date.</span></span> <span data-ttu-id="833c7-115">Töökäsu loomisel seatakse väli **Garantii alguskuupäev** automaatselt loomise kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="833c7-115">When you create a work order, the **Warranty start** field is automatically set to the date of creation.</span></span> <span data-ttu-id="833c7-116">Samas saate kuupäeva muuta nii, et see vastaks näiteks garantiilepingu alguskuupäevale.</span><span class="sxs-lookup"><span data-stu-id="833c7-116">However, you can change the date so that it corresponds to, for example, the start date of a warranty agreement.</span></span>
    >
    > ![Joonis 1](media/02-warranty.png)

> [!NOTE]
> <span data-ttu-id="833c7-118">Hankija garantiiga kaetud varale töökäsu loomisel, kui töökäsul on garantiiaja jooksul eeldatav alguskuupäev, saate garantiilepingu kohta teatise.</span><span class="sxs-lookup"><span data-stu-id="833c7-118">When you create a work order for an asset that is covered by a vendor warranty, if the work order has an expected start date during the warranty period, you receive a notification about the warranty agreement.</span></span> <span data-ttu-id="833c7-119">Seejärel saate töökäsu vastavalt vajadusele tühistada.</span><span class="sxs-lookup"><span data-stu-id="833c7-119">You can then cancel the work order, as you require.</span></span>
