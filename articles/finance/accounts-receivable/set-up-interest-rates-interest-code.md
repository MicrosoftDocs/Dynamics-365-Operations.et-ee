---
title: Intressikoodile intressimäära seadistamine
description: Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62868c30d3ff60e51d99c71b743ab0bbb3c87451
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5835192"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="63470-103">Intressikoodile intressimäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="63470-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63470-104">Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="63470-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="63470-105">Saate seadistada ühe intressikoodi ja rakendada seda mitme kliendi sisestusreeglitele, arvelduskoodidele või kindlatele arveridadele.</span><span class="sxs-lookup"><span data-stu-id="63470-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="63470-106">Intressikoodi üksikasjade muutumisel rakendavad kõik koodi kasutavad funktsioonid muutusi automaatselt uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="63470-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="63470-107">Iga intressikoodi puhul saate seadistada kaht tüüpi määrasid.</span><span class="sxs-lookup"><span data-stu-id="63470-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="63470-108">Intressitulu määrad − need kujutavad endast tulu, mis on saadud arvete ja viivisearvete intressidest.</span><span class="sxs-lookup"><span data-stu-id="63470-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="63470-109">Intressimaksete määrad − need kujutavad endast kulu, mis tasutakse kreeditarvete intressidena.</span><span class="sxs-lookup"><span data-stu-id="63470-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="63470-110">Mõlemad määratüübid võivad eksisteerida samal ajal ja samas intressikoodis.</span><span class="sxs-lookup"><span data-stu-id="63470-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="63470-111">Intressimäärad võivad põhineda kolmel arvutamistüübil.</span><span class="sxs-lookup"><span data-stu-id="63470-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="63470-112">Intress protsendi järgi.</span><span class="sxs-lookup"><span data-stu-id="63470-112">Interest by percentage.</span></span>
-   <span data-ttu-id="63470-113">Intress summa järgi.</span><span class="sxs-lookup"><span data-stu-id="63470-113">Interest by amount.</span></span>
-   <span data-ttu-id="63470-114">Intress vahemiku järgi, mille tulemuseks on üksik protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="63470-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="63470-115">Kui intressi arvutamiseks kasutatakse intressikoodi, luuakse iga intressimäära kohta eraldi viivisearve, mis kehtib seni, kuni makse on ületanud kande tähtaja.</span><span class="sxs-lookup"><span data-stu-id="63470-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="63470-116">Vahekaardi **Tulud** abil lehel **Intressikood** saate seadistada intressimäärasid intressi jaoks, mida intressi küsides teenite.</span><span class="sxs-lookup"><span data-stu-id="63470-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="63470-117">Makstava intressi määra seadistamiseks kasutage vahekaarti **Maksed**.</span><span class="sxs-lookup"><span data-stu-id="63470-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="63470-118">Protsendil põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="63470-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="63470-119">Saate seadistada intressimäärad, mis arvutavad kindlaksmääratud protsendi.</span><span class="sxs-lookup"><span data-stu-id="63470-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="63470-120">Intressimäär kehtib kõigile valuutadele.</span><span class="sxs-lookup"><span data-stu-id="63470-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="63470-121">Sisestada saab valikulisi intressisumma limiite.</span><span class="sxs-lookup"><span data-stu-id="63470-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="63470-122">**Protsent** valitakse väljal **Intressi arvutusalus mis põhineb** väljal **Intressikoodide seadistamine** lehel.</span><span class="sxs-lookup"><span data-stu-id="63470-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="63470-123">Näiteks intressikoodi seadistamiseks, mis määrab 5 protsenti intressi iga kahe kuu eest, mille võrra arve makse ületab kande tähtaega, tuleks sisestada 2 väljale **Arvuta intress iga** ja valida **Kuu**.</span><span class="sxs-lookup"><span data-stu-id="63470-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="63470-124">Viivisearve arvutamise uus algoritm lisatakse funktsioonihalduse abil.</span><span class="sxs-lookup"><span data-stu-id="63470-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="63470-125">Selle algoritmi kasutamiseks lubage **(GBL) Lubage arvutada päeva viivist iga-aastase protsendina jagatuna 365** funktsioon.</span><span class="sxs-lookup"><span data-stu-id="63470-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="63470-126">Lisateavet funktsioonide lubamise kohta, vaata [Funktsioonihalduse ülevaade](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="63470-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="63470-127">Viivisearve summa arvutamise valem on:</span><span class="sxs-lookup"><span data-stu-id="63470-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="63470-128">Viivisearve summa = võlgnetav summa \* Aastane viiviseprotsent % / 365 \* Hilinemispäevade arv</span><span class="sxs-lookup"><span data-stu-id="63470-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="63470-129">See funktsioon on saadaval rakenduses versioonis 10.0.18 ja uuemas.</span><span class="sxs-lookup"><span data-stu-id="63470-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="63470-130">Summal põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="63470-130">Interest rates based on amounts</span></span>
<span data-ttu-id="63470-131">Saate seadistada intressimäärad, mis arvutavad määratud summa valuuta kaupa.</span><span class="sxs-lookup"><span data-stu-id="63470-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="63470-132">Intressi summa määratakse iga intressikoodi valuuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="63470-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="63470-133">Sisestada saab valikulisi intressisumma limiite.</span><span class="sxs-lookup"><span data-stu-id="63470-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="63470-134">**Summa** valitakse väljal **Intressi arvutusalus** lehel **Intressikoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="63470-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="63470-135">Näiteks intressikoodi seadistamiseks, mis määrab 25,00 protsenti intressi iga 20 päeva eest, mille võrra arve makse ületab kande tähtaega, tuleks sisestada 20 väljale **Arvuta intress iga** ja valida **Päev**.</span><span class="sxs-lookup"><span data-stu-id="63470-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="63470-136">Vahemikel põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="63470-136">Interest rates based on ranges</span></span>
<span data-ttu-id="63470-137">Saate seadistada intressimäärad, mis varieeruvad sõltuvalt tähtaja ületanud summast, summa hilinemise päevadest või kuudest.</span><span class="sxs-lookup"><span data-stu-id="63470-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="63470-138">Saate kasutada vahekaarti **Tulud valuuta järgi** konkreetsete intressisätete määratlemiseks iga valuuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="63470-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="63470-139">Siin saate määratleda ka vahemiku.</span><span class="sxs-lookup"><span data-stu-id="63470-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="63470-140">Lisage nupuga **Vahemikud** ridu, mis kajastavad vahemikke, mida seadistada soovite.</span><span class="sxs-lookup"><span data-stu-id="63470-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="63470-141">Väärtus **Alates** kajastab vahemiku algust ja arv **Intressi väärtus** kajastab kas protsenti või summat, sõltuvalt valikust väljal **Intressi arvutusalus:** lehel **Intressikoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="63470-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="63470-142">Näide 1: Intress vahemiku järgi = summa</span><span class="sxs-lookup"><span data-stu-id="63470-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="63470-143">Saate seadistada intressikoodi, mis määrab intressi üks kord iga kolme kuu tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="63470-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="63470-144">Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele summaintervallidele.</span><span class="sxs-lookup"><span data-stu-id="63470-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="63470-145">Intressi väärtus on 1 protsent arvesummadest kuni 1000.00, 2 protsenti summadest alates 1001.00 kuni 5000.00 ja 3 protsenti summadest, mis on suuremad kui 5000.00.</span><span class="sxs-lookup"><span data-stu-id="63470-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="63470-146">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="63470-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="63470-147">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="63470-147">**Field name**</span></span>                  | <span data-ttu-id="63470-148">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="63470-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="63470-149">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="63470-149">**Interest code**</span></span>               | <span data-ttu-id="63470-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="63470-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="63470-151">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="63470-151">**Calculate interest every**</span></span>    | <span data-ttu-id="63470-152">3/kuu</span><span class="sxs-lookup"><span data-stu-id="63470-152">3/Month</span></span>         |
| <span data-ttu-id="63470-153">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="63470-153">**Interest by range**</span></span>           | <span data-ttu-id="63470-154">Summa</span><span class="sxs-lookup"><span data-stu-id="63470-154">Amount</span></span>          |
| <span data-ttu-id="63470-155">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="63470-155">**Calculate interest based on**</span></span> | <span data-ttu-id="63470-156">Protsent</span><span class="sxs-lookup"><span data-stu-id="63470-156">Percentage</span></span>      |

<span data-ttu-id="63470-157">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="63470-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="63470-158">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="63470-158">**From value**</span></span> | <span data-ttu-id="63470-159">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="63470-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="63470-160">0</span><span class="sxs-lookup"><span data-stu-id="63470-160">0</span></span>              | <span data-ttu-id="63470-161">1</span><span class="sxs-lookup"><span data-stu-id="63470-161">1</span></span>                  |
| <span data-ttu-id="63470-162">1,001</span><span class="sxs-lookup"><span data-stu-id="63470-162">1,001</span></span>          | <span data-ttu-id="63470-163">2</span><span class="sxs-lookup"><span data-stu-id="63470-163">2</span></span>                  |
| <span data-ttu-id="63470-164">5,001</span><span class="sxs-lookup"><span data-stu-id="63470-164">5,001</span></span>          | <span data-ttu-id="63470-165">3</span><span class="sxs-lookup"><span data-stu-id="63470-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="63470-166">Näide 2: Intress vahemiku järgi = päevad</span><span class="sxs-lookup"><span data-stu-id="63470-166">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="63470-167">Saate seadistada intressikoodi, mis määrab intressi üks kord iga 15 päeva tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="63470-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="63470-168">Soovite arvutuse aluseks võtta summapõhise intressiväärtuse, vastavalt astmelistele päevaintervallidele.</span><span class="sxs-lookup"><span data-stu-id="63470-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="63470-169">Intressi väärtus on 10.00 15 päeva kohta esimese 60 päeva jooksul, 15.00 15 päeva kohta päevadel 61 kuni 90 ja 20.00 15 päeva kohta 91. päevast edasi.</span><span class="sxs-lookup"><span data-stu-id="63470-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="63470-170">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="63470-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="63470-171">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="63470-171">**Field name**</span></span>                  | <span data-ttu-id="63470-172">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="63470-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="63470-173">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="63470-173">**Interest code**</span></span>               | <span data-ttu-id="63470-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="63470-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="63470-175">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="63470-175">**Calculate interest every**</span></span>    | <span data-ttu-id="63470-176">15/päev</span><span class="sxs-lookup"><span data-stu-id="63470-176">15/Day</span></span>          |
| <span data-ttu-id="63470-177">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="63470-177">**Interest by range**</span></span>           | <span data-ttu-id="63470-178">Päevi</span><span class="sxs-lookup"><span data-stu-id="63470-178">Days</span></span>            |
| <span data-ttu-id="63470-179">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="63470-179">**Calculate interest based on**</span></span> | <span data-ttu-id="63470-180">Summa</span><span class="sxs-lookup"><span data-stu-id="63470-180">Amount</span></span>          |

<span data-ttu-id="63470-181">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="63470-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="63470-182">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="63470-182">**From value**</span></span> | <span data-ttu-id="63470-183">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="63470-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="63470-184">0</span><span class="sxs-lookup"><span data-stu-id="63470-184">0</span></span>              | <span data-ttu-id="63470-185">10</span><span class="sxs-lookup"><span data-stu-id="63470-185">10</span></span>                 |
| <span data-ttu-id="63470-186">61</span><span class="sxs-lookup"><span data-stu-id="63470-186">61</span></span>             | <span data-ttu-id="63470-187">15</span><span class="sxs-lookup"><span data-stu-id="63470-187">15</span></span>                 |
| <span data-ttu-id="63470-188">91</span><span class="sxs-lookup"><span data-stu-id="63470-188">91</span></span>             | <span data-ttu-id="63470-189">20</span><span class="sxs-lookup"><span data-stu-id="63470-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="63470-190">Näide 3: Intress vahemiku järgi = kuud</span><span class="sxs-lookup"><span data-stu-id="63470-190">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="63470-191">Saate seadistada intressikoodi, mis määrab intressi üks kord iga kuu tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="63470-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="63470-192">Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele kuuintervallidele.</span><span class="sxs-lookup"><span data-stu-id="63470-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="63470-193">Intressi väärtus on 1,5 protsenti kuus kolmel esimesel tähtaja ületanud kuul, 2,0 protsenti kuus järgmised kolm kuud ja 2,5 protsenti kuus kõigil järgnevatel kuudel.</span><span class="sxs-lookup"><span data-stu-id="63470-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="63470-194">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="63470-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="63470-195">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="63470-195">**Field name**</span></span>                  | <span data-ttu-id="63470-196">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="63470-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="63470-197">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="63470-197">**Interest code**</span></span>               | <span data-ttu-id="63470-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="63470-198">1M%ByMth</span></span>        |
| <span data-ttu-id="63470-199">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="63470-199">**Calculate interest every**</span></span>    | <span data-ttu-id="63470-200">1/kuu</span><span class="sxs-lookup"><span data-stu-id="63470-200">1/Month</span></span>         |
| <span data-ttu-id="63470-201">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="63470-201">**Interest by range**</span></span>           | <span data-ttu-id="63470-202">Kuud</span><span class="sxs-lookup"><span data-stu-id="63470-202">Months</span></span>          |
| <span data-ttu-id="63470-203">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="63470-203">**Calculate interest based on**</span></span> | <span data-ttu-id="63470-204">Protsent</span><span class="sxs-lookup"><span data-stu-id="63470-204">Percentage</span></span>      |

<span data-ttu-id="63470-205">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="63470-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="63470-206">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="63470-206">**From value**</span></span> | <span data-ttu-id="63470-207">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="63470-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="63470-208">0</span><span class="sxs-lookup"><span data-stu-id="63470-208">0</span></span>              | <span data-ttu-id="63470-209">1.5</span><span class="sxs-lookup"><span data-stu-id="63470-209">1.5</span></span>                |
| <span data-ttu-id="63470-210">4</span><span class="sxs-lookup"><span data-stu-id="63470-210">4</span></span>              | <span data-ttu-id="63470-211">2</span><span class="sxs-lookup"><span data-stu-id="63470-211">2</span></span>                  |
| <span data-ttu-id="63470-212">7</span><span class="sxs-lookup"><span data-stu-id="63470-212">7</span></span>              | <span data-ttu-id="63470-213">2,5</span><span class="sxs-lookup"><span data-stu-id="63470-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="63470-214">Uued versioonid</span><span class="sxs-lookup"><span data-stu-id="63470-214">New versions</span></span>
<span data-ttu-id="63470-215">Intressikoodidel on kehtivuskuupäevad.</span><span class="sxs-lookup"><span data-stu-id="63470-215">Interest codes are date effective.</span></span> <span data-ttu-id="63470-216">Kui soovite intressimäära muuta, saate luua **uue versiooni**, mis kehtib tulevasest kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="63470-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="63470-217">Erinevate versioonide vaatamiseks võite kasutada kuupäeva valimiseks menüüvalikut **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="63470-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="63470-218">Saate valida ka **Kuva kõik kirjed** kõigi intressikoodide kuvamiseks lehel.</span><span class="sxs-lookup"><span data-stu-id="63470-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
