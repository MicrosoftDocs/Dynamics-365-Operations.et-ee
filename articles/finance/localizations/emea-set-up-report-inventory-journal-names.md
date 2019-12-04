---
title: Varude töölehe aruanded
description: Kui kasutate elektroonilisel aruandlusel põhinevaid konfigureeritavaid varude aruandeid, siis peate seadistama seose konkreetse aruande ja töölehe tüübi vahel.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalName
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265144
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: d051c8ab7f15f69dd06db0986c3151b61d595b6d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175734"
---
# <a name="inventory-journal-reports"></a><span data-ttu-id="dbca8-103">Varude töölehe aruanded</span><span class="sxs-lookup"><span data-stu-id="dbca8-103">Inventory journal reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbca8-104">Kui kasutate elektroonilisel aruandlusel põhinevaid konfigureeritavaid varude aruandeid, siis peate seadistama seose konkreetse aruande ja töölehe tüübi vahel.</span><span class="sxs-lookup"><span data-stu-id="dbca8-104">When you use configurable inventory reports based on electronic reporting, you need to set up a relationship between a specific report and a journal type.</span></span>

<span data-ttu-id="dbca8-105">Konkreetse aruande ja töölehe tüübi vahelise seose seadistamiseks sisestage lehel **Varude töölehe nimed** (**Varude haldus** &gt; **Seadistus** &gt; **Töölehtede nimed** &gt; **Varud**) aruandele nimi.</span><span class="sxs-lookup"><span data-stu-id="dbca8-105">To set up a relationship between a specific report and a journal type, on the **Inventory journal names** page (**Inventory management** &gt; **Setup** &gt; **Journal names** &gt; **Inventory**), enter a name for the report.</span></span> <span data-ttu-id="dbca8-106">**Märkus:** toetatud konfiguratsioonide seadistamiseks laadige alla vajalikud elektroonilise aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="dbca8-106">**Note:** To set up supported configurations, download the required electronic reporting configurations.</span></span> <span data-ttu-id="dbca8-107">Lisateavet leiate jaotisest [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="dbca8-107">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span> <span data-ttu-id="dbca8-108">Näited Euroopas toetatud konfiguratsioonidega laoaruannete kohta on loetletud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="dbca8-108">Examples of inventory reports with supported configurations in Europe are listed in the following table.</span></span>

|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| <span data-ttu-id="dbca8-109">**Riik**</span><span class="sxs-lookup"><span data-stu-id="dbca8-109">**Country**</span></span>        | <span data-ttu-id="dbca8-110">**Aruande kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="dbca8-110">**Report description**</span></span>              | <span data-ttu-id="dbca8-111">**Töölehe tüüp**</span><span class="sxs-lookup"><span data-stu-id="dbca8-111">**Journal type**</span></span> | <span data-ttu-id="dbca8-112">**Vormingu vastenduse nimi**</span><span class="sxs-lookup"><span data-stu-id="dbca8-112">**Format mapping name**</span></span>                 |
| <span data-ttu-id="dbca8-113">Leedu, Ungari</span><span class="sxs-lookup"><span data-stu-id="dbca8-113">Lithuania, Hungary</span></span> | <span data-ttu-id="dbca8-114">Inventuuriväljavõtte aruanne</span><span class="sxs-lookup"><span data-stu-id="dbca8-114">Inventory statement report</span></span>          | <span data-ttu-id="dbca8-115">Inventuur</span><span class="sxs-lookup"><span data-stu-id="dbca8-115">Counting</span></span>         | <span data-ttu-id="dbca8-116">Inventuuriväljavõte (HU, LT)</span><span class="sxs-lookup"><span data-stu-id="dbca8-116">Inventory statement (HU, LT)</span></span>            |
| <span data-ttu-id="dbca8-117">Läti, Poola</span><span class="sxs-lookup"><span data-stu-id="dbca8-117">Latvia, Poland</span></span>     | <span data-ttu-id="dbca8-118">Varude ümberklassifitseerimise dokument</span><span class="sxs-lookup"><span data-stu-id="dbca8-118">Inventory reclassification document</span></span> | <span data-ttu-id="dbca8-119">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="dbca8-119">Transfer</span></span>         | <span data-ttu-id="dbca8-120">InventoryReclassificationDocument\_PLLV</span><span class="sxs-lookup"><span data-stu-id="dbca8-120">InventoryReclassificationDocument\_PLLV</span></span> |
| <span data-ttu-id="dbca8-121">Eesti</span><span class="sxs-lookup"><span data-stu-id="dbca8-121">Estonia</span></span>            | <span data-ttu-id="dbca8-122">Varude ümberklassifitseerimise dokument</span><span class="sxs-lookup"><span data-stu-id="dbca8-122">Inventory reclassification document</span></span> | <span data-ttu-id="dbca8-123">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="dbca8-123">Transfer</span></span>         | <span data-ttu-id="dbca8-124">InventoryReclassificationDocument\_EE</span><span class="sxs-lookup"><span data-stu-id="dbca8-124">InventoryReclassificationDocument\_EE</span></span>   |
| <span data-ttu-id="dbca8-125">Poola</span><span class="sxs-lookup"><span data-stu-id="dbca8-125">Poland</span></span>             | <span data-ttu-id="dbca8-126">Sisemine PW/RW</span><span class="sxs-lookup"><span data-stu-id="dbca8-126">Internal PW/RW</span></span>                      | <span data-ttu-id="dbca8-127">Liikumine</span><span class="sxs-lookup"><span data-stu-id="dbca8-127">Movement</span></span>         | <span data-ttu-id="dbca8-128">InventJournalLinesDocPL</span><span class="sxs-lookup"><span data-stu-id="dbca8-128">InventJournalLinesDocPL</span></span>                 |
| <span data-ttu-id="dbca8-129">Läti</span><span class="sxs-lookup"><span data-stu-id="dbca8-129">Latvia</span></span>             | <span data-ttu-id="dbca8-130"> Varude liikumise dokument</span><span class="sxs-lookup"><span data-stu-id="dbca8-130">Inventory movement document</span></span>         | <span data-ttu-id="dbca8-131">Liikumine</span><span class="sxs-lookup"><span data-stu-id="dbca8-131">Movement</span></span>         | <span data-ttu-id="dbca8-132">Liikumine\_LV</span><span class="sxs-lookup"><span data-stu-id="dbca8-132">Movement\_LV</span></span>                            |
| <span data-ttu-id="dbca8-133">Läti</span><span class="sxs-lookup"><span data-stu-id="dbca8-133">Latvia</span></span>             | <span data-ttu-id="dbca8-134">Varude allahindluse dokument</span><span class="sxs-lookup"><span data-stu-id="dbca8-134">Inventory write-down document</span></span>       | <span data-ttu-id="dbca8-135">Korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="dbca8-135">Adjustment</span></span>       | <span data-ttu-id="dbca8-136">InventJournalLines\_LV</span><span class="sxs-lookup"><span data-stu-id="dbca8-136">InventJournalLines\_LV</span></span>                  |
| <span data-ttu-id="dbca8-137">Läti</span><span class="sxs-lookup"><span data-stu-id="dbca8-137">Latvia</span></span>             | <span data-ttu-id="dbca8-138">Ülekande tarneteade</span><span class="sxs-lookup"><span data-stu-id="dbca8-138">Transfer delivery note</span></span>              | <span data-ttu-id="dbca8-139">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="dbca8-139">Transfer</span></span>         | <span data-ttu-id="dbca8-140">InternalTransferDeliveryNote\_LV</span><span class="sxs-lookup"><span data-stu-id="dbca8-140">InternalTransferDeliveryNote\_LV</span></span>        |
| <span data-ttu-id="dbca8-141">Läti</span><span class="sxs-lookup"><span data-stu-id="dbca8-141">Latvia</span></span>             | <span data-ttu-id="dbca8-142">Inventuuridokumendi aruanne</span><span class="sxs-lookup"><span data-stu-id="dbca8-142">Counting document report</span></span>            | <span data-ttu-id="dbca8-143">Inventuur</span><span class="sxs-lookup"><span data-stu-id="dbca8-143">Counting</span></span>         | <span data-ttu-id="dbca8-144">CountedDocument\_LV</span><span class="sxs-lookup"><span data-stu-id="dbca8-144">CountedDocument\_LV</span></span>                     |
| <span data-ttu-id="dbca8-145">Läti</span><span class="sxs-lookup"><span data-stu-id="dbca8-145">Latvia</span></span>             | <span data-ttu-id="dbca8-146">Inventuuri loendi aruanne</span><span class="sxs-lookup"><span data-stu-id="dbca8-146">Counting list report</span></span>                | <span data-ttu-id="dbca8-147">Inventuur</span><span class="sxs-lookup"><span data-stu-id="dbca8-147">Counting</span></span>         | <span data-ttu-id="dbca8-148">Inventuuri loend</span><span class="sxs-lookup"><span data-stu-id="dbca8-148">Counting list</span></span>                           |




