---
title: 200 protsenti väheneva saldoga kulum
description: Selles artiklis antakse ülevaade 200% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.
author: saraschi2
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
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442412"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="1e8ac-103">200 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="1e8ac-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e8ac-104">Selles artiklis antakse ülevaade 200% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="1e8ac-105">Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **200% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="1e8ac-106">Protsendimäära arvutamise aluseks on põhivara tööiga.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="1e8ac-107">Nt kui põhivara kasulik eluiga on viis aastat, arvutatakse perioodi kulumiks 40 protsenti (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="1e8ac-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="1e8ac-108">Seda meetodit tuntakse ka kahekordselt väheneva kulumina.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="1e8ac-109">200% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1e8ac-110">Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="1e8ac-111">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="1e8ac-111">Select a depreciation year</span></span>
<span data-ttu-id="1e8ac-112">Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1e8ac-113">Vaikeväärtus on **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="1e8ac-114">Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="1e8ac-115">See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="1e8ac-116">Kalender</span><span class="sxs-lookup"><span data-stu-id="1e8ac-116">Calendar</span></span>

<span data-ttu-id="1e8ac-117">Võite säilitada vaikeväärtuse väljal **Kulumiarvestusaasta** jaotises **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="1e8ac-118">Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="1e8ac-119">Kulumiarvestus on tavaliselt raamatupidamislik jääkväärtus miinus mahakandemaksumus.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="1e8ac-120">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="1e8ac-121">Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="1e8ac-122">**Kord aastas** sisestab summa 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="1e8ac-123">**Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="1e8ac-124">**Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="1e8ac-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="1e8ac-125">**Kord poolaastas** poolaasta kulumisumma sisestatakse poolaasta lõpus (30. juunil ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="1e8ac-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="1e8ac-126">**Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="1e8ac-127">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="1e8ac-127">Fiscal</span></span>

<span data-ttu-id="1e8ac-128">Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 200% väheneva jääkväärtuse kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="1e8ac-129">Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="1e8ac-130">Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="1e8ac-131">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="1e8ac-132">Iga perioodi kulumit korrigeeritakse.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="1e8ac-133">Järgmise rahandusaasta pikkuse määravad perioodid, mis on seadistatud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="1e8ac-134">Kui valite kulumiarvestusaastaks **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="1e8ac-135">**Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="1e8ac-136">**Rahandusperiood** sisestab rahandusaasta kohta arvutatud kulumi kogusumma.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="1e8ac-137">See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="1e8ac-138">200% väheneva saldoga kulumi näide</span><span class="sxs-lookup"><span data-stu-id="1e8ac-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="1e8ac-139">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="1e8ac-139">Acquisition cost</span></span>               | <span data-ttu-id="1e8ac-140">11 000</span><span class="sxs-lookup"><span data-stu-id="1e8ac-140">11,000</span></span> |
| <span data-ttu-id="1e8ac-141">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="1e8ac-141">Salvage value</span></span>                  | <span data-ttu-id="1e8ac-142">1000</span><span class="sxs-lookup"><span data-stu-id="1e8ac-142">1, 000</span></span> |
| <span data-ttu-id="1e8ac-143">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="1e8ac-143">Depreciation base</span></span>              | <span data-ttu-id="1e8ac-144">10 000</span><span class="sxs-lookup"><span data-stu-id="1e8ac-144">10,000</span></span> |
| <span data-ttu-id="1e8ac-145">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="1e8ac-145">Service life years</span></span>             | <span data-ttu-id="1e8ac-146">5</span><span class="sxs-lookup"><span data-stu-id="1e8ac-146">5</span></span>      |
| <span data-ttu-id="1e8ac-147">Kulumiprotsent aastas</span><span class="sxs-lookup"><span data-stu-id="1e8ac-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="1e8ac-148">40%</span><span class="sxs-lookup"><span data-stu-id="1e8ac-148">40%</span></span>    |

<span data-ttu-id="1e8ac-149">200% väheneva saldo meetod jagab 200 protsenti kasutusea aastatega.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="1e8ac-150">See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="1e8ac-151">Periood</span><span class="sxs-lookup"><span data-stu-id="1e8ac-151">Period</span></span> | <span data-ttu-id="1e8ac-152">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="1e8ac-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="1e8ac-153">Arvestuslik väärtus</span><span class="sxs-lookup"><span data-stu-id="1e8ac-153">Book value</span></span>             | <span data-ttu-id="1e8ac-154">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="1e8ac-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="1e8ac-155">aasta 1</span><span class="sxs-lookup"><span data-stu-id="1e8ac-155">Year 1</span></span> | <span data-ttu-id="1e8ac-156">(11 000 – 1000) × 40% = 4000</span><span class="sxs-lookup"><span data-stu-id="1e8ac-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="1e8ac-157">11 000 – 4000 = 7000</span><span class="sxs-lookup"><span data-stu-id="1e8ac-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="1e8ac-158">11 000 – 1 000 – 4 000 = 6 000</span><span class="sxs-lookup"><span data-stu-id="1e8ac-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="1e8ac-159">aasta 2</span><span class="sxs-lookup"><span data-stu-id="1e8ac-159">Year 2</span></span> | <span data-ttu-id="1e8ac-160">6000 × 40% = 2400</span><span class="sxs-lookup"><span data-stu-id="1e8ac-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="1e8ac-161">7000 – 2400 = 4600</span><span class="sxs-lookup"><span data-stu-id="1e8ac-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="1e8ac-162">6000 – 2400 = 3600</span><span class="sxs-lookup"><span data-stu-id="1e8ac-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="1e8ac-163">aasta 3</span><span class="sxs-lookup"><span data-stu-id="1e8ac-163">Year 3</span></span> | <span data-ttu-id="1e8ac-164">3600 × 40% = 1440</span><span class="sxs-lookup"><span data-stu-id="1e8ac-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="1e8ac-165">4600 – 1440 = 3160</span><span class="sxs-lookup"><span data-stu-id="1e8ac-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="1e8ac-166">3600 – 1440 = 2160</span><span class="sxs-lookup"><span data-stu-id="1e8ac-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="1e8ac-167">Tavaliselt kui 200% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



