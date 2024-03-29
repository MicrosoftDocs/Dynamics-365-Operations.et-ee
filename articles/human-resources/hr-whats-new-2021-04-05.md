---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (5. aprill, 2021)?
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 5. aprilli 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9388b2f43762bedf07c89a7a565935d2043ee90c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067997"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources (5. aprill, 2021)?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4074.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Ettevõtte kontaktteabe redigeerimise keelamine töötajatele | [Ettevõtte kontaktteabe redigeerimise keelamine töötajatele](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Isikuandmete redigeerimise piiramine](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.

| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 550852 | Nupp **Kinnitamine** ei kinnita vormil **Ülevaade** seatud kohustuslike väljadega. | Kui seate vormil **Ülevaade** välja kohustuslikuks ja avaldate halduri rolli muudatused, ei kinnitata vormi ootuspäraselt. |
| 559564 | Töötaja ajaloolised tegevused püsipalga muutmiseks annavad lõpetatud kasutajatele tõrke. | Töötaja lahkunud töötaja palk annab vea. Pärast töötaja lahkumist annab töötaja edutamine enne lõpetamist tõrke. |
| 560074 | Tööhõivekategooria ripploend ei filtreeri **töötaja tüüpi** ning kuvab töötajate ja töövõtjate kategooriad. | Vormil **Töötaja** peaks ripploendis **Töösuhte kategooria** kuvama töötaja- või töövõtjakategooriad vastavalt töötaja töötüübile. |
| 567388 | Osa vastloodud töötajate teabest ei sünkroonita kohe Dataverse  **cdm_worker**-i tabeliga. | Uue töötajakirje loomisel sünkroonitakse uus kirje rakenduses Dataverse tabeliga **cdm_worker**, kuid Dataverse kirjesse ei kaasata kõiki atribuute. |
| 563837 | Funktsioonid, mis pole personaliosakonna kuval saadaval. | Mitmed funktsioonid, mis ei rakendu funktsioonihalduses kuvatavatele inimressurssidele. Need funktsioonid eemaldatakse nüüd inimressurssides lubamiseks saadaolevate funktsioonide loendist. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |
| Platvormi värskendus 10.0.17 (41) | Platvormi värskendus 10.0.17 peaks algama järgmise väljalaskega (19. aprill 2021). Lisateavet vt platvormi värskendustest [versioonile 10.0.17 finantside ja toimingute rakendustest (aprill 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
