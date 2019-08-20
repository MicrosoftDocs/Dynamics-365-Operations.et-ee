---
title: Tootmisvoo ja versiooni kinnitamine
description: See protseduur kirjeldab, kuidas luua uus tootmisvoog ja esimene versioon lean manufacturingi jaoks.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 523f6414ec212aef48eece487f4199ea2cf4b87e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836143"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="d5566-103">Tootmisvoo ja versiooni kinnitamine</span><span class="sxs-lookup"><span data-stu-id="d5566-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5566-104">See protseduur kirjeldab, kuidas luua uus tootmisvoog ja esimene versioon lean manufacturingi jaoks.</span><span class="sxs-lookup"><span data-stu-id="d5566-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="d5566-105">Eeltingimused: Tuleb määratleda lean manufacturingi tootmisparameetrid ja klassiaja mõõtühikud.</span><span class="sxs-lookup"><span data-stu-id="d5566-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="d5566-106">Peate määratlema ka Väärtuse voo ja Tootmisgrupi.</span><span class="sxs-lookup"><span data-stu-id="d5566-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="d5566-107">Tootmisvoogude ja tegevuste kontseptsioonidega tutvumiseks vaadake lean manufacturingi ülevaateid.</span><span class="sxs-lookup"><span data-stu-id="d5566-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="d5566-108">See protseduur viitab demoandmetes juriidilisele isikule USMF.</span><span class="sxs-lookup"><span data-stu-id="d5566-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="d5566-109">Eeldusel, et juriidiline isik on seadistatud lean manufacturingi jaoks, võib samas kasutada teisi juriidilisi isikuid.</span><span class="sxs-lookup"><span data-stu-id="d5566-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="d5566-110">Tootmisvoo loomine</span><span class="sxs-lookup"><span data-stu-id="d5566-110">Create a production flow</span></span>
1. <span data-ttu-id="d5566-111">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="d5566-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d5566-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5566-112">Click New.</span></span>
3. <span data-ttu-id="d5566-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5566-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d5566-114">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d5566-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d5566-115">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d5566-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d5566-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d5566-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d5566-117">Väärtuse voog on tootmisüksus, mis hõlmab kõiki väärtuse voo tegevusi ja voogusid.</span><span class="sxs-lookup"><span data-stu-id="d5566-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="d5566-118">Selles etapis on tootmisüksused piiratud juriidilise isikuga ja muid funktsioone neil pole.</span><span class="sxs-lookup"><span data-stu-id="d5566-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="d5566-119">Klõpsake väljal Tootmisgrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d5566-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d5566-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d5566-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d5566-121">Tootmisgrupid võimaldavad tootmisprotsessi jaoks materjali, tööjõu ja lõpetamata toodangu kontode määratlemist.</span><span class="sxs-lookup"><span data-stu-id="d5566-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="d5566-122">Raamatupidamise konteksti seostamiseks tootmisvooga tuleb valida tootmisgrupp.</span><span class="sxs-lookup"><span data-stu-id="d5566-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="d5566-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5566-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="d5566-124">Tootmisvoo versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d5566-124">Create a production flow version</span></span>
1. <span data-ttu-id="d5566-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d5566-125">Click Add.</span></span>
2. <span data-ttu-id="d5566-126">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d5566-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="d5566-127">Saate värskendada versiooni aegumiskuupäeva igal ajal ja isegi aktiivsete versioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="d5566-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="d5566-128">Versiooni aegumiskuupäeva abil saate plaanida versiooni kasutusest kõrvaldamist.</span><span class="sxs-lookup"><span data-stu-id="d5566-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="d5566-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d5566-129">Click OK.</span></span>
4. <span data-ttu-id="d5566-130">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d5566-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d5566-131">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="d5566-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="d5566-132">Valige taktiühik.</span><span class="sxs-lookup"><span data-stu-id="d5566-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="d5566-133">Sisestage number väljale Keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d5566-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="d5566-134">Tootmisvoo versiooni takti juhtimiseks määratlege suunatud keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d5566-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="d5566-135">Takti määratletakse kogusena ajaperioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="d5566-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="d5566-136">Selles näiteks on takti aeg 0,2 tundi 10 tk kohta.</span><span class="sxs-lookup"><span data-stu-id="d5566-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="d5566-137">Kaheksatunnise tööaja puhul vastab see igapäevasele läbilaskevõimele 400 tk.</span><span class="sxs-lookup"><span data-stu-id="d5566-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="d5566-138">Sisestage number väljale Kogus tsükli kohta.</span><span class="sxs-lookup"><span data-stu-id="d5566-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="d5566-139">Laiendage või ahendage jaotist Versiooni üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d5566-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="d5566-140">Sisestage number väljale Minimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d5566-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="d5566-141">Minimaalne takti aeg peab olema väiksem või sama kui keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d5566-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="d5566-142">Sisestage number väljale Maksimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d5566-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="d5566-143">Maksimaalne takti aeg peab olema suurem või sama kui keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d5566-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="d5566-144">Sisestage väljale Tegeliku tsükliaja periood päevade arv</span><span class="sxs-lookup"><span data-stu-id="d5566-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="d5566-145">Tegeliku tsükliaja periood on tegelikust minutist tagasisuunas koondatud tööde päevade arv tegeliku tsükliaja arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5566-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="d5566-146">Väärtust saab igal ajal muuta ja seda kasutatakse ainult tegelike tsükliaegade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5566-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="d5566-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5566-147">Click Save.</span></span>

