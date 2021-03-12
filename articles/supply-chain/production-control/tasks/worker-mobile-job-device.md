---
title: Töötaja konfigureerimine töö mobiilse seadme abil
description: Selles teemas selgitatakse töötaja kasutajakontole õigete rollide määramist ja töötajale tööde juhtimise süsteemi registreerimiste tegemise lubamist.
author: ShylaThompson
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 89b75936ea9c0f25f82175a1871088da8fd74ad6
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980927"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="02d60-103">Töötaja konfigureerimine töö mobiilse seadme abil</span><span class="sxs-lookup"><span data-stu-id="02d60-103">Configure a worker using the mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02d60-104">Selles teemas selgitatakse töötaja kasutajakontole õigete rollide määramist ja töötajale tööde juhtimise süsteemi registreerimiste tegemise lubamist.</span><span class="sxs-lookup"><span data-stu-id="02d60-104">This topic explains how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a><span data-ttu-id="02d60-105">Töötajale teatud rolli määramise kontrollimine</span><span class="sxs-lookup"><span data-stu-id="02d60-105">Verify that a worker is assigned a certain role</span></span>

<span data-ttu-id="02d60-106">Selles näites kontrollige enne töötaja konto konfigureerimist, et „SHANNONILE“ on määratud maisina operaatori roll.</span><span class="sxs-lookup"><span data-stu-id="02d60-106">For this example, verify that user "SHANNON" is assigned the machine operator role before you configure the worker account.</span></span>

1. <span data-ttu-id="02d60-107">Avage **Navigeerimispaan > Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="02d60-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="02d60-108">Otsige kasutajat kiirfiltrist.</span><span class="sxs-lookup"><span data-stu-id="02d60-108">Search for a user in the quick filter.</span></span> <span data-ttu-id="02d60-109">Selles näites sisestage `shannon`.</span><span class="sxs-lookup"><span data-stu-id="02d60-109">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="02d60-110">Valige link kuvatava kasutajakonto veerus **Kasutaja ID**.</span><span class="sxs-lookup"><span data-stu-id="02d60-110">Select the link in the **User ID** column of the user account that appears.</span></span>
4. <span data-ttu-id="02d60-111">Valige puus **Kasutaja rollid** jaotis **Rollid > Masina operaator**.</span><span class="sxs-lookup"><span data-stu-id="02d60-111">In the **User's roles** tree, select **Roles > Machine operator**.</span></span>
5. <span data-ttu-id="02d60-112">Avalehele naasmiseks sulgege lehed **kasutaja üksikasjad** ja **kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="02d60-112">Close the **user details** and **users** pages to return to the home page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="02d60-113">Töötaja konto konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="02d60-113">Configure worker account</span></span>
1. <span data-ttu-id="02d60-114">Avage **Navigeerimispaan > Moodulid > Inimressursid > Töötajad > Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="02d60-114">Go to **Navigation pane > Modules > Human resources > Workers > Workers**.</span></span>
2. <span data-ttu-id="02d60-115">Otsige kasutajat kiirfiltrist.</span><span class="sxs-lookup"><span data-stu-id="02d60-115">Search for a user in the quick filter.</span></span> <span data-ttu-id="02d60-116">Selles näites sisestage `shannon`.</span><span class="sxs-lookup"><span data-stu-id="02d60-116">For this example, enter `shannon`.</span></span>
3. <span data-ttu-id="02d60-117">Valige link kuvatava kasutajakonto veerus **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="02d60-117">Select the link in the **Name** column of the user account that appears.</span></span>
4. <span data-ttu-id="02d60-118">Valige vahekaart **Aja registreerimine**.</span><span class="sxs-lookup"><span data-stu-id="02d60-118">Select the **Time registration** tab.</span></span>
5. <span data-ttu-id="02d60-119">Valige **Registreerimisterminaalides aktiveerimine**.</span><span class="sxs-lookup"><span data-stu-id="02d60-119">Select **Activate on registration terminals**.</span></span>
6. <span data-ttu-id="02d60-120">Sisestage või valige väärtused järgmistele väljadele.</span><span class="sxs-lookup"><span data-stu-id="02d60-120">Enter or select values in the following fields:</span></span>  

    - <span data-ttu-id="02d60-121">**Kalkulatsioonigrupp**</span><span class="sxs-lookup"><span data-stu-id="02d60-121">**Calculation group**</span></span>  
    - <span data-ttu-id="02d60-122">**Vaike-arvutusgrupp**</span><span class="sxs-lookup"><span data-stu-id="02d60-122">**Default calculation group**</span></span>  
    - <span data-ttu-id="02d60-123">**Kinnitusegrupp**</span><span class="sxs-lookup"><span data-stu-id="02d60-123">**Approval group**</span></span>  
    - <span data-ttu-id="02d60-124">**Standardreeglid**</span><span class="sxs-lookup"><span data-stu-id="02d60-124">**Standard profile**</span></span>  
    - <span data-ttu-id="02d60-125">**Reegligrupp**</span><span class="sxs-lookup"><span data-stu-id="02d60-125">**Profile group**</span></span>  

7. <span data-ttu-id="02d60-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="02d60-126">Select **OK**.</span></span>
8. <span data-ttu-id="02d60-127">Uue kellaaja registreerimisega töötaja märgi numbri sisestamiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="02d60-127">Select **Edit** to enter a badge number for the new time registration worker.</span></span> <span data-ttu-id="02d60-128">Sisestage väärtus väljale **Märgi ID**.</span><span class="sxs-lookup"><span data-stu-id="02d60-128">Enter a value in the **Badge ID** field.</span></span>
9. <span data-ttu-id="02d60-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="02d60-129">Select **Save**.</span></span>
10. <span data-ttu-id="02d60-130">Sulgege lehed **Töötaja üksikasjad** ja **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="02d60-130">Close the **Worker details** and **Workers** pages.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="02d60-131">Seadmete rühmale töötaja määramine</span><span class="sxs-lookup"><span data-stu-id="02d60-131">Assign worker to device group</span></span>
1. <span data-ttu-id="02d60-132">Avage **Tootmise juhtimine > Häälestus > Tootmise käivitamine > Seadmete töökaardi konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="02d60-132">Go to **Production control > Setup > Manufacturing execution > Configure job card for devices**.</span></span>
2. <span data-ttu-id="02d60-133">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="02d60-133">Select **Add**.</span></span>
3. <span data-ttu-id="02d60-134">Valige loendist soovitud töötaja.</span><span class="sxs-lookup"><span data-stu-id="02d60-134">In the list, select the desired worker.</span></span> <span data-ttu-id="02d60-135">Selles näites valige **SHANNON**.</span><span class="sxs-lookup"><span data-stu-id="02d60-135">For this example, select **SHANNON**.</span></span>
4. <span data-ttu-id="02d60-136">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="02d60-136">Select **OK**.</span></span>
5. <span data-ttu-id="02d60-137">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="02d60-137">Select **Edit**.</span></span>
6. <span data-ttu-id="02d60-138">Väljal **Tootmisüksus** saate määrata töötajale vaikefiltri.</span><span class="sxs-lookup"><span data-stu-id="02d60-138">In the **Production unit** field, you can set the default filter for the worker.</span></span> <span data-ttu-id="02d60-139">See tagab, et kui töötaja seadmesse sisse logib, kuvatakse ainult valitud tootmisüksuse tootmistööd.</span><span class="sxs-lookup"><span data-stu-id="02d60-139">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span> <span data-ttu-id="02d60-140">Sisestage soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="02d60-140">Enter the desired value.</span></span>
7. <span data-ttu-id="02d60-141">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="02d60-141">Close the page.</span></span>

