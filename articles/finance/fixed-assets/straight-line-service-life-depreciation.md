---
title: Kasuliku eluea lineaarne kulum
description: Selles artiklis antakse ülevaade kulumiarvestusmeetodist Lineaarne kasulik eluiga.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b7b9b240156263b4dc1bc308a7f4457380a27f3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177327"
---
# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="25a0f-103">Kasuliku eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="25a0f-103">Straight line service life depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25a0f-104">Selles artiklis antakse ülevaade kulumiarvestusmeetodist Lineaarne kasulik eluiga.</span><span class="sxs-lookup"><span data-stu-id="25a0f-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="25a0f-105">Kui seadistate põhivara kulumireegli ja valite lehe Kulumireeglid väljal Meetod suvandi Tööeapõhine lineaarne, arvutatakse varad, millele on määratud see kulumiprofiil, vara kogu tööea põhjal.</span><span class="sxs-lookup"><span data-stu-id="25a0f-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="25a0f-106">Tavaliselt on sel juhul kõigi kulumiperioodide kulumisumma ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="25a0f-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="25a0f-107">Erinevus allesjäänud tööea lineaarse kulumi ja tööea lineaarse kulumi puhul arvutatud kulumisummade vahel tekib, kui põhivarale on sisestatud korrektsioon.</span><span class="sxs-lookup"><span data-stu-id="25a0f-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="25a0f-108">Tööea lineaarse kulumi seadistamiseks peate valima ka suvandid lehe Kulumireeglid väljadel Kulumiaasta ja Perioodi sagedus.</span><span class="sxs-lookup"><span data-stu-id="25a0f-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="25a0f-109">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="25a0f-109">Select a depreciation year</span></span>
<span data-ttu-id="25a0f-110">Saate lehe Kulumireeglid väljalt Kulumiarvestusaasta valida kas suvandi Kalender või Rahandusaasta.</span><span class="sxs-lookup"><span data-stu-id="25a0f-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="25a0f-111">Valik määratleb väljal Perioodi sagedus saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="25a0f-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="25a0f-112">Vaikesuvandiks on Kalender.</span><span class="sxs-lookup"><span data-stu-id="25a0f-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="25a0f-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="25a0f-113">Calendar</span></span>

<span data-ttu-id="25a0f-114">Kui valite suvandi Kalender, arvestatakse aastana perioodi 1. jaanuarist kuni 31. detsembrini, isegi kui olete määratlenud rahanduskalendri teisiti.</span><span class="sxs-lookup"><span data-stu-id="25a0f-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="25a0f-115">Suvandiga Kalender värskendatakse iga aasta 1. jaanuaril kulumiarvestuse alust, mis on tavaliselt raamatupidamislik jääkväärtus miinus likvideerimisväärtus.</span><span class="sxs-lookup"><span data-stu-id="25a0f-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="25a0f-116">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="25a0f-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="25a0f-117">Valides suvandi Kalender on teil kalendriaasta kulumisumma jaotust ja selle sisestuskuupäevi määratleval väljal Perioodi sagedus saadaval järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="25a0f-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="25a0f-118">Sisestamine kord aastas (31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="25a0f-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="25a0f-119">Kord kuus sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="25a0f-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="25a0f-120">Kord kvartalis sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="25a0f-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="25a0f-121">Kord poolaastas (iga poolaasta lõpus, 30. juunil ja 31. detsembril) poole aasta summa sisestamine.</span><span class="sxs-lookup"><span data-stu-id="25a0f-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="25a0f-122">Kord päevas sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="25a0f-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="25a0f-123">Näiteks suvandi Kord aastas valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="25a0f-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="25a0f-124">Suvandi Kord kuus valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.</span><span class="sxs-lookup"><span data-stu-id="25a0f-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="25a0f-125">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="25a0f-125">Fiscal</span></span>

<span data-ttu-id="25a0f-126">Kui valite väljal Kulumiarvestusaasta suvandi Rahandusaasta, kasutatakse lineaarset tööea kulumit.</span><span class="sxs-lookup"><span data-stu-id="25a0f-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="25a0f-127">See arvutatakse raamatu jaoks määratud rahanduskalendriga või lehel Pearaamat valitud rahanduskalendriga määratletud rahandusaasta põhjal.</span><span class="sxs-lookup"><span data-stu-id="25a0f-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="25a0f-128">Rahanduskalendrid seadistatakse lehel Rahanduskalendrid.</span><span class="sxs-lookup"><span data-stu-id="25a0f-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="25a0f-129">Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="25a0f-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="25a0f-130">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="25a0f-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="25a0f-131">Iga rahandusperioodi kulumit korrigeeritakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="25a0f-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="25a0f-132">Järgmise rahandusaasta pikkus põhineb rahandusperioodidel, mille seadistate vormil Rahanduskalendrid uue rahandusaasta loomisel.</span><span class="sxs-lookup"><span data-stu-id="25a0f-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="25a0f-133">Rahandusaasta valimisel on väljal Perioodi sagedus saadaval järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="25a0f-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="25a0f-134">Kord aastas sisestatakse rahandusaasta kohta arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="25a0f-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="25a0f-135">Rahandusperiood arvutab rahandusaasta kulumi kogusumma, mis on jagatud vormil Rahanduskalendrid rahanduskalendri jaoks määratletud perioodideks.</span><span class="sxs-lookup"><span data-stu-id="25a0f-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="25a0f-136">Näide. Muutmata põhivara lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="25a0f-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="25a0f-137">Oletame, et põhivaral on järgmised näitajad.</span><span class="sxs-lookup"><span data-stu-id="25a0f-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="25a0f-138">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="25a0f-138">Acquisition cost</span></span>    | <span data-ttu-id="25a0f-139">11 000</span><span class="sxs-lookup"><span data-stu-id="25a0f-139">11,000</span></span> |
| <span data-ttu-id="25a0f-140">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="25a0f-140">Salvage value</span></span>       | <span data-ttu-id="25a0f-141">1000</span><span class="sxs-lookup"><span data-stu-id="25a0f-141">1,000</span></span>  |
| <span data-ttu-id="25a0f-142">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="25a0f-142">Depreciation base</span></span>   | <span data-ttu-id="25a0f-143">10 000</span><span class="sxs-lookup"><span data-stu-id="25a0f-143">10,000</span></span> |
| <span data-ttu-id="25a0f-144">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="25a0f-144">Service life years</span></span>  | <span data-ttu-id="25a0f-145">5</span><span class="sxs-lookup"><span data-stu-id="25a0f-145">5</span></span>      |
| <span data-ttu-id="25a0f-146">Aastane kulumisumma</span><span class="sxs-lookup"><span data-stu-id="25a0f-146">Yearly depreciation</span></span> | <span data-ttu-id="25a0f-147">2 000</span><span class="sxs-lookup"><span data-stu-id="25a0f-147">2,000</span></span>  |

<span data-ttu-id="25a0f-148">Saate sama kulumisumma igal aastal:</span><span class="sxs-lookup"><span data-stu-id="25a0f-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="25a0f-149">(soetusmaksumus - mahakandmismaksumus) / kasuliku eluea aastad</span><span class="sxs-lookup"><span data-stu-id="25a0f-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="25a0f-150">Periood</span><span class="sxs-lookup"><span data-stu-id="25a0f-150">Period</span></span> | <span data-ttu-id="25a0f-151">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="25a0f-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="25a0f-152">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="25a0f-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="25a0f-153">aasta 1</span><span class="sxs-lookup"><span data-stu-id="25a0f-153">Year 1</span></span> | <span data-ttu-id="25a0f-154">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="25a0f-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="25a0f-155">9000</span><span class="sxs-lookup"><span data-stu-id="25a0f-155">9,000</span></span>                                 |
| <span data-ttu-id="25a0f-156">aasta 2</span><span class="sxs-lookup"><span data-stu-id="25a0f-156">Year 2</span></span> | <span data-ttu-id="25a0f-157">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="25a0f-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="25a0f-158">7000</span><span class="sxs-lookup"><span data-stu-id="25a0f-158">7,000</span></span>                                 |
| <span data-ttu-id="25a0f-159">aasta 3</span><span class="sxs-lookup"><span data-stu-id="25a0f-159">Year 3</span></span> | <span data-ttu-id="25a0f-160">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="25a0f-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="25a0f-161">5000</span><span class="sxs-lookup"><span data-stu-id="25a0f-161">5,000</span></span>                                 |
| <span data-ttu-id="25a0f-162">aasta 4</span><span class="sxs-lookup"><span data-stu-id="25a0f-162">Year 4</span></span> | <span data-ttu-id="25a0f-163">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="25a0f-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="25a0f-164">3 000</span><span class="sxs-lookup"><span data-stu-id="25a0f-164">3,000</span></span>                                 |
| <span data-ttu-id="25a0f-165">aasta 5</span><span class="sxs-lookup"><span data-stu-id="25a0f-165">Year 5</span></span> | <span data-ttu-id="25a0f-166">(11 000 – 1000) / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="25a0f-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="25a0f-167">1000</span><span class="sxs-lookup"><span data-stu-id="25a0f-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="25a0f-168"> Näide. Muudetud põhivara lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="25a0f-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="25a0f-169">Oletame, et lisate 2. aastal samale põhivarale soetuse korrigeerimise summas 4000.</span><span class="sxs-lookup"><span data-stu-id="25a0f-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="25a0f-170">Soetuse korrigeerimise tööiga on sama mis põhivaral ning algab põhivara soetamisest.</span><span class="sxs-lookup"><span data-stu-id="25a0f-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="25a0f-171">Raamatupidamislik jääkväärtus aasta 5 lõpus säilib, vastavalt soetuse korrigeerimise raamatupidamislikule jääkväärtusele.</span><span class="sxs-lookup"><span data-stu-id="25a0f-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="25a0f-172">Perioodide kulumi arvutamist vt järgmisest tabelist.</span><span class="sxs-lookup"><span data-stu-id="25a0f-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="25a0f-173">Periood</span><span class="sxs-lookup"><span data-stu-id="25a0f-173">Period</span></span> | <span data-ttu-id="25a0f-174">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="25a0f-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="25a0f-175">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="25a0f-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="25a0f-176">aasta 1</span><span class="sxs-lookup"><span data-stu-id="25a0f-176">Year 1</span></span> | <span data-ttu-id="25a0f-177">10 000 / 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="25a0f-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="25a0f-178">11 000 – 2000 = 9000</span><span class="sxs-lookup"><span data-stu-id="25a0f-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="25a0f-179">aasta 2</span><span class="sxs-lookup"><span data-stu-id="25a0f-179">Year 2</span></span> | <span data-ttu-id="25a0f-180">4000 (soetuse korrigeerimine)</span><span class="sxs-lookup"><span data-stu-id="25a0f-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="25a0f-181">9000 + 4000 =13 000</span><span class="sxs-lookup"><span data-stu-id="25a0f-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="25a0f-182">aasta 2</span><span class="sxs-lookup"><span data-stu-id="25a0f-182">Year 2</span></span> | <span data-ttu-id="25a0f-183">14 000 / 5 = 2800</span><span class="sxs-lookup"><span data-stu-id="25a0f-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="25a0f-184">13 000 – 2800 = 10 200</span><span class="sxs-lookup"><span data-stu-id="25a0f-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="25a0f-185">aasta 3</span><span class="sxs-lookup"><span data-stu-id="25a0f-185">Year 3</span></span> | <span data-ttu-id="25a0f-186">14 000 / 5 = 2800</span><span class="sxs-lookup"><span data-stu-id="25a0f-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="25a0f-187">10 200 – 2800 = 7400</span><span class="sxs-lookup"><span data-stu-id="25a0f-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="25a0f-188">aasta 4</span><span class="sxs-lookup"><span data-stu-id="25a0f-188">Year 4</span></span> | <span data-ttu-id="25a0f-189">14 000 / 5 = 2800</span><span class="sxs-lookup"><span data-stu-id="25a0f-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="25a0f-190">7400 – 2800 = 4600</span><span class="sxs-lookup"><span data-stu-id="25a0f-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="25a0f-191">aasta 5</span><span class="sxs-lookup"><span data-stu-id="25a0f-191">Year 5</span></span> | <span data-ttu-id="25a0f-192">14 000 / 5 = 2800</span><span class="sxs-lookup"><span data-stu-id="25a0f-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="25a0f-193">4600 – 2800 = 1800</span><span class="sxs-lookup"><span data-stu-id="25a0f-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="25a0f-194">aasta 6</span><span class="sxs-lookup"><span data-stu-id="25a0f-194">Year 6</span></span> | <span data-ttu-id="25a0f-195">Jääksumma 800\*</span><span class="sxs-lookup"><span data-stu-id="25a0f-195">Remaining 800\*</span></span>                           | <span data-ttu-id="25a0f-196">1800 – 800 = 1000</span><span class="sxs-lookup"><span data-stu-id="25a0f-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="25a0f-197">\*Kuna jääksumma on kulumisummast väiksem, võetakse arvesse ainult jääksumma ilma jääkväärtuseta.</span><span class="sxs-lookup"><span data-stu-id="25a0f-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>




