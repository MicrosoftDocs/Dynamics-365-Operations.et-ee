---
title: Kiirvaatemoodul
description: See teema hõlmab kiirvaatemooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d7e88163fd9b8dc4f5636ed29e2c4248aece52bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792167"
---
# <a name="quick-view-module"></a><span data-ttu-id="16b93-103">Kiirvaatemoodul</span><span class="sxs-lookup"><span data-stu-id="16b93-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16b93-104">See teema hõlmab kiirvaatemooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="16b93-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="16b93-105">Kiirvaatemoodul võimaldab kasutajatel toodete sirvimisel loendilehel kiiresti vaadata tooteteavet ja lisada loendilehelt ostukorvi ühe või mitu toodet ilma toote üksikasjade lehele (PDP) minemiseta.</span><span class="sxs-lookup"><span data-stu-id="16b93-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="16b93-106">Kiirvaatemoodul annab ülevaate tooteteabest, mida kasutajad vajavad "ostukorvi lisamise" otsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="16b93-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="16b93-107">See sisaldab ka linki PDP-le, et kasutajad saaksid vaadata täiendavaid toote üksikasju ja ostuvalikuid.</span><span class="sxs-lookup"><span data-stu-id="16b93-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="16b93-108">Kiirvaatemoodulit toetavad moodulid [tootekogum](product-collection-module-overview.md) ja [otsingutulemused](search-result-module.md).</span><span class="sxs-lookup"><span data-stu-id="16b93-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16b93-109">Kiirvaatemoodul on saadaval alates Commerce'i versioonist 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="16b93-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="16b93-110">Järgmisel illustratsioonil on näide toodete loendi lehe kiirvaate moodulist.</span><span class="sxs-lookup"><span data-stu-id="16b93-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Toodete loendi lehe kiirvaate mooduli näide](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="16b93-112">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="16b93-112">Module properties</span></span>

<span data-ttu-id="16b93-113">Kiirvaate moodul toetab mõningaid samu funktsioone nagu ostuboksi moodul.</span><span class="sxs-lookup"><span data-stu-id="16b93-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="16b93-114">Seega on kiirvaate mooduli atribuudid sarnased ostukasti mooduli atribuutidega.</span><span class="sxs-lookup"><span data-stu-id="16b93-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="16b93-115">Atribuut</span><span class="sxs-lookup"><span data-stu-id="16b93-115">Property</span></span> | <span data-ttu-id="16b93-116">Väärtused</span><span class="sxs-lookup"><span data-stu-id="16b93-116">Values</span></span> | <span data-ttu-id="16b93-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16b93-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="16b93-118">Pealkirja silt</span><span class="sxs-lookup"><span data-stu-id="16b93-118">Heading tag</span></span> | <span data-ttu-id="16b93-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span><span class="sxs-lookup"><span data-stu-id="16b93-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="16b93-120">See atribuut määratleb toote pealkirjale pealkirja sildi.</span><span class="sxs-lookup"><span data-stu-id="16b93-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="16b93-121">Kui kiirvaate moodul on lehe ülaosas, tuleb see atribuut seada väärtusele **H1**, et vastata juurdepääsetavuse standarditele.</span><span class="sxs-lookup"><span data-stu-id="16b93-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="16b93-122">Luba kohandatud hind</span><span class="sxs-lookup"><span data-stu-id="16b93-122">Allow custom price</span></span> | <span data-ttu-id="16b93-123">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="16b93-123">**True** or **False**</span></span> | <span data-ttu-id="16b93-124">Kui atribuudi väärtuseks on seatud **Tõene**, saab kasutaja sisestada kohandatud hinna.</span><span class="sxs-lookup"><span data-stu-id="16b93-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="16b93-125">Vähim hind</span><span class="sxs-lookup"><span data-stu-id="16b93-125">Minimum price</span></span> | <span data-ttu-id="16b93-126">Täisarv</span><span class="sxs-lookup"><span data-stu-id="16b93-126">Integer</span></span> | <span data-ttu-id="16b93-127">See atribuut on rakendatav ainult siis, kui atribuut **Luba kohandatud hind** on seatud väärtusele **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="16b93-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="16b93-128">Sellega määratletakse minimaalne hind, mille kasutaja saab sisestada (nt $1).</span><span class="sxs-lookup"><span data-stu-id="16b93-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="16b93-129">Suurim hind</span><span class="sxs-lookup"><span data-stu-id="16b93-129">Maximum price</span></span> | <span data-ttu-id="16b93-130">Täisarv</span><span class="sxs-lookup"><span data-stu-id="16b93-130">Integer</span></span> | <span data-ttu-id="16b93-131">See atribuut on rakendatav ainult siis, kui atribuut **Luba kohandatud hind** on seatud väärtusele **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="16b93-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="16b93-132">Sellega määratletakse maksimaalne hind, mille kasutaja saab sisestada (nt $1,000).</span><span class="sxs-lookup"><span data-stu-id="16b93-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="16b93-133">Commerce'i saidiehitaja sätted</span><span class="sxs-lookup"><span data-stu-id="16b93-133">Commerce site builder settings</span></span>

<span data-ttu-id="16b93-134">Nagu ostukasti moodul, järgib ka kiirvaate moodul sätteid jaotises **Saidisätted \> Laiendused \> Toote ostukorvi lisamine**.</span><span class="sxs-lookup"><span data-stu-id="16b93-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="16b93-135">Siiski, ignoreeritakse sätet **Liigu ostukorvi lehele**, sest see ei vasta kiirvaate mooduli eesmärgile, mis on võimaldada kasutajatel sirvida mitmeid tooteid loendilehel ja lisada neid ostukorvi ilma loendilehelt eemale minemiseta.</span><span class="sxs-lookup"><span data-stu-id="16b93-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="16b93-136">Tootekogumi moodulile kiirvaate mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="16b93-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="16b93-137">Kiirvaatemoodulit saab lisada tootekogumi ja otsingutulemuste moodulitele.</span><span class="sxs-lookup"><span data-stu-id="16b93-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="16b93-138">Tootekogumi moodulile kiirvaatemooduli lisamisekd Commerce'i saidiehitajas toimige jägmiselt.</span><span class="sxs-lookup"><span data-stu-id="16b93-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="16b93-139">Avage **Lehed** ja seejärel valige Fabrikami saidi avaleht.</span><span class="sxs-lookup"><span data-stu-id="16b93-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="16b93-140">Avage avalehel mistahes **Tootekogum**, valige kolmikpunkt (**...**) ja seejärel valige **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="16b93-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="16b93-141">Valige dialoogiboksis **Lisa moodul** moodul **Kiirvaade** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="16b93-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="16b93-142">Valige mooduli **Kiirvaade** atribuutide paanil **Pealkiri**.</span><span class="sxs-lookup"><span data-stu-id="16b93-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="16b93-143">Seadistage dialoogiboksis **Pealkiri** väli **Pealkirja aste** väärtusele **H2** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="16b93-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="16b93-144">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="16b93-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="16b93-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="16b93-145">Additional resources</span></span>

[<span data-ttu-id="16b93-146">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="16b93-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="16b93-147">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="16b93-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="16b93-148">Tootekogumi moodul</span><span class="sxs-lookup"><span data-stu-id="16b93-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="16b93-149">Otsingutulemuste moodul</span><span class="sxs-lookup"><span data-stu-id="16b93-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
