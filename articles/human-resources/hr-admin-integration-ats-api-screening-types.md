---
title: Skriiningu tüübid
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Skriiningu tüübid.
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
ms.openlocfilehash: d3a45d802ab6b574338a09e77d432357cb9df507
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465914"
---
# <a name="screening-types"></a>Skriiningu tüübid

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources olemit Skriiningu tüübid.

Füüsiline nimi: mshr_hcmscreeningtypeentity

## <a name="description"></a>Kirjeldus

See üksus kirjeldab skriiningu tüüpe, mille ettevõte on seadistanud värbamiseelseks ja jooksvaks töötajate skriininguks.

## <a name="json-representation"></a>JSON-i esindus

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Skriiningu tüübi olemi ID**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Skriiningu tüübi kirje kordumatu peamine identifikaator. |
| **Skriiningu tüübi ID**<br>mshr_screeningtypeid<br>*String* | Loe/kirjuta<br>Nõutav | Skriiningu tüübi kasutaja määratletud kordumatu identifikaator. |
| **Kirjeldus**<br>mshr_description<br>*String* | Loe/kirjuta<br>Nõutav | Skriiningu tüübi kirjeldus. |
| **Sageduse üksus**<br>mshr_frequencyunit<br>*suvandikomplekt mshr_hcmfrequencyunit* | Loe/kirjuta<br>Nõutav | Kirjeldab sagedust, millal skriining tuleb määratud isiku jaoks läbi viia. |
| **Loo alates**<br>mshr_generatefrom<br>*suvandikomplekt mshr_hcmfrequencygeneratefrom* | Loe-kirjuta<br>Nõutav | Kui sageduse väärtus on muu kui "Ainult üks kord", määrab funktsiooni GenerateFrom väärtus kuupäeva, millest arvutada järgmine skriiningu sündmus. |
| **Sageduse intervall**<br>mshr_frequencyinterval<br>*Täisarv* | Loe-kirjuta<br>Nõutav | Kui sageduse väärtus on muu kui "ainult üks kord", peate iga skriiningu sündmuse vaheliste ajaühikute jaoks intervalli määrama. |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]