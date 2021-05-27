---
title: Kaardimoodul
description: See teema hõlmab kaardimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 659211f3a74c38389f991cd2385366d175b0c7c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020255"
---
# <a name="map-module"></a><span data-ttu-id="8dd43-103">Kaardimoodul</span><span class="sxs-lookup"><span data-stu-id="8dd43-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="8dd43-104">See teema hõlmab kaardimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="8dd43-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8dd43-105">Kaardimoodul kuvab kaupluste asukohad interaktiivsel kaardil, mis renderdatakse [Bing Maps V8 Web Controli](/bingmaps/v8-web-control/) abil.</span><span class="sxs-lookup"><span data-stu-id="8dd43-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="8dd43-106">Vajalik on Bing Maps kaartide API võti ja see tuleb lisada jagatud parameetrite lehele rakenduses Commerce peakontorid.</span><span class="sxs-lookup"><span data-stu-id="8dd43-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="8dd43-107">Kaardimoodulid pakuvad erinevaid vaateid, nagu tee-, ülalt- ja tänavavaade, mida kasutajad saavad valida, et vaadata kaardil asukohti.</span><span class="sxs-lookup"><span data-stu-id="8dd43-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="8dd43-108">Need võimaldavad ka toiminguid, nagu suumimine ja kasutaja asukoha kasutamine.</span><span class="sxs-lookup"><span data-stu-id="8dd43-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="8dd43-109">Kaardimoodul töötab koos kaupluse valija mooduliga, et määrata kaupluste geograafilised asukohad, mis tuleb kaardil renderdada.</span><span class="sxs-lookup"><span data-stu-id="8dd43-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="8dd43-110">Kaupluse valija ja kaardimoodul teevad koostööd, kui kasutaja valib saidilehel kaupluse ühes nendest moodulitest.</span><span class="sxs-lookup"><span data-stu-id="8dd43-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="8dd43-111">Kaardimooduleid saab kasutada ka teiste stsenaariumide puhul, mis ei ole seotud kaupluse valija moodulitega koos töötamisega.</span><span class="sxs-lookup"><span data-stu-id="8dd43-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="8dd43-112">Kuid selleks tuleb moodulit kohandada.</span><span class="sxs-lookup"><span data-stu-id="8dd43-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="8dd43-113">Kaardimoodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="8dd43-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="8dd43-114">Järgmisel pildil on näide kaardimoodulist, mida kasutatakse kaupluste asukohtade lehel.</span><span class="sxs-lookup"><span data-stu-id="8dd43-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Kaupluse valija mooduli näide](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="8dd43-116">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="8dd43-116">Module properties</span></span>

| <span data-ttu-id="8dd43-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="8dd43-117">Property name</span></span>             | <span data-ttu-id="8dd43-118">Väärtus</span><span class="sxs-lookup"><span data-stu-id="8dd43-118">Value</span></span>                 | <span data-ttu-id="8dd43-119">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8dd43-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="8dd43-120">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="8dd43-120">Heading</span></span> | <span data-ttu-id="8dd43-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="8dd43-121">Text</span></span> | <span data-ttu-id="8dd43-122">Mooduli pealkiri.</span><span class="sxs-lookup"><span data-stu-id="8dd43-122">The heading for the module.</span></span> |
| <span data-ttu-id="8dd43-123">Rõhknaela suvandid: vaikeikoon</span><span class="sxs-lookup"><span data-stu-id="8dd43-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="8dd43-124">Pilt</span><span class="sxs-lookup"><span data-stu-id="8dd43-124">Image</span></span> | <span data-ttu-id="8dd43-125">Rõhknaelasümboli pilt, mida kasutatakse kaardil kuvatud kaupluste puhul.</span><span class="sxs-lookup"><span data-stu-id="8dd43-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="8dd43-126">Rõhknaela suvandid: aktiivse üksuse ikoon</span><span class="sxs-lookup"><span data-stu-id="8dd43-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="8dd43-127">Pilt</span><span class="sxs-lookup"><span data-stu-id="8dd43-127">Image</span></span> | <span data-ttu-id="8dd43-128">Rõhknaelasümboli pilt, mida kasutatakse kaardil valitud kaupluse puhul.</span><span class="sxs-lookup"><span data-stu-id="8dd43-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="8dd43-129">Rõhknaela suvandid: ikooni vaikevärv</span><span class="sxs-lookup"><span data-stu-id="8dd43-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="8dd43-130">Tähemärkide string</span><span class="sxs-lookup"><span data-stu-id="8dd43-130">Character string</span></span> | <span data-ttu-id="8dd43-131">Kaardil olevate rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus.</span><span class="sxs-lookup"><span data-stu-id="8dd43-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="8dd43-132">Rõhknaela suvandid: aktiivse üksuse ikooni värv</span><span class="sxs-lookup"><span data-stu-id="8dd43-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="8dd43-133">Tähemärkide string</span><span class="sxs-lookup"><span data-stu-id="8dd43-133">Character string</span></span> | <span data-ttu-id="8dd43-134">Kaardil valitud rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus.</span><span class="sxs-lookup"><span data-stu-id="8dd43-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="8dd43-135">Näita indeksit</span><span class="sxs-lookup"><span data-stu-id="8dd43-135">Show index</span></span> | <span data-ttu-id="8dd43-136">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="8dd43-136">**True** or **False**</span></span> | <span data-ttu-id="8dd43-137">Kui selle atribuudi väärtuseks on seatud **Tõene**, näitavad kõik kauplust tähistavad rõhknaelasümbolid indeksit.</span><span class="sxs-lookup"><span data-stu-id="8dd43-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="8dd43-138">See indeks ühtib indeksiga loendivaates, mida kaupluse valija moodul näitab.</span><span class="sxs-lookup"><span data-stu-id="8dd43-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="8dd43-139">Lubatud vastendamis-URL-ide lisamine saidi sisu turbepoliitika direktiividele</span><span class="sxs-lookup"><span data-stu-id="8dd43-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="8dd43-140">Et kaardimoodul saaks suhelda Bingi kaartidega, peate tagama, et teie saidi sisu turbepoliitikas (CSP) oleksid lubatud järgmised vastendamise URL-id.</span><span class="sxs-lookup"><span data-stu-id="8dd43-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="8dd43-141">Seadistus toimub Commerce'i saidiehitajas, lisades lubatud URL-id erinevatele saidi CSP-direktiividele (nt **img-src**).</span><span class="sxs-lookup"><span data-stu-id="8dd43-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="8dd43-142">Lisateavet leiate teemast [Sisu turbepoliitika](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="8dd43-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="8dd43-143">Lisage direktiivile **connect-src** väärtus **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="8dd43-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="8dd43-144">Lisage direktiivile **img-src** väärtus **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="8dd43-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="8dd43-145">Lisage direktiivile **script-src** väärtus **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="8dd43-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="8dd43-146">Lisage direktiivile **script style-src** väärtus **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="8dd43-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="8dd43-147">Lehele kaardimooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="8dd43-147">Add a map module to a page</span></span>

<span data-ttu-id="8dd43-148">Üksikasjalikku teavet kaardimooduli lehel konfigureerimise kohta leiate teemast [Kaupluse valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="8dd43-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="8dd43-149">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="8dd43-149">Additional resources</span></span>

[<span data-ttu-id="8dd43-150">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="8dd43-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8dd43-151">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="8dd43-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="8dd43-152">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="8dd43-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8dd43-153">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="8dd43-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="8dd43-154">Organisatsiooni Bingi kaartide haldamine</span><span class="sxs-lookup"><span data-stu-id="8dd43-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="8dd43-155">Bing Maps V8 Web Control</span><span class="sxs-lookup"><span data-stu-id="8dd43-155">Bing Maps V8 Web Control</span></span>](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]