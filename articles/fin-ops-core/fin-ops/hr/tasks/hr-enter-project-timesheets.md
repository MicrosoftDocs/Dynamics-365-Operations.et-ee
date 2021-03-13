---
title: Projekti ajatabelite sisestamine
description: See protseduur laseb teil luua ajatabeli, kasutades tühja ajatabelivormi.
author: andreabichsel
manager: tfehr
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d4a600137fc583aef8c85c920ca3cd2949a1a19d
ms.sourcegitcommit: 0cca2f82ae5c91c409e2abbf5867ff4e59ba71d6
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/23/2021
ms.locfileid: "5055935"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="91f4e-103">Projekti ajatabelite sisestamine</span><span class="sxs-lookup"><span data-stu-id="91f4e-103">Enter project timesheets</span></span>

<span data-ttu-id="91f4e-104">See protseduur laseb teil luua ajatabeli, kasutades tühja ajatabelivormi.</span><span class="sxs-lookup"><span data-stu-id="91f4e-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="91f4e-105">Uue ajatabeli alusena saab kasutada eelmise ajatabeli teavet või projekti ja tegevuse määramisi leheküljelt **My favorites** (Minu lemmikud).</span><span class="sxs-lookup"><span data-stu-id="91f4e-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the **My favorites** page.</span></span> <span data-ttu-id="91f4e-106">Vaikimisi kuvatakse loendilehel **All timesheets** (Kõik ajatabelid) kõik teie praeguse perioodi ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="91f4e-106">By default, the **All timesheets** list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="91f4e-107">Saate ripploendit kasutada välja **näitamiseks** lehel **My timesheets** (Minu ajatabelid), et filtreerida ajatabelite loendit ajaperioodi või projekti alusel või kuvada ajatabeleid, mis on loodud teiste töötajate nimel.</span><span class="sxs-lookup"><span data-stu-id="91f4e-107">You can use the drop-down list for the **Show** field in the **My timesheets** page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="91f4e-108">Selle protseduuri loomiseks kasutati demoettevõtte USSI andmeid.</span><span class="sxs-lookup"><span data-stu-id="91f4e-108">The demo data company used to create this procedure is USSI.</span></span>  

1. <span data-ttu-id="91f4e-109">Avage **Navigeerimispaneelil** **Moodulid > Projektijuhtimine ja raamatupidamine > Ajatabelid > Minu ajatabelid**.</span><span class="sxs-lookup"><span data-stu-id="91f4e-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Timesheets > My timesheets**.</span></span>
2. <span data-ttu-id="91f4e-110">Uue ajatabeli sisestamiseks klõpsake valikut **New** (Uus).</span><span class="sxs-lookup"><span data-stu-id="91f4e-110">To enter a new timesheet, click **New**.</span></span>
    - <span data-ttu-id="91f4e-111">Ripploendis Resource kuvatakse vaikimisi praegusele kasutajale määratud töötaja.</span><span class="sxs-lookup"><span data-stu-id="91f4e-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    - <span data-ttu-id="91f4e-112">Kui kasutaja on määratud delegaadina, kuvatakse nimed nii, et kasutaja saab nende nimel ajatabeli sisestada.</span><span class="sxs-lookup"><span data-stu-id="91f4e-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
3. <span data-ttu-id="91f4e-113">Väljale **Kuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="91f4e-113">In the **Date** field, enter a date.</span></span> <span data-ttu-id="91f4e-114">Kui see suvand on valitud, luuakse uue ajatabeli read lemmikuteks määratud ajatabeli sätteid kasutades.</span><span class="sxs-lookup"><span data-stu-id="91f4e-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
4. <span data-ttu-id="91f4e-115">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="91f4e-115">Click **OK**.</span></span>
5. <span data-ttu-id="91f4e-116">Klõpsake valikut **New line** (Uus rida).</span><span class="sxs-lookup"><span data-stu-id="91f4e-116">Click **New line**.</span></span>
6. <span data-ttu-id="91f4e-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="91f4e-117">In the list, mark the selected row.</span></span> <span data-ttu-id="91f4e-118">Väljal **Legal Entity** (Juriidiline isik) kuvatakse vaikimisi praegune juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="91f4e-118">The **Legal Entity** field displays the current Legal entity by default.</span></span>   
7. <span data-ttu-id="91f4e-119">Klõpsake väljal **Project** (Projekt) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="91f4e-119">In the **Project** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="91f4e-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="91f4e-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="91f4e-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="91f4e-121">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="91f4e-122">Klõpsake väljal **Tegevuse number** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="91f4e-122">In the **Activity number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="91f4e-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="91f4e-123">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="91f4e-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="91f4e-124">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="91f4e-125">Klõpsake väljal **Category** (Kategooria) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="91f4e-125">In the **Category** field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="91f4e-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="91f4e-126">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="91f4e-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="91f4e-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="91f4e-128">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="91f4e-128">Enter the number of hours worked each day.</span></span> <span data-ttu-id="91f4e-129">Sisestage tunnid kümnendarvuna.</span><span class="sxs-lookup"><span data-stu-id="91f4e-129">Enter the hours in decimal format.</span></span> <span data-ttu-id="91f4e-130">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="91f4e-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="91f4e-131">**Rea üksikasjade** all on saadaval järgmised valikud:</span><span class="sxs-lookup"><span data-stu-id="91f4e-131">In **Line details**, the following options are available:</span></span>
    - <span data-ttu-id="91f4e-132">Maksude ja finantsdimensioonide teavet saab lisada vahekaartidelt **Üldine** ja **Finantsdimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="91f4e-132">Add information about taxes and financial dimensions in the **General** and the **Financial Dimensions** tab.</span></span>
    - <span data-ttu-id="91f4e-133">Kommenteerige vahekaardi **Kommentaar** ajatabeli rida.</span><span class="sxs-lookup"><span data-stu-id="91f4e-133">Add comments about the timesheet line in the **Comment** tab.</span></span>
20. <span data-ttu-id="91f4e-134">Rippdialoogi avamiseks klõpsake paanil **Toimingupaan** valikut **Töövoog**.</span><span class="sxs-lookup"><span data-stu-id="91f4e-134">In the **Action pane**, click **Workflow** to open the drop dialog.</span></span>
21. <span data-ttu-id="91f4e-135">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="91f4e-135">Click **Submit**.</span></span>
22. <span data-ttu-id="91f4e-136">Klõpsake **Edasta**.</span><span class="sxs-lookup"><span data-stu-id="91f4e-136">Click **Submit**.</span></span>

