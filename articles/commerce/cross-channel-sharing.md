---
title: Kanaliülese ühiskasutuse lubamine ja kasutamine
description: Selles teemas kirjeldatakse, kuidas lubada ja kasutada rakenduse Microsoft Dynamics 365 Commerce saidiehitaja kanaliülese ühiskasutuse funktsiooni.
author: psimolin
manager: annbe
ms.date: 10/09/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5dad866250bc57a9b158ee73948da509ecccd52c
ms.sourcegitcommit: 83ec80382bfeb693d5c5949b6f65296bd50eed12
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974075"
---
# <a name="enable-and-use-cross-channel-sharing"></a><span data-ttu-id="0793d-103">Kanaliülese ühiskasutuse lubamine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="0793d-103">Enable and use cross-channel sharing</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0793d-104">Selles teemas kirjeldatakse, kuidas lubada ja kasutada rakenduse Microsoft Dynamics 365 Commerce saidiehitaja kanaliülese ühiskasutuse funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="0793d-104">This topic describes how to enable and use the cross-channel sharing feature of Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="0793d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="0793d-105">Overview</span></span>

<span data-ttu-id="0793d-106">Kanaliülene ühiskasutus laseb jaemüüjatel taaskasutada ja jagada sisu saidi mitme kanali vahel.</span><span class="sxs-lookup"><span data-stu-id="0793d-106">Cross-channel sharing lets retailers reuse and share content among multiple channels of a site.</span></span> <span data-ttu-id="0793d-107">See võimalus on kasulik, kui saidi kanalitel on ühilduv baaskeel või kui neil on palju ühiseid sisuüksusi.</span><span class="sxs-lookup"><span data-stu-id="0793d-107">This capability is useful when the site channels have a compatible base language, or when they have numerous content items in common.</span></span>

<span data-ttu-id="0793d-108">Kanaliülene ühiskasutus toimib vaikekanali lubamise kaudu, millest otsitakse saadaolevat sisu, kui taotletud sisu kanalipõhist versiooni ei leita.</span><span class="sxs-lookup"><span data-stu-id="0793d-108">Cross-channel sharing works by enabling a default channel that will be searched for available content when a channel-specific version of the requested content isn't found.</span></span> <span data-ttu-id="0793d-109">Kanalite vahel jagamiseks mõeldud sisu luuakse vaikekanalis.</span><span class="sxs-lookup"><span data-stu-id="0793d-109">Content that is intended to be shared among channels is created in the default channel.</span></span> <span data-ttu-id="0793d-110">Seda sisu saab lokaliseerida mis tahes lokaadi jaoks, mida kasutatakse mis tahes saidikanalis.</span><span class="sxs-lookup"><span data-stu-id="0793d-110">That content can be localized for any locale that is used on any site channel.</span></span>

## <a name="when-to-use-cross-channel-sharing"></a><span data-ttu-id="0793d-111">Millal kanaliülest ühiskasutust kasutada?</span><span class="sxs-lookup"><span data-stu-id="0793d-111">When to use cross-channel sharing</span></span>

<span data-ttu-id="0793d-112">Kanaliülene ühiskasutus on kasulik, kui ühe saidi mitu kanalit saavad sisu jagada.</span><span class="sxs-lookup"><span data-stu-id="0793d-112">Cross-channel sharing is useful when multiple channels on a single site can share content.</span></span> <span data-ttu-id="0793d-113">Näiteks saab jaemüüja, kellel on mitu kaubamärki ja kauplust, mis on toodud ühele saidile, jagada osa sisust mõne või kõigi kauplustega.</span><span class="sxs-lookup"><span data-stu-id="0793d-113">For example, a retailer that has multiple brands and storefronts that are grouped under a single site can share some content among some or all of the storefronts.</span></span> <span data-ttu-id="0793d-114">See jagatud sisu võib hõlmata tingimuste, maksetingimuste, saatmisviiside ja korduma kippuvate küsimuste (KKK) lehti.</span><span class="sxs-lookup"><span data-stu-id="0793d-114">This shared content can include pages for terms and conditions, payment terms, shipment methods, and frequently asked questions (FAQ).</span></span>

<span data-ttu-id="0793d-115">Kanaliülene ühiskasutus toetab ka fragmente.</span><span class="sxs-lookup"><span data-stu-id="0793d-115">Cross-channel sharing also supports fragments.</span></span> <span data-ttu-id="0793d-116">Seetõttu on võimalik luua kanalipõhiseid fragmente sisaldav sisuleht kanaliülese sisuna.</span><span class="sxs-lookup"><span data-stu-id="0793d-116">Therefore, a content page that contains channel-specific fragments can be created as cross-channel content.</span></span> <span data-ttu-id="0793d-117">Sel juhul, kuigi enamikku sisust jagatakse kanalite vahel, renderdatakse kanalipõhised fragmendid kanaliülesel lehel ainult siis, kui neid päritakse asjaomase poe kanalist.</span><span class="sxs-lookup"><span data-stu-id="0793d-117">In this case, although most of the content will be shared among channels, channel-specific fragments on a cross-channel page will be rendered only when they are requested from the corresponding storefront channel.</span></span>

<span data-ttu-id="0793d-118">Saidid, millel on ainult üks kanal, või saidid, millel on mitu kanalit, mis ei saa sisu jagada, ei saa kanaliülesest ühiskasutusest kasu.</span><span class="sxs-lookup"><span data-stu-id="0793d-118">Sites that have only one channel, or sites that have multiple channels that can't share content, won't benefit from cross-channel sharing.</span></span>

## <a name="enable-cross-channel-sharing"></a><span data-ttu-id="0793d-119">Kanaliülese ühiskasutuse lubamine</span><span class="sxs-lookup"><span data-stu-id="0793d-119">Enable cross-channel sharing</span></span>

<span data-ttu-id="0793d-120">Kanaliülene ühiskasutus lubatakse saiditasemel.</span><span class="sxs-lookup"><span data-stu-id="0793d-120">Cross-channel sharing is enabled at the site level.</span></span> <span data-ttu-id="0793d-121">See toiming on ühesuunaline.</span><span class="sxs-lookup"><span data-stu-id="0793d-121">This operation is one-way.</span></span> <span data-ttu-id="0793d-122">Teisisõnu ei saa pärast kanaliülese ühiskasutuse lubamist seda enam keelata.</span><span class="sxs-lookup"><span data-stu-id="0793d-122">In other words, after cross-channel sharing is enabled, it can't be disabled.</span></span>

<span data-ttu-id="0793d-123">Et lubada kanaliülene ühiskasutus Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0793d-123">To enable cross-channel sharing in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0793d-124">Avage **Saidi sätted \> Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0793d-124">Go to **Site settings \> Features**.</span></span>
1. <span data-ttu-id="0793d-125">Seadke funktsiooni **Kanaliülene** suvandi väärtuseks **Sees**.</span><span class="sxs-lookup"><span data-stu-id="0793d-125">Set the option for the **Cross Channel** feature to **On**.</span></span>

    ![Commerce'i saidiehitajas sisselülitatud kanaliülene suvand](./media/enabling-cross-channel-sharing.png)

<span data-ttu-id="0793d-127">Pärast seda, kui lubate kanaliülese ühiskasutuse, kuvatakse kanaliülene teave jaotises **Kanalid**, mis asub jaotises **Saidi sätted \> Funktsioonid**, nagu järgmisel illustratsioonil näha.</span><span class="sxs-lookup"><span data-stu-id="0793d-127">After you enable cross-channel sharing, cross-channel information will appear in the **Channels** section at **Site settings \> Features**, as the example in the following illustration shows.</span></span>

![Kanalite teave, mis on nähtav pärast kanaliülese ühiskasutuse lubamist](./media/channels-cross-channel.png)

<span data-ttu-id="0793d-129">Pärast seda, kui lubate kanaliülese ühiskasutuse, sisaldab Commerce'i saidiehitaja ülemises parempoolses nurgas olev väli **Kanal** suvandit **Kanaliülene e-pood**, mille abil saate hallata kanaliülest sisu, nagu on näidatud järgmisel illustratsioonil.</span><span class="sxs-lookup"><span data-stu-id="0793d-129">Additionally, after you enable cross-channel sharing, the **Channel** field in the upper right of Commerce site builder will include a **Cross Channel Online Store** option that you can use to manage cross-channel content, as shown in the following illustration.</span></span>

![Kanaliülese e-poe suvand väljal „Kanalid” pärast kanaliülese ühiskasutuse lubamist](./media/cross-channel-dropdown.png)

## <a name="create-and-use-cross-channel-content"></a><span data-ttu-id="0793d-131">Kanaliülese sisu loomine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="0793d-131">Create and use cross-channel content</span></span>

<span data-ttu-id="0793d-132">Kanaliülest sisu saate luua ja kasutada mitmel viisil.</span><span class="sxs-lookup"><span data-stu-id="0793d-132">You can create and use cross-channel content in multiple ways.</span></span> <span data-ttu-id="0793d-133">Näiteks saate luua kanaliüleseid fragmente, kanaliüleseid lehti, mis kasutavad kanaliülest ja kanalispetsiifilist sisu, ning alistada fragmentide kanalispetsiifiliste versioonide kaudu kanaliüleseid fragmente.</span><span class="sxs-lookup"><span data-stu-id="0793d-133">For example, you can create cross-channel fragments, create cross-channel pages that use cross-channel and channel-specific content, and override cross-channel fragments with channel-specific versions of fragments.</span></span>

### <a name="create-a-cross-channel-fragment"></a><span data-ttu-id="0793d-134">Kanaliülese fragmendi loomine</span><span class="sxs-lookup"><span data-stu-id="0793d-134">Create a cross-channel fragment</span></span>

<span data-ttu-id="0793d-135">Et luua kanaliülene fragment Commerce'i saidiehitajas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0793d-135">To create a cross-channel fragment in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0793d-136">Avage **Fragmendid** ja valige uue fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0793d-136">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0793d-137">Valige dialoogiboksis **Uus lehe fragment** moodul **Reklaambänner** ja seejärel sisestage jaotises **Lehe fragmendi nimi** sellele nimi (nt **Kanaliülene bänner**).</span><span class="sxs-lookup"><span data-stu-id="0793d-137">In the **New page fragment** dialog box, select the **Promo banner** module, and then, under **Page fragment name**, enter a name (for example, **Cross-channel banner**).</span></span> <span data-ttu-id="0793d-138">Seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-138">Then select **OK**.</span></span>
1. <span data-ttu-id="0793d-139">Tehke mooduli **Reklaambänner** atribuudipaanil valikud **Lisa teade** ja **Teade**.</span><span class="sxs-lookup"><span data-stu-id="0793d-139">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="0793d-140">Sisestage dialoogiboksis **Teade** väljale **Tekst** väärtus **Kanaliülene** ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-140">In the **Message** dialog box, under **Text**, enter **Cross-channel**, and the select **OK**.</span></span> 
1. <span data-ttu-id="0793d-141">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0793d-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0793d-142">Seda kanaliülest fragmenti saab kasutada kanaliülestel või kanalispetsiifilistel lehtedel, mis on loodud mis tahes saidikanalis.</span><span class="sxs-lookup"><span data-stu-id="0793d-142">This cross-channel fragment can be used on cross-channel or channel-specific pages that are created on any site channel.</span></span>

### <a name="create-a-cross-channel-page-that-uses-cross-channel-content"></a><span data-ttu-id="0793d-143">Kanaliülese lehe loomine, mis kasutab kanaliülest sisu</span><span class="sxs-lookup"><span data-stu-id="0793d-143">Create a cross-channel page that uses cross-channel content</span></span>

<span data-ttu-id="0793d-144">Kanaliüleseid lehti saab kasutada teie saidi mis tahes kanalis.</span><span class="sxs-lookup"><span data-stu-id="0793d-144">Cross-channel pages can be used on any channel of your site.</span></span> <span data-ttu-id="0793d-145">Seetõttu saate luua jagatud sisulehe üks kord ja värskendada seda hiljem ühes kohas.</span><span class="sxs-lookup"><span data-stu-id="0793d-145">Therefore, you can create a shared content page one time and make any subsequent updates in a single place.</span></span> <span data-ttu-id="0793d-146">Näiteks on võimalik jagada kanaliülest lehte **Tingimused**, mille URL on `/toc`, kõikide saidil olevate kanalite vahel.</span><span class="sxs-lookup"><span data-stu-id="0793d-146">For example, a cross-channel **Terms and conditions** page that has the URL `/toc` can be shared among all the channels of a site.</span></span> <span data-ttu-id="0793d-147">Kui saidikanalite baas-URL-id on `www.fabrikam.com/brand1` ja `www.fabrikam.com/brand2`, siis on sama kanaliülene jagatud leht **Tingimused** saadaval mõlema saidikanali URL-idel vastavalt `www.fabrikam.com/brand1/toc` ja `www.fabrikam.com/brand2/toc`.</span><span class="sxs-lookup"><span data-stu-id="0793d-147">If the base URLs for the site channels are `www.fabrikam.com/brand1` and `www.fabrikam.com/brand2`, the same cross-channel, shared **Terms and conditions** page will be available from both site channel URLs, at `www.fabrikam.com/brand1/toc` and `www.fabrikam.com/brand2/toc`, respectively.</span></span> <span data-ttu-id="0793d-148">Kui lehte **Tingimused** tuleb hiljem värskendada, peate värskendama ainult üht jagatud lehte.</span><span class="sxs-lookup"><span data-stu-id="0793d-148">If the **Terms and conditions** page must be updated later, you have to update only the single, shared page.</span></span>

<span data-ttu-id="0793d-149">Commerce'i saidiehitajas kanaliülese lehe loomiseks, mis kasutab kanaliülest sisu, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0793d-149">To create a cross-channel page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="0793d-150">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0793d-150">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="0793d-151">Valige dialoogiboksis **Malli valimine** mõni mall, näiteks **Turundus**.</span><span class="sxs-lookup"><span data-stu-id="0793d-151">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="0793d-152">Sisestage väljale **Lehe nimi** lehele nimi (näiteks **Kanaliülene leht**).</span><span class="sxs-lookup"><span data-stu-id="0793d-152">Under **Page name**, enter a name for the page (for example, **Cross-channel page**).</span></span>
1. <span data-ttu-id="0793d-153">Sisestage väljale **Lehe URL** lehele URL (nt **examplepage**) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-153">Under **Page URL**, enter a page URL (for example, **examplepage**), and then select **OK**.</span></span>
1. <span data-ttu-id="0793d-154">Valige uue lehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="0793d-154">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="0793d-155">Valige dialoogiboksis **Fragmendi lisamine** varem loodud kanaliülene fragment, millel on reklaambänner, ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-155">In the **Add Fragment** dialog box, select the cross-channel fragment that you created earlier that has a promo banner, and then select **OK**.</span></span>
1. <span data-ttu-id="0793d-156">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="0793d-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0793d-157">Peaksite nägema reklaambännerit, millel on kiri „Kanaliülene”.</span><span class="sxs-lookup"><span data-stu-id="0793d-157">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="0793d-158">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0793d-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-page-that-uses-cross-channel-content"></a><span data-ttu-id="0793d-159">Kanalispetsiifilise lehe loomine, mis kasutab kanaliülest sisu</span><span class="sxs-lookup"><span data-stu-id="0793d-159">Create a channel-specific page that uses cross-channel content</span></span>

<span data-ttu-id="0793d-160">Kui kasutate kanaliülest sisu kanalispetsiifilisel lehtedel, saate luua jagatud sisufragmendi ühe korra ja seejärel kasutada seda kanalispetsiifilistel lehtedel.</span><span class="sxs-lookup"><span data-stu-id="0793d-160">By using cross-channel content on channel-specific pages, you can create a shared content fragment one time and then use it on channel-specific pages.</span></span> <span data-ttu-id="0793d-161">See „ühekordne allikas” on kasulik jagatud sisu jaoks, nagu tingimused, maksetingimused või kontaktteave.</span><span class="sxs-lookup"><span data-stu-id="0793d-161">This "single sourcing" is useful for shared content such as terms and conditions, payment terms, or contact information.</span></span>

<span data-ttu-id="0793d-162">Commerce'i saidiehitajas kanalispetsiifilise lehe loomiseks, mis kasutab kanaliülest sisu, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0793d-162">To create a channel-specific page in Commerce site builder that uses cross-channel content, follow these steps.</span></span>

1. <span data-ttu-id="0793d-163">Avage kindlas kanalis, näiteks kanalis **Fabrikami laiendatud e-pood**, jaotis **Lehed** ja valige **Uus**, et luua uus leht.</span><span class="sxs-lookup"><span data-stu-id="0793d-163">From within a specific channel, such as **Fabrikam extended online store**, go to **Pages**, and then select **New** to create a new page.</span></span>
1. <span data-ttu-id="0793d-164">Valige dialoogiboksis **Malli valimine** mõni mall, näiteks **Turundus**.</span><span class="sxs-lookup"><span data-stu-id="0793d-164">In the **Choose a template** dialog box, select a template, such as **Marketing**.</span></span>
1. <span data-ttu-id="0793d-165">Sisestage väljale **Lehe nimi** lehele nimi (näiteks **Kanalispetsiifiline leht**).</span><span class="sxs-lookup"><span data-stu-id="0793d-165">Under **Page name**, enter a name for the page (for example, **Channel-specific page**).</span></span>
1. <span data-ttu-id="0793d-166">Sisestage väljale **Lehe URL** lehele URL (nt **channelspecificpage**) ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-166">Under **Page URL**, enter a page URL (for example, **channelspecificpage**), and then select **OK**.</span></span>
1. <span data-ttu-id="0793d-167">Valige uue lehe jaotises **Peamine** kolmikpunkt (**...**) ja seejärel valige **Lisa fragment**.</span><span class="sxs-lookup"><span data-stu-id="0793d-167">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="0793d-168">Valige dialoogiboksis **Fragmendi lisamine** jaotises **Kanal** suvand **Kanaliülene e-pood**.</span><span class="sxs-lookup"><span data-stu-id="0793d-168">In the **Add Fragment** dialog box, under **Channel**, select **Cross Channel Online Store**.</span></span> <span data-ttu-id="0793d-169">Varem loodud kanaliülene fragment peaks loendis olema.</span><span class="sxs-lookup"><span data-stu-id="0793d-169">The cross-channel fragment that you created earlier should appear in the list.</span></span> <span data-ttu-id="0793d-170">Valige see ning seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-170">Select it, and then select **OK**.</span></span>
1. <span data-ttu-id="0793d-171">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="0793d-171">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0793d-172">Peaksite nägema reklaambännerit, millel on kiri „Kanaliülene”.</span><span class="sxs-lookup"><span data-stu-id="0793d-172">You should see the promo banner that says, "Cross-channel."</span></span>
1. <span data-ttu-id="0793d-173">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0793d-173">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

### <a name="create-a-channel-specific-version-of-a-cross-channel-page"></a><span data-ttu-id="0793d-174">Kanaliülese lehe kanalispetsiifilise versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="0793d-174">Create a channel-specific version of a cross-channel page</span></span>

<span data-ttu-id="0793d-175">Kanaliülene ühiskasutus toetab kanaliülese sisu alistamist.</span><span class="sxs-lookup"><span data-stu-id="0793d-175">Cross-channel sharing supports overrides of cross-channel content.</span></span> <span data-ttu-id="0793d-176">Näiteks jagavad kõik saidikanalid peale ühe sama kindlat sisu.</span><span class="sxs-lookup"><span data-stu-id="0793d-176">For example, all but one of your site channels share the same piece of content.</span></span> <span data-ttu-id="0793d-177">See üks saidikanal vajab erinevat sisu.</span><span class="sxs-lookup"><span data-stu-id="0793d-177">That one site channel requires different content.</span></span> <span data-ttu-id="0793d-178">Selleks, et rakendada selle puhul erinevat sisu, peate alistama kanaliülese sisu kanalispetsiifilise sisuga, luues kanaliülesest lehest kanalispetsiifilise versiooni.</span><span class="sxs-lookup"><span data-stu-id="0793d-178">To implement the different content for it, you override the cross-channel content with channel-specific content by creating a channel-specific version of the cross-channel page.</span></span>

<span data-ttu-id="0793d-179">Commerce'i saidiehitajas kanaliülese lehe kanalispetsiifilise versiooni loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0793d-179">To create a channel-specific version of a cross-channel page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0793d-180">Valige ülemises parempoolses väljas **Kanal** suvand **Kanaliülene e-pood**.</span><span class="sxs-lookup"><span data-stu-id="0793d-180">In the **Channel** field in the upper right, select **Cross Channel Online Store**.</span></span>
1. <span data-ttu-id="0793d-181">Avage varem loodud kanaliülene leht.</span><span class="sxs-lookup"><span data-stu-id="0793d-181">Open the cross-channel page that you created earlier.</span></span>
1. <span data-ttu-id="0793d-182">Valige ülemises parempoolses väljas **Kanal** see kanal, millel peaks olema kindel sisu.</span><span class="sxs-lookup"><span data-stu-id="0793d-182">In the **Channel** field in the upper right, select the channel that should have specific content.</span></span> <span data-ttu-id="0793d-183">Leheredaktor kuvab teate, mis palub teil luua uus lehevariant.</span><span class="sxs-lookup"><span data-stu-id="0793d-183">The page editor shows a message that prompts you to create a new page variant.</span></span>
1. <span data-ttu-id="0793d-184">Valige **Loo lehevariant**.</span><span class="sxs-lookup"><span data-stu-id="0793d-184">Select **Create page variant**.</span></span>
1. <span data-ttu-id="0793d-185">Valige lehevariandi pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0793d-185">In the **Main** slot of the page variant, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0793d-186">Valige dialoogiboksis **Mooduli lisamine** moodul **Reklaambänner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-186">In the **Add Module** dialog box, select the **Promo banner** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0793d-187">Tehke mooduli **Reklaambänner** atribuudipaanil valikud **Lisa teade** ja **Teade**.</span><span class="sxs-lookup"><span data-stu-id="0793d-187">In the property pane for the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="0793d-188">Sisestage dialoogiboksis **Teade** väljale **Tekst** väärtus **Kanalispetsiifiline** ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0793d-188">In the **Message** dialog box, under **Text**, enter **Channel-specific**, and the select **OK**.</span></span>
1. <span data-ttu-id="0793d-189">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="0793d-189">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0793d-190">Peaksite nägema reklaambännerit, millel on kiri „Kanalispetsiifiline”.</span><span class="sxs-lookup"><span data-stu-id="0793d-190">You should see the promo banner that says, "Channel-specific."</span></span>
1. <span data-ttu-id="0793d-191">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0793d-191">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0793d-192">Kui te kasutate nüüd kanali baas-URL-i ja avate selle saidi kanaliülese lehe URL-i, näete kanaliülese sisu asemel kanalispetsiifilist sisu.</span><span class="sxs-lookup"><span data-stu-id="0793d-192">Now, if you use the base URL of the channel and go to the URL of the cross-channel page on that site, you will see the channel-specific content instead of the cross-channel content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0793d-193">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0793d-193">Additional resources</span></span>

[<span data-ttu-id="0793d-194">Sisu lisamise viisid</span><span class="sxs-lookup"><span data-stu-id="0793d-194">Ways to add content</span></span>](add-manage-content.md)

[<span data-ttu-id="0793d-195">Lehemudeli sõnastik</span><span class="sxs-lookup"><span data-stu-id="0793d-195">Page model glossary</span></span>](page-elements-overview.md)

[<span data-ttu-id="0793d-196">Dokumendi olekud ja töötsükkel</span><span class="sxs-lookup"><span data-stu-id="0793d-196">Document states and lifecycle</span></span>](document-states-overview.md)

[<span data-ttu-id="0793d-197">Avaldamisrühmadega töötamine</span><span class="sxs-lookup"><span data-stu-id="0793d-197">Work with publish groups</span></span>](publish-groups.md)