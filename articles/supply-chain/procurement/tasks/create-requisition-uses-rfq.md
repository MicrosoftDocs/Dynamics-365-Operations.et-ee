---
title: Pakkumiskutset kasutava taotluse loomine
description: See juhend näitab, kuidas lisada ostutaotlusele pakkumiskutse protsessist hinda ja hankija teavet.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a9418b526f992008086f10ce78e95cb682bc164
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547395"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="e7182-103">Pakkumiskutset kasutava taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="e7182-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e7182-104">See juhend näitab, kuidas lisada ostutaotlusele pakkumiskutse protsessist hinda ja hankija teavet.</span><span class="sxs-lookup"><span data-stu-id="e7182-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="e7182-105">Selles juhendis olevat näidet saab kasutada demoandmete ettevõttes USMF ja kõigi etappide läbimiseks peate olema administraatorina sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="e7182-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="e7182-106">Selle juhendi ülesandeid täidavad tavaliselt hankespetsialistid.</span><span class="sxs-lookup"><span data-stu-id="e7182-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="e7182-107">Taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="e7182-107">Create a requisition</span></span>
1. <span data-ttu-id="e7182-108">Tehke valik Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused.</span><span class="sxs-lookup"><span data-stu-id="e7182-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="e7182-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e7182-109">Click New.</span></span>
3. <span data-ttu-id="e7182-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e7182-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="e7182-111">Sisestage kuupäev väljale Nõutav kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e7182-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="e7182-112">Sisestage kuupäev väljale Aruandluskuupäev.</span><span class="sxs-lookup"><span data-stu-id="e7182-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="e7182-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7182-113">Click OK.</span></span>
7. <span data-ttu-id="e7182-114">Valige või sisestage väärtus väljal Põhjus.</span><span class="sxs-lookup"><span data-stu-id="e7182-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="e7182-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="e7182-115">Click Add line.</span></span>
9. <span data-ttu-id="e7182-116">Valige väljalt Hankekategooria puult kategooria ja klõpsake siis nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7182-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="e7182-117">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="e7182-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="e7182-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="e7182-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="e7182-119">Sisestage või valige väärtus väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="e7182-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="e7182-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e7182-120">Click Save.</span></span>
14. <span data-ttu-id="e7182-121">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e7182-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="e7182-122">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="e7182-122">Click Submit.</span></span>
16. <span data-ttu-id="e7182-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7182-123">Close the page.</span></span>
17. <span data-ttu-id="e7182-124">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="e7182-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="e7182-125">Töövoo ülesande ümber määramine</span><span class="sxs-lookup"><span data-stu-id="e7182-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="e7182-126">Järgmine ülesanne on luua pakkumiskutse hankijatelt tootele pakkumiste saamiseks.</span><span class="sxs-lookup"><span data-stu-id="e7182-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="e7182-127">USMF-i demoandmetes seadistatakse taotluse töövoog reegliga, nii et kui hankijat pole valitud või kui ühiku hind on real 0, määratakse ülesanne konkreetsele töötajale, kes koostab pakkumiskutse.</span><span class="sxs-lookup"><span data-stu-id="e7182-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="e7182-128">Selle juhendiga jätkamiseks peate määrama selle ülesande ümber teisele kasutajale (endale).</span><span class="sxs-lookup"><span data-stu-id="e7182-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="e7182-129">Seda saate teha ainult siis, kui olete administraatorina sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="e7182-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="e7182-130">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e7182-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="e7182-131">Klõpsake valikut Kuva ajalugu.</span><span class="sxs-lookup"><span data-stu-id="e7182-131">Click View history.</span></span>
3. <span data-ttu-id="e7182-132">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="e7182-132">Refresh the page.</span></span>
4. <span data-ttu-id="e7182-133">Laiendage jaotist Jälgimise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e7182-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="e7182-134">Valige puult rida, mis algab sõnadega Rea töövoog aktiveeritud kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="e7182-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="e7182-135">Klõpsake valikut Kuva töövoo üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e7182-135">Click View workflow details.</span></span>
7. <span data-ttu-id="e7182-136">Laiendage jaotist Tööüksused.</span><span class="sxs-lookup"><span data-stu-id="e7182-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="e7182-137">Klõpsake käsku Määra uuesti.</span><span class="sxs-lookup"><span data-stu-id="e7182-137">Click Reassign.</span></span>
9. <span data-ttu-id="e7182-138">Tehke väljal Kasutaja valik Administraator.</span><span class="sxs-lookup"><span data-stu-id="e7182-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="e7182-139">Klõpsake käsku Määra uuesti.</span><span class="sxs-lookup"><span data-stu-id="e7182-139">Click Reassign.</span></span>
11. <span data-ttu-id="e7182-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7182-140">Close the page.</span></span>
12. <span data-ttu-id="e7182-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7182-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="e7182-142">Pakkumiskutse loomine</span><span class="sxs-lookup"><span data-stu-id="e7182-142">Create an RFQ</span></span>
1. <span data-ttu-id="e7182-143">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="e7182-143">Refresh the page.</span></span>
2. <span data-ttu-id="e7182-144">Klõpsake valikut Pakkumiskutse vastus.</span><span class="sxs-lookup"><span data-stu-id="e7182-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="e7182-145">Tehke väljal Ostev juriidiline isik valik USMF.</span><span class="sxs-lookup"><span data-stu-id="e7182-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="e7182-146">Peate valima sama juriidilise isiku, kes on taotluse real.</span><span class="sxs-lookup"><span data-stu-id="e7182-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="e7182-147">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e7182-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e7182-148">Kui ostutaotlusel oli mitu rida, valige kõik read, mida soovite pakkumiskutsesse lisada.</span><span class="sxs-lookup"><span data-stu-id="e7182-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="e7182-149">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7182-149">Click OK.</span></span>
6. <span data-ttu-id="e7182-150">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="e7182-150">Refresh the page.</span></span>
7. <span data-ttu-id="e7182-151">Avage kiirinfo ja laiendage siis jaotist Seotud dokumendid.</span><span class="sxs-lookup"><span data-stu-id="e7182-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="e7182-152">Teil võib kiirinfo juba lahti olla.</span><span class="sxs-lookup"><span data-stu-id="e7182-152">You may already have the FactBox open.</span></span> <span data-ttu-id="e7182-153">Otsige noolega ikooni nuppudest Read/päis paremal.</span><span class="sxs-lookup"><span data-stu-id="e7182-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="e7182-154">Kui nool osutab paremale, on kiirinfo juba avatud.</span><span class="sxs-lookup"><span data-stu-id="e7182-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="e7182-155">Kui nool osutab vasakule, klõpsake seda kiirinfo avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e7182-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="e7182-156">Klõpsake linki väljal Pakkumiskutse äsja loodud pakkumiskutse avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e7182-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="e7182-157">Klõpsake päist.</span><span class="sxs-lookup"><span data-stu-id="e7182-157">Click Header.</span></span>
10. <span data-ttu-id="e7182-158">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e7182-158">Click Add.</span></span>
11. <span data-ttu-id="e7182-159">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="e7182-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="e7182-160">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e7182-160">Click Add.</span></span>
13. <span data-ttu-id="e7182-161">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="e7182-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="e7182-162">Klõpsake käsku Saada.</span><span class="sxs-lookup"><span data-stu-id="e7182-162">Click Send.</span></span>
15. <span data-ttu-id="e7182-163">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7182-163">Click OK.</span></span>
16. <span data-ttu-id="e7182-164">Klõpsake nuppu Sisesta vastus.</span><span class="sxs-lookup"><span data-stu-id="e7182-164">Click Enter reply.</span></span>
17. <span data-ttu-id="e7182-165">Klõpsake toimingupaanil käsku Vasta.</span><span class="sxs-lookup"><span data-stu-id="e7182-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="e7182-166">Klõpsake käsku Kopeeri andmed vastuseväljadele.</span><span class="sxs-lookup"><span data-stu-id="e7182-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="e7182-167">Sellega kopeeritakse andmed nagu kogus ja kuupäevad pakkumiskutselt vastusele.</span><span class="sxs-lookup"><span data-stu-id="e7182-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="e7182-168">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="e7182-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="e7182-169">See on hind, mille hankijalt saite.</span><span class="sxs-lookup"><span data-stu-id="e7182-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="e7182-170">Teil võib olla vaja sisestada ka hankijalt saadud lisateavet.</span><span class="sxs-lookup"><span data-stu-id="e7182-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="e7182-171">Klõpsake suvandit Nõustu.</span><span class="sxs-lookup"><span data-stu-id="e7182-171">Click Accept.</span></span>
21. <span data-ttu-id="e7182-172">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e7182-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="e7182-173">Veenduge, et hankija ja hind oleksid taotlusele üle viidud</span><span class="sxs-lookup"><span data-stu-id="e7182-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="e7182-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7182-174">Close the page.</span></span>
2. <span data-ttu-id="e7182-175">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="e7182-175">Click Lines.</span></span>
3. <span data-ttu-id="e7182-176">Klõpsake valikut Seostuv teave.</span><span class="sxs-lookup"><span data-stu-id="e7182-176">Click Related information.</span></span>
4. <span data-ttu-id="e7182-177">Klõpsake valikut Ostutaotlus.</span><span class="sxs-lookup"><span data-stu-id="e7182-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="e7182-178">Valige rida, mis pakkumiskutsele üle viidi.</span><span class="sxs-lookup"><span data-stu-id="e7182-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="e7182-179">Veenduge, et hind ja hankija oleksid taotlusele kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="e7182-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="e7182-180">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="e7182-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="e7182-181">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="e7182-181">Click Complete.</span></span>
8. <span data-ttu-id="e7182-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7182-182">Close the page.</span></span>
9. <span data-ttu-id="e7182-183">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="e7182-183">Click Complete.</span></span>

