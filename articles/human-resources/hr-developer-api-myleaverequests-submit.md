---
title: Puhkusetaotluse edastamine töövoogu
description: Rakenduses Microsoft Dynamics 365 Human Resources saate kasutada rakenduse programmeerimisliidest (API) MyLeaveRequests submit(), et esitada töövoole puhkusetaotlusi.
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
ms.openlocfilehash: bd82bef29e5d1d33c1dc1aa3a039833741c1fdaf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793629"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="fc0f5-103">Puhkusetaotluse edastamine töövoogu</span><span class="sxs-lookup"><span data-stu-id="fc0f5-103">Submit a leave request to workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fc0f5-104">Rakenduses Microsoft Dynamics 365 Human Resources saate kasutada rakenduse programmeerimisliidest (API) MyLeaveRequests submit(), et esitada töövoole puhkusetaotlusi.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="fc0f5-105">Seda API-d pakutakse OData üksuse MyLeaveRequests tegevusena.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="fc0f5-106">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="fc0f5-106">Prerequisites</span></span>

<span data-ttu-id="fc0f5-107">Puhkusetaotlus peab olema andmebaasi salvestatud ja üksuse MyLeaveRequests kaudu kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="fc0f5-108">Õigused</span><span class="sxs-lookup"><span data-stu-id="fc0f5-108">Permissions</span></span>

<span data-ttu-id="fc0f5-109">Selle API kutsumiseks on nõutav üks järgmistest lubadest.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="fc0f5-110">Lisateavet lubade kohta ja kuidas neid valida, vt teemat [Autentimine](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="fc0f5-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="fc0f5-111">Loa tüüp</span><span class="sxs-lookup"><span data-stu-id="fc0f5-111">Permission type</span></span>                    | <span data-ttu-id="fc0f5-112">Load (kõige vähem privilegeeritust kõige rohkem privilegeerituni)</span><span class="sxs-lookup"><span data-stu-id="fc0f5-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="fc0f5-113">Delegeeritud (töö- või koolikonto)</span><span class="sxs-lookup"><span data-stu-id="fc0f5-113">Delegated (work or school account)</span></span> | <span data-ttu-id="fc0f5-114">kasutaja\_matkimine</span><span class="sxs-lookup"><span data-stu-id="fc0f5-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="fc0f5-115">HTTPS-i taotlus</span><span class="sxs-lookup"><span data-stu-id="fc0f5-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="fc0f5-116">Taotlus vastab OData standarditele.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-116">The request conforms to OData standards.</span></span> <span data-ttu-id="fc0f5-117">Parameetrid {requestId}, {leaveType}, {leaveDate} ja {dataArea} viitavad väljadele, millest koosneb üksuse MyLeaveRequests loomulik liitvõti.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="fc0f5-118">Kui üksuse MyLeaveRequests väljad viitavad puhkusetaotluse üksikule reale, siis esitamise API kutsumine esitab töövoole kogu puhkusetaotluse (kõik read).</span><span class="sxs-lookup"><span data-stu-id="fc0f5-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="fc0f5-119">Päringu päised</span><span class="sxs-lookup"><span data-stu-id="fc0f5-119">Request headers</span></span>

| <span data-ttu-id="fc0f5-120">Päis</span><span class="sxs-lookup"><span data-stu-id="fc0f5-120">Header</span></span>         | <span data-ttu-id="fc0f5-121">Value</span><span class="sxs-lookup"><span data-stu-id="fc0f5-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="fc0f5-122">Autoriseerimine</span><span class="sxs-lookup"><span data-stu-id="fc0f5-122">Authorization</span></span>  | <span data-ttu-id="fc0f5-123">Kandja {token} (nõutav)</span><span class="sxs-lookup"><span data-stu-id="fc0f5-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="fc0f5-124">Sisu tüüp</span><span class="sxs-lookup"><span data-stu-id="fc0f5-124">Content-Type</span></span>   | <span data-ttu-id="fc0f5-125">application/json</span><span class="sxs-lookup"><span data-stu-id="fc0f5-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="fc0f5-126">Taotluse kehatekst</span><span class="sxs-lookup"><span data-stu-id="fc0f5-126">Request body</span></span>

<span data-ttu-id="fc0f5-127">Ärge esitage selle meetodi jaoks taotluse kehateksti.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="fc0f5-128">Vastus</span><span class="sxs-lookup"><span data-stu-id="fc0f5-128">Response</span></span>

<span data-ttu-id="fc0f5-129">Edukas vastus on alati vastus **204, pole sisu**.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="fc0f5-130">Autoriseerimata kutsujad saavad vastuse **401, volitamata** või **403, keelatud**.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="fc0f5-131">Kui esitamine ei õnnestu (nt kinnituse tõttu), on vastuseks **500, serveri tõrge** ja vastuse kehatekst kaasab JSON-objekti täiendavate üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="fc0f5-132">Näide</span><span class="sxs-lookup"><span data-stu-id="fc0f5-132">Example</span></span>

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

## <a name="validation-and-error-messages"></a><span data-ttu-id="fc0f5-133">Kinnitamine ja veateated</span><span class="sxs-lookup"><span data-stu-id="fc0f5-133">Validation and error messages</span></span>

<span data-ttu-id="fc0f5-134">API esitamise kutsumise osana teostab rakendus Human Resources enne esitamist äriloogika kinnitamist, mis tagab, et puhkusetaotlus on esitamiseks kehtivas olekus.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="fc0f5-135">Võimalikud tõrketeated, mille võite saada vastusena, kui kinnitused siin ei õnnestu, on järgmised.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="fc0f5-136">Taotlus langetaks saldo {LeaveTypeId} alla lubatud minimaalset saldot {date}.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="fc0f5-137">Vaba aja taotlust olekus Lõpetatud ei saa esitada.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="fc0f5-138">Taotlust ei saa esitada ega salvestada, kuna muudatusi pole tehtud.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="fc0f5-139">Lisage või värskendage summat või puhkuse tüüpi ja proovige uuesti.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="fc0f5-140">Sisestatud vaba aja taotlus sisaldab olemasolevate ootel taotluste hulgas ühte või mitut päeva, mis on sama kuupäevaga või puhkuse tüübiga.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="fc0f5-141">Muudatuste tegemiseks kutsuge olemasolev taotlus tagasi.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="fc0f5-142">Põhjuse kood '{ReasonCodeId}' ei kehti taotluses olevatele puhkuse tüüpidele.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="fc0f5-143">Puhkuse tüüp {LeaveTypeId} nõuab põhjuse koodi.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="fc0f5-144">Valige sobiv tüüp ja põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="fc0f5-145">Vaba aja esitamine ei õnnestunud.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="fc0f5-146">Vaba aeg on salvestatud taotluse mustandina.</span><span class="sxs-lookup"><span data-stu-id="fc0f5-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="fc0f5-147">Vt ka</span><span class="sxs-lookup"><span data-stu-id="fc0f5-147">See also</span></span>

- [<span data-ttu-id="fc0f5-148">MyLeaveRequestsi ülevaade</span><span class="sxs-lookup"><span data-stu-id="fc0f5-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="fc0f5-149">Autentimine</span><span class="sxs-lookup"><span data-stu-id="fc0f5-149">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]