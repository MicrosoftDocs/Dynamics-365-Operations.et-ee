--- 
title: "Määrade koondandmete seadistamine"
description: "See protseduur näitab, kuidas seadistada koondmäära."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b7c02e5a6f5eeee270ca4b6f91e90f7799c2ca11
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="09a79-103">Määrade koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="09a79-103">Set up rate masters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09a79-104">See protseduur näitab, kuidas seadistada koondmäära.</span><span class="sxs-lookup"><span data-stu-id="09a79-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="09a79-105">Koondmäärad seadistab üldjuhul logistikahaldur vedajatega allkirjastatud lepingutest olenevalt.</span><span class="sxs-lookup"><span data-stu-id="09a79-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="09a79-106">Sel juhul saate seadistada koondmäära lennukompanii puhul.</span><span class="sxs-lookup"><span data-stu-id="09a79-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="09a79-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="09a79-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="09a79-108">Koondmäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="09a79-108">Set up rate master</span></span>
1. <span data-ttu-id="09a79-109">Avage Transpordihaldus > Seadistus > Hinnang > Koondmäär.</span><span class="sxs-lookup"><span data-stu-id="09a79-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="09a79-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="09a79-110">Click New.</span></span>
3. <span data-ttu-id="09a79-111">Sisestage väärtus väljale Koondmäär.</span><span class="sxs-lookup"><span data-stu-id="09a79-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="09a79-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="09a79-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="09a79-113">Klõpsake väljal Hindamise metaandmete ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="09a79-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="09a79-114">Hinnangu metaandmete ID määratleb koondmäära puhul vajalikud andmed, nagu see määratleb TMS-i mootori eeldatavad metaandmed seda koondmäära kasutades.</span><span class="sxs-lookup"><span data-stu-id="09a79-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="09a79-115">Selle näite puhul valige suvand P2P</span><span class="sxs-lookup"><span data-stu-id="09a79-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="09a79-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="09a79-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="09a79-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="09a79-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="09a79-118">Alusmäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="09a79-118">Set up rate base</span></span>
1. <span data-ttu-id="09a79-119">Klõpsake suvandit Alusmäär.</span><span class="sxs-lookup"><span data-stu-id="09a79-119">Click Rate base.</span></span>
    * <span data-ttu-id="09a79-120">Alusmäär määratleb vedaja määra ja seda saab kasutada tariifi struktuuri seadistamiseks, nagu see struktuurib määrasid katkestuse koondandmete määratletud katkestuspunktides.</span><span class="sxs-lookup"><span data-stu-id="09a79-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="09a79-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="09a79-121">Click New.</span></span>
3. <span data-ttu-id="09a79-122">Sisestage väärtus väljale Alusmäär.</span><span class="sxs-lookup"><span data-stu-id="09a79-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="09a79-123">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="09a79-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="09a79-124">Klõpsake väljal Katkestuse koondandmed otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="09a79-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="09a79-125">Katkestuse koondandmeid kasutatakse hinnakujunduse struktuuri ja selle katkestuspunktide määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="09a79-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="09a79-126">Hinnakujunduse struktuur kasutab mitmetasandilist hinnakujundust, mis põhineb füüsilistel dimensioonidel.</span><span class="sxs-lookup"><span data-stu-id="09a79-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="09a79-127">Selle näite puhul kasutage kaalu</span><span class="sxs-lookup"><span data-stu-id="09a79-127">For this example, use weight</span></span>
7. <span data-ttu-id="09a79-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="09a79-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="09a79-129">Laiendage jaotist Üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="09a79-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="09a79-130">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="09a79-130">Click New.</span></span>
10. <span data-ttu-id="09a79-131">Sisestage väljale Kohaleviimise saatja sihtnumber väärtus 30301.</span><span class="sxs-lookup"><span data-stu-id="09a79-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="09a79-132">Sisestage väljale Kohaleviimise saaja sihtnumber väärtus 30318.</span><span class="sxs-lookup"><span data-stu-id="09a79-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="09a79-133">Sisestage väljale Kohaleviimise riik/regioon suvand USA.</span><span class="sxs-lookup"><span data-stu-id="09a79-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="09a79-134">Sisestage väljale <1,00 naela väärtus 100.</span><span class="sxs-lookup"><span data-stu-id="09a79-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="09a79-135">Sisestage määr naela kohta, kui koorma kogukaal on alla 1 naela.</span><span class="sxs-lookup"><span data-stu-id="09a79-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="09a79-136">Sisestage väljale <5,00 naela väärtus 300.</span><span class="sxs-lookup"><span data-stu-id="09a79-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="09a79-137">Sisestage määr naela kohta, kui koorma kogukaal on alla 5 naela.</span><span class="sxs-lookup"><span data-stu-id="09a79-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="09a79-138">Sisestage väljale <20,00 naela väärtus 500.</span><span class="sxs-lookup"><span data-stu-id="09a79-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="09a79-139">Sisestage määr naela kohta, kui koorma kogukaal on alla 20 naela.</span><span class="sxs-lookup"><span data-stu-id="09a79-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="09a79-140">Sisestage väljale <100,00 naela väärtus 1000.</span><span class="sxs-lookup"><span data-stu-id="09a79-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="09a79-141">Sisestage määr naela kohta, kui koorma kogukaal on alla 100 naela.</span><span class="sxs-lookup"><span data-stu-id="09a79-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="09a79-142">Sisestage väljale <1000,00 naela väärtus 3000.</span><span class="sxs-lookup"><span data-stu-id="09a79-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="09a79-143">Sisestage määr naela kohta, kui koorma kogukaal on alla 1000 naela.</span><span class="sxs-lookup"><span data-stu-id="09a79-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="09a79-144">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="09a79-144">Click Save.</span></span>
19. <span data-ttu-id="09a79-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="09a79-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="09a79-146">Alusmäära määramine</span><span class="sxs-lookup"><span data-stu-id="09a79-146">Assign rate base</span></span>
1. <span data-ttu-id="09a79-147">Laiendage jaotist Alusmäära määrangud.</span><span class="sxs-lookup"><span data-stu-id="09a79-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="09a79-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="09a79-148">Click New.</span></span>
    * <span data-ttu-id="09a79-149">Teil võib iga määra koondandme puhul olla mitu alusmäära määramist.</span><span class="sxs-lookup"><span data-stu-id="09a79-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="09a79-150">See võimaldab luua mitu erinevat hinnaühtlustuspunkti iga vedaja puhul olenevalt sihtkohtadest, teenustest või erinevatest alusmääradest.</span><span class="sxs-lookup"><span data-stu-id="09a79-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="09a79-151">Selles protseduuris loote ainult ühe alusmäära määramise.</span><span class="sxs-lookup"><span data-stu-id="09a79-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="09a79-152">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="09a79-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="09a79-153">Klõpsake väljal Alusmäär otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="09a79-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="09a79-154">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="09a79-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="09a79-155">Klõpsake väljal Teenus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="09a79-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="09a79-156">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="09a79-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="09a79-157">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="09a79-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="09a79-158">Sisestage väljale Pealevõtmise postiindeks väärtus 98052.</span><span class="sxs-lookup"><span data-stu-id="09a79-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="09a79-159">Määrake, milline sihtnumber peaks selle alusmäära määramise puhul kehtima.</span><span class="sxs-lookup"><span data-stu-id="09a79-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="09a79-160">Sisestage väljale Pealevõtmise riik/regioon suvand USA.</span><span class="sxs-lookup"><span data-stu-id="09a79-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="09a79-161">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="09a79-161">Click Save.</span></span>


