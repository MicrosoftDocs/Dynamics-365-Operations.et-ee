---
title: Toote üksikasjade lehe ülevaade
description: See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792215"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="1afba-103">Toote üksikasjade lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="1afba-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1afba-104">See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1afba-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1afba-105">PDP annab toote kohta üksikasjalikku teavet ja laseb klientidel valida toote suvandid, nagu suurus, stiil ja värv.</span><span class="sxs-lookup"><span data-stu-id="1afba-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="1afba-106">PDP peaks esitlema kogu toote teavet, mis on kliendile vajalik ostuotsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="1afba-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="1afba-107">Järgmisel joonisel on toodud PDP näide.</span><span class="sxs-lookup"><span data-stu-id="1afba-107">The following illustration shows an example of a PDP.</span></span>

![Toote üksikasjade lehe näide](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="1afba-109">Päise ja jaluse moodulid</span><span class="sxs-lookup"><span data-stu-id="1afba-109">Header and footer modules</span></span>

<span data-ttu-id="1afba-110">PDP ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehekülgi, mida jaemüüja soovib klientidele sirvimiseks pakkuda.</span><span class="sxs-lookup"><span data-stu-id="1afba-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="1afba-111">Lehe allosas on jalus, mis sisaldab kiireid linke erinevatele teemadele, mis võivad klientidele huvi pakkuda.</span><span class="sxs-lookup"><span data-stu-id="1afba-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="1afba-112">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="1afba-112">Buy box module</span></span>

<span data-ttu-id="1afba-113">PDP kõige olulisem moodul on ostukasti moodul, mis kuvatakse lehe põhijaotises esimese üksusena.</span><span class="sxs-lookup"><span data-stu-id="1afba-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="1afba-114">Ostukasti moodul kuvab olulise tooteteabe, nagu tootenimetus, toote kirjeldus, toote hind, toote pildid ja toote hinnangud.</span><span class="sxs-lookup"><span data-stu-id="1afba-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="1afba-115">Ostukasti moodul võimaldab kliendil valida toote suvandid (nt suurus, stiil ja värv) ja lisada toote ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="1afba-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="1afba-116">Samuti võimaldab see kliendil toote veebis osta ja sellele kauplusesse järele minna.</span><span class="sxs-lookup"><span data-stu-id="1afba-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="1afba-117">Veebis ostes ja kauplusesse järele minemise moodul kasutab integratsiooni Bing Mapsi rakenduse programmeerimise liidestega (API-dega), et leida lähedalasuvaid kauplusi või kauplusi teises kliendi määratud asukohas.</span><span class="sxs-lookup"><span data-stu-id="1afba-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="1afba-118">Ostukasti moodul nõuab toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="1afba-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="1afba-119">See ID tuletatakse lehekülje kontekstist.</span><span class="sxs-lookup"><span data-stu-id="1afba-119">This ID is derived from the page context.</span></span> <span data-ttu-id="1afba-120">Kui ostukasti moodul lisatakse lehele, kus lehekülje kontekst ei sisalda toote ID-d, ei renderda see teavet õigesti.</span><span class="sxs-lookup"><span data-stu-id="1afba-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="1afba-121">Toote spetsifikatsioonide moodul</span><span class="sxs-lookup"><span data-stu-id="1afba-121">Product specifications module</span></span>

<span data-ttu-id="1afba-122">Toote spetsifikatsioonide moodulit saab kasutada toote kohta lisateabe esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="1afba-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="1afba-123">Need üksikasjad võetakse toote atribuutidest rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="1afba-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="1afba-124">Toote spetsifikatsioonide moodul näitab iga atribuuti, mille **nähtavuse** väärtuseks on seatud **tõene**.</span><span class="sxs-lookup"><span data-stu-id="1afba-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="1afba-125">See nõuab toote ID-d toote atribuutide toomiseks.</span><span class="sxs-lookup"><span data-stu-id="1afba-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="1afba-126">Soovituste moodul</span><span class="sxs-lookup"><span data-stu-id="1afba-126">Recommendations module</span></span>

<span data-ttu-id="1afba-127">Soovituste moodul on oluline moodul PDP-s.</span><span class="sxs-lookup"><span data-stu-id="1afba-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="1afba-128">Kui kliendid sirvivad tooteid, tuleb neile esitada rohkem toote võimalusi, et nad saaksid leida õige toote ja teha ostu.</span><span class="sxs-lookup"><span data-stu-id="1afba-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="1afba-129">Soovitused aitavad klientidel lihtsalt avastada seotud sisu ja jätkata ostlemist.</span><span class="sxs-lookup"><span data-stu-id="1afba-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="1afba-130">Saadaval on eri tüüpi soovituste loendid.</span><span class="sxs-lookup"><span data-stu-id="1afba-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="1afba-131">Loend **Inimestele meeldib ka** põhineb masina õppimisel.</span><span class="sxs-lookup"><span data-stu-id="1afba-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="1afba-132">See kasutab soovituste esitamiseks teiste klientide kannete ajalugu.</span><span class="sxs-lookup"><span data-stu-id="1afba-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="1afba-133">Selle loendi loob soovituste teenus ja see meenutab loendeid "kliendid, kes ostsid selle, ostsid ka...".</span><span class="sxs-lookup"><span data-stu-id="1afba-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="1afba-134">Selle loendi loomiseks on vaja toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="1afba-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="1afba-135">Loendit **Seotud** saab konfigureerida toote jaoks rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="1afba-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="1afba-136">Näiteks pruuni nahast reisikoti puhul saab seotud loendi jaoks konfigureerida rohkem käekotte, mis on nahast või mõeldud reisimiseks.</span><span class="sxs-lookup"><span data-stu-id="1afba-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="1afba-137">Muud tüüpi seostuvaid loendeid, nagu **Aksessuaarid** ja **Rohkem selliseid**, saab konfigureerida samuti rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="1afba-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="1afba-138">Selle loendi loomiseks on vaja toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="1afba-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="1afba-139">Seega, kui see on lisatud avalehele, kus lehekülje kontekst ei sisalda toote ID-d, on loend tühi.</span><span class="sxs-lookup"><span data-stu-id="1afba-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="1afba-140">Algoritmiliselt loodud soovituste loendeid, nagu **Populaarsed**, **Enim müüdud** ja **Uus**, saab kasutada PDP-s.</span><span class="sxs-lookup"><span data-stu-id="1afba-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="1afba-141">Kuigi need loendid ei pruugi olla otse seotud tootega PDP-s, on teisi viise, kuidas aidata klientidel leida tooteid, mis võivad neid huvitada.</span><span class="sxs-lookup"><span data-stu-id="1afba-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="1afba-142">Seda tüüpi loendid ei nõua toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="1afba-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="1afba-143">Need on üldised loendid, mis luuakse saidil olevate ostude põhjal.</span><span class="sxs-lookup"><span data-stu-id="1afba-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="1afba-144">Redaktori loendid on käsitsi kureeritud loendid.</span><span class="sxs-lookup"><span data-stu-id="1afba-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="1afba-145">Näiteks võib jaemüüja otsustada käsitsi kureerida loendi toodetest, mida ta soovib näidata.</span><span class="sxs-lookup"><span data-stu-id="1afba-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="1afba-146">Hinnangute ja arvustuste moodulid</span><span class="sxs-lookup"><span data-stu-id="1afba-146">Ratings and reviews modules</span></span>

<span data-ttu-id="1afba-147">Arvustuste kuvamiseks ja lisamiseks saab kasutada kolme moodulit.</span><span class="sxs-lookup"><span data-stu-id="1afba-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="1afba-148">**Arvustused** – see moodul loetleb teiste klientide esitatud hinnangud ja arvustused.</span><span class="sxs-lookup"><span data-stu-id="1afba-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="1afba-149">Kliendid saavad arvustusi sortida ja filtreerida.</span><span class="sxs-lookup"><span data-stu-id="1afba-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="1afba-150">See moodul võimaldab klientidel lisaks näidata, kas arvustus meeldib neile või ei meeldi, ja teavitada probleemidest.</span><span class="sxs-lookup"><span data-stu-id="1afba-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="1afba-151">**Arvustuse kirjutamine** – see moodul võimaldab kliendil kirjutada oma tootearvustusi.</span><span class="sxs-lookup"><span data-stu-id="1afba-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="1afba-152">**Hinnangute histogramm** – see moodul sisaldab histogrammi, mis näitab toote hinnangute suundumust.</span><span class="sxs-lookup"><span data-stu-id="1afba-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="1afba-153">Lisateavet leiate jaotisest [Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1afba-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="1afba-154">Turundusmoodulid</span><span class="sxs-lookup"><span data-stu-id="1afba-154">Marketing modules</span></span>

<span data-ttu-id="1afba-155">Kui turunduse sisu on konkreetse toote puhul unikaalne, saab mis tahes turunduse moodulit lisada PDP-sse.</span><span class="sxs-lookup"><span data-stu-id="1afba-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="1afba-156">Saate lisada turunduse moodulid PDP-sse lehekülge "rikastades".</span><span class="sxs-lookup"><span data-stu-id="1afba-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="1afba-157">Lisateavet vt teemast [Tootelehe rikastamine](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="1afba-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1afba-158">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1afba-158">Additional resources</span></span>

[<span data-ttu-id="1afba-159">Avalehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="1afba-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="1afba-160">Ostukorvi ja väljaregistreerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="1afba-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="1afba-161">Kontohalduse lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="1afba-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="1afba-162">Toote üksikasjade lehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="1afba-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
