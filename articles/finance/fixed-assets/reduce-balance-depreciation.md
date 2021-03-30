---
title: Väheneva jääkväärtuse kuluarvestusmeetod
description: Selles artiklis antakse ülevaade väheneva kulumiarvestusmeetodi kohta.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69228aec217826780ceb91771028a6a5a180d037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220981"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="5cc0e-103">Väheneva jääkväärtuse kuluarvestusmeetod</span><span class="sxs-lookup"><span data-stu-id="5cc0e-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cc0e-104">Selles artiklis antakse ülevaade väheneva kulumiarvestusmeetodi kohta.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="5cc0e-105">Kui valite põhivara kulumireeglite seadistamisel lehe Kulumireeglid väljal Meetod suvandi Vähenev saldo, on selle kulumireegliga põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="5cc0e-106">Väheneva saldoga kulumireegli seadistamiseks tuleb teil teha valikud ka lehe Kulumireeglid kiirkaardi Üldine väljadel.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="5cc0e-107">Kõigepealt valige aasta väljal Kulumiarvestusaasta.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="5cc0e-108">Valikust olenevalt kuvatakse väljal Perioodi sagedus erinevad väärtused, nagu selgitatakse järgmistes jaotistes.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="5cc0e-109">Samuti tuleb teil sisestada kulumireegli puhul väärtus väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="5cc0e-110">Valiku Täielik kulum puhul võetakse viimasel kulumiperioodil aluseks allesjäänud kulum ja selleks võib olla väga suur summa.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="5cc0e-111">Osades riikides/regioonides ei kasutata ümberlülitust lineaarsele meetodile.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="5cc0e-112">Ümberlülitus ilmneb, kui alternatiivse kulumimeetodi summa on algsest kulumireegli summast suurem või sellega võrdne ja arvestatakse alternatiivse meetodi summat.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="5cc0e-113">Kuna protsendiarvutuste alusel ei saa põhivara kunagi täielikult amortiseerida, tuleb põhivara täielikuks amortiseerimiseks kasutada valikut Täielik kulum.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="5cc0e-114">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="5cc0e-114">Select a depreciation year</span></span>
<span data-ttu-id="5cc0e-115">Saate lehe Kulumireeglid väljalt Kulumiarvestusaasta valida kas suvandi Kalender või Rahandusaasta.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="5cc0e-116">Valik määratleb väljal Perioodi sagedus saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="5cc0e-117">Vaikesuvandiks on Kalender.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="5cc0e-118">Kalender</span><span class="sxs-lookup"><span data-stu-id="5cc0e-118">Calendar</span></span>

<span data-ttu-id="5cc0e-119">Suvandiga Kalender värskendatakse iga aasta 1. jaanuaril kulumiarvestuse alust, milleks on tavaliselt raamatupidamislik jääkväärtus miinus mahakandmismaksumus.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="5cc0e-120">Selles teemas hiljem esinevas väheneva saldoga kulumi näites on kulumiarvestuse alus arvutusveeru avaldise esimeseks liikmeks.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="5cc0e-121">Valides suvandi Kalender on teil kalendriaasta kulumisumma jaotust ja selle sisestuskuupäevi määratleval väljal Perioodi sagedus saadaval järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="5cc0e-122">Kord aastas sisestatakse 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="5cc0e-123">Kord kuus sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="5cc0e-124">Kord kvartalis sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="5cc0e-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="5cc0e-125">Kord poolaastas sisestab kulumisumma iga poolaasta lõpus (30. juunil ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="5cc0e-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="5cc0e-126">Kord päevas sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="5cc0e-127">Näiteks suvandi Kord aastas valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="5cc0e-128">Suvandi Kord kuus valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="5cc0e-129">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="5cc0e-129">Fiscal</span></span>

<span data-ttu-id="5cc0e-130">Kui valite väljal Kulumiarvestusaasta suvandi Rahandusaasta, kasutatakse lineaarset kulumimeetodit.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="5cc0e-131">See arvutatakse rahandusaasta põhjal, mis seadistatakse lehel Rahanduskalendrid lehel Pearaamat valitud rahanduskalendri puhul.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="5cc0e-132">Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="5cc0e-133">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="5cc0e-134">Iga rahandusperioodi kulumit korrigeeritakse.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="5cc0e-135">Järgmise rahandusaasta pikkus põhineb rahandusperioodidel, mille seadistate lehel Rahanduskalendrid uue rahandusaasta loomisel.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="5cc0e-136">Rahandusaasta valimisel on väljal Perioodi sagedus saadaval järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="5cc0e-137">Kord aastas sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="5cc0e-138">Rahandusperiood sisestab arvutatud kulumi kogusumma rahandusaasta puhul, mis on jagatud rahandusperioodideks, mis on määratletud lehel Pearaamat valitud rahanduskalendrile või põhivara raamatu jaoks valitud rahanduskalendrile.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="5cc0e-139">Väheneva saldoga kulumi näide</span><span class="sxs-lookup"><span data-stu-id="5cc0e-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="5cc0e-140">Oletagem, et põhivara soetamisväärtus on 11 000, mahakandemaksumus on 1000 ja kulumi teguriks on protsendimäär 30.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="5cc0e-141">Kasutades väheneva saldo meetodit, arvutatakse 30 protsenti kulumialusest (raamatupidamislik jääkväärtus miinus mahakandmismaksumus) eelmise kulumiarvestusperioodi lõpus.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="5cc0e-142">Esimese kolme aasta kulumit näidatakse järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="5cc0e-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="5cc0e-143">Periood</span><span class="sxs-lookup"><span data-stu-id="5cc0e-143">Period</span></span> | <span data-ttu-id="5cc0e-144">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="5cc0e-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="5cc0e-145">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="5cc0e-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="5cc0e-146">aasta 1</span><span class="sxs-lookup"><span data-stu-id="5cc0e-146">Year 1</span></span> | <span data-ttu-id="5cc0e-147">(11 000 – 1 000) \* 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="5cc0e-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="5cc0e-148">(11 000 – 1000) – 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="5cc0e-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="5cc0e-149">aasta 2</span><span class="sxs-lookup"><span data-stu-id="5cc0e-149">Year 2</span></span> | <span data-ttu-id="5cc0e-150">(7000 – 1000) \* 30% = 1800</span><span class="sxs-lookup"><span data-stu-id="5cc0e-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="5cc0e-151">(7000 – 1800) = 5200</span><span class="sxs-lookup"><span data-stu-id="5cc0e-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="5cc0e-152">aasta 3</span><span class="sxs-lookup"><span data-stu-id="5cc0e-152">Year 3</span></span> | <span data-ttu-id="5cc0e-153">(5200 – 1000) \* 30% = 1260</span><span class="sxs-lookup"><span data-stu-id="5cc0e-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="5cc0e-154">(5200 – 1260) = 3940</span><span class="sxs-lookup"><span data-stu-id="5cc0e-154">(5,200 - 1,260) = 3,940</span></span>               |


-







[!INCLUDE[footer-include](../../includes/footer-banner.md)]