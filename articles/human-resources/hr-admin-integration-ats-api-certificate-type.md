---
title: Tunnistuse tüüp
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Sertifikaadi tüüp.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798388"
---
# <a name="certificate-type"></a>Tunnistuse tüüp

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Sertifikaadi tüüp.

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