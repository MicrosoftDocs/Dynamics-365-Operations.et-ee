---
title: Videote üleslaadimine
description: Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a8cabcd3528308919697a9f2ecb2a81ad5acbe31
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000921"
---
# <a name="upload-videos"></a><span data-ttu-id="de18d-103">Videote üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="de18d-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de18d-104">Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.</span><span class="sxs-lookup"><span data-stu-id="de18d-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="de18d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="de18d-105">Overview</span></span>

<span data-ttu-id="de18d-106">Kaubanduse saidiehitaja meediumiteek võimaldab teil videoid üles laadida.</span><span class="sxs-lookup"><span data-stu-id="de18d-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="de18d-107">Te peaksite alati üles laadima kõrgeima lahutuse ja kvaliteediga videoversiooni, sest video muundatakse automaatselt sobivaks erinevatele vaateportidele ja nende katkestuspunktidele.</span><span class="sxs-lookup"><span data-stu-id="de18d-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="de18d-108">Üleslaadimise ajal määratav videoteave</span><span class="sxs-lookup"><span data-stu-id="de18d-108">Video information specified during upload</span></span>

<span data-ttu-id="de18d-109">Video üleslaadimisel saab määrata järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="de18d-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="de18d-110">**Pealkiri, Kirjeldus, Märksõnad**: video metaandmed.</span><span class="sxs-lookup"><span data-stu-id="de18d-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="de18d-111">**Loo automaatselt suletud pealdised**: määrab, kas video jaoks luuakse automaatselt suletud pealdised.</span><span class="sxs-lookup"><span data-stu-id="de18d-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="de18d-112">**Suletud pealdis**: määrab suletud pealdised, mida kasutada.</span><span class="sxs-lookup"><span data-stu-id="de18d-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="de18d-113">**Regulaarne heli**: määrab regulaarse heliriba, mida kasutada.</span><span class="sxs-lookup"><span data-stu-id="de18d-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="de18d-114">**Pisipilt**: määrab video pisipildi.</span><span class="sxs-lookup"><span data-stu-id="de18d-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="de18d-115">Kui see ei ole sätestatud, luuakse see automaatselt.</span><span class="sxs-lookup"><span data-stu-id="de18d-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="de18d-116">**Kirjeldusheli**: määrab kirjeldusheliriba, mida kasutada.</span><span class="sxs-lookup"><span data-stu-id="de18d-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="de18d-117">Video üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="de18d-117">Upload a video</span></span>

<span data-ttu-id="de18d-118">Video üleslaadimiseks saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="de18d-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="de18d-119">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="de18d-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="de18d-120">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="de18d-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="de18d-121">Fail Exploreri aknas navigeerige ja valige üleslaadimiseks üks või mitu videofaili ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="de18d-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="de18d-122">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="de18d-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="de18d-123">Sisestage valikuline kirjeldus ja märksõnad ning valige soovi korral kategooria.</span><span class="sxs-lookup"><span data-stu-id="de18d-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="de18d-124">Piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**</span><span class="sxs-lookup"><span data-stu-id="de18d-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="de18d-125">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="de18d-125">Select **OK**.</span></span>

<span data-ttu-id="de18d-126">Kui sisestate mitut tüüpi varad üheaegselt (nt pildid ja videod), saate määrata dialoogiboksis **Meediumiüksuse üleslaadimine** märksõnad selle kohta, kas failid tuleb kohe pärast üleslaadimist avaldada ja kas videofailide jaoks tuleks automaatselt luua suletud pealdised.</span><span class="sxs-lookup"><span data-stu-id="de18d-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="de18d-127">Kõigil varadel on samad märksõnad.</span><span class="sxs-lookup"><span data-stu-id="de18d-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de18d-128">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="de18d-128">Additional resources</span></span>

[<span data-ttu-id="de18d-129">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="de18d-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="de18d-130">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="de18d-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="de18d-131">Failide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="de18d-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="de18d-132">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="de18d-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="de18d-133">Pildi keskpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="de18d-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="de18d-134">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="de18d-134">Upload and serve static files</span></span>](upload-serve-static-files.md)
