---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 22. veebruaril 2021?
description: Selles teemas kirjeldatakse rakenduse Microsoft Dynamics 365 Human Resources 22. veebruaril 2021 lisatud uusi või muudetud funktsioone.
author: marcelbf
manager: tfehr
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 363ea7d47a46234b2854a073029859c31277d88f
ms.sourcegitcommit: 75b432ce9019c81253eb6bd865db905701e28a26
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/11/2021
ms.locfileid: "5579351"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 22. veebruaril 2021?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3988.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Microsoft Teamsi rakendus Dynamics 365 Human Resources | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta |  Kirjeldus |
| --- | --- | --- |
| 529994 | Välja **Tuntud kui** muutmine vormil **Töötaja** ei käivita Dataverse'i värskendamist | Lahendatud on probleem, mille korral Dataverse'i ei värskendata välja **Tuntud kui** värskendamise korral vormil **Töötaja**. |
| 532651 | Kompensatsiooni analüüsi PBI aruanne ei kasuta kogu ettevõtte mõõdikute arvutamisel valuutateisendust | Lahendatud on probleem, mille korral kompensatsiooni analüüsi PBI aruandes ei tehtud valuutateisendusi õigesti. |
| 552226 | Elusündmuse töötlemine sulgeb ja taasavab plaanid ühe elusündmuse ajal mitu korda  | Lahendatud on probleem, mille korral mitmes juriidilises isikus töötava töötaja elusündmuse toimumisel genereeritakse elusündmuse kirje iga juriidilise isiku jaoks, milles töötaja asub. Elusündmuste töötlemisel tuleb valida töödeldav juriidiline isik. Töötlemisloogika ei piira end siiski üksnes selle juriidilise isikuga. Selle asemel töötleb see kõiki juriidilisi isikuid ning sulgeb ja avab plaanid valitud juriidilises isikus uuesti. See tegevus tähendab sama elusündmuse mitmekordset töötlemist samas juriidilises isikus, mille tulemusena suletakse ja taasavatakse iga elusündmusest mõjutatud plaan mitu korda. |
| 518064 | Tingimustele vastavates plaanides on valitud ainult üks sõltuv isik, ehkki volitatud isikuid on vaikimisi märgitud mitu | Lahendatud on probleem, mille korral tingimustele vastavates plaanides ei valita automaatselt mitut volitatud vaikeisikut. Isiklikuks kontaktisikuks saate nüüd määrata kindla esmase kasusaaja. Tingimustele vastavates plaanides, kus kasusaajaid on mitu, on esmane kasusaaja kirjas kui 100%. |
| 552365 | Oma andmebaasi toomise (BYOD) eksporditööd nurjuvad pärast üleminekut platvormivärskendusele 40 | Lahendatud on probleem, mille korral BYOD ekspordid nurjuvad pärast platvormivärskenduse 40 rakendamist keskkonnas. |
| 547123 | Armatuurlaual tehaolevate tööde loendisse lisatavate ülesannete arvu piiramine | Tehaolevate tööde loendis kuvatud ülesannete arvu ülempiir on nüüd 15, et lahendada jõudlusprobleem, mille põhjustas ülemäära suure hulga ülesannete laadimine. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Kogu ettevõtte puhkusete vaade juhtidele | [Kogu ettevõtte töövõtjate puhkuste vaade juhtidele](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Puhkuste ja puudumiste parameetrite konfigureerimine](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Ettevõtte kontaktteabe redigeerimise keelamine töötajatele | [Ettevõtte kontaktteabe redigeerimise keelamine töötajatele](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse'i terminoloogia uuendused

Alates novembrist 2020, on Common Data Service nimetatud ümber rakenduseks [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Vt [ametlikku teadaannet](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Appsi blogist. Seoses selle nimemuudatusega on uuendatud ka Dataverse'i terminoloogiat. Näiteks *olem* on nüüd *tabel* ja *väli* on nüüd *veerg*. Lisateavet leiad artiklist [Terminoloogia uuendused](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Selles väljalaskes on Dynamics 365 Human Resources'i Dataverse'iga integreerimisega seotud terminoloogiat uuendatud kogu rakenduses, et kajastada neid muudatusi. Näiteks **Common Data Service'i integreerimisvorm** on nüüd **Microsoft Dataverse'i integratsioon**.

Rakenduse Dynamics 365 Human Resources rakendusega Microsoft Dataverse integreerimise kohta leiate lisateavet jaotisest [Microsoft Dataverse'i integratsiooni konfigureerimine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) ja [Microsoft Dataverse'i virtuaalsete tabelite konfigureerimine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="updates-to-service-deployment"></a>Teenuse juurutuse värskendused

Alates 22. veebruari 2021 väljalaskest täpsustame piirkondlike teenusevärskenduste juurutamist. Täpsustuste raames muudetakse regulaarselt järjestust, milles inimressursside teenuse (Human Resources) värskendusi eri regioonides pakutakse, samuti muudetakse värskendusetappide vahelist ooteaega. Need muudatused tagavad senisest parema kooskõla turvaliste juurutuspraktikatega (SDP), et parendada teenuse stabiilsust, kvaliteeti ja tuge.

Järgime ka edaspidi kahenädalast juurutamissagedust. Kliendid võivad siiski märgata, et värskendused rakendatakse nende inimressursside teenuse keskkondades varasemate väljalasetega võrreldes sama kahenädalase tsükli erineval nädalapäeval.

Teenuse värskendamisprotsessi kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-setup-update-process).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
