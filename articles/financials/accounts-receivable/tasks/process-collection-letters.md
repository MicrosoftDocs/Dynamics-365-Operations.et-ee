--- 
title: "Märgukirjade töötlemine"
description: "See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5c146d6ef34137eb8eef3a5a5123ce0174df3033
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="b1865-103">Märgukirjade töötlemine</span><span class="sxs-lookup"><span data-stu-id="b1865-103">Process collection letters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1865-104">See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="b1865-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="b1865-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="b1865-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="b1865-106">Märgukirjaseeria häälestamine sisestusreeglis</span><span class="sxs-lookup"><span data-stu-id="b1865-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="b1865-107">Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="b1865-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="b1865-108">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="b1865-108">Click Edit.</span></span>
    * <span data-ttu-id="b1865-109">Valige ripploendist märgukirjaseeria.</span><span class="sxs-lookup"><span data-stu-id="b1865-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="b1865-110">Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b1865-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="b1865-111">Tabeli piirangu vahekaardil saate muuta seda, kuidas sissenõudekirju töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="b1865-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="b1865-112">Kui väli on seatud olekusse Jah, luuakse märgukirjad selle sisestusreegli jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1865-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="b1865-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b1865-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="b1865-114">Sissenõude märgukirjade loomine</span><span class="sxs-lookup"><span data-stu-id="b1865-114">Create collection letters</span></span>
1. <span data-ttu-id="b1865-115">Avage jaotis Krediit ja sissenõuded > Märgukiri > Märgukirjade loomine.</span><span class="sxs-lookup"><span data-stu-id="b1865-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="b1865-116">Valige kandetüübid, mille jaoks märgukirjad luuakse.</span><span class="sxs-lookup"><span data-stu-id="b1865-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="b1865-117">Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.</span><span class="sxs-lookup"><span data-stu-id="b1865-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="b1865-118">Valige üks suvand väljalt Märgukiri.</span><span class="sxs-lookup"><span data-stu-id="b1865-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="b1865-119">Sisestage märgukirja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b1865-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="b1865-120">Saadaval on kaks sisestusreeglit: Konto – kasutage viivisearve puhul kliendi kontole määratud sisestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="b1865-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="b1865-121">Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="b1865-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="b1865-122">Valige sisestusreegel, kui määrasite suvandi „Kasuta sisestusreegleid” olekusse „Vali”.</span><span class="sxs-lookup"><span data-stu-id="b1865-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="b1865-123">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="b1865-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="b1865-124">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="b1865-124">Click Filter.</span></span>
6. <span data-ttu-id="b1865-125">Sisestage väljale Kriteeriumid kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="b1865-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="b1865-126">Näiteks sisestage US-001.</span><span class="sxs-lookup"><span data-stu-id="b1865-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="b1865-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b1865-127">Click OK.</span></span>
8. <span data-ttu-id="b1865-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b1865-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="b1865-129">Märgukirjade printimine</span><span class="sxs-lookup"><span data-stu-id="b1865-129">Print collection letters</span></span>
1. <span data-ttu-id="b1865-130">Avage jaotis Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine.</span><span class="sxs-lookup"><span data-stu-id="b1865-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="b1865-131">Valige väljal Olek suvand Loodud.</span><span class="sxs-lookup"><span data-stu-id="b1865-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="b1865-132">Valige väljal Prinditud suvand Printimata.</span><span class="sxs-lookup"><span data-stu-id="b1865-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="b1865-133">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="b1865-133">Click Print.</span></span>
5. <span data-ttu-id="b1865-134">Klõpsake märgukirja märkust.</span><span class="sxs-lookup"><span data-stu-id="b1865-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="b1865-135">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="b1865-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="b1865-136">Sisestage sisestamiste äralõikekuupäev</span><span class="sxs-lookup"><span data-stu-id="b1865-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="b1865-137">Märgukirja printimiseks klõpsake OK.</span><span class="sxs-lookup"><span data-stu-id="b1865-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="b1865-138">Märgukirja sisestamine</span><span class="sxs-lookup"><span data-stu-id="b1865-138">Post the collection letter</span></span>
1. <span data-ttu-id="b1865-139">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="b1865-139">Click Post.</span></span>
2. <span data-ttu-id="b1865-140">Sisestage märgukirja sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="b1865-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="b1865-141">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="b1865-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b1865-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b1865-142">Click OK.</span></span>
5. <span data-ttu-id="b1865-143">Valige väljal Olek suvand Sisestatud.</span><span class="sxs-lookup"><span data-stu-id="b1865-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="b1865-144">Valige suvand väljal Prinditud.</span><span class="sxs-lookup"><span data-stu-id="b1865-144">In the Printed field, select an option.</span></span>


