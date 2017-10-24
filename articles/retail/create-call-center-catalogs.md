---
title: "Kõnekeskuse kataloogi loomine"
description: "See artikkel annab ülevaate kõnekeskusele kataloogi loomise protsessist."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 16212
ms.assetid: c9d1b9df-82e8-4b3a-a13c-166df8b9718e
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 94ff6d74d4a11b3b04be6b69f85e778c3b45de92
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-call-center-catalog"></a><span data-ttu-id="57ec9-103">Kõnekeskuse kataloogi loomine</span><span class="sxs-lookup"><span data-stu-id="57ec9-103">Create a call center catalog</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="57ec9-104">See artikkel annab ülevaate kõnekeskusele kataloogi loomise protsessist.</span><span class="sxs-lookup"><span data-stu-id="57ec9-104">This article provides an overview of the process for creating a catalog for a call center.</span></span> 

<span data-ttu-id="57ec9-105">Kõnekeskuses saate kasutada tootekatalooge, et tuvastada tooteid, mida soovite klientidele pakkuda.</span><span class="sxs-lookup"><span data-stu-id="57ec9-105">In a call center, you can use product catalogs to identify the products that you want to offer to customers.</span></span> <span data-ttu-id="57ec9-106">Kõnekeskused kasutavad tavaliselt prinditud katalooge.</span><span class="sxs-lookup"><span data-stu-id="57ec9-106">Call centers typically use printed catalogs.</span></span> <span data-ttu-id="57ec9-107">Trükitud kataloogi kujundust ja tootmist hallatakse väljaspool Microsoft Dynamics 365 for Retaili.</span><span class="sxs-lookup"><span data-stu-id="57ec9-107">The design and production of a printed catalog is handled outside Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="57ec9-108">Kuid saate luua ja talletada kataloogi digitaalse vormi, kasutades samu vorme, mida kasutate võrgus jaemüügikataloogide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="57ec9-108">However, you can create and store a digital form of a catalog by using the same forms that you use to set up online retail catalogs.</span></span> <span data-ttu-id="57ec9-109">Enne kataloogi loomist tuleb seadistada toote sortimendid ja määrata sortimendid kõnekeskusele.</span><span class="sxs-lookup"><span data-stu-id="57ec9-109">Before you can create a catalog, you must set up product assortments and assign the assortments to a call center.</span></span> <span data-ttu-id="57ec9-110">Seejärel saate lisada tooteid kataloogi, valides need sortimentidest.</span><span class="sxs-lookup"><span data-stu-id="57ec9-110">You then add products to the catalog by selecting products from these assortments.</span></span> <span data-ttu-id="57ec9-111">Pärast toodete lisamist kataloogi ja kataloogi lõpetamist tuleb kataloog andmete õigsuse kontrollimiseks kinnitada.</span><span class="sxs-lookup"><span data-stu-id="57ec9-111">After products have been added to the catalog, and the catalog is complete, you must validate the catalog to verify the data.</span></span> <span data-ttu-id="57ec9-112">Seejärel tuleb kataloog ülevaatamiseks ja heakskiitmiseks esitada.</span><span class="sxs-lookup"><span data-stu-id="57ec9-112">You must then submit the catalog for review and approval.</span></span> <span data-ttu-id="57ec9-113">Kui kataloog on kinnitatud, võib selle avaldada.</span><span class="sxs-lookup"><span data-stu-id="57ec9-113">After the catalog is approved, it can be published.</span></span> <span data-ttu-id="57ec9-114">Kui kõnekeskuse kataloog on loodud, saate kataloogi avaldamise hetkel kataloogi andmetest hetktõmmise teha.</span><span class="sxs-lookup"><span data-stu-id="57ec9-114">When a call center catalog is created, you can take a snapshot of the catalog data at the time when the catalog is published.</span></span> <span data-ttu-id="57ec9-115">See hetktõmmise funktsioon võimaldab juurdepääsu kataloogi konkreetsele versioonile isegi siis, kui kataloogi hiljem muudetakse ja uuendatakse.</span><span class="sxs-lookup"><span data-stu-id="57ec9-115">This snapshot functionality lets you access a particular version of the catalog even if the catalog is later changed and updated.</span></span> <span data-ttu-id="57ec9-116">Kõnekeskuse kataloogid saab seadistada ka nii, et neis sisalduvad järgmised valikulised funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="57ec9-116">Call center catalogs can also be set up to include the following optional features.</span></span>

-   <span data-ttu-id="57ec9-117">**Lähtekoodid** – koodid, mida kasutatakse kliendi reageeringu jälgimiseks konkreetsetele kataloogipostitustele.</span><span class="sxs-lookup"><span data-stu-id="57ec9-117">**Source codes** – Codes that are used to track the customer response to particular catalog mailings.</span></span>
-   <span data-ttu-id="57ec9-118">**Tasuta tooted** – kliendi tellimusse lisatasudeta kaasatud tooted.</span><span class="sxs-lookup"><span data-stu-id="57ec9-118">**Free products** – Products that are included in a customer's order at no additional charge.</span></span> <span data-ttu-id="57ec9-119">Need tooted lisatakse kataloogi lähtekoodi tellimusse sisestamisel automaatselt tellimusele.</span><span class="sxs-lookup"><span data-stu-id="57ec9-119">These products are automatically added to the order when the source code for the catalog is entered into the order.</span></span>
-   <span data-ttu-id="57ec9-120">**Skriptid** – tekstid, mida kõnekeskuse töötaja kliendile müügitellimuse loomisel ette loeb.</span><span class="sxs-lookup"><span data-stu-id="57ec9-120">**Scripts** – Texts that a call center worker reads to a customer when a sales order is being created.</span></span> <span data-ttu-id="57ec9-121">Skriptid võivad sisaldada tervitusi või ostusoovitusi.</span><span class="sxs-lookup"><span data-stu-id="57ec9-121">Scripts can include greetings or purchase suggestions.</span></span>
-   <span data-ttu-id="57ec9-122">**Kaupade ülesmüük või ristmüük** – tellimusele teatud toote lisamisel soovitusena kuvatavad kaubad.</span><span class="sxs-lookup"><span data-stu-id="57ec9-122">**Upsell or cross-sell items** - Items that are displayed as a suggestion when a specific product is added to the order.</span></span>

<span data-ttu-id="57ec9-123">Need suvandid tuleb seadistada enne kataloogi kinnitamist ja avaldamist.</span><span class="sxs-lookup"><span data-stu-id="57ec9-123">These options must be set up before the catalog is approved and published.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="57ec9-124">Eeltingimused </span><span class="sxs-lookup"><span data-stu-id="57ec9-124">Prerequisites</span></span>
<span data-ttu-id="57ec9-125">Enne alustamist peavad olema täidetud järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="57ec9-125">The following tasks must be completed before you start:</span></span>

-   <span data-ttu-id="57ec9-126">Toodete ja tootesortimentide seadistamine.</span><span class="sxs-lookup"><span data-stu-id="57ec9-126">Set up products and product assortments.</span></span>
-   <span data-ttu-id="57ec9-127">Jaemüügitoodete seadistamine.</span><span class="sxs-lookup"><span data-stu-id="57ec9-127">Set up retail products.</span></span>
-   <span data-ttu-id="57ec9-128">Sortimendi seadistamine.</span><span class="sxs-lookup"><span data-stu-id="57ec9-128">Set up an assortment.</span></span>
-   <span data-ttu-id="57ec9-129">Kõnekeskuse loomine.</span><span class="sxs-lookup"><span data-stu-id="57ec9-129">Create a call center.</span></span>
-   <span data-ttu-id="57ec9-130">Seadistage kõnekeskus.</span><span class="sxs-lookup"><span data-stu-id="57ec9-130">Set up a call center.</span></span>
-   <span data-ttu-id="57ec9-131">Organisatsioonihierarhiasse kõnekeskuse lisamine.</span><span class="sxs-lookup"><span data-stu-id="57ec9-131">Add the call center to an organization hierarchy.</span></span>
-   <span data-ttu-id="57ec9-132">Organisatsioonihierarhia loomine või muutmine.</span><span class="sxs-lookup"><span data-stu-id="57ec9-132">Create or modify an organization hierarchy.</span></span>

## <a name="create-a-catalog"></a><span data-ttu-id="57ec9-133">Kataloogi loomine</span><span class="sxs-lookup"><span data-stu-id="57ec9-133">Create a catalog</span></span>
<span data-ttu-id="57ec9-134">Esmalt tuleb luua kataloog, lisada kataloogi tooted ja vaadata seejärel üle ning uuendada toodete atribuute.</span><span class="sxs-lookup"><span data-stu-id="57ec9-134">You must first create a catalog, add products to the catalog, and then review and update the attributes for the products.</span></span>

## <a name="validate-the-catalog"></a><span data-ttu-id="57ec9-135">Kataloogi valideerimine</span><span class="sxs-lookup"><span data-stu-id="57ec9-135">Validate the catalog</span></span>
<span data-ttu-id="57ec9-136">Kui olete kataloogi seadistamise lõpetanud, peate selle valideerima.</span><span class="sxs-lookup"><span data-stu-id="57ec9-136">After you've finished setting up the catalog, you must validate it.</span></span> <span data-ttu-id="57ec9-137">Valideerimisprotsess kontrollib, kas kanali- ja tooteatribuutide jaoks nõutavad andmed on terviklikud ja kehtivad ning kas kataloogi saab avaldada.</span><span class="sxs-lookup"><span data-stu-id="57ec9-137">The validation process verifies that the data that is required for channel attributes and product attributes is complete and valid, and that the catalog can be published.</span></span>

## <a name="submit-the-catalog-for-review-and-approval"></a><span data-ttu-id="57ec9-138">Kataloogi esitamine ülevaatuseks ja kinnitamiseks</span><span class="sxs-lookup"><span data-stu-id="57ec9-138">Submit the catalog for review and approval</span></span>
<span data-ttu-id="57ec9-139">Kui kataloog on kontrollitud, saate esitada kataloogi ülevaatamiseks ja kinnitamiseks.</span><span class="sxs-lookup"><span data-stu-id="57ec9-139">After a catalog is validated, you can submit the catalog for review and approval.</span></span> <span data-ttu-id="57ec9-140">Kataloog peab olema kinnitatud enne avaldamist.</span><span class="sxs-lookup"><span data-stu-id="57ec9-140">A catalog must be approved before it can be published.</span></span> <span data-ttu-id="57ec9-141">Töövoo saate konfigureerida nii, et kataloogid kinnitatakse automaatselt või need nõuavad käsitsi kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="57ec9-141">You can configure a workflow so that catalogs either are automatically approved or require manual approval.</span></span>

## <a name="optional-add-source-codes-free-products-and-scripts"></a><span data-ttu-id="57ec9-142">Valikuline: lähtekoodide, tasuta toodete ja skriptide lisamine</span><span class="sxs-lookup"><span data-stu-id="57ec9-142">Optional: Add source codes, free products, and scripts</span></span>
<span data-ttu-id="57ec9-143">Saate sisestada kõnekeskuse kataloogi ka järgmisi üksusi.</span><span class="sxs-lookup"><span data-stu-id="57ec9-143">You can also add the following items to a call center catalog.</span></span> <span data-ttu-id="57ec9-144">Need üksused on valikulised.</span><span class="sxs-lookup"><span data-stu-id="57ec9-144">These items are optional.</span></span>

-   <span data-ttu-id="57ec9-145">**Lähtekoodide** abil saavad trükitud katalooge pakkuvad ettevõtted jälgida kliendi reageeringut kindlatele kataloogidele.</span><span class="sxs-lookup"><span data-stu-id="57ec9-145">**Source codes** can be used by companies that provide printed catalogs to track the customer response to particular catalogs.</span></span> <span data-ttu-id="57ec9-146">Lähtekoodid trükitakse sageli kataloogi tagaküljele ja sisestatakse müügitellimusse, kui klient sooritab ostu.</span><span class="sxs-lookup"><span data-stu-id="57ec9-146">Source codes are often printed on the back of a catalog and are entered into the sales order when a customer makes a purchase.</span></span> <span data-ttu-id="57ec9-147">Lähtekoodi kataloogi lisamiseks peate esmalt looma sihtturu.</span><span class="sxs-lookup"><span data-stu-id="57ec9-147">To add a source code to the catalog, you must first create a target market.</span></span> <span data-ttu-id="57ec9-148">Sihtturg vastendatakse tavaliselt omandisse kuuluva või renditud postiloendiga.</span><span class="sxs-lookup"><span data-stu-id="57ec9-148">The target market is usually mapped to an owned or rented mailing list.</span></span>
-   <span data-ttu-id="57ec9-149">**Tasuta tooted** on kampaaniakaubad, mis lisatakse kataloogi viitamisel kliendi tellimusele tasuta.</span><span class="sxs-lookup"><span data-stu-id="57ec9-149">**Free products** are promotional items that are included free of charge with the customer's order when the catalog is referenced.</span></span>
-   <span data-ttu-id="57ec9-150">**Skriptide** abil saab suunata töötaja suhtlust klientidega kataloogi või kataloogis oleva toote kontekstis.</span><span class="sxs-lookup"><span data-stu-id="57ec9-150">**Scripts** can be used to guide the worker's interactions with customers in the context of a catalog or a product within a catalog.</span></span>

## <a name="publish-the-catalog"></a><span data-ttu-id="57ec9-151">Kataloogi avaldamine</span><span class="sxs-lookup"><span data-stu-id="57ec9-151">Publish the catalog</span></span>
<span data-ttu-id="57ec9-152">Kõnekeskuse jaoks kataloogi avaldamisega saate tooteteabe kataloogis lõpetada.</span><span class="sxs-lookup"><span data-stu-id="57ec9-152">By publishing a catalog for a call center, you finalize the product information in the catalog.</span></span> <span data-ttu-id="57ec9-153">Avaldamine näitab ka, et kataloog on valmis lisategevusteks, mida soovite teha.</span><span class="sxs-lookup"><span data-stu-id="57ec9-153">Publication also indicates that the catalog is ready for any additional actions that you want to perform.</span></span> <span data-ttu-id="57ec9-154">Näiteks saate luua trükitud kataloogi.</span><span class="sxs-lookup"><span data-stu-id="57ec9-154">For example, you can create a printed catalog.</span></span> <span data-ttu-id="57ec9-155">Katalooge saab avaldada käsitsi või kasutades pakktöötlust graafiku alusel avaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="57ec9-155">You can publish your catalogs manually, or you can use a batch process to publish according to a schedule.</span></span> <span data-ttu-id="57ec9-156">Enne kataloogi avaldamist peab kataloog olema kontrollitud ja kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="57ec9-156">Before you can publish a catalog, the catalog must be validated and approved.</span></span> <span data-ttu-id="57ec9-157">Kataloogi muutmiseks pärast avaldamist saate selle tagasi võtta ja siis uuesti avaldada.</span><span class="sxs-lookup"><span data-stu-id="57ec9-157">To change the catalog after it's published, you can retract the catalog and then republish it.</span></span>




