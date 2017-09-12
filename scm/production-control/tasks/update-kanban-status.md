--- 
title: Kanbani oleku uuendamine
description: "Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 3c2b5a5fbfc5bd83cc68ffafaa243dac9244c003
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="update-kanban-status"></a><span data-ttu-id="d8983-103">Kanbani oleku uuendamine</span><span class="sxs-lookup"><span data-stu-id="d8983-103">Update kanban status</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8983-104">Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.</span><span class="sxs-lookup"><span data-stu-id="d8983-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="d8983-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d8983-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d8983-106">See protseduur on mõeldud tööde järelevaatajale.</span><span class="sxs-lookup"><span data-stu-id="d8983-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="d8983-107">Otsige kanban üles.</span><span class="sxs-lookup"><span data-stu-id="d8983-107">Find the kanban.</span></span>
1. <span data-ttu-id="d8983-108">Avage Tootmise juhtimine > Kanban > Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="d8983-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="d8983-109">Avage oleku veeru filter Töötlusühik</span><span class="sxs-lookup"><span data-stu-id="d8983-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="d8983-110">Klõpsake käsku Tühjenda.</span><span class="sxs-lookup"><span data-stu-id="d8983-110">Click Clear.</span></span>
    * <span data-ttu-id="d8983-111">See lähtestab filtrid.</span><span class="sxs-lookup"><span data-stu-id="d8983-111">This resets the filters.</span></span>  
4. <span data-ttu-id="d8983-112">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="d8983-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d8983-113">Filtreerige näiteks välja Kaardi number väärtusega 000149.</span><span class="sxs-lookup"><span data-stu-id="d8983-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="d8983-114">Tühjendatud oleku muutmine saadud olekuks</span><span class="sxs-lookup"><span data-stu-id="d8983-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="d8983-115">Klõpsake suvandit Tühja materjali käsitsemisühiku pööramine</span><span class="sxs-lookup"><span data-stu-id="d8983-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="d8983-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d8983-116">Click OK.</span></span>
    * <span data-ttu-id="d8983-117">Pange tähele, et suvandi Töötlusühik olek on Saadud.</span><span class="sxs-lookup"><span data-stu-id="d8983-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="d8983-118">Saadud oleku muutmine tühjendatud olekuks</span><span class="sxs-lookup"><span data-stu-id="d8983-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="d8983-119">Klõpsake suvandit Tühi kanban.</span><span class="sxs-lookup"><span data-stu-id="d8983-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="d8983-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d8983-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="d8983-121">Pange tähele, et suvandi Töötlusühik olek on Tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="d8983-121">Notice that the Handling unit status is Emptied.</span></span>  


