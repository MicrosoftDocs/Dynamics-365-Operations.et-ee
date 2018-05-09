--- 
title: "Tööjõu ja kulude standardsete kulude konfigureerimine"
description: "See protseduur näitab, kuidas saate projekti tööjõu ja kulude jaoks standardseid kulusid häälestada."
author: KimANelson
manager: AnnBe
ms.date: 02/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e4f1981bb35f7740bda6f662fd13f3505d1f8fda
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f97c7-103">Tööjõu ja kulude standardsete kulude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f97c7-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f97c7-104">See protseduur näitab, kuidas saate projekti tööjõu ja kulude jaoks standardseid kulusid häälestada.</span><span class="sxs-lookup"><span data-stu-id="f97c7-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f97c7-105">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="f97c7-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f97c7-106">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Omahind (tund).</span><span class="sxs-lookup"><span data-stu-id="f97c7-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="f97c7-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f97c7-107">Click New.</span></span>
3. <span data-ttu-id="f97c7-108">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f97c7-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="f97c7-109">Sisestage arv väljale Omahind.</span><span class="sxs-lookup"><span data-stu-id="f97c7-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="f97c7-110">Saate teatud projektikategooria jaoks standardse omahinna häälestada või häälestada omahinna töötaja koodi, projekti numbri, kategooria, kuupäeva või mis tahes nende kombinatsiooni alusel.</span><span class="sxs-lookup"><span data-stu-id="f97c7-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f97c7-111">Rakendatakse kõrgeima üksikasjatasemega omahind.</span><span class="sxs-lookup"><span data-stu-id="f97c7-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f97c7-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f97c7-112">Click Save.</span></span>
6. <span data-ttu-id="f97c7-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f97c7-113">Close the page.</span></span>
7. <span data-ttu-id="f97c7-114">Avage menüü Projektihaldus ja -arvestus > Häälestamine > Hinnad > Müügihind (hour).</span><span class="sxs-lookup"><span data-stu-id="f97c7-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="f97c7-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f97c7-115">Click New.</span></span>
9. <span data-ttu-id="f97c7-116">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f97c7-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="f97c7-117">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="f97c7-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="f97c7-118">Väljale Hinnakujundus sisestage number.</span><span class="sxs-lookup"><span data-stu-id="f97c7-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="f97c7-119">Saate häälestada standardse müügihinna tunnikannetele või projekti kategooriale.</span><span class="sxs-lookup"><span data-stu-id="f97c7-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f97c7-120">Saate häälestada ka müügihinnad töötaja koodi, projekti numbri, kategooria, kande kuupäeva või nende mis tahes kombinatsioonide alusel.</span><span class="sxs-lookup"><span data-stu-id="f97c7-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f97c7-121">Tegelik müügihind, mis rakendatakse, kui töötaja sisestab kande tunnitöölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="f97c7-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f97c7-122">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="f97c7-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="f97c7-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f97c7-123">Click Save.</span></span>
13. <span data-ttu-id="f97c7-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f97c7-124">Close the page.</span></span>
14. <span data-ttu-id="f97c7-125">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Omahind (kulu).</span><span class="sxs-lookup"><span data-stu-id="f97c7-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="f97c7-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f97c7-126">Click New.</span></span>
16. <span data-ttu-id="f97c7-127">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f97c7-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="f97c7-128">Sisestage arv väljale Omahind.</span><span class="sxs-lookup"><span data-stu-id="f97c7-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="f97c7-129">Täita saab mitut välja, kuid see on kirje salvestamiseks vajalik miinimum.</span><span class="sxs-lookup"><span data-stu-id="f97c7-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="f97c7-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f97c7-130">Click Save.</span></span>
19. <span data-ttu-id="f97c7-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f97c7-131">Close the page.</span></span>
20. <span data-ttu-id="f97c7-132">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Müügihind (kulu).</span><span class="sxs-lookup"><span data-stu-id="f97c7-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="f97c7-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f97c7-133">Click New.</span></span>
22. <span data-ttu-id="f97c7-134">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f97c7-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="f97c7-135">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="f97c7-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="f97c7-136">Väljale Hinnakujundus sisestage number.</span><span class="sxs-lookup"><span data-stu-id="f97c7-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="f97c7-137">Tegelik müügihind, mis seotakse, kui töötaja sisestab kanded kulude töölehele, on kõrgeima üksikasjatasemega müügihind.</span><span class="sxs-lookup"><span data-stu-id="f97c7-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f97c7-138">Näiteks kui nii üldine kui ka töötajapõhine müügihind on häälestatud, kasutatakse töötajapõhist müügihinda.</span><span class="sxs-lookup"><span data-stu-id="f97c7-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="f97c7-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f97c7-139">Click Save.</span></span>


