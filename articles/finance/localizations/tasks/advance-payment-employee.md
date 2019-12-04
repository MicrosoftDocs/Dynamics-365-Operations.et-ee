---
title: EEU-00047 Töötajale avansi maksmine
description: See protseduur näitab, kuidas seadistada ja registreerida avansisaaja kandeid.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cfc03cb9dc35a27f99b740da181fe54aa2e684d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175121"
---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="ed793-103">EEU-00047 Töötajale avansi maksmine</span><span class="sxs-lookup"><span data-stu-id="ed793-103">EEU-00047 Advance payment to employee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ed793-104">See protseduur näitab, kuidas seadistada ja registreerida avansisaaja kandeid.</span><span class="sxs-lookup"><span data-stu-id="ed793-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="ed793-105">Selle protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Leedu, andmeid.</span><span class="sxs-lookup"><span data-stu-id="ed793-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="ed793-106">Selle toiming sobib ainule juriidilistele isikutele esmase aadressiga Poolas, Leedus, Lätis, Eestis, Tšehhi Vabariigis või Ungaris.</span><span class="sxs-lookup"><span data-stu-id="ed793-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="ed793-107">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="ed793-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="ed793-108">Uue sularahakonto loomine</span><span class="sxs-lookup"><span data-stu-id="ed793-108">Create a new cash account</span></span>
1. <span data-ttu-id="ed793-109">Minge jaotisse Sularaha- ja pangahaldus > Pangakontod > Sularahakontod.</span><span class="sxs-lookup"><span data-stu-id="ed793-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="ed793-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-110">Click New.</span></span>
3. <span data-ttu-id="ed793-111">Tippige väärtus väljale Sularaha.</span><span class="sxs-lookup"><span data-stu-id="ed793-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="ed793-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ed793-113">Sisestage või valige väärtus väljal Numbriseeria grupp.</span><span class="sxs-lookup"><span data-stu-id="ed793-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="ed793-114">Laiendage jaotist Kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="ed793-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="ed793-115">Valige või sisestage väärtus väljal Valuuta.</span><span class="sxs-lookup"><span data-stu-id="ed793-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="ed793-116">Tehke väljal Negatiivne kassa valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ed793-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="ed793-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="ed793-118">Uue töölehe loomine</span><span class="sxs-lookup"><span data-stu-id="ed793-118">Create a new journal</span></span>
1. <span data-ttu-id="ed793-119">Minge jaotisesse Pearaamat > Töölehe seadistamine > Töölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="ed793-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="ed793-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-120">Click New.</span></span>
3. <span data-ttu-id="ed793-121">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ed793-122">Sisestage või valige väärtus väljal Kande seeria.</span><span class="sxs-lookup"><span data-stu-id="ed793-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="ed793-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-123">Click Save.</span></span>
6. <span data-ttu-id="ed793-124">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-124">Click New.</span></span>
7. <span data-ttu-id="ed793-125">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="ed793-126">Valige suvand väljal Töölehe tüüp.</span><span class="sxs-lookup"><span data-stu-id="ed793-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="ed793-127">Sisestage või valige väärtus väljal Kande seeria.</span><span class="sxs-lookup"><span data-stu-id="ed793-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="ed793-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="ed793-129">Avansisaajate grupi loomine</span><span class="sxs-lookup"><span data-stu-id="ed793-129">Create an advance holder group</span></span>
1. <span data-ttu-id="ed793-130">Avage Ostureskonto > Seadistus > Avansisaajad > Avansisaajate rühmad.</span><span class="sxs-lookup"><span data-stu-id="ed793-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="ed793-131">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-131">Click New.</span></span>
3. <span data-ttu-id="ed793-132">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="ed793-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="ed793-133">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ed793-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ed793-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="ed793-135">Töötaja sisestusreeglite loomine</span><span class="sxs-lookup"><span data-stu-id="ed793-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="ed793-136">Avage Ostureskontro > Seadistus > Avansisaajad > Töötaja sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="ed793-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="ed793-137">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-137">Click New.</span></span>
3. <span data-ttu-id="ed793-138">Sisestage väärtus väljale Sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="ed793-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="ed793-139">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ed793-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ed793-140">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ed793-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ed793-141">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="ed793-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="ed793-142">Määrake väljal Summakonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="ed793-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="ed793-143">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="ed793-144">Avansisaaja parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="ed793-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="ed793-145">Avage Ostureskontro > Seadistus > Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ed793-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="ed793-146">Klõpsake vahekaarti Avansisaajad.</span><span class="sxs-lookup"><span data-stu-id="ed793-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="ed793-147">Sisestage või valige väärtus väljal Sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="ed793-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="ed793-148">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="ed793-149">Valige või sisestage väärtus väljal Sularaha.</span><span class="sxs-lookup"><span data-stu-id="ed793-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="ed793-150">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="ed793-151">Valige suvand väljal Konto tüüp.</span><span class="sxs-lookup"><span data-stu-id="ed793-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="ed793-152">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="ed793-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="ed793-153">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="ed793-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="ed793-154">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="ed793-155">Kassa sisestusprofiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="ed793-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="ed793-156">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="ed793-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="ed793-157">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-157">Click New.</span></span>
3. <span data-ttu-id="ed793-158">Tippige väärtus väljale Kassaseisu sisestamine.</span><span class="sxs-lookup"><span data-stu-id="ed793-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="ed793-159">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ed793-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ed793-160">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ed793-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ed793-161">Valige suvand väljal Kehtiv.</span><span class="sxs-lookup"><span data-stu-id="ed793-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="ed793-162">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="ed793-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="ed793-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="ed793-164">Sularaha- ja pangahalduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="ed793-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="ed793-165">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="ed793-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="ed793-166">Klõpsake vahekaarti Sularaha.</span><span class="sxs-lookup"><span data-stu-id="ed793-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="ed793-167">Valige või sisestage väärtus väljal Sularaha.</span><span class="sxs-lookup"><span data-stu-id="ed793-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="ed793-168">Valige või sisestage väärtus väljal Kassaseisu sisestamine.</span><span class="sxs-lookup"><span data-stu-id="ed793-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="ed793-169">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-169">Click Save.</span></span>
6. <span data-ttu-id="ed793-170">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="ed793-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="ed793-171">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ed793-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ed793-172">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="ed793-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="ed793-173">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ed793-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ed793-174">Sisestage või valige väärtus väljal Numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="ed793-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="ed793-175">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="ed793-176">Maksetingimuste häälestamine</span><span class="sxs-lookup"><span data-stu-id="ed793-176">Set up terms of payment</span></span>
1. <span data-ttu-id="ed793-177">Avage Ostureskontro > Makse seadistus > Maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="ed793-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="ed793-178">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ed793-178">Click Edit.</span></span>
3. <span data-ttu-id="ed793-179">Tehke väljal Avansisaajalt valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ed793-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="ed793-180">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="ed793-181">Uue töötaja loomine</span><span class="sxs-lookup"><span data-stu-id="ed793-181">Create a new worker</span></span>
1. <span data-ttu-id="ed793-182">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="ed793-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="ed793-183">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-183">Click New.</span></span>
3. <span data-ttu-id="ed793-184">Sisestage väärtus väljale Eesnimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="ed793-185">Sisestage väärtus väljale Perekonnanimi.</span><span class="sxs-lookup"><span data-stu-id="ed793-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="ed793-186">Tippige väärtus väljale Töötaja ID.</span><span class="sxs-lookup"><span data-stu-id="ed793-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="ed793-187">Klõpsake suvandit Uue töötaja värbamine.</span><span class="sxs-lookup"><span data-stu-id="ed793-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="ed793-188">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="ed793-189">Töötaja seadistamine avansisaajaks</span><span class="sxs-lookup"><span data-stu-id="ed793-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="ed793-190">Avage Ostureskonto > Avansisaajad > Avansisaajad.</span><span class="sxs-lookup"><span data-stu-id="ed793-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="ed793-191">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ed793-191">Click Edit.</span></span>
3. <span data-ttu-id="ed793-192">Sisestage või valige väärtus väljal Grupp.</span><span class="sxs-lookup"><span data-stu-id="ed793-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="ed793-193">Tehke väljal Avansisaaja valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ed793-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="ed793-194">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="ed793-195">Ostutellimuse arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="ed793-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="ed793-196">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="ed793-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="ed793-197">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ed793-197">Click New.</span></span>
3. <span data-ttu-id="ed793-198">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="ed793-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="ed793-199">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ed793-199">Click OK.</span></span>
5. <span data-ttu-id="ed793-200">Valige üks suvand väljalt Read või päis.</span><span class="sxs-lookup"><span data-stu-id="ed793-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="ed793-201">Laiendage jaotist Hind ja allahindlus.</span><span class="sxs-lookup"><span data-stu-id="ed793-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="ed793-202">Valige või sisestage väärtus väljal Terms of payment (Makse tingimused).</span><span class="sxs-lookup"><span data-stu-id="ed793-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="ed793-203">Valige või sisestage väärtus väljal Avansisaaja.</span><span class="sxs-lookup"><span data-stu-id="ed793-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="ed793-204">Valige üks suvand väljalt Read või päis.</span><span class="sxs-lookup"><span data-stu-id="ed793-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="ed793-205">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ed793-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="ed793-206">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="ed793-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="ed793-207">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="ed793-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="ed793-208">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="ed793-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="ed793-209">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-209">Click Save.</span></span>
15. <span data-ttu-id="ed793-210">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="ed793-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="ed793-211">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="ed793-211">Click Confirm.</span></span>
17. <span data-ttu-id="ed793-212">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="ed793-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="ed793-213">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="ed793-213">Click Invoice.</span></span>
19. <span data-ttu-id="ed793-214">Rippdialoogi avamiseks klõpsake valikut Vaikimisi asukohast: toote sissetuleku kogus.</span><span class="sxs-lookup"><span data-stu-id="ed793-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="ed793-215">Valige suvand väljal Ridade vaikekogus.</span><span class="sxs-lookup"><span data-stu-id="ed793-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="ed793-216">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ed793-216">Click OK.</span></span>
22. <span data-ttu-id="ed793-217">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="ed793-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="ed793-218">Sisestage väljale Arve kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ed793-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="ed793-219">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ed793-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="ed793-220">Sisestage kuupäev väljale KM-registri kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ed793-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="ed793-221">Sisestage kuupäev väljale Vastuvõtudokumendi kuupäev.</span><span class="sxs-lookup"><span data-stu-id="ed793-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="ed793-222">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="ed793-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="ed793-223">Avansisaajate kannete tasakaalustamine ja sulgemine</span><span class="sxs-lookup"><span data-stu-id="ed793-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="ed793-224">Avage Ostureskonto > Avansisaajad > Avansisaajad.</span><span class="sxs-lookup"><span data-stu-id="ed793-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="ed793-225">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="ed793-225">Click Transactions.</span></span>
3. <span data-ttu-id="ed793-226">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ed793-226">Close the page.</span></span>
4. <span data-ttu-id="ed793-227">Klõpsake valikut Saldo.</span><span class="sxs-lookup"><span data-stu-id="ed793-227">Click Balance.</span></span>
5. <span data-ttu-id="ed793-228">Klõpsake valikut Sule panga kaudu.</span><span class="sxs-lookup"><span data-stu-id="ed793-228">Click Close via bank.</span></span>
6. <span data-ttu-id="ed793-229">Tehke väljal Automaatne valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ed793-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="ed793-230">Sisestage väljale Ülekantav summa</span><span class="sxs-lookup"><span data-stu-id="ed793-230">In the Amount to be transferred.</span></span> <span data-ttu-id="ed793-231">number.</span><span class="sxs-lookup"><span data-stu-id="ed793-231">field, enter a number.</span></span>
8. <span data-ttu-id="ed793-232">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ed793-232">Click OK.</span></span>
9. <span data-ttu-id="ed793-233">Klõpsake valikut Sule kassa kaudu.</span><span class="sxs-lookup"><span data-stu-id="ed793-233">Click Close via cash.</span></span>
10. <span data-ttu-id="ed793-234">Tehke väljal Automaatne valik Jah.</span><span class="sxs-lookup"><span data-stu-id="ed793-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="ed793-235">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ed793-235">Click OK.</span></span>
12. <span data-ttu-id="ed793-236">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ed793-236">Close the page.</span></span>
13. <span data-ttu-id="ed793-237">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="ed793-237">Click Transactions.</span></span>
