---
title: Tootedimensioonidele kuvasätete rakendamine
description: See teema hõlmab tootedimensioonide kuvasätteid ja kirjeldab, kuidas neid rakendada rakenduses Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
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
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117219"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="aabf2-103">Tootedimensioonidele kuvasätete rakendamine</span><span class="sxs-lookup"><span data-stu-id="aabf2-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="aabf2-104">See teema hõlmab tootedimensioonide kuvasätteid ja kirjeldab, kuidas neid rakendada rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aabf2-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aabf2-105">Dynamics 365 Commerce toetab suurust, stiili ja värvimõõtmeid tootevariantide eristamiseks.</span><span class="sxs-lookup"><span data-stu-id="aabf2-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="aabf2-106">Mõõtmed kuvatakse tavaliselt tekstiväärtustena, näiteks "Väike", "Keskmine" ja "Suur" suuruste puhul ning "Must" ja "Pruun" värvide puhul.</span><span class="sxs-lookup"><span data-stu-id="aabf2-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="aabf2-107">Kui aga toode toetab paljusid variatsioone, võib tootevariantide sirvimine olla keeruline, sest iga variandi pildi vaatamiseks on vaja mitut valikut.</span><span class="sxs-lookup"><span data-stu-id="aabf2-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="aabf2-108">Tootevariantide sirvimise lihtsustamiseks saab Commerce'i versioonis 10.0.20 kasutada pilte ja kuueteistkümnendkoode dimensioonide kuvamiseks näidistena.</span><span class="sxs-lookup"><span data-stu-id="aabf2-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="aabf2-109">Commerce site ehitajas määratletakse varude sätted saidiehitaja jaotises **Saidi sätted \> Laiendused \> Varude haldus**.</span><span class="sxs-lookup"><span data-stu-id="aabf2-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="aabf2-110">Järgmisel joonisel on toodud saidikoosturi dimensioonisätete näide.</span><span class="sxs-lookup"><span data-stu-id="aabf2-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Ärisaidi koostaja saidisätete näide](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="aabf2-112">Saadaval on kaks dimensioonisätet:</span><span class="sxs-lookup"><span data-stu-id="aabf2-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="aabf2-113">**Pildina kuvatavad dimensioonid** – määrake, millised dimensioonid peaksid e-kaubanduse saidi lehtedel nagu näiteks toote üksikasjade lehtedel (PDPd) ja otsingutulemite loendi lehtedel olema kuvatud.</span><span class="sxs-lookup"><span data-stu-id="aabf2-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="aabf2-114">Mis tahes värvi-, suuruse- ja stiilimõõtmete kombinatsiooni saab kuvada näitena.</span><span class="sxs-lookup"><span data-stu-id="aabf2-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="aabf2-115">Kui dimensioon on valitud kuvamiseks kui näide, otsib Commerce module renderdamine hex-koodi saada olevat konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="aabf2-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="aabf2-116">Kui hex-koodi pole konfigureeritud, otsib süsteemiloogika pildi URL-i näidise konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="aabf2-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="aabf2-117">Kui pole konfigureeritud ei hex-koodi ega pildi URL-i, kuvatakse tekst.</span><span class="sxs-lookup"><span data-stu-id="aabf2-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="aabf2-118">Järgmisel joonisel on kujutatud näide, kus e-kaubanduse saidi PDP sisaldab värvi- ja suuruse näiteid.</span><span class="sxs-lookup"><span data-stu-id="aabf2-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="aabf2-119">Selles näites on värvidimensiooni jaoks konfigureeritud heksi kood.</span><span class="sxs-lookup"><span data-stu-id="aabf2-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="aabf2-120">Seetõttu kuvatakse näited värvidena.</span><span class="sxs-lookup"><span data-stu-id="aabf2-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="aabf2-121">Kuid ei hex-kood ega pildi URL pole suuruse dimensiooni jaoks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="aabf2-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="aabf2-122">Seetõttu kuvatakse teksti.</span><span class="sxs-lookup"><span data-stu-id="aabf2-122">Therefore, text is shown.</span></span>

    ![Näide e-kaubanduse toote üksikasjade lehel näietena kuvatud värvidimensioonist](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="aabf2-124">**Tootekaardil kuvatavad dimensioonid** – määrake, millised dimensioonid tuleks kuvada loendites ja loendilehtedel kuvatavatel tootekaartidel.</span><span class="sxs-lookup"><span data-stu-id="aabf2-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="aabf2-125">Enne dimensiooni kuvamist tootekaardil peab see säte olema selle dimensiooni puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="aabf2-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="aabf2-126">Lubatud peaksid olem ka **Pildisättena kuvatavad dimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="aabf2-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="aabf2-127">Tootekaartide näidise valiku käitumine on optimeeritud värvidimensiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="aabf2-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="aabf2-128">Muude dimensioonide puhul võib näidise valiku käitumise kohandamiseks olla vaja vaatelaiendit.</span><span class="sxs-lookup"><span data-stu-id="aabf2-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="aabf2-129">Järgmisel joonisel on kujutatud näide, kus e-kaubanduse saidi loendileht sisaldab värvinäidistega tootekaarte.</span><span class="sxs-lookup"><span data-stu-id="aabf2-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Näide e-kaubanduse toote üksikasjade lehel näidetena kuvatud värvidimensioonist](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="aabf2-131">Lisateavet selle kohta, kuidas konfigureerida tootedimensioone nii, et neid kuvataks saidilehtedel kelladena, leiate teemast [Tootedimensiooniväärtuste konfigureerimine näidistena kuvamiseks](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="aabf2-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aabf2-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="aabf2-132">Additional resources</span></span>

[<span data-ttu-id="aabf2-133">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="aabf2-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aabf2-134">Otsingutulemuste moodul</span><span class="sxs-lookup"><span data-stu-id="aabf2-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="aabf2-135">Ostukastimoodul</span><span class="sxs-lookup"><span data-stu-id="aabf2-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="aabf2-136">Tootedimensiooni väärtuste konfigureerimine näidistena kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="aabf2-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
