---
title: Tellimuse üksikasjade moodul
description: See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464926"
---
# <a name="order-details-module"></a><span data-ttu-id="6ad6c-103">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6ad6c-104">See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6ad6c-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="6ad6c-105">Overview</span></span>

<span data-ttu-id="6ad6c-106">Tellimuse üksikasjade moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="6ad6c-107">See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kauvad makseteave ja tarneviis.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="6ad6c-108">Tellimuse üksikasjade mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="6ad6c-108">Order details module properties</span></span>

| <span data-ttu-id="6ad6c-109">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="6ad6c-109">Property name</span></span>  | <span data-ttu-id="6ad6c-110">Väärtused</span><span class="sxs-lookup"><span data-stu-id="6ad6c-110">Values</span></span> | <span data-ttu-id="6ad6c-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6ad6c-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="6ad6c-112">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="6ad6c-112">Heading</span></span>        | <span data-ttu-id="6ad6c-113">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="6ad6c-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="6ad6c-114">Tellimuse üksikasjade moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-114">The order details module can have a heading.</span></span> <span data-ttu-id="6ad6c-115">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="6ad6c-116">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="6ad6c-117">Kontakti number</span><span class="sxs-lookup"><span data-stu-id="6ad6c-117">Contact number</span></span> | <span data-ttu-id="6ad6c-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="6ad6c-118">Text</span></span> | <span data-ttu-id="6ad6c-119">Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="6ad6c-120">Moodulid, mida saab tellimuse üksikasjade lehel kasutada</span><span class="sxs-lookup"><span data-stu-id="6ad6c-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="6ad6c-121">Tellimuse üksikasjade lehe loomisel saate lisaks tellimuse üksikasjade moodulile lisada ka teisi asjakohaseid mooduleid.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="6ad6c-122">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-122">Here are some examples:</span></span>

- <span data-ttu-id="6ad6c-123">**Soovituste moodul** – soovituste mooduli saab lisada tellimuse üksikasjade lehele, et soovitada kliendile muid tooteid.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="6ad6c-124">**Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse üksikasjade lehele, et kuvada turunduse sisu.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="6ad6c-125">Lehele tellimuse üksikasjade mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="6ad6c-125">Add an order details module to a page</span></span>

<span data-ttu-id="6ad6c-126">Uuele lehele tellimuse üksikasjade mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="6ad6c-127">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="6ad6c-128">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all nimi **Tellimuse üksikasjade mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad6c-129">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ad6c-130">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad6c-131">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ad6c-132">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad6c-133">Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="6ad6c-134">Tellimuse üksikasjade moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="6ad6c-135">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="6ad6c-136">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="6ad6c-137">Valige dialoogiboksis **Vali mall** suvand **Tellimuse üksikasjade mall**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="6ad6c-138">Sisestage jaotises **Lehe nimi** väärtus **Tellimuse üksikasjade leht** ja seejärel klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad6c-139">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="6ad6c-140">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad6c-141">Valige tellimuse üksikasjade mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="6ad6c-142">Sisestage dialoogiboksi **Pealkiri** väljale **Pealkirja tekst** pealkirja tekst **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="6ad6c-143">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="6ad6c-144">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="6ad6c-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6ad6c-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6ad6c-145">Additional resources</span></span>

[<span data-ttu-id="6ad6c-146">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="6ad6c-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6ad6c-147">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-147">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6ad6c-148">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-148">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6ad6c-149">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6ad6c-150">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-150">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6ad6c-151">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-151">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6ad6c-152">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="6ad6c-152">Footer module</span></span>](author-footer-module.md)
