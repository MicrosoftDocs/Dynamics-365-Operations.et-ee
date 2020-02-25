---
title: Tellimuse üksikasjade moodul
description: See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.
author: anupamar
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: cb09a0b6ce1e48707f96021e9fad0006d9c1c55c
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026013"
---
# <a name="order-details-module"></a><span data-ttu-id="91a27-103">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="91a27-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="91a27-104">See teema hõlmab tellimuse üksikasjade mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce kasutada.</span><span class="sxs-lookup"><span data-stu-id="91a27-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91a27-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="91a27-105">Overview</span></span>

<span data-ttu-id="91a27-106">Tellimuse üksikasjade moodulit kasutatakse pärast tellimuse esitamist tellimuse kinnituse üksikasjade kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="91a27-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="91a27-107">See kuvab tellimuse kinnituse ID, tellimuse kontaktandmeid ja muud tellimuse üksikasjad, nagu ostetud kauvad makseteave ja tarneviis.</span><span class="sxs-lookup"><span data-stu-id="91a27-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="91a27-108">Tellimuse kinnituse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="91a27-108">Order confirmation module properties</span></span>

| <span data-ttu-id="91a27-109">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="91a27-109">Property name</span></span>  | <span data-ttu-id="91a27-110">Väärtused</span><span class="sxs-lookup"><span data-stu-id="91a27-110">Values</span></span> | <span data-ttu-id="91a27-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91a27-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="91a27-112">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="91a27-112">Heading</span></span>        | <span data-ttu-id="91a27-113">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="91a27-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="91a27-114">Tellimuse kinnituse moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="91a27-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="91a27-115">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="91a27-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="91a27-116">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="91a27-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="91a27-117">Kontakti number</span><span class="sxs-lookup"><span data-stu-id="91a27-117">Contact number</span></span> | <span data-ttu-id="91a27-118">Tekst</span><span class="sxs-lookup"><span data-stu-id="91a27-118">Text</span></span> | <span data-ttu-id="91a27-119">Tellimusega seotud küsimuste jaoks saab kasutada kontaktnumbrit.</span><span class="sxs-lookup"><span data-stu-id="91a27-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="91a27-120">Moodulid, mida saab tellimuse üksikasjade lehel kasutada</span><span class="sxs-lookup"><span data-stu-id="91a27-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="91a27-121">Tellimuse üksikasjade lehe loomisel saate lisaks tellimuse üksikasjade moodulile lisada ka teisi asjakohaseid mooduleid.</span><span class="sxs-lookup"><span data-stu-id="91a27-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="91a27-122">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="91a27-122">Here are some examples:</span></span>

- <span data-ttu-id="91a27-123">**Soovituste moodul** – soovituste mooduli saab lisada tellimuse üksikasjade lehele, et soovitada kliendile muid tooteid.</span><span class="sxs-lookup"><span data-stu-id="91a27-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="91a27-124">**Turunduse moodulid** – mis tahes turunduse mooduli saab lisada tellimuse üksikasjade lehele, et kuvada turunduse sisu.</span><span class="sxs-lookup"><span data-stu-id="91a27-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="create-an-order-details-page-module"></a><span data-ttu-id="91a27-125">Tellimuse üksikasjade lehe mooduli loomine</span><span class="sxs-lookup"><span data-stu-id="91a27-125">Create an order details page module</span></span>

1. <span data-ttu-id="91a27-126">Looge lehe mall nimega **Tellimuse üksikasjade mall**.</span><span class="sxs-lookup"><span data-stu-id="91a27-126">Create a page template that is named **Order details template**.</span></span>
1. <span data-ttu-id="91a27-127">Lisage vaikimisi lehe pesasse **Peamine** tellimuse üksikasjade moodul.</span><span class="sxs-lookup"><span data-stu-id="91a27-127">In the **Main** slot of the default page, add an order details module.</span></span>
1. <span data-ttu-id="91a27-128">Lisage tellimuse üksikasjade moodulis soovituste moodul.</span><span class="sxs-lookup"><span data-stu-id="91a27-128">In the order details module, add a recommendations module.</span></span>
1. <span data-ttu-id="91a27-129">Malli salvestamine ja eelvaade.</span><span class="sxs-lookup"><span data-stu-id="91a27-129">Save and preview the template.</span></span> <span data-ttu-id="91a27-130">Tellimuse üksikasjade moodulit ei renderdata, kuna see nõuab tellimuse kinnituse numbri konteksti.</span><span class="sxs-lookup"><span data-stu-id="91a27-130">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="91a27-131">Viige lõpuni malli redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="91a27-131">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="91a27-132">Kasutage äsja loodud tellimuse üksikasjade malli, et luua leht, mille nimi on **Tellimuse üksikasjade leht**.</span><span class="sxs-lookup"><span data-stu-id="91a27-132">Use the order details template that you just created to create a page that is named **order details page**.</span></span>
1. <span data-ttu-id="91a27-133">Lisage lehekülje liigendusele vaikimisi lehekülg.</span><span class="sxs-lookup"><span data-stu-id="91a27-133">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="91a27-134">Lisage päise fragment pesasse **Päis**.</span><span class="sxs-lookup"><span data-stu-id="91a27-134">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="91a27-135">Lisage jaluse fragment pesasse **Jalus**.</span><span class="sxs-lookup"><span data-stu-id="91a27-135">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="91a27-136">Lisage tellimuse üksikasjade moodul pesasse **Peamine**.</span><span class="sxs-lookup"><span data-stu-id="91a27-136">In the **Main** slot, add an order details module.</span></span>
1. <span data-ttu-id="91a27-137">Tellimuse üksikasjade mooduli atribuutide paanil lisage pealkiri **Tellimuse üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="91a27-137">In the property pane for the order details module, add the heading **Order details**.</span></span>
1. <span data-ttu-id="91a27-138">Lisage tellimuse üksikasjade mooduli alla soovituste moodul ja konfigureerige see nii, et see kasutaks sätteid **Uus** ja **Enimmüüdud**.</span><span class="sxs-lookup"><span data-stu-id="91a27-138">Below the order details module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="91a27-139">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="91a27-139">Save and preview the page.</span></span>
1. <span data-ttu-id="91a27-140">Viige lõpuni lehe redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="91a27-140">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91a27-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="91a27-141">Additional resources</span></span>

[<span data-ttu-id="91a27-142">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="91a27-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="91a27-143">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="91a27-143">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="91a27-144">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="91a27-144">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="91a27-145">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="91a27-145">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="91a27-146">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="91a27-146">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="91a27-147">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="91a27-147">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="91a27-148">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="91a27-148">Footer module</span></span>](author-footer-module.md)
