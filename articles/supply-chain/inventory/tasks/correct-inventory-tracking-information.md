---
title: Varude jälgimisteabe korrigeerimine
description: See protseduur juhib teid läbi varude üleviimistöölehe koostamise ja sisestamise protsessi, et parandada varude jälgimise teavet.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventBatchIdLookup, InventLocationIdLookup, InventDimTracking, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5155ada23fe4f559c79964e6bd10d86712009d1d
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145764"
---
# <a name="correct-inventory-tracking-information"></a><span data-ttu-id="b7d2e-103">Varude jälgimisteabe korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="b7d2e-103">Correct inventory tracking information</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b7d2e-104">See protseduur juhib teid läbi varude üleviimistöölehe koostamise ja sisestamise protsessi, et parandada varude jälgimise teavet.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to correct inventory tracking information.</span></span> <span data-ttu-id="b7d2e-105">Selles näites muudame partiiga kontrollitava kauba teavet, muutes valesti registreeritud partii teiseks partiiks.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-105">In this example, we'll update the information of a batch controlled item by changing an incorrectly registered batch to another batch.</span></span> <span data-ttu-id="b7d2e-106">Saate selle protseduuriga tutvuda demoettevõtte USPI või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-106">You can walk through this procedure in demo data company USPI, or using your own data.</span></span> <span data-ttu-id="b7d2e-107">Kui kasutate oma andmeid, peab teil olema lubatud partiiga kaup ja see ei tohi olla asukoha järgi kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-107">If you use your own data, you need to have an item that's batch-enabled, and it must not be location-controlled.</span></span> <span data-ttu-id="b7d2e-108">Samuti peate seadistama varude üleviimiste jaoks varude töölehe nime.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-108">You also need to have an inventory journal name set up for inventory transfers.</span></span> <span data-ttu-id="b7d2e-109">Neid ülesandeid täidab üldjuhul laotöötaja.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-109">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="b7d2e-110">Lao üleviimistöölehe loomine</span><span class="sxs-lookup"><span data-stu-id="b7d2e-110">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="b7d2e-111">Minge jaotisse Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-111">Go to Transfer.</span></span>
2. <span data-ttu-id="b7d2e-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-112">Click New.</span></span>
3. <span data-ttu-id="b7d2e-113">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-113">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="b7d2e-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-114">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="b7d2e-115">Tööleheridade loomine</span><span class="sxs-lookup"><span data-stu-id="b7d2e-115">Create journal lines</span></span>
1. <span data-ttu-id="b7d2e-116">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-116">Click New.</span></span>
2. <span data-ttu-id="b7d2e-117">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b7d2e-118">Kui kasutate USPI-d, võite valida üksuse M5003.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-118">If you are using USPI, select item M5003.</span></span>  
3. <span data-ttu-id="b7d2e-119">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-119">In the Quantity field, enter a number.</span></span>
4. <span data-ttu-id="b7d2e-120">Klõpsake vahekaarti Varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-120">Click the Inventory dimensions tab.</span></span>
5. <span data-ttu-id="b7d2e-121">Sisestage või valige väärtus väljal Partii number.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-121">In the Batch number field, enter or select a value.</span></span>
6. <span data-ttu-id="b7d2e-122">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-122">In the Site field, enter or select a value.</span></span>
7. <span data-ttu-id="b7d2e-123">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-123">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="b7d2e-124">Sisestage või valige väärtus väljal Partii number.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-124">In the Batch number field, enter or select a value.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="b7d2e-125">Töölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="b7d2e-125">Post the journal</span></span>
1. <span data-ttu-id="b7d2e-126">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-126">Click Post.</span></span>
2. <span data-ttu-id="b7d2e-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-127">Click OK.</span></span>

## <a name="check-tracing-information"></a><span data-ttu-id="b7d2e-128">Jälgimisteabe vaatamine</span><span class="sxs-lookup"><span data-stu-id="b7d2e-128">Check tracing information</span></span>
1. <span data-ttu-id="b7d2e-129">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-129">Click Inventory.</span></span>
2. <span data-ttu-id="b7d2e-130">Klõpsake käsku Jälgi.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-130">Click Trace.</span></span>
3. <span data-ttu-id="b7d2e-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-131">Click OK.</span></span>
    * <span data-ttu-id="b7d2e-132">Selle jälgimisteabe kasutamisel saate välja selgitada, millisest partiist varusid parandasite.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-132">Using this tracing information you can back trace which batch you corrected inventory from.</span></span>  <span data-ttu-id="b7d2e-133">Võite kasutada selle teabe vaatamiseks ka kauba jälgimise lehte.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-133">You can also use the Item tracing page to see this information.</span></span>  
4. <span data-ttu-id="b7d2e-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-134">Close the page.</span></span>

## <a name="check-inventory-transactions"></a><span data-ttu-id="b7d2e-135">Laokannete kontrollimine</span><span class="sxs-lookup"><span data-stu-id="b7d2e-135">Check inventory transactions</span></span>
1. <span data-ttu-id="b7d2e-136">Klõpsake Ladu.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-136">Click Inventory.</span></span>
2. <span data-ttu-id="b7d2e-137">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-137">Click Transactions.</span></span>
    * <span data-ttu-id="b7d2e-138">Siin näete kandeid, mis loodi, kui oma töölehe sisestasite.</span><span class="sxs-lookup"><span data-stu-id="b7d2e-138">Here you can see the transactions that were created when you posted your journal.</span></span>   

