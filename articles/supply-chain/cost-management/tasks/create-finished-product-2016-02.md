--- 
title: Valmistoote loomine (ainult veebruar 2016)
description: "See ülesanne keskendub lõpetatud toote loomisele."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 44f9693e04160ffe9307de5e454d8269ca883679
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-finished-product-february-2016-only"></a><span data-ttu-id="abd5e-103">Valmistoote loomine (ainult veebruar 2016)</span><span class="sxs-lookup"><span data-stu-id="abd5e-103">Create a finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="abd5e-104">See ülesanne keskendub lõpetatud toote loomisele.</span><span class="sxs-lookup"><span data-stu-id="abd5e-104">This task focuses on creating a finished product.</span></span> <span data-ttu-id="abd5e-105">Koosluse arvutamise seerias on see esimene ülesanne.</span><span class="sxs-lookup"><span data-stu-id="abd5e-105">It is the first task in the BOM calculation series.</span></span> <span data-ttu-id="abd5e-106">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="abd5e-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="abd5e-107">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="abd5e-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="abd5e-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="abd5e-108">Click New.</span></span>
3. <span data-ttu-id="abd5e-109">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="abd5e-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="abd5e-110">Demonstreerimiseks tippige BOM_1.</span><span class="sxs-lookup"><span data-stu-id="abd5e-110">For the demonstration, type BOM_1.</span></span>  
4. <span data-ttu-id="abd5e-111">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="abd5e-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-112">Valige suvand STD.</span><span class="sxs-lookup"><span data-stu-id="abd5e-112">Select STD.</span></span> <span data-ttu-id="abd5e-113">STD tähendab standardset kulu ja on kuluarvestustega töötamisel kõige sagedamini kasutatud mudel.</span><span class="sxs-lookup"><span data-stu-id="abd5e-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="abd5e-114">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="abd5e-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-115">Näiteks valige Heli.</span><span class="sxs-lookup"><span data-stu-id="abd5e-115">For example, select Audio.</span></span> <span data-ttu-id="abd5e-116">See ei mõjuta kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="abd5e-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="abd5e-117">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="abd5e-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-118">Valige SiteWH.</span><span class="sxs-lookup"><span data-stu-id="abd5e-118">Select SiteWH.</span></span> <span data-ttu-id="abd5e-119">Demonstreerimiseks kasutatakse ainult tegevuskohta ja ladu.</span><span class="sxs-lookup"><span data-stu-id="abd5e-119">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="abd5e-120">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="abd5e-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-121">Jälgimisdimensioone ei kasutata selles näites, seega valige Pole.</span><span class="sxs-lookup"><span data-stu-id="abd5e-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="abd5e-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="abd5e-122">Click OK.</span></span>
9. <span data-ttu-id="abd5e-123">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="abd5e-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="abd5e-124">Klõpsake valikut Tellimuse vaikesätted.</span><span class="sxs-lookup"><span data-stu-id="abd5e-124">Click Default order settings.</span></span>
11. <span data-ttu-id="abd5e-125">Väljal Vaikimisi tellimusetüüp valige Tootmine.</span><span class="sxs-lookup"><span data-stu-id="abd5e-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="abd5e-126">Kuna see on toodetav lõpetatud toode, valige Tootmine.</span><span class="sxs-lookup"><span data-stu-id="abd5e-126">Because this is a finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="abd5e-127">Sisestage või valige väärtus väljal Ostu tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="abd5e-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-128">Demonstreerimiseks valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="abd5e-128">For the demonstration, select Site 1.</span></span>  
13. <span data-ttu-id="abd5e-129">Sisestage või valige väärtus väljal Laovarude tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="abd5e-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-130">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="abd5e-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="abd5e-131">Sisestage või valige väärtus väljal Müügi tegevuskoht.</span><span class="sxs-lookup"><span data-stu-id="abd5e-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="abd5e-132">Selles näites valige Tegevuskoht 1.</span><span class="sxs-lookup"><span data-stu-id="abd5e-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="abd5e-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="abd5e-133">Close the page.</span></span>


