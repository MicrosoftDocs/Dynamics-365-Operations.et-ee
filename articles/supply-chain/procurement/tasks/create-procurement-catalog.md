---
title: Hankekataloogi loomine
description: Selles juhendis näidatakse, kuidas hankekataloogi luua.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcCategoryHierarchyManagement, CatProcureCatalogListPage, CatProcureCatalogCreate, CatProcureCatalogEdit, SysPolicyListPage, SysPolicy, CatCatalogPolicyRule, PurchReqTableListPage, PurchReqCreate, PurchReqTable, PurchReqAddItem
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6f2a010e21f16b3908a6ee5f18d8f144c5130be7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547648"
---
# <a name="create-a-procurement-catalog"></a><span data-ttu-id="89cb6-103">Hankekataloogi loomine</span><span class="sxs-lookup"><span data-stu-id="89cb6-103">Create a procurement catalog</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89cb6-104">Selles juhendis näidatakse, kuidas hankekataloogi luua.</span><span class="sxs-lookup"><span data-stu-id="89cb6-104">This guide shows you how to create a procurement catalog.</span></span> <span data-ttu-id="89cb6-105">Seda ülesannet täidab tavaliselt hankespetsialist.</span><span class="sxs-lookup"><span data-stu-id="89cb6-105">This task would typically be carried out by a procurement professional.</span></span> <span data-ttu-id="89cb6-106">Samuti saate teada, kuidas töötajad saavad kataloogi ostutellimuse loomisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="89cb6-106">You will also learn how employees can use the catalog when they create a requisition.</span></span> <span data-ttu-id="89cb6-107">Enne kataloogi loomist peab teie süsteemis olema hankekategooria hierarhia.</span><span class="sxs-lookup"><span data-stu-id="89cb6-107">Before you can create a catalog, there must be a procurement category hierarchy in your system.</span></span> <span data-ttu-id="89cb6-108">Uus kataloog pärib hierarhia koos kõigi hierarhias olevate toodetega.</span><span class="sxs-lookup"><span data-stu-id="89cb6-108">The hierarchy is inherited by the new catalog, along with all the products that are in the hierarchy.</span></span> <span data-ttu-id="89cb6-109">Saate kasutada seda juhendit demoandmete ettevõttes USMF, kus on saadaval hankekategooria hierarhia ja näited, mida protseduuri toimingutes kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="89cb6-109">You can use this guide in demo data company USMF where the procurement category hierarchy is available, as well as the examples used in the procedure steps.</span></span>


## <a name="ensure-that-a-procurement-category-hierarchy-exists"></a><span data-ttu-id="89cb6-110">Veenduge, et hankekategooria hierarhia on olemas</span><span class="sxs-lookup"><span data-stu-id="89cb6-110">Ensure that a procurement category hierarchy exists</span></span>
1. <span data-ttu-id="89cb6-111">Tehke valik Hanked > Hankekategooriad.</span><span class="sxs-lookup"><span data-stu-id="89cb6-111">Go to Procurement and sourcing > Procurement categories.</span></span>
    * <span data-ttu-id="89cb6-112">Demoandmete ettevõttes USMF on saadaval hanke kategooriahierarhia ja tooted on lisatud kategooriasse Kontoriseadmed/arvutid.</span><span class="sxs-lookup"><span data-stu-id="89cb6-112">A procurement category hierarchy is available in the USMF demo data company and products have been added to the Office machines/Computers category.</span></span> <span data-ttu-id="89cb6-113">Kui käitate seda protseduuri ülesandejuhendina, tuleb juhend lukust avada, kui soovite kategoorias sirvida.</span><span class="sxs-lookup"><span data-stu-id="89cb6-113">If you’re running this procedure as a task guide, you’ll need to unlock the guide if you want to browse through the category.</span></span> <span data-ttu-id="89cb6-114">Kui hierarhiat polnud saadaval, tuleb see luua, klõpsates valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="89cb6-114">If a hierarchy was not available, you’d create it by clicking New.</span></span> <span data-ttu-id="89cb6-115">Seda saab teha ainult ühe korra.</span><span class="sxs-lookup"><span data-stu-id="89cb6-115">This can only be done once.</span></span>  
2. <span data-ttu-id="89cb6-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cb6-116">Close the page.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="89cb6-117">Kataloogi loomine</span><span class="sxs-lookup"><span data-stu-id="89cb6-117">Create a catalog</span></span>
1. <span data-ttu-id="89cb6-118">Valige Hanked > Kataloogid > Hankekataloogid.</span><span class="sxs-lookup"><span data-stu-id="89cb6-118">Go to Procurement and sourcing > Catalogs > Procurement catalogs.</span></span>
2. <span data-ttu-id="89cb6-119">Rippdialoogi avamiseks klõpsake valikut Uus hankekataloog.</span><span class="sxs-lookup"><span data-stu-id="89cb6-119">Click New procurement catalog to open the drop dialog.</span></span>
3. <span data-ttu-id="89cb6-120">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="89cb6-120">In the Name field, type a value.</span></span>
4. <span data-ttu-id="89cb6-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="89cb6-121">Click OK.</span></span>
5. <span data-ttu-id="89cb6-122">Laiendage puul valikut ETTEV. HANKEKATEGOORIAD.</span><span class="sxs-lookup"><span data-stu-id="89cb6-122">In the tree, expand 'CORP PROCUREMENT CATEGORIES'.</span></span>
6. <span data-ttu-id="89cb6-123">Laiendage puul valikut KONTORSEADMED.</span><span class="sxs-lookup"><span data-stu-id="89cb6-123">In the tree, expand 'OFFICE MACHINES'.</span></span>
7. <span data-ttu-id="89cb6-124">Valige puult Arvutid.</span><span class="sxs-lookup"><span data-stu-id="89cb6-124">In the tree, select 'Computers'.</span></span>
    * <span data-ttu-id="89cb6-125">Hankekategooria tooted kuvatakse loendis.</span><span class="sxs-lookup"><span data-stu-id="89cb6-125">The products from the procurement category are displayed in the list.</span></span> <span data-ttu-id="89cb6-126">Kui soovite lisada toote kategooriasse, tuleb seda teha lehel Hankekategooria hierarhia või lehel Kauba üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="89cb6-126">If you want to add a product to the category you need to do this on the Procurement category hierarchy page or on the Item details page.</span></span>  
    * <span data-ttu-id="89cb6-127">Vaikimisi värskendamise tüüp määrab, kas uued tooted, mis on hankekategooria hierarhiasse lisatud, on kataloogis kohe näha.</span><span class="sxs-lookup"><span data-stu-id="89cb6-127">The Default update type determines whether new products that have been added to the procurement category hierarchy are immediately visible in the catalog.</span></span> <span data-ttu-id="89cb6-128">Kui värskenduse tüübiks on määratud Dünaamiline, on muudatused kohe näha.</span><span class="sxs-lookup"><span data-stu-id="89cb6-128">If the update type is set to Dynamic, changes are visible immediately.</span></span> <span data-ttu-id="89cb6-129">Kui värskenduse tüüp on Staatiline, on uued tooted kataloogi kasutavatele inimestele nähtavad alles pärast kataloogi uuesti avaldamist.</span><span class="sxs-lookup"><span data-stu-id="89cb6-129">If the update type is Static, new products are only visible to people using the catalog after the catalog has been re-published.</span></span> <span data-ttu-id="89cb6-130">Toiming Avalda on saadaval tegumiribal lehe ülaosas.</span><span class="sxs-lookup"><span data-stu-id="89cb6-130">The Publish action is available on the Action Pane at the top of the page.</span></span> <span data-ttu-id="89cb6-131">Kui tooteid hankekategooria hierarhiast eemaldatakse, on muudatus kohe näha, olenemata väärtusest väljal Vaikimisi värskendamise tüüp.</span><span class="sxs-lookup"><span data-stu-id="89cb6-131">If products are removed from the procurement category hierarchy, the change is immediately visible, regardless of the value in the Default update type field.</span></span>  
8. <span data-ttu-id="89cb6-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="89cb6-132">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="89cb6-133">Klõpsake käsku Peida.</span><span class="sxs-lookup"><span data-stu-id="89cb6-133">Click Hide.</span></span>
10. <span data-ttu-id="89cb6-134">Klõpsake toimingupaanil valikut Kategooria navigeerimine.</span><span class="sxs-lookup"><span data-stu-id="89cb6-134">On the Action Pane, click Category navigation.</span></span>
11. <span data-ttu-id="89cb6-135">Klõpsake käsku Keela.</span><span class="sxs-lookup"><span data-stu-id="89cb6-135">Click Disable.</span></span>
12. <span data-ttu-id="89cb6-136">Klõpsake toimingupaanil valikut Kategooria navigeerimine.</span><span class="sxs-lookup"><span data-stu-id="89cb6-136">On the Action Pane, click Category navigation.</span></span>
13. <span data-ttu-id="89cb6-137">Klõpsake käsku Luba.</span><span class="sxs-lookup"><span data-stu-id="89cb6-137">Click Enable.</span></span>
14. <span data-ttu-id="89cb6-138">Klõpsake käsku Aktiveeri kataloog.</span><span class="sxs-lookup"><span data-stu-id="89cb6-138">Click Activate catalog.</span></span>
15. <span data-ttu-id="89cb6-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cb6-139">Close the page.</span></span>

## <a name="make-the-catalog-visible"></a><span data-ttu-id="89cb6-140">Tehke kataloog nähtavaks</span><span class="sxs-lookup"><span data-stu-id="89cb6-140">Make the catalog visible</span></span>
1. <span data-ttu-id="89cb6-141">Valige Hanked > Seadistus > Poliitikad > Ostupoliitikad.</span><span class="sxs-lookup"><span data-stu-id="89cb6-141">Go to Procurement and sourcing > Setup > Policies > Purchasing policies.</span></span>
2. <span data-ttu-id="89cb6-142">Valige Hankepoliitika USMF.</span><span class="sxs-lookup"><span data-stu-id="89cb6-142">Select Procurement Policy USMF.</span></span>
    * <span data-ttu-id="89cb6-143">Peate valima ostupoliitika sellele juriidilisele isikule, milles teie kasutajaprofiiliga seotud töötajal on lubatud tooteid tellida.</span><span class="sxs-lookup"><span data-stu-id="89cb6-143">You need to select the purchasing policy for the legal entity that the worker connected to your user profile is allowed to order products in.</span></span> <span data-ttu-id="89cb6-144">Demoandmete USMF puhul on kasutaja Administraator seotud töötajaga nimega Julia Funderburk ja viimane tellib USMF-is vaikimisi tooteid.</span><span class="sxs-lookup"><span data-stu-id="89cb6-144">In the USMF demo data, the Admin user is connected to the worker called Julia Funderburk, and she orders products in USMF by default.</span></span>  
3. <span data-ttu-id="89cb6-145">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="89cb6-145">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="89cb6-146">Valige äsja loodud kataloog.</span><span class="sxs-lookup"><span data-stu-id="89cb6-146">Select the catalog that you’ve just created.</span></span>
5. <span data-ttu-id="89cb6-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="89cb6-147">Click OK.</span></span>
6. <span data-ttu-id="89cb6-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cb6-148">Close the page.</span></span>
7. <span data-ttu-id="89cb6-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="89cb6-149">Close the page.</span></span>

## <a name="use-the-catalog"></a><span data-ttu-id="89cb6-150">Kasutage kataloogi</span><span class="sxs-lookup"><span data-stu-id="89cb6-150">Use the catalog</span></span>
1. <span data-ttu-id="89cb6-151">Valige Hanked > Ostutaotlused > Kõik ostutaotlused.</span><span class="sxs-lookup"><span data-stu-id="89cb6-151">Go to Procurement and sourcing > Purchase requisitions > All purchase requisitions.</span></span>
2. <span data-ttu-id="89cb6-152">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="89cb6-152">Click New.</span></span>
3. <span data-ttu-id="89cb6-153">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="89cb6-153">In the Name field, type a value.</span></span>
4. <span data-ttu-id="89cb6-154">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="89cb6-154">Click OK.</span></span>
5. <span data-ttu-id="89cb6-155">Klõpsake suvandit Lisa tooteid.</span><span class="sxs-lookup"><span data-stu-id="89cb6-155">Click Add products.</span></span>
6. <span data-ttu-id="89cb6-156">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="89cb6-156">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="89cb6-157">Saate kasutada toodete filtreerimiseks vasakul olevat kategooriahierarhiat või ülal olevat filtrit.</span><span class="sxs-lookup"><span data-stu-id="89cb6-157">You can use the category hierarchy on the left or the filter at the top of the list to filter the products.</span></span>  
7. <span data-ttu-id="89cb6-158">Klõpsake suvandit Lisam ridadele.</span><span class="sxs-lookup"><span data-stu-id="89cb6-158">Click Add to lines.</span></span>
8. <span data-ttu-id="89cb6-159">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="89cb6-159">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="89cb6-160">Klõpsake suvandit Lisam ridadele.</span><span class="sxs-lookup"><span data-stu-id="89cb6-160">Click Add to lines.</span></span>
10. <span data-ttu-id="89cb6-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="89cb6-161">Click OK.</span></span>

