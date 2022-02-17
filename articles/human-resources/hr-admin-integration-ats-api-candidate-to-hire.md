---
title: Palgatav kandidaat
description: Selles teemas kirjeldatakse olemit Palgatav kandidaat rakenduse Dynamics 365 Human Resources jaoks.
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
ms.openlocfilehash: ef76a84c8a4edd1d209b976fc4c65a16cd020e96
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8067900"
---
# <a name="candidate-to-hire"></a>Palgatav kandidaat


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse olemit Palgatav kandidaat rakenduse Dynamics 365 Human Resources jaoks.

Füüsiline nimi: mshr_hcmcandidatetohireentity

## <a name="description"></a>Kirjeldus

Olem annab kandidaatide üksikasju, mida kasutatakse töötaja loomiseks rakenduses Dynamics 365 Human Resources. Seda kasutatakse kõikide kandidaadikirjete lugemiseks ja sisemiste ning väliste kandidaadikirjete loomiseks, võimaldades teil luua uuele kandidaadile isikuandmed.

Kui loote välise kandidaadi kirje, kellest saab süsteemis uus isikukirje, ei tohi te määratleda osapoole (isiku) numbrit, te sisestate uue kandidaadi kirje. Uue isiku olemi kirje luuakse uue kandidaadi kirjega.

Sisemise kandidaadi kirje (kandidaat ametikohale, kellel on ettevõttes töötajakirje juba olemas) loomisel määrake selle kirje osapool (isik), mis on isikule juba atribuudi mshr_partynumber jaoks kandidaadi kirjel olemas, mitte ärge määratlege isikuandmeid (nagu nimi, sugu või sünnipäev), mida kasutatakse uue isiku kirje loomiseks.

## <a name="json-representation"></a>JSON-i esindus

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Atribuudid

| Atribuut<br>**Füüsiline nimi**<br>**_Tüüp_** | Kasuta | Kirjeldus |
| --- | --- | --- |
| **Palgatava kandidaadi olemi ID**<br>mshr_hcmcandidatetohireentityid<br>GUID | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Olemi kirje süsteemi loodud kordumatu identifikaator. |
| **Kandidaadi ID**<br>mshr_candidateid<br>String | Kirjutuskaitstud<br>Nõutav<br>Süsteemi loodud | Olemi kordumatu identifikaator. |
| **Osapoole number**<br>mshr_partynumber<br>String | Kirjutuskaitstud<br>Nõutav | Kandidaadi isikukirje osapoole (isiku) number. |
| **Isiku ID väärtus**<br>_mshr_fk_person_id_value<br>GUID | Kirjutuskaitstud<br>Nõutav<br>Võõrvõti: mshr_dirpersonentityid olemile mshr_direpersonentity | Süsteemi loodud kandidaadi osapoole (isiku) kirje kordumatu identifikaator. |
| **Osapoole tüüp**<br>mshr_partytype<br>Suvandikomplekt mshr_dirpartytype | Kirjutuskaitstud<br>Nõutav | Kirje osapoole tüüp, nagu on määratletud suvandikomplektis mshr_dirpartytype. Selle üksuse puhul on tüübiks alati "Isik". |
| **Värbamistaotluse ID**<br>mshr_recruitingrequestid<br>String | Ühekordne kirjutamine<br>Valikuline | Viitab värbamistaotlusele, mida see kandidaat täidab. |
| **Värbamistaotluse ID väärtus**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Loe/kirjuta<br>Valikuline<br>Võõrvõti: mshr_hcmrecruitingrequestentityid olemist mshr_hcmrecruitingrequestentity | Selle värbamistaotluse süsteemi loodud identifitseerija, mida kandidaat täidab. |
| **Ametikoha ID**<br>mshr_positionid<br>String | Loe/kirjuta<br>Valikuline | Selle ametikoha ID, mille jaoks kandidaati kaalutakse. |
| **Positsiooni ID väärtus**<br>_mshr_fk_position_if_value<br>GUID | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmpositionv2entityid olemist mshr_hcmpositionv2entity | Süsteemi loodud identifikaator sellele ametikohale, mille jaoks kandidaati kaalutakse. |
| **Eesnimi**<br>mshr_firstname<br>String | Loe/kirjuta<br>Nõutav | Kandidaadi eesnimi. |
| **Teine eesnimi**<br>mshr_middlename<br>String | Loe/kirjuta<br>Valikuline | Kandidaadi teine eesnimi. |
| **Perekonnanime eesliide**<br>mshr_lastnameprefix<br>String | Loe/kirjuta<br>Valikuline | Kandidaadi perekonnanime eesliide. |
| **Perekonnanimi**<br>mshr_lastname<br>String | Loe/kirjuta<br>Valikuline | Kandidaadi perekonnanimi. |
| **Sugu**<br>mshr_gender<br>suvandikomplekt mshr_hcmpersongender | Loe/kirjuta<br>Valikuline | Kandidaadi sugu. |
| **Sünnikuupäev**<br>mshr_birthdate<br>Kuupäev ja kellaaeg | Loe/kirjuta<br>Valikuline | Kandidaadi sünnikuupäev. |
| **Kodakondsuse riigikood**<br>mshr_citizenshipcountrycode<br>String | Loe/kirjuta<br>Valikuline | Määrab riigi, kus kandidaadil on kodakondsus. Kehtivad riigikoodid on olemis mshr_logisticaddresscountryregionentity. |
| **Veterani staatuse ID**<br>mshr_veteranstatusid<br>String | Loe/kirjuta<br>Valikuline | Näitab kandidaadi veteranistaatust. |
| **Veterani staatuse ID väärtus**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmveteranstatusentityid olemist mshr_hcmveteranstatusentity | Süsteemi loodud kordumatu identifikaator veterani staatuse üksuse kirjele. |
| **Sõjaväeteenistuse alguskuupäev**<br>mshr_militaryservicestartdate<br>Kuupäev ja kellaaeg | Loe/kirjuta<br>Valikuline | Kandidaadi sõjaväeteenistuse alguskuupäev. |
| **Sõjaväeteenistuse lõpukuupäev**<br>mshr_militaryserviceenddate<br>Kuupäev ja kellaaeg | Loe/kirjuta<br>Valikuline | Kandidaadi sõjaväeteenistuse lõpukuupäev. |
| **On puudega veteran**<br>mshr_isdisabledveteran<br>suvandikomplekt mshr_noyes | Loe/kirjuta<br>Valikuline | Näitab, kas kandidaadil on puudega veterani olek. |
| **Kättesaadavuse kuupäev**<br>mshr_availabilitydate<br>Kuupäev ja kellaaeg | Loe/kirjuta<br>Valikuline | Varaseim kuupäev, mil kandidaat oleks tööle saadaval. |
| **Nõustub ümberpaigutamisega**<br>mshr_iswillingtorelocate<br>suvandikomplekt mshr_noyes | Loe/kirjuta<br>Valikuline | Näitab, kas kandidaat on nõus ametikoha jaoks kolima. |
| **Kommentaarid**<br>mshr_comments<br>String | Loe/kirjuta<br>Valikuline | Värbaja või värbamishalduri kasutatavad kommentaarid. |
| **Rakenduste integreerimise server**<br>mshr_applcantintegrationresult<br>suvandikomplekt mshr_applicantintegrationresult | Loe/kirjuta<br>Nõutav | Kandidaadi olek integratsiooniga seotud palkamisprotsessis. |
| **Ära Palka põhjuse koodi ID**<br>mshr_donothirereasoncodeid<br>String | Loe/kirjuta<br>Valikuline | Põhjusekood antakse valikuliselt siis, kui olek (taotluse integratsiooni tulemus) määratakse väärtusele "Ei palgatud". |
| **Põhjusekoodi ID väärtus**<br>_mshr_fk_reasoncode_id_value<br>GUID | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: mshr_hcmreasoncodeentityid olemist mshr_hcmreasoncodeentity | Süsteemi loodud **Ära palka** põhjuse koodi kordumatu identifikaator. |
| **Andmeala ID**<br>mshr_dataareaid<br>String | Loe/kirjuta<br>Valikuline |  Määratleb juriidilise isiku (ettevõtte). |
| **Andmeala ID väärtus**<br>_mshr_dataareaid_id_value<br>GUID | Kirjutuskaitstud<br>Valikuline<br>Võõrvõti: cdm_companyid olemist cdm_company | Süsteemi loodud GUID-väärtus, mis identifitseerib juriidilise isiku (ettevõtte). |

## <a name="see-also"></a>Vt ka

[Kandidaadi jälgimissüsteemi integreerimise API tutvustus](hr-admin-integration-ats-api-introduction.md)<br>
[Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
