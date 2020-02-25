---
title: Videopleieri moodul
description: See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025640"
---
# <a name="video-player-module"></a><span data-ttu-id="ee58e-103">Videopleieri moodul</span><span class="sxs-lookup"><span data-stu-id="ee58e-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ee58e-104">See teema hõlmab videopleieri mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="ee58e-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ee58e-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ee58e-105">Overview</span></span>

<span data-ttu-id="ee58e-106">Videopleieri moodulit kasutatakse video taasesituse toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee58e-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="ee58e-107">Seda saab lisada igale leheküljele, kui video sisu on üles laaditud ja sisuhaldussüsteemis (CMS) saadaval.</span><span class="sxs-lookup"><span data-stu-id="ee58e-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="ee58e-108">Videopleieri moodul toetab .mp4 meediatüüpi.</span><span class="sxs-lookup"><span data-stu-id="ee58e-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="ee58e-109">Videopleierimoodul</span><span class="sxs-lookup"><span data-stu-id="ee58e-109">Video player module</span></span>

<span data-ttu-id="ee58e-110">Videopleieri moodulit saab kasutada videote esitamiseks e-kaubanduse saidil.</span><span class="sxs-lookup"><span data-stu-id="ee58e-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="ee58e-111">See toetab kõiki taasesituse võimalusi, nagu esitamine, peatamine, täissuuruses režiim, helikirjeldused ja suletud pealdised.</span><span class="sxs-lookup"><span data-stu-id="ee58e-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="ee58e-112">Videopleieri moodul toetab ka suletud pealdiste kohandamist, et see vastaks Microsofti juurdepääsu standarditele.</span><span class="sxs-lookup"><span data-stu-id="ee58e-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="ee58e-113">Näiteks saate kohandada fondi suurust ja taustavärvi.</span><span class="sxs-lookup"><span data-stu-id="ee58e-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="ee58e-114">Video mängija moodul toetab ka sekundaarseid audio palasid.</span><span class="sxs-lookup"><span data-stu-id="ee58e-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="ee58e-115">Kui video on CMS-i üles laaditud, saab ka teisese heliriba üles laadida.</span><span class="sxs-lookup"><span data-stu-id="ee58e-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="ee58e-116">Kui kasutaja valib selle, saab video pleieri moodul esitada teise heliriba.</span><span class="sxs-lookup"><span data-stu-id="ee58e-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="ee58e-117">E-kaubanduse videopleieri moodulite näited</span><span class="sxs-lookup"><span data-stu-id="ee58e-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="ee58e-118">Juhiste videod toote üksikasjade lehtedel või turunduse lehtedel</span><span class="sxs-lookup"><span data-stu-id="ee58e-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="ee58e-119">Kampaaniavideod või videod eeskirjade kohta mis tahes turunduse lehel</span><span class="sxs-lookup"><span data-stu-id="ee58e-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="ee58e-120">Turundusvideod, mis tõstavad toote üksikasjade lehtedel või turunduse lehtedel esile toote omadused</span><span class="sxs-lookup"><span data-stu-id="ee58e-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="ee58e-121">Videopleieri mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="ee58e-121">Video player module properties</span></span>

| <span data-ttu-id="ee58e-122">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="ee58e-122">Property name</span></span>         | <span data-ttu-id="ee58e-123">Väärtus</span><span class="sxs-lookup"><span data-stu-id="ee58e-123">Value</span></span>                               | <span data-ttu-id="ee58e-124">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ee58e-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="ee58e-125">Automaatesitus</span><span class="sxs-lookup"><span data-stu-id="ee58e-125">Auto play</span></span>             | <span data-ttu-id="ee58e-126">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-126">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-127">Kui väärtuseks on seatud **Tõene**, esitatakse video automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ee58e-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="ee58e-128">Vaigista</span><span class="sxs-lookup"><span data-stu-id="ee58e-128">Mute</span></span>                  | <span data-ttu-id="ee58e-129">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-129">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-130">Kui väärtuseks on seatud **Tõene**, on heli vaigistatud.</span><span class="sxs-lookup"><span data-stu-id="ee58e-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="ee58e-131">Selle pleieri vaikeväärtus on **Väär**.</span><span class="sxs-lookup"><span data-stu-id="ee58e-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="ee58e-132">Chrome’i brauseris on automaatselt esitatavad videod vaikimisi vaigistatud ja heli esitatakse ainult siis, kui kasutaja esitab videot käsitsi.</span><span class="sxs-lookup"><span data-stu-id="ee58e-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="ee58e-133">Silmus</span><span class="sxs-lookup"><span data-stu-id="ee58e-133">Loop</span></span>                  | <span data-ttu-id="ee58e-134">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-134">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-135">Kui väärtuseks on seatud **Tõene**, korratakse videot tsüklis.</span><span class="sxs-lookup"><span data-stu-id="ee58e-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="ee58e-136">Värbamisvahend</span><span class="sxs-lookup"><span data-stu-id="ee58e-136">Media</span></span>                 | <span data-ttu-id="ee58e-137">Videofaili tee ja nimi</span><span class="sxs-lookup"><span data-stu-id="ee58e-137">Video file path and name</span></span> | <span data-ttu-id="ee58e-138">Videopleieris esitatav videofail.</span><span class="sxs-lookup"><span data-stu-id="ee58e-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="ee58e-139">Täisekraanil esitamine</span><span class="sxs-lookup"><span data-stu-id="ee58e-139">Play fullscreen</span></span>       | <span data-ttu-id="ee58e-140">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-140">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-141">Kui väärtuseks on seatud **Tõene**, esitatakse video täisekraanil režiimis.</span><span class="sxs-lookup"><span data-stu-id="ee58e-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="ee58e-142">Lüliti Esita/Peata</span><span class="sxs-lookup"><span data-stu-id="ee58e-142">Play pause trigger</span></span>    | <span data-ttu-id="ee58e-143">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-143">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-144">Kui väärtuseks on seatud **Tõene**, kuvatakse videol esitamise/peatamise nupp.</span><span class="sxs-lookup"><span data-stu-id="ee58e-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="ee58e-145">Videopleieri juhtelemendid</span><span class="sxs-lookup"><span data-stu-id="ee58e-145">Video player controls</span></span> | <span data-ttu-id="ee58e-146">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-146">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-147">Kui väärtuseks on seatud **Tõene**, kuvatakse kõik vidopleieri juhtelemendid.</span><span class="sxs-lookup"><span data-stu-id="ee58e-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="ee58e-148">Need juhtelemendid hõlmavad esitamise ja peatamise nuppe, edenemise näidikut ja suletud pealdise suvandeid.</span><span class="sxs-lookup"><span data-stu-id="ee58e-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="ee58e-149">Peida plakati pilt</span><span class="sxs-lookup"><span data-stu-id="ee58e-149">Hide poster image</span></span>     | <span data-ttu-id="ee58e-150">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="ee58e-150">**True** or **False**</span></span>               | <span data-ttu-id="ee58e-151">Videol võib olla plakati raam.</span><span class="sxs-lookup"><span data-stu-id="ee58e-151">A video can have a poster frame.</span></span> <span data-ttu-id="ee58e-152">Kui selle atribuudi väärtuseks on seatud **Tõene**, on plakati raam peidetud.</span><span class="sxs-lookup"><span data-stu-id="ee58e-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="ee58e-153">Maski tase</span><span class="sxs-lookup"><span data-stu-id="ee58e-153">Mask level</span></span>            | <span data-ttu-id="ee58e-154">Number vahemikus **0** kuni **100**</span><span class="sxs-lookup"><span data-stu-id="ee58e-154">A number from **0** through **100**</span></span> | <span data-ttu-id="ee58e-155">Video laadi jaoks rakendatav mask.</span><span class="sxs-lookup"><span data-stu-id="ee58e-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="ee58e-156">Videopleieri mooduli lisamine lehele</span><span class="sxs-lookup"><span data-stu-id="ee58e-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="ee58e-157">Enne kui loote videopleieri mooduli, peate esmalt video meediateeki üles laadima.</span><span class="sxs-lookup"><span data-stu-id="ee58e-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="ee58e-158">Uuele lehele videopleieri mooduli lisamiseks ja vajalike atribuutide seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ee58e-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ee58e-159">Looge lehe mall nimega **videopleieri mall**.</span><span class="sxs-lookup"><span data-stu-id="ee58e-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="ee58e-160">Lisage vaikelehe pessa **Peamine** konteinermoodul.</span><span class="sxs-lookup"><span data-stu-id="ee58e-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="ee58e-161">Lisage konteinermoodulis videopleieri ja ümbrise videopleieri moodulid.</span><span class="sxs-lookup"><span data-stu-id="ee58e-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="ee58e-162">Viige lõpuni malli redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="ee58e-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="ee58e-163">Kasutage äsja loodud videopleieri malli, et luua leht, mille nimi on **videopleieri leht**.</span><span class="sxs-lookup"><span data-stu-id="ee58e-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="ee58e-164">Lisage uue lehe pessa **Peamine** videopleieri moodul.</span><span class="sxs-lookup"><span data-stu-id="ee58e-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="ee58e-165">Valige videopleieri mooduli paanil atribuudid **Video lisamine**.</span><span class="sxs-lookup"><span data-stu-id="ee58e-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="ee58e-166">Valige dialoogiaknas **Meedia valija** video ja seejärel valige **Laadi üles uus meedium**.</span><span class="sxs-lookup"><span data-stu-id="ee58e-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="ee58e-167">Salvestage ja kuvage lehe eelvaade.</span><span class="sxs-lookup"><span data-stu-id="ee58e-167">Save and preview the page.</span></span> <span data-ttu-id="ee58e-168">Peaksite nägema lehel videomoodulit.</span><span class="sxs-lookup"><span data-stu-id="ee58e-168">You should see the video module on the page.</span></span> <span data-ttu-id="ee58e-169">Saate muuta täiendavaid sätteid mooduli käitumise kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="ee58e-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="ee58e-170">Viige lõpuni lehe redigeerimine ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="ee58e-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee58e-171">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ee58e-171">Additional resources</span></span>

[<span data-ttu-id="ee58e-172">Alustuskomplekti ülevaade</span><span class="sxs-lookup"><span data-stu-id="ee58e-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ee58e-173">Reklaambänneri moodul</span><span class="sxs-lookup"><span data-stu-id="ee58e-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="ee58e-174">Karusellmoodul</span><span class="sxs-lookup"><span data-stu-id="ee58e-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="ee58e-175">Tekstiploki moodul</span><span class="sxs-lookup"><span data-stu-id="ee58e-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ee58e-176">Sisuploki moodul</span><span class="sxs-lookup"><span data-stu-id="ee58e-176">Content block module</span></span>](add-hero-module.md)
