--- 
title: "Elektroonilise aruandluse (ER) mudeli vastenduse määratlemine ja andmeallikate valimine"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab valida andmeallikaid elektroonilise aruandluse (ER) andmemudeli jaoks."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 512e24b5d0e20f00890e2a9abfe45b660a913913
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="define-model-mapping-and-select-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="394c8-103">Elektroonilise aruandluse (ER) mudeli vastenduse määratlemine ja andmeallikate valimine</span><span class="sxs-lookup"><span data-stu-id="394c8-103">Define model mapping and select data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="394c8-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab valida andmeallikaid elektroonilise aruandluse (ER) andmemudeli jaoks.</span><span class="sxs-lookup"><span data-stu-id="394c8-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="394c8-105">Andmeallikad seotakse valitud andmemudeli üksikute komponentidega kujundamise ajal ja täidetakse selle andmemudeli äriandmetega töö ajal.</span><span class="sxs-lookup"><span data-stu-id="394c8-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="394c8-106">Selles näites valite andmeallikad olemasoleva andmemudeli jaoks, mis on loodud näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Uue andmemudeli loomine.</span><span class="sxs-lookup"><span data-stu-id="394c8-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="394c8-107">Elektroonilise aruandluse konfiguratsioonipuu avamine</span><span class="sxs-lookup"><span data-stu-id="394c8-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="394c8-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="394c8-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="394c8-109">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="394c8-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="394c8-110">Sisestage uue mudeli vastendamine</span><span class="sxs-lookup"><span data-stu-id="394c8-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="394c8-111">Valige puul suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="394c8-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="394c8-112">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="394c8-112">Click Designer.</span></span>
3. <span data-ttu-id="394c8-113">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="394c8-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="394c8-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="394c8-114">Click New.</span></span>
    * <span data-ttu-id="394c8-115">See loob uue kirje, mis vastendab andmemudeli andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="394c8-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="394c8-116">Selles näites vastendate andmemudeli andmeallikatega soovitud maksetüübi puhul: kreeditiülekanne.</span><span class="sxs-lookup"><span data-stu-id="394c8-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="394c8-117">Konkreetse andmemudeli puhul on võimalik kavandada rohkem kui ühe vastendamise.</span><span class="sxs-lookup"><span data-stu-id="394c8-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="394c8-118">Näiteks võite luua vastendamise eri maksetüüpide puhul, nagu otsekorraldus või kreeditiülekanded.</span><span class="sxs-lookup"><span data-stu-id="394c8-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="394c8-119">Selles näites loote vastendamise kreeditiülekannete puhul.</span><span class="sxs-lookup"><span data-stu-id="394c8-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="394c8-120">Sisestage väljale Nimi suvand Kreeditiülekande vastendamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="394c8-121">Kreeditiülekande vastendamine</span><span class="sxs-lookup"><span data-stu-id="394c8-121">CT mapping</span></span>  
6. <span data-ttu-id="394c8-122">Sisestage väljale Kirjeldus suvand Maksemudeli vastendamine (kreeditiülekanne).</span><span class="sxs-lookup"><span data-stu-id="394c8-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="394c8-123">Maksemudeli vastendamine (kreeditiülekanne)</span><span class="sxs-lookup"><span data-stu-id="394c8-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="394c8-124">Väljale Definitsioon tippige „CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="394c8-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="394c8-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="394c8-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="394c8-126">ResolveChanges definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="394c8-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="394c8-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="394c8-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="394c8-128">Praeguse mudeli vastendamise puhul nõutud andmeallikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="394c8-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="394c8-129">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="394c8-129">Click Designer.</span></span>
2. <span data-ttu-id="394c8-130">Valige puul suvand "Dynamics 365 for Operations\tabeli kirjed".</span><span class="sxs-lookup"><span data-stu-id="394c8-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="394c8-131">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-131">Click Add root.</span></span>
    * <span data-ttu-id="394c8-132">Sisestage maksekannete juurde pääsemiseks see andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="394c8-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="394c8-133">Sisestage väljale Nimi suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="394c8-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="394c8-134">Kanded</span><span class="sxs-lookup"><span data-stu-id="394c8-134">Transactions</span></span>  
5. <span data-ttu-id="394c8-135">Sisestage väljale Silt suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="394c8-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="394c8-136">Kanded</span><span class="sxs-lookup"><span data-stu-id="394c8-136">Transactions</span></span>  
6. <span data-ttu-id="394c8-137">Sisestage väljale Spikker suvand Pearaamatu töölehe read.</span><span class="sxs-lookup"><span data-stu-id="394c8-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="394c8-138">Pearaamatu töölehe read</span><span class="sxs-lookup"><span data-stu-id="394c8-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="394c8-139">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="394c8-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="394c8-140">Valige Jah.</span><span class="sxs-lookup"><span data-stu-id="394c8-140">Select Yes.</span></span>  
8. <span data-ttu-id="394c8-141">Sisestage väljale Tabel suvand LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="394c8-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="394c8-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="394c8-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="394c8-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="394c8-143">Click OK.</span></span>
    * <span data-ttu-id="394c8-144">Valige tabel LedgerJournalTrans praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="394c8-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="394c8-145">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="394c8-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="394c8-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="394c8-146">Click Add.</span></span>
    * <span data-ttu-id="394c8-147">Klõpsake uue arvutatud välja lisamiseks käsku Lisa.</span><span class="sxs-lookup"><span data-stu-id="394c8-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="394c8-148">Sisestage väljale Nimi suvand $EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="394c8-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="394c8-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="394c8-149">$EndToEndID</span></span>  
13. <span data-ttu-id="394c8-150">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="394c8-150">Click Edit formula.</span></span>
14. <span data-ttu-id="394c8-151">Valige puul suvand String\ÜHENDA.</span><span class="sxs-lookup"><span data-stu-id="394c8-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="394c8-152">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-152">Click Add function.</span></span>
16. <span data-ttu-id="394c8-153">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="394c8-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="394c8-154">Valige puul suvand Kanded\kanne.</span><span class="sxs-lookup"><span data-stu-id="394c8-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="394c8-155">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-155">Click Add data source.</span></span>
19. <span data-ttu-id="394c8-156">Väljale Valem sisestage „CONCATENATE(Transactions.Voucher, "-", ”.</span><span class="sxs-lookup"><span data-stu-id="394c8-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="394c8-157">Sisestage valemi lõppu [ , “-“, ].</span><span class="sxs-lookup"><span data-stu-id="394c8-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="394c8-158">Valige puul suvand String\TEKST.</span><span class="sxs-lookup"><span data-stu-id="394c8-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="394c8-159">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-159">Click Add function.</span></span>
22. <span data-ttu-id="394c8-160">Valige puul suvand Transactions\Record-ID(RecId).</span><span class="sxs-lookup"><span data-stu-id="394c8-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="394c8-161">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-161">Click Add data source.</span></span>
24. <span data-ttu-id="394c8-162">Väljale Valem sisestage „CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))”.</span><span class="sxs-lookup"><span data-stu-id="394c8-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="394c8-163">Sisestage valemi lõppu [))].</span><span class="sxs-lookup"><span data-stu-id="394c8-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="394c8-164">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="394c8-164">Click Save.</span></span>
    * <span data-ttu-id="394c8-165">Veenduge, et loodud valemis poleks tuvastatud tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="394c8-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="394c8-166">Vaadake valemi redaktori kontrolli all olevat vahekaarti TÕRKED.</span><span class="sxs-lookup"><span data-stu-id="394c8-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="394c8-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="394c8-167">Close the page.</span></span>
27. <span data-ttu-id="394c8-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="394c8-168">Click OK.</span></span>
    * <span data-ttu-id="394c8-169">Lisage arvutatud väli sellele andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="394c8-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="394c8-170">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="394c8-170">Click Add.</span></span>
    * <span data-ttu-id="394c8-171">Klõpsake uue arvutatud välja lisamiseks käsku Lisa.</span><span class="sxs-lookup"><span data-stu-id="394c8-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="394c8-172">Sisestage väljale Nimi suvand $Amount.</span><span class="sxs-lookup"><span data-stu-id="394c8-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="394c8-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="394c8-173">$Amount</span></span>  
30. <span data-ttu-id="394c8-174">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="394c8-174">Click Edit formula.</span></span>
31. <span data-ttu-id="394c8-175">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="394c8-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="394c8-176">Valige puul suvand Transactions\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="394c8-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="394c8-177">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-177">Click Add data source.</span></span>
34. <span data-ttu-id="394c8-178">Väljale Valem sisestage „Transactions.AmountCurDebit - ”.</span><span class="sxs-lookup"><span data-stu-id="394c8-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="394c8-179">Sisestage valemi lõppu [ - ].</span><span class="sxs-lookup"><span data-stu-id="394c8-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="394c8-180">Valige puul suvand Transactions\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="394c8-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="394c8-181">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-181">Click Add data source.</span></span>
37. <span data-ttu-id="394c8-182">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="394c8-182">Click Save.</span></span>
38. <span data-ttu-id="394c8-183">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="394c8-183">Close the page.</span></span>
39. <span data-ttu-id="394c8-184">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="394c8-184">Click OK.</span></span>
    * <span data-ttu-id="394c8-185">See lisab arvutatud välja $Amount praeguse andmemudeli puhul valitud andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="394c8-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="394c8-186">Valige puul suvand „Kanded\$Summa“.</span><span class="sxs-lookup"><span data-stu-id="394c8-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="394c8-187">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="394c8-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="394c8-188">Puuvaates laiendage või ahendage suvandit „Kanded\$Summa“.</span><span class="sxs-lookup"><span data-stu-id="394c8-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="394c8-189">Puuvaates laiendage või ahendage valikut „Kanded”.</span><span class="sxs-lookup"><span data-stu-id="394c8-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="394c8-190">Valige puul suvand "Dynamics 365 for Operations\tabeli kirjed".</span><span class="sxs-lookup"><span data-stu-id="394c8-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="394c8-191">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-191">Click Add root.</span></span>
    * <span data-ttu-id="394c8-192">Sisestage see andmeallikas ettevõtte pangakonto üksikasjade juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="394c8-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="394c8-193">Sisestage väljale Nimi suvand BankAccount.</span><span class="sxs-lookup"><span data-stu-id="394c8-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="394c8-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="394c8-194">BankAccount</span></span>  
47. <span data-ttu-id="394c8-195">Sisestage väljale Silt suvand Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="394c8-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="394c8-196">Pangakonto</span><span class="sxs-lookup"><span data-stu-id="394c8-196">Bank Account</span></span>  
48. <span data-ttu-id="394c8-197">Sisestage väljale Spikker suvand Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="394c8-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="394c8-198">Pangakonto</span><span class="sxs-lookup"><span data-stu-id="394c8-198">Bank Account</span></span>  
49. <span data-ttu-id="394c8-199">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="394c8-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="394c8-200">Valige Jah.</span><span class="sxs-lookup"><span data-stu-id="394c8-200">Select Yes.</span></span>  
50. <span data-ttu-id="394c8-201">Sisestage väljale Tabel suvand BankAccountTable.</span><span class="sxs-lookup"><span data-stu-id="394c8-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="394c8-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="394c8-202">BankAccountTable</span></span>  
51. <span data-ttu-id="394c8-203">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="394c8-203">Click OK.</span></span>
    * <span data-ttu-id="394c8-204">Valige tabel BankAccountTable praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="394c8-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="394c8-205">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-205">Click Add root.</span></span>
    * <span data-ttu-id="394c8-206">Sisestage see andmeallikas ettevõtte rekvisiitide juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="394c8-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="394c8-207">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="394c8-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="394c8-208">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="394c8-208">Company</span></span>  
54. <span data-ttu-id="394c8-209">Sisestage väärtus väljale Silt.</span><span class="sxs-lookup"><span data-stu-id="394c8-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="394c8-210">Ettevõtte andmed</span><span class="sxs-lookup"><span data-stu-id="394c8-210">Company information</span></span>  
55. <span data-ttu-id="394c8-211">Sisestage väljale Spikker suvand Ettevõtte andmed.</span><span class="sxs-lookup"><span data-stu-id="394c8-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="394c8-212">Ettevõtte andmed</span><span class="sxs-lookup"><span data-stu-id="394c8-212">Company information</span></span>  
56. <span data-ttu-id="394c8-213">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="394c8-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="394c8-214">Valige Jah.</span><span class="sxs-lookup"><span data-stu-id="394c8-214">Select Yes.</span></span>  
57. <span data-ttu-id="394c8-215">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="394c8-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="394c8-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="394c8-216">CompanyInfo</span></span>  
58. <span data-ttu-id="394c8-217">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="394c8-217">Click OK.</span></span>
    * <span data-ttu-id="394c8-218">Valige tabel CompanyInfo praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="394c8-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="394c8-219">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="394c8-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="394c8-220">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-220">Click Add root.</span></span>
    * <span data-ttu-id="394c8-221">Sisestage arvutatud väli uue andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="394c8-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="394c8-222">Sisestage väljale Nimi suvand ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="394c8-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="394c8-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="394c8-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="394c8-224">Sisestage väljale Silt suvand Töötlemise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="394c8-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="394c8-225">Töötlemise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="394c8-225">Processing date & time</span></span>  
63. <span data-ttu-id="394c8-226">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="394c8-226">Click Edit formula.</span></span>
64. <span data-ttu-id="394c8-227">Puuvaates valige „Kuupäev/kellaaeg\SESSIONNOW”.</span><span class="sxs-lookup"><span data-stu-id="394c8-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="394c8-228">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="394c8-228">Click Add function.</span></span>
66. <span data-ttu-id="394c8-229">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="394c8-229">Click Save.</span></span>
67. <span data-ttu-id="394c8-230">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="394c8-230">Close the page.</span></span>
68. <span data-ttu-id="394c8-231">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="394c8-231">Click OK.</span></span>
    * <span data-ttu-id="394c8-232">Lisage arvutatud väli ProcessingDateTime praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="394c8-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="394c8-233">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="394c8-233">Click Save.</span></span>
70. <span data-ttu-id="394c8-234">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="394c8-234">Close the page.</span></span>
71. <span data-ttu-id="394c8-235">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="394c8-235">Close the page.</span></span>
72. <span data-ttu-id="394c8-236">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="394c8-236">Close the page.</span></span>


