---
title: Ostukulutuste analüüsi Power BI sisu
description: See teema kirjeldab, mida hõlmab ostukulutuste analüüsi Power BI sisu.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559545"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="96aa9-103">Ostukulutuste analüüsi Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="96aa9-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96aa9-104">See teema kirjeldab, mida hõlmab **Ostukulutuste analüüsi** Microsoft Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="96aa9-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="96aa9-105">See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="96aa9-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="96aa9-106">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="96aa9-106">Overview</span></span>

<span data-ttu-id="96aa9-107">**Ostukulutuste analüüsi** Power BI sisu on mõeldud eelarvete eest vastutavate ostujuhtide ja juhtide abistamiseks ostukulutuste jälgimisel.</span><span class="sxs-lookup"><span data-stu-id="96aa9-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="96aa9-108">Juhid saavad analüüsida ostukulutusi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="96aa9-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="96aa9-109">Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)</span><span class="sxs-lookup"><span data-stu-id="96aa9-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="96aa9-110">Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)</span><span class="sxs-lookup"><span data-stu-id="96aa9-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="96aa9-111">Sisu kasutab ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa.</span><span class="sxs-lookup"><span data-stu-id="96aa9-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="96aa9-112">Aruanded tõstavad esile ostukulude muutusi aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="96aa9-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="96aa9-113">Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest.</span><span class="sxs-lookup"><span data-stu-id="96aa9-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="96aa9-114">Lisaks näitavad diagrammid erinevate hankekategooriate ja hankijagruppide kulusid.</span><span class="sxs-lookup"><span data-stu-id="96aa9-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="96aa9-115">Seega saavad kategooria- ja piirkonnajuhid kasutada neid diagramme muutuste tuvastamiseks kulutamiskäitumises.</span><span class="sxs-lookup"><span data-stu-id="96aa9-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="96aa9-116">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="96aa9-116">Accessing the Power BI content</span></span>
<span data-ttu-id="96aa9-117">**Ostukulutuste analüüsi** Power BI sisu kuvatakse lehel **Ostu- ja kulutusanalüüs** (**Hanked** \> **Päringud ja aruanded** \> **Ostujõudluse analüüs** \> **Ostu- ja kulutusanalüüs**).</span><span class="sxs-lookup"><span data-stu-id="96aa9-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="96aa9-118">Power BI sisusse kuuluvad mõõdikud</span><span class="sxs-lookup"><span data-stu-id="96aa9-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="96aa9-119">**Ostukulutuste analüüsi** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet.</span><span class="sxs-lookup"><span data-stu-id="96aa9-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="96aa9-120">Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena.</span><span class="sxs-lookup"><span data-stu-id="96aa9-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="96aa9-121">Järgmistes jaotistes antakse ülevaade visualiseeringutest.</span><span class="sxs-lookup"><span data-stu-id="96aa9-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="96aa9-122">Ostmine hankija aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-122">Purchase by vendor report page</span></span>
<span data-ttu-id="96aa9-123">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-123">**Charts**</span></span>
- <span data-ttu-id="96aa9-124">10 tipphankijat ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="96aa9-125">Ostud kokku hankijagrupi/riigi/nime alusel (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="96aa9-126">Ostud hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="96aa9-127">Keskmine ost hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="96aa9-128">**Paanid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-128">**Tiles**</span></span>
- <span data-ttu-id="96aa9-129">Koguost</span><span class="sxs-lookup"><span data-stu-id="96aa9-129">Total purchase</span></span>
- <span data-ttu-id="96aa9-130">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="96aa9-130">YOY purchase growth</span></span>
- <span data-ttu-id="96aa9-131">Hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="96aa9-131">Total # vendors</span></span>
- <span data-ttu-id="96aa9-132">Aktiivsete hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="96aa9-132">Total # of active vendors</span></span>

<span data-ttu-id="96aa9-133">**Näide**</span><span class="sxs-lookup"><span data-stu-id="96aa9-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="96aa9-134">Ostmine toote aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-134">Purchase by product report page</span></span>

<span data-ttu-id="96aa9-135">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-135">**Charts**</span></span>
- <span data-ttu-id="96aa9-136">Ostud hankekategooria / toote nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="96aa9-137">Ostud hankekategooria / toote nime alusel kokku (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="96aa9-138">10 tipptoodet ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="96aa9-139">**Paanid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-139">**Tiles**</span></span>
- <span data-ttu-id="96aa9-140">Toodete arv kokku</span><span class="sxs-lookup"><span data-stu-id="96aa9-140">Total # of products</span></span></li>
- <span data-ttu-id="96aa9-141">Aktiivsete toodete osakaal toodete arvust kokku</span><span class="sxs-lookup"><span data-stu-id="96aa9-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="96aa9-142">Toodete arv, mis annavad 80% ostudest</span><span class="sxs-lookup"><span data-stu-id="96aa9-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="96aa9-143">**Näide**</span><span class="sxs-lookup"><span data-stu-id="96aa9-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="96aa9-144">Ostmine ajaperioodi aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-144">Purchase by period report page</span></span>
<span data-ttu-id="96aa9-145">See leht näitab selle ja eelmise aasta oste ja kasvu hankekategooriate alusel.</span><span class="sxs-lookup"><span data-stu-id="96aa9-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="96aa9-146">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-146">**Charts**</span></span> 
- <span data-ttu-id="96aa9-147">Ostud kuu/päeva alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="96aa9-148">Kumulatiivsete ostude YOY hälve (kaskaaddiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="96aa9-149">Ostude YOY kasv kokku (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="96aa9-150">Hankeväljavõte (maatriks)</span><span class="sxs-lookup"><span data-stu-id="96aa9-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="96aa9-151">**Paanid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-151">**Tiles**</span></span>
- <span data-ttu-id="96aa9-152">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="96aa9-152">YOY purchase growth</span></span>
- <span data-ttu-id="96aa9-153">YOY ostude kasvu %</span><span class="sxs-lookup"><span data-stu-id="96aa9-153">YOY purchase growth %</span></span>

<span data-ttu-id="96aa9-154">**Näide**</span><span class="sxs-lookup"><span data-stu-id="96aa9-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="96aa9-155">Ostmine hankija asukoha aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="96aa9-156">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-156">**Charts**</span></span>
- <span data-ttu-id="96aa9-157">Ostud linna alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-157">Purchase by city</span></span>
- <span data-ttu-id="96aa9-158">Ostude YOY kasvu %</span><span class="sxs-lookup"><span data-stu-id="96aa9-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="96aa9-159">Ostud riikide järgi</span><span class="sxs-lookup"><span data-stu-id="96aa9-159">Purchase by country</span></span>

<span data-ttu-id="96aa9-160">**Näide**</span><span class="sxs-lookup"><span data-stu-id="96aa9-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="96aa9-161">Ostukulutuste analüüs aja aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="96aa9-162">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-162">**Charts**</span></span> 
- <span data-ttu-id="96aa9-163">Jooksva aasta ostud kuu/päeva alusel (joondiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="96aa9-164">Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="96aa9-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="96aa9-165">**Näide**</span><span class="sxs-lookup"><span data-stu-id="96aa9-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="96aa9-166">Ostukulutuste analüüs hankija aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="96aa9-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="96aa9-167">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="96aa9-167">**Charts**</span></span> 
- <span data-ttu-id="96aa9-168">10 juhtiva hankija ostude % ostudest (lehter)</span><span class="sxs-lookup"><span data-stu-id="96aa9-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="96aa9-169">10 parimat hankijat suurema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="96aa9-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="96aa9-170">10 parimat hankijat väiksema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="96aa9-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="96aa9-171">**Näide** 
</span><span class="sxs-lookup"><span data-stu-id="96aa9-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="96aa9-172">Andmemudel ja üksused</span><span class="sxs-lookup"><span data-stu-id="96aa9-172">Data model and entities</span></span>
<span data-ttu-id="96aa9-173">Aruandelehtede täitmiseks **ostukulutuste analüüsi** Power BI sisus kasutatakse järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="96aa9-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="96aa9-174">Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised.</span><span class="sxs-lookup"><span data-stu-id="96aa9-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="96aa9-175">Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas.</span><span class="sxs-lookup"><span data-stu-id="96aa9-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="96aa9-176">Lisateavet vt teemast [Power BI integratsioon üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="96aa9-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="96aa9-177">Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 ostukuubis saadaval olnud koondmõõtmiste alamkogum.</span><span class="sxs-lookup"><span data-stu-id="96aa9-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="96aa9-178">Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks.</span><span class="sxs-lookup"><span data-stu-id="96aa9-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="96aa9-179">Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Power BI integreerimine üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="96aa9-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="96aa9-180">Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisu alusena.</span><span class="sxs-lookup"><span data-stu-id="96aa9-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="96aa9-181">Üksus</span><span class="sxs-lookup"><span data-stu-id="96aa9-181">Entity</span></span>        | <span data-ttu-id="96aa9-182">Peamised koondmõõtmised</span><span class="sxs-lookup"><span data-stu-id="96aa9-182">Key aggregate measurements</span></span> | <span data-ttu-id="96aa9-183">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="96aa9-183">Data source</span></span>                                 | <span data-ttu-id="96aa9-184">Väli</span><span class="sxs-lookup"><span data-stu-id="96aa9-184">Field</span></span>              | <span data-ttu-id="96aa9-185">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="96aa9-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="96aa9-186">Arve read</span><span class="sxs-lookup"><span data-stu-id="96aa9-186">Invoice lines</span></span> | <span data-ttu-id="96aa9-187">Ost</span><span class="sxs-lookup"><span data-stu-id="96aa9-187">Purchase</span></span>                   | <span data-ttu-id="96aa9-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="96aa9-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="96aa9-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="96aa9-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="96aa9-190">Summa arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="96aa9-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="96aa9-191">Järgmises tabelis on antud peamised mõõtmised, mis arvutatakse sisupaketis arve ridade üksusest.</span><span class="sxs-lookup"><span data-stu-id="96aa9-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="96aa9-192">Mõõt</span><span class="sxs-lookup"><span data-stu-id="96aa9-192">Measure</span></span>               | <span data-ttu-id="96aa9-193">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="96aa9-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96aa9-194">Jooksva aasta ostud</span><span class="sxs-lookup"><span data-stu-id="96aa9-194">Purchase current year</span></span> | <span data-ttu-id="96aa9-195">Jooksva aasta ostud = SUM('Arve read'\[Ost\])</span><span class="sxs-lookup"><span data-stu-id="96aa9-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="96aa9-196">Eelmise aasta ostud</span><span class="sxs-lookup"><span data-stu-id="96aa9-196">Purchase last year</span></span>    | <span data-ttu-id="96aa9-197">Eelmise aasta ostud = CALCULATE(SUM('Arve read'\[Ost\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\]))</span><span class="sxs-lookup"><span data-stu-id="96aa9-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="96aa9-198">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="96aa9-198">YOY purchase growth</span></span>   | <span data-ttu-id="96aa9-199">YOY ostude kasv = \[Jooksva aasta ostud\] – \[Eelmise aasta ostud\]</span><span class="sxs-lookup"><span data-stu-id="96aa9-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="96aa9-200">Järgmisi sisu põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate saamiseks.</span><span class="sxs-lookup"><span data-stu-id="96aa9-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="96aa9-201">Üksus</span><span class="sxs-lookup"><span data-stu-id="96aa9-201">Entity</span></span>                 | <span data-ttu-id="96aa9-202">Atribuutide näited</span><span class="sxs-lookup"><span data-stu-id="96aa9-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="96aa9-203">Hankijad</span><span class="sxs-lookup"><span data-stu-id="96aa9-203">Vendors</span></span>                | <span data-ttu-id="96aa9-204">Hankijagrupid, Hankija riik või regioonid, Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="96aa9-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="96aa9-205">Tooted</span><span class="sxs-lookup"><span data-stu-id="96aa9-205">Products</span></span>               | <span data-ttu-id="96aa9-206">Tootenumber, Toote nimi, Kaubagruppide nimi</span><span class="sxs-lookup"><span data-stu-id="96aa9-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="96aa9-207">Hankekategooriad</span><span class="sxs-lookup"><span data-stu-id="96aa9-207">Procurement categories</span></span> | <span data-ttu-id="96aa9-208">Hankekategooria, Hankekategooria nimed</span><span class="sxs-lookup"><span data-stu-id="96aa9-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="96aa9-209">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="96aa9-209">Legal entities</span></span>         | <span data-ttu-id="96aa9-210">Juriidilise isiku nimi</span><span class="sxs-lookup"><span data-stu-id="96aa9-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="96aa9-211">Kuupäevad</span><span class="sxs-lookup"><span data-stu-id="96aa9-211">Dates</span></span>                  | <span data-ttu-id="96aa9-212">Kuupäevad, Aasta vastaskonto</span><span class="sxs-lookup"><span data-stu-id="96aa9-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="96aa9-213">Vaikimisi näitab sisu jooksva kalendriaasta andmeid.</span><span class="sxs-lookup"><span data-stu-id="96aa9-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="96aa9-214">Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises.</span><span class="sxs-lookup"><span data-stu-id="96aa9-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="96aa9-215">Saate muuta ka ettevõtte filtrit.</span><span class="sxs-lookup"><span data-stu-id="96aa9-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]