---
title: Varude sätete rakendamine
description: See teema hõlmab varude sätteid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce rakendada.
author: anupamar-ms
ms.date: 09/15/2020
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
ms.openlocfilehash: b2c44eb5ece74de15e22180abc6d9d0448ab401b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798885"
---
# <a name="apply-inventory-settings"></a><span data-ttu-id="c7153-103">Varude sätete rakendamine</span><span class="sxs-lookup"><span data-stu-id="c7153-103">Apply inventory settings</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c7153-104">See teema hõlmab varude sätteid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce rakendada.</span><span class="sxs-lookup"><span data-stu-id="c7153-104">This topic covers inventory settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="c7153-105">Varude sätted määratlevad, kas varusid tuleks enne toodete ostukorvi lisamist kontrollida.</span><span class="sxs-lookup"><span data-stu-id="c7153-105">Inventory settings specify whether inventory should be checked before products are added to the cart.</span></span> <span data-ttu-id="c7153-106">Samuti määratletakse nende abil varudega seotud kaubandusteated, nagu näiteks „Olemas“ ja „Ainult mõni alles“.</span><span class="sxs-lookup"><span data-stu-id="c7153-106">They also define inventory-related merchandising messages, such as "In stock" and "Only a few left."</span></span> <span data-ttu-id="c7153-107">Need sätted tagavad, et toodet ei saa soetada, kui see on laost otsas.</span><span class="sxs-lookup"><span data-stu-id="c7153-107">These settings ensure that a product can't be purchased if it's out of stock.</span></span>

<span data-ttu-id="c7153-108">Dynamics 365 Commerce annab vabade toodete saadavuse hinnangu.</span><span class="sxs-lookup"><span data-stu-id="c7153-108">Dynamics 365 Commerce provides estimates of on-hand availability for products.</span></span> <span data-ttu-id="c7153-109">Lisateavet vabade varude saadavuse hinnangu arvutamise kohta vt teemast [Varude saadavuse arvutamine jaemüügikanalite jaoks](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="c7153-109">For information about how estimated on-hand availability is calculated, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>

<span data-ttu-id="c7153-110">Commerce'i saidiehitajas saab määratleda toote või kategooria varude künnised ja vahemikud.</span><span class="sxs-lookup"><span data-stu-id="c7153-110">In Commerce site builder, inventory thresholds and ranges can be defined for a product or a category.</span></span> <span data-ttu-id="c7153-111">Need määratlevad, kas varude liigituseks on „olemas“, „madal varu“ või „laost otsas“.</span><span class="sxs-lookup"><span data-stu-id="c7153-111">They determine whether inventory can be classified as in stock, low stock, or out of stock.</span></span> <span data-ttu-id="c7153-112">Lisateavet vt teemast [Varude puhvrite ja varude tasemete konfigureerimine](inventory-buffers-levels.md).</span><span class="sxs-lookup"><span data-stu-id="c7153-112">For details, see [Configure inventory buffers and inventory levels](inventory-buffers-levels.md).</span></span>

> [!NOTE]
> <span data-ttu-id="c7153-113">Varude lävesid ja vahemikke toetatakse rakenduse Dynamics 365 Commerce väljalaskes 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="c7153-113">Support for inventory thresholds and ranges is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

## <a name="inventory-settings"></a><span data-ttu-id="c7153-114">Varude sätted</span><span class="sxs-lookup"><span data-stu-id="c7153-114">Inventory settings</span></span>

<span data-ttu-id="c7153-115">Commerce'is määratletakse varude sätted saidiehitajas jaotises **Saidi sätted \> Laiendused \> Varude haldus**.</span><span class="sxs-lookup"><span data-stu-id="c7153-115">In Commerce, inventory settings are defined at **Site Settings \> Extensions \> Inventory Management** in site builder.</span></span> <span data-ttu-id="c7153-116">On neli varude sätet, millest üks on aegunud.</span><span class="sxs-lookup"><span data-stu-id="c7153-116">There are four inventory settings, one of which is obsolete (deprecated):</span></span>

- <span data-ttu-id="c7153-117">**Luba rakenduses varude kontrollimine** – see säte lülitab sisse tootevarude kontrollimise võimaluse.</span><span class="sxs-lookup"><span data-stu-id="c7153-117">**Enable stock check in app** – This setting turns on a product inventory check.</span></span> <span data-ttu-id="c7153-118">Seejärel kontrollitakse moodulite ostukast, ostukorv ja poodi järeletulemine raames tootevarusid ja lubatakse lisada toode ostukorvi vaid siis, kui vastavad varud on saadaval.</span><span class="sxs-lookup"><span data-stu-id="c7153-118">Buy box, cart, and pick up in store modules will then check product inventory, and will allow a product to be added to the cart only if inventory is available.</span></span>
- <span data-ttu-id="c7153-119">**Varude taseme alus** – see säte määratleb, kuidas arvutatakse varude tasemeid.</span><span class="sxs-lookup"><span data-stu-id="c7153-119">**Inventory level based on** – This setting defines how inventory levels are calculated.</span></span> <span data-ttu-id="c7153-120">Saadaolevad väärtused on **Kokku saadaval**, **Füüsiliselt saadaval** ja **Laost otsas künnis**.</span><span class="sxs-lookup"><span data-stu-id="c7153-120">The available values are **Total Available**, **Physical Available**, and **Out of stock threshold**.</span></span> <span data-ttu-id="c7153-121">Commerce'i saidiehitajas saab määratleda iga toote või kategooria varude künnise ja vahemikud.</span><span class="sxs-lookup"><span data-stu-id="c7153-121">In Commerce, inventory threshold and ranges can be defined for each product and category.</span></span> <span data-ttu-id="c7153-122">Varude API-d hangivad toote varusid puudutavat teavet nii **Kokku saadaval** atribuudi kui ka **Füüsiliselt saadaval** atribuudi kohta.</span><span class="sxs-lookup"><span data-stu-id="c7153-122">The inventory APIs return product inventory information for both the **Total Available** property and the **Physical Available** property.</span></span> <span data-ttu-id="c7153-123">Jaemüüja otsustab, kas varude arvu ja vastavate olemas ja laost otsas vahemike määramiseks tuleks kasutada väärtust **Kokku saadaval** või **Füüsiliselt saadaval**.</span><span class="sxs-lookup"><span data-stu-id="c7153-123">The retailer decides whether the **Total Available** or **Physical Available** value should be used to determine the inventory count and the corresponding ranges for in-stock and out-of-stock statuses.</span></span>

    <span data-ttu-id="c7153-124">Sätte **Varude taseme alus** väärtus **Laost otsas künnis** on vana (pärand), aegunud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c7153-124">The **Out of stock threshold** value of the **Inventory level based on** setting is an old (legacy), obsolete value.</span></span> <span data-ttu-id="c7153-125">Selle valimisel määratakse varude arv väärtuse **Kokku saadaval** tulemuste alusel, kuid künnis määratletakse hiljem kirjeldatava numbrilise sätte **Laost otsas künnis** alusel.</span><span class="sxs-lookup"><span data-stu-id="c7153-125">When it's selected, the inventory count is determined from the results of the **Total Available** value, but the threshold is defined by the **Out of stock threshold** numeric setting that is described later.</span></span> <span data-ttu-id="c7153-126">See künnis kehtib kõikidele toodetele kogu e-kaubanduse saidil.</span><span class="sxs-lookup"><span data-stu-id="c7153-126">This threshold setting applies to all products across an e-commerce site.</span></span> <span data-ttu-id="c7153-127">Kui varud jäävad alla künnise numbri, siis arvatakse toode olevat laost otsas.</span><span class="sxs-lookup"><span data-stu-id="c7153-127">If inventory is below the threshold number, a product is considered out of stock.</span></span> <span data-ttu-id="c7153-128">Vastasel juhul on toode aga olemas.</span><span class="sxs-lookup"><span data-stu-id="c7153-128">Otherwise, it's considered in stock.</span></span> <span data-ttu-id="c7153-129">Väärtuse **Laost otsas künnis** võimalused on piiratud ja me ei soovita seda kasutada versioonis 10.0.12 ega hilisemates versioonides.</span><span class="sxs-lookup"><span data-stu-id="c7153-129">The capabilities of the **Out of stock threshold** value are limited, and we don't recommend that you use it in version 10.0.12 and later.</span></span>

- <span data-ttu-id="c7153-130">**Varude vahemikud** – säte määratleb varude vahemikud, mille kohta kuvatakse saidi moodulites teade.</span><span class="sxs-lookup"><span data-stu-id="c7153-130">**Inventory ranges** – This setting defines the inventory ranges that message are shown for on site modules.</span></span> <span data-ttu-id="c7153-131">See on kohaldatav vaid juhul, kui sätte **Varude taseme alus** jaoks valitakse väärtus **Kokku saadaval** või väärtus **Füüsiliselt saadaval**.</span><span class="sxs-lookup"><span data-stu-id="c7153-131">It's applicable only if either the **Total Available** value or the **Physical Available** value is selected for the **Inventory level based on** setting.</span></span> <span data-ttu-id="c7153-132">Saadaolevad väärtused on **Kõik**, **Varud madalad ja laost otsas** ja **Laost otsas**.</span><span class="sxs-lookup"><span data-stu-id="c7153-132">The available values are **All**, **Low and out of stock**, and **Out of stock**.</span></span>

    - <span data-ttu-id="c7153-133">Suvandi **Kõik** valimisel kuvatakse kõik varude vahemikud, alates olemasolevast (teade „olemas“) ja lõpetades väärtusega laost otsas (teade „Laost otsas“).</span><span class="sxs-lookup"><span data-stu-id="c7153-133">When **All** is selected, messages for all inventory ranges, from in stock ("Available" message) to out of stock ("Out of stock" message), will be shown.</span></span>
    - <span data-ttu-id="c7153-134">Suvandi **Varud madalad ja laost otsas** valimisel kuvatakse kõik varude vahemikud, v.a väärtus olemasolev (teade „olemas“).</span><span class="sxs-lookup"><span data-stu-id="c7153-134">When **Low and out of stock** is selected, messages for all inventory ranges except in stock ("Available" message) will be shown.</span></span>
    - <span data-ttu-id="c7153-135">Suvandi **Laost otsas** valimisel kuvatakse ainult teade „Laost otsas“.</span><span class="sxs-lookup"><span data-stu-id="c7153-135">When **Out of stock** is selected, only the "Out of stock" message will be shown.</span></span>

- <span data-ttu-id="c7153-136">**Laost otsas künnis** – see vana numbrisäte jõustub ainult siis, kui sätte **Varude taseme alus** jaoks valitakse väärtus **Laost otsas künnis**.</span><span class="sxs-lookup"><span data-stu-id="c7153-136">**Out of stock threshold** – This old numeric setting will take effect only if the **Out of stock threshold** value is selected for the **Inventory level based on** setting.</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="c7153-137">Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="c7153-137">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="c7153-138">Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="c7153-138">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="c7153-139">Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="c7153-139">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-inventory-settings"></a><span data-ttu-id="c7153-140">Varude sätteid kasutavad moodulid</span><span class="sxs-lookup"><span data-stu-id="c7153-140">Modules that use inventory settings</span></span>

<span data-ttu-id="c7153-141">Ostukasti, soovinimekirja, kaupluse valija, ostukorvi ja ostukorvi ikooni moodulid kasutavad varude sätteid varude vahemike ja teadete kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="c7153-141">Buy box, wishlist, store selector, cart, and cart icon modules use inventory settings to show the inventory ranges and messages.</span></span>

<span data-ttu-id="c7153-142">Järgmisel pildil on toodud toodete üksikasjade lehe näide, kus kuvatakse teadet laos olemas („Olemas“).</span><span class="sxs-lookup"><span data-stu-id="c7153-142">The following image shows an example of a product details page (PDP) that is showing an in-stock ("Available") message.</span></span>

![Laos olemas teadet kuvava toote üksikasjade lehe mooduli näide](./media/pdp-InStock.png)

<span data-ttu-id="c7153-144">Järgmisel pildil on toodud toodete üksikasjade lehe näide, kus kuvatakse teadet laost otsas („Laost otsas“).</span><span class="sxs-lookup"><span data-stu-id="c7153-144">The following image shows an example of a PDP that is showing an "Out of stock" message.</span></span>

![Laost otsas teadet kuvava toote üksikasjade lehe mooduli näide](./media/pdp-outofstock.png)

<span data-ttu-id="c7153-146">Järgmisel pildil on toodud ostukorvi näide, kus kuvatakse teadet laos olemas („Olemas“).</span><span class="sxs-lookup"><span data-stu-id="c7153-146">The following image shows an example of a cart that is showing an in-stock ("Available") message.</span></span>

![Laos olemas teadet kuvava ostukorvi mooduli näide](./media/cart-instock.png)

## <a name="additional-resources"></a><span data-ttu-id="c7153-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c7153-148">Additional resources</span></span>

[<span data-ttu-id="c7153-149">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="c7153-149">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c7153-150">Varude puhvrite ja varude tasemete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c7153-150">Configure inventory buffers and inventory levels</span></span>](inventory-buffers-levels.md)

[<span data-ttu-id="c7153-151">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="c7153-151">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c7153-152">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="c7153-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c7153-153">Kontohalduse lehed ja moodulid</span><span class="sxs-lookup"><span data-stu-id="c7153-153">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="c7153-154">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="c7153-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="c7153-155">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="c7153-155">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
