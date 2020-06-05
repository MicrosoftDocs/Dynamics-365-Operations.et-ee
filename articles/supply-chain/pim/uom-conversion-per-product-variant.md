---
title: Mõõtühiku teisendus tootevariandi kohta
description: See teema kirjeldab, kuidas seadistada tootevariantide mõõtühikute teisendusi. See sisaldab seadistuse näidet.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 92611ec276da6f7211d722cfcd66739b612296dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3382793"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="e0597-104">Mõõtühiku teisendus tootevariandi kohta</span><span class="sxs-lookup"><span data-stu-id="e0597-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0597-105">See teema kirjeldab, kuidas seadistada erinevaid tootevariantide mõõtühikute teisendusi.</span><span class="sxs-lookup"><span data-stu-id="e0597-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="e0597-106">Selle asemel, et luua mitut haldamist vajavat individuaalset toodet, saate kasutada tootevariante ühe toote variatsioonide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e0597-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="e0597-107">Näiteks võib tootevariant olla antud suuruse ja värviga t-särk.</span><span class="sxs-lookup"><span data-stu-id="e0597-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="e0597-108">Varasemalt sai ühiku teisendusi seadistada ainult tooteetalonil.</span><span class="sxs-lookup"><span data-stu-id="e0597-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="e0597-109">Seetõttu olid kõigil tootevariantisel samad ühikuteisenduse reeglid.</span><span class="sxs-lookup"><span data-stu-id="e0597-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="e0597-110">Kui aga funktsioon *Tootevariantide mõõtühiku teisendused* on sisse lülitatud, kui müüte t-särke kastides ja ühte kasti pakendatavate t-särkide kogus sõltub t-särgi suurusest, saate nüüd seadistada ühikuteisendusi erinevate särgisuuruste ja pakendamiseks kasutatavate kastide vahel.</span><span class="sxs-lookup"><span data-stu-id="e0597-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="e0597-111">Funktsiooni sisselülitamine teie süsteemis</span><span class="sxs-lookup"><span data-stu-id="e0597-111">Turn on the feature in your system</span></span>

<span data-ttu-id="e0597-112">Kui seda funktsiooni veel ei kuvata teie süsteemis, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage sisse funktsioon *Tootevariantide mõõtühiku teisendused*.</span><span class="sxs-lookup"><span data-stu-id="e0597-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="e0597-113">Seadistage toode ühiku teisaldamiseks varjandi kohta</span><span class="sxs-lookup"><span data-stu-id="e0597-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="e0597-114">Tootevariante saab luua ainult toodetele, mis on tooteetalonid.</span><span class="sxs-lookup"><span data-stu-id="e0597-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="e0597-115">Lisateavet vt jaotisest [Tooteetaloni loomine](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="e0597-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="e0597-116">Funktsioon *Tootevariantide mõõtühiku teisendused* ei ole saadaval toodete puhul, millel on seadistatud tegeliku kaalu protsessid.</span><span class="sxs-lookup"><span data-stu-id="e0597-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="e0597-117">Tooteetaloni konfigureerimiseks, et toetada ühikuteisendust ühe variandi kohta, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e0597-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="e0597-118">Avage **Tooteteabe haldus \> Tooted \> Tooteetalonid**.</span><span class="sxs-lookup"><span data-stu-id="e0597-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="e0597-119">Looge või avage tooteetalon, et avada selle leht **Toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="e0597-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="e0597-120">Määrake suvandi **Luba mõõtühiku teisendused** Väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="e0597-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="e0597-121">Tehke Toimingupaani vahekaardil **Toode** grupis **Häälesta** valik **Ühiku teisendused**.</span><span class="sxs-lookup"><span data-stu-id="e0597-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="e0597-122">Avaneb leht **Ühiku teisendused**.</span><span class="sxs-lookup"><span data-stu-id="e0597-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="e0597-123">Valige üks järgmistest vahekaartidest.</span><span class="sxs-lookup"><span data-stu-id="e0597-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="e0597-124">**Klassisisesed teisendused** – valige see vahekaart, et teisendada samasse ühiku klassi kuuluvaid ühikuid.</span><span class="sxs-lookup"><span data-stu-id="e0597-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="e0597-125">**Klassivahelised teisendused** – valige see vahekaart, et teisendada erinevatesse ühiku klassidesse kuuluvaid ühikuid.</span><span class="sxs-lookup"><span data-stu-id="e0597-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="e0597-126">Uue ühiku teisenduse lisamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e0597-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="e0597-127">Määrake väljale **Loo teisendus:** üks järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="e0597-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="e0597-128">**Toode** – selle väärtuse valimisel saate seadistada ühiku teisenduse tooteetaloni jaoks.</span><span class="sxs-lookup"><span data-stu-id="e0597-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="e0597-129">Seda ühiku teisendust kasutatakse varuvariandina kõigi tootevariantide puhul, millele pole ühiku teisendust määratletud.</span><span class="sxs-lookup"><span data-stu-id="e0597-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="e0597-130">**Tootevariant** – selle väärtuse valimisel saate seadistada ühiku teisenduse kindla tootevariandi jaoks.</span><span class="sxs-lookup"><span data-stu-id="e0597-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="e0597-131">Variandi valimiseks kasutage välja **Tootevariant**.</span><span class="sxs-lookup"><span data-stu-id="e0597-131">Use the **Product variant** field to select the variant.</span></span>

    <span data-ttu-id="e0597-132">![Uue ühiku teisenduse lisamine](media/uom-new-conversion.png "Uue ühiku teisenduse lisamine")</span><span class="sxs-lookup"><span data-stu-id="e0597-132">![Adding a new unit conversion](media/uom-new-conversion.png "Adding a new unit conversion")</span></span>

1. <span data-ttu-id="e0597-133">Ühiku teisenduse seadistamiseks kasutage teisi saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="e0597-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="e0597-134">Uue ühiku teisenduse salvestamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e0597-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="e0597-135">Toote või tootevariandi lehe **Ühiku teisendused** saate avada mis tahes järgmistelt lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="e0597-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="e0597-136">Toote üksikasjad</span><span class="sxs-lookup"><span data-stu-id="e0597-136">Product details</span></span>
> - <span data-ttu-id="e0597-137">Väljastatud toodete üksikasjad</span><span class="sxs-lookup"><span data-stu-id="e0597-137">Released products details</span></span>
> - <span data-ttu-id="e0597-138">Väljastatud tootevariandid</span><span class="sxs-lookup"><span data-stu-id="e0597-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e0597-139">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="e0597-139">Example scenario</span></span>

<span data-ttu-id="e0597-140">Selles stsenaariumis müüb ettevõte t-särke suuruses S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="e0597-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="e0597-141">T-särk määratletakse tootena ja erinevad suurused määratletakse selle toote variantidena.</span><span class="sxs-lookup"><span data-stu-id="e0597-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="e0597-142">Särke pakendatakse kastidesse.</span><span class="sxs-lookup"><span data-stu-id="e0597-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="e0597-143">Suuruste S, M ja L, saab ühte kasti pakendada viis särki.</span><span class="sxs-lookup"><span data-stu-id="e0597-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="e0597-144">Kuid suuruse XL puhul on ühes kastis ruumi ainult nelja särgi jaoks.</span><span class="sxs-lookup"><span data-stu-id="e0597-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="e0597-145">Ettevõte soovib jälgida t-särkide erinevaid variante ühiku *Tükid* järgi, aga müüb t-särke ühikus *Kastid*.</span><span class="sxs-lookup"><span data-stu-id="e0597-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="e0597-146">Suuruste S, M ja L puhul on lao- ja müügiüksuse vaheliseks teisenduseks 1 kast = 5 tükki.</span><span class="sxs-lookup"><span data-stu-id="e0597-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="e0597-147">Suuruse XL puhul on teisenduseks 1 kast = 4 tükki.</span><span class="sxs-lookup"><span data-stu-id="e0597-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="e0597-148">Avage toote **T-särk** lehel **Väljastatut toote üksikasjad** leht **Ühiku teisendused**.</span><span class="sxs-lookup"><span data-stu-id="e0597-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="e0597-149">Seadistage lehel **Ühiku teisendused** väljastatud tootevariandi **XL** jaoks järgmine ühiku teisendus.</span><span class="sxs-lookup"><span data-stu-id="e0597-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="e0597-150">Field</span><span class="sxs-lookup"><span data-stu-id="e0597-150">Field</span></span>                 | <span data-ttu-id="e0597-151">Sätted</span><span class="sxs-lookup"><span data-stu-id="e0597-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="e0597-152">Loo teisendus:</span><span class="sxs-lookup"><span data-stu-id="e0597-152">Create conversion for</span></span> | <span data-ttu-id="e0597-153">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="e0597-153">Product variant</span></span>         |
    | <span data-ttu-id="e0597-154">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="e0597-154">Product variant</span></span>       | <span data-ttu-id="e0597-155">T-särk : : XL : :</span><span class="sxs-lookup"><span data-stu-id="e0597-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="e0597-156">Lähteühik</span><span class="sxs-lookup"><span data-stu-id="e0597-156">From unit</span></span>             | <span data-ttu-id="e0597-157">Kastid</span><span class="sxs-lookup"><span data-stu-id="e0597-157">Boxes</span></span>                   |
    | <span data-ttu-id="e0597-158">Tegur</span><span class="sxs-lookup"><span data-stu-id="e0597-158">Factor</span></span>                | <span data-ttu-id="e0597-159">4</span><span class="sxs-lookup"><span data-stu-id="e0597-159">4</span></span>                       |
    | <span data-ttu-id="e0597-160">Ühikuks</span><span class="sxs-lookup"><span data-stu-id="e0597-160">To Unit</span></span>               | <span data-ttu-id="e0597-161">Osad</span><span class="sxs-lookup"><span data-stu-id="e0597-161">Pieces</span></span>                  |

1. <span data-ttu-id="e0597-162">Kuna väljastatud toodete variantidel **S**, **M** ja **L** on ühikute *Kast* ja *Tükid* vahel sama ühiku teisendus, saate nende tootevariantide ühiku teisendused määratleda tooteetalonis.</span><span class="sxs-lookup"><span data-stu-id="e0597-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="e0597-163">Field</span><span class="sxs-lookup"><span data-stu-id="e0597-163">Field</span></span>                 | <span data-ttu-id="e0597-164">Sätted</span><span class="sxs-lookup"><span data-stu-id="e0597-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="e0597-165">Loo teisendus:</span><span class="sxs-lookup"><span data-stu-id="e0597-165">Create conversion for</span></span> | <span data-ttu-id="e0597-166">Toode</span><span class="sxs-lookup"><span data-stu-id="e0597-166">Product</span></span> |
    | <span data-ttu-id="e0597-167">Toode</span><span class="sxs-lookup"><span data-stu-id="e0597-167">Product</span></span>               | <span data-ttu-id="e0597-168">T-särk</span><span class="sxs-lookup"><span data-stu-id="e0597-168">T-Shirt</span></span> |
    | <span data-ttu-id="e0597-169">Lähteühik</span><span class="sxs-lookup"><span data-stu-id="e0597-169">From unit</span></span>             | <span data-ttu-id="e0597-170">Kastid</span><span class="sxs-lookup"><span data-stu-id="e0597-170">Boxes</span></span>   |
    | <span data-ttu-id="e0597-171">Tegur</span><span class="sxs-lookup"><span data-stu-id="e0597-171">Factor</span></span>                | <span data-ttu-id="e0597-172">5</span><span class="sxs-lookup"><span data-stu-id="e0597-172">5</span></span>       |
    | <span data-ttu-id="e0597-173">Ühikuks</span><span class="sxs-lookup"><span data-stu-id="e0597-173">To Unit</span></span>               | <span data-ttu-id="e0597-174">Osad</span><span class="sxs-lookup"><span data-stu-id="e0597-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="e0597-175">Exceli kasutamine ühikuteisenduste värskendamiseks</span><span class="sxs-lookup"><span data-stu-id="e0597-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="e0597-176">Kui tootel on palju erinevate ühiku teisendustega tootevariante, oleks hea eksportida ühiku teisendused Microsoft Exceli töövihikusse, värskendada need ja seejärel avaldada Dynamics 365 Supply Chain Managementis uuesti.</span><span class="sxs-lookup"><span data-stu-id="e0597-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e0597-177">Ühiku teisenduste eksportimiseks Excelisse Toimingupaani lehe **Ühiku teisendused** kaudu, valige **Ava Microsoft Office'is**.</span><span class="sxs-lookup"><span data-stu-id="e0597-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e0597-178">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e0597-178">Additional resources</span></span>

[<span data-ttu-id="e0597-179">Mõõtühiku haldamine</span><span class="sxs-lookup"><span data-stu-id="e0597-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
