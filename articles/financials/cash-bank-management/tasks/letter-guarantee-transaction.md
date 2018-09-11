--- 
title: Garantiikirja kanne
description: "See protseduur selgitab garantiikirja töötlemist."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 3b15133106d751c28029862217427e47085044f4
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="45f9c-103">Garantiikirja kanne</span><span class="sxs-lookup"><span data-stu-id="45f9c-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="45f9c-104">See protseduur selgitab garantiikirja töötlemist.</span><span class="sxs-lookup"><span data-stu-id="45f9c-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="45f9c-105">Enne selle toimingu tegemist peavad olema tehtud järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="45f9c-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="45f9c-106">Pangateenuste ja garantiikirjade sisestusreeglite häälestamine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="45f9c-107">Garantiikirja jaoks panga süsteemiteenuse leppe loomine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="45f9c-108">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="45f9c-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="45f9c-109">Garantiikirjaga müügitellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="45f9c-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="45f9c-110">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="45f9c-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="45f9c-111">Click New.</span></span>
3. <span data-ttu-id="45f9c-112">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="45f9c-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="45f9c-113">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-113">Expand the General section.</span></span>
5. <span data-ttu-id="45f9c-114">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="45f9c-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="45f9c-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="45f9c-116">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="45f9c-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="45f9c-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="45f9c-118">Valige väljal Pangadokumendi tüüp suvand Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="45f9c-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-119">Click OK.</span></span>
11. <span data-ttu-id="45f9c-120">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="45f9c-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="45f9c-121">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="45f9c-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="45f9c-122">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="45f9c-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="45f9c-123">Klõpsake vahekaarti Tarne.</span><span class="sxs-lookup"><span data-stu-id="45f9c-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="45f9c-124">Märkus. Valige suvandi Tarnekuupäeva kontroll sätteks Puudub</span><span class="sxs-lookup"><span data-stu-id="45f9c-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="45f9c-125">Sisestage kuupäev väljale Nõutav lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="45f9c-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="45f9c-126">Sisestage kuupäev väljale Kinnitatud lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="45f9c-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="45f9c-127">Garantiikirja protsess Taotlemine</span><span class="sxs-lookup"><span data-stu-id="45f9c-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="45f9c-128">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="45f9c-129">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="45f9c-130">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="45f9c-131">Klõpsake suvandit Taotlus rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="45f9c-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="45f9c-132">Sisestage või valige väärtus väljal Tüüp.</span><span class="sxs-lookup"><span data-stu-id="45f9c-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="45f9c-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="45f9c-134">Sisestage number väljale Väärtus.</span><span class="sxs-lookup"><span data-stu-id="45f9c-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="45f9c-135">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="45f9c-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="45f9c-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-136">Click OK.</span></span>
10. <span data-ttu-id="45f9c-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="45f9c-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="45f9c-138">Garantiikirja protsess Edasta panka</span><span class="sxs-lookup"><span data-stu-id="45f9c-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="45f9c-139">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="45f9c-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="45f9c-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45f9c-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="45f9c-141">Klõpsake suvandit Edasta panka, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="45f9c-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="45f9c-142">Sisestage väärtus väljale Pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="45f9c-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="45f9c-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="45f9c-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="45f9c-145">Garantiikirja Protsess Võta pangalt vastu</span><span class="sxs-lookup"><span data-stu-id="45f9c-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="45f9c-146">Klõpsake suvandit Võta pangalt vastu, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="45f9c-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="45f9c-147">Sisestage väärtus väljale Panga number.</span><span class="sxs-lookup"><span data-stu-id="45f9c-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="45f9c-148">Kontrollige arvutatud väärtusi väljadel Marginaal ja Kulu.</span><span class="sxs-lookup"><span data-stu-id="45f9c-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="45f9c-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-149">Click OK.</span></span>
4. <span data-ttu-id="45f9c-150">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="45f9c-151">Kontrollige kirjet Võta pangalt vastu.</span><span class="sxs-lookup"><span data-stu-id="45f9c-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="45f9c-152">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="45f9c-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="45f9c-153">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="45f9c-153">Click Lines.</span></span>
    * <span data-ttu-id="45f9c-154">Kontrollige töölehekannete sisestamist.</span><span class="sxs-lookup"><span data-stu-id="45f9c-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="45f9c-155">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="45f9c-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="45f9c-156">Garantiikirja protsess Anna kasusaajale</span><span class="sxs-lookup"><span data-stu-id="45f9c-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="45f9c-157">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="45f9c-158">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="45f9c-159">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="45f9c-160">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="45f9c-161">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="45f9c-162">Klõpsake suvandit Anna kasusaajale, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="45f9c-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="45f9c-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-163">Click OK.</span></span>
8. <span data-ttu-id="45f9c-164">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="45f9c-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="45f9c-165">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45f9c-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="45f9c-166">Klõpsake suvandit Anna kasusaajale, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="45f9c-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="45f9c-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-167">Click OK.</span></span>
12. <span data-ttu-id="45f9c-168">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="45f9c-169">Kinnitage kirje Anna kasusaajale.</span><span class="sxs-lookup"><span data-stu-id="45f9c-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="45f9c-170">Garantiikirja protsess Suurenda väärtust</span><span class="sxs-lookup"><span data-stu-id="45f9c-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="45f9c-171">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="45f9c-172">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="45f9c-173">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="45f9c-174">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="45f9c-175">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="45f9c-176">Klõpsake suvandit suurenda väärtust rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="45f9c-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="45f9c-177">Sisestage arv väljale Lisatav väärtus.</span><span class="sxs-lookup"><span data-stu-id="45f9c-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="45f9c-178">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-178">Click OK.</span></span>
9. <span data-ttu-id="45f9c-179">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="45f9c-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="45f9c-180">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45f9c-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="45f9c-181">Klõpsake suvandit suurenda väärtust rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="45f9c-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="45f9c-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-182">Click OK.</span></span>
13. <span data-ttu-id="45f9c-183">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="45f9c-184">Kontrollige kirjet Suurenda väärtust.</span><span class="sxs-lookup"><span data-stu-id="45f9c-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="45f9c-185">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45f9c-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="45f9c-186">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="45f9c-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="45f9c-187">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="45f9c-187">Click Lines.</span></span>
    * <span data-ttu-id="45f9c-188">Kontrollige sisestatud töölehekandeid.</span><span class="sxs-lookup"><span data-stu-id="45f9c-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="45f9c-189">Garantiikirja protsess Likvideeri</span><span class="sxs-lookup"><span data-stu-id="45f9c-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="45f9c-190">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="45f9c-191">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="45f9c-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="45f9c-192">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="45f9c-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="45f9c-193">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="45f9c-194">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="45f9c-195">Klõpsake suvandit Likvideeri, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="45f9c-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="45f9c-196">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-196">Click OK.</span></span>
8. <span data-ttu-id="45f9c-197">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="45f9c-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="45f9c-198">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45f9c-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="45f9c-199">Klõpsake suvandit Likvideeri, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="45f9c-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="45f9c-200">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="45f9c-200">Click OK.</span></span>
12. <span data-ttu-id="45f9c-201">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="45f9c-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="45f9c-202">Kontrollige kirjet Likvideeri.</span><span class="sxs-lookup"><span data-stu-id="45f9c-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="45f9c-203">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="45f9c-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="45f9c-204">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="45f9c-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="45f9c-205">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="45f9c-205">Click Lines.</span></span>
    * <span data-ttu-id="45f9c-206">Kontrollige sisestatud töölehekandeid.</span><span class="sxs-lookup"><span data-stu-id="45f9c-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="45f9c-207">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="45f9c-207">Close the page.</span></span>


