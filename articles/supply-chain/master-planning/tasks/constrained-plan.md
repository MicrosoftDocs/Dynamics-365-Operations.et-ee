--- 
title: Piirangutega plaani koostamine
description: "Selles protseduuris näitlikustatakse, kuidas luua plaani, mis võtab arvesse nii materjali kui ka võimsuse piiranguid."
author: ShylaThompson
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e19e51fa916e39a079ba9fd92d2b2ec03a2fe010
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="c4ed3-103">Piirangutega plaani koostamine</span><span class="sxs-lookup"><span data-stu-id="c4ed3-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4ed3-104">Selles protseduuris näitlikustatakse, kuidas luua plaani, mis võtab arvesse nii materjali kui ka võimsuse piiranguid.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="c4ed3-105">Plaan tagab, et tootmine ei käivitu enne, kui materjalid on olemas ja ressursid pole üle broneeritud.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="c4ed3-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="c4ed3-107">See protseduur on mõeldud tootmisplaanijale.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="c4ed3-108">Piirangutega plaani seadistamine</span><span class="sxs-lookup"><span data-stu-id="c4ed3-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="c4ed3-109">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-109">Click Master planning.</span></span>
2. <span data-ttu-id="c4ed3-110">Klõpsake valikul Koondplaneerimise plaanid.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-110">Click Master plans.</span></span>
3. <span data-ttu-id="c4ed3-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c4ed3-112">Näide: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="c4ed3-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="c4ed3-113">Valige väljal Piiratud võimsus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="c4ed3-114">Sisestage väärtus „30” väljale Piiratud võimsus.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="c4ed3-115">Laiendage jaotist Ajapiirid päevades.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="c4ed3-116">Valige väljal Võimsus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="c4ed3-117">Sisestage arv väljale Võimsuse plaanimise ajapiir (päevades).</span><span class="sxs-lookup"><span data-stu-id="c4ed3-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="c4ed3-118">Näide: 60</span><span class="sxs-lookup"><span data-stu-id="c4ed3-118">Example: 60</span></span>  
9. <span data-ttu-id="c4ed3-119">Valige väljal Arvutatud hilinemised suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="c4ed3-120">Sisestage arv väljale Hilinemiste ajapiiri arvutamine (päevades).</span><span class="sxs-lookup"><span data-stu-id="c4ed3-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="c4ed3-121">Näide: 60</span><span class="sxs-lookup"><span data-stu-id="c4ed3-121">Example: 60</span></span>  
11. <span data-ttu-id="c4ed3-122">Laiendage jaotist Arvutatud hilinemised.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="c4ed3-123">Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="c4ed3-124">Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="c4ed3-125">Valige suvand Jah väljal Arvutatud hilinemise lisamine vajaduse kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="c4ed3-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="c4ed3-127">Piirangutega plaani loomine</span><span class="sxs-lookup"><span data-stu-id="c4ed3-127">Create a constrained plan</span></span>
1. <span data-ttu-id="c4ed3-128">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-128">Click Run.</span></span>
2. <span data-ttu-id="c4ed3-129">Sisestage või valige väärtus väljal Koondplaan.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="c4ed3-130">Valige plaan, millele olete piirangud seadistanud.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="c4ed3-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-131">Click OK.</span></span>
    * <span data-ttu-id="c4ed3-132">See võib veidi aega võtta.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-132">This may take a while.</span></span>  
4. <span data-ttu-id="c4ed3-133">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="c4ed3-133">Click Planned orders.</span></span>


