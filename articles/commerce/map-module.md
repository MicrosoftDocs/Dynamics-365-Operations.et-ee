---
title: Kaardimoodul
description: See teema hõlmab kaardimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d2cbc67a186a76647a4f7ddc7942b15d3e469ece
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817202"
---
# <a name="map-module"></a><span data-ttu-id="e624d-103">Kaardimoodul</span><span class="sxs-lookup"><span data-stu-id="e624d-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="e624d-104">See teema hõlmab kaardimooduleid ja kirjeldab, kuidas neid rakenduses Microsoft Dynamics 365 Commerce konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="e624d-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e624d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="e624d-105">Overview</span></span>

<span data-ttu-id="e624d-106">Kaardimoodul kuvab kaupluste asukohad interaktiivsel kaardil, mis renderdatakse [Bing Maps V8 Web Controli](https://docs.microsoft.com/bingmaps/v8-web-control/) abil.</span><span class="sxs-lookup"><span data-stu-id="e624d-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="e624d-107">Vajalik on Bing Maps kaartide API võti ja see tuleb lisada jagatud parameetrite lehele rakenduses Commerce peakontorid.</span><span class="sxs-lookup"><span data-stu-id="e624d-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="e624d-108">Kaardimoodulid pakuvad erinevaid vaateid, nagu tee-, ülalt- ja tänavavaade, mida kasutajad saavad valida, et vaadata kaardil asukohti.</span><span class="sxs-lookup"><span data-stu-id="e624d-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="e624d-109">Need võimaldavad ka toiminguid, nagu suumimine ja kasutaja asukoha kasutamine.</span><span class="sxs-lookup"><span data-stu-id="e624d-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="e624d-110">Kaardimoodul töötab koos kaupluse valija mooduliga, et määrata kaupluste geograafilised asukohad, mis tuleb kaardil renderdada.</span><span class="sxs-lookup"><span data-stu-id="e624d-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="e624d-111">Kaupluse valija ja kaardimoodul teevad koostööd, kui kasutaja valib saidilehel kaupluse ühes nendest moodulitest.</span><span class="sxs-lookup"><span data-stu-id="e624d-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="e624d-112">Kaardimooduleid saab kasutada ka teiste stsenaariumide puhul, mis ei ole seotud kaupluse valija moodulitega koos töötamisega.</span><span class="sxs-lookup"><span data-stu-id="e624d-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="e624d-113">Kuid selleks tuleb moodulit kohandada.</span><span class="sxs-lookup"><span data-stu-id="e624d-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="e624d-114">Kaardimoodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="e624d-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="e624d-115">Järgmisel pildil on näide kaardimoodulist, mida kasutatakse kaupluste asukohtade lehel.</span><span class="sxs-lookup"><span data-stu-id="e624d-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Kaupluse valija mooduli näide](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="e624d-117">Mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="e624d-117">Module properties</span></span>

| <span data-ttu-id="e624d-118">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="e624d-118">Property name</span></span>             | <span data-ttu-id="e624d-119">Väärtus</span><span class="sxs-lookup"><span data-stu-id="e624d-119">Value</span></span>                 | <span data-ttu-id="e624d-120">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e624d-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e624d-121">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="e624d-121">Heading</span></span> | <span data-ttu-id="e624d-122">Tekst</span><span class="sxs-lookup"><span data-stu-id="e624d-122">Text</span></span> | <span data-ttu-id="e624d-123">Mooduli pealkiri.</span><span class="sxs-lookup"><span data-stu-id="e624d-123">The heading for the module.</span></span> |
| <span data-ttu-id="e624d-124">Rõhknaela suvandid: vaikeikoon</span><span class="sxs-lookup"><span data-stu-id="e624d-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="e624d-125">Pilt</span><span class="sxs-lookup"><span data-stu-id="e624d-125">Image</span></span> | <span data-ttu-id="e624d-126">Rõhknaelasümboli pilt, mida kasutatakse kaardil kuvatud kaupluste puhul.</span><span class="sxs-lookup"><span data-stu-id="e624d-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="e624d-127">Rõhknaela suvandid: aktiivse üksuse ikoon</span><span class="sxs-lookup"><span data-stu-id="e624d-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="e624d-128">Pilt</span><span class="sxs-lookup"><span data-stu-id="e624d-128">Image</span></span> | <span data-ttu-id="e624d-129">Rõhknaelasümboli pilt, mida kasutatakse kaardil valitud kaupluse puhul.</span><span class="sxs-lookup"><span data-stu-id="e624d-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="e624d-130">Rõhknaela suvandid: ikooni vaikevärv</span><span class="sxs-lookup"><span data-stu-id="e624d-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="e624d-131">Tähemärkide string</span><span class="sxs-lookup"><span data-stu-id="e624d-131">Character string</span></span> | <span data-ttu-id="e624d-132">Kaardil olevate rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus.</span><span class="sxs-lookup"><span data-stu-id="e624d-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e624d-133">Rõhknaela suvandid: aktiivse üksuse ikooni värv</span><span class="sxs-lookup"><span data-stu-id="e624d-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="e624d-134">Tähemärkide string</span><span class="sxs-lookup"><span data-stu-id="e624d-134">Character string</span></span> | <span data-ttu-id="e624d-135">Kaardil valitud rõhknaelasümbolite värvi tekstiline või kuueteistkümnendsüsteemis väärtus.</span><span class="sxs-lookup"><span data-stu-id="e624d-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e624d-136">Näita indeksit</span><span class="sxs-lookup"><span data-stu-id="e624d-136">Show index</span></span> | <span data-ttu-id="e624d-137">**Tõene** või **Väär**</span><span class="sxs-lookup"><span data-stu-id="e624d-137">**True** or **False**</span></span> | <span data-ttu-id="e624d-138">Kui selle atribuudi väärtuseks on seatud **Tõene**, näitavad kõik kauplust tähistavad rõhknaelasümbolid indeksit.</span><span class="sxs-lookup"><span data-stu-id="e624d-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="e624d-139">See indeks ühtib indeksiga loendivaates, mida kaupluse valija moodul näitab.</span><span class="sxs-lookup"><span data-stu-id="e624d-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="e624d-140">Lubatud vastendamis-URL-ide lisamine saidi sisu turbepoliitika direktiividele</span><span class="sxs-lookup"><span data-stu-id="e624d-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="e624d-141">Et kaardimoodul saaks suhelda Bingi kaartidega, peate tagama, et teie saidi sisu turbepoliitikas (CSP) oleksid lubatud järgmised vastendamise URL-id (tuntud ka kui valgesse nimekirja lisamine).</span><span class="sxs-lookup"><span data-stu-id="e624d-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="e624d-142">Seadistus toimub Commerce'i saidiehitajas, lisades lubatud URL-id erinevatele saidi CSP-direktiividele (nt **img-src**).</span><span class="sxs-lookup"><span data-stu-id="e624d-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="e624d-143">Lisateavet leiate teemast [Sisu turbepoliitika](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="e624d-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="e624d-144">Lisage direktiivile **connect-src** väärtus **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e624d-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="e624d-145">Lisage direktiivile **img-src** väärtus **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e624d-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e624d-146">Lisage direktiivile **script-src** väärtus **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e624d-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e624d-147">Lisage direktiivile **script style-src** väärtus **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e624d-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="e624d-148">Lehele kaardimooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="e624d-148">Add a map module to a page</span></span>

<span data-ttu-id="e624d-149">Üksikasjalikku teavet kaardimooduli lehel konfigureerimise kohta leiate teemast [Kaupluse valija moodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="e624d-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="e624d-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e624d-150">Additional resources</span></span>

[<span data-ttu-id="e624d-151">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="e624d-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e624d-152">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="e624d-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e624d-153">Ostukorvimoodul</span><span class="sxs-lookup"><span data-stu-id="e624d-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e624d-154">Kaupluse valimise moodul</span><span class="sxs-lookup"><span data-stu-id="e624d-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="e624d-155">Organisatsiooni Bingi kaartide haldamine</span><span class="sxs-lookup"><span data-stu-id="e624d-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="e624d-156">Bing Maps V8 Web Control</span><span class="sxs-lookup"><span data-stu-id="e624d-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
