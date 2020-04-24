---
title: Mõõteühiku teisendus tootevariandi kohta
description: See teema kirjeldab, kuidas saab seadistada tootevariantide mõõtühikute teisendusi.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
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
ms.openlocfilehash: e50be7fa6fa686a90b2dd5c5200c881e4629f019
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204489"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="efaa5-103">Mõõteühiku teisendus tootevariandi kohta</span><span class="sxs-lookup"><span data-stu-id="efaa5-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="efaa5-104">See teema kirjeldab, kuidas saab seadistada tootevariantide mõõtühikute teisendusi.</span><span class="sxs-lookup"><span data-stu-id="efaa5-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="efaa5-105">See sisaldab seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="efaa5-105">It includes an example of the setup.</span></span>

<span data-ttu-id="efaa5-106">Funktsioon võimaldab ettevõtetel määratleda erinevaid ühikuteisendusi sama kauba variantide vahel.</span><span class="sxs-lookup"><span data-stu-id="efaa5-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="efaa5-107">Selles teemas kasutatakse järgmist näidet.</span><span class="sxs-lookup"><span data-stu-id="efaa5-107">The following example is used in this topic.</span></span> <span data-ttu-id="efaa5-108">Ettevõte müüb t-särke suuruses S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="efaa5-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="efaa5-109">T-särgi määratletakse tootena ja erinevad suurused määratletakse toote variantidena.</span><span class="sxs-lookup"><span data-stu-id="efaa5-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="efaa5-110">T-särgid on pakendatud kastidesse ja ühes kastis võib olla viis t-särki, välja arvatud XL suurus, kus on ruumi ainult neljale t-särgile.</span><span class="sxs-lookup"><span data-stu-id="efaa5-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="efaa5-111">Ettevõte soovib jälgida t-särkide erinevaid variante üksuses **Tükid**, aga müüb T-särke üksuses **Kastid**.</span><span class="sxs-lookup"><span data-stu-id="efaa5-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="efaa5-112">Teisendused laoüksuse ja müügiüksuse vahel on 1 kast = 5 tükki, välja arvatud variant XL, kus teisendus on 1 kast = 4 tükki.</span><span class="sxs-lookup"><span data-stu-id="efaa5-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="efaa5-113">Seadistage toode ühiku teisaldamiseks varjandi kohta</span><span class="sxs-lookup"><span data-stu-id="efaa5-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="efaa5-114">Tootevariantide saab luua ainult toodetele **Toote alamtüüp**: **Tooteetalon**.</span><span class="sxs-lookup"><span data-stu-id="efaa5-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="efaa5-115">Lisateavet vt jaotisest [Tooteetaloni loomine](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="efaa5-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="efaa5-116">Funktsioon ei ole lubatud toodete puhul, mis on seadistatud tegeliku kaalu protsesside jaoks.</span><span class="sxs-lookup"><span data-stu-id="efaa5-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="efaa5-117">Kui tooteetalon koos väljastatud toodete variantidega on loodud, saab seadistada ühikuteisendused variantide kohta.</span><span class="sxs-lookup"><span data-stu-id="efaa5-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="efaa5-118">Toote või tootevariandi kontekstis toimuvate ühikuteisenduste avamise menüüelemendi leiate järgmistel lehekülgedelt.</span><span class="sxs-lookup"><span data-stu-id="efaa5-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="efaa5-119">Leht **Toote üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="efaa5-119">**Product details** page</span></span>
-   <span data-ttu-id="efaa5-120">Leht **Väljastatud toodete üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="efaa5-120">**Released products details** page</span></span>
-   <span data-ttu-id="efaa5-121">Leht **Väljastatud toodete variandid**</span><span class="sxs-lookup"><span data-stu-id="efaa5-121">**Released product variants** page</span></span>

<span data-ttu-id="efaa5-122">Kui avate lehe **Ühikuteisendused** tooteetaloni kontekstis või väljastatud tootevariandi konstekstis, võite valida, kas soovite seadistada ühikuteisenduse tootele või tootevariandile.</span><span class="sxs-lookup"><span data-stu-id="efaa5-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="efaa5-123">Seda saate teha valides kas **Tootevariant** või **Toode** väljal **Loo teisendus:**.</span><span class="sxs-lookup"><span data-stu-id="efaa5-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="efaa5-124">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="efaa5-124">Product variant</span></span>

<span data-ttu-id="efaa5-125">Kui valite valiku **Tootevariant**, siis saate valida, millisele variandile soovite ühikuteisendusi seadistada, väljal **Tootevariant**.</span><span class="sxs-lookup"><span data-stu-id="efaa5-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="efaa5-126">Toode</span><span class="sxs-lookup"><span data-stu-id="efaa5-126">Product</span></span>

<span data-ttu-id="efaa5-127">Kui valite valiku **Toode**, siis saate seadistada ühikuteisenduse tooteetaloni jaoks.</span><span class="sxs-lookup"><span data-stu-id="efaa5-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="efaa5-128">See ühikuteisendus rakendub kõigile tootevariantidele ilma määratletud ühiku teisenduseta.</span><span class="sxs-lookup"><span data-stu-id="efaa5-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="efaa5-129">Näide</span><span class="sxs-lookup"><span data-stu-id="efaa5-129">Example</span></span>

<span data-ttu-id="efaa5-130">Tooteetalonil **T-särk** on neli väljastatud toodete varianti, S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="efaa5-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="efaa5-131">T-särgid on pakendatud kastidesse ja ühes kastis võib olla viis t-särki, välja arvatud XL suurus, kus on ruumi ainult neljale t-särgile.</span><span class="sxs-lookup"><span data-stu-id="efaa5-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="efaa5-132">Avage kõigepealt lehekülg **Ühikuteisendus** toote **T-särk** väljastatut toote üksikasjade lehelt.</span><span class="sxs-lookup"><span data-stu-id="efaa5-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="efaa5-133">Seadistage lehel **Ühikuteisendus** ühikuteisendus väljastatud tootevariandi XL jaoks.</span><span class="sxs-lookup"><span data-stu-id="efaa5-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="efaa5-134">**Väli**</span><span class="sxs-lookup"><span data-stu-id="efaa5-134">**Field**</span></span>             | <span data-ttu-id="efaa5-135">**Sätted**</span><span class="sxs-lookup"><span data-stu-id="efaa5-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="efaa5-136">Loo teisendus:</span><span class="sxs-lookup"><span data-stu-id="efaa5-136">Create conversion for</span></span> | <span data-ttu-id="efaa5-137">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="efaa5-137">Product variant</span></span>         |
| <span data-ttu-id="efaa5-138">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="efaa5-138">Product variant</span></span>       | <span data-ttu-id="efaa5-139">T-särk : : XL : :</span><span class="sxs-lookup"><span data-stu-id="efaa5-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="efaa5-140">Lähteühik</span><span class="sxs-lookup"><span data-stu-id="efaa5-140">From unit</span></span>             | <span data-ttu-id="efaa5-141">Kastid</span><span class="sxs-lookup"><span data-stu-id="efaa5-141">Boxes</span></span>                   |
| <span data-ttu-id="efaa5-142">Tegur</span><span class="sxs-lookup"><span data-stu-id="efaa5-142">Factor</span></span>                | <span data-ttu-id="efaa5-143">4</span><span class="sxs-lookup"><span data-stu-id="efaa5-143">4</span></span>                       |
| <span data-ttu-id="efaa5-144">Ühikuks</span><span class="sxs-lookup"><span data-stu-id="efaa5-144">To Unit</span></span>               | <span data-ttu-id="efaa5-145">Osad</span><span class="sxs-lookup"><span data-stu-id="efaa5-145">Pieces</span></span>                  |

<span data-ttu-id="efaa5-146">Väljastatud toodete variantidel S, M ja L on ühikute Kast ja Tükid vahel sama ühikuteisendus, mis tähendab, et saate nende tootevariantide ühikuteisendused määratleda tooteetalonis.</span><span class="sxs-lookup"><span data-stu-id="efaa5-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="efaa5-147">**Väli**</span><span class="sxs-lookup"><span data-stu-id="efaa5-147">**Field**</span></span>             | <span data-ttu-id="efaa5-148">**Sätted**</span><span class="sxs-lookup"><span data-stu-id="efaa5-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="efaa5-149">Loo teisendus:</span><span class="sxs-lookup"><span data-stu-id="efaa5-149">Create conversion for</span></span> | <span data-ttu-id="efaa5-150">Toode</span><span class="sxs-lookup"><span data-stu-id="efaa5-150">Product</span></span>     |
| <span data-ttu-id="efaa5-151">Toode</span><span class="sxs-lookup"><span data-stu-id="efaa5-151">Product</span></span>               | <span data-ttu-id="efaa5-152">T-särk</span><span class="sxs-lookup"><span data-stu-id="efaa5-152">T-Shirt</span></span>     |
| <span data-ttu-id="efaa5-153">Lähteühik</span><span class="sxs-lookup"><span data-stu-id="efaa5-153">From unit</span></span>             | <span data-ttu-id="efaa5-154">Kastid</span><span class="sxs-lookup"><span data-stu-id="efaa5-154">Boxes</span></span>       |
| <span data-ttu-id="efaa5-155">Tegur</span><span class="sxs-lookup"><span data-stu-id="efaa5-155">Factor</span></span>                | <span data-ttu-id="efaa5-156">5</span><span class="sxs-lookup"><span data-stu-id="efaa5-156">5</span></span>           |
| <span data-ttu-id="efaa5-157">Ühikuks</span><span class="sxs-lookup"><span data-stu-id="efaa5-157">To Unit</span></span>               | <span data-ttu-id="efaa5-158">Osad</span><span class="sxs-lookup"><span data-stu-id="efaa5-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="efaa5-159">Exceli kasutamine ühikuteisenduste värskendamiseks</span><span class="sxs-lookup"><span data-stu-id="efaa5-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="efaa5-160">Kui tootel on palju tootevariante erinevate ühikuteisendustega, on hea mõte eksportida ühikuteisendused leheküljelt **Ühikuteisendus** Exceli tabelisse, värskendada teisendusi ja seejärel laadida need tagasi rakendusse Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="efaa5-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="efaa5-161">Excelisse eksportimise ja muudatuste uuesti rakendusse Supply Chain Mangementi laadimise valiku saab sisse lülitada lehekülje **Ühikuteisendus** tegumirea menüüelemendist **Ava Microsoft Office’is**.</span><span class="sxs-lookup"><span data-stu-id="efaa5-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
