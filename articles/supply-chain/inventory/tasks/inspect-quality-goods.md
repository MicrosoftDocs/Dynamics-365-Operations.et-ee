---
title: Kaupade kvaliteedi kontrollimine
description: "See protseduur näitab, kuidas kvaliteettellimust töödelda."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ab536047340bdebecb7c8317e20208c87a4776f7
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="9430f-103">Kaupade kvaliteedi kontrollimine</span><span class="sxs-lookup"><span data-stu-id="9430f-103">Inspect the quality of goods</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9430f-104">See protseduur näitab, kuidas kvaliteettellimust töödelda.</span><span class="sxs-lookup"><span data-stu-id="9430f-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="9430f-105">Saate selle juhendi käitada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="9430f-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="9430f-106">Enne selle näidisprotseduuri käivitamist peate ostutellimuse 000016 kinnitama ja toote sissetuleku sisestama.</span><span class="sxs-lookup"><span data-stu-id="9430f-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="9430f-107">See loob kvaliteettellimuse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="9430f-107">This will automatically create a quality order.</span></span> <span data-ttu-id="9430f-108">Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="9430f-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="9430f-109">Kvaliteettellimuse valimine</span><span class="sxs-lookup"><span data-stu-id="9430f-109">Select a quality order</span></span>
1. <span data-ttu-id="9430f-110">Avage Varude haldus > Perioodilised ülesanded > Kvaliteedijuhtimine > Kvaliteettellimused.</span><span class="sxs-lookup"><span data-stu-id="9430f-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="9430f-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9430f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9430f-112">Valige kvaliteettellimus, mis loodi enne selle protseduuri käivitamist.</span><span class="sxs-lookup"><span data-stu-id="9430f-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="9430f-113">Testitulemuste salvestamine</span><span class="sxs-lookup"><span data-stu-id="9430f-113">Record test results</span></span>
1. <span data-ttu-id="9430f-114">Klõpsake suvandit Tulemused.</span><span class="sxs-lookup"><span data-stu-id="9430f-114">Click Results.</span></span>
2. <span data-ttu-id="9430f-115">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="9430f-115">Click Edit.</span></span>
3. <span data-ttu-id="9430f-116">Sisestage number väljale Tulemuse kogus.</span><span class="sxs-lookup"><span data-stu-id="9430f-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="9430f-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9430f-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9430f-118">Klõpsake väljal Tulemus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9430f-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9430f-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9430f-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9430f-120">Selles näites põhineb tulemus eelmääratletud tulemusel.</span><span class="sxs-lookup"><span data-stu-id="9430f-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="9430f-121">Üldjuhul saate salvestada täpsema katse tulemuse, nt suuruse või muu dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="9430f-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="9430f-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9430f-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9430f-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9430f-123">Click Save.</span></span>
9. <span data-ttu-id="9430f-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9430f-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="9430f-125">Kontrolli kvaliteettellimuse õigsust</span><span class="sxs-lookup"><span data-stu-id="9430f-125">Validate the quality order</span></span>
1. <span data-ttu-id="9430f-126">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="9430f-126">Click Validate.</span></span>
2. <span data-ttu-id="9430f-127">Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9430f-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9430f-128">Valige kontrolliv kasutaja.</span><span class="sxs-lookup"><span data-stu-id="9430f-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="9430f-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9430f-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9430f-130">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="9430f-130">Click Select.</span></span>
5. <span data-ttu-id="9430f-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9430f-131">Click OK.</span></span>
6. <span data-ttu-id="9430f-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9430f-132">Close the page.</span></span>

