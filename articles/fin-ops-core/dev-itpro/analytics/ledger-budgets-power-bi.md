---
title: Power BI sisu Tegelik võrreldes eelarvega
description: Selles teemas kirjeldatakse Power BI sisu Tegelik võrreldes eelarvega. See selgitab, kuidas aruannetele juurde pääseda, ja annab andmemudeli kohta teavet.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568569"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="037f0-104">Power BI sisu Tegelik võrreldes eelarvega</span><span class="sxs-lookup"><span data-stu-id="037f0-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="037f0-105">Selles teemas kirjeldatakse **Tegelik võrreldes eelarvega** Microsoft Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="037f0-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="037f0-106">See selgitab ka seda, kuidas pääseda juurde Power BI aruannetele, ning annab teavet andmemudeli ja üksuste kohta, mida kasutatakse sisu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="037f0-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="037f0-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="037f0-107">Overview</span></span>

<span data-ttu-id="037f0-108">Power BI sisu **Tegelik võrreldes** eelarvega on koostatud inimestele, kes vastutavad oma organisatsioonist tegelike tulemuste jälgimise eest eelarvega võrreldes.</span><span class="sxs-lookup"><span data-stu-id="037f0-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="037f0-109">Power BI sisu **Tegelik võrreldes eelarvega** toob nähtavale eelarvehälbed.</span><span class="sxs-lookup"><span data-stu-id="037f0-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="037f0-110">Saate analüüsida jooksva aasta eelarvet kontokategooria, eelarvekoodi, põhikonto, põhikonto kirjelduste või rahandusperioodi järgi, et saada parem ülevaade hälvete põhjusest.</span><span class="sxs-lookup"><span data-stu-id="037f0-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="037f0-111">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="037f0-111">Accessing the Power BI content</span></span>
<span data-ttu-id="037f0-112">Aruanded Power BI sisust **Tegelik võrreldes eelarvega** kuvatakse tööruumides **Pearaamatu eelarved** ja prognoosid ja **CFO**.</span><span class="sxs-lookup"><span data-stu-id="037f0-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="037f0-113">Power BI sisusse kuuluvad aruanded</span><span class="sxs-lookup"><span data-stu-id="037f0-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="037f0-114">Järgmises tabelis on üksikasjad Power BI sisu **Tegelik võrreldes eelarvega** igal aruandelehel leiduvate mõõdikute kohta.</span><span class="sxs-lookup"><span data-stu-id="037f0-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="037f0-115">Aruanne</span><span class="sxs-lookup"><span data-stu-id="037f0-115">Report</span></span>                      | <span data-ttu-id="037f0-116">Mõõdikud</span><span class="sxs-lookup"><span data-stu-id="037f0-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="037f0-117">Kulud – tegelik võrreldes eelarvega</span><span class="sxs-lookup"><span data-stu-id="037f0-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="037f0-118">Selle aasta kulud kokku</span><span class="sxs-lookup"><span data-stu-id="037f0-118">Total expenses this year</span></span></li><li><span data-ttu-id="037f0-119">Selle aasta eelarvekulud kokku</span><span class="sxs-lookup"><span data-stu-id="037f0-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="037f0-120">Tulu – tegelik võrreldes eelarvega</span><span class="sxs-lookup"><span data-stu-id="037f0-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="037f0-121">Selle aasta kogutulu</span><span class="sxs-lookup"><span data-stu-id="037f0-121">Total revenue this year</span></span></li><li><span data-ttu-id="037f0-122">Selle aasta eelarvetulu kokku</span><span class="sxs-lookup"><span data-stu-id="037f0-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="037f0-123">Kulu</span><span class="sxs-lookup"><span data-stu-id="037f0-123">Expense</span></span>                     | <ul><li><span data-ttu-id="037f0-124">Selle aasta kulud kokku</span><span class="sxs-lookup"><span data-stu-id="037f0-124">Total expenses this year</span></span></li><li><span data-ttu-id="037f0-125">Kulude eesmärk eelarve alusel</span><span class="sxs-lookup"><span data-stu-id="037f0-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="037f0-126">Tulu</span><span class="sxs-lookup"><span data-stu-id="037f0-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="037f0-127">Selle aasta kogutulu</span><span class="sxs-lookup"><span data-stu-id="037f0-127">Total revenue this year</span></span></li><li><span data-ttu-id="037f0-128">Tulueesmärk eelarve alusel</span><span class="sxs-lookup"><span data-stu-id="037f0-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="037f0-129">Netotulu</span><span class="sxs-lookup"><span data-stu-id="037f0-129">Net income</span></span>                  | <ul><li><span data-ttu-id="037f0-130">Selle aasta netotulu</span><span class="sxs-lookup"><span data-stu-id="037f0-130">Net income this year</span></span></li><li><span data-ttu-id="037f0-131">Netotulu eesmärk eelarve alusel</span><span class="sxs-lookup"><span data-stu-id="037f0-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="037f0-132">Andmemudelid ja üksused</span><span class="sxs-lookup"><span data-stu-id="037f0-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="037f0-133">Üksus</span><span class="sxs-lookup"><span data-stu-id="037f0-133">Entity</span></span>                    | <span data-ttu-id="037f0-134">Sisu</span><span class="sxs-lookup"><span data-stu-id="037f0-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="037f0-135">Pearaamatu tegevused</span><span class="sxs-lookup"><span data-stu-id="037f0-135">General Ledger Activities</span></span> | <span data-ttu-id="037f0-136">Pearaamatu kandesummad</span><span class="sxs-lookup"><span data-stu-id="037f0-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="037f0-137">Eelarvetegevused</span><span class="sxs-lookup"><span data-stu-id="037f0-137">Budget Activities</span></span>         | <span data-ttu-id="037f0-138">Eelarveregistri kandesummad</span><span class="sxs-lookup"><span data-stu-id="037f0-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="037f0-139">Põhikontod</span><span class="sxs-lookup"><span data-stu-id="037f0-139">Main Accounts</span></span>             | <span data-ttu-id="037f0-140">Põhikontod, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="037f0-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="037f0-141">Rahanduskalendrid</span><span class="sxs-lookup"><span data-stu-id="037f0-141">Fiscal Calendars</span></span>          | <span data-ttu-id="037f0-142">Rahanduskalendrid, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="037f0-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="037f0-143">Pearaamatud</span><span class="sxs-lookup"><span data-stu-id="037f0-143">Ledgers</span></span>                   | <span data-ttu-id="037f0-144">Pearaamatud, mida saab kasutada praeguse pearaamatu aruande filtreerimiseks</span><span class="sxs-lookup"><span data-stu-id="037f0-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="037f0-145">Eelarvekoodid</span><span class="sxs-lookup"><span data-stu-id="037f0-145">Budget Codes</span></span>              | <span data-ttu-id="037f0-146">Eelarvekoodid, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="037f0-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="037f0-147">Juriidilised isikud</span><span class="sxs-lookup"><span data-stu-id="037f0-147">Legal Entities</span></span>            | <span data-ttu-id="037f0-148">Juriidilised isikud, mida saab kasutada praeguse juriidilise isiku aruande filtreerimiseks</span><span class="sxs-lookup"><span data-stu-id="037f0-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]