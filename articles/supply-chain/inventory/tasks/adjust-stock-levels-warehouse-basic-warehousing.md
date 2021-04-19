---
title: Laovaru tasemete korrigeerimine laos (üldine ladustamine)
description: See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834141"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a><span data-ttu-id="38878-103">Laovaru tasemete korrigeerimine laos (üldine ladustamine)</span><span class="sxs-lookup"><span data-stu-id="38878-103">Adjust stock levels in the warehouse (basic warehousing)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="38878-104">See protseduur selgitab varude korrigeerimise töölehe loomise ja sisestamise protsessi laos olevate toodete laovarude korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="38878-104">This procedure walks you through the process of creating and posting an inventory adjustment journal in order to adjust stock levels of products in the warehouse.</span></span> <span data-ttu-id="38878-105">Enne selle käivitamist peate seadistama varude korrigeerimiste jaoks varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="38878-105">You need to have an inventory journal name set up for inventory adjustments before you start this.</span></span> <span data-ttu-id="38878-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="38878-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="38878-107">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="38878-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-adjustment-journal"></a><span data-ttu-id="38878-108">Varude korrigeerimise töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="38878-108">Create an inventory adjustment journal</span></span>
1. <span data-ttu-id="38878-109">Avage Varude haldus > Töölehe sisestused > Kaubad > Varude korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="38878-109">Go to Inventory management > Journal entries > Items > Inventory adjustment.</span></span>
2. <span data-ttu-id="38878-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="38878-110">Click New.</span></span>
3. <span data-ttu-id="38878-111">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="38878-111">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="38878-112">Klõpsake loendis soovitud varude korrigeerimise töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="38878-112">In the list, click on the inventory adjustment journal name you want to use.</span></span>
    * <span data-ttu-id="38878-113">Osad muud väljad täidetakse teie valitud varude korrigeerimise töölehe nime seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="38878-113">Some other fields will be populated based on the setup of the inventory adjustment journal name you select.</span></span>  
5. <span data-ttu-id="38878-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="38878-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="38878-115">Tööleheridade loomine</span><span class="sxs-lookup"><span data-stu-id="38878-115">Create journal lines</span></span>
1. <span data-ttu-id="38878-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="38878-116">Click New.</span></span>
2. <span data-ttu-id="38878-117">Märkige loendis kaubakoodi väli.</span><span class="sxs-lookup"><span data-stu-id="38878-117">In the list, mark the item number field.</span></span>
3. <span data-ttu-id="38878-118">Valige kaup väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="38878-118">In the Item number field, Select an item.</span></span> <span data-ttu-id="38878-119">Kui kasutate demoettevõtte USMF andmeid, sisestage „D0001”.</span><span class="sxs-lookup"><span data-stu-id="38878-119">If you are using demo data company USMF, type 'D0001'.</span></span>
4. <span data-ttu-id="38878-120">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="38878-120">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="38878-121">Valige loendist tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="38878-121">In the list, select a site.</span></span>
6. <span data-ttu-id="38878-122">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="38878-122">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="38878-123">Valige loendist ladu.</span><span class="sxs-lookup"><span data-stu-id="38878-123">In the list, select a warehouse.</span></span>
    * <span data-ttu-id="38878-124">Kui olete valinud kauba, mille puhul asukoht on kohustuslik dimensioon, peate siin määratlema asukoha.</span><span class="sxs-lookup"><span data-stu-id="38878-124">If you have selected an item with Location as a mandatory dimension, you would have to specify the location here.</span></span>  
8. <span data-ttu-id="38878-125">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="38878-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="38878-126">Omahinna väli määrab ühiku omahinna lao sissetulekutele.</span><span class="sxs-lookup"><span data-stu-id="38878-126">The cost price field specifies the cost per unit for inventory receipts.</span></span> <span data-ttu-id="38878-127">Kui kaubakoodi kohta pole kulu määratud või kui soovite seda käsitsi muuta, tehke seda siin.</span><span class="sxs-lookup"><span data-stu-id="38878-127">If the cost is not specified for the item number or if you wanted to change it manually, you would do this here.</span></span>  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a><span data-ttu-id="38878-128">Varude korrigeerimise töölehe kinnitamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="38878-128">Validate and post the inventory adjustment journal</span></span>
1. <span data-ttu-id="38878-129">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="38878-129">Click Validate.</span></span>
2. <span data-ttu-id="38878-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="38878-130">Click OK.</span></span>
3. <span data-ttu-id="38878-131">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="38878-131">Click Post.</span></span>
    * <span data-ttu-id="38878-132">Sellist tüüpi töölehe sisestamisel sisestatakse lao sissetulek või väljaminek, muudetakse laotaset ja -väärtust ning luuakse pearaamatu kanded.</span><span class="sxs-lookup"><span data-stu-id="38878-132">When you post this kind of journal, an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
4. <span data-ttu-id="38878-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="38878-133">Click OK.</span></span>
5. <span data-ttu-id="38878-134">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="38878-134">Close the form.</span></span>
6. <span data-ttu-id="38878-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="38878-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]