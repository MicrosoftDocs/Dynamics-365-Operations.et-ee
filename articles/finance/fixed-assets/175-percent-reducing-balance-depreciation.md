---
title: 175 protsenti väheneva saldoga kulum
description: Selles teemas antakse ülevaade 175% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3a21c315aa9a7193c20e4184da20d4d6d38386c4
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177338"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="1ac04-103">175 protsenti väheneva saldoga kulum</span><span class="sxs-lookup"><span data-stu-id="1ac04-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ac04-104">Selles teemas antakse ülevaade 175% väheneva jääkväärtuse kulumiarvestusmeetodi kohta.</span><span class="sxs-lookup"><span data-stu-id="1ac04-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="1ac04-105">Kui valite põhivara kulumireeglite seadistamisel lehe **Kulumireeglid** väljal **Meetod** suvandi **175% vähenev saldo**, on sellele kulumireeglile määratud põhivarade kulumiprotsent kõigil kulumiperioodidel ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="1ac04-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="1ac04-106">175% väheneva saldoga kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1ac04-107">Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="1ac04-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="1ac04-108">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="1ac04-108">Select a depreciation year</span></span>
<span data-ttu-id="1ac04-109">Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="1ac04-110">Vaikeväärtus on **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="1ac04-111">Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="1ac04-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="1ac04-112">See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.</span><span class="sxs-lookup"><span data-stu-id="1ac04-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="1ac04-113">Kalender</span><span class="sxs-lookup"><span data-stu-id="1ac04-113">Calendar</span></span>

<span data-ttu-id="1ac04-114">Võite säilitada vaikeväärtuse väljal **Kulumiarvestusaasta** jaotises **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="1ac04-115">Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="1ac04-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="1ac04-116">Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus mahakandemaksumus.</span><span class="sxs-lookup"><span data-stu-id="1ac04-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="1ac04-117">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="1ac04-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="1ac04-118">Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="1ac04-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="1ac04-119">**Kord aastas** sisestab summa 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="1ac04-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="1ac04-120">**Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="1ac04-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="1ac04-121">**Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="1ac04-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="1ac04-122">**Kord poolaastas** poolaasta kulumisumma sisestatakse poolaasta lõpus (30. juunil ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="1ac04-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="1ac04-123">**Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="1ac04-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="1ac04-124">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="1ac04-124">Fiscal</span></span>

<span data-ttu-id="1ac04-125">Kui valite väljal **Kulumiaasta** suvandi **Rahandusaasta**, arvutatakse 175% väheneva jääkväärtuse kulumist rahanduskalendri rahandusaasta alusel, mis on määratud raamatule, või rahanduskalendri alusel, mis on valitud lehel **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="1ac04-126">Rahanduskalendrid seadistatakse lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="1ac04-127">Lisateavet leiate jaotisest [Rahanduskalendrid, rahandusaastad ja -perioodid](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="1ac04-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="1ac04-128">Näiteks rahandusaasta puhul 1. juulist kuni 30. juunini algab kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="1ac04-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="1ac04-129">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="1ac04-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="1ac04-130">Kulumit korrigeeritakse iga perioodi puhul automaatselt ja järgmise rahandusaasta pikkuse määrab perioodide seadistus lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="1ac04-131">Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="1ac04-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="1ac04-132">**Kord aastas** rahandusaasta alusel arvestatud kulumisumma sisestatakse ühe summana rahandusaasta viimasel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="1ac04-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="1ac04-133">**Rahandusperiood** arvutab rahandusaasta kulumi kogusumma.</span><span class="sxs-lookup"><span data-stu-id="1ac04-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="1ac04-134">See summa on jagatud rahandusperioodideks, mis on määratletud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="1ac04-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="1ac04-135">175% väheneva saldoga kulumireegli näide</span><span class="sxs-lookup"><span data-stu-id="1ac04-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="1ac04-136">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="1ac04-136">Acquisition cost</span></span>               | <span data-ttu-id="1ac04-137">11 000</span><span class="sxs-lookup"><span data-stu-id="1ac04-137">11,000</span></span> |
| <span data-ttu-id="1ac04-138">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="1ac04-138">Salvage value</span></span>                  | <span data-ttu-id="1ac04-139">1000</span><span class="sxs-lookup"><span data-stu-id="1ac04-139">1,000</span></span>  |
| <span data-ttu-id="1ac04-140">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="1ac04-140">Depreciation base</span></span>              | <span data-ttu-id="1ac04-141">10 000</span><span class="sxs-lookup"><span data-stu-id="1ac04-141">10,000</span></span> |
| <span data-ttu-id="1ac04-142">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="1ac04-142">Service life years</span></span>             | <span data-ttu-id="1ac04-143">5</span><span class="sxs-lookup"><span data-stu-id="1ac04-143">5</span></span>      |
| <span data-ttu-id="1ac04-144">Kulumiprotsent aastas</span><span class="sxs-lookup"><span data-stu-id="1ac04-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="1ac04-145">35%</span><span class="sxs-lookup"><span data-stu-id="1ac04-145">35%</span></span>    |

<span data-ttu-id="1ac04-146">175% väheneva jääkväärtuse kulumiarvestusmeetod jagab 175 protsenti kasutusea aastatega.</span><span class="sxs-lookup"><span data-stu-id="1ac04-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="1ac04-147">See protsendimäär korrutatakse aasta kulumisumma kindlaksmääramiseks põhivara raamatupidamisliku jääkväärtusega.</span><span class="sxs-lookup"><span data-stu-id="1ac04-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="1ac04-148">Periood</span><span class="sxs-lookup"><span data-stu-id="1ac04-148">Period</span></span> | <span data-ttu-id="1ac04-149">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="1ac04-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="1ac04-150">Arvestuslik väärtus</span><span class="sxs-lookup"><span data-stu-id="1ac04-150">Book value</span></span>                  | <span data-ttu-id="1ac04-151">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="1ac04-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="1ac04-152">aasta 1</span><span class="sxs-lookup"><span data-stu-id="1ac04-152">Year 1</span></span> | <span data-ttu-id="1ac04-153">(11 000 – 1000) × 35% = 3500</span><span class="sxs-lookup"><span data-stu-id="1ac04-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="1ac04-154">11 000 – 3500 = 7500</span><span class="sxs-lookup"><span data-stu-id="1ac04-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="1ac04-155">11 000 – 1000 – 3500 = 6500</span><span class="sxs-lookup"><span data-stu-id="1ac04-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="1ac04-156">aasta 2</span><span class="sxs-lookup"><span data-stu-id="1ac04-156">Year 2</span></span> | <span data-ttu-id="1ac04-157">6500 × 35% = 2275</span><span class="sxs-lookup"><span data-stu-id="1ac04-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="1ac04-158">7,500 – 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="1ac04-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="1ac04-159">6500 – 2275 = 4225</span><span class="sxs-lookup"><span data-stu-id="1ac04-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="1ac04-160">aasta 3</span><span class="sxs-lookup"><span data-stu-id="1ac04-160">Year 3</span></span> | <span data-ttu-id="1ac04-161">4225 × 35% = 1478.75</span><span class="sxs-lookup"><span data-stu-id="1ac04-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="1ac04-162">5225 – 1478.75 = 3746.25</span><span class="sxs-lookup"><span data-stu-id="1ac04-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="1ac04-163">4225 – 1478.75 = 2746.25</span><span class="sxs-lookup"><span data-stu-id="1ac04-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="1ac04-164">Tavaliselt kui 175% väheneva saldo kulumiarvestusmeetodiga arvutatud summa on väiksem kui lineaarse meetodiga arvutades tulemuseks olev summa, teisendatakse järelejäänud eluiga lineaarse meetodi järgi.</span><span class="sxs-lookup"><span data-stu-id="1ac04-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>


