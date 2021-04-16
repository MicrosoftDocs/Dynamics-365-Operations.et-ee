---
title: Käibemaksuarvutusmeetodid valimine väljal Päritolu
description: See artikkel selgitab käibemaksukoodide lehe välja Päritolu valikuid ja seda, kuidas käibemaks arvutatakse, tuginedes tehtud käibemaksukoodi valikule.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7d322d0a59c2d1fe7be98b97bf25c6db8dec2d6e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815352"
---
# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="3e89e-103">Käibemaksuarvutusmeetodid valimine väljal Päritolu</span><span class="sxs-lookup"><span data-stu-id="3e89e-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3e89e-104">See artikkel selgitab käibemaksukoodide lehe välja Päritolu valikuid ja seda, kuidas käibemaks arvutatakse, tuginedes tehtud käibemaksukoodi valikule.</span><span class="sxs-lookup"><span data-stu-id="3e89e-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="3e89e-105">Iga lehel Käibemaksukoodid loodud käibemaksukoodi puhul peate valima arvutamismeetodi, mida rakendatakse väljal Päritolu olevale käibemaksu baassummale.</span><span class="sxs-lookup"><span data-stu-id="3e89e-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="3e89e-106">Protsent netosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-106">Percentage of net amount</span></span>
<span data-ttu-id="3e89e-107">Välja Päritolu vaikeväärtus on Arvutamismeetod Protsent netosummast.</span><span class="sxs-lookup"><span data-stu-id="3e89e-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="3e89e-108">Käibemaks arvutatakse protsendina ostu- või müügisummast, mis ei sisalda muid käibemakse.</span><span class="sxs-lookup"><span data-stu-id="3e89e-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="3e89e-109">Näide</span><span class="sxs-lookup"><span data-stu-id="3e89e-109">Example</span></span>

<span data-ttu-id="3e89e-110">maksumäär on 25%.</span><span class="sxs-lookup"><span data-stu-id="3e89e-110">The tax rate is 25%.</span></span> <span data-ttu-id="3e89e-111">Arve real kuvatakse kogus (10 kaupa, igaüks hinnaga 1.00), ja kliendile pakutakse 10% rea allahindlust.</span><span class="sxs-lookup"><span data-stu-id="3e89e-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="3e89e-112">Netosumma: (10 x 1,00) – 10% = 9,00, käibemaks: 9,00 x 25% = 2,25, kogusumma: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="3e89e-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="3e89e-113"> Protsent brutosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-113">Percentage of gross amount</span></span>
<span data-ttu-id="3e89e-114">Kui valite meetodi Protsent brutosummast, arvutatakse käibemaks protsendina müügi brutosummast.</span><span class="sxs-lookup"><span data-stu-id="3e89e-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="3e89e-115">Brutosumma on rea netosumma pluss kõik rea maksud ja tasud, välja arvatud maks, mille välja Päritolu väärtus on Protsent brutosummast.</span><span class="sxs-lookup"><span data-stu-id="3e89e-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="3e89e-116">Näide</span><span class="sxs-lookup"><span data-stu-id="3e89e-116">Example</span></span>

<span data-ttu-id="3e89e-117">Maksuamet on kehtestanud kaubale eri lõivud.</span><span class="sxs-lookup"><span data-stu-id="3e89e-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="3e89e-118">Lõivusummad lisati netosummale enne käibemaksu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="3e89e-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="3e89e-119">Võtame arvesse järgmisi käibemaksukoode.</span><span class="sxs-lookup"><span data-stu-id="3e89e-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="3e89e-120">LÕIV 1 = 10%, kasutades arvutusmeetodit Protsent netosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="3e89e-121">LÕIV 2 = 20%, kasutades arvutusmeetodit Protsent netosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="3e89e-122">KÄIBEMAKS = 25%, kasutades arvutusmeetodit Protsent brutosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="3e89e-123">Kui netosumma on 10,00, siis LÕIV 1 = 1,00 (10,00 × 10%) ja LÕIV 2 = 2,00 (10,00 × 20%).</span><span class="sxs-lookup"><span data-stu-id="3e89e-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="3e89e-124">Summad on järgmised. Brutosumma: netosumma + LÕIVU 1 summa + LÕIVU 2 summa (10,00 + 1,00 + 2,00) = 13,00, KÄIBEMAKS: 13,00 × 25% = 3,25, LÕIVUD ja KÄIBEMAKS kokku: 1,00 + 2,00 + 3,25 = 6,25, kogusumma: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="3e89e-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="3e89e-125">**Märkus.**</span><span class="sxs-lookup"><span data-stu-id="3e89e-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e89e-126">Kande puhul saab kasutada ainult üht maksukoodi, mille välja Päritolu väärtus on Protsent brutosummast.</span><span class="sxs-lookup"><span data-stu-id="3e89e-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="3e89e-127">Kui kande kohta määratakse mitu sellist maksukoodi, kuvatakse tõrge, et käibemaksu ei saa arvutada.</span><span class="sxs-lookup"><span data-stu-id="3e89e-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="3e89e-128">Protsent käibemaksust</span><span class="sxs-lookup"><span data-stu-id="3e89e-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="3e89e-129">Kui valite väljal Päritolu väärtuse Protsent käibemaksust, arvutatakse käibemaks protsendina käibemaksust, mis on valitud väljal Käibemaks käibemaksult.</span><span class="sxs-lookup"><span data-stu-id="3e89e-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="3e89e-130">Esimesena arvutatakse käibemaks, mis on valitud väljal Käibemaks käibemaksult.</span><span class="sxs-lookup"><span data-stu-id="3e89e-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="3e89e-131">Teine käibemaks arvutatakse seejärel esimese käibemaksusumma alusel.</span><span class="sxs-lookup"><span data-stu-id="3e89e-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="3e89e-132">Näide</span><span class="sxs-lookup"><span data-stu-id="3e89e-132">Example</span></span>

<span data-ttu-id="3e89e-133">Võtame arvesse järgmisi käibemaksukoode.</span><span class="sxs-lookup"><span data-stu-id="3e89e-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="3e89e-134">LÕIV 1 = 10%, kasutades meetodit Protsent netosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="3e89e-135">LÕIV 2 = 20%, kasutades meetodit Protsent käibemaksust, nii et väljal Käibemaks käibemaksult on valitud väärtus Lõiv 1.</span><span class="sxs-lookup"><span data-stu-id="3e89e-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="3e89e-136">KÄIBEMAKS = 25%, kasutades meetodit Protsent brutosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="3e89e-137">Netosumma: 10,00, LÕIV 1: 10,00 × 10% = 1,00, LÕIV 2: 1,00 × 20% = 0,20, brutosumma: 10,00 + 1,00 + 0,20 = 11,20, KÄIBEMAKS: 11,20 × 25% = 2,80, LÕIVUD ja KÄIBEMAKS kokku: 1,00 + 0,20 + 2,80 = 4,00, kogusumma: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="3e89e-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="3e89e-138">**Märkus.**</span><span class="sxs-lookup"><span data-stu-id="3e89e-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e89e-139">Mitmetasandiline maks pole maksuarvutustes võimalik.</span><span class="sxs-lookup"><span data-stu-id="3e89e-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="3e89e-140">Maksu ei saa arvutada maksu põhjal, mis on teise maksu põhjal juba arvutatud.</span><span class="sxs-lookup"><span data-stu-id="3e89e-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="3e89e-141">Kandes saab arvutada maksukoodide põhjal mitu ühetasemelist maksu.</span><span class="sxs-lookup"><span data-stu-id="3e89e-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="3e89e-142"> Summa ühiku kohta</span><span class="sxs-lookup"><span data-stu-id="3e89e-142">Amount per unit</span></span>
<span data-ttu-id="3e89e-143">Kui valite väljal Päritolu suvandi Summa ühiku kohta, arvutatakse käibemaks ühiku kohta fikseeritud summana korrutatuna dokumendireale sisestatud kogusega.</span><span class="sxs-lookup"><span data-stu-id="3e89e-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="3e89e-144">Ühik tuleb valida väljal Ühik.</span><span class="sxs-lookup"><span data-stu-id="3e89e-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="3e89e-145">Summa ühiku kohta on määratud lehel Käibemaksukoodi väärtused.</span><span class="sxs-lookup"><span data-stu-id="3e89e-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="3e89e-146">Näide</span><span class="sxs-lookup"><span data-stu-id="3e89e-146">Example</span></span>

<span data-ttu-id="3e89e-147">Käibemaksukoodi seadistatakse järgmiselt: 1,20 USD ühiku kohta = kast. Müügiarve real on kaupa müüdud 25 kasti. Käibemaks arvutatakse järgmiselt: 25 × 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="3e89e-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="3e89e-148">**Märkus.**</span><span class="sxs-lookup"><span data-stu-id="3e89e-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e89e-149">Kui kanne sisestatakse muus kui käibemaksukoodi jaoks määratud ühikus, teisendatakse see automaatselt ühikuteisenduste alusel, mis on seadistatud lehel Ühikuteisendused.</span><span class="sxs-lookup"><span data-stu-id="3e89e-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="3e89e-150"> Summa ühiku kohta, lisavalik</span><span class="sxs-lookup"><span data-stu-id="3e89e-150">Amount per unit, additional option</span></span>

<span data-ttu-id="3e89e-151">Vahekaardil Kalkulatsioon saate valida, kas ühikusumma kohta arvutatav maks arvutatakse enne muid maksukoode ja lisatakse netosummale enne muude maksukoodide arvutamist, mille puhul välja Päritolu väärtus on Protsent netosummast.</span><span class="sxs-lookup"><span data-stu-id="3e89e-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="3e89e-152">Näited</span><span class="sxs-lookup"><span data-stu-id="3e89e-152">Examples</span></span>

<span data-ttu-id="3e89e-153">Oletame, et arvutame kannetel kaks maksukoodi.</span><span class="sxs-lookup"><span data-stu-id="3e89e-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="3e89e-154">LÕIV: Päritolu = Summa ühiku kohta ja käibemaks, väärtuseks on määratud 5,00 ühiku (tk) kohta.</span><span class="sxs-lookup"><span data-stu-id="3e89e-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="3e89e-155">KÄIBEMAKS: Päritolu = nagu allolevates näidetes on näidatud, on väärtuseks seatud 25%</span><span class="sxs-lookup"><span data-stu-id="3e89e-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="3e89e-156">Müüme kaupa 1 tüki ühikuhinnaga 10,00.</span><span class="sxs-lookup"><span data-stu-id="3e89e-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="3e89e-157">Näide 1</span><span class="sxs-lookup"><span data-stu-id="3e89e-157">Example 1</span></span>

<span data-ttu-id="3e89e-158">KÄIBEMAKS: Päritolu = meetod Protsent brutosummast. Suvandil Arvuta enne käibemaksu pole mõju, kuna KÄIBEMAKS arvutatakse protsendina brutosummast.</span><span class="sxs-lookup"><span data-stu-id="3e89e-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="3e89e-159">LÕIV: 1 × 5,00 = 5,00, brutosumma: 10,00 + 5,00 = 15,00, KÄIBEMAKS: 15,00 × 25% = 3,75, käibemaks kokku: 5,00 + 3,75 = 8,75, kogusumma: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="3e89e-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="3e89e-160">Näide 2</span><span class="sxs-lookup"><span data-stu-id="3e89e-160">Example 2</span></span>

<span data-ttu-id="3e89e-161">KÄIBEMAKS: Päritolu = Protsent netosummast . Suvand Arvuta enne käibemaksu pole LÕIVU arvutamiseks valitud.</span><span class="sxs-lookup"><span data-stu-id="3e89e-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="3e89e-162">Netosumma: 10,00, LÕIV: 1 × 5,00 = 5,00, KÄIBEMAKS: 10,00 × 25% = 2,50, käibemaks kokku: 5,00 + 2,50 = 7,50, kogusumma: 10,00 + 7,50 = 17,50.</span><span class="sxs-lookup"><span data-stu-id="3e89e-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="3e89e-163">Näide 3</span><span class="sxs-lookup"><span data-stu-id="3e89e-163">Example 3</span></span>

<span data-ttu-id="3e89e-164">KÄIBEMAKS: Päritolu = Protsent netosummast . Suvand Arvuta enne käibemaksu on LÕIVU arvutamiseks valitud.</span><span class="sxs-lookup"><span data-stu-id="3e89e-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="3e89e-165">Netosumma: 10,00, LÕIV: 1 × 5,00 = 5,00, KÄIBEMAKS: (10,00 + 5,00) × 25% = 3,75, käibemaks kokku: 5,00 + 3,75 = 8,75, kogusumma: 10,00 + 8,75 = 18,75.</span><span class="sxs-lookup"><span data-stu-id="3e89e-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="3e89e-166">Näide 4</span><span class="sxs-lookup"><span data-stu-id="3e89e-166">Example 4</span></span>

<span data-ttu-id="3e89e-167">Näite 3 ja näite 1 tulemus on sama, sest kasutatakse ainult ühte lõivu.</span><span class="sxs-lookup"><span data-stu-id="3e89e-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="3e89e-168">Oletame, et teil on kaks LÕIVU, millest vaid üks on kaasatud käibemaksu arvutamisel netosummasse: LÕIV 1: 5,00, kasutades meetodit Summa ühiku kohta ja suvand Arvuta enne käibemaksu on valitud. LÕIV 2: 2,50, kasutades meetodit Summa ühiku kohta ja suvand Arvuta enne käibemaksu pole valitud. Käibemaks: 25%, kasutades meetodit Protsent netosummast. Netosumma: 10,00, LÕIV 1: 1 × 5,00 = 5,00, LÕIV 2: 1 × 2,50 = 2,50, netosumma käibemaksu jaoks: 10,00 + 5,00 = 15,00, KÄIBEMAKS: 15,00 × 25% = 3,75, käibemaks kokku, k.a lõivud: 5,00 + 2,50 + 3,75 = 11,25, kogusumma: 10,00 + 11,25 = 21,25, 25% KÄIBEMAKS arvutatakse netosumma (10,00) + LÕIVU 1 (5,00) = 15,00 summana.</span><span class="sxs-lookup"><span data-stu-id="3e89e-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="3e89e-169">LÕIV 2 lisatakse maksusummale pärast käibemaksu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="3e89e-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="3e89e-170"> Arvutatud protsent netosummast</span><span class="sxs-lookup"><span data-stu-id="3e89e-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="3e89e-171">Arvutatud protsent netosummast käsitleb maksuarvutust teisiti, olenevalt dokumendi või töölehe parameetri Summad sisaldavad käibemaksu sättest.</span><span class="sxs-lookup"><span data-stu-id="3e89e-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="3e89e-172">Näide 1</span><span class="sxs-lookup"><span data-stu-id="3e89e-172">Example 1</span></span>

<span data-ttu-id="3e89e-173">Dokumendi/töölehe suvandi Summad sisaldavad käibemaksu sätteks on valitud Jah. Kanderea summa: 10,00, maksumäär: 25%, käibemaks: kanderea summa × maksumäär (10,00 × 25%) = 2,50, maksubaasi summa (päritolu summa): kanderea summa – käibemaks (10,00 - 2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="3e89e-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="3e89e-174">Näide 2</span><span class="sxs-lookup"><span data-stu-id="3e89e-174">Example 2</span></span>

<span data-ttu-id="3e89e-175">Dokumendi/töölehe suvandi Summad sisaldavad käibemaksu sätteks on valitud Ei. Kanderea summa: 10,00, maksumäär: 25%, käibemaks: (kanderea summa × maksumäär) / (100 – maksumäär) (10,00 × 25%) / (100% – 25%) = 3,33, maksubaasi summa (päritolu summa): kanderea summa = 10,00</span><span class="sxs-lookup"><span data-stu-id="3e89e-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="3e89e-176">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3e89e-176">Additional resources</span></span>
--------

[<span data-ttu-id="3e89e-177">Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal</span><span class="sxs-lookup"><span data-stu-id="3e89e-177">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)

[<span data-ttu-id="3e89e-178">Kogusumma ja intervalli arvutamise valikud käibemaksukoodide puhul</span><span class="sxs-lookup"><span data-stu-id="3e89e-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]