--- 
title: "Täpsemate reeglite loomine töölehtede jaoks"
description: "See protseduur hõlmab töölehtedele täpsemate reeglite loomise etappe."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 36f4edd6fa9711022e291ea5ceffbcc9ef55b2a9
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="6804f-103">Täpsemate reeglite loomine töölehtede jaoks</span><span class="sxs-lookup"><span data-stu-id="6804f-103">Create advanced rules for journals</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6804f-104">See protseduur hõlmab töölehtedele täpsemate reeglite loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="6804f-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="6804f-105">Muu hulgas hõlmab see töölehe juhtimise ja kasutaja sisestamispiirangute seadistamist.</span><span class="sxs-lookup"><span data-stu-id="6804f-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="6804f-106">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="6804f-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="6804f-107">Töölehe juhtimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="6804f-107">Set up journal control</span></span>
1. <span data-ttu-id="6804f-108">Minge jaotisesse Pearaamat > Töölehe seadistamine > Töölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="6804f-108">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="6804f-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6804f-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="6804f-110">Klõpsake suvandit Töölehe juhtimine.</span><span class="sxs-lookup"><span data-stu-id="6804f-110">Click Journal control.</span></span>
4. <span data-ttu-id="6804f-111">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6804f-111">Click Add.</span></span>
5. <span data-ttu-id="6804f-112">Klõpsake väljal Ettevõtte kontod otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6804f-112">In the Company accounts field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="6804f-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6804f-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6804f-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6804f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="6804f-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6804f-115">Click Add.</span></span>
9. <span data-ttu-id="6804f-116">Klõpsake väljal Konto struktuur otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6804f-116">In the Account structure field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="6804f-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6804f-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="6804f-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6804f-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="6804f-119">Klõpsake väljal Segment otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6804f-119">In the Segment field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="6804f-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6804f-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="6804f-121">Klõpsake väljal Alates väärtusest otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6804f-121">In the From value field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="6804f-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6804f-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="6804f-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6804f-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="6804f-124">Klõpsake väljal Kuni väärtuseni otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="6804f-124">In the To value field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="6804f-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6804f-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="6804f-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6804f-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="6804f-127">Sisestuspiirangute seadistamine</span><span class="sxs-lookup"><span data-stu-id="6804f-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="6804f-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6804f-128">Close the page.</span></span>
2. <span data-ttu-id="6804f-129">Klõpsake suvandit Sisestamispiirangud.</span><span class="sxs-lookup"><span data-stu-id="6804f-129">Click Posting restrictions.</span></span>
3. <span data-ttu-id="6804f-130">Valige jaotises Kuidas soovite seadistada sisestamispiiranguid? suvand Kasutajagrupi järgi.</span><span class="sxs-lookup"><span data-stu-id="6804f-130">In the How do you want to set up posting restrictions, select By user group.</span></span>
4. <span data-ttu-id="6804f-131">Märkige puul ruut „grupp, millel lubate selle töölehe nime puhul sisestamist”.</span><span class="sxs-lookup"><span data-stu-id="6804f-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="6804f-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6804f-132">Click OK.</span></span>


