---
title: Mõõteühiku teisendus tootevariandi kohta
description: See teema kirjeldab, kuidas saab seadistada tootevariantide mõõtühikute teisendusi.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 9d5d6fd65717cd886f1c6576aabf2bc59ca4fcaf
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "345923"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="1caf9-103">Mõõteühiku teisendus tootevariandi kohta</span><span class="sxs-lookup"><span data-stu-id="1caf9-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="1caf9-104">See teema kirjeldab, kuidas saab seadistada tootevariantide mõõtühikute teisendusi.</span><span class="sxs-lookup"><span data-stu-id="1caf9-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="1caf9-105">See sisaldab seadistuse näidet.</span><span class="sxs-lookup"><span data-stu-id="1caf9-105">It includes an example of the setup.</span></span>

<span data-ttu-id="1caf9-106">Funktsioon võimaldab ettevõtetel määratleda erinevaid ühikuteisendusi sama kauba variantide vahel.</span><span class="sxs-lookup"><span data-stu-id="1caf9-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="1caf9-107">Selles teemas kasutatakse järgmist näidet.</span><span class="sxs-lookup"><span data-stu-id="1caf9-107">The following example is used in this topic.</span></span> <span data-ttu-id="1caf9-108">Ettevõte müüb t-särke suuruses S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="1caf9-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="1caf9-109">T-särgi määratletakse tootena ja erinevad suurused määratletakse toote variantidena.</span><span class="sxs-lookup"><span data-stu-id="1caf9-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="1caf9-110">T-särgid on pakendatud kastidesse ja ühes kastis võib olla viis t-särki, välja arvatud XL suurus, kus on ruumi ainult neljale t-särgile.</span><span class="sxs-lookup"><span data-stu-id="1caf9-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="1caf9-111">Ettevõte soovib jälgida t-särkide erinevaid variante üksuses **Tükid**, aga müüb T-särke üksuses **Kastid**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="1caf9-112">Teisendused laoüksuse ja müügiüksuse vahel on 1 kast = 5 tükki, välja arvatud variant XL, kus teisendus on 1 kast = 4 tükki.</span><span class="sxs-lookup"><span data-stu-id="1caf9-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="1caf9-113">Seadistus</span><span class="sxs-lookup"><span data-stu-id="1caf9-113">Setup</span></span>

<span data-ttu-id="1caf9-114">Saate konfigureerida parameetrid funktsiooni kasutamiseks kas toodetele, mille puhul on lubatud **Kõik protsessid** või ainult tootele, mille puhul on lubatud **Lao protsessid**, kasutades suvandit **Luba mõõtühiku teisaldamine** lehel **Tooteteabe parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="1caf9-115">Seadistage toode ühiku teisaldamiseks varjandi kohta</span><span class="sxs-lookup"><span data-stu-id="1caf9-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="1caf9-116">Tootevariantide saab luua ainult toodetele **Toote alamtüüp**: **Tooteetalon**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="1caf9-117">Lisateavet vt jaotisest [Tooteetaloni loomine](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="1caf9-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="1caf9-118">Funktsioon ei ole lubatud toodete puhul, mis on seadistatud tegeliku kaalu protsesside jaoks.</span><span class="sxs-lookup"><span data-stu-id="1caf9-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="1caf9-119">Tooteetaloni loomise ajal lubage mõõtühiku teisendamine, kasutades suvandit **Luba mõõtühiku teisendused** lehel **Toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="1caf9-120">Kui tooteetalon koos väljastatud toodete variantidega on loodud, saab seadistada ühikuteisendused variantide kohta.</span><span class="sxs-lookup"><span data-stu-id="1caf9-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="1caf9-121">Toote või tootevariandi kontekstis toimuvate ühikuteisenduste avamise menüüelemendi leiate järgmistel lehekülgedelt.</span><span class="sxs-lookup"><span data-stu-id="1caf9-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="1caf9-122">Leht **Toote üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="1caf9-122">**Product details** page</span></span>
-   <span data-ttu-id="1caf9-123">Leht **Väljastatud toodete üksikasjad**</span><span class="sxs-lookup"><span data-stu-id="1caf9-123">**Released products details** page</span></span>
-   <span data-ttu-id="1caf9-124">Leht **Väljastatud toodete variandid**</span><span class="sxs-lookup"><span data-stu-id="1caf9-124">**Released product variants** page</span></span>

<span data-ttu-id="1caf9-125">Kui avate lehe **Ühikuteisendused** tooteetaloni kontekstis või väljastatud tootevariandi konstekstis, võite valida, kas soovite seadistada ühikuteisenduse tootele või tootevariandile.</span><span class="sxs-lookup"><span data-stu-id="1caf9-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="1caf9-126">Seda saate teha valides kas **Tootevariant** või **Toode** väljal **Loo teisendus:**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="1caf9-127">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="1caf9-127">Product variant</span></span>

<span data-ttu-id="1caf9-128">Kui valite valiku **Tootevariant**, siis saate valida, millisele variandile soovite ühikuteisendusi seadistada, väljal **Tootevariant**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="1caf9-129">Toode</span><span class="sxs-lookup"><span data-stu-id="1caf9-129">Product</span></span>

<span data-ttu-id="1caf9-130">Kui valite valiku **Toode**, siis saate seadistada ühikuteisenduse tooteetaloni jaoks.</span><span class="sxs-lookup"><span data-stu-id="1caf9-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="1caf9-131">See ühikuteisendus rakendub kõigile tootevariantidele ilma määratletud ühiku teisenduseta.</span><span class="sxs-lookup"><span data-stu-id="1caf9-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="1caf9-132">Näide</span><span class="sxs-lookup"><span data-stu-id="1caf9-132">Example</span></span>

<span data-ttu-id="1caf9-133">Tooteetalonil **T-särk** on neli väljastatud toodete varianti, S, M, L ja XL.</span><span class="sxs-lookup"><span data-stu-id="1caf9-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="1caf9-134">T-särgid on pakendatud kastidesse ja ühes kastis võib olla viis t-särki, välja arvatud XL suurus, kus on ruumi ainult neljale t-särgile.</span><span class="sxs-lookup"><span data-stu-id="1caf9-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="1caf9-135">Avage kõigepealt lehekülg **Ühikuteisendus** toote **T-särk** väljastatut toote üksikasjade lehelt.</span><span class="sxs-lookup"><span data-stu-id="1caf9-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="1caf9-136">Seadistage lehel **Ühikuteisendus** ühikuteisendus väljastatud tootevariandi XL jaoks.</span><span class="sxs-lookup"><span data-stu-id="1caf9-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="1caf9-137">**Väli**</span><span class="sxs-lookup"><span data-stu-id="1caf9-137">**Field**</span></span>             | <span data-ttu-id="1caf9-138">**Sätted**</span><span class="sxs-lookup"><span data-stu-id="1caf9-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="1caf9-139">Loo teisendus:</span><span class="sxs-lookup"><span data-stu-id="1caf9-139">Create conversion for</span></span> | <span data-ttu-id="1caf9-140">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="1caf9-140">Product variant</span></span>         |
| <span data-ttu-id="1caf9-141">Tootevariant</span><span class="sxs-lookup"><span data-stu-id="1caf9-141">Product variant</span></span>       | <span data-ttu-id="1caf9-142">T-särk : : XL : :</span><span class="sxs-lookup"><span data-stu-id="1caf9-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="1caf9-143">Lähteühik</span><span class="sxs-lookup"><span data-stu-id="1caf9-143">From unit</span></span>             | <span data-ttu-id="1caf9-144">Kastid</span><span class="sxs-lookup"><span data-stu-id="1caf9-144">Boxes</span></span>                   |
| <span data-ttu-id="1caf9-145">Tegur</span><span class="sxs-lookup"><span data-stu-id="1caf9-145">Factor</span></span>                | <span data-ttu-id="1caf9-146">4</span><span class="sxs-lookup"><span data-stu-id="1caf9-146">4</span></span>                       |
| <span data-ttu-id="1caf9-147">Ühikuks</span><span class="sxs-lookup"><span data-stu-id="1caf9-147">To Unit</span></span>               | <span data-ttu-id="1caf9-148">Osad</span><span class="sxs-lookup"><span data-stu-id="1caf9-148">Pieces</span></span>                  |

<span data-ttu-id="1caf9-149">Väljastatud toodete variantidel S, M ja L on ühikute Kast ja Tükid vahel sama ühikuteisendus, mis tähendab, et saate nende tootevariantide ühikuteisendused määratleda tooteetalonis.</span><span class="sxs-lookup"><span data-stu-id="1caf9-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="1caf9-150">**Väli**</span><span class="sxs-lookup"><span data-stu-id="1caf9-150">**Field**</span></span>             | <span data-ttu-id="1caf9-151">**Sätted**</span><span class="sxs-lookup"><span data-stu-id="1caf9-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="1caf9-152">Loo teisendus:</span><span class="sxs-lookup"><span data-stu-id="1caf9-152">Create conversion for</span></span> | <span data-ttu-id="1caf9-153">Toode</span><span class="sxs-lookup"><span data-stu-id="1caf9-153">Product</span></span>     |
| <span data-ttu-id="1caf9-154">Toode</span><span class="sxs-lookup"><span data-stu-id="1caf9-154">Product</span></span>               | <span data-ttu-id="1caf9-155">T-särk</span><span class="sxs-lookup"><span data-stu-id="1caf9-155">T-Shirt</span></span>     |
| <span data-ttu-id="1caf9-156">Lähteühik</span><span class="sxs-lookup"><span data-stu-id="1caf9-156">From unit</span></span>             | <span data-ttu-id="1caf9-157">Kastid</span><span class="sxs-lookup"><span data-stu-id="1caf9-157">Boxes</span></span>       |
| <span data-ttu-id="1caf9-158">Tegur</span><span class="sxs-lookup"><span data-stu-id="1caf9-158">Factor</span></span>                | <span data-ttu-id="1caf9-159">5</span><span class="sxs-lookup"><span data-stu-id="1caf9-159">5</span></span>           |
| <span data-ttu-id="1caf9-160">Ühikuks</span><span class="sxs-lookup"><span data-stu-id="1caf9-160">To Unit</span></span>               | <span data-ttu-id="1caf9-161">Osad</span><span class="sxs-lookup"><span data-stu-id="1caf9-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="1caf9-162">Exceli kasutamine ühikuteisenduste värskendamiseks</span><span class="sxs-lookup"><span data-stu-id="1caf9-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="1caf9-163">Kui tootel on palju tootevariante erinevate ühikuteisendustega, on hea mõte eksportida ühikuteisendused leheküljelt **Ühikuteisendus** Exceli tabelisse, värskendada teisendusi ja seejärel laadida need tagasi rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="1caf9-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="1caf9-164">Excelisse eksportimise ja muudatuste uuesti rakendusse Finance and Operations laadimise valiku saab sisse lülitada lehekülje **Ühikuteisendus** tegumirea menüüelemendist **Ava Microsoft Office’is**.</span><span class="sxs-lookup"><span data-stu-id="1caf9-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
