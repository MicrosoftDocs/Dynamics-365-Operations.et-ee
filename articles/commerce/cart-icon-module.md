---
title: Ostukorvi ikooni moodul
description: See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ebc5cfa490a4c8538fd081aced0844ed01d63a26
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/07/2020
ms.locfileid: "4411833"
---
# <a name="cart-icon-module"></a><span data-ttu-id="38153-103">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="38153-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="38153-104">See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="38153-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="38153-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="38153-105">Overview</span></span>

<span data-ttu-id="38153-106">Ostukorvi ikooni moodul tähistab ostukorvi lehe päisemoodulis ja kuvab ostukorvis olevate kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="38153-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="38153-107">Ostukorvi ikooni moodul kuvab ka ostukorvi kokkuvõtte (tuntud ka kui väike ostukorv), kui hiirt hõljutatakse üle ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="38153-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="38153-108">Väike ostukorv esitab kasutajale kokkuvõtte ostukorvis olevatest kaupadest, ilma et peaksite liikuma ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="38153-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="38153-109">Lisaks võimaldab see kasutajal ka otse kassa lehele minna, kui nad on kokkuvõttega rahul.</span><span class="sxs-lookup"><span data-stu-id="38153-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="38153-110">See vähendab lehekülgede vahel liikumiste arvu ja teeb väljaregistreerimise kiiremaks.</span><span class="sxs-lookup"><span data-stu-id="38153-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

> [!NOTE]
> <span data-ttu-id="38153-111">Ostukorvi ikooni mooduli tugi on saadaval väljalaskes Dynamics 365 Commerce 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="38153-111">Support for the cart icon module is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>

<span data-ttu-id="38153-112">Järgmisel pildil on kuvatud näide ostukorvi ikooni moodulist, kus on kuvatud Fabrikami päises miniostukorv.</span><span class="sxs-lookup"><span data-stu-id="38153-112">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Ostukorvi ikooni mooduli näide](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="38153-114">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="38153-114">Module properties</span></span>

- <span data-ttu-id="38153-115">**Kuva väike ostukorv** – kui on tõene, võimaldab see atribuut kuvada ostukorvi kokkuvõtte (väikese ostukorvi) hiire hõljutamisel ostukorvi ikooni kohal.</span><span class="sxs-lookup"><span data-stu-id="38153-115">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="38153-116">Seda funktsiooni toetatakse ainult töölaua vaateportide korral.</span><span class="sxs-lookup"><span data-stu-id="38153-116">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="38153-117">Lehele ostukorvi ikooni mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="38153-117">Add a cart icon module to a page</span></span>

<span data-ttu-id="38153-118">Ostukorvi ikooni mooduli lisamiseks vaadake teemat [Päise moodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="38153-118">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38153-119">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="38153-119">Additional resources</span></span>

[<span data-ttu-id="38153-120">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="38153-120">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="38153-121">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="38153-121">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="38153-122">Makse moodul</span><span class="sxs-lookup"><span data-stu-id="38153-122">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="38153-123">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="38153-123">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="38153-124">Tarnesuvandite moodul</span><span class="sxs-lookup"><span data-stu-id="38153-124">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="38153-125">Järeletulemisteabe moodul</span><span class="sxs-lookup"><span data-stu-id="38153-125">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="38153-126">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="38153-126">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="38153-127">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="38153-127">Gift card module</span></span>](add-giftcard.md)
