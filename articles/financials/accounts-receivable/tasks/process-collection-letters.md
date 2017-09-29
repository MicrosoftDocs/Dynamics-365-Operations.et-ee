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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="f213c-103">Märgukirjade töötlemine</span><span class="sxs-lookup"><span data-stu-id="f213c-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f213c-104">See protseduur kirjeldab märgukirjade loomist, printimist ja sisestamist.</span><span class="sxs-lookup"><span data-stu-id="f213c-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="f213c-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="f213c-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="f213c-106">Märgukirjaseeria häälestamine sisestusreeglis</span><span class="sxs-lookup"><span data-stu-id="f213c-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="f213c-107">Avage Krediit ja sissenõuded > Seadistus > Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="f213c-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="f213c-108">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f213c-108">Click Edit.</span></span>
    * <span data-ttu-id="f213c-109">Valige ripploendist märgukirjaseeria.</span><span class="sxs-lookup"><span data-stu-id="f213c-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="f213c-110">Kui te ei soovi luua kannete jaoks märgukirju selle sisestusreegliga, jätke väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="f213c-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="f213c-111">Tabeli piirangu vahekaardil saate muuta seda, kuidas sissenõudekirju töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="f213c-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="f213c-112">Kui väli on seatud olekusse Jah, luuakse märgukirjad selle sisestusreegli jaoks.</span><span class="sxs-lookup"><span data-stu-id="f213c-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="f213c-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f213c-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="f213c-114">Sissenõude märgukirjade loomine</span><span class="sxs-lookup"><span data-stu-id="f213c-114">Create collection letters</span></span>
1. <span data-ttu-id="f213c-115">Avage jaotis Krediit ja sissenõuded > Märgukiri > Märgukirjade loomine.</span><span class="sxs-lookup"><span data-stu-id="f213c-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="f213c-116">Valige kandetüübid, mille jaoks märgukirjad luuakse.</span><span class="sxs-lookup"><span data-stu-id="f213c-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="f213c-117">Kõik seda tüüpi avatud kanded kaasatakse kalkulatsiooni.</span><span class="sxs-lookup"><span data-stu-id="f213c-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="f213c-118">Valige üks suvand väljalt Märgukiri.</span><span class="sxs-lookup"><span data-stu-id="f213c-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="f213c-119">Sisestage märgukirja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f213c-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="f213c-120">Saadaval on kaks sisestusreeglit: Konto – kasutage viivisearve puhul kliendi kontole määratud sisestusreeglit.</span><span class="sxs-lookup"><span data-stu-id="f213c-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="f213c-121">Vali – kasutage sisestusreeglit, mille valite väljal Sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="f213c-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="f213c-122">Valige sisestusreegel, kui määrasite suvandi „Kasuta sisestusreegleid” olekusse „Vali”.</span><span class="sxs-lookup"><span data-stu-id="f213c-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="f213c-123">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="f213c-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="f213c-124">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="f213c-124">Click Filter.</span></span>
6. <span data-ttu-id="f213c-125">Sisestage väljale Kriteeriumid kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="f213c-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="f213c-126">Näiteks sisestage US-001.</span><span class="sxs-lookup"><span data-stu-id="f213c-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="f213c-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f213c-127">Click OK.</span></span>
8. <span data-ttu-id="f213c-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f213c-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="f213c-129">Märgukirjade printimine</span><span class="sxs-lookup"><span data-stu-id="f213c-129">Print collection letters</span></span>
1. <span data-ttu-id="f213c-130">Avage jaotis Krediit ja sissenõuded > Märgukiri > Märgukirjade ülevaatamine ja töötlemine.</span><span class="sxs-lookup"><span data-stu-id="f213c-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="f213c-131">Valige väljal Olek suvand Loodud.</span><span class="sxs-lookup"><span data-stu-id="f213c-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="f213c-132">Valige väljal Prinditud suvand Printimata.</span><span class="sxs-lookup"><span data-stu-id="f213c-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="f213c-133">Klõpsake Prindi.</span><span class="sxs-lookup"><span data-stu-id="f213c-133">Click Print.</span></span>
5. <span data-ttu-id="f213c-134">Klõpsake märgukirja märkust.</span><span class="sxs-lookup"><span data-stu-id="f213c-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="f213c-135">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="f213c-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="f213c-136">Sisestage sisestamiste äralõikekuupäev</span><span class="sxs-lookup"><span data-stu-id="f213c-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="f213c-137">Märgukirja printimiseks klõpsake OK.</span><span class="sxs-lookup"><span data-stu-id="f213c-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="f213c-138">Märgukirja sisestamine</span><span class="sxs-lookup"><span data-stu-id="f213c-138">Post the collection letter</span></span>
1. <span data-ttu-id="f213c-139">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="f213c-139">Click Post.</span></span>
2. <span data-ttu-id="f213c-140">Sisestage märgukirja sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f213c-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="f213c-141">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="f213c-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="f213c-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f213c-142">Click OK.</span></span>
5. <span data-ttu-id="f213c-143">Valige väljal Olek suvand Sisestatud.</span><span class="sxs-lookup"><span data-stu-id="f213c-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="f213c-144">Valige suvand väljal Prinditud.</span><span class="sxs-lookup"><span data-stu-id="f213c-144">In the Printed field, select an option.</span></span>


