---
title: Elektroonilise aruandluse mudeli vastendamiste määratlemine ja andmeallikate valimine
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab valida andmeallikaid elektroonilise aruandluse andmemudeli jaoks.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a6287fa95b7ce7341e99d1b1a6b972db68a30398
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142160"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="b2b15-103">Elektroonilise aruandluse mudeli vastendamiste määratlemine ja andmeallikate valimine</span><span class="sxs-lookup"><span data-stu-id="b2b15-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2b15-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab valida andmeallikaid elektroonilise aruandluse (ER) andmemudeli jaoks.</span><span class="sxs-lookup"><span data-stu-id="b2b15-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="b2b15-105">Andmeallikad seotakse valitud andmemudeli üksikute komponentidega kujundamise ajal ja täidetakse selle andmemudeli äriandmetega töö ajal.</span><span class="sxs-lookup"><span data-stu-id="b2b15-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="b2b15-106">Selles näites valite andmeallikad olemasoleva andmemudeli jaoks, mis on loodud näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpule viimiseks peate kõigepealt läbima etapid protseduuris „Uue andmemudeli loomine”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="b2b15-107">Elektroonilise aruandluse konfiguratsioonipuu avamine</span><span class="sxs-lookup"><span data-stu-id="b2b15-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="b2b15-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="b2b15-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b2b15-109">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="b2b15-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="b2b15-110">Sisestage uue mudeli vastendamine</span><span class="sxs-lookup"><span data-stu-id="b2b15-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="b2b15-111">Valige puul suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="b2b15-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="b2b15-112">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="b2b15-112">Click Designer.</span></span>
3. <span data-ttu-id="b2b15-113">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="b2b15-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="b2b15-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b2b15-114">Click New.</span></span>
    * <span data-ttu-id="b2b15-115">See loob uue kirje, mis vastendab andmemudeli andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="b2b15-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="b2b15-116">Selles näites vastendate andmemudeli andmeallikatega soovitud maksetüübi puhul: kreeditiülekanne.</span><span class="sxs-lookup"><span data-stu-id="b2b15-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="b2b15-117">Konkreetse andmemudeli puhul on võimalik kavandada rohkem kui ühe vastendamise.</span><span class="sxs-lookup"><span data-stu-id="b2b15-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="b2b15-118">Näiteks võite luua vastendamise eri maksetüüpide puhul, nagu otsekorraldus või kreeditiülekanded.</span><span class="sxs-lookup"><span data-stu-id="b2b15-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="b2b15-119">Selles näites loote vastendamise kreeditiülekannete puhul.</span><span class="sxs-lookup"><span data-stu-id="b2b15-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="b2b15-120">Sisestage väljale Nimi suvand Kreeditiülekande vastendamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="b2b15-121">Kreeditiülekande vastendamine</span><span class="sxs-lookup"><span data-stu-id="b2b15-121">CT mapping</span></span>  
6. <span data-ttu-id="b2b15-122">Sisestage väljale Kirjeldus suvand Maksemudeli vastendamine (kreeditiülekanne).</span><span class="sxs-lookup"><span data-stu-id="b2b15-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="b2b15-123">Maksemudeli vastendamine (kreeditiülekanne)</span><span class="sxs-lookup"><span data-stu-id="b2b15-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="b2b15-124">Väljale Definitsioon tippige „CustomerCreditTransferInitiation”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="b2b15-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="b2b15-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="b2b15-126">ResolveChanges definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="b2b15-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="b2b15-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2b15-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="b2b15-128">Praeguse mudeli vastendamise puhul nõutud andmeallikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="b2b15-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="b2b15-129">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="b2b15-129">Click Designer.</span></span>
2. <span data-ttu-id="b2b15-130">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="b2b15-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="b2b15-131">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-131">Click Add root.</span></span>
    * <span data-ttu-id="b2b15-132">Sisestage maksekannete juurde pääsemiseks see andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="b2b15-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="b2b15-133">Sisestage väljale Nimi suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="b2b15-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="b2b15-134">Kanded</span><span class="sxs-lookup"><span data-stu-id="b2b15-134">Transactions</span></span>  
5. <span data-ttu-id="b2b15-135">Sisestage väljale Silt suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="b2b15-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="b2b15-136">Kanded</span><span class="sxs-lookup"><span data-stu-id="b2b15-136">Transactions</span></span>  
6. <span data-ttu-id="b2b15-137">Sisestage väljale Spikker suvand Pearaamatu töölehe read.</span><span class="sxs-lookup"><span data-stu-id="b2b15-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="b2b15-138">Pearaamatu töölehe read</span><span class="sxs-lookup"><span data-stu-id="b2b15-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="b2b15-139">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="b2b15-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b2b15-140">Valige Jah.</span><span class="sxs-lookup"><span data-stu-id="b2b15-140">Select Yes.</span></span>  
8. <span data-ttu-id="b2b15-141">Sisestage väljale Tabel suvand LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="b2b15-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="b2b15-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="b2b15-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="b2b15-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2b15-143">Click OK.</span></span>
    * <span data-ttu-id="b2b15-144">Valige tabel LedgerJournalTrans praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="b2b15-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="b2b15-145">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="b2b15-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="b2b15-146">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b2b15-146">Click Add.</span></span>
    * <span data-ttu-id="b2b15-147">Klõpsake uue arvutatud välja lisamiseks käsku Lisa.</span><span class="sxs-lookup"><span data-stu-id="b2b15-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="b2b15-148">Sisestage väljale Nimi suvand $EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="b2b15-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="b2b15-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="b2b15-149">$EndToEndID</span></span>  
13. <span data-ttu-id="b2b15-150">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="b2b15-150">Click Edit formula.</span></span>
14. <span data-ttu-id="b2b15-151">Valige puul suvand String\ÜHENDA.</span><span class="sxs-lookup"><span data-stu-id="b2b15-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="b2b15-152">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-152">Click Add function.</span></span>
16. <span data-ttu-id="b2b15-153">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="b2b15-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="b2b15-154">Valige puul suvand Kanded\kanne.</span><span class="sxs-lookup"><span data-stu-id="b2b15-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="b2b15-155">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-155">Click Add data source.</span></span>
19. <span data-ttu-id="b2b15-156">Väljale Valem sisestage „CONCATENATE(Transactions.Voucher, "-", ”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="b2b15-157">Sisestage valemi lõppu [ , "-", ].</span><span class="sxs-lookup"><span data-stu-id="b2b15-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="b2b15-158">Valige puul suvand String\TEKST.</span><span class="sxs-lookup"><span data-stu-id="b2b15-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="b2b15-159">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-159">Click Add function.</span></span>
22. <span data-ttu-id="b2b15-160">Valige puul suvand Transactions\Record-ID(RecId).</span><span class="sxs-lookup"><span data-stu-id="b2b15-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="b2b15-161">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-161">Click Add data source.</span></span>
24. <span data-ttu-id="b2b15-162">Väljale Valem sisestage „CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="b2b15-163">Sisestage valemi lõppu [))].</span><span class="sxs-lookup"><span data-stu-id="b2b15-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="b2b15-164">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2b15-164">Click Save.</span></span>
    * <span data-ttu-id="b2b15-165">Veenduge, et loodud valemis poleks tuvastatud tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="b2b15-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="b2b15-166">Vaadake valemi redaktori kontrolli all olevat vahekaarti TÕRKED.</span><span class="sxs-lookup"><span data-stu-id="b2b15-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="b2b15-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2b15-167">Close the page.</span></span>
27. <span data-ttu-id="b2b15-168">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2b15-168">Click OK.</span></span>
    * <span data-ttu-id="b2b15-169">Lisage arvutatud väli sellele andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="b2b15-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="b2b15-170">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b2b15-170">Click Add.</span></span>
    * <span data-ttu-id="b2b15-171">Klõpsake uue arvutatud välja lisamiseks käsku Lisa.</span><span class="sxs-lookup"><span data-stu-id="b2b15-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="b2b15-172">Sisestage väljale Nimi suvand $Amount.</span><span class="sxs-lookup"><span data-stu-id="b2b15-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="b2b15-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="b2b15-173">$Amount</span></span>  
30. <span data-ttu-id="b2b15-174">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="b2b15-174">Click Edit formula.</span></span>
31. <span data-ttu-id="b2b15-175">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="b2b15-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="b2b15-176">Valige puul suvand Transactions\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="b2b15-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="b2b15-177">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-177">Click Add data source.</span></span>
34. <span data-ttu-id="b2b15-178">Väljale Valem sisestage „Transactions.AmountCurDebit - ”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="b2b15-179">Sisestage valemi lõppu [ - ].</span><span class="sxs-lookup"><span data-stu-id="b2b15-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="b2b15-180">Valige puul suvand Transactions\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="b2b15-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="b2b15-181">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-181">Click Add data source.</span></span>
37. <span data-ttu-id="b2b15-182">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2b15-182">Click Save.</span></span>
38. <span data-ttu-id="b2b15-183">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2b15-183">Close the page.</span></span>
39. <span data-ttu-id="b2b15-184">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2b15-184">Click OK.</span></span>
    * <span data-ttu-id="b2b15-185">See lisab arvutatud välja $Amount praeguse andmemudeli puhul valitud andmeallikale.</span><span class="sxs-lookup"><span data-stu-id="b2b15-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="b2b15-186">Valige puul suvand „Kanded\$Summa“.</span><span class="sxs-lookup"><span data-stu-id="b2b15-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="b2b15-187">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="b2b15-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="b2b15-188">Puuvaates laiendage või ahendage suvandit „Kanded\$Summa“.</span><span class="sxs-lookup"><span data-stu-id="b2b15-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="b2b15-189">Puuvaates laiendage või ahendage valikut „Kanded”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="b2b15-190">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="b2b15-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="b2b15-191">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-191">Click Add root.</span></span>
    * <span data-ttu-id="b2b15-192">Sisestage see andmeallikas ettevõtte pangakonto üksikasjade juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="b2b15-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="b2b15-193">Sisestage väljale Nimi suvand BankAccount.</span><span class="sxs-lookup"><span data-stu-id="b2b15-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="b2b15-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="b2b15-194">BankAccount</span></span>  
47. <span data-ttu-id="b2b15-195">Sisestage väljale Silt suvand Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="b2b15-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b2b15-196">Pangakonto</span><span class="sxs-lookup"><span data-stu-id="b2b15-196">Bank Account</span></span>  
48. <span data-ttu-id="b2b15-197">Sisestage väljale Spikker suvand Pangakonto.</span><span class="sxs-lookup"><span data-stu-id="b2b15-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="b2b15-198">Pangakonto</span><span class="sxs-lookup"><span data-stu-id="b2b15-198">Bank Account</span></span>  
49. <span data-ttu-id="b2b15-199">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="b2b15-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b2b15-200">Valige Jah.</span><span class="sxs-lookup"><span data-stu-id="b2b15-200">Select Yes.</span></span>  
50. <span data-ttu-id="b2b15-201">Sisestage väljale Tabel suvand BankAccountTable.</span><span class="sxs-lookup"><span data-stu-id="b2b15-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="b2b15-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="b2b15-202">BankAccountTable</span></span>  
51. <span data-ttu-id="b2b15-203">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2b15-203">Click OK.</span></span>
    * <span data-ttu-id="b2b15-204">Valige tabel BankAccountTable praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="b2b15-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="b2b15-205">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-205">Click Add root.</span></span>
    * <span data-ttu-id="b2b15-206">Sisestage see andmeallikas ettevõtte rekvisiitide juurde pääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="b2b15-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="b2b15-207">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="b2b15-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="b2b15-208">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="b2b15-208">Company</span></span>  
54. <span data-ttu-id="b2b15-209">Sisestage väärtus väljale Silt.</span><span class="sxs-lookup"><span data-stu-id="b2b15-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="b2b15-210">Ettevõtte andmed</span><span class="sxs-lookup"><span data-stu-id="b2b15-210">Company information</span></span>  
55. <span data-ttu-id="b2b15-211">Sisestage väljale Spikker suvand Ettevõtte andmed.</span><span class="sxs-lookup"><span data-stu-id="b2b15-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="b2b15-212">Ettevõtte andmed</span><span class="sxs-lookup"><span data-stu-id="b2b15-212">Company information</span></span>  
56. <span data-ttu-id="b2b15-213">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="b2b15-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="b2b15-214">Valige Jah.</span><span class="sxs-lookup"><span data-stu-id="b2b15-214">Select Yes.</span></span>  
57. <span data-ttu-id="b2b15-215">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="b2b15-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="b2b15-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="b2b15-216">CompanyInfo</span></span>  
58. <span data-ttu-id="b2b15-217">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2b15-217">Click OK.</span></span>
    * <span data-ttu-id="b2b15-218">Valige tabel CompanyInfo praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="b2b15-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="b2b15-219">Valige puul suvand Funktsioonid\arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="b2b15-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="b2b15-220">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-220">Click Add root.</span></span>
    * <span data-ttu-id="b2b15-221">Sisestage arvutatud väli uue andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="b2b15-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="b2b15-222">Sisestage väljale Nimi suvand ProcessingDateTime.</span><span class="sxs-lookup"><span data-stu-id="b2b15-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="b2b15-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="b2b15-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="b2b15-224">Sisestage väljale Silt suvand Töötlemise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="b2b15-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="b2b15-225">Töötlemise kuupäev ja kellaaeg</span><span class="sxs-lookup"><span data-stu-id="b2b15-225">Processing date & time</span></span>  
63. <span data-ttu-id="b2b15-226">Klõpsake suvandit Muuda valemit.</span><span class="sxs-lookup"><span data-stu-id="b2b15-226">Click Edit formula.</span></span>
64. <span data-ttu-id="b2b15-227">Puuvaates valige „Kuupäev/kellaaeg\SESSIONNOW”.</span><span class="sxs-lookup"><span data-stu-id="b2b15-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="b2b15-228">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="b2b15-228">Click Add function.</span></span>
66. <span data-ttu-id="b2b15-229">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2b15-229">Click Save.</span></span>
67. <span data-ttu-id="b2b15-230">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2b15-230">Close the page.</span></span>
68. <span data-ttu-id="b2b15-231">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b2b15-231">Click OK.</span></span>
    * <span data-ttu-id="b2b15-232">Lisage arvutatud väli ProcessingDateTime praeguse andmemudeli andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="b2b15-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="b2b15-233">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b2b15-233">Click Save.</span></span>
70. <span data-ttu-id="b2b15-234">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2b15-234">Close the page.</span></span>
71. <span data-ttu-id="b2b15-235">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2b15-235">Close the page.</span></span>
72. <span data-ttu-id="b2b15-236">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2b15-236">Close the page.</span></span>

