---
title: Pearaamatu eraldamistöölehe töötlemine
description: Kasutage lehte Eraldamistaotluse töötlemine selleks, et luua eraldamistööleht, mille saab üle vaadata ja kinnitada enne pearaamatusse sisestamist või sisestada otse pearaamatusse.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 087bd4f203e8762447e823b19076b79296a390d6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846363"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="e9e58-103">Pearaamatu eraldamistöölehe töötlemine</span><span class="sxs-lookup"><span data-stu-id="e9e58-103">Process ledger allocation journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e9e58-104">Kasutage lehte Eraldamistaotluse töötlemine selleks, et luua eraldamistööleht, mille saab üle vaadata ja kinnitada enne pearaamatusse sisestamist või sisestada otse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="e9e58-104">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="e9e58-105">Eraldamistöölehe saate luua alles siis, kui on olemas vähemalt üks aktiivne töölehe eraldamisreegel.</span><span class="sxs-lookup"><span data-stu-id="e9e58-105">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="e9e58-106">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="e9e58-106">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e9e58-107">Tehke valik Pearaamat > Eraldamised > Protsessi eraldamise päring.</span><span class="sxs-lookup"><span data-stu-id="e9e58-107">Go to General ledger > Allocations > Process allocation request.</span></span>
2. <span data-ttu-id="e9e58-108">Klõpsake väljal Reegel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e9e58-108">In the Rule field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="e9e58-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e9e58-109">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="e9e58-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e9e58-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e9e58-111">Sisestage kuupäev väljale Kuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="e9e58-111">In the As of date field, enter a date.</span></span>
    * <span data-ttu-id="e9e58-112">Parameeter Kuupäevaga on väga tähtis, kui reegli andmeallikas on pearaamat.</span><span class="sxs-lookup"><span data-stu-id="e9e58-112">The As of Date is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="e9e58-113">See kuupäev määrab, millised pearaamatusaldod eraldamisse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="e9e58-113">This date controls which ledger balances to include for allocation.</span></span>     <span data-ttu-id="e9e58-114">Valige väljal Nullväärtus suvand Peata.</span><span class="sxs-lookup"><span data-stu-id="e9e58-114">In the Zero source field select Stop.</span></span> <span data-ttu-id="e9e58-115">See peatab eraldamisprotsessi ja kuvab teate, et valitud on nullkogus.</span><span class="sxs-lookup"><span data-stu-id="e9e58-115">This will  Stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  
6. <span data-ttu-id="e9e58-116">Valige väljal Soovituse valikud suvand Ainult soovitus</span><span class="sxs-lookup"><span data-stu-id="e9e58-116">In the Proposal options field, select 'Proposal only'.</span></span>
    * <span data-ttu-id="e9e58-117">Valige suvand Soovitus ainult eraldamistöölehel oleva tulemuse ülevaatamiseks ja soovi korral kinnitamiseks enne eraldamise sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="e9e58-117">Select Proposal only to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
7. <span data-ttu-id="e9e58-118">Sisestage kuupäev väljale Pearaamatu sisestamisekuupäev.</span><span class="sxs-lookup"><span data-stu-id="e9e58-118">In the GL posting date field, enter a date.</span></span>
8. <span data-ttu-id="e9e58-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e9e58-119">Click OK.</span></span>
9. <span data-ttu-id="e9e58-120">Tehke valik Pearaamat > Eraldamised > Eraldamise töölehed.</span><span class="sxs-lookup"><span data-stu-id="e9e58-120">Go to General ledger > Allocations > Allocation journals.</span></span>
10. <span data-ttu-id="e9e58-121">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="e9e58-121">Click Lines.</span></span>
11. <span data-ttu-id="e9e58-122">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="e9e58-122">Click Post.</span></span>
12. <span data-ttu-id="e9e58-123">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="e9e58-123">Click Post.</span></span>

