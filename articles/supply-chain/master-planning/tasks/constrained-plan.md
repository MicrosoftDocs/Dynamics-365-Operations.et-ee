---
title: Piirangutega plaani koostamine
description: Selles teemas selgitatakse, kuidas luua plaani, mis arvestab nii materiaalsete kui ka võimsuse piirangutega.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808012"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="07d68-103">Piirangutega plaani koostamine</span><span class="sxs-lookup"><span data-stu-id="07d68-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07d68-104">Selles teemas selgitatakse, kuidas luua plaani, mis arvestab nii materiaalsete kui ka võimsuse piirangutega.</span><span class="sxs-lookup"><span data-stu-id="07d68-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="07d68-105">Plaan tagab, et tootmine ei käivitu enne, kui materjalid on olemas ja ressursid pole üle broneeritud.</span><span class="sxs-lookup"><span data-stu-id="07d68-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="07d68-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="07d68-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07d68-107">See protseduur on mõeldud tootmisplaanijale.</span><span class="sxs-lookup"><span data-stu-id="07d68-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="07d68-108">Piirangutega plaani seadistamine</span><span class="sxs-lookup"><span data-stu-id="07d68-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="07d68-109">Avalehel valige tööruum **Koondplaneerimine**.</span><span class="sxs-lookup"><span data-stu-id="07d68-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="07d68-110">Valige tööruumi kõige parempoolsemalt küljelt linkide loendist **Koondplaan**.</span><span class="sxs-lookup"><span data-stu-id="07d68-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="07d68-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="07d68-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="07d68-112">Näide: **StaticPlan**</span><span class="sxs-lookup"><span data-stu-id="07d68-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="07d68-113">Valige väärtus **Jah** väljal **Piiratud võimsus**.</span><span class="sxs-lookup"><span data-stu-id="07d68-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="07d68-114">Väljale **Piiratud võimsuse ajapiir** sisestage `30`.</span><span class="sxs-lookup"><span data-stu-id="07d68-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="07d68-115">Laiendage jaotist **Ajapiir päevades**.</span><span class="sxs-lookup"><span data-stu-id="07d68-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="07d68-116">Valige väärtus **Jah** väljal **Võimsus**.</span><span class="sxs-lookup"><span data-stu-id="07d68-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="07d68-117">Väljale **Võimsuse plaanimise ajapiir (päevad)** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="07d68-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="07d68-118">Näide: `60`</span><span class="sxs-lookup"><span data-stu-id="07d68-118">Example: `60`</span></span>  
9. <span data-ttu-id="07d68-119">Valige väärtus **Jah** väljal **Arvutatud hilinemised**.</span><span class="sxs-lookup"><span data-stu-id="07d68-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="07d68-120">Väljale **Arvuta hilinemiste ajapiir (päevad)** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="07d68-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="07d68-121">Näide: `60`</span><span class="sxs-lookup"><span data-stu-id="07d68-121">Example: `60`</span></span> 
11. <span data-ttu-id="07d68-122">Laiendage jaotist **Arvutatud hilinemised**.</span><span class="sxs-lookup"><span data-stu-id="07d68-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="07d68-123">Valige väärtus **Jah** kõigile suvandi **Lisa arvutatud hilinemine vajaduse kuupäevale** väljadele.</span><span class="sxs-lookup"><span data-stu-id="07d68-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="07d68-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="07d68-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="07d68-125">Piirangutega plaani loomine</span><span class="sxs-lookup"><span data-stu-id="07d68-125">Create a constrained plan</span></span>
1. <span data-ttu-id="07d68-126">Valige käsk **Käitus**.</span><span class="sxs-lookup"><span data-stu-id="07d68-126">Select **Run**.</span></span>
2. <span data-ttu-id="07d68-127">Väljale **Koondplaan** sisestage või valige plaan, millele soovite seadistada piiranguid.</span><span class="sxs-lookup"><span data-stu-id="07d68-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="07d68-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="07d68-128">Select **OK**.</span></span>
4. <span data-ttu-id="07d68-129">Valige **Plaanitud tellimused**.</span><span class="sxs-lookup"><span data-stu-id="07d68-129">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]