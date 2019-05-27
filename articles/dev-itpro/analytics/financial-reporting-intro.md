---
title: Finantsaruandlus
description: Finance and Operationsi finantsaruandlus võimaldab finants- ja äriprofessionaalidel finantsaruandeid koostada, hallata, juurutada ja kuvada. See ületab tavapärased aruandluse piirangud, aidates teil tõhusalt mitmesuguseid aruandeid koostada.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: ae2087cf142fc2670bda3c542b336f12978178a6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553892"
---
# <a name="financial-reporting"></a><span data-ttu-id="fc8c9-104">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="fc8c9-104">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc8c9-105">Finance and Operationsi finantsaruandlus võimaldab finants- ja äriprofessionaalidel finantsaruandeid koostada, hallata, juurutada ja kuvada.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-105">Financial reporting for Finance and Operations allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="fc8c9-106">See ületab tavapärased aruandluse piirangud, aidates teil tõhusalt mitmesuguseid aruandeid koostada.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-106">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="fc8c9-107">Aruandlus hõlmab dimensiooni toetust.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-107">Financial reporting includes dimension support.</span></span> <span data-ttu-id="fc8c9-108">Seetõttu on kontosegmendid või dimensioonid kohe saadaval.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-108">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="fc8c9-109">Täiendavaid tööriistu ega konfigureerimistoiminguid pole vaja.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-109">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="fc8c9-110">Finantsaruandluse häälestus</span><span class="sxs-lookup"><span data-stu-id="fc8c9-110">Financial reporting setup</span></span>
<span data-ttu-id="fc8c9-111">Lehel **Finantsaruandluse häälestus** on kõigi süsteemis olevate finantsdimensioonide loend.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-111">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="fc8c9-112">**Pearaamat** \> **Pearaamatu seadistamine** \> **Finantsaruandluse häälestus**.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-112">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="fc8c9-113">Lehel **Finantsaruandluse häälestus** on kaks jaotist, mis määratlevad andmeid, mille kohta esitate finantsaruandluses aruandeid:</span><span class="sxs-lookup"><span data-stu-id="fc8c9-113">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="fc8c9-114">**Vahekaart Dimensioonid** – kuna eri ettevõtted kasutavad erinevaid dimensioone ja konto struktuure, ei ole võimalik kindlaks määrata, millises järjekorras kasutajad soovivad kõiki finantsdimensioone aruannetes vaadata.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-114">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="fc8c9-115">Sellel lehel saate määrata, millises järjekorras soovite finantsmõõtmeid kuvada, kui loote ja vaatate finantsaruandluses aruannet.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-115">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="fc8c9-116">**Vahekaardil Atribuudid** saate valida, kas soovite, et valikuid **Hankijad** ja **Kliendid** saab kasutada atribuutidena filtreerimiseks ja aruande kujundamiseks.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-116">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="fc8c9-117">Tarnija ja kliendi aruandlus on kasulik ainult siis, kui te ei sisesta kannete sisestamisel ühte kandesse mitut tarnijat või klienti.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-117">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="fc8c9-118">Tarnija ja/või kliendi valimine pikendab integreerimise aega.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-118">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="fc8c9-119">Finantsaruandluse komponendid</span><span class="sxs-lookup"><span data-stu-id="fc8c9-119">Financial reporting components</span></span>
<span data-ttu-id="fc8c9-120">Järgmised finantsaruandluse komponendid lihtsustavad aruennete loomist, kuvamist ja plaanimist.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-120">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="fc8c9-121">Komponent</span><span class="sxs-lookup"><span data-stu-id="fc8c9-121">Component</span></span>        | <span data-ttu-id="fc8c9-122">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="fc8c9-122">Functions</span></span> | <span data-ttu-id="fc8c9-123">Lisateave</span><span class="sxs-lookup"><span data-stu-id="fc8c9-123">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="fc8c9-124">Aruande kujundaja</span><span class="sxs-lookup"><span data-stu-id="fc8c9-124">Report Designer</span></span>  | <span data-ttu-id="fc8c9-125">Saate luua aruande määratlemiseks ja koostamiseks ühendatavaid aruande koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-125">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="fc8c9-126">Aruande viisard juhendab vähem kogenud kasutajaid kujunduse protsessis.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-126">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="fc8c9-127">Edasijõudnud kasutajad saavad luua uued aruande koosteüksused või muuta olemasolevaid koosteüksusi oma vajaduste järgi.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-127">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="fc8c9-128">Aruandegraafikud</span><span class="sxs-lookup"><span data-stu-id="fc8c9-128">Report schedules</span></span> | <span data-ttu-id="fc8c9-129">Saate plaanida regulaarseks koostamiseks üksiku aruande või aruanderühma.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-129">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="fc8c9-130">Finantsaruande loomine</span><span class="sxs-lookup"><span data-stu-id="fc8c9-130">Generate a financial report</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="fc8c9-131">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="fc8c9-131">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="fc8c9-132">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="fc8c9-132">Feature</span></span></th>
<th><span data-ttu-id="fc8c9-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fc8c9-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="fc8c9-134">Aruande kujunduse paindlikkus</span><span class="sxs-lookup"><span data-stu-id="fc8c9-134">Report design flexibility</span></span></td>
<td><span data-ttu-id="fc8c9-135">Aruandekoostur pakub aruande koostamisel järgmisi aruandlussuvandeid.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-135">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="fc8c9-136">Dimensiooni kombinatsioonide salvestamine ja dimensioonide taaskasutamine mitme aruande puhul.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-136">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="fc8c9-137">Dimensiooni kirjelduste vormindamise ja kuvamise juhtimine.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-137">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="fc8c9-138">Aruande koosteüksustest välja jäetud kontode või dimensioonide tuvastamine.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-138">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="fc8c9-139">Jooksvate prognooside päiste vormindamine.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-139">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="fc8c9-140">Finantsaruande koostöö</span><span class="sxs-lookup"><span data-stu-id="fc8c9-140">Financial report collaboration</span></span></td>
<td><span data-ttu-id="fc8c9-141">Järgmised funktsioonid aitavad teil hallata aruannete loomist ja jaotamist.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-141">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="fc8c9-142">Aruannete plaanimine nende automaatseks loomiseks päeva, nädala, kuu või aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-142">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="fc8c9-143">Eksportimine kirjutuskaitstud XPS-vormingusse, mis tagab parema dokumendi turvalisuse digitaalallkirjadele.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-143">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="fc8c9-144">Eksportimine Microsoft Exceli töölehele.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-144">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="fc8c9-145">Aruannete jagamiseks saate luua meilisõnumeid, mis sisaldavad linke aruannete juurde.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-145">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="fc8c9-146">Interaktiivne aruande vaatamine</span><span class="sxs-lookup"><span data-stu-id="fc8c9-146">Interactive report viewing</span></span></td>
<td><span data-ttu-id="fc8c9-147">Interaktiivsed funktsioonid võimaldavad teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-147">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="fc8c9-148">Kuvatava aruande kuupäeva muutmine.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-148">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="fc8c9-149">Kuvatava aruande valuuta muutmine.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-149">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="fc8c9-150">Aruande kuvamine koondvaates või üksikasjavaates.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-150">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="fc8c9-151">Dimensioonifiltrite lisamine aruande sisu piiramiseks konkreetse dimensiooni või dimensioonide kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-151">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="fc8c9-152">Atribuudifiltrite lisamine aruande sisu piiramiseks konkreetse atribuudi või atribuutide kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="fc8c9-152">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="fc8c9-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="fc8c9-153">Additional resources</span></span>
[<span data-ttu-id="fc8c9-154">Finantsaruande loomine</span><span class="sxs-lookup"><span data-stu-id="fc8c9-154">Generate a financial report</span></span>](generate-financial-report.md)
