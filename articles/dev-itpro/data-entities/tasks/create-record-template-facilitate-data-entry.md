--- 
title: "Andmesisestuse hõlbustamiseks kirje malli loomine"
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6f8d804133f8e9c6f47420d41df8d9430381e2fe
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-record-template-to-facilitate-data-entry"></a><span data-ttu-id="b3573-103">Andmesisestuse hõlbustamiseks kirje malli loomine</span><span class="sxs-lookup"><span data-stu-id="b3573-103">Create a record template to facilitate data entry</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3573-104">See protseduur näitab, kuidas luua kirje malli nii, et sageli kasutatavaid välja väärtuseid ei pea iga uue kirje jaoks selgesõnaliselt sisestama.</span><span class="sxs-lookup"><span data-stu-id="b3573-104">This procedure demonstrates how to create a record template so that field values that are used often do not have to be entered explicitly for each new record.</span></span> <span data-ttu-id="b3573-105">Selles protseduuris loote uue kirje uutele sülearvutitele, mis tuleks põhivaradele lisada.</span><span class="sxs-lookup"><span data-stu-id="b3573-105">In this procedure, you’ll create a new record for new laptops that should be added to your fixed assets.</span></span> <span data-ttu-id="b3573-106">See protseduur kasutab USMF-i näidisettevõtet.</span><span class="sxs-lookup"><span data-stu-id="b3573-106">This procedure uses the USMF sample company.</span></span>

1. <span data-ttu-id="b3573-107">Minge jaotisse Põhivarad > Põhivarad > Põhivarad.</span><span class="sxs-lookup"><span data-stu-id="b3573-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b3573-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b3573-108">Click New.</span></span>
3. <span data-ttu-id="b3573-109">Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="b3573-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="b3573-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b3573-110">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b3573-111">Näiteks sisestage „ettevõtte müügivihje sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="b3573-111">For example, enter 'Corporate lead laptop'.</span></span>  
5. <span data-ttu-id="b3573-112">Sisestage väärtus väljale Otsingunimi.</span><span class="sxs-lookup"><span data-stu-id="b3573-112">In the Search name field, type a value.</span></span>
    * <span data-ttu-id="b3573-113">Näiteks sisestage „sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="b3573-113">For example, enter 'laptop.'</span></span>  
6. <span data-ttu-id="b3573-114">Laiendage jaotist Tehniline teave.</span><span class="sxs-lookup"><span data-stu-id="b3573-114">Expand the Technical information section.</span></span>
7. <span data-ttu-id="b3573-115">Sisestage väärtus väljale Mudel.</span><span class="sxs-lookup"><span data-stu-id="b3573-115">In the Make field, type a value.</span></span>
8. <span data-ttu-id="b3573-116">Väljale Mudel sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="b3573-116">In the Model field, type a value.</span></span>
9. <span data-ttu-id="b3573-117">Sisestage väärtus väljale Ehitusaasta.</span><span class="sxs-lookup"><span data-stu-id="b3573-117">In the Model year field, type a value.</span></span>
10. <span data-ttu-id="b3573-118">Klõpsake toimingupaanil valikut Suvandid.</span><span class="sxs-lookup"><span data-stu-id="b3573-118">On the Action Pane, click Options.</span></span>
11. <span data-ttu-id="b3573-119">Klõpsake nuppu Kirje teave.</span><span class="sxs-lookup"><span data-stu-id="b3573-119">Click Record info.</span></span>
12. <span data-ttu-id="b3573-120">Klõpsake nuppu Kasutajamall.</span><span class="sxs-lookup"><span data-stu-id="b3573-120">Click User template.</span></span>
13. <span data-ttu-id="b3573-121">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b3573-121">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b3573-122">Näiteks sisestage „ettevõtte müügivihje sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="b3573-122">For example, enter 'Corporate laptop.'</span></span>  
14. <span data-ttu-id="b3573-123">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="b3573-123">In the Description field, type a value.</span></span>
    * <span data-ttu-id="b3573-124">Näiteks sisestage „ettevõtte sülearvuti”.</span><span class="sxs-lookup"><span data-stu-id="b3573-124">For example, enter 'Corporate laptop'.</span></span>  
15. <span data-ttu-id="b3573-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b3573-125">Click OK.</span></span>
16. <span data-ttu-id="b3573-126">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="b3573-126">Click Close.</span></span>


