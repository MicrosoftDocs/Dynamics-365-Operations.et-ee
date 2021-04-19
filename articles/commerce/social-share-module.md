---
title: Suhtlussaidil jagamise moodul
description: See teema hõlmab suhtlussaidil jagamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: c34410a8c817de9fed350bf2cd2dd918a37c230f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795353"
---
# <a name="social-share-module"></a><span data-ttu-id="0aa80-103">Sotsiaalmeedias jagamise moodul</span><span class="sxs-lookup"><span data-stu-id="0aa80-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0aa80-104">See teema hõlmab suhtlussaidil jagamise mooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="0aa80-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0aa80-105">Suhtlussaidil jagamise moodulid võimaldavad kasutajatel jagada e-kaubanduse saidi URL-e sotsiaalmeedias (nt Facebook, Twitter, Pinterest ja LinkedIn).</span><span class="sxs-lookup"><span data-stu-id="0aa80-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="0aa80-106">Saidi URL-e saab jagada ka meili teel.</span><span class="sxs-lookup"><span data-stu-id="0aa80-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="0aa80-107">Suhtlussaidil jagamise mooduleid kasutatakse tavaliselt toote üksikasjade lehtedel (PDP-d), et aidata kasutajatel toote teavet jagada.</span><span class="sxs-lookup"><span data-stu-id="0aa80-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="0aa80-108">Iga suhtlussaidil jagamise moodul on konteiner suhtlussaidil jagatava üksuse moodulitele.</span><span class="sxs-lookup"><span data-stu-id="0aa80-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="0aa80-109">Iga suhtlussaidil jagatava üksuse mooduit saab konfigureerida nii, et see osutaks konkreetsele sotsiaalmeedia saidile.</span><span class="sxs-lookup"><span data-stu-id="0aa80-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="0aa80-110">Integreerimist Facebooki, Twitteri, Pinteresti, LinkedIni ja meiliga toetatakse valmislahendusena.</span><span class="sxs-lookup"><span data-stu-id="0aa80-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="0aa80-111">Kui saidi kasutaja valib sotsiaalmeedia sümboli, käivitatakse vastava sotsiaalmeedia saidi jaoks HTML-i iFrame.</span><span class="sxs-lookup"><span data-stu-id="0aa80-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="0aa80-112">iFrame'is saab kasutaja sisse logida ja postitada vaadatud lehe sisu.</span><span class="sxs-lookup"><span data-stu-id="0aa80-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="0aa80-113">Iga sotsiaalmeedia platvorm võib küpsiseid jälgida, nii et see moodul nõuab saidi kasutajatelt küpsistega nõustumise teatise aktsepteerimist.</span><span class="sxs-lookup"><span data-stu-id="0aa80-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="0aa80-114">Kui küpsistega ei nõustuta, on moodul lehel peidetud.</span><span class="sxs-lookup"><span data-stu-id="0aa80-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="0aa80-115">Lisateavet vt teemast [Küpsise vastavus](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="0aa80-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="0aa80-116">Järgmisel illustratsioonil on toodud näide toote üksikasjade lehel kasutatavast suhtlussaidil jagamise moodulist.</span><span class="sxs-lookup"><span data-stu-id="0aa80-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Suhtlussaidil jagamise mooduli näide](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="0aa80-118">Suhtlussaidil jagamise mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="0aa80-118">Social share module properties</span></span>

| <span data-ttu-id="0aa80-119">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="0aa80-119">Property name</span></span>             | <span data-ttu-id="0aa80-120">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0aa80-120">Value</span></span>                 | <span data-ttu-id="0aa80-121">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0aa80-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0aa80-122">Pealdis</span><span class="sxs-lookup"><span data-stu-id="0aa80-122">Caption</span></span>                  | <span data-ttu-id="0aa80-123">Tekst</span><span class="sxs-lookup"><span data-stu-id="0aa80-123">Text</span></span> | <span data-ttu-id="0aa80-124">See atribuut määrab mooduli pealdise.</span><span class="sxs-lookup"><span data-stu-id="0aa80-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="0aa80-125">Asetus</span><span class="sxs-lookup"><span data-stu-id="0aa80-125">Orientation</span></span> | <span data-ttu-id="0aa80-126">**Horisontaalne** või **Vertikaalne**</span><span class="sxs-lookup"><span data-stu-id="0aa80-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="0aa80-127">See atribuut määratleb suhtlussaidil olevate üksuste paigutuse.</span><span class="sxs-lookup"><span data-stu-id="0aa80-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="0aa80-128">Suhtlussaidil jagatava üksuse mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="0aa80-128">Social share item module properties</span></span>
| <span data-ttu-id="0aa80-129">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="0aa80-129">Property name</span></span>             | <span data-ttu-id="0aa80-130">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0aa80-130">Value</span></span>                 | <span data-ttu-id="0aa80-131">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0aa80-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="0aa80-132">Suhtlusvõrgustik</span><span class="sxs-lookup"><span data-stu-id="0aa80-132">Social media</span></span>              | <span data-ttu-id="0aa80-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **meilirakendus**</span><span class="sxs-lookup"><span data-stu-id="0aa80-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="0aa80-134">Rippmenüü suhtlusvõrgustiku platvormide nimekirjaga.</span><span class="sxs-lookup"><span data-stu-id="0aa80-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="0aa80-135">Ikoon</span><span class="sxs-lookup"><span data-stu-id="0aa80-135">Icon</span></span> |<span data-ttu-id="0aa80-136">Pilt</span><span class="sxs-lookup"><span data-stu-id="0aa80-136">Image</span></span>    | <span data-ttu-id="0aa80-137">See on pilt, mida kuvatakse vastava suhtlusvõrgustiku korral.</span><span class="sxs-lookup"><span data-stu-id="0aa80-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="0aa80-138">Iga platvormi jaoks soovitatava pildi leiate suhtlusvõrgustiku platvormi SDK-st.</span><span class="sxs-lookup"><span data-stu-id="0aa80-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="0aa80-139">Suhtlussaidil jagamise mooduli lisamine ostukasti moodulile</span><span class="sxs-lookup"><span data-stu-id="0aa80-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="0aa80-140">Suhtlussaidil jagamise mooduli lisamiseks ostukasti moodulile tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="0aa80-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="0aa80-141">Valige saidil Fabrikam **Lehed** ja seejärel tehke toote üksikasjade lehe avamiseks valik **Vaike-PDP**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="0aa80-142">Valige pesas **Ostukast (nõutav)** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0aa80-143">Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussait** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0aa80-144">Valige pesas **Suhtlussait** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0aa80-145">Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussait** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0aa80-146">Tehke mooduli **Suhtlussait** atribuutide paani jaotises **Paigutus** valik **Horisontaalne**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="0aa80-147">Lisage pealdis vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="0aa80-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="0aa80-148">Valige pesas **Suhtlussait** kolmikpunkt (**…**) ja seejärel käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0aa80-149">Valige dialoogiboksis **Lisa moodul** moodul **Suhtlussaidil jagatav üksus** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0aa80-150">Tehke mooduli **Suhtlussaidil jagatav üksus** atribuutide paani jaotises **Suhtlussait** valik **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="0aa80-151">Tehke mooduli **Suhtlussaidil jagatav üksus** atribuutide paani jaotises **Ikoon** valik **+ Lisa pilt**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="0aa80-152">Valige dialoogiboksis **Meedia valija** rakenduse Facebook logo ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="0aa80-153">Kui rakenduse Facebook logo ei kuvata, valige selle üleslaadimiseks käsk **Laadi üles uus meedium**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="0aa80-154">Lisage ja konfigureerige täiendavaid mooduleid **Suhtlussaidil jagatav üksus** vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="0aa80-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="0aa80-155">Valige **Salvesta** ja seejärel lehe eelvaate kuvamiseks **Eelvaade**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="0aa80-156">Leht kuvab suhtlussaidil jagamise mooduli.</span><span class="sxs-lookup"><span data-stu-id="0aa80-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="0aa80-157">Valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="0aa80-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0aa80-158">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0aa80-158">Additional resources</span></span>

[<span data-ttu-id="0aa80-159">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="0aa80-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0aa80-160">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="0aa80-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0aa80-161">Küpsise vastavus</span><span class="sxs-lookup"><span data-stu-id="0aa80-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]