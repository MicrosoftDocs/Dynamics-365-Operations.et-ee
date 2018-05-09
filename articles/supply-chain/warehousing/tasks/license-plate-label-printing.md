--- 
title: "Registreerimismärgi sildi printimise lubamine"
description: "Kui müügi komplekteerimise tööprotsessis on viimane kaup varudest valitud, lubab see protseduur konteineri seeriaviisi lähetamise koodi (SSCC) sildi automaatse printimise."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0c0515d61f651b9244525fc20c242f3d31eb3a20
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="f9cde-103">Registreerimismärgi sildi printimise lubamine</span><span class="sxs-lookup"><span data-stu-id="f9cde-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9cde-104">Kui müügi komplekteerimise tööprotsessis on viimane kaup varudest valitud, lubab see protseduur konteineri seeriaviisi lähetamise koodi (SSCC) sildi automaatse printimise.</span><span class="sxs-lookup"><span data-stu-id="f9cde-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="f9cde-105">Võite seda protseduuri käitada demoettevõtte USMF-i andmetega.</span><span class="sxs-lookup"><span data-stu-id="f9cde-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="f9cde-106">Kui käitate seda omaenda andmeid kasutades, peaksite määrama litsentsiplaatide numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="f9cde-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="f9cde-107">Enne ülesande juurde asumist peaksite määrama sildiprinteri.</span><span class="sxs-lookup"><span data-stu-id="f9cde-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="f9cde-108">Avage Organisatsiooni haldus > Seadistus > Võrguprinterid.</span><span class="sxs-lookup"><span data-stu-id="f9cde-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="f9cde-109">Klõpsake toimingupaanil Suvandid, seejärel klõpsake nuppu Laadi dokumendi marsruudivaliku agendi installer alla.</span><span class="sxs-lookup"><span data-stu-id="f9cde-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="f9cde-110">Käitage installer ja veenduge enne protseduuriga jätkamist, et töötav võrguprinter on seatud olekusse Aktiivne.</span><span class="sxs-lookup"><span data-stu-id="f9cde-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="f9cde-111">GS1 ettevõtteprefiksi seadistus</span><span class="sxs-lookup"><span data-stu-id="f9cde-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="f9cde-112">Avage Laohaldus > Seadistus > Laohalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f9cde-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="f9cde-113">Sisestage väljale GS1 ettevõtteprefiks GS1 ettevõtte koodi 7 numbrit.</span><span class="sxs-lookup"><span data-stu-id="f9cde-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="f9cde-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-114">Click Save.</span></span>
4. <span data-ttu-id="f9cde-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="f9cde-116">SSCC-identifitseerimisnumbri numbriseeria seadistus</span><span class="sxs-lookup"><span data-stu-id="f9cde-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="f9cde-117">Avage Organisatsiooni haldus > Numbriseeriad > Numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="f9cde-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="f9cde-118">Valige suvand väljal Ala.</span><span class="sxs-lookup"><span data-stu-id="f9cde-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="f9cde-119">Valige suvand väljal Viide.</span><span class="sxs-lookup"><span data-stu-id="f9cde-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="f9cde-120">Sisestage väärtus väljale Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="f9cde-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="f9cde-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f9cde-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f9cde-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f9cde-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f9cde-123">Laiendage jaotist Segmendid.</span><span class="sxs-lookup"><span data-stu-id="f9cde-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="f9cde-124">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f9cde-124">Click Edit.</span></span>
9. <span data-ttu-id="f9cde-125">Valige tabelist Segmendid esimene rida.</span><span class="sxs-lookup"><span data-stu-id="f9cde-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="f9cde-126">Klõpsake nuppu Eemalda.</span><span class="sxs-lookup"><span data-stu-id="f9cde-126">Click Remove.</span></span>
11. <span data-ttu-id="f9cde-127">Klõpsake nuppu Eemalda.</span><span class="sxs-lookup"><span data-stu-id="f9cde-127">Click Remove.</span></span>
12. <span data-ttu-id="f9cde-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-128">Click Save.</span></span>
13. <span data-ttu-id="f9cde-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="f9cde-130">Dokumendi marsruudivaliku paigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="f9cde-130">Create the document route layout</span></span>
1. <span data-ttu-id="f9cde-131">Avage Laohaldus > Seadistus > Dokumendi marsruudivalik > Dokumendi marsruudivaliku paigutused.</span><span class="sxs-lookup"><span data-stu-id="f9cde-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="f9cde-132">Saate lubada SSCC-paigutuse.</span><span class="sxs-lookup"><span data-stu-id="f9cde-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="f9cde-133">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-133">Click New.</span></span>
3. <span data-ttu-id="f9cde-134">Sisestage väärtus väljale Paigutuse ID.</span><span class="sxs-lookup"><span data-stu-id="f9cde-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="f9cde-135">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f9cde-136">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f9cde-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="f9cde-137">Klõpsake Lisa teksti lõppu.</span><span class="sxs-lookup"><span data-stu-id="f9cde-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="f9cde-138">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-138">Click Save.</span></span>
8. <span data-ttu-id="f9cde-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="f9cde-140">Dokumendi marsruudivaliku häälestamine</span><span class="sxs-lookup"><span data-stu-id="f9cde-140">Set up the document routing</span></span>
1. <span data-ttu-id="f9cde-141">Avage Laohaldus > Seadistus > Dokumendi marsruudivalik > Dokumendi marsruudivalik.</span><span class="sxs-lookup"><span data-stu-id="f9cde-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="f9cde-142">Valige suvand väljal Töökäsu tüüp.</span><span class="sxs-lookup"><span data-stu-id="f9cde-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="f9cde-143">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-143">Click New.</span></span>
4. <span data-ttu-id="f9cde-144">Sisestage väärtus väljale Ladu.</span><span class="sxs-lookup"><span data-stu-id="f9cde-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="f9cde-145">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f9cde-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="f9cde-146">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-146">Click New.</span></span>
7. <span data-ttu-id="f9cde-147">Sisestage või valige väärtus väljal Paigutuse ID.</span><span class="sxs-lookup"><span data-stu-id="f9cde-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="f9cde-148">Sisestage väljale Nimi printeri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="f9cde-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="f9cde-149">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-149">Click Save.</span></span>
10. <span data-ttu-id="f9cde-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="f9cde-151">Mobiilse seadme menüü loomine</span><span class="sxs-lookup"><span data-stu-id="f9cde-151">Create mobile device menu</span></span>
1. <span data-ttu-id="f9cde-152">Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü-üksused.</span><span class="sxs-lookup"><span data-stu-id="f9cde-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="f9cde-153">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-153">Click New.</span></span>
3. <span data-ttu-id="f9cde-154">Sisestage väärtus väljale Menüü-üksuse nimi.</span><span class="sxs-lookup"><span data-stu-id="f9cde-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="f9cde-155">Sisestage väärtus väljale Pealkiri.</span><span class="sxs-lookup"><span data-stu-id="f9cde-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="f9cde-156">Valige suvand väljal Režiim.</span><span class="sxs-lookup"><span data-stu-id="f9cde-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="f9cde-157">Valige suvand Jah väljal Kasuta olemasolevat tööd.</span><span class="sxs-lookup"><span data-stu-id="f9cde-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="f9cde-158">Valige suvand Jah väljal Loo litsentsiplaat.</span><span class="sxs-lookup"><span data-stu-id="f9cde-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="f9cde-159">Laiendage jaotist Tööklassid.</span><span class="sxs-lookup"><span data-stu-id="f9cde-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="f9cde-160">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-160">Click New.</span></span>
10. <span data-ttu-id="f9cde-161">Sisestage väärtus väljale Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="f9cde-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="f9cde-162">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-162">Click Save.</span></span>
12. <span data-ttu-id="f9cde-163">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-163">Close the page.</span></span>
13. <span data-ttu-id="f9cde-164">Avage Laohaldus > Seadistus > Mobiilne seade > Mobiilse seadme menüü.</span><span class="sxs-lookup"><span data-stu-id="f9cde-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="f9cde-165">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f9cde-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f9cde-166">Valige puul Vali puul varem loodud menüü-üksus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="f9cde-167">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f9cde-167">Click Edit.</span></span>
17. <span data-ttu-id="f9cde-168">Menüü-üksuse menüüsse lisamiseks klõpsake noolel.</span><span class="sxs-lookup"><span data-stu-id="f9cde-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="f9cde-169">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-169">Click Save.</span></span>
19. <span data-ttu-id="f9cde-170">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="f9cde-171">Töömalli värskendus</span><span class="sxs-lookup"><span data-stu-id="f9cde-171">Update a work template</span></span>
1. <span data-ttu-id="f9cde-172">Avage Laohaldus > Seadistus > Töö > Töömallid.</span><span class="sxs-lookup"><span data-stu-id="f9cde-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="f9cde-173">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f9cde-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f9cde-174">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="f9cde-174">Click Edit.</span></span>
4. <span data-ttu-id="f9cde-175">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f9cde-175">Click New.</span></span>
5. <span data-ttu-id="f9cde-176">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f9cde-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="f9cde-177">Valige Prindi väljal Töö tüüp.</span><span class="sxs-lookup"><span data-stu-id="f9cde-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="f9cde-178">Sisestage või valige väärtus väljal Tööklassi ID.</span><span class="sxs-lookup"><span data-stu-id="f9cde-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="f9cde-179">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f9cde-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="f9cde-180">Klõpsake nuppu Ülespoole.</span><span class="sxs-lookup"><span data-stu-id="f9cde-180">Click Move up.</span></span>
10. <span data-ttu-id="f9cde-181">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f9cde-181">Click Save.</span></span>
11. <span data-ttu-id="f9cde-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f9cde-182">Close the page.</span></span>


