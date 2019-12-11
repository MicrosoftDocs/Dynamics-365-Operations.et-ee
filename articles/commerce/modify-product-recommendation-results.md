---
title: AI-ML-põhiste tootesoovituse tulemuste haldamine
description: Selles teemas selgitatakse, kuidas kohandada tehisintellekti masinõppel (AI-ML) põhinevaid tootesoovituse tulemusi teie ettevõttele.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 669b056c38614c8ac9be2d7b244a0ab0c73bc9f8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770066"
---
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="8b4a6-103">AI-ML-põhiste tootesoovituse tulemuste haldamine</span><span class="sxs-lookup"><span data-stu-id="8b4a6-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8b4a6-104">Selles teemas selgitatakse, kuidas kohandada tehisintellekti masinõppel (AI-ML) põhinevaid tootesoovituse tulemusi teie ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="8b4a6-105">Pärast tootesoovituste lubamist hakkavad kehtima vaikesätted; need parameetrid töötavad, võivad töötada paljude vajaduste jaoks.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="8b4a6-106">Parim on planeerida kulutada aega hindamisele, kas tulemused vastavad toodete müügiliikumisele.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="8b4a6-107">Soovitame hinnata tulemusi paar päeva, enne kui muudate parameetreid vastavalt vajadusele enne uuesti testimist.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="8b4a6-108">Soovituste loendi parameetrite mõistmine</span><span class="sxs-lookup"><span data-stu-id="8b4a6-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="8b4a6-109">Enne parameetrite muutmist vaadake, kuidas need mõjutavad tulemusi allpool.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="8b4a6-110">Populaarne tooteloend</span><span class="sxs-lookup"><span data-stu-id="8b4a6-110">Trending product list</span></span>

<span data-ttu-id="8b4a6-111">Tooteloendil **Populaarne** on kaks parameetrit, mida saab muuta: ![Populaarsete loendi vaikeparameetrite näide](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="8b4a6-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="8b4a6-112">**Kaasa viimase X päeva uued tooted** – tooteid, mis on lisatud konkreetne arv päevi enne praegust kuupäeva, saab kasutada tootekanditaatide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="8b4a6-113">Vaikeväärtus pildil näitab, et populaarsete toodete loendis saab kasutada tooteid, mis on vähemalt 180 päeva vabad.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="8b4a6-114">**Kaasa viimase X päeva müügid** – müügitehinguid, mis on toimunud konkreetne arv päevi enne praegust kuupäeva, saab kasutada toodete tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="8b4a6-115">Ülaltoodud vaikeväärtus näitab, et kõiki viimase 30 päeva jooksul sooritatud toote ostusid kasutatakse toote asukoha määratlemiseks populaarsete toodete loendis.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="8b4a6-116">Enim müüdud toodete loend</span><span class="sxs-lookup"><span data-stu-id="8b4a6-116">Best selling product list</span></span>

<span data-ttu-id="8b4a6-117">Sõltuvalt teie ettevõttest, võib suvand Enim müüdud anda populaarsete toodetega võrreldes erineva tulemuse, olgugi need mõlemad kasutavad toodete tellimiseks kandeandmeid.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="8b4a6-118">Kuna suvandil enim müüdud puudub sortimise kuupäeva põhjal tähtaeg, võib suvand enim müüdud tõsta esile endiselt väga populaarsed vanemad tooted, mis võisid populaarsete loendist välja langeda.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="8b4a6-119">**Enim müüdud** toodete loendis on võimalik muuta ühte parameetrit.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Enim müüdud loendi vaikeparameetri näide](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="8b4a6-121">**Kaasa viimase X päeva müügid** – müügitehinguid, mis on toimunud konkreetne arv päevi enne praegust kuupäeva, saab kasutada toodete tellimiseks.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="8b4a6-122">Ülaltoodud vaikeväärtus näitab, et kõiki viimase 30 päeva jooksul sooritatud toote ostusid kasutatakse toote asukoha määratlemiseks enim müüdud toodete loendis.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="8b4a6-123">Toodete käsitsi soovituse loenditesse lisamine või nendest eemaldamine</span><span class="sxs-lookup"><span data-stu-id="8b4a6-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="8b4a6-124">Suvandite Uus, Populaarne ja Enim müüdud jaoks</span><span class="sxs-lookup"><span data-stu-id="8b4a6-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="8b4a6-125">Avage **Jaemüük** > **Tootesoovitused** > **Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="8b4a6-126">Jaemüügi jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="8b4a6-127">Valige toodete loendisse lisamine või sellest eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="8b4a6-128">Toodete tabelisse lisamiseks valige suvand **Lisa rida.**</span><span class="sxs-lookup"><span data-stu-id="8b4a6-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="8b4a6-129">Veerus Toode otsige toodet suvandite **Nimi** või **Tootenumber** alusel.
![Näide toote otsimisest tooteloendis Uus](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="8b4a6-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="8b4a6-130">Valige veerus Rea tüüp üks kahest suvandist.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="8b4a6-131">**Kaasa** – sunnib toote loendi ette</span><span class="sxs-lookup"><span data-stu-id="8b4a6-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="8b4a6-132">**Välista** – tühistab toote loendis ilmumise ![Näide toote loendisse Uus toode kaasamisest või sellest eemaldamisest](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="8b4a6-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="8b4a6-133">Suvandi **Kuvamise järjekord** muutmine muudab järjestust, kuidas suvandiga **kaasa** tähistatud tooted loendisse ilmuvad.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="8b4a6-134">Kui kahel tootel on sama **kuvamise järjestuse** väärtus, siis võib nende kahe tulemuse lõplik tellimus kontorist erineda.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="8b4a6-135">Toodete tabelist eemaldamiseks: valige eemaldatav rida ja klõpsake käsku **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="8b4a6-136">Loendite Inimestele meeldib ka ja Sageli koos ostetud jaoks</span><span class="sxs-lookup"><span data-stu-id="8b4a6-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="8b4a6-137">Loendite **Sageli koos ostetud** või **Inimestele meeldib ka** kontekstis kasutatakse masinõpet tarbija ostumustrite analüüsimiseks, et soovitada sageli koos ostetavaid seotud tooteid ainulaadseks lähteväärtuse tooteks.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="8b4a6-138">**Lähteväärtuse toode** on toode, mille jaoks soovite tulemusi luua.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="8b4a6-139">Soovituse loendite käsitsi reguleerimise kontekstis te lisate või eemaldate selle toote tulemusi.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="8b4a6-140">Lähteväärtus toote tulemuste käsitsi lisamiseks või eemaldamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="8b4a6-141">Valige suvand **Lähteväärtuse toode**.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="8b4a6-142">Veerus **Toode** otsige toodet suvandite **Nimi** või **Tootenumber** alusel.
![Näide toote otsimisest loendist Sageli koos ostetud](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="8b4a6-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="8b4a6-143">Valige veerus **Rea tüüp** üks kahest suvandist.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="8b4a6-144">**Kaasa** – sunnib toote loendi ette</span><span class="sxs-lookup"><span data-stu-id="8b4a6-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="8b4a6-145">**Välista** – tühistab toote loendis ilmumise</span><span class="sxs-lookup"><span data-stu-id="8b4a6-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="8b4a6-146">![Näide toote loendisse Sageli koos ostetud kaasamisest või sellest eemaldamisest](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="8b4a6-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="8b4a6-147">Toodete tabelist eemaldamiseks: valige eemaldatav rida ja klõpsake käsku Eemalda.</span><span class="sxs-lookup"><span data-stu-id="8b4a6-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="8b4a6-148">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8b4a6-148">Additional resources</span></span>

[<span data-ttu-id="8b4a6-149">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="8b4a6-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="8b4a6-150">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="8b4a6-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="8b4a6-151">Tootesoovituste loendite lisamine lehtedele</span><span class="sxs-lookup"><span data-stu-id="8b4a6-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
