---
title: MyLeaveRequestsi ülevaade
description: Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092033"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="bea21-103">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="bea21-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="bea21-104">Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.</span><span class="sxs-lookup"><span data-stu-id="bea21-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="bea21-105">Võti</span><span class="sxs-lookup"><span data-stu-id="bea21-105">Key</span></span>

  | <span data-ttu-id="bea21-106">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="bea21-106">Property Name</span></span> | <span data-ttu-id="bea21-107">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="bea21-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="bea21-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="bea21-108">dataAreaId</span></span>    | <span data-ttu-id="bea21-109">String</span><span class="sxs-lookup"><span data-stu-id="bea21-109">String</span></span>    |
  | <span data-ttu-id="bea21-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="bea21-110">RequestId</span></span>     | <span data-ttu-id="bea21-111">String</span><span class="sxs-lookup"><span data-stu-id="bea21-111">String</span></span>    |
  | <span data-ttu-id="bea21-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="bea21-112">LeaveType</span></span>     | <span data-ttu-id="bea21-113">String</span><span class="sxs-lookup"><span data-stu-id="bea21-113">String</span></span>    |
  | <span data-ttu-id="bea21-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="bea21-114">LeaveDate</span></span>     | <span data-ttu-id="bea21-115">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bea21-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="bea21-116">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="bea21-116">Properties</span></span>

  | <span data-ttu-id="bea21-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="bea21-117">Property Name</span></span>     | <span data-ttu-id="bea21-118">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="bea21-118">Data Type</span></span> | <span data-ttu-id="bea21-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="bea21-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="bea21-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="bea21-120">dataAreaId</span></span>        | <span data-ttu-id="bea21-121">String</span><span class="sxs-lookup"><span data-stu-id="bea21-121">String</span></span>    | <span data-ttu-id="bea21-122">X</span><span class="sxs-lookup"><span data-stu-id="bea21-122">X</span></span>        |
  | <span data-ttu-id="bea21-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="bea21-123">RequestId</span></span>         | <span data-ttu-id="bea21-124">String</span><span class="sxs-lookup"><span data-stu-id="bea21-124">String</span></span>    | <span data-ttu-id="bea21-125">X</span><span class="sxs-lookup"><span data-stu-id="bea21-125">X</span></span>        |
  | <span data-ttu-id="bea21-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="bea21-126">LeaveType</span></span>         | <span data-ttu-id="bea21-127">String</span><span class="sxs-lookup"><span data-stu-id="bea21-127">String</span></span>    | <span data-ttu-id="bea21-128">X</span><span class="sxs-lookup"><span data-stu-id="bea21-128">X</span></span>        |
  | <span data-ttu-id="bea21-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="bea21-129">LeaveDate</span></span>         | <span data-ttu-id="bea21-130">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bea21-130">Date</span></span>      | <span data-ttu-id="bea21-131">X</span><span class="sxs-lookup"><span data-stu-id="bea21-131">X</span></span>        |
  | <span data-ttu-id="bea21-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="bea21-132">ReasonCodeId</span></span>      | <span data-ttu-id="bea21-133">String</span><span class="sxs-lookup"><span data-stu-id="bea21-133">String</span></span>    |          |
  | <span data-ttu-id="bea21-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="bea21-134">PersonnelNumber</span></span>   | <span data-ttu-id="bea21-135">String</span><span class="sxs-lookup"><span data-stu-id="bea21-135">String</span></span>    | <span data-ttu-id="bea21-136">X</span><span class="sxs-lookup"><span data-stu-id="bea21-136">X</span></span>        |
  | <span data-ttu-id="bea21-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="bea21-137">RequestDate</span></span>       | <span data-ttu-id="bea21-138">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="bea21-138">Date</span></span>      | <span data-ttu-id="bea21-139">X</span><span class="sxs-lookup"><span data-stu-id="bea21-139">X</span></span>        |
  | <span data-ttu-id="bea21-140">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="bea21-140">Comment</span></span>           | <span data-ttu-id="bea21-141">String</span><span class="sxs-lookup"><span data-stu-id="bea21-141">String</span></span>    |          |
  | <span data-ttu-id="bea21-142">Olek</span><span class="sxs-lookup"><span data-stu-id="bea21-142">Status</span></span>            | <span data-ttu-id="bea21-143">Loetelu</span><span class="sxs-lookup"><span data-stu-id="bea21-143">Enum</span></span>      | <span data-ttu-id="bea21-144">X</span><span class="sxs-lookup"><span data-stu-id="bea21-144">X</span></span>        |
  | <span data-ttu-id="bea21-145">Summa</span><span class="sxs-lookup"><span data-stu-id="bea21-145">Amount</span></span>            | <span data-ttu-id="bea21-146">Tegelik</span><span class="sxs-lookup"><span data-stu-id="bea21-146">Real</span></span>      |          |
  | <span data-ttu-id="bea21-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="bea21-147">HalfDayDefinition</span></span> | <span data-ttu-id="bea21-148">Loetelu</span><span class="sxs-lookup"><span data-stu-id="bea21-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="bea21-149">Tegevused</span><span class="sxs-lookup"><span data-stu-id="bea21-149">Actions</span></span>

 | <span data-ttu-id="bea21-150">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="bea21-150">Action Name</span></span>                               | <span data-ttu-id="bea21-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bea21-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="bea21-152">esita</span><span class="sxs-lookup"><span data-stu-id="bea21-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="bea21-153">Esitage taotlus töövoo poolt töötlemiseks..</span><span class="sxs-lookup"><span data-stu-id="bea21-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="bea21-154">Vt ka</span><span class="sxs-lookup"><span data-stu-id="bea21-154">See also</span></span>

- [<span data-ttu-id="bea21-155">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="bea21-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="bea21-156">Autentimine</span><span class="sxs-lookup"><span data-stu-id="bea21-156">Authentication</span></span>](hr-developer-api-authentication.md)