---
title: Toiminguressursi loomine
description: Operatsiooniressurss sooritab projekti või tootmisprotsessi tegevusi.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9d8f13e29ea813eb9721ddca795b67837e2aa5e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "350063"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="63110-103">Toiminguressursi loomine</span><span class="sxs-lookup"><span data-stu-id="63110-103">Create an operations resource</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63110-104">Operatsiooniressurss sooritab projekti või tootmisprotsessi tegevusi.</span><span class="sxs-lookup"><span data-stu-id="63110-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="63110-105">Selles protseduuris näitlikustatakse, kuidas määratleda operatsiooniressurssi.</span><span class="sxs-lookup"><span data-stu-id="63110-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="63110-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="63110-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="63110-107">Avage Ressursid.</span><span class="sxs-lookup"><span data-stu-id="63110-107">Go to Resources.</span></span>
2. <span data-ttu-id="63110-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="63110-108">Click New.</span></span>
3. <span data-ttu-id="63110-109">Sisestage väärtus väljale Ressurss.</span><span class="sxs-lookup"><span data-stu-id="63110-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="63110-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="63110-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="63110-111">Võimsus- ja tarbimisparameetrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="63110-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="63110-112">Laiendage jaotist Toiming.</span><span class="sxs-lookup"><span data-stu-id="63110-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="63110-113">Sisestage arv väljale Praagi protsent.</span><span class="sxs-lookup"><span data-stu-id="63110-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="63110-114">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="63110-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="63110-115">Määrake kulukategooria, mis määratleb seadistuskulu konto.</span><span class="sxs-lookup"><span data-stu-id="63110-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="63110-116">Sisestage või valige väärtus väljal Käitusaja kategooria.</span><span class="sxs-lookup"><span data-stu-id="63110-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="63110-117">Määrake kulukategooria, mis määratleb käitusaja kulu konto.</span><span class="sxs-lookup"><span data-stu-id="63110-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="63110-118">Valige või sisestage väärtus väljal Koguse kategooria.</span><span class="sxs-lookup"><span data-stu-id="63110-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="63110-119">Määrake kulukategooria, mis määratleb väljundkoguse põhjal ressursikulu konto.</span><span class="sxs-lookup"><span data-stu-id="63110-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="63110-120">Valige suvand väljal Võimsusühik.</span><span class="sxs-lookup"><span data-stu-id="63110-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="63110-121">Määrake operatsiooniressursside võimsuse väljendamise ühik.</span><span class="sxs-lookup"><span data-stu-id="63110-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="63110-122">Sisestage arv väljale Võimsus.</span><span class="sxs-lookup"><span data-stu-id="63110-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="63110-123">Sisestage arv väljale Efektiivsusprotsent.</span><span class="sxs-lookup"><span data-stu-id="63110-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="63110-124">Määrake operatsiooniressursside oodatav efektiivsus.</span><span class="sxs-lookup"><span data-stu-id="63110-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="63110-125">Efektiivsusprotsent reguleerib operatsiooniressursside läbilaskevõimet ja mõjutab ressursile reserveeritud aega.</span><span class="sxs-lookup"><span data-stu-id="63110-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="63110-126">Sisestage arv väljale Operatsioonide planeerimise protsent.</span><span class="sxs-lookup"><span data-stu-id="63110-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="63110-127">Määrake operatsiooniressursi suurim tootmisvõimsuse protsent, mida soovite operatsioonide planeerimisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="63110-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="63110-128">Valige väljal Piiratud võimsus suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="63110-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="63110-129">Valige suvand Jah, kui operatsiooniressurss tuleks planeerida tegeliku saadavaloleva võimsuse alusel ning kui arvesse tuleks võtta olemasolevaid võimsuse reserveeringuid.</span><span class="sxs-lookup"><span data-stu-id="63110-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="63110-130">Kui valitud on suvand Ei, eeldatakse, et operatsiooniressursil on piiramatu võimsus, mistõttu ressurss võib olla üle broneeritud.</span><span class="sxs-lookup"><span data-stu-id="63110-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="63110-131">Valige suvand Jah väljal Kitsaskohana toimiv ressurss.</span><span class="sxs-lookup"><span data-stu-id="63110-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="63110-132">Tööaegade määratlemine</span><span class="sxs-lookup"><span data-stu-id="63110-132">Define working times</span></span>
1. <span data-ttu-id="63110-133">Laiendage jaotist Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="63110-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="63110-134">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="63110-134">Click Add.</span></span>
3. <span data-ttu-id="63110-135">Sisestage või valige väärtus väljal Kalender.</span><span class="sxs-lookup"><span data-stu-id="63110-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="63110-136">Määrake ressursi võimsust (tundides) määratlev töögraafik.</span><span class="sxs-lookup"><span data-stu-id="63110-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="63110-137">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="63110-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="63110-138">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="63110-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="63110-139">Ressursivõimaluste määratlemine</span><span class="sxs-lookup"><span data-stu-id="63110-139">Define resource capabilities</span></span>
1. <span data-ttu-id="63110-140">Laiendage jaotist Võimalused.</span><span class="sxs-lookup"><span data-stu-id="63110-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="63110-141">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="63110-141">Click Add.</span></span>
    * <span data-ttu-id="63110-142">Võimsus on operatsiooniressursi võime konkreetset tegevust sooritada.</span><span class="sxs-lookup"><span data-stu-id="63110-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="63110-143">Planeerimismootor eraldab ressursid, sobitades iga tegevuse ressursinõuded saadaolevate operatsiooniressursside võimsustega.</span><span class="sxs-lookup"><span data-stu-id="63110-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="63110-144">Sisestage või valige väärtus väljal Võimalus.</span><span class="sxs-lookup"><span data-stu-id="63110-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="63110-145">Sisestage arv väljale Tase.</span><span class="sxs-lookup"><span data-stu-id="63110-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="63110-146">Määrake oskusetase, mille alusel ressurss võimsust töötleb.</span><span class="sxs-lookup"><span data-stu-id="63110-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="63110-147">Sisestage arv väljale Prioriteet.</span><span class="sxs-lookup"><span data-stu-id="63110-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="63110-148">Määrake operatsiooniressursi prioriteet võimsuse suhtes.</span><span class="sxs-lookup"><span data-stu-id="63110-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="63110-149">Prioriteedi planeerimisel valitakse esmalt kõrgeima prioriteediga (madalaima arvväärtusega) operatsiooniressurss.</span><span class="sxs-lookup"><span data-stu-id="63110-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="63110-150">Ressursigrupile ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="63110-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="63110-151">Laiendage jaotist Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="63110-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="63110-152">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="63110-152">Click Add.</span></span>
    * <span data-ttu-id="63110-153">Ressursigrupp määratleb operatsiooniressursside koha, tootmisüksuse ja lao konteksti.</span><span class="sxs-lookup"><span data-stu-id="63110-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="63110-154">Operatsiooniressurssi saab planeerida ainult juhul, kui see määratakse ressursigrupile, ja ainult kohta, kus on ressursigrupi asukoht.</span><span class="sxs-lookup"><span data-stu-id="63110-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="63110-155">Sisestage või valige väärtus väljal Ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="63110-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="63110-156">Sisestage või valige väärtus väljal Sisendasukoht.</span><span class="sxs-lookup"><span data-stu-id="63110-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="63110-157">Määrake operatsiooniressursi tarbitavate materjalide lao asukoht.</span><span class="sxs-lookup"><span data-stu-id="63110-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

