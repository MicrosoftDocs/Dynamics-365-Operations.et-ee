---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261417"
---
# <a name="cart-module"></a><span data-ttu-id="8a265-103">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a265-104">See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="8a265-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8a265-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="8a265-105">Overview</span></span>

<span data-ttu-id="8a265-106">Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud.</span><span class="sxs-lookup"><span data-stu-id="8a265-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="8a265-107">Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.</span><span class="sxs-lookup"><span data-stu-id="8a265-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="8a265-108">Ostukorvi moodul toetab sisselogitud ostu ja külalisostu.</span><span class="sxs-lookup"><span data-stu-id="8a265-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="8a265-109">Samuti toetab see linki **Tagasi ostlema**.</span><span class="sxs-lookup"><span data-stu-id="8a265-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="8a265-110">Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.</span><span class="sxs-lookup"><span data-stu-id="8a265-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="8a265-111">Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis.</span><span class="sxs-lookup"><span data-stu-id="8a265-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="8a265-112">Ostukorvi mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="8a265-112">Cart module properties and slots</span></span>

<span data-ttu-id="8a265-113">Ostukorvi moodulis on atribuut **Pealkiri**, mida saab seadistada sellistele väärtustele nagu **Ostukorv** ja **Ostukorvis olevad kaubad**.</span><span class="sxs-lookup"><span data-stu-id="8a265-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="8a265-114">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="8a265-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="8a265-115">**Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="8a265-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="8a265-116">Sõnumeid juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="8a265-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="8a265-117">Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="8a265-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="8a265-118">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="8a265-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="8a265-119">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="8a265-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="8a265-120">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="8a265-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="8a265-121">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="8a265-121">Module properties</span></span>

<span data-ttu-id="8a265-122">Ostukorvi moodulitel on järgmised seadistused, mida saab konfigureerida jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="8a265-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="8a265-123">**Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="8a265-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="8a265-124">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="8a265-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="8a265-125">**Varude kontroll** – kui väärtus on satud suvandile **Tõene**, saab kauba lisada ostukorvi ainult pärast seda, kui ostukasti moodul on veendunud, et see oleks laos olemas.</span><span class="sxs-lookup"><span data-stu-id="8a265-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="8a265-126">See varude kontroll tehakse nii stsenaariumide jaoks, kus kaup saadetakse, kui ka stsenaariumide jaoks, kus sellele tullakse poodi järele.</span><span class="sxs-lookup"><span data-stu-id="8a265-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="8a265-127">Kui väärtuseks on seatud suvand **Väär**, siis enne kauba ostukorvi lisamist ja tellimuse esitamist varude kontrolli ei tehta.</span><span class="sxs-lookup"><span data-stu-id="8a265-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="8a265-128">Lisateavet varude sätete konfigureerimise kohta varukontoris leiate teemast [Jaemüügikanalite varude saadavuse arvutamine](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="8a265-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="8a265-129">**Varude puhver** – seda atribuuti kasutatakse varude puhvri arvu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8a265-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="8a265-130">Varusid hallatakse reaalajas ja kui paljud kliendid esitavad tellimusi, võib täpse varude arvu säilitamine olla keeruline.</span><span class="sxs-lookup"><span data-stu-id="8a265-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="8a265-131">Kui varude kontroll on tehtud, siis kui varusid on vähem kui puhvri kogus, käsitletakse toodet kui laost otsas.</span><span class="sxs-lookup"><span data-stu-id="8a265-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="8a265-132">Seega kui müük toimub kiiresti läbi mitme kanali, nii et varade arv pole täielikult sünkroonitud, on vähem ohtu, et müüakse kaup, mis on laost otsas.</span><span class="sxs-lookup"><span data-stu-id="8a265-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="8a265-133">**Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8a265-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="8a265-134">Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.</span><span class="sxs-lookup"><span data-stu-id="8a265-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="8a265-135">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="8a265-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="8a265-136">Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil.</span><span class="sxs-lookup"><span data-stu-id="8a265-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="8a265-137">Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.</span><span class="sxs-lookup"><span data-stu-id="8a265-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="8a265-138">Lehele ostukorvi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="8a265-138">Add a cart module to a page</span></span>

<span data-ttu-id="8a265-139">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8a265-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8a265-140">Looge fragment nimega **Ostukorvi fragment** ja lisage uuele fragmendile ostukorvi moodul.</span><span class="sxs-lookup"><span data-stu-id="8a265-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="8a265-141">Lisage ostukorvi moodulile päis.</span><span class="sxs-lookup"><span data-stu-id="8a265-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="8a265-142">Lisage kaupluse valija moodul ostukorvi moodulile.</span><span class="sxs-lookup"><span data-stu-id="8a265-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="8a265-143">Salvestage fragment, viige lõpule selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8a265-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="8a265-144">Looge mall nimega **Ostukorvi mall**ja lisage ostukorvi fragment, mille just lõite.</span><span class="sxs-lookup"><span data-stu-id="8a265-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="8a265-145">Salvestage mall, viige lõpule selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8a265-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="8a265-146">Looge leht, mis kasutab uut malli.</span><span class="sxs-lookup"><span data-stu-id="8a265-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="8a265-147">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="8a265-147">Save and preview the page.</span></span>
1. <span data-ttu-id="8a265-148">Viige lõpule lehe redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="8a265-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a265-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8a265-149">Additional resources</span></span>

[<span data-ttu-id="8a265-150">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="8a265-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8a265-151">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8a265-152">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8a265-153">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8a265-154">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="8a265-155">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="8a265-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8a265-156">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8a265-157">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8a265-158">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="8a265-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="8a265-159">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="8a265-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
