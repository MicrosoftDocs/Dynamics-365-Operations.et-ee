---
title: MyLeaveRequestsi ülevaade
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008747"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="677ae-102">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="677ae-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="677ae-103">Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.</span><span class="sxs-lookup"><span data-stu-id="677ae-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="677ae-104">Võti</span><span class="sxs-lookup"><span data-stu-id="677ae-104">Key</span></span>

  | <span data-ttu-id="677ae-105">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="677ae-105">Property Name</span></span> | <span data-ttu-id="677ae-106">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="677ae-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="677ae-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="677ae-107">dataAreaId</span></span>    | <span data-ttu-id="677ae-108">String</span><span class="sxs-lookup"><span data-stu-id="677ae-108">String</span></span>    |
  | <span data-ttu-id="677ae-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="677ae-109">RequestId</span></span>     | <span data-ttu-id="677ae-110">String</span><span class="sxs-lookup"><span data-stu-id="677ae-110">String</span></span>    |
  | <span data-ttu-id="677ae-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="677ae-111">LeaveType</span></span>     | <span data-ttu-id="677ae-112">String</span><span class="sxs-lookup"><span data-stu-id="677ae-112">String</span></span>    |
  | <span data-ttu-id="677ae-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="677ae-113">LeaveDate</span></span>     | <span data-ttu-id="677ae-114">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="677ae-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="677ae-115">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="677ae-115">Properties</span></span>

  | <span data-ttu-id="677ae-116">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="677ae-116">Property Name</span></span>     | <span data-ttu-id="677ae-117">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="677ae-117">Data Type</span></span> | <span data-ttu-id="677ae-118">Nõutav</span><span class="sxs-lookup"><span data-stu-id="677ae-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="677ae-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="677ae-119">dataAreaId</span></span>        | <span data-ttu-id="677ae-120">String</span><span class="sxs-lookup"><span data-stu-id="677ae-120">String</span></span>    | <span data-ttu-id="677ae-121">X</span><span class="sxs-lookup"><span data-stu-id="677ae-121">X</span></span>        |
  | <span data-ttu-id="677ae-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="677ae-122">RequestId</span></span>         | <span data-ttu-id="677ae-123">String</span><span class="sxs-lookup"><span data-stu-id="677ae-123">String</span></span>    | <span data-ttu-id="677ae-124">X</span><span class="sxs-lookup"><span data-stu-id="677ae-124">X</span></span>        |
  | <span data-ttu-id="677ae-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="677ae-125">LeaveType</span></span>         | <span data-ttu-id="677ae-126">String</span><span class="sxs-lookup"><span data-stu-id="677ae-126">String</span></span>    | <span data-ttu-id="677ae-127">X</span><span class="sxs-lookup"><span data-stu-id="677ae-127">X</span></span>        |
  | <span data-ttu-id="677ae-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="677ae-128">LeaveDate</span></span>         | <span data-ttu-id="677ae-129">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="677ae-129">Date</span></span>      | <span data-ttu-id="677ae-130">X</span><span class="sxs-lookup"><span data-stu-id="677ae-130">X</span></span>        |
  | <span data-ttu-id="677ae-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="677ae-131">ReasonCodeId</span></span>      | <span data-ttu-id="677ae-132">String</span><span class="sxs-lookup"><span data-stu-id="677ae-132">String</span></span>    |          |
  | <span data-ttu-id="677ae-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="677ae-133">PersonnelNumber</span></span>   | <span data-ttu-id="677ae-134">String</span><span class="sxs-lookup"><span data-stu-id="677ae-134">String</span></span>    | <span data-ttu-id="677ae-135">X</span><span class="sxs-lookup"><span data-stu-id="677ae-135">X</span></span>        |
  | <span data-ttu-id="677ae-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="677ae-136">RequestDate</span></span>       | <span data-ttu-id="677ae-137">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="677ae-137">Date</span></span>      | <span data-ttu-id="677ae-138">X</span><span class="sxs-lookup"><span data-stu-id="677ae-138">X</span></span>        |
  | <span data-ttu-id="677ae-139">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="677ae-139">Comment</span></span>           | <span data-ttu-id="677ae-140">String</span><span class="sxs-lookup"><span data-stu-id="677ae-140">String</span></span>    |          |
  | <span data-ttu-id="677ae-141">Olek</span><span class="sxs-lookup"><span data-stu-id="677ae-141">Status</span></span>            | <span data-ttu-id="677ae-142">Loetelu</span><span class="sxs-lookup"><span data-stu-id="677ae-142">Enum</span></span>      | <span data-ttu-id="677ae-143">X</span><span class="sxs-lookup"><span data-stu-id="677ae-143">X</span></span>        |
  | <span data-ttu-id="677ae-144">Summa</span><span class="sxs-lookup"><span data-stu-id="677ae-144">Amount</span></span>            | <span data-ttu-id="677ae-145">Tegelik</span><span class="sxs-lookup"><span data-stu-id="677ae-145">Real</span></span>      |          |
  | <span data-ttu-id="677ae-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="677ae-146">HalfDayDefinition</span></span> | <span data-ttu-id="677ae-147">Loetelu</span><span class="sxs-lookup"><span data-stu-id="677ae-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="677ae-148">Tegevused</span><span class="sxs-lookup"><span data-stu-id="677ae-148">Actions</span></span>

 | <span data-ttu-id="677ae-149">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="677ae-149">Action Name</span></span>                               | <span data-ttu-id="677ae-150">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="677ae-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="677ae-151">esita</span><span class="sxs-lookup"><span data-stu-id="677ae-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="677ae-152">Esitage taotlus töövoo poolt töötlemiseks..</span><span class="sxs-lookup"><span data-stu-id="677ae-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="677ae-153">Vt ka</span><span class="sxs-lookup"><span data-stu-id="677ae-153">See also</span></span>

- [<span data-ttu-id="677ae-154">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="677ae-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="677ae-155">Autentimine</span><span class="sxs-lookup"><span data-stu-id="677ae-155">Authentication</span></span>](hr-developer-api-authentication.md)