--- 
title: "Kanban-töö oleku taastamine"
description: "Protseduur keskendub vale kanban-töö oleku ennistamisele."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 2bcc83c0a422ed1480f2ed41460fd710bc51ff3d
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="7b429-103">Kanban-töö oleku taastamine</span><span class="sxs-lookup"><span data-stu-id="7b429-103">Revert kanban job status</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b429-104">Protseduur keskendub vale kanban-töö oleku ennistamisele.</span><span class="sxs-lookup"><span data-stu-id="7b429-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="7b429-105">See on kasulik juhul, kui masinaoperaator uuendab vale tööd või määrab kogemata vale oleku.</span><span class="sxs-lookup"><span data-stu-id="7b429-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="7b429-106">Selles protseduuris on kanban-töö kogemata registreeritud olekuga Ettevalmistatud, mistõttu olek ennistatakse.</span><span class="sxs-lookup"><span data-stu-id="7b429-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="7b429-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="7b429-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="7b429-108">Protseduur on mõeldud tööde järelevaatajale või masinaoperaatorile, kes töötavad lean manufacturingil põhinevas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="7b429-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="7b429-109">Avage tööraku protsessitahvel</span><span class="sxs-lookup"><span data-stu-id="7b429-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="7b429-110">Avage Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="7b429-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="7b429-111">Valige või sisestage väärtus väljal Töörakk.</span><span class="sxs-lookup"><span data-stu-id="7b429-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="7b429-112">Valige töörakk 1260.</span><span class="sxs-lookup"><span data-stu-id="7b429-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="7b429-113">Kanban-töö ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="7b429-113">Prepare kanban job</span></span>
1. <span data-ttu-id="7b429-114">Klõpsake suvandit Valmista ette.</span><span class="sxs-lookup"><span data-stu-id="7b429-114">Click Prepare.</span></span>
    * <span data-ttu-id="7b429-115">Kui te ei saa klõpsata suvandit Ettevalmistamine, kuna see on tuhm, kontrollige, kas valitud kanban-töö olek on plaanitud, mida näitab tühja kanbani ikoon.</span><span class="sxs-lookup"><span data-stu-id="7b429-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="7b429-116">Kui ettevalmistamine nurjub, veenduge, et kõik komplekteerimislehel olevad materjalid oleksid saadaval.</span><span class="sxs-lookup"><span data-stu-id="7b429-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="7b429-117">Valige loendis ettevalmistatud töö.</span><span class="sxs-lookup"><span data-stu-id="7b429-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="7b429-118">Valige esimene töö, mille äsja ette valmistasite.</span><span class="sxs-lookup"><span data-stu-id="7b429-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="7b429-119">Pange tähele, et töö olek on Ettevalmistatud, mida tähistab kanbani ikoonil olev kolmnurk.</span><span class="sxs-lookup"><span data-stu-id="7b429-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="7b429-120">Ettevalmistatud kanban-töö oleku ennistamine</span><span class="sxs-lookup"><span data-stu-id="7b429-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="7b429-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7b429-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7b429-122">Valige esimene töö, mille ette valmistasite.</span><span class="sxs-lookup"><span data-stu-id="7b429-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="7b429-123">Klõpsake toimingupaanil suvandit Tootmine.</span><span class="sxs-lookup"><span data-stu-id="7b429-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="7b429-124">Klõpsake suvandit Oleku ennistamine.</span><span class="sxs-lookup"><span data-stu-id="7b429-124">Click Revert status.</span></span>
    * <span data-ttu-id="7b429-125">Saate kasutada alternatiivset kanban-reeglit, kui on täidetud järgmised tingimused. - Täiendusstrateegia on mõlema reegli jaoks sama.</span><span class="sxs-lookup"><span data-stu-id="7b429-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="7b429-126">- Tootmisvoo versioon on mõlema reegli jaoks sama.</span><span class="sxs-lookup"><span data-stu-id="7b429-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="7b429-127">- Tarnitav toode on mõlema reegli jaoks sama.</span><span class="sxs-lookup"><span data-stu-id="7b429-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="7b429-128">- Kõik kanban-reeglite viimase tegevuse jaoks konfigureeritavad järgnevad tegevused peavad mõlema reegli jaoks olema samad.</span><span class="sxs-lookup"><span data-stu-id="7b429-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="7b429-129">- Mõlema reegli jaoks peavad olema konfigureeritud samad tarnitud varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="7b429-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="7b429-130">- Materjali käsitlemisühiku olek peab olema Määramata.</span><span class="sxs-lookup"><span data-stu-id="7b429-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="7b429-131">- Sündmuse kanbanide konfiguratsioon peab olema sama.</span><span class="sxs-lookup"><span data-stu-id="7b429-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="7b429-132">Kontrollige, kas uus olek on Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="7b429-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="7b429-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7b429-133">Click OK.</span></span>
5. <span data-ttu-id="7b429-134">Eemaldage loendis valitud realt märge.</span><span class="sxs-lookup"><span data-stu-id="7b429-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="7b429-135">Valige sama töö.</span><span class="sxs-lookup"><span data-stu-id="7b429-135">Select the same job.</span></span>  
    * <span data-ttu-id="7b429-136">Pange tähele, et ennistatakse kanban-töö olek Plaanitud, mida tähistab kanbani tühi ikoon.</span><span class="sxs-lookup"><span data-stu-id="7b429-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  


