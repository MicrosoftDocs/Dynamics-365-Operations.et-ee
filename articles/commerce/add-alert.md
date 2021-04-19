---
title: Reklaambänneri moodul
description: See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796242"
---
# <a name="promo-banner-module"></a><span data-ttu-id="57d66-103">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="57d66-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="57d66-104">See teema hõlmab reklaambänneri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="57d66-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="57d66-105">Reklaambänneri mooduleid kasutatakse lehel sisemiste teabesõnumite kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="57d66-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="57d66-106">Neid saab kasutada kõikidel e-kaubanduse saidi lehtedel ilmuvate saidiüleste kampaaniate kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="57d66-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="57d66-107">Reklaambännerid toetavad tekstsõnumit ja linki.</span><span class="sxs-lookup"><span data-stu-id="57d66-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="57d66-108">Kui reklaambänneri moodulile on lisatud mitu teadet, muutub see pöörlevaks karussell-bänneriks, mis võimaldab klientidel vaadata läbi kõik sõnumid.</span><span class="sxs-lookup"><span data-stu-id="57d66-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="57d66-109">Reklaambänneri moodulid põhinevad sisuhaldussüsteemi (CMS) andmetel ja neid saab panna igale lehele.</span><span class="sxs-lookup"><span data-stu-id="57d66-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="57d66-110">Reklaambännerite kasutamise näited e-kaubanduses</span><span class="sxs-lookup"><span data-stu-id="57d66-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="57d66-111">Reklaambännereid saab kasutada saidi päises, et näidata kogu saiti hõlmavaid kampaaniaid või teateid, nagu näiteks järgmistes näidetes.</span><span class="sxs-lookup"><span data-stu-id="57d66-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="57d66-112">„Iga-aastane allahindlus lõppeb 10 päeva pärast”</span><span class="sxs-lookup"><span data-stu-id="57d66-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="57d66-113">„Suured allahindlused tagasi kooli kampaania ajal.</span><span class="sxs-lookup"><span data-stu-id="57d66-113">"Save big with back to school sale.</span></span> <span data-ttu-id="57d66-114">Ostke kohe.”</span><span class="sxs-lookup"><span data-stu-id="57d66-114">Shop Now."</span></span>

<span data-ttu-id="57d66-115">„Ostle ja naudi tänupühade KAMPAANIAT!“</span><span class="sxs-lookup"><span data-stu-id="57d66-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="57d66-116">Järgmisel pildil on toodud reklaambänneri näide.</span><span class="sxs-lookup"><span data-stu-id="57d66-116">The following image shows an example of a promo banner.</span></span>

![Reklaambänneri mooduli näide](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="57d66-118">Reklaambänneri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="57d66-118">Promo banner module properties</span></span>

| <span data-ttu-id="57d66-119">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="57d66-119">Property name</span></span>             | <span data-ttu-id="57d66-120">Väärtus</span><span class="sxs-lookup"><span data-stu-id="57d66-120">Value</span></span>                              | <span data-ttu-id="57d66-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="57d66-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="57d66-122">Bänneri teated</span><span class="sxs-lookup"><span data-stu-id="57d66-122">Banner messages</span></span>           | <span data-ttu-id="57d66-123">Tekst ja lingid</span><span class="sxs-lookup"><span data-stu-id="57d66-123">Text and links</span></span>                     | <span data-ttu-id="57d66-124">Valik tekste ja linke.</span><span class="sxs-lookup"><span data-stu-id="57d66-124">An array of text and links.</span></span> |
| <span data-ttu-id="57d66-125">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="57d66-125">Autoplay</span></span>                  | <span data-ttu-id="57d66-126">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="57d66-126">**True** or **False**</span></span>              | <span data-ttu-id="57d66-127">Väärtus, mis näitab, kas juhul kui konfigureeritud on mitu sõnumit, keritakse sõnumid automaatselt läbi.</span><span class="sxs-lookup"><span data-stu-id="57d66-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="57d66-128">Slaidi ülemineku intervall</span><span class="sxs-lookup"><span data-stu-id="57d66-128">Slide transition interval</span></span> | <span data-ttu-id="57d66-129">Millisekundite arv (ms)</span><span class="sxs-lookup"><span data-stu-id="57d66-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="57d66-130">Sõnumite läbimiseks kasutatav intervall.</span><span class="sxs-lookup"><span data-stu-id="57d66-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="57d66-131">Luba sulgemine</span><span class="sxs-lookup"><span data-stu-id="57d66-131">Allow dismiss</span></span>             | <span data-ttu-id="57d66-132">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="57d66-132">**True** or **False**</span></span>              | <span data-ttu-id="57d66-133">Kui väärtuseks on seatud olekusse **Tõene**, saavad kliendid teatise hüljata.</span><span class="sxs-lookup"><span data-stu-id="57d66-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="57d66-134">Näita karusselli keerajat</span><span class="sxs-lookup"><span data-stu-id="57d66-134">Show carousel flipper</span></span>     | <span data-ttu-id="57d66-135">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="57d66-135">**True** or **False**</span></span>              | <span data-ttu-id="57d66-136">Väärtus, mis näitab, kas karusselli keerajaid tuleb kuvada, et kliendid saaksid käsitsi liikuda mitme bänneri vahel.</span><span class="sxs-lookup"><span data-stu-id="57d66-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="57d66-137">Teksti joondus</span><span class="sxs-lookup"><span data-stu-id="57d66-137">Text alignment</span></span>            | <span data-ttu-id="57d66-138">**Paremal**, **Vasakul** või **Keskel**</span><span class="sxs-lookup"><span data-stu-id="57d66-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="57d66-139">Teksti joondamine reklaambänneri moodulis.</span><span class="sxs-lookup"><span data-stu-id="57d66-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="57d66-140">Seos</span><span class="sxs-lookup"><span data-stu-id="57d66-140">Link</span></span>                      | <span data-ttu-id="57d66-141">URL</span><span class="sxs-lookup"><span data-stu-id="57d66-141">A URL</span></span>                              | <span data-ttu-id="57d66-142">Valikulise lingi URL.</span><span class="sxs-lookup"><span data-stu-id="57d66-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="57d66-143">Reklaambänneri mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="57d66-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="57d66-144">Lehele reklaambänneri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="57d66-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="57d66-145">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="57d66-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="57d66-146">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Reklaambänneri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="57d66-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="57d66-147">Lisage jaotisse **Lehe liigendus** moodul **Vaikeleht** pesasse **Kehatekst**.</span><span class="sxs-lookup"><span data-stu-id="57d66-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="57d66-148">Valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="57d66-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="57d66-149">Kasutage äsja loodud teatise malli, et luua leht, mille nimi on **Reklaambänneri leht**.</span><span class="sxs-lookup"><span data-stu-id="57d66-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="57d66-150">Lisage uue lehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="57d66-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="57d66-151">Seadistage paremal paanil väärtus **Laius** olekusse **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="57d66-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="57d66-152">Lisage jaotises **Lehe liigendus** konteineri moodulile reklaambänneri moodul.</span><span class="sxs-lookup"><span data-stu-id="57d66-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="57d66-153">Lisage bänneri mooduli sätetes üks või mitu bänneri sõnumit.</span><span class="sxs-lookup"><span data-stu-id="57d66-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="57d66-154">Igas sõnumis võib olla tekst koos lingiga.</span><span class="sxs-lookup"><span data-stu-id="57d66-154">Each message can have text together with a link.</span></span> <span data-ttu-id="57d66-155">Et moodulit veelgi kohandada, võite redigeerida teisi atribuute.</span><span class="sxs-lookup"><span data-stu-id="57d66-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="57d66-156">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="57d66-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="57d66-157">Lehe ülaosas peaksite nägema teatist teie lisatud tekstiga.</span><span class="sxs-lookup"><span data-stu-id="57d66-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="57d66-158">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="57d66-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="57d66-159">Reklaambännerit kasutatakse tavaliselt lehekülje päise pesas või alapealkirja pesas.</span><span class="sxs-lookup"><span data-stu-id="57d66-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="57d66-160">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="57d66-160">Additional resources</span></span>

[<span data-ttu-id="57d66-161">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="57d66-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="57d66-162">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="57d66-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="57d66-163">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="57d66-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="57d66-164">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="57d66-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="57d66-165">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="57d66-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]