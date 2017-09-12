---
title: "Allesjäänud eluea lineaarne kulum"
description: "Selles artiklis antakse ülevaade kulumiarvestusmeetodist Allesjäänud lineaarne eluiga."
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 4ad82f3177e4abb7b9cb575b910aabc69901f475
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="39bd1-103">Allesjäänud eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="39bd1-103">Straight line life remaining depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="39bd1-104">Selles artiklis antakse ülevaade kulumiarvestusmeetodist Allesjäänud lineaarne eluiga.</span><span class="sxs-lookup"><span data-stu-id="39bd1-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="39bd1-105">Kui seadistate põhivara kulumireegli ja valite lehe **Kulumireeglid** väljal **Meetod** suvandi **Allesjäänud lineaarne eluiga**, siis põhineb kulumireeglile määratud põhivarade tarbimiskulum põhivara järelejäänud tööeal.</span><span class="sxs-lookup"><span data-stu-id="39bd1-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="39bd1-106">Tavaliselt on sel juhul kõigi kulumiperioodide kulumisumma ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="39bd1-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="39bd1-107">Allesjäänud eluea lineaarne kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="39bd1-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="39bd1-108">Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="39bd1-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="39bd1-109">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="39bd1-109">Select a depreciation year</span></span>
<span data-ttu-id="39bd1-110">Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="39bd1-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="39bd1-111">Vaikeväärtus on **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="39bd1-111">The default value is **Calendar**.</span></span> <span data-ttu-id="39bd1-112">Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="39bd1-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="39bd1-113">See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.</span><span class="sxs-lookup"><span data-stu-id="39bd1-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="39bd1-114">Kalender</span><span class="sxs-lookup"><span data-stu-id="39bd1-114">Calendar</span></span>

<span data-ttu-id="39bd1-115">Kui valite suvandi **Kalender** väljal ***Kulumiaasta***, arvestatakse aastana perioodi 1. jaanuarist kuni 31. detsembrini, isegi kui olete rahanduskalendri teisiti määratlenud.</span><span class="sxs-lookup"><span data-stu-id="39bd1-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="39bd1-116">Valik **Kalendriaasta** värskendab kulumiarvestuse alust iga aasta 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="39bd1-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="39bd1-117">Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus jääkväärtus.</span><span class="sxs-lookup"><span data-stu-id="39bd1-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="39bd1-118">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="39bd1-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="39bd1-119">Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="39bd1-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="39bd1-120">**Kord aastas** sisestab summa 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="39bd1-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="39bd1-121">**Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="39bd1-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="39bd1-122">**Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="39bd1-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="39bd1-123">**Kord poolaastas** iga poolaasta lõpus (30. juunil ja 31. detsembril) poole aasta summa sisestamine.</span><span class="sxs-lookup"><span data-stu-id="39bd1-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="39bd1-124">**Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="39bd1-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="39bd1-125">Näiteks suvandi **Kord aastas** valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="39bd1-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="39bd1-126">Suvandi **Kord kuus** valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.</span><span class="sxs-lookup"><span data-stu-id="39bd1-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="39bd1-127">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="39bd1-127">Fiscal</span></span>

<span data-ttu-id="39bd1-128">Kuiv alite väljal **Kulumiarvestusaasta** suvandi **Rahandusaasta**, kasutatakse allesjäänud eluea lineaarset kulumit.</span><span class="sxs-lookup"><span data-stu-id="39bd1-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="39bd1-129">Kulum arvutatakse järelejäänud rahandusaastate alusel.</span><span class="sxs-lookup"><span data-stu-id="39bd1-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="39bd1-130">Näiteks finantsaastal 1. juulist 2015 kuni 30. juunini 2016 käivitub kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="39bd1-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="39bd1-131">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="39bd1-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="39bd1-132">Iga rahandusperioodi kulumit korrigeeritakse.</span><span class="sxs-lookup"><span data-stu-id="39bd1-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="39bd1-133">Järgmise rahandusaasta pikkuse määravad rahandusperioodid, mis on seadistatud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="39bd1-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="39bd1-134">Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="39bd1-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="39bd1-135">**Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="39bd1-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="39bd1-136">**Rahandusperiood**arvutab rahandusaasta kulumi kogusumma.</span><span class="sxs-lookup"><span data-stu-id="39bd1-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="39bd1-137">See summa kogutakse siis rahandusperioodidesse, mis on määratletud lehel **Rahaduskalendrid** raamatu jaoks määratud rahanduskalendri jaoks.</span><span class="sxs-lookup"><span data-stu-id="39bd1-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="39bd1-138">Muutmata põhivara lineaarse kulumi näide</span><span class="sxs-lookup"><span data-stu-id="39bd1-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="39bd1-139">Põhivaral on järgmised näitajad.</span><span class="sxs-lookup"><span data-stu-id="39bd1-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="39bd1-140">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="39bd1-140">Acquisition cost</span></span>    | <span data-ttu-id="39bd1-141">11 000</span><span class="sxs-lookup"><span data-stu-id="39bd1-141">11,000</span></span> |
| <span data-ttu-id="39bd1-142">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="39bd1-142">Salvage value</span></span>       | <span data-ttu-id="39bd1-143">1000</span><span class="sxs-lookup"><span data-stu-id="39bd1-143">1,000</span></span>  |
| <span data-ttu-id="39bd1-144">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="39bd1-144">Depreciation base</span></span>   | <span data-ttu-id="39bd1-145">10 000</span><span class="sxs-lookup"><span data-stu-id="39bd1-145">10,000</span></span> |
| <span data-ttu-id="39bd1-146">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="39bd1-146">Service life years</span></span>  | <span data-ttu-id="39bd1-147">5</span><span class="sxs-lookup"><span data-stu-id="39bd1-147">5</span></span>      |
| <span data-ttu-id="39bd1-148">Aastane kulumisumma</span><span class="sxs-lookup"><span data-stu-id="39bd1-148">Yearly depreciation</span></span> | <span data-ttu-id="39bd1-149">2 000</span><span class="sxs-lookup"><span data-stu-id="39bd1-149">2,000</span></span>  |

<span data-ttu-id="39bd1-150">Kulumisumma on igal aastal sama: (soetusmaksumus – jääkväärtus) ÷ kasuliku eluea aastad</span><span class="sxs-lookup"><span data-stu-id="39bd1-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="39bd1-151">Periood</span><span class="sxs-lookup"><span data-stu-id="39bd1-151">Period</span></span> | <span data-ttu-id="39bd1-152">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="39bd1-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="39bd1-153">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="39bd1-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="39bd1-154">aasta 1</span><span class="sxs-lookup"><span data-stu-id="39bd1-154">Year 1</span></span> | <span data-ttu-id="39bd1-155">(11 000 – 1000) ÷ 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="39bd1-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="39bd1-156">9000</span><span class="sxs-lookup"><span data-stu-id="39bd1-156">9,000</span></span>                                 |
| <span data-ttu-id="39bd1-157">aasta 2</span><span class="sxs-lookup"><span data-stu-id="39bd1-157">Year 2</span></span> | <span data-ttu-id="39bd1-158">(9000 – 1000) ÷ 4 = 2000</span><span class="sxs-lookup"><span data-stu-id="39bd1-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="39bd1-159">7 000</span><span class="sxs-lookup"><span data-stu-id="39bd1-159">7,000</span></span>                                 |
| <span data-ttu-id="39bd1-160">aasta 3</span><span class="sxs-lookup"><span data-stu-id="39bd1-160">Year 3</span></span> | <span data-ttu-id="39bd1-161">(7000 – 1000) ÷ 3 = 2000</span><span class="sxs-lookup"><span data-stu-id="39bd1-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="39bd1-162">5 000</span><span class="sxs-lookup"><span data-stu-id="39bd1-162">5,000</span></span>                                 |
| <span data-ttu-id="39bd1-163">aasta 4</span><span class="sxs-lookup"><span data-stu-id="39bd1-163">Year 4</span></span> | <span data-ttu-id="39bd1-164">(5000 – 1000) ÷ 2 = 2000</span><span class="sxs-lookup"><span data-stu-id="39bd1-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="39bd1-165">3 000</span><span class="sxs-lookup"><span data-stu-id="39bd1-165">3,000</span></span>                                 |
| <span data-ttu-id="39bd1-166">aasta 5</span><span class="sxs-lookup"><span data-stu-id="39bd1-166">Year 5</span></span> | <span data-ttu-id="39bd1-167">(3000 – 1000) ÷ 1 = 2000</span><span class="sxs-lookup"><span data-stu-id="39bd1-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="39bd1-168">1000</span><span class="sxs-lookup"><span data-stu-id="39bd1-168">1,000</span></span>                                 |






