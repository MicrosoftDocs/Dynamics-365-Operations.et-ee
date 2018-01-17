---
title: "Varude jälgimisteabe korrigeerimine"
description: "See protseduur juhib teid läbi varude üleviimistöölehe koostamise ja sisestamise protsessi, et parandada varude jälgimise teavet."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 4ca093e74daaf102a92d74f3f05d8ad4ea9cbf1b
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="4dfe5-103">Varude jälgimisteabe korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="4dfe5-103">Correct inventory tracking information</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4dfe5-104">See protseduur juhib teid läbi varude üleviimistöölehe koostamise ja sisestamise protsessi, et parandada varude jälgimise teavet.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="4dfe5-105">Selles näites muudame partiiga kontrollitava kauba teavet, muutes valesti registreeritud partii teiseks partiiks.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-105">In this example, we’ll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="4dfe5-106">Saate selle protseduuriga tutvuda demoettevõtte USPI või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="4dfe5-107">Kui kasutate oma andmeid, peab teil olema lubatud partiiga kaup ja see ei tohi olla asukoha järgi kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-107">If you use your own data, you need to have an item that’s batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="4dfe5-108">Samuti peate seadistama varude üleviimiste jaoks varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="4dfe5-109">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="4dfe5-110">Lao üleviimistöölehe loomine</span><span class="sxs-lookup"><span data-stu-id="4dfe5-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="4dfe5-111">Minge jaotisse Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-111">Go to Transfer.</span></span>
2. <span data-ttu-id="4dfe5-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-112">Click New.</span></span>
3. <span data-ttu-id="4dfe5-113">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="4dfe5-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="4dfe5-115">Tööleheridade loomine</span><span class="sxs-lookup"><span data-stu-id="4dfe5-115">Create journal lines</span></span>
1. <span data-ttu-id="4dfe5-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-116">Click New.</span></span>
2. <span data-ttu-id="4dfe5-117">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="4dfe5-118">Kui kasutate USPI-d, võite valida üksuse M5003.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="4dfe5-119">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="4dfe5-120">Klõpsake vahekaarti Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="4dfe5-121">Sisestage või valige väärtus väljal Partii number.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="4dfe5-122">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="4dfe5-123">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="4dfe5-124">Sisestage või valige väärtus väljal Partii number.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="4dfe5-125">Töölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="4dfe5-125">Post the journal</span></span>
1. <span data-ttu-id="4dfe5-126">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-126">Click Post.</span></span>
2. <span data-ttu-id="4dfe5-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="4dfe5-128">Jälgimisteabe vaatamine</span><span class="sxs-lookup"><span data-stu-id="4dfe5-128">Check tracing information</span></span>
1. <span data-ttu-id="4dfe5-129">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-129">Click Inventory.</span></span>
2. <span data-ttu-id="4dfe5-130">Klõpsake käsku Jälgi.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-130">Click Trace.</span></span>
3. <span data-ttu-id="4dfe5-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-131">Click OK.</span></span>
    * <span data-ttu-id="4dfe5-132">Selle jälgimisteabe kasutamisel saate välja selgitada, millisest partiist varusid parandasite.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="4dfe5-133">Võite kasutada selle teabe vaatamiseks ka kauba jälgimise lehte.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="4dfe5-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="4dfe5-135">Laokannete kontrollimine</span><span class="sxs-lookup"><span data-stu-id="4dfe5-135">Check inventory transactions</span></span>
1. <span data-ttu-id="4dfe5-136">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-136">Click Inventory.</span></span>
2. <span data-ttu-id="4dfe5-137">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-137">Click Transactions.</span></span>
    * <span data-ttu-id="4dfe5-138">Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.</span><span class="sxs-lookup"><span data-stu-id="4dfe5-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

