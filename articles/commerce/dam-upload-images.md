---
title: Piltide üleslaadimine
description: Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.
author: psimolin
ms.date: 03/03/2020
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799225"
---
# <a name="upload-images"></a><span data-ttu-id="55618-103">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="55618-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="55618-104">Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.</span><span class="sxs-lookup"><span data-stu-id="55618-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="55618-105">Kaubanduse saidiehitaja meediumiteek võimaldab teil üles laadida pilte, kas üksikult või kaustades hulgakaupa.</span><span class="sxs-lookup"><span data-stu-id="55618-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="55618-106">Te peaksite alati üles laadima kõrgeima lahutuse ja kvaliteediga pildiversiooni, sest pildi suuruse muutmise komponent optimeerib pildi automaatselt erinevate vaateportide ja nende katkestuspunktide järgi.</span><span class="sxs-lookup"><span data-stu-id="55618-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="55618-107">Üleslaadimise ajal määratav pilditeave</span><span class="sxs-lookup"><span data-stu-id="55618-107">Image information specified during upload</span></span>

<span data-ttu-id="55618-108">Pildi üleslaadimisel saab määrata järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="55618-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="55618-109">**Pealkiri, Alt tekst, Kirjeldus, Märksõnad**: pildi või piltide metaandmed.</span><span class="sxs-lookup"><span data-stu-id="55618-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="55618-110">Pealkiri ja alt-tekst on nõutavad väärtused.</span><span class="sxs-lookup"><span data-stu-id="55618-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="55618-111">**Vali kategooria**:</span><span class="sxs-lookup"><span data-stu-id="55618-111">**Select category**:</span></span>
    - <span data-ttu-id="55618-112">**Puudub**: kasutatakse e-Kaubanduse jutustuse pildi või piltide jaoks.</span><span class="sxs-lookup"><span data-stu-id="55618-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="55618-113">**Toode, Kategooria, Klient, Töötaja, Kataloog**: kasutatakse Dynamics 365 Commerce omnikanali pildi või piltide jaoks.</span><span class="sxs-lookup"><span data-stu-id="55618-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="55618-114">**Avalda varad pärast üleslaadimist**: kui see ruut on märgitud, avaldatakse pilt või pildid kohe pärast üleslaadimist.</span><span class="sxs-lookup"><span data-stu-id="55618-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="55618-115">Pildivarad, mille kategooria on määratud, sildistatakse automaatselt selle kategooriaga märksõnana, mis aitab otsida kindla kategooria varasid.</span><span class="sxs-lookup"><span data-stu-id="55618-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="55618-116">Omnikanali piltide nimetustavad</span><span class="sxs-lookup"><span data-stu-id="55618-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="55618-117">Kui olete konfigureerinud Meediumiteegi omnikanali pildi taustaks, saate kasutada kujutise kategooriaid, et näidata, millisesse kategooriasse üleslaaditud pilt kuulub.</span><span class="sxs-lookup"><span data-stu-id="55618-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="55618-118">On olemas ka nimetava, mida tuleb järgida tagamaks, et pildid võetakse õigesti vastu teiste kanalite kaudu, nt kassas (POS).</span><span class="sxs-lookup"><span data-stu-id="55618-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="55618-119">Vaikimisi nimetava sõltub kategooriast:</span><span class="sxs-lookup"><span data-stu-id="55618-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="55618-120">Kataloogipildid peavad olema nimega "**/Catalogs/\{LanguageId\}/\{CatalogName\}. jpg**"</span><span class="sxs-lookup"><span data-stu-id="55618-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="55618-121">Kategooriapildid tuleb nimetada "**/Categories/\{CategoryName\}. png**"</span><span class="sxs-lookup"><span data-stu-id="55618-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="55618-122">Kliendipildid peavad olema nimega "**/Customers/\{CustomerNumber\}. jpg**"</span><span class="sxs-lookup"><span data-stu-id="55618-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="55618-123">Töötajapildid peavad olema nimega "**/Workers/\{WorkerNumber\}. jpg**"</span><span class="sxs-lookup"><span data-stu-id="55618-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="55618-124">Tootepildid tuleb nimetada "**/Products/\{ProductNumber\}_000_001. png**"</span><span class="sxs-lookup"><span data-stu-id="55618-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="55618-125">001 on pildijärjestus ja see võib olla 001, 002, 003, 004 või 005</span><span class="sxs-lookup"><span data-stu-id="55618-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="55618-126">Tootevariandi pildid tuleb nimetada "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="55618-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="55618-127">Näiteks: 93039 \^ \^ 2 \^ Black \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="55618-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="55618-128">Laadi pilt üles</span><span class="sxs-lookup"><span data-stu-id="55618-128">Upload an image</span></span>

<span data-ttu-id="55618-129">Pildi üleslaadimiseks saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="55618-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="55618-130">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="55618-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="55618-131">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="55618-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="55618-132">Fail Exploreri aknas navigeerige ja valige üleslaadimiseks üks või mitu pildifaili ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="55618-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="55618-133">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="55618-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="55618-134">Sisestage valikuline kirjeldus ja märksõnad ning valige soovi korral kategooria.</span><span class="sxs-lookup"><span data-stu-id="55618-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="55618-135">Piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="55618-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="55618-136">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="55618-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="55618-137">Pildikausta üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="55618-137">Upload a folder of images</span></span>

<span data-ttu-id="55618-138">Pildikausta üleslaadimiseks saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="55618-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="55618-139">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="55618-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="55618-140">Valige tegumiriba käsk **Laadi üles \> Laadi üles kaust**.</span><span class="sxs-lookup"><span data-stu-id="55618-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="55618-141">Fail Exploreri aknas navigeerige ja valige üleslaadimiseks kaust ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="55618-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="55618-142">Dialoogiaknas **Meediumiüksuse üleslaadimine** sisestage valikulised märksõnad ja valige soovi korral kategooria.</span><span class="sxs-lookup"><span data-stu-id="55618-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="55618-143">Kausta piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="55618-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="55618-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="55618-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55618-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="55618-145">Additional resources</span></span>

[<span data-ttu-id="55618-146">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="55618-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="55618-147">Video üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="55618-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="55618-148">Failide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="55618-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="55618-149">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="55618-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="55618-150">Pildi keskpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="55618-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="55618-151">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="55618-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
