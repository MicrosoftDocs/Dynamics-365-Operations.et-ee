---
title: Puhkusetaotluse edastamine töövoogu
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
ms.openlocfilehash: 008ee231ca9f0459e332b17cea9f2a3f3e3cc2a5
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008798"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="1f45c-102">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="1f45c-102">Submit a leave request to workflow</span></span>

<span data-ttu-id="1f45c-103">Rakenduses Microsoft Dynamics 365 Human Resources saate kasutada rakenduse programmeerimisliidest (API) MyLeaveRequests submit(), et esitada töövoole puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="1f45c-103">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="1f45c-104">Seda API-d pakutakse OData üksuse MyLeaveRequests tegevusena.</span><span class="sxs-lookup"><span data-stu-id="1f45c-104">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1f45c-105">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="1f45c-105">Prerequisites</span></span>

<span data-ttu-id="1f45c-106">Puhkusetaotlus peab olema andmebaasi salvestatud ja üksuse MyLeaveRequests kaudu kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="1f45c-106">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="1f45c-107">Õigused</span><span class="sxs-lookup"><span data-stu-id="1f45c-107">Permissions</span></span>

<span data-ttu-id="1f45c-108">Selle API kutsumiseks on nõutav üks järgmistest lubadest.</span><span class="sxs-lookup"><span data-stu-id="1f45c-108">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="1f45c-109">Lisateavet lubade kohta ja kuidas neid valida, vt teemat [Autentimine](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="1f45c-109">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="1f45c-110">Loa tüüp</span><span class="sxs-lookup"><span data-stu-id="1f45c-110">Permission type</span></span>                    | <span data-ttu-id="1f45c-111">Load (kõige vähem privilegeeritust kõige rohkem privilegeerituni)</span><span class="sxs-lookup"><span data-stu-id="1f45c-111">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="1f45c-112">Delegeeritud (töö- või koolikonto)</span><span class="sxs-lookup"><span data-stu-id="1f45c-112">Delegated (work or school account)</span></span> | <span data-ttu-id="1f45c-113">kasutaja\_matkimine</span><span class="sxs-lookup"><span data-stu-id="1f45c-113">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="1f45c-114">HTTPS-i taotlus</span><span class="sxs-lookup"><span data-stu-id="1f45c-114">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="1f45c-115">Taotlus vastab OData standarditele.</span><span class="sxs-lookup"><span data-stu-id="1f45c-115">The request conforms to OData standards.</span></span> <span data-ttu-id="1f45c-116">Parameetrid {requestId}, {leaveType}, {leaveDate} ja {dataArea} viitavad väljadele, millest koosneb üksuse MyLeaveRequests loomulik liitvõti.</span><span class="sxs-lookup"><span data-stu-id="1f45c-116">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="1f45c-117">Kui üksuse MyLeaveRequests väljad viitavad puhkusetaotluse üksikule reale, siis esitamise API kutsumine esitab töövoole kogu puhkusetaotluse (kõik read).</span><span class="sxs-lookup"><span data-stu-id="1f45c-117">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="1f45c-118">Päringu päised</span><span class="sxs-lookup"><span data-stu-id="1f45c-118">Request headers</span></span>

| <span data-ttu-id="1f45c-119">Päis</span><span class="sxs-lookup"><span data-stu-id="1f45c-119">Header</span></span>         | <span data-ttu-id="1f45c-120">Value</span><span class="sxs-lookup"><span data-stu-id="1f45c-120">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="1f45c-121">Autoriseerimine</span><span class="sxs-lookup"><span data-stu-id="1f45c-121">Authorization</span></span>  | <span data-ttu-id="1f45c-122">Kandja {token} (nõutav)</span><span class="sxs-lookup"><span data-stu-id="1f45c-122">Bearer {token} (required)</span></span> |
| <span data-ttu-id="1f45c-123">Sisu tüüp</span><span class="sxs-lookup"><span data-stu-id="1f45c-123">Content-Type</span></span>   | <span data-ttu-id="1f45c-124">application/json</span><span class="sxs-lookup"><span data-stu-id="1f45c-124">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="1f45c-125">Taotluse kehatekst</span><span class="sxs-lookup"><span data-stu-id="1f45c-125">Request body</span></span>

<span data-ttu-id="1f45c-126">Ärge esitage selle meetodi jaoks taotluse kehateksti.</span><span class="sxs-lookup"><span data-stu-id="1f45c-126">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="1f45c-127">Vastus</span><span class="sxs-lookup"><span data-stu-id="1f45c-127">Response</span></span>

<span data-ttu-id="1f45c-128">Edukas vastus on alati vastus **204, pole sisu**.</span><span class="sxs-lookup"><span data-stu-id="1f45c-128">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="1f45c-129">Autoriseerimata kutsujad saavad vastuse **401, volitamata** või **403, keelatud**.</span><span class="sxs-lookup"><span data-stu-id="1f45c-129">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="1f45c-130">Kui esitamine ei õnnestu (nt kinnituse tõttu), on vastuseks **500, serveri tõrge** ja vastuse kehatekst kaasab JSON-objekti täiendavate üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="1f45c-130">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="1f45c-131">Näide</span><span class="sxs-lookup"><span data-stu-id="1f45c-131">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="1f45c-132">Kinnitamine ja veateated</span><span class="sxs-lookup"><span data-stu-id="1f45c-132">Validation and error messages</span></span>

<span data-ttu-id="1f45c-133">API esitamise kutsumise osana teostab rakendus Human Resources enne esitamist äriloogika kinnitamist, mis tagab, et puhkusetaotlus on esitamiseks kehtivas olekus.</span><span class="sxs-lookup"><span data-stu-id="1f45c-133">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="1f45c-134">Võimalikud tõrketeated, mille võite saada vastusena, kui kinnitused siin ei õnnestu, on järgmised.</span><span class="sxs-lookup"><span data-stu-id="1f45c-134">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="1f45c-135">Taotlus langetaks saldo {LeaveTypeId} alla lubatud minimaalset saldot {date}.</span><span class="sxs-lookup"><span data-stu-id="1f45c-135">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="1f45c-136">Vaba aja taotlust olekus Lõpetatud ei saa esitada.</span><span class="sxs-lookup"><span data-stu-id="1f45c-136">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="1f45c-137">Taotlust ei saa esitada ega salvestada, kuna muudatusi pole tehtud.</span><span class="sxs-lookup"><span data-stu-id="1f45c-137">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="1f45c-138">Lisage või värskendage summat või puhkuse tüüpi ja proovige uuesti.</span><span class="sxs-lookup"><span data-stu-id="1f45c-138">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="1f45c-139">Sisestatud vaba aja taotlus sisaldab olemasolevate ootel taotluste hulgas ühte või mitut päeva, mis on sama kuupäevaga või puhkuse tüübiga.</span><span class="sxs-lookup"><span data-stu-id="1f45c-139">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="1f45c-140">Muudatuste tegemiseks kutsuge olemasolev taotlus tagasi.</span><span class="sxs-lookup"><span data-stu-id="1f45c-140">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="1f45c-141">Põhjuse kood '{ReasonCodeId}' ei kehti taotluses olevatele puhkuse tüüpidele.</span><span class="sxs-lookup"><span data-stu-id="1f45c-141">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="1f45c-142">Puhkuse tüüp {LeaveTypeId} nõuab põhjuse koodi.</span><span class="sxs-lookup"><span data-stu-id="1f45c-142">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="1f45c-143">Valige sobiv tüüp ja põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="1f45c-143">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="1f45c-144">Vaba aja esitamine ei õnnestunud.</span><span class="sxs-lookup"><span data-stu-id="1f45c-144">The time off was not submitted successfully.</span></span> <span data-ttu-id="1f45c-145">Vaba aeg on salvestatud taotluse mustandina.</span><span class="sxs-lookup"><span data-stu-id="1f45c-145">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f45c-146">Vt ka</span><span class="sxs-lookup"><span data-stu-id="1f45c-146">See also</span></span>

- [<span data-ttu-id="1f45c-147">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="1f45c-147">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="1f45c-148">Autentimine</span><span class="sxs-lookup"><span data-stu-id="1f45c-148">Authentication</span></span>](hr-developer-api-authentication.md)