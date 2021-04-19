---
title: Isikupärastatud soovitustest loobumine
description: See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce isikupärastatud soovituste saamisest.
author: bebeale
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1e7d0f505ce49bc9be0d027cbb0d636c9de0600b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804449"
---
# <a name="opt-out-of-personalized-recommendations"></a><span data-ttu-id="1ffd3-103">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="1ffd3-103">Opt out of personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1ffd3-104">See teema selgitab, kuidas saate lubada klientidel loobuda rakenduses Microsoft Dynamics 365 Commerce isikupärastatud soovituste saamisest.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-104">This topic explains how you can let customers opt out of receiving personalized recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1ffd3-105">Konto loomise ajal seadistatakse uued kliendid automaatselt saama isikupärastatud soovitusi.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-105">During account creation, new customers are automatically set up to receive personalized recommendations.</span></span> <span data-ttu-id="1ffd3-106">Samas pakub rakendus Dynamics 365 Commerce jaemüüjatele erinevaid võimalusi nende soovituste saamisest loobumiseks ja oma isikuandmete töötlemise piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-106">However, Dynamics 365 Commerce provides various ways for retailers to let users opt out of receiving these recommendations and restrict the processing of their personal data.</span></span> <span data-ttu-id="1ffd3-107">Autenditud kasutajad, kes loobuvad isikupärastatud soovituste saamisest, lõpetavad kohe isikupärastatud loendite nägemise.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-107">Authenticated users who opt out of receiving personalized recommendations will immediately stop seeing personalized lists.</span></span> <span data-ttu-id="1ffd3-108">Lisaks eemaldatakse kõik isikupärastamiseks kogutavad isikuandmed isikupärastatud soovituste mudelitest.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-108">Additionally, all personal data that is collected for personalization will be removed from personalized recommendations models.</span></span>

<span data-ttu-id="1ffd3-109">Lisateavet isikupärastatud tootesoovituste kohta vt jaotisest [Isikupärastatud soovituste lubamine](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="1ffd3-109">For more information about personalized product recommendations, see [Enable personalized recommendations](personalized-recommendations.md).</span></span>

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a><span data-ttu-id="1ffd3-110">Jaemüüjate loobumiskogemuse rakendamise viisid</span><span class="sxs-lookup"><span data-stu-id="1ffd3-110">Ways for retailers to implement an opt-out experience</span></span>

<span data-ttu-id="1ffd3-111">Jaemüüjatel on loobumiskogemuse rakendamiseks kolm viisi.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-111">Retailers have three ways to implement an opt-out experience.</span></span>

### <a name="opting-out-on-behalf-of-users"></a><span data-ttu-id="1ffd3-112">Kasutajate nimel loobumine</span><span class="sxs-lookup"><span data-stu-id="1ffd3-112">Opting out on behalf of users</span></span>

<span data-ttu-id="1ffd3-113">Commerce’i kontori kontohalduses saavad jaemüüjad loobuda kasutajate nimel.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-113">In Account management in Commerce back office, retailers can opt out on behalf of users.</span></span>

1. <span data-ttu-id="1ffd3-114">Otsige kontori avalehelt **kõiki kliente**.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-114">From the back-office home page, search for **all customers**.</span></span>
1. <span data-ttu-id="1ffd3-115">Otsige ja valige klient ning seejärel valige kiirkaart **Jaemüük**.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-115">Search for and select a customer, and then select the **Retail** FastTab.</span></span>

    ![Jaemüügi kiirkaart](./media/Disablepersonalizationpart1.png)

1. <span data-ttu-id="1ffd3-117">Jaotises **Privaatsus** seadke suvand **Keela isikupärastamine** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-117">Under **Privacy**, set the **Disable personalization** option to **Yes**.</span></span>

    ![Privaatsussätted](./media/Disablepersonalizationpart2.png)

1. <span data-ttu-id="1ffd3-119">Valige **Salvesta** ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-119">Select **Save**, and close the page.</span></span>

### <a name="module-based-opt-out-experience"></a><span data-ttu-id="1ffd3-120">Moodulipõhine loobumise kogemus</span><span class="sxs-lookup"><span data-stu-id="1ffd3-120">Module-based opt-out experience</span></span>

<span data-ttu-id="1ffd3-121">Jaemüüjad võivad lubada autenditud kasutajatel ise isikupärastatud soovitustest loobuda.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-121">Retailers can let authenticated users opt out of personalized recommendations by themselves.</span></span> <span data-ttu-id="1ffd3-122">Selle loobumiskogemuse pakkumiseks lisage kasutaja loobumise moodul konto profiili lehtedele.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-122">To provide this opt-out experience, add the user opt-out module to customer account profile pages.</span></span>

### <a name="custom-extensions"></a><span data-ttu-id="1ffd3-123">Kohandatud laiendid</span><span class="sxs-lookup"><span data-stu-id="1ffd3-123">Custom extensions</span></span>

<span data-ttu-id="1ffd3-124">Jaemüüjad saavad luua oma laiendid, et hallata kasutajate loobumise kogemust.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-124">Retailers can create their own extensions to manage the opt-out experience for users.</span></span> <span data-ttu-id="1ffd3-125">Lisateavet vt [Jaemüügiserveri API-de kutsumine](e-commerce-extensibility/call-retail-server-apis.md) ja [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="1ffd3-125">For more information, see [Call Retail Server APIs](e-commerce-extensibility/call-retail-server-apis.md) and [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a><span data-ttu-id="1ffd3-126">Isikupärastatud soovituste andmete digitaalse koopia hankimine autenditud kasutaja nimel</span><span class="sxs-lookup"><span data-stu-id="1ffd3-126">Obtain a digital copy of personalized recommendations data on behalf of an authenticated user</span></span>

<span data-ttu-id="1ffd3-127">Kliendid võivad soovida saada oma isikuandmete digitaalset koopiat ja vaadata nende soovituste tulemusi ka eksporditud vaates.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-127">Customers might want to obtain a digital copy of their personal data and also see an exported view of their recommendations results.</span></span> <span data-ttu-id="1ffd3-128">Kui klient seda teavet taotleb, peab jaemüüja looma kohandatud laienduse, mis kutsub jaemüügiserveri rakenduse programmeerimise liidest (API) ja päringuid teie loendist **Teile valitud**, mis põhineb kliendi ID-l.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-128">If a customer requests this information, the retailer must create a customized extension that calls the Retail Server application programming interface (API) and queries for the full results from the **Picks for you** list, based on the customer's customer ID.</span></span> <span data-ttu-id="1ffd3-129">Seejärel saab tulemusi eksportida komaeraldusega väärtuste (CSV) vormingus ja jagada kliendiga.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-129">The results can then be exported in comma-separated values (CSV) format and shared with the customer.</span></span>

<span data-ttu-id="1ffd3-130">Järgmine näide näitab, kuidas jaemüüja saab seda ülesannet täita.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-130">The following example shows how a retailer can accomplish this task.</span></span>

1. <span data-ttu-id="1ffd3-131">Jaemüüja loob kohandatud laienduse, et tõmmata kasutaja nimel isiklikke soovituste andmeid.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-131">The retailer creates a custom extension to pull personal recommendations data on behalf of the user.</span></span> <span data-ttu-id="1ffd3-132">Lisateavet moodulite loomise, olemasolevate moodulite kloonimise, jaemüügiserveri API-de kutsumise ja andmetegevuste kutsumise kohta vt teemast [Võrgukanali laiendatavus](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="1ffd3-132">For information about how to create modules, clone existing modules, call Retail Server APIs, and call data actions, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>
2. <span data-ttu-id="1ffd3-133">Kohandatud laiend teeb kutsungi tuumandmetegevusele **hangi-soovitused** ja edastab sellele nõutud teabe, mis põhineb loendi nõuetel.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-133">The custom extension makes a call to the **get-recommendations** core data action and passes the required information to it, based on the requirements of the list.</span></span> <span data-ttu-id="1ffd3-134">Loendi **Teile valitud** korral peab laiend edastama andmetegevusele õige loendi nime ja kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-134">In the case of the **Picks for you** list, the extension must pass the correct list name and customer ID to the data action.</span></span>

    <span data-ttu-id="1ffd3-135">Üks kohandatud laiendi loomise viis on kloonida olemasolevaid toote kogumise mooduleid, mida kasutatakse soovituste tulemuste tagastamiseks.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-135">One way to create the custom extension is to clone the existing product collection module that is used to return recommendations results.</span></span> <span data-ttu-id="1ffd3-136">Selle olemasoleva mooduli kloonimisega saab jaemüüja olemasolevat koodi muuta ja lisada uue nupu, mis ekspordib soovituste tulemused CSV-faili.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-136">By cloning this existing module, a retailer can modify the existing code and add a new button that exports the recommendations results to a CSV file.</span></span> <span data-ttu-id="1ffd3-137">Lisateavet leiate teemast [Mooduliteegi mooduli kloonimine](e-commerce-extensibility/clone-starter-module.md) ja [Tootekogumi moodulid](product-collection-module-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1ffd3-137">For more information, see [Clone a module library module](e-commerce-extensibility/clone-starter-module.md) and [Product collection modules](product-collection-module-overview.md).</span></span>

    <span data-ttu-id="1ffd3-138">Jaemüügiserveri API teegi täieliku vaate leiate teemast [Jaemüügiserveri kliendi ja tarbija API-d](dev-itpro/retail-server-customer-consumer-api.md).</span><span class="sxs-lookup"><span data-stu-id="1ffd3-138">For a full view of the Retail Server API library, see [Retail Server Customer and Consumer APIs](dev-itpro/retail-server-customer-consumer-api.md).</span></span>

3. <span data-ttu-id="1ffd3-139">Pärast kohandatud laiendi loomist saab jaemüüja eksportida CSV-faili kõigi soovituste tulemustega autenditud kasutaja kordumatu kliendi ID alusel.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-139">After the custom extension is created, the retailer can export a CSV file of all recommendations results, based on the unique customer ID of the authenticated user.</span></span>
4. <span data-ttu-id="1ffd3-140">Jaemüüja saab anda eksporditud CSV-faili, mis sisaldab soovitatavate toodete täielikku isikupärastatud loendit, autenditud kasutajaga ühiskasutusse.</span><span class="sxs-lookup"><span data-stu-id="1ffd3-140">The retailer can share the exported CSV file that contains the full personalized list of recommended products with the authenticated user.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1ffd3-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1ffd3-141">Additional resources</span></span>

[<span data-ttu-id="1ffd3-142">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="1ffd3-142">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="1ffd3-143">Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="1ffd3-143">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="1ffd3-144">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="1ffd3-144">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="1ffd3-145">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="1ffd3-145">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="1ffd3-146">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="1ffd3-146">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="1ffd3-147">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="1ffd3-147">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="1ffd3-148">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="1ffd3-148">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="1ffd3-149">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="1ffd3-149">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="1ffd3-150">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="1ffd3-150">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="1ffd3-151">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="1ffd3-151">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="1ffd3-152">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="1ffd3-152">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
