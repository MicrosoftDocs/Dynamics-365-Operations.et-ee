---
title: Dimensioonipõhiste konfiguratsioonide loomine
description: See protseduur selgitab, kuidas määratleda dimensioonipõhise toote konfiguratsiooni.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, EcoResDimensionBasedConfiguration, ConfigChooseFromRoute, ConfigChooseFromGroup, ConfigChoiceApprove
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e612e3cd0343d386da4755f13eca6bf1443816d5
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150146"
---
# <a name="create-dimension-based-configurations"></a><span data-ttu-id="4e30f-103">Dimensioonipõhiste konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="4e30f-103">Create dimension-based configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e30f-104">See protseduur selgitab, kuidas määratleda dimensioonipõhise toote konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="4e30f-104">This procedure shows how to define a configuration for a dimension-based product.</span></span> <span data-ttu-id="4e30f-105">See on viimane protseduur seerias, mis selgitab kombinatsioonide loomist dimensioonipõhise konfiguratsiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="4e30f-105">This is the last procedure in the series that explains how to build combinations for dimension-based configuration.</span></span> <span data-ttu-id="4e30f-106">Selle protseduuri käivitamine sõltub andmetest, mis on loodud seitsmes eelnevas salvestises.</span><span class="sxs-lookup"><span data-stu-id="4e30f-106">The execution of this procedure is dependent on the data created in the previous seven recordings.</span></span> <span data-ttu-id="4e30f-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="4e30f-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="find-the-dimension-based-product-master"></a><span data-ttu-id="4e30f-108">Dimensioonipõhise tooteetaloni otsimine</span><span class="sxs-lookup"><span data-stu-id="4e30f-108">Find the dimension-based product master</span></span>
1. <span data-ttu-id="4e30f-109">Klõpsake valikut Väljastatud toodete hooldus.</span><span class="sxs-lookup"><span data-stu-id="4e30f-109">Click Released product maintenance.</span></span>
2. <span data-ttu-id="4e30f-110">Klõpsake valikut Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="4e30f-110">Click Released products.</span></span>
3. <span data-ttu-id="4e30f-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="4e30f-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4e30f-112">Valige dimensioonipõhine tooteetalon, mille lõite 8 salvestuse esimese salvestuses.</span><span class="sxs-lookup"><span data-stu-id="4e30f-112">Select the dimension-based product master that you created in the first recording in this sequence of 8 recordings.</span></span>  

## <a name="create-configurations"></a><span data-ttu-id="4e30f-113">Konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="4e30f-113">Create configurations</span></span>
1. <span data-ttu-id="4e30f-114">Klõpsake toimingupaanil Tehnika suvandit Konfiguratsioonide haldamine.</span><span class="sxs-lookup"><span data-stu-id="4e30f-114">On the Engineering Action Pane, click Maintain configurations.</span></span>
2. <span data-ttu-id="4e30f-115">Klõpsake nuppu Konfigureeri.</span><span class="sxs-lookup"><span data-stu-id="4e30f-115">Click Configure.</span></span>
3. <span data-ttu-id="4e30f-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="4e30f-116">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4e30f-117">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="4e30f-117">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="4e30f-118">Valige mis tahes kaup esimeses konfiguratsioonigrupis.</span><span class="sxs-lookup"><span data-stu-id="4e30f-118">Select any of the items in the first configuration group.</span></span>  
5. <span data-ttu-id="4e30f-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="4e30f-119">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="4e30f-120">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="4e30f-120">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="4e30f-121">Valige mis tahes kaup teisest konfiguratsioonigrupist.</span><span class="sxs-lookup"><span data-stu-id="4e30f-121">Select any item from the second configuration group.</span></span>  
7. <span data-ttu-id="4e30f-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4e30f-122">Click OK.</span></span>
8. <span data-ttu-id="4e30f-123">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="4e30f-123">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4e30f-124">Tippige väärtus väljale Konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="4e30f-124">In the Configuration field, type a value.</span></span>
    * <span data-ttu-id="4e30f-125">Sisestage konfiguratsiooni nimi, mis lihtsustab konfiguratsiooni tuvastamist.</span><span class="sxs-lookup"><span data-stu-id="4e30f-125">Enter a configuration name that will make it easy to identify the configuration.</span></span>  
10. <span data-ttu-id="4e30f-126">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="4e30f-126">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4e30f-127">Sisestage konfiguratsiooni kirjeldus, mis selgitab, mida see sisaldab.</span><span class="sxs-lookup"><span data-stu-id="4e30f-127">Enter a description of the configuration to explain what it contains.</span></span>  
11. <span data-ttu-id="4e30f-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4e30f-128">Click OK.</span></span>

