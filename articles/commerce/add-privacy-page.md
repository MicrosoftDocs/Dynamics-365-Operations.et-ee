---
title: Privaatsuspoliitika lehe lisamine
description: Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.
author: v-chgri
manager: annbe
ms.date: 01/08/2020
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
ms.openlocfilehash: fd39ff5f8c5d97f2d524043b65627dc7e87fcf64
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2946001"
---
# <a name="add-a-privacy-policy-page"></a><span data-ttu-id="3b45a-103">Privaatsuspoliitika lehe lisamine</span><span class="sxs-lookup"><span data-stu-id="3b45a-103">Add a privacy policy page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3b45a-104">Selles teemas kirjeldatakse, kuidas lisada privaatsuspoliitika rakenduses Microsoft Dynamics 365 Commerce oma saidile.</span><span class="sxs-lookup"><span data-stu-id="3b45a-104">This topic describes how to add a privacy policy page to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3b45a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3b45a-105">Overview</span></span>

<span data-ttu-id="3b45a-106">Privaatsuse vastavus hõlmab organisatsioonilisi meetmeid, mis teavitavad saidi kasutajaid nende andmete kogumisest ja käitlemisest.</span><span class="sxs-lookup"><span data-stu-id="3b45a-106">Privacy compliance includes organizational measures that inform site users about how their data is collected and handled.</span></span> <span data-ttu-id="3b45a-107">Kasutajad saavad seejärel otsustada, kuidas nad soovivad oma isiklikke andmeid töödelda ja võtta asjakohaseid meetmeid.</span><span class="sxs-lookup"><span data-stu-id="3b45a-107">Users can then decide how they want their personal data to be handled and can take appropriate action.</span></span>

## <a name="review-the-microsoft-privacy-statement-in-dynamics-365-commerce"></a><span data-ttu-id="3b45a-108">Microsofti privaatsusavalduse ülevaatamine Dynamics 365 Commerce'is</span><span class="sxs-lookup"><span data-stu-id="3b45a-108">Review the Microsoft privacy statement in Dynamics 365 Commerce</span></span>

<span data-ttu-id="3b45a-109">Microsofti privaatsusavalduse ülevaatamiseks, kui olete sisse logitud Dynamics 365 Commerce, valige ülemises parempoolses nurgas nupp **spikker** (**?**) ja seejärel valige **Privaatsus ja küpsised.**</span><span class="sxs-lookup"><span data-stu-id="3b45a-109">To review the Microsoft privacy statement while you're signed in to the Dynamics 365 Commerce authoring tools, select the **Help** button (**?**) in the upper-right corner, and then select **Privacy and cookies**.</span></span> <span data-ttu-id="3b45a-110">Avatakse uus vahekaart, millel on link [Microsofti privaatsusavaldusele.](https://privacy.microsoft.com/privacystatement)</span><span class="sxs-lookup"><span data-stu-id="3b45a-110">A new tab is opened that has a link to the [Microsoft privacy statement](https://privacy.microsoft.com/privacystatement).</span></span>

## <a name="build-a-privacy-policy-page-for-your-site"></a><span data-ttu-id="3b45a-111">Oma saidi privaatsuspoliitika loomine</span><span class="sxs-lookup"><span data-stu-id="3b45a-111">Build a privacy policy page for your site</span></span>

<span data-ttu-id="3b45a-112">Rakenduses Dynamics 365 Commerceon mitu võimalust, kuidas anda kasutajatele saidile juurdepääs teie privaatsuspoliitikale.</span><span class="sxs-lookup"><span data-stu-id="3b45a-112">In Dynamics 365 Commerce, there are several ways to give users of your site access to your privacy policy.</span></span> <span data-ttu-id="3b45a-113">Selles jaotises kirjeldatakse, kuidas luua privaatsuspoliitika lehte ja seejärel viidata leheküljele, kasutades jaluse fragmenti.</span><span class="sxs-lookup"><span data-stu-id="3b45a-113">This section shows how to build a privacy policy page and then reference the page by using a footer fragment.</span></span>

<span data-ttu-id="3b45a-114">Järgnev juhend on näide, mis näitab, kuidas luua Commerce saidi üldise privaatsuspoliitika lehte.</span><span class="sxs-lookup"><span data-stu-id="3b45a-114">The guidance that follows is an example that shows how to build a generic privacy policy page for a Commerce site.</span></span> <span data-ttu-id="3b45a-115">Olete vastutav privaatsuspoliitika lehekülje lahenduse projekteerimise ja rakendamise eest, mis vastab kõige paremini teie ettevõtte juriidilistele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="3b45a-115">You're responsible for designing and implementing a privacy policy page solution that best meets your company's legal requirements.</span></span>

<span data-ttu-id="3b45a-116">Alustamiseks valige loomise tööriistade abil sait, mille jaoks soovite luua privaatsuspoliitika lehekülje.</span><span class="sxs-lookup"><span data-stu-id="3b45a-116">To start, in the authoring tools, go to the site that you want to build a privacy policy page for.</span></span>

### <a name="create-a-template"></a><span data-ttu-id="3b45a-117">Loo mall</span><span class="sxs-lookup"><span data-stu-id="3b45a-117">Create a template</span></span>

> [!NOTE]
> <span data-ttu-id="3b45a-118">Kui mall, mida saab kasutada privaatsuspoliitika jaoks, on juba loodud, minge edasi, et [luua privaatsuspoliitika lehekülg.](#build-a-privacy-policy-page)</span><span class="sxs-lookup"><span data-stu-id="3b45a-118">If a template that can be used for the privacy policy page has already been created, skip ahead to the [Build a privacy policy page](#build-a-privacy-policy-page) section.</span></span>

<span data-ttu-id="3b45a-119">Malli loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3b45a-119">To create a template, follow these steps.</span></span>

1. <span data-ttu-id="3b45a-120">Avage **Mallid \> Uus mall**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-120">Go to **Templates \> New Template**.</span></span>
1. <span data-ttu-id="3b45a-121">Sisestage malli nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-121">Enter the template name, and then select **OK**.</span></span>
1. <span data-ttu-id="3b45a-122">Mallis lisage nõutavad moodulid nõutavatele lehekülje pesadele.</span><span class="sxs-lookup"><span data-stu-id="3b45a-122">In the template, add any required modules to the required page slots.</span></span> <span data-ttu-id="3b45a-123">Juhiste saamiseks liikuge üle punase hüüumärgi.</span><span class="sxs-lookup"><span data-stu-id="3b45a-123">For guidance, hover over the red exclamation marks.</span></span>

    <span data-ttu-id="3b45a-124">Näiteks võib **HTML-i pea** pesa nõuda **vaikimisi välise skripti** moodulit.</span><span class="sxs-lookup"><span data-stu-id="3b45a-124">For example, the **HTML Head** slot might require a **Default External Script** module.</span></span>

1. <span data-ttu-id="3b45a-125">Lisage **kehateksti** pesasse **vaikelehe** moodul.</span><span class="sxs-lookup"><span data-stu-id="3b45a-125">In the **Body** slot, add a **Default Page** module.</span></span>
1. <span data-ttu-id="3b45a-126">Lisage **vaikelehe** mooduli **peamisesse** pessa **sisurikka ploki** moodul.</span><span class="sxs-lookup"><span data-stu-id="3b45a-126">In the **Default Page** module, in the **Main** slot, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="3b45a-127">**Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="3b45a-127">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="3b45a-128">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="3b45a-128">Check the template in, and publish it.</span></span>

### <a name="build-a-privacy-policy-page"></a><span data-ttu-id="3b45a-129">Privaatsuspoliitika lehe loomine</span><span class="sxs-lookup"><span data-stu-id="3b45a-129">Build a privacy policy page</span></span>

<span data-ttu-id="3b45a-130">Privaatsusoliitika lehe loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3b45a-130">To build a privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="3b45a-131">Avage **Lehed \> Uus leht**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-131">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="3b45a-132">Valige privaatsuspoliitika lehele mall.</span><span class="sxs-lookup"><span data-stu-id="3b45a-132">Select the template for the privacy policy page.</span></span>
1. <span data-ttu-id="3b45a-133">Sisestage lehe nimi ja URL, seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-133">Enter a page name and URL, and then select **OK**.</span></span> 
1. <span data-ttu-id="3b45a-134">**Peamisesse** lehe pessa lisage **sisurikka ploki** moodul.</span><span class="sxs-lookup"><span data-stu-id="3b45a-134">In the **Main** slot of the page, add a **Content Rich Block** module.</span></span>
1. <span data-ttu-id="3b45a-135">**Sisurikka ploki** moodulis lisage **sisurikka ploki üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="3b45a-135">In the **Content Rich Block** module, add a **Content rich block item** module.</span></span>
1. <span data-ttu-id="3b45a-136">**Sisurikka ploki** mooduli atribuutide paanil valige **lisa andmeallikas** ja seejärel valige **rikkaliku teksti sisu.**</span><span class="sxs-lookup"><span data-stu-id="3b45a-136">In the properties pane for the **Content Rich Block** module, select **Add Data Source**, and then select **Rich Text Content**.</span></span>
1. <span data-ttu-id="3b45a-137">RTF-redaktoris sisestage privaatsuspoliitika lehele sisu.</span><span class="sxs-lookup"><span data-stu-id="3b45a-137">In the rich text editor, enter the content for the privacy policy page.</span></span> <span data-ttu-id="3b45a-138">Laiendage RTF-redaktorit täisekraani režiimile, nagu vajate.</span><span class="sxs-lookup"><span data-stu-id="3b45a-138">Expand the rich text editor to full-screen mode as you require.</span></span>
1. <span data-ttu-id="3b45a-139">Kui olete sisu sisestamise lõpetanud, valige veebibrauseris lehe eelvaate kuvamiseks **eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-139">When you've finished entering content, select **Preview** to preview the page in the web browser.</span></span>
1. <span data-ttu-id="3b45a-140">Täitke kõik järelejäänud täiendused leheküljele ja mooduli atribuutidele.</span><span class="sxs-lookup"><span data-stu-id="3b45a-140">Complete any remaining additions to the page and module properties.</span></span>
1. <span data-ttu-id="3b45a-141">Registreerige privaatsuspoliitika leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="3b45a-141">Check the privacy policy page in, and publish it.</span></span>

<span data-ttu-id="3b45a-142">Privaatsuspoliitika lehe URL-i avaldamiseks järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="3b45a-142">To publish the URL for the privacy policy page, follow these steps.</span></span>

1. <span data-ttu-id="3b45a-143">Avage **URL-** id ja valige privaatsuspoliitika lehele URL.</span><span class="sxs-lookup"><span data-stu-id="3b45a-143">Go to **URLs**, and select the URL for the privacy policy page.</span></span>
1. <span data-ttu-id="3b45a-144">Avaldage valitud URL.</span><span class="sxs-lookup"><span data-stu-id="3b45a-144">Publish the selected URL.</span></span>

### <a name="create-a-link-to-the-privacy-policy-page-in-a-footer"></a><span data-ttu-id="3b45a-145">Lingi loomine privaatsuspoliitika lehele jaluses</span><span class="sxs-lookup"><span data-stu-id="3b45a-145">Create a link to the privacy policy page in a footer</span></span>

<span data-ttu-id="3b45a-146">Saate lisada lingi privaatsuspoliitika lehele fragmenti.</span><span class="sxs-lookup"><span data-stu-id="3b45a-146">You can add a link to the privacy policy page to a fragment.</span></span> <span data-ttu-id="3b45a-147">Sel viisil saate linki jagada ja värskendada selle mitme saidi lehekülgede vahel, viitades fragmendile.</span><span class="sxs-lookup"><span data-stu-id="3b45a-147">In this way, you can share the link and update it across multiple site pages by referencing the fragment.</span></span> <span data-ttu-id="3b45a-148">See näide näitab, kuidas lisada privaatsuspoliitika lehele jaluse fragmendile link.</span><span class="sxs-lookup"><span data-stu-id="3b45a-148">This example shows how to add a link to the privacy policy page to a footer fragment.</span></span>

<span data-ttu-id="3b45a-149">Jaluse fragmendile lingi lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="3b45a-149">To add a link to a footer fragment, follow these steps.</span></span>

1. <span data-ttu-id="3b45a-150">Avage **Lehe fragmendid \> Uus lehe fragment**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-150">Go to **Page Fragments \> New Page Fragment**.</span></span>
1. <span data-ttu-id="3b45a-151">Valige **jaluse** moodul ja sisestage nimi väljale **lehekülje fragmendi nimi**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-151">Select the **Footer** module, and then enter a name in the **Page Fragment Name** field.</span></span>
1. <span data-ttu-id="3b45a-152">**Jaluse kategooria** pesas lisage **jaluse üksuse** moodul.</span><span class="sxs-lookup"><span data-stu-id="3b45a-152">In the **Footer category** slot, add a **Footer item** module.</span></span>
1. <span data-ttu-id="3b45a-153">Parempoolsel atribuutide paanil valige suvand **Lingi tekst**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-153">In the properties pane on the right, select **Link text**.</span></span>
1. <span data-ttu-id="3b45a-154">Dialoogiaknas **lingi tekst** sisestage lingi tekst ja lingi eesmärk privaatsuspoliitika lehele ja seejärel klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="3b45a-154">In the **Link text** dialog box, enter the link text and link target of the privacy policy page, and then click **OK**.</span></span>

    <span data-ttu-id="3b45a-155">Privaatsuspoliitika lehe URL-i saamiseks minge lehele **Leheküljed**, minge lehele privaatsuspoliitika ja kopeerige URL atribuutide paanilt.</span><span class="sxs-lookup"><span data-stu-id="3b45a-155">To get the URL of the privacy policy page, go to **Pages**, go to the privacy policy page, and copy the URL from the properties pane.</span></span>

1. <span data-ttu-id="3b45a-156">Salvestage lehe fragment, registreerige see ja avaldage.</span><span class="sxs-lookup"><span data-stu-id="3b45a-156">Save the fragment, check it in, and publish it.</span></span>
1. <span data-ttu-id="3b45a-157">Vaadake fragment üle ja kontrollige linki privaatsuse poliitika lehele.</span><span class="sxs-lookup"><span data-stu-id="3b45a-157">Preview the fragment, and test the link to the privacy policy page.</span></span>

<span data-ttu-id="3b45a-158">Nüüd saab fragmenti viidata teiste saidi lehtede mallis.</span><span class="sxs-lookup"><span data-stu-id="3b45a-158">The fragment can now be referenced in the template for other site pages.</span></span> <span data-ttu-id="3b45a-159">Kui seda fragmenti viidatakse malli **jaluse** moodulis, kuvatakse lingi viide kõigil lehekülgedel, mis on selle malli abil ehitatud.</span><span class="sxs-lookup"><span data-stu-id="3b45a-159">When this fragment is referenced in the **Footer** module of a template, the link reference will appear on any pages that are built by using that template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3b45a-160">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3b45a-160">Additional resources</span></span>

[<span data-ttu-id="3b45a-161">Vastavuse ülevaade</span><span class="sxs-lookup"><span data-stu-id="3b45a-161">Compliance overview</span></span>](compliance-overview.md)

[<span data-ttu-id="3b45a-162">Hõlbustusfunktsioonid ja -võimalused</span><span class="sxs-lookup"><span data-stu-id="3b45a-162">Accessibility features and capabilities</span></span>](accessibility.md)

[<span data-ttu-id="3b45a-163">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="3b45a-163">Cookie compliance</span></span>](cookie-compliance.md)
