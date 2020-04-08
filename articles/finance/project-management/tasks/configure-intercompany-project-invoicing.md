---
title: Kontsernisisese projekti arveldamise konfigureerimine
description: Selles teemas selgitatakse, kuidas seadistada projekti arveldamist oma organisatsiooni kahe ettevõtte vahel.
author: KimANelson
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 31dbae2d37aefe1841fe85cb6caf185c78596e55
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144275"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="e775f-103">Kontsernisisese projekti arveldamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e775f-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e775f-104">Selles teemas selgitatakse, kuidas seadistada projekti arveldamist oma organisatsiooni kahe ettevõtte vahel.</span><span class="sxs-lookup"><span data-stu-id="e775f-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="e775f-105">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="e775f-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e775f-106">Navigeerimispaanil avage **Moodulid > Ostureskontro > Hankijad > Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="e775f-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="e775f-107">Loendist **Kõik müüjad** leidke ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e775f-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="e775f-108">Valige toimingupaanil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="e775f-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="e775f-109">Valige **Kontsernisisene**.</span><span class="sxs-lookup"><span data-stu-id="e775f-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="e775f-110">Seadke oleku **Aktiivne** väärtuseks **Jah**, et lubada kontsernisisene kaubandus.</span><span class="sxs-lookup"><span data-stu-id="e775f-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="e775f-111">Väljale **Kliendi ettevõte** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e775f-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="e775f-112">Väljale **Minu konto** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e775f-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="e775f-113">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e775f-113">Select **Save**.</span></span>
9. <span data-ttu-id="e775f-114">Avalehele naasmiseks sulgege leheküljed.</span><span class="sxs-lookup"><span data-stu-id="e775f-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="e775f-115">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Projektihalduse ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e775f-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="e775f-116">Valige vahekaart **Kontsernisisene**.</span><span class="sxs-lookup"><span data-stu-id="e775f-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="e775f-117">Liigutage liugur väärtusele **Jah**, et lubada kontsernisisene ressursside plaanimine ja ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="e775f-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="e775f-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e775f-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="e775f-119">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e775f-119">Select **New**.</span></span>
15. <span data-ttu-id="e775f-120">Väljale **Laenav juriidiline isik** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e775f-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="e775f-121">Valige märkeruut **Tekkepõhine tulu**.</span><span class="sxs-lookup"><span data-stu-id="e775f-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="e775f-122">Väljale **Vaikeajatabeli kategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e775f-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="e775f-123">Väljale **Vaikekulukategooria** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e775f-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="e775f-124">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e775f-124">Select **Save**.</span></span>
20. <span data-ttu-id="e775f-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e775f-125">Close the page.</span></span>
21. <span data-ttu-id="e775f-126">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Sisestamine > Pearaamatu sisestamise seadistus**.</span><span class="sxs-lookup"><span data-stu-id="e775f-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="e775f-127">Väljale **Pearaamatu konto tüübid** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="e775f-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="e775f-128">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e775f-128">Select **New**.</span></span>
24. <span data-ttu-id="e775f-129">Uue rea väljal **Põhikonto** täpsustage soovitud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="e775f-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="e775f-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e775f-130">Select **Save**.</span></span>
26. <span data-ttu-id="e775f-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e775f-131">Close the page.</span></span>
27. <span data-ttu-id="e775f-132">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Seadistus > Hinnad > Sisehind**.</span><span class="sxs-lookup"><span data-stu-id="e775f-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="e775f-133">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e775f-133">Select **New**.</span></span>
29. <span data-ttu-id="e775f-134">Väljale **Jõustumiskuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="e775f-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="e775f-135">Väljale **Laenav juriidiline isik** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="e775f-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="e775f-136">Väljale **Sisehinna mudel** valige sobiv variant.</span><span class="sxs-lookup"><span data-stu-id="e775f-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="e775f-137">Väljale **Hinnakujundus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="e775f-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="e775f-138">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e775f-138">Select **Save**.</span></span>

