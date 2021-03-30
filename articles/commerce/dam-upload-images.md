---
title: Piltide üleslaadimine
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
ms.openlocfilehash: 51571ce221714598b2e2d39c76cb69dcb57cc52b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213790"
---
# <a name="upload-images"></a><span data-ttu-id="80265-103">Piltide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="80265-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80265-104">Selle teema all kirjeldatakse, kuidas üles laadida videosid rakenduse Microsoft Dynamics 365 Commerce saidiehituses.</span><span class="sxs-lookup"><span data-stu-id="80265-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="80265-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="80265-105">Overview</span></span>

<span data-ttu-id="80265-106">Kaubanduse saidiehitaja meediumiteek võimaldab teil üles laadida pilte, kas üksikult või kaustades hulgakaupa.</span><span class="sxs-lookup"><span data-stu-id="80265-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="80265-107">Te peaksite alati üles laadima kõrgeima lahutuse ja kvaliteediga pildiversiooni, sest pildi suuruse muutmise komponent optimeerib pildi automaatselt erinevate vaateportide ja nende katkestuspunktide järgi.</span><span class="sxs-lookup"><span data-stu-id="80265-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="80265-108">Üleslaadimise ajal määratav pilditeave</span><span class="sxs-lookup"><span data-stu-id="80265-108">Image information specified during upload</span></span>

<span data-ttu-id="80265-109">Pildi üleslaadimisel saab määrata järgmise teabe.</span><span class="sxs-lookup"><span data-stu-id="80265-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="80265-110">**Pealkiri, Alt tekst, Kirjeldus, Märksõnad**: pildi või piltide metaandmed.</span><span class="sxs-lookup"><span data-stu-id="80265-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="80265-111">Pealkiri ja alt-tekst on nõutavad väärtused.</span><span class="sxs-lookup"><span data-stu-id="80265-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="80265-112">**Vali kategooria**:</span><span class="sxs-lookup"><span data-stu-id="80265-112">**Select category**:</span></span>
    - <span data-ttu-id="80265-113">**Puudub**: kasutatakse e-Kaubanduse jutustuse pildi või piltide jaoks.</span><span class="sxs-lookup"><span data-stu-id="80265-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="80265-114">**Toode, Kategooria, Klient, Töötaja, Kataloog**: kasutatakse Dynamics 365 Commerce omnikanali pildi või piltide jaoks.</span><span class="sxs-lookup"><span data-stu-id="80265-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="80265-115">**Avalda varad pärast üleslaadimist**: kui see ruut on märgitud, avaldatakse pilt või pildid kohe pärast üleslaadimist.</span><span class="sxs-lookup"><span data-stu-id="80265-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="80265-116">Pildivarad, mille kategooria on määratud, sildistatakse automaatselt selle kategooriaga märksõnana, mis aitab otsida kindla kategooria varasid.</span><span class="sxs-lookup"><span data-stu-id="80265-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="80265-117">Omnikanali piltide nimetustavad</span><span class="sxs-lookup"><span data-stu-id="80265-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="80265-118">Kui olete konfigureerinud Meediumiteegi omnikanali pildi taustaks, saate kasutada kujutise kategooriaid, et näidata, millisesse kategooriasse üleslaaditud pilt kuulub.</span><span class="sxs-lookup"><span data-stu-id="80265-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="80265-119">On olemas ka nimetava, mida tuleb järgida tagamaks, et pildid võetakse õigesti vastu teiste kanalite kaudu, nt kassas (POS).</span><span class="sxs-lookup"><span data-stu-id="80265-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="80265-120">Vaikimisi nimetava sõltub kategooriast:</span><span class="sxs-lookup"><span data-stu-id="80265-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="80265-121">Kataloogipildid peavad olema nimega "**/Catalogs/\{LanguageId\}/\{CatalogName\}. jpg**"</span><span class="sxs-lookup"><span data-stu-id="80265-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="80265-122">Kategooriapildid tuleb nimetada "**/Categories/\{CategoryName\}. png**"</span><span class="sxs-lookup"><span data-stu-id="80265-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="80265-123">Kliendipildid peavad olema nimega "**/Customers/\{CustomerNumber\}. jpg**"</span><span class="sxs-lookup"><span data-stu-id="80265-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="80265-124">Töötajapildid peavad olema nimega "**/Workers/\{WorkerNumber\}. jpg**"</span><span class="sxs-lookup"><span data-stu-id="80265-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="80265-125">Tootepildid tuleb nimetada "**/Products/\{ProductNumber\}_000_001. png**"</span><span class="sxs-lookup"><span data-stu-id="80265-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="80265-126">001 on pildijärjestus ja see võib olla 001, 002, 003, 004 või 005</span><span class="sxs-lookup"><span data-stu-id="80265-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="80265-127">Tootevariandi pildid tuleb nimetada "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span><span class="sxs-lookup"><span data-stu-id="80265-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="80265-128">Laadi pilt üles</span><span class="sxs-lookup"><span data-stu-id="80265-128">Upload an image</span></span>

<span data-ttu-id="80265-129">Pildi üleslaadimiseks saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="80265-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="80265-130">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="80265-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="80265-131">Valige tegumiriba käsk **Laadi üles \> Laadi üles meediumiüksused**.</span><span class="sxs-lookup"><span data-stu-id="80265-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="80265-132">Fail Exploreri aknas navigeerige ja valige üleslaadimiseks üks või mitu pildifaili ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="80265-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="80265-133">Sisestage dialoogiboksis **Meediumiüksuse üleslaadimine** nõutav pealkiri ja alt-tekst.</span><span class="sxs-lookup"><span data-stu-id="80265-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="80265-134">Sisestage valikuline kirjeldus ja märksõnad ning valige soovi korral kategooria.</span><span class="sxs-lookup"><span data-stu-id="80265-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="80265-135">Piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="80265-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="80265-136">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="80265-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="80265-137">Pildikausta üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="80265-137">Upload a folder of images</span></span>

<span data-ttu-id="80265-138">Pildikausta üleslaadimiseks saidiehitajasse toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="80265-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="80265-139">Valige vasakpoolsel navigeerimispaanil suvand **Meediumiteek**.</span><span class="sxs-lookup"><span data-stu-id="80265-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="80265-140">Valige tegumiriba käsk **Laadi üles \> Laadi üles kaust**.</span><span class="sxs-lookup"><span data-stu-id="80265-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="80265-141">Fail Exploreri aknas navigeerige ja valige üleslaadimiseks kaust ja seejärel valige **Ava**.</span><span class="sxs-lookup"><span data-stu-id="80265-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="80265-142">Dialoogiaknas **Meediumiüksuse üleslaadimine** sisestage valikulised märksõnad ja valige soovi korral kategooria.</span><span class="sxs-lookup"><span data-stu-id="80265-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="80265-143">Kausta piltide avaldamiseks kohe pärast üleslaadimist märkige ruut **Avalda meediumiüksused üksused pärast üleslaadimist**.</span><span class="sxs-lookup"><span data-stu-id="80265-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="80265-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="80265-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80265-145">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="80265-145">Additional resources</span></span>

[<span data-ttu-id="80265-146">Digitaalse varahalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="80265-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="80265-147">Video üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="80265-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="80265-148">Failide üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="80265-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="80265-149">Piltide kärpimine</span><span class="sxs-lookup"><span data-stu-id="80265-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="80265-150">Pildi keskpunktide kohandamine</span><span class="sxs-lookup"><span data-stu-id="80265-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="80265-151">Staatiliste failide üleslaadimine ja kasutamine</span><span class="sxs-lookup"><span data-stu-id="80265-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]