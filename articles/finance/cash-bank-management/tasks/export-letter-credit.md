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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d389c4a85bbf39a0974e8e456c781ae839461d87
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177366"
---
# <a name="export-letter-of-credit"></a><span data-ttu-id="aab41-103">Akreditiivi eksport</span><span class="sxs-lookup"><span data-stu-id="aab41-103">Export letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aab41-104">See protseduur selgitab akreditiivi eksportimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="aab41-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="aab41-105">Akreditiiv on panga väljastatud lepe, milles pank nõustub tagama makse ostja nimel, kui ostja ja müüja vahelise leppe tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="aab41-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="aab41-106">Enne seda protseduuri käitage protseduuri „Pangateenuste ja sisestusreeglite seadistamine” ja „Akreditiivi jaoks panga süsteemiteenuse leppe loomine”.</span><span class="sxs-lookup"><span data-stu-id="aab41-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="aab41-107">Selleks et protseduur õnnestuks, peab USMF-i demoettevõte olema valitud.</span><span class="sxs-lookup"><span data-stu-id="aab41-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="aab41-108">Akreditiivi eksportimise jaoks müügitellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="aab41-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="aab41-109">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="aab41-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="aab41-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="aab41-110">Click New.</span></span>
3. <span data-ttu-id="aab41-111">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aab41-112">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aab41-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="aab41-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="aab41-114">Laiendage või ahendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="aab41-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="aab41-115">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="aab41-116">Valige laoala, kus väljastatavat kaupa ladustatakse.</span><span class="sxs-lookup"><span data-stu-id="aab41-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="aab41-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aab41-118">Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="aab41-119">Valige ladu, kus väljastatavat kaupa ladustatakse.</span><span class="sxs-lookup"><span data-stu-id="aab41-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="aab41-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aab41-121">Märkus. Väljal Pangadokumendi tüüp tuleb valida väärtus „Akreditiiv”.</span><span class="sxs-lookup"><span data-stu-id="aab41-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="aab41-122">Valige väljal Pangadokumendi tüüp suvand Akreditiiv.</span><span class="sxs-lookup"><span data-stu-id="aab41-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="aab41-123">Laiendage või ahendage jaotist Tarne.</span><span class="sxs-lookup"><span data-stu-id="aab41-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="aab41-124">Valige suvandi Tarnekuupäeva kontroll sätteks Puudub.</span><span class="sxs-lookup"><span data-stu-id="aab41-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="aab41-125">Sisestage kuupäev väljale Nõutav sissetulekukuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="aab41-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aab41-126">Click OK.</span></span>
15. <span data-ttu-id="aab41-127">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="aab41-128">Valige väljastamiseks/müümiseks vajalik kaup.</span><span class="sxs-lookup"><span data-stu-id="aab41-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="aab41-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aab41-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="aab41-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="aab41-131">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="aab41-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="aab41-132">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="aab41-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="aab41-133">Klõpsake vahekaarti Tarne.</span><span class="sxs-lookup"><span data-stu-id="aab41-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="aab41-134">Sisestage kuupäev väljale Nõutav lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="aab41-135">Sisestage kuupäev väljale Kinnitatud lähetuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="aab41-136">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="aab41-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="aab41-137">Klõpsake suvandit Akreditiiv.</span><span class="sxs-lookup"><span data-stu-id="aab41-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="aab41-138">Tippige väärtus väljale Pangadokumendi number.</span><span class="sxs-lookup"><span data-stu-id="aab41-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="aab41-139">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="aab41-140">Laiendage või ahendage jaotist Panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="aab41-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="aab41-141">Klõpsake väljal Väljaandev pank otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="aab41-142">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="aab41-143">Klõpsake väljal Nõustav pank otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="aab41-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aab41-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="aab41-145">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="aab41-146">Klõpsake suvandit Müügitellimuse saadetiste toomine.</span><span class="sxs-lookup"><span data-stu-id="aab41-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="aab41-147">Klõpsake suvandit Pangadokumendi väljastamine.</span><span class="sxs-lookup"><span data-stu-id="aab41-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="aab41-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="aab41-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="aab41-149">Saatelehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="aab41-149">Post Packing slip</span></span>
1. <span data-ttu-id="aab41-150">Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.</span><span class="sxs-lookup"><span data-stu-id="aab41-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="aab41-151">Klõpsake valikut Saatelehe sisestamine.</span><span class="sxs-lookup"><span data-stu-id="aab41-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="aab41-152">Laiendage või ahendage jaotist Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="aab41-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="aab41-153">Väljal Kogus valige Kõik.</span><span class="sxs-lookup"><span data-stu-id="aab41-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="aab41-154">Laiendage või ahendage jaotist Häälestus.</span><span class="sxs-lookup"><span data-stu-id="aab41-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="aab41-155">Sisestage kuupäev väljale Saatelehe kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="aab41-156">Valige saadetise number.</span><span class="sxs-lookup"><span data-stu-id="aab41-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="aab41-157">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="aab41-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aab41-158">Click OK.</span></span>
10. <span data-ttu-id="aab41-159">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aab41-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="aab41-160">Müügiarve sisestamine</span><span class="sxs-lookup"><span data-stu-id="aab41-160">Post sales invoice</span></span>
1. <span data-ttu-id="aab41-161">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="aab41-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="aab41-162">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="aab41-162">Click Invoice.</span></span>
3. <span data-ttu-id="aab41-163">Laiendage või ahendage jaotist Ülevaade.</span><span class="sxs-lookup"><span data-stu-id="aab41-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="aab41-164">Valige saadetise number.</span><span class="sxs-lookup"><span data-stu-id="aab41-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="aab41-165">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="aab41-166">Laiendage või ahendage jaotist Häälestus.</span><span class="sxs-lookup"><span data-stu-id="aab41-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="aab41-167">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="aab41-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aab41-168">Click OK.</span></span>
9. <span data-ttu-id="aab41-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aab41-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="aab41-170">Saadetise dokumendi esitamise olek</span><span class="sxs-lookup"><span data-stu-id="aab41-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="aab41-171">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="aab41-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="aab41-172">Klõpsake suvandit Akreditiiv.</span><span class="sxs-lookup"><span data-stu-id="aab41-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="aab41-173">Laiendage või ahendage jaotist Read.</span><span class="sxs-lookup"><span data-stu-id="aab41-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="aab41-174">Märkus. Välja „Dokument on saadetud” väärtus peab olema „Jah”.</span><span class="sxs-lookup"><span data-stu-id="aab41-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="aab41-175">Akreditiivi eksportimise kinnitamine</span><span class="sxs-lookup"><span data-stu-id="aab41-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="aab41-176">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Ekspordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="aab41-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="aab41-177">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aab41-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="aab41-178">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aab41-179">Veenduge, et akreditiivi eksportimise tarne olek oleks „Arveldatud”.</span><span class="sxs-lookup"><span data-stu-id="aab41-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="aab41-180">Kliendi makse</span><span class="sxs-lookup"><span data-stu-id="aab41-180">Customer payment</span></span>
1. <span data-ttu-id="aab41-181">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="aab41-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="aab41-182">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="aab41-182">Click New.</span></span>
3. <span data-ttu-id="aab41-183">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="aab41-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="aab41-184">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aab41-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="aab41-185">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="aab41-186">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="aab41-186">Click Lines.</span></span>
7. <span data-ttu-id="aab41-187">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="aab41-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="aab41-188">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="aab41-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="aab41-189">Klõpsake suvandit Tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="aab41-189">Click Settlement.</span></span>
10. <span data-ttu-id="aab41-190">Valige märkeruut jaotise Kogusummad päises.</span><span class="sxs-lookup"><span data-stu-id="aab41-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="aab41-191">Märkus. Valige väljal Kuva suvand „Akreditiiv”.</span><span class="sxs-lookup"><span data-stu-id="aab41-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="aab41-192">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aab41-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="aab41-193">Märkige või tühjendage ruut Märgi.</span><span class="sxs-lookup"><span data-stu-id="aab41-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="aab41-194">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="aab41-194">Click OK.</span></span>
14. <span data-ttu-id="aab41-195">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="aab41-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="aab41-196">Kontrollige pangakonto numbri ja saadetise numbri üksikasju</span><span class="sxs-lookup"><span data-stu-id="aab41-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="aab41-197">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="aab41-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="aab41-198">Akreditiivi eksportimise kinnitamine pärast makset</span><span class="sxs-lookup"><span data-stu-id="aab41-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="aab41-199">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Ekspordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="aab41-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="aab41-200">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aab41-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="aab41-201">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aab41-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="aab41-202">Veenduge, et tarne olek oleks Makse vastu võetud ja saldo summa oleks 0.00.</span><span class="sxs-lookup"><span data-stu-id="aab41-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  
