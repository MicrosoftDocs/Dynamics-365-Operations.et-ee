---
title: Määrade koondandmete seadistamine
description: See protseduur näitab, kuidas seadistada koondmäära.
author: ShylaThompson
manager: tfehr
ms.date: 10/16/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSBreakMaster,TMSRateMaster,TMSRateMasterBase,TMSRateBaseType, TMSRouteWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 47fa7edeba81d826a00668a2da74113f552437f4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4974256"
---
# <a name="set-up-rate-masters"></a><span data-ttu-id="17876-103">Määrade koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="17876-103">Set up rate masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17876-104">See protseduur näitab, kuidas seadistada koondmäära.</span><span class="sxs-lookup"><span data-stu-id="17876-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="17876-105">Koondmäärad seadistab üldjuhul logistikahaldur vedajatega allkirjastatud lepingutest olenevalt.</span><span class="sxs-lookup"><span data-stu-id="17876-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="17876-106">Sel juhul saate seadistada koondmäära lennukompanii puhul.</span><span class="sxs-lookup"><span data-stu-id="17876-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="17876-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="17876-107">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-break-master"></a><span data-ttu-id="17876-108">Katkestuse koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="17876-108">Set up break master</span></span>

1. <span data-ttu-id="17876-109">Avage **Transpordihaldus > Seadistus > Hinnang > Katkestuste koondandmed**.</span><span class="sxs-lookup"><span data-stu-id="17876-109">Go to **Transportation management > Setup > Rating > Break master**.</span></span> <span data-ttu-id="17876-110">Katkestuse koondandmeid kasutatakse hinnakujunduse struktuuri ja selle katkestuspunktide määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="17876-110">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="17876-111">Hinnakujunduse struktuur kasutab mitmetasandilist hinnakujundust, mis põhineb füüsilistel dimensioonidel.</span><span class="sxs-lookup"><span data-stu-id="17876-111">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
1. <span data-ttu-id="17876-112">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17876-112">Select **New**.</span></span>
1. <span data-ttu-id="17876-113">Sisestage väärtus väljal **Katkestuse koondandmed**.</span><span class="sxs-lookup"><span data-stu-id="17876-113">In the **Break master** field, enter a value.</span></span>
1. <span data-ttu-id="17876-114">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="17876-114">In the **Name** field, enter a value.</span></span>
1. <span data-ttu-id="17876-115">Valige **Andmetüüp** väljal andmetüüp.</span><span class="sxs-lookup"><span data-stu-id="17876-115">In the **Data type** field, select the data type.</span></span>
1. <span data-ttu-id="17876-116">Sisestage väljale **Võrdlus** taotletud võrdluse tüüp (kasutades tehtemärke).</span><span class="sxs-lookup"><span data-stu-id="17876-116">In the **Comparison** field, enter the kind of comparison requested (using operators).</span></span>
1. <span data-ttu-id="17876-117">Sisestage **Katkestuse ühik** väljale katkestuse ühiku väärtused.</span><span class="sxs-lookup"><span data-stu-id="17876-117">In the **Break unit** field, enter the break unit.</span></span>
1. <span data-ttu-id="17876-118">Looge **Üksikasjad** jaotises nii palju katkestusi, kui on vaja hinnakujunduse struktuuri jaoks.</span><span class="sxs-lookup"><span data-stu-id="17876-118">In the **Details** section, create as many breaks as needed for the pricing structure.</span></span>
1. <span data-ttu-id="17876-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="17876-119">Select **Save**.</span></span>

## <a name="set-up-rate-master"></a><span data-ttu-id="17876-120">Koondmäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="17876-120">Set up rate master</span></span>

1. <span data-ttu-id="17876-121">Avage **Transpordihaldus > Seadistus > Hinnang > Hinnangu koondandmed**.</span><span class="sxs-lookup"><span data-stu-id="17876-121">Go to **Transportation management > Setup > Rating > Rate master**.</span></span>
1. <span data-ttu-id="17876-122">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17876-122">Select **New**.</span></span>
1. <span data-ttu-id="17876-123">Sisestage väärtus väljale **Hinnangu koondandmed**.</span><span class="sxs-lookup"><span data-stu-id="17876-123">In the **Rate master** field, type a value.</span></span>
1. <span data-ttu-id="17876-124">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="17876-124">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="17876-125">Valige **Meta-andmete ID hindamine** väljal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="17876-125">In the **Rating metadata ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="17876-126">Hinnangu meta-andmete ID määratleb koondmäära puhul vajalikud andmed, nagu see määratleb transpordihalduse mootori eeldatavad metaandmed seda koondmäära kasutades.</span><span class="sxs-lookup"><span data-stu-id="17876-126">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the transportation management engine using this rate master.</span></span>  
1. <span data-ttu-id="17876-127">Selle näite puhul valige suvand P2P.</span><span class="sxs-lookup"><span data-stu-id="17876-127">For this example, select the P2P option.</span></span> <span data-ttu-id="17876-128">See on juba demo andmetega määratletud.</span><span class="sxs-lookup"><span data-stu-id="17876-128">This is already defined in the demo data.</span></span>
1. <span data-ttu-id="17876-129">Valige loendis link valitud reas.</span><span class="sxs-lookup"><span data-stu-id="17876-129">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="17876-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="17876-130">Select **Save**.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="17876-131">Alusmäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="17876-131">Set up rate base</span></span>

1. <span data-ttu-id="17876-132">Valige **Hinnangu alus**.</span><span class="sxs-lookup"><span data-stu-id="17876-132">Select **Rate base**.</span></span>
    * <span data-ttu-id="17876-133">Alusmäär määratleb vedaja määra ja seda saab kasutada tariifi struktuuri seadistamiseks, nagu see struktuurib määrasid katkestuse koondandmete määratletud katkestuspunktides.</span><span class="sxs-lookup"><span data-stu-id="17876-133">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="17876-134">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17876-134">Select **New**.</span></span>
3. <span data-ttu-id="17876-135">Sisestage **Hinnangu alus** väljale väärtus.</span><span class="sxs-lookup"><span data-stu-id="17876-135">In the **Rate base** field, type a value.</span></span>
4. <span data-ttu-id="17876-136">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="17876-136">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="17876-137">Valige **Katkestuse koondandmed** väljal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="17876-137">In the **Break master** field, select the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="17876-138">Katkestuse koondandmeid kasutatakse hinnakujunduse struktuuri ja selle katkestuspunktide määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="17876-138">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="17876-139">Hinnakujunduse struktuur kasutab mitmetasandilist hinnakujundust, mis põhineb füüsilistel dimensioonidel.</span><span class="sxs-lookup"><span data-stu-id="17876-139">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="17876-140">Selle näite puhul kasutage kaalu.</span><span class="sxs-lookup"><span data-stu-id="17876-140">For this example, use weight.</span></span> <span data-ttu-id="17876-141">See on juba demo andmetega määratletud.</span><span class="sxs-lookup"><span data-stu-id="17876-141">This is already defined in the demo data.</span></span>
7. <span data-ttu-id="17876-142">Valige loendis link esiletõstetud reas.</span><span class="sxs-lookup"><span data-stu-id="17876-142">In the list, select the link in the highlighted row.</span></span>
8. <span data-ttu-id="17876-143">Laiendage jaotist **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="17876-143">Expand the **Details** section.</span></span>
9. <span data-ttu-id="17876-144">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17876-144">Select **New**.</span></span>
10. <span data-ttu-id="17876-145">Sisestage **Kohaletoimetamise lähtekoha sihtnumber** väljale väärtus 30301.</span><span class="sxs-lookup"><span data-stu-id="17876-145">In the **Drop-off Postal Code From** field, type "30301".</span></span>
11. <span data-ttu-id="17876-146">Sisestage **Kohaletoimetamise sihtkoha sihtnumber** väljale "30318".</span><span class="sxs-lookup"><span data-stu-id="17876-146">In the **Drop-off Postal Code To** field, type "30318".</span></span>
12. <span data-ttu-id="17876-147">Sisestage **Kohaletoimetamise riik/regioon** väljale "USA".</span><span class="sxs-lookup"><span data-stu-id="17876-147">In the **Drop-off Country Region** field, type "USA".</span></span>
13. <span data-ttu-id="17876-148">Sisestage **<1,00 naela** väljale "100".</span><span class="sxs-lookup"><span data-stu-id="17876-148">In the **<1.00 Lbs** field, type "100".</span></span>
    * <span data-ttu-id="17876-149">Sisestage määr naela kohta, kui koorma kogukaal on vähem kui 1 nael.</span><span class="sxs-lookup"><span data-stu-id="17876-149">Insert the rate per pounds if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="17876-150">Sisestage **<5,00 naela** väljale "300".</span><span class="sxs-lookup"><span data-stu-id="17876-150">In the **<5.00 Lbs** field, type "300".</span></span>
    * <span data-ttu-id="17876-151">Sisestage määr naela kohta, kui koorma kogukaal on kuni 5 naela.</span><span class="sxs-lookup"><span data-stu-id="17876-151">Insert the rate per pounds if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="17876-152">Sisestage **<20,00 naela** väljale "500".</span><span class="sxs-lookup"><span data-stu-id="17876-152">In the **<20.00 Lbs** field, type "500".</span></span>
    * <span data-ttu-id="17876-153">Sisestage määr naela kohta, kui koorma kogukaal on kuni 20 naela.</span><span class="sxs-lookup"><span data-stu-id="17876-153">Insert the rate per pounds if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="17876-154">Sisestage **<100,00 naela** väljale "1000".</span><span class="sxs-lookup"><span data-stu-id="17876-154">In the **<100.00 Lbs** field, type "1000".</span></span>
    * <span data-ttu-id="17876-155">Sisestage määr naela kohta, kui koorma kogukaal on kuni 100 naela.</span><span class="sxs-lookup"><span data-stu-id="17876-155">Insert the rate per pounds if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="17876-156">Sisestage **<1000,00 naela** väljale "3000".</span><span class="sxs-lookup"><span data-stu-id="17876-156">In the **<1,000.00 Lbs** field, type "3000".</span></span>
    * <span data-ttu-id="17876-157">Sisestage määr naela kohta, kui koorma kogukaal on kuni 1000 naela.</span><span class="sxs-lookup"><span data-stu-id="17876-157">Insert the rate per pounds if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="17876-158">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="17876-158">Select **Save**.</span></span>
19. <span data-ttu-id="17876-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="17876-159">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="17876-160">Alusmäära määramine</span><span class="sxs-lookup"><span data-stu-id="17876-160">Assign rate base</span></span>

1. <span data-ttu-id="17876-161">Laiendage **Alusmäära määramised** jaotist.</span><span class="sxs-lookup"><span data-stu-id="17876-161">Expand the **Rate base assignments** section.</span></span>
2. <span data-ttu-id="17876-162">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="17876-162">Select **New**.</span></span>
    * <span data-ttu-id="17876-163">Teil võib iga määra koondandme puhul olla mitu alusmäära määramist.</span><span class="sxs-lookup"><span data-stu-id="17876-163">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="17876-164">See võimaldab luua mitu erinevat hinnaühtlustuspunkti iga vedaja puhul olenevalt sihtkohtadest, teenustest või erinevatest alusmääradest.</span><span class="sxs-lookup"><span data-stu-id="17876-164">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="17876-165">Selles protseduuris loote ainult ühe alusmäära määramise.</span><span class="sxs-lookup"><span data-stu-id="17876-165">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="17876-166">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="17876-166">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="17876-167">Klõpsake **Alusmäär** väljal otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="17876-167">In the **Rate base** field, select the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="17876-168">Valige loendis link esiletõstetud reas.</span><span class="sxs-lookup"><span data-stu-id="17876-168">In the list, select the link in the highlighted row.</span></span>
6. <span data-ttu-id="17876-169">Klõpsake väljal **Teenus** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="17876-169">In the **Service** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="17876-170">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="17876-170">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="17876-171">Valige loendis link esiletõstetud reas.</span><span class="sxs-lookup"><span data-stu-id="17876-171">In the list, select the link in the highlighted row.</span></span>
9. <span data-ttu-id="17876-172">Sisestage väljale **Peale võtmise postiindeks** väärtus "98052".</span><span class="sxs-lookup"><span data-stu-id="17876-172">In the **Pick-up Postal Code** field, type "98052".</span></span>
    * <span data-ttu-id="17876-173">Määrake, milline sihtnumber peaks selle alusmäära määramise puhul kehtima.</span><span class="sxs-lookup"><span data-stu-id="17876-173">Specify which postal code this rate base assignment should be valid from.</span></span>
10. <span data-ttu-id="17876-174">Sisestage väljale **Peale võtmise riik/regioon** "USA".</span><span class="sxs-lookup"><span data-stu-id="17876-174">In the **Pick-up Country Region** field, type "USA".</span></span>
11. <span data-ttu-id="17876-175">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="17876-175">Select **Save**.</span></span>
