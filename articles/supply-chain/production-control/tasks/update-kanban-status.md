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
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1161e642f8b3b1cd0a2568e0745caa6db5fe5afb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980989"
---
# <a name="update-kanban-status"></a><span data-ttu-id="4b71f-103">Kanbani oleku uuendamine</span><span class="sxs-lookup"><span data-stu-id="4b71f-103">Update kanban status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b71f-104">Kui kanban on tühjendatud kogemata või vkui saadud kanban tuleb tühjendada, tuleb värskendada kanbani olekut.</span><span class="sxs-lookup"><span data-stu-id="4b71f-104">When a kanban is emptied by mistake or a received kanban needs to be emptied, you need to update kanban status.</span></span> <span data-ttu-id="4b71f-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="4b71f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4b71f-106">See protseduur on mõeldud tööde järelevaatajale.</span><span class="sxs-lookup"><span data-stu-id="4b71f-106">This procedure is intended for the shop supervisor.</span></span>


## <a name="find-the-kanban"></a><span data-ttu-id="4b71f-107">Otsige kanban üles.</span><span class="sxs-lookup"><span data-stu-id="4b71f-107">Find the kanban.</span></span>
1. <span data-ttu-id="4b71f-108">Avage Tootmise juhtimine > Kanban > Kanbanid.</span><span class="sxs-lookup"><span data-stu-id="4b71f-108">Go to Production control > Kanban > Kanbans.</span></span>
2. <span data-ttu-id="4b71f-109">Avage oleku veeru filter Töötlusühik</span><span class="sxs-lookup"><span data-stu-id="4b71f-109">Open Handling unit status column filter.</span></span>
3. <span data-ttu-id="4b71f-110">Klõpsake käsku Tühjenda.</span><span class="sxs-lookup"><span data-stu-id="4b71f-110">Click Clear.</span></span>
    * <span data-ttu-id="4b71f-111">See lähtestab filtrid.</span><span class="sxs-lookup"><span data-stu-id="4b71f-111">This resets the filters.</span></span>  
4. <span data-ttu-id="4b71f-112">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="4b71f-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="4b71f-113">Filtreerige näiteks välja Kaardi number väärtusega 000149.</span><span class="sxs-lookup"><span data-stu-id="4b71f-113">For example, filter on the Card number field with a value of '000149'.</span></span>

## <a name="change-emptied-status-to-received-status"></a><span data-ttu-id="4b71f-114">Tühjendatud oleku muutmine saadud olekuks</span><span class="sxs-lookup"><span data-stu-id="4b71f-114">Change emptied status to received status</span></span>
1. <span data-ttu-id="4b71f-115">Klõpsake suvandit Tühja materjali käsitsemisühiku pööramine</span><span class="sxs-lookup"><span data-stu-id="4b71f-115">Click Reverse empty handling unit.</span></span>
2. <span data-ttu-id="4b71f-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4b71f-116">Click OK.</span></span>
    * <span data-ttu-id="4b71f-117">Pange tähele, et suvandi Töötlusühik olek on Saadud.</span><span class="sxs-lookup"><span data-stu-id="4b71f-117">Notice that the Handling unit status is Received.</span></span>  

## <a name="change-received-status-to-emptied-status"></a><span data-ttu-id="4b71f-118">Saadud oleku muutmine tühjendatud olekuks</span><span class="sxs-lookup"><span data-stu-id="4b71f-118">Change received status to emptied status</span></span>
1. <span data-ttu-id="4b71f-119">Klõpsake suvandit Tühi kanban.</span><span class="sxs-lookup"><span data-stu-id="4b71f-119">Click Empty kanban.</span></span>
2. <span data-ttu-id="4b71f-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="4b71f-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4b71f-121">Pange tähele, et suvandi Töötlusühik olek on Tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="4b71f-121">Notice that the Handling unit status is Emptied.</span></span>  

