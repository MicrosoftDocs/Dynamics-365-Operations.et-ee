--- 
title: "Tööaja mallide loomine"
description: "Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="8c870-103">Tööaja mallide loomine</span><span class="sxs-lookup"><span data-stu-id="8c870-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c870-104">Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks.</span><span class="sxs-lookup"><span data-stu-id="8c870-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="8c870-105">See protseduur näitab, kuidas tööajamalli määratleda, kasutades tööaja plaanimise atribuute tööajaintervallide kategooriatesse jaotamiseks.</span><span class="sxs-lookup"><span data-stu-id="8c870-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="8c870-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="8c870-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="8c870-107">Avage Kõik tööruumid > Ressursi elutsükli haldus.</span><span class="sxs-lookup"><span data-stu-id="8c870-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="8c870-108">Klõpsake valikut Tööajamallid.</span><span class="sxs-lookup"><span data-stu-id="8c870-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="8c870-109">Tööajamalli loomine</span><span class="sxs-lookup"><span data-stu-id="8c870-109">Create working time template</span></span>
1. <span data-ttu-id="8c870-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8c870-110">Click New.</span></span>
2. <span data-ttu-id="8c870-111">Tippige väärtus väljale Tööaeg.</span><span class="sxs-lookup"><span data-stu-id="8c870-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="8c870-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="8c870-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="8c870-113">Laiendage jaotist Esmaspäev.</span><span class="sxs-lookup"><span data-stu-id="8c870-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="8c870-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8c870-114">Click Add.</span></span>
6. <span data-ttu-id="8c870-115">Sisestage kellaaeg väljale Alates.</span><span class="sxs-lookup"><span data-stu-id="8c870-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="8c870-116">Määrake kellaaeg, millal töö hommikul algab.</span><span class="sxs-lookup"><span data-stu-id="8c870-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="8c870-117">Sisestage kellaaeg väljale Kuni.</span><span class="sxs-lookup"><span data-stu-id="8c870-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="8c870-118">Määrake töötajate lõunavaheaja alguskellaaeg.</span><span class="sxs-lookup"><span data-stu-id="8c870-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="8c870-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="8c870-119">Click Add.</span></span>
9. <span data-ttu-id="8c870-120">Sisestage kellaaeg väljale Alates.</span><span class="sxs-lookup"><span data-stu-id="8c870-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="8c870-121">Määrake töö jätkamise kellaaeg pärast lõunat.</span><span class="sxs-lookup"><span data-stu-id="8c870-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="8c870-122">Sisestage kellaaeg väljale Kuni.</span><span class="sxs-lookup"><span data-stu-id="8c870-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="8c870-123">Määrake tööpäeva lõpp.</span><span class="sxs-lookup"><span data-stu-id="8c870-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="8c870-124">Tööaegade kopeerimine kõigile nädalapäevadele</span><span class="sxs-lookup"><span data-stu-id="8c870-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="8c870-125">Klõpsake valikut Kopeeri päev.</span><span class="sxs-lookup"><span data-stu-id="8c870-125">Click Copy day.</span></span>
    * <span data-ttu-id="8c870-126">Kopeerige tööajamääratlused esmaspäevalt teisipäevale.</span><span class="sxs-lookup"><span data-stu-id="8c870-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="8c870-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8c870-127">Click OK.</span></span>
3. <span data-ttu-id="8c870-128">Klõpsake valikut Kopeeri päev.</span><span class="sxs-lookup"><span data-stu-id="8c870-128">Click Copy day.</span></span>
    * <span data-ttu-id="8c870-129">Kopeerige tööajamääratlused esmaspäevalt kolmapäevale.</span><span class="sxs-lookup"><span data-stu-id="8c870-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="8c870-130">Tehke valik väljal Kuni nädalapäevani.</span><span class="sxs-lookup"><span data-stu-id="8c870-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="8c870-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8c870-131">Click OK.</span></span>
6. <span data-ttu-id="8c870-132">Klõpsake valikut Kopeeri päev.</span><span class="sxs-lookup"><span data-stu-id="8c870-132">Click Copy day.</span></span>
    * <span data-ttu-id="8c870-133">Kopeerige tööajamääratlused esmaspäevalt neljapäevale.</span><span class="sxs-lookup"><span data-stu-id="8c870-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="8c870-134">Tehke valik väljal Kuni nädalapäevani.</span><span class="sxs-lookup"><span data-stu-id="8c870-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="8c870-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8c870-135">Click OK.</span></span>
9. <span data-ttu-id="8c870-136">Klõpsake valikut Kopeeri päev.</span><span class="sxs-lookup"><span data-stu-id="8c870-136">Click Copy day.</span></span>
    * <span data-ttu-id="8c870-137">Kopeerige tööajamääratlused esmaspäevalt reedele.</span><span class="sxs-lookup"><span data-stu-id="8c870-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="8c870-138">Tehke valik väljal Kuni nädalapäevani.</span><span class="sxs-lookup"><span data-stu-id="8c870-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="8c870-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8c870-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="8c870-140">Eritoimingute ajavahemike määratlemine</span><span class="sxs-lookup"><span data-stu-id="8c870-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="8c870-141">Laiendage jaotist Reede.</span><span class="sxs-lookup"><span data-stu-id="8c870-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="8c870-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8c870-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8c870-143">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="8c870-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="8c870-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="8c870-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="8c870-145">Valige või sisestage väärtus väljal Atribuut.</span><span class="sxs-lookup"><span data-stu-id="8c870-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="8c870-146">Puhkepäevade märkimine komplekteerimiseks suletuks</span><span class="sxs-lookup"><span data-stu-id="8c870-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="8c870-147">Laiendage jaotist Laupäev.</span><span class="sxs-lookup"><span data-stu-id="8c870-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="8c870-148">Valige Jah väljal Komplekteerimiseks suletud.</span><span class="sxs-lookup"><span data-stu-id="8c870-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="8c870-149">Laiendage jaotist Pühapäev.</span><span class="sxs-lookup"><span data-stu-id="8c870-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="8c870-150">Valige Jah väljal Komplekteerimiseks suletud.</span><span class="sxs-lookup"><span data-stu-id="8c870-150">Select Yes in the Closed for pickup field.</span></span>


