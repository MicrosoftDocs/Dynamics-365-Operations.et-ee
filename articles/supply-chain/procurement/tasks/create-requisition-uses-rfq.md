--- 
title: Pakkumiskutset kasutava taotluse loomine
description: "See juhend näitab, kuidas lisada ostutaotlusele pakkumiskutse protsessist hinda ja hankija teavet."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2c2daad961ec5c47ca49b2e53a2118570caf6a58
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="51a69-103">Pakkumiskutset kasutava taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="51a69-103">Create a requisition that uses an RFQ</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51a69-104">See juhend näitab, kuidas lisada ostutaotlusele pakkumiskutse protsessist hinda ja hankija teavet.</span><span class="sxs-lookup"><span data-stu-id="51a69-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="51a69-105">Selles juhendis olevat näidet saab kasutada demoandmete ettevõttes USMF ja kõigi etappide läbimiseks peate olema administraatorina sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="51a69-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="51a69-106">Selle juhendi ülesandeid täidavad tavaliselt hankespetsialistid.</span><span class="sxs-lookup"><span data-stu-id="51a69-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="51a69-107">Taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="51a69-107">Create a requisition</span></span>
1. <span data-ttu-id="51a69-108">Tehke valik Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused.</span><span class="sxs-lookup"><span data-stu-id="51a69-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="51a69-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="51a69-109">Click New.</span></span>
3. <span data-ttu-id="51a69-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="51a69-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="51a69-111">Sisestage kuupäev väljale Nõutav kuupäev.</span><span class="sxs-lookup"><span data-stu-id="51a69-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="51a69-112">Sisestage kuupäev väljale Aruandluskuupäev.</span><span class="sxs-lookup"><span data-stu-id="51a69-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="51a69-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="51a69-113">Click OK.</span></span>
7. <span data-ttu-id="51a69-114">Valige või sisestage väärtus väljal Põhjus.</span><span class="sxs-lookup"><span data-stu-id="51a69-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="51a69-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="51a69-115">Click Add line.</span></span>
9. <span data-ttu-id="51a69-116">Valige väljalt Hankekategooria puult kategooria ja klõpsake siis nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="51a69-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="51a69-117">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="51a69-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="51a69-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="51a69-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="51a69-119">Sisestage või valige väärtus väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="51a69-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="51a69-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="51a69-120">Click Save.</span></span>
14. <span data-ttu-id="51a69-121">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="51a69-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="51a69-122">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="51a69-122">Click Submit.</span></span>
16. <span data-ttu-id="51a69-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51a69-123">Close the page.</span></span>
17. <span data-ttu-id="51a69-124">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="51a69-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="51a69-125">Töövoo ülesande ümber määramine</span><span class="sxs-lookup"><span data-stu-id="51a69-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="51a69-126">Järgmine ülesanne on luua pakkumiskutse hankijatelt tootele pakkumiste saamiseks.</span><span class="sxs-lookup"><span data-stu-id="51a69-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="51a69-127">USMF-i demoandmetes seadistatakse taotluse töövoog reegliga, nii et kui hankijat pole valitud või kui ühiku hind on real 0, määratakse ülesanne konkreetsele töötajale, kes koostab pakkumiskutse.</span><span class="sxs-lookup"><span data-stu-id="51a69-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="51a69-128">Selle juhendiga jätkamiseks peate määrama selle ülesande ümber teisele kasutajale (endale).</span><span class="sxs-lookup"><span data-stu-id="51a69-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="51a69-129">Seda saate teha ainult siis, kui olete administraatorina sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="51a69-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="51a69-130">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="51a69-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="51a69-131">Klõpsake valikut Kuva ajalugu.</span><span class="sxs-lookup"><span data-stu-id="51a69-131">Click View history.</span></span>
3. <span data-ttu-id="51a69-132">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="51a69-132">Refresh the page.</span></span>
4. <span data-ttu-id="51a69-133">Laiendage jaotist Jälgimise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="51a69-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="51a69-134">Valige puult rida, mis algab sõnadega Rea töövoog aktiveeritud kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="51a69-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="51a69-135">Klõpsake valikut Kuva töövoo üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="51a69-135">Click View workflow details.</span></span>
7. <span data-ttu-id="51a69-136">Laiendage jaotist Tööüksused.</span><span class="sxs-lookup"><span data-stu-id="51a69-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="51a69-137">Klõpsake käsku Määra uuesti.</span><span class="sxs-lookup"><span data-stu-id="51a69-137">Click Reassign.</span></span>
9. <span data-ttu-id="51a69-138">Tehke väljal Kasutaja valik Administraator.</span><span class="sxs-lookup"><span data-stu-id="51a69-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="51a69-139">Klõpsake käsku Määra uuesti.</span><span class="sxs-lookup"><span data-stu-id="51a69-139">Click Reassign.</span></span>
11. <span data-ttu-id="51a69-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51a69-140">Close the page.</span></span>
12. <span data-ttu-id="51a69-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51a69-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="51a69-142">Pakkumiskutse loomine</span><span class="sxs-lookup"><span data-stu-id="51a69-142">Create an RFQ</span></span>
1. <span data-ttu-id="51a69-143">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="51a69-143">Refresh the page.</span></span>
2. <span data-ttu-id="51a69-144">Klõpsake valikut Pakkumiskutse vastus.</span><span class="sxs-lookup"><span data-stu-id="51a69-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="51a69-145">Tehke väljal Ostev juriidiline isik valik USMF.</span><span class="sxs-lookup"><span data-stu-id="51a69-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="51a69-146">Peate valima sama juriidilise isiku, kes on taotluse real.</span><span class="sxs-lookup"><span data-stu-id="51a69-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="51a69-147">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="51a69-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="51a69-148">Kui ostutaotlusel oli mitu rida, valige kõik read, mida soovite pakkumiskutsesse lisada.</span><span class="sxs-lookup"><span data-stu-id="51a69-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="51a69-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="51a69-149">Click OK.</span></span>
6. <span data-ttu-id="51a69-150">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="51a69-150">Refresh the page.</span></span>
7. <span data-ttu-id="51a69-151">Avage kiirinfo ja laiendage siis jaotist Seotud dokumendid.</span><span class="sxs-lookup"><span data-stu-id="51a69-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="51a69-152">Teil võib kiirinfo juba lahti olla.</span><span class="sxs-lookup"><span data-stu-id="51a69-152">You may already have the FactBox open.</span></span> <span data-ttu-id="51a69-153">Otsige noolega ikooni nuppudest Read/päis paremal.</span><span class="sxs-lookup"><span data-stu-id="51a69-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="51a69-154">Kui nool osutab paremale, on kiirinfo juba avatud.</span><span class="sxs-lookup"><span data-stu-id="51a69-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="51a69-155">Kui nool osutab vasakule, klõpsake seda kiirinfo avamiseks.</span><span class="sxs-lookup"><span data-stu-id="51a69-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="51a69-156">Klõpsake linki väljal Pakkumiskutse äsja loodud pakkumiskutse avamiseks.</span><span class="sxs-lookup"><span data-stu-id="51a69-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="51a69-157">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="51a69-157">Click Header.</span></span>
10. <span data-ttu-id="51a69-158">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="51a69-158">Click Add.</span></span>
11. <span data-ttu-id="51a69-159">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="51a69-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="51a69-160">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="51a69-160">Click Add.</span></span>
13. <span data-ttu-id="51a69-161">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="51a69-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="51a69-162">Klõpsake käsku Saada.</span><span class="sxs-lookup"><span data-stu-id="51a69-162">Click Send.</span></span>
15. <span data-ttu-id="51a69-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="51a69-163">Click OK.</span></span>
16. <span data-ttu-id="51a69-164">Klõpsake nuppu Sisesta vastus.</span><span class="sxs-lookup"><span data-stu-id="51a69-164">Click Enter reply.</span></span>
17. <span data-ttu-id="51a69-165">Klõpsake toimingupaanil käsku Vasta.</span><span class="sxs-lookup"><span data-stu-id="51a69-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="51a69-166">Klõpsake käsku Kopeeri andmed vastuseväljadele.</span><span class="sxs-lookup"><span data-stu-id="51a69-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="51a69-167">Sellega kopeeritakse andmed nagu kogus ja kuupäevad pakkumiskutselt vastusele.</span><span class="sxs-lookup"><span data-stu-id="51a69-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="51a69-168">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="51a69-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="51a69-169">See on hind, mille hankijalt saite.</span><span class="sxs-lookup"><span data-stu-id="51a69-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="51a69-170">Teil võib olla vaja sisestada ka hankijalt saadud lisateavet.</span><span class="sxs-lookup"><span data-stu-id="51a69-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="51a69-171">Klõpsake suvandit Nõustu.</span><span class="sxs-lookup"><span data-stu-id="51a69-171">Click Accept.</span></span>
21. <span data-ttu-id="51a69-172">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="51a69-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="51a69-173">Veenduge, et hankija ja hind oleksid taotlusele üle viidud</span><span class="sxs-lookup"><span data-stu-id="51a69-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="51a69-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51a69-174">Close the page.</span></span>
2. <span data-ttu-id="51a69-175">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="51a69-175">Click Lines.</span></span>
3. <span data-ttu-id="51a69-176">Klõpsake valikut Seostuv teave.</span><span class="sxs-lookup"><span data-stu-id="51a69-176">Click Related information.</span></span>
4. <span data-ttu-id="51a69-177">Klõpsake valikut Ostutaotlus.</span><span class="sxs-lookup"><span data-stu-id="51a69-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="51a69-178">Valige rida, mis pakkumiskutsele üle viidi.</span><span class="sxs-lookup"><span data-stu-id="51a69-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="51a69-179">Veenduge, et hind ja hankija oleksid taotlusele kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="51a69-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="51a69-180">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="51a69-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="51a69-181">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="51a69-181">Click Complete.</span></span>
8. <span data-ttu-id="51a69-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51a69-182">Close the page.</span></span>
9. <span data-ttu-id="51a69-183">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="51a69-183">Click Complete.</span></span>


