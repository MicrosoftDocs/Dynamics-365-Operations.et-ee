---
title: Partii tellimuse elutsükkel loomisest käivitamiseni
description: See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 67c44341b1c8633917f41fa82593ab66611ca1ea
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255417"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="fa459-103">Partii tellimuse elutsükkel loomisest käivitamiseni</span><span class="sxs-lookup"><span data-stu-id="fa459-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa459-104">See protseduur juhib teid läbi partiitellimuse elutsükli esimese osa.</span><span class="sxs-lookup"><span data-stu-id="fa459-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="fa459-105">Alates loomisest, kulude prognoosimisest ja tootmistöö plaanimisest kuni partiitellimuse tegeliku alguseni.</span><span class="sxs-lookup"><span data-stu-id="fa459-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="fa459-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="fa459-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="fa459-107">Protseduuri teise andmekogumiga käitamise eeltingimus on aktiivse valemi ja protsessiversiooniga väljastatud toode.</span><span class="sxs-lookup"><span data-stu-id="fa459-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="fa459-108">Partiitellimuse koostamine</span><span class="sxs-lookup"><span data-stu-id="fa459-108">Create a batch order</span></span>
1. <span data-ttu-id="fa459-109">Minge jaotisse Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="fa459-109">Go to All production orders.</span></span>
2. <span data-ttu-id="fa459-110">Klõpsake valikut Uus partiitellimus.</span><span class="sxs-lookup"><span data-stu-id="fa459-110">Click New batch order.</span></span>
3. <span data-ttu-id="fa459-111">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="fa459-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="fa459-112">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="fa459-112">Click Create.</span></span>
5. <span data-ttu-id="fa459-113">Kasutage kiirfiltrit, et filtreerida välja Tootmine väärtuse b järgi.</span><span class="sxs-lookup"><span data-stu-id="fa459-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="fa459-114">Tootmisvalemi ja eeldatavate kaastoodete kuvamine</span><span class="sxs-lookup"><span data-stu-id="fa459-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="fa459-115">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="fa459-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="fa459-116">Klõpsake valikut Valem.</span><span class="sxs-lookup"><span data-stu-id="fa459-116">Click Formula.</span></span>
3. <span data-ttu-id="fa459-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-117">Close the page.</span></span>
4. <span data-ttu-id="fa459-118">Klõpsake valikut Kaastooted.</span><span class="sxs-lookup"><span data-stu-id="fa459-118">Click Co-products.</span></span>
5. <span data-ttu-id="fa459-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="fa459-120">Partiitellimuse hindamine</span><span class="sxs-lookup"><span data-stu-id="fa459-120">Estimate the batch order</span></span>
1. <span data-ttu-id="fa459-121">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="fa459-121">Click Estimate.</span></span>
2. <span data-ttu-id="fa459-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fa459-122">Click OK.</span></span>
3. <span data-ttu-id="fa459-123">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="fa459-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="fa459-124">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="fa459-124">Click View calculation details.</span></span>
5. <span data-ttu-id="fa459-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="fa459-126">Partiitellimuse väljastamine</span><span class="sxs-lookup"><span data-stu-id="fa459-126">Release the batch order</span></span>
1. <span data-ttu-id="fa459-127">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="fa459-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="fa459-128">Klõpsake valikut Vabasta.</span><span class="sxs-lookup"><span data-stu-id="fa459-128">Click Release.</span></span>
3. <span data-ttu-id="fa459-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fa459-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="fa459-130">Tootmistööde plaanimine</span><span class="sxs-lookup"><span data-stu-id="fa459-130">Schedule production jobs</span></span>
1. <span data-ttu-id="fa459-131">Klõpsake tegumiribal valikut Graafik.</span><span class="sxs-lookup"><span data-stu-id="fa459-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="fa459-132">Klõpsake valikut Tööde planeerimine.</span><span class="sxs-lookup"><span data-stu-id="fa459-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="fa459-133">Tehke väljal Piiratud võimsus valik Ei.</span><span class="sxs-lookup"><span data-stu-id="fa459-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="fa459-134">Tehke väljal Piiratud materjal valik Ei.</span><span class="sxs-lookup"><span data-stu-id="fa459-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="fa459-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fa459-135">Click OK.</span></span>
6. <span data-ttu-id="fa459-136">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="fa459-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="fa459-137">Klõpsake valikut Kõik tööd.</span><span class="sxs-lookup"><span data-stu-id="fa459-137">Click All jobs.</span></span>
8. <span data-ttu-id="fa459-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="fa459-139">Partiitellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="fa459-139">Start the batch order</span></span>
1. <span data-ttu-id="fa459-140">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="fa459-140">Click Start.</span></span>
2. <span data-ttu-id="fa459-141">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="fa459-141">Click the General tab.</span></span>
3. <span data-ttu-id="fa459-142">Tehke väljal Sisesta komplekteerimisleht kohe valik Ei.</span><span class="sxs-lookup"><span data-stu-id="fa459-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="fa459-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fa459-143">Click OK.</span></span>
5. <span data-ttu-id="fa459-144">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="fa459-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="fa459-145">Klõpsake suvandit Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="fa459-145">Click Picking list.</span></span>
7. <span data-ttu-id="fa459-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="fa459-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fa459-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-147">Close the page.</span></span>
9. <span data-ttu-id="fa459-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-148">Close the page.</span></span>
10. <span data-ttu-id="fa459-149">Klõpsake suvandit Protsessikaart.</span><span class="sxs-lookup"><span data-stu-id="fa459-149">Click Route card.</span></span>
11. <span data-ttu-id="fa459-150">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="fa459-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="fa459-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-151">Close the page.</span></span>
13. <span data-ttu-id="fa459-152">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fa459-152">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]