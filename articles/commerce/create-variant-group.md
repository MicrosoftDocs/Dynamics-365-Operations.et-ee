---
title: Variandi grupi loomine
description: See teema kirjeldab, kuidas luua Microsoftis Dynamics 365 Commerce'is tootele suuruse-, stiili- või värvivariandi grupp.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001871"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="d344d-103">Variandi grupi loomine</span><span class="sxs-lookup"><span data-stu-id="d344d-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d344d-104">See teema kirjeldab, kuidas luua Microsoftis Dynamics 365 Commerce'is tootele suuruse-, stiili- või värvivariandi grupp.</span><span class="sxs-lookup"><span data-stu-id="d344d-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d344d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="d344d-105">Overview</span></span>

<span data-ttu-id="d344d-106">Dynamics 365 Commerce toetab mitmeid toodete variante.</span><span class="sxs-lookup"><span data-stu-id="d344d-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="d344d-107">See on ideaalne erinevate tootekategooriate jaoks variandigruppide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="d344d-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="d344d-108">Näiteks saab t-särkide puhul luua suuruse grupi suurustega XS, S, M, L ja XL või värvigrupi, mis sisaldaks toote kõiki saadaolevaid värve.</span><span class="sxs-lookup"><span data-stu-id="d344d-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="d344d-109">Variandigrupid tuleb lisada enne toodete lisamist.</span><span class="sxs-lookup"><span data-stu-id="d344d-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="d344d-110">Selles teemas luuakse ja konfigureeritakse suuruse grupp.</span><span class="sxs-lookup"><span data-stu-id="d344d-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="d344d-111">Sarnase toiminguga saab lisada ja konfigureerida ka stiili- ja värvigruppe.</span><span class="sxs-lookup"><span data-stu-id="d344d-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="d344d-112">Suuruse grupi loomine</span><span class="sxs-lookup"><span data-stu-id="d344d-112">Create a size group</span></span>

<span data-ttu-id="d344d-113">Suuruse grupi loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="d344d-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="d344d-114">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Variandi grupid \> Suuruse grupid**.</span><span class="sxs-lookup"><span data-stu-id="d344d-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="d344d-115">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d344d-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="d344d-116">Sisestage kasti **Suuruse grupp** suuruse grupile nimi.</span><span class="sxs-lookup"><span data-stu-id="d344d-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="d344d-117">Sisestage väljale **Kirjeldus** sobiv kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d344d-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="d344d-118">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d344d-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="d344d-119">Atribuutide lisamine suuruse grupile</span><span class="sxs-lookup"><span data-stu-id="d344d-119">Add attributes to the size group</span></span>

<span data-ttu-id="d344d-120">Suuruse grupile atribuutide lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d344d-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="d344d-121">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Variandi grupid \> Suuruse grupid**</span><span class="sxs-lookup"><span data-stu-id="d344d-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="d344d-122">Valige navigeerimispaanil suuruse grupp.</span><span class="sxs-lookup"><span data-stu-id="d344d-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="d344d-123">Valige jaotises **Suuruse grupi read** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d344d-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="d344d-124">Sisestage kasti **Suurus** suurust esindav string (näiteks "XL").</span><span class="sxs-lookup"><span data-stu-id="d344d-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="d344d-125">Sisestage väljale **Suuruse nimi** suuruse nimi (nt "Eriti suur").</span><span class="sxs-lookup"><span data-stu-id="d344d-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="d344d-126">Sisestage väljale **Täiendamise kaal** täiendamise kaalu tähistav number.</span><span class="sxs-lookup"><span data-stu-id="d344d-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="d344d-127">Sisestage väljale **Triipkoodi number** triipkoodi tähistav number.</span><span class="sxs-lookup"><span data-stu-id="d344d-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="d344d-128">Sisestage väljale **Kuva järjekord** kuva järjekorda tähistav number.</span><span class="sxs-lookup"><span data-stu-id="d344d-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="d344d-129">Kui olete suuruse lisamise lõpetanud, valige tegevuspaanilt **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d344d-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="d344d-130">Järgmine pilt näitab "vabaajasärkide suuruste" suuruse grupi näidet.</span><span class="sxs-lookup"><span data-stu-id="d344d-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Suuruse grupi loomine](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="d344d-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d344d-132">Additional resources</span></span>

[<span data-ttu-id="d344d-133">Tooteteabe ülevaade</span><span class="sxs-lookup"><span data-stu-id="d344d-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="d344d-134">Jaemüügitoodete häälestamine</span><span class="sxs-lookup"><span data-stu-id="d344d-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="d344d-135">Tootedimensioonid</span><span class="sxs-lookup"><span data-stu-id="d344d-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
