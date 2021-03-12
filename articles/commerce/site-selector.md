---
title: Saidi valija moodul
description: See teema hõlmab saidi valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: ed00836c435bd391e5edef1f6a99889c80f45211
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985582"
---
# <a name="site-selector-module"></a><span data-ttu-id="74507-103">Saidi valija moodul</span><span class="sxs-lookup"><span data-stu-id="74507-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="74507-104">See teema hõlmab saidi valija moodulit ja kirjeldab, kuidas seda rakenduses Microsoft Dynamics 365 Commerce saidi lehtedele lisada.</span><span class="sxs-lookup"><span data-stu-id="74507-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74507-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="74507-105">Overview</span></span>

<span data-ttu-id="74507-106">Kui ettevõttel on eri turgudel, piirkondadel ja lokaatidel erinevad saidid, on saidi kasutajatel vaja hõlpsasti liikuda saitide vahel ja valida enda eelistatud ostlemissait.</span><span class="sxs-lookup"><span data-stu-id="74507-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="74507-107">Selle stsenaariumi võimaldamiseks saavad kasutajad saidi valija moodulis sirvida mitmel saidil.</span><span class="sxs-lookup"><span data-stu-id="74507-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="74507-108">Saidi valija moodulis tuleb konfigureerida saitide loend (turud, piirkonnad või lokaadid), millel saidi kasutajad saavad sirvida.</span><span class="sxs-lookup"><span data-stu-id="74507-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="74507-109">Saidi valija moodul on saadaval rakenduse Dynamics 365 Commerce väljalaskes 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="74507-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="74507-110">Järgmisel joonisel on kujutatud saidi lehe päises esiletõstetud saidi valija mooduli näide.</span><span class="sxs-lookup"><span data-stu-id="74507-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Saidi valija mooduli näide saidi lehe päises](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="74507-112">Saidi valija mooduli atribuudid</span><span class="sxs-lookup"><span data-stu-id="74507-112">Site selector module properties</span></span>

| <span data-ttu-id="74507-113">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="74507-113">Property name</span></span> | <span data-ttu-id="74507-114">Väärtus</span><span class="sxs-lookup"><span data-stu-id="74507-114">Value</span></span>                 | <span data-ttu-id="74507-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="74507-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="74507-116">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="74507-116">Heading</span></span>       | <span data-ttu-id="74507-117">Tekst</span><span class="sxs-lookup"><span data-stu-id="74507-117">Text</span></span>                  | <span data-ttu-id="74507-118">Mooduli pealkiri.</span><span class="sxs-lookup"><span data-stu-id="74507-118">The heading for the module.</span></span> |
| <span data-ttu-id="74507-119">Saidisuvandid</span><span class="sxs-lookup"><span data-stu-id="74507-119">Site options</span></span>  | <span data-ttu-id="74507-120">Nimi, pilt, URL</span><span class="sxs-lookup"><span data-stu-id="74507-120">Name, Image, URL</span></span>      | <span data-ttu-id="74507-121">See atribuut määrab nime, lingi saidi avalehele ja valikulise pildi, mida kuvatakse iga moodulisse lisatud saidi jaoks.</span><span class="sxs-lookup"><span data-stu-id="74507-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="74507-122">Pildiks võib olla lipp või midagi muud, mis tähistab turgu, piirkonda või lokaati.</span><span class="sxs-lookup"><span data-stu-id="74507-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="74507-123">Saidi valija mooduli lehele lisamine</span><span class="sxs-lookup"><span data-stu-id="74507-123">Add a site selector module to a page</span></span>

<span data-ttu-id="74507-124">Saidi valija moodulit saab lisada saidi valija pesa [päise moodulisse](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="74507-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="74507-125">Pärast selle lisamist saate määratleda mooduli pealkirja ja saidi suvandid.</span><span class="sxs-lookup"><span data-stu-id="74507-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74507-126">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="74507-126">Additional resources</span></span>

[<span data-ttu-id="74507-127">Mooduliteegi ülevaade</span><span class="sxs-lookup"><span data-stu-id="74507-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="74507-128">Päisemoodul</span><span class="sxs-lookup"><span data-stu-id="74507-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="74507-129">Lingireamoodul</span><span class="sxs-lookup"><span data-stu-id="74507-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="74507-130">Navigeerimismenüü moodul</span><span class="sxs-lookup"><span data-stu-id="74507-130">Navigation menu module</span></span>](nav-menu-module.md)
