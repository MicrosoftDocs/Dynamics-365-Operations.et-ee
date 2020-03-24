---
title: AI-ML-põhiste tootesoovituse tulemuste kohandamine
description: Selles teemas selgitatakse, kuidas kohandada tehisintellekti masinõppel (AI-ML) põhinevaid tootesoovituse tulemusi teie ettevõttele.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4631ef03e1d73b70d80e774d1efa4909e619bbc0
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127924"
---
# <a name="adjust-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="b46c1-103">AI-ML-põhiste tootesoovituse tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="b46c1-103">Adjust AI-ML-based product recommendation results</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b46c1-104">Selles teemas selgitatakse, kuidas kohandada tehisintellekti masinõppel (AI-ML) põhinevaid tootesoovituse tulemusi teie ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="b46c1-104">This topic explains how to adjust product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="b46c1-105">Pärast tootesoovituste lubamist hakkavad kehtima vaikesätted; need parameetrid töötavad, võivad töötada paljude vajaduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="b46c1-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="b46c1-106">Parim on planeerida kulutada aega hindamisele, kas tulemused vastavad toodete müügiliikumisele.</span><span class="sxs-lookup"><span data-stu-id="b46c1-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="b46c1-107">Soovitame hinnata tulemusi paar päeva, enne kui muudate parameetreid vastavalt vajadusele enne uuesti testimist.</span><span class="sxs-lookup"><span data-stu-id="b46c1-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="b46c1-108">Soovituste loendi parameetrite mõistmine</span><span class="sxs-lookup"><span data-stu-id="b46c1-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="b46c1-109">Enne parameetrite muutmist vaadake, kuidas need mõjutavad tulemusi allpool.</span><span class="sxs-lookup"><span data-stu-id="b46c1-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="b46c1-110">Populaarne tooteloend</span><span class="sxs-lookup"><span data-stu-id="b46c1-110">"Trending" product list</span></span>

<span data-ttu-id="b46c1-111">Populaarses tooteloendis on võimalik muuta kahte parameetrit.</span><span class="sxs-lookup"><span data-stu-id="b46c1-111">The "Trending" product list has two parameters that can be changed:</span></span>

![Populaarse loendi vaikeparameetrite näide](./media/exampletrendingparameters.png)

1. <span data-ttu-id="b46c1-113">**Kaasa viimase X päeva uued tooted** – tooteid, mis on lisatud konkreetne arv päevi enne praegust kuupäeva, saab kasutada tootekanditaatide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="b46c1-113">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="b46c1-114">Vaikeväärtus pildil näitab, et populaarsete toodete loendis saab kasutada tooteid, mis on vähemalt 180 päeva vabad.</span><span class="sxs-lookup"><span data-stu-id="b46c1-114">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="b46c1-115">**Kaasa viimase X päeva müügid** – müügitehinguid, mis on toimunud konkreetne arv päevi enne praegust kuupäeva, saab kasutada toodete tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="b46c1-115">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="b46c1-116">Ülaltoodud vaikeväärtus näitab, et kõiki viimase 30 päeva jooksul sooritatud toote ostusid kasutatakse toote asukoha määratlemiseks populaarsete toodete loendis.</span><span class="sxs-lookup"><span data-stu-id="b46c1-116">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="b46c1-117">Enim müüdud toodete loend</span><span class="sxs-lookup"><span data-stu-id="b46c1-117">"Best selling" product list</span></span>

<span data-ttu-id="b46c1-118">Sõltuvalt teie ettevõttest, võib loend Enim müüdud anda populaarsete toodetega võrreldes erineva tulemuse, olgugi need mõlemad kasutavad toodete tellimiseks kandeandmeid.</span><span class="sxs-lookup"><span data-stu-id="b46c1-118">Depending on your business, the "Best selling" list can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="b46c1-119">Kuna suvandil enim müüdud puudub sortimise kuupäeva põhjal tähtaeg, võib suvand enim müüdud tõsta esile endiselt väga populaarsed vanemad tooted, mis võisid populaarsete loendist välja langeda.</span><span class="sxs-lookup"><span data-stu-id="b46c1-119">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="b46c1-120">Enim müüdud toodete loendis on võimalik muuta ühte parameetrit.</span><span class="sxs-lookup"><span data-stu-id="b46c1-120">The "Best selling" product list has one parameter that can be changed:</span></span>

![Enim müüdud loendi vaikeparameetri näide](./media/examplebestsellingparameters.PNG)

1. <span data-ttu-id="b46c1-122">**Kaasa viimase X päeva müügid** – müügitehinguid, mis on toimunud konkreetne arv päevi enne praegust kuupäeva, saab kasutada toodete tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="b46c1-122">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="b46c1-123">Ülaltoodud vaikeväärtus näitab, et kõiki viimase 30 päeva jooksul sooritatud toote ostusid kasutatakse toote asukoha määratlemiseks enim müüdud toodete loendis.</span><span class="sxs-lookup"><span data-stu-id="b46c1-123">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="b46c1-124">Toodete käsitsi soovituse loenditesse lisamine või nendest eemaldamine</span><span class="sxs-lookup"><span data-stu-id="b46c1-124">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling-lists"></a><span data-ttu-id="b46c1-125">Loendite Uus, Populaarne ja Enim müüdud jaoks</span><span class="sxs-lookup"><span data-stu-id="b46c1-125">For "New," "Trending," or "Best selling" lists</span></span>

1.  <span data-ttu-id="b46c1-126">Avage **Jaemüük ja kaubandus** > **Tootesoovitused** > **Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="b46c1-126">Go to **Retail and Commerce** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="b46c1-127">Jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="b46c1-127">In the list of shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="b46c1-128">Valige toodete loendisse lisamine või sellest eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="b46c1-128">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="b46c1-129">Toodete tabelisse lisamiseks valige suvand **Lisa rida.**</span><span class="sxs-lookup"><span data-stu-id="b46c1-129">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="b46c1-130">Veerus Toode otsige toodet suvandi **Nimi** või **Tootenumber** järgi.</span><span class="sxs-lookup"><span data-stu-id="b46c1-130">Under the Product column, search for a product by **Name** or **Product number.**</span></span>

    ![Näide toodete otsimisest uute toodete loendis](./media/examplenewlistconfiguration1.png)

1.  <span data-ttu-id="b46c1-132">Valige veerus Rea tüüp üks kahest suvandist.</span><span class="sxs-lookup"><span data-stu-id="b46c1-132">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="b46c1-133">**Kaasa** – sunnib toote loendi ette</span><span class="sxs-lookup"><span data-stu-id="b46c1-133">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="b46c1-134">**Välista** – tühistab toote loendis ilmumise</span><span class="sxs-lookup"><span data-stu-id="b46c1-134">**Exclude** – removes a product from appearing in the list</span></span>
    
    ![Näide toote kaasamisest või välistamisest uute toodete loendist](./media/examplenewlistconfiguration2.png)

1.  <span data-ttu-id="b46c1-136">Suvandi **Kuvamise järjekord** muutmine muudab järjestust, kuidas suvandiga **kaasa** tähistatud tooted loendisse ilmuvad.</span><span class="sxs-lookup"><span data-stu-id="b46c1-136">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="b46c1-137">Kui kahel tootel on sama **kuvamise järjestuse** väärtus, siis võib nende kahe tulemuse lõplik tellimus kontorist erineda.</span><span class="sxs-lookup"><span data-stu-id="b46c1-137">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="b46c1-138">Toodete tabelist eemaldamiseks: valige eemaldatav rida ja klõpsake käsku **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="b46c1-138">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="b46c1-139">Loendite Inimestele meeldib ka ja Sageli koos ostetud jaoks</span><span class="sxs-lookup"><span data-stu-id="b46c1-139">For "People also like" or "Frequently bought together" lists</span></span>

<span data-ttu-id="b46c1-140">Loendite Sageli koos ostetud või Inimestele meeldib ka kontekstis kasutatakse masinõpet tarbija ostumustrite analüüsimiseks, et soovitada sageli koos ostetavaid seotud tooteid ainulaadseks lähteväärtuse tooteks.</span><span class="sxs-lookup"><span data-stu-id="b46c1-140">In the context of "Frequently bought together" or "People also like" lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="b46c1-141">*Lähteväärtuse toode* on toode, mille jaoks soovite tulemusi luua.</span><span class="sxs-lookup"><span data-stu-id="b46c1-141">A *seed product* is the product you want to generate results for.</span></span> <span data-ttu-id="b46c1-142">Soovituse loendite käsitsi reguleerimise kontekstis te lisate või eemaldate selle toote tulemusi.</span><span class="sxs-lookup"><span data-stu-id="b46c1-142">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="b46c1-143">Lähteväärtus toote tulemuste käsitsi lisamiseks või eemaldamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b46c1-143">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="b46c1-144">Valige suvand **Lähteväärtuse toode**.</span><span class="sxs-lookup"><span data-stu-id="b46c1-144">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="b46c1-145">Veerus **Toode** otsige toodet suvandite **Nimi** või **Tootenumber** alusel.
![Näide toote otsimisest loendist Sageli koos ostetud](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="b46c1-145">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="b46c1-146">Valige veerus **Rea tüüp** üks kahest suvandist.</span><span class="sxs-lookup"><span data-stu-id="b46c1-146">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="b46c1-147">**Kaasa** – sunnib toote loendi ette</span><span class="sxs-lookup"><span data-stu-id="b46c1-147">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="b46c1-148">**Välista** – tühistab toote loendis ilmumise</span><span class="sxs-lookup"><span data-stu-id="b46c1-148">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="b46c1-149">![Näide toote loendisse Sageli koos ostetud kaasamisest või sellest eemaldamisest](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="b46c1-149">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="b46c1-150">Toodete tabelist eemaldamiseks: valige eemaldatav rida ja klõpsake käsku Eemalda.</span><span class="sxs-lookup"><span data-stu-id="b46c1-150">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b46c1-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b46c1-151">Additional resources</span></span>

[<span data-ttu-id="b46c1-152">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b46c1-152">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="b46c1-153">ADLS-i lubamine Dynamics 365 Commerce keskkonnas</span><span class="sxs-lookup"><span data-stu-id="b46c1-153">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="b46c1-154">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="b46c1-154">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="b46c1-155">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="b46c1-155">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="b46c1-156">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="b46c1-156">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="b46c1-157">Soovitusloendite lisamine e-Kaubanduse saidile</span><span class="sxs-lookup"><span data-stu-id="b46c1-157">Add recommendation lists to an e-Commerce site</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="b46c1-158">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="b46c1-158">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="b46c1-159">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="b46c1-159">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="b46c1-160">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="b46c1-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="b46c1-161">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="b46c1-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="b46c1-162">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="b46c1-162">Product recommendations FAQ</span></span>](faq-recommendations.md)
