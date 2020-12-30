---
title: Tellimuse kinnituse moodul
description: See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.openlocfilehash: bf33ebf9c0c5136f40fcd7e1012988d186c4169b
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411837"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="a7100-103">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a7100-104">See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.</span><span class="sxs-lookup"><span data-stu-id="a7100-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a7100-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="a7100-105">Overview</span></span>

<span data-ttu-id="a7100-106">Tellimuse kinnitamise moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7100-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="a7100-107">See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kaubad, makseteave, järeletulemisvõimalused ja tarneviis.</span><span class="sxs-lookup"><span data-stu-id="a7100-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="a7100-108">Tellimuse kinnituse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="a7100-108">Order confirmation module properties</span></span>

| <span data-ttu-id="a7100-109">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="a7100-109">Property name</span></span>  | <span data-ttu-id="a7100-110">Väärtused</span><span class="sxs-lookup"><span data-stu-id="a7100-110">Values</span></span> | <span data-ttu-id="a7100-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a7100-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="a7100-112">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="a7100-112">Heading</span></span>        | <span data-ttu-id="a7100-113">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="a7100-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="a7100-114">Tellimuse kinnituse moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="a7100-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="a7100-115">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="a7100-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="a7100-116">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="a7100-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="a7100-117">Kontakti number</span><span class="sxs-lookup"><span data-stu-id="a7100-117">Contact number</span></span> | <span data-ttu-id="a7100-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="a7100-118">Text</span></span> | <span data-ttu-id="a7100-119">Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit.</span><span class="sxs-lookup"><span data-stu-id="a7100-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="a7100-120">Järeletulemise ajavahemiku teabe kuvamine</span><span class="sxs-lookup"><span data-stu-id="a7100-120">Show pickup timeslot information</span></span> | <span data-ttu-id="a7100-121">Tõene või väär</span><span class="sxs-lookup"><span data-stu-id="a7100-121">True or False</span></span> | <span data-ttu-id="a7100-122">See atribuut on saadaval Dynamics 365 Commerce'i versioonis 10.0.15 või uuemas versioonis.</span><span class="sxs-lookup"><span data-stu-id="a7100-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="a7100-123">Kui see on tõene, kuvatakse järeletulemise ajavahemiku teave, kui see on kauba järeletulemise jaoks ette nähtud</span><span class="sxs-lookup"><span data-stu-id="a7100-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="a7100-124">Moodulid, mida saab tellimuse kinnitamise lehel kasutada</span><span class="sxs-lookup"><span data-stu-id="a7100-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="a7100-125">Tellimuse kinnitamise lehe loomisel saate lisaks tellimuse kinnitamise moodulile lisada ka teisi asjakohaseid mooduleid.</span><span class="sxs-lookup"><span data-stu-id="a7100-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="a7100-126">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="a7100-126">Here are some examples:</span></span>

- <span data-ttu-id="a7100-127">**Soovituste moodul** – soovituste mooduli saab lisada tellimuse kinnitamise lehele, et soovitada kliendile muid tooteid.</span><span class="sxs-lookup"><span data-stu-id="a7100-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="a7100-128">**Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse kinnitamise lehele, et kuvada turunduse sisu.</span><span class="sxs-lookup"><span data-stu-id="a7100-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="a7100-129">Lehele tellimuse kinnitamise mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="a7100-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="a7100-130">Uuele lehele tellimuse kinnitamise mooduli lisamiseks ja vajalike atribuutide häälestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a7100-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a7100-131">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7100-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="a7100-132">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all nimi **Tellimuse kinnitamise mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7100-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a7100-133">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="a7100-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a7100-134">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7100-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a7100-135">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="a7100-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a7100-136">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse kinnitamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7100-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a7100-137">Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="a7100-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="a7100-138">Tellimuse kinnituse moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.</span><span class="sxs-lookup"><span data-stu-id="a7100-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="a7100-139">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a7100-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="a7100-140">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a7100-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="a7100-141">Valige dialoogiboksis **Malli valimine** suvand **Tellimuse kinnitamise mall**.</span><span class="sxs-lookup"><span data-stu-id="a7100-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="a7100-142">Sisestage jaotises **Lehe nimi** väärtus **Tellimuse kinnitamise leht** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7100-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="a7100-143">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="a7100-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a7100-144">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse kinnitamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7100-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a7100-145">Valige tellimuse kinnitamise mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="a7100-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="a7100-146">Sisestage dialoogiboksi **Pealkiri** väljale **Pealkirja tekst** pealkirja tekst **Tellimuse kinnitamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7100-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="a7100-147">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="a7100-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="a7100-148">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a7100-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7100-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a7100-149">Additional resources</span></span>

[<span data-ttu-id="a7100-150">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="a7100-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="a7100-151">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a7100-152">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="a7100-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a7100-153">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="a7100-154">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="a7100-155">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="a7100-156">Järeletulemise teabe moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="a7100-157">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="a7100-157">Gift card module</span></span>](add-giftcard.md)
