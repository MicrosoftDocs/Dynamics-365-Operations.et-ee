---
title: "Käsitsi kulumiarvestus"
description: "Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: e43b9397dd4e362eff9d78f302732e6bcc53d1db
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="manual-depreciation"></a><span data-ttu-id="5e25f-103">Käsitsi kulumiarvestus</span><span class="sxs-lookup"><span data-stu-id="5e25f-103">Manual depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5e25f-104">Selles artiklis antakse ülevaade käsitsi rakendatavast kulumiarvestusmeetodist.</span><span class="sxs-lookup"><span data-stu-id="5e25f-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="5e25f-105">Kui teete põhivara kulumireeglite seadistamisel valiku **Käsitsi** väljal **Meetod** lehel **Kulumireeglid**, määratletakse selle kulumireegliga põhivarade kulum kalendriaasta intervallidele sisestatud protsendimääraga.</span><span class="sxs-lookup"><span data-stu-id="5e25f-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="5e25f-106">Intervallid, millele protsendimäärad seadistate, sisestatakse väärtuse järgi, mille valite väljal **Perioodi sagedus** kiirkaardil **Üldine** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="5e25f-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="5e25f-107">Siin on väärtused, mida valida saate.</span><span class="sxs-lookup"><span data-stu-id="5e25f-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="5e25f-108">Kord aastas</span><span class="sxs-lookup"><span data-stu-id="5e25f-108">Yearly</span></span>
-   <span data-ttu-id="5e25f-109">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="5e25f-109">Monthly</span></span>
-   <span data-ttu-id="5e25f-110">Kord kvartalis</span><span class="sxs-lookup"><span data-stu-id="5e25f-110">Quarterly</span></span>
-   <span data-ttu-id="5e25f-111">Kord poolaastas</span><span class="sxs-lookup"><span data-stu-id="5e25f-111">Half-Yearly</span></span>
-   <span data-ttu-id="5e25f-112">Kord päevas</span><span class="sxs-lookup"><span data-stu-id="5e25f-112">Daily</span></span>

<span data-ttu-id="5e25f-113">Pärast perioodi sageduse valimist klõpsake valikut **Käsitsi koostatud graafikud** ja seadistage kõigi sisestusintervallide protsendimäärad.</span><span class="sxs-lookup"><span data-stu-id="5e25f-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="5e25f-114">Käsitsi koostatud graafikud koos sisestusintervallidega määratlevad kulumisumma, nagu selles artiklis antud näidetest näha võib.</span><span class="sxs-lookup"><span data-stu-id="5e25f-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="5e25f-115">Käsitsi sisestatud kulumid arvutatakse alati protsendina soetusmaksumusest.</span><span class="sxs-lookup"><span data-stu-id="5e25f-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="5e25f-116">Käsitsi sisestatud kulumi puhul ei pea teie poolt kulumiintervallidele sisestatavate protsendimäärade summa olema 100 protsenti.</span><span class="sxs-lookup"><span data-stu-id="5e25f-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="5e25f-117">Käsitsi kulumiarvestus on paindlik kulumiarvestusmeetod, mida kasutatakse sageli erakorralise kulumireegli määratlemiseks lehel **Raamatud**, nt mitteperioodiline kulum erieesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="5e25f-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="5e25f-118">Näited</span><span class="sxs-lookup"><span data-stu-id="5e25f-118">Examples</span></span>
<span data-ttu-id="5e25f-119">Soetusmaksumus: 11 000.00 Eeldatav mahakandmismaksumus: 1000.00 Järgmises tabelis on näidatud intervallid ja protsendid, mille saab seadistada lehel **Põhivara kulumireeglite graafikud**.</span><span class="sxs-lookup"><span data-stu-id="5e25f-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="5e25f-120">Intervalli number</span><span class="sxs-lookup"><span data-stu-id="5e25f-120">Interval number</span></span> | <span data-ttu-id="5e25f-121">Protsent</span><span class="sxs-lookup"><span data-stu-id="5e25f-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="5e25f-122">1</span><span class="sxs-lookup"><span data-stu-id="5e25f-122">1</span></span>               | <span data-ttu-id="5e25f-123">10,00</span><span class="sxs-lookup"><span data-stu-id="5e25f-123">10.00</span></span>      |
| <span data-ttu-id="5e25f-124">2</span><span class="sxs-lookup"><span data-stu-id="5e25f-124">2</span></span>               | <span data-ttu-id="5e25f-125">50,00</span><span class="sxs-lookup"><span data-stu-id="5e25f-125">50.00</span></span>      |
| <span data-ttu-id="5e25f-126">3</span><span class="sxs-lookup"><span data-stu-id="5e25f-126">3</span></span>               | <span data-ttu-id="5e25f-127">8.00</span><span class="sxs-lookup"><span data-stu-id="5e25f-127">8.00</span></span>       |

<span data-ttu-id="5e25f-128">Järgmises tabelis on näidatud, kuidas iga intervalli kulum arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="5e25f-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="5e25f-129">Intervalli number</span><span class="sxs-lookup"><span data-stu-id="5e25f-129">Interval number</span></span> | <span data-ttu-id="5e25f-130">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="5e25f-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="5e25f-131">Raamatupidamislik jääkväärtus intervalli lõpus</span><span class="sxs-lookup"><span data-stu-id="5e25f-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="5e25f-132">1</span><span class="sxs-lookup"><span data-stu-id="5e25f-132">1</span></span>                | <span data-ttu-id="5e25f-133">(11 000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="5e25f-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="5e25f-134">10 000 (11 000 – 1000)</span><span class="sxs-lookup"><span data-stu-id="5e25f-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="5e25f-135">2</span><span class="sxs-lookup"><span data-stu-id="5e25f-135">2</span></span>                | <span data-ttu-id="5e25f-136">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="5e25f-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="5e25f-137">5000 (10000 – 5000)</span><span class="sxs-lookup"><span data-stu-id="5e25f-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="5e25f-138">3</span><span class="sxs-lookup"><span data-stu-id="5e25f-138">3</span></span>                | <span data-ttu-id="5e25f-139">(11 000 – 1000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="5e25f-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="5e25f-140">4200 (5000 – 800)</span><span class="sxs-lookup"><span data-stu-id="5e25f-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="5e25f-141">Kui teete valiku **Igakuine** väljal**Perioodi sagedus**, seadistate 12 käsitsi graafikuintervalli.</span><span class="sxs-lookup"><span data-stu-id="5e25f-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="5e25f-142">Järgmine tabel näitab kahe esimese intervalli kulumisummasid.</span><span class="sxs-lookup"><span data-stu-id="5e25f-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="5e25f-143">Intervall</span><span class="sxs-lookup"><span data-stu-id="5e25f-143">Interval</span></span> | <span data-ttu-id="5e25f-144">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="5e25f-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="5e25f-145">Jaanuar</span><span class="sxs-lookup"><span data-stu-id="5e25f-145">January</span></span>  | <span data-ttu-id="5e25f-146">(11 000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="5e25f-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="5e25f-147">Veebruar</span><span class="sxs-lookup"><span data-stu-id="5e25f-147">February</span></span> | <span data-ttu-id="5e25f-148">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="5e25f-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="5e25f-149">Kui valite **Kord poolaastas** väljalt ****Perioodi sagedus** **, seadistate kaks käsitsi graafikuintervalli.</span><span class="sxs-lookup"><span data-stu-id="5e25f-149">If you select **Half-Yearly** in the ****Period frequency** field**, you set up two manual schedule intervals.</span></span> <span data-ttu-id="5e25f-150">Järgmine tabel näitab nende kahe intervalli kulumisummasid.</span><span class="sxs-lookup"><span data-stu-id="5e25f-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="5e25f-151">Intervall</span><span class="sxs-lookup"><span data-stu-id="5e25f-151">Interval</span></span>    | <span data-ttu-id="5e25f-152">Kulumisumma</span><span class="sxs-lookup"><span data-stu-id="5e25f-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="5e25f-153">30. juuni</span><span class="sxs-lookup"><span data-stu-id="5e25f-153">June 30</span></span>     | <span data-ttu-id="5e25f-154">(11 000 – 1000) × 10% = 1000</span><span class="sxs-lookup"><span data-stu-id="5e25f-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="5e25f-155">31. detsember</span><span class="sxs-lookup"><span data-stu-id="5e25f-155">December 31</span></span> | <span data-ttu-id="5e25f-156">(11 000 – 1000) × 50% = 5000</span><span class="sxs-lookup"><span data-stu-id="5e25f-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="5e25f-157">Kõigi intervallide protsentide kogusumma ei pea olema 100.</span><span class="sxs-lookup"><span data-stu-id="5e25f-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="5e25f-158">Kuid saate teate, kui väärtus väljal **Kumulatiivne protsent** lehel **Põhivara kulumireeglite graafikud** ei ole **100**.</span><span class="sxs-lookup"><span data-stu-id="5e25f-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>




