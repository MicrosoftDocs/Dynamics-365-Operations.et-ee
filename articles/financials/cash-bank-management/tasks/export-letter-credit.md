---
title: Akreditiivi eksport
description: See protseduur selgitab akreditiivi eksportimise protsessi.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustBankAccounts, DefaultDashboard, SalesTableListPage, SalesCreateOrder, SalesTable, BankLCExport, SalesEditLines,  LedgerJournalTable, LedgerJournalTransCustPaym, CustOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 730a6cc6ed4872f8d0ad92b89665587f472f6791
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566152"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="f970c-103">Akreditiivi eksport</span><span class="sxs-lookup"><span data-stu-id="f970c-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f970c-104">See protseduur selgitab akreditiivi eksportimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="f970c-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="f970c-105">Akreditiiv on panga väljastatud lepe, milles pank nõustub tagama makse ostja nimel, kui ostja ja müüja vahelise leppe tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="f970c-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="f970c-106">Enne seda protseduuri käitage protseduuri „Pangateenuste ja sisestusreeglite seadistamine” ja „Akreditiivi jaoks panga süsteemiteenuse leppe loomine”.</span><span class="sxs-lookup"><span data-stu-id="f970c-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="f970c-107">Selleks et protseduur õnnestuks, peab USMF-i demoettevõte olema valitud.</span><span class="sxs-lookup"><span data-stu-id="f970c-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="f970c-108">Akreditiivi eksportimise jaoks müügitellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="f970c-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="f970c-109">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="f970c-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f970c-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f970c-110">Click New.</span></span>
3. <span data-ttu-id="f970c-111">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f970c-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f970c-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="f970c-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f970c-114">Laiendage või ahendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="f970c-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="f970c-115">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f970c-116">Valige laoala, kus väljastatavat kaupa ladustatakse.</span><span class="sxs-lookup"><span data-stu-id="f970c-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="f970c-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f970c-118">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f970c-119">Valige ladu, kus väljastatavat kaupa ladustatakse.</span><span class="sxs-lookup"><span data-stu-id="f970c-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="f970c-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f970c-121">Märkus. Väljal Pangadokumendi tüüp tuleb valida väärtus „Akreditiiv”.</span><span class="sxs-lookup"><span data-stu-id="f970c-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="f970c-122">Valige väljal Pangadokumendi tüüp suvand Akreditiiv.</span><span class="sxs-lookup"><span data-stu-id="f970c-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="f970c-123">Laiendage või ahendage jaotist Tarne.</span><span class="sxs-lookup"><span data-stu-id="f970c-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="f970c-124">Valige suvandi Tarnekuupäeva kontroll sätteks Puudub.</span><span class="sxs-lookup"><span data-stu-id="f970c-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="f970c-125">Sisestage kuupäev väljale Nõutav sissetulekukuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="f970c-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f970c-126">Click OK.</span></span>
15. <span data-ttu-id="f970c-127">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="f970c-128">Valige väljastamiseks/müümiseks vajalik kaup.</span><span class="sxs-lookup"><span data-stu-id="f970c-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="f970c-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f970c-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="f970c-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f970c-131">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="f970c-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="f970c-132">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f970c-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="f970c-133">Klõpsake vahekaarti Tarne.</span><span class="sxs-lookup"><span data-stu-id="f970c-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="f970c-134">Sisestage kuupäev väljale Nõutav lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="f970c-135">Sisestage kuupäev väljale Kinnitatud lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="f970c-136">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="f970c-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="f970c-137">Klõpsake suvandit Akreditiiv.</span><span class="sxs-lookup"><span data-stu-id="f970c-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="f970c-138">Tippige väärtus väljale Pangadokumendi number.</span><span class="sxs-lookup"><span data-stu-id="f970c-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="f970c-139">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="f970c-140">Laiendage või ahendage jaotist Panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="f970c-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="f970c-141">Klõpsake väljal Väljaandev pank otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="f970c-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="f970c-143">Klõpsake väljal Nõustav pank otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="f970c-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f970c-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="f970c-145">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="f970c-146">Klõpsake suvandit Müügitellimuse saadetiste toomine.</span><span class="sxs-lookup"><span data-stu-id="f970c-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="f970c-147">Klõpsake suvandit Pangadokumendi väljastamine.</span><span class="sxs-lookup"><span data-stu-id="f970c-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="f970c-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f970c-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="f970c-149">Saatelehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="f970c-149">Post Packing slip</span></span>
1. <span data-ttu-id="f970c-150">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="f970c-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="f970c-151">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f970c-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="f970c-152">Laiendage või ahendage jaotist Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f970c-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="f970c-153">Väljal Kogus valige Kõik.</span><span class="sxs-lookup"><span data-stu-id="f970c-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="f970c-154">Laiendage või ahendage jaotist Häälestus.</span><span class="sxs-lookup"><span data-stu-id="f970c-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="f970c-155">Sisestage kuupäev väljale Saatelehe kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="f970c-156">Valige saadetise number.</span><span class="sxs-lookup"><span data-stu-id="f970c-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="f970c-157">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f970c-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f970c-158">Click OK.</span></span>
10. <span data-ttu-id="f970c-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f970c-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="f970c-160">Müügiarve sisestamine</span><span class="sxs-lookup"><span data-stu-id="f970c-160">Post sales invoice</span></span>
1. <span data-ttu-id="f970c-161">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="f970c-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f970c-162">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="f970c-162">Click Invoice.</span></span>
3. <span data-ttu-id="f970c-163">Laiendage või ahendage jaotist Ülevaade.</span><span class="sxs-lookup"><span data-stu-id="f970c-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="f970c-164">Valige saadetise number.</span><span class="sxs-lookup"><span data-stu-id="f970c-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="f970c-165">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f970c-166">Laiendage või ahendage jaotist Häälestus.</span><span class="sxs-lookup"><span data-stu-id="f970c-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="f970c-167">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="f970c-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f970c-168">Click OK.</span></span>
9. <span data-ttu-id="f970c-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f970c-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="f970c-170">Saadetise dokumendi esitamise olek</span><span class="sxs-lookup"><span data-stu-id="f970c-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="f970c-171">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="f970c-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="f970c-172">Klõpsake suvandit Akreditiiv.</span><span class="sxs-lookup"><span data-stu-id="f970c-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="f970c-173">Laiendage või ahendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="f970c-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="f970c-174">Märkus. Välja „Dokument on saadetud” väärtus peab olema „Jah”.</span><span class="sxs-lookup"><span data-stu-id="f970c-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="f970c-175">Akreditiivi eksportimise kinnitamine</span><span class="sxs-lookup"><span data-stu-id="f970c-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="f970c-176">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Ekspordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="f970c-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="f970c-177">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f970c-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f970c-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f970c-179">Veenduge, et akreditiivi eksportimise tarne olek oleks „Arveldatud”.</span><span class="sxs-lookup"><span data-stu-id="f970c-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="f970c-180">Kliendi makse</span><span class="sxs-lookup"><span data-stu-id="f970c-180">Customer payment</span></span>
1. <span data-ttu-id="f970c-181">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="f970c-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="f970c-182">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f970c-182">Click New.</span></span>
3. <span data-ttu-id="f970c-183">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f970c-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f970c-184">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f970c-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f970c-185">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f970c-186">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="f970c-186">Click Lines.</span></span>
7. <span data-ttu-id="f970c-187">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f970c-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="f970c-188">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="f970c-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="f970c-189">Klõpsake suvandit Tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="f970c-189">Click Settlement.</span></span>
10. <span data-ttu-id="f970c-190">Valige märkeruut jaotise Kogusummad päises.</span><span class="sxs-lookup"><span data-stu-id="f970c-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="f970c-191">Märkus. Valige väljal Kuva suvand „Akreditiiv”.</span><span class="sxs-lookup"><span data-stu-id="f970c-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="f970c-192">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f970c-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="f970c-193">Märkige või tühjendage ruut Märgi.</span><span class="sxs-lookup"><span data-stu-id="f970c-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="f970c-194">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f970c-194">Click OK.</span></span>
14. <span data-ttu-id="f970c-195">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="f970c-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="f970c-196">Kontrollige pangakonto numbri ja saadetise numbri üksikasju</span><span class="sxs-lookup"><span data-stu-id="f970c-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="f970c-197">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="f970c-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="f970c-198">Akreditiivi eksportimise kinnitamine pärast makset</span><span class="sxs-lookup"><span data-stu-id="f970c-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="f970c-199">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Ekspordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="f970c-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="f970c-200">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f970c-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f970c-201">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f970c-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f970c-202">Veenduge, et tarne olek oleks Makse vastu võetud ja saldo summa oleks 0.00.</span><span class="sxs-lookup"><span data-stu-id="f970c-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  

