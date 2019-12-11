---
title: Tellimuse kinnituse moodul
description: See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: e339ce02bb646d0d9a68c22b24fde9b72071de6f
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698322"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="5715c-103">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="5715c-103">Order confirmation module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5715c-104">See teema hõlmab tellimuse kinnitamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce luua.</span><span class="sxs-lookup"><span data-stu-id="5715c-104">This topic covers order confirmation modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5715c-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="5715c-105">Overview</span></span>

<span data-ttu-id="5715c-106">Tellimuse kinnituse moodulit kasutatakse kinnitusteate kuvamiseks tellimuse kinnitamise lehel pärast tellimuse esitamist.</span><span class="sxs-lookup"><span data-stu-id="5715c-106">An order confirmation module is used to show a confirmation message on an order confirmation page after an order is placed.</span></span> <span data-ttu-id="5715c-107">Tellimuse kinnituse moodul näitab tellimuse kinnituse numbrit ja kliendi meiliaadressi, mis esitati maksmise ajal.</span><span class="sxs-lookup"><span data-stu-id="5715c-107">The order confirmation module shows the order confirmation number and the customer email address that was provided during checkout.</span></span>

<span data-ttu-id="5715c-108">Kui tellimus esitatakse maksmise ajal, edastatakse tellimuse kinnituse number ja kliendi meiliaadress tellimuse kinnitamise lehe URL-i päringu stringina.</span><span class="sxs-lookup"><span data-stu-id="5715c-108">When an order is placed during checkout, the order confirmation number and customer email address are passed to the order confirmation page as a query string in the page's URL.</span></span> <span data-ttu-id="5715c-109">Tellimuse kinnituse moodul võtab selle teabe vastu ja muudab tellimuse oleku tellimuse kinnitamise lehele.</span><span class="sxs-lookup"><span data-stu-id="5715c-109">The order confirmation module receives this information and renders the order status on the order confirmation page.</span></span> <span data-ttu-id="5715c-110">Tellimuse kinnituse moodul nõuab tellimuse oleku esitamiseks lehe konteksti.</span><span class="sxs-lookup"><span data-stu-id="5715c-110">The order confirmation module requires this page context to provide the status of the order.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="5715c-111">Tellimuse kinnituse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="5715c-111">Order confirmation module properties</span></span>

| <span data-ttu-id="5715c-112">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="5715c-112">Property name</span></span> | <span data-ttu-id="5715c-113">Väärtused</span><span class="sxs-lookup"><span data-stu-id="5715c-113">Values</span></span> | <span data-ttu-id="5715c-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5715c-114">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="5715c-115">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="5715c-115">Heading</span></span>       | <span data-ttu-id="5715c-116">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="5715c-116">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="5715c-117">Tellimuse kinnituse moodulil võib olla pealkiri.</span><span class="sxs-lookup"><span data-stu-id="5715c-117">The order confirmation module can have a heading.</span></span> <span data-ttu-id="5715c-118">Vaikimisi kasutatakse pealkirja jaks pealkirja silti **H2**.</span><span class="sxs-lookup"><span data-stu-id="5715c-118">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="5715c-119">Samas saab silti muuta, et see vastaks juurdepääsetavuse nõuetele.</span><span class="sxs-lookup"><span data-stu-id="5715c-119">However, the tag can be changed to meet accessibility requirements.</span></span> |

## <a name="modules-that-can-be-used-in-an-order-confirmation-page-module"></a><span data-ttu-id="5715c-120">Moodulid, mida saab kasutada tellimuse kinnitamise lehe moodulis</span><span class="sxs-lookup"><span data-stu-id="5715c-120">Modules that can be used in an order confirmation page module</span></span> 

- <span data-ttu-id="5715c-121">**Soovitused** – soovituste mooduli saab panna tellimuse kinnitamise lehele, et soovitada kliendile muid tooteid.</span><span class="sxs-lookup"><span data-stu-id="5715c-121">**Recommendations** – The recommendations module can be put on the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="5715c-122">**Turundus** – turunduse moodul saab lisada turunduse sisu tellimuse kinnitamise lehele.</span><span class="sxs-lookup"><span data-stu-id="5715c-122">**Marketing** – The marketing module can add marketing content to the order confirmation page.</span></span>

## <a name="create-an-order-confirmation-page-module"></a><span data-ttu-id="5715c-123">Tellimuse kinnitamise lehe mooduli loomine</span><span class="sxs-lookup"><span data-stu-id="5715c-123">Create an order confirmation page module</span></span>

1. <span data-ttu-id="5715c-124">Looge lehe mall nimega **tellimuse kinnituse mall**.</span><span class="sxs-lookup"><span data-stu-id="5715c-124">Create a page template that is named **order confirmation template**.</span></span>
1. <span data-ttu-id="5715c-125">Lisage vaikimisi lehe pesasse **Peamine** tellimuse kinnituse moodul.</span><span class="sxs-lookup"><span data-stu-id="5715c-125">In the **Main** slot of the default page, add an order confirmation module.</span></span>
1. <span data-ttu-id="5715c-126">Tellimuse kinnituse moodulis lisage soovituste moodul.</span><span class="sxs-lookup"><span data-stu-id="5715c-126">In the order confirmation module, add a recommendations module.</span></span>
1. <span data-ttu-id="5715c-127">Malli salvestamine ja eelvaade.</span><span class="sxs-lookup"><span data-stu-id="5715c-127">Save and preview the template.</span></span> <span data-ttu-id="5715c-128">Tellimuse kinnituse moodulit ei tohi renderdada, kuna see nõuab tellimuse kinnituse numbri konteksti.</span><span class="sxs-lookup"><span data-stu-id="5715c-128">The order confirmation module should not be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="5715c-129">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="5715c-129">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="5715c-130">Kasutage äsja loodud tellimuse kinnituse malli, et luua leht, mille nimi on **tellimuse kinnituse leht**.</span><span class="sxs-lookup"><span data-stu-id="5715c-130">Use the order confirmation template that you just created to create a page that is named **order confirmation page**.</span></span>
1. <span data-ttu-id="5715c-131">Lisage lehekülje liigendusele vaikimisi lehekülg.</span><span class="sxs-lookup"><span data-stu-id="5715c-131">Add the default page to the page outline.</span></span>
1. <span data-ttu-id="5715c-132">Lisage päise fragment pesasse **Päis**.</span><span class="sxs-lookup"><span data-stu-id="5715c-132">In the **Header** slot, add a header fragment.</span></span>
1. <span data-ttu-id="5715c-133">Lisage jaluse fragment pesasse **Jalus**.</span><span class="sxs-lookup"><span data-stu-id="5715c-133">In the **Footer** slot, add a footer fragment.</span></span>
1. <span data-ttu-id="5715c-134">Lisage tellimuse kinnituse moodul pesasse **Peamine**.</span><span class="sxs-lookup"><span data-stu-id="5715c-134">In the **Main** slot, add an order confirmation module.</span></span>
1. <span data-ttu-id="5715c-135">Tellimuse kinnituse mooduli atribuutide paanil lisage pealkiri **Tellimuse kinnitus**.</span><span class="sxs-lookup"><span data-stu-id="5715c-135">In the property pane of the order confirmation module, add the heading **Order confirmation**.</span></span>
1. <span data-ttu-id="5715c-136">Tellimuse kinnituse mooduli alla lisage soovituste moodul ja konfigureerige see nii, et see kasutaks sätteid **Uus** ja **Enimmüüdud**.</span><span class="sxs-lookup"><span data-stu-id="5715c-136">Below the order confirmation module, add a recommendations module, and configure it so that it uses the **New** and **Best Selling** settings.</span></span>
1. <span data-ttu-id="5715c-137">Salvestage ja eelvaadake lehte, registreerige ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="5715c-137">Save and preview the page, check it in, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5715c-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5715c-138">Additional resources</span></span>

[<span data-ttu-id="5715c-139">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="5715c-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5715c-140">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="5715c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5715c-141">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="5715c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5715c-142">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="5715c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5715c-143">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="5715c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5715c-144">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="5715c-144">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5715c-145">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="5715c-145">Footer module</span></span>](author-footer-module.md)
