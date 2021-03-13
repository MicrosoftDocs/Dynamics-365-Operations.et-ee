---
title: MyLeaveRequestsi ülevaade
description: Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115532"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="5f297-103">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="5f297-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="5f297-104">Üksus MyLeaveRequests rakenduses Microsoft Dynamics 365 Human Resources pakub süsteemi puhkusetaotluste loendit, mis on määratletud (piiratud) praegusele üksusele päringuid esitavale kasutajale juurdepääsetavad.</span><span class="sxs-lookup"><span data-stu-id="5f297-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="5f297-105">Võti</span><span class="sxs-lookup"><span data-stu-id="5f297-105">Key</span></span>

  | <span data-ttu-id="5f297-106">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="5f297-106">Property Name</span></span> | <span data-ttu-id="5f297-107">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="5f297-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="5f297-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5f297-108">dataAreaId</span></span>    | <span data-ttu-id="5f297-109">String</span><span class="sxs-lookup"><span data-stu-id="5f297-109">String</span></span>    |
  | <span data-ttu-id="5f297-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="5f297-110">RequestId</span></span>     | <span data-ttu-id="5f297-111">String</span><span class="sxs-lookup"><span data-stu-id="5f297-111">String</span></span>    |
  | <span data-ttu-id="5f297-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5f297-112">LeaveType</span></span>     | <span data-ttu-id="5f297-113">String</span><span class="sxs-lookup"><span data-stu-id="5f297-113">String</span></span>    |
  | <span data-ttu-id="5f297-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5f297-114">LeaveDate</span></span>     | <span data-ttu-id="5f297-115">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="5f297-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="5f297-116">Atribuudid</span><span class="sxs-lookup"><span data-stu-id="5f297-116">Properties</span></span>

  | <span data-ttu-id="5f297-117">Atribuudi nimi</span><span class="sxs-lookup"><span data-stu-id="5f297-117">Property Name</span></span>     | <span data-ttu-id="5f297-118">Andmetüüp</span><span class="sxs-lookup"><span data-stu-id="5f297-118">Data Type</span></span> | <span data-ttu-id="5f297-119">Nõutav</span><span class="sxs-lookup"><span data-stu-id="5f297-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="5f297-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="5f297-120">dataAreaId</span></span>        | <span data-ttu-id="5f297-121">String</span><span class="sxs-lookup"><span data-stu-id="5f297-121">String</span></span>    | <span data-ttu-id="5f297-122">X</span><span class="sxs-lookup"><span data-stu-id="5f297-122">X</span></span>        |
  | <span data-ttu-id="5f297-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="5f297-123">RequestId</span></span>         | <span data-ttu-id="5f297-124">String</span><span class="sxs-lookup"><span data-stu-id="5f297-124">String</span></span>    | <span data-ttu-id="5f297-125">X</span><span class="sxs-lookup"><span data-stu-id="5f297-125">X</span></span>        |
  | <span data-ttu-id="5f297-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="5f297-126">LeaveType</span></span>         | <span data-ttu-id="5f297-127">String</span><span class="sxs-lookup"><span data-stu-id="5f297-127">String</span></span>    | <span data-ttu-id="5f297-128">X</span><span class="sxs-lookup"><span data-stu-id="5f297-128">X</span></span>        |
  | <span data-ttu-id="5f297-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="5f297-129">LeaveDate</span></span>         | <span data-ttu-id="5f297-130">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="5f297-130">Date</span></span>      | <span data-ttu-id="5f297-131">X</span><span class="sxs-lookup"><span data-stu-id="5f297-131">X</span></span>        |
  | <span data-ttu-id="5f297-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="5f297-132">ReasonCodeId</span></span>      | <span data-ttu-id="5f297-133">String</span><span class="sxs-lookup"><span data-stu-id="5f297-133">String</span></span>    |          |
  | <span data-ttu-id="5f297-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="5f297-134">PersonnelNumber</span></span>   | <span data-ttu-id="5f297-135">String</span><span class="sxs-lookup"><span data-stu-id="5f297-135">String</span></span>    | <span data-ttu-id="5f297-136">X</span><span class="sxs-lookup"><span data-stu-id="5f297-136">X</span></span>        |
  | <span data-ttu-id="5f297-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="5f297-137">RequestDate</span></span>       | <span data-ttu-id="5f297-138">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="5f297-138">Date</span></span>      | <span data-ttu-id="5f297-139">X</span><span class="sxs-lookup"><span data-stu-id="5f297-139">X</span></span>        |
  | <span data-ttu-id="5f297-140">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="5f297-140">Comment</span></span>           | <span data-ttu-id="5f297-141">String</span><span class="sxs-lookup"><span data-stu-id="5f297-141">String</span></span>    |          |
  | <span data-ttu-id="5f297-142">Olek</span><span class="sxs-lookup"><span data-stu-id="5f297-142">Status</span></span>            | <span data-ttu-id="5f297-143">Loetelu</span><span class="sxs-lookup"><span data-stu-id="5f297-143">Enum</span></span>      | <span data-ttu-id="5f297-144">X</span><span class="sxs-lookup"><span data-stu-id="5f297-144">X</span></span>        |
  | <span data-ttu-id="5f297-145">Summa</span><span class="sxs-lookup"><span data-stu-id="5f297-145">Amount</span></span>            | <span data-ttu-id="5f297-146">Tegelik</span><span class="sxs-lookup"><span data-stu-id="5f297-146">Real</span></span>      |          |
  | <span data-ttu-id="5f297-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="5f297-147">HalfDayDefinition</span></span> | <span data-ttu-id="5f297-148">Loetelu</span><span class="sxs-lookup"><span data-stu-id="5f297-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="5f297-149">Tegevused</span><span class="sxs-lookup"><span data-stu-id="5f297-149">Actions</span></span>

 | <span data-ttu-id="5f297-150">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="5f297-150">Action Name</span></span>                               | <span data-ttu-id="5f297-151">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5f297-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="5f297-152">esita</span><span class="sxs-lookup"><span data-stu-id="5f297-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="5f297-153">Esitage taotlus töövoo poolt töötlemiseks..</span><span class="sxs-lookup"><span data-stu-id="5f297-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="5f297-154">Vt ka</span><span class="sxs-lookup"><span data-stu-id="5f297-154">See also</span></span>

- [<span data-ttu-id="5f297-155">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="5f297-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="5f297-156">Autentimine</span><span class="sxs-lookup"><span data-stu-id="5f297-156">Authentication</span></span>](hr-developer-api-authentication.md)