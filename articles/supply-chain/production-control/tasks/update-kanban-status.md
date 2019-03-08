---
title: Kanbani oleku uuendamine
description: Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d069414829518c8c952a0e7a74cd0ae4f24c450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "346268"
---
# <a name="update-kanban-status"></a><span data-ttu-id="9522d-103">Kanbani oleku uuendamine</span><span class="sxs-lookup"><span data-stu-id="9522d-103">Update kanban status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9522d-104">Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.</span><span class="sxs-lookup"><span data-stu-id="9522d-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="9522d-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="9522d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9522d-106">See protseduur on mõeldud tööde järelevaatajale.</span><span class="sxs-lookup"><span data-stu-id="9522d-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="9522d-107">Otsige kanban üles.</span><span class="sxs-lookup"><span data-stu-id="9522d-107">Find the kanban.</span></span>
1. <span data-ttu-id="9522d-108">Avage Tootmise juhtimine > Kanban > Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="9522d-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="9522d-109">Avage oleku veeru filter Töötlusühik</span><span class="sxs-lookup"><span data-stu-id="9522d-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="9522d-110">Klõpsake käsku Tühjenda.</span><span class="sxs-lookup"><span data-stu-id="9522d-110">Click Clear.</span></span>
    * <span data-ttu-id="9522d-111">See lähtestab filtrid.</span><span class="sxs-lookup"><span data-stu-id="9522d-111">This resets the filters.</span></span>  
4. <span data-ttu-id="9522d-112">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="9522d-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9522d-113">Filtreerige näiteks välja Kaardi number väärtusega 000149.</span><span class="sxs-lookup"><span data-stu-id="9522d-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="9522d-114">Tühjendatud oleku muutmine saadud olekuks</span><span class="sxs-lookup"><span data-stu-id="9522d-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="9522d-115">Klõpsake suvandit Tühja materjali käsitsemisühiku pööramine</span><span class="sxs-lookup"><span data-stu-id="9522d-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="9522d-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9522d-116">Click OK.</span></span>
    * <span data-ttu-id="9522d-117">Pange tähele, et suvandi Töötlusühik olek on Saadud.</span><span class="sxs-lookup"><span data-stu-id="9522d-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="9522d-118">Saadud oleku muutmine tühjendatud olekuks</span><span class="sxs-lookup"><span data-stu-id="9522d-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="9522d-119">Klõpsake suvandit Tühi kanban.</span><span class="sxs-lookup"><span data-stu-id="9522d-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="9522d-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9522d-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9522d-121">Pange tähele, et suvandi Töötlusühik olek on Tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="9522d-121">Notice that the Handling unit status is Emptied.</span></span>  

