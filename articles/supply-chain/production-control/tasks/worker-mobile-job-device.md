--- 
title: "Töötaja konfigureerimine töö mobiilse seadme abil"
description: "See protseduur näitab, kuidas määrata töötaja kasutajakontole õigeid rolle ja lubada siis töötajal teha tööde juhtimise moodulis registreerimisi."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d56f861dbbf579e44fcd3fc4d8b45c24029acecc
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="a47f2-103">Töötaja konfigureerimine töö mobiilse seadme abil</span><span class="sxs-lookup"><span data-stu-id="a47f2-103">Configure a worker using the mobile job device</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a47f2-104">See protseduur näitab, kuidas määrata töötaja kasutajakontole õigeid rolle ja lubada siis töötajal teha tööde juhtimise moodulis registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="a47f2-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="a47f2-105">Kasutajakontole rollide määramine</span><span class="sxs-lookup"><span data-stu-id="a47f2-105">Assign roles to user account</span></span>
1. <span data-ttu-id="a47f2-106">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="a47f2-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="a47f2-107">Kasutage kiirfiltrit töötaja nime filtreerimiseks, kui kasutajakonto on seotud masina operaatori rolliga.</span><span class="sxs-lookup"><span data-stu-id="a47f2-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="a47f2-108">Näidisandmetes oleks see nimi Shannon.</span><span class="sxs-lookup"><span data-stu-id="a47f2-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="a47f2-109">Tõstke soovitud kasutajakonto kirje esile.</span><span class="sxs-lookup"><span data-stu-id="a47f2-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="a47f2-110">Klõpsake loendis valitud real linki Nimi, et vaadata kasutajakonto üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a47f2-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="a47f2-111">Valige puul Rollid \ Masina operaator.</span><span class="sxs-lookup"><span data-stu-id="a47f2-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="a47f2-112">Sulgege kasutajakonto üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="a47f2-112">Close the user account details page.</span></span>
7. <span data-ttu-id="a47f2-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a47f2-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="a47f2-114">Töötaja konto konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="a47f2-114">Configure worker account.</span></span>
1. <span data-ttu-id="a47f2-115">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="a47f2-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="a47f2-116">Kasutage kiirfiltrit töötaja nime filtreerimiseks, kui kasutajakonto on seotud masina operaatori rolliga.</span><span class="sxs-lookup"><span data-stu-id="a47f2-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="a47f2-117">Näidisandmetes oleks see nimi Shannon.</span><span class="sxs-lookup"><span data-stu-id="a47f2-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="a47f2-118">Tõstke soovitud kasutajakonto kirje esile.</span><span class="sxs-lookup"><span data-stu-id="a47f2-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="a47f2-119">Klõpsake loendis valitud real linki Nimi, et vaadata kasutajakonto üksikasju.</span><span class="sxs-lookup"><span data-stu-id="a47f2-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="a47f2-120">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="a47f2-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="a47f2-121">Laiendage kiirkaarti Ajaline registreerimine ja klõpsake valikut Aktiveeri registreerimisterminalides.</span><span class="sxs-lookup"><span data-stu-id="a47f2-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="a47f2-122">Klõpsake valikut Aktiveeri registreerimisterminalides.</span><span class="sxs-lookup"><span data-stu-id="a47f2-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="a47f2-123">Sisestage või valige väärtus väljal Arvutusgrupp.</span><span class="sxs-lookup"><span data-stu-id="a47f2-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="a47f2-124">Sisestage või valige väärtus väljal Vaike-arvutusgrupp.</span><span class="sxs-lookup"><span data-stu-id="a47f2-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="a47f2-125">Sisestage või valige väärtus väljal Kinnitusgrupp.</span><span class="sxs-lookup"><span data-stu-id="a47f2-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="a47f2-126">Sisestage või valige väärtus väljal Standardreeglid.</span><span class="sxs-lookup"><span data-stu-id="a47f2-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="a47f2-127">Sisestage või valige väärtus väljal Reegligrupp.</span><span class="sxs-lookup"><span data-stu-id="a47f2-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="a47f2-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a47f2-128">Click OK.</span></span>
14. <span data-ttu-id="a47f2-129">Klõpsake nuppu Redigeeri uue töötajale kellaaja registreerimise pääsme numbri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="a47f2-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="a47f2-130">Sisestage väärtus väljale Pääsme ID.</span><span class="sxs-lookup"><span data-stu-id="a47f2-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="a47f2-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a47f2-131">Click Save.</span></span>
17. <span data-ttu-id="a47f2-132">Kasutage kirje salvestamise otseteed.</span><span class="sxs-lookup"><span data-stu-id="a47f2-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="a47f2-133">Sulgege töötaja üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="a47f2-133">Close the worker details page.</span></span>
19. <span data-ttu-id="a47f2-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a47f2-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="a47f2-135">Määrake seadmegrupile töötaja.</span><span class="sxs-lookup"><span data-stu-id="a47f2-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="a47f2-136">Avage Tootmise juhtimine > Seadistus > Tootmise käivitamine > Töökaardi konfigureerimine seadmetele.</span><span class="sxs-lookup"><span data-stu-id="a47f2-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="a47f2-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a47f2-137">Click Add.</span></span>
3. <span data-ttu-id="a47f2-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a47f2-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a47f2-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a47f2-139">Click OK.</span></span>
5. <span data-ttu-id="a47f2-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a47f2-140">Click Edit.</span></span>
6. <span data-ttu-id="a47f2-141">Väljal Tootmisüksus saate määrata töötajale vaikefiltri.</span><span class="sxs-lookup"><span data-stu-id="a47f2-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="a47f2-142">See tagab, et kui töötaja seadmesse sisse logib, kuvatakse ainult valitud tootmisüksuse tootmistööd.</span><span class="sxs-lookup"><span data-stu-id="a47f2-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="a47f2-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a47f2-143">Close the page.</span></span>


