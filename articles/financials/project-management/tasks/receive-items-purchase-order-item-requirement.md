---
title: Ostutellimusel olevate kaupade kaubavajadusest vastuvõtmine
description: See protseduur näitab, kuidas ostutellimusel olevaid kaupu kaubavajadusest vastu võtta.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fee2c965b0c065f00564b849ec93504336fb3f60
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838243"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="99152-103">Ostutellimusel olevate kaupade kaubavajadusest vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="99152-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99152-104">See protseduur näitab, kuidas ostutellimusel olevaid kaupu kaubavajadusest vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="99152-104">This procedure shows how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="99152-105">Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.</span><span class="sxs-lookup"><span data-stu-id="99152-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="99152-106">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="99152-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="99152-107">Avage Projektihaldus ja -arvestus > Projektid > Kõik projektid.</span><span class="sxs-lookup"><span data-stu-id="99152-107">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="99152-108">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="99152-108">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="99152-109">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="99152-109">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="99152-110">Klõpsake nuppu Kaubavajadused.</span><span class="sxs-lookup"><span data-stu-id="99152-110">Click Item requirements.</span></span>
5. <span data-ttu-id="99152-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="99152-111">Click New.</span></span>
6. <span data-ttu-id="99152-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="99152-112">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="99152-113">Sisestage või valige väärtus väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="99152-113">In the Item number field, enter or select a value.</span></span>
8. <span data-ttu-id="99152-114">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="99152-114">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="99152-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="99152-115">Click Save.</span></span>
10. <span data-ttu-id="99152-116">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="99152-116">On the Action Pane, click Manage.</span></span>
11. <span data-ttu-id="99152-117">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="99152-117">Click Functions.</span></span>
12. <span data-ttu-id="99152-118">Klõpsake nuppu Loo ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="99152-118">Click Create purchase order.</span></span>
13. <span data-ttu-id="99152-119">Märkige ruut Kaasata.</span><span class="sxs-lookup"><span data-stu-id="99152-119">Select the Include check box.</span></span>
14. <span data-ttu-id="99152-120">Sisestage väärtus väljale Hankija konto või valige see.</span><span class="sxs-lookup"><span data-stu-id="99152-120">In the Vendor account field, enter or select a value.</span></span>
15. <span data-ttu-id="99152-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="99152-121">Click OK.</span></span>
16. <span data-ttu-id="99152-122">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="99152-122">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
17. <span data-ttu-id="99152-123">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="99152-123">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="99152-124">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="99152-124">On the Action Pane, click Purchase.</span></span>
19. <span data-ttu-id="99152-125">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="99152-125">Click Confirm.</span></span>
20. <span data-ttu-id="99152-126">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="99152-126">On the Action Pane, click Receive.</span></span>
21. <span data-ttu-id="99152-127">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="99152-127">Click Product receipt.</span></span>
22. <span data-ttu-id="99152-128">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="99152-128">In the list, mark the selected row.</span></span>
23. <span data-ttu-id="99152-129">Sisestage väärtus väljale Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="99152-129">In the Product receipt field, type a value.</span></span>
24. <span data-ttu-id="99152-130">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="99152-130">Click OK.</span></span>

