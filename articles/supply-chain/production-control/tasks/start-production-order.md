---
title: Tootmistellimuse alustamine
description: See protseduur selgitab, kuidas alustada tootmistellimust tööde juhtimisel.
author: johanhoffmann
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e444f6c521c47964b9b9b864b62fb486102c2fc7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210383"
---
# <a name="start-a-production-order"></a><span data-ttu-id="f4b80-103">Tootmistellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="f4b80-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4b80-104">See protseduur selgitab, kuidas alustada tootmistellimust tööde juhtimisel.</span><span class="sxs-lookup"><span data-stu-id="f4b80-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="f4b80-105">Selles protsessis edastatakse aja- ja materjalitarbimine.</span><span class="sxs-lookup"><span data-stu-id="f4b80-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="f4b80-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f4b80-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f4b80-107">See on viies protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="f4b80-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="f4b80-108">Tootmistellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="f4b80-108">Start a production order</span></span>
1. <span data-ttu-id="f4b80-109">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="f4b80-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="f4b80-110">Valige tootmistellimus, mille olek on Väljastatud.</span><span class="sxs-lookup"><span data-stu-id="f4b80-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="f4b80-111">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="f4b80-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="f4b80-112">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="f4b80-112">Click Start.</span></span>
    * <span data-ttu-id="f4b80-113">Sellel lehel saate kinnitada tootmistellimuse alguse.</span><span class="sxs-lookup"><span data-stu-id="f4b80-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="f4b80-114">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="f4b80-114">Click the General tab.</span></span>
5. <span data-ttu-id="f4b80-115">Sisestage väljale Alates oper.</span><span class="sxs-lookup"><span data-stu-id="f4b80-115">In the From Oper.</span></span> <span data-ttu-id="f4b80-116">Nr</span><span class="sxs-lookup"><span data-stu-id="f4b80-116">No.</span></span> <span data-ttu-id="f4b80-117">number '10'.</span><span class="sxs-lookup"><span data-stu-id="f4b80-117">field, enter '10'.</span></span>
6. <span data-ttu-id="f4b80-118">Valige väljal Automaatne protsessi tarbimine suvand Alati.</span><span class="sxs-lookup"><span data-stu-id="f4b80-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="f4b80-119">Märkige ruut Sisesta protsessikaart kohe.</span><span class="sxs-lookup"><span data-stu-id="f4b80-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="f4b80-120">Valige väljal Automaatne koosluse tarbimine suvand Alati.</span><span class="sxs-lookup"><span data-stu-id="f4b80-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="f4b80-121">Märkige ruut Sisesta komplekteerimisleht kohe.</span><span class="sxs-lookup"><span data-stu-id="f4b80-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="f4b80-122">Märkige ruut Prindi komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="f4b80-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="f4b80-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f4b80-123">Click OK.</span></span>
    * <span data-ttu-id="f4b80-124">See on trükitud komplekteerimisleht, millel on toodud tootmistellimuse jaoks kasutatud materjalid.</span><span class="sxs-lookup"><span data-stu-id="f4b80-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="f4b80-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f4b80-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="f4b80-126">Komplekteerimislehe kinnitamine</span><span class="sxs-lookup"><span data-stu-id="f4b80-126">Validate the picking list</span></span>
1. <span data-ttu-id="f4b80-127">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="f4b80-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f4b80-128">Klõpsake suvandit Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="f4b80-128">Click Picking list.</span></span>
3. <span data-ttu-id="f4b80-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f4b80-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f4b80-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f4b80-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f4b80-131">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f4b80-131">Click Edit.</span></span>
6. <span data-ttu-id="f4b80-132">Sisestage number väljale Tarbimine.</span><span class="sxs-lookup"><span data-stu-id="f4b80-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="f4b80-133">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="f4b80-133">Click Post.</span></span>
8. <span data-ttu-id="f4b80-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f4b80-134">Click OK.</span></span>
    * <span data-ttu-id="f4b80-135">Komplekteerimislehe töölehele sisestatakse tootmistellimuse tarbitud materjalid.</span><span class="sxs-lookup"><span data-stu-id="f4b80-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="f4b80-136">Enne töölehe sisestamist saate teha korrigeerimisi, kui eeldatav kogus erineb tegelikust tarbitud kogusest.</span><span class="sxs-lookup"><span data-stu-id="f4b80-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="f4b80-137">Klõpsake vahekaarti GridPanel.</span><span class="sxs-lookup"><span data-stu-id="f4b80-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="f4b80-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f4b80-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="f4b80-139">Protsessikaardi töölehe kontrollimine</span><span class="sxs-lookup"><span data-stu-id="f4b80-139">Verify the route card journal</span></span>
1. <span data-ttu-id="f4b80-140">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="f4b80-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="f4b80-141">Klõpsake suvandit Protsessikaart.</span><span class="sxs-lookup"><span data-stu-id="f4b80-141">Click Route card.</span></span>
3. <span data-ttu-id="f4b80-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f4b80-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f4b80-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f4b80-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f4b80-144">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f4b80-144">Click Edit.</span></span>
6. <span data-ttu-id="f4b80-145">Sisestage number väljale Tunnid.</span><span class="sxs-lookup"><span data-stu-id="f4b80-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="f4b80-146">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="f4b80-146">Click Post.</span></span>
8. <span data-ttu-id="f4b80-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f4b80-147">Click OK.</span></span>
    * <span data-ttu-id="f4b80-148">Protsessikaardi töölehele kantakse üksikutele toimingutele kulunud aeg.</span><span class="sxs-lookup"><span data-stu-id="f4b80-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="f4b80-149">Saate esitada ka õige ja veakoguse.</span><span class="sxs-lookup"><span data-stu-id="f4b80-149">Good and error quantity can also be reported.</span></span>  
