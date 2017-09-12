--- 
title: "Kontsernisisese finantsandmete ühiskasutuse konfigureerimine"
description: "Selles protseduuris selgitatakse, kuidas konfigureerida, lubada, kinnitada ja lahendada konflikte ettevõtete vahel andmeid ühiskasutades."
author: aprilolson
manager: AnnBe
ms.date: 06/22/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d36f19b5fa617169d33e7720e6a7602581cb525a
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="ae710-103">Kontsernisisese finantsandmete ühiskasutuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ae710-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae710-104">Selles protseduuris selgitatakse, kuidas konfigureerida, lubada, kinnitada ja lahendada konflikte ettevõtete vahel andmeid ühiskasutades.</span><span class="sxs-lookup"><span data-stu-id="ae710-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="ae710-105">See kasutab USMF-ettevõtet ja finantsandmete ühiskasutuse malli.</span><span class="sxs-lookup"><span data-stu-id="ae710-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="ae710-106">Selle ülesande juhise jaoks on nõutav Dynamics AX-i platvorm 7.1 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="ae710-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="ae710-107">Avage Süsteemihaldus > Tööruumid > Andmehaldus.</span><span class="sxs-lookup"><span data-stu-id="ae710-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="ae710-108">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="ae710-108">Click Import.</span></span>
3. <span data-ttu-id="ae710-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ae710-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ae710-110">Valige pakendi tüüp väljal Lähteandmete vorming.</span><span class="sxs-lookup"><span data-stu-id="ae710-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="ae710-111">Klõpsake Üleslaadimine.</span><span class="sxs-lookup"><span data-stu-id="ae710-111">Click Upload.</span></span> <span data-ttu-id="ae710-112">Liikuge finantsandmete ühiskasutuse malli paketifaili asukohta ja valige see fail.</span><span class="sxs-lookup"><span data-stu-id="ae710-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="ae710-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ae710-113">Click Save.</span></span>
6. <span data-ttu-id="ae710-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ae710-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ae710-115">Valige andmete ühiskasutuspoliitika, mis äsja loodi.</span><span class="sxs-lookup"><span data-stu-id="ae710-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="ae710-116">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="ae710-116">Click Import.</span></span>
8. <span data-ttu-id="ae710-117">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="ae710-117">Click Close.</span></span>
9. <span data-ttu-id="ae710-118">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="ae710-118">Refresh the page.</span></span>
10. <span data-ttu-id="ae710-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ae710-119">Close the page.</span></span>
11. <span data-ttu-id="ae710-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ae710-120">Close the page.</span></span>
12. <span data-ttu-id="ae710-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ae710-121">Close the page.</span></span>
13. <span data-ttu-id="ae710-122">Avage süsteemihaldus > Seadistus > Kontsernisisese andmete ühiskasutuse konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="ae710-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="ae710-123">Otsige loendist ja valige maksepäevad.</span><span class="sxs-lookup"><span data-stu-id="ae710-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="ae710-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="ae710-124">Click Add.</span></span>
16. <span data-ttu-id="ae710-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ae710-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ae710-126">Tippige USSI väljale Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="ae710-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="ae710-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="ae710-127">Click Add.</span></span>
19. <span data-ttu-id="ae710-128">Tippige USMF väljale Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="ae710-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="ae710-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ae710-129">Click Save.</span></span>
21. <span data-ttu-id="ae710-130">Klõpsake käsku Luba.</span><span class="sxs-lookup"><span data-stu-id="ae710-130">Click Enable.</span></span>
22. <span data-ttu-id="ae710-131">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="ae710-131">Click Yes.</span></span>
23. <span data-ttu-id="ae710-132">Klõpsake käsku Otsi ühiskasutusprobleeme.</span><span class="sxs-lookup"><span data-stu-id="ae710-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="ae710-133">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="ae710-133">Click Yes.</span></span>
25. <span data-ttu-id="ae710-134">Klõpsake käsku Värskenda välja väärtust.</span><span class="sxs-lookup"><span data-stu-id="ae710-134">Click Update field value.</span></span>
26. <span data-ttu-id="ae710-135">Klõpsake käsku Kasuta väärtust ettevõttest 1.</span><span class="sxs-lookup"><span data-stu-id="ae710-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="ae710-136">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="ae710-136">Refresh the page.</span></span>
28. <span data-ttu-id="ae710-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ae710-137">Close the page.</span></span>


