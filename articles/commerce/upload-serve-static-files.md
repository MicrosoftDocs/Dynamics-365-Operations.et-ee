---
title: Staatiliste failide üleslaadimine ja kasutamine
description: See teema kirjeldab, kuidas laadida staatilist faili Microsoft Dynamics 365 Commerce saidiloojasse ja kuidas luua kohandatud URL-i ja faili nime, mida saab kasutada faili taotlemiseks.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
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
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 981bbf03480abfd812b4020173b7acfdad0fef14
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594958"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="bdb49-103">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="bdb49-103">Upload and serve static files</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="bdb49-104">See teema kirjeldab, kuidas laadida staatilist faili Microsoft Dynamics 365 Commerce saidiloojasse ja kuidas luua kohandatud URL-i ja faili nime, mida saab kasutada faili taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="bdb49-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="bdb49-105">Mõned kolmanda osapoole konnektorid nõuavad, et fail majutatakse ja serveeritakse e-kaubanduse saidilt.</span><span class="sxs-lookup"><span data-stu-id="bdb49-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="bdb49-106">Need konnektorid eeldavad, et fail tagastatakse taotlustega kindlale tagasihelistamise URL-i teele ja failinimele.</span><span class="sxs-lookup"><span data-stu-id="bdb49-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="bdb49-107">Seetõttu selgitab see teema, kuidas üles laadida ja kasutada staatilist faili, millel on Dynamics 365 Commerce e-kaubanduse saidil kasutaja poolt määratletavad URL ja failinimi.</span><span class="sxs-lookup"><span data-stu-id="bdb49-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="bdb49-108">Looge saidi URL, mis tagastab staatilise faili.</span><span class="sxs-lookup"><span data-stu-id="bdb49-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="bdb49-109">Saidi URL-i loomiseks, mis tagastaks staatilise faili e-kaubanduse saidiloojas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="bdb49-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="bdb49-110">Minge oma saidi meediateeki ja laadige üles fail, mis tuleks kätte toimetada teie määratud URL-i taotlustega.</span><span class="sxs-lookup"><span data-stu-id="bdb49-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="bdb49-111">Kui olete faili juba üles laadinud, võite selle sammu vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="bdb49-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="bdb49-112">Avage oma saidi **URL-id**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="bdb49-113">Valige **uus \> Uus URL**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="bdb49-114">**Uus URL** dialoogiaknas valige **Meediateegi vara**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="bdb49-115">Sisestage **URL-i tee** väljale URL-i tee.</span><span class="sxs-lookup"><span data-stu-id="bdb49-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="bdb49-116">Kaasake teele faili nimi.</span><span class="sxs-lookup"><span data-stu-id="bdb49-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="bdb49-117">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-117">Select **Next**.</span></span> <span data-ttu-id="bdb49-118">Avatakse meediateek ja kuvatakse kõik üleslaetud **dokumendi** tüübi meediumid.</span><span class="sxs-lookup"><span data-stu-id="bdb49-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="bdb49-119">Valige fail, mis peaks olema saadaval sammus 5 määratletud URL-i taotluste jaoks.</span><span class="sxs-lookup"><span data-stu-id="bdb49-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="bdb49-120">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-120">Select **Save**.</span></span>

<span data-ttu-id="bdb49-121">Sel hetkel on teie poolt loodud URL mustandi olekus.</span><span class="sxs-lookup"><span data-stu-id="bdb49-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="bdb49-122">Faili, millele URL osutab, ei tagastata enne, kui olete URL-i avaldanud.</span><span class="sxs-lookup"><span data-stu-id="bdb49-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="bdb49-123">Enne URL-i avaldamist saate tõendada, et see tagastab õiged andmed.</span><span class="sxs-lookup"><span data-stu-id="bdb49-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="bdb49-124">Tõendage ja avaldage URL</span><span class="sxs-lookup"><span data-stu-id="bdb49-124">Validate and publish a URL</span></span>

<span data-ttu-id="bdb49-125">URL-i valideerimiseks enne selle avaldamist tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="bdb49-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="bdb49-126">Avage oma saidi **URL-id** ja valige eelvaateks URL.</span><span class="sxs-lookup"><span data-stu-id="bdb49-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="bdb49-127">Parempoolsel atribuutide paanil valige **Redigeeri** nupu all olev õige URL-i link.</span><span class="sxs-lookup"><span data-stu-id="bdb49-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="bdb49-128">Avatakse uus brauseri aken ja te peaksite saama 404 tõrke.</span><span class="sxs-lookup"><span data-stu-id="bdb49-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="bdb49-129">Lisage see **?preview=inprogress** päringu string URL-iks (nt `https://yoursite.com/callback.html?preview=inprogress`) ja laadige leht uuesti.</span><span class="sxs-lookup"><span data-stu-id="bdb49-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="bdb49-130">Mediateeki üleslaetud fail tuleks vastuseks tagastada.</span><span class="sxs-lookup"><span data-stu-id="bdb49-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="bdb49-131">Pärast URL-i kontrollimist saate selle avaldada.</span><span class="sxs-lookup"><span data-stu-id="bdb49-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="bdb49-132">Avage oma saidi **URL-id** ja valige URL.</span><span class="sxs-lookup"><span data-stu-id="bdb49-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="bdb49-133">Valige käsuribal **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="bdb49-134">Värskendage faili, millele URL osutab</span><span class="sxs-lookup"><span data-stu-id="bdb49-134">Update the file that a URL points to</span></span>

<span data-ttu-id="bdb49-135">Pärast URL-i avaldamist saate seda värskendada nii, et see osutab mõnele muule failile.</span><span class="sxs-lookup"><span data-stu-id="bdb49-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="bdb49-136">Teise võimalusena saate URL-i värskendada nii, et see osutab erinevale ressursitüübile, nagu on kirjeldatud järgmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="bdb49-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="bdb49-137">Näiteks saate suunata URL-i sisemisele lehele või ümber suunata.</span><span class="sxs-lookup"><span data-stu-id="bdb49-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="bdb49-138">URL-i osutatud faili värskendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="bdb49-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="bdb49-139">Avage oma saidi **URL-id** ja valige uuendamiseks URL.</span><span class="sxs-lookup"><span data-stu-id="bdb49-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="bdb49-140">Parempoolsel atribuutide paanil valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="bdb49-141">Jaotises **URL-i määramine** valige **Samm 2** aken ja seejärel valige uus meediateegist dokument.</span><span class="sxs-lookup"><span data-stu-id="bdb49-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="bdb49-142">Valige **Rakendamine**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="bdb49-143">Värskendage varatüüpi, millele URL osutab</span><span class="sxs-lookup"><span data-stu-id="bdb49-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="bdb49-144">Samuti saate värskendada URL-i nii, et see osutab erinevat tüüpi varale (ressurss), nagu sisemine leht või ümbersuunamine.</span><span class="sxs-lookup"><span data-stu-id="bdb49-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="bdb49-145">URL-i osutatud ressursitüübi värskendamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="bdb49-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="bdb49-146">Avage oma saidi **URL-id** ja valige uuendamiseks URL.</span><span class="sxs-lookup"><span data-stu-id="bdb49-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="bdb49-147">Parempoolsel atribuutide paanil valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="bdb49-148">Valige **URL-i määramine** jaotises **Samm 1** ja valige muu ressursitüüp.</span><span class="sxs-lookup"><span data-stu-id="bdb49-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="bdb49-149">Valige **Samm 2** aken ja seejärel valige uus ressurss.</span><span class="sxs-lookup"><span data-stu-id="bdb49-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="bdb49-150">Valige **Rakendamine**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="bdb49-151">Muuda URL-i teed</span><span class="sxs-lookup"><span data-stu-id="bdb49-151">Change the URL path</span></span>

<span data-ttu-id="bdb49-152">Pärast URL-i loomist ei saa selle teed muuta.</span><span class="sxs-lookup"><span data-stu-id="bdb49-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="bdb49-153">Kui peate muutma faili või mõnda muud tüüpi ressurssi sisaldavat URL-i teed, peate looma uue URL-i, vastendama selle olemasoleva faili või muu ressursiga ning seejärel tühistama ja kustutama vana URL-i.</span><span class="sxs-lookup"><span data-stu-id="bdb49-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="bdb49-154">URL-i tee muutmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="bdb49-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="bdb49-155">Uue URL-i loomiseks ja selle olemasolevale failile või muule ressursile vastendamiseks järgige juhiseid selles teemas olevaid varasemaid juhised [Saidi URL-i loomine, mis tagastab staatilise faili](#create-a-site-url-that-returns-a-static-file).</span><span class="sxs-lookup"><span data-stu-id="bdb49-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="bdb49-156">Valige uus URL ja valige käsk **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="bdb49-157">Uus URL on avaldatud.</span><span class="sxs-lookup"><span data-stu-id="bdb49-157">The new URL is published.</span></span>
1. <span data-ttu-id="bdb49-158">Vana URL-i avaldamise tühistamiseks valige see ja seejärel valige käsuribal käsk **Tühista avaldamine**.</span><span class="sxs-lookup"><span data-stu-id="bdb49-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="bdb49-159">Soovi korral võite nüüd vana URL-i kustutada.</span><span class="sxs-lookup"><span data-stu-id="bdb49-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdb49-160">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="bdb49-160">Additional resources</span></span>

[<span data-ttu-id="bdb49-161">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="bdb49-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="bdb49-162">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="bdb49-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="bdb49-163">Videote üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="bdb49-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="bdb49-164">Failide üleslaadimine, v. a pildid ja videod</span><span class="sxs-lookup"><span data-stu-id="bdb49-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="bdb49-165">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="bdb49-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="bdb49-166">Pildi keskpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="bdb49-166">Customize image focal points</span></span>](dam-custom-focal-point.md)
