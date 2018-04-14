--- 
title: "Avansimakse töötajale (Ida-Euroopa)"
description: "See protseduur näitab, kuidas seadistada ja registreerida avansisaaja kandeid."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c0def57d9dd0a3a5b57103303b6a5e301155f46f
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="advance-payment-to-an-employee-eastern-europe"></a><span data-ttu-id="e058e-103">Avansimakse töötajale (Ida-Euroopa)</span><span class="sxs-lookup"><span data-stu-id="e058e-103">Advance payment to an employee (Eastern Europe)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e058e-104">See protseduur näitab, kuidas seadistada ja registreerida avansisaaja kandeid.</span><span class="sxs-lookup"><span data-stu-id="e058e-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="e058e-105">Selle protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Leedu, andmeid.</span><span class="sxs-lookup"><span data-stu-id="e058e-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="e058e-106">Selle toiming sobib ainule juriidilistele isikutele esmase aadressiga Poolas, Leedus, Lätis, Eestis, Tšehhi Vabariigis või Ungaris.</span><span class="sxs-lookup"><span data-stu-id="e058e-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="e058e-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="e058e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="e058e-108">Uue sularahakonto loomine</span><span class="sxs-lookup"><span data-stu-id="e058e-108">Create a new cash account</span></span>
1. <span data-ttu-id="e058e-109">Minge jaotisse Sularaha- ja pangahaldus > Pangakontod > Sularahakontod.</span><span class="sxs-lookup"><span data-stu-id="e058e-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="e058e-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-110">Click New.</span></span>
3. <span data-ttu-id="e058e-111">Tippige väärtus väljale Sularaha.</span><span class="sxs-lookup"><span data-stu-id="e058e-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="e058e-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="e058e-113">Sisestage või valige väärtus väljal Numbriseeria grupp.</span><span class="sxs-lookup"><span data-stu-id="e058e-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="e058e-114">Laiendage jaotist Kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="e058e-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="e058e-115">Valige või sisestage väärtus väljal Valuuta.</span><span class="sxs-lookup"><span data-stu-id="e058e-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="e058e-116">Tehke väljal Negatiivne kassa valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e058e-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="e058e-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="e058e-118">Uue töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="e058e-118">Create a new journal</span></span>
1. <span data-ttu-id="e058e-119">Minge jaotisesse Pearaamat > Töölehe seadistamine > Töölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="e058e-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="e058e-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-120">Click New.</span></span>
3. <span data-ttu-id="e058e-121">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e058e-122">Sisestage või valige väärtus väljal Kande seeria.</span><span class="sxs-lookup"><span data-stu-id="e058e-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="e058e-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-123">Click Save.</span></span>
6. <span data-ttu-id="e058e-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-124">Click New.</span></span>
7. <span data-ttu-id="e058e-125">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="e058e-126">Valige suvand väljal Töölehe tüüp.</span><span class="sxs-lookup"><span data-stu-id="e058e-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="e058e-127">Sisestage või valige väärtus väljal Kande seeria.</span><span class="sxs-lookup"><span data-stu-id="e058e-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="e058e-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="e058e-129">Avansisaajate grupi loomine</span><span class="sxs-lookup"><span data-stu-id="e058e-129">Create an advance holder group</span></span>
1. <span data-ttu-id="e058e-130">Avage Ostureskonto > Seadistus > Avansisaajad > Avansisaajate rühmad.</span><span class="sxs-lookup"><span data-stu-id="e058e-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="e058e-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-131">Click New.</span></span>
3. <span data-ttu-id="e058e-132">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="e058e-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="e058e-133">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e058e-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e058e-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="e058e-135">Töötaja sisestusreeglite loomine</span><span class="sxs-lookup"><span data-stu-id="e058e-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="e058e-136">Avage Ostureskontro > Seadistus > Avansisaajad > Töötaja sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="e058e-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="e058e-137">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-137">Click New.</span></span>
3. <span data-ttu-id="e058e-138">Sisestage väärtus väljale Sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="e058e-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="e058e-139">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e058e-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e058e-140">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e058e-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e058e-141">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="e058e-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="e058e-142">Määrake väljal Summakonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e058e-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="e058e-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="e058e-144">Avansisaaja parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="e058e-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="e058e-145">Avage Ostureskontro > Seadistus > Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e058e-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="e058e-146">Klõpsake vahekaarti Avansisaajad.</span><span class="sxs-lookup"><span data-stu-id="e058e-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="e058e-147">Sisestage või valige väärtus väljal Sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="e058e-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="e058e-148">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="e058e-149">Valige või sisestage väärtus väljal Sularaha.</span><span class="sxs-lookup"><span data-stu-id="e058e-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="e058e-150">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="e058e-151">Valige suvand väljal Konto tüüp.</span><span class="sxs-lookup"><span data-stu-id="e058e-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="e058e-152">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e058e-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="e058e-153">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="e058e-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="e058e-154">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="e058e-155">Kassa sisestusprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="e058e-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="e058e-156">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="e058e-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="e058e-157">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-157">Click New.</span></span>
3. <span data-ttu-id="e058e-158">Tippige väärtus väljale Kassaseisu sisestamine.</span><span class="sxs-lookup"><span data-stu-id="e058e-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="e058e-159">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e058e-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e058e-160">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e058e-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="e058e-161">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="e058e-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="e058e-162">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e058e-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="e058e-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="e058e-164">Sularaha- ja pangahalduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="e058e-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="e058e-165">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e058e-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="e058e-166">Klõpsake vahekaarti Sularaha.</span><span class="sxs-lookup"><span data-stu-id="e058e-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="e058e-167">Valige või sisestage väärtus väljal Sularaha.</span><span class="sxs-lookup"><span data-stu-id="e058e-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="e058e-168">Valige või sisestage väärtus väljal Kassaseisu sisestamine.</span><span class="sxs-lookup"><span data-stu-id="e058e-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="e058e-169">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-169">Click Save.</span></span>
6. <span data-ttu-id="e058e-170">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="e058e-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="e058e-171">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e058e-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="e058e-172">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="e058e-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="e058e-173">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e058e-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e058e-174">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="e058e-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="e058e-175">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="e058e-176">Maksetingimuste häälestamine</span><span class="sxs-lookup"><span data-stu-id="e058e-176">Set up terms of payment</span></span>
1. <span data-ttu-id="e058e-177">Avage Ostureskontro > Makse seadistus > Maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="e058e-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="e058e-178">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e058e-178">Click Edit.</span></span>
3. <span data-ttu-id="e058e-179">Tehke väljal Avansisaajalt valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e058e-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="e058e-180">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="e058e-181">Uue töötaja loomine</span><span class="sxs-lookup"><span data-stu-id="e058e-181">Create a new worker</span></span>
1. <span data-ttu-id="e058e-182">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="e058e-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="e058e-183">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-183">Click New.</span></span>
3. <span data-ttu-id="e058e-184">Sisestage väärtus väljale Eesnimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="e058e-185">Sisestage väärtus väljale Perekonnanimi.</span><span class="sxs-lookup"><span data-stu-id="e058e-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="e058e-186">Tippige väärtus väljale Töötaja ID.</span><span class="sxs-lookup"><span data-stu-id="e058e-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="e058e-187">Klõpsake suvandit Uue töötaja värbamine.</span><span class="sxs-lookup"><span data-stu-id="e058e-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="e058e-188">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="e058e-189">Töötaja seadistamine avansisaajaks</span><span class="sxs-lookup"><span data-stu-id="e058e-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="e058e-190">Avage Ostureskonto > Avansisaajad > Avansisaajad.</span><span class="sxs-lookup"><span data-stu-id="e058e-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="e058e-191">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e058e-191">Click Edit.</span></span>
3. <span data-ttu-id="e058e-192">Sisestage või valige väärtus väljal Grupp.</span><span class="sxs-lookup"><span data-stu-id="e058e-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="e058e-193">Tehke väljal Avansisaaja valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e058e-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="e058e-194">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="e058e-195">Ostutellimuse arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="e058e-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="e058e-196">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="e058e-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="e058e-197">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e058e-197">Click New.</span></span>
3. <span data-ttu-id="e058e-198">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="e058e-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="e058e-199">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e058e-199">Click OK.</span></span>
5. <span data-ttu-id="e058e-200">Valige üks suvand väljalt Read või päis.</span><span class="sxs-lookup"><span data-stu-id="e058e-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="e058e-201">Laiendage jaotist Hind ja allahindlus.</span><span class="sxs-lookup"><span data-stu-id="e058e-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="e058e-202">Valige või sisestage väärtus väljal Terms of payment (Makse tingimused).</span><span class="sxs-lookup"><span data-stu-id="e058e-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="e058e-203">Valige või sisestage väärtus väljal Avansisaaja.</span><span class="sxs-lookup"><span data-stu-id="e058e-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="e058e-204">Valige üks suvand väljalt Read või päis.</span><span class="sxs-lookup"><span data-stu-id="e058e-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="e058e-205">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e058e-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="e058e-206">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="e058e-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="e058e-207">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="e058e-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="e058e-208">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="e058e-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="e058e-209">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-209">Click Save.</span></span>
15. <span data-ttu-id="e058e-210">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="e058e-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="e058e-211">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="e058e-211">Click Confirm.</span></span>
17. <span data-ttu-id="e058e-212">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="e058e-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="e058e-213">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="e058e-213">Click Invoice.</span></span>
19. <span data-ttu-id="e058e-214">Rippdialoogi avamiseks klõpsake valikut Vaikimisi asukohast: toote sissetuleku kogus.</span><span class="sxs-lookup"><span data-stu-id="e058e-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="e058e-215">Valige suvand väljal Ridade vaikekogus.</span><span class="sxs-lookup"><span data-stu-id="e058e-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="e058e-216">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e058e-216">Click OK.</span></span>
22. <span data-ttu-id="e058e-217">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="e058e-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="e058e-218">Sisestage väljale Arve kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e058e-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="e058e-219">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e058e-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="e058e-220">Sisestage kuupäev väljale KM-registri kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e058e-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="e058e-221">Sisestage kuupäev väljale Vastuvõtudokumendi kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e058e-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="e058e-222">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="e058e-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="e058e-223">Avansisaajate kannete tasakaalustamine ja sulgemine</span><span class="sxs-lookup"><span data-stu-id="e058e-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="e058e-224">Avage Ostureskonto > Avansisaajad > Avansisaajad.</span><span class="sxs-lookup"><span data-stu-id="e058e-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="e058e-225">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="e058e-225">Click Transactions.</span></span>
3. <span data-ttu-id="e058e-226">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e058e-226">Close the page.</span></span>
4. <span data-ttu-id="e058e-227">Klõpsake valikut Saldo.</span><span class="sxs-lookup"><span data-stu-id="e058e-227">Click Balance.</span></span>
5. <span data-ttu-id="e058e-228">Klõpsake valikut Sule panga kaudu.</span><span class="sxs-lookup"><span data-stu-id="e058e-228">Click Close via bank.</span></span>
6. <span data-ttu-id="e058e-229">Tehke väljal Automaatne valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e058e-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="e058e-230">Sisestage väljale Ülekantav summa</span><span class="sxs-lookup"><span data-stu-id="e058e-230">In the Amount to be transferred.</span></span> <span data-ttu-id="e058e-231">number.</span><span class="sxs-lookup"><span data-stu-id="e058e-231">field, enter a number.</span></span>
8. <span data-ttu-id="e058e-232">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e058e-232">Click OK.</span></span>
9. <span data-ttu-id="e058e-233">Klõpsake valikut Sule kassa kaudu.</span><span class="sxs-lookup"><span data-stu-id="e058e-233">Click Close via cash.</span></span>
10. <span data-ttu-id="e058e-234">Tehke väljal Automaatne valik Jah.</span><span class="sxs-lookup"><span data-stu-id="e058e-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="e058e-235">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e058e-235">Click OK.</span></span>
12. <span data-ttu-id="e058e-236">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e058e-236">Close the page.</span></span>
13. <span data-ttu-id="e058e-237">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="e058e-237">Click Transactions.</span></span>


