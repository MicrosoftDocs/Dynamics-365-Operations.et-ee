--- 
title: "Dimensioonipõhiste konfiguratsioonide loomine"
description: "See protseduur selgitab, kuidas määratleda dimensioonipõhise toote konfiguratsiooni."
author: YuyuScheller
manager: AnnBe
ms.date: 06/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: d6ea85cedbb96266f82e0a4ec1ad17f3ba829322
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="d3b3d-103">Dimensioonipõhiste konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="d3b3d-103">Create dimension-based configurations</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d3b3d-104">See protseduur selgitab, kuidas määratleda dimensioonipõhise toote konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="d3b3d-105">See on viimane protseduur seerias, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="d3b3d-106">Selle protseduuri käivitamine sõltub andmetest, mis on loodud seitsmes eelnevas salvestises.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="d3b3d-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="d3b3d-108">Dimensioonipõhise tooteetaloni otsimine</span><span class="sxs-lookup"><span data-stu-id="d3b3d-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="d3b3d-109">Klõpsake valikut Väljastatud toodete hooldus.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="d3b3d-110">Klõpsake valikut Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-110">Click Released products.</span></span>
3. <span data-ttu-id="d3b3d-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d3b3d-112">Valige dimensioonipõhine tooteetalon, mille lõite 8 salvestuse esimese salvestuses.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="d3b3d-113">Konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="d3b3d-113">Create configurations</span></span>
1. <span data-ttu-id="d3b3d-114">Klõpsake toimingupaanil Tehnika suvandit Konfiguratsioonide haldamine.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="d3b3d-115">Klõpsake nuppu Konfigureeri.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-115">Click Configure.</span></span>
3. <span data-ttu-id="d3b3d-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d3b3d-117">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="d3b3d-118">Valige mis tahes kaup esimeses konfiguratsioonigrupis.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="d3b3d-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="d3b3d-120">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="d3b3d-121">Valige mis tahes kaup teisest konfiguratsioonigrupist.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="d3b3d-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-122">Click OK.</span></span>
8. <span data-ttu-id="d3b3d-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d3b3d-124">Tippige väärtus väljale Konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="d3b3d-125">Sisestage konfiguratsiooni nimi, mis lihtsustab konfiguratsiooni tuvastamist.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="d3b3d-126">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d3b3d-127">Sisestage konfiguratsiooni kirjeldus, mis selgitab, mida see sisaldab.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="d3b3d-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d3b3d-128">Click OK.</span></span>


