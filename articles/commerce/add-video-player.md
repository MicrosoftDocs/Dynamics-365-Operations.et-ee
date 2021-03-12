---
title: Videopleieri moodul
description: See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 712e9359e31be96c426d6f16c878f18f05cc1bd2
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980103"
---
# <a name="video-player-module"></a><span data-ttu-id="cee18-103">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="cee18-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cee18-104">See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="cee18-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cee18-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="cee18-105">Overview</span></span>

<span data-ttu-id="cee18-106">Videopleieri moodulit kasutatakse video taasesituse toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="cee18-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="cee18-107">Seda saab lisada igale leheküljele, kui video sisu on üles laaditud ja sisuhaldussüsteemis (CMS) saadaval.</span><span class="sxs-lookup"><span data-stu-id="cee18-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="cee18-108">Videopleieri moodul toetab .mp4 meediatüüpi.</span><span class="sxs-lookup"><span data-stu-id="cee18-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="cee18-109">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="cee18-109">Video player module</span></span>

<span data-ttu-id="cee18-110">Videopleieri moodulit saab kasutada videote esitamiseks e-kaubanduse saidil.</span><span class="sxs-lookup"><span data-stu-id="cee18-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="cee18-111">See toetab kõiki taasesituse võimalusi, nagu esitamine, peatamine, täissuuruses režiim, helikirjeldused ja suletud pealdised.</span><span class="sxs-lookup"><span data-stu-id="cee18-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="cee18-112">Videopleieri moodul toetab ka suletud pealdiste kohandamist, et see vastaks Microsofti juurdepääsu standarditele.</span><span class="sxs-lookup"><span data-stu-id="cee18-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="cee18-113">Näiteks saate kohandada fondi suurust ja taustavärvi.</span><span class="sxs-lookup"><span data-stu-id="cee18-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="cee18-114">Video mängija moodul toetab ka sekundaarseid audio palasid.</span><span class="sxs-lookup"><span data-stu-id="cee18-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="cee18-115">Kui video on CMS-i üles laaditud, saab ka teisese heliriba üles laadida.</span><span class="sxs-lookup"><span data-stu-id="cee18-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="cee18-116">Kui kasutaja valib selle, saab video pleieri moodul esitada teise heliriba.</span><span class="sxs-lookup"><span data-stu-id="cee18-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="cee18-117">E-kaubanduse videopleieri moodulite näited</span><span class="sxs-lookup"><span data-stu-id="cee18-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="cee18-118">Juhiste videod toote üksikasjade lehtedel või turunduse lehtedel</span><span class="sxs-lookup"><span data-stu-id="cee18-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="cee18-119">Kampaaniavideod või videod eeskirjade kohta mis tahes turunduse lehel</span><span class="sxs-lookup"><span data-stu-id="cee18-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="cee18-120">Turundusvideod, mis tõstavad toote üksikasjade lehtedel või turunduse lehtedel esile toote omadused</span><span class="sxs-lookup"><span data-stu-id="cee18-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="cee18-121">Järgmisel pildil on näide videopleieri moodulist avalehel.</span><span class="sxs-lookup"><span data-stu-id="cee18-121">The following image shows an example of a video player module on a home page.</span></span>

![Videopleieri mooduli näide](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="cee18-123">Videopleieri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="cee18-123">Video player module properties</span></span>

| <span data-ttu-id="cee18-124">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="cee18-124">Property name</span></span>         | <span data-ttu-id="cee18-125">Väärtus</span><span class="sxs-lookup"><span data-stu-id="cee18-125">Value</span></span>                               | <span data-ttu-id="cee18-126">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cee18-126">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="cee18-127">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="cee18-127">Auto play</span></span>             | <span data-ttu-id="cee18-128">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-128">**True** or **False**</span></span>               | <span data-ttu-id="cee18-129">Kui väärtuseks on seatud **Tõene**, esitatakse video automaatselt.</span><span class="sxs-lookup"><span data-stu-id="cee18-129">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="cee18-130">Vaigista</span><span class="sxs-lookup"><span data-stu-id="cee18-130">Mute</span></span>                  | <span data-ttu-id="cee18-131">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-131">**True** or **False**</span></span>               | <span data-ttu-id="cee18-132">Kui väärtuseks on seatud **Tõene**, on heli vaigistatud.</span><span class="sxs-lookup"><span data-stu-id="cee18-132">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="cee18-133">Selle pleieri vaikeväärtus on **Väär**.</span><span class="sxs-lookup"><span data-stu-id="cee18-133">For this player, the default value is **False**.</span></span> <span data-ttu-id="cee18-134">Chrome’i brauseris on automaatselt esitatavad videod vaikimisi vaigistatud ja heli esitatakse ainult siis, kui kasutaja esitab videot käsitsi.</span><span class="sxs-lookup"><span data-stu-id="cee18-134">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="cee18-135">Silmus</span><span class="sxs-lookup"><span data-stu-id="cee18-135">Loop</span></span>                  | <span data-ttu-id="cee18-136">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-136">**True** or **False**</span></span>               | <span data-ttu-id="cee18-137">Kui väärtuseks on seatud **Tõene**, korratakse videot tsüklis.</span><span class="sxs-lookup"><span data-stu-id="cee18-137">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="cee18-138">Värbamisvahend</span><span class="sxs-lookup"><span data-stu-id="cee18-138">Media</span></span>                 | <span data-ttu-id="cee18-139">Videofaili tee ja nimi</span><span class="sxs-lookup"><span data-stu-id="cee18-139">Video file path and name</span></span> | <span data-ttu-id="cee18-140">Videopleieris esitatav videofail.</span><span class="sxs-lookup"><span data-stu-id="cee18-140">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="cee18-141">Täisekraanil esitamine</span><span class="sxs-lookup"><span data-stu-id="cee18-141">Play fullscreen</span></span>       | <span data-ttu-id="cee18-142">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-142">**True** or **False**</span></span>               | <span data-ttu-id="cee18-143">Kui väärtuseks on seatud **Tõene**, esitatakse video täisekraanil režiimis.</span><span class="sxs-lookup"><span data-stu-id="cee18-143">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="cee18-144">Lüliti Esita/Peata</span><span class="sxs-lookup"><span data-stu-id="cee18-144">Play pause trigger</span></span>    | <span data-ttu-id="cee18-145">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-145">**True** or **False**</span></span>               | <span data-ttu-id="cee18-146">Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp.</span><span class="sxs-lookup"><span data-stu-id="cee18-146">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="cee18-147">Videopleieri juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="cee18-147">Video player controls</span></span> | <span data-ttu-id="cee18-148">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-148">**True** or **False**</span></span>               | <span data-ttu-id="cee18-149">Kui väärtuseks on seatud **Tõene**, kuvatakse kõik vidopleieri juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="cee18-149">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="cee18-150">Need juhtelemendid hõlmavad esitamise ja peatamise nuppe, edenemise näidikut ja suletud pealdise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="cee18-150">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="cee18-151">Peida plakati pilt</span><span class="sxs-lookup"><span data-stu-id="cee18-151">Hide poster image</span></span>     | <span data-ttu-id="cee18-152">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="cee18-152">**True** or **False**</span></span>               | <span data-ttu-id="cee18-153">Videol võib olla plakati raam.</span><span class="sxs-lookup"><span data-stu-id="cee18-153">A video can have a poster frame.</span></span> <span data-ttu-id="cee18-154">Kui selle atribuudi väärtuseks on seatud **Tõene**, on plakati raam peidetud.</span><span class="sxs-lookup"><span data-stu-id="cee18-154">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="cee18-155">Maski tase</span><span class="sxs-lookup"><span data-stu-id="cee18-155">Mask level</span></span>            | <span data-ttu-id="cee18-156">Number vahemikus **0** kuni **100**</span><span class="sxs-lookup"><span data-stu-id="cee18-156">A number from **0** through **100**</span></span> | <span data-ttu-id="cee18-157">Video laadi jaoks rakendatav mask.</span><span class="sxs-lookup"><span data-stu-id="cee18-157">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="cee18-158">Videopleieri mooduli lisamine lehele</span><span class="sxs-lookup"><span data-stu-id="cee18-158">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="cee18-159">Enne kui loote videopleieri mooduli, peate esmalt video meediateeki üles laadima.</span><span class="sxs-lookup"><span data-stu-id="cee18-159">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="cee18-160">Uuele lehele videopleieri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cee18-160">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cee18-161">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cee18-161">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="cee18-162">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Videopleieri mall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-162">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-163">Valige pesas **Keha** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cee18-163">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cee18-164">Valige dialoogiboksis **Lisa moodul** moodul **Vaikeleht** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-164">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-165">Valige mooduli **Vaikeleht** pesas **Peamine** kolmikpunkt (**...**) ja seejärel suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cee18-165">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cee18-166">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-166">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-167">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cee18-167">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cee18-168">Valige dialoogiboksis **Lisa moodul** moodul **Videopleier** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-168">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-169">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="cee18-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="cee18-170">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cee18-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="cee18-171">Valige dialoogiboksis **Vali mall** teie loodud videopleieri mall.</span><span class="sxs-lookup"><span data-stu-id="cee18-171">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="cee18-172">Sisestage jaotises **Lehe nimi** väärtus **Videopleieri leht** ja seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-172">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-173">Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cee18-173">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cee18-174">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-175">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="cee18-175">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cee18-176">Valige dialoogiboksis **Lisa moodul** moodul **Videopleier** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-176">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-177">Valige videopleieri mooduli atribuutide paanil **Video lisamine**.</span><span class="sxs-lookup"><span data-stu-id="cee18-177">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="cee18-178">Valige dialoogiaknas **Meedia valija** video ja seejärel valige **Laadi üles uus meedium**.</span><span class="sxs-lookup"><span data-stu-id="cee18-178">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="cee18-179">Valige File Exploreris videofail ja seejärel **Ava**.</span><span class="sxs-lookup"><span data-stu-id="cee18-179">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="cee18-180">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** pealkiri ja muu vajalik teave ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="cee18-180">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="cee18-181">Valige dialoogiboksis **Meedia valija** käsk **Sule**.</span><span class="sxs-lookup"><span data-stu-id="cee18-181">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="cee18-182">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="cee18-182">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="cee18-183">Peaksite nägema lehel videomoodulit.</span><span class="sxs-lookup"><span data-stu-id="cee18-183">You should see the video module on the page.</span></span> <span data-ttu-id="cee18-184">Saate muuta täiendavaid sätteid mooduli käitumise kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="cee18-184">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="cee18-185">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="cee18-185">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="cee18-186">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cee18-186">Additional resources</span></span>

[<span data-ttu-id="cee18-187">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="cee18-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cee18-188">Kampaania ribareklaami moodul</span><span class="sxs-lookup"><span data-stu-id="cee18-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="cee18-189">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="cee18-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="cee18-190">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="cee18-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="cee18-191">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="cee18-191">Content block module</span></span>](add-hero-module.md)
