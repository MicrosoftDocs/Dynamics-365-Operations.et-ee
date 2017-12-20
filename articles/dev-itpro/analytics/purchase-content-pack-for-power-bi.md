---
title: "Ostukulutuste analüüsi Power BI sisu"
description: "See teema kirjeldab, mida hõlmab ostukulutuste analüüsi Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutatakse."
author: FrankDahl
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
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
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: f38f82b4275599a6b958c495f32b72778b400024
ms.contentlocale: et-ee
ms.lasthandoff: 12/01/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="eaf95-104">Ostukulutuste analüüsi Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="eaf95-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="eaf95-105">See teema kirjeldab, mida hõlmab **ostukulutuste analüüsi** Microsoft Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="eaf95-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="eaf95-106">See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="eaf95-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="eaf95-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="eaf95-107">Overview</span></span>

<span data-ttu-id="eaf95-108">**Ostukulutuste analüüsi** Power BI sisu on mõeldud eelarvete eest vastutavate ostujuhtide ja juhtide abistamiseks ostukulutuste jälgimisel.</span><span class="sxs-lookup"><span data-stu-id="eaf95-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="eaf95-109">Juhid saavad analüüsida ostukulutusi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="eaf95-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="eaf95-110">Aasta seniste ostude summa (hankijarühmade ja eraldi hankijate, tootekategooriate ja eraldi toodete ning hankija asukoha järgi)</span><span class="sxs-lookup"><span data-stu-id="eaf95-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="eaf95-111">Ostmise muutumine aastate lõikes (hankijarühmade ja hankekategooriate järgi)</span><span class="sxs-lookup"><span data-stu-id="eaf95-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="eaf95-112">Sisu kasutab ostukannete andmeid ning annab koondvaate kogu ettevõtte ostunumbritest ja ostukulude jaotuse hankijate ja toodete kaupa.</span><span class="sxs-lookup"><span data-stu-id="eaf95-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="eaf95-113">Aruanded tõstavad esile ostukulude muutusi aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="eaf95-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="eaf95-114">Seega saab neid aruandeid kasutada juhtide teavitamiseks eraldi hankijate ja toodete positiivsetest ning negatiivsetest kulutamistrendidest.</span><span class="sxs-lookup"><span data-stu-id="eaf95-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="eaf95-115">Lisaks näitavad diagrammid erinevate hankekategooriate ja hankijagruppide kulusid.</span><span class="sxs-lookup"><span data-stu-id="eaf95-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="eaf95-116">Seega saavad kategooria- ja piirkonnajuhid kasutada neid diagramme muutuste tuvastamiseks kulutamiskäitumises.</span><span class="sxs-lookup"><span data-stu-id="eaf95-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="eaf95-117">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="eaf95-117">Accessing the Power BI content</span></span>
<span data-ttu-id="eaf95-118">Power BI sisu **Ostu kulutusanalüüs** kuvatakse lehel **Ostu- ja kulutusanalüüs** (**Hanked** > **Päringud ja aruanded** > **Ostujõudluse analüüs** > **Ostu- ja kulutusanalüüs**).</span><span class="sxs-lookup"><span data-stu-id="eaf95-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="eaf95-119">Power BI sisu hulka kuuluvad mõõdikud</span><span class="sxs-lookup"><span data-stu-id="eaf95-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="eaf95-120">**Ostukulutuste analüüsi** Power BI sisu sisaldab mõõdikute kogumist koosnevat aruannet.</span><span class="sxs-lookup"><span data-stu-id="eaf95-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="eaf95-121">Neid mõõdikuid visualiseeritakse diagrammide, paanide ja tabelitena.</span><span class="sxs-lookup"><span data-stu-id="eaf95-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="eaf95-122">Järgmises tabelis antakse ülevaade visualiseeringutest.</span><span class="sxs-lookup"><span data-stu-id="eaf95-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eaf95-123">Aruandeleht</span><span class="sxs-lookup"><span data-stu-id="eaf95-123">Report page</span></span></th>
<th><span data-ttu-id="eaf95-124">Diagrammid</span><span class="sxs-lookup"><span data-stu-id="eaf95-124">Charts</span></span></th>
<th><span data-ttu-id="eaf95-125">Paanid</span><span class="sxs-lookup"><span data-stu-id="eaf95-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="eaf95-126">Ostud hankija alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="eaf95-127">10 tipphankijat ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="eaf95-128">Ostud kokku hankijagrupi/riigi/nime alusel (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="eaf95-129">Ostud hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="eaf95-130">Keskmine ost hankijagrupi/riigi/nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaf95-131">Koguost</span><span class="sxs-lookup"><span data-stu-id="eaf95-131">Total purchase</span></span></li>
<li><span data-ttu-id="eaf95-132">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="eaf95-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="eaf95-133">Hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="eaf95-133">Total # vendors</span></span></li>
<li><span data-ttu-id="eaf95-134">Aktiivsete hankijate arv kokku</span><span class="sxs-lookup"><span data-stu-id="eaf95-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf95-135">Ostud toodete alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="eaf95-136">Ostud hankekategooria / toote nime alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="eaf95-137">Ostud hankekategooria / toote nime alusel kokku (sektordiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="eaf95-138">10 tipptoodet ostu alusel (virntulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaf95-139">Toodete arv kokku</span><span class="sxs-lookup"><span data-stu-id="eaf95-139">Total # of products</span></span></li>
<li><span data-ttu-id="eaf95-140">Aktiivsete toodete osakaal toodete arvust kokku</span><span class="sxs-lookup"><span data-stu-id="eaf95-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="eaf95-141">Toodete arv, mis annavad 80% ostudest</span><span class="sxs-lookup"><span data-stu-id="eaf95-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaf95-142">Ostud perioodi alusel*</span><span class="sxs-lookup"><span data-stu-id="eaf95-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="eaf95-143">Ostud kuu/päeva alusel (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="eaf95-144">Kumulatiivsete ostude YOY hälve (kaskaaddiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="eaf95-145">Ostude YOY kasv kokku (tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="eaf95-146">Hankeväljavõte (maatriks)</span><span class="sxs-lookup"><span data-stu-id="eaf95-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="eaf95-147">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="eaf95-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="eaf95-148">YOY ostude kasvu %</span><span class="sxs-lookup"><span data-stu-id="eaf95-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf95-149">Ostud hankija asukoha alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="eaf95-150">Ostud linna alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-150">Purchase by city</span></span></li>
<li><span data-ttu-id="eaf95-151">Ostude YOY kasvu %</span><span class="sxs-lookup"><span data-stu-id="eaf95-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="eaf95-152">Ostud riikide järgi</span><span class="sxs-lookup"><span data-stu-id="eaf95-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="eaf95-153">Ostukulutuste analüüs aja alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="eaf95-154">Jooksva aasta ostud kuu/päeva alusel (joondiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="eaf95-155">Jooksva ja eelmise aasta ostud (joon- ja tulpdiagramm)</span><span class="sxs-lookup"><span data-stu-id="eaf95-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="eaf95-156">Ostukulutuste analüüs hankija alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="eaf95-157">10 juhtiva hankija ostude % ostudest (lehter)</span><span class="sxs-lookup"><span data-stu-id="eaf95-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="eaf95-158">10 parimat hankijat suurema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="eaf95-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="eaf95-159">10 parimat hankijat väiksema kulutuste YOY-ga</span><span class="sxs-lookup"><span data-stu-id="eaf95-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="eaf95-160">\* Selle ja eelmise aasta ostud ja kasv hankekategooriate alusel</span><span class="sxs-lookup"><span data-stu-id="eaf95-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="eaf95-161">Power BI sisu laiendamine</span><span class="sxs-lookup"><span data-stu-id="eaf95-161">Extending the Power BI content</span></span>
<span data-ttu-id="eaf95-162">Kasutades teenuses Microsoft Dynamics Lifecycle Services (LCS) olevaid sisupakette, saate pakkuda suurepäraseid analüüsivõimalusi inimestele, kes rakendusse Microsoft Dynamics 365 sisse ei logi.</span><span class="sxs-lookup"><span data-stu-id="eaf95-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="eaf95-163">Neid sisupakette saab muuta nii, et need sisaldaksid teisi aruandeid või visuaale, ja avaldada siis sisupaketid analüüsimiseks Power BI.com-i rentnikus.</span><span class="sxs-lookup"><span data-stu-id="eaf95-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="eaf95-164">Power BI sisu **Ostukulutuste analüüs** leiate LCS-i ühiste vahendite teegist.</span><span class="sxs-lookup"><span data-stu-id="eaf95-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="eaf95-165">Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="eaf95-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="eaf95-166">Demo vaatamiseks, mis näitab, kuidas Power BI sisu juurutada, vt [Power BI sisu Microsoftilt ja teie partneritelt teenuses Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) (Office Mix).</span><span class="sxs-lookup"><span data-stu-id="eaf95-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="eaf95-167">Laadige kindlasti alla **ostukulutuste analüüsi** Power BI sisu, mis kehtib teie kasutatava Dynamics 365 versiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="eaf95-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="eaf95-168">Kui kasutate rakenduse Microsoft Dynamics 365 for Finance and Operationsi versiooni 1611, siis on selle Power BI sisu eeltingimus KB 4011327.</span><span class="sxs-lookup"><span data-stu-id="eaf95-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="eaf95-169">Pärast LCS-i sisselogimist pääsete teabebaasiartiklile juurde aadressil https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="eaf95-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="eaf95-170">Andmemudel ja üksused</span><span class="sxs-lookup"><span data-stu-id="eaf95-170">Data model and entities</span></span>
<span data-ttu-id="eaf95-171">Aruandelehtede täitmiseks **ostukulutuste analüüsi** Power BI sisus kasutatakse järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="eaf95-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="eaf95-172">Need andmed on esitatud koondmõõtmistena, mis on üksuse kaupluses etapiviisilised.</span><span class="sxs-lookup"><span data-stu-id="eaf95-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="eaf95-173">Üksuse kauplus on analüüsile optimeeritud Microsoft SQL Serveri andmebaas.</span><span class="sxs-lookup"><span data-stu-id="eaf95-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="eaf95-174">Lisateavet vt teemast [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="eaf95-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="eaf95-175">Selle sisu koondmõõtmised on rakenduste Microsoft Dynamics AX 2012 ja Microsoft Dynamics AX 2012 R3 ostukuubis olnud koondmõõtmiste alamkogum.</span><span class="sxs-lookup"><span data-stu-id="eaf95-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="eaf95-176">Kuubi koondmõõtmiste korraldamiseks üksuse kaupluses tuleb muuta need juurutatavaks.</span><span class="sxs-lookup"><span data-stu-id="eaf95-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="eaf95-177">Lisateavet leiate üksuse kaupluses koondmõõtmiste korraldamise protseduurist ajaveebipostituses [Ülevaade Power BI integratsioonist üksuse kauplusega](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="eaf95-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="eaf95-178">Järgmised peamised koondmõõtmised on saadaval otse arve ridade üksusest ja neid kasutatakse sisu alusena.</span><span class="sxs-lookup"><span data-stu-id="eaf95-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="eaf95-179">Üksus</span><span class="sxs-lookup"><span data-stu-id="eaf95-179">Entity</span></span>        | <span data-ttu-id="eaf95-180">Peamised koondmõõtmised</span><span class="sxs-lookup"><span data-stu-id="eaf95-180">Key aggregate measurements</span></span> | <span data-ttu-id="eaf95-181">Andmeallikas</span><span class="sxs-lookup"><span data-stu-id="eaf95-181">Data source</span></span>                                 | <span data-ttu-id="eaf95-182">Väli</span><span class="sxs-lookup"><span data-stu-id="eaf95-182">Field</span></span>              | <span data-ttu-id="eaf95-183">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="eaf95-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="eaf95-184">Arve read</span><span class="sxs-lookup"><span data-stu-id="eaf95-184">Invoice lines</span></span> | <span data-ttu-id="eaf95-185">Ost</span><span class="sxs-lookup"><span data-stu-id="eaf95-185">Purchase</span></span>                   | <span data-ttu-id="eaf95-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="eaf95-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="eaf95-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="eaf95-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="eaf95-188">Summa arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="eaf95-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="eaf95-189">Järgmises tabelis on antud peamised mõõtmised, mis arvutatakse sisupaketis arve ridade üksusest.</span><span class="sxs-lookup"><span data-stu-id="eaf95-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="eaf95-190">Mõõt</span><span class="sxs-lookup"><span data-stu-id="eaf95-190">Measure</span></span>               | <span data-ttu-id="eaf95-191">Kalkulatsioon</span><span class="sxs-lookup"><span data-stu-id="eaf95-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eaf95-192">Jooksva aasta ostud</span><span class="sxs-lookup"><span data-stu-id="eaf95-192">Purchase current year</span></span> | <span data-ttu-id="eaf95-193">Jooksva aasta ostud = SUM('Arve read'\[Ost\])</span><span class="sxs-lookup"><span data-stu-id="eaf95-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="eaf95-194">Eelmise aasta ostud</span><span class="sxs-lookup"><span data-stu-id="eaf95-194">Purchase last year</span></span>    | <span data-ttu-id="eaf95-195">Eelmise aasta ostud = CALCULATE(SUM('Arve read'\[Ost\]), SAMEPERIODLASTYEAR(Kuupäevad\[Kuupäev\]))</span><span class="sxs-lookup"><span data-stu-id="eaf95-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="eaf95-196">YOY ostude kasv</span><span class="sxs-lookup"><span data-stu-id="eaf95-196">YOY purchase growth</span></span>   | <span data-ttu-id="eaf95-197">YOY ostude kasv = \[Jooksva aasta ostud\] – \[Eelmise aasta ostud\]</span><span class="sxs-lookup"><span data-stu-id="eaf95-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="eaf95-198">Järgmisi sisu põhidimensioone kasutatakse filtritena koondmõõtmiste tükeldamiseks suurema granulaarsuse saavutamiseks ja sügavama analüütilise ülevaate saamiseks.</span><span class="sxs-lookup"><span data-stu-id="eaf95-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="eaf95-199">Üksus</span><span class="sxs-lookup"><span data-stu-id="eaf95-199">Entity</span></span>                 | <span data-ttu-id="eaf95-200">Atribuutide näited</span><span class="sxs-lookup"><span data-stu-id="eaf95-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="eaf95-201">Hankijad</span><span class="sxs-lookup"><span data-stu-id="eaf95-201">Vendors</span></span>                | <span data-ttu-id="eaf95-202">Hankijagrupid, Hankija riik või regioonid, Hankija nimi</span><span class="sxs-lookup"><span data-stu-id="eaf95-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="eaf95-203">Tooted</span><span class="sxs-lookup"><span data-stu-id="eaf95-203">Products</span></span>               | <span data-ttu-id="eaf95-204">Tootenumber, Toote nimi, Kaubagruppide nimi</span><span class="sxs-lookup"><span data-stu-id="eaf95-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="eaf95-205">Hankekategooriad</span><span class="sxs-lookup"><span data-stu-id="eaf95-205">Procurement categories</span></span> | <span data-ttu-id="eaf95-206">Hankekategooria, Hankekategooria nimed</span><span class="sxs-lookup"><span data-stu-id="eaf95-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="eaf95-207">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="eaf95-207">Legal entities</span></span>         | <span data-ttu-id="eaf95-208">Juriidilise isiku nimi</span><span class="sxs-lookup"><span data-stu-id="eaf95-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="eaf95-209">Kuupäevad</span><span class="sxs-lookup"><span data-stu-id="eaf95-209">Dates</span></span>                  | <span data-ttu-id="eaf95-210">Kuupäevad, Aasta vastaskonto</span><span class="sxs-lookup"><span data-stu-id="eaf95-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="eaf95-211">Vaikimisi näitab sisu jooksva kalendriaasta andmeid.</span><span class="sxs-lookup"><span data-stu-id="eaf95-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="eaf95-212">Kuid kuupäevafiltrit saab muuta aruande filtrite jaotises.</span><span class="sxs-lookup"><span data-stu-id="eaf95-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="eaf95-213">Saate muuta ka ettevõtte filtrit.</span><span class="sxs-lookup"><span data-stu-id="eaf95-213">You can also change the company filter.</span></span>

