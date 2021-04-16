---
title: Käsitsi kulumiarvestus
description: Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bb8d739f3c6c8315ba8f135e7a71075f34f32f1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815640"
---
# <a name="manual-depreciation"></a><span data-ttu-id="252ea-103">Käsitsi kulumiarvestus</span><span class="sxs-lookup"><span data-stu-id="252ea-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="252ea-104">Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist.</span><span class="sxs-lookup"><span data-stu-id="252ea-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="252ea-105">Kui teete põhivara kulumireeglite seadistamisel valiku **Käsitsi** väljal **Meetod** lehel **Kulumireeglid**, määratletakse selle kulumireegliga põhivarade kulum kalendriaasta intervallidele sisestatud protsendimääraga.</span><span class="sxs-lookup"><span data-stu-id="252ea-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="252ea-106">Intervallid, millele protsendimäärad seadistate, sisestatakse väärtuse järgi, mille valite väljal **Perioodi sagedus** kiirkaardil **Üldine** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="252ea-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="252ea-107">Siin on väärtused, mida valida saate.</span><span class="sxs-lookup"><span data-stu-id="252ea-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="252ea-108">Kord aastas</span><span class="sxs-lookup"><span data-stu-id="252ea-108">Yearly</span></span>
-   <span data-ttu-id="252ea-109">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="252ea-109">Monthly</span></span>
-   <span data-ttu-id="252ea-110">Kord kvartalis</span><span class="sxs-lookup"><span data-stu-id="252ea-110">Quarterly</span></span>
-   <span data-ttu-id="252ea-111">Kord poolaastas</span><span class="sxs-lookup"><span data-stu-id="252ea-111">Half-Yearly</span></span>
-   <span data-ttu-id="252ea-112">Kord päevas</span><span class="sxs-lookup"><span data-stu-id="252ea-112">Daily</span></span>

<span data-ttu-id="252ea-113">Pärast perioodi sageduse valimist klõpsake valikut **Käsitsi koostatud graafikud** ja seadistage kõigi sisestusintervallide protsendimäärad.</span><span class="sxs-lookup"><span data-stu-id="252ea-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="252ea-114">Käsitsi koostatud graafikud koos sisestusintervallidega määratlevad kulumisumma, nagu selles artiklis antud näidetest näha võib.</span><span class="sxs-lookup"><span data-stu-id="252ea-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="252ea-115">Käsitsi sisestatud kulumid arvutatakse alati protsendina soetusmaksumusest.</span><span class="sxs-lookup"><span data-stu-id="252ea-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="252ea-116">Käsitsi sisestatud kulumi puhul ei pea teie poolt kulumiintervallidele sisestatavate protsendimäärade summa olema 100 protsenti.</span><span class="sxs-lookup"><span data-stu-id="252ea-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="252ea-117">Käsitsi kulumiarvestus on paindlik kulumiarvestusmeetod, mida kasutatakse sageli erakorralise kulumireegli määratlemiseks lehel **Raamatud**, nt mitteperioodiline kulum erieesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="252ea-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="252ea-118">Näited</span><span class="sxs-lookup"><span data-stu-id="252ea-118">Examples</span></span>
<span data-ttu-id="252ea-119">Soetusmaksumus: 11 000.00 Eeldatav mahakandmismaksumus: 1000.00 Järgmises tabelis on näidatud intervallid ja protsendid, mille saab seadistada lehel **Põhivara kulumireeglite graafikud**.</span><span class="sxs-lookup"><span data-stu-id="252ea-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="252ea-120">Intervalli number</span><span class="sxs-lookup"><span data-stu-id="252ea-120">Interval number</span></span> | <span data-ttu-id="252ea-121">Protsent</span><span class="sxs-lookup"><span data-stu-id="252ea-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="252ea-122">1</span><span class="sxs-lookup"><span data-stu-id="252ea-122">1</span></span>               | <span data-ttu-id="252ea-123">10,00</span><span class="sxs-lookup"><span data-stu-id="252ea-123">10.00</span></span>      |
| <span data-ttu-id="252ea-124">2</span><span class="sxs-lookup"><span data-stu-id="252ea-124">2</span></span>               | <span data-ttu-id="252ea-125">50,00</span><span class="sxs-lookup"><span data-stu-id="252ea-125">50.00</span></span>      |
| <span data-ttu-id="252ea-126">3</span><span class="sxs-lookup"><span data-stu-id="252ea-126">3</span></span>               | <span data-ttu-id="252ea-127">8.00</span><span class="sxs-lookup"><span data-stu-id="252ea-127">8.00</span></span>       |

<span data-ttu-id="252ea-128">Järgmises tabelis on näidatud, kuidas iga intervalli kulum arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="252ea-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="252ea-129">Intervalli number</span><span class="sxs-lookup"><span data-stu-id="252ea-129">Interval number</span></span> | <span data-ttu-id="252ea-130">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="252ea-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="252ea-131">Raamatupidamislik jääkväärtus intervalli lõpus</span><span class="sxs-lookup"><span data-stu-id="252ea-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="252ea-132">1</span><span class="sxs-lookup"><span data-stu-id="252ea-132">1</span></span>                | <span data-ttu-id="252ea-133">(11 000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="252ea-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="252ea-134">10 000 (11 000 – 1000)</span><span class="sxs-lookup"><span data-stu-id="252ea-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="252ea-135">2</span><span class="sxs-lookup"><span data-stu-id="252ea-135">2</span></span>                | <span data-ttu-id="252ea-136">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="252ea-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="252ea-137">5000 (10000 – 5000)</span><span class="sxs-lookup"><span data-stu-id="252ea-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="252ea-138">3</span><span class="sxs-lookup"><span data-stu-id="252ea-138">3</span></span>                | <span data-ttu-id="252ea-139">(11 000 – 1000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="252ea-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="252ea-140">4200 (5000 – 800)</span><span class="sxs-lookup"><span data-stu-id="252ea-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="252ea-141">Kui teete valiku **Igakuine** väljal **Perioodi sagedus**, seadistate 12 käsitsi graafikuintervalli.</span><span class="sxs-lookup"><span data-stu-id="252ea-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="252ea-142">Järgmine tabel näitab kahe esimese intervalli kulumisummasid.</span><span class="sxs-lookup"><span data-stu-id="252ea-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="252ea-143">Intervall</span><span class="sxs-lookup"><span data-stu-id="252ea-143">Interval</span></span> | <span data-ttu-id="252ea-144">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="252ea-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="252ea-145">Jaanuar</span><span class="sxs-lookup"><span data-stu-id="252ea-145">January</span></span>  | <span data-ttu-id="252ea-146">(11 000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="252ea-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="252ea-147">Veebruar</span><span class="sxs-lookup"><span data-stu-id="252ea-147">February</span></span> | <span data-ttu-id="252ea-148">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="252ea-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="252ea-149">Kui valite <strong>Kord poolaastas</strong> *<strong>väljalt<em>Perioodi sagedus</em>*</strong>, seadistate kaks käsitsi graafikuintervalli.</span><span class="sxs-lookup"><span data-stu-id="252ea-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="252ea-150">Järgmine tabel näitab nende kahe intervalli kulumisummasid.</span><span class="sxs-lookup"><span data-stu-id="252ea-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="252ea-151">Intervall</span><span class="sxs-lookup"><span data-stu-id="252ea-151">Interval</span></span>    | <span data-ttu-id="252ea-152">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="252ea-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="252ea-153">30. juuni</span><span class="sxs-lookup"><span data-stu-id="252ea-153">June 30</span></span>     | <span data-ttu-id="252ea-154">(11 000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="252ea-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="252ea-155">31. detsember</span><span class="sxs-lookup"><span data-stu-id="252ea-155">December 31</span></span> | <span data-ttu-id="252ea-156">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="252ea-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="252ea-157">Kõigi intervallide protsentide kogusumma ei pea olema 100.</span><span class="sxs-lookup"><span data-stu-id="252ea-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="252ea-158">Kuid saate teate, kui väärtus väljal **Kumulatiivne protsent** lehel **Põhivara kulumireeglite graafikud** ei ole **100**.</span><span class="sxs-lookup"><span data-stu-id="252ea-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]