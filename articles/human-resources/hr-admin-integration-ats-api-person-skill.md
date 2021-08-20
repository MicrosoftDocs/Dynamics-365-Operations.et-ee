---
title: Isiku oskus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku oskus.
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
ms.openlocfilehash: d2721e3eace401537e85e57b5895d508317e6c4b71d481d15ff176b786a937e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756192"
---
# <a name="person-skill"></a>Isiku oskus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku oskus.

Füüsiline nimi: mshr_hcmpersonskillentity

## <a name="description"></a>Kirjeldus

See üksus kirjeldab kandidaadi oskusi.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku oskuse olemi ID**<br>mshr_hcmpersonskillentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav | Olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav |   Seotud osapoole (isiku) ID. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator. |
| **Sertifikaati väljastaaja**<br>mshr_certifier<br>*String* | Loe/kirjuta<br>Valikuline | Oskuse kinnitanud töötaja personalinumber. |
| **Serdi ID väärtus**<br>_mshr_fk_certifier_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmworkerentityid olemist mshr_hcmworkerentity | Süsteemi loodud oskuse kinnitanud töötaja kirje kordumatu identifikaator. |
| **Oskuse ID**<br>mshr_skillid<br>*String* | Loe/kirjuta<br>Nõutav | Human Resourcesis määratletud oskuse identifikaator. |
| **Oskuse ID väärtus**<br>_mshr_fk_skill_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmskillentityid olemist mshr_hcmskillentity | Süsteemi loodud valitud oskuse identifikaator. |
| **Kogemus aastates**<br>mshr_yearsofexperience<br>*Kümnendkoht* | Loe/kirjuta<br>Valikuline | Töökogemus aastates, mis kandidaadil selle oskusega on. |
| **Hinnangu ID**<br>mshr_ratingid<br>*String* | Loe/kirjuta<br>Nõutav | Hindamisskaala tüüp. Selle üksuse puhul on väärtus **Oskused**. |
| **Taseme tüüp**<br>mshr_leveltype<br>*suvandikomplekt mshr_hrmskillleveltype* | Loe/kirjuta<br>Nõutav | Oskusele määratud taseme kategoriseerimise tüüp. |
| **Taseme ID**<br>mshr_levelid<br>*String* | Loe/kirjuta<br>Nõutav | Hindamistaseme ID, mis kandidaadil selle oskuse jaoks on. |
| **Hindamistaseme ID väärtus**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmratinglevelentityid olemist mshr_hcmratinglevelentity | Tase,e süsteemi loodud kordumatu hindamistaseme identifikaator. |
| **Taseme kuupäev**<br>mshr_leveldate<br>*Datetime* | Loe/kirjuta<br>Nõutav | Kuupäev, mil kandidaati oskuses hinnati. |
| **Hindamistaseme kontrollija**<br>mshr_ratinglevelexaminer<br>*String* | Loe/kirjuta<br>Valikuline | Kandidaati hinnanud töötaja personalinumber. |
| **Hindamistaseme kontrollija ID väärtus**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmworkerentityid olemist mshr_hcmworkerentity | Süsteemi loodud selle töötaja identifikaator, kes uuris kandidaadi oskuste taset. |
| **Kinnitatud**<br>mshr_verified<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Nõutav | Näitab, kas hinnanguline oskuste tase on kinnitatud. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje esmase ID-na. Osapoole numbri, taseme tüübi, oskuse ID ja taseme kuupäeva kombinatsioon. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]