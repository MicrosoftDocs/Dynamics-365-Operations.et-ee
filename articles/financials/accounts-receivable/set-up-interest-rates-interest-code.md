---
title: "Intressikoodile intressimäära seadistamine"
description: "Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7ae0bfdc157a7e2e5b9f871dae487a6f85e889b9
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="2d58d-103">Intressikoodile intressimäära seadistamine</span><span class="sxs-lookup"><span data-stu-id="2d58d-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2d58d-104">Intressikoodid sisaldavad sätteid, mis määratlevad, millal intressi võetakse ja kuidas seda arvutatakse tähtaja ületanud arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="2d58d-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="2d58d-105">Saate seadistada ühe intressikoodi ja rakendada seda mitme kliendi sisestusreeglitele, arvelduskoodidele või kindlatele arveridadele.</span><span class="sxs-lookup"><span data-stu-id="2d58d-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="2d58d-106">Intressikoodi üksikasjade muutumisel rakendavad kõik koodi kasutavad funktsioonid muutusi automaatselt uutele kannetele.</span><span class="sxs-lookup"><span data-stu-id="2d58d-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="2d58d-107">Iga intressikoodi puhul saate seadistada kaht tüüpi määrasid.</span><span class="sxs-lookup"><span data-stu-id="2d58d-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="2d58d-108">Intressitulu määrad − need kujutavad endast tulu, mis on saadud arvete ja viivisearvete intressidest.</span><span class="sxs-lookup"><span data-stu-id="2d58d-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="2d58d-109">Intressimaksete määrad − need kujutavad endast kulu, mis tasutakse kreeditarvete intressidena.</span><span class="sxs-lookup"><span data-stu-id="2d58d-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="2d58d-110">Mõlemad määratüübid võivad eksisteerida samal ajal ja samas intressikoodis.</span><span class="sxs-lookup"><span data-stu-id="2d58d-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="2d58d-111">Intressimäärad võivad põhineda kolmel arvutamistüübil.</span><span class="sxs-lookup"><span data-stu-id="2d58d-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="2d58d-112">Intress protsendi järgi.</span><span class="sxs-lookup"><span data-stu-id="2d58d-112">Interest by percentage.</span></span>
-   <span data-ttu-id="2d58d-113">Intress summa järgi.</span><span class="sxs-lookup"><span data-stu-id="2d58d-113">Interest by amount.</span></span>
-   <span data-ttu-id="2d58d-114">Intress vahemiku järgi, mille tulemuseks on üksik protsent või summa.</span><span class="sxs-lookup"><span data-stu-id="2d58d-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="2d58d-115">Kui intressi arvutamiseks kasutatakse intressikoodi, luuakse iga intressimäära kohta eraldi viivisearve, mis kehtib seni, kuni makse on ületanud kande tähtaja.</span><span class="sxs-lookup"><span data-stu-id="2d58d-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="2d58d-116">Vahekaardi **Tulud** abil lehel **Intressikood** saate seadistada intressimäärasid intressi jaoks, mida intressi küsides teenite.</span><span class="sxs-lookup"><span data-stu-id="2d58d-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="2d58d-117">Makstava intressi määra seadistamiseks kasutage vahekaarti **Maksed**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="2d58d-118">Protsendil põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="2d58d-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="2d58d-119">Saate seadistada intressimäärad, mis arvutavad kindlaksmääratud protsendi.</span><span class="sxs-lookup"><span data-stu-id="2d58d-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="2d58d-120">Intressimäär kehtib kõigile valuutadele.</span><span class="sxs-lookup"><span data-stu-id="2d58d-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="2d58d-121">Sisestada saab valikulisi intressisumma limiite.</span><span class="sxs-lookup"><span data-stu-id="2d58d-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="2d58d-122">**Protsent** valitakse** **väljal **Intressi arvutusalus** lehel **Intressikoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="2d58d-123">Näiteks intressikoodi seadistamiseks, mis määrab 5 protsenti intressi iga kahe kuu eest, mille võrra arve makse ületab kande tähtaega, tuleks sisestada 2 väljale **Arvuta intress iga** ja valida **Kuu**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="2d58d-124">Summal põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="2d58d-124">Interest rates based on amounts</span></span>
<span data-ttu-id="2d58d-125">Saate seadistada intressimäärad, mis arvutavad määratud summa valuuta kaupa.</span><span class="sxs-lookup"><span data-stu-id="2d58d-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="2d58d-126">Intressi summa määratakse iga intressikoodi valuuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="2d58d-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="2d58d-127">Sisestada saab valikulisi intressisumma limiite.</span><span class="sxs-lookup"><span data-stu-id="2d58d-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="2d58d-128">Väärtus **Summa **valitakse väljal **Intressi arvutusalus** lehel **Viivisekoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="2d58d-129">Näiteks intressikoodi seadistamiseks, mis määrab 25,00 protsenti intressi iga 20 päeva eest, mille võrra arve makse ületab kande tähtaega, tuleks sisestada 20 väljale **Arvuta intress iga** ja valida **Päev**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="2d58d-130">Vahemikel põhinevad intressimäärad</span><span class="sxs-lookup"><span data-stu-id="2d58d-130">Interest rates based on ranges</span></span>
<span data-ttu-id="2d58d-131">Saate seadistada intressimäärad, mis varieeruvad sõltuvalt tähtaja ületanud summast, summa hilinemise päevadest või kuudest.</span><span class="sxs-lookup"><span data-stu-id="2d58d-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="2d58d-132">Saate kasutada vahekaarti **Tulud valuuta järgi** konkreetsete intressisätete määratlemiseks iga valuuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="2d58d-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="2d58d-133">Siin saate määratleda ka vahemiku.</span><span class="sxs-lookup"><span data-stu-id="2d58d-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="2d58d-134">Lisage nupuga **Vahemikud** ridu, mis kajastavad vahemikke, mida seadistada soovite.</span><span class="sxs-lookup"><span data-stu-id="2d58d-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="2d58d-135">Väärtus **Alates** kajastab vahemiku algust ja arv **Intressi väärtus** kajastab kas protsenti või summat, sõltuvalt valikust väljal **Intressi arvutusalus:** lehel **Intressikoodide seadistamine**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="2d58d-136">Näide 1: Intress vahemiku järgi = summa</span><span class="sxs-lookup"><span data-stu-id="2d58d-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="2d58d-137">Saate seadistada intressikoodi, mis määrab intressi üks kord iga kolme kuu tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="2d58d-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="2d58d-138">Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele summaintervallidele.</span><span class="sxs-lookup"><span data-stu-id="2d58d-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="2d58d-139">Intressi väärtus on 1 protsent arvesummadest kuni 1000.00, 2 protsenti summadest alates 1001.00 kuni 5000.00 ja 3 protsenti summadest, mis on suuremad kui 5000.00.</span><span class="sxs-lookup"><span data-stu-id="2d58d-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="2d58d-140">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d58d-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="2d58d-141">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="2d58d-141">**Field name**</span></span>                  | <span data-ttu-id="2d58d-142">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="2d58d-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="2d58d-143">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="2d58d-143">**Interest code**</span></span>               | <span data-ttu-id="2d58d-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="2d58d-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="2d58d-145">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="2d58d-145">**Calculate interest every**</span></span>    | <span data-ttu-id="2d58d-146">3/kuu</span><span class="sxs-lookup"><span data-stu-id="2d58d-146">3/Month</span></span>         |
| <span data-ttu-id="2d58d-147">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="2d58d-147">**Interest by range**</span></span>           | <span data-ttu-id="2d58d-148">Summa</span><span class="sxs-lookup"><span data-stu-id="2d58d-148">Amount</span></span>          |
| <span data-ttu-id="2d58d-149">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="2d58d-149">**Calculate interest based on**</span></span> | <span data-ttu-id="2d58d-150">Protsent</span><span class="sxs-lookup"><span data-stu-id="2d58d-150">Percentage</span></span>      |

<span data-ttu-id="2d58d-151">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d58d-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="2d58d-152">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="2d58d-152">**From value**</span></span> | <span data-ttu-id="2d58d-153">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="2d58d-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="2d58d-154">0</span><span class="sxs-lookup"><span data-stu-id="2d58d-154">0</span></span>              | <span data-ttu-id="2d58d-155">1</span><span class="sxs-lookup"><span data-stu-id="2d58d-155">1</span></span>                  |
| <span data-ttu-id="2d58d-156">1,001</span><span class="sxs-lookup"><span data-stu-id="2d58d-156">1,001</span></span>          | <span data-ttu-id="2d58d-157">2</span><span class="sxs-lookup"><span data-stu-id="2d58d-157">2</span></span>                  |
| <span data-ttu-id="2d58d-158">5,001</span><span class="sxs-lookup"><span data-stu-id="2d58d-158">5,001</span></span>          | <span data-ttu-id="2d58d-159">3</span><span class="sxs-lookup"><span data-stu-id="2d58d-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="2d58d-160">Näide 2: Intress vahemiku järgi = päevad</span><span class="sxs-lookup"><span data-stu-id="2d58d-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="2d58d-161">Saate seadistada intressikoodi, mis määrab intressi üks kord iga 15 päeva tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="2d58d-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="2d58d-162">Soovite arvutuse aluseks võtta summapõhise intressiväärtuse, vastavalt astmelistele päevaintervallidele.</span><span class="sxs-lookup"><span data-stu-id="2d58d-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="2d58d-163">Intressi väärtus on 10.00 15 päeva kohta esimese 60 päeva jooksul, 15.00 15 päeva kohta päevadel 61 kuni 90 ja 20.00 15 päeva kohta 91. päevast edasi.</span><span class="sxs-lookup"><span data-stu-id="2d58d-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="2d58d-164">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d58d-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="2d58d-165">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="2d58d-165">**Field name**</span></span>                  | <span data-ttu-id="2d58d-166">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="2d58d-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="2d58d-167">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="2d58d-167">**Interest code**</span></span>               | <span data-ttu-id="2d58d-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="2d58d-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="2d58d-169">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="2d58d-169">**Calculate interest every**</span></span>    | <span data-ttu-id="2d58d-170">15/päev</span><span class="sxs-lookup"><span data-stu-id="2d58d-170">15/Day</span></span>          |
| <span data-ttu-id="2d58d-171">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="2d58d-171">**Interest by range**</span></span>           | <span data-ttu-id="2d58d-172">Päevi</span><span class="sxs-lookup"><span data-stu-id="2d58d-172">Days</span></span>            |
| <span data-ttu-id="2d58d-173">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="2d58d-173">**Calculate interest based on**</span></span> | <span data-ttu-id="2d58d-174">Summa</span><span class="sxs-lookup"><span data-stu-id="2d58d-174">Amount</span></span>          |

<span data-ttu-id="2d58d-175">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d58d-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="2d58d-176">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="2d58d-176">**From value**</span></span> | <span data-ttu-id="2d58d-177">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="2d58d-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="2d58d-178">0</span><span class="sxs-lookup"><span data-stu-id="2d58d-178">0</span></span>              | <span data-ttu-id="2d58d-179">10</span><span class="sxs-lookup"><span data-stu-id="2d58d-179">10</span></span>                 |
| <span data-ttu-id="2d58d-180">61</span><span class="sxs-lookup"><span data-stu-id="2d58d-180">61</span></span>             | <span data-ttu-id="2d58d-181">15</span><span class="sxs-lookup"><span data-stu-id="2d58d-181">15</span></span>                 |
| <span data-ttu-id="2d58d-182">91</span><span class="sxs-lookup"><span data-stu-id="2d58d-182">91</span></span>             | <span data-ttu-id="2d58d-183">20</span><span class="sxs-lookup"><span data-stu-id="2d58d-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="2d58d-184">Näide 3: Intress vahemiku järgi = kuud</span><span class="sxs-lookup"><span data-stu-id="2d58d-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="2d58d-185">Saate seadistada intressikoodi, mis määrab intressi üks kord iga kuu tagant, mil arve makse ületab kande tähtaega.</span><span class="sxs-lookup"><span data-stu-id="2d58d-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="2d58d-186">Soovite arvutuse aluseks võtta protsentuaalse intressiväärtuse, vastavalt astmelistele kuuintervallidele.</span><span class="sxs-lookup"><span data-stu-id="2d58d-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="2d58d-187">Intressi väärtus on 1,5 protsenti kuus kolmel esimesel tähtaja ületanud kuul, 2,0 protsenti kuus järgmised kolm kuud ja 2,5 protsenti kuus kõigil järgnevatel kuudel.</span><span class="sxs-lookup"><span data-stu-id="2d58d-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="2d58d-188">Saate seadistada intressikoodi välja väärtused järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d58d-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="2d58d-189">**Välja nimi**</span><span class="sxs-lookup"><span data-stu-id="2d58d-189">**Field name**</span></span>                  | <span data-ttu-id="2d58d-190">**Välja väärtus**</span><span class="sxs-lookup"><span data-stu-id="2d58d-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="2d58d-191">**Viivise kood**</span><span class="sxs-lookup"><span data-stu-id="2d58d-191">**Interest code**</span></span>               | <span data-ttu-id="2d58d-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="2d58d-192">1M%ByMth</span></span>        |
| <span data-ttu-id="2d58d-193">**Arvuta intress iga**</span><span class="sxs-lookup"><span data-stu-id="2d58d-193">**Calculate interest every**</span></span>    | <span data-ttu-id="2d58d-194">1/kuu</span><span class="sxs-lookup"><span data-stu-id="2d58d-194">1/Month</span></span>         |
| <span data-ttu-id="2d58d-195">**Intress vahemiku järgi**</span><span class="sxs-lookup"><span data-stu-id="2d58d-195">**Interest by range**</span></span>           | <span data-ttu-id="2d58d-196">Kuud</span><span class="sxs-lookup"><span data-stu-id="2d58d-196">Months</span></span>          |
| <span data-ttu-id="2d58d-197">**Intressi arvutusalus:**</span><span class="sxs-lookup"><span data-stu-id="2d58d-197">**Calculate interest based on**</span></span> | <span data-ttu-id="2d58d-198">Protsent</span><span class="sxs-lookup"><span data-stu-id="2d58d-198">Percentage</span></span>      |

<span data-ttu-id="2d58d-199">Saate seadistada vahemiku andmed järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2d58d-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="2d58d-200">**Alates väärtusest**</span><span class="sxs-lookup"><span data-stu-id="2d58d-200">**From value**</span></span> | <span data-ttu-id="2d58d-201">**Intressi väärtus**</span><span class="sxs-lookup"><span data-stu-id="2d58d-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="2d58d-202">0</span><span class="sxs-lookup"><span data-stu-id="2d58d-202">0</span></span>              | <span data-ttu-id="2d58d-203">1.5</span><span class="sxs-lookup"><span data-stu-id="2d58d-203">1.5</span></span>                |
| <span data-ttu-id="2d58d-204">4</span><span class="sxs-lookup"><span data-stu-id="2d58d-204">4</span></span>              | <span data-ttu-id="2d58d-205">2</span><span class="sxs-lookup"><span data-stu-id="2d58d-205">2</span></span>                  |
| <span data-ttu-id="2d58d-206">7</span><span class="sxs-lookup"><span data-stu-id="2d58d-206">7</span></span>              | <span data-ttu-id="2d58d-207">2,5</span><span class="sxs-lookup"><span data-stu-id="2d58d-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="2d58d-208">Uued versioonid</span><span class="sxs-lookup"><span data-stu-id="2d58d-208">New versions</span></span>
<span data-ttu-id="2d58d-209">Intressikoodidel on kehtivuskuupäevad.</span><span class="sxs-lookup"><span data-stu-id="2d58d-209">Interest codes are date effective.</span></span> <span data-ttu-id="2d58d-210">Kui soovite intressimäära muuta, saate luua **uue versiooni**, mis kehtib tulevasest kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="2d58d-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="2d58d-211">Erinevate versioonide vaatamiseks võite kasutada kuupäeva valimiseks menüüvalikut **Alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="2d58d-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="2d58d-212">Saate valida ka **Kuva kõik kirjed** kõigi intressikoodide kuvamiseks lehel.</span><span class="sxs-lookup"><span data-stu-id="2d58d-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




