---
title: Töötaja konfigureerimine töö mobiilse seadme abil
description: See protseduur näitab, kuidas määrata töötaja kasutajakontole õigeid rolle ja lubada siis töötajal teha tööde juhtimise moodulis registreerimisi.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1571354"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="5b3a9-103">Töötaja konfigureerimine töö mobiilse seadme abil</span><span class="sxs-lookup"><span data-stu-id="5b3a9-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b3a9-104">See protseduur näitab, kuidas määrata töötaja kasutajakontole õigeid rolle ja lubada siis töötajal teha tööde juhtimise moodulis registreerimisi.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="5b3a9-105">Kasutajakontole rollide määramine</span><span class="sxs-lookup"><span data-stu-id="5b3a9-105">Assign roles to user account</span></span>
1. <span data-ttu-id="5b3a9-106">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="5b3a9-107">Kasutage kiirfiltrit töötaja nime filtreerimiseks, kui kasutajakonto on seotud masina operaatori rolliga.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="5b3a9-108">Näidisandmetes oleks see nimi Shannon.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="5b3a9-109">Tõstke soovitud kasutajakonto kirje esile.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="5b3a9-110">Klõpsake loendis valitud real linki Nimi, et vaadata kasutajakonto üksikasju.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="5b3a9-111">Valige puul Rollid \ Masina operaator.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="5b3a9-112">Sulgege kasutajakonto üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-112">Close the user account details page.</span></span>
7. <span data-ttu-id="5b3a9-113">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="5b3a9-114">Töötaja konto konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-114">Configure worker account.</span></span>
1. <span data-ttu-id="5b3a9-115">Avage Personaliarvestus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="5b3a9-116">Kasutage kiirfiltrit töötaja nime filtreerimiseks, kui kasutajakonto on seotud masina operaatori rolliga.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="5b3a9-117">Näidisandmetes oleks see nimi Shannon.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="5b3a9-118">Tõstke soovitud kasutajakonto kirje esile.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="5b3a9-119">Klõpsake loendis valitud real linki Nimi, et vaadata kasutajakonto üksikasju.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="5b3a9-120">Klõpsake vahekaarti Tööhõive.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="5b3a9-121">Laiendage kiirkaarti Ajaline registreerimine ja klõpsake valikut Aktiveeri registreerimisterminalides.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="5b3a9-122">Klõpsake valikut Aktiveeri registreerimisterminalides.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="5b3a9-123">Sisestage või valige väärtus väljal Arvutusgrupp.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="5b3a9-124">Sisestage või valige väärtus väljal Vaike-arvutusgrupp.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="5b3a9-125">Sisestage või valige väärtus väljal Kinnitusgrupp.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="5b3a9-126">Sisestage või valige väärtus väljal Standardreeglid.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="5b3a9-127">Sisestage või valige väärtus väljal Reegligrupp.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="5b3a9-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-128">Click OK.</span></span>
14. <span data-ttu-id="5b3a9-129">Klõpsake nuppu Redigeeri uue töötajale kellaaja registreerimise pääsme numbri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="5b3a9-130">Sisestage väärtus väljale Pääsme ID.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="5b3a9-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-131">Click Save.</span></span>
17. <span data-ttu-id="5b3a9-132">Kasutage kirje salvestamise otseteed.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="5b3a9-133">Sulgege töötaja üksikasjade leht.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-133">Close the worker details page.</span></span>
19. <span data-ttu-id="5b3a9-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="5b3a9-135">Määrake seadmegrupile töötaja.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="5b3a9-136">Avage Tootmise juhtimine > Seadistus > Tootmise käivitamine > Töökaardi konfigureerimine seadmetele.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="5b3a9-137">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-137">Click Add.</span></span>
3. <span data-ttu-id="5b3a9-138">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="5b3a9-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-139">Click OK.</span></span>
5. <span data-ttu-id="5b3a9-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-140">Click Edit.</span></span>
6. <span data-ttu-id="5b3a9-141">Väljal Tootmisüksus saate määrata töötajale vaikefiltri.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="5b3a9-142">See tagab, et kui töötaja seadmesse sisse logib, kuvatakse ainult valitud tootmisüksuse tootmistööd.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="5b3a9-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5b3a9-143">Close the page.</span></span>

