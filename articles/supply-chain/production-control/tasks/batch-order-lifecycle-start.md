---
title: Partii tellimuse elutsükkel loomisest käivitamiseni
description: See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8d9ed44c9e05ea815e78ae041234ad61f76d89d8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825034"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="b3e25-103">Partii tellimuse elutsükkel loomisest käivitamiseni</span><span class="sxs-lookup"><span data-stu-id="b3e25-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b3e25-104">See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa.</span><span class="sxs-lookup"><span data-stu-id="b3e25-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="b3e25-105">Alates loomisest, kulude prognoosimisest ja tootmistöö plaanimisest kuni partiitellimuse tegeliku alguseni.</span><span class="sxs-lookup"><span data-stu-id="b3e25-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="b3e25-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b3e25-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="b3e25-107">Protseduuri teise andmekogumiga käitamise eeltingimus on aktiivse valemi ja protsessiversiooniga väljastatud toode.</span><span class="sxs-lookup"><span data-stu-id="b3e25-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="b3e25-108">Partiitellimuse koostamine</span><span class="sxs-lookup"><span data-stu-id="b3e25-108">Create a batch order</span></span>
1. <span data-ttu-id="b3e25-109">Minge jaotisse Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="b3e25-109">Go to All production orders.</span></span>
2. <span data-ttu-id="b3e25-110">Klõpsake valikut Uus partiitellimus.</span><span class="sxs-lookup"><span data-stu-id="b3e25-110">Click New batch order.</span></span>
3. <span data-ttu-id="b3e25-111">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b3e25-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="b3e25-112">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="b3e25-112">Click Create.</span></span>
5. <span data-ttu-id="b3e25-113">Kasutage kiirfiltrit, et filtreerida välja Tootmine väärtuse b järgi.</span><span class="sxs-lookup"><span data-stu-id="b3e25-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="b3e25-114">Tootmisvalemi ja eeldatavate kaastoodete kuvamine</span><span class="sxs-lookup"><span data-stu-id="b3e25-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="b3e25-115">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="b3e25-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b3e25-116">Klõpsake valikut Valem.</span><span class="sxs-lookup"><span data-stu-id="b3e25-116">Click Formula.</span></span>
3. <span data-ttu-id="b3e25-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-117">Close the page.</span></span>
4. <span data-ttu-id="b3e25-118">Klõpsake valikut Kaastooted.</span><span class="sxs-lookup"><span data-stu-id="b3e25-118">Click Co-products.</span></span>
5. <span data-ttu-id="b3e25-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="b3e25-120">Partiitellimuse hindamine</span><span class="sxs-lookup"><span data-stu-id="b3e25-120">Estimate the batch order</span></span>
1. <span data-ttu-id="b3e25-121">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="b3e25-121">Click Estimate.</span></span>
2. <span data-ttu-id="b3e25-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3e25-122">Click OK.</span></span>
3. <span data-ttu-id="b3e25-123">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="b3e25-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="b3e25-124">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b3e25-124">Click View calculation details.</span></span>
5. <span data-ttu-id="b3e25-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="b3e25-126">Partiitellimuse väljastamine</span><span class="sxs-lookup"><span data-stu-id="b3e25-126">Release the batch order</span></span>
1. <span data-ttu-id="b3e25-127">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="b3e25-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="b3e25-128">Klõpsake valikut Vabasta.</span><span class="sxs-lookup"><span data-stu-id="b3e25-128">Click Release.</span></span>
3. <span data-ttu-id="b3e25-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3e25-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="b3e25-130">Tootmistööde plaanimine</span><span class="sxs-lookup"><span data-stu-id="b3e25-130">Schedule production jobs</span></span>
1. <span data-ttu-id="b3e25-131">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="b3e25-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="b3e25-132">Klõpsake valikut Tööde planeerimine.</span><span class="sxs-lookup"><span data-stu-id="b3e25-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="b3e25-133">Tehke väljal Piiratud võimsus valik Ei.</span><span class="sxs-lookup"><span data-stu-id="b3e25-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="b3e25-134">Tehke väljal Piiratud materjal valik Ei.</span><span class="sxs-lookup"><span data-stu-id="b3e25-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="b3e25-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3e25-135">Click OK.</span></span>
6. <span data-ttu-id="b3e25-136">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="b3e25-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="b3e25-137">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="b3e25-137">Click All jobs.</span></span>
8. <span data-ttu-id="b3e25-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="b3e25-139">Partiitellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="b3e25-139">Start the batch order</span></span>
1. <span data-ttu-id="b3e25-140">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="b3e25-140">Click Start.</span></span>
2. <span data-ttu-id="b3e25-141">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="b3e25-141">Click the General tab.</span></span>
3. <span data-ttu-id="b3e25-142">Tehke väljal Sisesta komplekteerimisleht kohe valik Ei.</span><span class="sxs-lookup"><span data-stu-id="b3e25-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="b3e25-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3e25-143">Click OK.</span></span>
5. <span data-ttu-id="b3e25-144">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="b3e25-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="b3e25-145">Klõpsake suvandit Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-145">Click Picking list.</span></span>
7. <span data-ttu-id="b3e25-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b3e25-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="b3e25-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-147">Close the page.</span></span>
9. <span data-ttu-id="b3e25-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-148">Close the page.</span></span>
10. <span data-ttu-id="b3e25-149">Klõpsake suvandit Protsessikaart.</span><span class="sxs-lookup"><span data-stu-id="b3e25-149">Click Route card.</span></span>
11. <span data-ttu-id="b3e25-150">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b3e25-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="b3e25-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-151">Close the page.</span></span>
13. <span data-ttu-id="b3e25-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b3e25-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]