---
title: Loo müügipakkumised hulgi
description: See protseduur näitab, kuidas tõhusalt pakkumisi koostada, pakkudes mitmele kliendile toodete või teenuste komplekte.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1a9c7235f37ccdedc87ce70d3846443f645c0fe
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211878"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="05334-103">Loo müügipakkumised hulgi</span><span class="sxs-lookup"><span data-stu-id="05334-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="05334-104">See protseduur näitab, kuidas tõhusalt pakkumisi koostada, pakkudes mitmele kliendile toodete või teenuste komplekte.</span><span class="sxs-lookup"><span data-stu-id="05334-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="05334-105">Selle hulgipakkumise koostamine põhineb pakkumise mallidel.</span><span class="sxs-lookup"><span data-stu-id="05334-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="05334-106">Saate seda protseduuri käitada oma andmete või demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="05334-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="05334-107">Pakkumisemalli loomine</span><span class="sxs-lookup"><span data-stu-id="05334-107">Create a quotation template</span></span>
1. <span data-ttu-id="05334-108">Avage Müük ja turundus > Seadistamine > Hinnapakkumised > Malligrupid.</span><span class="sxs-lookup"><span data-stu-id="05334-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="05334-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="05334-109">Click New.</span></span>
3. <span data-ttu-id="05334-110">Tippige väljale Grupi ID oma valitud ID.</span><span class="sxs-lookup"><span data-stu-id="05334-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="05334-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="05334-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="05334-112">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="05334-112">Click Save.</span></span>
6. <span data-ttu-id="05334-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05334-113">Close the page.</span></span>
7. <span data-ttu-id="05334-114">Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.</span><span class="sxs-lookup"><span data-stu-id="05334-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="05334-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="05334-115">Click New.</span></span>
9. <span data-ttu-id="05334-116">Valige väljal Konto tüüp väärtus Klient.</span><span class="sxs-lookup"><span data-stu-id="05334-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="05334-117">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="05334-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="05334-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05334-118">Click OK.</span></span>
    * <span data-ttu-id="05334-119">Selleks, et hinnapakkumisest saaks mall, tuleb läbida hinnapakkumise päisel seadistusetapid.</span><span class="sxs-lookup"><span data-stu-id="05334-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="05334-120">Seda tuleb teha enne pakkumisse ridade lisamist.</span><span class="sxs-lookup"><span data-stu-id="05334-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="05334-121">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="05334-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="05334-122">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="05334-122">Click Change view.</span></span>
14. <span data-ttu-id="05334-123">Klõpsake suvandit Päisevaade.</span><span class="sxs-lookup"><span data-stu-id="05334-123">Click Header view.</span></span>
15. <span data-ttu-id="05334-124">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="05334-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="05334-125">Sisestage või valige väärtus väljal Grupi ID.</span><span class="sxs-lookup"><span data-stu-id="05334-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="05334-126">Sisestage väärtus väljale Malli nimi.</span><span class="sxs-lookup"><span data-stu-id="05334-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="05334-127">Tehke väljal Aktiivne valik Jah.</span><span class="sxs-lookup"><span data-stu-id="05334-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="05334-128">Uuele müügipakkumisele malli rakendamisel saab kasutada ainult aktiivseid malle.</span><span class="sxs-lookup"><span data-stu-id="05334-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="05334-129">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="05334-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="05334-130">Klõpsake suvandit Muuda vaadet.</span><span class="sxs-lookup"><span data-stu-id="05334-130">Click Change view.</span></span>
21. <span data-ttu-id="05334-131">Klõpsake suvandit Reavaade.</span><span class="sxs-lookup"><span data-stu-id="05334-131">Click Line view.</span></span>
22. <span data-ttu-id="05334-132">Valige või sisestage väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="05334-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="05334-133">Tippige väärtus väljale Kaup.</span><span class="sxs-lookup"><span data-stu-id="05334-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="05334-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05334-134">Close the page.</span></span>
25. <span data-ttu-id="05334-135">Sisestage arv väljale Allahindlusprotsent.</span><span class="sxs-lookup"><span data-stu-id="05334-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="05334-136">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="05334-136">Click Add line.</span></span>
27. <span data-ttu-id="05334-137">Valige või sisestage väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="05334-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="05334-138">Tippige väärtus väljale Kaup.</span><span class="sxs-lookup"><span data-stu-id="05334-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="05334-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05334-139">Close the page.</span></span>
30. <span data-ttu-id="05334-140">Sisestage väljale Ühiku hind uus hind või muutke olemasolevat hinda.</span><span class="sxs-lookup"><span data-stu-id="05334-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="05334-141">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="05334-141">Click Add line.</span></span>
32. <span data-ttu-id="05334-142">Valige või sisestage väärtus väljal Kaup.</span><span class="sxs-lookup"><span data-stu-id="05334-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="05334-143">Tippige väärtus väljale Kaup.</span><span class="sxs-lookup"><span data-stu-id="05334-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="05334-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05334-144">Close the page.</span></span>
35. <span data-ttu-id="05334-145">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="05334-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="05334-146">Sisestage number väljale Allahindlus.</span><span class="sxs-lookup"><span data-stu-id="05334-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="05334-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="05334-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="05334-148">Rakendage malli ühe pakkumise koostamiseks</span><span class="sxs-lookup"><span data-stu-id="05334-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="05334-149">Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.</span><span class="sxs-lookup"><span data-stu-id="05334-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="05334-150">Pange tähele, et äsja koostatud pakkumine on märgitud mallina.</span><span class="sxs-lookup"><span data-stu-id="05334-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="05334-151">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="05334-151">Click New.</span></span>
3. <span data-ttu-id="05334-152">Valige väljal Konto tüüp väärtus Klient.</span><span class="sxs-lookup"><span data-stu-id="05334-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="05334-153">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="05334-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="05334-154">Laiendage jaotist Mall.</span><span class="sxs-lookup"><span data-stu-id="05334-154">Expand the Template section.</span></span>
6. <span data-ttu-id="05334-155">Sisestage või valige väärtus väljal Grupi ID.</span><span class="sxs-lookup"><span data-stu-id="05334-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="05334-156">Sisestage või valige väärtus väljal Malli nimi.</span><span class="sxs-lookup"><span data-stu-id="05334-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="05334-157">Tehke väljal Arvutusmeetod valik Põhineb näidisväärtustel.</span><span class="sxs-lookup"><span data-stu-id="05334-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="05334-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05334-158">Click OK.</span></span>
    * <span data-ttu-id="05334-159">Uus pakkumine on nüüd koostatud, tuginedes malli andmetele ja tingimustele.</span><span class="sxs-lookup"><span data-stu-id="05334-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="05334-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05334-160">Close the page.</span></span>
11. <span data-ttu-id="05334-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="05334-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="05334-162">Rakendage malli hulgipakkumiste koostamiseks</span><span class="sxs-lookup"><span data-stu-id="05334-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="05334-163">Avage Müük ja turundus > Müügipakkumised > Pakkumise uuendamine > Pakkumiste hulgiloomine.</span><span class="sxs-lookup"><span data-stu-id="05334-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="05334-164">Valige väljal Konto tüüp väärtus Klient.</span><span class="sxs-lookup"><span data-stu-id="05334-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="05334-165">Sisestage või valige väärtus väljal Grupi ID.</span><span class="sxs-lookup"><span data-stu-id="05334-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="05334-166">Sisestage või valige väärtus väljal Malli nimi.</span><span class="sxs-lookup"><span data-stu-id="05334-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="05334-167">Tehke väljal Arvutusmeetod valik Põhineb näidisväärtustel.</span><span class="sxs-lookup"><span data-stu-id="05334-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="05334-168">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="05334-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="05334-169">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="05334-169">Click Filter.</span></span>
8. <span data-ttu-id="05334-170">Määrake väljal Kriteeriumid filter, mis hõlmab klientide hulka, keda soovite hulgipakkumise koostamisse kaasata.</span><span class="sxs-lookup"><span data-stu-id="05334-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="05334-171">Kasutage järgmist vormingut: Customer1..CustomerN.</span><span class="sxs-lookup"><span data-stu-id="05334-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="05334-172">Näiteks saab määrata filtriks US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="05334-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="05334-173">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05334-173">Click OK.</span></span>
10. <span data-ttu-id="05334-174">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05334-174">Click OK.</span></span>
11. <span data-ttu-id="05334-175">Avage Müük ja turundus > Müügipakkumised > Kõik hinnapakkumised.</span><span class="sxs-lookup"><span data-stu-id="05334-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="05334-176">Kontrollige, et pakkumised on koostatud valitud malli põhjal kõigile klientidele, kes on hulgiuuendamise protseduuris määratud.</span><span class="sxs-lookup"><span data-stu-id="05334-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

