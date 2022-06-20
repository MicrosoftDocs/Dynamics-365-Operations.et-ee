---
title: Värbamistaotluse ametikoht
description: See artikkel kirjeldab värbamise taotluse ametikoha üksust üksuse jaoks Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0996532edf09ea5159e143d92fb2a93c4d6f826d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904242"
---
# <a name="recruiting-request-position"></a>Värbamistaotluse ametikoht


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab värbamise taotluse ametikoha üksust üksuse jaoks Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>Kirjeldus

Kirjeldab värbamistaotlusega täidetavat ametikohta või ametikohti. Ametikoha lisamine värbamistaotlusele on valikuline. Ametikoha atribuudid on kirjutuskaitstud, kuna ametikoha atribuudid ei pea värbamistaotlusel erinema ametikoha koondkirjest. Kui atribuute on vaja muuta, tuleb seda teha ametikoha koondkirjel enne ametikoha lisamist värbamistaotlusele.

### <a name="json-representation"></a>JSON-i esindus
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Värbamistaotluse ametikoha olemi ID**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav |    Värbamistaotluse ametikoha süsteemi loodud kordumatu identifikaator. |
| **Värbamistaotluse ID**<br>mshr_recruitingrequestid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Värbamistaotluse kasutaja loetav kordumatu identifikaator. |
| **Värbamistaotluse ID väärtus**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmrecruitingrequestentityid olemist mshr_hcmrecruitingrequestentity | Värbamistaotluse, millele ametikoht on määratud, süsteemi loodud kordumatu identifikaator. |
| **Ametikoha ID**<br>mshr_positionid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Ametikoha kasutaja loetav kordumatu identifikaator. |
| **Positsiooni ID väärtus**<br>_mshr_fk_position_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmpositionv2entityid olemist mshr_hcmpositionv2entity | Ametikoha süsteemi loodud identifikaator. |
| **Kirjeldus**<br>mshr_description<br>*String* | Kirjutuskaitstud<br>Nõutav | Ametikoha kirjeldus. |
| **Ametikoha tüübi ID**<br>mshr_positiontypeid<br>*String* | Kirjutuskaitstud<br>Valikuline | Selle ametikoha tüübi kasutaja loetav kordumatu identifikaator. |
| **Ametikoha tüübi ID väärtus**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmpositiontypeentityid olemist mshr_hcmpositiontypeentity | Selle ametikoha tüübi süsteemi loodud kordumatu identifikaator. |
| **Olek**<br>mshr_status<br>Suvandikomplekt *RecruitingRequestPositionStatus* | Loe/kirjuta<br>Nõutav | Näitab värbamistaotluse ametikoha olek. |
| **Osakonna number**<br>mshr_departmentnumber<br>*String* | Kirjutuskaitstud<br>Valikuline<br> | Ametikoha osakonna number. |
| **Osakonna ID väärtus**<br>_mshr_fk_department_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_omdepartmententityid olemist mshr_omdepartmententity | Ametikoha osakonna süsteemi loodud kordumatu identifikaator. |
| **Järelevaataja ametikoha ID**<br>mshr_reportstopositionid<br>*String* | Kirjutuskaitstud<br>Nõutav | Selle ametikoha kasutaja loetav ID, millele värvatav ametikoht organisatsiooni hierarhias annab aru. |
| **Järelevaataja ametikoha ID väärtus**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmpositionv2entityid olemist mshr_hcmpositionv2entity | Süsteemi loodud selle ametikoha ID, millele värvatav ametikoht aru annab. |
| **Juhataja personalinumber**<br>mshr_reportstopersonnelnumber<br>*String* | Kirjutuskaitstud<br>Nõutav | Selle töötaja ID, kellele palgatud kandidaat allub. |
| **Järelevaataja töötaja ID väärtus**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmworkerbaseentityid olemist mshr_hcmworkerbaseentity | Selle töötaja süsteemi loodud ID, kellele palgatud kandidaat allub. |
| **Finantsdimensioon**<br>mshr_financialdimension<br>*String* | Kirjutuskaitstud<br>Valikuline | Ametikohale määratud finantsdimensioon (nt kulukeskus). Finantsdimensioon määratakse igale ametikohale juriidilise isiku kohta. Dimensioonides määratletud kulukeskused on juurdepääsetavad selle olemi mshr_dimattributeomcostcenterentity kaudu. |
| **Andmeala ID**<br>mshr_dataareaid<br>*String* | Loe/kirjuta<br>Valikuline | Määratleb värbamistaotluse ametikoha juriidilise isiku (ettevõtte). |
| **Andmeala ID väärtus**<br>_mshr_dataareaid_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: cdm_companyid olemist cdm_company | Süsteemi loodud GUID-väärtus, mis identifitseerib värbamistaotluse ametikoha juriidilise isiku (ettevõtte). |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Teise meetodina värbamistaotluse väärtuse ja ametikoha ID ühendamine kirje kordumatuks tuvastamiseks. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
