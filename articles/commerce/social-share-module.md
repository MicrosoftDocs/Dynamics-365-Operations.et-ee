---
title: Suhtlussaidil jagamise moodul
description: See teema hõlmab suhtlussaidil jagamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 5052957a2f4e59791ef02c12bc2aef5ed36e95c7
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816933"
---
# <a name="social-share-module"></a><span data-ttu-id="49986-103">Suhtlussaidil jagamise moodul</span><span class="sxs-lookup"><span data-stu-id="49986-103">Social share module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="49986-104">See teema hõlmab suhtlussaidil jagamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="49986-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="49986-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="49986-105">Overview</span></span>

<span data-ttu-id="49986-106">Suhtlussaidil jagamise moodulid võimaldavad kasutajatel jagada e-kaubanduse saidi URL-e sotsiaalmeedias (nt Facebook, Twitter, Pinterest ja LinkedIn).</span><span class="sxs-lookup"><span data-stu-id="49986-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="49986-107">Saidi URL-e saab jagada ka meili teel.</span><span class="sxs-lookup"><span data-stu-id="49986-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="49986-108">Suhtlussaidil jagamise mooduleid kasutatakse tavaliselt toote üksikasjade lehtedel (PDP-d), et aidata kasutajatel toote teavet jagada.</span><span class="sxs-lookup"><span data-stu-id="49986-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="49986-109">Iga suhtlussaidil jagamise moodul on konteiner suhtlussaidil jagatava üksuse moodulitele.</span><span class="sxs-lookup"><span data-stu-id="49986-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="49986-110">Iga suhtlussaidil jagatava üksuse mooduit saab konfigureerida nii, et see osutaks konkreetsele sotsiaalmeedia saidile.</span><span class="sxs-lookup"><span data-stu-id="49986-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="49986-111">Integreerimist Facebooki, Twitteri, Pinteresti, LinkedIni ja meiliga toetatakse valmislahendusena.</span><span class="sxs-lookup"><span data-stu-id="49986-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="49986-112">Kui saidi kasutaja valib sotsiaalmeedia sümboli, käivitatakse vastava sotsiaalmeedia saidi jaoks HTML-i iFrame.</span><span class="sxs-lookup"><span data-stu-id="49986-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="49986-113">iFrame'is saab kasutaja sisse logida ja postitada vaadatud lehe sisu.</span><span class="sxs-lookup"><span data-stu-id="49986-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="49986-114">Iga sotsiaalmeedia platvorm võib küpsiseid jälgida, nii et see moodul nõuab saidi kasutajatelt küpsistega nõustumise teatise aktsepteerimist.</span><span class="sxs-lookup"><span data-stu-id="49986-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="49986-115">Kui küpsistega ei nõustuta, on moodul lehel peidetud.</span><span class="sxs-lookup"><span data-stu-id="49986-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="49986-116">Lisateavet vt teemast [Küpsise vastavus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="49986-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="49986-117">Järgmisel illustratsioonil on toodud näide toote üksikasjade lehel kasutatavast suhtlussaidil jagamise moodulist.</span><span class="sxs-lookup"><span data-stu-id="49986-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Suhtlussaidil jagamise mooduli näide](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="49986-119">Suhtlussaidil jagamise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="49986-119">Social share module properties</span></span>

| <span data-ttu-id="49986-120">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="49986-120">Property name</span></span>             | <span data-ttu-id="49986-121">Väärtus</span><span class="sxs-lookup"><span data-stu-id="49986-121">Value</span></span>                 | <span data-ttu-id="49986-122">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="49986-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="49986-123">Pealdis</span><span class="sxs-lookup"><span data-stu-id="49986-123">Caption</span></span>                  | <span data-ttu-id="49986-124">Tekst</span><span class="sxs-lookup"><span data-stu-id="49986-124">Text</span></span> | <span data-ttu-id="49986-125">See atribuut määrab mooduli pealdise.</span><span class="sxs-lookup"><span data-stu-id="49986-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="49986-126">Asetus</span><span class="sxs-lookup"><span data-stu-id="49986-126">Orientation</span></span> | <span data-ttu-id="49986-127">**Horisontaalne** või **Vertikaalne**</span><span class="sxs-lookup"><span data-stu-id="49986-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="49986-128">See atribuut määratleb suhtlussaidil olevate üksuste paigutuse.</span><span class="sxs-lookup"><span data-stu-id="49986-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="49986-129">Suhtlussaidil jagatava üksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="49986-129">Social share item module properties</span></span>
| <span data-ttu-id="49986-130">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="49986-130">Property name</span></span>             | <span data-ttu-id="49986-131">Väärtus</span><span class="sxs-lookup"><span data-stu-id="49986-131">Value</span></span>                 | <span data-ttu-id="49986-132">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="49986-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="49986-133">Suhtlusvõrgustik</span><span class="sxs-lookup"><span data-stu-id="49986-133">Social media</span></span>              | <span data-ttu-id="49986-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **meilirakendus**</span><span class="sxs-lookup"><span data-stu-id="49986-134">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="49986-135">Rippmenüü suhtlusvõrgustiku platvormide nimekirjaga.</span><span class="sxs-lookup"><span data-stu-id="49986-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="49986-136">Ikoon</span><span class="sxs-lookup"><span data-stu-id="49986-136">Icon</span></span> |<span data-ttu-id="49986-137">Pilt</span><span class="sxs-lookup"><span data-stu-id="49986-137">Image</span></span>    | <span data-ttu-id="49986-138">See on pilt, mida kuvatakse vastava suhtlusvõrgustiku korral.</span><span class="sxs-lookup"><span data-stu-id="49986-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="49986-139">Iga platvormi jaoks soovitatava pildi leiate suhtlusvõrgustiku platvormi SDK-st.</span><span class="sxs-lookup"><span data-stu-id="49986-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="49986-140">Suhtlussaidil jagamise mooduli lisamine ostukasti moodulile</span><span class="sxs-lookup"><span data-stu-id="49986-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="49986-141">Suhtlussaidil jagamise mooduli lisamiseks ostukasti moodulile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="49986-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="49986-142">Valige saidil Fabrikam **Lehed** ja seejärel tehke toote üksikasjade lehe avamiseks valik **Vaike-PDP**.</span><span class="sxs-lookup"><span data-stu-id="49986-142">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="49986-143">Valige pesas **Ostukast (nõutav)** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="49986-143">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="49986-144">Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussait** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="49986-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="49986-145">Valige pesas **Suhtlussait** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="49986-145">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="49986-146">Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussait** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="49986-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="49986-147">Tehke mooduli **Suhtlussait** atribuutide paani jaotises **Paigutus** valik **Horisontaalne**.</span><span class="sxs-lookup"><span data-stu-id="49986-147">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="49986-148">Lisage pealdis vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="49986-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="49986-149">Valige pesas **Suhtlussait** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="49986-149">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="49986-150">Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussaidil jagatav üksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="49986-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="49986-151">Tehke mooduli **Suhtlussaidil jagatav üksus** atribuutide paani jaotises **Suhtlussait** valik **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="49986-151">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="49986-152">Tehke mooduli **Suhtlussaidil jagatav üksus** atribuutide paani jaotises **Ikoon** valik **+ Lisa pilt**.</span><span class="sxs-lookup"><span data-stu-id="49986-152">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="49986-153">Valige dialoogiboksis **Meedia valija** rakenduse Facebook logo ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="49986-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="49986-154">Kui rakenduse Facebook logo ei kuvata, valige selle üleslaadimiseks käsk **Laadi üles uus meedium**.</span><span class="sxs-lookup"><span data-stu-id="49986-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="49986-155">Lisage ja konfigureerige täiendavaid mooduleid **Suhtlussaidil jagatav üksus** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="49986-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="49986-156">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="49986-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="49986-157">Leht kuvab suhtlussaidil jagamise mooduli.</span><span class="sxs-lookup"><span data-stu-id="49986-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="49986-158">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="49986-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49986-159">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="49986-159">Additional resources</span></span>

[<span data-ttu-id="49986-160">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="49986-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="49986-161">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="49986-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="49986-162">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="49986-162">Cookie compliance</span></span>](cookie-compliance.md)
