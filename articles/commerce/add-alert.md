---
title: Reklaambänneri moodul
description: See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: dae824cdbaaf56f85f125c5f36aaa56171bbd6bc
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411361"
---
# <a name="promo-banner-module"></a><span data-ttu-id="1cbb0-103">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="1cbb0-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1cbb0-104">See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1cbb0-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="1cbb0-105">Overview</span></span>

<span data-ttu-id="1cbb0-106">Reklaambänneri mooduleid kasutatakse lehel sisemiste teabesõnumite kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="1cbb0-107">Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="1cbb0-108">Reklaambännerid toetavad tekstsõnumit ja linki.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="1cbb0-109">Kui reklaambänneri moodulile on lisatud mitu teadet, muutub see pöörlevaks karussell-bänneriks, mis võimaldab klientidel vaadata läbi kõik sõnumid.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="1cbb0-110">Reklaambänneri moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="1cbb0-111">Reklaambännerite kasutamise näited e-kaubanduses</span><span class="sxs-lookup"><span data-stu-id="1cbb0-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="1cbb0-112">Reklaambännereid saab kasutada saidi päises, et näidata kogu saiti hõlmavaid kampaaniaid või teateid, nagu näiteks järgmistes näidetes.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="1cbb0-113">„Iga-aastane allahindlus lõppeb 10 päeva pärast”</span><span class="sxs-lookup"><span data-stu-id="1cbb0-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="1cbb0-114">„Suured allahindlused tagasi kooli kampaania ajal.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-114">"Save big with back to school sale.</span></span> <span data-ttu-id="1cbb0-115">Ostke kohe.”</span><span class="sxs-lookup"><span data-stu-id="1cbb0-115">Shop Now."</span></span>

<span data-ttu-id="1cbb0-116">„Ostle ja naudi tänupühade KAMPAANIAT!“</span><span class="sxs-lookup"><span data-stu-id="1cbb0-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="1cbb0-117">Järgmisel pildil on toodud reklaambänneri näide.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-117">The following image shows an example of a promo banner.</span></span>

![Reklaambänneri mooduli näide](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="1cbb0-119">Reklaambänneri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="1cbb0-119">Promo banner module properties</span></span>

| <span data-ttu-id="1cbb0-120">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="1cbb0-120">Property name</span></span>             | <span data-ttu-id="1cbb0-121">Väärtus</span><span class="sxs-lookup"><span data-stu-id="1cbb0-121">Value</span></span>                              | <span data-ttu-id="1cbb0-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1cbb0-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="1cbb0-123">Bänneri teated</span><span class="sxs-lookup"><span data-stu-id="1cbb0-123">Banner messages</span></span>           | <span data-ttu-id="1cbb0-124">Tekst ja lingid</span><span class="sxs-lookup"><span data-stu-id="1cbb0-124">Text and links</span></span>                     | <span data-ttu-id="1cbb0-125">Valik tekste ja linke.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-125">An array of text and links.</span></span> |
| <span data-ttu-id="1cbb0-126">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="1cbb0-126">Autoplay</span></span>                  | <span data-ttu-id="1cbb0-127">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-127">**True** or **False**</span></span>              | <span data-ttu-id="1cbb0-128">Väärtus, mis näitab, kas juhul kui konfigureeritud on mitu sõnumit, keritakse sõnumid automaatselt läbi.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="1cbb0-129">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="1cbb0-129">Slide transition interval</span></span> | <span data-ttu-id="1cbb0-130">Millisekundite arv (ms)</span><span class="sxs-lookup"><span data-stu-id="1cbb0-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="1cbb0-131">Sõnumite läbimiseks kasutatav intervall.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="1cbb0-132">Luba sulgemine</span><span class="sxs-lookup"><span data-stu-id="1cbb0-132">Allow dismiss</span></span>             | <span data-ttu-id="1cbb0-133">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-133">**True** or **False**</span></span>              | <span data-ttu-id="1cbb0-134">Kui väärtuseks on seatud olekusse **Tõene**, saavad kliendid teatise hüljata.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="1cbb0-135">Näita karusselli keerajat</span><span class="sxs-lookup"><span data-stu-id="1cbb0-135">Show carousel flipper</span></span>     | <span data-ttu-id="1cbb0-136">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-136">**True** or **False**</span></span>              | <span data-ttu-id="1cbb0-137">Väärtus, mis näitab, kas karusselli keerajaid tuleb kuvada, et kliendid saaksid käsitsi liikuda mitme bänneri vahel.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="1cbb0-138">Teksti joondus</span><span class="sxs-lookup"><span data-stu-id="1cbb0-138">Text alignment</span></span>            | <span data-ttu-id="1cbb0-139">**Paremal**, **Vasakul** või **Keskel**</span><span class="sxs-lookup"><span data-stu-id="1cbb0-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="1cbb0-140">Teksti joondamine reklaambänneri moodulis.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="1cbb0-141">Seos</span><span class="sxs-lookup"><span data-stu-id="1cbb0-141">Link</span></span>                      | <span data-ttu-id="1cbb0-142">URL</span><span class="sxs-lookup"><span data-stu-id="1cbb0-142">A URL</span></span>                              | <span data-ttu-id="1cbb0-143">Valikulise lingi URL.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="1cbb0-144">Reklaambänneri mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="1cbb0-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="1cbb0-145">Lehele reklaambänneri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="1cbb0-146">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1cbb0-147">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="1cbb0-148">Lisage jaotisse **Lehe liigendus** moodul **Vaikeleht** pesasse **Kehatekst**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="1cbb0-149">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="1cbb0-150">Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **Reklaambänneri leht**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="1cbb0-151">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="1cbb0-152">Seadistage paremal paanil väärtus **Laius** olekusse **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="1cbb0-153">Lisage jaotises **Lehe liigendus** konteineri moodulile reklaambänneri moodul.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="1cbb0-154">Lisage bänneri mooduli sätetes üks või mitu bänneri sõnumit.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="1cbb0-155">Igas sõnumis võib olla tekst koos lingiga.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-155">Each message can have text together with a link.</span></span> <span data-ttu-id="1cbb0-156">Et moodulit veelgi kohandada, võite redigeerida teisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="1cbb0-157">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="1cbb0-158">Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="1cbb0-159">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="1cbb0-160">Reklaambännerit kasutatakse tavaliselt lehekülje päise pesas või alapealkirja pesas.</span><span class="sxs-lookup"><span data-stu-id="1cbb0-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="1cbb0-161">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1cbb0-161">Additional resources</span></span>

[<span data-ttu-id="1cbb0-162">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="1cbb0-162">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1cbb0-163">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="1cbb0-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="1cbb0-164">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="1cbb0-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="1cbb0-165">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="1cbb0-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="1cbb0-166">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="1cbb0-166">Video player module</span></span>](add-video-player.md)
