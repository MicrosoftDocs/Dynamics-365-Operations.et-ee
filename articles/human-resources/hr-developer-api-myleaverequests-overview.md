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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803629"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="7be95-103">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="7be95-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7be95-104">Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.</span><span class="sxs-lookup"><span data-stu-id="7be95-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="7be95-105">Võti</span><span class="sxs-lookup"><span data-stu-id="7be95-105">Key</span></span>

  | <span data-ttu-id="7be95-106">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="7be95-106">Property Name</span></span> | <span data-ttu-id="7be95-107">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="7be95-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="7be95-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7be95-108">dataAreaId</span></span>    | <span data-ttu-id="7be95-109">String</span><span class="sxs-lookup"><span data-stu-id="7be95-109">String</span></span>    |
  | <span data-ttu-id="7be95-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="7be95-110">RequestId</span></span>     | <span data-ttu-id="7be95-111">String</span><span class="sxs-lookup"><span data-stu-id="7be95-111">String</span></span>    |
  | <span data-ttu-id="7be95-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7be95-112">LeaveType</span></span>     | <span data-ttu-id="7be95-113">String</span><span class="sxs-lookup"><span data-stu-id="7be95-113">String</span></span>    |
  | <span data-ttu-id="7be95-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7be95-114">LeaveDate</span></span>     | <span data-ttu-id="7be95-115">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="7be95-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="7be95-116">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="7be95-116">Properties</span></span>

  | <span data-ttu-id="7be95-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="7be95-117">Property Name</span></span>     | <span data-ttu-id="7be95-118">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="7be95-118">Data Type</span></span> | <span data-ttu-id="7be95-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="7be95-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="7be95-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="7be95-120">dataAreaId</span></span>        | <span data-ttu-id="7be95-121">String</span><span class="sxs-lookup"><span data-stu-id="7be95-121">String</span></span>    | <span data-ttu-id="7be95-122">X</span><span class="sxs-lookup"><span data-stu-id="7be95-122">X</span></span>        |
  | <span data-ttu-id="7be95-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="7be95-123">RequestId</span></span>         | <span data-ttu-id="7be95-124">String</span><span class="sxs-lookup"><span data-stu-id="7be95-124">String</span></span>    | <span data-ttu-id="7be95-125">X</span><span class="sxs-lookup"><span data-stu-id="7be95-125">X</span></span>        |
  | <span data-ttu-id="7be95-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="7be95-126">LeaveType</span></span>         | <span data-ttu-id="7be95-127">String</span><span class="sxs-lookup"><span data-stu-id="7be95-127">String</span></span>    | <span data-ttu-id="7be95-128">X</span><span class="sxs-lookup"><span data-stu-id="7be95-128">X</span></span>        |
  | <span data-ttu-id="7be95-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="7be95-129">LeaveDate</span></span>         | <span data-ttu-id="7be95-130">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="7be95-130">Date</span></span>      | <span data-ttu-id="7be95-131">X</span><span class="sxs-lookup"><span data-stu-id="7be95-131">X</span></span>        |
  | <span data-ttu-id="7be95-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="7be95-132">ReasonCodeId</span></span>      | <span data-ttu-id="7be95-133">String</span><span class="sxs-lookup"><span data-stu-id="7be95-133">String</span></span>    |          |
  | <span data-ttu-id="7be95-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="7be95-134">PersonnelNumber</span></span>   | <span data-ttu-id="7be95-135">String</span><span class="sxs-lookup"><span data-stu-id="7be95-135">String</span></span>    | <span data-ttu-id="7be95-136">X</span><span class="sxs-lookup"><span data-stu-id="7be95-136">X</span></span>        |
  | <span data-ttu-id="7be95-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="7be95-137">RequestDate</span></span>       | <span data-ttu-id="7be95-138">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="7be95-138">Date</span></span>      | <span data-ttu-id="7be95-139">X</span><span class="sxs-lookup"><span data-stu-id="7be95-139">X</span></span>        |
  | <span data-ttu-id="7be95-140">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="7be95-140">Comment</span></span>           | <span data-ttu-id="7be95-141">String</span><span class="sxs-lookup"><span data-stu-id="7be95-141">String</span></span>    |          |
  | <span data-ttu-id="7be95-142">Olek</span><span class="sxs-lookup"><span data-stu-id="7be95-142">Status</span></span>            | <span data-ttu-id="7be95-143">Loetelu</span><span class="sxs-lookup"><span data-stu-id="7be95-143">Enum</span></span>      | <span data-ttu-id="7be95-144">X</span><span class="sxs-lookup"><span data-stu-id="7be95-144">X</span></span>        |
  | <span data-ttu-id="7be95-145">Summa</span><span class="sxs-lookup"><span data-stu-id="7be95-145">Amount</span></span>            | <span data-ttu-id="7be95-146">Tegelik</span><span class="sxs-lookup"><span data-stu-id="7be95-146">Real</span></span>      |          |
  | <span data-ttu-id="7be95-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="7be95-147">HalfDayDefinition</span></span> | <span data-ttu-id="7be95-148">Loetelu</span><span class="sxs-lookup"><span data-stu-id="7be95-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="7be95-149">Tegevused</span><span class="sxs-lookup"><span data-stu-id="7be95-149">Actions</span></span>

 | <span data-ttu-id="7be95-150">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="7be95-150">Action Name</span></span>                               | <span data-ttu-id="7be95-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="7be95-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="7be95-152">esita</span><span class="sxs-lookup"><span data-stu-id="7be95-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="7be95-153">Esitage taotlus töövoo poolt töötlemiseks..</span><span class="sxs-lookup"><span data-stu-id="7be95-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="7be95-154">Vt ka</span><span class="sxs-lookup"><span data-stu-id="7be95-154">See also</span></span>

- [<span data-ttu-id="7be95-155">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="7be95-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="7be95-156">Autentimine</span><span class="sxs-lookup"><span data-stu-id="7be95-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]