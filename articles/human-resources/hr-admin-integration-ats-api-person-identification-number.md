---
title: Isiku ID-number
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit isiku ID-number.
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
ms.openlocfilehash: 054547c4f33e50d2dc0fa275559ba6ed44c27971
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125397"
---
# <a name="person-identification-number"></a>Isiku ID-number

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit isiku ID-number.

Füüsiline nimi: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>Kirjeldus

Selles olemis kirjeldatakse kandidaadi ID-numbreid. See võimaldab API tarbijal kirjutada kandidaadi kirjesse ID-koode, nt isikukoode või passinumbreid. Töötaja kirjel on ID-numbrid, aga mitte kandidaadi kirjel. Integreeriv rakendus saab kirjutada väärtused rakenduse Human Resources andmebaasi, kuid numbreid ei kuvata rakenduses Human Resources enne, kui kandidaadi töötajakirje on loodud.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku ID-numbri olemi ID**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Isiku ID-numbri kirje kordumatu peamine identifikaator. |
| **Kirje tüüp**<br>mshr_entrytype<br>*String* | Loe-kirjuta<br>Valikuline | Vaba väärtus ID-numbri kirjetüübile viitamiseks. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe-kirjuta<br>Valikuline | ID-numbri kirjeldus. |
| **Aegumiskuupäev**<br>mshr_expirationdate<br>*Datetime* | Loe-kirjuta<br>Valikuline | Kuupäev, millal seotud dokumendi ID-number aegub. |
| **On esmane**<br>mshr_isprimary<br>*suvandikomplekt mshr_noyes* | Loe-kirjuta<br>Valikuline | Määratleb, kas ID-number on selle ID-tüübi jaoks isiku esmane kirje. |
| **ID-number**<br>mshr_identificationnumber<br>*String* | Loe-kirjuta<br>Nõutav | ID-number. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe-kirjuta<br>Nõutav | ID-numbri omanikuks oleva osapoole (isiku) identifikaator. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Osapoole (isiku) kordumatu identifikaator. |
| **ID-tüübi ID**<br>mshr_identificationtypeid<br>*String* | Loe-kirjuta<br>Nõutav | ID-numbri tüüp. |
| **ID-tüübi ID väärtus**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmidentificationtypeentityid olemist mshr_hcmidentificationtypeentity entity | ID-tüübi süsteemi loodud kordumatu identifikaator. |
| **Väljastava asutuse ID**<br>mshr_issuingagencyid<br>*String* | Loe-kirjuta<br>Valikuline | ID-koodi väljastanud asutus või organisatsioon. |
| **Väljastava asutuse ID väärtus**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmissuingagencyentityid olemist mshr_hcmissuingagencyentity entity | ID-numbri väljastanud asutuse süsteemi loodud kordumatu identifikaator. |
| **Esmane väli**<br>mshr_primaryfield<br>*String* | Kirjutuskaitstud<br>Nõutav | Väli, mida kasutatakse üksusekirje esmase ID-na. Osapoole numbri, ID tüübi ID ja ID-numbri kombinatsioon. |
| **Väljastamise kuupäev**<br>mshr_issuedate<br>*Kuupäev* | Loe-kirjuta<br>Valikuline | ID-numbri väljastamise kuupäev. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]