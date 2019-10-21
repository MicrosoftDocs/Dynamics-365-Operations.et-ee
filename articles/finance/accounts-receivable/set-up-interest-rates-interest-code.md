---
title: Intressikoodile intressimäära seadistamine
description: Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188989"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="16ba8-103">Intressikoodile intressimäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="16ba8-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16ba8-104">Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="16ba8-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="16ba8-105">Saate seadistada ühe intressikoodi ja rakendada seda mitme kliendi sisestusreeglitele, arvelduskoodidele või kindlatele arveridadele.</span><span class="sxs-lookup"><span data-stu-id="16ba8-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="16ba8-106">Intressikoodi üksikasjade muutumisel rakendavad kõik koodi kasutavad funktsioonid muutusi automaatselt uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="16ba8-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="16ba8-107">Iga intressikoodi puhul saate seadistada kaht tüüpi määrasid.</span><span class="sxs-lookup"><span data-stu-id="16ba8-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="16ba8-108">Intressitulu määrad − need kujutavad endast tulu, mis on saadud arvete ja viivisearvete intressidest.</span><span class="sxs-lookup"><span data-stu-id="16ba8-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="16ba8-109">Intressimaksete määrad − need kujutavad endast kulu, mis tasutakse kreeditarvete intressidena.</span><span class="sxs-lookup"><span data-stu-id="16ba8-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="16ba8-110">Mõlemad määratüübid võivad eksisteerida samal ajal ja samas intressikoodis.</span><span class="sxs-lookup"><span data-stu-id="16ba8-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="16ba8-111">Intressimäärad võivad põhineda kolmel arvutamistüübil.</span><span class="sxs-lookup"><span data-stu-id="16ba8-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="16ba8-112">Intress protsendi järgi.</span><span class="sxs-lookup"><span data-stu-id="16ba8-112">Interest by percentage.</span></span>
-   <span data-ttu-id="16ba8-113">Intress summa järgi.</span><span class="sxs-lookup"><span data-stu-id="16ba8-113">Interest by amount.</span></span>
-   <span data-ttu-id="16ba8-114">Intress vahemiku järgi, mille tulemuseks on üksik protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="16ba8-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="16ba8-115">Kui intressi arvutamiseks kasutatakse intressikoodi, luuakse iga intressimäära kohta eraldi viivisearve, mis kehtib seni, kuni makse on ületanud kande tähtaja.</span><span class="sxs-lookup"><span data-stu-id="16ba8-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="16ba8-116">Vahekaardi **Tulud** abil lehel **Intressikood** saate seadistada intressimäärasid intressi jaoks, mida intressi küsides teenite.</span><span class="sxs-lookup"><span data-stu-id="16ba8-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="16ba8-117">Makstava intressi määra seadistamiseks kasutage vahekaarti **Maksed**.</span><span class="sxs-lookup"><span data-stu-id="16ba8-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="16ba8-118">Protsendil põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="16ba8-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="16ba8-119">Saate seadistada intressimäärad, mis arvutavad kindlaksmääratud protsendi.</span><span class="sxs-lookup"><span data-stu-id="16ba8-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="16ba8-120">Intressimäär kehtib kõigile valuutadele.</span><span class="sxs-lookup"><span data-stu-id="16ba8-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="16ba8-121">Sisestada saab valikulisi intressisumma limiite.</span><span class="sxs-lookup"><span data-stu-id="16ba8-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="16ba8-122"><strong>Protsent</strong> valitakse väljal\*\* <strong>\*\*Intressi arvutusalus:</strong> lehel <strong>Intressikoodide</strong> seadistamine.</span><span class="sxs-lookup"><span data-stu-id="16ba8-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="16ba8-123">Näiteks intressikoodi seadistamiseks, mis määrab 5 protsenti intressi iga kahe kuu eest, mille võrra arve makse ületab kande tähtaega, tuleks sisestada 2 väljale **Arvuta intress iga** ja valida **Kuu**.</span><span class="sxs-lookup"><span data-stu-id="16ba8-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="16ba8-124">Summal põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="16ba8-124">Interest rates based on amounts</span></span>
<span data-ttu-id="16ba8-125">Saate seadistada intressimäärad, mis arvutavad määratud summa valuuta kaupa.</span><span class="sxs-lookup"><span data-stu-id="16ba8-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="16ba8-126">Intressi summa määratakse iga intressikoodi valuuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="16ba8-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="16ba8-127">Sisestada saab valikulisi intressisumma limiite.</span><span class="sxs-lookup"><span data-stu-id="16ba8-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="16ba8-128">**Summa** valitakse väljal **Intressi arvutusalus** lehel **Intressikoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="16ba8-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="16ba8-129">Näiteks intressikoodi seadistamiseks, mis määrab 25,00 protsenti intressi iga 20 päeva eest, mille võrra arve makse ületab kande tähtaega, tuleks sisestada 20 väljale **Arvuta intress iga** ja valida **Päev**.</span><span class="sxs-lookup"><span data-stu-id="16ba8-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="16ba8-130">Vahemikel põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="16ba8-130">Interest rates based on ranges</span></span>
<span data-ttu-id="16ba8-131">Saate seadistada intressimäärad, mis varieeruvad sõltuvalt tähtaja ületanud summast, summa hilinemise päevadest või kuudest.</span><span class="sxs-lookup"><span data-stu-id="16ba8-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="16ba8-132">Saate kasutada vahekaarti **Tulud valuuta järgi** konkreetsete intressisätete määratlemiseks iga valuuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="16ba8-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="16ba8-133">Siin saate määratleda ka vahemiku.</span><span class="sxs-lookup"><span data-stu-id="16ba8-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="16ba8-134">Lisage nupuga **Vahemikud** ridu, mis kajastavad vahemikke, mida seadistada soovite.</span><span class="sxs-lookup"><span data-stu-id="16ba8-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="16ba8-135">Väärtus **Alates** kajastab vahemiku algust ja arv **Intressi väärtus** kajastab kas protsenti või summat, sõltuvalt valikust väljal **Intressi arvutusalus:** lehel **Intressikoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="16ba8-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="16ba8-136">Näide 1: Intress vahemiku järgi = summa</span><span class="sxs-lookup"><span data-stu-id="16ba8-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="16ba8-137">Saate seadistada intressikoodi, mis määrab intressi üks kord iga kolme kuu tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="16ba8-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="16ba8-138">Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele summaintervallidele.</span><span class="sxs-lookup"><span data-stu-id="16ba8-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="16ba8-139">Intressi väärtus on 1 protsent arvesummadest kuni 1000.00, 2 protsenti summadest alates 1001.00 kuni 5000.00 ja 3 protsenti summadest, mis on suuremad kui 5000.00.</span><span class="sxs-lookup"><span data-stu-id="16ba8-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="16ba8-140">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="16ba8-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="16ba8-141">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="16ba8-141">**Field name**</span></span>                  | <span data-ttu-id="16ba8-142">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="16ba8-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="16ba8-143">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="16ba8-143">**Interest code**</span></span>               | <span data-ttu-id="16ba8-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="16ba8-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="16ba8-145">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="16ba8-145">**Calculate interest every**</span></span>    | <span data-ttu-id="16ba8-146">3/kuu</span><span class="sxs-lookup"><span data-stu-id="16ba8-146">3/Month</span></span>         |
| <span data-ttu-id="16ba8-147">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="16ba8-147">**Interest by range**</span></span>           | <span data-ttu-id="16ba8-148">Summa</span><span class="sxs-lookup"><span data-stu-id="16ba8-148">Amount</span></span>          |
| <span data-ttu-id="16ba8-149">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="16ba8-149">**Calculate interest based on**</span></span> | <span data-ttu-id="16ba8-150">Protsent</span><span class="sxs-lookup"><span data-stu-id="16ba8-150">Percentage</span></span>      |

<span data-ttu-id="16ba8-151">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="16ba8-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="16ba8-152">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="16ba8-152">**From value**</span></span> | <span data-ttu-id="16ba8-153">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="16ba8-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="16ba8-154">0</span><span class="sxs-lookup"><span data-stu-id="16ba8-154">0</span></span>              | <span data-ttu-id="16ba8-155">1</span><span class="sxs-lookup"><span data-stu-id="16ba8-155">1</span></span>                  |
| <span data-ttu-id="16ba8-156">1,001</span><span class="sxs-lookup"><span data-stu-id="16ba8-156">1,001</span></span>          | <span data-ttu-id="16ba8-157">2</span><span class="sxs-lookup"><span data-stu-id="16ba8-157">2</span></span>                  |
| <span data-ttu-id="16ba8-158">5,001</span><span class="sxs-lookup"><span data-stu-id="16ba8-158">5,001</span></span>          | <span data-ttu-id="16ba8-159">3</span><span class="sxs-lookup"><span data-stu-id="16ba8-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="16ba8-160">Näide 2: Intress vahemiku järgi = päevad</span><span class="sxs-lookup"><span data-stu-id="16ba8-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="16ba8-161">Saate seadistada intressikoodi, mis määrab intressi üks kord iga 15 päeva tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="16ba8-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="16ba8-162">Soovite arvutuse aluseks võtta summapõhise intressiväärtuse, vastavalt astmelistele päevaintervallidele.</span><span class="sxs-lookup"><span data-stu-id="16ba8-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="16ba8-163">Intressi väärtus on 10.00 15 päeva kohta esimese 60 päeva jooksul, 15.00 15 päeva kohta päevadel 61 kuni 90 ja 20.00 15 päeva kohta 91. päevast edasi.</span><span class="sxs-lookup"><span data-stu-id="16ba8-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="16ba8-164">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="16ba8-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="16ba8-165">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="16ba8-165">**Field name**</span></span>                  | <span data-ttu-id="16ba8-166">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="16ba8-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="16ba8-167">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="16ba8-167">**Interest code**</span></span>               | <span data-ttu-id="16ba8-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="16ba8-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="16ba8-169">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="16ba8-169">**Calculate interest every**</span></span>    | <span data-ttu-id="16ba8-170">15/päev</span><span class="sxs-lookup"><span data-stu-id="16ba8-170">15/Day</span></span>          |
| <span data-ttu-id="16ba8-171">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="16ba8-171">**Interest by range**</span></span>           | <span data-ttu-id="16ba8-172">Päevi</span><span class="sxs-lookup"><span data-stu-id="16ba8-172">Days</span></span>            |
| <span data-ttu-id="16ba8-173">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="16ba8-173">**Calculate interest based on**</span></span> | <span data-ttu-id="16ba8-174">Summa</span><span class="sxs-lookup"><span data-stu-id="16ba8-174">Amount</span></span>          |

<span data-ttu-id="16ba8-175">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="16ba8-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="16ba8-176">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="16ba8-176">**From value**</span></span> | <span data-ttu-id="16ba8-177">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="16ba8-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="16ba8-178">0</span><span class="sxs-lookup"><span data-stu-id="16ba8-178">0</span></span>              | <span data-ttu-id="16ba8-179">10</span><span class="sxs-lookup"><span data-stu-id="16ba8-179">10</span></span>                 |
| <span data-ttu-id="16ba8-180">61</span><span class="sxs-lookup"><span data-stu-id="16ba8-180">61</span></span>             | <span data-ttu-id="16ba8-181">15</span><span class="sxs-lookup"><span data-stu-id="16ba8-181">15</span></span>                 |
| <span data-ttu-id="16ba8-182">91</span><span class="sxs-lookup"><span data-stu-id="16ba8-182">91</span></span>             | <span data-ttu-id="16ba8-183">20</span><span class="sxs-lookup"><span data-stu-id="16ba8-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="16ba8-184">Näide 3: Intress vahemiku järgi = kuud</span><span class="sxs-lookup"><span data-stu-id="16ba8-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="16ba8-185">Saate seadistada intressikoodi, mis määrab intressi üks kord iga kuu tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="16ba8-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="16ba8-186">Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele kuuintervallidele.</span><span class="sxs-lookup"><span data-stu-id="16ba8-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="16ba8-187">Intressi väärtus on 1,5 protsenti kuus kolmel esimesel tähtaja ületanud kuul, 2,0 protsenti kuus järgmised kolm kuud ja 2,5 protsenti kuus kõigil järgnevatel kuudel.</span><span class="sxs-lookup"><span data-stu-id="16ba8-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="16ba8-188">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="16ba8-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="16ba8-189">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="16ba8-189">**Field name**</span></span>                  | <span data-ttu-id="16ba8-190">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="16ba8-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="16ba8-191">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="16ba8-191">**Interest code**</span></span>               | <span data-ttu-id="16ba8-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="16ba8-192">1M%ByMth</span></span>        |
| <span data-ttu-id="16ba8-193">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="16ba8-193">**Calculate interest every**</span></span>    | <span data-ttu-id="16ba8-194">1/kuu</span><span class="sxs-lookup"><span data-stu-id="16ba8-194">1/Month</span></span>         |
| <span data-ttu-id="16ba8-195">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="16ba8-195">**Interest by range**</span></span>           | <span data-ttu-id="16ba8-196">Kuud</span><span class="sxs-lookup"><span data-stu-id="16ba8-196">Months</span></span>          |
| <span data-ttu-id="16ba8-197">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="16ba8-197">**Calculate interest based on**</span></span> | <span data-ttu-id="16ba8-198">Protsent</span><span class="sxs-lookup"><span data-stu-id="16ba8-198">Percentage</span></span>      |

<span data-ttu-id="16ba8-199">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="16ba8-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="16ba8-200">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="16ba8-200">**From value**</span></span> | <span data-ttu-id="16ba8-201">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="16ba8-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="16ba8-202">0</span><span class="sxs-lookup"><span data-stu-id="16ba8-202">0</span></span>              | <span data-ttu-id="16ba8-203">1.5</span><span class="sxs-lookup"><span data-stu-id="16ba8-203">1.5</span></span>                |
| <span data-ttu-id="16ba8-204">4</span><span class="sxs-lookup"><span data-stu-id="16ba8-204">4</span></span>              | <span data-ttu-id="16ba8-205">2</span><span class="sxs-lookup"><span data-stu-id="16ba8-205">2</span></span>                  |
| <span data-ttu-id="16ba8-206">7</span><span class="sxs-lookup"><span data-stu-id="16ba8-206">7</span></span>              | <span data-ttu-id="16ba8-207">2,5</span><span class="sxs-lookup"><span data-stu-id="16ba8-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="16ba8-208">Uued versioonid</span><span class="sxs-lookup"><span data-stu-id="16ba8-208">New versions</span></span>
<span data-ttu-id="16ba8-209">Intressikoodidel on kehtivuskuupäevad.</span><span class="sxs-lookup"><span data-stu-id="16ba8-209">Interest codes are date effective.</span></span> <span data-ttu-id="16ba8-210">Kui soovite intressimäära muuta, saate luua **uue versiooni**, mis kehtib tulevasest kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="16ba8-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="16ba8-211">Erinevate versioonide vaatamiseks võite kasutada kuupäeva valimiseks menüüvalikut **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="16ba8-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="16ba8-212">Saate valida ka **Kuva kõik kirjed** kõigi intressikoodide kuvamiseks lehel.</span><span class="sxs-lookup"><span data-stu-id="16ba8-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



