---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (2. osa – mudeli vastendamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.
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
ms.openlocfilehash: 3214ddb1e077d889fb7b785bee2554b96c3907ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681681"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="15689-103">Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (2. osa – mudeli vastendamine)</span><span class="sxs-lookup"><span data-stu-id="15689-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="15689-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="15689-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="15689-105">Neid toiminguid saab teha igas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="15689-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="15689-106">Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine)”.</span><span class="sxs-lookup"><span data-stu-id="15689-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="15689-107">Vajalike andmeallikate lisamine mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="15689-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="15689-108">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="15689-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="15689-109">Valige puult Finantsdimensioonide näidismudel.</span><span class="sxs-lookup"><span data-stu-id="15689-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="15689-110">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="15689-110">Click Designer.</span></span>
4. <span data-ttu-id="15689-111">Klõpsake suvandit Mudeli vastendamine andmeallikaga.</span><span class="sxs-lookup"><span data-stu-id="15689-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="15689-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="15689-112">Click New.</span></span>
6. <span data-ttu-id="15689-113">Tehke väljal Definitsioon valik Kirje.</span><span class="sxs-lookup"><span data-stu-id="15689-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="15689-114">Tippige Dimensioonide andmete vastendamine väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="15689-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="15689-115">Tippige Dimensioonide andmete vastendamine väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="15689-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="15689-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15689-116">Click Save.</span></span>
10. <span data-ttu-id="15689-117">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="15689-117">Click Designer.</span></span>
11. <span data-ttu-id="15689-118">Valige puul väärtus Dynamics 365 for Operations \ Tabel.</span><span class="sxs-lookup"><span data-stu-id="15689-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="15689-119">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="15689-119">Click Add root.</span></span>
13. <span data-ttu-id="15689-120">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="15689-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="15689-121">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="15689-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="15689-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15689-122">Click OK.</span></span>
16. <span data-ttu-id="15689-123">Valige puult Funktsionid \ Finantsdimensioonide üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="15689-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="15689-124">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="15689-124">Click Add root.</span></span>
    * <span data-ttu-id="15689-125">See andmeallikas määrab, kuidas määratletakse finantsdimensioonide ulatus mis tahes aruande puhul, mis kasutab seda mudelit andmeallikana.</span><span class="sxs-lookup"><span data-stu-id="15689-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="15689-126">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="15689-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="15689-127">Valige väljal Dimensioonide küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="15689-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="15689-128">Valige Jah, et lubada kasutajal valida käitusajal dimensioone vormilt Kasutaja dialoog.</span><span class="sxs-lookup"><span data-stu-id="15689-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="15689-129">Kui olekuks on määratud Ei, kasutatakse vaikimisi kõiki praeguse eksemplari finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="15689-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="15689-130">Tehke väljal Finantsdimensioonide valimine valik Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="15689-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="15689-131">Valige Kõik, et võimaldada kasutajal valida praeguse eksemplari soovitud dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="15689-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="15689-132">Valige Juriidiline isik, et võimaldada kasutajal valida ettevõtte dimensioone väljalt Otsing.</span><span class="sxs-lookup"><span data-stu-id="15689-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="15689-133">Valige Dimensioon, et võimaldada kasutajal valida dimensioone, kasutades ühte dimensioonikogumit.</span><span class="sxs-lookup"><span data-stu-id="15689-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="15689-134">Valige väljal Põhikonto küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="15689-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="15689-135">Määrake valiku „Põhikonto küsimine” väärtuseks Jah, et lasta kasutajatel valida põhikontot dimensioonide loendi osana.</span><span class="sxs-lookup"><span data-stu-id="15689-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="15689-136">Kui väärtus on Ei, ei lisata põhikontot dimensioonide loendisse ja valik „Kas põhikonto on kohustuslik” on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="15689-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="15689-137">Kui valiku „Kas põhikonto on kohustuslik” väärtuseks on määratud Jah, siis lisatakse põhikonto dimensioonide loendisse kasutaja valikust olenemata.</span><span class="sxs-lookup"><span data-stu-id="15689-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="15689-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15689-138">Click OK.</span></span>
<span data-ttu-id="15689-139">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="15689-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="15689-140">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="15689-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="15689-141">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="15689-141">Click Add root.</span></span>
25. <span data-ttu-id="15689-142">Tippige väljale Nimi tekst LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="15689-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="15689-143">Valige väljal Päringu küsimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="15689-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="15689-144">Tippige väljale Tabel tekst LedgerJournalTable.</span><span class="sxs-lookup"><span data-stu-id="15689-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="15689-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15689-145">Click OK.</span></span>
<span data-ttu-id="15689-146">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="15689-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="15689-147">Andmemudeli elementide vastendamine lisatud andmeallikatega</span><span class="sxs-lookup"><span data-stu-id="15689-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="15689-148">Laiendage puul väärtust 'Tööleht.</span><span class="sxs-lookup"><span data-stu-id="15689-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="15689-149">Laiendage puul väärtust Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="15689-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="15689-150">Laiendage puul väärtust Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="15689-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="15689-151">Laiendage puul valikut Dimensioonide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="15689-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="15689-152">Laiendage puul valikut LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="15689-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="15689-153">Laiendage puul valikut „LedgerJournal\<Seosed“.</span><span class="sxs-lookup"><span data-stu-id="15689-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="15689-154">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="15689-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="15689-155">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Kanne“.</span><span class="sxs-lookup"><span data-stu-id="15689-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="15689-156">Valige puult Tööleht \ Kanne \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="15689-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="15689-157">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-157">Click Bind.</span></span>
11. <span data-ttu-id="15689-158">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="15689-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="15689-159">Pange tähele, et igasuguse viite puhul finantsdimensioonidele, mille väärtuseks on määratud näiteks LedgerDimension, on saadaval vastav andmeallika üksus (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="15689-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="15689-160">See andmeallika üksus pakub selle dimensioonikogumi finantsdimensioone kirjete loendina.</span><span class="sxs-lookup"><span data-stu-id="15689-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="15689-161">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="15689-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="15689-162">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="15689-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="15689-163">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus“.</span><span class="sxs-lookup"><span data-stu-id="15689-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="15689-164">Laiendage puul valikut „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon“.</span><span class="sxs-lookup"><span data-stu-id="15689-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="15689-165">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Definitsioon\Nimi“.</span><span class="sxs-lookup"><span data-stu-id="15689-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="15689-166">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="15689-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="15689-167">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-167">Click Bind.</span></span>
19. <span data-ttu-id="15689-168">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kirjeldus“.</span><span class="sxs-lookup"><span data-stu-id="15689-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="15689-169">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="15689-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="15689-170">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-170">Click Bind.</span></span>
22. <span data-ttu-id="15689-171">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid\Väärtus\Kood“.</span><span class="sxs-lookup"><span data-stu-id="15689-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="15689-172">Valige puult Tööleht \ Kanne \ Dimensioonide andmed \ Kood.</span><span class="sxs-lookup"><span data-stu-id="15689-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="15689-173">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-173">Click Bind.</span></span>
25. <span data-ttu-id="15689-174">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Põhikonto ja dimensioonid“.</span><span class="sxs-lookup"><span data-stu-id="15689-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="15689-175">Valige puult Tööleht \ Kanne \ Dimensioonide andmed.</span><span class="sxs-lookup"><span data-stu-id="15689-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="15689-176">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-176">Click Bind.</span></span>
<span data-ttu-id="15689-177">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="15689-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="15689-178">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="15689-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="15689-179">Valige puult Tööleht \ Kanne \ Deebet.</span><span class="sxs-lookup"><span data-stu-id="15689-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="15689-180">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-180">Click Bind.</span></span>
31. <span data-ttu-id="15689-181">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="15689-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="15689-182">Valige puult Tööleht \ Kanne \ Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="15689-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="15689-183">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-183">Click Bind.</span></span>
34. <span data-ttu-id="15689-184">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="15689-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="15689-185">Valige puult Tööleht \ Kanne \ Valuuta.</span><span class="sxs-lookup"><span data-stu-id="15689-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="15689-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-186">Click Bind.</span></span>
37. <span data-ttu-id="15689-187">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="15689-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="15689-188">Valige puult Tööleht \ Kanne \ Kreedit.</span><span class="sxs-lookup"><span data-stu-id="15689-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="15689-189">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-189">Click Bind.</span></span>
40. <span data-ttu-id="15689-190">Valige puult „LedgerJournal\<Seosed\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="15689-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="15689-191">Valige puult Tööleht \ Kanne.</span><span class="sxs-lookup"><span data-stu-id="15689-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="15689-192">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-192">Click Bind.</span></span>
43. <span data-ttu-id="15689-193">Valige puult LedgerJournal \ Töölehe partiinumber(JournalNum).</span><span class="sxs-lookup"><span data-stu-id="15689-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="15689-194">Valige puult Tööleht \ Partii.</span><span class="sxs-lookup"><span data-stu-id="15689-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="15689-195">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-195">Click Bind.</span></span>
46. <span data-ttu-id="15689-196">Valige puult LedgerJournal.</span><span class="sxs-lookup"><span data-stu-id="15689-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="15689-197">Valige puult Tööleht.</span><span class="sxs-lookup"><span data-stu-id="15689-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="15689-198">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-198">Click Bind.</span></span>
49. <span data-ttu-id="15689-199">Laiendage puul väärtust Dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="15689-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="15689-200">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="15689-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="15689-201">Laiendage puul väärtust Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon.</span><span class="sxs-lookup"><span data-stu-id="15689-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="15689-202">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="15689-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="15689-203">Valige puult Dimensioonide seadistus \ Kood.</span><span class="sxs-lookup"><span data-stu-id="15689-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="15689-204">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-204">Click Bind.</span></span>
55. <span data-ttu-id="15689-205">Valige puult Dimensioonid \ Põhikonto ja dimensioonid \ Definitsioon \ Aruande veeru nimi.</span><span class="sxs-lookup"><span data-stu-id="15689-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="15689-206">Valige puult Dimensioonide seadistus \ Nimi.</span><span class="sxs-lookup"><span data-stu-id="15689-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="15689-207">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-207">Click Bind.</span></span>
58. <span data-ttu-id="15689-208">Valige puult Dimensioonid \ Põhikonto ja dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="15689-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="15689-209">Valige puult Dimensioonide seadistus.</span><span class="sxs-lookup"><span data-stu-id="15689-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="15689-210">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="15689-210">Click Bind.</span></span>
61. <span data-ttu-id="15689-211">Valige puult väärtus Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="15689-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="15689-212">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="15689-212">Click Edit.</span></span>
63. <span data-ttu-id="15689-213">Sisestage väljale expressionAsStringText väärtus Company.'find()'.'name()'.</span><span class="sxs-lookup"><span data-stu-id="15689-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="15689-214">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="15689-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="15689-215">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15689-215">Click Save.</span></span>
<span data-ttu-id="15689-216">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="15689-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="15689-217">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="15689-217">Close the page.</span></span>
66. <span data-ttu-id="15689-218">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="15689-218">Click Save.</span></span>
67. <span data-ttu-id="15689-219">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="15689-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="15689-220">Täitke see mudeli mustandi versioon</span><span class="sxs-lookup"><span data-stu-id="15689-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="15689-221">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="15689-221">Close the page.</span></span>
2. <span data-ttu-id="15689-222">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="15689-222">Close the page.</span></span>
3. <span data-ttu-id="15689-223">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="15689-223">Click Change status.</span></span>
4. <span data-ttu-id="15689-224">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="15689-224">Click Complete.</span></span>
5. <span data-ttu-id="15689-225">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="15689-225">Click OK.</span></span>
<span data-ttu-id="15689-226">![ER-i mudelivastenduse koostaja leht](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="15689-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
