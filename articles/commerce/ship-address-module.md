---
title: Tarneaadressi moodul
description: See teema hõlmab tarneaadressi moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 380d268ec0ba64367f090c31408eac1c54d0ff17
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661437"
---
# <a name="shipping-address-module"></a><span data-ttu-id="bc5ba-103">Tarneaadressi moodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="bc5ba-104">See teema käsitleb tarneaadressi moodulit ja seletab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bc5ba-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="bc5ba-105">Overview</span></span>

<span data-ttu-id="bc5ba-106">Tarneaadressi moodul võimaldab klientidel maksmise voo ajal lisada või valida tellimuse tarneaadressi.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="bc5ba-107">Kui klient on sisse logitud, kuvatakse aadressid, mis selle kliendi jaoks eelmisel korral salvestati, ja klient saab teha nende seast valiku.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="bc5ba-108">Klient saab lisada ka uue aadressi.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-108">The customer can also add a new address.</span></span> <span data-ttu-id="bc5ba-109">Tarneaadressi moodulit kasutatakse kõigi kaupade puhul, mis nõuavad tarnet.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="bc5ba-110">Tarneaadressi vorminguid saab määratleda Commerce'i peakontoris iga riigi või regiooni jaoks ning tarneaadressi moodul täidab seejärel riigi-/regioonipõhiseid reegleid.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="bc5ba-111">Kui kliendid sisestavad tarneaadressi maksmise voos, on neil võimalus salvestada aadress esmase aadressina.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="bc5ba-112">See valik kuvatakse ainult siis, kui klient on sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="bc5ba-113">Kuigi tarneaadressi moodul ei paku aadressi kinnitamist, saab seda funktsiooni rakendada kohandamise kaudu.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="bc5ba-114">Järgmisel pildil on näide uuest tarneaadressi moodulist maksmise lehel.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Tarneaadressi mooduli näide maksmise lehel](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="bc5ba-116">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="bc5ba-116">Module properties</span></span>

| <span data-ttu-id="bc5ba-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="bc5ba-117">Property name</span></span> | <span data-ttu-id="bc5ba-118">Väärtused</span><span class="sxs-lookup"><span data-stu-id="bc5ba-118">Values</span></span> | <span data-ttu-id="bc5ba-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bc5ba-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="bc5ba-120">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="bc5ba-120">Heading</span></span> | <span data-ttu-id="bc5ba-121">Pealkirja tekst ja pealkirja silt (**H1**, **H2**, **H3**, **H4**, **H5** või **H6**)</span><span class="sxs-lookup"><span data-stu-id="bc5ba-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="bc5ba-122">Tarneaadressi mooduli valikuline pealkiri.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="bc5ba-123">Kuva aadressi tüüp</span><span class="sxs-lookup"><span data-stu-id="bc5ba-123">Show address type</span></span> | <span data-ttu-id="bc5ba-124">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="bc5ba-124">**True** or **False**</span></span> | <span data-ttu-id="bc5ba-125">Kui selle valikulise atribuudi väärtuseks on seatud **Tõene**, kuvatakse aadressi tüüp, nt **Kodu** või **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="bc5ba-126">Kui aadressi tüüpi pole määratud, salvestatakse aadress automaatselt nii, et selle **Tüüp**=**Muu**.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="bc5ba-127">Maksmise lehele tarneaadressi mooduli lisamine ja vajalike atribuutide seadistamine</span><span class="sxs-lookup"><span data-stu-id="bc5ba-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="bc5ba-128">Tarneaadressi moodulit saab lisada ainult maksmise moodulisse.</span><span class="sxs-lookup"><span data-stu-id="bc5ba-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="bc5ba-129">Lisateavet selle kohta, kuidas konfigureerida tarneaadressi moodulit ja lisada seda maksmise lehele, leiate teemast [Maksmise moodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="bc5ba-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bc5ba-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bc5ba-130">Additional resources</span></span>

[<span data-ttu-id="bc5ba-131">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bc5ba-132">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bc5ba-133">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bc5ba-134">Maksemoodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="bc5ba-135">Tarnevalikute moodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="bc5ba-136">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-136">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bc5ba-137">Kinkekaardi moodul</span><span class="sxs-lookup"><span data-stu-id="bc5ba-137">Gift card module</span></span>](add-giftcard.md)
