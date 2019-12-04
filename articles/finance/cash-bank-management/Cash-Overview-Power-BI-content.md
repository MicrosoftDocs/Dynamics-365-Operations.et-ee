---
title: Kassa ülevaate Power BI sisu
description: Selles teemas kirjeldatakse kassa ülevaate Power BI sisu. See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.
author: saraschi2
manager: AnnBe
ms.date: 06/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 7621ca961288af81966e0ac883c6525f89960654
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553136"
---
# <a name="cash-overview-power-bi-content"></a><span data-ttu-id="b2eab-104">Kassa ülevaate Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="b2eab-104">Cash overview Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2eab-105">Selles teemas kirjeldatakse **kassa ülevaate** Microsoft Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="b2eab-105">This topic describes the **Cash overview** Microsoft Power BI content.</span></span> <span data-ttu-id="b2eab-106">See selgitab juurdepääsu sisus sisalduvatele aruannetele ning annab teavet andmemudeli ja olemite kohta, mida sisu loomiseks kasutati.</span><span class="sxs-lookup"><span data-stu-id="b2eab-106">It explains how to access the reports that are included in the content, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b2eab-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b2eab-107">Overview</span></span>

<span data-ttu-id="b2eab-108">**Kassa ülevaate** Power BI sisu loodi inimeste jaoks, kes vastutavad oma organisatsioonis sularaha eest.</span><span class="sxs-lookup"><span data-stu-id="b2eab-108">The **Cash overview** Power BI content was created for individuals who are responsible for cash in their organization.</span></span> <span data-ttu-id="b2eab-109">**Kassa ülevaate** Power BI sisu annab ülevaate rahavoogudest.</span><span class="sxs-lookup"><span data-stu-id="b2eab-109">The **Cash overview** Power BI content provides visibility into your cash flow.</span></span> <span data-ttu-id="b2eab-110">Samuti pakub see prognoose, mis aitavad teil teha paremaid otsuseid ja parandavad seeläbi teie rahavoogude seisundit.</span><span class="sxs-lookup"><span data-stu-id="b2eab-110">It also provides forecasts that can help you make better decisions and therefore improve the health of your cash flow.</span></span> <span data-ttu-id="b2eab-111">Saate analüüsida sularaha juriidilise isiku, valuuta ja pangakonto järgi, et ülejääke ja puudujääke paremini mõista.</span><span class="sxs-lookup"><span data-stu-id="b2eab-111">You can analyze cash by legal entity, currency, and bank account to get a better understanding of surpluses and shortfalls.</span></span>

## <a name="setup-needed-to-view-power-bi-content"></a><span data-ttu-id="b2eab-112">Power BI sisu vaatamiseks on vajalik häälestus</span><span class="sxs-lookup"><span data-stu-id="b2eab-112">Setup needed to view Power BI content</span></span>

<span data-ttu-id="b2eab-113">Järgmine seadistus tuleb lõpule viia, et kuvada andmeid **Sularaha ülevaade** ja **Panga juhtkond** Power BI visuaalides.</span><span class="sxs-lookup"><span data-stu-id="b2eab-113">The following setup needs to be completed in order for data to display in **Cash overview** and **Bank management** Power BI visuals.</span></span>

1. <span data-ttu-id="b2eab-114">Avage **Süsteemihaldus > Seadistamine > Süsteemi parameetrid**, et määrata **Süsteemi valuuta** ja **Süsteemi vahetuskurss**.</span><span class="sxs-lookup"><span data-stu-id="b2eab-114">Go to **System administration > Setup > System Parameters** to set **System currency** and **System Exchange Rate**.</span></span>
2. <span data-ttu-id="b2eab-115">Avage **Üldine pearaamat > Seadistus > Pearaamat**, et seadistada **Raamatupidamise valuutat** ja **Vahetuskursi tüüpi**.</span><span class="sxs-lookup"><span data-stu-id="b2eab-115">Go to **General Ledger > Setup > Ledger** to set **Accounting Currency** and **Exchange Rate Type**.</span></span>
2. <span data-ttu-id="b2eab-116">Määratlege vahetuskursid kannete valuutade ja arvestusvaluuta, raamatupidamise valuuta ja süsteemi valuuta ning raamatupidamise valuuta ja panga valuutade vahel.</span><span class="sxs-lookup"><span data-stu-id="b2eab-116">Define exchange rates between Transaction currencies and Accounting currency, Accounting currency and System currency, and Accounting currency and Bank currencies.</span></span> <span data-ttu-id="b2eab-117">Selleks avage **Pearaamat > Valuutad > Valuutakursid**.</span><span class="sxs-lookup"><span data-stu-id="b2eab-117">To do this, go **General Ledger > Currencies > Currency exchange rates**.</span></span>
3. <span data-ttu-id="b2eab-118">Konfigureerige ja käivitage likviidsuse planeerimine.</span><span class="sxs-lookup"><span data-stu-id="b2eab-118">Configure and run Cash Flow Forecasting.</span></span> <span data-ttu-id="b2eab-119">Lisainfo saamiseks likviidsuse planeerimise kohta vt [Likviidsuse planeerimine](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span><span class="sxs-lookup"><span data-stu-id="b2eab-119">For more information about how to set up Cash flow forecasting, see [Cash flow forecasting](https://docs.microsoft.com/dynamics365/finance/cash-bank-management/cash-flow-forecasting).</span></span> 
4. <span data-ttu-id="b2eab-120">Avage **Süsteemihaldus > Seadistamine > Üksuse kauplus**, et värskendada **LedgerCovLiquidityMeasurement** koondmõõtmist.</span><span class="sxs-lookup"><span data-stu-id="b2eab-120">Go to **System administration > Setup > Entity Store** to refresh the **LedgerCovLiquidityMeasurement** aggregate measurement.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b2eab-121">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="b2eab-121">Accessing the Power BI content</span></span>

<span data-ttu-id="b2eab-122">Aruanded **kassa ülevaate** Power BI sisust kuvatakse tööruumides **Kassa ülevaade** ja **Pangahaldus**.</span><span class="sxs-lookup"><span data-stu-id="b2eab-122">Reports from the **Cash overview** Power BI content are displayed in the **Cash overview** and **Bank management** workspaces.</span></span>

<span data-ttu-id="b2eab-123">Likviidsuse plaanimise aruannete kuvamiseks koos andmetega peate esmalt käivitama prognoosiarvutusprotsessi, kasutades funktsiooni **Likviidsuse plaanimiste arvutamine** alal Sularaha- ja pangahaldus.</span><span class="sxs-lookup"><span data-stu-id="b2eab-123">To view the Cash flow forecasting reports with data, you must first run the forecast calculation process using the **Calculate cash flow forecasts** function from the Cash and bank management area.</span></span> <span data-ttu-id="b2eab-124">Seda tuleb teha iga prognoosi kaasatava ettevõtte puhul.</span><span class="sxs-lookup"><span data-stu-id="b2eab-124">This needs to be completed for each company included in the forecast.</span></span>  <span data-ttu-id="b2eab-125">Seejärel peate värskendama atribuudi LedgerCovLiquidityMeasurement koondmõõtmist lehel **Üksuse kauplus**.</span><span class="sxs-lookup"><span data-stu-id="b2eab-125">You then need to refresh the LedgerCovLiquidityMeasurement aggregate measurement on the **Entity Store** page.</span></span>  

<span data-ttu-id="b2eab-126">Demoeesmärgil saate lisada likviidsuse plaanimise demoandmed, kasutades mooduli Demoandmed lehte **Andmete loomine**.</span><span class="sxs-lookup"><span data-stu-id="b2eab-126">For demonstration purposes, you can add cash flow forecasting demo data using the **Generate data** page from the Demo data module.</span></span>  <span data-ttu-id="b2eab-127">See skript sisestab andmed likviidsuse plaanimise tabelitesse, et aruannete jaoks vajalikku teavet kiiresti sisestada.</span><span class="sxs-lookup"><span data-stu-id="b2eab-127">This script will insert data into the cash flow forecasting tables to quickly populate information necessary for reports.</span></span>  <span data-ttu-id="b2eab-128">See moodul on saadaval ainult siis, kui teie keskkonnas on juurutatud demoandmete komplekti moodul.</span><span class="sxs-lookup"><span data-stu-id="b2eab-128">This module is only available if you have the Demo data suite model deployed on the environment.</span></span> 

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b2eab-129">Power BI sisusse kuuluvad aruanded</span><span class="sxs-lookup"><span data-stu-id="b2eab-129">Reports that are included in the Power BI content</span></span>

<span data-ttu-id="b2eab-130">Järgmises tabelis on üksikasjad **kassa ülevaate** Power BI sisu igal aruandelehel leiduvate mõõdikute kohta.</span><span class="sxs-lookup"><span data-stu-id="b2eab-130">The following table provides details about the metrics that are found on each report page in the **Cash overview** Power BI content.</span></span>

| <span data-ttu-id="b2eab-131">Aruanne</span><span class="sxs-lookup"><span data-stu-id="b2eab-131">Report</span></span>                                | <span data-ttu-id="b2eab-132">Sisu</span><span class="sxs-lookup"><span data-stu-id="b2eab-132">Contents</span></span> |
|---------------------------------------|----------|
| <span data-ttu-id="b2eab-133">Kassa ülevaade – kõik ettevõtted</span><span class="sxs-lookup"><span data-stu-id="b2eab-133">Cash overview – all companies</span></span>         | <ul><li><span data-ttu-id="b2eab-134">Sissetulekud ja väljaminekud süsteemi valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-134">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="b2eab-135">Prognoositud valuutasaldod</span><span class="sxs-lookup"><span data-stu-id="b2eab-135">Forecasted currency balances</span></span></li><li><span data-ttu-id="b2eab-136">Kogu pangasaldo süsteemi valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-136">Total bank balance in system currency</span></span></li><li><span data-ttu-id="b2eab-137">Saldo juriidilise isiku järgi</span><span class="sxs-lookup"><span data-stu-id="b2eab-137">Balance by legal entity</span></span></li><li><span data-ttu-id="b2eab-138">Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-138">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="b2eab-139">Kassa ülevaade – praegune ettevõte</span><span class="sxs-lookup"><span data-stu-id="b2eab-139">Cash overview – current company</span></span>       | <ul><li><span data-ttu-id="b2eab-140">Sissetulekud ja väljaminekud arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-140">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="b2eab-141">Prognoositud valuutasaldod</span><span class="sxs-lookup"><span data-stu-id="b2eab-141">Forecasted currency balances</span></span></li><li><span data-ttu-id="b2eab-142">Kogu pangasaldo arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-142">Total bank balance in accounting currency</span></span></li><li><span data-ttu-id="b2eab-143">Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-143">Today’s actual vs forecasted balance in bank account currency</span></span></li></ul> |
| <span data-ttu-id="b2eab-144">Likviidsuse plaanimine – kõik ettevõtted</span><span class="sxs-lookup"><span data-stu-id="b2eab-144">Cash flow forecast – all companies</span></span>    | <ul><li><span data-ttu-id="b2eab-145">Sissetulekud ja väljaminekud süsteemi valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-145">Inflows and outflows in system currency</span></span></li><li><span data-ttu-id="b2eab-146">Päevaprognoosi kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="b2eab-146">Daily forecast summary</span></span></li><li><span data-ttu-id="b2eab-147">Prognoosi andmed</span><span class="sxs-lookup"><span data-stu-id="b2eab-147">Forecast details</span></span></li></ul> |
| <span data-ttu-id="b2eab-148">Likviidsuse plaanimine – ettevõtte valuuta</span><span class="sxs-lookup"><span data-stu-id="b2eab-148">Cash flow forecast – currency company</span></span> | <ul><li><span data-ttu-id="b2eab-149">Sissetulekud ja väljaminekud arvestusvaluutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-149">Inflows and outflows in accounting currency</span></span></li><li><span data-ttu-id="b2eab-150">Päevaprognoosi kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="b2eab-150">Daily forecast summary</span></span></li><li><span data-ttu-id="b2eab-151">Prognoosi andmed</span><span class="sxs-lookup"><span data-stu-id="b2eab-151">Forecast details</span></span></li></ul> |
| <span data-ttu-id="b2eab-152">Valuutaprognoos</span><span class="sxs-lookup"><span data-stu-id="b2eab-152">Currency forecast</span></span>                     | <ul><li><span data-ttu-id="b2eab-153">Prognoositud valuutasaldod</span><span class="sxs-lookup"><span data-stu-id="b2eab-153">Forecasted currency balances</span></span></li><li><span data-ttu-id="b2eab-154">Igapäevane valuuta kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="b2eab-154">Daily currency summary</span></span></li><li><span data-ttu-id="b2eab-155">Prognoosi andmed</span><span class="sxs-lookup"><span data-stu-id="b2eab-155">Forecast details</span></span></li></ul> |
| <span data-ttu-id="b2eab-156">Pangasaldod</span><span class="sxs-lookup"><span data-stu-id="b2eab-156">Bank balances</span></span>                         | <ul><li><span data-ttu-id="b2eab-157">Kogu pangasaldo süsteemi valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-157">Total bank balance in system currency</span></span></li><li><span data-ttu-id="b2eab-158">Saldo juriidilise isiku järgi</span><span class="sxs-lookup"><span data-stu-id="b2eab-158">Balance by legal entity</span></span></li><li><span data-ttu-id="b2eab-159">Tänane tegelik saldo võrreldes prognoositava saldoga pangakonto valuutas</span><span class="sxs-lookup"><span data-stu-id="b2eab-159">Today’s actual vs forecasted balance in bank account currency</span></span></li><li><span data-ttu-id="b2eab-160">Saldo pangakonto järgi</span><span class="sxs-lookup"><span data-stu-id="b2eab-160">Balance by bank account</span></span></li><li><span data-ttu-id="b2eab-161">Saldo valuuta järgi</span><span class="sxs-lookup"><span data-stu-id="b2eab-161">Balance by currency</span></span></li></ul> |


## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="b2eab-162">Andmemudelid ja üksused</span><span class="sxs-lookup"><span data-stu-id="b2eab-162">Understanding the data model and entities</span></span>

<span data-ttu-id="b2eab-163">Järgmises tabelis on näidatud üksused, millel **kassa ülevaate** Power BI sisu põhineb.</span><span class="sxs-lookup"><span data-stu-id="b2eab-163">The following table shows the entities that the **Cash overview** Power BI content is based on.</span></span>

| <span data-ttu-id="b2eab-164">Üksus</span><span class="sxs-lookup"><span data-stu-id="b2eab-164">Entity</span></span>                                                                          | <span data-ttu-id="b2eab-165">Sisu</span><span class="sxs-lookup"><span data-stu-id="b2eab-165">Contents</span></span> |
|---------------------------------------------------------------------------------|----------|
| <span data-ttu-id="b2eab-166">LedgerCovLiquidityMeasurement\_ettevõte</span><span class="sxs-lookup"><span data-stu-id="b2eab-166">LedgerCovLiquidityMeasurement\_Company</span></span>                                          | <span data-ttu-id="b2eab-167">Ettevõtted, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="b2eab-167">Companies to filter reports by</span></span> |
| <span data-ttu-id="b2eab-168">LedgerCovLiquidityMeasurement\_Kuupäev</span><span class="sxs-lookup"><span data-stu-id="b2eab-168">LedgerCovLiquidityMeasurement\_Date</span></span>                                             | <span data-ttu-id="b2eab-169">Kuupäevad, mille alusel aruandeid filtreerida</span><span class="sxs-lookup"><span data-stu-id="b2eab-169">Dates to filter reports by</span></span> |
| <span data-ttu-id="b2eab-170">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span><span class="sxs-lookup"><span data-stu-id="b2eab-170">LedgerCovLiquidityMeasurement\_LedgerCovForecastActual</span></span>                          | <span data-ttu-id="b2eab-171">Tegelikud pangasaldod vs viimati prognoositud pangasaldo</span><span class="sxs-lookup"><span data-stu-id="b2eab-171">Actual bank balance vs last forecasted bank balance</span></span> |
| <span data-ttu-id="b2eab-172">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span><span class="sxs-lookup"><span data-stu-id="b2eab-172">LedgerCovLiquidityMeasurement\_LedgerCovLiquidity</span></span>                               | <span data-ttu-id="b2eab-173">Prognoositud kande üksikasjad</span><span class="sxs-lookup"><span data-stu-id="b2eab-173">Forecasted transaction details</span></span> |
| <span data-ttu-id="b2eab-174">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span><span class="sxs-lookup"><span data-stu-id="b2eab-174">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany</span></span>    | <span data-ttu-id="b2eab-175">Summeeritud sularaha sissetulekud ja väljaminekud, kasutades iga ettevõtte arvestusvaluutat</span><span class="sxs-lookup"><span data-stu-id="b2eab-175">Summarized cash inflows, outflows, and balance using each company’s accounting currency</span></span> |
| <span data-ttu-id="b2eab-176">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span><span class="sxs-lookup"><span data-stu-id="b2eab-176">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise</span></span> | <span data-ttu-id="b2eab-177">Summeeritud sularaha sissetulekud ja väljaminekud, kasutades kõigi ettevõtete puhul süsteemivaluutat</span><span class="sxs-lookup"><span data-stu-id="b2eab-177">Summarized cash inflows, outflows, and balance using the system currency for all companies</span></span> |
| <span data-ttu-id="b2eab-178">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span><span class="sxs-lookup"><span data-stu-id="b2eab-178">LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency</span></span>            | <span data-ttu-id="b2eab-179">Summeeritud kande netosumma ja valuutade saldo, kasutades kandevaluutat</span><span class="sxs-lookup"><span data-stu-id="b2eab-179">Summarized net transaction amount and balance of currencies using the transaction currency</span></span> |