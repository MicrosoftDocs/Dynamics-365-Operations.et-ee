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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6d1385a83da5b6448a9c753d7469979796043b60
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203766"
---
# <a name="create-sales-price-selection-criteria"></a><span data-ttu-id="6669b-103">Müügihinna valikukriteeriumide loomine</span><span class="sxs-lookup"><span data-stu-id="6669b-103">Create sales price selection criteria</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6669b-104">See protseduur näitab, kuidas luua atribuudipõhistele hinnamudelitele müügihinna valikukriteeriumi.</span><span class="sxs-lookup"><span data-stu-id="6669b-104">This procedure shows how to create a sales price selection criterion for attribute-based sales price models.</span></span> <span data-ttu-id="6669b-105">See protseduur nõuab, et saadaval oleks vähemalt üks müügihinna mudel.</span><span class="sxs-lookup"><span data-stu-id="6669b-105">This procedure requires that at least one sales price model be available.</span></span> <span data-ttu-id="6669b-106">Selles näites kasutatakse hinnamudelina demoettevõtte USMF müügihinnamudelit Kõlarilahendus.</span><span class="sxs-lookup"><span data-stu-id="6669b-106">This example uses the price model for the Speaker solution sales price model in the USMF demo data company.</span></span> <span data-ttu-id="6669b-107">Tavaliselt kasutab seda protseduuri tootejuht.</span><span class="sxs-lookup"><span data-stu-id="6669b-107">Typically, a product manager uses this procedure.</span></span>


## <a name="add-a-new-criterion-for-an-existing-sales-price-model"></a><span data-ttu-id="6669b-108">Lisage olemasolevale müügihinna mudelile uus kriteerium</span><span class="sxs-lookup"><span data-stu-id="6669b-108">Add a new criterion for an existing sales price model</span></span>
1. <span data-ttu-id="6669b-109">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="6669b-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="6669b-110">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="6669b-110">Click Product configuration models.</span></span>
3. <span data-ttu-id="6669b-111">Valige loendist tootemudeli Kõlarilahendus rida, kuid ärge klõpsake mudeli nime linki.</span><span class="sxs-lookup"><span data-stu-id="6669b-111">In the list, select the row for the Speaker solution product model, but don't click the link for the model name.</span></span>
4. <span data-ttu-id="6669b-112">Klõpsake tegumiribal valikut Mudel.</span><span class="sxs-lookup"><span data-stu-id="6669b-112">On the Action Pane, click Model.</span></span>
5. <span data-ttu-id="6669b-113">Klõpsake valikut Hinnamudeli kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="6669b-113">Click Price model criteria.</span></span>
6. <span data-ttu-id="6669b-114">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="6669b-114">Click New.</span></span>
7. <span data-ttu-id="6669b-115">Tippige väljale Nimi tekst „Kliendigrupp 10”.</span><span class="sxs-lookup"><span data-stu-id="6669b-115">In the Name field, type 'Customer group 10'.</span></span>
    * <span data-ttu-id="6669b-116">Hinnamudeli kriteeriumi nime abil saab tuvastada aluseks olevad valikukriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="6669b-116">The name of the price model criterion is used to help identify the underlying selection criteria.</span></span>  
8. <span data-ttu-id="6669b-117">Valige või sisestage väärtus väljal Hinnamudel.</span><span class="sxs-lookup"><span data-stu-id="6669b-117">In the Price model field, enter or select a value.</span></span>
9. <span data-ttu-id="6669b-118">Tehke väljal Tellimuse tüüp valik Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="6669b-118">In the Order type field, select Sales order.</span></span>
    * <span data-ttu-id="6669b-119">Tellimuse tüüp määrab andmebaasiväljad, mis on valikupäringu puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="6669b-119">The order type determines the database fields that will be available for the selection query.</span></span>  
10. <span data-ttu-id="6669b-120">Sisestage kuupäev väljale Kehtiv alates.</span><span class="sxs-lookup"><span data-stu-id="6669b-120">In the Valid from field, enter a date.</span></span>
11. <span data-ttu-id="6669b-121">Sisestage kuupäev väljale Loe aegunuks kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="6669b-121">In the Expire by field, enter a date.</span></span>
12. <span data-ttu-id="6669b-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6669b-122">Click Save.</span></span>

## <a name="create-the-query-for-the-selection-criteria"></a><span data-ttu-id="6669b-123">Valikukriteeriumile päringu loomine</span><span class="sxs-lookup"><span data-stu-id="6669b-123">Create the query for the selection criteria</span></span>
1. <span data-ttu-id="6669b-124">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6669b-124">Click Edit.</span></span>
2. <span data-ttu-id="6669b-125">Valige Kliendid väljalt Tabel.</span><span class="sxs-lookup"><span data-stu-id="6669b-125">In the Table field, select Customers.</span></span> 
3. <span data-ttu-id="6669b-126">Valige Kliendigrupp väljalt Väli.</span><span class="sxs-lookup"><span data-stu-id="6669b-126">In the Field field, select Customer group.</span></span>
    * <span data-ttu-id="6669b-127">Selles näites kasutame valikukriteeriumide puhul konkreetset kliendigruppi.</span><span class="sxs-lookup"><span data-stu-id="6669b-127">In this example, we will use a specific customer group for the selection criteria.</span></span>  
4. <span data-ttu-id="6669b-128">Valige Kliendigrupp 10 väljalt Kriteerium.</span><span class="sxs-lookup"><span data-stu-id="6669b-128">In the Criteria field, select Customer group 10.</span></span> 
5. <span data-ttu-id="6669b-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6669b-129">Click OK.</span></span>

