--- 
title: "Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil"
description: "See protseduur näitab, kuidas kasutada müügitellimuse koorma loomiseks koorma planeerimise töölauda."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f840a4c15305af5f55451ae7f1cec2da25e685a4
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="d33d1-103">Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil</span><span class="sxs-lookup"><span data-stu-id="d33d1-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d33d1-104">See protseduur näitab, kuidas kasutada müügitellimuse koorma loomiseks koorma planeerimise töölauda.</span><span class="sxs-lookup"><span data-stu-id="d33d1-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="d33d1-105">Eeltingimusena loome esmalt müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="d33d1-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="d33d1-106">See protseduur on osa transpordikoordinaatori igapäevatööst.</span><span class="sxs-lookup"><span data-stu-id="d33d1-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="d33d1-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d33d1-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="d33d1-108">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="d33d1-108">Create a sales order</span></span>
1. <span data-ttu-id="d33d1-109">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="d33d1-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="d33d1-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d33d1-110">Click New.</span></span>
3. <span data-ttu-id="d33d1-111">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d33d1-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d33d1-112">Valige konto US-004.</span><span class="sxs-lookup"><span data-stu-id="d33d1-112">Select account US-004.</span></span>
5. <span data-ttu-id="d33d1-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d33d1-113">Click OK.</span></span>
6. <span data-ttu-id="d33d1-114">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d33d1-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="d33d1-115">Valige kaup A0001.</span><span class="sxs-lookup"><span data-stu-id="d33d1-115">Select item A0001.</span></span>
    * <span data-ttu-id="d33d1-116">A0001 on lubatud transpordihalduse puhul.</span><span class="sxs-lookup"><span data-stu-id="d33d1-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="d33d1-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d33d1-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="d33d1-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="d33d1-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="d33d1-119">Sisestage väljale Ladu väärtus 24.</span><span class="sxs-lookup"><span data-stu-id="d33d1-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="d33d1-120">Valige selle näite puhul ladu 24.</span><span class="sxs-lookup"><span data-stu-id="d33d1-120">In this example select warehouse 24.</span></span> <span data-ttu-id="d33d1-121">See ladu võimaldab transpordihaldust ja täiustatud laohaldust.</span><span class="sxs-lookup"><span data-stu-id="d33d1-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="d33d1-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d33d1-122">Click Save.</span></span>
12. <span data-ttu-id="d33d1-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d33d1-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="d33d1-124">Uue koorma loomine</span><span class="sxs-lookup"><span data-stu-id="d33d1-124">Create a new load</span></span>
1. <span data-ttu-id="d33d1-125">Avage Transpordihaldus > Plaanimine > Koorma plaanimise töölaud.</span><span class="sxs-lookup"><span data-stu-id="d33d1-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="d33d1-126">Klõpsake vahekaarti Müügiread.</span><span class="sxs-lookup"><span data-stu-id="d33d1-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="d33d1-127">Nüüd saate luua äsja loodud müügitellimuse koorma.</span><span class="sxs-lookup"><span data-stu-id="d33d1-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="d33d1-128">Koormaid saab luua ostutellimuste, üleviimistellimuste ja müügitellimuste pakkumise ja nõudluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="d33d1-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="d33d1-129">Klõpsake toimingupaanil suvandit Pakkumine ja nõudlus.</span><span class="sxs-lookup"><span data-stu-id="d33d1-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="d33d1-130">Klõpsake suvandit Uude koormasse.</span><span class="sxs-lookup"><span data-stu-id="d33d1-130">Click To new load.</span></span>
5. <span data-ttu-id="d33d1-131">Klõpsake väljal Koorma malli ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d33d1-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d33d1-132">Koorma mall määratleb kogu koorma maksimaalse kaalu ja mahu mõõtmed.</span><span class="sxs-lookup"><span data-stu-id="d33d1-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="d33d1-133">Näiteks võib koorma mall tähistada konteineri või veoauto suurust.</span><span class="sxs-lookup"><span data-stu-id="d33d1-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="d33d1-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d33d1-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d33d1-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d33d1-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="d33d1-136">Koorma hindamine ja marsruudi määramine</span><span class="sxs-lookup"><span data-stu-id="d33d1-136">Rate and route the load</span></span>
1. <span data-ttu-id="d33d1-137">Klõpsake suvandit Hindamine ja marsruudivalik.</span><span class="sxs-lookup"><span data-stu-id="d33d1-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="d33d1-138">Klõpsake suvandit Marsruudi töölaua määr.</span><span class="sxs-lookup"><span data-stu-id="d33d1-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="d33d1-139">Klõpsake suvandit Kogumäär.</span><span class="sxs-lookup"><span data-stu-id="d33d1-139">Click Rate shop.</span></span>
4. <span data-ttu-id="d33d1-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d33d1-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="d33d1-141">Klõpsake käsku Määra.</span><span class="sxs-lookup"><span data-stu-id="d33d1-141">Click Assign.</span></span>
6. <span data-ttu-id="d33d1-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d33d1-142">Close the page.</span></span>
7. <span data-ttu-id="d33d1-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d33d1-143">Close the page.</span></span>


