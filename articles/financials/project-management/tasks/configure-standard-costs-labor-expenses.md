---
title: Tööjõu ja kulude standardsete kulude konfigureerimine
description: See protseduur näitab, kuidas saate projekti tööjõu ja kulude jaoks standardseid kulusid häälestada.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: b76956e9b1ce1a1e977aaa7c4974e73754e0d261
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845880"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="591cd-103">Tööjõu ja kulude standardsete kulude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="591cd-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="591cd-104">See protseduur näitab, kuidas saate projekti tööjõu ja kulude jaoks standardseid kulusid häälestada.</span><span class="sxs-lookup"><span data-stu-id="591cd-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="591cd-105">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="591cd-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="591cd-106">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Omahind (tund).</span><span class="sxs-lookup"><span data-stu-id="591cd-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="591cd-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="591cd-107">Click New.</span></span>
3. <span data-ttu-id="591cd-108">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="591cd-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="591cd-109">Sisestage arv väljale Omahind.</span><span class="sxs-lookup"><span data-stu-id="591cd-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="591cd-110">Saate teatud projektikategooria jaoks standardse omahinna häälestada või häälestada omahinna töötaja koodi, projekti numbri, kategooria, kuupäeva või mis tahes nende kombinatsiooni alusel.</span><span class="sxs-lookup"><span data-stu-id="591cd-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="591cd-111">Rakendatakse kõrgeima üksikasjatasemega omahind.</span><span class="sxs-lookup"><span data-stu-id="591cd-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="591cd-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="591cd-112">Click Save.</span></span>
6. <span data-ttu-id="591cd-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="591cd-113">Close the page.</span></span>
7. <span data-ttu-id="591cd-114">Avage menüü Projektihaldus ja -arvestus > Häälestamine > Hinnad > Müügihind (hour).</span><span class="sxs-lookup"><span data-stu-id="591cd-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="591cd-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="591cd-115">Click New.</span></span>
9. <span data-ttu-id="591cd-116">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="591cd-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="591cd-117">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="591cd-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="591cd-118">Väljale Hinnakujundus sisestage number.</span><span class="sxs-lookup"><span data-stu-id="591cd-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="591cd-119">Saate häälestada standardse müügihinna tunnikannetele või projekti kategooriale.</span><span class="sxs-lookup"><span data-stu-id="591cd-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="591cd-120">Saate häälestada ka müügihinnad töötaja koodi, projekti numbri, kategooria, kande kuupäeva või nende mis tahes kombinatsioonide alusel.</span><span class="sxs-lookup"><span data-stu-id="591cd-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="591cd-121">Tegelik müügihind, mis rakendatakse, kui töötaja sisestab kande tunnitöölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="591cd-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="591cd-122">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="591cd-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="591cd-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="591cd-123">Click Save.</span></span>
13. <span data-ttu-id="591cd-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="591cd-124">Close the page.</span></span>
14. <span data-ttu-id="591cd-125">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Omahind (kulu).</span><span class="sxs-lookup"><span data-stu-id="591cd-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="591cd-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="591cd-126">Click New.</span></span>
16. <span data-ttu-id="591cd-127">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="591cd-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="591cd-128">Sisestage arv väljale Omahind.</span><span class="sxs-lookup"><span data-stu-id="591cd-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="591cd-129">Täita saab mitut välja, kuid see on kirje salvestamiseks vajalik miinimum.</span><span class="sxs-lookup"><span data-stu-id="591cd-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="591cd-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="591cd-130">Click Save.</span></span>
19. <span data-ttu-id="591cd-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="591cd-131">Close the page.</span></span>
20. <span data-ttu-id="591cd-132">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Müügihind (kulu).</span><span class="sxs-lookup"><span data-stu-id="591cd-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="591cd-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="591cd-133">Click New.</span></span>
22. <span data-ttu-id="591cd-134">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="591cd-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="591cd-135">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="591cd-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="591cd-136">Väljale Hinnakujundus sisestage number.</span><span class="sxs-lookup"><span data-stu-id="591cd-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="591cd-137">Tegelik müügihind, mis seotakse, kui töötaja sisestab kanded kulude töölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="591cd-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="591cd-138">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="591cd-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="591cd-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="591cd-139">Click Save.</span></span>

