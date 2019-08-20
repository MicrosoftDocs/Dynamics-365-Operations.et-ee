---
title: Kontsernisisese projekti arveldamise konfigureerimine
description: See protseduur käitab, kuidas häälestada projekti arveldamist organisatsiooni kahe ettevõtte vahel.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 53871db9223eef6ba78f2e327e60f45110891478
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838267"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="90ec0-103">Kontsernisisese projekti arveldamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="90ec0-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90ec0-104">See protseduur käitab, kuidas häälestada projekti arveldamist organisatsiooni kahe ettevõtte vahel.</span><span class="sxs-lookup"><span data-stu-id="90ec0-104">This procedure shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="90ec0-105">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="90ec0-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="90ec0-106">Minge jaotisse Ostureskontrod > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="90ec0-106">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="90ec0-107">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="90ec0-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="90ec0-108">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="90ec0-108">On the Action Pane, click General.</span></span>
4. <span data-ttu-id="90ec0-109">Klõpsake valikut Kontsernisisene.</span><span class="sxs-lookup"><span data-stu-id="90ec0-109">Click Intercompany.</span></span>
5. <span data-ttu-id="90ec0-110">Kontserdisisese kaubanduse lubamiseks määrake suvandi Aktiivne valikuks Jah.</span><span class="sxs-lookup"><span data-stu-id="90ec0-110">Set Active to Yes to enable intercompany trading.</span></span>
6. <span data-ttu-id="90ec0-111">Sisestage või valige väärtus väljal Kliendi ettevõte.</span><span class="sxs-lookup"><span data-stu-id="90ec0-111">In the Customer company field, enter or select a value.</span></span>
7. <span data-ttu-id="90ec0-112">Sisestage või valige väärtus väljal Minu konto.</span><span class="sxs-lookup"><span data-stu-id="90ec0-112">In the My account field, enter or select a value.</span></span>
8. <span data-ttu-id="90ec0-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="90ec0-113">Click Save.</span></span>
9. <span data-ttu-id="90ec0-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="90ec0-114">Close the page.</span></span>
10. <span data-ttu-id="90ec0-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="90ec0-115">Close the page.</span></span>
11. <span data-ttu-id="90ec0-116">Avage menüü Projektihaldus ja raamatupidamine > Häälestamine > Projektihalduse ja -arvestuse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="90ec0-116">Go to Project management and accounting > Setup > Project management and accounting parameters.</span></span>
12. <span data-ttu-id="90ec0-117">Klõpsake vahekaarti Kontsernisisene.</span><span class="sxs-lookup"><span data-stu-id="90ec0-117">Click the Intercompany tab.</span></span>
13. <span data-ttu-id="90ec0-118">Liigutage liugurit valikule Jah, et lubada kontsernisisene ressursside plaanimine ja ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="90ec0-118">Move the slider to Yes to enable intercompany resource scheduling and timesheets.</span></span>
14. <span data-ttu-id="90ec0-119">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="90ec0-119">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="90ec0-120">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="90ec0-120">Click New.</span></span>
16. <span data-ttu-id="90ec0-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="90ec0-121">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="90ec0-122">Sisestage või valige väärtus väljal Laenav juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="90ec0-122">In the Borrowing legal entity field, enter or select a value.</span></span>
18. <span data-ttu-id="90ec0-123">Märkige ruut Tulu lisamine.</span><span class="sxs-lookup"><span data-stu-id="90ec0-123">Select the Accrue revenue check box.</span></span>
19. <span data-ttu-id="90ec0-124">Sisestage või valige väärtus väljal Vaikeajatabeli kategooria.</span><span class="sxs-lookup"><span data-stu-id="90ec0-124">In the Default timesheet category field, enter or select a value.</span></span>
20. <span data-ttu-id="90ec0-125">Sisestage või valige väärtus väljal Vaikekulukategooria.</span><span class="sxs-lookup"><span data-stu-id="90ec0-125">In the Default expense category field, enter or select a value.</span></span>
21. <span data-ttu-id="90ec0-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="90ec0-126">Click Save.</span></span>
22. <span data-ttu-id="90ec0-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="90ec0-127">Close the page.</span></span>
23. <span data-ttu-id="90ec0-128">Avage Projektihaldus ja raamatupidamine > Häälestamine > Sisestamine > Pearaamatu sisestamise häälestamine.</span><span class="sxs-lookup"><span data-stu-id="90ec0-128">Go to Project management and accounting > Setup > Posting > Ledger posting setup.</span></span>
24. <span data-ttu-id="90ec0-129">Valige suvand väljal Pearaamatukontode tüübid.</span><span class="sxs-lookup"><span data-stu-id="90ec0-129">In the Ledger account types field, select an option.</span></span>
25. <span data-ttu-id="90ec0-130">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="90ec0-130">Click New.</span></span>
26. <span data-ttu-id="90ec0-131">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="90ec0-131">In the list, mark the selected row.</span></span>
27. <span data-ttu-id="90ec0-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="90ec0-132">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="90ec0-133">Täpsustage soovitud väärtusi väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="90ec0-133">In the Main account field, specify the desired values.</span></span>
29. <span data-ttu-id="90ec0-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="90ec0-134">Click Save.</span></span>
30. <span data-ttu-id="90ec0-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="90ec0-135">Close the page.</span></span>
31. <span data-ttu-id="90ec0-136">Avage Projektihaldus ja raamatupidamine > Häälestamine > Hinnad > Ülekande hind.</span><span class="sxs-lookup"><span data-stu-id="90ec0-136">Go to Project management and accounting > Setup > Prices > Transfer price.</span></span>
32. <span data-ttu-id="90ec0-137">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="90ec0-137">Click New.</span></span>
33. <span data-ttu-id="90ec0-138">Sisestage kuupäev väljale Jõustumiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="90ec0-138">In the Effective date field, enter a date.</span></span>
34. <span data-ttu-id="90ec0-139">Sisestage või valige väärtus väljal Laenav juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="90ec0-139">In the Borrowing legal entity field, enter or select a value.</span></span>
35. <span data-ttu-id="90ec0-140">Valige suvand väljal Ülekande hinnamudel.</span><span class="sxs-lookup"><span data-stu-id="90ec0-140">In the Transfer price model field, select an option.</span></span>
36. <span data-ttu-id="90ec0-141">Väljale Hinnakujundus sisestage number.</span><span class="sxs-lookup"><span data-stu-id="90ec0-141">In the Pricing field, enter a number.</span></span>
37. <span data-ttu-id="90ec0-142">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="90ec0-142">Click Save.</span></span>

