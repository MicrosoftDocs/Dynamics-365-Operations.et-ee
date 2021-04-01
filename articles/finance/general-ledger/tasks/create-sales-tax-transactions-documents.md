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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3cc70915902863d85aa75af7f4c03e5b83c7cb22
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240806"
---
# <a name="create-sales-tax-transactions-on-documents"></a><span data-ttu-id="34078-103">Käibemaksukannete loomine dokumentidel</span><span class="sxs-lookup"><span data-stu-id="34078-103">Create sales tax transactions on documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34078-104">Dokumentide käibemaks arvutatakse, luues dokumendi ridadel käibemaksugrupi ja kauba käibemaksugrupi.</span><span class="sxs-lookup"><span data-stu-id="34078-104">Sales tax on documents is calculated by providing a Sales tax group and an Item sales tax group on document lines.</span></span> <span data-ttu-id="34078-105">Need tulenevad vaikimisi koondandmetest, kuid neid saab vajaduse korral käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="34078-105">These default from master data but can be changed manually if necessary.</span></span> <span data-ttu-id="34078-106">Arvutatud käibemaksu saab kontrollida rea ja dokumendi tasemel.</span><span class="sxs-lookup"><span data-stu-id="34078-106">The calculated sales tax can be checked on a line and document level.</span></span> <span data-ttu-id="34078-107">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="34078-107">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="34078-108">Avage Müügireskontro > Tellimused > Kõik müügitellimused.</span><span class="sxs-lookup"><span data-stu-id="34078-108">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="34078-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="34078-109">Click New.</span></span>
3. <span data-ttu-id="34078-110">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="34078-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="34078-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="34078-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="34078-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="34078-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="34078-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34078-113">Click OK.</span></span>
7. <span data-ttu-id="34078-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="34078-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="34078-115">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="34078-115">In the Item number field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="34078-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="34078-116">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="34078-117">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="34078-117">In the Unit price field, enter a number.</span></span>
11. <span data-ttu-id="34078-118">Laiendage või ahendage jaotist Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="34078-118">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="34078-119">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="34078-119">Click the Setup tab.</span></span>
13. <span data-ttu-id="34078-120">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="34078-120">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="34078-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="34078-121">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="34078-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="34078-122">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="34078-123">Klõpsake suvandit Finantsid.</span><span class="sxs-lookup"><span data-stu-id="34078-123">Click Financials.</span></span>
17. <span data-ttu-id="34078-124">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="34078-124">Click Sales tax.</span></span>
18. <span data-ttu-id="34078-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34078-125">Click OK.</span></span>
19. <span data-ttu-id="34078-126">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="34078-126">Click Add line.</span></span>
20. <span data-ttu-id="34078-127">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="34078-127">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="34078-128">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="34078-128">In the Item number field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="34078-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="34078-129">In the list, find and select the desired record.</span></span>
23. <span data-ttu-id="34078-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="34078-130">In the list, click the link in the selected row.</span></span>
24. <span data-ttu-id="34078-131">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="34078-131">In the Unit price field, enter a number.</span></span>
25. <span data-ttu-id="34078-132">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="34078-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
26. <span data-ttu-id="34078-133">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="34078-133">In the list, find and select the desired record.</span></span>
27. <span data-ttu-id="34078-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="34078-134">In the list, click the link in the selected row.</span></span>
28. <span data-ttu-id="34078-135">Klõpsake toimingupaanil suvandit Müük.</span><span class="sxs-lookup"><span data-stu-id="34078-135">On the Action Pane, click Sell.</span></span>
29. <span data-ttu-id="34078-136">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="34078-136">Click Sales tax.</span></span>
30. <span data-ttu-id="34078-137">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="34078-137">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]