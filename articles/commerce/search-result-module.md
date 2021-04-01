---
title: Otsingutulemuste moodul
description: See teema hõlmab otsingutulemuste mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5d852fe1a81b1e42484bc49ae136ef8613a2d3a5
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254765"
---
# <a name="search-results-module"></a><span data-ttu-id="cd8e5-103">Otsingutulemuste moodul</span><span class="sxs-lookup"><span data-stu-id="cd8e5-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="cd8e5-104">See teema hõlmab otsingutulemuste mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cd8e5-105">Otsingutulemuste moodul annab tulemuseks tooteotsingu ja loendi tootele kohaldatavatest filtritest.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="cd8e5-106">Dynamics 365 Commerce'i saitide otsingumooduleid saab kasutada järgmiste stsenaariumidega saitide renderdamiseks.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="cd8e5-107">Kasutajaotsingu käivitatud otsingutulemused</span><span class="sxs-lookup"><span data-stu-id="cd8e5-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="cd8e5-108">Otsingutulemused, mis näitavad kindlat tootekomplekti, nt "Osta sarnaseid tooteid"</span><span class="sxs-lookup"><span data-stu-id="cd8e5-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="cd8e5-109">Kindlasse kategooriasse kuuluvate toodete loendid</span><span class="sxs-lookup"><span data-stu-id="cd8e5-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="cd8e5-110">Lisateavet kategooria ja otsingutulemuste lehtede kohta vt jaotisest [Vaikekategooria sihtleht ja otsingutulemuste lehe ülevaade](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cd8e5-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="cd8e5-111">Järgmisel joonisel on kujutatud Fabrikami saidi kategooria otsingutulemuste leht.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Otsingutulemuste lehe näide Fabrikami saidil](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="cd8e5-113">Otsingutulemuste mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="cd8e5-113">Search results module properties</span></span>

<span data-ttu-id="cd8e5-114">Järgmises tabelis loetletakse otsingutulemimoodulite atribuudid koos nende väärtuste ja kirjeldustega.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="cd8e5-115">Atribuut</span><span class="sxs-lookup"><span data-stu-id="cd8e5-115">Property</span></span> | <span data-ttu-id="cd8e5-116">Väärtused</span><span class="sxs-lookup"><span data-stu-id="cd8e5-116">Values</span></span> | <span data-ttu-id="cd8e5-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cd8e5-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="cd8e5-118">Kaupu lehekülje kohta</span><span class="sxs-lookup"><span data-stu-id="cd8e5-118">Items per page</span></span> | <span data-ttu-id="cd8e5-119">Täisarv</span><span class="sxs-lookup"><span data-stu-id="cd8e5-119">Integer</span></span> | <span data-ttu-id="cd8e5-120">Kaupade arv, mis tuleb igal lehel kuvada.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="cd8e5-121">Luba PDP naasmine</span><span class="sxs-lookup"><span data-stu-id="cd8e5-121">Allow back on PDP</span></span> | <span data-ttu-id="cd8e5-122">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cd8e5-122">**True** or **False**</span></span> | <span data-ttu-id="cd8e5-123">Kui see atribuut on seatud väärtusele **Tõene**, siis kui kasutaja valib otsingutulemuste lehel toote, kuvatakse avatud toote üksikasjade lehe (DPD) lingireal link "Tagasi tulemuste juurde".</span><span class="sxs-lookup"><span data-stu-id="cd8e5-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="cd8e5-124">Laienda piiritlusatribuudid</span><span class="sxs-lookup"><span data-stu-id="cd8e5-124">Expand Refiners</span></span> | <span data-ttu-id="cd8e5-125">**Kõik**, **1**, **2**, **3**, or **4**</span><span class="sxs-lookup"><span data-stu-id="cd8e5-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="cd8e5-126">Parimate filtrite arv, mis tuleks lehe laadimisel laiendada.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="cd8e5-127">Näiteks kui selle atribuudi väärtuseks on seatud **3**, laiendatakse leheküljel esimesed kolm filtrit.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="cd8e5-128">Peida kategooriahierarhia kuvamine</span><span class="sxs-lookup"><span data-stu-id="cd8e5-128">Hide category hierarchy display</span></span> | <span data-ttu-id="cd8e5-129">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cd8e5-129">**True** or **False**</span></span> | <span data-ttu-id="cd8e5-130">Kui atribuudi väärtuseks on seatud **Tõene**, on leheküljel kategooriahierarhia kuvamine peidetud.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="cd8e5-131">Kui kasutate kategooria hierarhia kuvamiseks [lingirea moodulit](add-breadcrumb.md), peaks see atribuut olema seasitatud olekusse **Tõene**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="cd8e5-132">Tooteatribuutide kaasamine otsingutulemitesse</span><span class="sxs-lookup"><span data-stu-id="cd8e5-132">Include product attributes in search results</span></span> | <span data-ttu-id="cd8e5-133">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cd8e5-133">**True** or **False**</span></span> | <span data-ttu-id="cd8e5-134">Kui selle atribuudi väärtuseks on seadistatud **Tõene**, tagastatakse otsingutulemustes toodete atribuudid.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="cd8e5-135">Kuigi neid atribuute saab Commerce'i saidil kuvada, on vajalik laiendus.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="cd8e5-136">Kuva sidusettevõtte hinnad</span><span class="sxs-lookup"><span data-stu-id="cd8e5-136">Show affiliation prices</span></span> | <span data-ttu-id="cd8e5-137">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cd8e5-137">**True** or **False**</span></span> | <span data-ttu-id="cd8e5-138">Kui selle atribuudi väärtuseks on seatud **Tõene**, kuvatakse toote allahindluse hinnad otsingutulemustes, kui lehte sirvib sisselogitud kasutaja.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="cd8e5-139">Rakenduse Dynamics 365 Commerce väljalaskes 10.0.16 ja uuemas saab konfiguratsiooni **Kuva allahindluse hinnad** kasutada allahindluse hindade lehel näitamiseks.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="cd8e5-140">Toetatud moodulid</span><span class="sxs-lookup"><span data-stu-id="cd8e5-140">Supported modules</span></span>

<span data-ttu-id="cd8e5-141">Otsingutulemuse moodul toetab [kiirvaate moodulit](quick-view-module.md), mis võimaldab kasutajatel otsingutulemuste lehelt tooteteavet vaadata ja lisada asju ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="cd8e5-142">Otsingutulemuste mooduli lisamine kategoorialehele</span><span class="sxs-lookup"><span data-stu-id="cd8e5-142">Add a search results module to a category page</span></span>

<span data-ttu-id="cd8e5-143">Otsingutulemuste mooduli lisamiseks kategoorialehele toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="cd8e5-144">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="cd8e5-145">Sisestage dialoogiboksi **Uus mall** nimi **Otsingutulemus** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="cd8e5-146">Valige lahtris **Keha** kolmikpunkt (...) ja seejärel valige **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cd8e5-147">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cd8e5-148">Valige lahtris **Peamine** moodulis **Vaikeleht** kolmikpunkt (...) ja seejärel valige **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cd8e5-149">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cd8e5-150">Valige lahtris **Konteiner** kolmikpunkt (…) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cd8e5-151">Valige dialoogiboksis **Lisa moodul** moodul **Lingirida** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cd8e5-152">Sisestage atribuutide paanile **Lingirida** väärtus **1** üksuse **Miinimum esinemiskorrad** puhul.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="cd8e5-153">Valige lahtris **Konteiner** kolmikpunkt (…) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cd8e5-154">Valige dialoogiboksis **Lisa moodul** moodul **Otsingutulemused** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cd8e5-155">Sisestage atribuutide paanil **Otsingutulemused** väärtus **1** üksuse **Miiniumu esinemiskorrad** puhul ja seejärel seadistage mistahes muud vajalikud otsingutulemuste mooduli atribuudid.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="cd8e5-156">Mallis nende atribuutide seadmisega tagate, et konkreetse kategooria lehekülje kohandused kaasavad need sätted automaatselt.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="cd8e5-157">Valige **Lõpeta redigeerimine** ja seejärel valige malli avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="cd8e5-158">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="cd8e5-159">Valige dialoogiboksis **Malli valik** loodud **Otsingutulemuste** mall, sisestage **Kategooria leht** üksuse **Lehekülje nimi** jaoks ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="cd8e5-160">Kuna kõik väärtused on mallis seadistatud, on lehekülg avaldamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="cd8e5-161">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="cd8e5-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd8e5-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cd8e5-162">Additional resources</span></span>

[<span data-ttu-id="cd8e5-163">Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="cd8e5-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="cd8e5-164">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="cd8e5-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cd8e5-165">Kiirvaatemoodul</span><span class="sxs-lookup"><span data-stu-id="cd8e5-165">Quick view module</span></span>](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]