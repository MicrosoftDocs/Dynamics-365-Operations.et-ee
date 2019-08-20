---
title: Säästliku graafiku gruppide määratlemine
description: Säästliku graafiku grupid määratletakse toodete grupeerimiseks ja eristamiseks kanban-plaanimisel.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0cb17c68abbc4979a65e33c50450be575df3d93
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836260"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="b4977-103">Säästliku graafiku gruppide määratlemine</span><span class="sxs-lookup"><span data-stu-id="b4977-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4977-104">Säästliku graafiku grupid määratletakse toodete grupeerimiseks ja eristamiseks kanban-plaanimisel.</span><span class="sxs-lookup"><span data-stu-id="b4977-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="b4977-105">Grupeerimine võib toimuda üldise seosena ettevõtte kohta või tööraku põhiselt.</span><span class="sxs-lookup"><span data-stu-id="b4977-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="b4977-106">Igale grupile määratakse kanban-plaanimise loendilehel visuaalseks tähistamiseks värvikood.</span><span class="sxs-lookup"><span data-stu-id="b4977-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="b4977-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b4977-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="b4977-108">Säästliku plaanimise grupi määratlemine</span><span class="sxs-lookup"><span data-stu-id="b4977-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="b4977-109">Avage Tooteteabe haldus > Lean manufacturing > Säästliku graafiku grupid.</span><span class="sxs-lookup"><span data-stu-id="b4977-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="b4977-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b4977-110">Click New.</span></span>
3. <span data-ttu-id="b4977-111">Sisestage väärtus väljale Graafikugrupp.</span><span class="sxs-lookup"><span data-stu-id="b4977-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="b4977-112">Graafikugruppi saab määratleda üldise grupina või töörakupõhise grupina.</span><span class="sxs-lookup"><span data-stu-id="b4977-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="b4977-113">Selles lihtsas näites määratleme üldise grupi ja töörakk jääb tühjaks.</span><span class="sxs-lookup"><span data-stu-id="b4977-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="b4977-114">Selle grupi sätted kehtivad kõigi töörakkude puhul, millel pole konkreetseid graafikugruppe.</span><span class="sxs-lookup"><span data-stu-id="b4977-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="b4977-115">Valige värvivalikust värv.</span><span class="sxs-lookup"><span data-stu-id="b4977-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="b4977-116">Värve kasutatakse tööde esiletõstmiseks kanban-graafiku loendilehel või kanban-protsessi tahvlil.</span><span class="sxs-lookup"><span data-stu-id="b4977-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="b4977-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b4977-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b4977-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b4977-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="b4977-119">Toote seostamine</span><span class="sxs-lookup"><span data-stu-id="b4977-119">Associate product</span></span>
1. <span data-ttu-id="b4977-120">Konkreetse toote seostamine</span><span class="sxs-lookup"><span data-stu-id="b4977-120">Associate a specific product</span></span>
    * <span data-ttu-id="b4977-121">Toodete seostamiseks säästliku graafiku gruppidega on kaks võimalust: kas konkreetse tootena (kauba seose tüüp = kaup) või kauba eraldamisvõtme osana (kauba seose tüüp = grupp).</span><span class="sxs-lookup"><span data-stu-id="b4977-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="b4977-122">Valige Kaup väljalt Kauba seose tüüp.</span><span class="sxs-lookup"><span data-stu-id="b4977-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="b4977-123">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b4977-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="b4977-124">Sisestage number väljale Läbilaskemäär.</span><span class="sxs-lookup"><span data-stu-id="b4977-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="b4977-125">Läbilaskemäär on vaikimisi 1, mis tähendab, et seotud tooted tarbivad täpselt nii palju võimsust, kui on määratud tootmisvoogude protsessitoimingutes.</span><span class="sxs-lookup"><span data-stu-id="b4977-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="b4977-126">Läbilaskemäär >1 määratleb suurema ressursitarbimise, Läbilaskemäär <1 määratleb väiksema ressursitarbimise.</span><span class="sxs-lookup"><span data-stu-id="b4977-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="b4977-127">Suhtarvu kasutatakse kuluarvestuses ja kanban-töö tarbimise arvestuses.</span><span class="sxs-lookup"><span data-stu-id="b4977-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="b4977-128">Kauba eraldamisvõtme seostamine</span><span class="sxs-lookup"><span data-stu-id="b4977-128">Associate item allocation key</span></span>
1. <span data-ttu-id="b4977-129">Kauba eraldamisvõtme seostamine</span><span class="sxs-lookup"><span data-stu-id="b4977-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="b4977-130">Lisage kauba eraldamisvõtmele seos, kasutades kauba seose tüübi gruppi.</span><span class="sxs-lookup"><span data-stu-id="b4977-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="b4977-131">Pange tähele, et selle protsessi puhul on vaja teie andmetes määratletud eelarvekauba eraldamisvõtit.</span><span class="sxs-lookup"><span data-stu-id="b4977-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="b4977-132">Valige Grupp väljalt Kauba seose tüüp.</span><span class="sxs-lookup"><span data-stu-id="b4977-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="b4977-133">Klõpsake väljal Kauba eraldamisvõti otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b4977-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b4977-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b4977-134">In the list, click the link in the selected row.</span></span>

