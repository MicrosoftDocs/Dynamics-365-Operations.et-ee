---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a542ece226750330262e0c44427e5654fa4f6369
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916480"
---
# <a name="create-new-users"></a><span data-ttu-id="7bbbf-103">Uute kasutajate loomine</span><span class="sxs-lookup"><span data-stu-id="7bbbf-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7bbbf-104">Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="7bbbf-105">Süsteemiadministraatorid saavad selle protseduuri abil lisada süsteemi kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="7bbbf-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="7bbbf-107">Lisa uus kasutaja</span><span class="sxs-lookup"><span data-stu-id="7bbbf-107">Add a new user</span></span>
1. <span data-ttu-id="7bbbf-108">Avage **Navigeerimispaan > Moodulid > Süsteemiadministraator > Kasutajad > Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-108">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="7bbbf-109">Paanil **Toimingupaan** klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-109">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="7bbbf-110">Sisestage väärtus väljale **Kasutaja ID**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-110">In the **User ID** field, type a value.</span></span> <span data-ttu-id="7bbbf-111">Sisestage kasutaja ainuidentifikaator.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="7bbbf-112">Kasutaja ID on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-112">A user ID is required.</span></span>  
4. <span data-ttu-id="7bbbf-113">Sisestage väärtus väljale **Kasutajanimi**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-113">In the **User name** field, type a value.</span></span> <span data-ttu-id="7bbbf-114">Sisestage kasutaja nimi.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="7bbbf-115">Sisestage väärtus väljale **Domeen**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-115">In the **Domain** field, type a value.</span></span> <span data-ttu-id="7bbbf-116">Sisestage kasutaja domeen.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="7bbbf-117">Sisestage väärtus väljale **Pseudonüüm**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-117">In the **Alias** field, type a value.</span></span> <span data-ttu-id="7bbbf-118">Sisestage kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="7bbbf-119">Väljal **Ettevõte** klõpsake ripploendi nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-119">In the **Company** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="7bbbf-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-120">In the list, find and select the desired record.</span></span> 
9. <span data-ttu-id="7bbbf-121">Jaotises **Kasutaja rollid** klõpsake **Määra rollid**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-121">In the **User's roles** section, click **Assign roles**.</span></span>
10. <span data-ttu-id="7bbbf-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-122">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="7bbbf-123">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-123">Click **OK**.</span></span>
12. <span data-ttu-id="7bbbf-124">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-124">Click **Save**.</span></span>

## <a name="import-users"></a><span data-ttu-id="7bbbf-125">Impordi kasutajad</span><span class="sxs-lookup"><span data-stu-id="7bbbf-125">Import users</span></span>
1. <span data-ttu-id="7bbbf-126">Paanil **Toimingupaan** klõpsake **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-126">On the **Action pane**, click **Import users**.</span></span>
2. <span data-ttu-id="7bbbf-127">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-127">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="7bbbf-128">Klõpsake **Impordi kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-128">Click **Import users**.</span></span>
4. <span data-ttu-id="7bbbf-129">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="7bbbf-129">Click **Close**.</span></span>

