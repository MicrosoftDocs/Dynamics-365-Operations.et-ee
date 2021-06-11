---
title: Mis on uus või muudetud rakenduses Dynamics 365 Human Resources (20. mai 2021)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 20. mai 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: afa64474e8eaf4c7b73e4f76d85e379f77b570a7
ms.sourcegitcommit: eff3da7ea98758f100d44ff7feec17157afc2e80
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6111563"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Mis on uus või muudetud rakenduses Dynamics 365 Human Resources (20. mai 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4189.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Platvormi värskendus 10.0.18 (42) | -- | [Rakenduse Finance and Operations platvormi versiooni 10.0.18 uuendused (mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Inimressursside rakendus Microsoft Teams toetab poole päeva definitsioone ja päeva tükeldamise võimalust | -- | [Puhkusetaotluste haldamine Teamsis](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 583776 | Töötajate hulgiregistreerimine puhkuseplaanidesse põhjustab duplikaatkirje tõrget | See viga on parandatud viimase vabastamisega ja hulgipuhkuste plaani registreerimist peab edukalt töötlema. |
| 582263 | Kõigi töötajate elusündmuse töötlemist ei saa korraga käivitada | Kui **Töötaja** väli on jäetud tühjaks elusündmuse töötlemiseks, töödeldakse kõik töötajad. |
| 558383 | Esmane kasusaaja pole märgitud 100%-na, kui vaikeprojekte pole valitud | Viga on fikseeritud, nii et kasutaja peab valima ainult esmase kasusaaja tumbleri.|
| 509404 | Osakonna töötajate arvu analüüsis ei arvestata töötajate liikumist osakonna vahel |Analüüsi värskendati, et kaasata töötajate üleviimised osakondade vahel|
| 579420 | Ruudustike funktsiooni veergude külmutamine ei tohiks veel saadaval olla | Funktsiooni **Saadaolevad külmutamisveerud ruudustikes** mis ei ole inimressurssides saadaval, on loetletud funktsioonihalduses saadaval olevana. Funktsioon eemaldati lubamiseks funktsioonide loendist. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Kohandatud väljade toe jaoks kvalifitseerumise reeglid soodustuste halduses | [Kohandatud välja tugi kõlblikkuse töötlemiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Sobivuse reeglite konfigureerimine](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Puhkuse ja puudumise töövoo kogemuse täiustused | [Puhkuse ja puudumise töövoo kogemuse täiustused](https://go.microsoft.com/fwlink/?linkid=2147528) | [Taotle vaba aega](hr-employee-self-service-request-time-off.md)|
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|
| Puhkuse tekkepõhise kande auditeerimine | - | [Puhkuse tekkepõhise kande auditeerimine](hr-leave-and-absence-accrue.md#preview-leave-accrual-transaction-auditing)|

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
|  Luba puudumiste halduril puhkusi hallata | [Luba puudumiste halduril puhkusi hallata](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
