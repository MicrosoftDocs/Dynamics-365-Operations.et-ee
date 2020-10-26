---
title: Olemasoleva saidilehe muutmine
description: Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce olemasolevat saidi lehte muuta.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8ca23dcf568cb0df6934f0d6201e4aafba5f9ba1
ms.sourcegitcommit: f16db76c1c235dfa445b50614bcee9219782d6dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961630"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="c8b20-103">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="c8b20-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c8b20-104">Selles teemas kirjeldatakse, kuidas rakenduses Microsoft Dynamics 365 Commerce olemasolevat saidi lehte muuta.</span><span class="sxs-lookup"><span data-stu-id="c8b20-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c8b20-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c8b20-105">Overview</span></span>

<span data-ttu-id="c8b20-106">Kui peate lehte muutma, on esimene etapp selle avamine lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="c8b20-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="c8b20-107">Avage teie lehte sisaldav sait ja seejärel leidke lehtede loendist soovitud leht.</span><span class="sxs-lookup"><span data-stu-id="c8b20-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="c8b20-108">Kui te lehte ei leia, saate kasutada autorluse tööriista rikkalikku sisuga otsingufunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="c8b20-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="c8b20-109">Sisestage kas lehe täpne nimi või sisestage selle esimesed paar tähte ja seejärel tärn (\*).</span><span class="sxs-lookup"><span data-stu-id="c8b20-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="c8b20-110">Kuvatakse filtreeritud lehtede loend.</span><span class="sxs-lookup"><span data-stu-id="c8b20-110">A filtered list of pages appears.</span></span> <span data-ttu-id="c8b20-111">Seda loendit saate kasutada soovitud lehe leidmiseks.</span><span class="sxs-lookup"><span data-stu-id="c8b20-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="c8b20-112">Pärast õige lehe leidmist valige lehe nimi, et avada leht lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="c8b20-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="c8b20-113">Kui leht on leheinspektoris nähtav, saate valida **Redigeeri** ja lehte enne selle leheredaktoris avamist vaadata.</span><span class="sxs-lookup"><span data-stu-id="c8b20-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="c8b20-114">Sel viisil saate registreerida välja mitu lehte korraga.</span><span class="sxs-lookup"><span data-stu-id="c8b20-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="c8b20-115">Kui leht on lehe redaktoris avatud, peate veenduma, et see oleks teile välja registreeritud.</span><span class="sxs-lookup"><span data-stu-id="c8b20-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="c8b20-116">Autorluse tööriista käsuriba on dünaamiline, kontekstitundlik ja oleku tundlik.</span><span class="sxs-lookup"><span data-stu-id="c8b20-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="c8b20-117">Seetõttu kuvab see ainult toimingud, mida saate lehel praegu teha.</span><span class="sxs-lookup"><span data-stu-id="c8b20-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="c8b20-118">Näiteks kui leht ei ole teile välja registreeritud, siis nupud **Salvesta** ja **Lõpeta redigeerimine** käsuribal ei ilmu.</span><span class="sxs-lookup"><span data-stu-id="c8b20-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="c8b20-119">Akna paremal küljel on näidatud ka lehe olek.</span><span class="sxs-lookup"><span data-stu-id="c8b20-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="c8b20-120">Kui leht ei ole veel teile välja registreeritud, valige käsuribal käsk **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="c8b20-121">Käsuriba muutub, et peegeldada lehe uut olekut.</span><span class="sxs-lookup"><span data-stu-id="c8b20-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="c8b20-122">Samuti saate teatise, mis ütleb, et leht registreeriti teile välja.</span><span class="sxs-lookup"><span data-stu-id="c8b20-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="c8b20-123">Järgmine etapp on teha tegelikud muudatused.</span><span class="sxs-lookup"><span data-stu-id="c8b20-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="c8b20-124">Sageli kasutate vasakul lehe liigendpuud, et leida ja valida moodul, mida soovite muuta, ja seejärel teete paremal atribuutide paanil muudatused.</span><span class="sxs-lookup"><span data-stu-id="c8b20-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="c8b20-125">Samas võib teie muudatus hõlmata mudelite või fragmentide lisamist või eemaldamist.</span><span class="sxs-lookup"><span data-stu-id="c8b20-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="c8b20-126">Fragmendi või mooduli lisamiseks kasutage lehekülje liigendpuud, et leida pesa, kuhu soovite mooduli või fragmendi lisada, ja valige seejärel selle pesa kolmikpunkti nupp (**...**).</span><span class="sxs-lookup"><span data-stu-id="c8b20-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="c8b20-127">Kuvatakse menüü, mis sisaldab mooduli või fragmenti lisamise käske.</span><span class="sxs-lookup"><span data-stu-id="c8b20-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="c8b20-128">Mooduli või fragmenti eemaldamiseks leidke ja valige see lehekülje liigendpuus, valige kolmikpunkti nupp ning seejärel valige mooduli või fragmenti kustutamiseks käsk.</span><span class="sxs-lookup"><span data-stu-id="c8b20-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="c8b20-129">Samuti saate vaadata ja redigeerida iga mooduli atribuute, mis on nähtavad visuaalse leheehitaja eelvaates, valides selle otse.</span><span class="sxs-lookup"><span data-stu-id="c8b20-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="c8b20-130">Kui olete muudatuste tegemise ja nende mõju eelvaate vaatamise lõpetanud, tuleb teil leht registreerida, valides käsiribal käsu **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="c8b20-131">Muudatuste koheseks avaldamiseks valige käsuribal käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="c8b20-132">Avaldatakse uusim muudetud lehe registreeritud versioon ja see muutub kättesaadavaks välistele kasutajatele, kes teie saiti vaatavad.</span><span class="sxs-lookup"><span data-stu-id="c8b20-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="c8b20-133">Näide: avalehel video muutmine</span><span class="sxs-lookup"><span data-stu-id="c8b20-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="c8b20-134">Järgmine näide selgitab, kuidas muuta avalehte, muutes videopleieri moodulis ilmuva video.</span><span class="sxs-lookup"><span data-stu-id="c8b20-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="c8b20-135">Jaotises **Saidid** valige suvand **Fabrikam** (või oma saidi nimi).</span><span class="sxs-lookup"><span data-stu-id="c8b20-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="c8b20-136">Valige navigeerimispaanilt vasakult suvand **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="c8b20-137">Leidke ja valige avaleht, et avada see lehe redaktoris.</span><span class="sxs-lookup"><span data-stu-id="c8b20-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="c8b20-138">Klõpsake käsuribal käsku **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="c8b20-139">Valige lehe liigenduses pesa **Peamine**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="c8b20-140">Laiendage pesas **Peamine** kõiki sujuvaid konteinei mooduleid.</span><span class="sxs-lookup"><span data-stu-id="c8b20-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="c8b20-141">Leidke ja valige videopleieri moodul.</span><span class="sxs-lookup"><span data-stu-id="c8b20-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="c8b20-142">Valige paremalt atribuutide paanil **video** atribuut.</span><span class="sxs-lookup"><span data-stu-id="c8b20-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="c8b20-143">Kuvatakse varade valija.</span><span class="sxs-lookup"><span data-stu-id="c8b20-143">The asset picker appears.</span></span>
1. <span data-ttu-id="c8b20-144">Valige varade valijas saadaolev videovara või valige uue videovara üleslaadimiseks suvand **Uue vara üleslaadimine**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="c8b20-145">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-145">Select **OK**.</span></span>
1. <span data-ttu-id="c8b20-146">Valige nupp **Salvesta** ja seejärel suvand **Lõpeta redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c8b20-147">Sisestage väljale **Kommentaarid** suvand **Muutsin video** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="c8b20-148">Uuendatud lehe eelvaate kuvamiseks valige suvand **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="c8b20-149">Kui olete lõpetanud, sulgege eelvaate vahekaart, et naasta autorluse tööriista.</span><span class="sxs-lookup"><span data-stu-id="c8b20-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="c8b20-150">Valige **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c8b20-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c8b20-151">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c8b20-151">Additional resources</span></span>

[<span data-ttu-id="c8b20-152">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="c8b20-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="c8b20-153">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="c8b20-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c8b20-154">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="c8b20-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="c8b20-155">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="c8b20-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c8b20-156">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="c8b20-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c8b20-157">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="c8b20-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="c8b20-158">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="c8b20-158">Verify page content accessibility</span></span>](verify-accessibility.md)
