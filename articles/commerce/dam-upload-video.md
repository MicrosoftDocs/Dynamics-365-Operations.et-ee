---
title: Videote üleslaadimine
description: Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.
author: psimolin
ms.date: 06/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: e3579b54c58898b79c84406480a3b58f541c4621
ms.sourcegitcommit: 257437a57e146496a49782bc8aad179c92fbf6e8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/11/2021
ms.locfileid: "6224534"
---
# <a name="upload-videos"></a><span data-ttu-id="8a220-103">Videote üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="8a220-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8a220-104">Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.</span><span class="sxs-lookup"><span data-stu-id="8a220-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="8a220-105">Kaubanduse saidiehitaja meediumiteek võimaldab teil videoid üles laadida.</span><span class="sxs-lookup"><span data-stu-id="8a220-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="8a220-106">Te peaksite alati üles laadima kõrgeima lahutuse ja kvaliteediga videoversiooni, sest video muundatakse automaatselt sobivaks erinevatele vaateportidele ja nende katkestuspunktidele.</span><span class="sxs-lookup"><span data-stu-id="8a220-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="8a220-107">Üleslaadimise ajal määratav videoteave</span><span class="sxs-lookup"><span data-stu-id="8a220-107">Video information specified during upload</span></span>

<span data-ttu-id="8a220-108">Video üleslaadimisel saab määrata järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="8a220-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="8a220-109">**Pealkiri, Kirjeldus, Märksõnad**: video metaandmed.</span><span class="sxs-lookup"><span data-stu-id="8a220-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="8a220-110">**Loo automaatselt suletud pealdised**: määrab, kas video jaoks luuakse automaatselt suletud pealdised (toetatud ainult inglise keeles).</span><span class="sxs-lookup"><span data-stu-id="8a220-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video (only English language is supported).</span></span> 
- <span data-ttu-id="8a220-111">**Suletud pealdis**: määrab suletud pealdised, mida kasutada.</span><span class="sxs-lookup"><span data-stu-id="8a220-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="8a220-112">**Regulaarne heli**: määrab regulaarse heliriba, mida kasutada.</span><span class="sxs-lookup"><span data-stu-id="8a220-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="8a220-113">**Pisipilt**: määrab video pisipildi.</span><span class="sxs-lookup"><span data-stu-id="8a220-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="8a220-114">Kui see ei ole sätestatud, luuakse see automaatselt.</span><span class="sxs-lookup"><span data-stu-id="8a220-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="8a220-115">**Kirjeldusheli**: määrab kirjeldusheliriba, mida kasutada.</span><span class="sxs-lookup"><span data-stu-id="8a220-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="8a220-116">Video üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="8a220-116">Upload a video</span></span>

<span data-ttu-id="8a220-117">Video üleslaadimiseks saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="8a220-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="8a220-118">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="8a220-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="8a220-119">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="8a220-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="8a220-120">Fail Exploreri aknas navigeerige ja valige üleslaadimiseks üks või mitu videofaili ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="8a220-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="8a220-121">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="8a220-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="8a220-122">Sisestage valikuline kirjeldus ja märksõnad ning valige soovi korral kategooria.</span><span class="sxs-lookup"><span data-stu-id="8a220-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="8a220-123">Piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**</span><span class="sxs-lookup"><span data-stu-id="8a220-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="8a220-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a220-124">Select **OK**.</span></span>

<span data-ttu-id="8a220-125">Kui sisestate mitut tüüpi varad üheaegselt (nt pildid ja videod), saate määrata dialoogiboksis **Meediumiüksuse üleslaadimine** märksõnad selle kohta, kas failid tuleb kohe pärast üleslaadimist avaldada ja kas videofailide jaoks tuleks automaatselt luua suletud pealdised.</span><span class="sxs-lookup"><span data-stu-id="8a220-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="8a220-126">Kõigil varadel on samad märksõnad.</span><span class="sxs-lookup"><span data-stu-id="8a220-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8a220-127">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8a220-127">Additional resources</span></span>

[<span data-ttu-id="8a220-128">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="8a220-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="8a220-129">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="8a220-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="8a220-130">Failide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="8a220-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="8a220-131">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="8a220-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="8a220-132">Pildi keskpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="8a220-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="8a220-133">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="8a220-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
