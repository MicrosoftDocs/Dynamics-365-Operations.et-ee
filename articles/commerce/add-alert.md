---
title: Reklaambänneri moodul
description: See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025616"
---
# <a name="promo-banner-module"></a><span data-ttu-id="2beb4-103">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="2beb4-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2beb4-104">See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="2beb4-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2beb4-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="2beb4-105">Overview</span></span>

<span data-ttu-id="2beb4-106">Reklaambänneri mooduleid kasutatakse lehel sisemiste teabesõnumite kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="2beb4-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="2beb4-107">Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="2beb4-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="2beb4-108">Reklaambännerid toetavad tekstsõnumit ja linki.</span><span class="sxs-lookup"><span data-stu-id="2beb4-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="2beb4-109">Kui reklaambänneri moodulile on lisatud mitu teadet, muutub see pöörlevaks karussell-bänneriks, mis võimaldab klientidel vaadata läbi kõik sõnumid.</span><span class="sxs-lookup"><span data-stu-id="2beb4-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="2beb4-110">Reklaambänneri moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="2beb4-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="2beb4-111">Reklaambännerite kasutamise näited e-kaubanduses</span><span class="sxs-lookup"><span data-stu-id="2beb4-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="2beb4-112">Reklaambännereid saab kasutada saidi päises, et näidata kogu saiti hõlmavaid kampaaniaid või teateid, nagu näiteks järgmistes näidetes.</span><span class="sxs-lookup"><span data-stu-id="2beb4-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="2beb4-113">„Iga-aastane allahindlus lõppeb 10 päeva pärast”</span><span class="sxs-lookup"><span data-stu-id="2beb4-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="2beb4-114">„Suured allahindlused tagasi kooli kampaania ajal.</span><span class="sxs-lookup"><span data-stu-id="2beb4-114">"Save big with back to school sale.</span></span> <span data-ttu-id="2beb4-115">Ostke kohe.”</span><span class="sxs-lookup"><span data-stu-id="2beb4-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="2beb4-116">Reklaambänneri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="2beb4-116">Promo banner module properties</span></span>

| <span data-ttu-id="2beb4-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="2beb4-117">Property name</span></span>             | <span data-ttu-id="2beb4-118">Value</span><span class="sxs-lookup"><span data-stu-id="2beb4-118">Value</span></span>                              | <span data-ttu-id="2beb4-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2beb4-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="2beb4-120">Bänneri teated</span><span class="sxs-lookup"><span data-stu-id="2beb4-120">Banner messages</span></span>           | <span data-ttu-id="2beb4-121">Tekst ja lingid</span><span class="sxs-lookup"><span data-stu-id="2beb4-121">Text and links</span></span>                     | <span data-ttu-id="2beb4-122">Valik tekste ja linke.</span><span class="sxs-lookup"><span data-stu-id="2beb4-122">An array of text and links.</span></span> |
| <span data-ttu-id="2beb4-123">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="2beb4-123">Autoplay</span></span>                  | <span data-ttu-id="2beb4-124">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="2beb4-124">**True** or **False**</span></span>              | <span data-ttu-id="2beb4-125">Väärtus, mis näitab, kas juhul kui konfigureeritud on mitu sõnumit, keritakse sõnumid automaatselt läbi.</span><span class="sxs-lookup"><span data-stu-id="2beb4-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="2beb4-126">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="2beb4-126">Slide transition interval</span></span> | <span data-ttu-id="2beb4-127">Millisekundite arv (ms)</span><span class="sxs-lookup"><span data-stu-id="2beb4-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="2beb4-128">Sõnumite läbimiseks kasutatav intervall.</span><span class="sxs-lookup"><span data-stu-id="2beb4-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="2beb4-129">Luba sulgemine</span><span class="sxs-lookup"><span data-stu-id="2beb4-129">Allow dismiss</span></span>             | <span data-ttu-id="2beb4-130">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="2beb4-130">**True** or **False**</span></span>              | <span data-ttu-id="2beb4-131">Kui väärtuseks on seatud olekusse **Tõene**, saavad kliendid teatise hüljata.</span><span class="sxs-lookup"><span data-stu-id="2beb4-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="2beb4-132">Näita karusselli keerajat</span><span class="sxs-lookup"><span data-stu-id="2beb4-132">Show carousel flipper</span></span>     | <span data-ttu-id="2beb4-133">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="2beb4-133">**True** or **False**</span></span>              | <span data-ttu-id="2beb4-134">Väärtus, mis näitab, kas karusselli keerajaid tuleb kuvada, et kliendid saaksid käsitsi liikuda mitme bänneri vahel.</span><span class="sxs-lookup"><span data-stu-id="2beb4-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="2beb4-135">Teksti joondus</span><span class="sxs-lookup"><span data-stu-id="2beb4-135">Text alignment</span></span>            | <span data-ttu-id="2beb4-136">**Paremal**, **Vasakul** või **Keskel**</span><span class="sxs-lookup"><span data-stu-id="2beb4-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="2beb4-137">Teksti joondamine reklaambänneri moodulis.</span><span class="sxs-lookup"><span data-stu-id="2beb4-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="2beb4-138">Seos</span><span class="sxs-lookup"><span data-stu-id="2beb4-138">Link</span></span>                      | <span data-ttu-id="2beb4-139">URL</span><span class="sxs-lookup"><span data-stu-id="2beb4-139">A URL</span></span>                              | <span data-ttu-id="2beb4-140">Valikulise lingi URL.</span><span class="sxs-lookup"><span data-stu-id="2beb4-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="2beb4-141">Reklaambänneri mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="2beb4-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="2beb4-142">Lehele reklaambänneri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2beb4-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2beb4-143">Looge lehe mall nimega **Reklaambänneri mall**.</span><span class="sxs-lookup"><span data-stu-id="2beb4-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="2beb4-144">Lisage jaotisse **Lehe liigendus** moodul **Vaikeleht** pesasse **Kehatekst**.</span><span class="sxs-lookup"><span data-stu-id="2beb4-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="2beb4-145">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="2beb4-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="2beb4-146">Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **Reklaambänneri leht**.</span><span class="sxs-lookup"><span data-stu-id="2beb4-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="2beb4-147">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="2beb4-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="2beb4-148">Seadistage paremal paanil väärtus **Laius** olekusse **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="2beb4-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="2beb4-149">Lisage jaotises **Lehe liigendus** konteineri moodulile reklaambänneri moodul.</span><span class="sxs-lookup"><span data-stu-id="2beb4-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="2beb4-150">Lisage bänneri mooduli sätetes üks või mitu bänneri sõnumit.</span><span class="sxs-lookup"><span data-stu-id="2beb4-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="2beb4-151">Igas sõnumis võib olla tekst koos lingiga.</span><span class="sxs-lookup"><span data-stu-id="2beb4-151">Each message can have text together with a link.</span></span> <span data-ttu-id="2beb4-152">Et moodulit veelgi kohandada, võite redigeerida teisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="2beb4-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="2beb4-153">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="2beb4-153">Save and preview the page.</span></span> <span data-ttu-id="2beb4-154">Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="2beb4-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="2beb4-155">Viige lõpuni lehe redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="2beb4-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="2beb4-156">Reklaambännerit kasutatakse tavaliselt lehekülje päise pesas või alapealkirja pesas.</span><span class="sxs-lookup"><span data-stu-id="2beb4-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="2beb4-157">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2beb4-157">Additional resources</span></span>

[<span data-ttu-id="2beb4-158">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="2beb4-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2beb4-159">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="2beb4-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2beb4-160">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="2beb4-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2beb4-161">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="2beb4-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2beb4-162">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="2beb4-162">Video player module</span></span>](add-video-player.md)
