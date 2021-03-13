---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (2. osa – mudeli vastendamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit kasutama finantsdimensioone andmeallikana ER-i aruannetele. (2. osa)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 02c730d08c411e736a7f8b9e7bad3d6a18cb8e6a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093233"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="bd1e5-104">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (2. osa – mudeli vastendamine)</span><span class="sxs-lookup"><span data-stu-id="bd1e5-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd1e5-105">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="bd1e5-106">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="bd1e5-107">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine)”.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="bd1e5-108">Vajalike andmeallikate lisamine mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="bd1e5-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="bd1e5-109">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="bd1e5-110">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="bd1e5-111">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-111">Click Designer.</span></span>
4. <span data-ttu-id="bd1e5-112">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="bd1e5-113">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-113">Click New.</span></span>
6. <span data-ttu-id="bd1e5-114">Tehke väljal Definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="bd1e5-115">Tippige Dimensioonide andmete vastendamine väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="bd1e5-116">Tippige Dimensioonide andmete vastendamine väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="bd1e5-117">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-117">Click Save.</span></span>
10. <span data-ttu-id="bd1e5-118">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-118">Click Designer.</span></span>
11. <span data-ttu-id="bd1e5-119">Valige puul väärtus Dynamics 365 for Operations \ Tabel.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="bd1e5-120">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-120">Click Add root.</span></span>
13. <span data-ttu-id="bd1e5-121">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="bd1e5-122">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="bd1e5-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-123">Click OK.</span></span>
16. <span data-ttu-id="bd1e5-124">Valige puult Funktsionid \ Finantsdimensioonide üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="bd1e5-125">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-125">Click Add root.</span></span>
    * <span data-ttu-id="bd1e5-126">See andmeallikas määrab, kuidas määratletakse finantsdimensioonide ulatus mis tahes aruande puhul, mis kasutab seda mudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="bd1e5-127">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="bd1e5-128">Valige väljal Dimensioonide küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="bd1e5-129">Valige Jah, et lubada kasutajal valida käitusajal dimensioone vormilt Kasutaja dialoog.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="bd1e5-130">Kui olekuks on määratud Ei, kasutatakse vaikimisi kõiki praeguse eksemplari finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="bd1e5-131">Tehke väljal Finantsdimensioonide valimine valik Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="bd1e5-132">Valige Kõik, et võimaldada kasutajal valida praeguse eksemplari soovitud dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="bd1e5-133">Valige Juriidiline isik, et võimaldada kasutajal valida ettevõtte dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="bd1e5-134">Valige Dimensioon, et võimaldada kasutajal valida dimensioone, kasutades ühte dimensioonikogumit.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="bd1e5-135">Valige väljal Põhikonto küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="bd1e5-136">Määrake valiku „Põhikonto küsimine” väärtuseks Jah, et lasta kasutajatel valida põhikontot dimensioonide loendi osana.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="bd1e5-137">Kui väärtus on Ei, ei lisata põhikontot dimensioonide loendisse ja valik „Kas põhikonto on kohustuslik” on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="bd1e5-138">Kui valiku „Kas põhikonto on kohustuslik” väärtuseks on määratud Jah, siis lisatakse põhikonto dimensioonide loendisse kasutaja valikust olenemata.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="bd1e5-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-139">Click OK.</span></span>
<span data-ttu-id="bd1e5-140">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="bd1e5-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="bd1e5-141">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="bd1e5-142">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-142">Click Add root.</span></span>
25. <span data-ttu-id="bd1e5-143">Tippige väljale Nimi tekst LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="bd1e5-144">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="bd1e5-145">Tippige väljale Tabel tekst LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="bd1e5-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-146">Click OK.</span></span>
<span data-ttu-id="bd1e5-147">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="bd1e5-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="bd1e5-148">Andmemudeli elementide vastendamine lisatud andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="bd1e5-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="bd1e5-149">Laiendage puul väärtust 'Tööleht.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="bd1e5-150">Laiendage puul väärtust Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="bd1e5-151">Laiendage puul väärtust Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="bd1e5-152">Laiendage puul valikut Dimensioonide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="bd1e5-153">Laiendage puul valikut LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="bd1e5-154">Laiendage puul valikut „LedgerJournal\<Seosed“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="bd1e5-155">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="bd1e5-156">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Kanne“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="bd1e5-157">Valige puult Tööleht \ Kanne \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="bd1e5-158">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-158">Click Bind.</span></span>
11. <span data-ttu-id="bd1e5-159">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="bd1e5-160">Pange tähele, et igasuguse viite puhul finantsdimensioonidele, mille väärtuseks on määratud näiteks LedgerDimension, on saadaval vastav andmeallika üksus (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="bd1e5-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="bd1e5-161">See andmeallika üksus pakub selle dimensioonikogumi finantsdimensioone kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="bd1e5-162">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="bd1e5-163">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="bd1e5-164">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="bd1e5-165">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="bd1e5-166">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon\Nimi“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="bd1e5-167">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="bd1e5-168">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-168">Click Bind.</span></span>
19. <span data-ttu-id="bd1e5-169">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kirjeldus“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="bd1e5-170">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="bd1e5-171">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-171">Click Bind.</span></span>
22. <span data-ttu-id="bd1e5-172">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kood“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="bd1e5-173">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kood.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="bd1e5-174">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-174">Click Bind.</span></span>
25. <span data-ttu-id="bd1e5-175">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="bd1e5-176">Valige puult Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="bd1e5-177">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-177">Click Bind.</span></span>
<span data-ttu-id="bd1e5-178">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="bd1e5-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="bd1e5-179">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="bd1e5-180">Valige puult Tööleht \ Kanne \ Deebet.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="bd1e5-181">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-181">Click Bind.</span></span>
31. <span data-ttu-id="bd1e5-182">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="bd1e5-183">Valige puult Tööleht \ Kanne \ Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="bd1e5-184">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-184">Click Bind.</span></span>
34. <span data-ttu-id="bd1e5-185">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="bd1e5-186">Valige puult Tööleht \ Kanne \ Valuuta.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="bd1e5-187">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-187">Click Bind.</span></span>
37. <span data-ttu-id="bd1e5-188">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="bd1e5-189">Valige puult Tööleht \ Kanne \ Kreedit.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="bd1e5-190">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-190">Click Bind.</span></span>
40. <span data-ttu-id="bd1e5-191">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="bd1e5-192">Valige puult Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="bd1e5-193">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-193">Click Bind.</span></span>
43. <span data-ttu-id="bd1e5-194">Valige puult LedgerJournal \ Töölehe partiinumber(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="bd1e5-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="bd1e5-195">Valige puult Tööleht \ Partii.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="bd1e5-196">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-196">Click Bind.</span></span>
46. <span data-ttu-id="bd1e5-197">Valige puult LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="bd1e5-198">Valige puult Tööleht.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="bd1e5-199">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-199">Click Bind.</span></span>
49. <span data-ttu-id="bd1e5-200">Laiendage puul väärtust Dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="bd1e5-201">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="bd1e5-202">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="bd1e5-203">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="bd1e5-204">Valige puult Dimensioonide seadistus \ Kood.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="bd1e5-205">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-205">Click Bind.</span></span>
55. <span data-ttu-id="bd1e5-206">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Aruande veeru nimi.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="bd1e5-207">Valige puult Dimensioonide seadistus \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="bd1e5-208">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-208">Click Bind.</span></span>
58. <span data-ttu-id="bd1e5-209">Valige puult Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="bd1e5-210">Valige puult Dimensioonide seadistus.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="bd1e5-211">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-211">Click Bind.</span></span>
61. <span data-ttu-id="bd1e5-212">Valige puult väärtus Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="bd1e5-213">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-213">Click Edit.</span></span>
63. <span data-ttu-id="bd1e5-214">Sisestage väljale expressionAsStringText väärtus Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="bd1e5-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="bd1e5-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="bd1e5-216">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-216">Click Save.</span></span>
<span data-ttu-id="bd1e5-217">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="bd1e5-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="bd1e5-218">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-218">Close the page.</span></span>
66. <span data-ttu-id="bd1e5-219">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-219">Click Save.</span></span>
67. <span data-ttu-id="bd1e5-220">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="bd1e5-221">Täitke see mudeli mustandi versioon</span><span class="sxs-lookup"><span data-stu-id="bd1e5-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="bd1e5-222">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-222">Close the page.</span></span>
2. <span data-ttu-id="bd1e5-223">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-223">Close the page.</span></span>
3. <span data-ttu-id="bd1e5-224">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-224">Click Change status.</span></span>
4. <span data-ttu-id="bd1e5-225">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-225">Click Complete.</span></span>
5. <span data-ttu-id="bd1e5-226">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bd1e5-226">Click OK.</span></span>
<span data-ttu-id="bd1e5-227">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="bd1e5-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
