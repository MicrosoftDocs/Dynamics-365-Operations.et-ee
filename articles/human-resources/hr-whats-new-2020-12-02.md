---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (2. detsember 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 2. deptembri 2020 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d95c92fe15f4dfe77d2bc8a153f86165c17edb4e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892629"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (2. detsember 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3788.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Juhid saavad esitada ametikohtade värbamistaotlusi | [Juhid saavad esitada avatud ametikohtade värbamistaotluse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Värbamistaotluse lisamine](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Täiustatud kandidaadi profiil personalihalduses | [Täiustatud kandidaadi profiil personalihalduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Kandidaadi profiili lisamine või muutmine](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Lihtsustatud integreerimise lubamine värbamispakkujatega | [Lihtsustatud integreerimise lubamine värbamispakkujatega](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaatide värbamine](./hr-personnel-recruit.md) |
| Kohandatud lingid juhi iseteeninduses | [Kohandatud lingid juhi iseteeninduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Kohandatud lingid juhi iseteeninduses](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta | Kirjeldus |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult peaks sisaldama kuupäeva ja kellaaega, mida kasutati töötlemisel. | BenefitEligibity töötlemise tulemuses on nüüd viimase töötluse datetimestamp, mis varem puudus. |
| 526903 | Soodustuste registreerimine nurjub sõltuvate isikutega lepingute puhul, kui jaotises **Human Resourcesi ühiskasutuses parameetrid** lülitatakse sisse suvand **Volitatud isikute automaatne valimine**. | Lahendati probleem, kus soodustuste registreerimine nurjus sültuvate isikute puhul, kui suvand **Volitatud isikute automaatne valimine** oli volitatud isikute korral vaikimisi sisse lülitatud. |
| 521922 | Parameeter **Kuva puudumine ilma üksikasjadeta** näitab vaba aja taotlusi töörühma puudumiste kalendris. | Puhkuse tüüp, puhkuse tüübi värv ja päeva üksikasjad kuvatakse töörühma puudumiste kalendris, kui jaotise **Puhkuste ja puudumiste parameetrid** parameetri **Kuva puudumine ilma üksikasjadeta** väärtuseks määrati **Jah**. See probleem lahendati ja nüüd puhkuse tüüpi ei kuvata ja vaikimisi puhkuse tüübi värvi (tumesinist) kasutatakse kõigi puhkuse tüüpide jaoks töörühma puudumiste kalendris. |
| 527316 | Töö, ametikoha ja töötaja teatise pealkirju ei sünkroonita. | Pealkirjaseos lisati varem töö-, ametikoha- ja töötajaüksusele. Selle seose sünkroonimine töötab Human Resourcesi sünkroonimisel teenusega Dataverse, kuid ei töötanud teenuse Dataverse saadetud teatiste korral. See probleem lahendati. |
| 512275 | Jaotisest **Puhkuste ja puudumiste parameetrid** eemaldati värvivalikud. | Nüüd, kui värve määratletakse puhkusetüübiga, ei ole värvivalik enam jaotises **Puhkuste ja puudumiste parameetrid** vajalik, mistõttu see eemaldati. |
| 437112 | Töötaja ametikoha määramisel kuvatakse eksitav tõrketeade. | Värskendati tõrketeadet, mis kuvatakse töötaja palkamisel ja kui töötajat püütakse määrata ametikohale, mis pole aktiivne. Teadet värskendati: „**Määratud ametikoht pole töösuhte alguskuupäeval aktiivne. Kontrollige ametikoha kestust.**“ |
| 527816 | Jõudlusprobleemid lehel **Vaba aeg**. | Lehe **Vaba aeg** jõudlust parandati. |
| 523158 | Üksust BenefitPeriodMigrationUpgrade ja BenefitPlanMigrationUpgrade ei käivitata. | Lahendati probleemid soodustuse migreerimise töödega, mis on seotud selega, et üksust **Periood** ja **Plaan** ei käivitata õigesti. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| LinkedIn talent Hubiga integreerimine | [LinkedIn talent Hubiga integreerimine](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn talent Hubiga integreerimine](./hr-admin-integration-linkedin.md) |
|Kogu ettevõtte puhkusete vaade juhtidele | [Kogu ettevõtte töövõtjate puhkuste vaade juhtidele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Puhkuste ja puudumiste parameetrite konfigureerimine](./hr-leave-and-absence-parameters.md) |
|Täiendava ülevaate andmine puhkusesaldodest| [Täiendava ülevaate andmine puhkusesaldodest](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Töötaja puhkuse haldamine](./hr-leave-and-absence-manage-employee-leave.md) |
| Juhid saavad esitada ametikohtade värbamistaotlusi | [Juhid saavad esitada avatud ametikohtade värbamistaotluse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Värbamistaotluse lisamine](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Täiustatud kandidaadi profiil personalihalduses | [Täiustatud kandidaadi profiil personalihalduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Kandidaadi profiili lisamine või muutmine](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Lihtsustatud integreerimise lubamine värbamispakkujatega | [Lihtsustatud integreerimise lubamine värbamispakkujatega](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidaatide värbamine](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2020. aasta väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]