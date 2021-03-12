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
ms.search.form: JmgRegistrationStartJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9822dd66876ef8ed6bbcd5846a39d69d2446d7a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981069"
---
# <a name="start-a-production-order"></a><span data-ttu-id="c1756-103">Tootmistellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="c1756-103">Start a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1756-104">See protseduur selgitab, kuidas alustada tootmistellimust tööde juhtimisel.</span><span class="sxs-lookup"><span data-stu-id="c1756-104">This procedure shows how to start a production order on the shop floor.</span></span> <span data-ttu-id="c1756-105">Selles protsessis edastatakse aja- ja materjalitarbimine.</span><span class="sxs-lookup"><span data-stu-id="c1756-105">Time and material consumption are reported in this process.</span></span> <span data-ttu-id="c1756-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c1756-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c1756-107">See on viies protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="c1756-107">This is the fifth procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="start-a-production-order"></a><span data-ttu-id="c1756-108">Tootmistellimuse alustamine</span><span class="sxs-lookup"><span data-stu-id="c1756-108">Start a production order</span></span>
1. <span data-ttu-id="c1756-109">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="c1756-109">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="c1756-110">Valige tootmistellimus, mille olek on Väljastatud.</span><span class="sxs-lookup"><span data-stu-id="c1756-110">Select a production order that has the Released status.</span></span>  
2. <span data-ttu-id="c1756-111">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="c1756-111">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="c1756-112">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="c1756-112">Click Start.</span></span>
    * <span data-ttu-id="c1756-113">Sellel lehel saate kinnitada tootmistellimuse alguse.</span><span class="sxs-lookup"><span data-stu-id="c1756-113">On this page, you can confirm the start of the production order.</span></span>  
4. <span data-ttu-id="c1756-114">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="c1756-114">Click the General tab.</span></span>
5. <span data-ttu-id="c1756-115">Sisestage väljale Alates oper.</span><span class="sxs-lookup"><span data-stu-id="c1756-115">In the From Oper.</span></span> <span data-ttu-id="c1756-116">Nr</span><span class="sxs-lookup"><span data-stu-id="c1756-116">No.</span></span> <span data-ttu-id="c1756-117">number '10'.</span><span class="sxs-lookup"><span data-stu-id="c1756-117">field, enter '10'.</span></span>
6. <span data-ttu-id="c1756-118">Valige väljal Automaatne protsessi tarbimine suvand Alati.</span><span class="sxs-lookup"><span data-stu-id="c1756-118">In the Automatic route consumption field, select 'Always'.</span></span>
7. <span data-ttu-id="c1756-119">Märkige ruut Sisesta protsessikaart kohe.</span><span class="sxs-lookup"><span data-stu-id="c1756-119">Click the Post route card now checkbox.</span></span>
8. <span data-ttu-id="c1756-120">Valige väljal Automaatne koosluse tarbimine suvand Alati.</span><span class="sxs-lookup"><span data-stu-id="c1756-120">In the Automatic BOM consumption field, select 'Always'.</span></span>
9. <span data-ttu-id="c1756-121">Märkige ruut Sisesta komplekteerimisleht kohe.</span><span class="sxs-lookup"><span data-stu-id="c1756-121">Click the Post picking list now checkbox.</span></span>
10. <span data-ttu-id="c1756-122">Märkige ruut Prindi komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="c1756-122">Click the Print picking list checkbox.</span></span>
11. <span data-ttu-id="c1756-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c1756-123">Click OK.</span></span>
    * <span data-ttu-id="c1756-124">See on trükitud komplekteerimisleht, millel on toodud tootmistellimuse jaoks kasutatud materjalid.</span><span class="sxs-lookup"><span data-stu-id="c1756-124">This is the printed picking list that shows the materials used for the production order.</span></span>  
12. <span data-ttu-id="c1756-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1756-125">Close the page.</span></span>

## <a name="validate-the-picking-list"></a><span data-ttu-id="c1756-126">Komplekteerimislehe kinnitamine</span><span class="sxs-lookup"><span data-stu-id="c1756-126">Validate the picking list</span></span>
1. <span data-ttu-id="c1756-127">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="c1756-127">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="c1756-128">Klõpsake suvandit Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="c1756-128">Click Picking list.</span></span>
3. <span data-ttu-id="c1756-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c1756-129">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c1756-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c1756-130">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c1756-131">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c1756-131">Click Edit.</span></span>
6. <span data-ttu-id="c1756-132">Sisestage number väljale Tarbimine.</span><span class="sxs-lookup"><span data-stu-id="c1756-132">In the Consumption field, enter a number.</span></span>
7. <span data-ttu-id="c1756-133">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="c1756-133">Click Post.</span></span>
8. <span data-ttu-id="c1756-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c1756-134">Click OK.</span></span>
    * <span data-ttu-id="c1756-135">Komplekteerimislehe töölehele sisestatakse tootmistellimuse tarbitud materjalid.</span><span class="sxs-lookup"><span data-stu-id="c1756-135">In the picking list journal, the materials consumed by the production order are posted.</span></span> <span data-ttu-id="c1756-136">Enne töölehe sisestamist saate teha korrigeerimisi, kui eeldatav kogus erineb tegelikust tarbitud kogusest.</span><span class="sxs-lookup"><span data-stu-id="c1756-136">Before posting the journal, you can make adjustments if there is a difference between the estimated quantity and the actual consumed quantity.</span></span>  
9. <span data-ttu-id="c1756-137">Klõpsake vahekaarti GridPanel.</span><span class="sxs-lookup"><span data-stu-id="c1756-137">Click the GridPanel tab.</span></span>
10. <span data-ttu-id="c1756-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1756-138">Close the page.</span></span>

## <a name="verify-the-route-card-journal"></a><span data-ttu-id="c1756-139">Protsessikaardi töölehe kontrollimine</span><span class="sxs-lookup"><span data-stu-id="c1756-139">Verify the route card journal</span></span>
1. <span data-ttu-id="c1756-140">Klõpsake toimingupaanil valikut Kuva.</span><span class="sxs-lookup"><span data-stu-id="c1756-140">On the Action Pane, click View.</span></span>
2. <span data-ttu-id="c1756-141">Klõpsake suvandit Protsessikaart.</span><span class="sxs-lookup"><span data-stu-id="c1756-141">Click Route card.</span></span>
3. <span data-ttu-id="c1756-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c1756-142">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c1756-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c1756-143">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c1756-144">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="c1756-144">Click Edit.</span></span>
6. <span data-ttu-id="c1756-145">Sisestage number väljale Tunnid.</span><span class="sxs-lookup"><span data-stu-id="c1756-145">In the Hours field, enter a number.</span></span>
7. <span data-ttu-id="c1756-146">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="c1756-146">Click Post.</span></span>
8. <span data-ttu-id="c1756-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c1756-147">Click OK.</span></span>
    * <span data-ttu-id="c1756-148">Protsessikaardi töölehele kantakse üksikutele toimingutele kulunud aeg.</span><span class="sxs-lookup"><span data-stu-id="c1756-148">In the Route card journal, the time spent on the individual operations is recorded.</span></span> <span data-ttu-id="c1756-149">Saate esitada ka õige ja veakoguse.</span><span class="sxs-lookup"><span data-stu-id="c1756-149">Good and error quantity can also be reported.</span></span>  
