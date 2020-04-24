---
title: Ostukorvi ikooni moodul
description: See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: 8cc96e0476a9d8a46aed7011359dc65fbc678fbf
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261562"
---
# <a name="cart-icon-module"></a><span data-ttu-id="87034-103">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="87034-103">Cart icon module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="87034-104">See teema hõlmab ostukorvi ikooni moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="87034-104">This topic covers the cart icon module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="87034-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="87034-105">Overview</span></span>

<span data-ttu-id="87034-106">Ostukorvi ikooni moodul tähistab ostukorvi lehe päisemoodulis ja kuvab ostukorvis olevate kaupade arvu.</span><span class="sxs-lookup"><span data-stu-id="87034-106">The cart icon module represents the cart in the header module of the page, and shows the number of items in the cart.</span></span> <span data-ttu-id="87034-107">Ostukorvi ikooni moodul kuvab ka ostukorvi kokkuvõtte (tuntud ka kui väike ostukorv), kui hiirt hõljutatakse üle ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="87034-107">The cart icon module also displays a cart summary (also known as a mini cart) when the cart icon is hovered over.</span></span> <span data-ttu-id="87034-108">Väike ostukorv esitab kasutajale kokkuvõtte ostukorvis olevatest kaupadest, ilma et peaksite liikuma ostukorvi lehele.</span><span class="sxs-lookup"><span data-stu-id="87034-108">The mini cart provides the user with a summary of the items in the cart without having to navigate to the cart page.</span></span> <span data-ttu-id="87034-109">Lisaks võimaldab see kasutajal ka otse kassa lehele minna, kui nad on kokkuvõttega rahul.</span><span class="sxs-lookup"><span data-stu-id="87034-109">In addition, it also allows the user to directly go to checkout page if they are happy with the summary.</span></span> <span data-ttu-id="87034-110">See vähendab lehekülgede vahel liikumiste arvu ja teeb väljaregistreerimise kiiremaks.</span><span class="sxs-lookup"><span data-stu-id="87034-110">This reduces the number of page navigations and makes checkout faster.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="87034-111">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="87034-111">Module properties</span></span>

- <span data-ttu-id="87034-112">**Kuva väike ostukorv** – kui on tõene, võimaldab see atribuut kuvada ostukorvi kokkuvõtte (väikese ostukorvi) hiire hõljutamisel ostukorvi ikooni kohal.</span><span class="sxs-lookup"><span data-stu-id="87034-112">**Show mini cart** – When true, this property enables a cart summary (mini cart) to be displayed when the cart icon is hovered over.</span></span> <span data-ttu-id="87034-113">Seda funktsiooni toetatakse ainult töölaua vaateportide korral.</span><span class="sxs-lookup"><span data-stu-id="87034-113">This functionality is only supported for desktop view ports.</span></span>


## <a name="add-a-cart-icon-module-to-a-page"></a><span data-ttu-id="87034-114">Lehele ostukorvi ikooni mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="87034-114">Add a cart icon module to a page</span></span>

<span data-ttu-id="87034-115">Ostukorvi ikooni mooduli lisamiseks vaadake teemat [Päise moodul](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="87034-115">To add a cart icon module, see [Header module](author-header-module.md).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="87034-116">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="87034-116">Additional resources</span></span>

[<span data-ttu-id="87034-117">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="87034-117">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="87034-118">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="87034-118">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="87034-119">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="87034-119">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="87034-120">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="87034-120">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="87034-121">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="87034-121">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="87034-122">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="87034-122">Footer module</span></span>](author-footer-module.md)
