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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 265144
ms.search.region: Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 4369500884d4a55c2960126a16dc612d7dbbe737
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1513050"
---
# <a name="inventory-journal-reports"></a><span data-ttu-id="2a800-103">Varude töölehe aruanded</span><span class="sxs-lookup"><span data-stu-id="2a800-103">Inventory journal reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a800-104">Kui kasutate elektroonilisel aruandlusel põhinevaid konfigureeritavaid varude aruandeid, siis peate seadistama seose konkreetse aruande ja töölehe tüübi vahel.</span><span class="sxs-lookup"><span data-stu-id="2a800-104">When you use configurable inventory reports based on electronic reporting, you need to set up a relationship between a specific report and a journal type.</span></span>

<span data-ttu-id="2a800-105">Konkreetse aruande ja töölehe tüübi vahelise seose seadistamiseks sisestage lehel **Varude töölehe nimed** (**Varude haldus** &gt; **Seadistus** &gt; **Töölehtede nimed** &gt; **Varud**) aruandele nimi.</span><span class="sxs-lookup"><span data-stu-id="2a800-105">To set up a relationship between a specific report and a journal type, on the **Inventory journal names** page (**Inventory management** &gt; **Setup** &gt; **Journal names** &gt; **Inventory**), enter a name for the report.</span></span> <span data-ttu-id="2a800-106">**Märkus:** toetatud konfiguratsioonide seadistamiseks laadige alla vajalikud elektroonilise aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="2a800-106">**Note:** To set up supported configurations, download the required electronic reporting configurations.</span></span> <span data-ttu-id="2a800-107">Lisateavet leiate jaotisest [Elektroonilise aruandluse konfiguratsioonide allalaadimine teenusest Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="2a800-107">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span> <span data-ttu-id="2a800-108">Näited Euroopas toetatud konfiguratsioonidega laoaruannete kohta on loetletud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="2a800-108">Examples of inventory reports with supported configurations in Europe are listed in the following table.</span></span>

|                    |                                     |                  |                                         |
|--------------------|-------------------------------------|------------------|-----------------------------------------|
| <span data-ttu-id="2a800-109">**Riik**</span><span class="sxs-lookup"><span data-stu-id="2a800-109">**Country**</span></span>        | <span data-ttu-id="2a800-110">**Aruande kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="2a800-110">**Report description**</span></span>              | <span data-ttu-id="2a800-111">**Töölehe tüüp**</span><span class="sxs-lookup"><span data-stu-id="2a800-111">**Journal type**</span></span> | <span data-ttu-id="2a800-112">**Vormingu vastenduse nimi**</span><span class="sxs-lookup"><span data-stu-id="2a800-112">**Format mapping name**</span></span>                 |
| <span data-ttu-id="2a800-113">Leedu, Ungari</span><span class="sxs-lookup"><span data-stu-id="2a800-113">Lithuania, Hungary</span></span> | <span data-ttu-id="2a800-114">Inventuuriväljavõtte aruanne</span><span class="sxs-lookup"><span data-stu-id="2a800-114">Inventory statement report</span></span>          | <span data-ttu-id="2a800-115">Inventuur</span><span class="sxs-lookup"><span data-stu-id="2a800-115">Counting</span></span>         | <span data-ttu-id="2a800-116">Inventuuriväljavõte (HU, LT)</span><span class="sxs-lookup"><span data-stu-id="2a800-116">Inventory statement (HU, LT)</span></span>            |
| <span data-ttu-id="2a800-117">Läti, Poola</span><span class="sxs-lookup"><span data-stu-id="2a800-117">Latvia, Poland</span></span>     | <span data-ttu-id="2a800-118">Varude ümberklassifitseerimise dokument</span><span class="sxs-lookup"><span data-stu-id="2a800-118">Inventory reclassification document</span></span> | <span data-ttu-id="2a800-119">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="2a800-119">Transfer</span></span>         | <span data-ttu-id="2a800-120">InventoryReclassificationDocument\_PLLV</span><span class="sxs-lookup"><span data-stu-id="2a800-120">InventoryReclassificationDocument\_PLLV</span></span> |
| <span data-ttu-id="2a800-121">Eesti</span><span class="sxs-lookup"><span data-stu-id="2a800-121">Estonia</span></span>            | <span data-ttu-id="2a800-122">Varude ümberklassifitseerimise dokument</span><span class="sxs-lookup"><span data-stu-id="2a800-122">Inventory reclassification document</span></span> | <span data-ttu-id="2a800-123">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="2a800-123">Transfer</span></span>         | <span data-ttu-id="2a800-124">InventoryReclassificationDocument\_EE</span><span class="sxs-lookup"><span data-stu-id="2a800-124">InventoryReclassificationDocument\_EE</span></span>   |
| <span data-ttu-id="2a800-125">Poola</span><span class="sxs-lookup"><span data-stu-id="2a800-125">Poland</span></span>             | <span data-ttu-id="2a800-126">Sisemine PW/RW</span><span class="sxs-lookup"><span data-stu-id="2a800-126">Internal PW/RW</span></span>                      | <span data-ttu-id="2a800-127">Liikumine</span><span class="sxs-lookup"><span data-stu-id="2a800-127">Movement</span></span>         | <span data-ttu-id="2a800-128">InventJournalLinesDocPL</span><span class="sxs-lookup"><span data-stu-id="2a800-128">InventJournalLinesDocPL</span></span>                 |
| <span data-ttu-id="2a800-129">Läti</span><span class="sxs-lookup"><span data-stu-id="2a800-129">Latvia</span></span>             | <span data-ttu-id="2a800-130"> Varude liikumise dokument</span><span class="sxs-lookup"><span data-stu-id="2a800-130">Inventory movement document</span></span>         | <span data-ttu-id="2a800-131">Liikumine</span><span class="sxs-lookup"><span data-stu-id="2a800-131">Movement</span></span>         | <span data-ttu-id="2a800-132">Liikumine\_LV</span><span class="sxs-lookup"><span data-stu-id="2a800-132">Movement\_LV</span></span>                            |
| <span data-ttu-id="2a800-133">Läti</span><span class="sxs-lookup"><span data-stu-id="2a800-133">Latvia</span></span>             | <span data-ttu-id="2a800-134">Varude allahindluse dokument</span><span class="sxs-lookup"><span data-stu-id="2a800-134">Inventory write-down document</span></span>       | <span data-ttu-id="2a800-135">Korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="2a800-135">Adjustment</span></span>       | <span data-ttu-id="2a800-136">InventJournalLines\_LV</span><span class="sxs-lookup"><span data-stu-id="2a800-136">InventJournalLines\_LV</span></span>                  |
| <span data-ttu-id="2a800-137">Läti</span><span class="sxs-lookup"><span data-stu-id="2a800-137">Latvia</span></span>             | <span data-ttu-id="2a800-138">Ülekande tarneteade</span><span class="sxs-lookup"><span data-stu-id="2a800-138">Transfer delivery note</span></span>              | <span data-ttu-id="2a800-139">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="2a800-139">Transfer</span></span>         | <span data-ttu-id="2a800-140">InternalTransferDeliveryNote\_LV</span><span class="sxs-lookup"><span data-stu-id="2a800-140">InternalTransferDeliveryNote\_LV</span></span>        |
| <span data-ttu-id="2a800-141">Läti</span><span class="sxs-lookup"><span data-stu-id="2a800-141">Latvia</span></span>             | <span data-ttu-id="2a800-142">Inventuuridokumendi aruanne</span><span class="sxs-lookup"><span data-stu-id="2a800-142">Counting document report</span></span>            | <span data-ttu-id="2a800-143">Inventuur</span><span class="sxs-lookup"><span data-stu-id="2a800-143">Counting</span></span>         | <span data-ttu-id="2a800-144">CountedDocument\_LV</span><span class="sxs-lookup"><span data-stu-id="2a800-144">CountedDocument\_LV</span></span>                     |
| <span data-ttu-id="2a800-145">Läti</span><span class="sxs-lookup"><span data-stu-id="2a800-145">Latvia</span></span>             | <span data-ttu-id="2a800-146">Inventuuri loendi aruanne</span><span class="sxs-lookup"><span data-stu-id="2a800-146">Counting list report</span></span>                | <span data-ttu-id="2a800-147">Inventuur</span><span class="sxs-lookup"><span data-stu-id="2a800-147">Counting</span></span>         | <span data-ttu-id="2a800-148">Inventuuri loend</span><span class="sxs-lookup"><span data-stu-id="2a800-148">Counting list</span></span>                           |





