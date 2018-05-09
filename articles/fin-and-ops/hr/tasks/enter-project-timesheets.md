--- 
title: Projekti ajatabelite sisestamine
description: "See protseduur laseb teil luua ajatabeli, kasutades tühja ajatabelivormi."
author: kherr75
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: b1ccaeffde4c288667fe797d07e08b5a346b4716
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="enter-project-timesheets"></a><span data-ttu-id="5d332-103">Projekti ajatabelite sisestamine</span><span class="sxs-lookup"><span data-stu-id="5d332-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5d332-104">See protseduur laseb teil luua ajatabeli, kasutades tühja ajatabelivormi.</span><span class="sxs-lookup"><span data-stu-id="5d332-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="5d332-105">Uue ajatabeli alusena saab kasutada eelmise ajatabeli teavet või projekti ja tegevuse määramisi leheküjelt My favorites (Minu lemmikud).</span><span class="sxs-lookup"><span data-stu-id="5d332-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="5d332-106">Vaikimisi kuvatakse loendilehel All timesheets (Kõik ajatabelid) kõik teie praeguse perioodi ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="5d332-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="5d332-107">Saate ripploendit kasutada välja näitamiseks lehel My timesheets (Minu ajatabelid), et filtreerida ajatabelite loendit ajaperioodi või projekti alusel või kuvada ajatabeleid, mis on loodud teiste töötajate nimel.</span><span class="sxs-lookup"><span data-stu-id="5d332-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="5d332-108">Selle protseduuri loomiseks kasutati demoettevõtte USSI andmeid.</span><span class="sxs-lookup"><span data-stu-id="5d332-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="5d332-109">Selle toimingu alustamiseks avage Projekti haldamine ja raamatupidamine > Ajatabelid > Minu ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="5d332-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="5d332-110">Uue ajatabeli sisestamiseks klõpsake valikut New (Uus).</span><span class="sxs-lookup"><span data-stu-id="5d332-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="5d332-111">Ripploendis Resource kuvatakse vaikimisi praegusele kasutajale määratud töötaja.</span><span class="sxs-lookup"><span data-stu-id="5d332-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="5d332-112">Kui kasutaja on määratud delegaadina, kuvatakse nimed nii, et kasutaja saab nende nimel ajatabeli sisestada.</span><span class="sxs-lookup"><span data-stu-id="5d332-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="5d332-113">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="5d332-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="5d332-114">Kui see suvand on valitud, luuakse uue ajatabeli read lemmikuteks määratud ajatabeli sätteid kasutades.</span><span class="sxs-lookup"><span data-stu-id="5d332-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="5d332-115">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="5d332-115">Click OK.</span></span>
4. <span data-ttu-id="5d332-116">Klõpsake valikut New line (Uus rida).</span><span class="sxs-lookup"><span data-stu-id="5d332-116">Click New line.</span></span>
5. <span data-ttu-id="5d332-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="5d332-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="5d332-118">Väljal Legal Entity (Juriidiline isik) kuvatakse vaikimisi praegune juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="5d332-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="5d332-119">Klõpsake väljal Project (Projekt) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5d332-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="5d332-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5d332-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="5d332-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5d332-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5d332-122">Klõpsake väljal Tegevus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5d332-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="5d332-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5d332-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="5d332-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5d332-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="5d332-125">Klõpsake väljal Category (Kategooria) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="5d332-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="5d332-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5d332-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="5d332-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="5d332-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="5d332-128">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="5d332-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="5d332-129">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="5d332-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="5d332-130">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="5d332-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="5d332-131">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="5d332-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="5d332-132">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="5d332-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="5d332-133">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="5d332-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="5d332-134">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="5d332-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="5d332-135">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="5d332-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="5d332-136">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="5d332-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="5d332-137">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="5d332-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="5d332-138">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="5d332-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="5d332-139">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="5d332-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="5d332-140">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="5d332-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="5d332-141">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="5d332-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="5d332-142">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="5d332-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="5d332-143">Rea üksikasjade all on saadaval järgmised valikud: o Maksude ja finantsdimensioonide teabe lisamine.</span><span class="sxs-lookup"><span data-stu-id="5d332-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="5d332-144">o Ajatabeli rea kohta kommentaaride lisamine.</span><span class="sxs-lookup"><span data-stu-id="5d332-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="5d332-145">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5d332-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="5d332-146">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="5d332-146">Click Submit.</span></span>
22. <span data-ttu-id="5d332-147">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="5d332-147">Click Submit.</span></span>


