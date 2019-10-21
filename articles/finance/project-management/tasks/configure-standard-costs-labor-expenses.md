---
title: Tööjõu ja kulude standardsete kulude konfigureerimine
description: Selles teemas selgitatakse, kuidas seadistada töö jaoks standardne kulu ja projekti kulutused.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 60ab8eb94d4a8a0fb2c1e732ec7b25bfd5e7611e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185401"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="9be57-103">Tööjõu ja kulude standardsete kulude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9be57-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9be57-104">Selles teemas selgitatakse, kuidas seadistada töö jaoks standardne kulu ja projekti kulutused.</span><span class="sxs-lookup"><span data-stu-id="9be57-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="9be57-105">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="9be57-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9be57-106">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Omahind (tund)**.</span><span class="sxs-lookup"><span data-stu-id="9be57-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="9be57-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9be57-107">Select **New**.</span></span>
3. <span data-ttu-id="9be57-108">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9be57-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="9be57-109">Väljale **Omahind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="9be57-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="9be57-110">Saate teatud projektikategooria jaoks standardse omahinna häälestada või häälestada omahinna töötaja koodi, projekti numbri, kategooria, kuupäeva või mis tahes nende kombinatsiooni alusel.</span><span class="sxs-lookup"><span data-stu-id="9be57-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="9be57-111">Rakendatakse kõrgeima üksikasjatasemega omahind.</span><span class="sxs-lookup"><span data-stu-id="9be57-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="9be57-112">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9be57-112">Select **Save**.</span></span>
6. <span data-ttu-id="9be57-113">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Müügihind (tund)**.</span><span class="sxs-lookup"><span data-stu-id="9be57-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="9be57-114">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9be57-114">Select **New**.</span></span>
8. <span data-ttu-id="9be57-115">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9be57-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="9be57-116">Väljal **Kehtib** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="9be57-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="9be57-117">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="9be57-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="9be57-118">Saate häälestada standardse müügihinna tunnikannetele või projekti kategooriale.</span><span class="sxs-lookup"><span data-stu-id="9be57-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="9be57-119">Saate häälestada ka müügihinnad töötaja koodi, projekti numbri, kategooria, kande kuupäeva või nende mis tahes kombinatsioonide alusel.</span><span class="sxs-lookup"><span data-stu-id="9be57-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="9be57-120">Tegelik müügihind, mis rakendatakse, kui töötaja sisestab kande tunnitöölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="9be57-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9be57-121">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="9be57-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="9be57-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9be57-122">Select **Save**.</span></span>
12. <span data-ttu-id="9be57-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9be57-123">Close the page.</span></span>
13. <span data-ttu-id="9be57-124">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Omahind (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="9be57-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="9be57-125">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9be57-125">Select **New**.</span></span>
15. <span data-ttu-id="9be57-126">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9be57-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="9be57-127">Väljale **Omahind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="9be57-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="9be57-128">Täita saab mitut välja, kuid see on kirje salvestamiseks vajalik miinimum.</span><span class="sxs-lookup"><span data-stu-id="9be57-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="9be57-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9be57-129">Select **Save**.</span></span>
18. <span data-ttu-id="9be57-130">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Müügihind (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="9be57-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="9be57-131">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9be57-131">Select **New**.</span></span>
20. <span data-ttu-id="9be57-132">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="9be57-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="9be57-133">Väljal **Kehtib** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="9be57-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="9be57-134">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="9be57-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="9be57-135">Tegelik müügihind, mis seotakse, kui töötaja sisestab kanded kulude töölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="9be57-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9be57-136">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="9be57-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="9be57-137">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9be57-137">Select **Save**.</span></span>

