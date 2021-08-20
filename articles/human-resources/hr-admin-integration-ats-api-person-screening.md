---
title: Isiku skriining
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.
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
ms.openlocfilehash: 241b9888624d95bf37a82b6e9b807509818387d2d4f4e5eac67bd67afdaed735
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782775"
---
# <a name="person-screening"></a>Isiku skriining

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Isiku skriinig.

Füüsiline nimi: mshr_hcmpersonscreeningentity

## <a name="description"></a>Kirjeldus

See üksus kirjeldab skriininguid, mille kandidaat on läbinud või peab tööle võtmiseks läbima.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Isiku skriiningu olemi ID**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Isiku skriiningu kirje kordumatu peamine identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>*String* | Loe/kirjuta<br>Nõutav | Kandidaadiga seotud osapoole (isiku) number. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_dirpersonentity | Süsteemi loodud osapoole (isiku) olemi kirje kordumatu identifikaator. |
| **Skriiningu tüübi ID**<br>mshr_screeningtypeid<br>*String* | Loe/kirjuta<br>Nõutav<br>Võõrvõti: screeningtype | Human Resourcesis määratletud skriiningu tüübi identifikaator. |
| **Skriiningu tüübi ID väärtus**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_hcmscreeningtypeentityid olemist mshr_hcmscreeningtypeentity | Seostatud üksuse skriiningu tüübi kirje süsteemi loodud kordumatu identifikaator. |
| **Nõutav kuupäevaks**<br>mshr_requiredby<br>*Datetime* | Loe/kirjuta<br>Valikuline | Skriiningu nõutav lõpule viismise kuupäev. |
| **Olek**<br>mshr_status<br>*suvandikomplekt mshr_hcmcompletionstatus*<br>Loe/kirjuta<br>Nõutav | Esitab skriiningu jaoks kandidaadi oleku. |
| **Lõpule viimise kuupäev**<br>mshr_completeddate<br>*Datetime* | Loe/kirjuta<br>Valikuline | Skriiningu lõpule viimise kuupäev. |
| **Märkmed**<br>mshr_note<br>*String* | Loe/kirjuta<br>Valikuline | Märkused värbamishalduritele ja värbajatele kasutamiseks. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]