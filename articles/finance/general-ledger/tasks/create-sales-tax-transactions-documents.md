---
title: Käibemaksukannete loomine dokumentidel
description: Dokumentide käibemaks arvutatakse, luues dokumendi ridadel käibemaksugrupi ja kauba käibemaksugrupi.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 653b93744f5b891655cade0cb669d34179fca9cd
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186137"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="7c4cd-103">Käibemaksukannete loomine dokumentidel</span><span class="sxs-lookup"><span data-stu-id="7c4cd-103">Create sales tax transactions on documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c4cd-104">Dokumentide käibemaks arvutatakse, luues dokumendi ridadel käibemaksugrupi ja kauba käibemaksugrupi.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="7c4cd-105">Need tulenevad vaikimisi koondandmetest, kuid neid saab vajaduse korral käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="7c4cd-106">Arvutatud käibemaksu saab kontrollida rea ja dokumendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="7c4cd-107">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="7c4cd-108">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="7c4cd-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-109">Click New.</span></span>
3. <span data-ttu-id="7c4cd-110">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="7c4cd-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="7c4cd-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="7c4cd-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-113">Click OK.</span></span>
7. <span data-ttu-id="7c4cd-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7c4cd-115">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="7c4cd-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="7c4cd-117">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="7c4cd-118">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="7c4cd-119">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="7c4cd-120">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="7c4cd-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="7c4cd-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="7c4cd-123">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-123">Click Financials.</span></span>
17. <span data-ttu-id="7c4cd-124">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-124">Click Sales tax.</span></span>
18. <span data-ttu-id="7c4cd-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-125">Click OK.</span></span>
19. <span data-ttu-id="7c4cd-126">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-126">Click Add line.</span></span>
20. <span data-ttu-id="7c4cd-127">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="7c4cd-128">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="7c4cd-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="7c4cd-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="7c4cd-131">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="7c4cd-132">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="7c4cd-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="7c4cd-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="7c4cd-135">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="7c4cd-136">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-136">Click Sales tax.</span></span>
30. <span data-ttu-id="7c4cd-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7c4cd-137">Click OK.</span></span>

