---
title: Lehepaigutuste valimine
description: Selles teemas kirjeldatakse, kuidas luua ja valida lehepaigutusi rakenduses Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8f86a0b651bfa16aeb1c483daceed321699ead83
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945647"
---
# <a name="select-page-layouts"></a><span data-ttu-id="53f30-103">Lehepaigutuste valimine</span><span class="sxs-lookup"><span data-stu-id="53f30-103">Select page layouts</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="53f30-104">Selles teemas kirjeldatakse, kuidas luua ja valida lehepaigutusi rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="53f30-104">This topic explains how to create and select page layouts in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="create-layouts-for-an-existing-page"></a><span data-ttu-id="53f30-105">Olemasolevale leheküljele paigutuste loomine</span><span class="sxs-lookup"><span data-stu-id="53f30-105">Create layouts for an existing page</span></span>

> [!NOTE]
> <span data-ttu-id="53f30-106">Saate luua paigutusi olemasolevale lehele ainult siis, kui sellel leheküljel on vähemalt kaks moodulit põhipesa all.</span><span class="sxs-lookup"><span data-stu-id="53f30-106">You can create layouts for an existing page only if that page has at least two modules under the main slot.</span></span>

<span data-ttu-id="53f30-107">Olemasolevale leheküljele paigutuste loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="53f30-107">To create layouts for an existing page, follow these steps.</span></span>

1. <span data-ttu-id="53f30-108">Avage suvand **Lehed** ja leidke loendist olemasolev lehekülg.</span><span class="sxs-lookup"><span data-stu-id="53f30-108">Go to **Pages**, and find the existing page in the list.</span></span> <span data-ttu-id="53f30-109">Vajaduse korral kasutage otsingufunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="53f30-109">Use the search feature as you require.</span></span>
1. <span data-ttu-id="53f30-110">Valige leht, vaadake seda ja seejärel valige see, et leht avada.</span><span class="sxs-lookup"><span data-stu-id="53f30-110">Select the page, check it out, and then select it to open it.</span></span> <span data-ttu-id="53f30-111">Märkige üles mooduli tellimus.</span><span class="sxs-lookup"><span data-stu-id="53f30-111">Make a note of the module order.</span></span>
1. <span data-ttu-id="53f30-112">Valige suvand **Salvesta uue paigutusena**.</span><span class="sxs-lookup"><span data-stu-id="53f30-112">Select **Save as New Layout**.</span></span>
1. <span data-ttu-id="53f30-113">Sisestage paigutuse nimi ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="53f30-113">Enter a name for the layout, and then select **OK**.</span></span>
1. <span data-ttu-id="53f30-114">Valige suvand **Teisenda manustatud paigutuseks**.</span><span class="sxs-lookup"><span data-stu-id="53f30-114">Select **Convert to Embedded Layout**.</span></span>
1. <span data-ttu-id="53f30-115">Muutke vajadusel moodulite järjestust ja märkige uus tellimus.</span><span class="sxs-lookup"><span data-stu-id="53f30-115">Change the order of the modules as you require, and make a note of the new order.</span></span>
1. <span data-ttu-id="53f30-116">Valige suvand **Salvesta uue paigutusena**.</span><span class="sxs-lookup"><span data-stu-id="53f30-116">Select **Save as New Layout**.</span></span>
1. <span data-ttu-id="53f30-117">Sisestage paigutuse nimi ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="53f30-117">Enter a name for the layout, and then select **OK**.</span></span>
1. <span data-ttu-id="53f30-118">Valige suvand **Muuda kavandit**, valige esimene loodud paigutus ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="53f30-118">Select **Change Layout**, select the first layout that you created, and then select **OK**.</span></span> <span data-ttu-id="53f30-119">Märkige üles mooduli tellimus.</span><span class="sxs-lookup"><span data-stu-id="53f30-119">Make a note of the module order.</span></span> <span data-ttu-id="53f30-120">Muutke seda nii, et see ühtiks paigutusega salvestatud mooduli tellimuses.</span><span class="sxs-lookup"><span data-stu-id="53f30-120">Change it so that it matches the module order that was saved with the layout.</span></span>

## <a name="select-a-different-layout-for-an-existing-page"></a><span data-ttu-id="53f30-121">Olemasoleva lehekülje jaoks mõne muu paigutuse valimine</span><span class="sxs-lookup"><span data-stu-id="53f30-121">Select a different layout for an existing page</span></span>

> [!NOTE]
> <span data-ttu-id="53f30-122">Saate valida olemasolevale leheküljele mõne muu paigutuse ainult juhul, kui selle lehe loomiseks kasutatud mallil on rohkem kui üks paigutus.</span><span class="sxs-lookup"><span data-stu-id="53f30-122">You can select a different layout for an existing page only if the template that was used to create that page has more than one layout.</span></span>

<span data-ttu-id="53f30-123">Muu paigutuse valimiseks olemasoleva lehe jaoks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="53f30-123">To select a different layout for an existing page, follow these steps.</span></span>

1. <span data-ttu-id="53f30-124">Avage suvand **Lehed** ja leidke loendist olemasolev lehekülg.</span><span class="sxs-lookup"><span data-stu-id="53f30-124">Go to **Pages**, and find the existing page in the list.</span></span> <span data-ttu-id="53f30-125">Vajaduse korral kasutage otsingufunktsiooni.</span><span class="sxs-lookup"><span data-stu-id="53f30-125">Use the search feature as you require.</span></span>
1. <span data-ttu-id="53f30-126">Valige leht, vaadake seda ja seejärel valige see, et leht avada.</span><span class="sxs-lookup"><span data-stu-id="53f30-126">Select the page, check it out, and then select it to open it.</span></span>
1. <span data-ttu-id="53f30-127">Valige suvand **Muuda paigutust**.</span><span class="sxs-lookup"><span data-stu-id="53f30-127">Select **Change layout**.</span></span>
1. <span data-ttu-id="53f30-128">Valige lehe jaoks uus paigutus ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="53f30-128">Select the new layout for the page, and then select **OK**.</span></span> <span data-ttu-id="53f30-129">Lehe redaktor värskendatakse uue paigutuse kuvamiseks.</span><span class="sxs-lookup"><span data-stu-id="53f30-129">The page editor is refreshed to show the new layout.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="53f30-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="53f30-130">Additional resources</span></span>

[<span data-ttu-id="53f30-131">Olemasoleva saidilehe muutmine</span><span class="sxs-lookup"><span data-stu-id="53f30-131">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="53f30-132">Uue saidilehe lisamine</span><span class="sxs-lookup"><span data-stu-id="53f30-132">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="53f30-133">SEO metaandmete haldamine</span><span class="sxs-lookup"><span data-stu-id="53f30-133">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="53f30-134">Lehe salvestamine, eelvaade ja avaldamine</span><span class="sxs-lookup"><span data-stu-id="53f30-134">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="53f30-135">Tootelehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="53f30-135">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="53f30-136">Kategooria sihtlehe rikastamine</span><span class="sxs-lookup"><span data-stu-id="53f30-136">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="53f30-137">Lehe sisu hõlbustusfunktsioonide kinnitamine</span><span class="sxs-lookup"><span data-stu-id="53f30-137">Verify page content accessibility</span></span>](verify-accessibility.md)

