---
title: Müügihinna valikukriteeriumide loomine
description: See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCPriceModelSelectionCriteria, SysQueryForm, SysQueryTableLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae444008e550d808a02d55dad02cc1b52874f0d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985457"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="08d93-103">Müügihinna valikukriteeriumide loomine</span><span class="sxs-lookup"><span data-stu-id="08d93-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="08d93-104">See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.</span><span class="sxs-lookup"><span data-stu-id="08d93-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="08d93-105">See protseduur nõuab, et saadaval oleks vähemalt üks müügihinna mudel.</span><span class="sxs-lookup"><span data-stu-id="08d93-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="08d93-106">Selles näites kasutatakse hinnamudelina demoettevõtte USMF müügihinnamudelit Kõlarilahendus.</span><span class="sxs-lookup"><span data-stu-id="08d93-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="08d93-107">Tavaliselt kasutab seda protseduuri tootejuht.</span><span class="sxs-lookup"><span data-stu-id="08d93-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="08d93-108">Lisage olemasolevale müügihinna mudelile uus kriteerium</span><span class="sxs-lookup"><span data-stu-id="08d93-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="08d93-109">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="08d93-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="08d93-110">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="08d93-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="08d93-111">Valige loendist tootemudeli Kõlarilahendus rida, kuid ärge klõpsake mudeli nime linki.</span><span class="sxs-lookup"><span data-stu-id="08d93-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="08d93-112">Klõpsake tegumiribal valikut Mudel.</span><span class="sxs-lookup"><span data-stu-id="08d93-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="08d93-113">Klõpsake valikut Hinnamudeli kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="08d93-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="08d93-114">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="08d93-114">Click New.</span></span>
7. <span data-ttu-id="08d93-115">Tippige väljale Nimi tekst „Kliendigrupp 10”.</span><span class="sxs-lookup"><span data-stu-id="08d93-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="08d93-116">Hinnamudeli kriteeriumi nime abil saab tuvastada aluseks olevad valikukriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="08d93-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="08d93-117">Valige või sisestage väärtus väljal Hinnamudel.</span><span class="sxs-lookup"><span data-stu-id="08d93-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="08d93-118">Tehke väljal Tellimuse tüüp valik Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="08d93-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="08d93-119">Tellimuse tüüp määrab andmebaasiväljad, mis on valikupäringu puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="08d93-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="08d93-120">Sisestage kuupäev väljale Kehtiv alates.</span><span class="sxs-lookup"><span data-stu-id="08d93-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="08d93-121">Sisestage kuupäev väljale Loe aegunuks kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="08d93-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="08d93-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="08d93-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="08d93-123">Valikukriteeriumile päringu loomine</span><span class="sxs-lookup"><span data-stu-id="08d93-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="08d93-124">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="08d93-124">Click Edit.</span></span>
2. <span data-ttu-id="08d93-125">Valige Kliendid väljalt Tabel.</span><span class="sxs-lookup"><span data-stu-id="08d93-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="08d93-126">Valige Kliendigrupp väljalt Väli.</span><span class="sxs-lookup"><span data-stu-id="08d93-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="08d93-127">Selles näites kasutame valikukriteeriumide puhul konkreetset kliendigruppi.</span><span class="sxs-lookup"><span data-stu-id="08d93-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="08d93-128">Valige Kliendigrupp 10 väljalt Kriteerium.</span><span class="sxs-lookup"><span data-stu-id="08d93-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="08d93-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="08d93-129">Click OK.</span></span>

