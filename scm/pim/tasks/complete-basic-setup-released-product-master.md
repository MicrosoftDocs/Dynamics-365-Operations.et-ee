--- 
title: "Vabastatud tooteetaloni täielik põhiseadistus"
description: See protseduur selgitab, kuidas teha miinimumseadistust, mis on vajalik enne tooteetaloni kasutamist koosluse versioonides.
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: c42476ca3ffee41e303457150ef15da0f5af8a8f
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="48404-103">Vabastatud tooteetaloni täielik põhiseadistus</span><span class="sxs-lookup"><span data-stu-id="48404-103">Complete basic setup of a released product master</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48404-104">See protseduur selgitab, kuidas teha miinimumseadistust, mis on vajalik enne tooteetaloni kasutamist koosluse versioonides.</span><span class="sxs-lookup"><span data-stu-id="48404-104">This procedure shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="48404-105">See on kolmas protseduur kaheksast, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="48404-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="48404-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="48404-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="48404-107">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="48404-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="48404-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="48404-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48404-109">Valige teises protseduuris väljastatud tooteetalon.</span><span class="sxs-lookup"><span data-stu-id="48404-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="48404-110">Selle tooteetalon on loodud dimensioonipõhine konfiguratsioonitehnoloogia abil.</span><span class="sxs-lookup"><span data-stu-id="48404-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="48404-111">Klõpsake toimingupaanil suvandit Toode.</span><span class="sxs-lookup"><span data-stu-id="48404-111">On the Action Pane, click Product.</span></span>
4. <span data-ttu-id="48404-112">Klõpsake rippdialoogi avamiseks suvandit Dimensioonigrupid.</span><span class="sxs-lookup"><span data-stu-id="48404-112">Click Dimension groups to open the drop dialog.</span></span>
5. <span data-ttu-id="48404-113">Klõpsake väljal Laoala dimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="48404-113">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="48404-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="48404-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48404-115">Laoala dimensioonigrupp määratleb, milliseid laoala dimensioone toote kande puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="48404-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="48404-116">Valige selle protseduuri puhul suvand Protseduur.</span><span class="sxs-lookup"><span data-stu-id="48404-116">Select Site for this procedure.</span></span>  
7. <span data-ttu-id="48404-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="48404-117">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="48404-118">Klõpsake väljal Jälgimisdimensiooni grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="48404-118">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="48404-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="48404-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48404-120">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone toote kande puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="48404-120">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="48404-121">Valige selle protseduuri puhul suvand Puudub.</span><span class="sxs-lookup"><span data-stu-id="48404-121">Select None for this procedure.</span></span>  
10. <span data-ttu-id="48404-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="48404-122">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="48404-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="48404-123">Click OK.</span></span>
12. <span data-ttu-id="48404-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="48404-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="48404-125">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="48404-125">Click Edit.</span></span>
    * <span data-ttu-id="48404-126">Seadistusülesande jätkamiseks avage vorm Väljastatud toote üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="48404-126">Open the Released product details form to continue the setup task.</span></span>  
14. <span data-ttu-id="48404-127">Klõpsake väljal Kauba mudeligrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="48404-127">In the Item model group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="48404-128">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="48404-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48404-129">Kaubamudeligrupid sisaldavad sätteid, mis määratlevad, kuidas kaupu sissetulekutel ja väljaminekutel kontrollitakse ning käsitletakse.</span><span class="sxs-lookup"><span data-stu-id="48404-129">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="48404-130">Need määravad ka selle, kuidas arvutatakse kauba tarbimist.</span><span class="sxs-lookup"><span data-stu-id="48404-130">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="48404-131">Valige selle protseduuri puhul FIFO.</span><span class="sxs-lookup"><span data-stu-id="48404-131">Select   FIFO for this procedure.</span></span>  
16. <span data-ttu-id="48404-132">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="48404-132">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="48404-133">Laiendage või ahendage jaotist Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="48404-133">Expand or collapse the Manage costs section.</span></span>
18. <span data-ttu-id="48404-134">Klõpsake väljal Kaubagrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="48404-134">In the Item group field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="48404-135">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="48404-135">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48404-136">Kaubagruppe kasutatakse varude haldamisel laokaupade jagamiseks gruppidesse.</span><span class="sxs-lookup"><span data-stu-id="48404-136">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="48404-137">Valige selle protseduuri puhul CarAudio.</span><span class="sxs-lookup"><span data-stu-id="48404-137">Select   CarAudio for this procedure.</span></span>  
20. <span data-ttu-id="48404-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="48404-138">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="48404-139">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="48404-139">On the Action Pane, click Plan.</span></span>
22. <span data-ttu-id="48404-140">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="48404-140">Click Default order settings.</span></span>
23. <span data-ttu-id="48404-141">Valige suvand väljal Vaikimisi tellimusetüüp.</span><span class="sxs-lookup"><span data-stu-id="48404-141">In the Default order type field, select an option.</span></span>
    * <span data-ttu-id="48404-142">Valige suvand Tootmine määramaks, et selle tooteetaloni vaikimisi tarnesuvand on selle tootmine.</span><span class="sxs-lookup"><span data-stu-id="48404-142">Select Production to specify that the default supply option for this product master is to produce it.</span></span>  
24. <span data-ttu-id="48404-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="48404-143">Close the page.</span></span>
25. <span data-ttu-id="48404-144">Sulgege vorm Väljastatud toote üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="48404-144">Close the Released product details form.</span></span>


