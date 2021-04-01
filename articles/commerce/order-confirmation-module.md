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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 407fc2724d4b589ef5f611974f9358e879dba7ed
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257143"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="b6d24-103">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b6d24-104">See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.</span><span class="sxs-lookup"><span data-stu-id="b6d24-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b6d24-105">Tellimuse kinnitamise moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="b6d24-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="b6d24-106">See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kaubad, makseteave, järeletulemisvõimalused ja tarneviis.</span><span class="sxs-lookup"><span data-stu-id="b6d24-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="b6d24-107">Tellimuse kinnituse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="b6d24-107">Order confirmation module properties</span></span>

| <span data-ttu-id="b6d24-108">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="b6d24-108">Property name</span></span>  | <span data-ttu-id="b6d24-109">Väärtused</span><span class="sxs-lookup"><span data-stu-id="b6d24-109">Values</span></span> | <span data-ttu-id="b6d24-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b6d24-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b6d24-111">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="b6d24-111">Heading</span></span>        | <span data-ttu-id="b6d24-112">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="b6d24-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b6d24-113">Tellimuse kinnituse moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="b6d24-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="b6d24-114">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="b6d24-115">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="b6d24-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="b6d24-116">Kontakti number</span><span class="sxs-lookup"><span data-stu-id="b6d24-116">Contact number</span></span> | <span data-ttu-id="b6d24-117">Tekst</span><span class="sxs-lookup"><span data-stu-id="b6d24-117">Text</span></span> | <span data-ttu-id="b6d24-118">Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit.</span><span class="sxs-lookup"><span data-stu-id="b6d24-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="b6d24-119">Järeletulemise ajavahemiku teabe kuvamine</span><span class="sxs-lookup"><span data-stu-id="b6d24-119">Show pickup timeslot information</span></span> | <span data-ttu-id="b6d24-120">Tõene või väär</span><span class="sxs-lookup"><span data-stu-id="b6d24-120">True or False</span></span> | <span data-ttu-id="b6d24-121">See atribuut on saadaval Dynamics 365 Commerce'i versioonis 10.0.15 või uuemas versioonis.</span><span class="sxs-lookup"><span data-stu-id="b6d24-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="b6d24-122">Kui see on tõene, kuvatakse järeletulemise ajavahemiku teave, kui see on kauba järeletulemise jaoks ette nähtud</span><span class="sxs-lookup"><span data-stu-id="b6d24-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="b6d24-123">Moodulid, mida saab tellimuse kinnitamise lehel kasutada</span><span class="sxs-lookup"><span data-stu-id="b6d24-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="b6d24-124">Tellimuse kinnitamise lehe loomisel saate lisaks tellimuse kinnitamise moodulile lisada ka teisi asjakohaseid mooduleid.</span><span class="sxs-lookup"><span data-stu-id="b6d24-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="b6d24-125">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="b6d24-125">Here are some examples:</span></span>

- <span data-ttu-id="b6d24-126">**Soovituste moodul** – soovituste mooduli saab lisada tellimuse kinnitamise lehele, et soovitada kliendile muid tooteid.</span><span class="sxs-lookup"><span data-stu-id="b6d24-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="b6d24-127">**Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse kinnitamise lehele, et kuvada turunduse sisu.</span><span class="sxs-lookup"><span data-stu-id="b6d24-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="b6d24-128">Lehele tellimuse kinnitamise mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="b6d24-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="b6d24-129">Uuele lehele tellimuse kinnitamise mooduli lisamiseks ja vajalike atribuutide häälestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b6d24-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b6d24-130">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b6d24-131">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all nimi **Tellimuse kinnitamise mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b6d24-132">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b6d24-133">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b6d24-134">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b6d24-135">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse kinnitamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b6d24-136">Valige **Salvesta** ja seejärel malli eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="b6d24-137">Tellimuse kinnituse moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.</span><span class="sxs-lookup"><span data-stu-id="b6d24-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="b6d24-138">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b6d24-139">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b6d24-140">Valige dialoogiboksis **Malli valimine** suvand **Tellimuse kinnitamise mall**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="b6d24-141">Sisestage jaotises **Lehe nimi** väärtus **Tellimuse kinnitamise leht** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="b6d24-142">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b6d24-143">Valige dialoogiboksis **Lisa moodul** moodul **Tellimuse kinnitamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b6d24-144">Valige tellimuse kinnitamise mooduli atribuutide paanil pliiatsisümboli kõrval olev suvand **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="b6d24-145">Sisestage dialoogiboksi **Pealkiri** väljale **Pealkirja tekst** pealkirja tekst **Tellimuse kinnitamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="b6d24-146">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="b6d24-147">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="b6d24-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b6d24-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b6d24-148">Additional resources</span></span>

[<span data-ttu-id="b6d24-149">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b6d24-150">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b6d24-151">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b6d24-152">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b6d24-153">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b6d24-154">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="b6d24-155">Järeletulemise teabe moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b6d24-156">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="b6d24-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]