---
title: Täpsemate reeglite loomine töölehtede jaoks
description: See protseduur hõlmab töölehtedele täpsemate reeglite loomise etappe.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3fc764a6fa92a050084ae610a11acac46995d2a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1553103"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="c13a9-103">Täpsemate reeglite loomine töölehtede jaoks</span><span class="sxs-lookup"><span data-stu-id="c13a9-103">Create advanced rules for journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c13a9-104">See protseduur hõlmab töölehtedele täpsemate reeglite loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="c13a9-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="c13a9-105">Muu hulgas hõlmab see töölehe juhtimise ja kasutaja sisestamispiirangute seadistamist.</span><span class="sxs-lookup"><span data-stu-id="c13a9-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="c13a9-106">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="c13a9-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="c13a9-107">Töölehe juhtimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="c13a9-107">Set up journal control</span></span>
1. <span data-ttu-id="c13a9-108">Minge jaotisesse Pearaamat > Töölehe seadistamine > Töölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="c13a9-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="c13a9-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c13a9-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c13a9-110">Klõpsake suvandit Töölehe juhtimine.</span><span class="sxs-lookup"><span data-stu-id="c13a9-110">Click Journal control.</span></span>
4. <span data-ttu-id="c13a9-111">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c13a9-111">Click Add.</span></span>
5. <span data-ttu-id="c13a9-112">Klõpsake väljal Ettevõtte kontod otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c13a9-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="c13a9-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c13a9-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="c13a9-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c13a9-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="c13a9-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c13a9-115">Click Add.</span></span>
9. <span data-ttu-id="c13a9-116">Klõpsake väljal Konto struktuur otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c13a9-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c13a9-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c13a9-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c13a9-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c13a9-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c13a9-119">Klõpsake väljal Segment otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c13a9-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="c13a9-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c13a9-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c13a9-121">Klõpsake väljal Alates väärtusest otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c13a9-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="c13a9-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c13a9-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="c13a9-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c13a9-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="c13a9-124">Klõpsake väljal Kuni väärtuseni otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c13a9-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="c13a9-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c13a9-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="c13a9-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c13a9-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="c13a9-127">Sisestuspiirangute seadistamine</span><span class="sxs-lookup"><span data-stu-id="c13a9-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="c13a9-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c13a9-128">Close the page.</span></span>
2. <span data-ttu-id="c13a9-129">Klõpsake suvandit Sisestamispiirangud.</span><span class="sxs-lookup"><span data-stu-id="c13a9-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="c13a9-130">Valige jaotises Kuidas soovite seadistada sisestamispiiranguid? suvand Kasutajagrupi järgi.</span><span class="sxs-lookup"><span data-stu-id="c13a9-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="c13a9-131">Märkige puul ruut „grupp, millel lubate selle töölehe nime puhul sisestamist”.</span><span class="sxs-lookup"><span data-stu-id="c13a9-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="c13a9-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="c13a9-132">Click OK.</span></span>

