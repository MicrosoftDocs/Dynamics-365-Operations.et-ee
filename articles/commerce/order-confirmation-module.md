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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6610d2abe0a1b03ddd763f9a65fc1dab42f1da1b
ms.sourcegitcommit: 49f3011b8a6d8cdd038e153d8cb3cf773be25ae4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015176"
---
# <a name="order-details-module"></a><span data-ttu-id="14995-103">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="14995-103">Order details module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="14995-104">See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.</span><span class="sxs-lookup"><span data-stu-id="14995-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="14995-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="14995-105">Overview</span></span>

<span data-ttu-id="14995-106">Tellimuse üksikasjade moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="14995-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="14995-107">See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kauvad makseteave ja tarneviis.</span><span class="sxs-lookup"><span data-stu-id="14995-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="14995-108">Tellimuse üksikasjade mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="14995-108">Order details module properties</span></span>

| <span data-ttu-id="14995-109">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="14995-109">Property name</span></span>  | <span data-ttu-id="14995-110">Väärtused</span><span class="sxs-lookup"><span data-stu-id="14995-110">Values</span></span> | <span data-ttu-id="14995-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="14995-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="14995-112">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="14995-112">Heading</span></span>        | <span data-ttu-id="14995-113">Pealkirja tekst ja pealkirja silt ( **H1** , **H2** , **H3** , **H4** , **H5** või **H6** )</span><span class="sxs-lookup"><span data-stu-id="14995-113">Heading text and heading tag ( **H1** , **H2** , **H3** , **H4** , **H5** , or **H6** )</span></span> | <span data-ttu-id="14995-114">Tellimuse üksikasjade moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="14995-114">The order details module can have a heading.</span></span> <span data-ttu-id="14995-115">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="14995-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="14995-116">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="14995-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="14995-117">Kontakti number</span><span class="sxs-lookup"><span data-stu-id="14995-117">Contact number</span></span> | <span data-ttu-id="14995-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="14995-118">Text</span></span> | <span data-ttu-id="14995-119">Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit.</span><span class="sxs-lookup"><span data-stu-id="14995-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="14995-120">Moodulid, mida saab tellimuse üksikasjade lehel kasutada</span><span class="sxs-lookup"><span data-stu-id="14995-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="14995-121">Tellimuse üksikasjade lehe loomisel saate lisaks tellimuse üksikasjade moodulile lisada ka teisi asjakohaseid mooduleid.</span><span class="sxs-lookup"><span data-stu-id="14995-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="14995-122">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="14995-122">Here are some examples:</span></span>

- <span data-ttu-id="14995-123">**Soovituste moodul** – soovituste mooduli saab lisada tellimuse üksikasjade lehele, et soovitada kliendile muid tooteid.</span><span class="sxs-lookup"><span data-stu-id="14995-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="14995-124">**Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse üksikasjade lehele, et kuvada turunduse sisu.</span><span class="sxs-lookup"><span data-stu-id="14995-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="14995-125">Lehele tellimuse üksikasjade mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="14995-125">Add an order details module to a page</span></span>

<span data-ttu-id="14995-126">Uuele lehele tellimuse üksikasjade mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="14995-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="14995-127">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14995-127">Go to **Templates** , and select **New** to create a new template.</span></span>
1. <span data-ttu-id="14995-128">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all nimi **Tellimuse üksikasjade mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="14995-128">In the **New Template** dialog box, under **Template name** , enter the name **Order details template** , and then select **OK**.</span></span>
1. <span data-ttu-id="14995-129">Valige pesas **Keha** kolmikpunkt ( **…** ) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="14995-129">In the **Body** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="14995-130">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="14995-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="14995-131">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt ( **...** ) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="14995-131">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="14995-132">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="14995-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="14995-133">Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="14995-133">Select **Save** , and then select **Preview** to preview the template.</span></span> <span data-ttu-id="14995-134">Tellimuse üksikasjade moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.</span><span class="sxs-lookup"><span data-stu-id="14995-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="14995-135">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="14995-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="14995-136">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14995-136">Go to **Pages** , and select **New** to create a new page.</span></span>
1. <span data-ttu-id="14995-137">Valige dialoogiboksis **Vali mall** suvand **Tellimuse üksikasjade mall**.</span><span class="sxs-lookup"><span data-stu-id="14995-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="14995-138">Sisestage jaotises **Lehe nimi** väärtus **Tellimuse üksikasjade leht** ja seejärel klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="14995-138">Under **Page name** , enter **Order details page** , and then select **OK**.</span></span>
1. <span data-ttu-id="14995-139">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt ( **...** ) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="14995-139">In the **Main** slot of the **Default Page** module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="14995-140">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="14995-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="14995-141">Valige tellimuse üksikasjade mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="14995-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="14995-142">Sisestage dialoogiboksi **Pealkiri** väljale **Pealkirja tekst** pealkirja tekst **Tellimuse üksikasjad** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="14995-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details** , and then select **OK**.</span></span>
1. <span data-ttu-id="14995-143">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="14995-143">Select **Save** , and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="14995-144">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="14995-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14995-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="14995-145">Additional resources</span></span>

[<span data-ttu-id="14995-146">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="14995-146">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="14995-147">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="14995-147">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="14995-148">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="14995-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="14995-149">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="14995-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="14995-150">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="14995-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="14995-151">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="14995-151">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="14995-152">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="14995-152">Gift card module</span></span>](add-giftcard.md)
