---
title: Värbamistaotluse oskus
description: See artikkel kirjeldab värbamise taotluse oskuste üksust isikule Dynamics 365 Human Resources.
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
ms.openlocfilehash: b17bbdfbc977112344302deada085681ceca9bb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856392"
---
# <a name="recruiting-request-skill"></a>Värbamistaotluse oskus


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab värbamise taotluse oskuste üksust isikule Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>Kirjeldus

Kirjeldab oskuse nõudeid värbamistaotluse jaoks.

### <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Värbamistaotluse oskuse olemi ID**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Süsteemi loodud kordumatu identifikaator kirjele **Värbamistaotluse oskus**. |
| **Värbamistaotluse ID**<br>mshr_recruitingrequestid<br>*String* | Ühekordseks kirjutamiseks<br>Nõutav | Seotud värbamistaotluse kasutaja loetav kordumatu identifikaator. |
| **Värbamistaotluse ID väärtus**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br> Võõrvõti: mshr_hcmrecruitingrequestentityid olemist mshr_hcmrecruitingrequestentity | Seotud värbamistaotluse süsteemi loodud kordumatu identifikaator. |
| **Oskuse ID**<br>mshr_skillid<br>*String*<br> | Ühekordseks kirjutamiseks<br>Nõutav | Vajaliku oskuse kasutaja loetav kordumatu identifikaator. |
| **Oskuse ID väärtus**<br>_mshr_fk_skill_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmskillentityid olemist mshr_hcmskillentity | Nõutava oskuse süsteemi loodud kordumatu identifikaator. |
| **Hindamistaseme ID**<br>mshr_ratinglevelid<br>*String* | Ühekordseks kirjutamiseks<br>Valikuline | Töö jaoks valitud nõutav oskuste taseme väärtus, mis põhineb oskusele määratud hindamismudelil. |
| **Hindamistaseme ID väärtus**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmratinglevelentityid olemist mshr_hcmratinglevelentity | Taseme süsteemi loodud kordumatu identifikaator. |
| **Oskuse kirjeldus**<br>mshr_skilldescription<br>*String* | Kirjutuskaitstud<br>Nõutav | Oskuse kirjeldus. |
| **Hindamistaseme kirjeldus**<br>mshr_ratingleveldescription<br>*String* | Kirjutuskaitstud<br>Valikuline | Valitud oskuse taseme kirjeldus. |
| **Andmeala ID**<br>mshr_dataareaid<br>*String* | Loe/kirjuta<br>Valikuline | Määratleb juriidilise isiku (ettevõtte). |
| **Andmeala ID väärtus**<br>_mshr_dataareaid_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: cdm_companyid olemist cdm_company | Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte). |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Teise meetodina värbamistaotluse väärtuse ja oskuse ID ühendamine kirje kordumatuks tuvastamiseks. |
| **Hindamismudeli ID**<br>mshr_ratingmodelid<br>*String* | Loe-kirjuta<br>Nõutav | Oskuse hindamiseks kasutatav hindamismudel. |
| **Hindamismudeli ID väärtus**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmratingmodelentityid olemist mshr_hcmratingmodelentity | Süsteemi loodud oskuse hindamiseks kasutatava hindamismudeli kordumatu identifikaator. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
