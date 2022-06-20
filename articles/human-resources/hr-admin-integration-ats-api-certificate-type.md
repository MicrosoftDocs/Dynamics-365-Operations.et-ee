---
title: Tunnistuse tüüp
description: See artikkel kirjeldab serditüübi üksust üksuse <a0/& jaoks Dynamics 365 Human Resources.
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
ms.openlocfilehash: bfe7f06176098a504f8d2ad1c1431a6f60fe059c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886185"
---
# <a name="certificate-type"></a>Tunnistuse tüüp


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab serditüübi üksust üksuse <a0/& jaoks Dynamics 365 Human Resources.

Füüsiline nimi: mshr_hcmcertificatetypeentity

## <a name="description"></a>Kirjeldus

See üksus määratleb Human Resourcesis seadistatud kutsetunnistuste tüüpide loendi. Üksus pole juriidilisele isikule (ettevõttele) omane.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Serdi tüübi olemi ID**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav 
Süsteemi loodud | Sertifikaadi tüübi kordumatu peamine identifikaator. |
| **Sertifikaadi tüüp**<br>mshr_certificatetype<br>*String* | Loe/kirjuta<br>Nõutav | Sertifikaadi tüübi kordumatu kasutaja loetav identifikaator. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Serfifikaadi tüübi kirjeldus. |
| **Nõuab uuendamist**<br>mshr_requirerenewal<br>*suvandikomplekt mshr_noyes* | Loe/kirjuta<br>Valikuline | Näitab, kas serdi uuendamine on nõutav. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
