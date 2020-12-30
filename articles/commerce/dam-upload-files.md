---
title: Failide üleslaadimine, v.a pildid ja videod
description: Selle teema all kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce saidiehitajas üles laadida binaarfaile, v.a pildid ja videod.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4acd3bec32cdfe627f6eb33dd5dc652f7cff74a8
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594208"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="3ca02-103">Failide üleslaadimine, v.a pildid ja videod</span><span class="sxs-lookup"><span data-stu-id="3ca02-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3ca02-104">Selle teema all kirjeldatakse, kuidas Microsoft Dynamics 365 Commerce saidiehitajas üles laadida faile, v.a pildid ja videod.</span><span class="sxs-lookup"><span data-stu-id="3ca02-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="3ca02-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3ca02-105">Overview</span></span>

<span data-ttu-id="3ca02-106">Kaubanduse saidiehitaja meediumiteek toetab binaarvarade, v.a pildid ja videod, üleslaadimist.</span><span class="sxs-lookup"><span data-stu-id="3ca02-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="3ca02-107">Näiteks võite soovida üles laadida Microsoft Excel, Microsoft Word, Microsoft PowerPointi faile või PDF-faile.</span><span class="sxs-lookup"><span data-stu-id="3ca02-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="3ca02-108">Toetatakse järgmisi dokumenditüüpe:</span><span class="sxs-lookup"><span data-stu-id="3ca02-108">The following document types are supported:</span></span>
- <span data-ttu-id="3ca02-109">7Z</span><span class="sxs-lookup"><span data-stu-id="3ca02-109">7Z</span></span>
- <span data-ttu-id="3ca02-110">AVI</span><span class="sxs-lookup"><span data-stu-id="3ca02-110">AVI</span></span>
- <span data-ttu-id="3ca02-111">CS</span><span class="sxs-lookup"><span data-stu-id="3ca02-111">CS</span></span>
- <span data-ttu-id="3ca02-112">CSS</span><span class="sxs-lookup"><span data-stu-id="3ca02-112">CSS</span></span>
- <span data-ttu-id="3ca02-113">DOC</span><span class="sxs-lookup"><span data-stu-id="3ca02-113">DOC</span></span>
- <span data-ttu-id="3ca02-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="3ca02-114">DOCX</span></span>
- <span data-ttu-id="3ca02-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="3ca02-115">EPUB</span></span>
- <span data-ttu-id="3ca02-116">GIF</span><span class="sxs-lookup"><span data-stu-id="3ca02-116">GIF</span></span>
- <span data-ttu-id="3ca02-117">INDD</span><span class="sxs-lookup"><span data-stu-id="3ca02-117">INDD</span></span>
- <span data-ttu-id="3ca02-118">JAR</span><span class="sxs-lookup"><span data-stu-id="3ca02-118">JAR</span></span>
- <span data-ttu-id="3ca02-119">JPG</span><span class="sxs-lookup"><span data-stu-id="3ca02-119">JPG</span></span>
- <span data-ttu-id="3ca02-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="3ca02-120">JPEG</span></span>
- <span data-ttu-id="3ca02-121">JS</span><span class="sxs-lookup"><span data-stu-id="3ca02-121">JS</span></span>
- <span data-ttu-id="3ca02-122">MP3</span><span class="sxs-lookup"><span data-stu-id="3ca02-122">MP3</span></span>
- <span data-ttu-id="3ca02-123">MP4</span><span class="sxs-lookup"><span data-stu-id="3ca02-123">MP4</span></span>
- <span data-ttu-id="3ca02-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="3ca02-124">MPEG</span></span>
- <span data-ttu-id="3ca02-125">MPG</span><span class="sxs-lookup"><span data-stu-id="3ca02-125">MPG</span></span>
- <span data-ttu-id="3ca02-126">ODP</span><span class="sxs-lookup"><span data-stu-id="3ca02-126">ODP</span></span>
- <span data-ttu-id="3ca02-127">ODS</span><span class="sxs-lookup"><span data-stu-id="3ca02-127">ODS</span></span>
- <span data-ttu-id="3ca02-128">ODT</span><span class="sxs-lookup"><span data-stu-id="3ca02-128">ODT</span></span>
- <span data-ttu-id="3ca02-129">PDF</span><span class="sxs-lookup"><span data-stu-id="3ca02-129">PDF</span></span>
- <span data-ttu-id="3ca02-130">PNG</span><span class="sxs-lookup"><span data-stu-id="3ca02-130">PNG</span></span>
- <span data-ttu-id="3ca02-131">PPT</span><span class="sxs-lookup"><span data-stu-id="3ca02-131">PPT</span></span>
- <span data-ttu-id="3ca02-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="3ca02-132">PPTX</span></span>
- <span data-ttu-id="3ca02-133">PS</span><span class="sxs-lookup"><span data-stu-id="3ca02-133">PS</span></span>
- <span data-ttu-id="3ca02-134">QXP</span><span class="sxs-lookup"><span data-stu-id="3ca02-134">QXP</span></span>
- <span data-ttu-id="3ca02-135">RAR</span><span class="sxs-lookup"><span data-stu-id="3ca02-135">RAR</span></span>
- <span data-ttu-id="3ca02-136">RTF</span><span class="sxs-lookup"><span data-stu-id="3ca02-136">RTF</span></span>
- <span data-ttu-id="3ca02-137">SVG</span><span class="sxs-lookup"><span data-stu-id="3ca02-137">SVG</span></span>
- <span data-ttu-id="3ca02-138">TAR</span><span class="sxs-lookup"><span data-stu-id="3ca02-138">TAR</span></span>
- <span data-ttu-id="3ca02-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="3ca02-139">TGZ</span></span>
- <span data-ttu-id="3ca02-140">TXT</span><span class="sxs-lookup"><span data-stu-id="3ca02-140">TXT</span></span>
- <span data-ttu-id="3ca02-141">WMV</span><span class="sxs-lookup"><span data-stu-id="3ca02-141">WMV</span></span>
- <span data-ttu-id="3ca02-142">XLS</span><span class="sxs-lookup"><span data-stu-id="3ca02-142">XLS</span></span>
- <span data-ttu-id="3ca02-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="3ca02-143">XLSX</span></span>
- <span data-ttu-id="3ca02-144">XML</span><span class="sxs-lookup"><span data-stu-id="3ca02-144">XML</span></span>
- <span data-ttu-id="3ca02-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="3ca02-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="3ca02-146">Laadi fail üles</span><span class="sxs-lookup"><span data-stu-id="3ca02-146">Upload a file</span></span>

<span data-ttu-id="3ca02-147">Faili üleslaadimiseks Kaubanduse saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3ca02-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="3ca02-148">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="3ca02-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="3ca02-149">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="3ca02-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="3ca02-150">Valige File Exploreris üks või mitu faili ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="3ca02-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="3ca02-151">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** pealkiri, kirjeldus ja vajaduse korral märksõnade metaandmed.</span><span class="sxs-lookup"><span data-stu-id="3ca02-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="3ca02-152">Failide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="3ca02-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="3ca02-153">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3ca02-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ca02-154">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3ca02-154">Additional resources</span></span>

[<span data-ttu-id="3ca02-155">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="3ca02-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="3ca02-156">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="3ca02-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="3ca02-157">Video üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="3ca02-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="3ca02-158">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="3ca02-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="3ca02-159">Pildi keskpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="3ca02-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="3ca02-160">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="3ca02-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
