---
title: Isikupärastatud tootesoovituste lubamine
description: See teema kirjeldab, kuidas teha rakenduses Microsoft Dynamics 365 Commerce isikupärastatud tootesoovitused klientidele kättesaadavaks.
author: bebeale
ms.date: 08/18/2020
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
ms.openlocfilehash: dc0fbff437bfa948d70a03479561542106805bdb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804425"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="4950e-103">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="4950e-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4950e-104">See teema kirjeldab, kuidas teha rakenduses Microsoft Dynamics 365 Commerce isikupärastatud tootesoovitused klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="4950e-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4950e-105">Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine).</span><span class="sxs-lookup"><span data-stu-id="4950e-105">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="4950e-106">Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas.</span><span class="sxs-lookup"><span data-stu-id="4950e-106">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="4950e-107">Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="4950e-107">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="4950e-108">Isikupärastamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="4950e-108">Personalization prerequisites</span></span>

<span data-ttu-id="4950e-109">Enne isikupärastatud soovituste klientidele kättesaadavaks tegemist võtke arvesse, et tootesoovitusi toetatakse ainult nende Commerce’i kasutajate jaoks, kes on migreerinud oma salvestusruumi Azure Data Lake’i salve.</span><span class="sxs-lookup"><span data-stu-id="4950e-109">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="4950e-110">Enne kui kliendid saavad võtta vastu isikupärastatud tootesoovitusi, peavad jaemüüjad [lülitama tootesoovitused sisse](enable-product-recommendations.md)soovitused sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="4950e-110">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4950e-111">Tootesoovituste sisselülitamisega lülitate sisse ka isikupärastamise.</span><span class="sxs-lookup"><span data-stu-id="4950e-111">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="4950e-112">Kuid kui lülitate isikupärastamise välja, ei saa te muud tüüpi tootesoovitusi välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="4950e-112">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="4950e-113">Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="4950e-113">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="4950e-114">Isikupärastamise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="4950e-114">Turn on personalization</span></span>

<span data-ttu-id="4950e-115">Isikupärastamise sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4950e-115">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="4950e-116">Commerce'i peakontorist otsige valikut **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="4950e-116">In Commerce headquarters, search for **Feature Management**.</span></span>
1. <span data-ttu-id="4950e-117">Saadaolevate funktsioonide vaatamiseks valige **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="4950e-117">Select **All** to see a list of available features.</span></span> 
1. <span data-ttu-id="4950e-118">Sisestage otsinguväljale **Soovitused**.</span><span class="sxs-lookup"><span data-stu-id="4950e-118">In the search box, enter **Recommendations**.</span></span>
1. <span data-ttu-id="4950e-119">Valige funktsioon **Isikupärastatud tootesoovitused**.</span><span class="sxs-lookup"><span data-stu-id="4950e-119">Select the **Personalized product recommendations** feature.</span></span>
1. <span data-ttu-id="4950e-120">Tehke atribuutide paanil **Isikupärastatud tootesoovitused** valik **Luba kohe**.</span><span class="sxs-lookup"><span data-stu-id="4950e-120">In the **Personalized product recommendations** properties pane, select **Enable now**.</span></span>

![Isikupärastamise sisselülitamine](./media/FeatureManagement_Personalized.PNG)

> [!NOTE]
> <span data-ttu-id="4950e-122">Kui lülitate isikupärastamise sisse, käivitatakse isikupärastatud tootesoovituste loendite loomise protsess.</span><span class="sxs-lookup"><span data-stu-id="4950e-122">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="4950e-123">Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassas.</span><span class="sxs-lookup"><span data-stu-id="4950e-123">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="4950e-124">Isikupärastatud loendid</span><span class="sxs-lookup"><span data-stu-id="4950e-124">Personalized lists</span></span>

<span data-ttu-id="4950e-125">Lisaks olemasolevate arvuti loodud loendite isikupärastamise lubamisele võimaldab soovituste teenus toote avastamise kogemuse isikupärastamist nii võrgus kui ka kassas.</span><span class="sxs-lookup"><span data-stu-id="4950e-125">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="4950e-126">Pärast isikupärastamise sisselülitamist saavad jaemüüjad kuvada ostjatele isikustatud loendeid „Teile valitud” veebis või loendeid „Kliendile soovitatud” kassaterminalis.</span><span class="sxs-lookup"><span data-stu-id="4950e-126">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="4950e-127">Lisaks saavad jaemüüjad rakendada isikupärastamist olemasolevatele tootesoovituse loenditele ja pakkuda autenditud kasutajate jaoks isikuandmete kaitse üldmäärusest (GDPR) loobumise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="4950e-127">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="4950e-128">Kui lülitate isikupärastamise välja, lülitate ka need funktsioonid välja.</span><span class="sxs-lookup"><span data-stu-id="4950e-128">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="4950e-129">Veebipõhised loendid „Teile valitud”</span><span class="sxs-lookup"><span data-stu-id="4950e-129">Online "Picks for you" lists</span></span>

<span data-ttu-id="4950e-130">Loend „Teile valitud” on tehisintellekti masinõppe (AI-ML) loend, mis kuvab autenditud kasutaja soovitatud toodete isikupärastatud loendi.</span><span class="sxs-lookup"><span data-stu-id="4950e-130">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="4950e-131">See loend põhineb kasutaja omnikanali ostuajalool.</span><span class="sxs-lookup"><span data-stu-id="4950e-131">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="4950e-132">Isikupärastatud soovitusi värskendatakse dünaamiliselt, kui kasutaja teeb rohkem oste.</span><span class="sxs-lookup"><span data-stu-id="4950e-132">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="4950e-133">Seda tüüpi loend toetab ka kategooria filtreerimist, nii et jaemüüjad saavad kuvada navigeerimise hierarhial põhinevad peamised valikud.</span><span class="sxs-lookup"><span data-stu-id="4950e-133">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="4950e-134">Enne kui loend „Teile valitud” saab e-kaubanduse lehel ilmuda, peavad järgmised kasutajanõuded olema täidetud.</span><span class="sxs-lookup"><span data-stu-id="4950e-134">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="4950e-135">Kasutajad peavad olema sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="4950e-135">Users must be signed in.</span></span> <span data-ttu-id="4950e-136">Anonüümsed kasutajad ei näe isikupärastatud soovitusi.</span><span class="sxs-lookup"><span data-stu-id="4950e-136">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="4950e-137">Kasutajatel peab olema kontol vähemalt üks ost.</span><span class="sxs-lookup"><span data-stu-id="4950e-137">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="4950e-138">Kasutajad peavad isikupärastatud soovituste saamisega nõustuma.</span><span class="sxs-lookup"><span data-stu-id="4950e-138">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="4950e-139">Järgmisel joonisel on kujutatud loendi „Teile valitud” näide veebipoe lehel.</span><span class="sxs-lookup"><span data-stu-id="4950e-139">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Veebipõhine loend Teile valitud](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="4950e-141">Loendid „Kliendile soovitatud” kassas</span><span class="sxs-lookup"><span data-stu-id="4950e-141">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="4950e-142">Oma kliendisuhtluse kogemuse parandamiseks saavad jaemüüjad isikupärastada olemasolevate klientide üksikasjade lehti, lisades kontekstipõhise loendi „Kliendile soovitatud”.</span><span class="sxs-lookup"><span data-stu-id="4950e-142">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="4950e-143">Järgmisel joonisel on kujutatud loendi „Kliendile soovitatud” näide kassaterminalis.</span><span class="sxs-lookup"><span data-stu-id="4950e-143">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Loend Kliendile soovitatud kassas](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="4950e-145">Isikupärastamise rakendamine olemasolevatele soovituste loenditele</span><span class="sxs-lookup"><span data-stu-id="4950e-145">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="4950e-146">Jaemüüjad saavad rakendada isikupärastamist olemasolevatele soovituste loenditele, nagu „Uus”, „Populaarne”, „Enim müüdud”, „Inimestele meeldib ka” ja „Sageli koos ostetud”.</span><span class="sxs-lookup"><span data-stu-id="4950e-146">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="4950e-147">Olemasolevatele loenditele isikupärastamise rakendamisel eemaldatakse nendest loenditest sisselogitud kasutaja poolt varasemalt ostetud esemed.</span><span class="sxs-lookup"><span data-stu-id="4950e-147">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="4950e-148">Nii anonüümsetele kasutajatele kui isikupärastatud soovituste saamisest loobunud kasutajatele kuvatakse olemasolevate loendite vaikimisi versioonid.</span><span class="sxs-lookup"><span data-stu-id="4950e-148">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="4950e-149">Nii ei pea jaemüüjad eraldi lehe kogemust käsitsi haldama.</span><span class="sxs-lookup"><span data-stu-id="4950e-149">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="4950e-150">Näiteks on sisselogitud kasutaja juba ostnud musta kella ja pruunid töösaapad, mis ilmuvad järgmisel joonisel loendis „Populaarne – vaikimisi”.</span><span class="sxs-lookup"><span data-stu-id="4950e-150">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="4950e-151">Seetõttu näeb kasutaja nende toodete asemel uusi tooteid, nagu on näidatud loendis „Populaarne – isikustatud”.</span><span class="sxs-lookup"><span data-stu-id="4950e-151">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Isikupärastamise rakendamine](./media/applypersonalization.png)

<span data-ttu-id="4950e-153">Isikupärastamise rakendamiseks olemasolevale soovituste loendile rakenduse Commerce saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4950e-153">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4950e-154">Avage olemasoleva saidiehitaja leht, mis sisaldab tootekogumi moodulit.</span><span class="sxs-lookup"><span data-stu-id="4950e-154">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="4950e-155">Valige vasakpoolsel navigeerimispaanil tootekogumi moodul.</span><span class="sxs-lookup"><span data-stu-id="4950e-155">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="4950e-156">Valige parempoolsel navigeerimispaani jaotises **Tooted** loend.</span><span class="sxs-lookup"><span data-stu-id="4950e-156">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="4950e-157">Dialoogiaknas **Vali toote loendi konfigureerimine** jaotises **Tüüp** valige loendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="4950e-157">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="4950e-158">Valige märkeruut **Rakenda isikupärastamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="4950e-158">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Populaarsete loendile isikupärastamise rakendamine](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="4950e-160">Salvestage leht, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="4950e-160">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="4950e-161">Pärast lehe avaldamist kuvatakse sisselogitud kasutajatele isikupärastatud populaarsete loendeid.</span><span class="sxs-lookup"><span data-stu-id="4950e-161">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4950e-162">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4950e-162">Additional resources</span></span>

[<span data-ttu-id="4950e-163">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="4950e-163">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="4950e-164"> Azure Data Lake Storage'i lubamine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="4950e-164">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="4950e-165">Luba tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="4950e-165">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="4950e-166">„Sarnaste toodete vaatamise” soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="4950e-166">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="4950e-167">Isikupärastatud tootesoovitustest loobumine</span><span class="sxs-lookup"><span data-stu-id="4950e-167">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="4950e-168">Tootesoovituste lisamine kassas</span><span class="sxs-lookup"><span data-stu-id="4950e-168">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="4950e-169">Soovituste lisamine kandeekraanile</span><span class="sxs-lookup"><span data-stu-id="4950e-169">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="4950e-170">AI-ML-i soovituste tulemuste kohandamine</span><span class="sxs-lookup"><span data-stu-id="4950e-170">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="4950e-171">Loo kuraatorite soovitused käsitsi</span><span class="sxs-lookup"><span data-stu-id="4950e-171">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="4950e-172">Soovituste loomine demoandmetega</span><span class="sxs-lookup"><span data-stu-id="4950e-172">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="4950e-173">Tootesoovituste KKK</span><span class="sxs-lookup"><span data-stu-id="4950e-173">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
