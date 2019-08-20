---
title: Varude loendamine laos
description: Selles teemas kirjeldatakse protsessi, kuidas luua ja sisestada varude inventuuritöölehte, et loendada konkreetset kaupa asukohas laos.
author: MarkusFogelberg
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0909625f31d15fe6b1387ff9ab7fd5d9a9135f4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836440"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="ef36c-103">Varude loendamine laos</span><span class="sxs-lookup"><span data-stu-id="ef36c-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef36c-104">Selles teemas kirjeldatakse protsessi, kuidas luua ja sisestada varude inventuuritöölehte, et loendada konkreetset kaupa asukohas laos.</span><span class="sxs-lookup"><span data-stu-id="ef36c-104">This topic describes the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="ef36c-105">Seda protseduuri rakendatakse funktsiooni „üldine ladustamine” puhul laohalduse moodulis, mitte ladustamisfunktsiooni puhul moodulis Laohaldus.</span><span class="sxs-lookup"><span data-stu-id="ef36c-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="ef36c-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="ef36c-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="ef36c-107">Kui kasutate oma andmeid, siis veenduge, et teil oleksid tooted ja asukohad seadistatud ja et oleksite loonud inventuuritöölehtedele varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="ef36c-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="ef36c-108">Inventuuri teeb harilikult laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="ef36c-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="ef36c-109">Lao inventuuritöölehe loomine</span><span class="sxs-lookup"><span data-stu-id="ef36c-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="ef36c-110">**Avage Laohaldus > Töölehe sisestused > Kauba inventuur > Inventuur.**</span><span class="sxs-lookup"><span data-stu-id="ef36c-110">Go to **Navigation pane > Modules > Inventory management > Journal entries > Item counting > Counting**.</span></span>
2. <span data-ttu-id="ef36c-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-111">Select **New**.</span></span>
3. <span data-ttu-id="ef36c-112">Valige väljal **Nimi** varude inventuuri töölehe nimi, mida soovite ripploendis kasutada.</span><span class="sxs-lookup"><span data-stu-id="ef36c-112">In the **Name** field, select the inventory counting journal name you want to use from the drop-down list.</span></span> <span data-ttu-id="ef36c-113">Mõned muud väljad täidetakse teie valitud lao inventuuritöölehe nime seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="ef36c-113">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
4. <span data-ttu-id="ef36c-114">Klõpsake välja **Töötaja** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ef36c-114">In the **Worker** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ef36c-115">**Valige** loendist töötaja, keda soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="ef36c-115">In the list, **Select** the worker you want to use.</span></span>
6. <span data-ttu-id="ef36c-116">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-116">Select **OK**.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="ef36c-117">Loo töölehe read</span><span class="sxs-lookup"><span data-stu-id="ef36c-117">Create journal lines</span></span>
1. <span data-ttu-id="ef36c-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-118">Select **New**.</span></span>
2. <span data-ttu-id="ef36c-119">Väljal **Eseme number** valige soovitud kirje ripploendist.</span><span class="sxs-lookup"><span data-stu-id="ef36c-119">In the **Item number** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="ef36c-120">Kui kasutate demoettevõtte USMF andmeid, valige **A0001**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-120">If you are using demo data company USMF, select **A0001**.</span></span>  
3. <span data-ttu-id="ef36c-121">Väljal **sait** valige soovitud kirje ripploendist.</span><span class="sxs-lookup"><span data-stu-id="ef36c-121">In the **Site** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="ef36c-122">Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht **2**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-122">If you are using demo data company USMF, select site **2**.</span></span>
4. <span data-ttu-id="ef36c-123">Väljal **Ladu** valige soovitud kirje ripploendist.</span><span class="sxs-lookup"><span data-stu-id="ef36c-123">In the **Warehouse** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="ef36c-124">Kui kasutate demoettevõtte USMF andmeid, valige ladu **24**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-124">If you are using demo data company USMF, select warehouse **24**.</span></span>  
5. <span data-ttu-id="ef36c-125">Väljal **Asukoht** valige soovitud kirje ripploendist.</span><span class="sxs-lookup"><span data-stu-id="ef36c-125">In the **Location** field, select the desired record from the drop-down list.</span></span> <span data-ttu-id="ef36c-126">Kui kasutate demoettevõtte USMF andmeid, valige tegevuskoht **BULK-001**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-126">If you are using demo data company USMF, select location **BULK-001**.</span></span>  
6. <span data-ttu-id="ef36c-127">Sisestage number väljale Loendatud.</span><span class="sxs-lookup"><span data-stu-id="ef36c-127">In the Counted field, enter a number.</span></span> <span data-ttu-id="ef36c-128">Kui sisestate loendatud arvu, mis erineb väljal **Laos** näidatud arvust, värskendatakse välja **Kogus**, näidates lahknevust.</span><span class="sxs-lookup"><span data-stu-id="ef36c-128">If you enter a counted number that’s different to the number shown in the **On-hand** field, the **Quantity** field is updated to show the discrepancy.</span></span>  
7. <span data-ttu-id="ef36c-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-129">Select **Save**.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="ef36c-130">Lao inventuuritöölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="ef36c-130">Post the inventory counting journal</span></span>
1. <span data-ttu-id="ef36c-131">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-131">Select **Post**.</span></span> <span data-ttu-id="ef36c-132">Kui sisestate lao inventuuritöölehe ja loendatud arv erineb väljal **Laos** olevast kogusest, sisestatakse lao sissetulek või väljaminek, kaubavaru taset ja väärtust muudetakse ja tekitatakse pearaamatukanded.</span><span class="sxs-lookup"><span data-stu-id="ef36c-132">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the **On-hand** field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>
2. <span data-ttu-id="ef36c-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-133">Select **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="ef36c-134">Varude kannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="ef36c-134">View inventory transactions</span></span>
1. <span data-ttu-id="ef36c-135">Valige **Laoseis**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-135">Select **Inventory**.</span></span>
2. <span data-ttu-id="ef36c-136">Valige **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="ef36c-136">Select **Transactions**.</span></span> <span data-ttu-id="ef36c-137">Siin saate vaadata kõiki seotud kandeid, mis teie laoinventuuri töölehe sisestamisel luuakse.</span><span class="sxs-lookup"><span data-stu-id="ef36c-137">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

