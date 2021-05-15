---
title: Maksu ei arvutatud või maksusumma on null
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui maksusumma on 0 (null) või maksu ei arvutata.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947626"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="1e3de-103">Maksu ei arvutatud või maksusumma on null</span><span class="sxs-lookup"><span data-stu-id="1e3de-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e3de-104">Kandel võib olla rea summa, mis ei ole 0 (null), kuid maksu pole arvutatud või on arvutatud maksusumma 0.</span><span class="sxs-lookup"><span data-stu-id="1e3de-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="1e3de-105">Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.</span><span class="sxs-lookup"><span data-stu-id="1e3de-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="1e3de-106">Kontrollige, kas kanne on maksukoodid õigesti valinud</span><span class="sxs-lookup"><span data-stu-id="1e3de-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="1e3de-107">Kui kanne ei vali õigeid maksukoode või kui see ei vali ühtegi maksukoodi, siis makse ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="1e3de-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="1e3de-108">Järgige neid samme, et kontrollida, kas kanne on maksukoodid õigesti valinud.</span><span class="sxs-lookup"><span data-stu-id="1e3de-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="1e3de-109">Kandereal **Rea detailid** kiirkaardil **Seaded** vahekaardi jaotises **Käibemaks** kontrollige, kas on valitud õiged maksugrupid väljadel **Kauba käibemaksugrupp** ja **Käibemaksugrupp**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="1e3de-110">Kui õigeid maksugruppe ei ole valitud, valige need.</span><span class="sxs-lookup"><span data-stu-id="1e3de-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="1e3de-111">[![Kauba käibemaksugrupp ja käibemaksugrupi väljad](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="1e3de-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="1e3de-112">Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksu grupid**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="1e3de-113">Valige sobiv käibemaksugrupp ja tehke seejärel kiirkaardil **Seaded** maksukoodi märkus väljal **Käibemaksukood**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="1e3de-114">[![Käibemaksugruppide leht](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="1e3de-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="1e3de-115">Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Kauba käibemaksugrupid**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="1e3de-116">Valige sobiv kauba käibemaksugrupp ja seejärel kontrollige kiirkaardil **Seaded**, et välja **Käibemaksukood** maksukood vastab käibemaksugrupi maksukoodile.</span><span class="sxs-lookup"><span data-stu-id="1e3de-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="1e3de-117">[![Kauba käibemaksugruppide leht](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="1e3de-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="1e3de-118">Kui maksukoodid ei kattu, värskendage käibemaksukoodi ühele grupist.</span><span class="sxs-lookup"><span data-stu-id="1e3de-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="1e3de-119">Kontrollige, kas valitud maksukoodid ei ole maksuvabad ja kas neil on õige maksumäära väärtus</span><span class="sxs-lookup"><span data-stu-id="1e3de-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="1e3de-120">Kui maksukoodid on maksuvabad või kui maksumäär on 0 (null), on maksu arvutamise tulemus 0.</span><span class="sxs-lookup"><span data-stu-id="1e3de-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="1e3de-121">Järgige neid samme, et määrata, kas valitud maksukoodid on maksuvabad, ja kontrollimaks, et neile rakendatakse õiget maksumäära.</span><span class="sxs-lookup"><span data-stu-id="1e3de-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="1e3de-122">Avage **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksu grupid**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="1e3de-123">Valige sobiv käibemaksugrupp ja seejärel kontrollige kiirkaardil **Seaded**, et **Maksuvabastus** märkeruut on tühi.</span><span class="sxs-lookup"><span data-stu-id="1e3de-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="1e3de-124">Kui ruut on märgitud, tühjendage see.</span><span class="sxs-lookup"><span data-stu-id="1e3de-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="1e3de-125">[![Maksuvaba märkeruut käibemaksugruppide lehel](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="1e3de-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="1e3de-126">Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="1e3de-127">Valige sobiv käibemaksukood ja seejärel kontrollige, et maksumäära väärtus väljal **Väärtus** ei oleks 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1e3de-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="1e3de-128">Kui väärtus on 0, uuendage välja nii, et selle väärtuseks oleks seadistatud õige maksumäär.</span><span class="sxs-lookup"><span data-stu-id="1e3de-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="1e3de-129">[![Välja väärtus Käibemaksukoodi väärtuse lehel](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="1e3de-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="1e3de-130">Määrake, kas null on õige maksusumma</span><span class="sxs-lookup"><span data-stu-id="1e3de-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="1e3de-131">Mõnes stsenaariumis on maksusumma 0 (null) õige.</span><span class="sxs-lookup"><span data-stu-id="1e3de-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="1e3de-132">Järgige neid samme, et määratleda, kas 0 on teie kandele õige maksusumma.</span><span class="sxs-lookup"><span data-stu-id="1e3de-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="1e3de-133">Avage **Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="1e3de-134">Kontrollige vahekaardi **Käibemaks** väljal **Arvutusmeetod**, et **Kogusumma** on valitud.</span><span class="sxs-lookup"><span data-stu-id="1e3de-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="1e3de-135">[![Kalkulatsiooni meetodi väli pearaamatu parameetrite lehel](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="1e3de-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="1e3de-136">Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="1e3de-137">Valige sobiv käibemaksukood, valige **Kalkulatsioon** \> **Marginaali alus** ja kontrollige, et marginaali aluseks on seatud **Arve saldo netosumma** või **Arve kogusumma koos teiste käibemaksusummadega**.</span><span class="sxs-lookup"><span data-stu-id="1e3de-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="1e3de-138">Lisateavet vt [Arve kogusumma koos teiste käibemaksusummadega](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="1e3de-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="1e3de-139">Kui õiged väärtused on seadistatud 2. ja 4. sammus, määratlege, kas kande kogusumma on 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1e3de-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="1e3de-140">Kui kogusumma on 0, on eeldatav maksusumma 0.</span><span class="sxs-lookup"><span data-stu-id="1e3de-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="1e3de-141">Kuna maksu arvutamine põhineb arve saldo kogusummal ja see summa ei ole rida realt, eraldatakse maksusumma 0 igale reale pärast maksu arvutamist.</span><span class="sxs-lookup"><span data-stu-id="1e3de-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="1e3de-142">Kohanduse olemasolu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="1e3de-142">Determine whether customization exists</span></span>

<span data-ttu-id="1e3de-143">Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="1e3de-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="1e3de-144">Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.</span><span class="sxs-lookup"><span data-stu-id="1e3de-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
