---
title: Laovaru tasemete korrigeerimine laos (üldine ladustamine)
description: See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 450e95d8a4d5a216b84a3c944c6c63b4a8ad10c5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838819"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="8a133-103">Laovaru tasemete korrigeerimine laos (üldine ladustamine)</span><span class="sxs-lookup"><span data-stu-id="8a133-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8a133-104">See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8a133-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="8a133-105">Enne selle käivitamist peate seadistama varude korrigeerimiste jaoks varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="8a133-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="8a133-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="8a133-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="8a133-107">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="8a133-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="8a133-108">Varude korrigeerimise töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="8a133-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="8a133-109">Avage Varude haldus > Töölehe sisestused > Kaubad > Varude korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="8a133-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="8a133-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8a133-110">Click New.</span></span>
3. <span data-ttu-id="8a133-111">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8a133-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="8a133-112">Klõpsake loendis soovitud varude korrigeerimise töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="8a133-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="8a133-113">Osad muud väljad täidetakse teie valitud varude korrigeerimise töölehe nime seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="8a133-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="8a133-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8a133-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="8a133-115">Tööleheridade loomine</span><span class="sxs-lookup"><span data-stu-id="8a133-115">Create journal lines</span></span>
1. <span data-ttu-id="8a133-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8a133-116">Click New.</span></span>
2. <span data-ttu-id="8a133-117">Märkige loendis kaubakoodi väli.</span><span class="sxs-lookup"><span data-stu-id="8a133-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="8a133-118">Valige kaup väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="8a133-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="8a133-119">Kui kasutate demoettevõtte USMF andmeid, sisestage „D0001”.</span><span class="sxs-lookup"><span data-stu-id="8a133-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="8a133-120">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8a133-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="8a133-121">Valige loendist tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="8a133-121">In the list, select a site.</span></span>
6. <span data-ttu-id="8a133-122">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8a133-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="8a133-123">Valige loendist ladu.</span><span class="sxs-lookup"><span data-stu-id="8a133-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="8a133-124">Kui olete valinud kauba, mille puhul asukoht on kohustuslik dimensioon, peate siin määratlema asukoha.</span><span class="sxs-lookup"><span data-stu-id="8a133-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="8a133-125">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="8a133-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="8a133-126">Omahinna väli määrab ühiku omahinna lao sissetulekutele.</span><span class="sxs-lookup"><span data-stu-id="8a133-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="8a133-127">Kui kaubakoodi kohta pole kulu määratud või kui soovite seda käsitsi muuta, tehke seda siin.</span><span class="sxs-lookup"><span data-stu-id="8a133-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="8a133-128">Varude korrigeerimise töölehe kinnitamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="8a133-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="8a133-129">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="8a133-129">Click Validate.</span></span>
2. <span data-ttu-id="8a133-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8a133-130">Click OK.</span></span>
3. <span data-ttu-id="8a133-131">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="8a133-131">Click Post.</span></span>
    * <span data-ttu-id="8a133-132">Sellist tüüpi töölehe sisestamisel sisestatakse lao sissetulek või väljaminek, muudetakse laotaset ja -väärtust ning luuakse pearaamatu kanded.</span><span class="sxs-lookup"><span data-stu-id="8a133-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="8a133-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8a133-133">Click OK.</span></span>
5. <span data-ttu-id="8a133-134">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="8a133-134">Close the form.</span></span>
6. <span data-ttu-id="8a133-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8a133-135">Close the page.</span></span>

