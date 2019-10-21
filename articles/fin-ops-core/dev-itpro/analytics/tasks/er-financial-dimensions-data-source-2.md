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
ms.openlocfilehash: eedb8321b43ab5f5d9cb56166b68d6e9508c104f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182458"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2-model-mapping"></a><span data-ttu-id="effcb-103">Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine)</span><span class="sxs-lookup"><span data-stu-id="effcb-103">ER Use financial dimensions as a data source (Part 2: Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="effcb-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="effcb-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="effcb-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="effcb-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="effcb-106">Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine).</span><span class="sxs-lookup"><span data-stu-id="effcb-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="effcb-107">Vajalike andmeallikate lisamine mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="effcb-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="effcb-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="effcb-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="effcb-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="effcb-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="effcb-110">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="effcb-110">Click Designer.</span></span>
4. <span data-ttu-id="effcb-111">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="effcb-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="effcb-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="effcb-112">Click New.</span></span>
6. <span data-ttu-id="effcb-113">Tehke väljal Definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="effcb-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="effcb-114">Tippige Dimensioonide andmete vastendamine väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="effcb-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="effcb-115">Tippige Dimensioonide andmete vastendamine väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="effcb-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="effcb-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="effcb-116">Click Save.</span></span>
10. <span data-ttu-id="effcb-117">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="effcb-117">Click Designer.</span></span>
11. <span data-ttu-id="effcb-118">Valige puul väärtus Dynamics 365 for Operations \ Tabel.</span><span class="sxs-lookup"><span data-stu-id="effcb-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="effcb-119">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="effcb-119">Click Add root.</span></span>
13. <span data-ttu-id="effcb-120">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="effcb-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="effcb-121">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="effcb-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="effcb-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="effcb-122">Click OK.</span></span>
16. <span data-ttu-id="effcb-123">Valige puult Funktsionid \ Finantsdimensioonide üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="effcb-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="effcb-124">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="effcb-124">Click Add root.</span></span>
    * <span data-ttu-id="effcb-125">See andmeallikas määrab, kuidas määratletakse finantsdimensioonide ulatus mis tahes aruande puhul, mis kasutab seda mudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="effcb-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="effcb-126">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="effcb-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="effcb-127">Valige väljal Dimensioonide küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="effcb-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="effcb-128">Valige Jah, et lubada kasutajal valida käitusajal dimensioone vormilt Kasutaja dialoog.</span><span class="sxs-lookup"><span data-stu-id="effcb-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="effcb-129">Kui olekuks on määratud Ei, kasutatakse vaikimisi kõiki praeguse eksemplari finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="effcb-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="effcb-130">Tehke väljal Finantsdimensioonide valimine valik Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="effcb-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="effcb-131">Valige Kõik, et võimaldada kasutajal valida praeguse eksemplari soovitud dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="effcb-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="effcb-132">Valige Juriidiline isik, et võimaldada kasutajal valida ettevõtte dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="effcb-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="effcb-133">Valige Dimensioon, et võimaldada kasutajal valida dimensioone, kasutades ühte dimensioonikogumit.</span><span class="sxs-lookup"><span data-stu-id="effcb-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="effcb-134">Valige väljal Põhikonto küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="effcb-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="effcb-135">Määrake valiku Põhikonto küsimine väärtuseks Jah, et lasta kasutajatel valida põhikontot dimensioonide loendi osana.</span><span class="sxs-lookup"><span data-stu-id="effcb-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="effcb-136">Kui väärtus on Ei, ei lisata põhikontot dimensioonide loendisse ja valik On põhikonto kohustuslik on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="effcb-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="effcb-137">Kui valiku On põhikonto kohustuslik väärtuseks on määratud Jah, siis lisatakse põhikonto dimensioonide loendisse kasutaja valikust olenemata.</span><span class="sxs-lookup"><span data-stu-id="effcb-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="effcb-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="effcb-138">Click OK.</span></span>
23. <span data-ttu-id="effcb-139">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="effcb-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="effcb-140">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="effcb-140">Click Add root.</span></span>
25. <span data-ttu-id="effcb-141">Tippige väljale Nimi tekst LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="effcb-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="effcb-142">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="effcb-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="effcb-143">Tippige väljale Tabel tekst LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="effcb-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="effcb-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="effcb-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="effcb-145">Andmemudeli elementide vastendamine lisatud andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="effcb-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="effcb-146">Laiendage puul väärtust 'Tööleht.</span><span class="sxs-lookup"><span data-stu-id="effcb-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="effcb-147">Laiendage puul väärtust Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="effcb-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="effcb-148">Laiendage puul väärtust Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="effcb-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="effcb-149">Laiendage puul valikut Dimensioonide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="effcb-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="effcb-150">Laiendage puul valikut LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="effcb-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="effcb-151">Laiendage puul valikut „LedgerJournal\<Seosed“.</span><span class="sxs-lookup"><span data-stu-id="effcb-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="effcb-152">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="effcb-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="effcb-153">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Kanne“.</span><span class="sxs-lookup"><span data-stu-id="effcb-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="effcb-154">Valige puult Tööleht \ Kanne \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="effcb-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="effcb-155">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-155">Click Bind.</span></span>
11. <span data-ttu-id="effcb-156">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="effcb-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="effcb-157">Pange tähele, et igasuguse viite puhul finantsdimensioonidele, mille väärtuseks on määratud näiteks LedgerDimension, on saadaval vastav andmeallika üksus (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="effcb-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="effcb-158">See andmeallika üksus pakub selle dimensioonikogumi finantsdimensioone kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="effcb-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="effcb-159">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="effcb-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="effcb-160">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="effcb-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="effcb-161">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus“.</span><span class="sxs-lookup"><span data-stu-id="effcb-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="effcb-162">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon“.</span><span class="sxs-lookup"><span data-stu-id="effcb-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="effcb-163">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon\Nimi“.</span><span class="sxs-lookup"><span data-stu-id="effcb-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="effcb-164">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="effcb-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="effcb-165">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-165">Click Bind.</span></span>
19. <span data-ttu-id="effcb-166">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kirjeldus“.</span><span class="sxs-lookup"><span data-stu-id="effcb-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="effcb-167">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="effcb-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="effcb-168">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-168">Click Bind.</span></span>
22. <span data-ttu-id="effcb-169">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kood“.</span><span class="sxs-lookup"><span data-stu-id="effcb-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="effcb-170">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kood.</span><span class="sxs-lookup"><span data-stu-id="effcb-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="effcb-171">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-171">Click Bind.</span></span>
25. <span data-ttu-id="effcb-172">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="effcb-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="effcb-173">Valige puult Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="effcb-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="effcb-174">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-174">Click Bind.</span></span>
28. <span data-ttu-id="effcb-175">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="effcb-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="effcb-176">Valige puult Tööleht \ Kanne \ Deebet.</span><span class="sxs-lookup"><span data-stu-id="effcb-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="effcb-177">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-177">Click Bind.</span></span>
31. <span data-ttu-id="effcb-178">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="effcb-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="effcb-179">Valige puult Tööleht \ Kanne \ Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="effcb-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="effcb-180">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-180">Click Bind.</span></span>
34. <span data-ttu-id="effcb-181">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="effcb-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="effcb-182">Valige puult Tööleht \ Kanne \ Valuuta.</span><span class="sxs-lookup"><span data-stu-id="effcb-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="effcb-183">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-183">Click Bind.</span></span>
37. <span data-ttu-id="effcb-184">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="effcb-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="effcb-185">Valige puult Tööleht \ Kanne \ Kreedit.</span><span class="sxs-lookup"><span data-stu-id="effcb-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="effcb-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-186">Click Bind.</span></span>
40. <span data-ttu-id="effcb-187">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="effcb-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="effcb-188">Valige puult Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="effcb-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="effcb-189">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-189">Click Bind.</span></span>
43. <span data-ttu-id="effcb-190">Valige puult LedgerJournal \ Töölehe partiinumber(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="effcb-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="effcb-191">Valige puult Tööleht \ Partii.</span><span class="sxs-lookup"><span data-stu-id="effcb-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="effcb-192">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-192">Click Bind.</span></span>
46. <span data-ttu-id="effcb-193">Valige puult LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="effcb-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="effcb-194">Valige puult Tööleht.</span><span class="sxs-lookup"><span data-stu-id="effcb-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="effcb-195">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-195">Click Bind.</span></span>
49. <span data-ttu-id="effcb-196">Laiendage puul väärtust Dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="effcb-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="effcb-197">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="effcb-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="effcb-198">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon.</span><span class="sxs-lookup"><span data-stu-id="effcb-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="effcb-199">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="effcb-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="effcb-200">Valige puult Dimensioonide seadistus \ Kood.</span><span class="sxs-lookup"><span data-stu-id="effcb-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="effcb-201">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-201">Click Bind.</span></span>
55. <span data-ttu-id="effcb-202">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Aruande veeru nimi.</span><span class="sxs-lookup"><span data-stu-id="effcb-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="effcb-203">Valige puult Dimensioonide seadistus \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="effcb-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="effcb-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-204">Click Bind.</span></span>
58. <span data-ttu-id="effcb-205">Valige puult Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="effcb-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="effcb-206">Valige puult Dimensioonide seadistus.</span><span class="sxs-lookup"><span data-stu-id="effcb-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="effcb-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="effcb-207">Click Bind.</span></span>
61. <span data-ttu-id="effcb-208">Valige puult väärtus Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="effcb-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="effcb-209">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="effcb-209">Click Edit.</span></span>
63. <span data-ttu-id="effcb-210">Sisestage väljale expressionAsStringText väärtus Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="effcb-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="effcb-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="effcb-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="effcb-212">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="effcb-212">Click Save.</span></span>
65. <span data-ttu-id="effcb-213">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="effcb-213">Close the page.</span></span>
66. <span data-ttu-id="effcb-214">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="effcb-214">Click Save.</span></span>
67. <span data-ttu-id="effcb-215">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="effcb-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="effcb-216">Täitke see mudeli mustandi versioon</span><span class="sxs-lookup"><span data-stu-id="effcb-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="effcb-217">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="effcb-217">Close the page.</span></span>
2. <span data-ttu-id="effcb-218">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="effcb-218">Close the page.</span></span>
3. <span data-ttu-id="effcb-219">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="effcb-219">Click Change status.</span></span>
4. <span data-ttu-id="effcb-220">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="effcb-220">Click Complete.</span></span>
5. <span data-ttu-id="effcb-221">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="effcb-221">Click OK.</span></span>

