---
title: Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil
description: Selles teemas näidatakse, kuidas kasutada koormuse planeerimise töölauda müügitellimuse koormuse loomiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a51031647e270662f37138848b0db9ed08d544e
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145874"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="71233-103">Koormate ja saadetiste planeerimine koorma planeerimise töölaua abil</span><span class="sxs-lookup"><span data-stu-id="71233-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71233-104">Selles teemas näidatakse, kuidas kasutada koormuse planeerimise töölauda müügitellimuse koormuse loomiseks.</span><span class="sxs-lookup"><span data-stu-id="71233-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="71233-105">Eeltingimusena loome esmalt müügitellimuse.</span><span class="sxs-lookup"><span data-stu-id="71233-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="71233-106">See protseduur on osa transpordikoordinaatori igapäevatööst.</span><span class="sxs-lookup"><span data-stu-id="71233-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="71233-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="71233-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="71233-108">Loo müügitellimus</span><span class="sxs-lookup"><span data-stu-id="71233-108">Create a sales order</span></span>
1. <span data-ttu-id="71233-109">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Tellimused > Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="71233-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="71233-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="71233-110">Select **New**.</span></span>
3. <span data-ttu-id="71233-111">Valige otsingu avamiseks väljal **Kliendi konto** ripploendi nupp.</span><span class="sxs-lookup"><span data-stu-id="71233-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="71233-112">Valige konto **US-004**.</span><span class="sxs-lookup"><span data-stu-id="71233-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="71233-113">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71233-113">Select **OK**.</span></span>
6. <span data-ttu-id="71233-114">Valige otsingu avamiseks väljal **Kaubakood** ripploendi nupp.</span><span class="sxs-lookup"><span data-stu-id="71233-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="71233-115">Valige üksus **A0001**.</span><span class="sxs-lookup"><span data-stu-id="71233-115">Select item **A0001**.</span></span> <span data-ttu-id="71233-116">**A0001** on transpordihaldusele lubatud.</span><span class="sxs-lookup"><span data-stu-id="71233-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="71233-117">Valige väljal **Koht** ripploendi nupp, et avada otsing, ja seejärel valige üksus.</span><span class="sxs-lookup"><span data-stu-id="71233-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="71233-118">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="71233-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="71233-119">Selle näite korral sisestage väljale **Ladu** tekst „24“.</span><span class="sxs-lookup"><span data-stu-id="71233-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="71233-120">See ladu võimaldab transpordihaldust ja täiustatud laohaldust.</span><span class="sxs-lookup"><span data-stu-id="71233-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="71233-121">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71233-121">Select **Save**.</span></span>
12. <span data-ttu-id="71233-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="71233-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="71233-123">Uue koorma loomine</span><span class="sxs-lookup"><span data-stu-id="71233-123">Create a new load</span></span>
1. <span data-ttu-id="71233-124">Avage **Navigeerimispaan > Moodulid > Transpordihaldus > planeerimine > Koormuse planeerimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="71233-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="71233-125">Valige vahekaart **Müügiread**. Nüüd saate luua koormuse äsja loodud müügitellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="71233-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="71233-126">Koormaid saab luua ostutellimuste, üleviimistellimuste ja müügitellimuste pakkumise ja nõudluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="71233-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="71233-127">Valige toimingupaanil **Pakkumine ja nõudlus**.</span><span class="sxs-lookup"><span data-stu-id="71233-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="71233-128">Valige **Uuele koormusele**.</span><span class="sxs-lookup"><span data-stu-id="71233-128">Select **To new load**.</span></span>
5. <span data-ttu-id="71233-129">Valige väljal **Koormuse malli ID** otsingu avamiseks ripploendi nupp.</span><span class="sxs-lookup"><span data-stu-id="71233-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="71233-130">Koorma mall määratleb kogu koorma maksimaalse kaalu ja mahu mõõtmed.</span><span class="sxs-lookup"><span data-stu-id="71233-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="71233-131">Näiteks võib koorma mall tähistada konteineri või veoauto suurust.</span><span class="sxs-lookup"><span data-stu-id="71233-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="71233-132">Valige kaup.</span><span class="sxs-lookup"><span data-stu-id="71233-132">Select an item.</span></span>
6. <span data-ttu-id="71233-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71233-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="71233-134">Koorma hindamine ja marsruudi määramine</span><span class="sxs-lookup"><span data-stu-id="71233-134">Rate and route the load</span></span>
1. <span data-ttu-id="71233-135">Valige **Hindamine ja marsruutimine**.</span><span class="sxs-lookup"><span data-stu-id="71233-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="71233-136">Valige **Hinda marsruudi töölauda**.</span><span class="sxs-lookup"><span data-stu-id="71233-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="71233-137">Valige **Hinda poodi**.</span><span class="sxs-lookup"><span data-stu-id="71233-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="71233-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="71233-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="71233-139">Valige **Määra**.</span><span class="sxs-lookup"><span data-stu-id="71233-139">Select **Assign**.</span></span>
6. <span data-ttu-id="71233-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="71233-140">Close the page.</span></span>

