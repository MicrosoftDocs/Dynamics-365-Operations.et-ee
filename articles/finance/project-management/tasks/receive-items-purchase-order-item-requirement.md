---
title: Ostutellimusel olevate kaupade kaubavajadusest vastuvõtmine
description: Selles teemas selgitatakse, kuidas ostutellimusel olevaid kaupu kaubavajadusest vastu võtta.
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
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
ms.openlocfilehash: 7afdae65c5ae7e3196c6b9f142dd87aec39b5ea3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174416"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="7e722-103">Ostutellimusel olevate kaupade kaubavajadusest vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="7e722-103">Receive items on purchase order from item requirement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e722-104">Selles teemas selgitatakse, kuidas ostutellimusel olevaid kaupu kaubavajadusest vastu võtta.</span><span class="sxs-lookup"><span data-stu-id="7e722-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="7e722-105">Kasutades kaubakannete asemel kaubavajadusi, saate planeerida tarne just selleks ajaks, mil kaupa tegelikult kasutatakse, luua ostutellimuse, kaasata kauba kaubandusleppe raamistikku ja kaasata kaubavajaduse tootmisplaanidesse.</span><span class="sxs-lookup"><span data-stu-id="7e722-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="7e722-106">Ülesandes kasutatakse USSI andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="7e722-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="7e722-107">Navigeerimispaanil avage **Moodulid > Projektihaldus ja raamatupidamine > Projektid > Kõik projektid**.</span><span class="sxs-lookup"><span data-stu-id="7e722-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="7e722-108">Valige loendis link soovitud reas.</span><span class="sxs-lookup"><span data-stu-id="7e722-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="7e722-109">Valige toimingupaanil nupp **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="7e722-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="7e722-110">Valige **Kaubavajadused**.</span><span class="sxs-lookup"><span data-stu-id="7e722-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="7e722-111">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7e722-111">Select **New**.</span></span>
6. <span data-ttu-id="7e722-112">Uuel real sisestage või valige väärtus väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="7e722-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="7e722-113">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="7e722-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="7e722-114">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7e722-114">Select **Save**.</span></span>
9. <span data-ttu-id="7e722-115">Valige toimingupaanil **Haldus**.</span><span class="sxs-lookup"><span data-stu-id="7e722-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="7e722-116">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="7e722-116">Select **Functions**.</span></span>
11. <span data-ttu-id="7e722-117">Valige käsk **Loo ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="7e722-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="7e722-118">Valige märkeruut **Kaasa kõik**.</span><span class="sxs-lookup"><span data-stu-id="7e722-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="7e722-119">Sisestage või valige väärtus väljale **Hankija konto**.</span><span class="sxs-lookup"><span data-stu-id="7e722-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="7e722-120">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7e722-120">Select **OK**.</span></span>
15. <span data-ttu-id="7e722-121">Avage navigeerimispaanil **Moodulid > Ostureskontro > Ostutellimused > Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="7e722-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="7e722-122">Valige loendis link soovitud reas.</span><span class="sxs-lookup"><span data-stu-id="7e722-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="7e722-123">Valige toimingupaanil **Ostmine**.</span><span class="sxs-lookup"><span data-stu-id="7e722-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="7e722-124">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="7e722-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="7e722-125">Valige toimingupaanil **Vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="7e722-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="7e722-126">Valige **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="7e722-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="7e722-127">Sisestage väärtus väljale **Toote sissetulek**.</span><span class="sxs-lookup"><span data-stu-id="7e722-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="7e722-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="7e722-128">Select **OK**.</span></span>

