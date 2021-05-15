---
title: Tööaja mallide loomine
description: Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920924"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="61640-103">Tööaja mallide loomine</span><span class="sxs-lookup"><span data-stu-id="61640-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="61640-104">Tööajamallid määratlevad kogu nädala tööaja ja neid kasutatakse ajavahemiku tööaegade loomiseks.</span><span class="sxs-lookup"><span data-stu-id="61640-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="61640-105">See protseduur näitab, kuidas tööajamalli määratleda, kasutades tööaja plaanimise atribuute tööajaintervallide kategooriatesse jaotamiseks.</span><span class="sxs-lookup"><span data-stu-id="61640-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="61640-106">Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="61640-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="61640-107">Valige **Tööruumid > Ressursi elutsükli haldus**.</span><span class="sxs-lookup"><span data-stu-id="61640-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="61640-108">Valige **Tööaja mallide loomine**.</span><span class="sxs-lookup"><span data-stu-id="61640-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="61640-109">Tööajamalli loomine</span><span class="sxs-lookup"><span data-stu-id="61640-109">Create working time template</span></span>

1. <span data-ttu-id="61640-110">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="61640-110">Select **New**.</span></span>
1. <span data-ttu-id="61640-111">Tippige väärtus väljale **Tööaja mall**.</span><span class="sxs-lookup"><span data-stu-id="61640-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="61640-112">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="61640-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="61640-113">Laiendage jaotist **Esmaspäev**.</span><span class="sxs-lookup"><span data-stu-id="61640-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="61640-114">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="61640-114">Select **Add**.</span></span>
1. <span data-ttu-id="61640-115">Sisestage kellaaeg väljale **Alates**.</span><span class="sxs-lookup"><span data-stu-id="61640-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="61640-116">Määrake kellaaeg, millal töö hommikul algab.</span><span class="sxs-lookup"><span data-stu-id="61640-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="61640-117">Sisestage kellaaeg väljale **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="61640-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="61640-118">Määrake töötajate lõunavaheaja alguskellaaeg.</span><span class="sxs-lookup"><span data-stu-id="61640-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="61640-119">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="61640-119">Select **Add**.</span></span>
1. <span data-ttu-id="61640-120">Sisestage kellaaeg väljale **Alates**.</span><span class="sxs-lookup"><span data-stu-id="61640-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="61640-121">Määrake töö jätkamise kellaaeg pärast lõunat.</span><span class="sxs-lookup"><span data-stu-id="61640-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="61640-122">Sisestage kellaaeg väljale **Kuni**.</span><span class="sxs-lookup"><span data-stu-id="61640-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="61640-123">Määrake tööpäeva lõpp.</span><span class="sxs-lookup"><span data-stu-id="61640-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="61640-124">Tööaegade kopeerimine kõigile nädalapäevadele</span><span class="sxs-lookup"><span data-stu-id="61640-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="61640-125">Valige suvand **Kopeeri päev**.</span><span class="sxs-lookup"><span data-stu-id="61640-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="61640-126">Kopeerige tööajamääratlused esmaspäevalt teisipäevale.</span><span class="sxs-lookup"><span data-stu-id="61640-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="61640-127">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="61640-127">Select **OK**.</span></span>
1. <span data-ttu-id="61640-128">Valige suvand **Kopeeri päev**.</span><span class="sxs-lookup"><span data-stu-id="61640-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="61640-129">Kopeerige tööajamääratlused esmaspäevalt kolmapäevale.</span><span class="sxs-lookup"><span data-stu-id="61640-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="61640-130">Tehke valik väljal **Kuni nädalapäevani**.</span><span class="sxs-lookup"><span data-stu-id="61640-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="61640-131">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="61640-131">Select **OK**.</span></span>
1. <span data-ttu-id="61640-132">Valige suvand **Kopeeri päev**.</span><span class="sxs-lookup"><span data-stu-id="61640-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="61640-133">Kopeerige tööajamääratlused esmaspäevalt neljapäevale.</span><span class="sxs-lookup"><span data-stu-id="61640-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="61640-134">Tehke valik väljal **Kuni nädalapäevani**.</span><span class="sxs-lookup"><span data-stu-id="61640-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="61640-135">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="61640-135">Select **OK**.</span></span>
1. <span data-ttu-id="61640-136">Valige suvand **Kopeeri päev**.</span><span class="sxs-lookup"><span data-stu-id="61640-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="61640-137">Kopeerige tööajamääratlused esmaspäevalt reedele.</span><span class="sxs-lookup"><span data-stu-id="61640-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="61640-138">Tehke valik väljal **Kuni nädalapäevani**.</span><span class="sxs-lookup"><span data-stu-id="61640-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="61640-139">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="61640-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="61640-140">Eritoimingute ajavahemike määratlemine</span><span class="sxs-lookup"><span data-stu-id="61640-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="61640-141">Laiendage jaotist **Reede**.</span><span class="sxs-lookup"><span data-stu-id="61640-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="61640-142">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="61640-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="61640-143">Valige või sisestage väärtus väljal **Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="61640-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="61640-144">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="61640-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="61640-145">Valige või sisestage väärtus väljal **Atribuut**.</span><span class="sxs-lookup"><span data-stu-id="61640-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="61640-146">Puhkepäevade märkimine komplekteerimiseks suletuks</span><span class="sxs-lookup"><span data-stu-id="61640-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="61640-147">Laiendage jaotist **Laupäev**.</span><span class="sxs-lookup"><span data-stu-id="61640-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="61640-148">Valige väljal *Komplekteerimiseks suletud* suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="61640-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="61640-149">Laiendage jaotist **Pühapäev**.</span><span class="sxs-lookup"><span data-stu-id="61640-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="61640-150">Valige väljal *Komplekteerimiseks suletud* suvand **Jah**.</span><span class="sxs-lookup"><span data-stu-id="61640-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]