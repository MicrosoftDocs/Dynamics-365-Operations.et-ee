---
title: Uute osakondade määratlemine
description: Osakonnad on tootmisüksused, mis tähistavad ettevõtte funktsionaalvaldkonna, nagu müük või raamatupidamine.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMOperatingUnit, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6dedddf305e303de5b284b34420cd0eda5170ed1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "342841"
---
# <a name="define-new-departments"></a><span data-ttu-id="62573-103">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="62573-103">Define new departments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="62573-104">Osakonnad on tootmisüksused, mis tähistavad ettevõtte funktsionaalvaldkonna, nagu müük või raamatupidamine.</span><span class="sxs-lookup"><span data-stu-id="62573-104">Departments are operating units that represent a functional area of a business, such as sales or accounting.</span></span> <span data-ttu-id="62573-105">Paljudel ettevõtetel on organisatsioonihierarhiad, mis näitavad ettevõtte erinevaid osakondi.</span><span class="sxs-lookup"><span data-stu-id="62573-105">Many companies have organizational hierarchies that display the various departments within a business.</span></span> <span data-ttu-id="62573-106">See protseduur selgitab osakondade loomise ja nende osakondade organisatsiooni osakonnahierarhiasse lisamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="62573-106">This procedure walks through the process of creating departments, and adding those departments to an organizations departmental hierarchy.</span></span> <span data-ttu-id="62573-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="62573-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="62573-108">Avage Inimressursid > Osakonnad > Osakonnad.</span><span class="sxs-lookup"><span data-stu-id="62573-108">Go to Human resources > Departments > Departments.</span></span>
2. <span data-ttu-id="62573-109">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="62573-109">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="62573-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="62573-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="62573-111">Näide: projekti arveldus</span><span class="sxs-lookup"><span data-stu-id="62573-111">Example: Project billing</span></span>  
4. <span data-ttu-id="62573-112">Sisestage väärtus väljale Memo.</span><span class="sxs-lookup"><span data-stu-id="62573-112">In the Memo field, type a value.</span></span>
    * <span data-ttu-id="62573-113">Näide: projekti arveldus</span><span class="sxs-lookup"><span data-stu-id="62573-113">Example: Project billing</span></span>  
5. <span data-ttu-id="62573-114">Sisestage või valige väärtus väljal Haldur.</span><span class="sxs-lookup"><span data-stu-id="62573-114">In the Manager field, enter or select a value.</span></span>
    * <span data-ttu-id="62573-115">Näide: Jodi Christiansen</span><span class="sxs-lookup"><span data-stu-id="62573-115">Example: Jodi Christiansen</span></span>  
6. <span data-ttu-id="62573-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="62573-116">Click Save.</span></span>
7. <span data-ttu-id="62573-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="62573-117">Close the page.</span></span>
8. <span data-ttu-id="62573-118">Avage Inimressursid > Osakonnad > Osakonnahierarhia.</span><span class="sxs-lookup"><span data-stu-id="62573-118">Go to Human resources > Departments > Department hierarchy.</span></span>
9. <span data-ttu-id="62573-119">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="62573-119">Click Edit.</span></span>
10. <span data-ttu-id="62573-120">Klõpsake nuppu Sisesta.</span><span class="sxs-lookup"><span data-stu-id="62573-120">Click Insert.</span></span>
11. <span data-ttu-id="62573-121">Klõpsake suvandit Osakond.</span><span class="sxs-lookup"><span data-stu-id="62573-121">Click Department.</span></span>
12. <span data-ttu-id="62573-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="62573-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="62573-123">Näide: projekti arveldus</span><span class="sxs-lookup"><span data-stu-id="62573-123">Example: Project billing</span></span>  
13. <span data-ttu-id="62573-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="62573-124">Click OK.</span></span>
14. <span data-ttu-id="62573-125">Rippdialoogi avamiseks klõpsake käsku Avalda.</span><span class="sxs-lookup"><span data-stu-id="62573-125">Click Publish to open the drop dialog.</span></span>
15. <span data-ttu-id="62573-126">Sisestage kuupäev ja kellaaeg väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="62573-126">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="62573-127">Osakonna hierarhia avaldamisel saate valida, millal muudatused jõustuvad.</span><span class="sxs-lookup"><span data-stu-id="62573-127">When publishing the department hierarchy, you can select when to make the changes effective.</span></span> <span data-ttu-id="62573-128">Muudatused saab dateerida hilisemale kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="62573-128">Changes can be future dated.</span></span> <span data-ttu-id="62573-129">Näiteks teate võib-olla, et lisate finantsaasta alguses uue osakonna.</span><span class="sxs-lookup"><span data-stu-id="62573-129">For example, you may know that at the beginning of your fiscal year you will be adding an additional department.</span></span> <span data-ttu-id="62573-130">Saate määrata jõustumiskuupäeva finantsaasta algusse ja hierarhia muudatused jõustuvad sellel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="62573-130">You can set your effective date to the beginning of the fiscal year, and the changes to the hierarchy will be effective on that date.</span></span>  
16. <span data-ttu-id="62573-131">Sisestage väärtus väljale Kirjelda muudatusi.</span><span class="sxs-lookup"><span data-stu-id="62573-131">In the Describe changes field, type a value.</span></span>
17. <span data-ttu-id="62573-132">Klõpsake Avalda.</span><span class="sxs-lookup"><span data-stu-id="62573-132">Click Publish.</span></span>

