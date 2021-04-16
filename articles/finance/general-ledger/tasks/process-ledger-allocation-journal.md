---
title: Pearaamatu eraldamistöölehe töötlemine
description: Selles teemas selgitatakse eraldamise taotluse töötlemist rakenduses Dynamics 365 Finance.
author: aprilolson
ms.date: 07/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e89aa21f988d50bc1a922e053be0ff2dcd196268
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834408"
---
# <a name="process-ledger-allocation-journal"></a><span data-ttu-id="f6463-103">Pearaamatu eraldamistöölehe töötlemine</span><span class="sxs-lookup"><span data-stu-id="f6463-103">Process ledger allocation journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f6463-104">Selles teemas selgitatakse eraldamise taotluse töötlemist.</span><span class="sxs-lookup"><span data-stu-id="f6463-104">This topic explains how to process an allocation request.</span></span> <span data-ttu-id="f6463-105">Kasutage lehte Eraldamistaotluse töötlemine selleks, et luua eraldamistööleht, mille saab üle vaadata ja kinnitada enne pearaamatusse sisestamist või sisestada otse pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="f6463-105">Use the Process allocation request page to create an allocation journal that can be reviewed and approved before posting to General ledger, or posted directly to General ledger.</span></span> <span data-ttu-id="f6463-106">Eraldamistöölehe saate luua alles siis, kui on olemas vähemalt üks aktiivne töölehe eraldamisreegel.</span><span class="sxs-lookup"><span data-stu-id="f6463-106">Before you can create an allocations journal, there must be least one active Ledger allocation rule.</span></span> <span data-ttu-id="f6463-107">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="f6463-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="f6463-108">Navigeerimispaanil avage **Moodulid > Pearaamat > Eraldamised > Protsessi eraldamise taotlus**.</span><span class="sxs-lookup"><span data-stu-id="f6463-108">In the navigation pane, go to **Modules > General ledger > Allocations > Process allocation request**.</span></span>
2. <span data-ttu-id="f6463-109">Valige väljal **Reegel** ripploendist soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f6463-109">In the **Rule** field, select the desired record in the drop-down menu.</span></span>
3. <span data-ttu-id="f6463-110">Sisestage väljale **Kuupäevaga** kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f6463-110">In the **As of date** field, enter a date.</span></span>

    - <span data-ttu-id="f6463-111">**Kuupäevaga** on väga tähtis, kui reegli andmeallikas on pearaamat.</span><span class="sxs-lookup"><span data-stu-id="f6463-111">The **As of Date** is very important when the Ledger is the Data source for the rule.</span></span> <span data-ttu-id="f6463-112">See kuupäev määrab, millised pearaamatusaldod eraldamisse kaasatakse.</span><span class="sxs-lookup"><span data-stu-id="f6463-112">This date controls which ledger balances to include for allocation.</span></span>  
    - <span data-ttu-id="f6463-113">Valige väljal **Nullväärtus** suvand **Peata**.</span><span class="sxs-lookup"><span data-stu-id="f6463-113">In the **Zero source** field select **Stop**.</span></span> <span data-ttu-id="f6463-114">See peatab eraldamisprotsessi ja kuvab teate, et valitud on nullkogus.</span><span class="sxs-lookup"><span data-stu-id="f6463-114">This will stop the allocation process and display a message that states that a zero source amount is selected.</span></span>  

4. <span data-ttu-id="f6463-115">Valige väljal **Soovituse valikud** suvand **Ainult soovitus**.</span><span class="sxs-lookup"><span data-stu-id="f6463-115">In the **Proposal options** field, select **Proposal only**.</span></span> <span data-ttu-id="f6463-116">Valige suvand **Ainult soovitus** eraldamistöölehel oleva tulemuse ülevaatamiseks ja soovi korral kinnitamiseks enne eraldamise sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="f6463-116">Select **Proposal only** to review and optionally approve the result in Allocation journals prior to posting the allocation to General ledger.</span></span>  
5. <span data-ttu-id="f6463-117">Sisestage kuupäev väljale Pearaamatu sisestamisekuupäev.</span><span class="sxs-lookup"><span data-stu-id="f6463-117">In the GL posting date field, enter a date.</span></span>
6. <span data-ttu-id="f6463-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f6463-118">Select **OK**.</span></span>
7. <span data-ttu-id="f6463-119">Navigeerimispaanil avage **Moodulid > Pearaamat > Eraldamised > Eraldamise päevikud**.</span><span class="sxs-lookup"><span data-stu-id="f6463-119">In the navigation pane, go to **Modules > General ledger > Allocations > Allocation journals**.</span></span>
8. <span data-ttu-id="f6463-120">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="f6463-120">Select **Lines**.</span></span>
9. <span data-ttu-id="f6463-121">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="f6463-121">Select **Post**.</span></span>
10. <span data-ttu-id="f6463-122">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="f6463-122">Select **Post**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]