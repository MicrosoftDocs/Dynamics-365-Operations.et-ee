---
title: Garantiikirja kanne
description: See protseduur selgitab garantiikirja töötlemist.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4dc6ee178121fae05d538f5103919442d91e65eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566106"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="159d7-103">Garantiikirja kanne</span><span class="sxs-lookup"><span data-stu-id="159d7-103">Letter of guarantee transaction</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="159d7-104">See protseduur selgitab garantiikirja töötlemist.</span><span class="sxs-lookup"><span data-stu-id="159d7-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="159d7-105">Enne selle toimingu tegemist peavad olema tehtud järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="159d7-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="159d7-106">Pangateenuste ja garantiikirjade sisestusreeglite häälestamine.</span><span class="sxs-lookup"><span data-stu-id="159d7-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="159d7-107">Garantiikirja jaoks panga süsteemiteenuse leppe loomine.</span><span class="sxs-lookup"><span data-stu-id="159d7-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="159d7-108">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="159d7-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="159d7-109">Garantiikirjaga müügitellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="159d7-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="159d7-110">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="159d7-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="159d7-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="159d7-111">Click New.</span></span>
3. <span data-ttu-id="159d7-112">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="159d7-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="159d7-113">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="159d7-113">Expand the General section.</span></span>
5. <span data-ttu-id="159d7-114">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="159d7-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="159d7-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="159d7-116">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="159d7-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="159d7-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="159d7-118">Valige väljal Pangadokumendi tüüp suvand Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="159d7-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-119">Click OK.</span></span>
11. <span data-ttu-id="159d7-120">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="159d7-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="159d7-121">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="159d7-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="159d7-122">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="159d7-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="159d7-123">Klõpsake vahekaarti Tarne.</span><span class="sxs-lookup"><span data-stu-id="159d7-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="159d7-124">Märkus. Valige suvandi Tarnekuupäeva kontroll sätteks Puudub</span><span class="sxs-lookup"><span data-stu-id="159d7-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="159d7-125">Sisestage kuupäev väljale Nõutav lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="159d7-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="159d7-126">Sisestage kuupäev väljale Kinnitatud lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="159d7-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guaranteerequest"></a><span data-ttu-id="159d7-127">Garantiikirja protsess Taotlemine</span><span class="sxs-lookup"><span data-stu-id="159d7-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="159d7-128">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="159d7-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="159d7-129">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="159d7-130">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="159d7-131">Klõpsake suvandit Taotlus rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="159d7-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="159d7-132">Sisestage või valige väärtus väljal Tüüp.</span><span class="sxs-lookup"><span data-stu-id="159d7-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="159d7-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="159d7-134">Sisestage number väljale Väärtus.</span><span class="sxs-lookup"><span data-stu-id="159d7-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="159d7-135">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="159d7-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="159d7-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-136">Click OK.</span></span>
10. <span data-ttu-id="159d7-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="159d7-137">Close the page.</span></span>

## <a name="process-letter-of-guaranteesubmit-to-bank"></a><span data-ttu-id="159d7-138">Garantiikirja protsess Edasta panka</span><span class="sxs-lookup"><span data-stu-id="159d7-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="159d7-139">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="159d7-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="159d7-140">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="159d7-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="159d7-141">Klõpsake suvandit Edasta panka, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="159d7-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="159d7-142">Sisestage väärtus väljale Pangakonto või valige see.</span><span class="sxs-lookup"><span data-stu-id="159d7-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="159d7-143">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="159d7-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-144">Click OK.</span></span>

## <a name="process-letter-of-guaranteereceive-from-bank"></a><span data-ttu-id="159d7-145">Garantiikirja Protsess Võta pangalt vastu</span><span class="sxs-lookup"><span data-stu-id="159d7-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="159d7-146">Klõpsake suvandit Võta pangalt vastu, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="159d7-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="159d7-147">Sisestage väärtus väljale Panga number.</span><span class="sxs-lookup"><span data-stu-id="159d7-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="159d7-148">Kontrollige arvutatud väärtusi väljadel Marginaal ja Kulu.</span><span class="sxs-lookup"><span data-stu-id="159d7-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="159d7-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-149">Click OK.</span></span>
4. <span data-ttu-id="159d7-150">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="159d7-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="159d7-151">Kontrollige kirjet Võta pangalt vastu.</span><span class="sxs-lookup"><span data-stu-id="159d7-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="159d7-152">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="159d7-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="159d7-153">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="159d7-153">Click Lines.</span></span>
    * <span data-ttu-id="159d7-154">Kontrollige töölehekannete sisestamist.</span><span class="sxs-lookup"><span data-stu-id="159d7-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="159d7-155">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="159d7-155">Close the page.</span></span>

## <a name="process-letter-of-guaranteegive-to-beneficiary"></a><span data-ttu-id="159d7-156">Garantiikirja protsess Anna kasusaajale</span><span class="sxs-lookup"><span data-stu-id="159d7-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="159d7-157">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="159d7-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="159d7-158">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="159d7-159">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="159d7-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="159d7-160">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="159d7-161">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="159d7-162">Klõpsake suvandit Anna kasusaajale, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="159d7-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="159d7-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-163">Click OK.</span></span>
8. <span data-ttu-id="159d7-164">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="159d7-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="159d7-165">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="159d7-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="159d7-166">Klõpsake suvandit Anna kasusaajale, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="159d7-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="159d7-167">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-167">Click OK.</span></span>
12. <span data-ttu-id="159d7-168">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="159d7-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="159d7-169">Kinnitage kirje Anna kasusaajale.</span><span class="sxs-lookup"><span data-stu-id="159d7-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guaranteeincrease-value"></a><span data-ttu-id="159d7-170">Garantiikirja protsess Suurenda väärtust</span><span class="sxs-lookup"><span data-stu-id="159d7-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="159d7-171">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="159d7-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="159d7-172">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="159d7-173">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="159d7-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="159d7-174">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="159d7-175">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="159d7-176">Klõpsake suvandit suurenda väärtust rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="159d7-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="159d7-177">Sisestage arv väljale Lisatav väärtus.</span><span class="sxs-lookup"><span data-stu-id="159d7-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="159d7-178">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-178">Click OK.</span></span>
9. <span data-ttu-id="159d7-179">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="159d7-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="159d7-180">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="159d7-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="159d7-181">Klõpsake suvandit suurenda väärtust rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="159d7-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="159d7-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-182">Click OK.</span></span>
13. <span data-ttu-id="159d7-183">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="159d7-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="159d7-184">Kontrollige kirjet Suurenda väärtust.</span><span class="sxs-lookup"><span data-stu-id="159d7-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="159d7-185">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="159d7-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="159d7-186">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="159d7-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="159d7-187">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="159d7-187">Click Lines.</span></span>
    * <span data-ttu-id="159d7-188">Kontrollige sisestatud töölehekandeid.</span><span class="sxs-lookup"><span data-stu-id="159d7-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guaranteeliquidate"></a><span data-ttu-id="159d7-189">Garantiikirja protsess Likvideeri</span><span class="sxs-lookup"><span data-stu-id="159d7-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="159d7-190">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="159d7-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="159d7-191">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="159d7-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="159d7-192">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="159d7-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="159d7-193">Klõpsake suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="159d7-194">Klõpsake tegevuspaanil suvandit Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="159d7-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="159d7-195">Klõpsake suvandit Likvideeri, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="159d7-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="159d7-196">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-196">Click OK.</span></span>
8. <span data-ttu-id="159d7-197">Avage Sularaha- ja pangahaldus > Garantiikirjad > Garantiikirjad.</span><span class="sxs-lookup"><span data-stu-id="159d7-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="159d7-198">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="159d7-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="159d7-199">Klõpsake suvandit Likvideeri, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="159d7-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="159d7-200">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="159d7-200">Click OK.</span></span>
12. <span data-ttu-id="159d7-201">Laiendage jaotist Tegevused.</span><span class="sxs-lookup"><span data-stu-id="159d7-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="159d7-202">Kontrollige kirjet Likvideeri.</span><span class="sxs-lookup"><span data-stu-id="159d7-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="159d7-203">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="159d7-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="159d7-204">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="159d7-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="159d7-205">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="159d7-205">Click Lines.</span></span>
    * <span data-ttu-id="159d7-206">Kontrollige sisestatud töölehekandeid.</span><span class="sxs-lookup"><span data-stu-id="159d7-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="159d7-207">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="159d7-207">Close the page.</span></span>

