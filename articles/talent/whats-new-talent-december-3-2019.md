---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (3. detsember 2019)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528689"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Mis on Dynamics 365 Talent-is uut või mida on muudetud (3. detsember 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles artiklis kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2646. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Funktsioonihalduse tööruum

Tööruumis **Funktsioonihaldus** on toodud loend igas väljaandes saadetud funktsioonidest. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks. Lisateavet funktsioonihalduse kohta vt [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Kõik uued funktsioonid jäävad vähemalt 30 päevaks eelvaatesse ja tavaliselt 30–60 päevaks. Peamised funktsioonid on tavaliselt saadaval eelvaate perioodile järgneva iga aasta oktoobris ja aprillis. Kohe kui näete tööruumis **Funktsioonihaldus** uusi võimalusi, saate need sisse lülitada. Mõned funktsioonid võivad olla vaikimisi sisse lülitatud.
 
Mõnikord on lahutamatu funktsioon vaikimisi sisse lülitatud ja seda ei saa välja lülitada (nt tööruum **Funktsioonihaldus**).
 
Kui funktsioon on üldsusele saadaval, võib selle tootmiskeskkonnas sisse või välja lülitada. Tööruum **Funktsioonihaldus** näitab, millal muutub eelvaate funktsioon kohustuslikuks. See kuupäev on tavaliselt 1. oktoobril või 1. aprillil, et ühitada poolaasta väljalaskeplaanidega. Kohustuslikke funktsioone välja lülitada ei saa. Kuni see muutub kohustuslikuks, saate funktsiooni kõikides keskkondades sisse ja välja lülitada.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Pakett-töö ajaloo puhastamise automaatse plaanimise lisamine (332528)

Selle muudatusega töötab suvand **Pakett-töö ajalugu** igal ööl ja eemaldab pakett-töö ajaloo üksused, mis on vanemad kui 30 päeva.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent ei vasta töötaja tegevusele, kui ID-numbri pikkus ei vasta identifitseerimistüübile (390971)

See versioon parandab probleemi, mis kerkib esile, kui ID-numbri pikkus ei vasta identifitseerimistüübi määratlusele. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Põhipalk ei värskenda taset ametikoha üksikasjade muudatustega (348085)

Selle nädala väljaandes määratleb suvand **Kompensatsiooni alguskuupäev** ametikohaga seotud töö uue töötaja põhipalga kirje loomise ajahetkel.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Töötajate, töövõtjate ja peatöövõtjate loendid kuvavad suvandi Töötaja tüüpi kui Mõlemad, kuigi peaks olema ainult Töötaja või Peatöövõtja (384473)

See muudatus peegeldab sisestatud töötaja tüüpi täpselt (peatöövõtja või töötaja).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Uute värbamistoimingute meiliteavitused ei sisalda turbereeglite tõttu nime teavet (383402)

See muudatus parandab töövoo kohatäidetes ees- või perekonnanime väljadel kuvatava teabe, kui lubatud on täiustatud turve.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Süsteem võimaldab samale päevale kaks täispäeva puhkuse taotlust (379284)

Selle muudatusega ei saa te väljastada kahte puhkusetaotlust samale päevale. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Aadressimuudatuste loend tuleks sortida suvandi Kehtivuse algus järgi (352798)

Selle muudatusega sorditakse aadressimuudatuste loend nüüd suvandi **Kehtivuse algus** järgi.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Puhkusetaotlused peaksid võimaldama Talentist teenuse Common Data Service kustutamisi (376999)

Selle muudatusega saab mustandina ja tühistatud puhkusetaotlusi teenusest Common Data Service kustutada ja eemaldada seejärel Talentist.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Tulukoodide kustutamine on lubatud, kui sama tulukood on töötajale määratud (371792)

Selles väljalaskes peate enne tulukoodi süsteemist kustutamist esmalt tulukoodi töötvõtjalt eemaldama.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Kahe kinnitamisetapiga puhkuse ja puudumise töövoo lõpetamine ebaõnnestub (391116)

Selle muudatusega jätkub puhkuse ja puudumise töövoog läbi kõikide etappide, kui taotluse jaoks on konfigureeritud rohkem kui üks kinnitusjärk.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Väljaandmise kuupäeva ei sünkroonita Common Data Service’iga Talentis värskendamisel või sisestamisel (397361)

See muudatus parandab probleemi, mille puhul kirjete **Isiku ID** väljaandmise kuupäeva ei sünkroonitud Talentist Common Data Service’isse

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Ametikohale juhi määramisel väljastati hierarhia ringviite tõrge (386659)

See muudatus parandab ainulaadse stsenaariumi, kus ametikohale uue juhi määramisel kuvatakse ringviite tõrge.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service’i üksused, mis nüüd toetavad kohandatud välju

Järgmised Common Data Service’i üksused toetavad nüüd kohandatud välju:

| Nimi | Üksus |
| --- | --- |
| Pangakonto väljamakse | cdm_bankaccountdisbursement |
| Soodustuse arvutamise sagedus | cdm_benefitcalculationfrequency |
| Soodustuse arvutamise sagedus makseperioodil | cdm_benefitcalculationfrequencypayperiod |
| Soodustuse arvutamise määr | cdm_benefitcalculationrate |
| Soodustuse arvutamise määra üksikasjad | cdm_benefitcalculationratedetail |
| Soodustuse suvand | cdm_benefitoption |
| Soodustuse plaan | cdm_benefitplan (kohandatud väljade toeks pole lubatud) |
| Hüvitise liik | cdm_benefittype |
| Äriprotsessi kalender | cdm_businessprocesscalendar |
| Äriprotsessi grupimäärang | cdm_businessprocessgroupassignment |
| Äriprotsessi teegi ülesandegrupp | cdm_businessprocesslibrarytaskgroup |
| Äriprotsessi etapp | cdm_businessprocessstage |
| Kontroll-loendi malli päis | cdm_businessprocesstemplateheader |
| Kontroll-loendi malli ülesanne | cdm_businessprocesstemplatetask |
| Ettevõte | cdm_company |
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
| Osakond | cdm_department |
| Töösuhe | cdm_employment |
| Etniline päritolu | cdm_ethnicorigin |
| Põhipalga sündmus | cdm_fixedcompensationevent |
| Amet | cdm_job |
| Tööfunktsioon | cdm_jobfunction |
| Ametikoht | cdm_jobposition |
| Töö tüüp | cdm_jobtype |
| Keel | cdm_language |
| Puhkuse pangakanne | cdm_leavebanktransaction |
| Puhkuse registreerimine | cdm_leaveenrollment |
| Puhkuseplaan | cdm_leaveplan |
| Puhkusetaotlus | cdm_leaverequest |
| Puhkuse taotluse üksikasjad | cdm_leaverequestdetail |
| Puhkuse tüüp | cdm_leavetype |
| Puhkusetüübi põhjusekood | cdm_leavetypereasoncode |
| Palgatsükkel | cdm_paycycle |
| Makseperiood | cdm_payperiod |
| Palga tulukood | cdm_payrollearningcode |
| Isikut ID väljastanud asutus | cdm_personidentificationissuingagency |
| Ametikoha tüüp | cdm_positiontype |
| Ametikoha töötaja määramine | cdm_positionworkerassignmentmap |
| Põhjuse kood | cdm_reasoncode |
| Oskuse tüüp | cdm_skilltype |
| Maksuregioon | cdm_taxregion |
| Pensionireegel | cdm_vestingrule |
| Veterani staatus | cdm_veteranstatus |
| Töökalender | cdm_workcalendar |
| Töökalendri päev | cdm_workcalendarday |
| Töökalendri püha |cdm_workcalendarholiday |
| Töökalendri puhkuse rida | cdm_workcalendarholidayline |
| Töökalendri ajaintervall | cdm_workcalendartimeinterval (kohandatud väljade toeks pole lubatud) |
| Töötaja | cdm_worker |
| Töötaja aadress | cdm_workeraddress |
| Töötaja pangakonto | cdm_workerbankaccount |
| Töötaja põhipalk | cdm_workerfixedcompensation |
| Töötaja isikuteave | cdm_workerpersonaldetail |
| Töötaja isiku ID-number | cdm_workerpersonidentificationnumber |
| Töötaja isiku identifitseerimistüüp | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Eelvaates

Eelvaatefunktsioonid on saadaval ainult keskkondades **Liivakast**.

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.
