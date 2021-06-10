---
title: MyLeaveRequestsi ülevaade
description: Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054952"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="11ce5-103">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="11ce5-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="11ce5-104">Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.</span><span class="sxs-lookup"><span data-stu-id="11ce5-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="11ce5-105">Võti</span><span class="sxs-lookup"><span data-stu-id="11ce5-105">Key</span></span>

  | <span data-ttu-id="11ce5-106">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="11ce5-106">Property Name</span></span> | <span data-ttu-id="11ce5-107">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="11ce5-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="11ce5-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="11ce5-108">dataAreaId</span></span>    | <span data-ttu-id="11ce5-109">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-109">String</span></span>    |
  | <span data-ttu-id="11ce5-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="11ce5-110">RequestId</span></span>     | <span data-ttu-id="11ce5-111">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-111">String</span></span>    |
  | <span data-ttu-id="11ce5-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="11ce5-112">LeaveType</span></span>     | <span data-ttu-id="11ce5-113">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-113">String</span></span>    |
  | <span data-ttu-id="11ce5-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="11ce5-114">LeaveDate</span></span>     | <span data-ttu-id="11ce5-115">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="11ce5-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="11ce5-116">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="11ce5-116">Properties</span></span>

  | <span data-ttu-id="11ce5-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="11ce5-117">Property Name</span></span>     | <span data-ttu-id="11ce5-118">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="11ce5-118">Data Type</span></span> | <span data-ttu-id="11ce5-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="11ce5-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="11ce5-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="11ce5-120">dataAreaId</span></span>        | <span data-ttu-id="11ce5-121">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-121">String</span></span>    | <span data-ttu-id="11ce5-122">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-122">X</span></span>        |
  | <span data-ttu-id="11ce5-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="11ce5-123">RequestId</span></span>         | <span data-ttu-id="11ce5-124">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-124">String</span></span>    | <span data-ttu-id="11ce5-125">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-125">X</span></span>        |
  | <span data-ttu-id="11ce5-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="11ce5-126">LeaveType</span></span>         | <span data-ttu-id="11ce5-127">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-127">String</span></span>    | <span data-ttu-id="11ce5-128">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-128">X</span></span>        |
  | <span data-ttu-id="11ce5-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="11ce5-129">LeaveDate</span></span>         | <span data-ttu-id="11ce5-130">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="11ce5-130">Date</span></span>      | <span data-ttu-id="11ce5-131">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-131">X</span></span>        |
  | <span data-ttu-id="11ce5-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="11ce5-132">ReasonCodeId</span></span>      | <span data-ttu-id="11ce5-133">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-133">String</span></span>    |          |
  | <span data-ttu-id="11ce5-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="11ce5-134">PersonnelNumber</span></span>   | <span data-ttu-id="11ce5-135">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-135">String</span></span>    | <span data-ttu-id="11ce5-136">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-136">X</span></span>        |
  | <span data-ttu-id="11ce5-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="11ce5-137">RequestDate</span></span>       | <span data-ttu-id="11ce5-138">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="11ce5-138">Date</span></span>      | <span data-ttu-id="11ce5-139">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-139">X</span></span>        |
  | <span data-ttu-id="11ce5-140">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="11ce5-140">Comment</span></span>           | <span data-ttu-id="11ce5-141">String</span><span class="sxs-lookup"><span data-stu-id="11ce5-141">String</span></span>    |          |
  | <span data-ttu-id="11ce5-142">Olek</span><span class="sxs-lookup"><span data-stu-id="11ce5-142">Status</span></span>            | <span data-ttu-id="11ce5-143">Loetelu</span><span class="sxs-lookup"><span data-stu-id="11ce5-143">Enum</span></span>      | <span data-ttu-id="11ce5-144">X</span><span class="sxs-lookup"><span data-stu-id="11ce5-144">X</span></span>        |
  | <span data-ttu-id="11ce5-145">Summa</span><span class="sxs-lookup"><span data-stu-id="11ce5-145">Amount</span></span>            | <span data-ttu-id="11ce5-146">Tegelik</span><span class="sxs-lookup"><span data-stu-id="11ce5-146">Real</span></span>      |          |
  | <span data-ttu-id="11ce5-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="11ce5-147">HalfDayDefinition</span></span> | <span data-ttu-id="11ce5-148">Loetelu</span><span class="sxs-lookup"><span data-stu-id="11ce5-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="11ce5-149">Tegevused</span><span class="sxs-lookup"><span data-stu-id="11ce5-149">Actions</span></span>

 | <span data-ttu-id="11ce5-150">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="11ce5-150">Action Name</span></span>                               | <span data-ttu-id="11ce5-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="11ce5-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="11ce5-152">esita</span><span class="sxs-lookup"><span data-stu-id="11ce5-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="11ce5-153">Esitage taotlus töövoo poolt töötlemiseks..</span><span class="sxs-lookup"><span data-stu-id="11ce5-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="11ce5-154">Vt ka</span><span class="sxs-lookup"><span data-stu-id="11ce5-154">See also</span></span>

- [<span data-ttu-id="11ce5-155">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="11ce5-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="11ce5-156">Autentimine</span><span class="sxs-lookup"><span data-stu-id="11ce5-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]