---
title: IFrame-moodul
description: See teema hõlmab iframe-moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
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
ms.openlocfilehash: 7b397b91d1b8a45347ef2d05f42fb7c610ab3912
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797066"
---
# <a name="iframe-module"></a><span data-ttu-id="1a8b8-103">IFrame-moodul</span><span class="sxs-lookup"><span data-stu-id="1a8b8-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a8b8-104">See teema hõlmab iframe-moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1a8b8-105">IFrame-moodul tagab iFrame'i (tekstisisene raam), mis majutab saidil välissisu.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-105">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="1a8b8-106">Näiteks saab seda kasutada YouTube'i video või PDF-faili vaaturi majutamiseks ükskõik millisel saidilehel.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-106">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="1a8b8-107">IFrame-mooduli jaoks on vaja siht-URL-i.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-107">An iframe module requires a target URL.</span></span> <span data-ttu-id="1a8b8-108">Seejärel majutab see sihtlehe sisu HTML-i **iFrame'i** elemendi sees.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-108">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="1a8b8-109">Välised URL-id peavad olema saidi sisu turbepoliitika (CSP) direktiivide põhjal lubatud URL-ide loendis.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-109">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="1a8b8-110">IFrame'i sisu jaoks peavad URL-id olema lubatud direktiivi **frame-ancestor** kaudu.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-110">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="1a8b8-111">Lisateavet leiate teemast [Sisu turbepoliitika (CSP) haldamine](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="1a8b8-111">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="1a8b8-112">IFrame-moodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-112">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="1a8b8-113">Järgmisel pildil on näited iFrame-moodulitest, mis näitavad saidilehtedel väliseid videoid.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![IFrame-moodulite näide, millel on näha välised videod](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="1a8b8-115">IFrame-mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="1a8b8-115">Iframe module properties</span></span>

| <span data-ttu-id="1a8b8-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="1a8b8-116">Property name</span></span>             | <span data-ttu-id="1a8b8-117">Väärtus</span><span class="sxs-lookup"><span data-stu-id="1a8b8-117">Value</span></span>                 | <span data-ttu-id="1a8b8-118">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1a8b8-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="1a8b8-119">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="1a8b8-119">Heading</span></span> | <span data-ttu-id="1a8b8-120">Tekst</span><span class="sxs-lookup"><span data-stu-id="1a8b8-120">Text</span></span> | <span data-ttu-id="1a8b8-121">Mooduli pealkiri.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-121">The heading for the module.</span></span> |
| <span data-ttu-id="1a8b8-122">Siht-URL</span><span class="sxs-lookup"><span data-stu-id="1a8b8-122">Target URL</span></span> | <span data-ttu-id="1a8b8-123">URL</span><span class="sxs-lookup"><span data-stu-id="1a8b8-123">URL</span></span> | <span data-ttu-id="1a8b8-124">Moodulis majutatud URL.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="1a8b8-125">Kõrgus</span><span class="sxs-lookup"><span data-stu-id="1a8b8-125">Height</span></span> | <span data-ttu-id="1a8b8-126">Arv või protsent</span><span class="sxs-lookup"><span data-stu-id="1a8b8-126">Number or percentage</span></span> | <span data-ttu-id="1a8b8-127">Mooduli kõrgus pikslites või protsendina.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="1a8b8-128">Näiteks koheldakse väärtust **100** pikslite arvuna ja väärtust **100%** protsendina.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="1a8b8-129">Aria-silt</span><span class="sxs-lookup"><span data-stu-id="1a8b8-129">Aria label</span></span> | <span data-ttu-id="1a8b8-130">Tekst</span><span class="sxs-lookup"><span data-stu-id="1a8b8-130">Text</span></span> | <span data-ttu-id="1a8b8-131">Juurdepääsetavuse eesmärgil saab määratleda ARIA-sildi (Accessible Rich Internet Applications).</span><span class="sxs-lookup"><span data-stu-id="1a8b8-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="1a8b8-132">Lehele iFrame-mooduli lisamine</span><span class="sxs-lookup"><span data-stu-id="1a8b8-132">Add an iframe module to a page</span></span>

<span data-ttu-id="1a8b8-133">Et lisada välise video kuvamiseks lehele iFrame-moodul, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="1a8b8-134">Avage **Mallid** ja valige uue malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="1a8b8-135">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all **Turundusmall** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="1a8b8-136">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1a8b8-137">Avage **Lehed** ja seejärel valige uue lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="1a8b8-138">Valige dialoogiboksis **Vali mall** mall **Turundusmall**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="1a8b8-139">Sisestage jaotises **Lehe nimi** väärtus **Turundusleht** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="1a8b8-140">Uue lehe pesas **Peamine** valige kolmikpunkt (**...**) ja seejärel valige suvand **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a8b8-141">Valige dialoogiboksis **Lisa moodul** moodul **Konteiner** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a8b8-142">Seadke mooduli atribuutide paanil **Laiuse** väärtuseks **Täida konteiner**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="1a8b8-143">Valige pesas **Konteiner** kolmikpunkt (**…**) ja seejärel valige käsk **Lisa moodul**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="1a8b8-144">Valige dialoogiboksis **Lisa moodul** moodul **iFrame** ja klõpsake seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="1a8b8-145">Seadke mooduli atribuutide paanil suvandi **Siht-URL** väärtuseks video väline URL.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="1a8b8-146">Määrake vajaduse järgi muud atribuudid, näiteks **Pealkiri** ja **Kõrgus**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="1a8b8-147">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="1a8b8-148">Minge oma saidil turunduslehele.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="1a8b8-149">Peaksite nägema iFrame-moodulis renderdatavat videot.</span><span class="sxs-lookup"><span data-stu-id="1a8b8-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="1a8b8-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="1a8b8-150">Additional resources</span></span>

[<span data-ttu-id="1a8b8-151">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="1a8b8-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="1a8b8-152">Sisu turbepoliitika (CSP) haldamine</span><span class="sxs-lookup"><span data-stu-id="1a8b8-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]