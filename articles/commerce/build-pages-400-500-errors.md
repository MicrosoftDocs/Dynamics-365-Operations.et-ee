---
title: 4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine
description: Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4477a0a43971b5322c6acd6971cba2e79e2dc8c6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001116"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="62a7a-103">4xx/5xx olekukoodi tõrgete jaoks kohandatud vastuselehtede loomine</span><span class="sxs-lookup"><span data-stu-id="62a7a-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="62a7a-104">Selles teemas kirjeldatakse, kuidas luua kohandatud vastuse lehekülgi 4xx ja 5xx olekukoodi tõrgete jaoks, kasutades rakenduse Microsoft Dynamics 365 Commerce autoriseerimise tööriistu.</span><span class="sxs-lookup"><span data-stu-id="62a7a-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="62a7a-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="62a7a-105">Overview</span></span>

<span data-ttu-id="62a7a-106">Kui taotlus ei ole edukas, väljastab server HTTP olekukoodi tõrkevastused.</span><span class="sxs-lookup"><span data-stu-id="62a7a-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="62a7a-107">Kui lehte ei leita, hõivatakse ja tagastatakse olekukood 404, ning serveritõrke ilmnemisel hõivatakse ja tagastatakse olekukood 500.</span><span class="sxs-lookup"><span data-stu-id="62a7a-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="62a7a-108">Rakenduses Dynamics 365 Commerce saavad rakenduse kasutajad luua kohandatud olekukoodi tõrkevastuse lehti, mis kuvatakse nende olekukoodi tõrkevastuste kasutajatele.</span><span class="sxs-lookup"><span data-stu-id="62a7a-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="62a7a-109">Olekukoodi tõrkevastuse lehe loomine</span><span class="sxs-lookup"><span data-stu-id="62a7a-109">Build a status code error response page</span></span>

<span data-ttu-id="62a7a-110">Olekukoodi tõrkevastuse lehe loomise alustamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62a7a-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="62a7a-111">Logige oma eelistatud veebibrauseris rakendusse Dynamics 365 Commerce sisse.</span><span class="sxs-lookup"><span data-stu-id="62a7a-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="62a7a-112">Valige sait, mille jaoks soovite 4xx/5xx olekukoodi tõrkevastuse lehe luua.</span><span class="sxs-lookup"><span data-stu-id="62a7a-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="62a7a-113">Malli loomine</span><span class="sxs-lookup"><span data-stu-id="62a7a-113">Build the template</span></span>

<span data-ttu-id="62a7a-114">Olekukoodi tõrkevastuse lehe malli loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62a7a-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="62a7a-115">Avage **Mallid \> Uus mall**.</span><span class="sxs-lookup"><span data-stu-id="62a7a-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="62a7a-116">Andke uuele mallile nimi.</span><span class="sxs-lookup"><span data-stu-id="62a7a-116">Name the new template.</span></span>
1. <span data-ttu-id="62a7a-117">Looge mall põhinedes struktuuril, mille soovite, et olekukoodi tõrkevastuse lehel olemas oleks.</span><span class="sxs-lookup"><span data-stu-id="62a7a-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="62a7a-118">Registreerige mall ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="62a7a-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="62a7a-119">Olekukoodi tõrkevastuse lehe loomine</span><span class="sxs-lookup"><span data-stu-id="62a7a-119">Build the status code error response page</span></span>

<span data-ttu-id="62a7a-120">Olekukoodi tõrkevastuse lehe loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62a7a-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="62a7a-121">Avage **Lehed \> Uus leht**.</span><span class="sxs-lookup"><span data-stu-id="62a7a-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="62a7a-122">Andke olekukoodi tõrkevastuse lehele nimi, kuid **ärge** määrake välja **URL**.</span><span class="sxs-lookup"><span data-stu-id="62a7a-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="62a7a-123">Looge leht.</span><span class="sxs-lookup"><span data-stu-id="62a7a-123">Build the page.</span></span>
1. <span data-ttu-id="62a7a-124">Registreerige leht ja avaldage see.</span><span class="sxs-lookup"><span data-stu-id="62a7a-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="62a7a-125">4xx ja 5xx olekukoodi tõrgete jaoks saate luua eraldi olekukoodi tõrkevastuse lehed.</span><span class="sxs-lookup"><span data-stu-id="62a7a-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="62a7a-126">Teise võimalusena saate mõlema tõrkekategooria puhul kasutada sama üldist olekukoodi tõrkevastuse lehte.</span><span class="sxs-lookup"><span data-stu-id="62a7a-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="62a7a-127">Olekukoodi tõrkevastuse lehe ümbersuunamise määramine</span><span class="sxs-lookup"><span data-stu-id="62a7a-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="62a7a-128">Olekukoodi tõrkevastuse lehe ümbersuunamise määramiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62a7a-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="62a7a-129">Avage **URL-id \> Uus \> Uus pseudonüüm** ja valige varem loodud olekukoodi tõrkevastuse leht.</span><span class="sxs-lookup"><span data-stu-id="62a7a-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="62a7a-130">Väljale **Pseudonüüm** sisestage kas **vaikimisi 4xx** või **vaikimisi 5xx**, olenevalt olekukoodi tõrkevastuse lehest, mille ümbersuunamise jaoks määrate.</span><span class="sxs-lookup"><span data-stu-id="62a7a-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="62a7a-131">Need pseudonüümid tuleb avaldada.</span><span class="sxs-lookup"><span data-stu-id="62a7a-131">These aliases must be published.</span></span> <span data-ttu-id="62a7a-132">Vastasel korral ümbersuunamine ei tööta.</span><span class="sxs-lookup"><span data-stu-id="62a7a-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="62a7a-133">Linkimise kinnitamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="62a7a-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="62a7a-134">Kui kasutate mõlema tõrkekategooria jaoks ühte olekukoodi tõrkevastuse lehte, korrake seda protseduuri samale lehele teise tõrkekategooria pseudonüümi linkimiseks.</span><span class="sxs-lookup"><span data-stu-id="62a7a-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62a7a-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="62a7a-135">Additional resources</span></span>

[<span data-ttu-id="62a7a-136">Mallidega töötamine</span><span class="sxs-lookup"><span data-stu-id="62a7a-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="62a7a-137">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="62a7a-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="62a7a-138">Lehe URL-i loomine</span><span class="sxs-lookup"><span data-stu-id="62a7a-138">Create a page URL</span></span>](create-page-url.md)
