---
title: Kontsernisisese plaani loomine
description: See protseduur näitab, kuidas luua kontsernisisest plaani.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978269"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="2513c-103">Kontsernisisese plaani loomine</span><span class="sxs-lookup"><span data-stu-id="2513c-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2513c-104">See protseduur näitab, kuidas luua kontsernisisest plaani.</span><span class="sxs-lookup"><span data-stu-id="2513c-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="2513c-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2513c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="2513c-106">Kontsernisisese plaanimisgrupi seadistamine</span><span class="sxs-lookup"><span data-stu-id="2513c-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="2513c-107">Paanil **Navigeerimispaan** avage **Moodulid > Koondplaneerimine > Kontsernisisesed plaanimisgrupid**.</span><span class="sxs-lookup"><span data-stu-id="2513c-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="2513c-108">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="2513c-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2513c-109">Näiteks saate filtrida välja Nimi väärtuse 10 järgi.</span><span class="sxs-lookup"><span data-stu-id="2513c-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="2513c-110">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2513c-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="2513c-111">Klõpsake  **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="2513c-111">Click **Delete**.</span></span> <span data-ttu-id="2513c-112">See etapp on vajalik kontsernisisese plaanimistsükli lühendamiseks.</span><span class="sxs-lookup"><span data-stu-id="2513c-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="2513c-113">Kontsernisisene plaanimine käivitab kõigis ettevõtetes koondplaneerimise plaanimisgrupis, alustades madalaimast plaanimisjärjestusest.</span><span class="sxs-lookup"><span data-stu-id="2513c-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="2513c-114">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="2513c-114">Click **Yes**.</span></span>
6. <span data-ttu-id="2513c-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2513c-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="2513c-116">Kontsernisisese plaani loomine</span><span class="sxs-lookup"><span data-stu-id="2513c-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="2513c-117">Paanil **Navigeerimispaan** avage **Moodulid > Koondplaneerimine > Tööruumid > Koondplaneerimine**.</span><span class="sxs-lookup"><span data-stu-id="2513c-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="2513c-118">Klõpsake **Kontsernisisene koondplaneerimine**.</span><span class="sxs-lookup"><span data-stu-id="2513c-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="2513c-119">Väljal **Kontsernisisene plaanimisgrupp** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="2513c-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="2513c-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2513c-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="2513c-121">Valige kontsernisisene plaanimisgrupp 10.</span><span class="sxs-lookup"><span data-stu-id="2513c-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="2513c-122">Väljale **Kontsernisisese plaanimise iteratsioonide arv** sisestage "2".</span><span class="sxs-lookup"><span data-stu-id="2513c-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="2513c-123">Kontsernisisesel plaanimisgrupil 10 on kaks liiget.</span><span class="sxs-lookup"><span data-stu-id="2513c-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="2513c-124">Selleks, et lisada lähteettevõtte (USMF) viivitused klientettevõtte (DEMF) ees, on vaja käivitada kontsernisisene plaanimine mõlemal ettevõttel kaks korda.</span><span class="sxs-lookup"><span data-stu-id="2513c-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="2513c-125">Esimene iteratsioon lisab nõudluse ja tuvastab viivitused lähteettevõttes (USMF).</span><span class="sxs-lookup"><span data-stu-id="2513c-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="2513c-126">Teine iteratsioon lisab viivitused USMF-ilt DEMF-ile.</span><span class="sxs-lookup"><span data-stu-id="2513c-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="2513c-127">Väljal **Esimene iteratsioon** valige "Taasloomine".</span><span class="sxs-lookup"><span data-stu-id="2513c-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="2513c-128">Väljal **Järgnevad iteratsioonid** valige "Taasloomine".</span><span class="sxs-lookup"><span data-stu-id="2513c-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="2513c-129">Väljale **Lõimede arv** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="2513c-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="2513c-130">See tähistab planeerimises kasutatavate paralleelsete lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="2513c-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="2513c-131">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="2513c-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="2513c-132">Plaani tulemuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="2513c-132">View the result of the plan</span></span>
1. <span data-ttu-id="2513c-133">Väljal **Plaan** klõpsake ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="2513c-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="2513c-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2513c-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="2513c-135">Klõpsake valiku StaticPlan linki.</span><span class="sxs-lookup"><span data-stu-id="2513c-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="2513c-136">Peate olema ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="2513c-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="2513c-137">Klõpsake **Plaanitud tellimused**.</span><span class="sxs-lookup"><span data-stu-id="2513c-137">Click **Planned orders**.</span></span>

