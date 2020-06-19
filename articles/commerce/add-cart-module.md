---
title: Ostukorvi moodul
description: See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411269"
---
# <a name="cart-module"></a><span data-ttu-id="97045-103">Ostukorvi moodul</span><span class="sxs-lookup"><span data-stu-id="97045-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="97045-104">See teema hõlmab ostukorvi mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="97045-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97045-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="97045-105">Overview</span></span>

<span data-ttu-id="97045-106">Ostukorvi moodul näitab ostukorvi lisatud kaupasid enne, kui klient on kassasse läinud.</span><span class="sxs-lookup"><span data-stu-id="97045-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="97045-107">Moodul näitab ka ostu kokkuvõtet ja võimaldab kliendil rakendada või eemaldada kampaaniakoode.</span><span class="sxs-lookup"><span data-stu-id="97045-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="97045-108">Ostukorvi moodul toetab sisselogitud ostu ja külalisostu.</span><span class="sxs-lookup"><span data-stu-id="97045-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="97045-109">Samuti toetab see linki **Tagasi ostlema**.</span><span class="sxs-lookup"><span data-stu-id="97045-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="97045-110">Saate konfigureerida selle lingi marsruudi jaotises **Saidi sätted \> Laiendused \> Marsruudid**.</span><span class="sxs-lookup"><span data-stu-id="97045-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="97045-111">Ostukorvi moodul renderdab andmed ostukorvi ID põhjal, mis on üle kogu saidi saadaval brauseri küpsis.</span><span class="sxs-lookup"><span data-stu-id="97045-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="97045-112">Järgmisel pildil on näide Fabrikami saidi ostukorvi lehest.</span><span class="sxs-lookup"><span data-stu-id="97045-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Ostukorvi mooduli näide](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="97045-114">Ostukorvi mooduli atribuudid ja pesad</span><span class="sxs-lookup"><span data-stu-id="97045-114">Cart module properties and slots</span></span>

<span data-ttu-id="97045-115">Ostukorvi moodulis on atribuut **Pealkiri**, mida saab seadistada sellistele väärtustele nagu **Ostukorv** ja **Ostukorvis olevad kaubad**.</span><span class="sxs-lookup"><span data-stu-id="97045-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="97045-116">Moodulid, mida saab ostukorvi moodulis kasutada</span><span class="sxs-lookup"><span data-stu-id="97045-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="97045-117">**Tekstiplokk** – see moodul toetab ostukorvi mooduli kohandatud sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="97045-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="97045-118">Sõnumeid juhib sisuhaldussüsteem (CMS).</span><span class="sxs-lookup"><span data-stu-id="97045-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="97045-119">Lisada on võimalik mis tahes sõnum, näiteks „Tellimusega esinevate probleemide osas võtke ühendust numbril 1-800-Fabrikam”.</span><span class="sxs-lookup"><span data-stu-id="97045-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="97045-120">**Kaupluse valija** – see moodul kuvab lähedalasuvate poodide loendi, kus kaup on kohapeal olemas.</span><span class="sxs-lookup"><span data-stu-id="97045-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="97045-121">See võimaldab kasutajatel sisestada asukoha, et leida läheduses asuvad kauplused.</span><span class="sxs-lookup"><span data-stu-id="97045-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="97045-122">Selle mooduli kohta lisateabe saamiseks vaadake teemat [Poe valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="97045-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="97045-123">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="97045-123">Module properties</span></span>

<span data-ttu-id="97045-124">Jaotises **Saidi sätted \> Laiendused** saab konfigureerida järgmisi ostukorvi mooduli sätteid.</span><span class="sxs-lookup"><span data-stu-id="97045-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="97045-125">**Maksimaalne kogus** – seda tribuuti kasutatakse iga kauba maksimaalselt ostukorvi lisatava arvu määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="97045-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="97045-126">Näiteks võib jaemüüja otsustada, et ühe tehinguga saab müüa iga toodet ainult 10 tükki.</span><span class="sxs-lookup"><span data-stu-id="97045-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="97045-127">**Varud** – varude sätete rakendamise kohta lisateabe saamiseks vt teemat [Varude sätete rakendamine](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="97045-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="97045-128">**Tagasi ostukorvi** – seda atribuuti kasutatakse ostukorvi lingi **Tagasi ostlema** marsruudi määramiseks.</span><span class="sxs-lookup"><span data-stu-id="97045-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="97045-129">Protsessi saab konfigureerida saiditasemel, võimaldades jaemüüjatel viia klient tagasi avalehele või saidi mis tahes teisele lehele.</span><span class="sxs-lookup"><span data-stu-id="97045-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="97045-130">Commerce Scale Unitiga suhtlemine</span><span class="sxs-lookup"><span data-stu-id="97045-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="97045-131">Ostukorvi moodul toob toote teabe välja Commerce Scale Uniti API-de abil.</span><span class="sxs-lookup"><span data-stu-id="97045-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="97045-132">Brauseriküpsise ostukorvi ID-d kasutatakse Commerce Sale Unitist kogu tooteteabe toomiseks.</span><span class="sxs-lookup"><span data-stu-id="97045-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="97045-133">Lehele ostukorvi mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="97045-133">Add a cart module to a page</span></span>

<span data-ttu-id="97045-134">Uuele lehele ostukorvi mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="97045-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="97045-135">Avage **Lehe fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="97045-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="97045-136">Valige dialoogiboksis **Uus lehe fragment** moodul **Ostukorv**.</span><span class="sxs-lookup"><span data-stu-id="97045-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="97045-137">Jaotises **Lehe fragmendi nimi** sisestage nimi **Ostukorvi fragment** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="97045-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="97045-138">Valige pesa **Ostukorv**.</span><span class="sxs-lookup"><span data-stu-id="97045-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="97045-139">Valige parempoolsel atribuutide paanil pliiatsisümbol, sisestage väljale pealkirja tekst ja seejärel valige märkesümbol.</span><span class="sxs-lookup"><span data-stu-id="97045-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="97045-140">Valige pesas **Ostukorv** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="97045-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97045-141">Valige dialoogiboksis **Lisa moodul** moodul **Kaupluse valija** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="97045-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="97045-142">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="97045-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="97045-143">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="97045-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="97045-144">Sisestage dialoogiboksis **Uus mall** jaotises **Malli nimi** mallile nimi.</span><span class="sxs-lookup"><span data-stu-id="97045-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="97045-145">Valige liigendpuust pesa **Keha**, valige kolmikpunkt (**...**) ja seejärel suvand **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="97045-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="97045-146">Valige dialoogiboksis **Lehe fragmendi valimine** fragment **Ostukorvi fragment** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="97045-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="97045-147">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="97045-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="97045-148">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="97045-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="97045-149">Valige dialoogiboksis **Malli valimine** varem teie loodud mall, sisestage lehe nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="97045-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="97045-150">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="97045-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="97045-151">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="97045-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97045-152">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="97045-152">Additional resources</span></span>

[<span data-ttu-id="97045-153">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="97045-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="97045-154">Konteineri moodul</span><span class="sxs-lookup"><span data-stu-id="97045-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="97045-155">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="97045-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="97045-156">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="97045-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="97045-157">Ostukorvi ikooni moodul</span><span class="sxs-lookup"><span data-stu-id="97045-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="97045-158">Väljaregistreerimismoodul</span><span class="sxs-lookup"><span data-stu-id="97045-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="97045-159">Tellimuse kinnituse moodul</span><span class="sxs-lookup"><span data-stu-id="97045-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="97045-160">Päise moodul</span><span class="sxs-lookup"><span data-stu-id="97045-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="97045-161">Jaluse moodul</span><span class="sxs-lookup"><span data-stu-id="97045-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="97045-162">Varude saadavuse arvutamine jaemüügikanalite jaoks</span><span class="sxs-lookup"><span data-stu-id="97045-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
