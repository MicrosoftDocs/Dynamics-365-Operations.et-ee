---
title: Värbamistaotluse haridus
description: Selles teemas kirjeldatakse olemit värbamistaotluse haridus rakenduse Dynamics 365 Human Resources jaoks.
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
ms.openlocfilehash: 98c1ba139b7685286757d88ebd5cb99dae0573fb1ddd5c2e88eb3479b4283293
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6759764"
---
# <a name="recruiting-request-education"></a>Värbamistaotluse haridus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse olemit värbamistaotluse haridus rakenduse Dynamics 365 Human Resources jaoks.

Füüsiline nimi: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>Kirjeldus

Kirjeldab haridusnõudeid värbamistaotluse jaoks.

### <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Värbamistaotluse hariduse olemi ID**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Süsteemi loodud kordumatu identifikaator värbamistaotluse hariduse kirjele. |
| **Värbamistaotluse ID**<br>mshr_recruitingrequestid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Seotud värbamistaotluse kasutaja loetav kordumatu identifikaator. |
| **Värbamistaotluse ID väärtus**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmrecruitingrequestentityid olemist mshr_hcmrecruitingrequestentity | Seotud värbamistaotluse süsteemi loodud kordumatu identifikaator. |
| **Haridustaseme ID**<br>mshr_educationlevelid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Nõutav haridustase. |
| **Haridustaseme ID väärtus**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmeducationlevelentityid olemist mshr_hcmeducationlevelentity | Nõutava haridustaseme süsteemi loodud kordumatu identifikaator. |
| **Haridustaseme kirjeldus**<br>mshr_educationleveldescription<br>*String* | Kirjutuskaitstud<br>Nõutav | Oskuse jaoks vajaliku taseme kirjeldus. |
| **Haridusdistsipliini ID**<br>mshr_educationdisciplinedescription<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Haridusdistsipliini valdkond. |
| **Haridusdistsipliini ID väärtus**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmeducationdisciplineentityid olemist mshr_hcmeducationdisciplineentity | Haridusdistsipliini valdkonna süsteemi loodud kordumatu identifikaator. |
| **Haridusdistsipliini kirjeldus**<br>mshr_educationdisciplinedescription<br>String | Kirjutuskaitstud<br>Nõutav | Haridusdistsipliini valdkonna kirjeldus. |
| **Andmeala ID**<br>mshr_dataareaid<br>*String* | Loe/kirjuta<br>Valikuline | Määratleb juriidilise isiku (ettevõtte).|
| **Andmeala ID väärtus**<br>_mshr_dataareaid_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: cdm_companyid olemist cdm_company | Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte). |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Teise meetodina värbamistaotluse väärtuse, haridustaseme ID ja haridusdistsipliini ID ühendamine kirje kordumatuks tuvastamiseks. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]