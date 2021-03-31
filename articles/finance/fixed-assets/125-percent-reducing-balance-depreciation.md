---
title: 125 protsenti väheneva saldoga kulum
description: Selles artiklis antakse ülevaade 125% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed1a382325396b30d3921904bcc3ac70f95633b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219887"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="c385d-103">125 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="c385d-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c385d-104">Selles artiklis antakse ülevaade 125% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.</span><span class="sxs-lookup"><span data-stu-id="c385d-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="c385d-105">Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **125% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="c385d-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="c385d-106">Selle protsendimäära arvutamise aluseks on põhivara tööiga.</span><span class="sxs-lookup"><span data-stu-id="c385d-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="c385d-107">Nt kui põhivara kasulik eluiga on viis aastat, arvutatakse perioodi kulumiks 25 protsenti (125% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="c385d-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="c385d-108">125% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="c385d-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c385d-109">Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="c385d-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="c385d-110">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="c385d-110">Select a depreciation year</span></span>
<span data-ttu-id="c385d-111">Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="c385d-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c385d-112">Vaikeväärtus on **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="c385d-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="c385d-113">Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="c385d-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="c385d-114">See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.</span><span class="sxs-lookup"><span data-stu-id="c385d-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="c385d-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="c385d-115">Calendar</span></span>

<span data-ttu-id="c385d-116">Võite säilitada vaikeväärtuse väljal **Kulumiarvestusaasta** jaotises **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="c385d-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="c385d-117">Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="c385d-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="c385d-118">Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus mahakandemaksumus.</span><span class="sxs-lookup"><span data-stu-id="c385d-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="c385d-119">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="c385d-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="c385d-120">Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="c385d-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c385d-121">**Kord aastas** sisestab summa 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="c385d-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="c385d-122">**Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="c385d-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="c385d-123">**Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="c385d-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="c385d-124">**Kord poolaastas** poolaasta kulumisumma sisestatakse poolaasta lõpus (30. juunil ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="c385d-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="c385d-125">**Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="c385d-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="c385d-126">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="c385d-126">Fiscal</span></span>

<span data-ttu-id="c385d-127">Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 125% vähenevast kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="c385d-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="c385d-128">Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="c385d-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="c385d-129">Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="c385d-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="c385d-130">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="c385d-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="c385d-131">Kulumit korrigeeritakse iga perioodi puhul automaatselt ja järgmise rahandusaasta pikkuse määrab perioodide seadistus lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="c385d-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="c385d-132">Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="c385d-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c385d-133">**Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="c385d-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="c385d-134">**Rahandusperiood** sisestab rahandusaasta kohta arvutatud kulumi kogusumma.</span><span class="sxs-lookup"><span data-stu-id="c385d-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="c385d-135">See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="c385d-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="c385d-136">125% väheneva saldoga kulumireegli näide</span><span class="sxs-lookup"><span data-stu-id="c385d-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="c385d-137">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="c385d-137">Acquisition cost</span></span>               | <span data-ttu-id="c385d-138">11 000</span><span class="sxs-lookup"><span data-stu-id="c385d-138">11,000</span></span> |
| <span data-ttu-id="c385d-139">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="c385d-139">Salvage value</span></span>                  | <span data-ttu-id="c385d-140">1000</span><span class="sxs-lookup"><span data-stu-id="c385d-140">1,000</span></span>  |
| <span data-ttu-id="c385d-141">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="c385d-141">Depreciation base</span></span>              | <span data-ttu-id="c385d-142">10 000</span><span class="sxs-lookup"><span data-stu-id="c385d-142">10,000</span></span> |
| <span data-ttu-id="c385d-143">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="c385d-143">Service life years</span></span>             | <span data-ttu-id="c385d-144">5</span><span class="sxs-lookup"><span data-stu-id="c385d-144">5</span></span>      |
| <span data-ttu-id="c385d-145">Kulumiprotsent aastas</span><span class="sxs-lookup"><span data-stu-id="c385d-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="c385d-146">25%</span><span class="sxs-lookup"><span data-stu-id="c385d-146">25%</span></span>    |

<span data-ttu-id="c385d-147">125% väheneva saldo meetod jagab 125 protsenti kasutusea aastatega.</span><span class="sxs-lookup"><span data-stu-id="c385d-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="c385d-148">See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.</span><span class="sxs-lookup"><span data-stu-id="c385d-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="c385d-149">Periood</span><span class="sxs-lookup"><span data-stu-id="c385d-149">Period</span></span> | <span data-ttu-id="c385d-150">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="c385d-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="c385d-151">Arvestuslik väärtus</span><span class="sxs-lookup"><span data-stu-id="c385d-151">Book value</span></span>                    | <span data-ttu-id="c385d-152">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="c385d-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="c385d-153">aasta 1</span><span class="sxs-lookup"><span data-stu-id="c385d-153">Year 1</span></span> | <span data-ttu-id="c385d-154">(11 000 – 1000) × 25% = 2500</span><span class="sxs-lookup"><span data-stu-id="c385d-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="c385d-155">(11 000 – 2500) = 8500</span><span class="sxs-lookup"><span data-stu-id="c385d-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="c385d-156">(11 000 – 1000 – 2500) = 7500</span><span class="sxs-lookup"><span data-stu-id="c385d-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="c385d-157">aasta 2</span><span class="sxs-lookup"><span data-stu-id="c385d-157">Year 2</span></span> | <span data-ttu-id="c385d-158">7500 × 25% = 1875</span><span class="sxs-lookup"><span data-stu-id="c385d-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="c385d-159">(8500 – 1875) = 6625</span><span class="sxs-lookup"><span data-stu-id="c385d-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="c385d-160">(7500 – 1875) = 5625</span><span class="sxs-lookup"><span data-stu-id="c385d-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="c385d-161">aasta 3</span><span class="sxs-lookup"><span data-stu-id="c385d-161">Year 3</span></span> | <span data-ttu-id="c385d-162">5625 × 25% = 1406,25</span><span class="sxs-lookup"><span data-stu-id="c385d-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="c385d-163">(6625 – 1406,25) = 5218,75</span><span class="sxs-lookup"><span data-stu-id="c385d-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="c385d-164">(5625 – 1406,25) = 4218,75</span><span class="sxs-lookup"><span data-stu-id="c385d-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="c385d-165">Tavaliselt kui 125% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.</span><span class="sxs-lookup"><span data-stu-id="c385d-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]