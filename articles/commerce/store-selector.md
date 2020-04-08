---
title: Kaupluse valija moodul
description: See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157336"
---
# <a name="store-selector-module"></a><span data-ttu-id="5390b-103">Kaupluse valija moodul</span><span class="sxs-lookup"><span data-stu-id="5390b-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5390b-104">See teema hõlmab kaupluse valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="5390b-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5390b-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="5390b-105">Overview</span></span>

<span data-ttu-id="5390b-106">Kaupluse valija moodulit kasutatakse kliendistsenaariumi „osta veebis, käi poes järel” (BOPIS) korral.</span><span class="sxs-lookup"><span data-stu-id="5390b-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="5390b-107">Seal kuvatakse kaupluste loend, kus toode on järele minemiseks saadaval ja ka iga kaupluse lahtiolekuajad ning toote varud.</span><span class="sxs-lookup"><span data-stu-id="5390b-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="5390b-108">Kaupluse valija moodul nõuab kaupluste otsimiseks toote konteksti ja otsingu asukohta.</span><span class="sxs-lookup"><span data-stu-id="5390b-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="5390b-109">Otsingu asukoha puudumise korral on see vaikimisi kliendi brauseri asukoht, kui klient on selleks nõusoleku andnud.</span><span class="sxs-lookup"><span data-stu-id="5390b-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="5390b-110">Moodulil on sisendkast, mis võimaldab kliendil sisestada läheduses asuvate kaupluste leidmiseks asukohta (sihtnumber, linn ja osariik).</span><span class="sxs-lookup"><span data-stu-id="5390b-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="5390b-111">Kaupluse valija moodul on integreeritud Bingi kaartide geokodeerimise rakenduse programmeerimisliidesega (API) asukoha laius- ja pikkuskraadideks teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="5390b-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="5390b-112">Vajalik on Bingi kaartide API võti ja see tuleb lisada Commerce'i jagatud parameetrite lehele rakenduses Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5390b-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5390b-113">Kaupluse valija moodulit saab lisada toote üksikasjade lehe (PDP) ostukasti moodulisse, et kuvada kauplusi, kus toode on järele tulemiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="5390b-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="5390b-114">Seda saab lisada ka ostukorvi moodulisse.</span><span class="sxs-lookup"><span data-stu-id="5390b-114">It can also be added to a cart module.</span></span> <span data-ttu-id="5390b-115">Ostukorvi moodulisse lisamisel kuvab kaupluse valija moodul iga ostukorvi rea kauba kohta järele minemise valikud.</span><span class="sxs-lookup"><span data-stu-id="5390b-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="5390b-116">Lisaks saab seda moodulit kohandatud kodeerimise abil lisada teistele lehtedele või moodulitele laienduste ja kohanduste kaudu.</span><span class="sxs-lookup"><span data-stu-id="5390b-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="5390b-117">Selleks, et BOPIS-stsenaarium töötaks, tuleb toodete tarneviisiks konfigureerida „kliendi järele minemine”.</span><span class="sxs-lookup"><span data-stu-id="5390b-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="5390b-118">Vastasel juhul ei kuvata moodulit vastavatel lehtedel.</span><span class="sxs-lookup"><span data-stu-id="5390b-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="5390b-119">Lisateavet tarneviisi konfigureerimise kohta vaadake teemast [Tarneviiside häälestamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="5390b-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="5390b-120">Järgmisel pildil on näide, kuidas kasutatakse kaupluse valija moodulit PDP-s.</span><span class="sxs-lookup"><span data-stu-id="5390b-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Kaupluse valija mooduli näide](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="5390b-122">Kaupluse valija mooduli kasutamine e-kaubanduses</span><span class="sxs-lookup"><span data-stu-id="5390b-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="5390b-123">Kaupluse valija moodulit saab kasutada toote üksikasjade lehel (PDP), et leida lähedal asuvaid kauplusi, kus toode on järele tulemiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="5390b-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="5390b-124">Kaupluse valija moodulit saab kasutada ostukorvi lehel, et leida lähedal asuvaid kauplusi, kus ostukorvis olev toode on järele tulemiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="5390b-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="5390b-125">Kaupluse valija mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="5390b-125">Store selector module properties</span></span>

| <span data-ttu-id="5390b-126">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="5390b-126">Property name</span></span>             | <span data-ttu-id="5390b-127">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5390b-127">Value</span></span>                 | <span data-ttu-id="5390b-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5390b-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5390b-129">Otsinguraadius</span><span class="sxs-lookup"><span data-stu-id="5390b-129">Search radius</span></span> | <span data-ttu-id="5390b-130">Number</span><span class="sxs-lookup"><span data-stu-id="5390b-130">Number</span></span> | <span data-ttu-id="5390b-131">Määratleb kaupluste otsinguraadiuse miilides.</span><span class="sxs-lookup"><span data-stu-id="5390b-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="5390b-132">Kui väärtust pole määratud, kasutatakse vaikimisi 50-miilist otsinguraadiust.</span><span class="sxs-lookup"><span data-stu-id="5390b-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="5390b-133">Teenusetingimused</span><span class="sxs-lookup"><span data-stu-id="5390b-133">Terms of Service</span></span> | <span data-ttu-id="5390b-134">URL</span><span class="sxs-lookup"><span data-stu-id="5390b-134">URL</span></span>    |  <span data-ttu-id="5390b-135">Bing kaartide teenuse korral on teenuse tingimuste URL nõutav.</span><span class="sxs-lookup"><span data-stu-id="5390b-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="5390b-136">Kaupluse valija mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="5390b-136">Add a store selector module to a page</span></span>

<span data-ttu-id="5390b-137">Kaupluse valija moodul vajab toote konteksti, seega seda saab kasutada ainult ostukasti ja ostukorvi moodulites.</span><span class="sxs-lookup"><span data-stu-id="5390b-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="5390b-138">Kaupluse valija moodulid ei tööta nendest moodulitest väljaspool.</span><span class="sxs-lookup"><span data-stu-id="5390b-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="5390b-139">Lisateavet selle kohta, kuidas lisada kaupluse valija moodulit ostukasti moodulisse, vaadake teemast [Ostukasti moodul](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="5390b-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="5390b-140">Lisateavet selle kohta, kuidas lisada kaupluse valija moodulit ostukorvii moodulisse, vaadake teemast [Ostukorvi moodul](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="5390b-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5390b-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5390b-141">Additional resources</span></span>

[<span data-ttu-id="5390b-142">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="5390b-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5390b-143">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="5390b-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5390b-144">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="5390b-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5390b-145">PDP lühiülevaade</span><span class="sxs-lookup"><span data-stu-id="5390b-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="5390b-146">Ostukorvi ja väljaregistreerimise lühiülevaade</span><span class="sxs-lookup"><span data-stu-id="5390b-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="5390b-147">Tarneviiside häälestamine</span><span class="sxs-lookup"><span data-stu-id="5390b-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
