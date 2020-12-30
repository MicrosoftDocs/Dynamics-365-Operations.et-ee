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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8ac4ceeb3e21ab089eb16565bb6e38c7eb44be80
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426269"
---
# <a name="complete-basic-setup-of-a-released-product-master"></a><span data-ttu-id="c85c2-103">Vabastatud tooteetaloni täielik põhiseadistus</span><span class="sxs-lookup"><span data-stu-id="c85c2-103">Complete basic setup of a released product master</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c85c2-104">Selles teemas selgitatkas, kuidas täiendada minimaalset häälestust, mis on vajalik enne tooteetaloni kasutamist koosluse versioonis.</span><span class="sxs-lookup"><span data-stu-id="c85c2-104">This topic shows how to complete the minimum setup that is required before the product master can be used in BOM versions.</span></span>

<span data-ttu-id="c85c2-105">See on kolmas protseduur kaheksast, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="c85c2-105">This is the third procedure out of eight which explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="c85c2-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c85c2-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="c85c2-107">Avage **Navigeerimispaan > Moodulid > Tooteteabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-107">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="c85c2-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c85c2-108">In the list, find and select the desired record.</span></span> <span data-ttu-id="c85c2-109">Valige teises protseduuris väljastatud tooteetalon.</span><span class="sxs-lookup"><span data-stu-id="c85c2-109">Select the product master that you have released in the second procedure.</span></span> <span data-ttu-id="c85c2-110">Selle tooteetalon on loodud dimensioonipõhine konfiguratsioonitehnoloogia abil.</span><span class="sxs-lookup"><span data-stu-id="c85c2-110">This product master is created with the dimension-based configuration technology.</span></span>  
3. <span data-ttu-id="c85c2-111">Klõpsake toimingupaanil suvandit **Toode**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-111">On the Action Pane, select **Product**.</span></span>
4. <span data-ttu-id="c85c2-112">Klõpsake rippdialoogi avamiseks suvandit **Dimensiooni rühmad**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-112">Select **Dimension groups** to open the drop dialog.</span></span>
5. <span data-ttu-id="c85c2-113">Klõpsake väljal **Laoala dimensiooni rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c85c2-113">In the **Storage dimension group** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c85c2-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c85c2-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="c85c2-115">Laoala dimensioonigrupp määratleb, milliseid laoala dimensioone toote kande puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="c85c2-115">The storage dimension group determines which storage dimensions are used for product transaction.</span></span> <span data-ttu-id="c85c2-116">Valige selle protseduuri puhul suvand **Tegevuskoht**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-116">Select **Site** for this procedure.</span></span>  
7. <span data-ttu-id="c85c2-117">Klõpsake väljal **Jälgimisdimensiooni rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c85c2-117">In the **Tracking dimension group** field, select the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c85c2-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c85c2-118">In the list, find and select the desired record.</span></span> <span data-ttu-id="c85c2-119">Jälgimisdimensioonigrupp määratleb, milliseid jälgimisdimensioone toote kande puhul kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="c85c2-119">The tracking dimension group determines which tracking dimensions are used for product transaction.</span></span> <span data-ttu-id="c85c2-120">Valige selle protseduuri puhul suvand **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-120">Select **None** for this procedure.</span></span>  
9. <span data-ttu-id="c85c2-121">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-121">Click **OK**.</span></span>
10. <span data-ttu-id="c85c2-122">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-122">Click **Edit**.</span></span>
11. <span data-ttu-id="c85c2-123">Klõpsake väljal **Kauba mudeli rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c85c2-123">In the **Item model group** field, select the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c85c2-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c85c2-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="c85c2-125">Kaubamudeligrupid sisaldavad sätteid, mis määratlevad, kuidas kaupu sissetulekutel ja väljaminekutel kontrollitakse ning käsitletakse.</span><span class="sxs-lookup"><span data-stu-id="c85c2-125">Item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="c85c2-126">Need määravad ka selle, kuidas arvutatakse kauba tarbimist.</span><span class="sxs-lookup"><span data-stu-id="c85c2-126">They also determine how item consumption is calculated.</span></span> <span data-ttu-id="c85c2-127">Valige selle protseduuri puhul **FIFO**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-127">Select **FIFO** for this procedure.</span></span>  
13. <span data-ttu-id="c85c2-128">Laiendage jaotist **Kulude haldamine**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-128">Expand the **Manage costs** section.</span></span>
14. <span data-ttu-id="c85c2-129">Klõpsake väljal **Kauba rühm** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c85c2-129">In the **Item group** field, select the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c85c2-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c85c2-130">In the list, find and select the desired record.</span></span> <span data-ttu-id="c85c2-131">Kaubagruppe kasutatakse varude haldamisel laokaupade jagamiseks gruppidesse.</span><span class="sxs-lookup"><span data-stu-id="c85c2-131">Item groups are used to manage inventory by dividing inventory items into groups.</span></span> <span data-ttu-id="c85c2-132">Valige selle protseduuri puhul **CarAudio**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-132">Select **CarAudio** for this procedure.</span></span>  
16. <span data-ttu-id="c85c2-133">Valige toimingupaanil nupp **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-133">On the Action Pane, select **Plan**.</span></span>
17. <span data-ttu-id="c85c2-134">Valige **Vaiketellimuse sätted**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-134">Select **Default order settings**.</span></span>
18. <span data-ttu-id="c85c2-135">Valige suvand **Vaiketellimuse tüübi väli**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-135">In the **Default order type field**, select an option.</span></span> <span data-ttu-id="c85c2-136">Valige suvand **Tootmine** määramaks, et selle tooteetaloni vaikimisi tarnesuvand on selle tootmine.</span><span class="sxs-lookup"><span data-stu-id="c85c2-136">Select **Production** to specify that the default supply option for this product master is to produce it.</span></span>  
19. <span data-ttu-id="c85c2-137">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-137">Select **Save**.</span></span>
20. <span data-ttu-id="c85c2-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c85c2-138">Close the page.</span></span>
21. <span data-ttu-id="c85c2-139">Sulgege vorm **Väljastatud toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="c85c2-139">Close the **Released product details** form.</span></span>

