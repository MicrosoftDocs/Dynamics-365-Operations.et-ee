---
title: Kontsernisisese plaani loomine
description: See protseduur näitab, kuidas luua kontsernisisest plaani.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 194bb78eed5a673030f7cead031cf286cddbe77c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845205"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="dd208-103">Kontsernisisese plaani loomine</span><span class="sxs-lookup"><span data-stu-id="dd208-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd208-104">See protseduur näitab, kuidas luua kontsernisisest plaani.</span><span class="sxs-lookup"><span data-stu-id="dd208-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="dd208-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="dd208-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="dd208-106">Kontsernisisese plaanimisgrupi seadistamine</span><span class="sxs-lookup"><span data-stu-id="dd208-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="dd208-107">Avage jaotis Kontsernisisesed plaanimisgrupid.</span><span class="sxs-lookup"><span data-stu-id="dd208-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="dd208-108">Koondplaneerimine > Seadistus > Kontsernisisesed plaanimisgrupid</span><span class="sxs-lookup"><span data-stu-id="dd208-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="dd208-109">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="dd208-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="dd208-110">Näiteks saate filtrida välja Nimi väärtuse 10 järgi.</span><span class="sxs-lookup"><span data-stu-id="dd208-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="dd208-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="dd208-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dd208-112">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="dd208-112">Click Delete.</span></span>
    * <span data-ttu-id="dd208-113">See etapp on vajalik kontsernisisese plaanimistsükli lühendamiseks.</span><span class="sxs-lookup"><span data-stu-id="dd208-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="dd208-114">Kontsernisisene plaanimine käivitab kõigis ettevõtetes koondplaneerimise plaanimisgrupis, alustades madalaimast plaanimisjärjestusest.</span><span class="sxs-lookup"><span data-stu-id="dd208-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="dd208-115">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="dd208-115">Click Yes.</span></span>
6. <span data-ttu-id="dd208-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="dd208-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="dd208-117">Kontsernisisese plaani loomine</span><span class="sxs-lookup"><span data-stu-id="dd208-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="dd208-118">Klõpsake valikut Kontsernisisene koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="dd208-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="dd208-119">See on koondplaneerimise tööruumis.</span><span class="sxs-lookup"><span data-stu-id="dd208-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="dd208-120">Klõpsake väljal Kontsernisisene plaanimisgrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="dd208-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="dd208-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dd208-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd208-122">Valige kontsernisisene plaanimisgrupp 10.</span><span class="sxs-lookup"><span data-stu-id="dd208-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="dd208-123">Sisestage väljale Plaanitud kontsernisiseste iteratsioonide arv number 2.</span><span class="sxs-lookup"><span data-stu-id="dd208-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="dd208-124">Kontsernisisesel plaanimisgrupil 10 on kaks liiget.</span><span class="sxs-lookup"><span data-stu-id="dd208-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="dd208-125">Selleks, et lisada lähteettevõtte (USMF) viivitused klientettevõtte (DEMF) ees, on vaja käivitada kontsernisisene plaanimine mõlemal ettevõttel kaks korda.</span><span class="sxs-lookup"><span data-stu-id="dd208-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="dd208-126">Esimene iteratsioon lisab nõudluse ja tuvastab viivitused lähteettevõttes (USMF).</span><span class="sxs-lookup"><span data-stu-id="dd208-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="dd208-127">Teine iteratsioon lisab viivitused USMF-ilt DEMF-ile.</span><span class="sxs-lookup"><span data-stu-id="dd208-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="dd208-128">Tehke valik väljal Esimene iteratsioon.</span><span class="sxs-lookup"><span data-stu-id="dd208-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="dd208-129">Valige Taasloomine väljalt Esimene iteratsioon.</span><span class="sxs-lookup"><span data-stu-id="dd208-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="dd208-130">Valige Taasloomine väljalt Järgnevad iteratsioonid.</span><span class="sxs-lookup"><span data-stu-id="dd208-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="dd208-131">Sisestage number väljale Lõimede arv.</span><span class="sxs-lookup"><span data-stu-id="dd208-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="dd208-132">See tähistab planeerimises kasutatavate paralleelsete lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="dd208-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="dd208-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="dd208-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="dd208-134">Plaani tulemuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="dd208-134">View the result of the plan</span></span>
1. <span data-ttu-id="dd208-135">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="dd208-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="dd208-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="dd208-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dd208-137">Klõpsake valiku StaticPlan linki.</span><span class="sxs-lookup"><span data-stu-id="dd208-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="dd208-138">Peate olema ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="dd208-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="dd208-139">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="dd208-139">Click Planned orders.</span></span>

