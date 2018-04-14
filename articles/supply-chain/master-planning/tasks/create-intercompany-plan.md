--- 
title: Kontsernisisese plaani loomine
description: "See protseduur näitab, kuidas luua kontsernisisest plaani."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b5ed1b47e3e0142a18761f5a47ca12a388305308
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="feee6-103">Kontsernisisese plaani loomine</span><span class="sxs-lookup"><span data-stu-id="feee6-103">Create an intercompany plan</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="feee6-104">See protseduur näitab, kuidas luua kontsernisisest plaani.</span><span class="sxs-lookup"><span data-stu-id="feee6-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="feee6-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="feee6-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="feee6-106">Kontsernisisese plaanimisgrupi seadistamine</span><span class="sxs-lookup"><span data-stu-id="feee6-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="feee6-107">Avage jaotis Kontsernisisesed plaanimisgrupid.</span><span class="sxs-lookup"><span data-stu-id="feee6-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="feee6-108">Koondplaneerimine > Seadistus > Kontsernisisesed plaanimisgrupid</span><span class="sxs-lookup"><span data-stu-id="feee6-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="feee6-109">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="feee6-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="feee6-110">Näiteks saate filtrida välja Nimi väärtuse 10 järgi.</span><span class="sxs-lookup"><span data-stu-id="feee6-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="feee6-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="feee6-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="feee6-112">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="feee6-112">Click Delete.</span></span>
    * <span data-ttu-id="feee6-113">See etapp on vajalik kontsernisisese plaanimistsükli lühendamiseks.</span><span class="sxs-lookup"><span data-stu-id="feee6-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="feee6-114">Kontsernisisene plaanimine käivitab kõigis ettevõtetes koondplaneerimise plaanimisgrupis, alustades madalaimast plaanimisjärjestusest.</span><span class="sxs-lookup"><span data-stu-id="feee6-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="feee6-115">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="feee6-115">Click Yes.</span></span>
6. <span data-ttu-id="feee6-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="feee6-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="feee6-117">Kontsernisisese plaani loomine</span><span class="sxs-lookup"><span data-stu-id="feee6-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="feee6-118">Klõpsake valikut Kontsernisisene koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="feee6-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="feee6-119">See on koondplaneerimise tööruumis.</span><span class="sxs-lookup"><span data-stu-id="feee6-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="feee6-120">Klõpsake väljal Kontsernisisene plaanimisgrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="feee6-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="feee6-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="feee6-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="feee6-122">Valige kontsernisisene plaanimisgrupp 10.</span><span class="sxs-lookup"><span data-stu-id="feee6-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="feee6-123">Sisestage väljale Plaanitud kontsernisiseste iteratsioonide arv number 2.</span><span class="sxs-lookup"><span data-stu-id="feee6-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="feee6-124">Kontsernisisesel plaanimisgrupil 10 on kaks liiget.</span><span class="sxs-lookup"><span data-stu-id="feee6-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="feee6-125">Selleks, et lisada lähteettevõtte (USMF) viivitused klientettevõtte (DEMF) ees, on vaja käivitada kontsernisisene plaanimine mõlemal ettevõttel kaks korda.</span><span class="sxs-lookup"><span data-stu-id="feee6-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="feee6-126">Esimene iteratsioon lisab nõudluse ja tuvastab viivitused lähteettevõttes (USMF).</span><span class="sxs-lookup"><span data-stu-id="feee6-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="feee6-127">Teine iteratsioon lisab viivitused USMF-ilt DEMF-ile.</span><span class="sxs-lookup"><span data-stu-id="feee6-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="feee6-128">Tehke valik väljal Esimene iteratsioon.</span><span class="sxs-lookup"><span data-stu-id="feee6-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="feee6-129">Valige Taasloomine väljalt Esimene iteratsioon.</span><span class="sxs-lookup"><span data-stu-id="feee6-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="feee6-130">Valige Taasloomine väljalt Järgnevad iteratsioonid.</span><span class="sxs-lookup"><span data-stu-id="feee6-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="feee6-131">Sisestage number väljale Lõimede arv.</span><span class="sxs-lookup"><span data-stu-id="feee6-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="feee6-132">See tähistab planeerimises kasutatavate paralleelsete lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="feee6-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="feee6-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="feee6-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="feee6-134">Plaani tulemuse vaatamine</span><span class="sxs-lookup"><span data-stu-id="feee6-134">View the result of the plan</span></span>
1. <span data-ttu-id="feee6-135">Klõpsake väljal Plaan otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="feee6-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="feee6-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="feee6-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="feee6-137">Klõpsake valiku StaticPlan linki.</span><span class="sxs-lookup"><span data-stu-id="feee6-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="feee6-138">Peate olema ettevõttes USMF.</span><span class="sxs-lookup"><span data-stu-id="feee6-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="feee6-139">Klõpsake valikut Planeeritud tellimused.</span><span class="sxs-lookup"><span data-stu-id="feee6-139">Click Planned orders.</span></span>


