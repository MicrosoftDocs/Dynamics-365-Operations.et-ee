---
title: Ostukulutuste analüüsi Power BI sisu
description: See teema kirjeldab, mida hõlmab ostukulutuste analüüsi Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutatakse.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182849"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="bdc45-104">Ostukulutuste analüüsi Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="bdc45-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdc45-105">See teema kirjeldab, mida hõlmab **ostukulutuste analüüsi** Microsoft Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="bdc45-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="bdc45-106">See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="bdc45-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="bdc45-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="bdc45-107">Overview</span></span>

<span data-ttu-id="bdc45-108">**Ostukulutuste analüüsi** Power BI sisu on mõeldud eelarvete eest vastutavate ostujuhtide ja juhtide abistamiseks ostukulutuste jälgimisel.</span><span class="sxs-lookup"><span data-stu-id="bdc45-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="bdc45-109">Juhid saavad analüüsida ostukulutusi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="bdc45-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="bdc45-110">Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)</span><span class="sxs-lookup"><span data-stu-id="bdc45-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="bdc45-111">Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)</span><span class="sxs-lookup"><span data-stu-id="bdc45-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="bdc45-112">Sisu kasutab ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa.</span><span class="sxs-lookup"><span data-stu-id="bdc45-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="bdc45-113">Aruanded tõstavad esile ostukulude muutusi aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="bdc45-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="bdc45-114">Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest.</span><span class="sxs-lookup"><span data-stu-id="bdc45-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="bdc45-115">Lisaks näitavad diagrammid erinevate hankekategooriate ja hankijagruppide kulusid.</span><span class="sxs-lookup"><span data-stu-id="bdc45-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="bdc45-116">Seega saavad kategooria- ja piirkonnajuhid kasutada neid diagramme muutuste tuvastamiseks kulutamiskäitumises.</span><span class="sxs-lookup"><span data-stu-id="bdc45-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="bdc45-117">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="bdc45-117">Accessing the Power BI content</span></span>
<span data-ttu-id="bdc45-118">**Ostukulutuste analüüsi** Power BI sisu kuvatakse lehel **Ostu- ja kulutusanalüüs** (**Hanked** \> **Päringud ja aruanded** \> **Ostujõudluse analüüs** \> **Ostu- ja kulutusanalüüs**).</span><span class="sxs-lookup"><span data-stu-id="bdc45-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="bdc45-119">Power BI sisusse kuuluvad mõõdikud</span><span class="sxs-lookup"><span data-stu-id="bdc45-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="bdc45-120">**Ostukulutuste analüüsi** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet.</span><span class="sxs-lookup"><span data-stu-id="bdc45-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="bdc45-121">Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena.</span><span class="sxs-lookup"><span data-stu-id="bdc45-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="bdc45-122">Järgmistes jaotistes antakse ülevaade visualiseeringutest.</span><span class="sxs-lookup"><span data-stu-id="bdc45-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="bdc45-123">Ostmine hankija aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-123">Purchase by vendor report page</span></span>
<span data-ttu-id="bdc45-124">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-124">**Charts**</span></span>
- <span data-ttu-id="bdc45-125">10 tipphankijat ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="bdc45-126">Ostud kokku hankijagrupi/riigi/nime alusel (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="bdc45-127">Ostud hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="bdc45-128">Keskmine ost hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="bdc45-129">**Paanid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-129">**Tiles**</span></span>
- <span data-ttu-id="bdc45-130">Koguost</span><span class="sxs-lookup"><span data-stu-id="bdc45-130">Total purchase</span></span>
- <span data-ttu-id="bdc45-131">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="bdc45-131">YOY purchase growth</span></span>
- <span data-ttu-id="bdc45-132">Hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="bdc45-132">Total # vendors</span></span>
- <span data-ttu-id="bdc45-133">Aktiivsete hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="bdc45-133">Total # of active vendors</span></span>

<span data-ttu-id="bdc45-134">**Näide**</span><span class="sxs-lookup"><span data-stu-id="bdc45-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="bdc45-135">Ostmine toote aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-135">Purchase by product report page</span></span>

<span data-ttu-id="bdc45-136">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-136">**Charts**</span></span>
- <span data-ttu-id="bdc45-137">Ostud hankekategooria / toote nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="bdc45-138">Ostud hankekategooria / toote nime alusel kokku (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="bdc45-139">10 tipptoodet ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="bdc45-140">**Paanid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-140">**Tiles**</span></span>
- <span data-ttu-id="bdc45-141">Toodete arv kokku</span><span class="sxs-lookup"><span data-stu-id="bdc45-141">Total # of products</span></span></li>
- <span data-ttu-id="bdc45-142">Aktiivsete toodete osakaal toodete arvust kokku</span><span class="sxs-lookup"><span data-stu-id="bdc45-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="bdc45-143">Toodete arv, mis annavad 80% ostudest</span><span class="sxs-lookup"><span data-stu-id="bdc45-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="bdc45-144">**Näide**</span><span class="sxs-lookup"><span data-stu-id="bdc45-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="bdc45-145">Ostmine ajaperioodi aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-145">Purchase by period report page</span></span>
<span data-ttu-id="bdc45-146">See leht näitab selle ja eelmise aasta oste ja kasvu hankekategooriate alusel.</span><span class="sxs-lookup"><span data-stu-id="bdc45-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="bdc45-147">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-147">**Charts**</span></span> 
- <span data-ttu-id="bdc45-148">Ostud kuu/päeva alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="bdc45-149">Kumulatiivsete ostude YOY hälve (kaskaaddiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="bdc45-150">Ostude YOY kasv kokku (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="bdc45-151">Hankeväljavõte (maatriks)</span><span class="sxs-lookup"><span data-stu-id="bdc45-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="bdc45-152">**Paanid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-152">**Tiles**</span></span>
- <span data-ttu-id="bdc45-153">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="bdc45-153">YOY purchase growth</span></span>
- <span data-ttu-id="bdc45-154">YOY ostude kasvu %</span><span class="sxs-lookup"><span data-stu-id="bdc45-154">YOY purchase growth %</span></span>

<span data-ttu-id="bdc45-155">**Näide**</span><span class="sxs-lookup"><span data-stu-id="bdc45-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="bdc45-156">Ostmine hankija asukoha aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="bdc45-157">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-157">**Charts**</span></span>
- <span data-ttu-id="bdc45-158">Ostud linna alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-158">Purchase by city</span></span>
- <span data-ttu-id="bdc45-159">Ostude YOY kasvu %</span><span class="sxs-lookup"><span data-stu-id="bdc45-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="bdc45-160">Ostud riikide järgi</span><span class="sxs-lookup"><span data-stu-id="bdc45-160">Purchase by country</span></span>

<span data-ttu-id="bdc45-161">**Näide**</span><span class="sxs-lookup"><span data-stu-id="bdc45-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="bdc45-162">Ostukulutuste analüüs aja aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="bdc45-163">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-163">**Charts**</span></span> 
- <span data-ttu-id="bdc45-164">Jooksva aasta ostud kuu/päeva alusel (joondiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="bdc45-165">Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="bdc45-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="bdc45-166">**Näide**</span><span class="sxs-lookup"><span data-stu-id="bdc45-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="bdc45-167">Ostukulutuste analüüs hankija aruandelehe alusel</span><span class="sxs-lookup"><span data-stu-id="bdc45-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="bdc45-168">**Diagrammid**</span><span class="sxs-lookup"><span data-stu-id="bdc45-168">**Charts**</span></span> 
- <span data-ttu-id="bdc45-169">10 juhtiva hankija ostude % ostudest (lehter)</span><span class="sxs-lookup"><span data-stu-id="bdc45-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="bdc45-170">10 parimat hankijat suurema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="bdc45-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="bdc45-171">10 parimat hankijat väiksema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="bdc45-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="bdc45-172">**Näide** 
</span><span class="sxs-lookup"><span data-stu-id="bdc45-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="bdc45-173">Andmemudel ja üksused</span><span class="sxs-lookup"><span data-stu-id="bdc45-173">Data model and entities</span></span>
<span data-ttu-id="bdc45-174">Aruandelehtede täitmiseks **ostukulutuste analüüsi** Power BI sisus kasutatakse järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="bdc45-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="bdc45-175">Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised.</span><span class="sxs-lookup"><span data-stu-id="bdc45-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="bdc45-176">Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas.</span><span class="sxs-lookup"><span data-stu-id="bdc45-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="bdc45-177">Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="bdc45-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="bdc45-178">Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 ostukuubis saadaval olnud koondmõõtmiste alamkogum.</span><span class="sxs-lookup"><span data-stu-id="bdc45-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="bdc45-179">Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks.</span><span class="sxs-lookup"><span data-stu-id="bdc45-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="bdc45-180">Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="bdc45-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="bdc45-181">Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisu alusena.</span><span class="sxs-lookup"><span data-stu-id="bdc45-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="bdc45-182">Üksus</span><span class="sxs-lookup"><span data-stu-id="bdc45-182">Entity</span></span>        | <span data-ttu-id="bdc45-183">Peamised koondmõõtmised</span><span class="sxs-lookup"><span data-stu-id="bdc45-183">Key aggregate measurements</span></span> | <span data-ttu-id="bdc45-184">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="bdc45-184">Data source</span></span>                                 | <span data-ttu-id="bdc45-185">Väli</span><span class="sxs-lookup"><span data-stu-id="bdc45-185">Field</span></span>              | <span data-ttu-id="bdc45-186">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bdc45-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="bdc45-187">Arve read</span><span class="sxs-lookup"><span data-stu-id="bdc45-187">Invoice lines</span></span> | <span data-ttu-id="bdc45-188">Ost</span><span class="sxs-lookup"><span data-stu-id="bdc45-188">Purchase</span></span>                   | <span data-ttu-id="bdc45-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="bdc45-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="bdc45-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="bdc45-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="bdc45-191">Summa arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="bdc45-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="bdc45-192">Järgmises tabelis on antud peamised mõõtmised, mis arvutatakse sisupaketis arve ridade üksusest.</span><span class="sxs-lookup"><span data-stu-id="bdc45-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="bdc45-193">Mõõt</span><span class="sxs-lookup"><span data-stu-id="bdc45-193">Measure</span></span>               | <span data-ttu-id="bdc45-194">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="bdc45-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc45-195">Jooksva aasta ostud</span><span class="sxs-lookup"><span data-stu-id="bdc45-195">Purchase current year</span></span> | <span data-ttu-id="bdc45-196">Jooksva aasta ostud = SUM('Arve read'\[Ost\])</span><span class="sxs-lookup"><span data-stu-id="bdc45-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="bdc45-197">Eelmise aasta ostud</span><span class="sxs-lookup"><span data-stu-id="bdc45-197">Purchase last year</span></span>    | <span data-ttu-id="bdc45-198">Eelmise aasta ostud = CALCULATE(SUM('Arve read'\[Ost\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\]))</span><span class="sxs-lookup"><span data-stu-id="bdc45-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="bdc45-199">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="bdc45-199">YOY purchase growth</span></span>   | <span data-ttu-id="bdc45-200">YOY ostude kasv = \[Jooksva aasta ostud\] – \[Eelmise aasta ostud\]</span><span class="sxs-lookup"><span data-stu-id="bdc45-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="bdc45-201">Järgmisi sisu põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate saamiseks.</span><span class="sxs-lookup"><span data-stu-id="bdc45-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="bdc45-202">Üksus</span><span class="sxs-lookup"><span data-stu-id="bdc45-202">Entity</span></span>                 | <span data-ttu-id="bdc45-203">Atribuutide näited</span><span class="sxs-lookup"><span data-stu-id="bdc45-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="bdc45-204">Hankijad</span><span class="sxs-lookup"><span data-stu-id="bdc45-204">Vendors</span></span>                | <span data-ttu-id="bdc45-205">Hankijagrupid, Hankija riik või regioonid, Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="bdc45-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="bdc45-206">Tooted</span><span class="sxs-lookup"><span data-stu-id="bdc45-206">Products</span></span>               | <span data-ttu-id="bdc45-207">Tootenumber, Toote nimi, Kaubagruppide nimi</span><span class="sxs-lookup"><span data-stu-id="bdc45-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="bdc45-208">Hankekategooriad</span><span class="sxs-lookup"><span data-stu-id="bdc45-208">Procurement categories</span></span> | <span data-ttu-id="bdc45-209">Hankekategooria, Hankekategooria nimed</span><span class="sxs-lookup"><span data-stu-id="bdc45-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="bdc45-210">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="bdc45-210">Legal entities</span></span>         | <span data-ttu-id="bdc45-211">Juriidilise isiku nimi</span><span class="sxs-lookup"><span data-stu-id="bdc45-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="bdc45-212">Kuupäevad</span><span class="sxs-lookup"><span data-stu-id="bdc45-212">Dates</span></span>                  | <span data-ttu-id="bdc45-213">Kuupäevad, Aasta vastaskonto</span><span class="sxs-lookup"><span data-stu-id="bdc45-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="bdc45-214">Vaikimisi näitab sisu jooksva kalendriaasta andmeid.</span><span class="sxs-lookup"><span data-stu-id="bdc45-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="bdc45-215">Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises.</span><span class="sxs-lookup"><span data-stu-id="bdc45-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="bdc45-216">Saate muuta ka ettevõtte filtrit.</span><span class="sxs-lookup"><span data-stu-id="bdc45-216">You can also change the company filter.</span></span>
