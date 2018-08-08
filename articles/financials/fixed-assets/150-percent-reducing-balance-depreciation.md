---
title: "150 protsenti väheneva saldoga kulum"
description: "Selles artiklis antakse ülevaade 150% väheneva jääkväärtuse kulumiarvestusmeetodi kohta."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: ff4b40663f0da6bcc01b00f3f44cd8d8b43b56a1
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="cecfc-103">150 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="cecfc-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cecfc-104">Selles artiklis antakse ülevaade 150% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.</span><span class="sxs-lookup"><span data-stu-id="cecfc-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="cecfc-105">Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **150% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="cecfc-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="cecfc-106">Selle protsendimäära arvutamise aluseks on põhivara tööiga.</span><span class="sxs-lookup"><span data-stu-id="cecfc-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="cecfc-107">Nt kui põhivara kasulik eluiga on viis aastat, arvutatakse perioodi kulumiks 30 protsenti (150% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="cecfc-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="cecfc-108">150% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="cecfc-109">Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="cecfc-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="cecfc-110">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="cecfc-110">Selection of depreciation year</span></span>
<span data-ttu-id="cecfc-111">Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="cecfc-112">Vaikeväärtus on **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-112">The default value is **Calendar**.</span></span> <span data-ttu-id="cecfc-113">Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="cecfc-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="cecfc-114">See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.</span><span class="sxs-lookup"><span data-stu-id="cecfc-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="cecfc-115">Kalender</span><span class="sxs-lookup"><span data-stu-id="cecfc-115">Calendar</span></span>

<span data-ttu-id="cecfc-116">Võite säilitada vaikeväärtuse väljal **Kulumiarvestusaasta** jaotises **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="cecfc-117">Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="cecfc-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="cecfc-118">Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus mahakandemaksumus.</span><span class="sxs-lookup"><span data-stu-id="cecfc-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="cecfc-119">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="cecfc-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="cecfc-120">Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="cecfc-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="cecfc-121">**Kord aastas** sisestab summa 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="cecfc-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="cecfc-122">**Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="cecfc-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="cecfc-123">**Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="cecfc-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="cecfc-124">**Kord poolaastas** poolaasta kulumisumma sisestatakse poolaasta lõpus (30. juunil ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="cecfc-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="cecfc-125">**Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="cecfc-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="cecfc-126">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="cecfc-126">Fiscal</span></span>

<span data-ttu-id="cecfc-127">Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 150% väheneva jääkväärtuse kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="cecfc-128">Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="cecfc-129">Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="cecfc-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="cecfc-130">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="cecfc-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="cecfc-131">Iga perioodi kulumit korrigeeritakse.</span><span class="sxs-lookup"><span data-stu-id="cecfc-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="cecfc-132">Järgmise rahandusaasta pikkuse määravad perioodid, mis on seadistatud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="cecfc-133">Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="cecfc-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="cecfc-134">**Kord aastas** rahandusaasta alusel arvestatud kulumisumma sisestatakse ühe summana rahandusaasta viimasel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="cecfc-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="cecfc-135">**Rahandusperiood** sisestab rahandusaasta kohta arvutatud kulumi kogusumma.</span><span class="sxs-lookup"><span data-stu-id="cecfc-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="cecfc-136">See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="cecfc-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="cecfc-137">150% väheneva saldoga kulumi näide</span><span class="sxs-lookup"><span data-stu-id="cecfc-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="cecfc-138">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="cecfc-138">Acquisition cost</span></span>               | <span data-ttu-id="cecfc-139">11 000</span><span class="sxs-lookup"><span data-stu-id="cecfc-139">11,000</span></span> |
| <span data-ttu-id="cecfc-140">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="cecfc-140">Salvage value</span></span>                  | <span data-ttu-id="cecfc-141">1000</span><span class="sxs-lookup"><span data-stu-id="cecfc-141">1,000</span></span>  |
| <span data-ttu-id="cecfc-142">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="cecfc-142">Depreciation base</span></span>              | <span data-ttu-id="cecfc-143">10 000</span><span class="sxs-lookup"><span data-stu-id="cecfc-143">10,000</span></span> |
| <span data-ttu-id="cecfc-144">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="cecfc-144">Service life years</span></span>             | <span data-ttu-id="cecfc-145">5</span><span class="sxs-lookup"><span data-stu-id="cecfc-145">5</span></span>      |
| <span data-ttu-id="cecfc-146">Kulumiprotsent aastas</span><span class="sxs-lookup"><span data-stu-id="cecfc-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="cecfc-147">30%</span><span class="sxs-lookup"><span data-stu-id="cecfc-147">30%</span></span>    |

<span data-ttu-id="cecfc-148">150% väheneva saldo meetod jagab 150 protsenti kasutusea aastatega.</span><span class="sxs-lookup"><span data-stu-id="cecfc-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="cecfc-149">See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.</span><span class="sxs-lookup"><span data-stu-id="cecfc-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="cecfc-150">Periood</span><span class="sxs-lookup"><span data-stu-id="cecfc-150">Period</span></span> | <span data-ttu-id="cecfc-151">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="cecfc-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="cecfc-152">Arvestuslik väärtus</span><span class="sxs-lookup"><span data-stu-id="cecfc-152">Book value</span></span>             | <span data-ttu-id="cecfc-153">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="cecfc-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="cecfc-154">aasta 1</span><span class="sxs-lookup"><span data-stu-id="cecfc-154">Year 1</span></span> | <span data-ttu-id="cecfc-155">(11 000 – 1000) × 30% = 3000</span><span class="sxs-lookup"><span data-stu-id="cecfc-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="cecfc-156">11 000 – 3000 = 8000</span><span class="sxs-lookup"><span data-stu-id="cecfc-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="cecfc-157">11 000 – 1000 – 3000 = 7000</span><span class="sxs-lookup"><span data-stu-id="cecfc-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="cecfc-158">aasta 2</span><span class="sxs-lookup"><span data-stu-id="cecfc-158">Year 2</span></span> | <span data-ttu-id="cecfc-159">7000 × 30% = 2100</span><span class="sxs-lookup"><span data-stu-id="cecfc-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="cecfc-160">8000 – 2100 = 5900</span><span class="sxs-lookup"><span data-stu-id="cecfc-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="cecfc-161">7000 – 2100 = 4900</span><span class="sxs-lookup"><span data-stu-id="cecfc-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="cecfc-162">aasta 3</span><span class="sxs-lookup"><span data-stu-id="cecfc-162">Year 3</span></span> | <span data-ttu-id="cecfc-163">4900 × 30% = 1470</span><span class="sxs-lookup"><span data-stu-id="cecfc-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="cecfc-164">5900 – 1470 = 4430</span><span class="sxs-lookup"><span data-stu-id="cecfc-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="cecfc-165">4900 – 1470 = 3430</span><span class="sxs-lookup"><span data-stu-id="cecfc-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="cecfc-166">Tavaliselt kui 150% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.</span><span class="sxs-lookup"><span data-stu-id="cecfc-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




