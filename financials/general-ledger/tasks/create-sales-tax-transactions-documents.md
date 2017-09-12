--- 
title: "Käibemaksukannete loomine dokumentidel"
description: "Dokumentide käibemaks arvutatakse, luues dokumendi ridadel käibemaksugrupi ja kauba käibemaksugrupi."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 27bf4ba33bd7d22443512d072572b9b1ffc164fa
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="571f0-103">Käibemaksukannete loomine dokumentidel</span><span class="sxs-lookup"><span data-stu-id="571f0-103">Create sales tax transactions on documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="571f0-104">Dokumentide käibemaks arvutatakse, luues dokumendi ridadel käibemaksugrupi ja kauba käibemaksugrupi.</span><span class="sxs-lookup"><span data-stu-id="571f0-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="571f0-105">Need tulenevad vaikimisi koondandmetest, kuid neid saab vajaduse korral käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="571f0-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="571f0-106">Arvutatud käibemaksu saab kontrollida rea ja dokumendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="571f0-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="571f0-107">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="571f0-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="571f0-108">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="571f0-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="571f0-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="571f0-109">Click New.</span></span>
3. <span data-ttu-id="571f0-110">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="571f0-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="571f0-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="571f0-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="571f0-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="571f0-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="571f0-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="571f0-113">Click OK.</span></span>
7. <span data-ttu-id="571f0-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="571f0-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="571f0-115">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="571f0-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="571f0-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="571f0-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="571f0-117">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="571f0-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="571f0-118">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="571f0-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="571f0-119">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="571f0-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="571f0-120">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="571f0-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="571f0-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="571f0-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="571f0-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="571f0-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="571f0-123">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="571f0-123">Click Financials.</span></span>
17. <span data-ttu-id="571f0-124">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="571f0-124">Click Sales tax.</span></span>
18. <span data-ttu-id="571f0-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="571f0-125">Click OK.</span></span>
19. <span data-ttu-id="571f0-126">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="571f0-126">Click Add line.</span></span>
20. <span data-ttu-id="571f0-127">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="571f0-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="571f0-128">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="571f0-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="571f0-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="571f0-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="571f0-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="571f0-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="571f0-131">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="571f0-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="571f0-132">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="571f0-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="571f0-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="571f0-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="571f0-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="571f0-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="571f0-135">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="571f0-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="571f0-136">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="571f0-136">Click Sales tax.</span></span>
30. <span data-ttu-id="571f0-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="571f0-137">Click OK.</span></span>


