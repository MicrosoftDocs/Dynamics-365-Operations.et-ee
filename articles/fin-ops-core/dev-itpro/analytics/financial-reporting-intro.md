---
title: Finantsaruandlus
description: Rahanduse finantsaruandlus võimaldab finants- ja äriprofessionaalidel finantsaruandeid koostada, hallata, juurutada ja kuvada.
author: aprilolson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinanicalReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 68813
ms.assetid: fe8b27e7-a40a-4689-ac6a-7f7401c387f5
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b6682295aa53acd5d3d6964c56ff7bcfcd59379d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568795"
---
# <a name="financial-reporting"></a><span data-ttu-id="03dbd-103">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="03dbd-103">Financial reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03dbd-104">Rakenduse finantsaruandlus võimaldab finants- ja äriprofessionaalidel finantsaruandeid koostada, hallata, juurutada ja kuvada.</span><span class="sxs-lookup"><span data-stu-id="03dbd-104">Financial reporting for the application allows financial and business professionals to create, maintain, deploy, and view financial statements.</span></span> <span data-ttu-id="03dbd-105">See ületab tavapärased aruandluse piirangud, aidates teil tõhusalt mitmesuguseid aruandeid koostada.</span><span class="sxs-lookup"><span data-stu-id="03dbd-105">It moves beyond traditional reporting constraints to help you efficiently design various types of reports.</span></span>

<span data-ttu-id="03dbd-106">Aruandlus hõlmab dimensiooni toetust.</span><span class="sxs-lookup"><span data-stu-id="03dbd-106">Financial reporting includes dimension support.</span></span> <span data-ttu-id="03dbd-107">Seetõttu on kontosegmendid või dimensioonid kohe saadaval.</span><span class="sxs-lookup"><span data-stu-id="03dbd-107">Therefore, account segments or dimensions are immediately available.</span></span> <span data-ttu-id="03dbd-108">Täiendavaid tööriistu ega konfigureerimistoiminguid pole vaja.</span><span class="sxs-lookup"><span data-stu-id="03dbd-108">No additional tools or configuration steps are required.</span></span>

## <a name="financial-reporting-setup"></a><span data-ttu-id="03dbd-109">Finantsaruandluse häälestus</span><span class="sxs-lookup"><span data-stu-id="03dbd-109">Financial reporting setup</span></span>
<span data-ttu-id="03dbd-110">Lehel **Finantsaruandluse häälestus** on kõigi süsteemis olevate finantsdimensioonide loend.</span><span class="sxs-lookup"><span data-stu-id="03dbd-110">The **Financial reporting setup** page has a list of all financial dimensions in the system.</span></span> <span data-ttu-id="03dbd-111">**Pearaamat** \> **Pearaamatu seadistamine** \> **Finantsaruandluse häälestus**.</span><span class="sxs-lookup"><span data-stu-id="03dbd-111">**General ledger** \> **Ledger setup** \> **Financial reporting setup**.</span></span>

<span data-ttu-id="03dbd-112">Lehel **Finantsaruandluse häälestus** on kaks jaotist, mis määratlevad andmeid, mille kohta esitate finantsaruandluses aruandeid:</span><span class="sxs-lookup"><span data-stu-id="03dbd-112">The **Financial reporting setup** page has two sections that determine the data you report on in Financial reporting:</span></span>

- <span data-ttu-id="03dbd-113">**Vahekaart Dimensioonid** – kuna eri ettevõtted kasutavad erinevaid dimensioone ja konto struktuure, ei ole võimalik kindlaks määrata, millises järjekorras kasutajad soovivad kõiki finantsdimensioone aruannetes vaadata.</span><span class="sxs-lookup"><span data-stu-id="03dbd-113">**Dimensions tab** - Because different companies use different dimensions and account structures, there is no way to determine the order in which users want to view all financial dimensions on reports.</span></span> <span data-ttu-id="03dbd-114">Sellel lehel saate määrata, millises järjekorras soovite finantsmõõtmeid kuvada, kui loote ja vaatate finantsaruandluses aruannet.</span><span class="sxs-lookup"><span data-stu-id="03dbd-114">This page allows you set the order in which you want financial dimensions to appear when you build and view a report in Financial reporting.</span></span>
- <span data-ttu-id="03dbd-115">**Vahekaardil Atribuudid** saate valida, kas soovite, et valikuid **Hankijad** ja **Kliendid** saab kasutada atribuutidena filtreerimiseks ja aruande kujundamiseks.</span><span class="sxs-lookup"><span data-stu-id="03dbd-115">**Attributes tab** is where you can select whether you want the ability to use **Vendors** and **Customers** as attributes for filtering and report design.</span></span> <span data-ttu-id="03dbd-116">Tarnija ja kliendi aruandlus on kasulik ainult siis, kui te ei sisesta kannete sisestamisel ühte kandesse mitut tarnijat või klienti.</span><span class="sxs-lookup"><span data-stu-id="03dbd-116">Reporting on Vendor and Customer will only be valuable if you do not enter multiple vendors or customers in a single voucher when posting transactions.</span></span> <span data-ttu-id="03dbd-117">Tarnija ja/või kliendi valimine pikendab integreerimise aega.</span><span class="sxs-lookup"><span data-stu-id="03dbd-117">Choosing Vendor and/or Customer will add additional time to the integration.</span></span>

## <a name="financial-reporting-components"></a><span data-ttu-id="03dbd-118">Finantsaruandluse komponendid</span><span class="sxs-lookup"><span data-stu-id="03dbd-118">Financial reporting components</span></span>
<span data-ttu-id="03dbd-119">Järgmised finantsaruandluse komponendid lihtsustavad aruennete loomist, kuvamist ja plaanimist.</span><span class="sxs-lookup"><span data-stu-id="03dbd-119">The following components of financial reporting make it easy to create, view, and schedule reports.</span></span>

| <span data-ttu-id="03dbd-120">Komponent</span><span class="sxs-lookup"><span data-stu-id="03dbd-120">Component</span></span>        | <span data-ttu-id="03dbd-121">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="03dbd-121">Functions</span></span> | <span data-ttu-id="03dbd-122">Lisateave</span><span class="sxs-lookup"><span data-stu-id="03dbd-122">Additional information</span></span> |
|------------------|-----------|------------------------|
| <span data-ttu-id="03dbd-123">Aruande kujundaja</span><span class="sxs-lookup"><span data-stu-id="03dbd-123">Report Designer</span></span>  | <span data-ttu-id="03dbd-124">Saate luua aruande määratlemiseks ja koostamiseks ühendatavaid aruande koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="03dbd-124">Create report building blocks that can be combined to define and generate a report.</span></span> <span data-ttu-id="03dbd-125">Aruande viisard juhendab vähem kogenud kasutajaid kujunduse protsessis.</span><span class="sxs-lookup"><span data-stu-id="03dbd-125">The report wizard guides less experienced users through the design process.</span></span> <span data-ttu-id="03dbd-126">Edasijõudnud kasutajad saavad luua uued aruande koosteüksused või muuta olemasolevaid koosteüksusi oma vajaduste järgi.</span><span class="sxs-lookup"><span data-stu-id="03dbd-126">Advanced users can create new report building blocks or modify existing building blocks to meet their requirements.</span></span> | |
| <span data-ttu-id="03dbd-127">Aruandegraafikud</span><span class="sxs-lookup"><span data-stu-id="03dbd-127">Report schedules</span></span> | <span data-ttu-id="03dbd-128">Saate plaanida regulaarseks koostamiseks üksiku aruande või aruanderühma.</span><span class="sxs-lookup"><span data-stu-id="03dbd-128">Schedule a single report or a group of reports so that it is generated on a regular basis.</span></span> | [<span data-ttu-id="03dbd-129">Finantsaruannete loomine</span><span class="sxs-lookup"><span data-stu-id="03dbd-129">Generate financial reports</span></span>](generate-financial-report.md) |

## <a name="features"></a><span data-ttu-id="03dbd-130">Funktsioonid</span><span class="sxs-lookup"><span data-stu-id="03dbd-130">Features</span></span>
<table>
<thead>
<tr>
<th><span data-ttu-id="03dbd-131">Funktsioon</span><span class="sxs-lookup"><span data-stu-id="03dbd-131">Feature</span></span></th>
<th><span data-ttu-id="03dbd-132">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="03dbd-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="03dbd-133">Aruande kujunduse paindlikkus</span><span class="sxs-lookup"><span data-stu-id="03dbd-133">Report design flexibility</span></span></td>
<td><span data-ttu-id="03dbd-134">Aruandekoostur pakub aruande koostamisel järgmisi aruandlussuvandeid.</span><span class="sxs-lookup"><span data-stu-id="03dbd-134">Report Designer provides the following reporting options when you design a report:</span></span>
<ul>
<li><span data-ttu-id="03dbd-135">Dimensiooni kombinatsioonide salvestamine ja dimensioonide taaskasutamine mitme aruande puhul.</span><span class="sxs-lookup"><span data-stu-id="03dbd-135">Save dimension combinations, and reuse the dimensions for multiple reports.</span></span></li>
<li><span data-ttu-id="03dbd-136">Dimensiooni kirjelduste vormindamise ja kuvamise juhtimine.</span><span class="sxs-lookup"><span data-stu-id="03dbd-136">Control how dimension descriptions are formatted and displayed.</span></span></li>
<li><span data-ttu-id="03dbd-137">Aruande koosteüksustest välja jäetud kontode või dimensioonide tuvastamine.</span><span class="sxs-lookup"><span data-stu-id="03dbd-137">Identify accounts or dimensions that have been omitted from report building blocks.</span></span></li>
<li><span data-ttu-id="03dbd-138">Jooksvate prognooside päiste vormindamine.</span><span class="sxs-lookup"><span data-stu-id="03dbd-138">Format headers for rolling forecasts.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="03dbd-139">Finantsaruande koostöö</span><span class="sxs-lookup"><span data-stu-id="03dbd-139">Financial report collaboration</span></span></td>
<td><span data-ttu-id="03dbd-140">Järgmised funktsioonid aitavad teil hallata aruannete loomist ja jaotamist.</span><span class="sxs-lookup"><span data-stu-id="03dbd-140">The following features help you manage the generation and distribution of reports:</span></span>
<ul>
<li><span data-ttu-id="03dbd-141">Aruannete plaanimine nende automaatseks loomiseks päeva, nädala, kuu või aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="03dbd-141">Schedule reports so that they are automatically generated on a daily, weekly, monthly, or annual basis.</span></span></li>
<li><span data-ttu-id="03dbd-142">Eksportimine kirjutuskaitstud XPS-vormingusse, mis tagab parema dokumendi turvalisuse digitaalallkirjadele.</span><span class="sxs-lookup"><span data-stu-id="03dbd-142">Export to the read-only XPS format, which provides better document security through digital signatures.</span></span></li>
<li><span data-ttu-id="03dbd-143">Eksportimine Microsoft Exceli töölehele.</span><span class="sxs-lookup"><span data-stu-id="03dbd-143">Export to a Microsoft Excel worksheet.</span></span></li>
<li><span data-ttu-id="03dbd-144">Aruannete jagamiseks saate luua meilisõnumeid, mis sisaldavad linke aruannete juurde.</span><span class="sxs-lookup"><span data-stu-id="03dbd-144">To share reports, you can create email messages that contain links to the reports.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="03dbd-145">Interaktiivne aruande vaatamine</span><span class="sxs-lookup"><span data-stu-id="03dbd-145">Interactive report viewing</span></span></td>
<td><span data-ttu-id="03dbd-146">Interaktiivsed funktsioonid võimaldavad teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="03dbd-146">Interactive features let you perform the following tasks:</span></span>
<ul>
<li><span data-ttu-id="03dbd-147">Kuvatava aruande kuupäeva muutmine.</span><span class="sxs-lookup"><span data-stu-id="03dbd-147">Change the report date for the report that you're viewing.</span></span></li>
<li><span data-ttu-id="03dbd-148">Kuvatava aruande valuuta muutmine.</span><span class="sxs-lookup"><span data-stu-id="03dbd-148">Change the currency of the report that you're viewing.</span></span></li>
<li><span data-ttu-id="03dbd-149">Aruande kuvamine koondvaates või üksikasjavaates.</span><span class="sxs-lookup"><span data-stu-id="03dbd-149">View the report in either a summary view or a detailed view.</span></span></li>
<li><span data-ttu-id="03dbd-150">Dimensioonifiltrite lisamine aruande sisu piiramiseks konkreetse dimensiooni või dimensioonide kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="03dbd-150">Add dimension filters to limit the report content to a specific dimension or combination of dimensions.</span></span></li>
<li><span data-ttu-id="03dbd-151">Atribuudifiltrite lisamine aruande sisu piiramiseks konkreetse atribuudi või atribuutide kombinatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="03dbd-151">Add attribute filters to limit the report content to a specific attribute or combination of attributes.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="03dbd-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="03dbd-152">Additional resources</span></span>
[<span data-ttu-id="03dbd-153">Finantsaruannete loomine</span><span class="sxs-lookup"><span data-stu-id="03dbd-153">Generate financial reports</span></span>](generate-financial-report.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]