---
title: Kaastoodete kopeerimine olemasolevast valemiversioonist
description: See protseduur näitab, kuidas kopeerida kaastooteid olemasolevalt valemiversioonilt teistsugusele väljastatud toote valemiversioonile.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, PmfFormulaCoBy, BOMRouteCopyDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cbcf2abc37441f9ff23e2b180c261831dfb79369
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829278"
---
# <a name="copy-co-products-from-an-existing-formula-version"></a><span data-ttu-id="211ea-103">Kaastoodete kopeerimine olemasolevast valemiversioonist</span><span class="sxs-lookup"><span data-stu-id="211ea-103">Copy co-products from an existing formula version</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="211ea-104">See protseduur näitab, kuidas kopeerida kaastooteid olemasolevalt valemiversioonilt teistsugusele väljastatud toote valemiversioonile.</span><span class="sxs-lookup"><span data-stu-id="211ea-104">This procedure shows how to copy co-products from an existing formula version to a different formula version for a released product.</span></span> <span data-ttu-id="211ea-105">Eeldus on, et kaastoodete on seotud vähemalt üks valemiversioon.</span><span class="sxs-lookup"><span data-stu-id="211ea-105">It is a prerequisite that there is at least one formula version associated with co-products.</span></span> <span data-ttu-id="211ea-106">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="211ea-106">The demo data company USP2 is used to create this procedure.</span></span>


## <a name="find-a-released-product"></a><span data-ttu-id="211ea-107">Väljastatud toote otsimine</span><span class="sxs-lookup"><span data-stu-id="211ea-107">Find a released product</span></span>
1. <span data-ttu-id="211ea-108">Avage Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="211ea-108">Go to Released products.</span></span>
2. <span data-ttu-id="211ea-109">Klõpsake suvandit Näita filtreid.</span><span class="sxs-lookup"><span data-stu-id="211ea-109">Click Show filters.</span></span>
    * <span data-ttu-id="211ea-110">Olete lisamas filtri dialoogiboksi välja Tootmise tüüp.</span><span class="sxs-lookup"><span data-stu-id="211ea-110">You are about to add the field Production type in the filter dialog box.</span></span>  
3. <span data-ttu-id="211ea-111">Klõpsake käsku Lisa filtri väli, et lisada väli Tootmise tüüp.</span><span class="sxs-lookup"><span data-stu-id="211ea-111">Click Add a filter field to add the field Production type.</span></span>
    * <span data-ttu-id="211ea-112">Järgmises etapis peate enne valiku Rakenda tegemist sisestama käsitsi valemi väljale Tootmise tüüp.</span><span class="sxs-lookup"><span data-stu-id="211ea-112">In the next step, you need to manually enter Formula in the Production type field before you select Apply.</span></span> <span data-ttu-id="211ea-113">See määrab filtri väljastatud toodete loendile.</span><span class="sxs-lookup"><span data-stu-id="211ea-113">This sets the filter on the list of released products.</span></span>  
4. <span data-ttu-id="211ea-114">Sisestage käsitsi valem väljale Tootmise tüüp.</span><span class="sxs-lookup"><span data-stu-id="211ea-114">Manually enter Formula in the Production type field.</span></span>
5. <span data-ttu-id="211ea-115">Klõpsake käsku Apply (Rakenda).</span><span class="sxs-lookup"><span data-stu-id="211ea-115">Click Apply.</span></span>

## <a name="select-a-released-product"></a><span data-ttu-id="211ea-116">Väljastatud toote valimine</span><span class="sxs-lookup"><span data-stu-id="211ea-116">Select a released product</span></span>
1. <span data-ttu-id="211ea-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="211ea-117">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="211ea-118">Klõpsake valikut Valemiversioonid.</span><span class="sxs-lookup"><span data-stu-id="211ea-118">Click Formula versions.</span></span>
    * <span data-ttu-id="211ea-119">Klõpsake tegumiribal Tehnika valikut Valemiversioonid.</span><span class="sxs-lookup"><span data-stu-id="211ea-119">On the Engineering Action Pane, click Formula versions.</span></span>  

## <a name="copy-co-products"></a><span data-ttu-id="211ea-120">Kaastoodete kopeerimine</span><span class="sxs-lookup"><span data-stu-id="211ea-120">Copy co-products</span></span>
1. <span data-ttu-id="211ea-121">Klõpsake tegumiribal valikut Valemiversioon.</span><span class="sxs-lookup"><span data-stu-id="211ea-121">On the Action Pane, click Formula version.</span></span>
2. <span data-ttu-id="211ea-122">Klõpsake valikut Kaastooted.</span><span class="sxs-lookup"><span data-stu-id="211ea-122">Click Co-products.</span></span>
3. <span data-ttu-id="211ea-123">Klõpsake käsku Kopeeri.</span><span class="sxs-lookup"><span data-stu-id="211ea-123">Click Copy.</span></span>
4. <span data-ttu-id="211ea-124">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="211ea-124">In the Item number field, enter or select a value.</span></span>
5. <span data-ttu-id="211ea-125">Valige või sisestage väärtus väljal Valemi versioon.</span><span class="sxs-lookup"><span data-stu-id="211ea-125">In the Formula version field, enter or select a value.</span></span>
6. <span data-ttu-id="211ea-126">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="211ea-126">Click OK.</span></span>
7. <span data-ttu-id="211ea-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="211ea-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]