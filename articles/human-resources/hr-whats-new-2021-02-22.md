---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 22. veebruaril 2021?
description: Selles artiklis kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 22. veebruari 2021 uusi või muutunud funktsioone.
author: marcelbf
ms.date: 02/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d07e73ccd922e9d52a9de9260577087a50ef1da4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897831"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 22. veebruaril 2021?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3988.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Microsoft Teamsi rakendus Dynamics 365 Human Resources | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.

| Väljaande number | Probleem |  Kirjeldus |
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
| Kogu ettevõtte puhkusete vaade juhtidele | [Kogu ettevõtte töövõtjate puhkuste vaade juhtidele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Puhkuste ja puudumiste parameetrite konfigureerimine](./hr-leave-and-absence-parameters.md) |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Ettevõtte kontaktteabe redigeerimise keelamine töötajatele | [Ettevõtte kontaktteabe redigeerimise keelamine töötajatele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse'i terminoloogia uuendused

Alates novembrist 2020, on Common Data Service nimetatud ümber rakenduseks [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Vt [ametlikku teadaannet](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Appsi blogist. Seoses selle nimemuudatusega on uuendatud ka Dataverse'i terminoloogiat. Näiteks *olem* on nüüd *tabel* ja *väli* on nüüd *veerg*. Lisateavet leiad artiklist [Terminoloogia uuendused](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Selles väljalaskes on Dynamics 365 Human Resources'i Dataverse'iga integreerimisega seotud terminoloogiat uuendatud kogu rakenduses, et kajastada neid muudatusi. Näiteks **Common Data Service'i integreerimisvorm** on nüüd **Microsoft Dataverse'i integratsioon**.

Rakenduse Dynamics 365 Human Resources rakendusega Microsoft Dataverse integreerimise kohta leiate lisateavet jaotisest [Microsoft Dataverse'i integratsiooni konfigureerimine](./hr-admin-integration-common-data-service.md) ja [Microsoft Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Teenuse juurutuse värskendused

Alates 22. veebruari 2021 väljalaskest täpsustame piirkondlike teenusevärskenduste juurutamist. Täpsustuste raames muudetakse regulaarselt järjestust, milles inimressursside teenuse (Human Resources) värskendusi eri regioonides pakutakse, samuti muudetakse värskendusetappide vahelist ooteaega. Need muudatused tagavad senisest parema kooskõla turvaliste juurutuspraktikatega (SDP), et parendada teenuse stabiilsust, kvaliteeti ja tuge.

Järgime ka edaspidi kahenädalast juurutamissagedust. Kliendid võivad siiski märgata, et värskendused rakendatakse nende inimressursside teenuse keskkondades varasemate väljalasetega võrreldes sama kahenädalase tsükli erineval nädalapäeval.

Teenuse värskendamisprotsessi kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]