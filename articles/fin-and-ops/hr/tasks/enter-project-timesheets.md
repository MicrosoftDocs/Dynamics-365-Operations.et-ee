---
title: Projekti ajatabelite sisestamine
description: See protseduur laseb teil luua ajatabeli, kasutades tühja ajatabelivormi.
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1510378"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="bccac-103">Projekti ajatabelite sisestamine</span><span class="sxs-lookup"><span data-stu-id="bccac-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bccac-104">See protseduur laseb teil luua ajatabeli, kasutades tühja ajatabelivormi.</span><span class="sxs-lookup"><span data-stu-id="bccac-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="bccac-105">Uue ajatabeli alusena saab kasutada eelmise ajatabeli teavet või projekti ja tegevuse määramisi leheküjelt My favorites (Minu lemmikud).</span><span class="sxs-lookup"><span data-stu-id="bccac-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="bccac-106">Vaikimisi kuvatakse loendilehel All timesheets (Kõik ajatabelid) kõik teie praeguse perioodi ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="bccac-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="bccac-107">Saate ripploendit kasutada välja näitamiseks lehel My timesheets (Minu ajatabelid), et filtreerida ajatabelite loendit ajaperioodi või projekti alusel või kuvada ajatabeleid, mis on loodud teiste töötajate nimel.</span><span class="sxs-lookup"><span data-stu-id="bccac-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="bccac-108">Selle protseduuri loomiseks kasutati demoettevõtte USSI andmeid.</span><span class="sxs-lookup"><span data-stu-id="bccac-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="bccac-109">Selle toimingu alustamiseks avage Projekti haldamine ja raamatupidamine > Ajatabelid > Minu ajatabelid.</span><span class="sxs-lookup"><span data-stu-id="bccac-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="bccac-110">Uue ajatabeli sisestamiseks klõpsake valikut New (Uus).</span><span class="sxs-lookup"><span data-stu-id="bccac-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="bccac-111">Ripploendis Resource kuvatakse vaikimisi praegusele kasutajale määratud töötaja.</span><span class="sxs-lookup"><span data-stu-id="bccac-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="bccac-112">Kui kasutaja on määratud delegaadina, kuvatakse nimed nii, et kasutaja saab nende nimel ajatabeli sisestada.</span><span class="sxs-lookup"><span data-stu-id="bccac-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="bccac-113">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="bccac-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="bccac-114">Kui see suvand on valitud, luuakse uue ajatabeli read lemmikuteks määratud ajatabeli sätteid kasutades.</span><span class="sxs-lookup"><span data-stu-id="bccac-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="bccac-115">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bccac-115">Click OK.</span></span>
4. <span data-ttu-id="bccac-116">Klõpsake valikut New line (Uus rida).</span><span class="sxs-lookup"><span data-stu-id="bccac-116">Click New line.</span></span>
5. <span data-ttu-id="bccac-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bccac-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="bccac-118">Väljal Legal Entity (Juriidiline isik) kuvatakse vaikimisi praegune juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="bccac-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="bccac-119">Klõpsake väljal Project (Projekt) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bccac-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bccac-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bccac-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="bccac-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bccac-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bccac-122">Klõpsake väljal Tegevus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bccac-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="bccac-123">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bccac-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="bccac-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bccac-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="bccac-125">Klõpsake väljal Category (Kategooria) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bccac-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="bccac-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bccac-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="bccac-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bccac-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="bccac-128">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="bccac-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="bccac-129">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="bccac-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="bccac-130">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="bccac-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="bccac-131">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="bccac-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="bccac-132">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="bccac-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="bccac-133">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="bccac-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="bccac-134">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="bccac-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="bccac-135">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="bccac-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="bccac-136">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="bccac-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="bccac-137">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="bccac-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="bccac-138">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="bccac-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="bccac-139">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="bccac-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="bccac-140">Sisestage igal päeval töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="bccac-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="bccac-141">Tunnid tuleb sisestada kümnendvormingus.</span><span class="sxs-lookup"><span data-stu-id="bccac-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="bccac-142">Näiteks kui töötasite 2 tundi ja 15 minutit, sisestage 2,25.</span><span class="sxs-lookup"><span data-stu-id="bccac-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="bccac-143">Rea üksikasjade all on saadaval järgmised valikud: o Maksude ja finantsdimensioonide teabe lisamine.</span><span class="sxs-lookup"><span data-stu-id="bccac-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="bccac-144">o Ajatabeli rea kohta kommentaaride lisamine.</span><span class="sxs-lookup"><span data-stu-id="bccac-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="bccac-145">Klõpsake suvandit Töövoog rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="bccac-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="bccac-146">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="bccac-146">Click Submit.</span></span>
22. <span data-ttu-id="bccac-147">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="bccac-147">Click Submit.</span></span>

