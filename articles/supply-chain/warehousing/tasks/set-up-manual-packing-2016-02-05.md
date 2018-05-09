--- 
title: "Käsitsi pakkimise seadistamine (ainult veebruar ja mai 2016)"
description: "Pakkimisprotsess võimaldab toodete kinnitamist ja pakendamist konteineritesse."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 714fd4762ae54f8f6638e81dd19fdd636091b88e
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="d180d-103">Käsitsi pakkimise seadistamine (ainult veebruar ja mai 2016)</span><span class="sxs-lookup"><span data-stu-id="d180d-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d180d-104">Pakkimisprotsess võimaldab toodete kinnitamist ja pakendamist konteineritesse.</span><span class="sxs-lookup"><span data-stu-id="d180d-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="d180d-105">Selle protsessi käigus valivad laotöötajad tooteid ladustamiskohtadest ja teisaldavad need pakendamisjaama, kus kontrollitakse kauba kogust ja tüüpe ning määratakse neile sobivad konteinerid.</span><span class="sxs-lookup"><span data-stu-id="d180d-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="d180d-106">Kui konteiner on täis, saab selle sulgeda ja teisaldada see lähetusalale ning tooted on saatmiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="d180d-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="d180d-107">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d180d-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="d180d-108">Asukohaprofiilide häälestamine</span><span class="sxs-lookup"><span data-stu-id="d180d-108">Set up location profiles</span></span>
1. <span data-ttu-id="d180d-109">Avage Laohaldus > Seadistus > Ladu > Asukohaprofiilid.</span><span class="sxs-lookup"><span data-stu-id="d180d-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="d180d-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d180d-110">Click New.</span></span>
    * <span data-ttu-id="d180d-111">Asukoha profiili kasutatakse pakkimisjaamade jaoks ja see sisaldab teavet ning reegleid asukoha kohta.</span><span class="sxs-lookup"><span data-stu-id="d180d-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="d180d-112">Sisestage väärtus väljale Asukohaprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="d180d-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="d180d-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d180d-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d180d-114">Sisestage või valige väärtus väljal Asukoha vorming.</span><span class="sxs-lookup"><span data-stu-id="d180d-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="d180d-115">Sisestage või valige väärtus väljal Asukoha tüüp.</span><span class="sxs-lookup"><span data-stu-id="d180d-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="d180d-116">Tehke väljal Luba segakaubad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="d180d-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="d180d-117">Tehke väljal Luba lao segaolekud valik Jah.</span><span class="sxs-lookup"><span data-stu-id="d180d-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="d180d-118">Tehke väljal Alista partiipäevade reeglid valik Jah.</span><span class="sxs-lookup"><span data-stu-id="d180d-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="d180d-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d180d-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="d180d-120">Laohalduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="d180d-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="d180d-121">Avage Laohaldus > Seadistus > Laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d180d-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="d180d-122">Klõpsake vahekaarti Pakkimine.</span><span class="sxs-lookup"><span data-stu-id="d180d-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="d180d-123">Sisestage või valige väärtus väljal Pakkimise asukoha profiili ID.</span><span class="sxs-lookup"><span data-stu-id="d180d-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="d180d-124">Valige asukoha profiil, mida soovite pakkimisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="d180d-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="d180d-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d180d-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="d180d-126">Konteineri tüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d180d-126">Set up container types</span></span>
1. <span data-ttu-id="d180d-127">Avage Laohaldus > Seadistus > Konteinerid > Konteinerite tüübid.</span><span class="sxs-lookup"><span data-stu-id="d180d-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="d180d-128">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d180d-128">Click New.</span></span>
    * <span data-ttu-id="d180d-129">Saate määratleda kasutatavate konteinerite tüübi.</span><span class="sxs-lookup"><span data-stu-id="d180d-129">You can define the types of containers to use.</span></span> <span data-ttu-id="d180d-130">Saate määrata konteineri füüsilised mõõdud, sh taara kaalu ja maksimaalse kaalu, maksimaalse mahu, pikkuse, laiuse ning kaalu.</span><span class="sxs-lookup"><span data-stu-id="d180d-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="d180d-131">Atribuudid on kohandatud väljad, mis võimaldavad teil lisada konteineri tüübile täiendavad dimensioone.</span><span class="sxs-lookup"><span data-stu-id="d180d-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="d180d-132">Tippige väärtus väljale Konteineri tüübi kood.</span><span class="sxs-lookup"><span data-stu-id="d180d-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="d180d-133">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d180d-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d180d-134">Sisestage number väljale Taarakaal.</span><span class="sxs-lookup"><span data-stu-id="d180d-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="d180d-135">Sisestage number väljale Maksimaalne kaal.</span><span class="sxs-lookup"><span data-stu-id="d180d-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="d180d-136">Sisestage number väljale Maht.</span><span class="sxs-lookup"><span data-stu-id="d180d-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="d180d-137">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="d180d-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="d180d-138">Sisestage number väljale Laius.</span><span class="sxs-lookup"><span data-stu-id="d180d-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="d180d-139">Sisestage number väljale Kõrgus.</span><span class="sxs-lookup"><span data-stu-id="d180d-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="d180d-140">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d180d-140">Click Save.</span></span>
12. <span data-ttu-id="d180d-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d180d-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="d180d-142">Pakkimisprofiilide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d180d-142">Set up packing profiles</span></span>
1. <span data-ttu-id="d180d-143">Avage Laohaldus > Seadistus > Pakkimine > Pakkimisprofiilid.</span><span class="sxs-lookup"><span data-stu-id="d180d-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="d180d-144">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d180d-144">Click New.</span></span>
3. <span data-ttu-id="d180d-145">Tippige väärtus väljale Pakkimisprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="d180d-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d180d-146">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d180d-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d180d-147">Sisestage või valige väärtus väljal Konteineri sulgemise profiili ID.</span><span class="sxs-lookup"><span data-stu-id="d180d-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="d180d-148">Konteineri sulgemise profiili ID on valikuline ja see on selle pakkimisprofiili konteineri sulgemise vaikeprofiil.</span><span class="sxs-lookup"><span data-stu-id="d180d-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="d180d-149">Valige suvand väljal Konteineri ID režiim.</span><span class="sxs-lookup"><span data-stu-id="d180d-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="d180d-150">See suvand määrab, kas konteineri ID luuakse automaatselt konteineri loomisel või kas konteineri ID luuakse käsitsi.</span><span class="sxs-lookup"><span data-stu-id="d180d-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="d180d-151">Sisestage või valige väärtus väljal Konteineri tüüp.</span><span class="sxs-lookup"><span data-stu-id="d180d-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="d180d-152">Konteineri tüüpi kasutatakse vaikimisi uue konteineri loomisel.</span><span class="sxs-lookup"><span data-stu-id="d180d-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="d180d-153">Märkige ruut Loo konteineri sulgemisel konteiner automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d180d-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="d180d-154">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d180d-154">Click Save.</span></span>
10. <span data-ttu-id="d180d-155">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d180d-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="d180d-156">Konteineri sulgemise profiilide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d180d-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="d180d-157">Avage Laohaldus > Seadistus > Konteinerid > Konteineri sulgemise profiilid.</span><span class="sxs-lookup"><span data-stu-id="d180d-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="d180d-158">Konteineri sulgemise profiilid määratlevad, mis juhtub, kui konteiner on suletud.</span><span class="sxs-lookup"><span data-stu-id="d180d-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="d180d-159">Saate seadistada mitu konteineri sulgemise profiili.</span><span class="sxs-lookup"><span data-stu-id="d180d-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="d180d-160">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d180d-160">Click New.</span></span>
3. <span data-ttu-id="d180d-161">Tippige väärtus väljale Konteineri sulgemise profiili ID.</span><span class="sxs-lookup"><span data-stu-id="d180d-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="d180d-162">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d180d-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d180d-163">Valige suvand väljal Manifest.</span><span class="sxs-lookup"><span data-stu-id="d180d-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="d180d-164">Määrake, kas avaldamine ilmneb konteinerite sulgemisel või saadetise kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="d180d-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="d180d-165">Arvestage sellega, et avaldamine nõuab transpordihaldust.</span><span class="sxs-lookup"><span data-stu-id="d180d-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="d180d-166">Avaldamine tuleb teha transpordimootorites, et see töötaks.</span><span class="sxs-lookup"><span data-stu-id="d180d-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="d180d-167">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="d180d-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="d180d-168">Sisestage või valige väärtus väljal Lõppsaadetise vaikeasukoht.</span><span class="sxs-lookup"><span data-stu-id="d180d-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="d180d-169">See on asukoht, kuhu tooted pärast konteinerite sulgemist teisaldatakse.</span><span class="sxs-lookup"><span data-stu-id="d180d-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="d180d-170">Sellel asukohal peab olema määratud lao parameetrites asukoha profiil.</span><span class="sxs-lookup"><span data-stu-id="d180d-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="d180d-171">Sisestage või valige väärtus väljal Kaaluühik.</span><span class="sxs-lookup"><span data-stu-id="d180d-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="d180d-172">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d180d-172">Click Save.</span></span>


