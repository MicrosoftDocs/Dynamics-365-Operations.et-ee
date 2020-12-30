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
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4418085"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="857db-103">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="857db-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="857db-104">Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.</span><span class="sxs-lookup"><span data-stu-id="857db-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="857db-105">Võti</span><span class="sxs-lookup"><span data-stu-id="857db-105">Key</span></span>

  | <span data-ttu-id="857db-106">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="857db-106">Property Name</span></span> | <span data-ttu-id="857db-107">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="857db-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="857db-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="857db-108">dataAreaId</span></span>    | <span data-ttu-id="857db-109">String</span><span class="sxs-lookup"><span data-stu-id="857db-109">String</span></span>    |
  | <span data-ttu-id="857db-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="857db-110">RequestId</span></span>     | <span data-ttu-id="857db-111">String</span><span class="sxs-lookup"><span data-stu-id="857db-111">String</span></span>    |
  | <span data-ttu-id="857db-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="857db-112">LeaveType</span></span>     | <span data-ttu-id="857db-113">String</span><span class="sxs-lookup"><span data-stu-id="857db-113">String</span></span>    |
  | <span data-ttu-id="857db-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="857db-114">LeaveDate</span></span>     | <span data-ttu-id="857db-115">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="857db-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="857db-116">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="857db-116">Properties</span></span>

  | <span data-ttu-id="857db-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="857db-117">Property Name</span></span>     | <span data-ttu-id="857db-118">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="857db-118">Data Type</span></span> | <span data-ttu-id="857db-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="857db-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="857db-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="857db-120">dataAreaId</span></span>        | <span data-ttu-id="857db-121">String</span><span class="sxs-lookup"><span data-stu-id="857db-121">String</span></span>    | <span data-ttu-id="857db-122">X</span><span class="sxs-lookup"><span data-stu-id="857db-122">X</span></span>        |
  | <span data-ttu-id="857db-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="857db-123">RequestId</span></span>         | <span data-ttu-id="857db-124">String</span><span class="sxs-lookup"><span data-stu-id="857db-124">String</span></span>    | <span data-ttu-id="857db-125">X</span><span class="sxs-lookup"><span data-stu-id="857db-125">X</span></span>        |
  | <span data-ttu-id="857db-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="857db-126">LeaveType</span></span>         | <span data-ttu-id="857db-127">String</span><span class="sxs-lookup"><span data-stu-id="857db-127">String</span></span>    | <span data-ttu-id="857db-128">X</span><span class="sxs-lookup"><span data-stu-id="857db-128">X</span></span>        |
  | <span data-ttu-id="857db-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="857db-129">LeaveDate</span></span>         | <span data-ttu-id="857db-130">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="857db-130">Date</span></span>      | <span data-ttu-id="857db-131">X</span><span class="sxs-lookup"><span data-stu-id="857db-131">X</span></span>        |
  | <span data-ttu-id="857db-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="857db-132">ReasonCodeId</span></span>      | <span data-ttu-id="857db-133">String</span><span class="sxs-lookup"><span data-stu-id="857db-133">String</span></span>    |          |
  | <span data-ttu-id="857db-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="857db-134">PersonnelNumber</span></span>   | <span data-ttu-id="857db-135">String</span><span class="sxs-lookup"><span data-stu-id="857db-135">String</span></span>    | <span data-ttu-id="857db-136">X</span><span class="sxs-lookup"><span data-stu-id="857db-136">X</span></span>        |
  | <span data-ttu-id="857db-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="857db-137">RequestDate</span></span>       | <span data-ttu-id="857db-138">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="857db-138">Date</span></span>      | <span data-ttu-id="857db-139">X</span><span class="sxs-lookup"><span data-stu-id="857db-139">X</span></span>        |
  | <span data-ttu-id="857db-140">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="857db-140">Comment</span></span>           | <span data-ttu-id="857db-141">String</span><span class="sxs-lookup"><span data-stu-id="857db-141">String</span></span>    |          |
  | <span data-ttu-id="857db-142">Olek</span><span class="sxs-lookup"><span data-stu-id="857db-142">Status</span></span>            | <span data-ttu-id="857db-143">Loetelu</span><span class="sxs-lookup"><span data-stu-id="857db-143">Enum</span></span>      | <span data-ttu-id="857db-144">X</span><span class="sxs-lookup"><span data-stu-id="857db-144">X</span></span>        |
  | <span data-ttu-id="857db-145">Summa</span><span class="sxs-lookup"><span data-stu-id="857db-145">Amount</span></span>            | <span data-ttu-id="857db-146">Tegelik</span><span class="sxs-lookup"><span data-stu-id="857db-146">Real</span></span>      |          |
  | <span data-ttu-id="857db-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="857db-147">HalfDayDefinition</span></span> | <span data-ttu-id="857db-148">Loetelu</span><span class="sxs-lookup"><span data-stu-id="857db-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="857db-149">Tegevused</span><span class="sxs-lookup"><span data-stu-id="857db-149">Actions</span></span>

 | <span data-ttu-id="857db-150">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="857db-150">Action Name</span></span>                               | <span data-ttu-id="857db-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="857db-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="857db-152">esita</span><span class="sxs-lookup"><span data-stu-id="857db-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="857db-153">Esitage taotlus töövoo poolt töötlemiseks..</span><span class="sxs-lookup"><span data-stu-id="857db-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="857db-154">Vt ka</span><span class="sxs-lookup"><span data-stu-id="857db-154">See also</span></span>

- [<span data-ttu-id="857db-155">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="857db-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="857db-156">Autentimine</span><span class="sxs-lookup"><span data-stu-id="857db-156">Authentication</span></span>](hr-developer-api-authentication.md)