---
title: Müügihinna valikukriteeriumide loomine
description: See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 69d22c3321beaa2667ee20bff00acd746714b993
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920527"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="2de5f-103">Müügihinna valikukriteeriumide loomine</span><span class="sxs-lookup"><span data-stu-id="2de5f-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2de5f-104">See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.</span><span class="sxs-lookup"><span data-stu-id="2de5f-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="2de5f-105">See protseduur nõuab, et saadaval oleks vähemalt üks müügihinna mudel.</span><span class="sxs-lookup"><span data-stu-id="2de5f-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="2de5f-106">Selles näites kasutatakse hinnamudelina demoettevõtte USMF müügihinnamudelit Kõlarilahendus.</span><span class="sxs-lookup"><span data-stu-id="2de5f-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="2de5f-107">Tavaliselt kasutab seda protseduuri tootejuht.</span><span class="sxs-lookup"><span data-stu-id="2de5f-107">Typically, a product manager uses this procedure.</span></span>

## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="2de5f-108">Lisage olemasolevale müügihinna mudelile uus kriteerium</span><span class="sxs-lookup"><span data-stu-id="2de5f-108">Add a new criterion for an existing sales price model</span></span>

1. <span data-ttu-id="2de5f-109">Avage **Tooteteabe haldus \> Tooted \> Tootekonfiguratsiooni mudelid**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-109">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="2de5f-110">Valige loendist tootemudeli Kõlarilahenduse rida, kuid ärge klõpsake valimiseks mudeli nime linki.</span><span class="sxs-lookup"><span data-stu-id="2de5f-110">In the list, select the row for the Speaker solution product model, but don't select the link for the model name.</span></span>
1. <span data-ttu-id="2de5f-111">Valige toiminguplaanil **Mudel**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-111">On the Action Pane, select **Model**.</span></span>
1. <span data-ttu-id="2de5f-112">Valige suvand **Hinnamudeli kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-112">Select **Price model criteria**.</span></span>
1. <span data-ttu-id="2de5f-113">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-113">Select **New**.</span></span>
1. <span data-ttu-id="2de5f-114">Tippige väljale **Nimi** tekst „Kliendigrupp 10”.</span><span class="sxs-lookup"><span data-stu-id="2de5f-114">In the **Name** field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="2de5f-115">Hinnamudeli kriteeriumi nime abil saab tuvastada aluseks olevad valikukriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="2de5f-115">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
1. <span data-ttu-id="2de5f-116">Valige või sisestage väljal **Hinnamudel** väärtus.</span><span class="sxs-lookup"><span data-stu-id="2de5f-116">In the **Price model** field, enter or select a value.</span></span>
1. <span data-ttu-id="2de5f-117">Valige väljal **Tellimuse tüüp** suvand *Müügitellimus*.</span><span class="sxs-lookup"><span data-stu-id="2de5f-117">In the **Order type** field, select *Sales order*.</span></span>
    * <span data-ttu-id="2de5f-118">Tellimuse tüüp määrab andmebaasiväljad, mis on valikupäringu puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="2de5f-118">The order type determines the database fields that will be available for the selection query.</span></span>  
1. <span data-ttu-id="2de5f-119">Sisestage kuupäev väljale **Kehtiv alates**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-119">In the **Valid from** field, enter a date.</span></span>
1. <span data-ttu-id="2de5f-120">Sisestage kuupäev väljale **Loe aegunuks**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-120">In the **Expire by** field, enter a date.</span></span>
1. <span data-ttu-id="2de5f-121">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-121">Select **Save**.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="2de5f-122">Valikukriteeriumile päringu loomine</span><span class="sxs-lookup"><span data-stu-id="2de5f-122">Create the query for the selection criteria</span></span>

1. <span data-ttu-id="2de5f-123">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-123">Select **Edit**.</span></span>
2. <span data-ttu-id="2de5f-124">Valige väljal **Tabel** suvand *Kliendid*.</span><span class="sxs-lookup"><span data-stu-id="2de5f-124">In the **Table** field, select *Customers*.</span></span>
3. <span data-ttu-id="2de5f-125">Valige väljal **Väli** suvand *Kliendigrupp*.</span><span class="sxs-lookup"><span data-stu-id="2de5f-125">In the **Field** field, select *Customer group*.</span></span>
    * <span data-ttu-id="2de5f-126">Selles näites kasutame valikukriteeriumide puhul konkreetset kliendigruppi.</span><span class="sxs-lookup"><span data-stu-id="2de5f-126">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="2de5f-127">Valige väljal **Kriteeriumid** *Kliendigrupp 10*.</span><span class="sxs-lookup"><span data-stu-id="2de5f-127">In the **Criteria** field, select *Customer group 10*.</span></span>
5. <span data-ttu-id="2de5f-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2de5f-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]