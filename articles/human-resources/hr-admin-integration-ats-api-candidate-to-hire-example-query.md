---
title: Palgatava kandidaadi päringu näidis
description: See teema annab näidispäringu Palgatava kandidaadi olemi kohta rakenduses Dynamics 365 Human Resources.
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
ms.openlocfilehash: d2fc08586914fd3815b0da062f24d83ac550302f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467621"
---
# <a name="example-query-for-candidate-to-hire"></a>Palgatava kandidaadi päringu näidis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See teema annab näidispäringu Palgatava kandidaadi olemi kohta rakenduses Dynamics 365 Human Resources.

See teema pakub näidet, mis demonstreerib, kuidas kasutada  *süvasisestusi*, et luua kõik uue kandidaadi kirje üksikasjad üheainsa API-toiminguga. Lisateavet süvasisestuste kohta leiate jaotisest [Seotud olemikirjete loomine ühe toiminguga](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Olem **mshr_hcmcandidatetohireentity** on kordumatu tänu oma seosele olemiga **mshr_dirpersonentity**. Paljud atribuudid olemil **mshr_hcmcandidatetohireentity** (näiteks **mshr_firstname**, **mshr_lastname** ja **mshr_birthdate**) on tuletatud kirjest **mshr_dirpersonentity**. Kui sisestate uue kandidaadi kirje olemisse **mshr_hcmcandidatetohireentity** ilma süvasisestusteta, saate määratleda nende atribuutide väärtusi otse kirjel **mshr_hcmcandidatetohireentity**. Seotud kirje **mshr_dirpersonentity** kirje luuakse vaikimisi atribuutide jaoks määratletud väärtustega. Seejärel saate eraldi API-kutsetena luua mis tahes teisi seotud üksuse kirjeid (nt oskused või haridus).

Kui te soovite siiski kasutada süvasisestust kõigi seotud olemite loomiseks ühe toiminguga, tuleb olemile **mshr_dirpersonentity** omased atribuudid olema määratletud sellel toimingu pesastatud tasemel.

See näide näitab, kuidas saate luua kandidaadikirjet, seotud isikukirjet ning isiku oskusi ja haridust kolmel pesastatud tasemel, kasutades süvasisestusi ühe API toiminguna.

> [!NOTE]
> Näide ei sisalda kõigi API-üksuste kõiki atribuute. See on demonstreerimise otstarbel lihtsustatud.

**Taotlus**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Vastus**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]