---
title: 4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine
description: Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799639"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="32a32-103">4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine</span><span class="sxs-lookup"><span data-stu-id="32a32-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="32a32-104">Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.</span><span class="sxs-lookup"><span data-stu-id="32a32-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="32a32-105">Kui taotlus ei ole edukas, väljastab server HTTP olekukoodi tõrkevastused.</span><span class="sxs-lookup"><span data-stu-id="32a32-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="32a32-106">Kui lehte ei leita, hõivatakse ja tagastatakse olekukood 404, ning serveritõrke ilmnemisel hõivatakse ja tagastatakse olekukood 500.</span><span class="sxs-lookup"><span data-stu-id="32a32-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="32a32-107">Rakenduses Dynamics 365 Commerce saavad rakenduse kasutajad luua kohandatud olekukoodi tõrkevastuse lehti, mis kuvatakse nende olekukoodi tõrkevastuste kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="32a32-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="32a32-108">Olekukoodi tõrkevastuse lehe loomine</span><span class="sxs-lookup"><span data-stu-id="32a32-108">Build a status code error response page</span></span>

<span data-ttu-id="32a32-109">Olekukoodi tõrkevastuse lehe loomise alustamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32a32-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32a32-110">Logige oma eelistatud veebibrauseris rakendusse Dynamics 365 Commerce sisse.</span><span class="sxs-lookup"><span data-stu-id="32a32-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="32a32-111">Valige sait, mille jaoks soovite 4xx/5xx olekukoodi tõrkevastuse lehe luua.</span><span class="sxs-lookup"><span data-stu-id="32a32-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="32a32-112">Malli loomine</span><span class="sxs-lookup"><span data-stu-id="32a32-112">Build the template</span></span>

<span data-ttu-id="32a32-113">Olekukoodi tõrkevastuse lehe malli loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32a32-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32a32-114">Avage **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="32a32-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="32a32-115">Valige lehe malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="32a32-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="32a32-116">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all uue malli nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="32a32-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="32a32-117">Looge mall põhinedes struktuuril, mille soovite, et olekukoodi tõrkevastuse lehel olemas oleks.</span><span class="sxs-lookup"><span data-stu-id="32a32-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="32a32-118">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="32a32-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="32a32-119">Olekukoodi tõrkevastuse lehe loomine</span><span class="sxs-lookup"><span data-stu-id="32a32-119">Build the status code error response page</span></span>

<span data-ttu-id="32a32-120">Olekukoodi tõrkevastuse lehe loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32a32-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32a32-121">Avage **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="32a32-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="32a32-122">Valige lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="32a32-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="32a32-123">Valige mall dialoogiboksis **Vali mall** ja seejärel sisestage olekukoodi tõrkevastuse lehe pealkiri jaotises **Lehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="32a32-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="32a32-124">Jätke väli **Lehe URL** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="32a32-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="32a32-125">Looge leht.</span><span class="sxs-lookup"><span data-stu-id="32a32-125">Build the page.</span></span>
1. <span data-ttu-id="32a32-126">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="32a32-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="32a32-127">4xx ja 5xx olekukoodi tõrgete jaoks saate luua eraldi olekukoodi tõrkevastuse lehed.</span><span class="sxs-lookup"><span data-stu-id="32a32-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="32a32-128">Teise võimalusena saate mõlema tõrkekategooria puhul kasutada sama üldist olekukoodi tõrkevastuse lehte.</span><span class="sxs-lookup"><span data-stu-id="32a32-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="32a32-129">Olekukoodi tõrkevastuse lehe ümbersuunamise määramine</span><span class="sxs-lookup"><span data-stu-id="32a32-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="32a32-130">Olekukoodi tõrkevastuse lehe ümbersuunamise määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="32a32-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="32a32-131">Avage **URL-id \> Uus \> Uus pseudonüüm** ja valige varem loodud olekukoodi tõrkevastuse leht.</span><span class="sxs-lookup"><span data-stu-id="32a32-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="32a32-132">Väljale **Pseudonüüm** sisestage kas **vaikimisi 4xx** või **vaikimisi 5xx**, olenevalt olekukoodi tõrkevastuse lehest, mille ümbersuunamise jaoks määrate.</span><span class="sxs-lookup"><span data-stu-id="32a32-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="32a32-133">Need pseudonüümid tuleb avaldada.</span><span class="sxs-lookup"><span data-stu-id="32a32-133">These aliases must be published.</span></span> <span data-ttu-id="32a32-134">Vastasel korral ümbersuunamine ei tööta.</span><span class="sxs-lookup"><span data-stu-id="32a32-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="32a32-135">Linkimise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="32a32-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="32a32-136">Kui kasutate mõlema tõrkekategooria jaoks ühte olekukoodi tõrkevastuse lehte, korrake seda protseduuri samale lehele teise tõrkekategooria pseudonüümi linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="32a32-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32a32-137">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="32a32-137">Additional resources</span></span>

[<span data-ttu-id="32a32-138">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="32a32-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="32a32-139">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="32a32-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="32a32-140">Lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="32a32-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
