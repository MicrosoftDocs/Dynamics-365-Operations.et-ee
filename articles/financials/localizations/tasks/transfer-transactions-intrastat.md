---
title: Kannete ülekandmine Intrastati
description: Selles protseduuris selgitatakse, kuidas seadistada Intrastati parameetreid ja edastada kandeid Intrastati.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResCategoryHierarchyListPage, EcoResCategory, UnitOfMeasureLookup, ProcCategoryAddCommodityCode, EcoResProductDetailsExtended, IntrastatCommodityLookup, IntrastatTransactionCode, IntrastatParameters, DeliveryMode, MarkupTable, SalesTableListPage, SalesCreateOrder, SalesTable, MarkupTrans, SalesEditLines,  Intrastat, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13cc9dc2119ad3dc85d580e92edee7bb9ef2075c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1559317"
---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="a22f5-103">Kannete ülekandmine Intrastati</span><span class="sxs-lookup"><span data-stu-id="a22f5-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a22f5-104">Selles protseduuris selgitatakse, kuidas seadistada Intrastati parameetreid ja edastada kandeid Intrastati.</span><span class="sxs-lookup"><span data-stu-id="a22f5-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="a22f5-105">Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="a22f5-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="a22f5-106">Uue kaubakoodi loomine ja olemasoleva kaubakoodi värskendamine</span><span class="sxs-lookup"><span data-stu-id="a22f5-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="a22f5-107">Minge jaotisse Tooteteabe haldus > Seadistus > Kategooriad ja atribuudid > Kategooriahierarhiad.</span><span class="sxs-lookup"><span data-stu-id="a22f5-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="a22f5-108">Otsige või valige loendist kirje „Intrastati kaubaartikli koodid."</span><span class="sxs-lookup"><span data-stu-id="a22f5-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="a22f5-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a22f5-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a22f5-110">Valige puustruktuuris väärtus 'kirje'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="a22f5-111">Valige näiteks Intrastat\Speaker.</span><span class="sxs-lookup"><span data-stu-id="a22f5-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="a22f5-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a22f5-112">Click Edit.</span></span>
6. <span data-ttu-id="a22f5-113">Laiendage jaotist Väliskaubandus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="a22f5-114">Sisestage või valige väärtus väljal Lisaühikud.</span><span class="sxs-lookup"><span data-stu-id="a22f5-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-115">Valige näiteks tk.</span><span class="sxs-lookup"><span data-stu-id="a22f5-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="a22f5-116">Tehke väljal Kaal pole rakendatav valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a22f5-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="a22f5-117">Tehke puustruktuuris valik 'Intrastat'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="a22f5-118">Klõpsake suvandit Uus kategooriasõlm.</span><span class="sxs-lookup"><span data-stu-id="a22f5-118">Click New category node.</span></span>
11. <span data-ttu-id="a22f5-119">Sisestage väljale Nimi kaubaartikli nimi.</span><span class="sxs-lookup"><span data-stu-id="a22f5-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="a22f5-120">Tippige näiteks Muu kaup.</span><span class="sxs-lookup"><span data-stu-id="a22f5-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="a22f5-121">Sisestage väljale Kood kauba kood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="a22f5-122">Tippige näiteks väärtus 995 00 00.</span><span class="sxs-lookup"><span data-stu-id="a22f5-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="a22f5-123">Sisestage väärtus väljale Hüüdnimi.</span><span class="sxs-lookup"><span data-stu-id="a22f5-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="a22f5-124">Tippige näiteks väärtus Muu.</span><span class="sxs-lookup"><span data-stu-id="a22f5-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="a22f5-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a22f5-125">Click Save.</span></span>
15. <span data-ttu-id="a22f5-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a22f5-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="a22f5-127">Kaubakoodi määramine toote hierarhiale ja väljastatud tootele</span><span class="sxs-lookup"><span data-stu-id="a22f5-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="a22f5-128">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="a22f5-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a22f5-129">Näiteks filtreerige välja Nimi väärtusega 'müük'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="a22f5-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a22f5-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="a22f5-131">Laiendage puustruktuuris väärtust 'kategooria sõlm'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="a22f5-132">Laiendage näiteks väärtust Sales hierarchy\Home audio.</span><span class="sxs-lookup"><span data-stu-id="a22f5-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="a22f5-133">Valige puustruktuuris 'kauba koodile määratav kategooria'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="a22f5-134">Tehke näiteks valik Sales hierarchy\Home audio\Speakers.</span><span class="sxs-lookup"><span data-stu-id="a22f5-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="a22f5-135">Laiendage jaotist Kaubakoodid.</span><span class="sxs-lookup"><span data-stu-id="a22f5-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="a22f5-136">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a22f5-136">Click Add.</span></span>
7. <span data-ttu-id="a22f5-137">Tehke väljal Vali hierarhia valik 'Intrastat'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="a22f5-138">Loendist kaubakoodi otsimine ja valimine</span><span class="sxs-lookup"><span data-stu-id="a22f5-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="a22f5-139">Tehke näiteks valik 920 20 34 Speaker.</span><span class="sxs-lookup"><span data-stu-id="a22f5-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="a22f5-140">Klõpsake suvandit SelectCodes.</span><span class="sxs-lookup"><span data-stu-id="a22f5-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="a22f5-141">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-141">Click OK.</span></span>
11. <span data-ttu-id="a22f5-142">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="a22f5-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="a22f5-143">Valige loendist väljastatud toode, mille saate määrata kauba koodile.</span><span class="sxs-lookup"><span data-stu-id="a22f5-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="a22f5-144">Valige näiteks väärtus D0001.</span><span class="sxs-lookup"><span data-stu-id="a22f5-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="a22f5-145">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a22f5-145">Click Edit.</span></span>
14. <span data-ttu-id="a22f5-146">Laiendage jaotist Väliskaubandus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="a22f5-147">Väljale Kaup kauba koodi sisestamine</span><span class="sxs-lookup"><span data-stu-id="a22f5-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="a22f5-148">Valige näiteks väärtus 920 20 34 Speaker.</span><span class="sxs-lookup"><span data-stu-id="a22f5-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="a22f5-149">Sisestage väljale Kulude protsent number.</span><span class="sxs-lookup"><span data-stu-id="a22f5-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="a22f5-150">Sisestage näiteks väärtus 3.</span><span class="sxs-lookup"><span data-stu-id="a22f5-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="a22f5-151">Väljale Riik/regioon päritoluriigi või -regiooni sisestamine</span><span class="sxs-lookup"><span data-stu-id="a22f5-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="a22f5-152">Valige näiteks väärtus AUT.</span><span class="sxs-lookup"><span data-stu-id="a22f5-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="a22f5-153">Laiendage jaotist Varude haldus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="a22f5-154">Sisestage väljale Netokaal kaal kilodes.</span><span class="sxs-lookup"><span data-stu-id="a22f5-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="a22f5-155">Sisestage näiteks väärtus 2,5.</span><span class="sxs-lookup"><span data-stu-id="a22f5-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="a22f5-156">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a22f5-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="a22f5-157">Intrastati kandekoodide ja väliskaubanduse parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="a22f5-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="a22f5-158">Avage Maks > Seadistus > Väliskaubandus > Kandekoodid</span><span class="sxs-lookup"><span data-stu-id="a22f5-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="a22f5-159">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-159">Click New.</span></span>
3. <span data-ttu-id="a22f5-160">Sisestage väärtus väljale Kande kood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="a22f5-161">Sisestage näiteks tagastusena kandekoodile väärtus 21.</span><span class="sxs-lookup"><span data-stu-id="a22f5-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="a22f5-162">Tippige väljale Nimi kandekoodi nimi.</span><span class="sxs-lookup"><span data-stu-id="a22f5-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="a22f5-163">Sisestage näiteks väärtus Tagasta.</span><span class="sxs-lookup"><span data-stu-id="a22f5-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="a22f5-164">Valige suvand väljal Statstiline summa.</span><span class="sxs-lookup"><span data-stu-id="a22f5-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="a22f5-165">Valige näiteks väärtus Tühi, mis näitab, et kandele tuleb alati esitada statistiline väärtus, mille puhul kandekood 21 on alati null.</span><span class="sxs-lookup"><span data-stu-id="a22f5-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="a22f5-166">Avage Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid</span><span class="sxs-lookup"><span data-stu-id="a22f5-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="a22f5-167">Sisestage või valige väärtus väljal Kande kood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-168">Valige näiteks väärtus 11.</span><span class="sxs-lookup"><span data-stu-id="a22f5-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="a22f5-169">Sisestage või valige väärtus väljal Kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="a22f5-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-170">See väärtus määratleb ka füüsilise tagastuse.</span><span class="sxs-lookup"><span data-stu-id="a22f5-170">This value also identifies the physical return.</span></span> <span data-ttu-id="a22f5-171">Füüsilise tagastuse kreeditarve kantakse Intrastati töölehel vastassuunaga.</span><span class="sxs-lookup"><span data-stu-id="a22f5-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="a22f5-172">Näiteks kantakse tagastustellimuse saabumine üle lähetusena.</span><span class="sxs-lookup"><span data-stu-id="a22f5-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="a22f5-173">Muidu käsitletakse kreeditarvet parandusena ja see edastatakse sama suuna ja vastasmärgiga.</span><span class="sxs-lookup"><span data-stu-id="a22f5-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="a22f5-174">Näiteks saabumise korrigeerimine edastatakse saabumisena, millel on negatiivne kogus ja aktiivne lipp on seatud olekusse Parandus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="a22f5-175">Laiendage jaotist Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="a22f5-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="a22f5-176">Tehke väljal Artikliga kaubad valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a22f5-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="a22f5-177">Valige see suvand, kui soovite üle kanda ainult kanded, millel on kaubaartikli kood määratud.</span><span class="sxs-lookup"><span data-stu-id="a22f5-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="a22f5-178">Kaubaartikli koodita kandeid ei edastata Intrastati.</span><span class="sxs-lookup"><span data-stu-id="a22f5-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="a22f5-179">Valige suvand väljal Kanna üle, kui täidetud on järgmine kriteerium.</span><span class="sxs-lookup"><span data-stu-id="a22f5-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="a22f5-180">Tehke näiteks valik Üks valitutest.</span><span class="sxs-lookup"><span data-stu-id="a22f5-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="a22f5-181">Laiendage jaotist Kaubakoodide hierarhia.</span><span class="sxs-lookup"><span data-stu-id="a22f5-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="a22f5-182">Klõpsake vahekaarti Riigi/regiooni atribuudid.</span><span class="sxs-lookup"><span data-stu-id="a22f5-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="a22f5-183">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-183">Click New.</span></span>
15. <span data-ttu-id="a22f5-184">Sisestage või valige väärtus väljal Riik/piirkond.</span><span class="sxs-lookup"><span data-stu-id="a22f5-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-185">Valige näiteks väärtus FRA.</span><span class="sxs-lookup"><span data-stu-id="a22f5-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="a22f5-186">Sisestage riigi ISO-kood väljale Intrastati kood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="a22f5-187">Tippige näiteks tekst FR.</span><span class="sxs-lookup"><span data-stu-id="a22f5-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="a22f5-188">Valige väljal Riigi/piirkonna tüüp suvand EL.</span><span class="sxs-lookup"><span data-stu-id="a22f5-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="a22f5-189">Klõpsake vahekaarti Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="a22f5-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="a22f5-190">Tarneviiside ja Intrastatis tasude lisamise reegliste seadistamine</span><span class="sxs-lookup"><span data-stu-id="a22f5-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="a22f5-191">Avage Müük ja turundus > Seadistus > Jaotus > Tarneviisid</span><span class="sxs-lookup"><span data-stu-id="a22f5-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="a22f5-192">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a22f5-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a22f5-193">Valige näiteks 20 Air.</span><span class="sxs-lookup"><span data-stu-id="a22f5-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="a22f5-194">Laiendage jaotist Väliskaubandus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="a22f5-195">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a22f5-195">Click Edit.</span></span>
5. <span data-ttu-id="a22f5-196">Sisestage või valige väärtus väljal Transport.</span><span class="sxs-lookup"><span data-stu-id="a22f5-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-197">Valige näiteks 02.</span><span class="sxs-lookup"><span data-stu-id="a22f5-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="a22f5-198">Avage Müügireskontro > Tasude seadistamine > Tasude kood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="a22f5-199">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="a22f5-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a22f5-200">Näiteks filtreerige välja Tasude kood väärtusega 'veos'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="a22f5-201">Laiendage jaotist Väliskaubandus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="a22f5-202">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a22f5-202">Click Edit.</span></span>
10. <span data-ttu-id="a22f5-203">Tehke väljal Intrastati arve väärtus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a22f5-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="a22f5-204">Summa kantakse väljale Arve tasud ja see võetakse kokku väljal Arve summa kantud summaga.</span><span class="sxs-lookup"><span data-stu-id="a22f5-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="a22f5-205">Tehke väljal Intrastati statistiline väärtus valik Jah, kui muudatuste summa tuleb edastada väljale Statistilised tasud ja liita statistilise summaga.</span><span class="sxs-lookup"><span data-stu-id="a22f5-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="a22f5-206">Toodete müümine EL-i klientidele</span><span class="sxs-lookup"><span data-stu-id="a22f5-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="a22f5-207">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="a22f5-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a22f5-208">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-208">Click New.</span></span>
3. <span data-ttu-id="a22f5-209">Väljal Kliendi konto EL-i kliendi valimine</span><span class="sxs-lookup"><span data-stu-id="a22f5-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="a22f5-210">Valige näiteks „DE-012 Litware Retail“.</span><span class="sxs-lookup"><span data-stu-id="a22f5-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="a22f5-211">Laiendage jaotist Tarne.</span><span class="sxs-lookup"><span data-stu-id="a22f5-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="a22f5-212">Sisestage või valige väärtus väljal Tarneviis.</span><span class="sxs-lookup"><span data-stu-id="a22f5-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-213">Valige näiteks 20 Air.</span><span class="sxs-lookup"><span data-stu-id="a22f5-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="a22f5-214">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-214">Click OK.</span></span>
7. <span data-ttu-id="a22f5-215">Asetage kursor müüsitellimuse ridade esimesele reale.</span><span class="sxs-lookup"><span data-stu-id="a22f5-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="a22f5-216">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-217">Valige näiteks 'D001'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="a22f5-218">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a22f5-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="a22f5-219">Klõpsake vahekaarti Väliskaubandus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="a22f5-220">Väli Transport täidetakse automaatselt valitud tarneviisi alusel.</span><span class="sxs-lookup"><span data-stu-id="a22f5-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="a22f5-221">Sisestage või valige väärtus väljal Sadam.</span><span class="sxs-lookup"><span data-stu-id="a22f5-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="a22f5-222">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="a22f5-222">Click Financials.</span></span>
    * <span data-ttu-id="a22f5-223">Vastavalt sätetele lisatakse see summa Intrastati arve väärtusele.</span><span class="sxs-lookup"><span data-stu-id="a22f5-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="a22f5-224">Klõpsake valikut Tasude haldamine.</span><span class="sxs-lookup"><span data-stu-id="a22f5-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="a22f5-225">Sisestage või valige väärtus väljal Tasukood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-226">Valige näiteks 'FREIGHT'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="a22f5-227">Märkige ruut Säilita.</span><span class="sxs-lookup"><span data-stu-id="a22f5-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="a22f5-228">Sisestage arv väljale Tasude väärtus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="a22f5-229">Sisestage näiteks '10'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="a22f5-230">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a22f5-230">Click Save.</span></span>
18. <span data-ttu-id="a22f5-231">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a22f5-231">Close the page.</span></span>
19. <span data-ttu-id="a22f5-232">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="a22f5-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="a22f5-233">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="a22f5-233">Click Invoice.</span></span>
21. <span data-ttu-id="a22f5-234">Laiendage jaotis Parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a22f5-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="a22f5-235">Valige väljal Kogus väärtus Kõik.</span><span class="sxs-lookup"><span data-stu-id="a22f5-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="a22f5-236">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="a22f5-237">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a22f5-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="a22f5-238">Sisestage näiteks '31.01.2015'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="a22f5-239">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-239">Click OK.</span></span>
26. <span data-ttu-id="a22f5-240">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-240">Click OK.</span></span>
27. <span data-ttu-id="a22f5-241">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a22f5-241">Close the page.</span></span>
28. <span data-ttu-id="a22f5-242">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a22f5-242">Click New.</span></span>
29. <span data-ttu-id="a22f5-243">Valige väljal Kliendi konto EL-i klient.</span><span class="sxs-lookup"><span data-stu-id="a22f5-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="a22f5-244">Valige näiteks 'DE-013 Trey Wholesales'</span><span class="sxs-lookup"><span data-stu-id="a22f5-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="a22f5-245">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-245">Click OK.</span></span>
31. <span data-ttu-id="a22f5-246">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="a22f5-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a22f5-247">Valige näiteks 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="a22f5-248">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a22f5-248">Click Save.</span></span>
33. <span data-ttu-id="a22f5-249">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="a22f5-249">Click Invoice.</span></span>
34. <span data-ttu-id="a22f5-250">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a22f5-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="a22f5-251">Sisestage näiteks kuupäev '31.01.2015'.</span><span class="sxs-lookup"><span data-stu-id="a22f5-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="a22f5-252">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-252">Click OK.</span></span>
36. <span data-ttu-id="a22f5-253">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="a22f5-254">Kannete ülekandmine Intrastati</span><span class="sxs-lookup"><span data-stu-id="a22f5-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="a22f5-255">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a22f5-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="a22f5-256">Klõpsake käsku Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="a22f5-256">Click Transfer.</span></span>
3. <span data-ttu-id="a22f5-257">Tehke väljal Kliendiarve valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a22f5-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="a22f5-258">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="a22f5-258">Click Filter.</span></span>
5. <span data-ttu-id="a22f5-259">Loendis rea märkimine kuupäevaga</span><span class="sxs-lookup"><span data-stu-id="a22f5-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="a22f5-260">Sisestage väärtus väljale Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="a22f5-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="a22f5-261">Sisestage näiteks filter perioodile jaanuar 2015 (täpne väärtus oleneb teie kuupäevavormingust): 01.01.2015..31.01.2015</span><span class="sxs-lookup"><span data-stu-id="a22f5-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="a22f5-262">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-262">Click OK.</span></span>
8. <span data-ttu-id="a22f5-263">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a22f5-263">Click OK.</span></span>
9. <span data-ttu-id="a22f5-264">Otsige ja valige loendist edastatud kirje.</span><span class="sxs-lookup"><span data-stu-id="a22f5-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="a22f5-265">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="a22f5-265">Click the General tab.</span></span>
    * <span data-ttu-id="a22f5-266">Vaadake üle edastatud andmed, sh sihtkoha/lähtekoha riik/-regioon, päritoluriik, kaal, kogus, kogus lisaühikutes, kaup, kande kood, arvesummad ja statistilised summad.</span><span class="sxs-lookup"><span data-stu-id="a22f5-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="a22f5-267">Vajaduse korral saate andmeid muuta.</span><span class="sxs-lookup"><span data-stu-id="a22f5-267">You can modify data if necessary.</span></span>  

