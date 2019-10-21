---
title: Saate häälestada ametikohti
description: Ametikohad on organisatsioonihierarhia madalama taseme oluline element.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fd355fb6c3d2742e046a616585ca349c623341d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190254"
---
# <a name="set-up-positions"></a><span data-ttu-id="b0663-103">Saate häälestada ametikohti</span><span class="sxs-lookup"><span data-stu-id="b0663-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0663-104">Ametikohad on organisatsioonihierarhia madalama taseme oluline element.</span><span class="sxs-lookup"><span data-stu-id="b0663-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="b0663-105">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="b0663-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="b0663-106">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="b0663-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="b0663-107">Osakonnas on töökoht ja sellega võib olla seostatud ainult üks töötaja.</span><span class="sxs-lookup"><span data-stu-id="b0663-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="b0663-108">Selles ülesandes tutvustatakse ametikoha loomiseks nõutavaid etappe.</span><span class="sxs-lookup"><span data-stu-id="b0663-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="b0663-109">See protseduur on mõeldud inimressursside spetsialistidele.</span><span class="sxs-lookup"><span data-stu-id="b0663-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="b0663-110">Klõpsake vahekaarti Tööjõu haldus.</span><span class="sxs-lookup"><span data-stu-id="b0663-110">Click Workforce management.</span></span>
2. <span data-ttu-id="b0663-111">Klõpsake suvandil Avatud ametikohad.</span><span class="sxs-lookup"><span data-stu-id="b0663-111">Click Open positions.</span></span>
3. <span data-ttu-id="b0663-112">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b0663-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="b0663-113">Sisestage või valige väärtus väljal Töö.</span><span class="sxs-lookup"><span data-stu-id="b0663-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="b0663-114">Töö kirjeldus, ametinimetus ja täistööajaga samaväärse tööhõive tegur kopeeritakse automaatselt valitud tööst ametikohale.</span><span class="sxs-lookup"><span data-stu-id="b0663-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="b0663-115">Töö toiming ResolveChanges.</span><span class="sxs-lookup"><span data-stu-id="b0663-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="b0663-116">Klõpsake käsku Loo ametikoht.</span><span class="sxs-lookup"><span data-stu-id="b0663-116">Click Create position.</span></span>
7. <span data-ttu-id="b0663-117">Sisestage või valige väärtus väljal Osakond.</span><span class="sxs-lookup"><span data-stu-id="b0663-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="b0663-118">Sisestage või valige väärtus väljal Ametikoha tüüp.</span><span class="sxs-lookup"><span data-stu-id="b0663-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="b0663-119">Sisestage või valige väärtus väljal Hüvituspiirkond.</span><span class="sxs-lookup"><span data-stu-id="b0663-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="b0663-120">Hüvituspiirkond määrab hüvituse sobivuse reeglid ja fikseeritud kasvuga eelarved, mis kehtivad töötajale sellel ametikohal.</span><span class="sxs-lookup"><span data-stu-id="b0663-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="b0663-121">Sisestage kuupäev ja kellaaeg väljal Määramiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="b0663-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="b0663-122">Laiendage jaotist Ametikoha kestus.</span><span class="sxs-lookup"><span data-stu-id="b0663-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="b0663-123">Amerikoha kestus sisestatakse vaikimisi varem sisestatud aktiveerimise ja pensionile minemise kuupäevade alusel</span><span class="sxs-lookup"><span data-stu-id="b0663-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="b0663-124">Laiendage jaotist Millisele ametikohale annab aru.</span><span class="sxs-lookup"><span data-stu-id="b0663-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="b0663-125">Kui määrate töötaja ametikohale, mis annab aru teisele ametikohale, loote neile kahele ametikohale määratud töötajate vahel otsese aruandlusseose.</span><span class="sxs-lookup"><span data-stu-id="b0663-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="b0663-126">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b0663-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b0663-127">Sisestage või valige väärtus väljal Aruannete sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="b0663-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="b0663-128">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="b0663-128">Click Create.</span></span>
16. <span data-ttu-id="b0663-129">Laiendage jaotist Töötaja määramine.</span><span class="sxs-lookup"><span data-stu-id="b0663-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="b0663-130">Laiendage jaotist Seosed.</span><span class="sxs-lookup"><span data-stu-id="b0663-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="b0663-131">Kui teie organisatsioon kasutab maatrikshierarhiat või mõnd muud kohandatud hierarhiat, saate seadistada ametikohahierarhia tüübid ja seejärel lisada iga seadistatud hierarhiatüübi puhul aruandlusseosed ametikohtadele.</span><span class="sxs-lookup"><span data-stu-id="b0663-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="b0663-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="b0663-132">Click Add.</span></span>
19. <span data-ttu-id="b0663-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b0663-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="b0663-134">Sisestage või valige väärtus väljal Hierarhia nimi.</span><span class="sxs-lookup"><span data-stu-id="b0663-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="b0663-135">Sisestage või valige väärtus väljal Millisele ametikohale annab aru.</span><span class="sxs-lookup"><span data-stu-id="b0663-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="b0663-136">Laiendage jaotist Palk.</span><span class="sxs-lookup"><span data-stu-id="b0663-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="b0663-137">Sisestage või valige väärtus väljal Palgatsükkel.</span><span class="sxs-lookup"><span data-stu-id="b0663-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="b0663-138">Sisestage või valige väärtus väljal Maksja.</span><span class="sxs-lookup"><span data-stu-id="b0663-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="b0663-139">Sisestage number väljale Iga-aastased töötunnid.</span><span class="sxs-lookup"><span data-stu-id="b0663-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="b0663-140">See on sellel ametikohal töötava töötaja iga-aastane eeldatav töötundide arv.</span><span class="sxs-lookup"><span data-stu-id="b0663-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="b0663-141">Laiendage jaotist Ametiühing.</span><span class="sxs-lookup"><span data-stu-id="b0663-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="b0663-142">Ahendage jaotist Ametiühing.</span><span class="sxs-lookup"><span data-stu-id="b0663-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="b0663-143">Laiendage jaotist Financial dimensions (Finantsdimensioonid).</span><span class="sxs-lookup"><span data-stu-id="b0663-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="b0663-144">Sisestage või valige väärtus väljal Jaotusmall.</span><span class="sxs-lookup"><span data-stu-id="b0663-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="b0663-145">Sisestage või valige väärtus väljal Osakond.</span><span class="sxs-lookup"><span data-stu-id="b0663-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="b0663-146">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b0663-146">Click Save.</span></span>

