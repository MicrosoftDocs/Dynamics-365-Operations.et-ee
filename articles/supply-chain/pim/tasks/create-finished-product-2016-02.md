---
title: Lõpetatud toote loomine (veebruar 2016)
description: See ülesanne keskendub lõpetatud toote loomisele.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 71aa4522a9d70883a01914f6aa59a2fba0e0f659
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845055"
---
# <a name="create-a-finished-product-february-2016"></a><span data-ttu-id="ac9db-103">Lõpetatud toote loomine (veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="ac9db-103">Create a finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac9db-104">See ülesanne keskendub lõpetatud toote loomisele.</span><span class="sxs-lookup"><span data-stu-id="ac9db-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="ac9db-105">Koosluse arvutamise seerias on see esimene ülesanne.</span><span class="sxs-lookup"><span data-stu-id="ac9db-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="ac9db-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ac9db-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="ac9db-107">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="ac9db-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ac9db-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ac9db-108">Click New.</span></span>
3. <span data-ttu-id="ac9db-109">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="ac9db-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ac9db-110">Demonstreerimiseks tippige BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ac9db-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="ac9db-111">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="ac9db-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-112">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="ac9db-112">Select STD.</span></span> <span data-ttu-id="ac9db-113">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="ac9db-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="ac9db-114">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="ac9db-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-115">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="ac9db-115">For example, select Audio.</span></span> <span data-ttu-id="ac9db-116">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="ac9db-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="ac9db-117">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="ac9db-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-118">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ac9db-118">Select SiteWH.</span></span> <span data-ttu-id="ac9db-119">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="ac9db-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="ac9db-120">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="ac9db-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-121">Jälgimisdimensioone ei kasutata selles näites, seega valige Pole.</span><span class="sxs-lookup"><span data-stu-id="ac9db-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="ac9db-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ac9db-122">Click OK.</span></span>
9. <span data-ttu-id="ac9db-123">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="ac9db-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="ac9db-124">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="ac9db-124">Click Default order settings.</span></span>
11. <span data-ttu-id="ac9db-125">Väljal Vaikimisi tellimusetüüp valige Tootmine.</span><span class="sxs-lookup"><span data-stu-id="ac9db-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="ac9db-126">Kuna see on toodetav lõpetatud toode, valige Tootmine.</span><span class="sxs-lookup"><span data-stu-id="ac9db-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="ac9db-127">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="ac9db-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-128">Demonstreerimiseks valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="ac9db-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="ac9db-129">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="ac9db-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-130">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="ac9db-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="ac9db-131">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="ac9db-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ac9db-132">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="ac9db-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="ac9db-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ac9db-133">Close the page.</span></span>

