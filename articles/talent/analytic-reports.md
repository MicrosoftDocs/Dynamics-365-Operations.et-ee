---
title: Analüüsiaruannete kasutamine rakenduses Microsoft Dynamics 365 for Talent - Attract
description: Selles teemas kirjeldatakse analüüsiaruandeid värbamisprotsessi ülevaate saamiseks rakenduses Microsoft Dynamics 365 for Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: f69c45e885d789d05a081064f30ccd6ce6bfec52
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742884"
---
# <a name="use-analytic-reports"></a><span data-ttu-id="451fa-103">Analüütiliste aruannete kasutamine</span><span class="sxs-lookup"><span data-stu-id="451fa-103">Use analytic reports</span></span>

<span data-ttu-id="451fa-104">Attracti analüütiliste aruannetega pakutakse valmislahendusi (OOTB) värbamisprotsessi ülevaadete jaoks.</span><span class="sxs-lookup"><span data-stu-id="451fa-104">Analytic reports in Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="451fa-105">Saadaval funktsioonid on:</span><span class="sxs-lookup"><span data-stu-id="451fa-105">Availabe features include:</span></span>

- <span data-ttu-id="451fa-106">**Töö analüüs** – klõpsake **Analüüsi** vahekaardil tööle, et näha ttöökoha kandidaatide mõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="451fa-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="451fa-107">**Analüüsi keskus** – klõpsake **Analüüs** vasakul navigeerimispaanil tööde kohta koondmõõdikute nägemiseks.</span><span class="sxs-lookup"><span data-stu-id="451fa-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="451fa-108">**Kasutajapõhine turvalisus** – Attract haldab aruannetele juurdepääsu [rolli](security-attract.md) ja töö osaleja rolli.</span><span class="sxs-lookup"><span data-stu-id="451fa-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="451fa-109">**Ristfiltreerimine** – klõpsake aruande visuaale, et vaadata valitud andmete alusel filtreeritud muid mõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="451fa-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="451fa-110">See funktsioon on praegu [eelvaateversioonis](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="451fa-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="451fa-111">Selle proovimiseks peab teil olema [**tervikliku värbamise lisandmoodul.**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="451fa-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="451fa-112">Kõik avalikud eelvaate aruanded kuvatakse inglise keeles.</span><span class="sxs-lookup"><span data-stu-id="451fa-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="451fa-113">Aruandeid värskendatakse iga kolme tunni järel.</span><span class="sxs-lookup"><span data-stu-id="451fa-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="451fa-114">Viimane värskendamisaeg (kohalikus ajavööndis) asub aruande ülaosas.</span><span class="sxs-lookup"><span data-stu-id="451fa-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="451fa-115">Värskendamise ajad on ligikaudsed ja varieeruvad vastavalt teie regiooni andmemahu ja ressursi koormusele.</span><span class="sxs-lookup"><span data-stu-id="451fa-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="451fa-116">Tööanalüüs</span><span class="sxs-lookup"><span data-stu-id="451fa-116">Job Analytics</span></span>

<span data-ttu-id="451fa-117">Töö analüüsi aruanne on ülevaade värbamisprotsessist.</span><span class="sxs-lookup"><span data-stu-id="451fa-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="451fa-118">Põhimõõdikud on järgmised.</span><span class="sxs-lookup"><span data-stu-id="451fa-118">Key metrics include:</span></span>

- <span data-ttu-id="451fa-119">Aktiivsed kandidaadid etapi kaupa</span><span class="sxs-lookup"><span data-stu-id="451fa-119">Active applicants by stage</span></span>
- <span data-ttu-id="451fa-120">Kandidaadi allikas</span><span class="sxs-lookup"><span data-stu-id="451fa-120">Applicant source</span></span>
- <span data-ttu-id="451fa-121">Kandidaadi tüüp (sisemine või väline)</span><span class="sxs-lookup"><span data-stu-id="451fa-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="451fa-122">Analüüsi keskus</span><span class="sxs-lookup"><span data-stu-id="451fa-122">Analytics Hub</span></span>

<span data-ttu-id="451fa-123">Analüüsi keskuse aruanded koondavad tööandmeid kõigi tööde kohta, et välja tuua värbamisprotsessi suundumused.</span><span class="sxs-lookup"><span data-stu-id="451fa-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="451fa-124">Attract sisaldab kahte OOTB-aruannet: müügivõimaluste kokkuvõte ja lehtri analüüs.</span><span class="sxs-lookup"><span data-stu-id="451fa-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="451fa-125">Müügivõimaluste kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="451fa-125">Pipeline Summary</span></span>

<span data-ttu-id="451fa-126">Müügivõimaluste kokkuvõtte aruanne koondab avatud tööde andmeid.</span><span class="sxs-lookup"><span data-stu-id="451fa-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="451fa-127">Põhimõõdikud on järgmised.</span><span class="sxs-lookup"><span data-stu-id="451fa-127">Key metrics include:</span></span>

- <span data-ttu-id="451fa-128">Kõikide tööde kandidaadid etapi järgi</span><span class="sxs-lookup"><span data-stu-id="451fa-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="451fa-129">Kandidaadi allikas</span><span class="sxs-lookup"><span data-stu-id="451fa-129">Applicant source</span></span>
- <span data-ttu-id="451fa-130">Avatud tööd staažitaseme järgi</span><span class="sxs-lookup"><span data-stu-id="451fa-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="451fa-131">Lehteranalüüs</span><span class="sxs-lookup"><span data-stu-id="451fa-131">Funnel Analysis</span></span>

<span data-ttu-id="451fa-132">Lehteranalüüsi aruanne koondab andmed tööde kohta, mis on suletud ametikoha täitmise pärast.</span><span class="sxs-lookup"><span data-stu-id="451fa-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="451fa-133">Põhimõõdikud on järgmised.</span><span class="sxs-lookup"><span data-stu-id="451fa-133">Key metrics include:</span></span>

- <span data-ttu-id="451fa-134">Värbamisaeg</span><span class="sxs-lookup"><span data-stu-id="451fa-134">Time to hire</span></span>
- <span data-ttu-id="451fa-135">Mõõdikute teisendus (üle liikumisel)</span><span class="sxs-lookup"><span data-stu-id="451fa-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="451fa-136">Pakkumise vastuvõtmismäär</span><span class="sxs-lookup"><span data-stu-id="451fa-136">Offer acceptance rate</span></span>

<span data-ttu-id="451fa-137">Märkus. Ajaliselt kõige täpsemaks värbamisaruandluseks on soovitatav kasutada [pakkumise halduse](offer-setup.md), funktsiooni, mis on saadaval tervikliku värbamise lisandmooduli osana.</span><span class="sxs-lookup"><span data-stu-id="451fa-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="451fa-138">Lisateabe saamiseks liigutage kursorit visuaalide kohal.</span><span class="sxs-lookup"><span data-stu-id="451fa-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="451fa-139">Näiteks, liikudes üle visuaali **Aktiivses kandidaadid**, kuvatakse keskmine päevade arv etapis.</span><span class="sxs-lookup"><span data-stu-id="451fa-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="451fa-140">Selle teabe analüüsimine võib anda kriitilise tähtsusega ülevaate värbamisaja vähendamiseks ja lubab värbajatel keskenduda meetoditele, milllega vähendada igale etapile kulutatud aega.</span><span class="sxs-lookup"><span data-stu-id="451fa-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="451fa-141">Kasutajapõhine turve</span><span class="sxs-lookup"><span data-stu-id="451fa-141">User-specific security</span></span>

<span data-ttu-id="451fa-142">Attracti aruanded on saadaval administraatori, loe kõike, värbaja ja personalijuhi [rollidele](security-attract.md)-</span><span class="sxs-lookup"><span data-stu-id="451fa-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="451fa-143">Määramata kasutajatel ei ole juurdepääsu kummalegi analüüsiaruannete lehtele, (Töö analüüs või Analüüsi keskus).</span><span class="sxs-lookup"><span data-stu-id="451fa-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="451fa-144">Töö analüüsi aruanded kuvavad andmeid valitud töö kohta.</span><span class="sxs-lookup"><span data-stu-id="451fa-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="451fa-145">Analüüsi keskuse aruanded koondavad andmed kõigi tööde kohta, mida kasutaja saab vaadata.</span><span class="sxs-lookup"><span data-stu-id="451fa-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="451fa-146">Kasutajatele, kes saavad vaadata nii Minu töid kui ka Kõiki töid Tööde lehel, on samad vaated saadaval ka Analüüsi keskuses.</span><span class="sxs-lookup"><span data-stu-id="451fa-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="451fa-147">Ristifilter</span><span class="sxs-lookup"><span data-stu-id="451fa-147">Cross-filter</span></span>

<span data-ttu-id="451fa-148">Üks Power BI suurepärastest funktsioonidest on see, kuidas kõik aruande lehe visuaalid on omavahel ühendatud.</span><span class="sxs-lookup"><span data-stu-id="451fa-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="451fa-149">Kui valite andmepunkti ühe visuaali alusel, siis kõik teised lehel olevad visuaalid, mis sisaldavad samu andmeid, muutuvad tehtud valiku põhjal.</span><span class="sxs-lookup"><span data-stu-id="451fa-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="451fa-150">Vaadake lisateavet ja näidet, [Kuidas visuaalid ristfiltreerivad üksteist Power BI aruandes](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="451fa-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="451fa-151">Excelisse eksportimine</span><span class="sxs-lookup"><span data-stu-id="451fa-151">Export to Excel</span></span>

<span data-ttu-id="451fa-152">Aruande andmete Excelis vaatamiseks klõpsake menüüs Suvandid (kolm punkti) visuaalil ja valige **Alusandmete eksportimine.**</span><span class="sxs-lookup"><span data-stu-id="451fa-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="451fa-153">Eksporditud andmed eksporditakse filtreeritud kujul, austades kasutaja õigusi Attractis.</span><span class="sxs-lookup"><span data-stu-id="451fa-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="451fa-154">Lisateavet vt teemast [Andmete eksportimine visualiseeringutest](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="451fa-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
