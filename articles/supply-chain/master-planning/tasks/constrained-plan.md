---
title: Piirangutega plaani koostamine
description: Selles protseduuris näitlikustatakse, kuidas luua plaani, mis võtab arvesse nii materjali kui ka võimsuse piiranguid.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "336033"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="e84e2-103">Piirangutega plaani koostamine</span><span class="sxs-lookup"><span data-stu-id="e84e2-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e84e2-104">Selles protseduuris näitlikustatakse, kuidas luua plaani, mis võtab arvesse nii materjali kui ka võimsuse piiranguid.</span><span class="sxs-lookup"><span data-stu-id="e84e2-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="e84e2-105">Plaan tagab, et tootmine ei käivitu enne, kui materjalid on olemas ja ressursid pole üle broneeritud.</span><span class="sxs-lookup"><span data-stu-id="e84e2-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="e84e2-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e84e2-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e84e2-107">See protseduur on mõeldud tootmisplaanijale.</span><span class="sxs-lookup"><span data-stu-id="e84e2-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="e84e2-108">Piirangutega plaani seadistamine</span><span class="sxs-lookup"><span data-stu-id="e84e2-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="e84e2-109">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="e84e2-109">Click Master planning.</span></span>
2. <span data-ttu-id="e84e2-110">Klõpsake valikul Koondplaneerimise plaanid.</span><span class="sxs-lookup"><span data-stu-id="e84e2-110">Click Master plans.</span></span>
3. <span data-ttu-id="e84e2-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e84e2-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e84e2-112">Näide: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="e84e2-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="e84e2-113">Valige väljal Piiratud võimsus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="e84e2-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="e84e2-114">Sisestage väärtus „30” väljale Piiratud võimsus.</span><span class="sxs-lookup"><span data-stu-id="e84e2-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="e84e2-115">Laiendage jaotist Ajapiirid päevades.</span><span class="sxs-lookup"><span data-stu-id="e84e2-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="e84e2-116">Valige väljal Võimsus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="e84e2-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="e84e2-117">Sisestage arv väljale Võimsuse plaanimise ajapiir (päevades).</span><span class="sxs-lookup"><span data-stu-id="e84e2-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="e84e2-118">Näide: 60</span><span class="sxs-lookup"><span data-stu-id="e84e2-118">Example: 60</span></span>  
9. <span data-ttu-id="e84e2-119">Valige väljal Arvutatud hilinemised suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="e84e2-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="e84e2-120">Sisestage arv väljale Hilinemiste ajapiiri arvutamine (päevades).</span><span class="sxs-lookup"><span data-stu-id="e84e2-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="e84e2-121">Näide: 60</span><span class="sxs-lookup"><span data-stu-id="e84e2-121">Example: 60</span></span>  
11. <span data-ttu-id="e84e2-122">Laiendage jaotist Arvutatud hilinemised.</span><span class="sxs-lookup"><span data-stu-id="e84e2-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="e84e2-123">Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="e84e2-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="e84e2-124">Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="e84e2-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="e84e2-125">Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="e84e2-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="e84e2-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e84e2-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="e84e2-127">Piirangutega plaani loomine</span><span class="sxs-lookup"><span data-stu-id="e84e2-127">Create a constrained plan</span></span>
1. <span data-ttu-id="e84e2-128">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="e84e2-128">Click Run.</span></span>
2. <span data-ttu-id="e84e2-129">Sisestage või valige väärtus väljal Koondplaan.</span><span class="sxs-lookup"><span data-stu-id="e84e2-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="e84e2-130">Valige plaan, millele olete piirangud seadistanud.</span><span class="sxs-lookup"><span data-stu-id="e84e2-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="e84e2-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e84e2-131">Click OK.</span></span>
    * <span data-ttu-id="e84e2-132">See võib veidi aega võtta.</span><span class="sxs-lookup"><span data-stu-id="e84e2-132">This may take a while.</span></span>  
4. <span data-ttu-id="e84e2-133">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="e84e2-133">Click Planned orders.</span></span>

