---
title: Privaatsuspoliitika lehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: v-chgri
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce6491d176f90717877f084b11546010084c5f3b
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761269"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="dd564-103">Privaatsuspoliitika lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="dd564-103">Add a privacy policy page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dd564-104">Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.</span><span class="sxs-lookup"><span data-stu-id="dd564-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dd564-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="dd564-105">Overview</span></span>

<span data-ttu-id="dd564-106">Privaatsuse vastavus hõlmab organisatsioonilisi meetmeid, mis teavitavad saidi kasutajaid nende andmete kogumisest ja käitlemisest.</span><span class="sxs-lookup"><span data-stu-id="dd564-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="dd564-107">Kasutajad saavad seejärel otsustada, kuidas nad soovivad oma isiklikke andmeid töödelda ja võtta asjakohaseid meetmeid.</span><span class="sxs-lookup"><span data-stu-id="dd564-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="dd564-108">Microsofti privaatsusavalduse ülevaatamine Dynamics 365 Commerce'is</span><span class="sxs-lookup"><span data-stu-id="dd564-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="dd564-109">Microsofti privaatsusavalduse ülevaatamiseks, kui olete sisse logitud Dynamics 365 Commerce, valige ülemises parempoolses nurgas nupp **spikker** (**?**) ja seejärel valige **Privaatsus ja küpsised.**</span><span class="sxs-lookup"><span data-stu-id="dd564-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="dd564-110">Avatakse uus vahekaart, millel on link [Microsofti privaatsusavaldusele.](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="dd564-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="dd564-111">Oma saidi privaatsuspoliitika loomine</span><span class="sxs-lookup"><span data-stu-id="dd564-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="dd564-112">Rakenduses Dynamics 365 Commerceon mitu võimalust, kuidas anda kasutajatele saidile juurdepääs teie privaatsuspoliitikale.</span><span class="sxs-lookup"><span data-stu-id="dd564-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="dd564-113">Selles jaotises kirjeldatakse, kuidas luua privaatsuspoliitika lehte ja seejärel viidata leheküljele, kasutades jaluse fragmenti.</span><span class="sxs-lookup"><span data-stu-id="dd564-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="dd564-114">Järgnev juhend on näide, mis näitab, kuidas luua Commerce saidi üldise privaatsuspoliitika lehte.</span><span class="sxs-lookup"><span data-stu-id="dd564-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="dd564-115">Olete vastutav privaatsuspoliitika lehekülje lahenduse projekteerimise ja rakendamise eest, mis vastab kõige paremini teie ettevõtte juriidilistele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="dd564-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="dd564-116">Alustamiseks valige loomise tööriistade abil sait, mille jaoks soovite luua privaatsuspoliitika lehekülje.</span><span class="sxs-lookup"><span data-stu-id="dd564-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="dd564-117">Loo mall</span><span class="sxs-lookup"><span data-stu-id="dd564-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="dd564-118">Kui mall, mida saab kasutada privaatsuspoliitika jaoks, on juba loodud, minge edasi, et [luua privaatsuspoliitika lehekülg.](#build-a-privacy-policy-page)</span><span class="sxs-lookup"><span data-stu-id="dd564-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="dd564-119">Malli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="dd564-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="dd564-120">Avage **Mallid** ja valige lehe malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd564-120">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="dd564-121">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd564-121">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="dd564-122">Mallis lisage nõutavad moodulid nõutavatele lehekülje pesadele.</span><span class="sxs-lookup"><span data-stu-id="dd564-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="dd564-123">Juhiste saamiseks liikuge üle punase hüüumärgi.</span><span class="sxs-lookup"><span data-stu-id="dd564-123">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="dd564-124">(Näiteks võib **HTML-i pea** pesa nõuda **vaikimisi välise skripti** moodulit.)</span><span class="sxs-lookup"><span data-stu-id="dd564-124">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="dd564-125">Lisage **kehateksti** pesasse **vaikelehe** moodul.</span><span class="sxs-lookup"><span data-stu-id="dd564-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="dd564-126">Lisage **vaikelehe** mooduli **peamisesse** pessa **sisurikka ploki** moodul.</span><span class="sxs-lookup"><span data-stu-id="dd564-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="dd564-127">**Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="dd564-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="dd564-128">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="dd564-128">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="dd564-129">Privaatsuspoliitika lehe loomine</span><span class="sxs-lookup"><span data-stu-id="dd564-129">Build a privacy policy page</span></span>

<span data-ttu-id="dd564-130">Privaatsusoliitika lehe loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="dd564-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="dd564-131">Avage **Lehed** ja seejärel uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd564-131">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="dd564-132">Valige privaatsuspoliitika lehe mall dialoogiboksis **Vali mall**.</span><span class="sxs-lookup"><span data-stu-id="dd564-132">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="dd564-133">Sisestage lehe nimi ja lehe URL, seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd564-133">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="dd564-134">**Peamisesse** lehe pessa lisage **sisurikka ploki** moodul.</span><span class="sxs-lookup"><span data-stu-id="dd564-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="dd564-135">**Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="dd564-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="dd564-136">**Sisurikka ploki** mooduli atribuutide paanil valige **lisa andmeallikas** ja seejärel valige **rikkaliku teksti sisu.**</span><span class="sxs-lookup"><span data-stu-id="dd564-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="dd564-137">RTF-redaktoris sisestage privaatsuspoliitika lehele sisu.</span><span class="sxs-lookup"><span data-stu-id="dd564-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="dd564-138">Laiendage RTF-redaktorit täisekraani režiimile, nagu vajate.</span><span class="sxs-lookup"><span data-stu-id="dd564-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="dd564-139">Kui olete sisu sisestamise lõpetanud, valige veebibrauseris lehe eelvaate kuvamiseks **eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="dd564-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="dd564-140">Täitke kõik järelejäänud täiendused leheküljele ja mooduli atribuutidele.</span><span class="sxs-lookup"><span data-stu-id="dd564-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="dd564-141">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="dd564-141">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="dd564-142">Privaatsuspoliitika lehe URL-i avaldamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="dd564-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="dd564-143">Avage **URL-** id ja valige privaatsuspoliitika lehele URL.</span><span class="sxs-lookup"><span data-stu-id="dd564-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="dd564-144">Valitud URL-i avaldamiseks valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="dd564-144">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="dd564-145">Lingi loomine privaatsuspoliitika lehele jaluses</span><span class="sxs-lookup"><span data-stu-id="dd564-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="dd564-146">Saate lisada lingi privaatsuspoliitika lehele fragmenti.</span><span class="sxs-lookup"><span data-stu-id="dd564-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="dd564-147">Sel viisil saate linki jagada ja värskendada selle mitme saidi lehekülgede vahel, viitades fragmendile.</span><span class="sxs-lookup"><span data-stu-id="dd564-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="dd564-148">See näide näitab, kuidas lisada privaatsuspoliitika lehele jaluse fragmendile link.</span><span class="sxs-lookup"><span data-stu-id="dd564-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="dd564-149">Jaluse fragmendile lingi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="dd564-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="dd564-150">Avage **Fragmendid** ja valige seejärel lehe fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="dd564-150">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="dd564-151">Valige dialoogiboksis **Uus fragment** moodul **Jalus**.</span><span class="sxs-lookup"><span data-stu-id="dd564-151">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="dd564-152">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd564-152">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="dd564-153">**Jaluse kategooria** pesas lisage **jaluse üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="dd564-153">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="dd564-154">Parempoolsel atribuutide paanil valige suvand **Lingi tekst**.</span><span class="sxs-lookup"><span data-stu-id="dd564-154">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="dd564-155">Dialoogiaknas **lingi tekst** sisestage lingi tekst ja lingi eesmärk privaatsuspoliitika lehele ja seejärel klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd564-155">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="dd564-156">Privaatsuspoliitika lehe URL-i saamiseks minge lehele **Leheküljed**, minge lehele privaatsuspoliitika ja kopeerige URL atribuutide paanilt.</span><span class="sxs-lookup"><span data-stu-id="dd564-156">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="dd564-157">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="dd564-157">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="dd564-158">Vaadake fragment üle ja kontrollige linki privaatsuse poliitika lehele.</span><span class="sxs-lookup"><span data-stu-id="dd564-158">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="dd564-159">Nüüd saab fragmenti viidata teiste saidi lehtede mallis.</span><span class="sxs-lookup"><span data-stu-id="dd564-159">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="dd564-160">Kui seda fragmenti viidatakse malli **jaluse** moodulis, kuvatakse lingi viide kõigil lehekülgedel, mis on selle malli abil ehitatud.</span><span class="sxs-lookup"><span data-stu-id="dd564-160">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd564-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="dd564-161">Additional resources</span></span>

[<span data-ttu-id="dd564-162">Vastavuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="dd564-162">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="dd564-163">Hõlbustusfunktsioonid ja -võimalused</span><span class="sxs-lookup"><span data-stu-id="dd564-163">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="dd564-164">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="dd564-164">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="dd564-165">Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine</span><span class="sxs-lookup"><span data-stu-id="dd564-165">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)
