---
title: Asukohtade konfigureerimine WMS-loaga laos
description: See juhend näitab, kuidas konfigureerida asukohaseadistust uue WMS-loaga lao puhul (ladu, mis kasutab täpsemaid laohaldusprotsesse).
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, WHSLocationFormat, WHSLocationType, WHSLocationProfile, WHSParameters, WHSZoneGroup, WHSZone, WHSLocationBuild, WHSLocation, WHSPackSizeCategory, WHSLocationLimit, WHSInventFixedLocation, WMSLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5df88f9ae7b07835db2911d55fae87f282826243
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847371"
---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="6d3cb-103">Asukohtade konfigureerimine WMS-loaga laos</span><span class="sxs-lookup"><span data-stu-id="6d3cb-103">Configure locations in a WMS-enabled warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d3cb-104">See juhend näitab, kuidas konfigureerida asukohaseadistust uue WMS-loaga lao puhul (ladu, mis kasutab täpsemaid laohaldusprotsesse).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="6d3cb-105">Selle protsessiga tegeleb tavaliselt laohaldur.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="6d3cb-106">Saate seda juhendit käitada demoettevõtte USMF andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6d3cb-107">Eeltingimuseks on vähemalt üks konfigureeritud sait.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="6d3cb-108">Uue lao loomine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-108">Create a new warehouse</span></span>
1. <span data-ttu-id="6d3cb-109">Minge jaotisse Laod.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="6d3cb-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-110">Click New.</span></span>
3. <span data-ttu-id="6d3cb-111">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-113">Sisestage väärtus väljale Koht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="6d3cb-114">Laiendage või ahendage jaotist Ladu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="6d3cb-115">Valige suvandi Kasuta laohaldusprotsesse sätteks Jah.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="6d3cb-116">See säte võimaldab käivitada täpsemaid laoprotsesse, kasutades laotööd ja mobiilseid seadmeid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="6d3cb-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="6d3cb-118">Asukohavormingu määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-118">Define a location format</span></span>
1. <span data-ttu-id="6d3cb-119">Minge jaotisse Asukohavormingud.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-119">Go to Location formats.</span></span>
    * <span data-ttu-id="6d3cb-120">Asukohavormingud on nimetussüsteem, mida kasutatakse erinevatele laos kasutatavatele asukoha kohapaigutustele kordumatute ja ühtsete nimede loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="6d3cb-121">Asukohavormingus on kasulik kasutada eraldajaid, et hõlbustada asukoha komponentide, nagu riiulirea numbri, tuvastamist.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="6d3cb-122">Selles näites loome nelja komponendiga nime.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="6d3cb-123">Need võivad olla näiteks riiulirida, sektsioon, riiul ja koht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="6d3cb-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-124">Click New.</span></span>
3. <span data-ttu-id="6d3cb-125">Sisestage väärtus väljale Asukohavorming.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-126">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-127">Sisestage väärtus väljale Segmendi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="6d3cb-128">See kirjeldab asukohanime esimest komponenti.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="6d3cb-129">See võib olla näiteks riiulirida.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="6d3cb-130">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="6d3cb-131">See määratleb, mitu tähemärki peab see asukohanime osa sisaldama.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="6d3cb-132">Pange tähele, et kõigi komponentide kohta kokku (koos eraldajatega) ei tohi nimi ületada 10 tärki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="6d3cb-133">Sisestage väärtus väljale Eraldaja.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="6d3cb-134">See määratleb, millist märki või sümbolit kasutatakse nime esimese ja teise komponendi vahel.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="6d3cb-135">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-135">Click New.</span></span>
9. <span data-ttu-id="6d3cb-136">Sisestage väärtus väljale Segmendi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="6d3cb-137">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="6d3cb-138">Sisestage väärtus väljale Eraldaja.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="6d3cb-139">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-139">Click New.</span></span>
13. <span data-ttu-id="6d3cb-140">Sisestage väärtus väljale Segmendi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="6d3cb-141">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="6d3cb-142">Sisestage väärtus väljale Eraldaja.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="6d3cb-143">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-143">Click New.</span></span>
17. <span data-ttu-id="6d3cb-144">Sisestage väärtus väljale Segmendi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="6d3cb-145">Sisestage number väljale Pikkus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="6d3cb-146">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-146">Click Save.</span></span>
20. <span data-ttu-id="6d3cb-147">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="6d3cb-148">Asukohatüüpide määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-148">Define location types</span></span>
1. <span data-ttu-id="6d3cb-149">Minge jaotisse Asukohatüübid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-149">Go to Location types.</span></span>
    * <span data-ttu-id="6d3cb-150">Asukohatüüpe saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="6d3cb-151">Minimaalselt peate looma saadetise vahe- ja lõppasukoha tüübid laohalduse väljaminev protsessi määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="6d3cb-152">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-152">Click New.</span></span>
3. <span data-ttu-id="6d3cb-153">Sisestage väärtus väljale Asukoha tüüp.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-154">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-155">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="6d3cb-156">Asukohaprofiili määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-156">Define location profile</span></span>
1. <span data-ttu-id="6d3cb-157">Minge jaotisse Asukohaprofiilid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="6d3cb-158">Asukohaprofiilide määratlus on väga oluline.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="6d3cb-159">Siin saab kontrollida grupeeritud asukohtade koormust, samuti poliitikaid, mis on seotud sellega, milliseid varusid ja kuidas hoitakse.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="6d3cb-160">Asukohaprofiile saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="6d3cb-161">Minimaalselt peate looma kasutaja asukohaprofiili laohalduse protsesside lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="6d3cb-162">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-162">Click New.</span></span>
3. <span data-ttu-id="6d3cb-163">Sisestage väärtus väljale Asukohaprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-164">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-165">Klõpsake väljal Asukohavorming otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6d3cb-166">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6d3cb-167">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6d3cb-168">Klõpsake väljal Asukoha tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6d3cb-169">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6d3cb-170">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="6d3cb-171">Valige või tühjendage märkeruut Luba lao segaolekud.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="6d3cb-172">Lubage see suvand, kui soovite lubada varude segaoleku väärtused asukohtades, mida grupeeritakse selle asukohaprofiili järgi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="6d3cb-173">Valige või tühjendage märkeruut Tühista partiipäevade reeglid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="6d3cb-174">Lubage see suvand, kui soovite tühistada reegli, mitu päeva võivad varude partii aegumiskuupäevad erineda, et lubada seda reeglit mittejärgivate varude partiide segamist.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="6d3cb-175">Valige või tühjendage märkeruut Luba tsükliline inventuur.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="6d3cb-176">Lubage see suvand, kui soovite lubada tsüklilise inventuuri töötlemise kõigis asukohtades, mida grupeeritakse selle asukohaprofiili järgi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="6d3cb-177">Laiendage või ahendage jaotist Dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="6d3cb-178">Vahekaardil Dimensioonid saate määratleda parameetrid ja meetodid, millega võimaldada koormuse võimsuse täpsed arvutused igas asukohas.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="6d3cb-179">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="6d3cb-180">Laohalduse parameetrite lubamine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="6d3cb-181">Minge jaotisse Laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="6d3cb-182">Laotöö töötlemiseks peate määrama kasutaja asukohaprofiili parameetrid vaheasukoha tüüp ja saadetise lõppasukoha tüüp. Niipea, kui väljaminev protsess saadetise teie määratletud tüüpi lõppasukohas lõpeb, värskendatakse seotud väljaminevad kanded olekusse Komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="6d3cb-183">Jaotise Asukoha profiilid laiendamine või ahendamine.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="6d3cb-184">Klõpsake väljal Kasutaja asukoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6d3cb-185">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6d3cb-186">Jaotise Asukohtade tüübid laiendamine või ahendamine.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="6d3cb-187">Klõpsake väljal Vaheasukoha tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="6d3cb-188">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6d3cb-189">Klõpsake väljal Saadetise lõppsihtkoha tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6d3cb-190">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="6d3cb-191">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="6d3cb-192">Laotsooni gruppide määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="6d3cb-193">Minge jaotisse Laotsooni grupid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="6d3cb-194">Laotsoone saab kasutada filtreerimissuvanditena erinevate laohaldusprotsesside kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="6d3cb-195">Enne tsooni määratlemist peate looma tsoonigrupi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="6d3cb-196">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-196">Click New.</span></span>
3. <span data-ttu-id="6d3cb-197">Sisestage väärtus väljale Tsoonigrupi ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-198">Sisestage väärtus väljale Tsoonigrupi nimi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-199">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="6d3cb-200">Laotsoonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="6d3cb-201">Minge jaotisse Tsoonid.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-201">Go to Zones.</span></span>
2. <span data-ttu-id="6d3cb-202">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-202">Click New.</span></span>
3. <span data-ttu-id="6d3cb-203">Sisestage väärtus väljale Tsooni ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-204">Sisestage väärtus väljale Tsooni nimi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-205">Klõpsake väljal Tsoonigrupi ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6d3cb-206">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6d3cb-207">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6d3cb-208">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="6d3cb-209">Asukohtade loomine asukoha seadistusviisardi abil</span><span class="sxs-lookup"><span data-stu-id="6d3cb-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="6d3cb-210">Minge jaotisse Asukoha seadistusviisard.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="6d3cb-211">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="6d3cb-212">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="6d3cb-213">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="6d3cb-214">Klõpsake väljal Tsooni ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6d3cb-215">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6d3cb-216">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6d3cb-217">Klõpsake väljal Asukohaprofiili ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="6d3cb-218">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6d3cb-219">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="6d3cb-220">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="6d3cb-221">Sisestage number väljale Alates numbrist.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="6d3cb-222">Väljad Alates numbrist ja Kuni numbrini määratlevad loodavate asukohtade arvu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="6d3cb-223">Näiteks kui määrate asukohavormingu kõigi nelja rea puhul välja Alates numbrist väärtuseks 1 ja välja Kuni numbrini väärtuseks 3, luuakse 81 välja (3 × 3 × 3 × 3).</span><span class="sxs-lookup"><span data-stu-id="6d3cb-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="6d3cb-224">Sisestage number väljale Kuni numbrini.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="6d3cb-225">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6d3cb-226">Sisestage number väljale Alates numbrist.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="6d3cb-227">Sisestage number väljale Kuni numbrini.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="6d3cb-228">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="6d3cb-229">Sisestage number väljale Alates numbrist.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="6d3cb-230">Sisestage number väljale Kuni numbrini.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="6d3cb-231">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="6d3cb-232">Sisestage number väljale Alates numbrist.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="6d3cb-233">Sisestage number väljale Kuni numbrini.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="6d3cb-234">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="6d3cb-235">Asukohtade käsitsi loomine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-235">Create locations manually</span></span>
1. <span data-ttu-id="6d3cb-236">Minge jaotisse Asukohad.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-236">Go to Locations.</span></span>
    * <span data-ttu-id="6d3cb-237">Asukohtade käsitsi loomine laos on lihtne.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="6d3cb-238">Väärtused Asukoha nimi ja Asukohaprofiili ID on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="6d3cb-239">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-239">Click New.</span></span>
3. <span data-ttu-id="6d3cb-240">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-241">Tippige väärtus väljale Asukoht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="6d3cb-242">Pange tähele, et loote siin uue asukoha, seega peate sisestama uue kordumatu nime, mitte valima olemasoleva.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="6d3cb-243">Sisestage väärtus väljale Asukohaprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="6d3cb-244">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="6d3cb-245">Pakendite suuruskategooriate määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-245">Define Pack size categories</span></span>
1. <span data-ttu-id="6d3cb-246">Minge jaotisse Pakendite suuruskategooriad.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="6d3cb-247">Pakendite suuruskategooriaid saab kasutada sarnaste füüsiliste pakendisuurustega kaupade grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="6d3cb-248">Selles näites kasutatakse pakendi suuruskategooriat võimsuse juhtimiseks komplekteerimisasukohtades lao teatud tsooni piires.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="6d3cb-249">Pange tähele, et pakendi suuruskategooria ID peab olema määratud väljastatud tooteüksusele, et seda kasutada osana ladustamispiirangute töötlemisest.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="6d3cb-250">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-250">Click New.</span></span>
3. <span data-ttu-id="6d3cb-251">Sisestage väärtus väljale Pakendisuuruse kategooria ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-252">Sisestage väärtus väljale Pakendisuuruse kategooria nimi.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-253">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="6d3cb-254">Asukoha ladustamispiirangute määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-254">Define location stocking limits</span></span>
1. <span data-ttu-id="6d3cb-255">Minge jaotisse Asukoha ladustamispiirangud.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="6d3cb-256">Asukoha ladustamispiirangud aitavad tagada, et ei loodaks tööd, mis nõuab varude panemist asukohta, milles puudub varude kandmiseks vajalik füüsiline võimsus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="6d3cb-257">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-257">Click New.</span></span>
3. <span data-ttu-id="6d3cb-258">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-259">Sisestage väärtus väljale Asukohaprofiili ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-260">Sisestage väärtus väljale Pakendisuuruse kategooria ID.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="6d3cb-261">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="6d3cb-262">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-262">Click Save.</span></span>
8. <span data-ttu-id="6d3cb-263">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="6d3cb-264">Fikseeritud komplekteerimiskohtade määratlemine</span><span class="sxs-lookup"><span data-stu-id="6d3cb-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="6d3cb-265">Minge jaotisse Fikseeritud asukohad.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="6d3cb-266">Saate määratleda kasutatavad asukohad toote või tootevariandi kohta.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="6d3cb-267">Sama toote kohta samas laos on võimalik luua mitu fikseeritud asukohta.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="6d3cb-268">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-268">Click New.</span></span>
3. <span data-ttu-id="6d3cb-269">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="6d3cb-270">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="6d3cb-271">Klõpsake väljal Asukoht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6d3cb-272">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6d3cb-273">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6d3cb-273">Close the page.</span></span>

