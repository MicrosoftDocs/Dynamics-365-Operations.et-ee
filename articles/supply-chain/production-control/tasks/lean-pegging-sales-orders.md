---
title: Säästlik sidumine müügitellimuste põhjal
description: Protseduur keskendub müügirea sidumispuu kinnitamisele, kui kaup on toodetud kanbanidega.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90032539d59b310cb2d4c1324312eac6593fba6b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843595"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="05a86-103">Säästlik sidumine müügitellimuste põhjal</span><span class="sxs-lookup"><span data-stu-id="05a86-103">Lean pegging from sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05a86-104">Protseduur keskendub müügirea sidumispuu kinnitamisele, kui kaup on toodetud kanbanidega.</span><span class="sxs-lookup"><span data-stu-id="05a86-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="05a86-105">Pärast sidumispuu kinnitamist on kõik kanban-tööd plaanitud.</span><span class="sxs-lookup"><span data-stu-id="05a86-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="05a86-106">See on kasulik tellimuste puhul, kus tellimuse vastuvõtja peab tagama, et tootmine saaks kohe alata.</span><span class="sxs-lookup"><span data-stu-id="05a86-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="05a86-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="05a86-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="05a86-108">Protseduur on mõeldud spetsialiseerunud tellimuste vastuvõtjale, kes töötab säästlikus ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="05a86-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="05a86-109">Kanbani juhitud kauba jaoks müügitellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="05a86-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="05a86-110">Avage Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="05a86-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="05a86-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="05a86-111">Click New.</span></span>
3. <span data-ttu-id="05a86-112">Valige või sisestage väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="05a86-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="05a86-113">Kasutage US-001.</span><span class="sxs-lookup"><span data-stu-id="05a86-113">Use US-001.</span></span>  
4. <span data-ttu-id="05a86-114">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="05a86-114">Click OK.</span></span>
5. <span data-ttu-id="05a86-115">Sisestage väljale Kaubakood tüüp L0001.</span><span class="sxs-lookup"><span data-stu-id="05a86-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="05a86-116">Määrake koguse väärtuseks 30.</span><span class="sxs-lookup"><span data-stu-id="05a86-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="05a86-117">Sündmuse kanban-reegli käivitamiseks peab kogus kindlasti olema suurem kui 24.</span><span class="sxs-lookup"><span data-stu-id="05a86-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="05a86-118">Sidumispuu avamine</span><span class="sxs-lookup"><span data-stu-id="05a86-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="05a86-119">Klõpsake valikut Toode ja tarnimine.</span><span class="sxs-lookup"><span data-stu-id="05a86-119">Click Product and supply.</span></span>
2. <span data-ttu-id="05a86-120">Klõpsake suvandit Kuva sidumispuu.</span><span class="sxs-lookup"><span data-stu-id="05a86-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="05a86-121">Pange tähele, et sidumispuus on kuvatud kõik müügitellimuse rea jaoks vajalikud sidumistasemed.</span><span class="sxs-lookup"><span data-stu-id="05a86-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="05a86-122">Selles näites on kaks kanbanide taset ja kõik nõutavad komponendid.</span><span class="sxs-lookup"><span data-stu-id="05a86-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="05a86-123">Sidumispuu plaanimine</span><span class="sxs-lookup"><span data-stu-id="05a86-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="05a86-124">Valige puus „Sales line 000832\Kanban 000558”.</span><span class="sxs-lookup"><span data-stu-id="05a86-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="05a86-125">Laiendage jaotist Kanban-tööd.</span><span class="sxs-lookup"><span data-stu-id="05a86-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="05a86-126">Pange tähele, et kanban-töö olek on Plaanimata.</span><span class="sxs-lookup"><span data-stu-id="05a86-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="05a86-127">Klõpsake käsku Plaani kogu sidumispuu.</span><span class="sxs-lookup"><span data-stu-id="05a86-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="05a86-128">See plaanib kõik sidumispuus olevad kanban-tööd, asendades töö oleku Plaanimata olekuga Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="05a86-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="05a86-129">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="05a86-129">Refresh the page.</span></span>
    * <span data-ttu-id="05a86-130">Pange tähele, et kanban-töö olek Plaanimata asendati olekuga Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="05a86-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="05a86-131">Valige puus suvand „Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559”.</span><span class="sxs-lookup"><span data-stu-id="05a86-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="05a86-132">Teise kanbani töö on samuti plaanitud, kuna kogu sidumispuu on plaanitud.</span><span class="sxs-lookup"><span data-stu-id="05a86-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="05a86-133">Pange tähele, et kanban-töö olek Plaanimata asendatakse olekuga Plaanitud.</span><span class="sxs-lookup"><span data-stu-id="05a86-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  

