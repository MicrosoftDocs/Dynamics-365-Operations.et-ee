---
title: Saidil navigeerimise kohandamine
description: Selles teemas kirjeldatakse, kuidas luua kohandatud veebipõhist navigeerimishierarhiat, et korrastada tooted rakenduse Microsoft Dynamics 365 Commerce saidil sirvimiseks.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2b6a7a3b35873e80be391c627d0397fd6398a99
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411659"
---
# <a name="customize-site-navigation"></a><span data-ttu-id="2a82d-103">Saidil navigeerimise kohandamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-103">Customize site navigation</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2a82d-104">Selles teemas kirjeldatakse, kuidas luua kohandatud veebipõhist navigeerimishierarhiat, et korrastada tooted rakenduse Microsoft Dynamics 365 Commerce saidil sirvimiseks.</span><span class="sxs-lookup"><span data-stu-id="2a82d-104">This topic describes how to create a customized online navigation hierarchy to organize your products for browsing on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="2a82d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="2a82d-105">Overview</span></span>

<span data-ttu-id="2a82d-106">Veebipoe fassaadid võimaldavad tavaliselt klientidel tooteid avastada ja sirvida, navigeerides tootekategooriate kaudu.</span><span class="sxs-lookup"><span data-stu-id="2a82d-106">Online storefronts typically let customers discover and browse products by navigating through product categories.</span></span> <span data-ttu-id="2a82d-107">Seda võimalust pakuvad tavaliselt lehe ülaosas olevad vahekaardid või vasakul olev navigeerimisriba.</span><span class="sxs-lookup"><span data-stu-id="2a82d-107">This capability is usually provided by tabs at the top of the page or by a navigation bar on the left.</span></span> <span data-ttu-id="2a82d-108">Rakenduses Dynamics 365 Commerce saate luua ja hallata kategooria navigeerimise hierarhilist struktuuri ja erinevates kategooriates sisalduvaid tooteid.</span><span class="sxs-lookup"><span data-stu-id="2a82d-108">In Dynamics 365 Commerce, you can create and manage the hierarchal structure of your category navigation and the products that are included in the various categories.</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="2a82d-109">Kanali navigeerimishierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="2a82d-109">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="2a82d-110">Kanali navigeerimishierarhia loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2a82d-110">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="2a82d-111">Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kategooria- ja tootehaldus**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-111">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="2a82d-112">Valige suvand **Kategooria hierarhiad** ja valige seejärel **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-112">Select **Category hierarchies**, and then select **New**.</span></span>
1. <span data-ttu-id="2a82d-113">Andke hierarhiale nimi.</span><span class="sxs-lookup"><span data-stu-id="2a82d-113">Name the hierarchy.</span></span>

    > [!NOTE]
    > <span data-ttu-id="2a82d-114">Kõige ülemine loodav kategooria on juurekategooria sõlm.</span><span class="sxs-lookup"><span data-stu-id="2a82d-114">The topmost category that you create is the root category node.</span></span> <span data-ttu-id="2a82d-115">Teie saidil seda ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="2a82d-115">It won't be shown on your site.</span></span> <span data-ttu-id="2a82d-116">Kategooriahierarhia loomiseks, kus teie saidil kuvatakse üks ülemise taseme sõlm, looge ja nimetage kategooria juurekategooria alamana.</span><span class="sxs-lookup"><span data-stu-id="2a82d-116">To create a category hierarchy where a single top-level node is shown on your site, create and name the category as a child of the root category.</span></span>

1. <span data-ttu-id="2a82d-117">Valige suvand **Uus kategooria sõlm** ja andke kategooriale nimi.</span><span class="sxs-lookup"><span data-stu-id="2a82d-117">Select **New category node**, and name the category.</span></span>
1. <span data-ttu-id="2a82d-118">Jätkake vastavalt vajadusele õe- ja alamkategooriate loomist.</span><span class="sxs-lookup"><span data-stu-id="2a82d-118">Continue to create sibling and child categories as you require.</span></span>

<span data-ttu-id="2a82d-119">Nüüd saate määrata tooted igale kategooriale, mille ülemise taseme kategooria alla lõite.</span><span class="sxs-lookup"><span data-stu-id="2a82d-119">You can now assign products to each category that you created under the top-level category.</span></span>

## <a name="customize-the-order-of-categories"></a><span data-ttu-id="2a82d-120">Kategooriate järjestuse kohandamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-120">Customize the order of categories</span></span>

<span data-ttu-id="2a82d-121">Vaikimisi ilmuvad määratletud kategooriad teie saidi tähestikulises järjestuses.</span><span class="sxs-lookup"><span data-stu-id="2a82d-121">By default, the categories that you define will appear in alphabetical order on your site.</span></span> <span data-ttu-id="2a82d-122">Samas saate kategooriate kuvamise järjestust ka kohandada.</span><span class="sxs-lookup"><span data-stu-id="2a82d-122">However, you can also customize the display order of categories.</span></span>

## <a name="assign-a-category-hierarchy-type"></a><span data-ttu-id="2a82d-123">Kategooriahierarhia tüübi määramine</span><span class="sxs-lookup"><span data-stu-id="2a82d-123">Assign a category hierarchy type</span></span>

1. <span data-ttu-id="2a82d-124">Avage **Jaemüük ja kaubandus \> Tooted ja kategooriad \> Kategooria- ja tootehaldus**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-124">Go to **Retail and Commerce \> Products and categories \> Category and product management**.</span></span>
1. <span data-ttu-id="2a82d-125">Valige suvand **Kategooriahierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-125">Select **Category hierarchies**.</span></span>
1. <span data-ttu-id="2a82d-126">Valige tegumiriba vahekaardil **Kategooriahierarhia** grupis **Häälesta** suvand **Hierarhiatüübi seostamine**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-126">On the Action Pane, on the **Category hierarchy** tab, in the **Set up** group, select **Associate hierarchy type**.</span></span>
1. <span data-ttu-id="2a82d-127">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-127">Select **New**.</span></span>
1. <span data-ttu-id="2a82d-128">Valige väljal **Kategooria hierarhia tüüp** suvand **Kanali navigeerimishierarhia**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-128">In the **Category hierarchy type** field, select **Channel navigation hierarchy**.</span></span>
1. <span data-ttu-id="2a82d-129">Valige väljal **Kategooriahierarhia** varem loodud kanali navigeerimishierarhia.</span><span class="sxs-lookup"><span data-stu-id="2a82d-129">In the **Category hierarchy** field, select the channel navigation hierarchy that you created earlier.</span></span>

## <a name="publish-new-or-updated-navigation-hierarchies"></a><span data-ttu-id="2a82d-130">Uute või värskendatud navigeerimishierarhiate avaldamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-130">Publish new or updated navigation hierarchies</span></span>

<span data-ttu-id="2a82d-131">Oma navigeerimishierarhia veebipoe fassaadis kättesaadavaks tegemiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2a82d-131">To make your navigation hierarchy available to your online storefront, follow these steps.</span></span>

1. <span data-ttu-id="2a82d-132">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kanali kategooriad ja toote atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-132">Go to **Retail and Commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="2a82d-133">Valige vasakpoolsel puul oma veebipood.</span><span class="sxs-lookup"><span data-stu-id="2a82d-133">In the tree on the left, select your online store.</span></span>
1. <span data-ttu-id="2a82d-134">Valige suvand **Kanalivärskenduste avaldamine**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-134">Select **Publish channel updates**.</span></span>
1. <span data-ttu-id="2a82d-135">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-135">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
1. <span data-ttu-id="2a82d-136">Otsige ja valige loendist **Töö 1040**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-136">In the list, find and select **Job 1040**.</span></span>
1. <span data-ttu-id="2a82d-137">Valige käsk **Käita kohe**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-137">Select **Run now**.</span></span>
1. <span data-ttu-id="2a82d-138">Korrake samme 5 ja 6 tööde 1070 ja 1150 jaoks.</span><span class="sxs-lookup"><span data-stu-id="2a82d-138">Repeat steps 5 and 6 for jobs 1070 and 1150.</span></span>

## <a name="show-categories-on-your-site"></a><span data-ttu-id="2a82d-139">Kategooriate kuvamine saidil</span><span class="sxs-lookup"><span data-stu-id="2a82d-139">Show categories on your site</span></span>

<span data-ttu-id="2a82d-140">Kategooriahierarhia kuvamiseks veebipoe fassaadil peate lisama mallis või fragmendis sobivasse asukohta navigeerimismenüü mooduli.</span><span class="sxs-lookup"><span data-stu-id="2a82d-140">To show your category hierarchy on your online storefront, you must add the navigation menu module in the appropriate location in a template or fragment.</span></span> <span data-ttu-id="2a82d-141">Seejärel kuvab navigeerimismenüü moodul teie navigeerimishierarhia, kui olete oma navigeerimishierarhia avaldanud kanalis, millega teie sait on seotud.</span><span class="sxs-lookup"><span data-stu-id="2a82d-141">The navigation menu module will then show your navigation hierarchy, provided that you've published your navigation hierarchy to the channel that your site is bound to.</span></span>

> [!NOTE]
> <span data-ttu-id="2a82d-142">Mooduliteegis sisalduv navigeerimismenüü moodul võimaldab kasutajatel navigeerida ainult kategooriatesse, millel puuduvad alamkategooriad.</span><span class="sxs-lookup"><span data-stu-id="2a82d-142">The navigation menu module that is included in the module library lets users navigate only to categories that don't have subcategories.</span></span> <span data-ttu-id="2a82d-143">Kui teie kliendid peaksid saama navigeerida kategooriatesse, millel on alamkategooriad, peate navigeerimispaani moodulit kohandama.</span><span class="sxs-lookup"><span data-stu-id="2a82d-143">If your customers should be able to navigate to categories that have subcategories, you must customize the navigation menu module.</span></span>

## <a name="add-custom-navigation-options"></a><span data-ttu-id="2a82d-144">Kohandatud navigeerimissuvandite lisamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-144">Add custom navigation options</span></span>

<span data-ttu-id="2a82d-145">Navigeerimismenüüs saate lisada navigeerimissuvandeid, mis ei kuulu teie toote kategooriahierarhiasse.</span><span class="sxs-lookup"><span data-stu-id="2a82d-145">On your navigation menu, you can add navigation options that aren't part of your product category hierarchy.</span></span> <span data-ttu-id="2a82d-146">Näiteks saate toote kategooria loendi lõpus saate lisada üksuse **Võtke meiega ühendust**, mis osutab saidi jaoks loodud kontaktide lehele.</span><span class="sxs-lookup"><span data-stu-id="2a82d-146">For example, at the end of the list of product categories, you can add a **Contact Us** item that points to a contact page that you've built for your site.</span></span>

<span data-ttu-id="2a82d-147">Navigeerimismenüüsse kohandatud navigeerimisesuvandite lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2a82d-147">To add custom navigation options to your navigation menu, follow these steps.</span></span>

1. <span data-ttu-id="2a82d-148">Valige mallis või fragmendis, mida soovite kohandada, navigeerimismenüü moodul.</span><span class="sxs-lookup"><span data-stu-id="2a82d-148">In the template or fragment that you want to customize, select the navigation menu module.</span></span>
1. <span data-ttu-id="2a82d-149">Valige atribuudipaanil vahekaardil **Andmed** suvand **Lisa üksus**, et luua uus sisuhaldussüsteemi (CMS) navigeerimisüksus.</span><span class="sxs-lookup"><span data-stu-id="2a82d-149">In the property pane, on the **Data** tab, select **Add item** to create a new content management system (CMS) navigation item.</span></span>
1. <span data-ttu-id="2a82d-150">Sisestage lingi tekst ja URL.</span><span class="sxs-lookup"><span data-stu-id="2a82d-150">Enter link text and a URL.</span></span>
1. <span data-ttu-id="2a82d-151">Rohkemate kohandatud navigeerimissuvandite lisamiseks korrake samme 2 ja 3.</span><span class="sxs-lookup"><span data-stu-id="2a82d-151">Repeat steps 2 and 3 to add more custom navigation options.</span></span>
1. <span data-ttu-id="2a82d-152">Kui olete lõpetanud, valige malli või fragmendi salvestamiseks **Salvesta** ja seejärel selle registreerimiseks **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="2a82d-152">When you've finished, select **Save** to save the template or fragment, and then select **Finish editing** to check it in.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2a82d-153">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2a82d-153">Additional resources</span></span>

[<span data-ttu-id="2a82d-154">Mallide ja paigutuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="2a82d-154">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="2a82d-155">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-155">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="2a82d-156">Eelmääratud paigutustega töötamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-156">Work with preset layouts</span></span>](work-with-layouts.md)

[<span data-ttu-id="2a82d-157">Fragmentidega töötamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-157">Work with fragments</span></span>](work-with-fragments.md)

[<span data-ttu-id="2a82d-158">Moodulitega töötamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-158">Work with modules</span></span>](work-with-modules.md)

[<span data-ttu-id="2a82d-159">Lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="2a82d-159">Create a page URL</span></span>](create-page-url.md)

[<span data-ttu-id="2a82d-160">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="2a82d-160">Work with publish groups</span></span>](publish-groups.md)
