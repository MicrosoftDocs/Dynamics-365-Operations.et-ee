---
title: 4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine
description: Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d21ce20b2c7ac8c656a718749dabd76f33893da8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991461"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="cefba-103">4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine</span><span class="sxs-lookup"><span data-stu-id="cefba-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cefba-104">Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.</span><span class="sxs-lookup"><span data-stu-id="cefba-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cefba-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="cefba-105">Overview</span></span>

<span data-ttu-id="cefba-106">Kui taotlus ei ole edukas, väljastab server HTTP olekukoodi tõrkevastused.</span><span class="sxs-lookup"><span data-stu-id="cefba-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="cefba-107">Kui lehte ei leita, hõivatakse ja tagastatakse olekukood 404, ning serveritõrke ilmnemisel hõivatakse ja tagastatakse olekukood 500.</span><span class="sxs-lookup"><span data-stu-id="cefba-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="cefba-108">Rakenduses Dynamics 365 Commerce saavad rakenduse kasutajad luua kohandatud olekukoodi tõrkevastuse lehti, mis kuvatakse nende olekukoodi tõrkevastuste kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="cefba-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="cefba-109">Olekukoodi tõrkevastuse lehe loomine</span><span class="sxs-lookup"><span data-stu-id="cefba-109">Build a status code error response page</span></span>

<span data-ttu-id="cefba-110">Olekukoodi tõrkevastuse lehe loomise alustamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cefba-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="cefba-111">Logige oma eelistatud veebibrauseris rakendusse Dynamics 365 Commerce sisse.</span><span class="sxs-lookup"><span data-stu-id="cefba-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="cefba-112">Valige sait, mille jaoks soovite 4xx/5xx olekukoodi tõrkevastuse lehe luua.</span><span class="sxs-lookup"><span data-stu-id="cefba-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="cefba-113">Malli loomine</span><span class="sxs-lookup"><span data-stu-id="cefba-113">Build the template</span></span>

<span data-ttu-id="cefba-114">Olekukoodi tõrkevastuse lehe malli loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cefba-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="cefba-115">Avage **Mallid**.</span><span class="sxs-lookup"><span data-stu-id="cefba-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="cefba-116">Valige lehe malli loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cefba-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="cefba-117">Sisestage dialoogiboksis **Uus mall** jaotise **Malli nimi** all uue malli nimi ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="cefba-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="cefba-118">Looge mall põhinedes struktuuril, mille soovite, et olekukoodi tõrkevastuse lehel olemas oleks.</span><span class="sxs-lookup"><span data-stu-id="cefba-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="cefba-119">Valige **Salvesta**, valige malli registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="cefba-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="cefba-120">Olekukoodi tõrkevastuse lehe loomine</span><span class="sxs-lookup"><span data-stu-id="cefba-120">Build the status code error response page</span></span>

<span data-ttu-id="cefba-121">Olekukoodi tõrkevastuse lehe loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cefba-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="cefba-122">Avage **Lehed**.</span><span class="sxs-lookup"><span data-stu-id="cefba-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="cefba-123">Valige lehe loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cefba-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="cefba-124">Valige mall dialoogiboksis **Vali mall** ja seejärel sisestage olekukoodi tõrkevastuse lehe pealkiri jaotises **Lehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="cefba-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="cefba-125">Jätke väli **Lehe URL** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="cefba-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="cefba-126">Looge leht.</span><span class="sxs-lookup"><span data-stu-id="cefba-126">Build the page.</span></span>
1. <span data-ttu-id="cefba-127">Valige **Salvesta**, valige lehe registreerimiseks **Lõpeta redigeerimine** ja seejärel selle avaldamiseks **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="cefba-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="cefba-128">4xx ja 5xx olekukoodi tõrgete jaoks saate luua eraldi olekukoodi tõrkevastuse lehed.</span><span class="sxs-lookup"><span data-stu-id="cefba-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="cefba-129">Teise võimalusena saate mõlema tõrkekategooria puhul kasutada sama üldist olekukoodi tõrkevastuse lehte.</span><span class="sxs-lookup"><span data-stu-id="cefba-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="cefba-130">Olekukoodi tõrkevastuse lehe ümbersuunamise määramine</span><span class="sxs-lookup"><span data-stu-id="cefba-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="cefba-131">Olekukoodi tõrkevastuse lehe ümbersuunamise määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="cefba-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="cefba-132">Avage **URL-id \> Uus \> Uus pseudonüüm** ja valige varem loodud olekukoodi tõrkevastuse leht.</span><span class="sxs-lookup"><span data-stu-id="cefba-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="cefba-133">Väljale **Pseudonüüm** sisestage kas **vaikimisi 4xx** või **vaikimisi 5xx**, olenevalt olekukoodi tõrkevastuse lehest, mille ümbersuunamise jaoks määrate.</span><span class="sxs-lookup"><span data-stu-id="cefba-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="cefba-134">Need pseudonüümid tuleb avaldada.</span><span class="sxs-lookup"><span data-stu-id="cefba-134">These aliases must be published.</span></span> <span data-ttu-id="cefba-135">Vastasel korral ümbersuunamine ei tööta.</span><span class="sxs-lookup"><span data-stu-id="cefba-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="cefba-136">Linkimise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="cefba-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="cefba-137">Kui kasutate mõlema tõrkekategooria jaoks ühte olekukoodi tõrkevastuse lehte, korrake seda protseduuri samale lehele teise tõrkekategooria pseudonüümi linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="cefba-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cefba-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cefba-138">Additional resources</span></span>

[<span data-ttu-id="cefba-139">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="cefba-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="cefba-140">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="cefba-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cefba-141">Lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="cefba-141">Create a page URL</span></span>](create-page-url.md)
