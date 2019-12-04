---
title: Power BI sisu Tegelik võrreldes eelarvega
description: Selles teemas kirjeldatakse Power BI sisu Tegelik võrreldes eelarvega. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a577ab24aaf86c1f7a22953e03f397a2e8213c78
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184389"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="b8b45-104">Power BI sisu Tegelik võrreldes eelarvega</span><span class="sxs-lookup"><span data-stu-id="b8b45-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8b45-105">Selles teemas kirjeldatakse Microsoft Power BI sisu **Tegelik võrreldes eelarvega**.</span><span class="sxs-lookup"><span data-stu-id="b8b45-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="b8b45-106">See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b8b45-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b8b45-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b8b45-107">Overview</span></span>

<span data-ttu-id="b8b45-108">Power BI sisu **Tegelik võrreldes** eelarvega on koostatud inimestele, kes vastutavad oma organisatsioonist tegelike tulemuste jälgimise eest eelarvega võrreldes.</span><span class="sxs-lookup"><span data-stu-id="b8b45-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="b8b45-109">Power BI sisu **Tegelik võrreldes eelarvega** toob nähtavale eelarvehälbed.</span><span class="sxs-lookup"><span data-stu-id="b8b45-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="b8b45-110">Saate analüüsida jooksva aasta eelarvet kontokategooria, eelarvekoodi, põhikonto, põhikonto kirjelduste või rahandusperioodi järgi, et saada parem ülevaade hälvete põhjusest.</span><span class="sxs-lookup"><span data-stu-id="b8b45-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b8b45-111">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="b8b45-111">Accessing the Power BI content</span></span>
<span data-ttu-id="b8b45-112">Aruanded Power BI sisust **Tegelik võrreldes eelarvega** kuvatakse tööruumides **Pearaamatu eelarved** ja prognoosid ja **CFO**.</span><span class="sxs-lookup"><span data-stu-id="b8b45-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b8b45-113">Power BI sisusse kuuluvad aruanded</span><span class="sxs-lookup"><span data-stu-id="b8b45-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="b8b45-114">Järgmises tabelis on üksikasjad Power BI sisu **Tegelik võrreldes eelarvega** igal aruandelehel leiduvate mõõdikute kohta.</span><span class="sxs-lookup"><span data-stu-id="b8b45-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="b8b45-115">Aruanne</span><span class="sxs-lookup"><span data-stu-id="b8b45-115">Report</span></span>                      | <span data-ttu-id="b8b45-116">Mõõdikud</span><span class="sxs-lookup"><span data-stu-id="b8b45-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b8b45-117">Kulud – tegelik võrreldes eelarvega</span><span class="sxs-lookup"><span data-stu-id="b8b45-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="b8b45-118">Selle aasta kulud kokku</span><span class="sxs-lookup"><span data-stu-id="b8b45-118">Total expenses this year</span></span></li><li><span data-ttu-id="b8b45-119">Selle aasta eelarvekulud kokku</span><span class="sxs-lookup"><span data-stu-id="b8b45-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="b8b45-120">Tulu – tegelik võrreldes eelarvega</span><span class="sxs-lookup"><span data-stu-id="b8b45-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="b8b45-121">Selle aasta kogutulu</span><span class="sxs-lookup"><span data-stu-id="b8b45-121">Total revenue this year</span></span></li><li><span data-ttu-id="b8b45-122">Selle aasta eelarvetulu kokku</span><span class="sxs-lookup"><span data-stu-id="b8b45-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="b8b45-123">Kulu</span><span class="sxs-lookup"><span data-stu-id="b8b45-123">Expense</span></span>                     | <ul><li><span data-ttu-id="b8b45-124">Selle aasta kulud kokku</span><span class="sxs-lookup"><span data-stu-id="b8b45-124">Total expenses this year</span></span></li><li><span data-ttu-id="b8b45-125">Kulude eesmärk eelarve alusel</span><span class="sxs-lookup"><span data-stu-id="b8b45-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="b8b45-126">Tulu</span><span class="sxs-lookup"><span data-stu-id="b8b45-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="b8b45-127">Selle aasta kogutulu</span><span class="sxs-lookup"><span data-stu-id="b8b45-127">Total revenue this year</span></span></li><li><span data-ttu-id="b8b45-128">Tulueesmärk eelarve alusel</span><span class="sxs-lookup"><span data-stu-id="b8b45-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="b8b45-129">Netotulu</span><span class="sxs-lookup"><span data-stu-id="b8b45-129">Net income</span></span>                  | <ul><li><span data-ttu-id="b8b45-130">Selle aasta netotulu</span><span class="sxs-lookup"><span data-stu-id="b8b45-130">Net income this year</span></span></li><li><span data-ttu-id="b8b45-131">Netotulu eesmärk eelarve alusel</span><span class="sxs-lookup"><span data-stu-id="b8b45-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="b8b45-132">Andmemudelid ja üksused</span><span class="sxs-lookup"><span data-stu-id="b8b45-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="b8b45-133">Üksus</span><span class="sxs-lookup"><span data-stu-id="b8b45-133">Entity</span></span>                    | <span data-ttu-id="b8b45-134">Sisu</span><span class="sxs-lookup"><span data-stu-id="b8b45-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b8b45-135">Pearaamatu tegevused</span><span class="sxs-lookup"><span data-stu-id="b8b45-135">General Ledger Activities</span></span> | <span data-ttu-id="b8b45-136">Pearaamatu kandesummad</span><span class="sxs-lookup"><span data-stu-id="b8b45-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="b8b45-137">Eelarvetegevused</span><span class="sxs-lookup"><span data-stu-id="b8b45-137">Budget Activities</span></span>         | <span data-ttu-id="b8b45-138">Eelarveregistri kandesummad</span><span class="sxs-lookup"><span data-stu-id="b8b45-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="b8b45-139">Põhikontod</span><span class="sxs-lookup"><span data-stu-id="b8b45-139">Main Accounts</span></span>             | <span data-ttu-id="b8b45-140">Põhikontod, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="b8b45-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="b8b45-141">Rahanduskalendrid</span><span class="sxs-lookup"><span data-stu-id="b8b45-141">Fiscal Calendars</span></span>          | <span data-ttu-id="b8b45-142">Rahanduskalendrid, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="b8b45-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="b8b45-143">Pearaamatud</span><span class="sxs-lookup"><span data-stu-id="b8b45-143">Ledgers</span></span>                   | <span data-ttu-id="b8b45-144">Pearaamatud, mida saab kasutada praeguse pearaamatu aruande filtreerimiseks</span><span class="sxs-lookup"><span data-stu-id="b8b45-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="b8b45-145">Eelarvekoodid</span><span class="sxs-lookup"><span data-stu-id="b8b45-145">Budget Codes</span></span>              | <span data-ttu-id="b8b45-146">Eelarvekoodid, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="b8b45-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="b8b45-147">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="b8b45-147">Legal Entities</span></span>            | <span data-ttu-id="b8b45-148">Juriidilised isikud, mida saab kasutada praeguse juriidilise isiku aruande filtreerimiseks</span><span class="sxs-lookup"><span data-stu-id="b8b45-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |