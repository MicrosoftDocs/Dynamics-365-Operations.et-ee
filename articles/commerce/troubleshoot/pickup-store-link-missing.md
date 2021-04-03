---
title: Järeleminemise valikut ei kuvata ostukorvi või toote üksikasjade lehtedel
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluses oleva kauba saatmisvalikut ei kuvata ostukorvi leheküljel või toote üksikasjade lehtedel.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585282"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a><span data-ttu-id="4a3a7-103">"Järeleminemise" valikut ei kuvata ostukorvi või toote üksikasjade lehtedel</span><span class="sxs-lookup"><span data-stu-id="4a3a7-103">"Pick this up" option doesn't appear on cart or product details pages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4a3a7-104">See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluses oleva kauba saatmisvalikut ei kuvata ostukorvi leheküljel või toote üksikasjade lehtedel.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-104">This topic provides troubleshooting guidance that can help when the option for in-store pickup doesn't appear on the cart page or product details pages.</span></span>

## <a name="description"></a><span data-ttu-id="4a3a7-105">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4a3a7-105">Description</span></span>

<span data-ttu-id="4a3a7-106">**Järeleminemise** nuppu ei kuvata ostukorvi või toote üksikasjade lehtedel.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-106">The **Pick this up** button doesn't appear on the cart page or product details pages.</span></span>

<span data-ttu-id="4a3a7-107">Järgmine illustratsioon näitab näidet lehekülje kohta, mis sisaldab **Järeleminemise** nuppu.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-107">The following illustration shows an example of a page that includes the **Pick this up** button.</span></span>

![Järeleminemise nupp](media/pickup-button-missing.jpg)

## <a name="resolution"></a><span data-ttu-id="4a3a7-109">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="4a3a7-109">Resolution</span></span>

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a><span data-ttu-id="4a3a7-110">BOPIS-i laiendi lubamine Commerce'i saidi koostajas</span><span class="sxs-lookup"><span data-stu-id="4a3a7-110">Enable the BOPIS extension in Commerce site builder</span></span>

<span data-ttu-id="4a3a7-111">Commerce'i saidi koostajas "võrgus ostmise" lubamiseks, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-111">To enable the "buy online, pick up in store" (BOPIS) extension in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4a3a7-112">Valige sait.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-112">Select your site.</span></span>
1. <span data-ttu-id="4a3a7-113">Valige **Saidi sätted** ja seejärel valige suvand **Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-113">Select **Site settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="4a3a7-114">Veenduge, et **Keela BOPIS** valik on tühi.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-114">Make sure that the **Disable BOPIS** option is cleared.</span></span>

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a><span data-ttu-id="4a3a7-115">Tarneviiside konfigureerimine Commerce Headquarters\`is</span><span class="sxs-lookup"><span data-stu-id="4a3a7-115">Configure modes of delivery in Commerce headquarters</span></span>

<span data-ttu-id="4a3a7-116">Commerce headquarters\`is kannete redigeerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-116">To configure modes of delivery in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4a3a7-117">Minge jaotisse **Ostmine ja hankimine \> Seadistamine \> Tarneviis**.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-117">Go to **Procurement and sourcing \> Setup \> Modes of delivery**.</span></span>
1. <span data-ttu-id="4a3a7-118">Veenduge, et **kliendi järeletulek** tarneviisina on loodud ja tooted ja aadressid on määratud.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-118">Make sure that a **Customer pickup** mode of delivery has been created, and that products and addresses are assigned to it.</span></span>
1. <span data-ttu-id="4a3a7-119">Valige suvandid **Jaemüük ja kaubandus \> Headquartersi seadistamine \> Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-119">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="4a3a7-120">Valige vasakpoolsel navigeerimispaanil suvand **Kliendi tellimused**.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-120">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="4a3a7-121">Veenduge, et **Järeleminemise tarneviis** on õigesti konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-121">Make sure that **Pickup mode of delivery** is correctly configured.</span></span>

### <a name="configure-customer-orders-payments"></a><span data-ttu-id="4a3a7-122">Klienditellimuste maksete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4a3a7-122">Configure customer orders payments</span></span>

<span data-ttu-id="4a3a7-123">Commerce headquarters\`is kannete redigeerimiseks toimige järgmiste sammudega.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-123">To configure customer orders payments in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="4a3a7-124">Valige suvandid **Jaemüük ja kaubandus \> Headquartersi seadistamine \> Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-124">Go to **Retail and Commerce \> Headquarters setup \> Parameters**.</span></span>
1. <span data-ttu-id="4a3a7-125">Valige vasakpoolsel navigeerimispaanil suvand **Kliendi tellimused**.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-125">In the left navigation, select **Customer orders**.</span></span>
1. <span data-ttu-id="4a3a7-126">Veenduge, et **Maksed** kiirkaardil on **Maksetingimused** ja **Makseviisi** väljad on õigesti seatud.</span><span class="sxs-lookup"><span data-stu-id="4a3a7-126">On the **Payments** FastTab, make sure that the **Terms of payment** and **Method of payment** fields are correctly set.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a3a7-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4a3a7-127">Additional resources</span></span>

[<span data-ttu-id="4a3a7-128">BOPIS-i konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="4a3a7-128">Configure BOPIS</span></span>](../cpe-bopis.md)

[<span data-ttu-id="4a3a7-129">Klienditellimuste korral mitme järeletulemisega tarneviisi lubamine</span><span class="sxs-lookup"><span data-stu-id="4a3a7-129">Enable multiple pickup delivery modes for customer orders</span></span>](../multiple-pickup-modes.md)

[<span data-ttu-id="4a3a7-130">Omnikanali Commerce'i tellimuste maksed</span><span class="sxs-lookup"><span data-stu-id="4a3a7-130">Omni-channel Commerce order payments</span></span>](../dev-itpro/commerce-payments.md)

[<span data-ttu-id="4a3a7-131">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="4a3a7-131">Store selector module</span></span>](../store-selector.md)
