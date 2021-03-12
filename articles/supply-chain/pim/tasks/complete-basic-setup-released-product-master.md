---
title: Vabastatud tooteetaloni täielik põhiseadistus
description: Selles teemas selgitatkas, kuidas täiendada minimaalset häälestust, mis on vajalik enne tooteetaloni kasutamist koosluse versioonis.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventTableInventoryDimensionGroups, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 668b60efa55fa553cf308d5bfc5da7e23f460366
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4987025"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="310ce-103">Vabastatud tooteetaloni täielik põhiseadistus</span><span class="sxs-lookup"><span data-stu-id="310ce-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="310ce-104">Selles teemas selgitatkas, kuidas täiendada minimaalset häälestust, mis on vajalik enne tooteetaloni kasutamist koosluse versioonis.</span><span class="sxs-lookup"><span data-stu-id="310ce-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="310ce-105">See on kolmas protseduur kaheksast, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="310ce-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="310ce-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="310ce-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="310ce-107">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="310ce-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="310ce-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="310ce-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="310ce-109">Valige teises protseduuris väljastatud tooteetalon.</span><span class="sxs-lookup"><span data-stu-id="310ce-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="310ce-110">Selle tooteetalon on loodud dimensioonipõhine konfiguratsioonitehnoloogia abil.</span><span class="sxs-lookup"><span data-stu-id="310ce-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="310ce-111">Klõpsake toimingupaanil suvandit **Toode**.</span><span class="sxs-lookup"><span data-stu-id="310ce-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="310ce-112">Klõpsake rippdialoogi avamiseks suvandit **Dimensiooni rühmad**.</span><span class="sxs-lookup"><span data-stu-id="310ce-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="310ce-113">Klõpsake väljal **Laoala dimensiooni rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="310ce-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="310ce-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="310ce-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="310ce-115">Laoala dimensioonigrupp määratleb, milliseid laoala dimensioone toote kande puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="310ce-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="310ce-116">Valige selle protseduuri puhul suvand **Tegevuskoht**.</span><span class="sxs-lookup"><span data-stu-id="310ce-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="310ce-117">Klõpsake väljal **Jälgimisdimensiooni rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="310ce-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="310ce-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="310ce-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="310ce-119">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone toote kande puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="310ce-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="310ce-120">Valige selle protseduuri puhul suvand **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="310ce-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="310ce-121">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="310ce-121">Click **OK**.</span></span>
10. <span data-ttu-id="310ce-122">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="310ce-122">Click **Edit**.</span></span>
11. <span data-ttu-id="310ce-123">Klõpsake väljal **Kauba mudeli rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="310ce-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="310ce-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="310ce-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="310ce-125">Kaubamudeligrupid sisaldavad sätteid, mis määratlevad, kuidas kaupu sissetulekutel ja väljaminekutel kontrollitakse ning käsitletakse.</span><span class="sxs-lookup"><span data-stu-id="310ce-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="310ce-126">Need määravad ka selle, kuidas arvutatakse kauba tarbimist.</span><span class="sxs-lookup"><span data-stu-id="310ce-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="310ce-127">Valige selle protseduuri puhul **FIFO**.</span><span class="sxs-lookup"><span data-stu-id="310ce-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="310ce-128">Laiendage jaotist **Kulude haldamine**.</span><span class="sxs-lookup"><span data-stu-id="310ce-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="310ce-129">Klõpsake väljal **Kauba rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="310ce-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="310ce-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="310ce-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="310ce-131">Kaubagruppe kasutatakse varude haldamisel laokaupade jagamiseks gruppidesse.</span><span class="sxs-lookup"><span data-stu-id="310ce-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="310ce-132">Valige selle protseduuri puhul **CarAudio**.</span><span class="sxs-lookup"><span data-stu-id="310ce-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="310ce-133">Valige toimingupaanil nupp **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="310ce-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="310ce-134">Valige **Vaiketellimuse sätted**.</span><span class="sxs-lookup"><span data-stu-id="310ce-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="310ce-135">Valige suvand **Vaiketellimuse tüübi väli**.</span><span class="sxs-lookup"><span data-stu-id="310ce-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="310ce-136">Valige suvand **Tootmine** määramaks, et selle tooteetaloni vaikimisi tarnesuvand on selle tootmine.</span><span class="sxs-lookup"><span data-stu-id="310ce-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="310ce-137">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="310ce-137">Select **Save**.</span></span>
20. <span data-ttu-id="310ce-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="310ce-138">Close the page.</span></span>
21. <span data-ttu-id="310ce-139">Sulgege vorm **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="310ce-139">Close the **Released product details** form.</span></span>

