---
title: Allesjäänud eluea lineaarne kulum
description: Selles artiklis antakse ülevaade kulumiarvestusmeetodist Allesjäänud lineaarne eluiga.
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 823b2569670adfbf04038abca656e34f0199fce1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210091"
---
# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="f6814-103">Allesjäänud eluea lineaarne kulum</span><span class="sxs-lookup"><span data-stu-id="f6814-103">Straight line life remaining depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f6814-104">Selles artiklis antakse ülevaade kulumiarvestusmeetodist Allesjäänud lineaarne eluiga.</span><span class="sxs-lookup"><span data-stu-id="f6814-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="f6814-105">Kui seadistate põhivara kulumireegli ja valite lehe **Kulumireeglid** väljal **Meetod** suvandi **Allesjäänud lineaarne eluiga**, siis põhineb kulumireeglile määratud põhivarade tarbimiskulum põhivara järelejäänud tööeal.</span><span class="sxs-lookup"><span data-stu-id="f6814-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="f6814-106">Tavaliselt on sel juhul kõigi kulumiperioodide kulumisumma ühesuurune.</span><span class="sxs-lookup"><span data-stu-id="f6814-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="f6814-107">Allesjäänud eluea lineaarne kulumi seadistamiseks peate valima ka suvandid lehe **Kulumireeglid** väljadel **Kulumiaasta** ja **Perioodi sagedus**.</span><span class="sxs-lookup"><span data-stu-id="f6814-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f6814-108">Väljal **Perioodi sagedus** olevad valikud erinevad olenevalt väljal **Kulumiarvestusaasta** valitud väärtusest.</span><span class="sxs-lookup"><span data-stu-id="f6814-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="f6814-109">Kulumiaasta valimine</span><span class="sxs-lookup"><span data-stu-id="f6814-109">Select a depreciation year</span></span>
<span data-ttu-id="f6814-110">Saate teha valiku **Kalendriaasta** või **Rahandusaasta** väljalt **Kulumiarvestusaasta** lehel **Kulumireeglid**.</span><span class="sxs-lookup"><span data-stu-id="f6814-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f6814-111">Vaikeväärtus on **Kalendriaasta**.</span><span class="sxs-lookup"><span data-stu-id="f6814-111">The default value is **Calendar**.</span></span> <span data-ttu-id="f6814-112">Teie valik määrab väljal **Perioodi sagedus** saadaolevad suvandid.</span><span class="sxs-lookup"><span data-stu-id="f6814-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="f6814-113">See väli määratleb kalendriaasta kulumisumma sisestuskuupäevad ja summad kalendriaasta lõikes.</span><span class="sxs-lookup"><span data-stu-id="f6814-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="f6814-114">Kalender</span><span class="sxs-lookup"><span data-stu-id="f6814-114">Calendar</span></span>

<span data-ttu-id="f6814-115">Kui teete valiku **Kalender** väljal **_Kuluaasta_*_, eeldatakse, et aasta on 1. jaanuar kuni 31. detsember, isegu kui olete määratlendu finantsaasta teisiti. Suvand _\* Kalender*\* värskendab kulumiarvestuse alust iga aasta 1. jaanuaril.</span><span class="sxs-lookup"><span data-stu-id="f6814-115">If you select **Calendar** in the **_Depreciation year_*_ field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently. The _\* Calendar*\* option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="f6814-116">Kulumiarvestuse alus on tavaliselt raamatupidamislik jääkväärtus miinus jääkväärtus.</span><span class="sxs-lookup"><span data-stu-id="f6814-116">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="f6814-117">Selle teema edasistes näidetes on kulumiarvestuse alus arvutuste veeru esimese avaldise esimene liige.</span><span class="sxs-lookup"><span data-stu-id="f6814-117">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="f6814-118">Kui valite kulumiarvestusaasta **Kalendriaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="f6814-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f6814-119">**Kord aastas** sisestab summa 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="f6814-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="f6814-120">**Kord kuus** sisestab igakuise summa iga kalendrikuu lõpus.</span><span class="sxs-lookup"><span data-stu-id="f6814-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="f6814-121">**Kord kvartalis** sisestab kulumisumma iga kvartali lõpus (31. märtsil, 30. juunil, 30. septembril ja 31. detsembril).</span><span class="sxs-lookup"><span data-stu-id="f6814-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="f6814-122">**Kord poolaastas** iga poolaasta lõpus (30. juunil ja 31. detsembril) poole aasta summa sisestamine.</span><span class="sxs-lookup"><span data-stu-id="f6814-122">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="f6814-123">**Kord päevas** sisestab kulumimeetodi puhul kulumisumma ühe kandena iga päeva kohta.</span><span class="sxs-lookup"><span data-stu-id="f6814-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="f6814-124">Näiteks suvandi **Kord aastas** valimisel sisestatakse aasta kulum ainult üks kord iga aasta 31. detsembril.</span><span class="sxs-lookup"><span data-stu-id="f6814-124">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="f6814-125">Suvandi **Kord kuus** valimisel sisestatakse kulum igal kuul kui 1/12 aasta kulumisummast.</span><span class="sxs-lookup"><span data-stu-id="f6814-125">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="f6814-126">Fiskaalne</span><span class="sxs-lookup"><span data-stu-id="f6814-126">Fiscal</span></span>

<span data-ttu-id="f6814-127">Kuiv alite väljal **Kulumiarvestusaasta** suvandi **Rahandusaasta**, kasutatakse allesjäänud eluea lineaarset kulumit.</span><span class="sxs-lookup"><span data-stu-id="f6814-127">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="f6814-128">Kulum arvutatakse järelejäänud rahandusaastate alusel.</span><span class="sxs-lookup"><span data-stu-id="f6814-128">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="f6814-129">Näiteks finantsaastal 1. juulist 2015 kuni 30. juunini 2016 käivitub kulumiarvestus 1. juulil.</span><span class="sxs-lookup"><span data-stu-id="f6814-129">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="f6814-130">Rahandusaasta võib olla pikem või lühem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="f6814-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="f6814-131">Iga rahandusperioodi kulumit korrigeeritakse.</span><span class="sxs-lookup"><span data-stu-id="f6814-131">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="f6814-132">Järgmise rahandusaasta pikkuse määravad rahandusperioodid, mis on seadistatud lehel **Rahanduskalendrid**.</span><span class="sxs-lookup"><span data-stu-id="f6814-132">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="f6814-133">Kui valite kulumiarvestusaasta **Rahandusaasta**, on väljal **Perioodi sagedus** saadaval järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="f6814-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f6814-134">**Kord aastas** sisestab rahandusaasta puhul arvutatud kulumi kogusumma ühe summana rahandusaasta viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="f6814-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="f6814-135">**Rahandusperiood** arvutab rahandusaasta kulumi kogusumma.</span><span class="sxs-lookup"><span data-stu-id="f6814-135">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="f6814-136">See summa kogutakse siis rahandusperioodidesse, mis on määratletud lehel **Rahaduskalendrid** raamatu jaoks määratud rahanduskalendri jaoks.</span><span class="sxs-lookup"><span data-stu-id="f6814-136">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="f6814-137">Muutmata põhivara lineaarse kulumi näide</span><span class="sxs-lookup"><span data-stu-id="f6814-137">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="f6814-138">Põhivaral on järgmised näitajad.</span><span class="sxs-lookup"><span data-stu-id="f6814-138">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="f6814-139">Soetusmaksumus</span><span class="sxs-lookup"><span data-stu-id="f6814-139">Acquisition cost</span></span>    | <span data-ttu-id="f6814-140">11 000</span><span class="sxs-lookup"><span data-stu-id="f6814-140">11,000</span></span> |
| <span data-ttu-id="f6814-141">Jääkväärtus</span><span class="sxs-lookup"><span data-stu-id="f6814-141">Salvage value</span></span>       | <span data-ttu-id="f6814-142">1000</span><span class="sxs-lookup"><span data-stu-id="f6814-142">1,000</span></span>  |
| <span data-ttu-id="f6814-143">Kulumiarvestuse alus</span><span class="sxs-lookup"><span data-stu-id="f6814-143">Depreciation base</span></span>   | <span data-ttu-id="f6814-144">10 000</span><span class="sxs-lookup"><span data-stu-id="f6814-144">10,000</span></span> |
| <span data-ttu-id="f6814-145">Kasutusea aastad</span><span class="sxs-lookup"><span data-stu-id="f6814-145">Service life years</span></span>  | <span data-ttu-id="f6814-146">5</span><span class="sxs-lookup"><span data-stu-id="f6814-146">5</span></span>      |
| <span data-ttu-id="f6814-147">Aastane kulumisumma</span><span class="sxs-lookup"><span data-stu-id="f6814-147">Yearly depreciation</span></span> | <span data-ttu-id="f6814-148">2 000</span><span class="sxs-lookup"><span data-stu-id="f6814-148">2,000</span></span>  |

<span data-ttu-id="f6814-149">Kulumisumma on igal aastal sama: (soetusmaksumus – jääkväärtus) ÷ kasuliku eluea aastad</span><span class="sxs-lookup"><span data-stu-id="f6814-149">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="f6814-150">Periood</span><span class="sxs-lookup"><span data-stu-id="f6814-150">Period</span></span> | <span data-ttu-id="f6814-151">Aasta kulumisumma arvutamine</span><span class="sxs-lookup"><span data-stu-id="f6814-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="f6814-152">Raamatupidamislik jääkväärtus aasta lõpus</span><span class="sxs-lookup"><span data-stu-id="f6814-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="f6814-153">aasta 1</span><span class="sxs-lookup"><span data-stu-id="f6814-153">Year 1</span></span> | <span data-ttu-id="f6814-154">(11 000 – 1000) ÷ 5 = 2000</span><span class="sxs-lookup"><span data-stu-id="f6814-154">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="f6814-155">9000</span><span class="sxs-lookup"><span data-stu-id="f6814-155">9,000</span></span>                                 |
| <span data-ttu-id="f6814-156">aasta 2</span><span class="sxs-lookup"><span data-stu-id="f6814-156">Year 2</span></span> | <span data-ttu-id="f6814-157">(9000 – 1000) ÷ 4 = 2000</span><span class="sxs-lookup"><span data-stu-id="f6814-157">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="f6814-158">7 000</span><span class="sxs-lookup"><span data-stu-id="f6814-158">7,000</span></span>                                 |
| <span data-ttu-id="f6814-159">aasta 3</span><span class="sxs-lookup"><span data-stu-id="f6814-159">Year 3</span></span> | <span data-ttu-id="f6814-160">(7000 – 1000) ÷ 3 = 2000</span><span class="sxs-lookup"><span data-stu-id="f6814-160">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="f6814-161">5 000</span><span class="sxs-lookup"><span data-stu-id="f6814-161">5,000</span></span>                                 |
| <span data-ttu-id="f6814-162">aasta 4</span><span class="sxs-lookup"><span data-stu-id="f6814-162">Year 4</span></span> | <span data-ttu-id="f6814-163">(5000 – 1000) ÷ 2 = 2000</span><span class="sxs-lookup"><span data-stu-id="f6814-163">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="f6814-164">3 000</span><span class="sxs-lookup"><span data-stu-id="f6814-164">3,000</span></span>                                 |
| <span data-ttu-id="f6814-165">aasta 5</span><span class="sxs-lookup"><span data-stu-id="f6814-165">Year 5</span></span> | <span data-ttu-id="f6814-166">(3000 – 1000) ÷ 1 = 2000</span><span class="sxs-lookup"><span data-stu-id="f6814-166">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="f6814-167">1000</span><span class="sxs-lookup"><span data-stu-id="f6814-167">1,000</span></span>                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]