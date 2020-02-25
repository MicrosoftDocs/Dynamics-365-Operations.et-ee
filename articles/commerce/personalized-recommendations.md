---
title: Isikupärastatud tootesoovituste lubamine
description: See teema kirjeldab, kuidas teha rakenduses Microsoft Dynamics 365 Commerce isikupärastatud tootesoovitused klientidele kättesaadavaks.
author: bebeale
manager: AnnBe
ms.date: 01/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 6b3c6140b8bd3ea15458223c0f61810421d0b2bc
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3025241"
---
# <a name="enable-personalized-recommendations"></a><span data-ttu-id="d03ca-103">Isikupärastatud soovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="d03ca-103">Enable personalized recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d03ca-104">See teema kirjeldab, kuidas teha rakenduses Microsoft Dynamics 365 Commerce isikupärastatud tootesoovitused klientidele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="d03ca-104">This topic describes how to make personalized product recommendations available for customers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d03ca-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d03ca-105">Overview</span></span>

<span data-ttu-id="d03ca-106">Rakenduses Dynamics 365 Commerce saavad jaemüüjad teha kättesaadavaks isikupärastatud tootesoovitused (tuntud ka kui isikupärastamine).</span><span class="sxs-lookup"><span data-stu-id="d03ca-106">In Dynamics 365 Commerce, retailers can make personalized product recommendations (also known as personalization) available.</span></span> <span data-ttu-id="d03ca-107">Sel viisil saab isikupärastatud soovitusi lisada kliendi kasutuskogemusele veebis ja kassas.</span><span class="sxs-lookup"><span data-stu-id="d03ca-107">In this way, personalized recommendations can be incorporated into the customer experience online and at the point of sale (POS).</span></span> <span data-ttu-id="d03ca-108">Kui isikupärastamise funktsioon on sisse lülitatud, saab süsteem seostada kasutaja ostu- ja tooteteabe individualiseeritud tootesoovituste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="d03ca-108">When the personalization functionality is turned on, the system can associate a user's purchase and product information to generate individualized product recommendations.</span></span>

## <a name="personalization-prerequisites"></a><span data-ttu-id="d03ca-109">Isikupärastamise eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d03ca-109">Personalization prerequisites</span></span>

<span data-ttu-id="d03ca-110">Enne isikupärastatud soovituste klientidele kättesaadavaks tegemist võtke arvesse, et tootesoovitusi toetatakse ainult nende Commerce’i kasutajate jaoks, kes on migreerinud oma salvestusruumi Azure Data Lake’i salve.</span><span class="sxs-lookup"><span data-stu-id="d03ca-110">Before you make personalized product recommendations available for customers, note that product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Store.</span></span> <span data-ttu-id="d03ca-111">Enne kui kliendid saavad võtta vastu isikupärastatud tootesoovitusi, peavad jaemüüjad [lülitama tootesoovitused sisse](enable-product-recommendations.md)soovitused sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="d03ca-111">Before customers can receive personalized product recommendations, retailers must [turn on product recommendations](enable-product-recommendations.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d03ca-112">Tootesoovituste sisselülitamisega lülitate sisse ka isikupärastamise.</span><span class="sxs-lookup"><span data-stu-id="d03ca-112">By turning on product recommendations, you also turn on personalization.</span></span> <span data-ttu-id="d03ca-113">Kuid kui lülitate isikupärastamise välja, ei saa te muud tüüpi tootesoovitusi välja lülitada.</span><span class="sxs-lookup"><span data-stu-id="d03ca-113">However, if you turn off personalization, you don't turn off the other types of product recommendations.</span></span>

<span data-ttu-id="d03ca-114">Lisateavet tootesoovituste kohta leiate teemast [Tootesoovituste ülevaade](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="d03ca-114">For more information about product recommendations, see the [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="turn-on-personalization"></a><span data-ttu-id="d03ca-115">Isikupärastamise sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="d03ca-115">Turn on personalization</span></span>

<span data-ttu-id="d03ca-116">Isikupärastamise sisselülitamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d03ca-116">To turn on personalization, follow these steps.</span></span>

1. <span data-ttu-id="d03ca-117">Avage **Jaemüük ja kaubandus \> Tootesoovitused \> Soovituste parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d03ca-117">Go to **Retail and commerce \> Product recommendations \> Recommendation parameters**.</span></span>
1. <span data-ttu-id="d03ca-118">Retaili jagatud parameetrite loendis valige suvand **Soovituste loendid**.</span><span class="sxs-lookup"><span data-stu-id="d03ca-118">In the list of Retail shared parameters, select **Recommendation lists**.</span></span>
1. <span data-ttu-id="d03ca-119">Seadke suvand **Luba isikupärastamine** valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d03ca-119">Set the **Enable personalization** option to **Yes**.</span></span>

![Isikupärastamise sisselülitamine](./media/enablepersonalization.png)

> [!NOTE]
> <span data-ttu-id="d03ca-121">Kui lülitate isikupärastamise sisse, käivitatakse isikupärastatud tootesoovituste loendite loomise protsess.</span><span class="sxs-lookup"><span data-stu-id="d03ca-121">When you turn on personalization, the process of generating personalized product recommendation lists is started.</span></span> <span data-ttu-id="d03ca-122">Kuluda võib kuni üks päev enne, kui need loendid on saadaval ja nähtavad veebis ning kassas.</span><span class="sxs-lookup"><span data-stu-id="d03ca-122">Up to one day might be required before these lists are available and visible online and at the POS.</span></span>

## <a name="personalized-lists"></a><span data-ttu-id="d03ca-123">Isikupärastatud loendid</span><span class="sxs-lookup"><span data-stu-id="d03ca-123">Personalized lists</span></span>

<span data-ttu-id="d03ca-124">Lisaks olemasolevate arvuti loodud loendite isikupärastamise lubamisele võimaldab soovituste teenus toote avastamise kogemuse isikupärastamist nii võrgus kui ka kassas.</span><span class="sxs-lookup"><span data-stu-id="d03ca-124">In addition to allowing for personalization of existing machine-generated lists, the recommendations service allows for personalization of the product discovery experience both online and at the POS.</span></span>

<span data-ttu-id="d03ca-125">Pärast isikupärastamise sisselülitamist saavad jaemüüjad kuvada ostjatele isikustatud loendeid „Teile valitud” veebis või loendeid „Kliendile soovitatud” kassaterminalis.</span><span class="sxs-lookup"><span data-stu-id="d03ca-125">After personalization is turned on, retailers can show shoppers personalized "Picks for you" lists online or "Recommended for customer" lists on POS terminals.</span></span> <span data-ttu-id="d03ca-126">Lisaks saavad jaemüüjad rakendada isikupärastamist olemasolevatele tootesoovituse loenditele ja pakkuda autenditud kasutajate jaoks isikuandmete kaitse üldmäärusest (GDPR) loobumise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="d03ca-126">Additionally, retailers can apply personalization to existing product recommendation lists and provide General Data Protection Regulation (GDPR) opt-out experiences for authenticated users.</span></span> <span data-ttu-id="d03ca-127">Kui lülitate isikupärastamise välja, lülitate ka need funktsioonid välja.</span><span class="sxs-lookup"><span data-stu-id="d03ca-127">If you turn off personalization, you also turn off these features.</span></span>

### <a name="online-picks-for-you-lists"></a><span data-ttu-id="d03ca-128">Veebipõhised loendid „Teile valitud”</span><span class="sxs-lookup"><span data-stu-id="d03ca-128">Online "Picks for you" lists</span></span>

<span data-ttu-id="d03ca-129">Loend „Teile valitud” on tehisintellekti masinõppe (AI-ML) loend, mis kuvab autenditud kasutaja soovitatud toodete isikupärastatud loendi.</span><span class="sxs-lookup"><span data-stu-id="d03ca-129">A "Picks for you" list is an artificial intelligence-machine learning (AI-ML) list that shows an authenticated user a personalized list of suggested products.</span></span> <span data-ttu-id="d03ca-130">See loend põhineb kasutaja omnikanali ostuajalool.</span><span class="sxs-lookup"><span data-stu-id="d03ca-130">This list is based on the user's omnichannel purchase history.</span></span> <span data-ttu-id="d03ca-131">Isikupärastatud soovitusi värskendatakse dünaamiliselt, kui kasutaja teeb rohkem oste.</span><span class="sxs-lookup"><span data-stu-id="d03ca-131">Personalized recommendations are dynamically updated as the user makes more purchases.</span></span> <span data-ttu-id="d03ca-132">Seda tüüpi loend toetab ka kategooria filtreerimist, nii et jaemüüjad saavad kuvada navigeerimise hierarhial põhinevad peamised valikud.</span><span class="sxs-lookup"><span data-stu-id="d03ca-132">This type of list also supports category filtering, so that retailers can show top picks, based on navigational hierarchies.</span></span>

<span data-ttu-id="d03ca-133">Enne kui loend „Teile valitud” saab e-kaubanduse lehel ilmuda, peavad järgmised kasutajanõuded olema täidetud.</span><span class="sxs-lookup"><span data-stu-id="d03ca-133">Before the "Picks for you" list can appear on any e-Commerce page, the following user requirements must be met:</span></span>

- <span data-ttu-id="d03ca-134">Kasutajad peavad olema sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="d03ca-134">Users must be signed in.</span></span> <span data-ttu-id="d03ca-135">Anonüümsed kasutajad ei näe isikupärastatud soovitusi.</span><span class="sxs-lookup"><span data-stu-id="d03ca-135">Anonymous users won't see personalized recommendations.</span></span>
- <span data-ttu-id="d03ca-136">Kasutajatel peab olema kontol vähemalt üks ost.</span><span class="sxs-lookup"><span data-stu-id="d03ca-136">Users must have at least one purchase on their account.</span></span>
- <span data-ttu-id="d03ca-137">Kasutajad peavad isikupärastatud soovituste saamisega nõustuma.</span><span class="sxs-lookup"><span data-stu-id="d03ca-137">Users must opt in to receive personalized recommendations.</span></span>

<span data-ttu-id="d03ca-138">Järgmisel joonisel on kujutatud loendi „Teile valitud” näide veebipoe lehel.</span><span class="sxs-lookup"><span data-stu-id="d03ca-138">The following illustration shows an example of a "Picks for you" list on an online store page.</span></span>

![Veebipõhine loend Teile valitud](./media/picksforyou.png)

### <a name="recommended-for-customer-lists-at-the-pos"></a><span data-ttu-id="d03ca-140">Loendid „Kliendile soovitatud” kassas</span><span class="sxs-lookup"><span data-stu-id="d03ca-140">"Recommended for customer" lists at the POS</span></span>

<span data-ttu-id="d03ca-141">Oma kliendisuhtluse kogemuse parandamiseks saavad jaemüüjad isikupärastada olemasolevate klientide üksikasjade lehti, lisades kontekstipõhise loendi „Kliendile soovitatud”.</span><span class="sxs-lookup"><span data-stu-id="d03ca-141">To enhance their clienteling experience, retailers can personalize existing customer details pages by adding a contextual "Recommended for customer" list.</span></span>

<span data-ttu-id="d03ca-142">Järgmisel joonisel on kujutatud loendi „Kliendile soovitatud” näide kassaterminalis.</span><span class="sxs-lookup"><span data-stu-id="d03ca-142">The following illustration shows an example of a "Recommended for customer" list on a POS terminal.</span></span>

![Loend Kliendile soovitatud kassas](./media/picksonpos.png)

## <a name="apply-personalization-to-existing-recommendation-lists"></a><span data-ttu-id="d03ca-144">Isikupärastamise rakendamine olemasolevatele soovituste loenditele</span><span class="sxs-lookup"><span data-stu-id="d03ca-144">Apply personalization to existing recommendation lists</span></span>

<span data-ttu-id="d03ca-145">Jaemüüjad saavad rakendada isikupärastamist olemasolevatele soovituste loenditele, nagu „Uus”, „Populaarne”, „Enim müüdud”, „Inimestele meeldib ka” ja „Sageli koos ostetud”.</span><span class="sxs-lookup"><span data-stu-id="d03ca-145">Retailers can apply personalization to existing recommendation lists, such as "New," "Trending," "Best selling," "People also like," and "Frequently bought together."</span></span> <span data-ttu-id="d03ca-146">Olemasolevatele loenditele isikupärastamise rakendamisel eemaldatakse nendest loenditest sisselogitud kasutaja poolt varasemalt ostetud esemed.</span><span class="sxs-lookup"><span data-stu-id="d03ca-146">When personalization is applied to existing lists, items that a signed-in user previously bought are removed from those lists.</span></span> <span data-ttu-id="d03ca-147">Nii anonüümsetele kasutajatele kui isikupärastatud soovituste saamisest loobunud kasutajatele kuvatakse olemasolevate loendite vaikimisi versioonid.</span><span class="sxs-lookup"><span data-stu-id="d03ca-147">For both anonymous users and users who opted out of receiving personalized recommendations, default versions of the existing lists are shown.</span></span> <span data-ttu-id="d03ca-148">Nii ei pea jaemüüjad eraldi lehe kogemust käsitsi haldama.</span><span class="sxs-lookup"><span data-stu-id="d03ca-148">Therefore, retailers don't have to manually maintain separate page experiences.</span></span>

<span data-ttu-id="d03ca-149">Näiteks on sisselogitud kasutaja juba ostnud musta kella ja pruunid töösaapad, mis ilmuvad järgmisel joonisel loendis „Populaarne – vaikimisi”.</span><span class="sxs-lookup"><span data-stu-id="d03ca-149">For example, a signed-in user has already bought the black watch and the brown work boots that appear in the "Trending - default" list in the following illustration.</span></span> <span data-ttu-id="d03ca-150">Seetõttu näeb kasutaja nende toodete asemel uusi tooteid, nagu on näidatud loendis „Populaarne – isikustatud”.</span><span class="sxs-lookup"><span data-stu-id="d03ca-150">Therefore, the user will see new products instead of those products, as shown in the "Trending - personalized" list.</span></span>

![Isikupärastamise rakendamine](./media/applypersonalization.png)

<span data-ttu-id="d03ca-152">Isikupärastamise rakendamiseks olemasolevale soovituste loendile rakenduse Commerce saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d03ca-152">To apply personalization to an existing recommendation list in the Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="d03ca-153">Avage olemasoleva saidiehitaja leht, mis sisaldab tootekogumi moodulit.</span><span class="sxs-lookup"><span data-stu-id="d03ca-153">Open an existing site builder page that contains a product collection module.</span></span>
1. <span data-ttu-id="d03ca-154">Valige vasakpoolsel navigeerimispaanil tootekogumi moodul.</span><span class="sxs-lookup"><span data-stu-id="d03ca-154">In the left navigation pane, select the product collection module.</span></span>
1. <span data-ttu-id="d03ca-155">Valige parempoolsel navigeerimispaani jaotises **Tooted** loend.</span><span class="sxs-lookup"><span data-stu-id="d03ca-155">In the right navigation pane, under **Products**, select the list.</span></span>
1. <span data-ttu-id="d03ca-156">Dialoogiaknas **Vali toote loendi konfigureerimine** jaotises **Tüüp**valige loendi tüüp.</span><span class="sxs-lookup"><span data-stu-id="d03ca-156">In the **Select product list configuration** dialog box, under **Type**, select the list type.</span></span>
1. <span data-ttu-id="d03ca-157">Valige märkeruut **Rakenda isikupärastamine** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="d03ca-157">Select the **Apply Personalization** check box, and then select **OK**.</span></span>

    ![Populaarsete loendile isikupärastamise rakendamine](./media/ApplyPersonalizationToTrending.PNG)

1. <span data-ttu-id="d03ca-159">Salvestage leht, lõpetage selle redigeerimine ja seejärel avaldage see.</span><span class="sxs-lookup"><span data-stu-id="d03ca-159">Save the page, finish editing it, and then publish it.</span></span> <span data-ttu-id="d03ca-160">Pärast lehe avaldamist kuvatakse sisselogitud kasutajatele isikupärastatud populaarsete loendeid.</span><span class="sxs-lookup"><span data-stu-id="d03ca-160">After the page is published, signed-in users will see personalized trending lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d03ca-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d03ca-161">Additional resources</span></span>

[<span data-ttu-id="d03ca-162">Tootesoovituste ülevaade</span><span class="sxs-lookup"><span data-stu-id="d03ca-162">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="d03ca-163">Tootesoovituste lubamine</span><span class="sxs-lookup"><span data-stu-id="d03ca-163">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="d03ca-164">GDPR ja tootesoovitused</span><span class="sxs-lookup"><span data-stu-id="d03ca-164">GDPR and product recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="d03ca-165">Tootesoovituste loendite lisamine lehtedele</span><span class="sxs-lookup"><span data-stu-id="d03ca-165">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)

[<span data-ttu-id="d03ca-166">Kassaseadmetele soovituste paneeli lisamine</span><span class="sxs-lookup"><span data-stu-id="d03ca-166">Add recommendations panel to POS devices</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="d03ca-167">Tootekogumi mooduli ülevaade</span><span class="sxs-lookup"><span data-stu-id="d03ca-167">Product collection module overview</span></span>](product-collection-module-overview.md)
