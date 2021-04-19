---
title: Pakkumiskutset kasutava taotluse loomine
description: Selles teemas selgitatakse, kuidas lisada hinda ja hankija teavet pakkumiskutselt ostutaotlusele.
author: kamaybac
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqLineRelatedDocuments, EcoResCategorySingleLookup, PurchReqWorkflowDropDialog, WorkflowSubmitDialog, WorkflowStatus, WorkflowWorkItemActionDialog, WorkflowUserListLookup, PurchReqCopyRFQ, SysDataAreaSelectLookup, PurchRFQCaseTable, PurchRFQEditLines, PurchRFQReplyTable, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6083afe0e2bfafd337d572863a198330e8cb6cc8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812129"
---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="f7d1f-103">Pakkumiskutset kasutava taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="f7d1f-103">Create a requisition that uses an RFQ</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f7d1f-104">Selles teemas selgitatakse, kuidas lisada hinda ja hankija teavet pakkumiskutselt ostutaotlusele.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-104">This topic explains how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="f7d1f-105">Selles juhendis olevat näidet saab kasutada demoandmete ettevõttes USMF ja kõigi etappide läbimiseks peate olema administraatorina sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="f7d1f-106">Selle juhendi ülesandeid täidavad tavaliselt hankespetsialistid.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="f7d1f-107">Taotluse loomine</span><span class="sxs-lookup"><span data-stu-id="f7d1f-107">Create a requisition</span></span>
1. <span data-ttu-id="f7d1f-108">Navigeerimispaanil avage **Moodulid > Hanked > Ostutaotlused > Minu ettevalmistatud ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-108">In the navigation pane, go to **Modules > Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me**.</span></span>
2. <span data-ttu-id="f7d1f-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-109">Select **New**.</span></span>
3. <span data-ttu-id="f7d1f-110">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-110">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f7d1f-111">**Sisestage kuupäev väljale Nõutav kuupäev.**</span><span class="sxs-lookup"><span data-stu-id="f7d1f-111">In the **Requested date** field, enter a date.</span></span>
5. <span data-ttu-id="f7d1f-112">Sisestage kuupäev väljale **Aruandluskuupäev.**</span><span class="sxs-lookup"><span data-stu-id="f7d1f-112">In the **Accounting date** field, enter a date.</span></span>
6. <span data-ttu-id="f7d1f-113">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-113">Select **OK**.</span></span>
7. <span data-ttu-id="f7d1f-114">Väljale **Põhjus** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-114">In the **Reason** field, enter or select a value.</span></span>
8. <span data-ttu-id="f7d1f-115">Valige **Lisa rida**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-115">Select **Add line**.</span></span>
9. <span data-ttu-id="f7d1f-116">Väljal **Hankekategooria** valige puust kategooria ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-116">In the **Procurement category** field, select a category in the tree, and then select **OK**.</span></span>
10. <span data-ttu-id="f7d1f-117">Sisestage väärtus väljale **Toote nimi**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-117">In the **Product name** field, type a value.</span></span>
11. <span data-ttu-id="f7d1f-118">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-118">In the **Quantity** field, enter a number.</span></span>
12. <span data-ttu-id="f7d1f-119">Sisestage või valige väärtus väljal **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-119">In the **Unit** field, enter or select a value.</span></span>
13. <span data-ttu-id="f7d1f-120">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-120">Select **Save**.</span></span>
14. <span data-ttu-id="f7d1f-121">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-121">Select **Workflow** to open the drop dialog.</span></span>
15. <span data-ttu-id="f7d1f-122">Valige käsk **Esita**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-122">Select **Submit**.</span></span>
16. <span data-ttu-id="f7d1f-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-123">Close the page.</span></span>
17. <span data-ttu-id="f7d1f-124">Valige käsk **Esita**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-124">Select **Submit**.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="f7d1f-125">Töövoo ülesande ümber määramine</span><span class="sxs-lookup"><span data-stu-id="f7d1f-125">Reassign a workflow task</span></span>
<span data-ttu-id="f7d1f-126">Järgmine ülesanne on luua pakkumiskutse hankijatelt tootele pakkumiste saamiseks.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="f7d1f-127">USMF-i demoandmetes seadistatakse taotluse töövoog reegliga, nii et kui hankijat pole valitud või kui ühiku hind on real 0, määratakse ülesanne konkreetsele töötajale, kes koostab pakkumiskutse.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="f7d1f-128">Selle juhendiga jätkamiseks peate määrama selle ülesande ümber teisele kasutajale (endale).</span><span class="sxs-lookup"><span data-stu-id="f7d1f-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="f7d1f-129">Seda saate teha ainult siis, kui olete administraatorina sisse loginud.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-129">You can only do this if you are logged in as an Admin.</span></span>  

1. <span data-ttu-id="f7d1f-130">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-130">Select **Workflow** to open the drop dialog.</span></span>
2. <span data-ttu-id="f7d1f-131">Valige **Kuva ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-131">Select **View history**.</span></span>
3. <span data-ttu-id="f7d1f-132">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-132">Refresh the page.</span></span>
4. <span data-ttu-id="f7d1f-133">Laiendage jaotist **Jälgimise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-133">Expand the **Tracking details** section.</span></span>
5. <span data-ttu-id="f7d1f-134">Valige puust rida, mille alguseks on „Rea töövoog aktiveeritud”.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-134">In the tree, select the line that starts with "Line workflow activated on".</span></span>
6. <span data-ttu-id="f7d1f-135">Valige **Kuva töövoo üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-135">Select **View workflow details**.</span></span>
7. <span data-ttu-id="f7d1f-136">Laiendage jaotist **Tööüksused**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-136">Expand the **Work items** section.</span></span>
8. <span data-ttu-id="f7d1f-137">Valige käsk **Määra ümber**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-137">Select **Reassign**.</span></span>
9. <span data-ttu-id="f7d1f-138">Väljal **Kasutaja** valige **Administraator**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-138">In the **User** field, select **Admin**.</span></span>
10. <span data-ttu-id="f7d1f-139">Valige käsk **Määra ümber**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-139">Select **Reassign**.</span></span>
11. <span data-ttu-id="f7d1f-140">Sulgege kaks lehte.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-140">Close the two pages.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="f7d1f-141">Pakkumiskutse loomine</span><span class="sxs-lookup"><span data-stu-id="f7d1f-141">Create an RFQ</span></span>

1. <span data-ttu-id="f7d1f-142">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-142">Refresh the page.</span></span>
2. <span data-ttu-id="f7d1f-143">Valige **Pakkumiskutse**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-143">Select **Request for quotation**.</span></span>
3. <span data-ttu-id="f7d1f-144">Väljal **Ostev juriidiline isik** valige **USMF**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-144">In the **Buying legal entity** field, select **USMF**.</span></span> <span data-ttu-id="f7d1f-145">Peate valima sama juriidilise isiku, kes on taotluse real.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-145">You must select the same legal entity that's on the requisition line.</span></span>  
4. <span data-ttu-id="f7d1f-146">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-146">In the list, mark the selected row.</span></span> <span data-ttu-id="f7d1f-147">Kui ostutaotlusel oli mitu rida, valige kõik read, mida soovite pakkumiskutsesse lisada.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-147">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="f7d1f-148">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-148">Select **OK**.</span></span>
6. <span data-ttu-id="f7d1f-149">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-149">Refresh the page.</span></span>
7. <span data-ttu-id="f7d1f-150">Veenduge, et kiirinfo on avatud, seejärel laiendage jaotist **Seotud dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-150">Ensure that the FactBox is open, then expand the **Related documents** section.</span></span>
8. <span data-ttu-id="f7d1f-151">Valige link väljal **Pakkumiskutse**, et avada äsja loodud pakkumiskutse.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-151">Select the link in the **Request for quotation** field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="f7d1f-152">Valige **Päis**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-152">Select **Header**.</span></span>
10. <span data-ttu-id="f7d1f-153">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-153">Select **Add**.</span></span>
11. <span data-ttu-id="f7d1f-154">Sisestage või valige väärtus väljale **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-154">In the **Vendor account** field, enter or select a value.</span></span>
12. <span data-ttu-id="f7d1f-155">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-155">Select **Add**.</span></span>
13. <span data-ttu-id="f7d1f-156">Sisestage või valige väärtus väljale **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-156">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="f7d1f-157">Valige **Saada**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-157">Select **Send**.</span></span>
15. <span data-ttu-id="f7d1f-158">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-158">Select **OK**.</span></span>
16. <span data-ttu-id="f7d1f-159">Valige **Sisesta vastus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-159">Select **Enter reply**.</span></span>
17. <span data-ttu-id="f7d1f-160">Toimingupaanil valige käsk **Vasta**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-160">On the Action Pane, select **Reply**.</span></span>
18. <span data-ttu-id="f7d1f-161">Valige **Kopeeri andmed vastuseväljadele**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-161">Select **Copy data to reply**.</span></span> <span data-ttu-id="f7d1f-162">Sellega kopeeritakse andmed nagu kogus ja kuupäevad pakkumiskutselt vastusele.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-162">This copies data, such as the quantity and dates, from the RFQ to the reply.</span></span>  
19. <span data-ttu-id="f7d1f-163">Sisestage arv väljale **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-163">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="f7d1f-164">See on hind, mille hankijalt saite.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-164">This is the price that you've received from the vendor.</span></span> <span data-ttu-id="f7d1f-165">Teil võib olla vaja sisestada ka hankijalt saadud lisateavet.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-165">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="f7d1f-166">Valige **Aktsepteerimine**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-166">Select **Accept**.</span></span>
21. <span data-ttu-id="f7d1f-167">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-167">Select **OK**.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="f7d1f-168">Veenduge, et hankija ja hind oleksid taotlusele üle viidud</span><span class="sxs-lookup"><span data-stu-id="f7d1f-168">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="f7d1f-169">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-169">Close the page.</span></span>
2. <span data-ttu-id="f7d1f-170">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-170">Select **Lines**.</span></span>
3. <span data-ttu-id="f7d1f-171">Valige **Seotud teave**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-171">Select **Related information**.</span></span>
4. <span data-ttu-id="f7d1f-172">Valige **Ostutaotlus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-172">Select **Purchase requisition**.</span></span>
5. <span data-ttu-id="f7d1f-173">Valige rida, mis pakkumiskutsele üle viidi.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-173">Select the line that was transferred to the RFQ.</span></span> <span data-ttu-id="f7d1f-174">Veenduge, et hind ja hankija oleksid taotlusele kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-174">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="f7d1f-175">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-175">Select **Workflow** to open the drop dialog.</span></span>
7. <span data-ttu-id="f7d1f-176">Valige Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-176">Select Complete.</span></span>
8. <span data-ttu-id="f7d1f-177">Valige leht.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-177">Select the page.</span></span>
9. <span data-ttu-id="f7d1f-178">Valige Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="f7d1f-178">Select Complete.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]