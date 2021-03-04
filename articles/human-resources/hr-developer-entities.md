---
title: Common Data Service’i üksused
description: Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530002"
---
# <a name="common-data-service-entities"></a>Common Data Service’i üksused

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Human Resources kasutab teenust Common Data Service, et lubada laiendatavus ja integreerimise stsenaariumid.

Teenuse Common Data Service kohta lisateabe saamiseks vt teemat [Mis on Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

Teenuses Common Data Service on saadaval järgmised rakenduse Human Resources üksused.

## <a name="benefit-entities"></a>Soodustuse üksused

| Nimi | Üksus |
| --- | --- |
| Soodustuse arvutamise sagedus | cdm_benefitcalculationfrequency |
| Soodustuse arvutamise sagedus makseperioodil | cdm_benefitcalculationfrequencypayperiod |
| Soodustuse arvutamise määr | cdm_benefitcalculationrate |
| Soodustuse arvutamise määra üksikasjad | cdm_benefitcalculationratedetail |
| Soodustuse suvand | cdm_benefitoption |
| Soodustuse plaan | cdm_benefitplan (kohandatud väljade toeks pole lubatud) |
| Hüvitise liik | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Äriprotsessi ülesannete üksused

| Nimi | Üksus |
| --- | --- |
| Äriprotsessi kalender | cdm_businessprocesscalendar |
| Äriprotsessi grupimäärang | cdm_businessprocessgroupassignment |
| Äriprotsessi teegi ülesandegrupp | cdm_businessprocesslibrarytaskgroup |
| Äriprotsessi etapp | cdm_businessprocessstage |
| Kontroll-loendi malli päis | cdm_businessprocesstemplateheader |
| Kontroll-loendi malli ülesanne | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Hüvitise üksused

| Nimi | Üksus |
| --- | --- |
| Palga põhiplaan | cdm_compensationfixedplan |
| Kogupalga tabel | cdm_compensationgrid |
| Hüvitustase | cdm_compensationlevel |
| Palga tasumissagedus | cdm_compensationpayfrequency |
| Palga võrdluspunkti seadistus | cdm_compensationreferencepointsetup |
| Palga võrdluspunkti seadistuse rida | cdm_compensationreferencepointsetupline |
| Hüvituspiirkond | cdm_compensationregion |
| Palga struktuur | cdm_compensationstructure |
| Muutuv hüvitisplaan | cdm_compensationvariableplan |
| Muutuva hüvitisplaani tase | cdm_compensationvariableplanlevel |
| Muutuva hüvitisplaani tüüp | cdm_compensationvariableplantype |
| Põhipalga sündmus | cdm_fixedcompensationevent |
| Pensionireegel | cdm_vestingrule |
| Töötaja põhipalk | cdm_workerfixedcompensation |

## <a name="organization-entities"></a>Organisatsiooni üksused

| Nimi | Üksus |
| --- | --- |
| Osakond | cdm_department |
| Töösuhe | cdm_employment |
| Ettevõte | cdm_company |
| Amet | cdm_job |
| Tööfunktsioon | cdm_jobfunction |
| Ametikoht | cdm_jobposition |
| Ametikoha tüüp | cdm_positiontype |
| Ametikoha töötaja määramine | cdm_positionworkerassignmentmap |
| Ametikoha dimensioon | cdm_jobpositiondimension|
| Töö tüüp | cdm_jobtype |
| Keel | cdm_language |
| Pealkiri | cdm_title |

> [!NOTE]
> Üksuste **Ametikoha tüüp** **Töötaja ametikoha määramine** ja **Töölevõtt** finantsdimensioonid pakuvad ühesuunalist integratsiooni Common Data Service'iga. Finantsdimensioonide värskendusi ei saa praegu sünkroonida Common Data Service'ist Human Resourcesisse. 

## <a name="leave-and-absence-entities"></a>Puhkuste ja puudumiste üksused

| Nimi | Üksus |
| --- | --- |
| Puhkuste panga kanne | cdm_leavebanktransaction |
| Puhkuse registreerimine | cdm_leaveenrollment |
| Puhkuseplaan | cdm_leaveplan |
| Puhkusetaotlus | cdm_leaverequest |
| Puhkuse taotluse üksikasjad | cdm_leaverequestdetail |
| Puhkuse tüüp | cdm_leavetype |
| Puhkusetüübi põhjusekood | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Palgaolemid

| Nimi | Üksus |
| --- | --- |
| Palgatsükkel | cdm_paycycle |
| Makseperiood | cdm_payperiod |
| Palga tulukood | cdm_payrollearningcode |
| Pangakonto väljamakse | cdm_bankaccountdisbursement |
| Maksuregioon | cdm_taxregion |

## <a name="worker-entities"></a>Töötaja üksused

| Nimi | Üksus |
| --- | --- |
| Töötaja | cdm_worker |
| Töötaja aadress | cdm_workeraddress |
| Töötaja isikuteave | cdm_workerpersonaldetail |
| Töötaja isiku ID-number | cdm_workerpersonidentificationnumber |
| Töötaja isiku identifitseerimistüüp | cdm_workerpersonidentificationtype |
| Töökalender | cdm_workcalendar |
| Töökalendri päev | cdm_workcalendarday |
| Töökalendri püha |cdm_workcalendarholiday |
| Töökalendri puhkuse rida | cdm_workcalendarholidayline |
| Töökalendri ajaintervall | cdm_workcalendartimeinterval (kohandatud väljade toeks pole lubatud) |
| Töötaja pangakonto | cdm_workerbankaccount |

## <a name="worker-setup-entities"></a>Töötaja seadistuse üksused

| Nimi | Üksus |
| --- | --- |
| Veterani staatus | cdm_veteranstatus |
| Etniline päritolu | cdm_ethnicorigin |
| Põhjuse kood | cdm_reasoncode |
| Isikut ID väljastanud asutus | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Pädevuse üksused

| Nimi | Üksus |
| --- | --- |
| Oskuse tüüp | cdm_skilltype |

## <a name="entity-relationship-models"></a>Üksuse seose mudelid

### <a name="worker"></a>Töötaja

![Töötaja](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Töö ja ametikoht

![Töö ja ametikoht](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Soodustused

![Soodustused](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompensatsioon

![Kompensatsioon](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Lahkumine

![Lahkumine](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Töökalender

![Töökalender](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Vt ka

[Andme integratsioonitehnoloogia valimine](hr-admin-integration-choose-technology.md)</br>
[Common Data Service’i integratsiooni konfigureerimine](hr-admin-integration-common-data-service.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]