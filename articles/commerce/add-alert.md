---
title: Reklaambänneri moodul
description: See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a77196be69bb71d917bf84c633199a3af3fbf478
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986025"
---
# <a name="promo-banner-module"></a><span data-ttu-id="c1dcc-103">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="c1dcc-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c1dcc-104">See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c1dcc-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="c1dcc-105">Overview</span></span>

<span data-ttu-id="c1dcc-106">Reklaambänneri mooduleid kasutatakse lehel sisemiste teabesõnumite kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="c1dcc-107">Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="c1dcc-108">Reklaambännerid toetavad tekstsõnumit ja linki.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="c1dcc-109">Kui reklaambänneri moodulile on lisatud mitu teadet, muutub see pöörlevaks karussell-bänneriks, mis võimaldab klientidel vaadata läbi kõik sõnumid.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="c1dcc-110">Reklaambänneri moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="c1dcc-111">Reklaambännerite kasutamise näited e-kaubanduses</span><span class="sxs-lookup"><span data-stu-id="c1dcc-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="c1dcc-112">Reklaambännereid saab kasutada saidi päises, et näidata kogu saiti hõlmavaid kampaaniaid või teateid, nagu näiteks järgmistes näidetes.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="c1dcc-113">„Iga-aastane allahindlus lõppeb 10 päeva pärast”</span><span class="sxs-lookup"><span data-stu-id="c1dcc-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="c1dcc-114">„Suured allahindlused tagasi kooli kampaania ajal.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-114">"Save big with back to school sale.</span></span> <span data-ttu-id="c1dcc-115">Ostke kohe.”</span><span class="sxs-lookup"><span data-stu-id="c1dcc-115">Shop Now."</span></span>

<span data-ttu-id="c1dcc-116">„Ostle ja naudi tänupühade KAMPAANIAT!“</span><span class="sxs-lookup"><span data-stu-id="c1dcc-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="c1dcc-117">Järgmisel pildil on toodud reklaambänneri näide.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-117">The following image shows an example of a promo banner.</span></span>

![Reklaambänneri mooduli näide](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="c1dcc-119">Reklaambänneri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="c1dcc-119">Promo banner module properties</span></span>

| <span data-ttu-id="c1dcc-120">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="c1dcc-120">Property name</span></span>             | <span data-ttu-id="c1dcc-121">Väärtus</span><span class="sxs-lookup"><span data-stu-id="c1dcc-121">Value</span></span>                              | <span data-ttu-id="c1dcc-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c1dcc-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="c1dcc-123">Bänneri teated</span><span class="sxs-lookup"><span data-stu-id="c1dcc-123">Banner messages</span></span>           | <span data-ttu-id="c1dcc-124">Tekst ja lingid</span><span class="sxs-lookup"><span data-stu-id="c1dcc-124">Text and links</span></span>                     | <span data-ttu-id="c1dcc-125">Valik tekste ja linke.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-125">An array of text and links.</span></span> |
| <span data-ttu-id="c1dcc-126">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="c1dcc-126">Autoplay</span></span>                  | <span data-ttu-id="c1dcc-127">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="c1dcc-127">**True** or **False**</span></span>              | <span data-ttu-id="c1dcc-128">Väärtus, mis näitab, kas juhul kui konfigureeritud on mitu sõnumit, keritakse sõnumid automaatselt läbi.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="c1dcc-129">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="c1dcc-129">Slide transition interval</span></span> | <span data-ttu-id="c1dcc-130">Millisekundite arv (ms)</span><span class="sxs-lookup"><span data-stu-id="c1dcc-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="c1dcc-131">Sõnumite läbimiseks kasutatav intervall.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="c1dcc-132">Luba sulgemine</span><span class="sxs-lookup"><span data-stu-id="c1dcc-132">Allow dismiss</span></span>             | <span data-ttu-id="c1dcc-133">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="c1dcc-133">**True** or **False**</span></span>              | <span data-ttu-id="c1dcc-134">Kui väärtuseks on seatud olekusse **Tõene**, saavad kliendid teatise hüljata.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="c1dcc-135">Näita karusselli keerajat</span><span class="sxs-lookup"><span data-stu-id="c1dcc-135">Show carousel flipper</span></span>     | <span data-ttu-id="c1dcc-136">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="c1dcc-136">**True** or **False**</span></span>              | <span data-ttu-id="c1dcc-137">Väärtus, mis näitab, kas karusselli keerajaid tuleb kuvada, et kliendid saaksid käsitsi liikuda mitme bänneri vahel.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="c1dcc-138">Teksti joondus</span><span class="sxs-lookup"><span data-stu-id="c1dcc-138">Text alignment</span></span>            | <span data-ttu-id="c1dcc-139">**Paremal**, **Vasakul** või **Keskel**</span><span class="sxs-lookup"><span data-stu-id="c1dcc-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="c1dcc-140">Teksti joondamine reklaambänneri moodulis.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="c1dcc-141">Seos</span><span class="sxs-lookup"><span data-stu-id="c1dcc-141">Link</span></span>                      | <span data-ttu-id="c1dcc-142">URL</span><span class="sxs-lookup"><span data-stu-id="c1dcc-142">A URL</span></span>                              | <span data-ttu-id="c1dcc-143">Valikulise lingi URL.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="c1dcc-144">Reklaambänneri mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="c1dcc-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="c1dcc-145">Lehele reklaambänneri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c1dcc-146">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="c1dcc-147">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="c1dcc-148">Lisage jaotisse **Lehe liigendus** moodul **Vaikeleht** pesasse **Kehatekst**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="c1dcc-149">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="c1dcc-150">Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **Reklaambänneri leht**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="c1dcc-151">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="c1dcc-152">Seadistage paremal paanil väärtus **Laius** olekusse **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="c1dcc-153">Lisage jaotises **Lehe liigendus** konteineri moodulile reklaambänneri moodul.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="c1dcc-154">Lisage bänneri mooduli sätetes üks või mitu bänneri sõnumit.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="c1dcc-155">Igas sõnumis võib olla tekst koos lingiga.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-155">Each message can have text together with a link.</span></span> <span data-ttu-id="c1dcc-156">Et moodulit veelgi kohandada, võite redigeerida teisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="c1dcc-157">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="c1dcc-158">Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="c1dcc-159">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="c1dcc-160">Reklaambännerit kasutatakse tavaliselt lehekülje päise pesas või alapealkirja pesas.</span><span class="sxs-lookup"><span data-stu-id="c1dcc-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="c1dcc-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c1dcc-161">Additional resources</span></span>

[<span data-ttu-id="c1dcc-162">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="c1dcc-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c1dcc-163">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="c1dcc-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="c1dcc-164">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="c1dcc-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="c1dcc-165">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="c1dcc-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="c1dcc-166">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="c1dcc-166">Video player module</span></span>](add-video-player.md)
