---
title: Mis on uus või muudetud rakenduses Dynamics 365 Human Resources (3. mai 2021)
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 3. mai 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df8bd0277e4f27c23ba25c886d12f589913e5d46
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066219"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Mis on uus või muudetud rakenduses Dynamics 365 Human Resources (3. mai 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4140.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Saate lisada teaberiba elusündmuste loomisel. | - | Kui loote elusündmuse, kuvab teaberiba teate, mis näitab loodud elusündmuse tüüpi.

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 559312 |  Töötaja fikseeritud tasuplaani loomisel taset ei kuvata. |  Kui kasutaja ajavöönd ja ettevõtte ajavöönd ei kattu, ei õnnestunud töö kompensatsioonitaset lugeda. Päringut värskendati UTC-kellaajal põhinevaks toomiseks. |
| 573676  | Uut perioodi ei saa vormi **Eelistuste plaan** lisada. | Vormi värskendati nii, et **Uus** nupp oleks lisatud kiirkaardi **Periood** kiirkaardi jaotises **Soodustusplaanid**. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Puhkuse ja puudumise töövoo kogemuse täiustused | [Puhkuse ja puudumise töövoo kogemuse täiustused](https://go.microsoft.com/fwlink/?linkid=2147528) | [Taotle vaba aega](hr-employee-self-service-request-time-off.md)|
| Lihtsustatud palgaintegratsiooni (palgaarvestuse integratsiooni API-d) lubamine | [Lihtsustatud integreerimise lubamine palgaarvestuse pakkujatega](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Palgaarvestuse integratsiooni API](hr-admin-integration-payroll-api-introduction.md)|
| Puhkuse tekkepõhise kande auditeerimine | - | [Puhkuse tekkepõhise kande auditeerimine](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Platvormi värskendus 10.0.18 (42) | Platvormi värskendus 10.0.18 peaks tuleb välja teenuseväljalaske raames 17. mail 2021. Lisateavet vt platvormi värskendustest [versioonile 10.0.18 finantside ja toimingute rakendustest (mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Kohandatud väljade toe jaoks kvalifitseerumise reeglid soodustuste halduses  | [Kohandatud välja tugi kõlblikkuse töötlemiseks](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

