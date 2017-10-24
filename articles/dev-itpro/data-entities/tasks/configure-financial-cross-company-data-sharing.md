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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 779722bd3acd10a85b089a4d30757b62293ea4e4
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="f93b8-103">Kontsernisisese finantsandmete ühiskasutuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f93b8-103">Configure financial cross-company data sharing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f93b8-104">Selles protseduuris selgitatakse, kuidas konfigureerida, lubada, kinnitada ja lahendada konflikte ettevõtete vahel andmeid ühiskasutades.</span><span class="sxs-lookup"><span data-stu-id="f93b8-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="f93b8-105">See kasutab USMF-ettevõtet ja finantsandmete ühiskasutuse malli.</span><span class="sxs-lookup"><span data-stu-id="f93b8-105">It uses the USMF company and the Financial data sharing template.</span></span>



<span data-ttu-id="f93b8-106">Selle ülesande juhise jaoks on nõutav Dynamics AX-i platvorm 7.1 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="f93b8-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="f93b8-107">Avage Süsteemihaldus > Tööruumid > Andmehaldus.</span><span class="sxs-lookup"><span data-stu-id="f93b8-107">Go to System administration > Workspaces > Data management.</span></span>
2. <span data-ttu-id="f93b8-108">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="f93b8-108">Click Import.</span></span>
3. <span data-ttu-id="f93b8-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="f93b8-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f93b8-110">Valige pakendi tüüp väljal Lähteandmete vorming.</span><span class="sxs-lookup"><span data-stu-id="f93b8-110">In the Source data format field, select the Package type.</span></span>
    * <span data-ttu-id="f93b8-111">Klõpsake Üleslaadimine.</span><span class="sxs-lookup"><span data-stu-id="f93b8-111">Click Upload.</span></span> <span data-ttu-id="f93b8-112">Liikuge finantsandmete ühiskasutuse malli paketifaili asukohta ja valige see fail.</span><span class="sxs-lookup"><span data-stu-id="f93b8-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>  
5. <span data-ttu-id="f93b8-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f93b8-113">Click Save.</span></span>
6. <span data-ttu-id="f93b8-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f93b8-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f93b8-115">Valige andmete ühiskasutuspoliitika, mis äsja loodi.</span><span class="sxs-lookup"><span data-stu-id="f93b8-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="f93b8-116">Klõpsake Import.</span><span class="sxs-lookup"><span data-stu-id="f93b8-116">Click Import.</span></span>
8. <span data-ttu-id="f93b8-117">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="f93b8-117">Click Close.</span></span>
9. <span data-ttu-id="f93b8-118">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="f93b8-118">Refresh the page.</span></span>
10. <span data-ttu-id="f93b8-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f93b8-119">Close the page.</span></span>
11. <span data-ttu-id="f93b8-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f93b8-120">Close the page.</span></span>
12. <span data-ttu-id="f93b8-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f93b8-121">Close the page.</span></span>
13. <span data-ttu-id="f93b8-122">Avage süsteemihaldus > Seadistus > Kontsernisisese andmete ühiskasutuse konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="f93b8-122">Go to System administration > Setup > Configure cross-company data sharing.</span></span>
14. <span data-ttu-id="f93b8-123">Otsige loendist ja valige maksepäevad.</span><span class="sxs-lookup"><span data-stu-id="f93b8-123">In the list, find and select Payment days.</span></span>
15. <span data-ttu-id="f93b8-124">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f93b8-124">Click Add.</span></span>
16. <span data-ttu-id="f93b8-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f93b8-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="f93b8-126">Tippige USSI väljale Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="f93b8-126">In the Company field, type 'USSI'.</span></span>
18. <span data-ttu-id="f93b8-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f93b8-127">Click Add.</span></span>
19. <span data-ttu-id="f93b8-128">Tippige USMF väljale Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="f93b8-128">In the Company field, type 'USMF'.</span></span>
20. <span data-ttu-id="f93b8-129">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="f93b8-129">Click Save.</span></span>
21. <span data-ttu-id="f93b8-130">Klõpsake käsku Luba.</span><span class="sxs-lookup"><span data-stu-id="f93b8-130">Click Enable.</span></span>
22. <span data-ttu-id="f93b8-131">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="f93b8-131">Click Yes.</span></span>
23. <span data-ttu-id="f93b8-132">Klõpsake käsku Otsi ühiskasutusprobleeme.</span><span class="sxs-lookup"><span data-stu-id="f93b8-132">Click Find sharing issues.</span></span>
24. <span data-ttu-id="f93b8-133">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="f93b8-133">Click Yes.</span></span>
25. <span data-ttu-id="f93b8-134">Klõpsake käsku Värskenda välja väärtust.</span><span class="sxs-lookup"><span data-stu-id="f93b8-134">Click Update field value.</span></span>
26. <span data-ttu-id="f93b8-135">Klõpsake käsku Kasuta väärtust ettevõttest 1.</span><span class="sxs-lookup"><span data-stu-id="f93b8-135">Click Use value from company 1.</span></span>
27. <span data-ttu-id="f93b8-136">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="f93b8-136">Refresh the page.</span></span>
28. <span data-ttu-id="f93b8-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f93b8-137">Close the page.</span></span>


