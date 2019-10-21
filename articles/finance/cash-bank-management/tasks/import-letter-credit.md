---
title: Akreditiivi importimine
description: See protseduur selgitab akreditiivi importimise protsessi.
author: kweekley
manager: AnnBe
ms.date: 02/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts, PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, BankLCImport,  PurchEditLines, VendEditInvoice, SrsReportViewerForm, LedgerJournalTable, LedgerJournalTransVendPaym, VendOpenTrans, SysQueryForm, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72a50b2cdda5d66e8aa4660f914e6f5e51531b5f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188138"
---
# <a name="import-letter-of-credit"></a><span data-ttu-id="10c45-103">Akreditiivi importimine</span><span class="sxs-lookup"><span data-stu-id="10c45-103">Import letter of credit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="10c45-104">See protseduur selgitab akreditiivi importimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="10c45-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="10c45-105">Enne seda protseduuri tuleb häälestada järgmised üksused: panga süsteemiteenused, sisestusreeglid, panga süsteemiteenuse lepe ja hankija panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="10c45-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="10c45-106">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="10c45-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="10c45-107">Ostutellimuse loomine akreditiiviga</span><span class="sxs-lookup"><span data-stu-id="10c45-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="10c45-108">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="10c45-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="10c45-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="10c45-109">Click New.</span></span>
3. <span data-ttu-id="10c45-110">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="10c45-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="10c45-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="10c45-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="10c45-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="10c45-113">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="10c45-113">Expand the General section.</span></span>
7. <span data-ttu-id="10c45-114">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="10c45-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="10c45-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="10c45-116">Sisestage või valige väärtus väljal Ladu.</span><span class="sxs-lookup"><span data-stu-id="10c45-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="10c45-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="10c45-118">Sisestage kuupäev väljale Aruandluskuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="10c45-119">Sisestage kuupäev väljale Tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="10c45-120">Märkus. Väljal „Pangadokumendi tüüp” tuleb valida väärtus „Akreditiiv”.</span><span class="sxs-lookup"><span data-stu-id="10c45-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="10c45-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10c45-121">Click OK.</span></span>
14. <span data-ttu-id="10c45-122">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="10c45-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="10c45-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="10c45-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="10c45-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="10c45-125">Laiendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="10c45-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="10c45-126">Klõpsake vahekaarti Tarne.</span><span class="sxs-lookup"><span data-stu-id="10c45-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="10c45-127">Sisestage kuupäev väljale Tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="10c45-128">Sisestage kuupäev väljale Kinnitatud tarnekuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="10c45-129">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="10c45-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="10c45-130">Määratlege akreditiivi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="10c45-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="10c45-131">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="10c45-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="10c45-132">Klõpsake suvandit Akreditiiv / sissenõude importimine.</span><span class="sxs-lookup"><span data-stu-id="10c45-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="10c45-133">Sisestage kuupäev ja kellaaeg väljale Avalduse kuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="10c45-134">Veenduge, et väljal „Pangakonto” on aktiivne vaikepangakonto, mis põhineb avalduse kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="10c45-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="10c45-135">Tippige väärtus väljale Pangadokumendi number.</span><span class="sxs-lookup"><span data-stu-id="10c45-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="10c45-136">Sisestage kuupäev ja kellaaeg väljale Sissetuleku kuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="10c45-137">Laiendage jaotist Pangadokument.</span><span class="sxs-lookup"><span data-stu-id="10c45-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="10c45-138">Sisestage kuupäev ja kellaaeg väljale Aegumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="10c45-139">Laiendage jaotist Panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="10c45-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="10c45-140">Sisestage või valige väärtus väljal Nõustav pank.</span><span class="sxs-lookup"><span data-stu-id="10c45-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="10c45-141">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="10c45-142">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="10c45-142">Click Save.</span></span>
33. <span data-ttu-id="10c45-143">Klõpsake suvandit Ostutellimuse saadetiste toomine.</span><span class="sxs-lookup"><span data-stu-id="10c45-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="10c45-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-144">Close the page.</span></span>
35. <span data-ttu-id="10c45-145">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="10c45-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="10c45-146">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="10c45-146">Click Confirm.</span></span>
37. <span data-ttu-id="10c45-147">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="10c45-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="10c45-148">Klõpsake suvandit Akreditiiv / sissenõude importimine.</span><span class="sxs-lookup"><span data-stu-id="10c45-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="10c45-149">Klõpsake suvandit Töötle.</span><span class="sxs-lookup"><span data-stu-id="10c45-149">Click Process.</span></span>
40. <span data-ttu-id="10c45-150">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="10c45-150">Click Confirm.</span></span>
    * <span data-ttu-id="10c45-151">Veenduge, et süsteemiteenuse saldo vähendaks ostutellimuse summat.</span><span class="sxs-lookup"><span data-stu-id="10c45-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="10c45-152">Selles näites on ostusumma = 500,00, süsteemiteenuse limiit = 10 000,00, seega on süsteemiteenuse saldo = 9500,00.</span><span class="sxs-lookup"><span data-stu-id="10c45-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="10c45-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-153">Close the page.</span></span>
42. <span data-ttu-id="10c45-154">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="10c45-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="10c45-155">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="10c45-155">Click Save.</span></span>
44. <span data-ttu-id="10c45-156">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="10c45-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="10c45-157">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="10c45-157">Click Confirm.</span></span>
    * <span data-ttu-id="10c45-158">Parandage akreditiivi ühiku hinna muutuse tõttu.</span><span class="sxs-lookup"><span data-stu-id="10c45-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="10c45-159">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="10c45-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="10c45-160">Klõpsake suvandit Akreditiiv / sissenõude importimine.</span><span class="sxs-lookup"><span data-stu-id="10c45-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="10c45-161">Parandage akreditiivi ühiku hinna muutuse tõttu.</span><span class="sxs-lookup"><span data-stu-id="10c45-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="10c45-162">Klõpsake suvandit Töötle.</span><span class="sxs-lookup"><span data-stu-id="10c45-162">Click Process.</span></span>
49. <span data-ttu-id="10c45-163">Klõpsake käsku Paranda.</span><span class="sxs-lookup"><span data-stu-id="10c45-163">Click Amend.</span></span>
50. <span data-ttu-id="10c45-164">Klõpsake nuppu Eemalda.</span><span class="sxs-lookup"><span data-stu-id="10c45-164">Click Remove.</span></span>
51. <span data-ttu-id="10c45-165">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="10c45-165">Click Yes.</span></span>
52. <span data-ttu-id="10c45-166">Klõpsake suvandit Ostutellimuse saadetiste toomine.</span><span class="sxs-lookup"><span data-stu-id="10c45-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="10c45-167">Klõpsake suvandit Töötle.</span><span class="sxs-lookup"><span data-stu-id="10c45-167">Click Process.</span></span>
54. <span data-ttu-id="10c45-168">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="10c45-168">Click Confirm.</span></span>
    * <span data-ttu-id="10c45-169">Veenduge, et süsteemiteenuse saldo vähendaks ostutellimuse summat.</span><span class="sxs-lookup"><span data-stu-id="10c45-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="10c45-170">Selles näites on muudetud ostusumma = 600,00, süsteemiteenuse limiit = 10 000,00, seega on süsteemiteenuse saldo = 9400,00.</span><span class="sxs-lookup"><span data-stu-id="10c45-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="10c45-171">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="10c45-172">Saatelehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="10c45-172">Post Packing slip</span></span>
1. <span data-ttu-id="10c45-173">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="10c45-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="10c45-174">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="10c45-174">Click Product receipt.</span></span>
3. <span data-ttu-id="10c45-175">Sisestage väärtus väljale PurchParmTable_Num.</span><span class="sxs-lookup"><span data-stu-id="10c45-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="10c45-176">Valige saadetise number, mis loodi viitega akreditiivile.</span><span class="sxs-lookup"><span data-stu-id="10c45-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="10c45-177">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10c45-178">Sisestage kuupäev väljale Toote sissetuleku kuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="10c45-179">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10c45-179">Click OK.</span></span>
7. <span data-ttu-id="10c45-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-180">Close the page.</span></span>
8. <span data-ttu-id="10c45-181">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="10c45-182">Akreditiivi importimise oleku kinnitamine</span><span class="sxs-lookup"><span data-stu-id="10c45-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="10c45-183">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Impordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="10c45-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="10c45-184">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="10c45-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="10c45-185">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="10c45-186">Kinnitage akreditiivi importimise olek.</span><span class="sxs-lookup"><span data-stu-id="10c45-186">Verify the Import letter of credit status.</span></span>     
4. <span data-ttu-id="10c45-187">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-187">Close the page.</span></span>
5. <span data-ttu-id="10c45-188">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="10c45-189">Ostuarve sisestamine</span><span class="sxs-lookup"><span data-stu-id="10c45-189">Post purchase invoice</span></span>
1. <span data-ttu-id="10c45-190">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="10c45-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="10c45-191">Valige akreditiiviga loodud ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="10c45-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="10c45-192">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="10c45-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="10c45-193">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="10c45-194">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="10c45-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="10c45-195">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="10c45-195">Click Invoice.</span></span>
6. <span data-ttu-id="10c45-196">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="10c45-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="10c45-197">Sisestage või valige väärtus väljal Saadetise number.</span><span class="sxs-lookup"><span data-stu-id="10c45-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="10c45-198">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="10c45-199">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="10c45-200">Klõpsake valikut Värskenda vastandamise olek.</span><span class="sxs-lookup"><span data-stu-id="10c45-200">Click Update match status.</span></span>
11. <span data-ttu-id="10c45-201">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="10c45-201">Click Post.</span></span>
12. <span data-ttu-id="10c45-202">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-202">Close the page.</span></span>
13. <span data-ttu-id="10c45-203">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="10c45-204">Akreditiivi importimise oleku kinnitamine</span><span class="sxs-lookup"><span data-stu-id="10c45-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="10c45-205">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Impordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="10c45-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="10c45-206">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="10c45-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="10c45-207">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="10c45-208">Kinnitage akreditiivi importimine.</span><span class="sxs-lookup"><span data-stu-id="10c45-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="10c45-209">Kinnitage: saadetise olek = arveldatud Panga süsteemiteenuse üksikasjad</span><span class="sxs-lookup"><span data-stu-id="10c45-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="10c45-210">Klõpsake käsku Kuva.</span><span class="sxs-lookup"><span data-stu-id="10c45-210">Click View.</span></span>
5. <span data-ttu-id="10c45-211">Klõpsake suvandit Avalduse printimine.</span><span class="sxs-lookup"><span data-stu-id="10c45-211">Click Print application.</span></span>
6. <span data-ttu-id="10c45-212">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10c45-212">Click OK.</span></span>
    * <span data-ttu-id="10c45-213">Veenduge, et akreditiiv prinditaks.</span><span class="sxs-lookup"><span data-stu-id="10c45-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="10c45-214">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-214">Close the page.</span></span>
8. <span data-ttu-id="10c45-215">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-215">Close the page.</span></span>
9. <span data-ttu-id="10c45-216">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="10c45-217">Akreditiiviga loodud ostuarve makse töölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="10c45-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="10c45-218">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="10c45-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="10c45-219">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="10c45-219">Click New.</span></span>
3. <span data-ttu-id="10c45-220">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="10c45-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="10c45-221">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="10c45-222">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="10c45-222">Click Lines.</span></span>
6. <span data-ttu-id="10c45-223">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="10c45-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="10c45-224">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="10c45-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="10c45-225">Klõpsake suvandit Kannete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="10c45-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="10c45-226">Laiendage jaotist Kogusummad.</span><span class="sxs-lookup"><span data-stu-id="10c45-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="10c45-227">Valige suvand väljal Kuva.</span><span class="sxs-lookup"><span data-stu-id="10c45-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="10c45-228">Veenduge, et väljad Pangakonto number ja Saadetise number oleksid uuendatud.</span><span class="sxs-lookup"><span data-stu-id="10c45-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="10c45-229">Märkige ruut Märgi.</span><span class="sxs-lookup"><span data-stu-id="10c45-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="10c45-230">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10c45-230">Click OK.</span></span>
13. <span data-ttu-id="10c45-231">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="10c45-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="10c45-232">Veenduge, et väljad Pangakonto number ja Saadetise number oleksid uuendatud.</span><span class="sxs-lookup"><span data-stu-id="10c45-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="10c45-233">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="10c45-233">Click Post.</span></span>
15. <span data-ttu-id="10c45-234">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-234">Close the page.</span></span>
16. <span data-ttu-id="10c45-235">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="10c45-236">Pärast arve tasumist kontrollige akreditiivi importimise olekut</span><span class="sxs-lookup"><span data-stu-id="10c45-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="10c45-237">Avage jaotis Sularaha- ja pangahaldus > Akreditiivid > Impordi akreditiiv ja sissenõue.</span><span class="sxs-lookup"><span data-stu-id="10c45-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="10c45-238">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="10c45-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="10c45-239">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="10c45-240">Kinnitage akreditiivi importimise olek.</span><span class="sxs-lookup"><span data-stu-id="10c45-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="10c45-241">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="10c45-242">Kontrollige panga süsteemiteenuse limiiti ja tulususe aruannet</span><span class="sxs-lookup"><span data-stu-id="10c45-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="10c45-243">Avage jaotis Sularaha- ja pangahaldus > Päringud ja aruanded > Akreditiivid või garantiikirjad > Pangateenuste ja kasutamise aruanne.</span><span class="sxs-lookup"><span data-stu-id="10c45-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="10c45-244">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="10c45-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="10c45-245">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="10c45-245">Click Filter.</span></span>
    * <span data-ttu-id="10c45-246">Määratlege väljal Kriteeriumid nõutav pangakonto.</span><span class="sxs-lookup"><span data-stu-id="10c45-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="10c45-247">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="10c45-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="10c45-248">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="10c45-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="10c45-249">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10c45-249">Click OK.</span></span>
7. <span data-ttu-id="10c45-250">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10c45-250">Click OK.</span></span>
    * <span data-ttu-id="10c45-251">Kinnitage aruanne, kus on loetletud kanded.</span><span class="sxs-lookup"><span data-stu-id="10c45-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="10c45-252">Veenduge, et aruandes oleks loetletud kanded koos pangadokumendi numbri, süsteemiteenuse limiidi, kasutatud summa ja süsteemiteenuse saldo summa.</span><span class="sxs-lookup"><span data-stu-id="10c45-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="10c45-253">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10c45-253">Close the page.</span></span>

