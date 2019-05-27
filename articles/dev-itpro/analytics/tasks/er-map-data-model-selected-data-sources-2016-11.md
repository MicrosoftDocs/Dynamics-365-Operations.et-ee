---
title: Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatele
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis kasutaja saab elektroonilise aruandluse (ER) andmemudeli vastendada valitud rakenduse Dynamics 365 for Finance and Operations, Enterprise edition andmeallikatega.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551226"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="4ca2e-103">Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatele</span><span class="sxs-lookup"><span data-stu-id="4ca2e-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4ca2e-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rollis kasutaja saab elektroonilise aruandluse (ER) andmemudeli vastendada valitud rakenduse Dynamics 365 for Finance and Operations, Enterprise edition andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="4ca2e-105">Seda mudeli vastendamist kasutatakse hiljem andmeallikana vormingu konfiguratsioonis, mida kasutatakse elektrooniliste maksedokumentide haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="4ca2e-106">Selles näites vastendate näidisettevõtte Litware, Inc andmemudelit andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="4ca2e-107">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Andmeallikate valimine mudeli vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="4ca2e-108">Avatud elektroonilise aruandluse konfiguratsioonide puu</span><span class="sxs-lookup"><span data-stu-id="4ca2e-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="4ca2e-109">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="4ca2e-110">Klõpsake suvandit Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="4ca2e-111">Loodud mudeli vastendamise valimine</span><span class="sxs-lookup"><span data-stu-id="4ca2e-111">Select created model mapping</span></span>
1. <span data-ttu-id="4ca2e-112">Valige puul suvand Maksed (lihtsustatud mudel).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="4ca2e-113">Veenduge, et mudeli konfiguratsioon Maksed (lihtsustatud mudel) oleks eelnevalt loodud.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="4ca2e-114">Vastasel juhul lõpetage kohe ja naaske pärast tegevusejuhise „Uue konfiguratsiooni loomine valitud domeeni andmemudeliga” lõpuleviimist.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="4ca2e-115">Klõpsake suvandit Mudeli koostaja.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-115">Click Model designer.</span></span>
3. <span data-ttu-id="4ca2e-116">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="4ca2e-117">Valige kirje Kreeditiülekande vastendamine.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="4ca2e-118">Kreeditiülekande vastendamine</span><span class="sxs-lookup"><span data-stu-id="4ca2e-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="4ca2e-119">Loodud andmeallikate sidumine andmemudeli elementidega</span><span class="sxs-lookup"><span data-stu-id="4ca2e-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="4ca2e-120">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-120">Click Designer.</span></span>
2. <span data-ttu-id="4ca2e-121">Valige puul suvand Töötluse kuupäev ja kellaaeg (ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="4ca2e-122">Valige puul suvand Processing date(ProcessingDateTime).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="4ca2e-123">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-123">Click Bind.</span></span>
5. <span data-ttu-id="4ca2e-124">Valige puul suvand Payment message identification(MessageIdentification).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="4ca2e-125">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="4ca2e-126">Valige puul suvand Transactions\Journal batch number(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="4ca2e-127">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-127">Click Bind.</span></span>
9. <span data-ttu-id="4ca2e-128">Valige puul suvand Maksed.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="4ca2e-129">Valige puul suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="4ca2e-130">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-130">Click Bind.</span></span>
12. <span data-ttu-id="4ca2e-131">Laiendage puus sõlme Payments= Transactions.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="4ca2e-132">Laiendage puus sõlme Payments= Transactions\Creditor.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="4ca2e-133">Laiendage puus sõlme Payments= Transactions\Creditor\Account.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="4ca2e-134">Valige puul suvand Payments= Transactions\Creditor\Account\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="4ca2e-135">Laiendage puus sõlme Transactions\vendBankAccountInTransactionCompany().</span><span class="sxs-lookup"><span data-stu-id="4ca2e-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="4ca2e-136">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="4ca2e-137">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-137">Click Bind.</span></span>
19. <span data-ttu-id="4ca2e-138">Valige puul suvand Payments= Transactions\Creditor\Account\IBAN code(IBAN).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="4ca2e-139">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="4ca2e-140">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-140">Click Bind.</span></span>
22. <span data-ttu-id="4ca2e-141">Valige puul suvand Payments= Transactions\Creditor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="4ca2e-142">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="4ca2e-143">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-143">Click Bind.</span></span>
25. <span data-ttu-id="4ca2e-144">Laiendage puus sõlme Payments= Transactions\Creditor\Agent.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="4ca2e-145">Valige puul suvand Payments= Transactions\Creditor\Agent\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="4ca2e-146">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="4ca2e-147">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-147">Click Bind.</span></span>
29. <span data-ttu-id="4ca2e-148">Valige puul suvand Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="4ca2e-149">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="4ca2e-150">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-150">Click Bind.</span></span>
32. <span data-ttu-id="4ca2e-151">Valige puul suvand Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="4ca2e-152">Valige puul suvand Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="4ca2e-153">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-153">Click Bind.</span></span>
35. <span data-ttu-id="4ca2e-154">Valige puul suvand Payments= Transactions\Creditor\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="4ca2e-155">Laiendage puus sõlme Transactions\findVendTable().</span><span class="sxs-lookup"><span data-stu-id="4ca2e-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="4ca2e-156">Valige puult 'Transactions\findVendTable()\name()'.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="4ca2e-157">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-157">Click Bind.</span></span>
39. <span data-ttu-id="4ca2e-158">Valige puul suvand Payments= Transactions\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="4ca2e-159">Laiendage puus valikut „Transactions\>Relations“.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="4ca2e-160">Laiendage puus sõlme „Transactions\>Relations\Currency table(Currency)“.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="4ca2e-161">Valige puul suvand „Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)“.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="4ca2e-162">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-162">Click Bind.</span></span>
44. <span data-ttu-id="4ca2e-163">Laiendage puus sõlme Payments= Transactions\Debtor.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="4ca2e-164">Laiendage puus sõlme Payments= Transactions\Debtor\Account.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="4ca2e-165">Valige puul suvand Payments= Transactions\Debtor\Account\Currency code(Currency).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="4ca2e-166">Valige puul suvand Bank Account(BankAccount).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="4ca2e-167">Laiendage puus sõlme Bank Account(BankAccount).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="4ca2e-168">Valige puul suvand Bank Account(BankAccount)\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="4ca2e-169">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-169">Click Bind.</span></span>
51. <span data-ttu-id="4ca2e-170">Valige puul suvand Bank Account(BankAccount)\IBAN.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="4ca2e-171">Valige puul suvand Payments= Transactions\Debtor\Account\IBAN code(IBAN).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="4ca2e-172">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-172">Click Bind.</span></span>
54. <span data-ttu-id="4ca2e-173">Valige puul suvand Payments= Transactions\Debtor\Account\Number.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="4ca2e-174">Valige puul suvand Bank Account(BankAccount)\Bank account number(AccountNum).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="4ca2e-175">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-175">Click Bind.</span></span>
57. <span data-ttu-id="4ca2e-176">Laiendage puus sõlme Payments= Transactions\Debtor\Agent.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="4ca2e-177">Valige puul suvand Payments= Transactions\Debtor\Agent\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="4ca2e-178">Valige puul suvand Bank Account(BankAccount)\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="4ca2e-179">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-179">Click Bind.</span></span>
61. <span data-ttu-id="4ca2e-180">Valige puul suvand Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="4ca2e-181">Valige puul suvand Bank Account(BankAccount)\Routing number(RegistrationNum).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="4ca2e-182">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-182">Click Bind.</span></span>
64. <span data-ttu-id="4ca2e-183">Valige puul suvand Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="4ca2e-184">Valige puul suvand Bank Account(BankAccount)\SWIFT code(SWIFTNo).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="4ca2e-185">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-185">Click Bind.</span></span>
67. <span data-ttu-id="4ca2e-186">Valige puul suvand Payments= Transactions\Debtor\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="4ca2e-187">Valige puul suvand Company information(Company).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="4ca2e-188">Laiendage puus sõlme Company information(Company).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="4ca2e-189">Valige puul suvand Company information(Company)\Name.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="4ca2e-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-190">Click Bind.</span></span>
72. <span data-ttu-id="4ca2e-191">Valige puul suvand Payments= Transactions\Description.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="4ca2e-192">Valige puul suvand Transactions\Description(Txt).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="4ca2e-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-193">Click Bind.</span></span>
75. <span data-ttu-id="4ca2e-194">Valige puul suvand Payments= Transactions\End to end identification code(End2EndID).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="4ca2e-195">Valige puul suvand „Transactions\$EndToEndID“.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="4ca2e-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-196">Click Bind.</span></span>
78. <span data-ttu-id="4ca2e-197">Valige puul suvand Payments= Transactions\Instructed amount(InstructedAmount).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="4ca2e-198">Valige puul suvand „Kanded\$Summa“.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="4ca2e-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-199">Click Bind.</span></span>
81. <span data-ttu-id="4ca2e-200">Valige puul suvand Payments= Transactions\Transaction date(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="4ca2e-201">Valige puul suvand Transactions\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="4ca2e-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="4ca2e-202">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="4ca2e-203">Loodud vastendamise kinnitamine</span><span class="sxs-lookup"><span data-stu-id="4ca2e-203">Validate created mapping</span></span>
1. <span data-ttu-id="4ca2e-204">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-204">Click Validate.</span></span>
    * <span data-ttu-id="4ca2e-205">Kinnitage uus vastendus tagamaks, et kõikide sidumistega on korras.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="4ca2e-206">Klõpsake noolt jaotise Vigade loend laiendamiseks või ahendamiseks.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="4ca2e-207">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-207">Click Save.</span></span>
4. <span data-ttu-id="4ca2e-208">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-208">Close the page.</span></span>
5. <span data-ttu-id="4ca2e-209">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-209">Close the page.</span></span>
6. <span data-ttu-id="4ca2e-210">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="4ca2e-211">Mudeli konfiguratsiooni praeguse versiooni oleku muutmine</span><span class="sxs-lookup"><span data-stu-id="4ca2e-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="4ca2e-212">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-212">Click Change status.</span></span>
    * <span data-ttu-id="4ca2e-213">Muutke kujundatud mudeli konfiguratsiooni olekut suvandilt Mustand suvandile Lõpule viidud, et muuta see kättesaadavaks maksevormingu kujundamiseks.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="4ca2e-214">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-214">Click Complete.</span></span>
    * <span data-ttu-id="4ca2e-215">Valige Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-215">Select Complete.</span></span>  
3. <span data-ttu-id="4ca2e-216">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4ca2e-217">Näiteks „versioon 1”.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="4ca2e-218">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-218">Click OK.</span></span>
5. <span data-ttu-id="4ca2e-219">Valige praeguse konfiguratsiooni lõpetatud versioon.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="4ca2e-220">Pange tähele, et loodud konfiguratsioon salvestatakse kui lõpetatud versioon 1.</span><span class="sxs-lookup"><span data-stu-id="4ca2e-220">Note that the created configuration is saved as completed version 1.</span></span>  

