---
title: Videopleieri moodul
description: See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid Microsofti rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 13072c8d6839fef1ab0dd55d626c23a2a1084d4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5209175"
---
# <a name="video-player-module"></a><span data-ttu-id="65ffd-103">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="65ffd-103">Video player module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="65ffd-104">See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid Microsofti rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="65ffd-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="65ffd-105">Videopleieri moodulit kasutatakse video taasesituse toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="65ffd-105">The video player module is used to support video playback.</span></span> <span data-ttu-id="65ffd-106">Seda saab lisada igale leheküljele, kui video sisu on üles laaditud ja sisuhaldussüsteemis (CMS) saadaval.</span><span class="sxs-lookup"><span data-stu-id="65ffd-106">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="65ffd-107">Videopleieri moodul toetab .mp4 meediatüüpi.</span><span class="sxs-lookup"><span data-stu-id="65ffd-107">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="65ffd-108">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="65ffd-108">Video player module</span></span>

<span data-ttu-id="65ffd-109">Videopleieri moodulit saab kasutada videote esitamiseks e-kaubanduse saidil.</span><span class="sxs-lookup"><span data-stu-id="65ffd-109">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="65ffd-110">See toetab kõiki taasesituse võimalusi, nagu esitamine, peatamine, täissuuruses režiim, helikirjeldused ja suletud pealdised.</span><span class="sxs-lookup"><span data-stu-id="65ffd-110">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="65ffd-111">Videopleieri moodul toetab ka suletud pealdiste kohandamist, et see vastaks Microsofti juurdepääsu standarditele.</span><span class="sxs-lookup"><span data-stu-id="65ffd-111">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="65ffd-112">Näiteks saate kohandada fondi suurust ja taustavärvi.</span><span class="sxs-lookup"><span data-stu-id="65ffd-112">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="65ffd-113">Video mängija moodul toetab ka sekundaarseid audio palasid.</span><span class="sxs-lookup"><span data-stu-id="65ffd-113">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="65ffd-114">Kui video on CMS-i üles laaditud, saab ka teisese heliriba üles laadida.</span><span class="sxs-lookup"><span data-stu-id="65ffd-114">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="65ffd-115">Kui kasutaja valib selle, saab video pleieri moodul esitada teise heliriba.</span><span class="sxs-lookup"><span data-stu-id="65ffd-115">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="65ffd-116">E-kaubanduse videopleieri moodulite näited</span><span class="sxs-lookup"><span data-stu-id="65ffd-116">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="65ffd-117">Juhiste videod toote üksikasjade lehtedel või turunduse lehtedel</span><span class="sxs-lookup"><span data-stu-id="65ffd-117">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="65ffd-118">Kampaaniavideod või videod eeskirjade kohta mis tahes turunduse lehel</span><span class="sxs-lookup"><span data-stu-id="65ffd-118">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="65ffd-119">Turundusvideod, mis tõstavad toote üksikasjade lehtedel või turunduse lehtedel esile toote omadused</span><span class="sxs-lookup"><span data-stu-id="65ffd-119">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="65ffd-120">Järgmisel pildil on näide videopleieri moodulist avalehel.</span><span class="sxs-lookup"><span data-stu-id="65ffd-120">The following image shows an example of a video player module on a home page.</span></span>

![Videopleieri mooduli näide](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="65ffd-122">Videopleieri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="65ffd-122">Video player module properties</span></span>

| <span data-ttu-id="65ffd-123">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="65ffd-123">Property name</span></span>         | <span data-ttu-id="65ffd-124">Väärtus</span><span class="sxs-lookup"><span data-stu-id="65ffd-124">Value</span></span>                               | <span data-ttu-id="65ffd-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="65ffd-125">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="65ffd-126">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="65ffd-126">Auto play</span></span>             | <span data-ttu-id="65ffd-127">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-127">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-128">Kui väärtuseks on seatud **Tõene**, esitatakse video automaatselt.</span><span class="sxs-lookup"><span data-stu-id="65ffd-128">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="65ffd-129">Vaigista</span><span class="sxs-lookup"><span data-stu-id="65ffd-129">Mute</span></span>                  | <span data-ttu-id="65ffd-130">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-130">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-131">Kui väärtuseks on seatud **Tõene**, on heli vaigistatud.</span><span class="sxs-lookup"><span data-stu-id="65ffd-131">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="65ffd-132">Selle pleieri vaikeväärtus on **Väär**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-132">For this player, the default value is **False**.</span></span> <span data-ttu-id="65ffd-133">Chrome’i brauseris on automaatselt esitatavad videod vaikimisi vaigistatud ja heli esitatakse ainult siis, kui kasutaja esitab videot käsitsi.</span><span class="sxs-lookup"><span data-stu-id="65ffd-133">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="65ffd-134">Silmus</span><span class="sxs-lookup"><span data-stu-id="65ffd-134">Loop</span></span>                  | <span data-ttu-id="65ffd-135">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-135">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-136">Kui väärtuseks on seatud **Tõene**, korratakse videot tsüklis.</span><span class="sxs-lookup"><span data-stu-id="65ffd-136">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="65ffd-137">Värbamisvahend</span><span class="sxs-lookup"><span data-stu-id="65ffd-137">Media</span></span>                 | <span data-ttu-id="65ffd-138">Videofaili tee ja nimi</span><span class="sxs-lookup"><span data-stu-id="65ffd-138">Video file path and name</span></span> | <span data-ttu-id="65ffd-139">Videopleieris esitatav videofail.</span><span class="sxs-lookup"><span data-stu-id="65ffd-139">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="65ffd-140">Täisekraanil esitamine</span><span class="sxs-lookup"><span data-stu-id="65ffd-140">Play fullscreen</span></span>       | <span data-ttu-id="65ffd-141">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-141">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-142">Kui väärtuseks on seatud **Tõene**, esitatakse video täisekraanil režiimis.</span><span class="sxs-lookup"><span data-stu-id="65ffd-142">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="65ffd-143">Lüliti Esita/Peata</span><span class="sxs-lookup"><span data-stu-id="65ffd-143">Play pause trigger</span></span>    | <span data-ttu-id="65ffd-144">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-144">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-145">Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp.</span><span class="sxs-lookup"><span data-stu-id="65ffd-145">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="65ffd-146">Videopleieri juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="65ffd-146">Video player controls</span></span> | <span data-ttu-id="65ffd-147">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-147">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-148">Kui väärtuseks on seatud **Tõene**, kuvatakse kõik vidopleieri juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="65ffd-148">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="65ffd-149">Need juhtelemendid hõlmavad esitamise ja peatamise nuppe, edenemise näidikut ja suletud pealdise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="65ffd-149">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="65ffd-150">Peida plakati pilt</span><span class="sxs-lookup"><span data-stu-id="65ffd-150">Hide poster image</span></span>     | <span data-ttu-id="65ffd-151">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="65ffd-151">**True** or **False**</span></span>               | <span data-ttu-id="65ffd-152">Videol võib olla plakati raam.</span><span class="sxs-lookup"><span data-stu-id="65ffd-152">A video can have a poster frame.</span></span> <span data-ttu-id="65ffd-153">Kui selle atribuudi väärtuseks on seatud **Tõene**, on plakati raam peidetud.</span><span class="sxs-lookup"><span data-stu-id="65ffd-153">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="65ffd-154">Maski tase</span><span class="sxs-lookup"><span data-stu-id="65ffd-154">Mask level</span></span>            | <span data-ttu-id="65ffd-155">Number vahemikus **0** kuni **100**</span><span class="sxs-lookup"><span data-stu-id="65ffd-155">A number from **0** through **100**</span></span> | <span data-ttu-id="65ffd-156">Video laadi jaoks rakendatav mask.</span><span class="sxs-lookup"><span data-stu-id="65ffd-156">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="65ffd-157">Videopleieri mooduli lisamine lehele</span><span class="sxs-lookup"><span data-stu-id="65ffd-157">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="65ffd-158">Enne kui loote videopleieri mooduli, peate esmalt video meediateeki üles laadima.</span><span class="sxs-lookup"><span data-stu-id="65ffd-158">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="65ffd-159">Uuele lehele videopleieri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="65ffd-159">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="65ffd-160">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="65ffd-161">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Videopleieri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-161">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-162">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-162">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65ffd-163">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-163">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-164">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-164">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65ffd-165">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-165">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-166">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-166">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65ffd-167">Valige dialoogiboksis **Lisa moodul** moodul **Videopleier** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-167">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-168">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-168">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="65ffd-169">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-169">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="65ffd-170">Valige dialoogiboksis **Vali mall** teie loodud videopleieri mall.</span><span class="sxs-lookup"><span data-stu-id="65ffd-170">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="65ffd-171">Sisestage jaotises **Lehe nimi** väärtus **Videopleieri leht** ja seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-171">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-172">Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-172">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65ffd-173">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-173">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-174">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-174">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="65ffd-175">Valige dialoogiboksis **Lisa moodul** moodul **Videopleier** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-175">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-176">Valige videopleieri mooduli atribuutide paanil **Video lisamine**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-176">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="65ffd-177">Valige dialoogiaknas **Meedia valija** video ja seejärel valige **Laadi üles uus meedium**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-177">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="65ffd-178">Valige File Exploreris videofail ja seejärel **Ava**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-178">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="65ffd-179">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** pealkiri ja muu vajalik teave ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-179">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="65ffd-180">Valige dialoogiboksis **Meedia valija** käsk **Sule**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-180">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="65ffd-181">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-181">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="65ffd-182">Peaksite nägema lehel videomoodulit.</span><span class="sxs-lookup"><span data-stu-id="65ffd-182">You should see the video module on the page.</span></span> <span data-ttu-id="65ffd-183">Saate muuta täiendavaid sätteid mooduli käitumise kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="65ffd-183">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="65ffd-184">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="65ffd-184">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="65ffd-185">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="65ffd-185">Additional resources</span></span>

[<span data-ttu-id="65ffd-186">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="65ffd-186">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="65ffd-187">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="65ffd-187">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="65ffd-188">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="65ffd-188">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="65ffd-189">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="65ffd-189">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="65ffd-190">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="65ffd-190">Content block module</span></span>](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]