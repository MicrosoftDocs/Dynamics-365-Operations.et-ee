---
title: Toote üksikasjade lehtede ülevaade
description: See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: dbf8f4c1ea479a508f4a0294020b7201b32fe228
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025921"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="d57da-103">Toote üksikasjade lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="d57da-103">Overview of product details pages</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d57da-104">See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d57da-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d57da-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d57da-105">Overview</span></span>

<span data-ttu-id="d57da-106">PDP annab toote kohta üksikasjalikku teavet ja laseb klientidel valida toote suvandid, nagu suurus, stiil ja värv.</span><span class="sxs-lookup"><span data-stu-id="d57da-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="d57da-107">PDP peaks esitlema kogu toote teavet, mis on kliendile vajalik ostuotsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="d57da-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="d57da-108">Järgmisel joonisel on toodud PDP näide.</span><span class="sxs-lookup"><span data-stu-id="d57da-108">The following illustration shows an example of a PDP.</span></span>

![Toote üksikasjade lehe näide](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="d57da-110">Päise ja jaluse moodulid</span><span class="sxs-lookup"><span data-stu-id="d57da-110">Header and footer modules</span></span>

<span data-ttu-id="d57da-111">PDP ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehekülgi, mida jaemüüja soovib klientidele sirvimiseks pakkuda.</span><span class="sxs-lookup"><span data-stu-id="d57da-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="d57da-112">Lehe allosas on jalus, mis sisaldab kiireid linke erinevatele teemadele, mis võivad klientidele huvi pakkuda.</span><span class="sxs-lookup"><span data-stu-id="d57da-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="d57da-113">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="d57da-113">Buy box module</span></span>

<span data-ttu-id="d57da-114">PDP kõige olulisem moodul on ostukasti moodul, mis kuvatakse lehe põhijaotises esimese üksusena.</span><span class="sxs-lookup"><span data-stu-id="d57da-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="d57da-115">Ostukasti moodul kuvab olulise tooteteabe, nagu tootenimetus, toote kirjeldus, toote hind, toote pildid ja toote hinnangud.</span><span class="sxs-lookup"><span data-stu-id="d57da-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="d57da-116">Ostukasti moodul võimaldab kliendil valida toote suvandid (nt suurus, stiil ja värv) ja lisada toote ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="d57da-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="d57da-117">Samuti võimaldab see kliendil toote veebis osta ja sellele kauplusesse järele minna.</span><span class="sxs-lookup"><span data-stu-id="d57da-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="d57da-118">Veebis ostes ja kauplusesse järele minemise moodul kasutab integratsiooni Bing Mapsi rakenduse programmeerimise liidestega (API-dega), et leida lähedalasuvaid kauplusi või kauplusi teises kliendi määratud asukohas.</span><span class="sxs-lookup"><span data-stu-id="d57da-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="d57da-119">Ostukasti moodul nõuab toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="d57da-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="d57da-120">See ID tuletatakse lehekülje kontekstist.</span><span class="sxs-lookup"><span data-stu-id="d57da-120">This ID is derived from the page context.</span></span> <span data-ttu-id="d57da-121">Kui ostukasti moodul lisatakse lehele, kus lehekülje kontekst ei sisalda toote ID-d, ei renderda see teavet õigesti.</span><span class="sxs-lookup"><span data-stu-id="d57da-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="d57da-122">Toote spetsifikatsioonide moodul</span><span class="sxs-lookup"><span data-stu-id="d57da-122">Product specifications module</span></span>

<span data-ttu-id="d57da-123">Toote spetsifikatsioonide moodulit saab kasutada toote kohta lisateabe esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d57da-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="d57da-124">Need üksikasjad võetakse toote atribuutidest rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="d57da-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="d57da-125">Toote spetsifikatsioonide moodul näitab iga atribuuti, mille **nähtavuse** väärtuseks on seatud **tõene**.</span><span class="sxs-lookup"><span data-stu-id="d57da-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="d57da-126">See nõuab toote ID-d toote atribuutide toomiseks.</span><span class="sxs-lookup"><span data-stu-id="d57da-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="d57da-127">Soovituste moodul</span><span class="sxs-lookup"><span data-stu-id="d57da-127">Recommendations module</span></span>

<span data-ttu-id="d57da-128">Soovituste moodul on oluline moodul PDP-s.</span><span class="sxs-lookup"><span data-stu-id="d57da-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="d57da-129">Kui kliendid sirvivad tooteid, tuleb neile esitada rohkem toote võimalusi, et nad saaksid leida õige toote ja teha ostu.</span><span class="sxs-lookup"><span data-stu-id="d57da-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="d57da-130">Soovitused aitavad klientidel lihtsalt avastada seotud sisu ja jätkata ostlemist.</span><span class="sxs-lookup"><span data-stu-id="d57da-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="d57da-131">Saadaval on eri tüüpi soovituste loendid.</span><span class="sxs-lookup"><span data-stu-id="d57da-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="d57da-132">Loend **Inimestele meeldib ka** põhineb masina õppimisel.</span><span class="sxs-lookup"><span data-stu-id="d57da-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="d57da-133">See kasutab soovituste esitamiseks teiste klientide kannete ajalugu.</span><span class="sxs-lookup"><span data-stu-id="d57da-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="d57da-134">Selle loendi loob soovituste teenus ja see meenutab loendeid "kliendid, kes ostsid selle, ostsid ka...".</span><span class="sxs-lookup"><span data-stu-id="d57da-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="d57da-135">Selle loendi loomiseks on vaja toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="d57da-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="d57da-136">Loendit **Seotud** saab konfigureerida toote jaoks rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="d57da-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="d57da-137">Näiteks pruuni nahast reisikoti puhul saab seotud loendi jaoks konfigureerida rohkem käekotte, mis on nahast või mõeldud reisimiseks.</span><span class="sxs-lookup"><span data-stu-id="d57da-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="d57da-138">Muud tüüpi seostuvaid loendeid, nagu **Aksessuaarid** ja **Rohkem selliseid**, saab konfigureerida samuti rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="d57da-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="d57da-139">Selle loendi loomiseks on vaja toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="d57da-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="d57da-140">Seega, kui see on lisatud avalehele, kus lehekülje kontekst ei sisalda toote ID-d, on loend tühi.</span><span class="sxs-lookup"><span data-stu-id="d57da-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="d57da-141">Algoritmiliselt loodud soovituste loendeid, nagu **Populaarsed**, **Enim müüdud** ja **Uus**, saab kasutada PDP-s.</span><span class="sxs-lookup"><span data-stu-id="d57da-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="d57da-142">Kuigi need loendid ei pruugi olla otse seotud tootega PDP-s, on teisi viise, kuidas aidata klientidel leida tooteid, mis võivad neid huvitada.</span><span class="sxs-lookup"><span data-stu-id="d57da-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="d57da-143">Seda tüüpi loendid ei nõua toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="d57da-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="d57da-144">Need on üldised loendid, mis luuakse saidil olevate ostude põhjal.</span><span class="sxs-lookup"><span data-stu-id="d57da-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="d57da-145">Redaktori loendid on käsitsi kureeritud loendid.</span><span class="sxs-lookup"><span data-stu-id="d57da-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="d57da-146">Näiteks võib jaemüüja otsustada käsitsi kureerida loendi toodetest, mida ta soovib näidata.</span><span class="sxs-lookup"><span data-stu-id="d57da-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="d57da-147">Hinnangute ja arvustuste moodulid</span><span class="sxs-lookup"><span data-stu-id="d57da-147">Ratings and reviews modules</span></span>

<span data-ttu-id="d57da-148">Arvustuste kuvamiseks ja lisamiseks saab kasutada kolme moodulit.</span><span class="sxs-lookup"><span data-stu-id="d57da-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="d57da-149">**Arvustused** – see moodul loetleb teiste klientide esitatud hinnangud ja arvustused.</span><span class="sxs-lookup"><span data-stu-id="d57da-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="d57da-150">Kliendid saavad arvustusi sortida ja filtreerida.</span><span class="sxs-lookup"><span data-stu-id="d57da-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="d57da-151">See moodul võimaldab klientidel lisaks näidata, kas arvustus meeldib neile või ei meeldi, ja teavitada probleemidest.</span><span class="sxs-lookup"><span data-stu-id="d57da-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="d57da-152">**Arvustuse kirjutamine** – see moodul võimaldab kliendil kirjutada oma tootearvustusi.</span><span class="sxs-lookup"><span data-stu-id="d57da-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="d57da-153">**Hinnangute histogramm** – see moodul sisaldab histogrammi, mis näitab toote hinnangute suundumust.</span><span class="sxs-lookup"><span data-stu-id="d57da-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="d57da-154">Lisateavet leiate jaotisest [Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d57da-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="d57da-155">Turundusmoodulid</span><span class="sxs-lookup"><span data-stu-id="d57da-155">Marketing modules</span></span>

<span data-ttu-id="d57da-156">Kui turunduse sisu on konkreetse toote puhul unikaalne, saab mis tahes turunduse moodulit lisada PDP-sse.</span><span class="sxs-lookup"><span data-stu-id="d57da-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="d57da-157">Saate lisada turunduse moodulid PDP-sse lehekülge "rikastades".</span><span class="sxs-lookup"><span data-stu-id="d57da-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="d57da-158">Lisateavet vt teemast [Tootelehe rikastamine](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="d57da-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d57da-159">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d57da-159">Additional resources</span></span>

[<span data-ttu-id="d57da-160">Avalehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="d57da-160">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="d57da-161">Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="d57da-161">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="d57da-162">Ostukorvi ja väljaregistreerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="d57da-162">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="d57da-163">Kontohalduse lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="d57da-163">Overview of account management pages</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="d57da-164">Toote üksikasjade lehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="d57da-164">Enrich a product details page</span></span>](enrich-product-page.md)
