--- 
title: Elektroonilise aruandluse (ER) andmemudeli vastendamine valitud andmeallikatega
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis kasutaja saab elektroonilise aruandluse (ER) andmemudeli vastendada valitud rakenduse Dynamics 365 for Finance and Operations, Enterprise edition andmeallikatega."
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
ms.openlocfilehash: 96974d7c1597db4ac31168be40cecbc7e12d6edd
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="febc0-103">Elektroonilise aruandluse (ER) andmemudeli vastendamine valitud andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="febc0-103">Map a data model to selected data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="febc0-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis kasutaja saab elektroonilise aruandluse (ER) andmemudeli vastendada valitud rakenduse Dynamics 365 for Finance and Operations, Enterprise edition andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="febc0-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="febc0-105">Seda mudeli vastendamist kasutatakse hiljem andmeallikana vormingu konfiguratsioonis, mida kasutatakse elektrooniliste maksedokumentide haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="febc0-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="febc0-106">Selles näites vastendate näidisettevõtte Litware, Inc andmemudelit andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="febc0-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="febc0-107">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Andmeallikate valimine mudeli vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="febc0-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="febc0-108">Avatud elektroonilise aruandluse konfiguratsioonide puu</span><span class="sxs-lookup"><span data-stu-id="febc0-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="febc0-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="febc0-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="febc0-110">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="febc0-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="febc0-111">Loodud mudeli vastendamise valimine</span><span class="sxs-lookup"><span data-stu-id="febc0-111">Select created model mapping</span></span>
1. <span data-ttu-id="febc0-112">Valige puul suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="febc0-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="febc0-113">Veenduge, et mudeli konfiguratsioon Maksed (lihtsustatud mudel) oleks eelnevalt loodud.</span><span class="sxs-lookup"><span data-stu-id="febc0-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="febc0-114">Vastasel juhul lõpetage kohe ja naaske pärast tegevusejuhise „Uue konfiguratsiooni loomine valitud domeeni andmemudeliga” lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="febc0-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="febc0-115">Klõpsake suvandit Mudeli koostaja.</span><span class="sxs-lookup"><span data-stu-id="febc0-115">Click Model designer.</span></span>
3. <span data-ttu-id="febc0-116">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="febc0-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="febc0-117">Valige kirje Kreeditiülekande vastendamine.</span><span class="sxs-lookup"><span data-stu-id="febc0-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="febc0-118">Kreeditiülekande vastendamine</span><span class="sxs-lookup"><span data-stu-id="febc0-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="febc0-119">Loodud andmeallikate sidumine andmemudeli elementidega</span><span class="sxs-lookup"><span data-stu-id="febc0-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="febc0-120">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="febc0-120">Click Designer.</span></span>
2. <span data-ttu-id="febc0-121">Valige puul suvand Töötluse kuupäev ja kellaaeg (ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="febc0-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="febc0-122">Valige puul suvand Processing date(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="febc0-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="febc0-123">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-123">Click Bind.</span></span>
5. <span data-ttu-id="febc0-124">Valige puul suvand Payment message identification(MessageIdentification).</span><span class="sxs-lookup"><span data-stu-id="febc0-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="febc0-125">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="febc0-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="febc0-126">Valige puul suvand Transactions\Journal batch number(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="febc0-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="febc0-127">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-127">Click Bind.</span></span>
9. <span data-ttu-id="febc0-128">Valige puul suvand Maksed.</span><span class="sxs-lookup"><span data-stu-id="febc0-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="febc0-129">Valige puul suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="febc0-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="febc0-130">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-130">Click Bind.</span></span>
12. <span data-ttu-id="febc0-131">Laiendage puus sõlme Payments= Transactions.</span><span class="sxs-lookup"><span data-stu-id="febc0-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="febc0-132">Laiendage puus sõlme Payments= Transactions\Creditor.</span><span class="sxs-lookup"><span data-stu-id="febc0-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="febc0-133">Laiendage puus sõlme Payments= Transactions\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="febc0-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="febc0-134">Valige puul suvand Payments= Transactions\Creditor\Account\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="febc0-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="febc0-135">Laiendage puus sõlme Transactions\vendBankAccountInTransactionCompany().</span><span class="sxs-lookup"><span data-stu-id="febc0-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="febc0-136">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="febc0-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="febc0-137">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-137">Click Bind.</span></span>
19. <span data-ttu-id="febc0-138">Valige puul suvand Payments= Transactions\Creditor\Account\IBAN code(IBAN).</span><span class="sxs-lookup"><span data-stu-id="febc0-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="febc0-139">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).</span><span class="sxs-lookup"><span data-stu-id="febc0-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="febc0-140">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-140">Click Bind.</span></span>
22. <span data-ttu-id="febc0-141">Valige puul suvand Payments= Transactions\Creditor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="febc0-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="febc0-142">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="febc0-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="febc0-143">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-143">Click Bind.</span></span>
25. <span data-ttu-id="febc0-144">Laiendage puus sõlme Payments= Transactions\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="febc0-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="febc0-145">Valige puul suvand Payments= Transactions\Creditor\Agent\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="febc0-146">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="febc0-147">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-147">Click Bind.</span></span>
29. <span data-ttu-id="febc0-148">Valige puul suvand Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="febc0-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="febc0-149">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="febc0-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="febc0-150">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-150">Click Bind.</span></span>
32. <span data-ttu-id="febc0-151">Valige puul suvand Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="febc0-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="febc0-152">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="febc0-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="febc0-153">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-153">Click Bind.</span></span>
35. <span data-ttu-id="febc0-154">Valige puul suvand Payments= Transactions\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="febc0-155">Laiendage puus sõlme Transactions\findVendTable().</span><span class="sxs-lookup"><span data-stu-id="febc0-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="febc0-156">Valige puult 'Transactions\findVendTable()\name()'.</span><span class="sxs-lookup"><span data-stu-id="febc0-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="febc0-157">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-157">Click Bind.</span></span>
39. <span data-ttu-id="febc0-158">Valige puul suvand Payments= Transactions\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="febc0-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="febc0-159">Laiendage puus valikut „Transactions\>Relations“.</span><span class="sxs-lookup"><span data-stu-id="febc0-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="febc0-160">Laiendage puus sõlme „Transactions\>Relations\Currency table(Currency)“.</span><span class="sxs-lookup"><span data-stu-id="febc0-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="febc0-161">Valige puul suvand „Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)“.</span><span class="sxs-lookup"><span data-stu-id="febc0-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="febc0-162">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-162">Click Bind.</span></span>
44. <span data-ttu-id="febc0-163">Laiendage puus sõlme Payments= Transactions\Debtor.</span><span class="sxs-lookup"><span data-stu-id="febc0-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="febc0-164">Laiendage puus sõlme Payments= Transactions\Debtor\Account.</span><span class="sxs-lookup"><span data-stu-id="febc0-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="febc0-165">Valige puul suvand Payments= Transactions\Debtor\Account\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="febc0-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="febc0-166">Valige puul suvand Bank Account(BankAccount).</span><span class="sxs-lookup"><span data-stu-id="febc0-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="febc0-167">Laiendage puus sõlme Bank Account(BankAccount).</span><span class="sxs-lookup"><span data-stu-id="febc0-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="febc0-168">Valige puul suvand Bank Account(BankAccount)\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="febc0-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="febc0-169">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-169">Click Bind.</span></span>
51. <span data-ttu-id="febc0-170">Valige puul suvand Bank Account(BankAccount)\IBAN.</span><span class="sxs-lookup"><span data-stu-id="febc0-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="febc0-171">Valige puul suvand Payments= Transactions\Debtor\Account\IBAN code(IBAN).</span><span class="sxs-lookup"><span data-stu-id="febc0-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="febc0-172">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-172">Click Bind.</span></span>
54. <span data-ttu-id="febc0-173">Valige puul suvand Payments= Transactions\Debtor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="febc0-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="febc0-174">Valige puul suvand Bank Account(BankAccount)\Bank account number(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="febc0-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="febc0-175">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-175">Click Bind.</span></span>
57. <span data-ttu-id="febc0-176">Laiendage puus sõlme Payments= Transactions\Debtor\Agent.</span><span class="sxs-lookup"><span data-stu-id="febc0-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="febc0-177">Valige puul suvand Payments= Transactions\Debtor\Agent\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="febc0-178">Valige puul suvand Bank Account(BankAccount)\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="febc0-179">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-179">Click Bind.</span></span>
61. <span data-ttu-id="febc0-180">Valige puul suvand Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="febc0-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="febc0-181">Valige puul suvand Bank Account(BankAccount)\Routing number(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="febc0-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="febc0-182">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-182">Click Bind.</span></span>
64. <span data-ttu-id="febc0-183">Valige puul suvand Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="febc0-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="febc0-184">Valige puul suvand Bank Account(BankAccount)\SWIFT code(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="febc0-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="febc0-185">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-185">Click Bind.</span></span>
67. <span data-ttu-id="febc0-186">Valige puul suvand Payments= Transactions\Debtor\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="febc0-187">Valige puul suvand Company information(Company).</span><span class="sxs-lookup"><span data-stu-id="febc0-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="febc0-188">Laiendage puus sõlme Company information(Company).</span><span class="sxs-lookup"><span data-stu-id="febc0-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="febc0-189">Valige puul suvand Company information(Company)\Name.</span><span class="sxs-lookup"><span data-stu-id="febc0-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="febc0-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-190">Click Bind.</span></span>
72. <span data-ttu-id="febc0-191">Valige puul suvand Payments= Transactions\Description.</span><span class="sxs-lookup"><span data-stu-id="febc0-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="febc0-192">Valige puul suvand Transactions\Description(Txt).</span><span class="sxs-lookup"><span data-stu-id="febc0-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="febc0-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-193">Click Bind.</span></span>
75. <span data-ttu-id="febc0-194">Valige puul suvand Payments= Transactions\End to end identification code(End2EndID).</span><span class="sxs-lookup"><span data-stu-id="febc0-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="febc0-195">Valige puul suvand „Transactions\$EndToEndID“.</span><span class="sxs-lookup"><span data-stu-id="febc0-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="febc0-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-196">Click Bind.</span></span>
78. <span data-ttu-id="febc0-197">Valige puul suvand Payments= Transactions\Instructed amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="febc0-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="febc0-198">Valige puul suvand „Kanded\$Summa“.</span><span class="sxs-lookup"><span data-stu-id="febc0-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="febc0-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-199">Click Bind.</span></span>
81. <span data-ttu-id="febc0-200">Valige puul suvand Payments= Transactions\Transaction date(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="febc0-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="febc0-201">Valige puul suvand Transactions\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="febc0-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="febc0-202">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="febc0-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="febc0-203">Loodud vastendamise kinnitamine</span><span class="sxs-lookup"><span data-stu-id="febc0-203">Validate created mapping</span></span>
1. <span data-ttu-id="febc0-204">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="febc0-204">Click Validate.</span></span>
    * <span data-ttu-id="febc0-205">Kinnitage uus vastendus tagamaks, et kõikide sidumistega on korras.</span><span class="sxs-lookup"><span data-stu-id="febc0-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="febc0-206">Klõpsake noolt jaotise Vigade loend laiendamiseks või ahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="febc0-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="febc0-207">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="febc0-207">Click Save.</span></span>
4. <span data-ttu-id="febc0-208">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="febc0-208">Close the page.</span></span>
5. <span data-ttu-id="febc0-209">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="febc0-209">Close the page.</span></span>
6. <span data-ttu-id="febc0-210">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="febc0-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="febc0-211">Mudeli konfiguratsiooni praeguse versiooni oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="febc0-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="febc0-212">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="febc0-212">Click Change status.</span></span>
    * <span data-ttu-id="febc0-213">Muutke kujundatud mudeli konfiguratsiooni olekut suvandilt Mustand suvandile Lõpule viidud, et muuta see kättesaadavaks maksevormingu kujundamiseks.</span><span class="sxs-lookup"><span data-stu-id="febc0-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="febc0-214">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="febc0-214">Click Complete.</span></span>
    * <span data-ttu-id="febc0-215">Valige Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="febc0-215">Select Complete.</span></span>  
3. <span data-ttu-id="febc0-216">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="febc0-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="febc0-217">Näiteks „versioon 1”.</span><span class="sxs-lookup"><span data-stu-id="febc0-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="febc0-218">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="febc0-218">Click OK.</span></span>
5. <span data-ttu-id="febc0-219">Valige praeguse konfiguratsiooni lõpetatud versioon.</span><span class="sxs-lookup"><span data-stu-id="febc0-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="febc0-220">Pange tähele, et loodud konfiguratsioon salvestatakse kui lõpetatud versioon 1.</span><span class="sxs-lookup"><span data-stu-id="febc0-220">Note that the created configuration is saved as completed version 1.</span></span>  


