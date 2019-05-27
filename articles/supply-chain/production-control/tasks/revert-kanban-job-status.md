---
title: Kanban-töö oleku taastamine
description: Protseduur keskendub vale kanban-töö oleku ennistamisele.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27874f89cede151b52b869fa0d58e320d548e6d3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562203"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="3cdfd-103">Kanban-töö oleku taastamine</span><span class="sxs-lookup"><span data-stu-id="3cdfd-103">Revert kanban job status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3cdfd-104">Protseduur keskendub vale kanban-töö oleku ennistamisele.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="3cdfd-105">See on kasulik juhul, kui masinaoperaator uuendab vale tööd või määrab kogemata vale oleku.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="3cdfd-106">Selles protseduuris on kanban-töö kogemata registreeritud olekuga Ettevalmistatud, mistõttu olek ennistatakse.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="3cdfd-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3cdfd-108">Protseduur on mõeldud tööde järelevaatajale või masinaoperaatorile, kes töötavad lean manufacturingil põhinevas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="3cdfd-109">Avage tööraku protsessitahvel</span><span class="sxs-lookup"><span data-stu-id="3cdfd-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="3cdfd-110">Avage Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="3cdfd-111">Valige või sisestage väärtus väljal Töörakk.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="3cdfd-112">Valige töörakk 1260.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="3cdfd-113">Kanban-töö ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="3cdfd-113">Prepare kanban job</span></span>
1. <span data-ttu-id="3cdfd-114">Klõpsake suvandit Valmista ette.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-114">Click Prepare.</span></span>
    * <span data-ttu-id="3cdfd-115">Kui te ei saa klõpsata suvandit Ettevalmistamine, kuna see on tuhm, kontrollige, kas valitud kanban-töö olek on plaanitud, mida näitab tühja kanbani ikoon.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="3cdfd-116">Kui ettevalmistamine nurjub, veenduge, et kõik komplekteerimislehel olevad materjalid oleksid saadaval.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="3cdfd-117">Valige loendis ettevalmistatud töö.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="3cdfd-118">Valige esimene töö, mille äsja ette valmistasite.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="3cdfd-119">Pange tähele, et töö olek on Ettevalmistatud, mida tähistab kanbani ikoonil olev kolmnurk.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="3cdfd-120">Ettevalmistatud kanban-töö oleku ennistamine</span><span class="sxs-lookup"><span data-stu-id="3cdfd-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="3cdfd-121">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3cdfd-122">Valige esimene töö, mille ette valmistasite.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="3cdfd-123">Klõpsake toimingupaanil suvandit Tootmine.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="3cdfd-124">Klõpsake suvandit Oleku ennistamine.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-124">Click Revert status.</span></span>
    * <span data-ttu-id="3cdfd-125">Saate kasutada alternatiivset kanban-reeglit, kui on täidetud järgmised tingimused. - Täiendusstrateegia on mõlema reegli jaoks sama.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="3cdfd-126">- Tootmisvoo versioon on mõlema reegli jaoks sama.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="3cdfd-127">- Tarnitav toode on mõlema reegli jaoks sama.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="3cdfd-128">- Kõik kanban-reeglite viimase tegevuse jaoks konfigureeritavad järgnevad tegevused peavad mõlema reegli jaoks olema samad.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="3cdfd-129">- Mõlema reegli jaoks peavad olema konfigureeritud samad tarnitud varude dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="3cdfd-130">- Materjali käsitlemisühiku olek peab olema Määramata.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="3cdfd-131">- Sündmuse kanbanide konfiguratsioon peab olema sama.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="3cdfd-132">Kontrollige, kas uus olek on Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="3cdfd-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-133">Click OK.</span></span>
5. <span data-ttu-id="3cdfd-134">Eemaldage loendis valitud realt märge.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="3cdfd-135">Valige sama töö.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-135">Select the same job.</span></span>  
    * <span data-ttu-id="3cdfd-136">Pange tähele, et ennistatakse kanban-töö olek Plaanitud, mida tähistab kanbani tühi ikoon.</span><span class="sxs-lookup"><span data-stu-id="3cdfd-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  

