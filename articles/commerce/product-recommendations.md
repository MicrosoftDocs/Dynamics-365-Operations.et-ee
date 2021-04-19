---
title: Tootesoovituste ülevaade
description: Selles teemas antakse üldist teavet tootesoovituste kohta. Tootesoovitused võimaldavad klientidel kergesti ja kiiresti leida tooteid, mida nad soovivad ja isegi tooteid, mida nad algselt ei kavatsenud osta.
author: Moonma
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: moonma
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 044a5c21e4ebf1bf83edc74335e655b9388bc1d4
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795593"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="b2a84-104">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b2a84-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b2a84-105">Rakendust Microsoft Dynamics 365 Commerce saab kasutada tootesoovituste kuvamiseks e-kaubanduse veebisaidil ja kassa (POS) seadmes.</span><span class="sxs-lookup"><span data-stu-id="b2a84-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="b2a84-106">Tootesoovitused on kaubad, millest klient võib huvitatud olla.</span><span class="sxs-lookup"><span data-stu-id="b2a84-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="b2a84-107">Soovitused põhinevad teiste klientide ostude suundumustel võrgus ja kliendiga näost-näkku suhtlevates kauplustes.</span><span class="sxs-lookup"><span data-stu-id="b2a84-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="b2a84-108">Tootesoovitused võimaldavad klientidel lihtsalt ja kiiresti leida tooteid, mida nad soovivad, kui neil on kogemus, mis neile hästi sobib.</span><span class="sxs-lookup"><span data-stu-id="b2a84-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="b2a84-109">Ristmüüki ja ülesmüüki saab kasutada isegi selleks, et suunata kliente leidma täiendavaid tooteid, mida nad algselt ei kavatsenud osta.</span><span class="sxs-lookup"><span data-stu-id="b2a84-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="b2a84-110">Kui soovitusi kasutatakse toote avastuse täiustamiseks, võivad need luua rohkem konversiooni võimalusi, aidata suurendada müügitulu ja aidata veelgi suurendada kliendi rahulolu ja hoidmist.</span><span class="sxs-lookup"><span data-stu-id="b2a84-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="b2a84-111">E-kaubanduses toetavad tootesoovitused suures osas Microsofti soovituste masinõppe tehnoloogiaid.</span><span class="sxs-lookup"><span data-stu-id="b2a84-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="b2a84-112">Soovitamise teenus</span><span class="sxs-lookup"><span data-stu-id="b2a84-112">Recommendation service</span></span>

<span data-ttu-id="b2a84-113">Tootesoovituste teenus kasutab tehisintellekti ja masinõppe (AI-ML) tehnoloogiaid järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="b2a84-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="b2a84-114">Andmed vormingus, mida soovitusteenus nõuab, ekstraheeritakse kaubanduse operatiivandmebaasist ja saadetakse Azure Data Lake Storage'isse või olemi kauplusesse.</span><span class="sxs-lookup"><span data-stu-id="b2a84-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure Data Lake Storage or Entity store.</span></span>
- <span data-ttu-id="b2a84-115">Soovitusteenus kasutab talletatud andmeid soovitusmudelite koolitamiseks järgmiste loendite jaoks: **Inimestele meeldib ka**, **Sageli koos ostetud**, **Uus**, **Enim müüdud** ja **Populaarsed**.</span><span class="sxs-lookup"><span data-stu-id="b2a84-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="b2a84-116">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="b2a84-116">Scenarios</span></span>

<span data-ttu-id="b2a84-117">Tootesoovitused on saadaval järgmiste stsenaariumide puhul.</span><span class="sxs-lookup"><span data-stu-id="b2a84-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="b2a84-118">**E-kaubanduse lehe sirvimise või sihtlehe mis tahes kaupluse lehel:** kui kliendid või kaupluse kaastöötajad külastavad kaupluse lehte, võib soovituse mootor soovitada tooteid loendites **Uus**, **Enim müüdud** ja **Populaarsed**.</span><span class="sxs-lookup"><span data-stu-id="b2a84-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="b2a84-119">**Lehel toote üksikasjad:** kui kliendid või kaupluse kaastöötajad külastavad lehte **Toote üksikasjad**, soovitab soovituse mootor lisakaupu, mida tõenäoliselt ka ostetakse.</span><span class="sxs-lookup"><span data-stu-id="b2a84-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="b2a84-120">Need kaubad kuvatakse loendis **Inimestele meeldib ka**.</span><span class="sxs-lookup"><span data-stu-id="b2a84-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="b2a84-121">**Kande või kassa lehel:** soovituse mootor pakub kaupu, mis põhinevad kogu ostukorvis olevate kaupade loendil.</span><span class="sxs-lookup"><span data-stu-id="b2a84-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="b2a84-122">Need kaubad kuvatakse loendis **Sageli koos ostetud**.</span><span class="sxs-lookup"><span data-stu-id="b2a84-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="b2a84-123">**Isikupärastatud soovitused** : turustajad võivad pakkuda sisselogitud klientidele isikupärastatud loendeid **Teile valitud** koos uue funktsiooniga, mis võimaldab olemasolevaid loendi stsenaariumeid vastavalt sellele kliendile isikupärastada.</span><span class="sxs-lookup"><span data-stu-id="b2a84-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="b2a84-124">Lisateabe saamiseks vt [Isikupärastatud soovituste lubamine.](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="b2a84-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="b2a84-125">Tootesoovituste tüübid</span><span class="sxs-lookup"><span data-stu-id="b2a84-125">Types of product recommendations</span></span>

<span data-ttu-id="b2a84-126">Järgmine tabel kirjeldab erinevaid automatiseeritud tootesoovituste tüüpe, mis on saadaval jaemüüjatele lahenduses Dynamics 365 Commerce rakendamiseks [tootekogumi mooduli kaudu](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b2a84-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="b2a84-127">Jaemüüjad saavad kuvada ka sisselogitud kasutajale isikupärastatud tulemusi, kui saidi autor valib selle suvandi.</span><span class="sxs-lookup"><span data-stu-id="b2a84-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="b2a84-128">Tootekogumi moodul</span><span class="sxs-lookup"><span data-stu-id="b2a84-128">Product collection module</span></span>  | <span data-ttu-id="b2a84-129">Tüüp</span><span class="sxs-lookup"><span data-stu-id="b2a84-129">Type</span></span> | <span data-ttu-id="b2a84-130">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b2a84-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="b2a84-131">New</span><span class="sxs-lookup"><span data-stu-id="b2a84-131">New</span></span>                        | <span data-ttu-id="b2a84-132">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="b2a84-132">Algorithmic</span></span> | <span data-ttu-id="b2a84-133">See moodul kuvab uusimate toodete loendi, mis on kanalitele ja kataloogidele hiljuti valitud.</span><span class="sxs-lookup"><span data-stu-id="b2a84-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="b2a84-134">Enim müüdud</span><span class="sxs-lookup"><span data-stu-id="b2a84-134">Best selling</span></span>               | <span data-ttu-id="b2a84-135">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="b2a84-135">Algorithmic</span></span> | <span data-ttu-id="b2a84-136">See moodul kuvab toodete loendi, mis on järjestatud kõige suurema müügi arvu alusel.</span><span class="sxs-lookup"><span data-stu-id="b2a84-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="b2a84-137">Populaarsed</span><span class="sxs-lookup"><span data-stu-id="b2a84-137">Trending</span></span>                   | <span data-ttu-id="b2a84-138">Algoritmiline</span><span class="sxs-lookup"><span data-stu-id="b2a84-138">Algorithmic</span></span> | <span data-ttu-id="b2a84-139">See moodul näitab kõige kõrgema jõudlusega toodete loendit valitud perioodil, mis on järjestatud suurima müüginumbri järgi.</span><span class="sxs-lookup"><span data-stu-id="b2a84-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="b2a84-140">Kliendid ostavad sageli koos</span><span class="sxs-lookup"><span data-stu-id="b2a84-140">Frequently bought together</span></span> | <span data-ttu-id="b2a84-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="b2a84-141">AI-ML</span></span> | <span data-ttu-id="b2a84-142">See moodul soovitab toodete loendit, mida tavaliselt ostetakse koos tarbija praeguse ostukorvi sisuga.</span><span class="sxs-lookup"><span data-stu-id="b2a84-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="b2a84-143">Inimestele meeldib ka</span><span class="sxs-lookup"><span data-stu-id="b2a84-143">People also like</span></span>           | <span data-ttu-id="b2a84-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="b2a84-144">AI-ML</span></span> | <span data-ttu-id="b2a84-145">See moodul soovitab tooteid lähteväärtuse toote põhjal, tuginedes tarbija ostuharjumustele.</span><span class="sxs-lookup"><span data-stu-id="b2a84-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="b2a84-146">Valib teile</span><span class="sxs-lookup"><span data-stu-id="b2a84-146">Picks for you</span></span>              | <span data-ttu-id="b2a84-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="b2a84-147">AI-ML</span></span> | <span data-ttu-id="b2a84-148">See moodul soovitab isikupärastatud toodete loendit sisselogitud kasutaja ostuharjumuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="b2a84-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="b2a84-149">Külalisekasutaja jaoks on see loend ahendatud.</span><span class="sxs-lookup"><span data-stu-id="b2a84-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b2a84-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b2a84-150">Additional resources</span></span>

[<span data-ttu-id="b2a84-151"> Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="b2a84-151">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b2a84-152">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="b2a84-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b2a84-153">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="b2a84-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b2a84-154">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="b2a84-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b2a84-155">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="b2a84-155">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="b2a84-156">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="b2a84-156">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b2a84-157">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="b2a84-157">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b2a84-158">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="b2a84-158">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="b2a84-159">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="b2a84-159">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b2a84-160">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="b2a84-160">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b2a84-161">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="b2a84-161">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]