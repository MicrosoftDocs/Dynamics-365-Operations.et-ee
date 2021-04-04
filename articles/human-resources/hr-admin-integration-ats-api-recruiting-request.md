---
title: Värbamistaotlus
description: Selles teemas kirjeldatakse olemit Värbamistaotlus rakenduse Dynamics 365 Human Resources jaoks.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b89d257e3874ad7395c0a2c02f259c2f063aa8d0
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500618"
---
# <a name="recruiting-request"></a>Värbamistaotlus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse olemit Värbamistaotlus rakenduse Dynamics 365 Human Resources jaoks.

Füüsiline nimi: mshr_hcmrecruitingrequestentity

### <a name="description"></a>Kirjeldus

Kirjeldab töökohale värbamise taotlust.

### <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Värbamistaotluse ID**<br>mshr_recruitingrequestid<br>*String* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Kasutaja loetav kordumatu identifikaator inimressursside rakenduses kuvatud taotlusele. Numbriseeria. |
| **Värbamistaotluse olemi ID**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Süsteemi loodud GUID-väärtus värbamistaotluse kordumatuks tuvastamiseks. |
| **Andmeala ID**<br>mshr_dataareaid<br>*String* | Loe/kirjuta<br>Valikuline<br> | Määratleb värbamistaotluse juriidilise isiku (ettevõtte). |
| **Andmeala ID väärtus**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: cdm_companyid olemist cdm_company | Süsteemi loodud GUID-väärtus, mis identifitseerib värbamistaotluse juriidilise isiku (ettevõtte). |
| **Värbamisjuhi personalinumber**<br>mshr_hiringmanagerpersonnelnumber<br>*String* | Loe/kirjuta<br>Valikuline | Selle värbamistaotlusega seotud värbamisjuhi personalinumber. |
| **Värbamishalduri ID väärtus**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmworkerbaseentityid olemist mshr_hcmworkerbaseentity | Süsteemi loodud GUID-väärtus värbamistaotlusega seotud halduri tuvastamiseks. |
| **Värbaja osapoolenumber**<br>mshr_recruiterpartynumber<br>*String* | Loe/kirjuta<br>Valikuline | Taotluse jaoks valitud värbaja isiku (osapoole) number. |
| **Värbaja ID väärtus**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud GUID-väärtus värbamistaotlusega seotud värbaja tuvastamiseks. |
| **Olek**<br>mshr_status<br>Suvandikomplekt *RecruitingRequestStatus* | Loe/kirjuta<br>Nõutav<br> | Näitab värbamistaotluse olekut. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Kirjeldab taotlust. |
| **Värbamistaotluse asukoha ID**<br>mshr_recruitingrequestlocationid<br>*String* | Loe/kirjuta<br>Valikuline | Selle taotlusega seotud töö asukoha kasutaja loetav kordumatu identifikaator. |
| **Värbamise asukoha ID väärtus**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmrecruitingrequestlocationentityid olemist mshr_hcmrecruitingrequestlocationentity | Süsteemi loodud GUID-väärtus taotlusele valitud asukoha värbamistaotluse tuvastamiseks. |
| **Kommentaarid**<br>mshr_comments<br>*String* | Loe/kirjuta<br>Valikuline | Kommentaarid värbamishaldurite ja värbajate kasutamiseks oleva taotluse kohta. |
| **Töö ID**<br>mshr_jobid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav |   Selle taotlusega seotud kõigi ametikohtade ühise töö kasutaja loetav kordumatu identifikaator. |
| **Töö ID väärtus**<br>_mshr_fk_job_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmjobentityid olemist mshr_hcmjobentity | Selle värbamistaotlusega seotud kõigi ametikohtade ühise töö süsteemi loodud kordumatu identifikaator. |
| **Ametinimetuse ID**<br>mshr_titleid<br>*String* | Kirjutuskaitstud<br>Nõutav | Selle taotlusega seotud ametinimetuse kasutaja loetav kordumatu identifikaator. |
| **Ametinimetuse ID väärtus**<br>_mshr_fk_title_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmtitleid olemist mshr_hcmtitleentity | Värbamistaotlusele valitud süsteemi loodud ametinimetuse kordumatu identifikaator. |
| **Tööfunktsiooni ID**<br>mshr_jobfunctionid<br>*String* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_jobfunctionid olemist mshr_hcmjobfunctionentity | Selle taotlusega seotud tööfunktsiooni kasutaja loetav kordumatu identifikaator. |
| **Vaikimisi täistööaja vaste**<br>mshr_defaultfulltimeequivalency<br>*Topelttäpsusega* | Kirjutuskaitstud<br>Nõutav | Töö täistööajaga samaväärne väärtus, kus 1.0 esindab täistööajaga töötajat. |
| **Regulatiivse töö kategooria**<br>mshr_regulatoryjobcategory<br>Suvandikomplekt *RegulatoryJobCategory* | Kirjutuskaitstud<br>Valikuline | Töö jaoks valitud tööfunktsiooni EEO töökategooria. Kehtivad väärtused suvandikomplektis HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **Töö tüübi ID**<br>mshr_jobtypeid<br>*String* | Kirjutuskaitstud<br>Valikuline | Ametikohaga seotud töö tüüp. Töö tüübid on kasutaja määratletud väärtused, mis on saadaval olemis mshr_hcmjobtypeentity. |
| **Töö tüübi ID väärtus**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmjobtypeentityid olemist mshr_hcmjobtypenentity | Selle värbamistaotlusega seotud töö tüübi süsteemi loodud kordumatu identifikaator. |
| **Vabastuse olek**<br>mshr_exemptstatus<br>Suvandikomplekt *JobExemptStatus* | Kirjutuskaitstud<br>Valikuline | Töötüübil põhinev FLSA-vabastuse olek. |
| **Eeldatav alguskuupäev**<br>mshr_estimatedstartdate<br>*Kuupäev* | Loe/kirjuta<br>Nõutav | Eeldatav kuupäev, mil kandidaat tööd alustaks. |
| **Väline kirjeldus**<br>mshr_externaldescription<br>*String* | Loe/kirjuta<br>Valikuline | Töö/ametikoha kirjeldus kandidaadile. | 
| **Kompensatsiooni madal lävi**<br>mshr_compensationlowthreshold<br>*Topelttäpsusega* | Loe/kirjuta<br>Valikuline | Hüvitustaseme alampiir. |
| **Hüvituse kontrollpunkt**<br>mshr_compensationcontrolpoint<br>*Topelttäpsusega* | Loe/kirjuta<br>Valikuline | Hüvitustaseme kontrollpunkt. |
| **Kompensatsiooni kõrge lävi**<br>mshr_compensationhighthreshold<br>*Topelttäpsusega* | Loe/kirjuta<br>Valikuline | Hüvitustaseme ülempiir. |
| **Hüvitustase**<br>mshr_compensationlevelid<br>*String* | Loe/kirjuta<br>Valikuline | Töö hüvituse tase. Töö saab seadistada mitme hüvitustasemega. See atribuut näitab selle taotluse jaoks valitud töö hüvituse taset. |
| **Töö hüvitise ID**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmjobcompensationentityid olemist mshr_hcmjobcompensationentity | Selle värbamistaotlusega seotud hüvitise taseme süsteemi loodud kordumatu identifikaator. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
