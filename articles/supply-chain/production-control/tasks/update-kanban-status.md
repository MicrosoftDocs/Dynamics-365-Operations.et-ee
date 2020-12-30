---
title: Kanbani oleku uuendamine
description: Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Kanban, KanbanResetEmpty
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb8559c0843d7e6e538b5b29dc394a50d05462ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426425"
---
# <a name="update-kanban-status"></a><span data-ttu-id="f2e9c-103">Kanbani oleku uuendamine</span><span class="sxs-lookup"><span data-stu-id="f2e9c-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2e9c-104">Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="f2e9c-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f2e9c-106">See protseduur on mõeldud tööde järelevaatajale.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="f2e9c-107">Otsige kanban üles.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-107">Find the kanban.</span></span>
1. <span data-ttu-id="f2e9c-108">Avage Tootmise juhtimine > Kanban > Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="f2e9c-109">Avage oleku veeru filter Töötlusühik</span><span class="sxs-lookup"><span data-stu-id="f2e9c-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="f2e9c-110">Klõpsake käsku Tühjenda.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-110">Click Clear.</span></span>
    * <span data-ttu-id="f2e9c-111">See lähtestab filtrid.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-111">This resets the filters.</span></span>  
4. <span data-ttu-id="f2e9c-112">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f2e9c-113">Filtreerige näiteks välja Kaardi number väärtusega 000149.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="f2e9c-114">Tühjendatud oleku muutmine saadud olekuks</span><span class="sxs-lookup"><span data-stu-id="f2e9c-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="f2e9c-115">Klõpsake suvandit Tühja materjali käsitsemisühiku pööramine</span><span class="sxs-lookup"><span data-stu-id="f2e9c-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="f2e9c-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-116">Click OK.</span></span>
    * <span data-ttu-id="f2e9c-117">Pange tähele, et suvandi Töötlusühik olek on Saadud.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="f2e9c-118">Saadud oleku muutmine tühjendatud olekuks</span><span class="sxs-lookup"><span data-stu-id="f2e9c-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="f2e9c-119">Klõpsake suvandit Tühi kanban.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="f2e9c-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f2e9c-121">Pange tähele, et suvandi Töötlusühik olek on Tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="f2e9c-121">Notice that the Handling unit status is Emptied.</span></span>  

