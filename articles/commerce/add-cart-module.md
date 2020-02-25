---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025432"
---
# <a name="cart-module"></a><span data-ttu-id="8e550-103">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="8e550-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8e550-104">See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="8e550-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8e550-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="8e550-105">Overview</span></span>

<span data-ttu-id="8e550-106">Ostukorvi moodulit kasutatakse ostukorvi lisatud kaupade näitamiseks enne, kui klient on kassasse läinud.</span><span class="sxs-lookup"><span data-stu-id="8e550-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="8e550-107">Näiteks sisaldab see kõiki ostukorvi lisatud kaupu ja tellimuse kokkuvõtet.</span><span class="sxs-lookup"><span data-stu-id="8e550-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="8e550-108">See võimaldab kliendil ka kampaaniakoode rakendada või eemaldada.</span><span class="sxs-lookup"><span data-stu-id="8e550-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="8e550-109">Ostukorvi moodul toetab sisselogitud ostu ja külalisostu.</span><span class="sxs-lookup"><span data-stu-id="8e550-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="8e550-110">Samuti toetab see linki **Tagasi ostlema**.</span><span class="sxs-lookup"><span data-stu-id="8e550-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="8e550-111">Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.</span><span class="sxs-lookup"><span data-stu-id="8e550-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="8e550-112">Ostukorvi moodul renderdab andmeid ostukorvi ID põhjal.</span><span class="sxs-lookup"><span data-stu-id="8e550-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="8e550-113">Ostukorvi ID on brauseri küpsis, mis on kogu saidil saadaval.</span><span class="sxs-lookup"><span data-stu-id="8e550-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="8e550-114">Ostukorvi mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="8e550-114">Cart module properties and slots</span></span>

<span data-ttu-id="8e550-115">Ostukorvi moodulis on atribuut **Pealkiri**, mida saab seadistada sellistele väärtustele nagu **Ostukorv** ja **Ostukorvis olevad kaubad**.</span><span class="sxs-lookup"><span data-stu-id="8e550-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="8e550-116">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="8e550-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="8e550-117">**Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="8e550-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="8e550-118">Sõnumeid juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="8e550-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="8e550-119">Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="8e550-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="8e550-120">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="8e550-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="8e550-121">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="8e550-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="8e550-122">Kaupluse valija moodul on integreeritud Bingi kaartide geokodeerimise rakenduse programmeerimisliidesega (API) asukoha laius- ja pikkuskraadideks teisendamiseks.</span><span class="sxs-lookup"><span data-stu-id="8e550-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="8e550-123">Vajalik on Bingi kaartide API võti ja see tuleb lisada jaemüügi jagatud parameetrite lehele rakenduses Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="8e550-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="8e550-124">See moodul toetab kaht atribuuti, **Otsinguraadius** ja **Teenusetingimuste link**.</span><span class="sxs-lookup"><span data-stu-id="8e550-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="8e550-125">Atribuut **Otsinguraadius** määratleb kaupluste otsinguraadiuse miilides.</span><span class="sxs-lookup"><span data-stu-id="8e550-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="8e550-126">Kui väärtust pole määratud, kasutatakse vaikimisi otsingu raadiust, 50 miili.</span><span class="sxs-lookup"><span data-stu-id="8e550-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="8e550-127">Kui kasutatakse Bingi kaarte või mis tahes välist teenust, saab kasutada atribuuti **Teenuse tingimuste link** teenuse tingimuste linki edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="8e550-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="8e550-128">Bing kaartide teenuse korral on teenuse tingimuste link nõutav.</span><span class="sxs-lookup"><span data-stu-id="8e550-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="8e550-129">Ostukorvi mooduli sätted</span><span class="sxs-lookup"><span data-stu-id="8e550-129">Cart module settings</span></span>

<span data-ttu-id="8e550-130">Ostukorvi moodulitel on järgmised seadistused, mida saab konfigureerida jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="8e550-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="8e550-131">**Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="8e550-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="8e550-132">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="8e550-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="8e550-133">**Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas.</span><span class="sxs-lookup"><span data-stu-id="8e550-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="8e550-134">See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele.</span><span class="sxs-lookup"><span data-stu-id="8e550-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="8e550-135">Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.</span><span class="sxs-lookup"><span data-stu-id="8e550-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="8e550-136">**Varude puhver** – seda atribuuti kasutatakse varude puhvri arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8e550-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="8e550-137">Varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline.</span><span class="sxs-lookup"><span data-stu-id="8e550-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="8e550-138">Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas.</span><span class="sxs-lookup"><span data-stu-id="8e550-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="8e550-139">Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.</span><span class="sxs-lookup"><span data-stu-id="8e550-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="8e550-140">**Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8e550-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="8e550-141">Seda marsruuti saab konfigureerida saidi tasemel.</span><span class="sxs-lookup"><span data-stu-id="8e550-141">This route can be configured at the site level.</span></span> <span data-ttu-id="8e550-142">See konfiguratsioon laseb jaemüüjal viia kliendi tagasi avalehele või mis tahes teisele leheküljele saidil.</span><span class="sxs-lookup"><span data-stu-id="8e550-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="8e550-143">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="8e550-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="8e550-144">Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil.</span><span class="sxs-lookup"><span data-stu-id="8e550-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="8e550-145">Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.</span><span class="sxs-lookup"><span data-stu-id="8e550-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="8e550-146">Lehele ostukorvi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="8e550-146">Add a cart module to a page</span></span>

<span data-ttu-id="8e550-147">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8e550-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8e550-148">Looge fragment nimega **Ostukorvi fragment** ja lisage sellele ostukorvi moodul.</span><span class="sxs-lookup"><span data-stu-id="8e550-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="8e550-149">Lisage ostukorvi moodulile päis.</span><span class="sxs-lookup"><span data-stu-id="8e550-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="8e550-150">Lisage kaupluse valija moodul ostukorvi moodulile.</span><span class="sxs-lookup"><span data-stu-id="8e550-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="8e550-151">Salvestage fragment, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8e550-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="8e550-152">Looge mall nimega **Ostukorvi mall**ja lisage sellele ostukorvi fragment, mille just lõite.</span><span class="sxs-lookup"><span data-stu-id="8e550-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="8e550-153">Salvestage mall, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8e550-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="8e550-154">Looge leht, mis kasutab uut malli.</span><span class="sxs-lookup"><span data-stu-id="8e550-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="8e550-155">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="8e550-155">Save and preview the page.</span></span>
1. <span data-ttu-id="8e550-156">Viige lõpuni lehe redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8e550-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8e550-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8e550-157">Additional resources</span></span>

[<span data-ttu-id="8e550-158">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="8e550-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8e550-159">Konteinermoodul</span><span class="sxs-lookup"><span data-stu-id="8e550-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8e550-160">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="8e550-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8e550-161">Väljaregistreerimise moodul</span><span class="sxs-lookup"><span data-stu-id="8e550-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8e550-162">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="8e550-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8e550-163">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="8e550-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8e550-164">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="8e550-164">Footer module</span></span>](author-footer-module.md)
