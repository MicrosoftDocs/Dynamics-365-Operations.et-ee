---
title: Puhkusetaotluse edastamine töövoogu
description: Rakenduses Microsoft Dynamics 365 Human Resources saate kasutada rakenduse programmeerimisliidest (API) MyLeaveRequests submit(), et esitada töövoole puhkusetaotlusi.
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
ms.openlocfilehash: aeb3d66ad24f96efea1b0ea9828a537f8853c94b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465482"
---
# <a name="submit-a-leave-request-to-workflow"></a>Puhkusetaotluse edastamine töövoogu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Rakenduses Microsoft Dynamics 365 Human Resources saate kasutada rakenduse programmeerimisliidest (API) MyLeaveRequests submit(), et esitada töövoole puhkusetaotlusi. Seda API-d pakutakse OData üksuse MyLeaveRequests tegevusena.

## <a name="prerequisites"></a>Eeltingimused

Puhkusetaotlus peab olema andmebaasi salvestatud ja üksuse MyLeaveRequests kaudu kättesaadav.

## <a name="permissions"></a>Õigused

Selle API kutsumiseks on nõutav üks järgmistest lubadest. Lisateavet lubade kohta ja kuidas neid valida, vt teemat [Autentimine](hr-developer-api-authentication.md).

| Loa tüüp                    | Load (kõige vähem privilegeeritust kõige rohkem privilegeerituni) |
|------------------------------------|--------------------------------------------------------|
| Delegeeritud (töö- või koolikonto) | kasutaja\_matkimine                                    |

## <a name="https-request"></a>HTTPS-i taotlus

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Taotlus vastab OData standarditele. Parameetrid {requestId}, {leaveType}, {leaveDate} ja {dataArea} viitavad väljadele, millest koosneb üksuse MyLeaveRequests loomulik liitvõti.

> [!NOTE]
> Kui üksuse MyLeaveRequests väljad viitavad puhkusetaotluse üksikule reale, siis esitamise API kutsumine esitab töövoole kogu puhkusetaotluse (kõik read).

### <a name="request-headers"></a>Päringu päised

| Päis         | Value                     |
|----------------|---------------------------|
| Autoriseerimine  | Kandja {token} (nõutav) |
| Sisu tüüp   | application/json          |

### <a name="request-body"></a>Taotluse kehatekst

Ärge esitage selle meetodi jaoks taotluse kehateksti.

### <a name="response"></a>Vastus

Edukas vastus on alati vastus **204, pole sisu**.

Autoriseerimata kutsujad saavad vastuse **401, volitamata** või **403, keelatud**.

Kui esitamine ei õnnestu (nt kinnituse tõttu), on vastuseks **500, serveri tõrge** ja vastuse kehatekst kaasab JSON-objekti täiendavate üksikasjadega.

## <a name="example"></a>Näide

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

## <a name="validation-and-error-messages"></a>Kinnitamine ja veateated

API esitamise kutsumise osana teostab rakendus Human Resources enne esitamist äriloogika kinnitamist, mis tagab, et puhkusetaotlus on esitamiseks kehtivas olekus. Võimalikud tõrketeated, mille võite saada vastusena, kui kinnitused siin ei õnnestu, on järgmised.

 - Taotlus langetaks saldo {LeaveTypeId} alla lubatud minimaalset saldot {date}.
 - Vaba aja taotlust olekus Lõpetatud ei saa esitada.
 - Taotlust ei saa esitada ega salvestada, kuna muudatusi pole tehtud. Lisage või värskendage summat või puhkuse tüüpi ja proovige uuesti.
 - Sisestatud vaba aja taotlus sisaldab olemasolevate ootel taotluste hulgas ühte või mitut päeva, mis on sama kuupäevaga või puhkuse tüübiga. Muudatuste tegemiseks kutsuge olemasolev taotlus tagasi.
 - Põhjuse kood '{ReasonCodeId}' ei kehti taotluses olevatele puhkuse tüüpidele.
 - Puhkuse tüüp {LeaveTypeId} nõuab põhjuse koodi. Valige sobiv tüüp ja põhjuse kood.
 - Vaba aja esitamine ei õnnestunud. Vaba aeg on salvestatud taotluse mustandina.

## <a name="see-also"></a>Vt ka

- [MyLeaveRequestsi ülevaade](hr-developer-api-myleaverequests-overview.md)
- [Autentimine](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]