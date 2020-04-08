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
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140089"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="fdcaa-103">Tööjõu ja kulude standardsete kulude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fdcaa-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fdcaa-104">Selles teemas selgitatakse, kuidas seadistada töö jaoks standardne kulu ja projekti kulutused.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="fdcaa-105">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="fdcaa-106">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Omahind (tund)**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="fdcaa-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-107">Select **New**.</span></span>
3. <span data-ttu-id="fdcaa-108">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="fdcaa-109">Väljale **Omahind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="fdcaa-110">Saate teatud projektikategooria jaoks standardse omahinna häälestada või häälestada omahinna töötaja koodi, projekti numbri, kategooria, kuupäeva või mis tahes nende kombinatsiooni alusel.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="fdcaa-111">Rakendatakse kõrgeima üksikasjatasemega omahind.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="fdcaa-112">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-112">Select **Save**.</span></span>
6. <span data-ttu-id="fdcaa-113">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Müügihind (tund)**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="fdcaa-114">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-114">Select **New**.</span></span>
8. <span data-ttu-id="fdcaa-115">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="fdcaa-116">Väljal **Kehtib** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="fdcaa-117">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="fdcaa-118">Saate häälestada standardse müügihinna tunnikannetele või projekti kategooriale.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="fdcaa-119">Saate häälestada ka müügihinnad töötaja koodi, projekti numbri, kategooria, kande kuupäeva või nende mis tahes kombinatsioonide alusel.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="fdcaa-120">Tegelik müügihind, mis rakendatakse, kui töötaja sisestab kande tunnitöölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="fdcaa-121">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="fdcaa-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-122">Select **Save**.</span></span>
12. <span data-ttu-id="fdcaa-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-123">Close the page.</span></span>
13. <span data-ttu-id="fdcaa-124">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Omahind (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="fdcaa-125">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-125">Select **New**.</span></span>
15. <span data-ttu-id="fdcaa-126">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="fdcaa-127">Väljale **Omahind** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="fdcaa-128">Täita saab mitut välja, kuid see on kirje salvestamiseks vajalik miinimum.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="fdcaa-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-129">Select **Save**.</span></span>
18. <span data-ttu-id="fdcaa-130">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Müügihind (kulu)**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="fdcaa-131">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-131">Select **New**.</span></span>
20. <span data-ttu-id="fdcaa-132">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="fdcaa-133">Väljal **Kehtib** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="fdcaa-134">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="fdcaa-135">Tegelik müügihind, mis seotakse, kui töötaja sisestab kanded kulude töölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="fdcaa-136">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="fdcaa-137">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="fdcaa-137">Select **Save**.</span></span>

