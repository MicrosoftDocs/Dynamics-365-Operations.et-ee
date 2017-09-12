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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c8cec376bcc8c50fb9a78bed039505608cd7782d
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="fadec-103">Käsitsi pakkimise seadistamine (ainult veebruar ja mai 2016)</span><span class="sxs-lookup"><span data-stu-id="fadec-103">Set up manual packing (February & May 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fadec-104">Pakkimisprotsess võimaldab toodete kinnitamist ja pakendamist konteineritesse.</span><span class="sxs-lookup"><span data-stu-id="fadec-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="fadec-105">Selle protsessi käigus valivad laotöötajad tooteid ladustamiskohtadest ja teisaldavad need pakendamisjaama, kus kontrollitakse kauba kogust ja tüüpe ning määratakse neile sobivad konteinerid.</span><span class="sxs-lookup"><span data-stu-id="fadec-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="fadec-106">Kui konteiner on täis, saab selle sulgeda ja teisaldada see lähetusalale ning tooted on saatmiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="fadec-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="fadec-107">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="fadec-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="fadec-108">See protseduur on mõeldud ainult rakenduse Dynamics 365 for Operations 2016. aasta veebruari ja mai versioonidele.</span><span class="sxs-lookup"><span data-stu-id="fadec-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="fadec-109">Asukohaprofiilide häälestamine</span><span class="sxs-lookup"><span data-stu-id="fadec-109">Set up location profiles</span></span>
1. <span data-ttu-id="fadec-110">Avage Laohaldus > Seadistus > Ladu > Asukohaprofiilid.</span><span class="sxs-lookup"><span data-stu-id="fadec-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="fadec-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fadec-111">Click New.</span></span>
    * <span data-ttu-id="fadec-112">Asukoha profiili kasutatakse pakkimisjaamade jaoks ja see sisaldab teavet ning reegleid asukoha kohta.</span><span class="sxs-lookup"><span data-stu-id="fadec-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="fadec-113">Sisestage väärtus väljale Asukohaprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="fadec-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="fadec-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="fadec-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="fadec-115">Sisestage või valige väärtus väljal Asukoha vorming.</span><span class="sxs-lookup"><span data-stu-id="fadec-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="fadec-116">Sisestage või valige väärtus väljal Asukoha tüüp.</span><span class="sxs-lookup"><span data-stu-id="fadec-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="fadec-117">Tehke väljal Luba segakaubad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="fadec-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="fadec-118">Tehke väljal Luba lao segaolekud valik Jah.</span><span class="sxs-lookup"><span data-stu-id="fadec-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="fadec-119">Tehke väljal Alista partiipäevade reeglid valik Jah.</span><span class="sxs-lookup"><span data-stu-id="fadec-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="fadec-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fadec-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="fadec-121">Laohalduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="fadec-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="fadec-122">Avage Laohaldus > Seadistus > Laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="fadec-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="fadec-123">Klõpsake vahekaarti Pakkimine.</span><span class="sxs-lookup"><span data-stu-id="fadec-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="fadec-124">Sisestage või valige väärtus väljal Pakkimise asukoha profiili ID.</span><span class="sxs-lookup"><span data-stu-id="fadec-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="fadec-125">Valige asukoha profiil, mida soovite pakkimisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="fadec-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="fadec-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fadec-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="fadec-127">Konteineri tüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="fadec-127">Set up container types</span></span>
1. <span data-ttu-id="fadec-128">Avage Laohaldus > Seadistus > Konteinerid > Konteinerite tüübid.</span><span class="sxs-lookup"><span data-stu-id="fadec-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="fadec-129">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fadec-129">Click New.</span></span>
    * <span data-ttu-id="fadec-130">Saate määratleda kasutatavate konteinerite tüübi.</span><span class="sxs-lookup"><span data-stu-id="fadec-130">You can define the types of containers to use.</span></span> <span data-ttu-id="fadec-131">Saate määrata konteineri füüsilised mõõdud, sh taara kaalu ja maksimaalse kaalu, maksimaalse mahu, pikkuse, laiuse ning kaalu.</span><span class="sxs-lookup"><span data-stu-id="fadec-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="fadec-132">Atribuudid on kohandatud väljad, mis võimaldavad teil lisada konteineri tüübile täiendavad dimensioone.</span><span class="sxs-lookup"><span data-stu-id="fadec-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="fadec-133">Tippige väärtus väljale Konteineri tüübi kood.</span><span class="sxs-lookup"><span data-stu-id="fadec-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="fadec-134">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="fadec-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fadec-135">Sisestage number väljale Taarakaal.</span><span class="sxs-lookup"><span data-stu-id="fadec-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="fadec-136">Sisestage number väljale Maksimaalne kaal.</span><span class="sxs-lookup"><span data-stu-id="fadec-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="fadec-137">Sisestage number väljale Maht.</span><span class="sxs-lookup"><span data-stu-id="fadec-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="fadec-138">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="fadec-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="fadec-139">Sisestage number väljale Laius.</span><span class="sxs-lookup"><span data-stu-id="fadec-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="fadec-140">Sisestage number väljale Kõrgus.</span><span class="sxs-lookup"><span data-stu-id="fadec-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="fadec-141">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="fadec-141">Click Save.</span></span>
12. <span data-ttu-id="fadec-142">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fadec-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="fadec-143">Pakkimisprofiilide seadistamine</span><span class="sxs-lookup"><span data-stu-id="fadec-143">Set up packing profiles</span></span>
1. <span data-ttu-id="fadec-144">Avage Laohaldus > Seadistus > Pakkimine > Pakkimisprofiilid.</span><span class="sxs-lookup"><span data-stu-id="fadec-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="fadec-145">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fadec-145">Click New.</span></span>
3. <span data-ttu-id="fadec-146">Tippige väärtus väljale Pakkimisprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="fadec-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="fadec-147">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="fadec-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fadec-148">Sisestage või valige väärtus väljal Konteineri sulgemise profiili ID.</span><span class="sxs-lookup"><span data-stu-id="fadec-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="fadec-149">Konteineri sulgemise profiili ID on valikuline ja see on selle pakkimisprofiili konteineri sulgemise vaikeprofiil.</span><span class="sxs-lookup"><span data-stu-id="fadec-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="fadec-150">Valige suvand väljal Konteineri ID režiim.</span><span class="sxs-lookup"><span data-stu-id="fadec-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="fadec-151">See suvand määrab, kas konteineri ID luuakse automaatselt konteineri loomisel või kas konteineri ID luuakse käsitsi.</span><span class="sxs-lookup"><span data-stu-id="fadec-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="fadec-152">Sisestage või valige väärtus väljal Konteineri tüüp.</span><span class="sxs-lookup"><span data-stu-id="fadec-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="fadec-153">Konteineri tüüpi kasutatakse vaikimisi uue konteineri loomisel.</span><span class="sxs-lookup"><span data-stu-id="fadec-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="fadec-154">Märkige ruut Loo konteineri sulgemisel konteiner automaatselt.</span><span class="sxs-lookup"><span data-stu-id="fadec-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="fadec-155">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="fadec-155">Click Save.</span></span>
10. <span data-ttu-id="fadec-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fadec-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="fadec-157">Konteineri sulgemise profiilide seadistamine</span><span class="sxs-lookup"><span data-stu-id="fadec-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="fadec-158">Avage Laohaldus > Seadistus > Konteinerid > Konteineri sulgemise profiilid.</span><span class="sxs-lookup"><span data-stu-id="fadec-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="fadec-159">Konteineri sulgemise profiilid määratlevad, mis juhtub, kui konteiner on suletud.</span><span class="sxs-lookup"><span data-stu-id="fadec-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="fadec-160">Saate seadistada mitu konteineri sulgemise profiili.</span><span class="sxs-lookup"><span data-stu-id="fadec-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="fadec-161">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="fadec-161">Click New.</span></span>
3. <span data-ttu-id="fadec-162">Tippige väärtus väljale Konteineri sulgemise profiili ID.</span><span class="sxs-lookup"><span data-stu-id="fadec-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="fadec-163">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="fadec-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fadec-164">Valige suvand väljal Manifest.</span><span class="sxs-lookup"><span data-stu-id="fadec-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="fadec-165">Määrake, kas avaldamine ilmneb konteinerite sulgemisel või saadetise kinnitamisel.</span><span class="sxs-lookup"><span data-stu-id="fadec-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="fadec-166">Arvestage sellega, et avaldamine nõuab transpordihaldust.</span><span class="sxs-lookup"><span data-stu-id="fadec-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="fadec-167">Avaldamine tuleb teha transpordimootorites, et see töötaks.</span><span class="sxs-lookup"><span data-stu-id="fadec-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="fadec-168">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="fadec-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="fadec-169">Sisestage või valige väärtus väljal Lõppsaadetise vaikeasukoht.</span><span class="sxs-lookup"><span data-stu-id="fadec-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="fadec-170">See on asukoht, kuhu tooted pärast konteinerite sulgemist teisaldatakse.</span><span class="sxs-lookup"><span data-stu-id="fadec-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="fadec-171">Sellel asukohal peab olema määratud lao parameetrites asukoha profiil.</span><span class="sxs-lookup"><span data-stu-id="fadec-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="fadec-172">Sisestage või valige väärtus väljal Kaaluühik.</span><span class="sxs-lookup"><span data-stu-id="fadec-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="fadec-173">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="fadec-173">Click Save.</span></span>


