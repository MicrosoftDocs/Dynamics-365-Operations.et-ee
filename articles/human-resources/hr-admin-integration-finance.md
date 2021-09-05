---
title: Integratsiooni konfigureerimine Finance’iga
description: Selles teemas kirjeldatakse maksuandmete integreerimist rakenduse Dynamics 365 Human Resources ja teenuse Dynamics 365 Finance vahel.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba984d26c5c0b1376c0ad85e5c0665da004a46a5
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414684"
---
# <a name="configure-integration-with-finance"></a>Integratsiooni konfigureerimine Finance’iga

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Human Resourcesi integreerimisel Dynamics 365 Finance'iga saate kasutada rakendusest Human Resources rakendusse Finance malli [Andmeintegraator](/powerapps/administrator/data-integrator). Rakendusest Human Resources rakendusse Finance mall lubab tööde, ametikohtade ja töötajate andmevoo. Mall lubab andmevoo rakendusest Human Resources rakendusse Finance, kuid ei luba andmevoogu Finance'ist Human Resourcesisse.

![Rakenduse Human Resources integratioonivoog.](./media/hr-admin-integration-finance-flow.png)

Rakendusest Human Resources rakendusse Finance lahendus pakub järgmist tüüpi andmete sünkroonimist.

- Hallake inimressursse ja sünkroonige neid rakendusest Human Resources rakendusse Finance
- Hallake rakenduse Human Resources ametikohti ja nende määramisi ning sünkroonige neid rakendusest Human Resources rakendusse Finance
- Hallake tööhõivet rakenduses Human Resources ja sünkroonige neid rakendusest Human Resources rakendusse Finance
- Hallake rakenduse Human Resources töötajaid ja töötajate aadresse ning sünkroonige neid rakendusest Human Resources rakendusse Finance

## <a name="system-requirements-for-human-resources"></a>Rakenduse Human Resources süsteeminõuded

Integratsioonilahenduse jaoks on vaja rakenduste Human Resources ja Finance järgmisi versioone. 

- Dynamics 365 Human Resources kuupäeval Dataverse
- Dynamics 365 Finance’i versioon 7.2 või uuem

## <a name="template-and-tasks"></a>Mall ja ülesanded

Rakendusest Human Resources rakendusse Finance malli juurde pääsemine.

1. Avage [Power Appsi halduskeskus](https://admin.powerapps.com/). 

2. Valige **Projektid** ja seejärel valige paremas ülanurgas **Uus projekt**. Looge iga juriidilise isiku jaoks uus projekt, mida soovite Finance’i integreerida.

3. Rakendusest Human Resources rakendusse Finance andmete sünkroonimiseks valige **Human Resources (Human Resources Dataverse rakendusse Finance)**.

Mall kasutab järgmisi ülesandeid kirjete sünkroonimiseks rakendusest Human Resources rakendusse Finance.

- **Tööfunktsioonidest tööfunktsioonide kompensatsioonile**
- **Osakondadest tootmisüksusele**
- **Töötüüpidest töötüübi kompensatsioonile**
- **Töödest töökohtadele**
- **Töödest töö üksikasjadele**
- **Positsiooni tüüpidest positsiooni tüübile**
- **Ametikohtadest peamise ametikoha jaoks**
- **Ametikohast ametikoha üksikasjadele**
- **Ametikohast ametikoha kestustele**
- **Ametikohast ametikoha hierarhiatele**
- **Töötajatelt töötajale**
- **Tööhõivetest tööhõivele**
- **Tööhõivetest tööhõive üksikasjadele**
- **Töötaja ametikoha määramisest töötaja ametikoha määrangutele**
- **Töötaja aadressitest töötaja postiaadressi v2-le**

## <a name="template-mappings"></a>Malli vastendamised

Järgmistes mallivastenduste tabelites sisaldab ülesande nimi igas rakenduses kasutatavaid üksuseid. Allikas (Human Resources) on vasakul ja sihtkoht (Finance) on paremal.

### <a name="job-functions-to-compensation-job-function"></a>Tööfunktsioonidest tööfunktsioonide kompensatsioonile

| Dataverse'i tabel (allikas) | Finance'i üksus (sihtkoht) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job Funktsiooni nimi)  | TÖÖ FUNKTSIOONI ID (TÖÖ FUNKTSIOONI ID)            |
| cdm_description (cdm_description) | KIRJELDUS (KIRJELDUS)                 |

### <a name="departments-to-operating-unit"></a>Osakondadest tootmisüksusele

| Dataverse'i tabel (allikas)           | Finance'i üksus (sihtkoht) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NIMI (NIMI)                                 |
| cdm_departmentnumber (cdm_departmentnumber) | TÖÖÜKSUSE NUMBER (TÖÖÜKSUSE NUMBER) |
|                                               | TÖÖÜKSUSE TÜÜP (TÖÖÜKSUSE TÜÜP)     |
| cdm_description (cdm_description)           | NIME PSEUDONÜÜM (NIME PSEUDONÜÜM)                     |

### <a name="job-types-to-compensation-job-type"></a>Töötüüpidest töötüübi kompensatsioonile

| Dataverse'i tabel (allikas)   | Finance'i üksus (sihtkoht) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | TÖÖTÜÜBI ID (TÖÖTÜÜBI ID)                     |
| cdm_description (cdm_description)   | KIRJELDUS (KIRJELDUS)                 |
| cdm_exemptstatus (cdm_exemptstatus) | MAKSUVABASTUSE OLEK (MAKSUVABASTUSE OLEK)               |

### <a name="jobs-to-jobs"></a>Töödest töökohtadele

| Dataverse'i tabel (allikas)                           | Finance'i üksus (sihtkoht)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | TÖÖ ID (TÖÖ ID)                                         |
| cdm_maximumnumberofpositions (cdm_maximumnumberofpositions) | AMETIKOHTADE MAX ARV (AMETIKOHTADE MAX ARV) |
| cdm_allowedunlimitedpositions (cdm_allowunlimitedpositions) | LUBA PIIRAMATULT AMETIKOHTI (LUBA PIIRAMATULT AMETIKOHTI)   |
| cdm_description (cdm_description)                           | KIRJELDUS (KIRJELDUS)                           |
| cdm_jobdescription (cdm_jobdescription)                     | TÖÖ KIRJELDUS (TÖÖ KIRJELDUSED)                    |

### <a name="jobs-to-job-detail"></a>Töödest töö üksikasjadele

| Dataverse'i tabel (allikas)                             | Finance'i üksus (sihtkoht) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | TÖÖ ID (TÖÖ ID)                               |
| cdm_jobtypeid.cdm_name (Töö tüüp (töö tüübi nimi))             | TÖÖTÜÜBI ID (TÖÖTÜÜBI ID)                     |
| cdm_jobfunctionid.cdm_name (Tööfunktsioon (tööfunktsiooni nimi)) | FUNKTSIOONI ID (FUNKTSIOONI ID)                   |
| cdm_validfrom (Kehtiv alates)                                    | KEHTIV ALATES (KEHTIV ALATES)                     |
| cdm_validto (Kehtib kuni)                                        | KEHTIB KUNI (KEHTIB KUNI)                           |
| cdm_defaultfulltimeequivalent (Täisaja vaikeekvivalent)   | TÄISAJA VAIKEEKVIVALENT (TÄISAJA VAIKEEKVIVALENT)   |

### <a name="position-types-to-position-type"></a>Positsiooni tüüpidest positsiooni tüübile

| Dataverse'i tabel (allikas)       | Finance'i üksus (sihtkoht) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | AMETIKOHA TÜÜBI ID (AMETIKOHA TÜÜBI ID)           |
| cdm_description (cdm_description)       | KIRJELDUS (KIRJELDUS)                 |
| cdm_classification (cdm_classification) | KLASSIFIKATSIOON (KLASSIFIKATSIOON)           |

### <a name="job-positions-to-base-position"></a>Ametikohtadest peamise ametikoha jaoks

| Dataverse'i tabel (allikas)           | Finance'i üksus (sihtkoht) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Ametikoha number) | AMETIKOHA ID (AMETIKOHA ID)                      |

### <a name="job-positions-to-position-details"></a>Ametikohast ametikoha üksikasjadele

| Dataverse'i tabel (allikas)              | Finance'i üksus (sihtkoht)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber (Ametikoha number)                            | AMETIKOHA ID (AMETIKOHA ID)                             |
| cdm_jobid.cdm_name (Töö (nimi))                                        | TÖÖ ID (TÖÖ ID)                                    |
| cdm_description (cdm_description)                                        | KIRJELDUS (KIRJELDUS)                       |
| cdm_departmentid.cdm_departmentnumber (Osakond (osakonna number)) | OSAKONNA NUMBER (OSAKONNA NUMBER)             |
| cdm_positiontypeid.cdm_name (Ametikoha tüüp (nimi))                     | AMETIKOHA TÜÜBI ID (AMETIKOHA TÜÜBI ID)                 |
| cdm_avaialableforassignment (Määramise jaoks saadaval)                 | MÄÄRAMISEKS SAADAVAL (MÄÄRAMISEKS SAADAVAL) |
| cdm_validfrom (Kehtiv alates)                                            | KEHTIV ALATES (KEHTIV ALATES)                           |
| cdm_validto (Kehtib kuni)                                                 | KEHTIB KUNI (KEHTIB KUNI)                               |
| cdm_fulltimeequivalent (Täisaja ekvivalent)                           | TÄISAJA VAIKEEKVIVALENT (TÄISAJA VAIKEEKVIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Ametikohast ametikoha kestustele

| Dataverse'i tabel (allikas)             | Finance'i üksus (sihtkoht) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Ametikoha number)   | AMETIKOHA ID (AMETIKOHA ID)                      |
| Arvutatud aktiveerimine (arvutatud aktiveerimine) | KEHTIV ALATES (KEHTIV ALATES)                        |
| Arvutatud pensionile jäämine (arvutatud pensionile jäämine) | KEHTIB KUNI (KEHTIB KUNI)                         |

### <a name="job-positions-to-position-hierarchies"></a>Ametikohast ametikoha hierarhiatele

| Dataverse'i tabel (allikas)        | Finance'i üksus (sihtkoht) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber (Ametikoha number)                                                 | AMETIKOHA ID (AMETIKOHA ID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber (cdm_parentjobpositionid.cdmjobpositionnumber) | ÜLEMAMETIKOHA ID (ÜLEMAMETIKOHA ID)         |
| cdm_validfrom (Kehtiv alates)                                                                  | KEHTIV ALATES (KEHTIV ALATES)                     |
| cdm_validto (Kehtib kuni)                                                                      | KEHTIB KUNI (KEHTIB KUNI)                           |
| HIERARHIATÜÜBI NIMI (HIERARHIATÜÜBI NIMI)                                                       | HIERARHIATÜÜBI NIMI (HIERARHIATÜÜBI NIMI)     |


### <a name="workers-to-worker"></a>Töötajatelt töötajale
| Dataverse'i tabel (allikas)           | Finance'i üksus (sihtkoht)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate (cdm_birthdate)               | SÜNNIKUUPÄEV (SÜNNIKUUPÄEV)                           |
| cdm_gender (cdm_gender)                     | SUGU (SUGU)                                   |
| cdm_primaryaddress (cdm_primaryaddress)     | ESMASE KONTAKTI MEILIAADRESS (ESMASE KONTAKTI MEILIAADRESS)      |
| cdm_primarytelephone (cdm_primarytelephone) | ESMASE KONTAKTI TELEFONINUMBER (ESMASE KONTAKTI TELEFONINUMBER)       |
| cdm_facebookidentity (cdm_facebookidentity) | ESMASE KONTAKTI FACEBOOK (ESMASE KONTAKTI FACEBOOK) |
| cdm_twitteridentity (cdm_twitteridentity)   | ESMASE KONTAKTI TWITTER (ESMASE KONTAKTI TWITTER)   |
| cdm_linkedinIdentity (cdm_linkedinIdentity) | ESMASE KONTAKTI LINKEDIN (ESMASE KONTAKTI LINKEDIN) |
| cdm_websiteurl (cdm_websiteurl)             | ESMASE KONTAKTI URL (ESMASE KONTAKTI URL)           |
| cdm_firstname (cdm_firstname)               | EESNIMI (EESNIMI)                           |
| cdm_middlename (cdm_middlename)             | KESKMINE NIMI (KESKMINE NIMI)                         |
| cdm_lastname (cdm_lastname)                 | PEREKONNANIMI (PEREKONNANIMI)                               |
| cdm_workernumber (cdm_workernumber)         | PERSONALI NUMBER (PERSONALI NUMBER)               |
| cdm_type (cdm_type)                           | TÖÖ TÜÜP (TÖÖ TÜÜP)                         |
| cdm_state (cdm_state)                       | TÖÖ OLEK (TÖÖ OLEK)                       |

### <a name="employments-to-employment"></a>Tööhõivetest tööhõivele

| Dataverse'i tabel (allikas)                             | Finance'i üksus (sihtkoht) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate (cdm_employmentstartdate)             | TÖÖHÕIVE ALGUSKUUPÄEV (TÖÖHÕIVE ALGUSKUUPÄEV) |
| cdm_employmentenddate (cdm_employmentenddate)                 | TÖÖHÕIVE LÕPPKUUPÄEV (TÖÖHÕIVE LÕPPKUUPÄEV)     |
| cdm_workertype (cdm_workertype)                               | TÖÖTAJA TÜÜP (TÖÖTAJA TÜÜP)                   |
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONALI NUMBER (PERSONALI NUMBER)         |
| cdm_companyid.cdm_companycode (cdm_companyid.cdm_companycode) | JURIIDILISE ISIKU ID (JURIIDILISE ISIKU ID)             |

### <a name="employments-to-employment-detail"></a>Tööhõivetest tööhõive üksikasjadele

| Dataverse'i tabel (allikas)                             | Finance'i üksus (sihtkoht)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate (cdm_employmentstartdate)             | TÖÖHÕIVE ALGUSKUUPÄEV (TÖÖHÕIVE ALGUSKUUPÄEV)   |
| cdm_employmentenddate (cdm_employmentenddate)                 | TÖÖHÕIVE LÕPPKUUPÄEV (TÖÖHÕIVE LÕPPKUUPÄEV)       |
| cdm_validfrom (Kehtiv alates)                                    | KEHTIV ALATES (KEHTIV ALATES)                       |
| cdm_validto (Kehtib kuni)                                        | KEHTIB KUNI (KEHTIB KUNI)                             |
| cdm_workerstartdate (cdm_workerstartdate)                     | TÖÖTAJA ALGUSKUUPÄEV (TÖÖTAJA LÕPPKUUPÄEV)           |
| cdm_lastdateworked (cdm_lastdateworked)                       | VIIMANE TÖÖPÄEV (VIIMANE TÖÖPÄEV)             |
| cdm_transitiondate (cdm_transitiondate)                       | ÜLEVIIMISE KUUPÄEV (ÜLEVIIMISE KUUPÄEV)             |
| cdm_employerunitofnotice (cdm_employerunitofnotice)           | TÖÖANDJA TEATE ÜKSUS (TÖÖANDJA TEATE ÜKSUS) |
| cdm_workerunitofnotice (cdm_workerunitofnotice)               | TÖÖTAJA TEATE ÜKSUS (TÖÖTAJA TEATE ÜKSUS)     |
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONALI NUMBER (PERSONALI NUMBER)           |
| cdm_companyid.cdm_companycode (cdm_companyid.cdm_companycode) | JURIIDILISE ISIKU ID (JURIIDILISE ISIKU ID)               |
| cdm_employernoticeamount (cdm_employernoticeamount)           | TÖÖANDJA TEADETE ARV (TÖÖANDJA TEADETE ARV) |
| cdm_workernoticeamount (cdm_workernoticeamount )              | TÖÖTAJA TEADETE ARV (TÖÖTAJA TEADETE ARV)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Töötaja ametikoha määramisest töötaja ametikoha määrangutele

| Dataverse'i tabel (allikas)                             | Finance'i üksus (sihtkoht)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONALI NUMBER (PERSONALI NUMBER)           |
| cdm_jobpositionnumber (Ametikoha number)                   | AMETIKOHA ID (AMETIKOHA ID)                        |
| cdm_validfrom (Kehtiv alates)                                    | KEHTIV ALATES (KEHTIV ALATES)                       |
| cdm_validto (Kehtib kuni)                                        | KEHTIB KUNI (KEHTIB KUNI)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Töötaja aadressitest töötaja postiaadressi v2-le

| Dataverse'i tabel (allikas)                             | Finance'i üksus (sihtkoht)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber (cdm_workerid.cdm_workernumber) | PERSONALI NUMBER (PERSONALI NUMBER)           |
| cdm_addresstype (cdm_addresstype)                             | AADRESSI ASUKOHA ROLLID (AADRESSI ASUKOHA ROLLID) |
| cdm_line1 (cdm_line1)                                         | AADRESS, TÄNAV (AADRESS, TÄNAV)               |
| cdm_city (cdm_city)                                             | AADRESS, LINN (AADRESS, LINN)                   |
| cdm_stateorprovince (cdm_stateorprovince)                     | AADRESS, OSARIIK (AADRESS, OSARIIK)                 |
| cdm_postalcode (cdm_postalcode)                               | AADRESS, SIHTNUMBER (AADRESS, SIHTNUMBER)                |
| cdm_countryregion (cdm_countryregion)                         | AADRESS, RIIK/REGIOON (AADRESS, RIIK/REGIOON)    |
| cdm_addressnumber (cdm_addressnumber)                         | AADRESSI ASUKOHA ID (AADRESSI ASUKOHA ID)          |
| cdm_ispreferred (cdm_ispreferred)                             | ON ESMANE (ON ESMANE)                       |
| cdm_county (cdm_county)                                       | AADRESS, MAAKONNA ID (AADRESS, MAAKONNA ID)              |
| cdm_addresstype (cdm_addresstype)                             | AADRESSI KIRJELDUS (AADRESSI KIRJELDUS)        |

## <a name="integration-considerations"></a>Integratsiooni kaalutlused

Integreerimine rakendusest Human Resources rakendusse Finance püüab kirjeid ID põhjal vastendada. Kui kirjed vastavad, kirjutab andmeintegraator rakenduse Finance andmed üle rakenduse Human Resources väärtustele. Kuid probleem võib ilmneda juhul, kui loogiliselt on need erinevad kirjed ja sama ID on loodud kas rakenduses Human Resources või Finance põhjal vastava numbriseeria alusel.

See probleem võib esineda üksusega **Töötaja**, kus kasutatakse sobitamiseks **Personali numbrit** ja **Ametikohti**. Tööd ei kasuta numbriseeriaid. Seega, kui sama töö ID on olemas nii rakenduses Human Resources kui ka Finance, kirjutab rakenduse Human Resources Dynamics 365 Finance’i teabe üle. 

Dubleeritud ID-dega seotud probleemide vältimiseks saate lisada [numbriseeriale](/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=%2fdynamics365%2funified-operations%2ftalent%2ftoc.json) eesliite või määrata numbrijärjestuse algusnumbri, mis ületab teise süsteemi vahemikku. 

Töötaja aadressi jaoks kasutatav asukoha ID ei ole numbriseeria osa. Töötaja aadressi integreerimisel rakendusest Human Resources rakendusse Finance, kui töötaja aadress on juba Finance’is olemas, võib luua aadressi duplikaatkirje. 

Järgmisel joonisel on toodud andmete integreerimise malli vastenduste näide. 

![Malli vastendamine.](./media/IntegrationMapping.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
