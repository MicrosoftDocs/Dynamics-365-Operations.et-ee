---
title: Täpsemate reeglite loomine töölehtede jaoks
description: See protseduur hõlmab töölehtedele täpsemate reeglite loomise etappe.
author: aprilolson
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalControl, CompanyLookup, LedgerJournalPostControl
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea6ca24d27bb5b00bbe31060ce2f7e40bf2fb335
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442442"
---
# <a name="create-advanced-rules-for-journals"></a><span data-ttu-id="efb95-103">Täpsemate reeglite loomine töölehtede jaoks</span><span class="sxs-lookup"><span data-stu-id="efb95-103">Create advanced rules for journals</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="efb95-104">See protseduur hõlmab töölehtedele täpsemate reeglite loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="efb95-104">This procedure steps through creating advanced rules for journals.</span></span> <span data-ttu-id="efb95-105">Muu hulgas hõlmab see töölehe juhtimise ja kasutaja sisestamispiirangute seadistamist.</span><span class="sxs-lookup"><span data-stu-id="efb95-105">This includes setting up journal control and user posting restrictions.</span></span> <span data-ttu-id="efb95-106">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="efb95-106">This procedure uses the USMF demo data company.</span></span>


## <a name="set-up-journal-control"></a><span data-ttu-id="efb95-107">Töölehe juhtimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="efb95-107">Set up journal control</span></span>
1. <span data-ttu-id="efb95-108">Paanil **Navigeerimispaan** avage **Moodulid > Pearaamat > Töölehe seadistus > Töölehe nimed**.</span><span class="sxs-lookup"><span data-stu-id="efb95-108">In the **Navigation pane**, go to **Modules > General ledger > Journal setup > Journal names**.</span></span>
2. <span data-ttu-id="efb95-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="efb95-109">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="efb95-110">Paanil **Toimingupaan** klõpsake **Töölehe juhtimine**.</span><span class="sxs-lookup"><span data-stu-id="efb95-110">On the **Action pane**, click **Journal control**.</span></span>
4. <span data-ttu-id="efb95-111">Kiirkaardil **Milliseid kontotüüpe saab sisestada** klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="efb95-111">In the **Which account types can be posted** fastTab, click **Add**.</span></span>
5. <span data-ttu-id="efb95-112">Väljal **Ettevõtte kontod** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="efb95-112">In the **Company accounts** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="efb95-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="efb95-113">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="efb95-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efb95-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="efb95-115">Kiirkaardil **Millised segmendi väärtused kehtivad sellele töölehele** klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="efb95-115">In the **Which segment values are valid for this journal** fastTab, click **Add**.</span></span>
9. <span data-ttu-id="efb95-116">Väljal **Konto struktuur** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="efb95-116">In the **Account structure** field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="efb95-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="efb95-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="efb95-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efb95-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="efb95-119">Väljal **Segment** klõpsake ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="efb95-119">In the **Segment** field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="efb95-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efb95-120">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="efb95-121">Väljal **Väärtusest** klõpsake ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="efb95-121">In the **From value** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="efb95-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="efb95-122">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="efb95-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efb95-123">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="efb95-124">Väljal **Väärtuseni** klõpsake ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="efb95-124">In the **To value** field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="efb95-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="efb95-125">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="efb95-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efb95-126">In the list, click the link in the selected row.</span></span>

## <a name="set-up-posting-restrictions"></a><span data-ttu-id="efb95-127">Sisestuspiirangute seadistamine</span><span class="sxs-lookup"><span data-stu-id="efb95-127">Set up posting restrictions</span></span>
1. <span data-ttu-id="efb95-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="efb95-128">Close the page.</span></span>
2. <span data-ttu-id="efb95-129">Klõpsake **Sisestamise piirangud**.</span><span class="sxs-lookup"><span data-stu-id="efb95-129">Click **Posting restrictions**.</span></span>
3. <span data-ttu-id="efb95-130">Väljal **Kuidas soovite seadistada sisestamispiiranguid** valige "Kasutajagrupi järgi".</span><span class="sxs-lookup"><span data-stu-id="efb95-130">In the **How do you want to set up posting restrictions** field, select 'By user group'.</span></span>
4. <span data-ttu-id="efb95-131">Märkige puul ruut „grupp, millel lubate selle töölehe nime puhul sisestamist”.</span><span class="sxs-lookup"><span data-stu-id="efb95-131">In the tree, check 'the group that you want to allow posting for this journal name.'.</span></span>
5. <span data-ttu-id="efb95-132">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="efb95-132">Click **OK**.</span></span>

