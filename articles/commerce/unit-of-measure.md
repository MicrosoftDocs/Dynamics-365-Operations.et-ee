---
title: Rakenda mõõtühiku sätted
description: See teema hõlmab mõõtühikute sätteid ja kirjeldab, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce rakendada.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d338ba207c9a101f5e224ca66555b16a457bcbc
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6271397"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="e3efd-103">Rakenda mõõtühiku sätted</span><span class="sxs-lookup"><span data-stu-id="e3efd-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e3efd-104">See teema hõlmab mõõtühikute sätteid ja kirjeldab, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce rakendada.</span><span class="sxs-lookup"><span data-stu-id="e3efd-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e3efd-105">Toodet saab müüa erinevates üksustes, näiteks "igaüks", "paar" ja "tosin."</span><span class="sxs-lookup"><span data-stu-id="e3efd-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="e3efd-106">Commerce peakorteris saab müügi mõõtühiku määrata tootele ja näidata e-kaubanduse saidil.</span><span class="sxs-lookup"><span data-stu-id="e3efd-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="e3efd-107">Näiteks kui jaemüüja müüb toodet nii eraldi kui ka kümnete kaupa, saab saadaolevaid mõõtühikuid näidata koos muu tooteteabega.</span><span class="sxs-lookup"><span data-stu-id="e3efd-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="e3efd-108">Järgmise illustratsiooni näites on üksuse mõõtühik **ea** (iga) Commerce peakorteri toote jaoks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="e3efd-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Näide tootest, mis on konfigureeritud mõõtühikuga Commerce peakorteris](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="e3efd-110">Mõõtühiku rakendamise ja näitamise tugi on saadaval Commerce versioonis 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="e3efd-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="e3efd-111">Mõõtühiku sätted</span><span class="sxs-lookup"><span data-stu-id="e3efd-111">Unit of measure settings</span></span>

<span data-ttu-id="e3efd-112">Mõõtühiku kuvasätted määratakse Commerce saidi koostajas jaotises **Saidisätted \> Laiendid \> Kuva toodete mõõtühik**.</span><span class="sxs-lookup"><span data-stu-id="e3efd-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="e3efd-113">Toetatud sätteid on kolm:</span><span class="sxs-lookup"><span data-stu-id="e3efd-113">There are three supported settings:</span></span>

- <span data-ttu-id="e3efd-114">**Ära kuva** – Kui see säte on valitud, ei näita e-kaubanduse sait toote mõõtühikuid.</span><span class="sxs-lookup"><span data-stu-id="e3efd-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="e3efd-115">See on vaikesäte.</span><span class="sxs-lookup"><span data-stu-id="e3efd-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="e3efd-116">**Kuva toote ostukogemuses** – Kui see säte on valitud, kuvatakse mõõtühik toote üksikasjades, ostukorvis, tellimuse kinnituses, tellimuste ajaloos ja tellimuse üksikasjade lehtedel.</span><span class="sxs-lookup"><span data-stu-id="e3efd-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="e3efd-117">**Kuvage toote sirvimise ja ostukogemuse ajal** – Kui see säte on valitud, näidatakse mõõtühikuid toote ostukogemuse lehtedel ja ka toote sirvimise ajal.</span><span class="sxs-lookup"><span data-stu-id="e3efd-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="e3efd-118">Osana sellest käitumisest näidatakse mõõtühikuid otsingutulemustes ja tootekogumi moodulites.</span><span class="sxs-lookup"><span data-stu-id="e3efd-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e3efd-119">Mõõtühiku kuvasätted on saadaval Commerce versioonis 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="e3efd-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="e3efd-120">Kui uuendate rakenduse Commerce'i varasemat versiooni, peate faili appsettings.json käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="e3efd-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="e3efd-121">Juhiste saamiseks vt [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="e3efd-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="e3efd-122">Mõõtühiku sätteid kasutavad moodulid</span><span class="sxs-lookup"><span data-stu-id="e3efd-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="e3efd-123">Mõõtühiku sätteid kasutavad moodulid hõlmavad ostuboksi, soovinimekirja, ostukorvi, ostukorvi ikooni, otsingutulemuste konteinerit, tootekogumit, tellimuse kinnitust ja tellimuse üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e3efd-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="e3efd-124">Järgmises näites on toote üksikasjade lehel (PDP) kuvatud toote mõõtühik (**ea**).</span><span class="sxs-lookup"><span data-stu-id="e3efd-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Mõõtühikuid näitava PDP näide](./media/Productunit-PDP.png)

<span data-ttu-id="e3efd-126">Järgmise illustratsiooni näites näitab tootekogumismoodul toote mõõtühikut (**ea**).</span><span class="sxs-lookup"><span data-stu-id="e3efd-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Mõõtühikuid näitava tootekogumi mooduli näide](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="e3efd-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e3efd-128">Additional resources</span></span>

[<span data-ttu-id="e3efd-129">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="e3efd-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e3efd-130">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="e3efd-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e3efd-131">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="e3efd-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e3efd-132">Kontohalduse lehed ja moodulid</span><span class="sxs-lookup"><span data-stu-id="e3efd-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="e3efd-133">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="e3efd-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
