---
title: Kandidaadi jälgimissüsteemi integreerimise API tutvustus
description: Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources kandidaadi jälgimissüsteemi (ATS) integratsiooni API-d.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f70e377d6844b5c4f9201f0a561ad9cfcab2eda1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890121"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Kandidaadi jälgimissüsteemi integreerimise API tutvustus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse rakenduse Dynamics 365 Human Resources kandidaadi jälgimissüsteemi (ATS) integratsiooni API-d. API eesmärk on võimaldada sujuvat integreerimist rakenduse Dynamics 365 Human Resources ja partneriks olevate ATS-ide vahel.

![ATS-integratsiooni voog](media/hr-admin-integration-ats-api-introduction-flow.png)

Integreeritud kogemus algab rakenduses Human Resources, kui värbamisjuht loob värbamistaotluse. Kui taotlus on aktiveeritud, tõmbab ATS üksikasjad värbamisprojekti loomise taotluse kohta. Seejärel jälgitakse värbamise konteinerit, et valida ja palgata ametikohale kandidaat. Lisaks lõpetab ATS integreerimise, saates valitud kandidaadi kirje rakendusse Human Resources. Kandidaadi kirje saab siis töötajakirje loomiseks läbida rohkem kinnitusi ja töövooge.

Integratsiooni lubamiseks on Human Resources lisanud järgmised komponendid.

1.  Funktsionaalsus värbamistaotluse loomiseks.
2.  Laiendatud kandidaadiprofiil ja seotud töövood.
3.  Integratsiooni API, mis avab uued funktsioonid rakenduste integreerimiseks.

Lisateavet värbamistaotluse ja kandidaadi funktsiooni seadistamise ja kasutamise kohta leiate jaotisest [Värbamistöö kandidaadid](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

See API on ehitatud rakendusele Microsoft Dataverse (varem Common Data Service). Kogu RESTful interaktsioon selle API-ga toimub Microsoft Dataverse'i veebi API kaudu, mis kasutab OData. See API on Dataverse'i Web API alamkogum. Dataverse'i WEB API määratleb sellised omadused nagu autentimine, SLA-d, partii, samaaegsuse kontrolli ja tõrketöötluse.

Lisateavet Microsoft Dataverse'i Web API kohta leidke alpoolt.

- [Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Microsoft Dataverse'i Web API kasutamine](/powerapps/developer/data-platform/webapi/overview)
- [Microsoft Dataverse'i arendaja juhend](/powerapps/developer/data-platform)

Ülaltoodud dokumentatsioon sisaldab üksikasju ja arendaja juhendeid Dataverse'i Web API kasutamiseks, näiteks [autentimise halduseks](/powerapps/developer/data-platform/webapi/authenticate-web-api), [toimingute tegemiseks](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [Postmani kasutamiseks API-ga](/powerapps/developer/data-platform/webapi/use-postman-web-api) ja [muudatuste jälgimise või delta sõnede kasutamiseks](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) API-ga.

### <a name="option-sets"></a>Suvandikomplektid

Dokumendis kirjeldatud ATS-integratsiooni API andmemudel hõlmab valikukomplekte, mis pakuvad üksuse atribuutidega seostatud nummerdatud väärtusi. Lisateavet Dataverse'i Web APIs suvandikomplektidega töötamise kohta leiate jaotisest [Suvandikomplektide loomine ja värskendamine Web API-ga](/powerapps/developer/data-platform/webapi/create-update-optionsets). Suvandikomplektid määratakse igale Dataverse'i keskkonnale.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuaalsed tabelid rakendusele Human Resources Dataverse'is

ATS-integratsiooni API lõpp-punktid kasutavad rakenduse Microsoft Dataverse virtuaalse tabeli platvormi võimalusi. Vaikimisi ei juurutata virtuaalseid tabeleid ja nendega seotud API-lõpp-punkte Human Resources'i keskkondades, võimaldades organisatsioonidel määrata, millised OData lõpp-punktid keskkonnaga kokku puutuvad. API kasutamiseks peavad keskkonna jaoks olema loodud virtuaalsed tabelid rakenduse Human Resources olemite jaoks. 

Lisateavet API jaoks virtuaaltabelite loomise kohta leiate jaotisest [Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Andmemudel

Andmemudel on keskendunud kahe põhiüksuse ümber.

- **RecruitingRequest** esindab ATS-i taotlust ühe või mitme avatud ametikoha värbamiseks. Näidispäringut vaadake jaotisest [Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** tähistab kandidaadi üksikasju, kes on ametikoha pakkumise aktsepteerinud. **Isik** tähistab isikut, kes on kandidaat. Isikul võib ettevõttes olla mitmeid rolle (nt kandidaat, tööline, töötaja või töövõtja). Näidispäringu leiate jaotisest [Palgatava kandidaadi näidispäring](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Järgmine diagramm illustreerib seoseid API sees. Mitmetel tüüpidel on võõrvõtmeid rakenduse Human Resources teiste, olemasolevate olemite jaoks, mida siin ei ole kujutatud. See dokument annab teavet üksuste kohta, mis on integratsioonistsenaariumide värbamisel spetsiifilised. Siiski on Dataverse'i Web APIs mitmeid teisi olemeid rakenduse Dynamics 365 Human Resources jaoks, mis võivad samuti olla teie integratsioonile asjakohased. Näiteks võite vajada üksikasju töötajate, tööde, ametikohtade või muude siin määratlemata üksuste kohta. Paljudele neile üksustele viidatakse võõrvõtme seostes või navigeerimisatribuutides.

![ATS-integratsiooni API andmemudel](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Värbamistaotlus ja seotud üksused ning suvandikomplektid

Näidispäring: 

- [Värbamistaotluse näidispäring](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Üksused:

- [Värbamistaotlus](hr-admin-integration-ats-api-recruiting-request.md)
- [Värbamistaotluse ametikoht](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Värbamistaotluse oskus](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Värbamistaotluse haridus](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Värbamistaotluse asukoht](hr-admin-integration-ats-api-recruiting-request-location.md)

Suvandikomplektid.

- [Töö vabastuse olek](hr-admin-integration-ats-api-job-exempt-status.md)
- [Värbamistaotluse ametikoha olek](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Värbamistaotluse olek](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Regulatiivse töö kategooria](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Palgatav kandidaat ja seotud üksused ning suvandikomplektid

Näidispäring:

- [Palgatava kandidaadi päringu näidis](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Üksused:

- [Palgatav kandidaat](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Isik](hr-admin-integration-ats-api-person.md)
- [Isiku haridus](hr-admin-integration-ats-api-person-education.md)
- [Isiku töökogemus](hr-admin-integration-ats-api-person-professional-experience.md)
- [Isiku aadress](hr-admin-integration-ats-api-person-address.md)
- [Osapoole kontakt](hr-admin-integration-ats-api-party-contact.md)
- [Isiku oskus](hr-admin-integration-ats-api-person-skill.md)
- [Hindamise tase](hr-admin-integration-ats-api-rating-level.md)
- [Isikutunnistus](hr-admin-integration-ats-api-person-certificate.md)
- [Tunnistuse tüüp](hr-admin-integration-ats-api-certificate-type.md)
- [Isiku skriining](hr-admin-integration-ats-api-person-screening.md)
- [Skriiningu tüübid](hr-admin-integration-ats-api-screening-types.md)
- [Isiku ID-number](hr-admin-integration-ats-api-person-identification-number.md)

Suvandikomplektid.

- [Kandidaadi integratsiooni tulemus](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Tühi Jah Ei](hr-admin-integration-ats-api-blank-yes-no.md)
- [Lõpuleviimise olek](hr-admin-integration-ats-api-completion-status.md)
- [Kontakti tüüp](hr-admin-integration-ats-api-contact-type.md)
- [Hariduskrediidi alus](hr-admin-integration-ats-api-education-credit-basis.md)
- [Sugu](hr-admin-integration-ats-api-gender.md)
- [Perekonnaseis](hr-admin-integration-ats-api-marital-status.md)
- [Kuud aastast](hr-admin-integration-ats-api-months-of-year.md)
- [Ei Jah](hr-admin-integration-ats-api-no-yes.md)
- [Perioodi ühik](hr-admin-integration-ats-api-period-unit.md)
- [Skriiningu sagedus](hr-admin-integration-ats-api-screening-frequency.md)
- [Skriiningu sageduse loomise vorm](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Oskuse taseme tüüp](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Vt ka

[Kandidaatide värbamine](hr-personnel-recruit.md)<br>
[Mis on Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Microsoft Dataverse'i Web API kasutamine](/powerapps/developer/data-platform/webapi/overview)<br>
[Suvandikomplektide loomine ja värskendamine Web API abil](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]