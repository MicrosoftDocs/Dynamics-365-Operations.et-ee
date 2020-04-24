---
title: Tootmisvoo versiooni loomine
description: See protseduur keskendub uue tootmisvoo versiooni loomisele.
author: cvocph
manager: tfehr
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da3b77ed459f42ef91d64066b18b07fece9efc8f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3212131"
---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="d9a92-103">Tootmisvoo versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d9a92-103">Create a production flow version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9a92-104">See protseduur keskendub uue tootmisvoo versiooni loomisele.</span><span class="sxs-lookup"><span data-stu-id="d9a92-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="d9a92-105">Selle protseduuri puhul tuleb määratleda lean manufacturingi tootmisparameetrid ja klassiaja mõõtühikud.</span><span class="sxs-lookup"><span data-stu-id="d9a92-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="d9a92-106">Peate määratlema ka väärtuse voo ja tootmisgrupi.</span><span class="sxs-lookup"><span data-stu-id="d9a92-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="d9a92-107">Lisateavet tootmisvoogude ja lean manufacturingi tegevuste kohta vaadake Microsoft Dynamics AX-i lean manufacturingi tehnilistest ülevaadetest.</span><span class="sxs-lookup"><span data-stu-id="d9a92-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="d9a92-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d9a92-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="d9a92-109">Tootmisvoo loomine</span><span class="sxs-lookup"><span data-stu-id="d9a92-109">Create a production flow</span></span>
1. <span data-ttu-id="d9a92-110">Minge jaotisse Tootmise juhtimine > Seadistus > Kulusäästlik tootmisvoog > Tootmisvood.</span><span class="sxs-lookup"><span data-stu-id="d9a92-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="d9a92-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d9a92-111">Click New.</span></span>
3. <span data-ttu-id="d9a92-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d9a92-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d9a92-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d9a92-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d9a92-114">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d9a92-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d9a92-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d9a92-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d9a92-116">Valige väärtuse voo tüüpi tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="d9a92-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="d9a92-117">Väärtuse voog on tootmisüksus, mis hõlmab kõiki väärtuse voo tegevusi ja voogusid.</span><span class="sxs-lookup"><span data-stu-id="d9a92-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="d9a92-118">Selles etapis on tootmisüksused piiratud juriidilise isikuga ja muid funktsioone neil pole.</span><span class="sxs-lookup"><span data-stu-id="d9a92-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="d9a92-119">Klõpsake väljal Tootmisgrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d9a92-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="d9a92-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d9a92-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d9a92-121">Valige tootmisvoole tootmisgrupp.</span><span class="sxs-lookup"><span data-stu-id="d9a92-121">Select a production group for the production flow.</span></span> <span data-ttu-id="d9a92-122">Tootmisgrupid võimaldavad tootmisprotsessi jaoks materjali, tööjõu ja lõpetamata toodangu kontode määratlemist.</span><span class="sxs-lookup"><span data-stu-id="d9a92-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="d9a92-123">Raamatupidamise konteksti seostamiseks tootmisvooga tuleb valida tootmisgrupp.</span><span class="sxs-lookup"><span data-stu-id="d9a92-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="d9a92-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="d9a92-125">Tootmisvoo versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="d9a92-125">Create a production flow version</span></span>
1. <span data-ttu-id="d9a92-126">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="d9a92-126">Click Add.</span></span>
2. <span data-ttu-id="d9a92-127">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d9a92-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="d9a92-128">Vajaduse korral määratlege versiooni aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d9a92-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="d9a92-129">Saate seda igal ajal värskendada isegi aktiivsete versioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="d9a92-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="d9a92-130">Saate selle abil planeerida versiooni kasutuselt kõrvaldamise.</span><span class="sxs-lookup"><span data-stu-id="d9a92-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="d9a92-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d9a92-131">Click OK.</span></span>
4. <span data-ttu-id="d9a92-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d9a92-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="d9a92-133">Sisestage väärtus väljale Ühik.</span><span class="sxs-lookup"><span data-stu-id="d9a92-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="d9a92-134">Tehke taktiühiku toiming ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="d9a92-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="d9a92-135">Sisestage number väljale Keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="d9a92-136">Määratlege versiooni keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="d9a92-137">Tootmisvoo versiooni takti juhtimiseks määratlege suunatud keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="d9a92-138">Takti määratletakse kogusena ajaperioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="d9a92-139">Selles näiteks on takti aeg 0,2 tundi 10 tk kohta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="d9a92-140">Kaheksatunnise tööaja puhul vastab see igapäevasele läbilaskevõimele 400 tk.</span><span class="sxs-lookup"><span data-stu-id="d9a92-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="d9a92-141">Sisestage number väljale Kogus tsükli kohta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="d9a92-142">Määratlege kogus tsükli kohta seoses keskmise takti ajaga.</span><span class="sxs-lookup"><span data-stu-id="d9a92-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="d9a92-143">Laiendage jaotist Versiooni üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="d9a92-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="d9a92-144">Sisestage number väljale Minimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="d9a92-145">Määratlege minimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-145">Define the minimum takt time.</span></span> <span data-ttu-id="d9a92-146">Minimaalne takti aeg peab olema väiksem või sama kui keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="d9a92-147">Sisestage number väljale Maksimaalne takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="d9a92-148">Maksimaalne takti aeg peab olema suurem või sama kui keskmine takti aeg.</span><span class="sxs-lookup"><span data-stu-id="d9a92-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="d9a92-149">Sisestage number väljale Tegeliku tsükli aja periood (päevades)</span><span class="sxs-lookup"><span data-stu-id="d9a92-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="d9a92-150">Sisestage väljale Tegeliku tsükliaja periood päevade arv.</span><span class="sxs-lookup"><span data-stu-id="d9a92-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="d9a92-151">Tegeliku tsükliaja periood on tegelikust minutist tagasisuunas koondatud tööde päevade arv tegeliku tsükliaja arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d9a92-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="d9a92-152">Väärtust saab igal ajal muuta ja seda kasutatakse ainult tegelike tsükliaegade arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d9a92-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="d9a92-153">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d9a92-153">Click Save.</span></span>

