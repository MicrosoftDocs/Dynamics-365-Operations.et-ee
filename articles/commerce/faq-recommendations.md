---
title: Tootesoovituste KKK
description: Sellest teemast leiate teavet toimingute ja tööriistade kohta, mida saate kasutada toote soovituste või nende tulemustega seotud probleemide tõrkeotsinguks.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, Core, Operations
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: cf3df2267671b50c20b28dbdb1c6a21696bf2515
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411564"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="57718-103">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="57718-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="57718-104">Sellest teemast leiate teavet toimingute ja tööriistade kohta, mida saate kasutada [toote soovituste](product-recommendations.md) või nende tulemustega seotud probleemide tõrkeotsinguks.</span><span class="sxs-lookup"><span data-stu-id="57718-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="57718-105">Head tavad</span><span class="sxs-lookup"><span data-stu-id="57718-105">Best practices</span></span>
<span data-ttu-id="57718-106">Väga oluline on kasutada tooteetalonide ja -variantide kontseptsiooni.</span><span class="sxs-lookup"><span data-stu-id="57718-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="57718-107">Ülema tooteetaloni variantide mõistlik rühmitamine aitab loetleda algoritme ja teenus loob paremaid mudeleid.</span><span class="sxs-lookup"><span data-stu-id="57718-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="57718-108">Lisaks saab teenus kasutada ainult üht toote eksemplari, mitte panna kõik lähedalt seotud variandid loendisse.</span><span class="sxs-lookup"><span data-stu-id="57718-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="57718-109">Kui kõik lähedalt seotud variandid pannakse loendisse, võivad ilmneda valed või topelttulemused.</span><span class="sxs-lookup"><span data-stu-id="57718-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="57718-110">Miks puuduvad tooted soovituste loenditest?</span><span class="sxs-lookup"><span data-stu-id="57718-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="57718-111">Tavaliselt kui toode puudub toote soovituste loendist, võib esineda toote konfiguratsiooni probleem.</span><span class="sxs-lookup"><span data-stu-id="57718-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="57718-112">Näiteks võib olla toote algus- või lõppkuupäev olla vale, mõõtmed võivad olla valesti konfigureeritud või toode ei pruugi olla õiges kanali sortimendis jne.</span><span class="sxs-lookup"><span data-stu-id="57718-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="57718-113">Kui kaup puudub tehisintellekti masinõppel (AI-ML) põhinevast soovituste loendist, võib toode mitte vastata soovituste loendi kriteeriumitele või see ei pruugi omada piisavalt ostutehinguid, et soovituste loend seda näitaks.</span><span class="sxs-lookup"><span data-stu-id="57718-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="57718-114">Soovitame teil kontrollida järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="57718-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="57718-115">**Veenduge, et toodete soovitused oleksid lubatud HQ-s.**</span><span class="sxs-lookup"><span data-stu-id="57718-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="57718-116">Lisateavet selle teenuse lubamise kohta leiate teemast [Tootesoovituste lubamine](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="57718-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="57718-117">**Veenduge, et toote põhiatribuudid oleksid määratud.**</span><span class="sxs-lookup"><span data-stu-id="57718-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="57718-118">Näiteks peavad tootesortimendid olema määratud valikule **Kaasa**.</span><span class="sxs-lookup"><span data-stu-id="57718-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="57718-119">**Värskelt sorditud toodete puhul võib kuluda kuni 3 tundi, enne kui toode hakkab uues loendis ilmuma.**</span><span class="sxs-lookup"><span data-stu-id="57718-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="57718-120">**Kui toode ei ilmu ikka veel suvandites Populaarne, Enim müüdud, inimestele meeldib ka, või Sageli koos ostetud, siis ei pruugi sellel tootel olla piisavalt kandeid.**</span><span class="sxs-lookup"><span data-stu-id="57718-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="57718-121">Sellisel juhul võite oodata, kuni esineb rohkem kandeid, värskendada vaikimisi soovituste loendi parameetreid või kasutada käsitsi sekkumist soovituste tooteloendi tulemuste muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="57718-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="57718-122">Lisateavet soovituse parameetrite kohta vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="57718-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="57718-123">**Veenduge, et toode vastaks loendi soovituste kriteeriumidele.**</span><span class="sxs-lookup"><span data-stu-id="57718-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="57718-124">Lisateavet toote soovituse parameetrite kohta vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="57718-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="57718-125">Kuidas ma saan vältida kehvade soovituse tulemuste tagastamist?</span><span class="sxs-lookup"><span data-stu-id="57718-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="57718-126">Soovituste loendid vajavad tulemuste esitamiseks suurt tehingute hulka.</span><span class="sxs-lookup"><span data-stu-id="57718-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="57718-127">Seetõttu on oluline, et kasutajad esitaksid täieliku ajaloolise kandeteabe.</span><span class="sxs-lookup"><span data-stu-id="57718-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="57718-128">Lisaks ei ole toodetel, millel puuduvad kanded või mis omavad vähe kandeid, tulemusi **Inimestele meeldib ka** või **Sageli koos ostetud**, seega need soovituse loendites **Populaarsed** ega **Enim müüdud** ei ilmu.</span><span class="sxs-lookup"><span data-stu-id="57718-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="57718-129">Selline olukord võib sageli esineda väga uute toodete puhul või vanade toodete puhul, mida on vähe ostetud.</span><span class="sxs-lookup"><span data-stu-id="57718-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="57718-130">Populaarsete uute kaupadega laheneb see probleem hõlpsalt.</span><span class="sxs-lookup"><span data-stu-id="57718-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="57718-131">Soovitame teil järgida järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="57718-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="57718-132">**Veenduge, et toode vastaks selle loendi soovituste kriteeriumidele.**</span><span class="sxs-lookup"><span data-stu-id="57718-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="57718-133">Lisateavet toote soovituse parameetrite kohta vaadake teemast AI-ML-põhiste tootesoovituse tulemuste muutmine.</span><span class="sxs-lookup"><span data-stu-id="57718-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="57718-134">**Kui toode on uus, kaaluge soovituste loendi muutmist, kuni tootel on rohkem kandeid.**</span><span class="sxs-lookup"><span data-stu-id="57718-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="57718-135">Lisateavet selle kohta, kuidas soovituse loendi tulemusi muuta, vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="57718-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="57718-136">**Veenduge, et toode vastaks selle loendi soovituste kriteeriumidele.**</span><span class="sxs-lookup"><span data-stu-id="57718-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="57718-137">Lisateavet toote soovituse parameetrite kohta vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="57718-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="57718-138">**Kui toode on uus, kaaluge soovituste loendi muutmist, kuni tootel on rohkem kandeid**.</span><span class="sxs-lookup"><span data-stu-id="57718-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="57718-139">Lisateavet selle kohta, kuidas soovituse loendi tulemusi muuta, vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="57718-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="57718-140">Kas ma saan toote eemaldada, kuid seda endiselt poes näha?</span><span class="sxs-lookup"><span data-stu-id="57718-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="57718-141">Kui ettevõttel tekib vajadus, saate algoritmiliselt loodud loendeid reguleerida.</span><span class="sxs-lookup"><span data-stu-id="57718-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="57718-142">Samas kui toode soovituse loendist eemaldatakse, jääb toode kaupluses leitavaks.</span><span class="sxs-lookup"><span data-stu-id="57718-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="57718-143">Lisateavet selle kohta, kuidas toote soovituse tulemusi muuta, vaadake teemast [AI-ML-põhiste tootesoovituse tulemuste haldamine](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="57718-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="57718-144">Kui peate blokeerima kauba poes avastamise, peate muutma suvandi **Kauba sortiment** valikule **Välista**.</span><span class="sxs-lookup"><span data-stu-id="57718-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="57718-145">Kuidas lisada loendit e-kaubanduse lehele?</span><span class="sxs-lookup"><span data-stu-id="57718-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="57718-146">Lisateavet toote soovituse lehtede e-kaubanduse veebisaidile lisamise kohta leiate teemast [Tootesoovituste loendite lisamine lehtedele](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="57718-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="57718-147">Kuidas lubada tootesoovitused kassas?</span><span class="sxs-lookup"><span data-stu-id="57718-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="57718-148">Pärast tootesoovituste lubamist peate lisama soovituste paneeli juhtelemendi kassaekraanile.</span><span class="sxs-lookup"><span data-stu-id="57718-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="57718-149">Lisateabe saamiseks vt [Soovituste juhtelemendi lisamine kassaseadmete kandekuvale](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="57718-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57718-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="57718-150">Additional resources</span></span>

[<span data-ttu-id="57718-151">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="57718-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="57718-152">Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="57718-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="57718-153">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="57718-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="57718-154">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="57718-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="57718-155">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="57718-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="57718-156">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="57718-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="57718-157">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="57718-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="57718-158">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="57718-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="57718-159">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="57718-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="57718-160">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="57718-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="57718-161">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="57718-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
