---
title: Kulujaotuspoliitika loomine ja määramine kulujuhtimisüksusele
description: Kulujaotuse reeglite abil jaotatakse kulusid, mis on finantsiliselt koondkulukeskuses loendatud.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b269c731776e26df24658feedfa301181c309a14
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4969274"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="dbc45-103">Kulujaotuspoliitika loomine ja määramine kulujuhtimisüksusele</span><span class="sxs-lookup"><span data-stu-id="dbc45-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbc45-104">Kulujaotuse reeglite abil jaotatakse kulusid, mis on finantsiliselt koondkulukeskuses loendatud.</span><span class="sxs-lookup"><span data-stu-id="dbc45-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="dbc45-105">Kuluarvestaja tagab kulude jaotamise kulukeskustele valitud eraldamisaluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="dbc45-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="dbc45-106">Kulude juhtseadmele määratakse poliitika ja vastavad reeglid.</span><span class="sxs-lookup"><span data-stu-id="dbc45-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="dbc45-107">Selles tegevusjuhises näidatakse näite abil, kuidas luua kulude jaotamise poliitikat ja vastavaid reegleid.</span><span class="sxs-lookup"><span data-stu-id="dbc45-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="dbc45-108">Poliitika loomine</span><span class="sxs-lookup"><span data-stu-id="dbc45-108">Create a policy</span></span>
1. <span data-ttu-id="dbc45-109">Avage Kuluarvestus > Poliitikad > Kulude jaotamise poliitikad.</span><span class="sxs-lookup"><span data-stu-id="dbc45-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="dbc45-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-110">Click New.</span></span>
3. <span data-ttu-id="dbc45-111">Tippige väärtus väljale Poliitika nimi.</span><span class="sxs-lookup"><span data-stu-id="dbc45-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="dbc45-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dbc45-113">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="dbc45-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-114">Valige suvand Organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="dbc45-114">Select Organization.</span></span>  
6. <span data-ttu-id="dbc45-115">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="dbc45-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-116">Valige CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="dbc45-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="dbc45-117">Sisestage või valige väärtus väljal Statistiline dimensioon.</span><span class="sxs-lookup"><span data-stu-id="dbc45-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-118">Valige suvand Statistilised elemendid.</span><span class="sxs-lookup"><span data-stu-id="dbc45-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="dbc45-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dbc45-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="dbc45-120">Poliitika jaoks reeglite loomine</span><span class="sxs-lookup"><span data-stu-id="dbc45-120">Create rules for the policy</span></span>
1. <span data-ttu-id="dbc45-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-121">Click New.</span></span>
2. <span data-ttu-id="dbc45-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dbc45-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="dbc45-123">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="dbc45-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-124">Laiendage hierarhia väärtuse 094 valimiseks.</span><span class="sxs-lookup"><span data-stu-id="dbc45-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="dbc45-125">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="dbc45-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-126">Valige suvand Muud tegevuskulud ja seejärel 605110 Puhastus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="dbc45-127">Valige suvand väljal Kulukäitumine.</span><span class="sxs-lookup"><span data-stu-id="dbc45-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="dbc45-128">Valige suvand Fikseeritud omahind.</span><span class="sxs-lookup"><span data-stu-id="dbc45-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="dbc45-129">Sisestage või valige väärtus väljal Eraldamise alus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="dbc45-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-130">Click New.</span></span>
8. <span data-ttu-id="dbc45-131">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dbc45-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="dbc45-132">Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="dbc45-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-133">Laiendage hierarhia väärtuse 094 valimiseks.</span><span class="sxs-lookup"><span data-stu-id="dbc45-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="dbc45-134">Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.</span><span class="sxs-lookup"><span data-stu-id="dbc45-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="dbc45-135">Valige suvand Muud tegevuskulud ja seejärel 605150 Üür.</span><span class="sxs-lookup"><span data-stu-id="dbc45-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="dbc45-136">Valige suvand väljal Kulukäitumine.</span><span class="sxs-lookup"><span data-stu-id="dbc45-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="dbc45-137">Valige suvand Fikseeritud omahind.</span><span class="sxs-lookup"><span data-stu-id="dbc45-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="dbc45-138">Sisestage või valige väärtus väljal Eraldamise alus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="dbc45-139">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dbc45-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="dbc45-140">Reeglite määramine kulu juhtseadmele</span><span class="sxs-lookup"><span data-stu-id="dbc45-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="dbc45-141">Klõpskae kulu juhtseadme suvandit Poliitikamäärangud.</span><span class="sxs-lookup"><span data-stu-id="dbc45-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="dbc45-142">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="dbc45-142">Click New.</span></span>
3. <span data-ttu-id="dbc45-143">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dbc45-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dbc45-144">Sisestage kuupäev väljale Aruandluse alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="dbc45-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="dbc45-145">Valige sobiva finantsaasta 1. september.</span><span class="sxs-lookup"><span data-stu-id="dbc45-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="dbc45-146">Sisestage või valige väärtus väljal Kulu juhtseade.</span><span class="sxs-lookup"><span data-stu-id="dbc45-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="dbc45-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="dbc45-147">Click Save.</span></span>

