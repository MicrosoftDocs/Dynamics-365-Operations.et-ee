---
title: Lingirea moodul
description: See teema hõlmab lingirea mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: ec9f5c72b03d9fd76055369e24491db5c7633cdf
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517156"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="505d3-103">Lingirea moodul</span><span class="sxs-lookup"><span data-stu-id="505d3-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="505d3-104">See teema hõlmab lingirea mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="505d3-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="505d3-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="505d3-105">Overview</span></span>

<span data-ttu-id="505d3-106">Lingirea mooduleid kasutatakse saidi lehtede teisese navigeerimise võimaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="505d3-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="505d3-107">Tavaliselt kuvatakse need lehe ülaosas päise all.</span><span class="sxs-lookup"><span data-stu-id="505d3-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="505d3-108">Kuigi lingirea mooduleid saab lisada igale lehele, kasutatakse neid kõige sagedamini toote üksikasjade lehtedel, et kuvada toote kategooriahierarhiat ja pakkuda kiiret võimalust saidil navigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="505d3-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="505d3-109">Lingirea moodulit saab kasutada ka lingi „Tagasi tulemuste juurde“ kuvamiseks, kui kasutajad avavad otsingus või loendilehel toote üksikasjade lehe.</span><span class="sxs-lookup"><span data-stu-id="505d3-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="505d3-110">Nii saavad kasutajad kiiresti filtreeritud loendilehele tagasi pöörduda ning jätkata ostlemist.</span><span class="sxs-lookup"><span data-stu-id="505d3-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="505d3-111">Tootekategooria kontekstiga lehtedel, nagu näiteks toote üksikasjade lehed ja kategooria lehed, kuvavad lingirea moodulid kategooriahierarhiat.</span><span class="sxs-lookup"><span data-stu-id="505d3-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="505d3-112">Kategooria kontekstita lehtedel kuvavad lingirea moodulid vaikimisi **&lt;Saidi juur&gt; / &lt;Praegune leht&gt;**.</span><span class="sxs-lookup"><span data-stu-id="505d3-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="505d3-113">Lisaks saab lingirea mooduleid teist tüüpi saidilehtedel käsitsi konfigureerida, et kuvada saidil konkreetsete lehtede linke.</span><span class="sxs-lookup"><span data-stu-id="505d3-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="505d3-114">Lingirea moodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="505d3-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="505d3-115">Järgmisel pildil on näidatud lingirea mooduli näide, kus on toodud toote üksikasjade lehe kategooriahierarhia.</span><span class="sxs-lookup"><span data-stu-id="505d3-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Lingirea mooduli näide](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="505d3-117">Lingirea mooduli sätted</span><span class="sxs-lookup"><span data-stu-id="505d3-117">Breadcrumb module settings</span></span>

<span data-ttu-id="505d3-118">Lingirea moodul tugineb sättele **Lingirea kuvamistüüp toote üksikasjade lehel**, mis on määratletud saidiehitaja jaotises **Saidi sätted \> Laiendused**.</span><span class="sxs-lookup"><span data-stu-id="505d3-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="505d3-119">Sellel sättel on kolm võimalikku väärtust.</span><span class="sxs-lookup"><span data-stu-id="505d3-119">This setting has three possible values:</span></span>

- <span data-ttu-id="505d3-120">**Kuva kategooriahierarhia** – kui see väärtus on valitud, kuvatakse lingirea moodulis toote üksikasjade lehel vaadatava toote terviklik kategooriahierarhia.</span><span class="sxs-lookup"><span data-stu-id="505d3-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="505d3-121">**Kuva tagasi tulemuste juurde** – kui see väärtus on valitud, kuvab lingirea moodul toote üksikasjade lehel linki „Tagasi tulemuste juurde“, juhul kui kasutaja on avanud toote üksikasjade lingi moodulist, mis võimaldab lingi „Tagasi tulemuste juurde“ kuvamist.</span><span class="sxs-lookup"><span data-stu-id="505d3-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="505d3-122">See funktsioon on saadaval juhul, kui kasutajad navigeerivad kategooria, otsingu, loendi ja soovituste loendi lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="505d3-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="505d3-123">Selle funktsionaalsuse toetamiseks on tootekogumi ja otsingutulemuste moodulitel atribuut nimega **Luba toote üksikasjade lehel tagasi tulemuste juurde**.</span><span class="sxs-lookup"><span data-stu-id="505d3-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="505d3-124">See atribuut annab teile paindlikkuse määratleda, millised moodulid peaks toetama toote üksikasjade lehel lingi „Tagasi tulemuste juurde“ funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="505d3-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="505d3-125">Näiteks kui lingirea mooduli sätte **Lingirea kuvamistüüp toote üksikasjade lehel** jaoks on valitud suvand **Kuva tagasi tulemuste juurde** ja otsingulehe otsingutulemuste mooduli jaoks on valitud suvand **Luba toote üksikasjade lehel tagasi tulemuste juurde**, siis kuvatakse link „Tagasi tulemuste juurde“, kui kasutaja navigeerib otsingulehelt toote üksikasjade lehele.</span><span class="sxs-lookup"><span data-stu-id="505d3-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="505d3-126">**Kuva kategooriahierarhia ja tagasi tulemuste juurde** – see väärtus on eelmise kahe kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="505d3-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="505d3-127">Kui see väärtus on valitud, siis kuvab lingirea moodul toote üksikasjade lehel nii terviklikku kategooriahierarhiat kui ka linki „Tagasi tulemuste juurde“ (kui see on konfigureeritud).</span><span class="sxs-lookup"><span data-stu-id="505d3-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="505d3-128">Need sätted on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="505d3-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="505d3-129">Kui värskendate rakenduse Dynamics 365 Commerce varasemast versioonist, peate faili appsettings.json käsitsi värskendama.</span><span class="sxs-lookup"><span data-stu-id="505d3-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="505d3-130">Faili appsettings.json värskendamise juhised leiate teemast [SDK ja mooduliteegi värskendused](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="505d3-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="505d3-131">Lingirea mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="505d3-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="505d3-132">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="505d3-132">Property name</span></span> | <span data-ttu-id="505d3-133">Väärtused</span><span class="sxs-lookup"><span data-stu-id="505d3-133">Values</span></span> | <span data-ttu-id="505d3-134">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="505d3-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="505d3-135">Juur</span><span class="sxs-lookup"><span data-stu-id="505d3-135">Root</span></span> | <span data-ttu-id="505d3-136">Tekst või link</span><span class="sxs-lookup"><span data-stu-id="505d3-136">Text or link</span></span>| <span data-ttu-id="505d3-137">See valikuline atribuut määratleb lingirea saidijuure jaoks lingi teksti ja lingi sihtkoha.</span><span class="sxs-lookup"><span data-stu-id="505d3-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="505d3-138">Kui atribuut ei ole konfigureeritud, siis juurt ei määratleta.</span><span class="sxs-lookup"><span data-stu-id="505d3-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="505d3-139">Lingirea link</span><span class="sxs-lookup"><span data-stu-id="505d3-139">Breadcrumb link</span></span> | <span data-ttu-id="505d3-140">Seos</span><span class="sxs-lookup"><span data-stu-id="505d3-140">Link</span></span> | <span data-ttu-id="505d3-141">See valikuline atribuut määratleb käsitsi konfigureeritud lingirea lingid, kui need lingid on nõutud.</span><span class="sxs-lookup"><span data-stu-id="505d3-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="505d3-142">Lingid kuvatakse selles järjekorras, nagu need on loetletud.</span><span class="sxs-lookup"><span data-stu-id="505d3-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="505d3-143">Lingirea mooduli lisamine uuele lehele</span><span class="sxs-lookup"><span data-stu-id="505d3-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="505d3-144">Toote üksikasjade lehele lingirea mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="505d3-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="505d3-145">Avage **Saidi sätted \> Laiendused** ja seejärel valige sätte **Lingirea kuvamistüüp PDP-s** jaoks **Kuva kategooriahierarhia**.</span><span class="sxs-lookup"><span data-stu-id="505d3-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="505d3-146">Avage **Mallid** ja seejärel valige toote üksikasjade lehe mall.</span><span class="sxs-lookup"><span data-stu-id="505d3-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="505d3-147">Valige ostukasti moodulit sisaldavas pesas **Konteiner** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="505d3-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="505d3-148">Valige dialoogiboksis **Lisa moodul** moodul **Lingirida** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="505d3-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="505d3-149">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="505d3-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="505d3-150">Avage **Lehed** ning avage toote üksikasjade lehe malli kasutav toote üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="505d3-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="505d3-151">Kui toote üksikasjade lehte ei ole veel olemas, siis looge see.</span><span class="sxs-lookup"><span data-stu-id="505d3-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="505d3-152">Valige ostukasti moodulit sisaldavas pesas **Konteiner** kolmikpunkt (**...**) ja seejärel **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="505d3-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="505d3-153">Valige dialoogiboksis **Lisa moodul** moodul **Lingirida** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="505d3-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="505d3-154">Valige pesas **Lingirida** toodud atribuutide paanilt **Juur**, valige **Lingi tekst**.</span><span class="sxs-lookup"><span data-stu-id="505d3-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="505d3-155">Valige dialoogiboksis **Lingi tekst** suvand **Avaleht** ja seejärel valige jaotises **Lingi sihtkoht** suvand **Lisa link**.</span><span class="sxs-lookup"><span data-stu-id="505d3-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="505d3-156">Valige lingirea juure jaoks link dialoogiboksis **Lisa link** ning valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="505d3-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="505d3-157">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="505d3-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="505d3-158">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="505d3-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="505d3-159">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="505d3-159">Additional resources</span></span>

[<span data-ttu-id="505d3-160">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="505d3-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="505d3-161">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="505d3-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="505d3-162">Saidi valija moodul</span><span class="sxs-lookup"><span data-stu-id="505d3-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="505d3-163">Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="505d3-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="505d3-164">Tootekogumi moodulid</span><span class="sxs-lookup"><span data-stu-id="505d3-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="505d3-165">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="505d3-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="505d3-166">SDK ja mooduliteegi värskendused</span><span class="sxs-lookup"><span data-stu-id="505d3-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
