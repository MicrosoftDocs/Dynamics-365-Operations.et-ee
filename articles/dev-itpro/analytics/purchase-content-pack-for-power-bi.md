---
title: "Ostukulutuste analüüsi Power BI sisu"
description: "See teema kirjeldab, mida hõlmab ostukulutuste analüüsi Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutatakse."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 37f3b1b4d362bd8b40977648b4aa4387011eea08
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="e17f0-104">Ostukulutuste analüüsi Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="e17f0-104">Purchase spend analysis Power BI content</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="e17f0-105">See teema kirjeldab, mida hõlmab **ostukulutuste analüüsi** Microsoft Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="e17f0-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="e17f0-106">See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e17f0-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="e17f0-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e17f0-107">Overview</span></span>

<span data-ttu-id="e17f0-108">**Ostukulutuste analüüsi** Power BI sisu on mõeldud eelarvete eest vastutavate ostujuhtide ja juhtide abistamiseks ostukulutuste jälgimisel.</span><span class="sxs-lookup"><span data-stu-id="e17f0-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="e17f0-109">Juhid saavad analüüsida ostukulutusi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e17f0-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="e17f0-110">Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)</span><span class="sxs-lookup"><span data-stu-id="e17f0-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="e17f0-111">Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)</span><span class="sxs-lookup"><span data-stu-id="e17f0-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="e17f0-112">Sisu kasutab ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa.</span><span class="sxs-lookup"><span data-stu-id="e17f0-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="e17f0-113">Aruanded tõstavad esile ostukulude muutusi aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="e17f0-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="e17f0-114">Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest.</span><span class="sxs-lookup"><span data-stu-id="e17f0-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="e17f0-115">Lisaks näitavad diagrammid erinevate hankekategooriate ja hankijagruppide kulusid.</span><span class="sxs-lookup"><span data-stu-id="e17f0-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="e17f0-116">Seega saavad kategooria- ja piirkonnajuhid kasutada neid diagramme muutuste tuvastamiseks kulutamiskäitumises.</span><span class="sxs-lookup"><span data-stu-id="e17f0-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="e17f0-117">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="e17f0-117">Accessing the Power BI content</span></span>
<span data-ttu-id="e17f0-118">Power BI sisu **Ostu kulutusanalüüs** kuvatakse lehel **Ostu- ja kulutusanalüüs** (**Hanked** > **Päringud ja aruanded** > **Ostujõudluse analüüs** > **Ostu- ja kulutusanalüüs**).</span><span class="sxs-lookup"><span data-stu-id="e17f0-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="e17f0-119">Power BI sisu hulka kuuluvad mõõdikud</span><span class="sxs-lookup"><span data-stu-id="e17f0-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="e17f0-120">**Ostukulutuste analüüsi** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet.</span><span class="sxs-lookup"><span data-stu-id="e17f0-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="e17f0-121">Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena.</span><span class="sxs-lookup"><span data-stu-id="e17f0-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="e17f0-122">Järgmises tabelis antakse ülevaade visualiseeringutest.</span><span class="sxs-lookup"><span data-stu-id="e17f0-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e17f0-123">Aruandeleht</span><span class="sxs-lookup"><span data-stu-id="e17f0-123">Report page</span></span></th>
<th><span data-ttu-id="e17f0-124">Diagrammid</span><span class="sxs-lookup"><span data-stu-id="e17f0-124">Charts</span></span></th>
<th><span data-ttu-id="e17f0-125">Paanid</span><span class="sxs-lookup"><span data-stu-id="e17f0-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e17f0-126">Ostud hankija alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="e17f0-127">10 tipphankijat ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="e17f0-128">Ostud kokku hankijagrupi/riigi/nime alusel (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="e17f0-129">Ostud hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="e17f0-130">Keskmine ost hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e17f0-131">Koguost</span><span class="sxs-lookup"><span data-stu-id="e17f0-131">Total purchase</span></span></li>
<li><span data-ttu-id="e17f0-132">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="e17f0-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="e17f0-133">Hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="e17f0-133">Total # vendors</span></span></li>
<li><span data-ttu-id="e17f0-134">Aktiivsete hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="e17f0-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e17f0-135">Ostud toodete alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="e17f0-136">Ostud hankekategooria / toote nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="e17f0-137">Ostud hankekategooria / toote nime alusel kokku (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="e17f0-138">10 tipptoodet ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e17f0-139">Toodete arv kokku</span><span class="sxs-lookup"><span data-stu-id="e17f0-139">Total # of products</span></span></li>
<li><span data-ttu-id="e17f0-140">Aktiivsete toodete osakaal toodete arvust kokku</span><span class="sxs-lookup"><span data-stu-id="e17f0-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="e17f0-141">Toodete arv, mis annavad 80% ostudest</span><span class="sxs-lookup"><span data-stu-id="e17f0-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e17f0-142">Ostud perioodi alusel\*</span><span class="sxs-lookup"><span data-stu-id="e17f0-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="e17f0-143">Ostud kuu/päeva alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="e17f0-144">Kumulatiivsete ostude YOY hälve (kaskaaddiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="e17f0-145">Ostude YOY kasv kokku (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="e17f0-146">Hankeväljavõte (maatriks)</span><span class="sxs-lookup"><span data-stu-id="e17f0-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="e17f0-147">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="e17f0-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="e17f0-148">YOY ostude kasvu %</span><span class="sxs-lookup"><span data-stu-id="e17f0-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e17f0-149">Ostud hankija asukoha alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="e17f0-150">Ostud linna alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-150">Purchase by city</span></span></li>
<li><span data-ttu-id="e17f0-151">Ostude YOY kasvu %</span><span class="sxs-lookup"><span data-stu-id="e17f0-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="e17f0-152">Ostud riikide järgi</span><span class="sxs-lookup"><span data-stu-id="e17f0-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e17f0-153">Ostukulutuste analüüs aja alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="e17f0-154">Jooksva aasta ostud kuu/päeva alusel (joondiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="e17f0-155">Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="e17f0-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e17f0-156">Ostukulutuste analüüs hankija alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="e17f0-157">10 juhtiva hankija ostude % ostudest (lehter)</span><span class="sxs-lookup"><span data-stu-id="e17f0-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="e17f0-158">10 parimat hankijat suurema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="e17f0-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="e17f0-159">10 parimat hankijat väiksema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="e17f0-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="e17f0-160">\* Selle ja eelmise aasta ostud ja kasv hankekategooriate alusel</span><span class="sxs-lookup"><span data-stu-id="e17f0-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="e17f0-161">Andmemudel ja üksused</span><span class="sxs-lookup"><span data-stu-id="e17f0-161">Data model and entities</span></span>
<span data-ttu-id="e17f0-162">Aruandelehtede täitmiseks **ostukulutuste analüüsi** Power BI sisus kasutatakse järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="e17f0-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="e17f0-163">Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised.</span><span class="sxs-lookup"><span data-stu-id="e17f0-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="e17f0-164">Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas.</span><span class="sxs-lookup"><span data-stu-id="e17f0-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="e17f0-165">Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="e17f0-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="e17f0-166">Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 ostukuubis olnud koondmõõtmiste alamkogum.</span><span class="sxs-lookup"><span data-stu-id="e17f0-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="e17f0-167">Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks.</span><span class="sxs-lookup"><span data-stu-id="e17f0-167">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="e17f0-168">Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="e17f0-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="e17f0-169">Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisu alusena.</span><span class="sxs-lookup"><span data-stu-id="e17f0-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="e17f0-170">Üksus</span><span class="sxs-lookup"><span data-stu-id="e17f0-170">Entity</span></span>        | <span data-ttu-id="e17f0-171">Peamised koondmõõtmised</span><span class="sxs-lookup"><span data-stu-id="e17f0-171">Key aggregate measurements</span></span> | <span data-ttu-id="e17f0-172">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="e17f0-172">Data source</span></span>                                 | <span data-ttu-id="e17f0-173">Väli</span><span class="sxs-lookup"><span data-stu-id="e17f0-173">Field</span></span>              | <span data-ttu-id="e17f0-174">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e17f0-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="e17f0-175">Arve read</span><span class="sxs-lookup"><span data-stu-id="e17f0-175">Invoice lines</span></span> | <span data-ttu-id="e17f0-176">Ost</span><span class="sxs-lookup"><span data-stu-id="e17f0-176">Purchase</span></span>                   | <span data-ttu-id="e17f0-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="e17f0-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="e17f0-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="e17f0-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="e17f0-179">Summa arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="e17f0-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="e17f0-180">Järgmises tabelis on antud peamised mõõtmised, mis arvutatakse sisupaketis arve ridade üksusest.</span><span class="sxs-lookup"><span data-stu-id="e17f0-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="e17f0-181">Mõõt</span><span class="sxs-lookup"><span data-stu-id="e17f0-181">Measure</span></span>               | <span data-ttu-id="e17f0-182">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="e17f0-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e17f0-183">Jooksva aasta ostud</span><span class="sxs-lookup"><span data-stu-id="e17f0-183">Purchase current year</span></span> | <span data-ttu-id="e17f0-184">Jooksva aasta ostud = SUM('Arve read'\[Ost\])</span><span class="sxs-lookup"><span data-stu-id="e17f0-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="e17f0-185">Eelmise aasta ostud</span><span class="sxs-lookup"><span data-stu-id="e17f0-185">Purchase last year</span></span>    | <span data-ttu-id="e17f0-186">Eelmise aasta ostud = CALCULATE(SUM('Arve read'\[Ost\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\]))</span><span class="sxs-lookup"><span data-stu-id="e17f0-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="e17f0-187">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="e17f0-187">YOY purchase growth</span></span>   | <span data-ttu-id="e17f0-188">YOY ostude kasv = \[Jooksva aasta ostud\] – \[Eelmise aasta ostud\]</span><span class="sxs-lookup"><span data-stu-id="e17f0-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="e17f0-189">Järgmisi sisu põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate saamiseks.</span><span class="sxs-lookup"><span data-stu-id="e17f0-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="e17f0-190">Üksus</span><span class="sxs-lookup"><span data-stu-id="e17f0-190">Entity</span></span>                 | <span data-ttu-id="e17f0-191">Atribuutide näited</span><span class="sxs-lookup"><span data-stu-id="e17f0-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="e17f0-192">Hankijad</span><span class="sxs-lookup"><span data-stu-id="e17f0-192">Vendors</span></span>                | <span data-ttu-id="e17f0-193">Hankijagrupid, Hankija riik või regioonid, Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="e17f0-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="e17f0-194">Tooted</span><span class="sxs-lookup"><span data-stu-id="e17f0-194">Products</span></span>               | <span data-ttu-id="e17f0-195">Tootenumber, Toote nimi, Kaubagruppide nimi</span><span class="sxs-lookup"><span data-stu-id="e17f0-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="e17f0-196">Hankekategooriad</span><span class="sxs-lookup"><span data-stu-id="e17f0-196">Procurement categories</span></span> | <span data-ttu-id="e17f0-197">Hankekategooria, Hankekategooria nimed</span><span class="sxs-lookup"><span data-stu-id="e17f0-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="e17f0-198">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="e17f0-198">Legal entities</span></span>         | <span data-ttu-id="e17f0-199">Juriidilise isiku nimi</span><span class="sxs-lookup"><span data-stu-id="e17f0-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="e17f0-200">Kuupäevad</span><span class="sxs-lookup"><span data-stu-id="e17f0-200">Dates</span></span>                  | <span data-ttu-id="e17f0-201">Kuupäevad, Aasta vastaskonto</span><span class="sxs-lookup"><span data-stu-id="e17f0-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="e17f0-202">Vaikimisi näitab sisu jooksva kalendriaasta andmeid.</span><span class="sxs-lookup"><span data-stu-id="e17f0-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="e17f0-203">Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises.</span><span class="sxs-lookup"><span data-stu-id="e17f0-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="e17f0-204">Saate muuta ka ettevõtte filtrit.</span><span class="sxs-lookup"><span data-stu-id="e17f0-204">You can also change the company filter.</span></span>

