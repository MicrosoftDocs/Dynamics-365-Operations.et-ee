--- 
title: Tootmisvoo versiooni loomine
description: See protseduur keskendub uue tootmisvoo versiooni loomisele.
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="3c5aa-103">Tootmisvoo versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="3c5aa-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3c5aa-104">See protseduur keskendub uue tootmisvoo versiooni loomisele.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="3c5aa-105">Selle protseduuri puhul tuleb määratleda lean manufacturingi tootmisparameetrid ja klassiaja mõõtühikud.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="3c5aa-106">Peate määratlema ka väärtuse voo ja tootmisgrupi.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="3c5aa-107">Lisateavet tootmisvoogude ja lean manufacturingi tegevuste kohta vaadake Microsoft Dynamics AX-i lean manufacturingi tehnilistest ülevaadetest.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="3c5aa-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="3c5aa-109">Tootmisvoo loomine</span><span class="sxs-lookup"><span data-stu-id="3c5aa-109">Create a production flow</span></span>
1. <span data-ttu-id="3c5aa-110">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="3c5aa-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-111">Click New.</span></span>
3. <span data-ttu-id="3c5aa-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="3c5aa-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3c5aa-114">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3c5aa-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3c5aa-116">Valige väärtuse voo tüüpi tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="3c5aa-117">Väärtuse voog on tootmisüksus, mis hõlmab kõiki väärtuse voo tegevusi ja voogusid.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="3c5aa-118">Selles etapis on tootmisüksused piiratud juriidilise isikuga ja muid funktsioone neil pole.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="3c5aa-119">Klõpsake väljal Tootmisgrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3c5aa-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3c5aa-121">Valige tootmisvoole tootmisgrupp.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-121">Select a production group for the production flow.</span></span> <span data-ttu-id="3c5aa-122">Tootmisgrupid võimaldavad tootmisprotsessi jaoks materjali, tööjõu ja lõpetamata toodangu kontode määratlemise.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-122">Production groups allow the definition of material, labour, and WIP accounts for a production process.</span></span> <span data-ttu-id="3c5aa-123">Raamatupidamise konteksti seostamiseks tootmisvooga tuleb valida tootmisgrupp.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="3c5aa-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="3c5aa-125">Tootmisvoo versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="3c5aa-125">Create a production flow version</span></span>
1. <span data-ttu-id="3c5aa-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-126">Click Add.</span></span>
2. <span data-ttu-id="3c5aa-127">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="3c5aa-128">Vajaduse korral määratlege versiooni aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="3c5aa-129">Saate seda igal ajal värskendada isegi aktiivsete versioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="3c5aa-130">Saate selle abil planeerida versiooni kasutuselt kõrvaldamise.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="3c5aa-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-131">Click OK.</span></span>
4. <span data-ttu-id="3c5aa-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="3c5aa-133">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="3c5aa-134">Tehke taktiühiku toiming ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="3c5aa-135">Sisestage number väljale Keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="3c5aa-136">Määratlege versiooni keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="3c5aa-137">Tootmisvoo versiooni takti juhtimiseks määratlege suunatud keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="3c5aa-138">Takti määratletakse kogusena ajaperioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="3c5aa-139">Selles näiteks on takti aeg 0,2 tundi 10 tk kohta.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="3c5aa-140">Kaheksatunnise tööaja puhul vastab see igapäevasele läbilaskevõimele 400 tk.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="3c5aa-141">Sisestage number väljale Kogus tsükli kohta.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="3c5aa-142">Määratlege kogus tsükli kohta seoses keskmise takti ajaga.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="3c5aa-143">Laiendage jaotist Versiooni üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="3c5aa-144">Sisestage number väljale Minimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="3c5aa-145">Määratlege minimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-145">Define the minimum takt time.</span></span> <span data-ttu-id="3c5aa-146">Minimaalne takti aeg peab olema väiksem või sama kui keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="3c5aa-147">Sisestage number väljale Maksimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="3c5aa-148">Maksimaalne takti aeg peab olema suurem või sama kui keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="3c5aa-149">Sisestage number väljale Tegeliku tsükli aja periood (päevades)</span><span class="sxs-lookup"><span data-stu-id="3c5aa-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="3c5aa-150">Sisestage väljale Tegeliku tsükliaja periood päevade arv.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="3c5aa-151">Tegeliku tsükliaja periood on tegelikust minutist tagasisuunas koondatud tööde päevade arv tegeliku tsükliaja arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="3c5aa-152">Väärtust saab igal ajal muuta ja seda kasutatakse ainult tegelike tsükliaegade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="3c5aa-153">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3c5aa-153">Click Save.</span></span>


