---
title: Hankekataloogi loomine
description: Selles teemas selgitatakse, kuidas luua hankekataloogi.
author: mkirknel
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55bc7479ca9ba3ca86e23b5bee106ef169c40077
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836376"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="599a8-103">Hankekataloogi loomine</span><span class="sxs-lookup"><span data-stu-id="599a8-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="599a8-104">Selles teemas selgitatakse, kuidas luua hankekataloogi.</span><span class="sxs-lookup"><span data-stu-id="599a8-104">This topic explains how to create a procurement catalog.</span></span> <span data-ttu-id="599a8-105">Seda ülesannet täidab tavaliselt hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="599a8-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="599a8-106">Samuti saate teada, kuidas töötajad saavad kataloogi ostutellimuse loomisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="599a8-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="599a8-107">Enne kataloogi loomist peab teie süsteemis olema hankekategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="599a8-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="599a8-108">Uus kataloog pärib hierarhia koos kõigi hierarhias olevate toodetega.</span><span class="sxs-lookup"><span data-stu-id="599a8-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="599a8-109">Saate kasutada seda juhendit demoandmete ettevõttes USMF, kus on saadaval hankekategooria hierarhia ja näited, mida protseduuri toimingutes kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="599a8-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="599a8-110">Veenduge, et hankekategooria hierarhia on olemas</span><span class="sxs-lookup"><span data-stu-id="599a8-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="599a8-111">Avage **Navigeerimispaan > Moodulid > Hanked > Hanke kategooriad**.</span><span class="sxs-lookup"><span data-stu-id="599a8-111">Go to **navigation pane > Modules > Procurement and sourcing > Procurement categories**.</span></span> <span data-ttu-id="599a8-112">Demoandmete ettevõttes USMF on saadaval hanke kategooriahierarhia ja tooted on lisatud kategooriasse **Kontoriseadmed/arvutid**.</span><span class="sxs-lookup"><span data-stu-id="599a8-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the **Office machines/Computers** category.</span></span> <span data-ttu-id="599a8-113">Kui käitate seda protseduuri ülesandejuhendina, tuleb juhend lukust avada, kui soovite kategoorias sirvida.</span><span class="sxs-lookup"><span data-stu-id="599a8-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="599a8-114">Kui hierarhiat polnud saadaval, tuleb see luua, klõpsates valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="599a8-114">If a hierarchy was not available, you’d create it by clicking **New**.</span></span> <span data-ttu-id="599a8-115">Seda saab teha ainult ühe korra.</span><span class="sxs-lookup"><span data-stu-id="599a8-115">This can only be done once.</span></span>  
2. <span data-ttu-id="599a8-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="599a8-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="599a8-117">Kataloogi loomine</span><span class="sxs-lookup"><span data-stu-id="599a8-117">Create a catalog</span></span>
1. <span data-ttu-id="599a8-118">Avage **Navigeerimispaan > Moodulid > Hanked > Kataloogid > Hankekataloogid**.</span><span class="sxs-lookup"><span data-stu-id="599a8-118">Go to **navigation pane > Modules > Procurement and sourcing > Catalogs > Procurement catalogs**.</span></span>
2. <span data-ttu-id="599a8-119">Rippdialoogi avamiseks klõpsake valikut **Uus hankekataloog**.</span><span class="sxs-lookup"><span data-stu-id="599a8-119">Select **New procurement catalog** to open the drop dialog.</span></span>
3. <span data-ttu-id="599a8-120">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="599a8-120">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="599a8-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="599a8-121">Select **OK**.</span></span>
5. <span data-ttu-id="599a8-122">Laiendage puul valikut **ETTEVÕTTE HANKEKATEGOORIAD**.</span><span class="sxs-lookup"><span data-stu-id="599a8-122">In the tree, expand **CORP PROCUREMENT CATEGORIES**.</span></span>
6. <span data-ttu-id="599a8-123">Laiendage puul valikut **KONTORSEADMED**.</span><span class="sxs-lookup"><span data-stu-id="599a8-123">In the tree, expand **OFFICE MACHINES**.</span></span>
7. <span data-ttu-id="599a8-124">Valige puult **Arvutid**.</span><span class="sxs-lookup"><span data-stu-id="599a8-124">In the tree, select **Computers**.</span></span>

  - <span data-ttu-id="599a8-125">Hankekategooria tooted kuvatakse loendis.</span><span class="sxs-lookup"><span data-stu-id="599a8-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="599a8-126">Kui soovite lisada toote kategooriasse, tuleb seda teha lehel **Hankekategooria hierarhia** või lehel **Kauba üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="599a8-126">If you want to add a product to the category you need to do this on the **Procurement category hierarchy** page or on the **Item details** page.</span></span>  
  - <span data-ttu-id="599a8-127">**Vaikimisi** värskendamise tüüp määrab, kas uued tooted, mis on hankekategooria hierarhiasse lisatud, on kataloogis kohe näha.</span><span class="sxs-lookup"><span data-stu-id="599a8-127">The **Default** update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="599a8-128">Kui värskenduse tüübiks on määratud **Dünaamiline**, on muudatused kohe näha.</span><span class="sxs-lookup"><span data-stu-id="599a8-128">If the update type is set to **Dynamic**, changes are visible immediately.</span></span> <span data-ttu-id="599a8-129">Kui värskenduse tüüp on **Staatiline**, on uued tooted kataloogi kasutavatele inimestele nähtavad alles pärast kataloogi uuesti avaldamist.</span><span class="sxs-lookup"><span data-stu-id="599a8-129">If the update type is **Static**, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="599a8-130">Toiming **Avalda** on saadaval tegumiribal lehe ülaosas.</span><span class="sxs-lookup"><span data-stu-id="599a8-130">The **Publish** action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="599a8-131">Kui tooteid hankekategooria hierarhiast eemaldatakse, on muudatus kohe näha, olenemata väärtusest väljal **Vaikimisi** värskendamise tüüp.</span><span class="sxs-lookup"><span data-stu-id="599a8-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the **Default** update type field.</span></span>  

8. <span data-ttu-id="599a8-132">Valige toimingupaanil **Kategooria navigeerimine** ja veenduge, et suvand **Luba** oleks valitud.</span><span class="sxs-lookup"><span data-stu-id="599a8-132">On the Action Pane, select **Category navigation** and ensure that **Enable** is selected.</span></span>
9. <span data-ttu-id="599a8-133">Valige **Aktiveeri kataloog**.</span><span class="sxs-lookup"><span data-stu-id="599a8-133">Select **Activate catalog**.</span></span>
10. <span data-ttu-id="599a8-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="599a8-134">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="599a8-135">Tehke kataloog nähtavaks</span><span class="sxs-lookup"><span data-stu-id="599a8-135">Make the catalog visible</span></span>
1. <span data-ttu-id="599a8-136">Avage navigeerimispaanil **Moodulid > Hange > Häälestus > Poliitika > Ostupoliitika**.</span><span class="sxs-lookup"><span data-stu-id="599a8-136">Go to **navigation pane > Modules > Procurement and sourcing > Setup > Policies > Purchasing policies**.</span></span>
2. <span data-ttu-id="599a8-137">Valige **Hankepoliitika USMF**.</span><span class="sxs-lookup"><span data-stu-id="599a8-137">Select **Procurement Policy USMF**.</span></span> <span data-ttu-id="599a8-138">Peate valima ostupoliitika sellele juriidilisele isikule, milles teie kasutajaprofiiliga seotud töötajal on lubatud tooteid tellida.</span><span class="sxs-lookup"><span data-stu-id="599a8-138">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="599a8-139">Demoandmete USMF puhul on kasutaja Administraator seotud töötajaga nimega **Julia Funderburk** ja viimane tellib USMF-is vaikimisi tooteid.</span><span class="sxs-lookup"><span data-stu-id="599a8-139">In the USMF demo data, the Admin user is connected to the worker called **Julia Funderburk**, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="599a8-140">Valige äsja loodud kataloog.</span><span class="sxs-lookup"><span data-stu-id="599a8-140">Select the catalog that you’ve just created.</span></span>
4. <span data-ttu-id="599a8-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="599a8-141">Select **OK**.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="599a8-142">Kasutage kataloogi</span><span class="sxs-lookup"><span data-stu-id="599a8-142">Use the catalog</span></span>
1. <span data-ttu-id="599a8-143">Avage **Navigeerimispaan > Moodulid > Hanked > Ostutaotlused > Kõik ostutaotlused**.</span><span class="sxs-lookup"><span data-stu-id="599a8-143">Go to **navigation pane > Modules > Procurement and sourcing > Purchase requisitions > All purchase requisitions**.</span></span>
2. <span data-ttu-id="599a8-144">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="599a8-144">Select **New**.</span></span>
3. <span data-ttu-id="599a8-145">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="599a8-145">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="599a8-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="599a8-146">Select **OK**.</span></span>
5. <span data-ttu-id="599a8-147">Valige **Lisa tooteid**.</span><span class="sxs-lookup"><span data-stu-id="599a8-147">Select **Add products**.</span></span>
6. <span data-ttu-id="599a8-148">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="599a8-148">In the list, find and select the desired record.</span></span> <span data-ttu-id="599a8-149">Saate kasutada toodete filtreerimiseks vasakul olevat kategooriahierarhiat või ülal olevat filtrit.</span><span class="sxs-lookup"><span data-stu-id="599a8-149">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="599a8-150">Valige **Lisa ridadele**.</span><span class="sxs-lookup"><span data-stu-id="599a8-150">Select **Add to lines**.</span></span>
8. <span data-ttu-id="599a8-151">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="599a8-151">Select **OK**.</span></span>

