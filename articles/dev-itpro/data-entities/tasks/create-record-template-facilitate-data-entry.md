--- 
title: "Kirje mallide loomine andmesisestuse hõlbustamiseks"
description: "See protseduur näitab, kuidas luua kirje malli nii, et sageli kasutatavaid välja väärtuseid ei pea iga uue kirje jaoks selgesõnaliselt sisestama."
author: sericks007
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: afe2da72ef6a6451e797ed6098df164e765e503e
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="create-record-templates-to-facilitate-data-entry"></a><span data-ttu-id="58286-103">Kirje mallide loomine andmesisestuse hõlbustamiseks</span><span class="sxs-lookup"><span data-stu-id="58286-103">Create record templates to facilitate data entry</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58286-104">See protseduur näitab, kuidas luua kirje malli nii, et sageli kasutatavaid välja väärtuseid ei pea iga uue kirje jaoks selgesõnaliselt sisestama.</span><span class="sxs-lookup"><span data-stu-id="58286-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="58286-105">Selles protseduuris loote uue kirje uutele sülearvutitele, mis tuleks põhivaradele lisada.</span><span class="sxs-lookup"><span data-stu-id="58286-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="58286-106">See protseduur kasutab USMF-i näidisettevõtet.</span><span class="sxs-lookup"><span data-stu-id="58286-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="58286-107">Minge jaotisse Põhivarad > Põhivarad > Põhivarad.</span><span class="sxs-lookup"><span data-stu-id="58286-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="58286-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="58286-108">Click New.</span></span>
3. <span data-ttu-id="58286-109">Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="58286-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="58286-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="58286-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="58286-111">Näiteks sisestage „ettevõtte müügivihje sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="58286-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="58286-112">Sisestage väärtus väljale Otsingunimi.</span><span class="sxs-lookup"><span data-stu-id="58286-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="58286-113">Näiteks sisestage „sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="58286-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="58286-114">Laiendage jaotist Tehniline teave.</span><span class="sxs-lookup"><span data-stu-id="58286-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="58286-115">Sisestage väärtus väljale Mudel.</span><span class="sxs-lookup"><span data-stu-id="58286-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="58286-116">Väljale Mudel sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="58286-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="58286-117">Sisestage väärtus väljale Ehitusaasta.</span><span class="sxs-lookup"><span data-stu-id="58286-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="58286-118">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="58286-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="58286-119">Klõpsake nuppu Kirje teave.</span><span class="sxs-lookup"><span data-stu-id="58286-119">Click Record info.</span></span>
12. <span data-ttu-id="58286-120">Klõpsake nuppu Kasutajamall.</span><span class="sxs-lookup"><span data-stu-id="58286-120">Click User template.</span></span>
13. <span data-ttu-id="58286-121">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="58286-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="58286-122">Näiteks sisestage „ettevõtte müügivihje sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="58286-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="58286-123">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="58286-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="58286-124">Näiteks sisestage „ettevõtte sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="58286-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="58286-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="58286-125">Click OK.</span></span>
16. <span data-ttu-id="58286-126">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="58286-126">Click Close.</span></span>


