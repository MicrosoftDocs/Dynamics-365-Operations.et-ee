---
title: Dataverse'i tabelid
description: Microsoft Dynamics 365 Human Resources kasutab teenust Dataverse, et lubada laiendatavus ja integreerimise stsenaariumid.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8ddb74a2f0b6265c5be3c13a009211455ea862da
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893396"
---
# <a name="dataverse-tables"></a>Dataverse'i tabelid

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources kasutab teenust Dataverse, et lubada laiendatavus ja integreerimise stsenaariumid.

> [!NOTE]
> Human Resourcesi olemid vastavad Dataverse'i tabelitele. Lisateavet Dataverse'i (varem Common Data Service) ja terminoloogiavärskenduste kohta vaadake jaotisest [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Järgmised Dataverse'i tabelid on saadaval Human Resources'i olemite põhjal.

## <a name="benefit-tables"></a>Soodustustabelid

| Nimi | Tabel |
| --- | --- |
| Hüvitise arvutamise sagedus | cdm_benefitcalculationfrequency |
| Soodustuse arvutamise sagedus makseperioodil | cdm_benefitcalculationfrequencypayperiod |
| Soodustuse arvutamise määr | cdm_benefitcalculationrate |
| Soodustuse arvutamise määra üksikasjad | cdm_benefitcalculationratedetail |
| Soodustuse suvand | cdm_benefitoption |
| Soodustuse plaan | cdm_benefitplan (kohandatud väljade toeks pole lubatud) |
| Hüvitise liik | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Äriprotsessi ülesannete tabelid

| Nimi | Tabel |
| --- | --- |
| Äriprotsessi kalender | cdm_businessprocesscalendar |
| Äriprotsessi grupimäärang | cdm_businessprocessgroupassignment |
| Äriprotsessi teegi ülesandegrupp | cdm_businessprocesslibrarytaskgroup |
| Äriprotsessi etapp | cdm_businessprocessstage |
| Kontroll-loendi malli päis | cdm_businessprocesstemplateheader |
| Kontroll-loendi malli ülesanne | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Hüvitise tabelid

| Nimi | Tabel |
| --- | --- |
| Tasu fikseeritud plaan | cdm_compensationfixedplan |
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

## <a name="organization-tables"></a>Organisatsiooni tabelid

| Nimi | Tabel |
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
> Üksuste **Ametikoha tüüp** **Töötaja ametikoha määramine** ja **Töölevõtt** finantsdimensioonid pakuvad ühesuunalist integratsiooni Dataverse'iga. Finantsdimensioonide värskendusi ei saa praegu sünkroonida Dataverse'ist Human Resourcesisse. 

## <a name="leave-and-absence-tables"></a>Puhkuste ja puudumiste tabelid

| Nimi | Tabel |
| --- | --- |
| Puhkuste panga kanne | cdm_leavebanktransaction |
| Puhkuste registreerimine | cdm_leaveenrollment |
| Puhkuseplaan | cdm_leaveplan |
| Puhkusetaotlus | cdm_leaverequest |
| Puhkuse taotluse üksikasjad | cdm_leaverequestdetail |
| Puhkuse tüüp | cdm_leavetype |
| Puhkusetüübi põhjusekood | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Palgatabelid

| Nimi | Tabel |
| --- | --- |
| Palgatsükkel | cdm_paycycle |
| Makseperiood | cdm_payperiod |
| Palga tulukood | cdm_payrollearningcode |
| Pangakonto väljamakse | cdm_bankaccountdisbursement |
| Maksuregioon | cdm_taxregion |

## <a name="worker-tables"></a>Töötajatabelid

| Nimi | Tabel |
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

## <a name="worker-setup-tables"></a>Töötaja seadistamise tabelid

| Nimi | Tabel |
| --- | --- |
| Veterani olek | cdm_veteranstatus |
| Etniline päritolu | cdm_ethnicorigin |
| Põhjuse kood | cdm_reasoncode |
| Isiku ID-d väljaandev asutus | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Kompetentsitabelid

| Nimi | Tabel |
| --- | --- |
| Oskuse tüüp | cdm_skilltype |

## <a name="table-relationship-models"></a>Tabelite seose mudelid

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

[Andme integratsioonitehnoloogia valimine](hr-admin-integration-choose-technology.md)<br>
[Dataverse’i integratsiooni konfigureerimine](hr-admin-integration-common-data-service.md)<br>
[Dataverse'i virtuaalsete tabelite konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Human Resourcesi virtuaaltabelite KKK](hr-admin-virtual-entity-faq.md)<br>
[Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminoloogia uuendused](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]