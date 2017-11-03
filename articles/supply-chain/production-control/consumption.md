---
title: Materjalikulu arvutamine
description: See artikkel annab teavet mitmesuguste valikute kohta, mis on seotud materjalikulu arvutamisega.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f674a1f0051ee4b228b8a92f717ef5348a452bed
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="calculate-material-consumption"></a><span data-ttu-id="2dfb4-103">Materjalikulu arvutamine</span><span class="sxs-lookup"><span data-stu-id="2dfb4-103">Calculate material consumption</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="2dfb4-104">See artikkel annab teavet mitmesuguste valikute kohta, mis on seotud materjalikulu arvutamisega.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="2dfb4-105">Lehe **Kooslus** kiirkaardil **Rea üksikasjad** vahekaartidel **Seadistus** ja **Etapiviisiline tarbimine** on saadaval järgmised materjalitarbimise arvutamisega seotud suvandid.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="2dfb4-106">Muutuv ja konstantne tarbimine</span><span class="sxs-lookup"><span data-stu-id="2dfb4-106">Variable and constant consumption</span></span>
<span data-ttu-id="2dfb4-107">Väljal **Tarbimine on** saate valida, kas tarbimine tuleks arvutada konstantse koguse või muutuva kogusena.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="2dfb4-108">Valige suvand **Konstantne**, kui tootmiseks on nõutav fikseeritud kogus või maht, olenemata toodetavast kogusest.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="2dfb4-109">Valige suvand **Muutuv**, mis on vaikesäte, kui materjali nõutav kogus valmiskaupades on toodetavate valmiskaupade arvuga proportsionaalne.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="2dfb4-110">Tarbimise arvutamine valemi põhjal</span><span class="sxs-lookup"><span data-stu-id="2dfb4-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="2dfb4-111">Väljal **Valem** saate seadistada erinevaid valemeid materjalitarbimise arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="2dfb4-112">Kui kasutate vaikeväärtust, **Standardne**, ei arvutata tarbimist valemi põhjal.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="2dfb4-113">Väljadega **Kõrgus**, **Laius**, **Sügavus**, **Tihedus** ja **Konstant** toimivad järgmised valemid.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="2dfb4-114">Kõrgus \* Konstant</span><span class="sxs-lookup"><span data-stu-id="2dfb4-114">Height \* Constant</span></span>
-   <span data-ttu-id="2dfb4-115">Kõrgus \* Laius \* Konstant</span><span class="sxs-lookup"><span data-stu-id="2dfb4-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="2dfb4-116">Kõrgus \* Laius \* Sügavus \* Konstant</span><span class="sxs-lookup"><span data-stu-id="2dfb4-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="2dfb4-117">(Kõrgus \* Laius \* Sügavus / Tihedus) \* Konstant</span><span class="sxs-lookup"><span data-stu-id="2dfb4-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="2dfb4-118">Ümardamine ja kordsed</span><span class="sxs-lookup"><span data-stu-id="2dfb4-118">Rounding up and multiples</span></span>
<span data-ttu-id="2dfb4-119">Väljad **Ümardamine** ja **Kordsed** võimaldavad ümardada materjalitarbimise väärtust.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="2dfb4-120">Näiteks saate ümardada väärtuse materjali käsitlemisühiku järgi, milles toormaterjali tootmisse komplekteeritakse.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="2dfb4-121">Väljal **Ümardamine** on saadaval järgmised valikud: **Kogus**, **Mõõt** ja **Tarbimine**.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="2dfb4-122">Kogus</span><span class="sxs-lookup"><span data-stu-id="2dfb4-122">Quantity</span></span>

<span data-ttu-id="2dfb4-123">Kui valite ümardamismehhanismiks suvandi **Kogus**, peab kogus olema määratud koguse kordne.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="2dfb4-124">Näiteks, kui nõutavad on täisarvud, valige väljal **Kordsed** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="2dfb4-125">Arvud ümardatakse seejärel koguseni, mis jaguvad on 1.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="2dfb4-126">Mõõtmine</span><span class="sxs-lookup"><span data-stu-id="2dfb4-126">Measurement</span></span>

<span data-ttu-id="2dfb4-127">Tavaliselt valite ümardamismehhanismiks suvandi **Mõõt**, kui toormaterjalil on kindlad mõõtmed.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="2dfb4-128">Näiteks on valmistoote jaoks nõutav 2-meetrine metalltoru ja metalltorusid hoiundatakse 4,5-meetri pikkustena.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="2dfb4-129">Sellisel juhul saab ümardusmehhanismiga **Mõõt** arvutada, kui palju metalltorusid on vaja kindla arvu valmistoodete tootmiseks.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="2dfb4-130">Selles näites on välja **Valem** väärtuseks seatud **Kõrgus \* Konstant**.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="2dfb4-131">Välja **Kõrgus** väärtuseks on seatud **2**, mis näitab valmiskauba jaoks vajaliku toru pikkust.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="2dfb4-132">Välja **Kordne** väärtuseks on seatud **4,5**, mis näitab, et toru komplekteeritakse pikkustes 4,5 meetrit.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="2dfb4-133">Arvutuskäik on järgmine.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="2dfb4-134">10 ühiku valmiskauba jaoks vajalike kordühikute arv: 10 ÷ 2 = 5 tk</span><span class="sxs-lookup"><span data-stu-id="2dfb4-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="2dfb4-135">Kogutarbimine: 4.5 × 5 = 22,5 meetrit metalltoru</span><span class="sxs-lookup"><span data-stu-id="2dfb4-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="2dfb4-136">Eeldatakse, et 0,5-meetrine toruosa kantakse iga viie tarrbitud toru kohta maha.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="2dfb4-137">Tarbimine</span><span class="sxs-lookup"><span data-stu-id="2dfb4-137">Consumption</span></span>

<span data-ttu-id="2dfb4-138">Tavaliselt valite ümardamismehhanismi suvandiks**Tarbimine**, kui toormaterjali komplekteeritakse toote kindla materjali käsitlemisühiku täielikes kogustes.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="2dfb4-139">Näiteks kasutatakse ühe valmistoote tootmiseks 2 liitrit värvi ja värvi komplekteeritakse 25-liitristes tünnides.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="2dfb4-140">Selles näites saab ümardamismehhanismiga **Tarbimine** ümardada tarbimise täisarvu, 25-liitristes tünnideni.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="2dfb4-141">Värvi, mis on vajalik, kui 180 lõpetatud kauba ühikut, tuleb esitada arvutusmeetodid järgnevalt:</span><span class="sxs-lookup"><span data-stu-id="2dfb4-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="2dfb4-142">Vajalik värv, v.a praak: 180 × 2 = 360 liitrit</span><span class="sxs-lookup"><span data-stu-id="2dfb4-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="2dfb4-143">Tünnide arv: 360 ÷ 25 = 14,4, ümardatuna 15</span><span class="sxs-lookup"><span data-stu-id="2dfb4-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="2dfb4-144">Vajalik värv, k.a praak: 15 × 25 = 375 liitrit</span><span class="sxs-lookup"><span data-stu-id="2dfb4-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="2dfb4-145">Sammu tarbimine</span><span class="sxs-lookup"><span data-stu-id="2dfb4-145">Step consumption</span></span>
<span data-ttu-id="2dfb4-146">Etapiviisilist tarbimist kasutatakse koguseintervalliga konstantse tarbimise arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="2dfb4-147">Kui teete vahekaardi **Seadistus** väljal **Valem** valiku **Etapiviisiline tarbimine**, saate lisada teavet etappide kohta vahekaardile **Etapiviisiline tarbimine**. Fikseeritud tarbitud koguse saab seadistada toodetud koguse intervalliga.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="2dfb4-148">Näiteks seadistatakse etapiviisiline tarbimine nii, nagu kirjeldatud allolevas tabelis.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="2dfb4-149">Seeriatest</span><span class="sxs-lookup"><span data-stu-id="2dfb4-149">From series</span></span> | <span data-ttu-id="2dfb4-150">Kogus</span><span class="sxs-lookup"><span data-stu-id="2dfb4-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="2dfb4-151">0,00</span><span class="sxs-lookup"><span data-stu-id="2dfb4-151">0.00</span></span>        | <span data-ttu-id="2dfb4-152">10,0000</span><span class="sxs-lookup"><span data-stu-id="2dfb4-152">10.0000</span></span>  |
| <span data-ttu-id="2dfb4-153">100,00</span><span class="sxs-lookup"><span data-stu-id="2dfb4-153">100.00</span></span>      | <span data-ttu-id="2dfb4-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="2dfb4-154">20.0000</span></span>  |
| <span data-ttu-id="2dfb4-155">200,00</span><span class="sxs-lookup"><span data-stu-id="2dfb4-155">200.00</span></span>      | <span data-ttu-id="2dfb4-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="2dfb4-156">40.0000</span></span>  |

<span data-ttu-id="2dfb4-157">Koosluse kogus on 1 ja tootmiskogus 110.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="2dfb4-158">Tarbimise valem on Lähteseeria (kogus) = tarbimine.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="2dfb4-159">Kuna tootmiskogus on 110, jääb see vahemikku „Alates 100 seeriast”.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="2dfb4-160">Seega on kogus 20.</span><span class="sxs-lookup"><span data-stu-id="2dfb4-160">Therefore, the quantity is 20.</span></span>




