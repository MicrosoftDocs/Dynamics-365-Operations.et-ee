---
title: Uue tootehierarhia loomine
description: Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus tootehierarhia.
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
ms.openlocfilehash: 73cecb0c6aacebf5c6fcf8a0edbc7513b3ce175d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001894"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="19fd7-103">Uue tootehierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="19fd7-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="19fd7-104">Selles teemas kirjeldatakse, kuidas luua rakenduses Microsoft Dynamics 365 Commerce uus tootehierarhia.</span><span class="sxs-lookup"><span data-stu-id="19fd7-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="19fd7-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="19fd7-105">Overview</span></span>

<span data-ttu-id="19fd7-106">Dynamics 365 Commerce toetab mitut jaemüügikanalit.</span><span class="sxs-lookup"><span data-stu-id="19fd7-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="19fd7-107">Jaemüügikanalid hõlmavad võrgupoode, kõnekeskusi ja jaekauplusi (neid nimetatakse ka füüsilisteks kauplusteks).</span><span class="sxs-lookup"><span data-stu-id="19fd7-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="19fd7-108">Igal kaupluse kanalil võivad olla oma makseviisid, hinnagrupid, kassaregistrid, tulu- ja kulukontod ning personal.</span><span class="sxs-lookup"><span data-stu-id="19fd7-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="19fd7-109">Enne jaekaupluse kanali loomist tuleb seadistada kõik need elemendid.</span><span class="sxs-lookup"><span data-stu-id="19fd7-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="19fd7-110">Commerce'i tootehierarhiat kasutatakse organisatsiooni üldise tootehierarhia määramiseks.</span><span class="sxs-lookup"><span data-stu-id="19fd7-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="19fd7-111">Saate Commerce'i tootehierarhiat kasutada tootesündmuste, hinnakujunduse ja kampaaniate, aruandluse ning sortimendi planeerimise jaoks.</span><span class="sxs-lookup"><span data-stu-id="19fd7-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="19fd7-112">Ühe organisatsiooni kohta saab määrata ainult ühe Commerce'i tootehierarhia.</span><span class="sxs-lookup"><span data-stu-id="19fd7-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="19fd7-113">Tootehierarhia loomine ja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="19fd7-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="19fd7-114">Commerce'i tootehierarhia loomiseks ja konfigureerimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="19fd7-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="19fd7-115">Avage navigeerimispaanil **Moodulid \> Jaemüük ja kaubandus \> Tooted ja kategooriad \> Commerce'i tootehierarhia**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="19fd7-116">Kui ühtegi hierachy pole veel olemas, valige **Tegevuspaanil** suvand **Uus**, et luua hierarhia juur.</span><span class="sxs-lookup"><span data-stu-id="19fd7-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="19fd7-117">Jaotises **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-117">Under **General**:</span></span>
    1. <span data-ttu-id="19fd7-118">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="19fd7-119">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="19fd7-120">Sisestage hüüdnimi väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="19fd7-121">Seadistage **Aktiivne** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="19fd7-122">Hierarhiasõlmede lisamine</span><span class="sxs-lookup"><span data-stu-id="19fd7-122">Add hierarchy nodes</span></span>

<span data-ttu-id="19fd7-123">Hierarhiasõlmede lisamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="19fd7-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="19fd7-124">Valige toimingupaanil **Kategooriahierarhia muutmine**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="19fd7-125">Valige peamine sõlm, millele soovite lisada uue sõlme, ja seejärel valige **Uus kategooria sõlm**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="19fd7-126">Sisestage jaotises **Üldine** väärtused **Nimi**, **Kirjeldus**, **Hüüdnimi** ja **Märksõnad**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="19fd7-127">Jaotises **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-127">Under **General**:</span></span>
    1. <span data-ttu-id="19fd7-128">Sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="19fd7-129">Sisestage kirjeldus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="19fd7-130">Sisestage hüüdnimi väljale **Hüüdnimi**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="19fd7-131">Sisestage väljale **Märksõnad** asjakohased märksõnad.</span><span class="sxs-lookup"><span data-stu-id="19fd7-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="19fd7-132">Sisestage väljale **Kuva järjekord** kuva järjekorda tähistav number (valikuline).</span><span class="sxs-lookup"><span data-stu-id="19fd7-132">In the **Display order**box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="19fd7-133">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="19fd7-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="19fd7-134">Täiendavate sõlmede lisamiseks korrake ülaltoodud samme.</span><span class="sxs-lookup"><span data-stu-id="19fd7-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="19fd7-135">Järgmine pilt näitab uue tootehierarhia sõlme loomist.</span><span class="sxs-lookup"><span data-stu-id="19fd7-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Tootehierarhia loomine](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="19fd7-137">Muud sätted</span><span class="sxs-lookup"><span data-stu-id="19fd7-137">Other settings</span></span>

<span data-ttu-id="19fd7-138">Kategooria atribuudigruppe saab vajadusel määrata ka igale grupile.</span><span class="sxs-lookup"><span data-stu-id="19fd7-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="19fd7-139">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="19fd7-139">Additional resources</span></span>

[<span data-ttu-id="19fd7-140">Jaemüügihierarhiad</span><span class="sxs-lookup"><span data-stu-id="19fd7-140">Retail hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="19fd7-141">Tootekategooriate ja toodete haldamine</span><span class="sxs-lookup"><span data-stu-id="19fd7-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="19fd7-142">Kaubastatavate üksuste sortimisjärjestuse muutmine</span><span class="sxs-lookup"><span data-stu-id="19fd7-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)
