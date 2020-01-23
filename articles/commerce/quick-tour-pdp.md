---
title: Toote üksikasjade lehtede ülevaade
description: See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697861"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="ac502-103">Toote üksikasjade lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac502-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ac502-104">See teema annab ülevaate toote üksikasjade lehtedest (PDP-dest) rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ac502-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ac502-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac502-105">Overview</span></span>

<span data-ttu-id="ac502-106">PDP annab toote kohta üksikasjalikku teavet ja laseb klientidel valida toote suvandid, nagu suurus, stiil ja värv.</span><span class="sxs-lookup"><span data-stu-id="ac502-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="ac502-107">PDP peaks esitlema kogu toote teavet, mis on kliendile vajalik ostuotsuse tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="ac502-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="ac502-108">Järgmisel joonisel on toodud PDP näide.</span><span class="sxs-lookup"><span data-stu-id="ac502-108">The following illustration shows an example of a PDP.</span></span>

![Toote üksikasjade lehe näide](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="ac502-110">Päise ja jaluse moodulid</span><span class="sxs-lookup"><span data-stu-id="ac502-110">Header and footer modules</span></span>

<span data-ttu-id="ac502-111">PDP ülaosas on päis, mis näitab kõiki tootekategooriaid ja teisi lehekülgi, mida jaemüüja soovib klientidele sirvimiseks pakkuda.</span><span class="sxs-lookup"><span data-stu-id="ac502-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="ac502-112">Lehe allosas on jalus, mis sisaldab kiireid linke erinevatele teemadele, mis võivad klientidele huvi pakkuda.</span><span class="sxs-lookup"><span data-stu-id="ac502-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="ac502-113">Ostukasti moodul</span><span class="sxs-lookup"><span data-stu-id="ac502-113">Buy box module</span></span>

<span data-ttu-id="ac502-114">Kõige olulisem moodul PDP-s on ostukasti moodul.</span><span class="sxs-lookup"><span data-stu-id="ac502-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="ac502-115">Seetõttu on see esimene üksus lehe põhijaotises.</span><span class="sxs-lookup"><span data-stu-id="ac502-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="ac502-116">Ostukasti moodul on konteineri moodul ja see majutab mitu moodulit, mis sisaldavad kõige olulisemat teavet toote kohta.</span><span class="sxs-lookup"><span data-stu-id="ac502-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="ac502-117">See teave sisaldab toote nime, toote pilte, kirjeldust, hinda ja toote hinnanguid.</span><span class="sxs-lookup"><span data-stu-id="ac502-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="ac502-118">Ostukasti moodul võimaldab kliendil valida toote suvandid (nt suurus, stiil ja värv) ja lisada toote ostukorvi.</span><span class="sxs-lookup"><span data-stu-id="ac502-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="ac502-119">Samuti võimaldab see kliendil toote veebis osta ja sellele kauplusesse järele minna.</span><span class="sxs-lookup"><span data-stu-id="ac502-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="ac502-120">Veebis ostes ja kauplusesse järele minemise moodul kasutab integratsiooni Bing Mapsi rakenduse programmeerimise liidestega (API-dega), et leida lähedalasuvaid kauplusi või kauplusi teises kliendi määratud asukohas.</span><span class="sxs-lookup"><span data-stu-id="ac502-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="ac502-121">Ostukasti moodul nõuab toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="ac502-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="ac502-122">See ID tuletatakse lehekülje kontekstist.</span><span class="sxs-lookup"><span data-stu-id="ac502-122">This ID is derived from the page context.</span></span> <span data-ttu-id="ac502-123">Kui ostukasti moodul lisatakse lehele, kus lehekülje kontekst ei sisalda toote ID-d, ei renderda see teavet õigesti.</span><span class="sxs-lookup"><span data-stu-id="ac502-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="ac502-124">Toote spetsifikatsioonide moodul</span><span class="sxs-lookup"><span data-stu-id="ac502-124">Product specifications module</span></span>

<span data-ttu-id="ac502-125">Toote spetsifikatsioonide moodulit saab kasutada toote kohta lisateabe esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="ac502-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="ac502-126">Need üksikasjad võetakse toote atribuutidest rakenduses Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="ac502-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="ac502-127">Toote spetsifikatsioonide moodul näitab iga atribuuti, mille **nähtavuse** väärtuseks on seatud **tõene**.</span><span class="sxs-lookup"><span data-stu-id="ac502-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="ac502-128">See nõuab toote ID-d toote atribuutide toomiseks.</span><span class="sxs-lookup"><span data-stu-id="ac502-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="ac502-129">Soovituste moodul</span><span class="sxs-lookup"><span data-stu-id="ac502-129">Recommendations module</span></span>

<span data-ttu-id="ac502-130">Soovituste moodul on oluline moodul PDP-s.</span><span class="sxs-lookup"><span data-stu-id="ac502-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="ac502-131">Kui kliendid sirvivad tooteid, tuleb neile esitada rohkem toote võimalusi, et nad saaksid leida õige toote ja teha ostu.</span><span class="sxs-lookup"><span data-stu-id="ac502-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="ac502-132">Soovitused aitavad klientidel lihtsalt avastada seotud sisu ja jätkata ostlemist.</span><span class="sxs-lookup"><span data-stu-id="ac502-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="ac502-133">Saadaval on eri tüüpi soovituste loendid.</span><span class="sxs-lookup"><span data-stu-id="ac502-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="ac502-134">Loend **Inimestele meeldib ka** põhineb masina õppimisel.</span><span class="sxs-lookup"><span data-stu-id="ac502-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="ac502-135">See kasutab soovituste esitamiseks teiste klientide kannete ajalugu.</span><span class="sxs-lookup"><span data-stu-id="ac502-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="ac502-136">Selle loendi loob soovituste teenus ja see meenutab loendeid "kliendid, kes ostsid selle, ostsid ka...".</span><span class="sxs-lookup"><span data-stu-id="ac502-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="ac502-137">Selle loendi loomiseks on vaja toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="ac502-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="ac502-138">Loendit **Seotud** saab konfigureerida toote jaoks jaemüügis.</span><span class="sxs-lookup"><span data-stu-id="ac502-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="ac502-139">Näiteks pruuni nahast reisikoti puhul saab seotud loendi jaoks konfigureerida rohkem käekotte, mis on nahast või mõeldud reisimiseks.</span><span class="sxs-lookup"><span data-stu-id="ac502-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="ac502-140">Muud tüüpi seostuvaid loendeid, nagu **Aksessuaarid** ja **Rohkem selliseid** saab konfigureerida ka jaemüügis.</span><span class="sxs-lookup"><span data-stu-id="ac502-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="ac502-141">Selle loendi loomiseks on vaja toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="ac502-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="ac502-142">Seega, kui see on lisatud avalehele, kus lehekülje kontekst ei sisalda toote ID-d, on loend tühi.</span><span class="sxs-lookup"><span data-stu-id="ac502-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="ac502-143">Algoritmiliselt loodud soovituste loendeid, nagu **Populaarsed**, **Enim müüdud** ja **Uus**, saab kasutada PDP-s.</span><span class="sxs-lookup"><span data-stu-id="ac502-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="ac502-144">Kuigi need loendid ei pruugi olla otse seotud tootega PDP-s, on teisi viise, kuidas aidata klientidel leida tooteid, mis võivad neid huvitada.</span><span class="sxs-lookup"><span data-stu-id="ac502-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="ac502-145">Seda tüüpi loendid ei nõua toote ID-d.</span><span class="sxs-lookup"><span data-stu-id="ac502-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="ac502-146">Need on üldised loendid, mis luuakse saidil olevate ostude põhjal.</span><span class="sxs-lookup"><span data-stu-id="ac502-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="ac502-147">Redaktori loendid on käsitsi kureeritud loendid.</span><span class="sxs-lookup"><span data-stu-id="ac502-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="ac502-148">Näiteks võib jaemüüja otsustada käsitsi kureerida loendi toodetest, mida ta soovib näidata.</span><span class="sxs-lookup"><span data-stu-id="ac502-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="ac502-149">Hinnangute ja arvustuste moodul</span><span class="sxs-lookup"><span data-stu-id="ac502-149">Ratings and reviews module</span></span>

<span data-ttu-id="ac502-150">Hinnangute ja arvustuste moodulis kuvatakse teiste klientide esitatud hinnangud ja arvustused.</span><span class="sxs-lookup"><span data-stu-id="ac502-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="ac502-151">Samuti võimaldab see kliendil kirjutada toote kohta oma arvustuse.</span><span class="sxs-lookup"><span data-stu-id="ac502-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="ac502-152">Lisaks sisaldab see histogrammi, mis näitab toote hinnangute trendi.</span><span class="sxs-lookup"><span data-stu-id="ac502-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="ac502-153">Lisateavet leiate jaotisest [Hinnangute ja arvustuste ülevaade](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ac502-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="ac502-154">Turundusmoodulid</span><span class="sxs-lookup"><span data-stu-id="ac502-154">Marketing modules</span></span>

<span data-ttu-id="ac502-155">Kui turunduse sisu on konkreetse toote puhul unikaalne, saab mis tahes turunduse moodulit lisada PDP-sse.</span><span class="sxs-lookup"><span data-stu-id="ac502-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="ac502-156">Saate lisada turunduse moodulid PDP-sse lehekülge "rikastades".</span><span class="sxs-lookup"><span data-stu-id="ac502-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ac502-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ac502-157">Additional resources</span></span>

[<span data-ttu-id="ac502-158">Avalehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac502-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="ac502-159">Kategooria vaikesihtlehe ja otsingutulemuste lehe ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac502-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="ac502-160">Ostukorvi ja maksmise lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac502-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="ac502-161">Kontohalduse lehtede ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac502-161">Overview of account management pages</span></span>](quick-tour-account-management.md)