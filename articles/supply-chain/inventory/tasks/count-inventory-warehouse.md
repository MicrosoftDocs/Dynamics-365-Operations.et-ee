---
title: Varude loendamine laos
description: Selle protseduuriga selgitatakse lao inventuuritöölehe loomise ja sisestamise protsessi lao asukohas oleva konkreetse toote inventuuriks.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549889"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="e43bd-103">Varude loendamine laos</span><span class="sxs-lookup"><span data-stu-id="e43bd-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e43bd-104">Selle protseduuriga selgitatakse lao inventuuritöölehe loomise ja sisestamise protsessi lao asukohas oleva konkreetse toote inventuuriks.</span><span class="sxs-lookup"><span data-stu-id="e43bd-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="e43bd-105">Seda protseduuri rakendatakse funktsiooni „üldine ladustamine” puhul laohalduse moodulis, mitte ladustamisfunktsiooni puhul moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="e43bd-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="e43bd-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="e43bd-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="e43bd-107">Kui kasutate oma andmeid, siis veenduge, et teil oleksid tooted ja asukohad seadistatud ja et oleksite loonud inventuuritöölehtedele varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="e43bd-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="e43bd-108">Inventuuri teeb harilikult laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="e43bd-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="e43bd-109">Lao inventuuritöölehe loomine</span><span class="sxs-lookup"><span data-stu-id="e43bd-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="e43bd-110">Avage Laohaldus > Töölehe sisestused > Kauba inventuur > Inventuur.</span><span class="sxs-lookup"><span data-stu-id="e43bd-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="e43bd-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e43bd-111">Click New.</span></span>
3. <span data-ttu-id="e43bd-112">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e43bd-113">Klõpsake loendis soovitud lao inventuuritöölehe nime</span><span class="sxs-lookup"><span data-stu-id="e43bd-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="e43bd-114">Mõned muud väljad täidetakse teie valitud lao inventuuritöölehe nime seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="e43bd-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="e43bd-115">Klõpsake väljal Töötaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e43bd-116">Valige loendist töötaja, keda soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="e43bd-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="e43bd-117">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="e43bd-117">Click Select.</span></span>
8. <span data-ttu-id="e43bd-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e43bd-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="e43bd-119">Tööleheridade loomine</span><span class="sxs-lookup"><span data-stu-id="e43bd-119">Create journal lines</span></span>
1. <span data-ttu-id="e43bd-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e43bd-120">Click New.</span></span>
2. <span data-ttu-id="e43bd-121">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e43bd-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e43bd-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e43bd-123">Kui kasutate demoettevõtte USMF andmeid, valige A0001.</span><span class="sxs-lookup"><span data-stu-id="e43bd-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="e43bd-124">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e43bd-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e43bd-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e43bd-126">Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht 2.</span><span class="sxs-lookup"><span data-stu-id="e43bd-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="e43bd-127">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="e43bd-128">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e43bd-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e43bd-129">Kui kasutate demoettevõtte USMF andmeid, valige ladu 24.</span><span class="sxs-lookup"><span data-stu-id="e43bd-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="e43bd-130">Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e43bd-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e43bd-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e43bd-132">Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht BULK-001.</span><span class="sxs-lookup"><span data-stu-id="e43bd-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="e43bd-133">Sisestage number väljale Loendatud.</span><span class="sxs-lookup"><span data-stu-id="e43bd-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="e43bd-134">Kui sisestate loendatud arvu, mis erineb väljal Laoseis näidatud arvust, värskendatakse välja Kogus, näidates lahknevust.</span><span class="sxs-lookup"><span data-stu-id="e43bd-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="e43bd-135">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e43bd-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="e43bd-136">Lao inventuuritöölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="e43bd-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="e43bd-137">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="e43bd-137">Click Post.</span></span>
    * <span data-ttu-id="e43bd-138">Kui sisestate lao inventuuritöölehe ja loendatud arv erineb väljal Laoseis olevast kogusest, sisestatakse lao sissetulek või väljaminek, kaubavaru taset ja väärtust muudetakse ja tekitatakse pearaamatukanded.</span><span class="sxs-lookup"><span data-stu-id="e43bd-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="e43bd-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e43bd-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="e43bd-140">Varude kannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="e43bd-140">View inventory transactions</span></span>
1. <span data-ttu-id="e43bd-141">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="e43bd-141">Click Inventory.</span></span>
2. <span data-ttu-id="e43bd-142">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="e43bd-142">Click Transactions.</span></span>
    * <span data-ttu-id="e43bd-143">Siin saate vaadata kõiki seotud kandeid, mis teie laoinventuuri töölehe sisestamisel luuakse.</span><span class="sxs-lookup"><span data-stu-id="e43bd-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

