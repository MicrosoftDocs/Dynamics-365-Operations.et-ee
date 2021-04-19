---
title: Privaatsuspoliitika lehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: v-chgri
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12cd0358279684ce1d3050348c37209ba3d29140
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797523"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="a786d-103">Privaatsuspoliitika lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="a786d-103">Add a privacy policy page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a786d-104">Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.</span><span class="sxs-lookup"><span data-stu-id="a786d-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a786d-105">Privaatsuse vastavus hõlmab organisatsioonilisi meetmeid, mis teavitavad saidi kasutajaid nende andmete kogumisest ja käitlemisest.</span><span class="sxs-lookup"><span data-stu-id="a786d-105">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="a786d-106">Kasutajad saavad seejärel otsustada, kuidas nad soovivad oma isiklikke andmeid töödelda ja võtta asjakohaseid meetmeid.</span><span class="sxs-lookup"><span data-stu-id="a786d-106">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="a786d-107">Microsofti privaatsusavalduse ülevaatamine Dynamics 365 Commerce'is</span><span class="sxs-lookup"><span data-stu-id="a786d-107">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="a786d-108">Microsofti privaatsusavalduse ülevaatamiseks, kui olete sisse logitud Dynamics 365 Commerce, valige ülemises parempoolses nurgas nupp **spikker** (**?**) ja seejärel valige **Privaatsus ja küpsised.**</span><span class="sxs-lookup"><span data-stu-id="a786d-108">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="a786d-109">Avatakse uus vahekaart, millel on link [Microsofti privaatsusavaldusele.](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="a786d-109">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="a786d-110">Oma saidi privaatsuspoliitika loomine</span><span class="sxs-lookup"><span data-stu-id="a786d-110">Build a privacy policy page for your site</span></span>

<span data-ttu-id="a786d-111">Rakenduses Dynamics 365 Commerceon mitu võimalust, kuidas anda kasutajatele saidile juurdepääs teie privaatsuspoliitikale.</span><span class="sxs-lookup"><span data-stu-id="a786d-111">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="a786d-112">Selles jaotises kirjeldatakse, kuidas luua privaatsuspoliitika lehte ja seejärel viidata leheküljele, kasutades jaluse fragmenti.</span><span class="sxs-lookup"><span data-stu-id="a786d-112">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="a786d-113">Järgnev juhend on näide, mis näitab, kuidas luua Commerce saidi üldise privaatsuspoliitika lehte.</span><span class="sxs-lookup"><span data-stu-id="a786d-113">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="a786d-114">Olete vastutav privaatsuspoliitika lehekülje lahenduse projekteerimise ja rakendamise eest, mis vastab kõige paremini teie ettevõtte juriidilistele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="a786d-114">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="a786d-115">Alustamiseks valige loomise tööriistade abil sait, mille jaoks soovite luua privaatsuspoliitika lehekülje.</span><span class="sxs-lookup"><span data-stu-id="a786d-115">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="a786d-116">Loo mall</span><span class="sxs-lookup"><span data-stu-id="a786d-116">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="a786d-117">Kui mall, mida saab kasutada privaatsuspoliitika jaoks, on juba loodud, minge edasi, et [luua privaatsuspoliitika lehekülg.](#build-a-privacy-policy-page)</span><span class="sxs-lookup"><span data-stu-id="a786d-117">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="a786d-118">Malli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a786d-118">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="a786d-119">Avage **Mallid** ja valige lehe malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a786d-119">Go to **Templates**, and then select **New** to create a page template.</span></span>
1. <span data-ttu-id="a786d-120">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="a786d-120">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="a786d-121">Mallis lisage nõutavad moodulid nõutavatele lehekülje pesadele.</span><span class="sxs-lookup"><span data-stu-id="a786d-121">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="a786d-122">Juhiste saamiseks liikuge üle punase hüüumärgi.</span><span class="sxs-lookup"><span data-stu-id="a786d-122">For guidance, hover over the red exclamation marks.</span></span> <span data-ttu-id="a786d-123">(Näiteks võib **HTML-i pea** pesa nõuda **vaikimisi välise skripti** moodulit.)</span><span class="sxs-lookup"><span data-stu-id="a786d-123">(For example, the **HTML Head** slot might require a **Default External Script** module.)</span></span>
1. <span data-ttu-id="a786d-124">Lisage **kehateksti** pesasse **vaikelehe** moodul.</span><span class="sxs-lookup"><span data-stu-id="a786d-124">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="a786d-125">Lisage **vaikelehe** mooduli **peamisesse** pessa **sisurikka ploki** moodul.</span><span class="sxs-lookup"><span data-stu-id="a786d-125">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="a786d-126">**Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="a786d-126">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="a786d-127">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a786d-127">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="a786d-128">Privaatsuspoliitika lehe loomine</span><span class="sxs-lookup"><span data-stu-id="a786d-128">Build a privacy policy page</span></span>

<span data-ttu-id="a786d-129">Privaatsusoliitika lehe loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a786d-129">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="a786d-130">Avage **Lehed** ja seejärel uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a786d-130">Go to **Pages**, and then select **New** to create a page.</span></span>
1. <span data-ttu-id="a786d-131">Valige privaatsuspoliitika lehe mall dialoogiboksis **Vali mall**.</span><span class="sxs-lookup"><span data-stu-id="a786d-131">In the **Choose a template** dialog box, select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="a786d-132">Sisestage lehe nimi ja lehe URL, seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a786d-132">Enter a page name and page URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="a786d-133">**Peamisesse** lehe pessa lisage **sisurikka ploki** moodul.</span><span class="sxs-lookup"><span data-stu-id="a786d-133">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="a786d-134">**Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="a786d-134">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="a786d-135">**Sisurikka ploki** mooduli atribuutide paanil valige **lisa andmeallikas** ja seejärel valige **rikkaliku teksti sisu.**</span><span class="sxs-lookup"><span data-stu-id="a786d-135">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="a786d-136">RTF-redaktoris sisestage privaatsuspoliitika lehele sisu.</span><span class="sxs-lookup"><span data-stu-id="a786d-136">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="a786d-137">Laiendage RTF-redaktorit täisekraani režiimile, nagu vajate.</span><span class="sxs-lookup"><span data-stu-id="a786d-137">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="a786d-138">Kui olete sisu sisestamise lõpetanud, valige veebibrauseris lehe eelvaate kuvamiseks **eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="a786d-138">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="a786d-139">Täitke kõik järelejäänud täiendused leheküljele ja mooduli atribuutidele.</span><span class="sxs-lookup"><span data-stu-id="a786d-139">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="a786d-140">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a786d-140">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="a786d-141">Privaatsuspoliitika lehe URL-i avaldamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="a786d-141">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="a786d-142">Avage **URL-** id ja valige privaatsuspoliitika lehele URL.</span><span class="sxs-lookup"><span data-stu-id="a786d-142">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="a786d-143">Valitud URL-i avaldamiseks valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a786d-143">Select **Publish** to publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="a786d-144">Lingi loomine privaatsuspoliitika lehele jaluses</span><span class="sxs-lookup"><span data-stu-id="a786d-144">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="a786d-145">Saate lisada lingi privaatsuspoliitika lehele fragmenti.</span><span class="sxs-lookup"><span data-stu-id="a786d-145">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="a786d-146">Sel viisil saate linki jagada ja värskendada selle mitme saidi lehekülgede vahel, viitades fragmendile.</span><span class="sxs-lookup"><span data-stu-id="a786d-146">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="a786d-147">See näide näitab, kuidas lisada privaatsuspoliitika lehele jaluse fragmendile link.</span><span class="sxs-lookup"><span data-stu-id="a786d-147">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="a786d-148">Jaluse fragmendile lingi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="a786d-148">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="a786d-149">Avage **Fragmendid** ja valige seejärel lehe fragmendi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a786d-149">Go to **Fragments**, and then select **New** to create a page fragment.</span></span>
1. <span data-ttu-id="a786d-150">Valige dialoogiboksis **Uus fragment** moodul **Jalus**.</span><span class="sxs-lookup"><span data-stu-id="a786d-150">In the **New fragment** dialog box, select the **Footer** module.</span></span>
1. <span data-ttu-id="a786d-151">Sisestage jaotises **Fragmendi nimi** fragmendi nimi ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="a786d-151">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="a786d-152">**Jaluse kategooria** pesas lisage **jaluse üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="a786d-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="a786d-153">Parempoolsel atribuutide paanil valige suvand **Lingi tekst**.</span><span class="sxs-lookup"><span data-stu-id="a786d-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="a786d-154">Dialoogiaknas **lingi tekst** sisestage lingi tekst ja lingi eesmärk privaatsuspoliitika lehele ja seejärel klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="a786d-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>
1. <span data-ttu-id="a786d-155">Privaatsuspoliitika lehe URL-i saamiseks minge lehele **Leheküljed**, minge lehele privaatsuspoliitika ja kopeerige URL atribuutide paanilt.</span><span class="sxs-lookup"><span data-stu-id="a786d-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>
1. <span data-ttu-id="a786d-156">Valige **Salvesta**, valige fragmendi registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="a786d-156">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="a786d-157">Vaadake fragment üle ja kontrollige linki privaatsuse poliitika lehele.</span><span class="sxs-lookup"><span data-stu-id="a786d-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="a786d-158">Nüüd saab fragmenti viidata teiste saidi lehtede mallis.</span><span class="sxs-lookup"><span data-stu-id="a786d-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="a786d-159">Kui seda fragmenti viidatakse malli **jaluse** moodulis, kuvatakse lingi viide kõigil lehekülgedel, mis on selle malli abil ehitatud.</span><span class="sxs-lookup"><span data-stu-id="a786d-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a786d-160">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="a786d-160">Additional resources</span></span>

[<span data-ttu-id="a786d-161">Vastavuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="a786d-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="a786d-162">Hõlbustusfunktsioonid ja -võimalused</span><span class="sxs-lookup"><span data-stu-id="a786d-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="a786d-163">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="a786d-163">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="a786d-164">Jälgitud sisumuudatustega seostatud kasutaja ID-de asendamine</span><span class="sxs-lookup"><span data-stu-id="a786d-164">Replace user IDs associated with tracked content changes</span></span>](replace-IDs-tracked-changes.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
