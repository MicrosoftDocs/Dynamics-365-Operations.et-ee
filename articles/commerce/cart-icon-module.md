---
title: Ostukorvi ikooni moodul
description: See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 137debe3f4cad3948d20b2902ea80e66fa74ffd4
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661143"
---
# <a name="cart-icon-module"></a><span data-ttu-id="97890-103">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="97890-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="97890-104">See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="97890-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97890-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="97890-105">Overview</span></span>

<span data-ttu-id="97890-106">Ostukorvi ikooni moodul tähistab ostukorvi lehe päisemoodulis ja kuvab ostukorvis olevate kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="97890-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="97890-107">Ostukorvi ikooni moodul kuvab ka ostukorvi kokkuvõtte (tuntud ka kui väike ostukorv), kui hiirt hõljutatakse üle ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="97890-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="97890-108">Väike ostukorv esitab kasutajale kokkuvõtte ostukorvis olevatest kaupadest, ilma et peaksite liikuma ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="97890-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="97890-109">Lisaks võimaldab see kasutajal ka otse kassa lehele minna, kui nad on kokkuvõttega rahul.</span><span class="sxs-lookup"><span data-stu-id="97890-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="97890-110">See vähendab lehekülgede vahel liikumiste arvu ja teeb väljaregistreerimise kiiremaks.</span><span class="sxs-lookup"><span data-stu-id="97890-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

<span data-ttu-id="97890-111">Järgmisel pildil on kuvatud näide ostukorvi ikooni moodulist, kus on kuvatud Fabrikami päises miniostukorv.</span><span class="sxs-lookup"><span data-stu-id="97890-111">The following image shows an example of a cart icon module that displays a mini cart in the Fabrikam header.</span></span>

![Ostukorvi ikooni mooduli näide](./media/ecommerce-Minicart.PNG)

## <a name="module-properties"></a><span data-ttu-id="97890-113">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="97890-113">Module properties</span></span>

- <span data-ttu-id="97890-114">**Kuva väike ostukorv** – kui on tõene, võimaldab see atribuut kuvada ostukorvi kokkuvõtte (väikese ostukorvi) hiire hõljutamisel ostukorvi ikooni kohal.</span><span class="sxs-lookup"><span data-stu-id="97890-114">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="97890-115">Seda funktsiooni toetatakse ainult töölaua vaateportide korral.</span><span class="sxs-lookup"><span data-stu-id="97890-115">This functionality is only supported for desktop view ports.</span></span>

## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="97890-116">Lehele ostukorvi ikooni mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="97890-116">Add a cart icon module to a page</span></span>

<span data-ttu-id="97890-117">Ostukorvi ikooni mooduli lisamiseks vaadake teemat [Päise moodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="97890-117">To add a cart icon module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97890-118">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="97890-118">Additional resources</span></span>

[<span data-ttu-id="97890-119">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="97890-119">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="97890-120">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="97890-120">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="97890-121">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="97890-121">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="97890-122">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="97890-122">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="97890-123">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="97890-123">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="97890-124">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="97890-124">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="97890-125">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="97890-125">Gift card module</span></span>](add-giftcard.md)
