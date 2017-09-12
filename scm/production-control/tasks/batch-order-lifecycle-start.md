--- 
title: "Partii tellimuse elutsükkel loomisest käivitamiseni"
description: "See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa."
author: YuyuScheller
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
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 418bf29aff3ff03455b4be150409fc9b55e965c9
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="56d9c-103">Partii tellimuse elutsükkel loomisest käivitamiseni</span><span class="sxs-lookup"><span data-stu-id="56d9c-103">Batch order lifecycle from create to start</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56d9c-104">See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa.</span><span class="sxs-lookup"><span data-stu-id="56d9c-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="56d9c-105">Alates loomisest, kulude prognoosimisest ja tootmistöö plaanimisest kuni partiitellimuse tegeliku alguseni.</span><span class="sxs-lookup"><span data-stu-id="56d9c-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="56d9c-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="56d9c-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="56d9c-107">Protseduuri teise andmekogumiga käitamise eeltingimus on aktiivse valemi ja protsessiversiooniga väljastatud toode.</span><span class="sxs-lookup"><span data-stu-id="56d9c-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="56d9c-108">Partiitellimuse koostamine</span><span class="sxs-lookup"><span data-stu-id="56d9c-108">Create a batch order</span></span>
1. <span data-ttu-id="56d9c-109">Minge jaotisse Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="56d9c-109">Go to All production orders.</span></span>
2. <span data-ttu-id="56d9c-110">Klõpsake valikut Uus partiitellimus.</span><span class="sxs-lookup"><span data-stu-id="56d9c-110">Click New batch order.</span></span>
3. <span data-ttu-id="56d9c-111">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="56d9c-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="56d9c-112">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="56d9c-112">Click Create.</span></span>
5. <span data-ttu-id="56d9c-113">Kasutage kiirfiltrit, et filtreerida välja Tootmine väärtuse b järgi.</span><span class="sxs-lookup"><span data-stu-id="56d9c-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="56d9c-114">Tootmisvalemi ja eeldatavate kaastoodete kuvamine</span><span class="sxs-lookup"><span data-stu-id="56d9c-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="56d9c-115">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="56d9c-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="56d9c-116">Klõpsake valikut Valem.</span><span class="sxs-lookup"><span data-stu-id="56d9c-116">Click Formula.</span></span>
3. <span data-ttu-id="56d9c-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-117">Close the page.</span></span>
4. <span data-ttu-id="56d9c-118">Klõpsake valikut Kaastooted.</span><span class="sxs-lookup"><span data-stu-id="56d9c-118">Click Co-products.</span></span>
5. <span data-ttu-id="56d9c-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="56d9c-120">Partiitellimuse hindamine</span><span class="sxs-lookup"><span data-stu-id="56d9c-120">Estimate the batch order</span></span>
1. <span data-ttu-id="56d9c-121">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="56d9c-121">Click Estimate.</span></span>
2. <span data-ttu-id="56d9c-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="56d9c-122">Click OK.</span></span>
3. <span data-ttu-id="56d9c-123">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="56d9c-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="56d9c-124">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="56d9c-124">Click View calculation details.</span></span>
5. <span data-ttu-id="56d9c-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="56d9c-126">Partiitellimuse väljastamine</span><span class="sxs-lookup"><span data-stu-id="56d9c-126">Release the batch order</span></span>
1. <span data-ttu-id="56d9c-127">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="56d9c-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="56d9c-128">Klõpsake valikut Vabasta.</span><span class="sxs-lookup"><span data-stu-id="56d9c-128">Click Release.</span></span>
3. <span data-ttu-id="56d9c-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="56d9c-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="56d9c-130">Tootmistööde plaanimine</span><span class="sxs-lookup"><span data-stu-id="56d9c-130">Schedule production jobs</span></span>
1. <span data-ttu-id="56d9c-131">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="56d9c-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="56d9c-132">Klõpsake valikut Tööde planeerimine.</span><span class="sxs-lookup"><span data-stu-id="56d9c-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="56d9c-133">Tehke väljal Piiratud võimsus valik Ei.</span><span class="sxs-lookup"><span data-stu-id="56d9c-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="56d9c-134">Tehke väljal Piiratud materjal valik Ei.</span><span class="sxs-lookup"><span data-stu-id="56d9c-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="56d9c-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="56d9c-135">Click OK.</span></span>
6. <span data-ttu-id="56d9c-136">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="56d9c-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="56d9c-137">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="56d9c-137">Click All jobs.</span></span>
8. <span data-ttu-id="56d9c-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="56d9c-139">Partiitellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="56d9c-139">Start the batch order</span></span>
1. <span data-ttu-id="56d9c-140">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="56d9c-140">Click Start.</span></span>
2. <span data-ttu-id="56d9c-141">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="56d9c-141">Click the General tab.</span></span>
3. <span data-ttu-id="56d9c-142">Tehke väljal Sisesta komplekteerimisleht kohe valik Ei.</span><span class="sxs-lookup"><span data-stu-id="56d9c-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="56d9c-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="56d9c-143">Click OK.</span></span>
5. <span data-ttu-id="56d9c-144">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="56d9c-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="56d9c-145">Klõpsake suvandit Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-145">Click Picking list.</span></span>
7. <span data-ttu-id="56d9c-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="56d9c-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="56d9c-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-147">Close the page.</span></span>
9. <span data-ttu-id="56d9c-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-148">Close the page.</span></span>
10. <span data-ttu-id="56d9c-149">Klõpsake suvandit Protsessikaart.</span><span class="sxs-lookup"><span data-stu-id="56d9c-149">Click Route card.</span></span>
11. <span data-ttu-id="56d9c-150">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="56d9c-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="56d9c-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-151">Close the page.</span></span>
13. <span data-ttu-id="56d9c-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56d9c-152">Close the page.</span></span>


