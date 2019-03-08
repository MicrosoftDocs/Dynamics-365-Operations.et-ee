---
title: Kättetoimetamisettevõtte seadistus
description: See protseduur näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "314482"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="78c10-103">Kättetoimetamisettevõtte seadistus</span><span class="sxs-lookup"><span data-stu-id="78c10-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="78c10-104">See protseduur näitab, kuidas seadistada tarne vedaja ja määratleda üksikasjad, nt teenus, saadetise režiim, transpordi maksevahend, transpordi piirangud ja tarnekulu.</span><span class="sxs-lookup"><span data-stu-id="78c10-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="78c10-105">Transpordi koordinaator saab seejärel määrata saadetise vedaja sissetulevale või väljaminevale koormale.</span><span class="sxs-lookup"><span data-stu-id="78c10-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="78c10-106">Uue kättetoimetaja loomine</span><span class="sxs-lookup"><span data-stu-id="78c10-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="78c10-107">Tehke valik Transpordi haldus > Seadistus > Vedajad > Kättetoimetajad.</span><span class="sxs-lookup"><span data-stu-id="78c10-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="78c10-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="78c10-108">Click New.</span></span>
3. <span data-ttu-id="78c10-109">Sisestage väärtus väljale Kättetoimetaja.</span><span class="sxs-lookup"><span data-stu-id="78c10-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="78c10-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="78c10-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="78c10-111">Klõpsake väljal Režiim otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="78c10-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="78c10-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="78c10-114">Kättetoimetaja üldise teabe sisestamine</span><span class="sxs-lookup"><span data-stu-id="78c10-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="78c10-115">Laiendage jaotist Ülevaade.</span><span class="sxs-lookup"><span data-stu-id="78c10-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="78c10-116">Märkige või tühjendage ruut Aktiveeri saadetise vedaja.</span><span class="sxs-lookup"><span data-stu-id="78c10-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="78c10-117">Klõpsake väljal Hankija otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="78c10-118">Valige hankija konto, millele tarne vedaja määrata.</span><span class="sxs-lookup"><span data-stu-id="78c10-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="78c10-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="78c10-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="78c10-121">Valige suvand väljalt Transpordi maksevahendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="78c10-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="78c10-122">Valige leht Transpordi maksevahendi kasutamise juhend või valige EDI pakkumise värskendamiseks elektroonilise andmevahetuse (EDI) abil.</span><span class="sxs-lookup"><span data-stu-id="78c10-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="78c10-123">Märkige või tühjendage ruut Aktiveeri vedaja hinnang.</span><span class="sxs-lookup"><span data-stu-id="78c10-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="78c10-124">Kättetoimetaja vajalike teenuste loomine</span><span class="sxs-lookup"><span data-stu-id="78c10-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="78c10-125">Laiendage jaotist Teenused.</span><span class="sxs-lookup"><span data-stu-id="78c10-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="78c10-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="78c10-126">Click New.</span></span>
3. <span data-ttu-id="78c10-127">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="78c10-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="78c10-128">Sisestage väärtus väljale Vedaja teenus.</span><span class="sxs-lookup"><span data-stu-id="78c10-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="78c10-129">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="78c10-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="78c10-130">Klõpsake väljal Transpordiviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="78c10-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="78c10-132">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="78c10-133">Vedaja aadressi seadistamine (valikuline)</span><span class="sxs-lookup"><span data-stu-id="78c10-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="78c10-134">Lülitage ümber jaotis Aadressid.</span><span class="sxs-lookup"><span data-stu-id="78c10-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="78c10-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="78c10-135">Click New.</span></span>
3. <span data-ttu-id="78c10-136">Sisestage väärtus väljale Nimi või kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="78c10-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="78c10-137">Klõpsake väljal Riik/regioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="78c10-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="78c10-139">Klõpsake väljal Sihtnumber otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="78c10-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="78c10-141">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="78c10-142">Sisestage väärtus väljale Tänav.</span><span class="sxs-lookup"><span data-stu-id="78c10-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="78c10-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="78c10-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="78c10-144">Kättetoimetaja hinnanguprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="78c10-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="78c10-145">Laiendage jaotist Hinnanguprofiilid.</span><span class="sxs-lookup"><span data-stu-id="78c10-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="78c10-146">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="78c10-146">Click New.</span></span>
3. <span data-ttu-id="78c10-147">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="78c10-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="78c10-148">Sisestage väärtus väljale Hinnanguprofiil.</span><span class="sxs-lookup"><span data-stu-id="78c10-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="78c10-149">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="78c10-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="78c10-150">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="78c10-151">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="78c10-152">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="78c10-153">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="78c10-154">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="78c10-155">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="78c10-156">Klõpsake väljal Määra mootor otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="78c10-157">Valige Määra mootor, mis on kooskõlas vedaja lepinguga.</span><span class="sxs-lookup"><span data-stu-id="78c10-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="78c10-158">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="78c10-159">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="78c10-160">Klõpsake väljal Koondmäär otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="78c10-161">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="78c10-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="78c10-162">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="78c10-163">Klõpsake väljal Transiitaja mootor otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="78c10-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="78c10-164">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="78c10-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="78c10-165">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="78c10-165">Click Save.</span></span>

