---
title: Järeletulemisteabe moodul
description: See teema hõlmab järeletulemisteabe moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce maksmise lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-09021
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 222e8ad79b30e5197f7140958309d442b284f286
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5263176"
---
# <a name="pickup-information-module"></a><span data-ttu-id="32cb8-103">Järeletulemise teabe moodul</span><span class="sxs-lookup"><span data-stu-id="32cb8-103">Pickup information module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32cb8-104">See teema hõlmab järeletulemisteabe moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce maksmise lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="32cb8-104">This topic covers the pickup information module and describes how to add it to checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="32cb8-105">Järeletulemisteabe moodulit saab kasutada maksmise moodulis tellimusele järele tulemise teabe näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="32cb8-105">The pickup information module can be used in a checkout module to show order pickup information.</span></span> <span data-ttu-id="32cb8-106">Kliendid saavad vaadata saadaolevaid järeletulemiskuupäevi ja -aegu ning seejärel valida tellimusele järeletulemiseks sobiva aja.</span><span class="sxs-lookup"><span data-stu-id="32cb8-106">Customers can view available pickup dates and time slots, and then select a suitable time to pick up their order.</span></span> <span data-ttu-id="32cb8-107">Näiteks saab klient valida, et tuleb San Francisco poodi tellimusele järele 21. märtsil kell 15.00.</span><span class="sxs-lookup"><span data-stu-id="32cb8-107">For example, a customer can choose to pick up an order at 3 PM on March 21 from the San Francisco store.</span></span>

<span data-ttu-id="32cb8-108">Sobivate poodide järeletulemise ajavahemik peab olema konfigureeritud Commerce'i peakontoris.</span><span class="sxs-lookup"><span data-stu-id="32cb8-108">Pickup time slots for the appropriate stores must be configured in Commerce headquarters.</span></span> <span data-ttu-id="32cb8-109">Lisateavet vt teemast [Kliendi järeletulemise ajavahemike loomine ja värskendamine](dev-itpro/pickup-timeslots.md).</span><span class="sxs-lookup"><span data-stu-id="32cb8-109">For more information, see [Create and update time slots for customer pickup](dev-itpro/pickup-timeslots.md).</span></span>

<span data-ttu-id="32cb8-110">Kui järeletulemisteabe moodul luuakse maksmise lehel, kuid pealevõtmiseks valitud poele ei ole määratud ajavahemikke, näitab moodul teavet, kuid kasutaja ei saa valida ühtegi ajavahemikku.</span><span class="sxs-lookup"><span data-stu-id="32cb8-110">If a pickup information module is created on a checkout page, but no time slots are defined for the store that is selected for pickup, the module will show information, but the user won't be able to select any time slots.</span></span> <span data-ttu-id="32cb8-111">Ajavahemikud on valikulised ja neid ei nõuta tellimuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="32cb8-111">Time slots are optional and aren't required to place an order.</span></span>

<span data-ttu-id="32cb8-112">Kui mitmele kaubale tullakse järele mitmesse poodi, võimaldab järeletulemisteabe moodul kasutajal valida iga kaupluse jaoks ajavahemiku tingimusel, et selle jaoks on saadaval ajavahemikud.</span><span class="sxs-lookup"><span data-stu-id="32cb8-112">If multiple items are selected for pickup across multiple stores, the pickup information module will let the user select a time slot for each store, provided that time slots are available for it.</span></span>

> [!NOTE]
> <span data-ttu-id="32cb8-113">Ajavahemikue ja maksmisel järeletulemisteabe mooduli tugi on saadaval Dynamics 365 Commerce'i versioonis 10.0.15 ja uuemates versioonides.</span><span class="sxs-lookup"><span data-stu-id="32cb8-113">Support for time slots and the checkout pickup information module is available in Dynamics 365 Commerce version 10.0.15 and later.</span></span>

<span data-ttu-id="32cb8-114">Järgmisel joonisel on kujutatud ajavahemiku valiku näide maksmise lehel järeletulemisteabe mooduli kaudu.</span><span class="sxs-lookup"><span data-stu-id="32cb8-114">The following illustration shows an example of time slot selection through the pickup information module on a checkout page.</span></span>

![Järeletulemisteabe mooduli näide maksmise lehel](./dev-itpro/media/Curbside_timeslot_eCommerce.PNG)

## <a name="module-properties"></a><span data-ttu-id="32cb8-116">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="32cb8-116">Module properties</span></span>

- <span data-ttu-id="32cb8-117">**Pealkiri** – sisestage mooduli pealkiri.</span><span class="sxs-lookup"><span data-stu-id="32cb8-117">**Heading** – Enter a heading for the module.</span></span>

## <a name="show-time-slot-information-after-an-order-is-placed"></a><span data-ttu-id="32cb8-118">Ajavahemikuteabe kuvamine tellimuse esitamise järel</span><span class="sxs-lookup"><span data-stu-id="32cb8-118">Show time slot information after an order is placed</span></span>

<span data-ttu-id="32cb8-119">Pärast tellimuse esitamist saab valitud ajavahemiku teavet vaadata [tellimuse kinnitamise moodulis](order-confirmation-module.md) ja [tellimuse üksikasjade moodulis](account-management.md#order-details-page).</span><span class="sxs-lookup"><span data-stu-id="32cb8-119">After an order is placed, information about the selected time slot can be viewed in the [order confirmation module](order-confirmation-module.md) and the [order details module](account-management.md#order-details-page).</span></span> <span data-ttu-id="32cb8-120">Mõlemal moodulil on atribuut **Ajavahemiku teabe kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="32cb8-120">Both these modules have a **Show timeslot information** property.</span></span> <span data-ttu-id="32cb8-121">Enne valitud ajavahemiku kuvamist tellimise ajal peab selle atribuudi väärtuseks olema seatud **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="32cb8-121">Before they can show the selected time slot during the order process, this property must be set to **True**.</span></span>

## <a name="add-a-checkout-pickup-information-module-to-a-page"></a><span data-ttu-id="32cb8-122">Maksmise lehele järeletulemisteabe mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="32cb8-122">Add a checkout pickup information module to a page</span></span>

<span data-ttu-id="32cb8-123">Juhiste saamiseks järeletulemisteabe mooduli lisamiseks maksmise lehele ja nõutavate atribuutide määramiseks vt teemat [Maksmismoodul](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="32cb8-123">For instructions about how to add a pickup information module to a checkout page and set the required properties, see [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="32cb8-124">Järgmisel joonisel on kujutatud näide e-kaubanduse maksmise lehest, mis sisaldab reaüksuste jaoks järeletulemise ajavahemikke.</span><span class="sxs-lookup"><span data-stu-id="32cb8-124">The following illustration shows an example of an e-Commerce checkout page that includes time slots for pickup line items.</span></span>

![Näide e-kaubanduse maksmise lehest, mis sisaldab reaüksuste jaoks järeletulemise ajavahemikke](./dev-itpro/media/Curbside_timeslot_eCommerce_checkoutsummary.PNG)

## <a name="additional-resources"></a><span data-ttu-id="32cb8-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="32cb8-126">Additional resources</span></span>

[<span data-ttu-id="32cb8-127">Kliendi järeletulemise ajavahemike loomine ja värskendamine</span><span class="sxs-lookup"><span data-stu-id="32cb8-127">Create and update time slots for customer pickup</span></span>](dev-itpro/pickup-timeslots.md)

[<span data-ttu-id="32cb8-128">Maksmismoodul</span><span class="sxs-lookup"><span data-stu-id="32cb8-128">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="32cb8-129">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="32cb8-129">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="32cb8-130">Tellimuse üksikasjade moodul</span><span class="sxs-lookup"><span data-stu-id="32cb8-130">Order details module</span></span>](account-management.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]