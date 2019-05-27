---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (2. osa – mudeli vastendamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92efd6a0b36471286c292a80542b81cd14a8eff3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551341"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a><span data-ttu-id="86910-103">Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine)</span><span class="sxs-lookup"><span data-stu-id="86910-103">ER Use financial dimensions as a data source (Part 2: Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86910-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="86910-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="86910-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="86910-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="86910-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine).</span><span class="sxs-lookup"><span data-stu-id="86910-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="86910-107">Vajalike andmeallikate lisamine mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="86910-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="86910-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="86910-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="86910-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="86910-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="86910-110">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="86910-110">Click Designer.</span></span>
4. <span data-ttu-id="86910-111">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="86910-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="86910-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="86910-112">Click New.</span></span>
6. <span data-ttu-id="86910-113">Tehke väljal Definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="86910-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="86910-114">Tippige Dimensioonide andmete vastendamine väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="86910-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="86910-115">Tippige Dimensioonide andmete vastendamine väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="86910-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="86910-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="86910-116">Click Save.</span></span>
10. <span data-ttu-id="86910-117">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="86910-117">Click Designer.</span></span>
11. <span data-ttu-id="86910-118">Valige puul väärtus Dynamics 365 for Operations \ Tabel.</span><span class="sxs-lookup"><span data-stu-id="86910-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="86910-119">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="86910-119">Click Add root.</span></span>
13. <span data-ttu-id="86910-120">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="86910-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="86910-121">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="86910-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="86910-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="86910-122">Click OK.</span></span>
16. <span data-ttu-id="86910-123">Valige puult Funktsionid \ Finantsdimensioonide üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="86910-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="86910-124">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="86910-124">Click Add root.</span></span>
    * <span data-ttu-id="86910-125">See andmeallikas määrab, kuidas määratletakse finantsdimensioonide ulatus mis tahes aruande puhul, mis kasutab seda mudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="86910-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="86910-126">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="86910-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="86910-127">Valige väljal Dimensioonide küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="86910-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="86910-128">Valige Jah, et lubada kasutajal valida käitusajal dimensioone vormilt Kasutaja dialoog.</span><span class="sxs-lookup"><span data-stu-id="86910-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="86910-129">Kui olekuks on määratud Ei, kasutatakse vaikimisi kõiki praeguse eksemplari finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="86910-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="86910-130">Tehke väljal Finantsdimensioonide valimine valik Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="86910-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="86910-131">Valige Kõik, et võimaldada kasutajal valida praeguse eksemplari soovitud dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="86910-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="86910-132">Valige Juriidiline isik, et võimaldada kasutajal valida ettevõtte dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="86910-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="86910-133">Valige Dimensioon, et võimaldada kasutajal valida dimensioone, kasutades ühte dimensioonikogumit.</span><span class="sxs-lookup"><span data-stu-id="86910-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="86910-134">Valige väljal Põhikonto küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="86910-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="86910-135">Määrake valiku Põhikonto küsimine väärtuseks Jah, et lasta kasutajatel valida põhikontot dimensioonide loendi osana.</span><span class="sxs-lookup"><span data-stu-id="86910-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="86910-136">Kui väärtus on Ei, ei lisata põhikontot dimensioonide loendisse ja valik On põhikonto kohustuslik on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="86910-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="86910-137">Kui valiku On põhikonto kohustuslik väärtuseks on määratud Jah, siis lisatakse põhikonto dimensioonide loendisse kasutaja valikust olenemata.</span><span class="sxs-lookup"><span data-stu-id="86910-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="86910-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="86910-138">Click OK.</span></span>
23. <span data-ttu-id="86910-139">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="86910-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="86910-140">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="86910-140">Click Add root.</span></span>
25. <span data-ttu-id="86910-141">Tippige väljale Nimi tekst LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="86910-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="86910-142">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="86910-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="86910-143">Tippige väljale Tabel tekst LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="86910-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="86910-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="86910-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="86910-145">Andmemudeli elementide vastendamine lisatud andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="86910-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="86910-146">Laiendage puul väärtust 'Tööleht.</span><span class="sxs-lookup"><span data-stu-id="86910-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="86910-147">Laiendage puul väärtust Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="86910-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="86910-148">Laiendage puul väärtust Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="86910-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="86910-149">Laiendage puul valikut Dimensioonide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="86910-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="86910-150">Laiendage puul valikut LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="86910-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="86910-151">Laiendage puul valikut „LedgerJournal\<Seosed“.</span><span class="sxs-lookup"><span data-stu-id="86910-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="86910-152">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="86910-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="86910-153">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Kanne“.</span><span class="sxs-lookup"><span data-stu-id="86910-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="86910-154">Valige puult Tööleht \ Kanne \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="86910-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="86910-155">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-155">Click Bind.</span></span>
11. <span data-ttu-id="86910-156">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="86910-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="86910-157">Pange tähele, et igasuguse viite puhul finantsdimensioonidele, mille väärtuseks on määratud näiteks LedgerDimension, on saadaval vastav andmeallika üksus (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="86910-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="86910-158">See andmeallika üksus pakub selle dimensioonikogumi finantsdimensioone kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="86910-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="86910-159">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="86910-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="86910-160">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="86910-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="86910-161">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus“.</span><span class="sxs-lookup"><span data-stu-id="86910-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="86910-162">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon“.</span><span class="sxs-lookup"><span data-stu-id="86910-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="86910-163">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon\Nimi“.</span><span class="sxs-lookup"><span data-stu-id="86910-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="86910-164">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="86910-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="86910-165">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-165">Click Bind.</span></span>
19. <span data-ttu-id="86910-166">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kirjeldus“.</span><span class="sxs-lookup"><span data-stu-id="86910-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="86910-167">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="86910-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="86910-168">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-168">Click Bind.</span></span>
22. <span data-ttu-id="86910-169">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kood“.</span><span class="sxs-lookup"><span data-stu-id="86910-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="86910-170">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kood.</span><span class="sxs-lookup"><span data-stu-id="86910-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="86910-171">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-171">Click Bind.</span></span>
25. <span data-ttu-id="86910-172">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="86910-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="86910-173">Valige puult Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="86910-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="86910-174">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-174">Click Bind.</span></span>
28. <span data-ttu-id="86910-175">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="86910-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="86910-176">Valige puult Tööleht \ Kanne \ Deebet.</span><span class="sxs-lookup"><span data-stu-id="86910-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="86910-177">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-177">Click Bind.</span></span>
31. <span data-ttu-id="86910-178">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="86910-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="86910-179">Valige puult Tööleht \ Kanne \ Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="86910-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="86910-180">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-180">Click Bind.</span></span>
34. <span data-ttu-id="86910-181">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="86910-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="86910-182">Valige puult Tööleht \ Kanne \ Valuuta.</span><span class="sxs-lookup"><span data-stu-id="86910-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="86910-183">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-183">Click Bind.</span></span>
37. <span data-ttu-id="86910-184">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="86910-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="86910-185">Valige puult Tööleht \ Kanne \ Kreedit.</span><span class="sxs-lookup"><span data-stu-id="86910-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="86910-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-186">Click Bind.</span></span>
40. <span data-ttu-id="86910-187">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="86910-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="86910-188">Valige puult Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="86910-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="86910-189">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-189">Click Bind.</span></span>
43. <span data-ttu-id="86910-190">Valige puult LedgerJournal \ Töölehe partiinumber(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="86910-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="86910-191">Valige puult Tööleht \ Partii.</span><span class="sxs-lookup"><span data-stu-id="86910-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="86910-192">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-192">Click Bind.</span></span>
46. <span data-ttu-id="86910-193">Valige puult LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="86910-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="86910-194">Valige puult Tööleht.</span><span class="sxs-lookup"><span data-stu-id="86910-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="86910-195">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-195">Click Bind.</span></span>
49. <span data-ttu-id="86910-196">Laiendage puul väärtust Dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="86910-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="86910-197">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="86910-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="86910-198">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon.</span><span class="sxs-lookup"><span data-stu-id="86910-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="86910-199">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="86910-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="86910-200">Valige puult Dimensioonide seadistus \ Kood.</span><span class="sxs-lookup"><span data-stu-id="86910-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="86910-201">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-201">Click Bind.</span></span>
55. <span data-ttu-id="86910-202">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Aruande veeru nimi.</span><span class="sxs-lookup"><span data-stu-id="86910-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="86910-203">Valige puult Dimensioonide seadistus \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="86910-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="86910-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-204">Click Bind.</span></span>
58. <span data-ttu-id="86910-205">Valige puult Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="86910-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="86910-206">Valige puult Dimensioonide seadistus.</span><span class="sxs-lookup"><span data-stu-id="86910-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="86910-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="86910-207">Click Bind.</span></span>
61. <span data-ttu-id="86910-208">Valige puult väärtus Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="86910-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="86910-209">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="86910-209">Click Edit.</span></span>
63. <span data-ttu-id="86910-210">Sisestage väljale expressionAsStringText väärtus Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="86910-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="86910-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="86910-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="86910-212">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="86910-212">Click Save.</span></span>
65. <span data-ttu-id="86910-213">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="86910-213">Close the page.</span></span>
66. <span data-ttu-id="86910-214">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="86910-214">Click Save.</span></span>
67. <span data-ttu-id="86910-215">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="86910-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="86910-216">Täitke see mudeli mustandi versioon</span><span class="sxs-lookup"><span data-stu-id="86910-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="86910-217">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="86910-217">Close the page.</span></span>
2. <span data-ttu-id="86910-218">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="86910-218">Close the page.</span></span>
3. <span data-ttu-id="86910-219">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="86910-219">Click Change status.</span></span>
4. <span data-ttu-id="86910-220">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="86910-220">Click Complete.</span></span>
5. <span data-ttu-id="86910-221">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="86910-221">Click OK.</span></span>

