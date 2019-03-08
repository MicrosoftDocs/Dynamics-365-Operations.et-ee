---
title: Uute kasutajate loomine
description: Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysDataAreaSelectLookup, SysSecUserAddRoles, SysUserMSODSUserImport
audience: Application User
ms.reviewer: margoc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 12cf223d262c4e0f2a195e95c83a00fc1a3f07e5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "361954"
---
# <a name="create-new-users"></a><span data-ttu-id="2da16-103">Uute kasutajate loomine</span><span class="sxs-lookup"><span data-stu-id="2da16-103">Create new users</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2da16-104">Kasutajad on teie organisatsioonisisesed töötajad või välised kliendid ja hankijad, kes vajavad oma töö tegemiseks juurdepääsu süsteemile.</span><span class="sxs-lookup"><span data-stu-id="2da16-104">Users are internal employees of your organization, or external customers and vendors, who require access to the system to perform their jobs.</span></span> <span data-ttu-id="2da16-105">Süsteemiadministraatorid saavad selle protseduuri abil lisada süsteemi kasutajaid.</span><span class="sxs-lookup"><span data-stu-id="2da16-105">System administrators can complete this procedure to add users to the system.</span></span> <span data-ttu-id="2da16-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2da16-106">The demo data company used to create this procedure is USMF.</span></span> 


## <a name="add-a-new-user"></a><span data-ttu-id="2da16-107">Lisab uue kirje</span><span class="sxs-lookup"><span data-stu-id="2da16-107">Add a new user</span></span>
1. <span data-ttu-id="2da16-108">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="2da16-108">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="2da16-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2da16-109">Click New.</span></span>
3. <span data-ttu-id="2da16-110">Sisestage väärtus väljale Kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="2da16-110">In the User ID field, type a value.</span></span>
    * <span data-ttu-id="2da16-111">Sisestage kasutaja ainuidentifikaator.</span><span class="sxs-lookup"><span data-stu-id="2da16-111">Enter a unique identifier for the user.</span></span> <span data-ttu-id="2da16-112">Kasutaja ID on kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="2da16-112">A user ID is required.</span></span>  
4. <span data-ttu-id="2da16-113">Sisestage väärtus väljale Kasutaja nimi.</span><span class="sxs-lookup"><span data-stu-id="2da16-113">In the User name field, type a value.</span></span>
    * <span data-ttu-id="2da16-114">Sisestage kasutaja nimi.</span><span class="sxs-lookup"><span data-stu-id="2da16-114">Enter the user's name.</span></span>  
5. <span data-ttu-id="2da16-115">Sisestage väärtus väljale Domeen.</span><span class="sxs-lookup"><span data-stu-id="2da16-115">In the Domain field, type a value.</span></span>
    * <span data-ttu-id="2da16-116">Sisestage kasutaja domeen.</span><span class="sxs-lookup"><span data-stu-id="2da16-116">Enter the user's domain.</span></span>  
6. <span data-ttu-id="2da16-117">Sisestage väärtus väljale Pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="2da16-117">In the Alias field, type a value.</span></span>
    * <span data-ttu-id="2da16-118">Sisestage kasutaja pseudonüüm.</span><span class="sxs-lookup"><span data-stu-id="2da16-118">Enter the user's alias.</span></span>  
7. <span data-ttu-id="2da16-119">Klõpsake väljal Ettevõte otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="2da16-119">In the Company field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="2da16-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2da16-120">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="2da16-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2da16-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2da16-122">Valige kasutaja ettevõte.</span><span class="sxs-lookup"><span data-stu-id="2da16-122">Select the user's company</span></span>  
10. <span data-ttu-id="2da16-123">Klõpsake suvandit Määra rollid.</span><span class="sxs-lookup"><span data-stu-id="2da16-123">Click Assign roles.</span></span>
11. <span data-ttu-id="2da16-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2da16-124">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="2da16-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="2da16-125">Click OK.</span></span>
13. <span data-ttu-id="2da16-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2da16-126">Click Save.</span></span>

## <a name="import-users"></a><span data-ttu-id="2da16-127">Impordi kasutajad</span><span class="sxs-lookup"><span data-stu-id="2da16-127">Import users</span></span>
1. <span data-ttu-id="2da16-128">Klõpsake suvandit Impordi kasutajad.</span><span class="sxs-lookup"><span data-stu-id="2da16-128">Click Import users.</span></span>
2. <span data-ttu-id="2da16-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="2da16-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="2da16-130">Klõpsake suvandit Impordi kasutajad.</span><span class="sxs-lookup"><span data-stu-id="2da16-130">Click Import users.</span></span>
4. <span data-ttu-id="2da16-131">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="2da16-131">Click Close.</span></span>

