---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 22. märtsil 2021?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 22. märtsil 2021 lisatud uusi või muudetud funktsioone.
author: marcelbf
ms.date: 03/22/2021
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
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b973be365b3afa8461f7709c1ecee835c5dcf2f1
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890647"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 22. märtsil 2021?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4049.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Suvand kinniste pakett-tööde tühistamiseks ja lähtestamiseks (560976) | NA | [Lähtesta kinnised pakett-tööd](./hr-admin-troubleshooting-batch-execution.md) |
| Väikesed UX-i värskendused uue soodustusplaani loomiseks (419941) | NA | [Soodustuse plaani loomine](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta |  Kirjeldus |
| --- | --- | --- |
| 554239 | Jõudluse parandamine üksustele, mis on seotud **ÄriProtsessiÜlesandeÜlesandega** tabel | Paranda jõudlust üksustes, mis on seotud **ÄriPotsessiÜlesandeÜlesande** tabeliga lisades tabelile soovituslikud indeksid. |
| 566061 | V2 üksuse varukoodi eemaldamine öiselt sünkroonimiselt | Saate eemaldada V2 varukoodi öiselt Dataverse -i  sünkroonimise jaoks. Taane ei ole enam vajalik ja takistab filtreeritud sünkroonimise töötamist nii, nagu oodatud. Muudatus parandab andmete sünkroonimise Dataverse ühtsust. |
| 538024 | Töötaja hüvitisplaanid > Väljaregistreerimise eemaldamise tõrge | Fikseeritud tõrge soodustusplaani suvandi väljaregistreerimise eemaldamisel töötaja soodustuste vormis. |
| 557965 | **Soodustuste** tööruum: **Aktiivse elu sündmused** link peab alati olema nähtav jaotises **Lingid** | Parandatud probleem, kus **aktiivse elusündmuse** link oli jaotises **Lingid** nähtav, kuid navigeerimisel ilmnes tõrge, kui **(Eelvaade) Soodustuste halduse tööruum** funktsioon ei ole lubatud. Lisateavet tööruumi lubamise kohta vt [Soodustuste halduse tööruumist](hr-benefits-management-workspace.md). |
| 556672 | Lõpetatud töötaja viitvõlgu ei saa töödelda, kui **streamlined töötaja kirje** on funktsioonihalduses lubatud | Puhkuse ja puudumisplaanide lisandumise suvand on lisatud jaotisesse **Rohkem suvandeid** **Töö ajaloo** all töötajatele kui **Lihtsustatud töötaja kirje** on funktsioonihalduses lubatud. |
| 562656 | Menüükäsk **SysRecordChangeLogValidTimeState** peab olema kaasatud turbe privileegi ja **SystemExternalBasicMaintain turbekohustuse** turbekohustuse laiendusse | Mittesüsteemi halduri roll oli kadunud **Vaata muudatusi** nupp ajahalduri vormil. |
| 505989 | Elusündmuste töötlemine: Sobivuse muutust ei töödeldud õigesti kasutatud kuupäeva tõttu | Parandatud probleem, mille puhul sobivuse töötlemise muutus sõltus ametikoha alguskuupäevast ja mitte ainult praegusest ametikohast. |
| 562286 | Töötajaga lepingu lõpetamisel saadetakse mitu värskendamist Dataverse -i | Kui töötaja on töölt lõpetatud, saadetakse rohkem kui üks uuendustoiming Dataverse -i, mille tulemusena on sama muudatuse kohta kaks uuendusteatist. See võib põhjustada mitmeid Power Automate päästikuid, kui voog on konfigureeritud käivituma toimingust. |
| 527340 | Puhkuse ja puudumiste registreerumise avamisel kuvatakse tõrge "Unrepresentable DateTime" | Puhkuse ja puudumiste registreerimise valimisel tõrget enam ei kuvatud. |
| 561663 | Klastri ettevalmistuse jaoks ooteaja intervalli suurendamine | Parandada infrastruktuuri stabiilsust ja ettevalmistuse sisu koos klastri ettevalmistuse värskendamisega. |
| 486129 | Kohandatud välju ei saa redigeerida käskudes **Ametikohad > Muudatuste haldamine** | Paranda probleem, mille korral ei saanud kohandatud välju redigeerida vahekaardil **Halda muudatusi** **ametikohtade** puhul. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse halduse tööruum | [Soodustuste halduse tööruum (eelversioon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Soodustuse halduse tööruum](hr-benefits-management-workspace.md) |
| Ettevõtte kontaktteabe redigeerimise keelamine töötajatele | [Ettevõtte kontaktteabe redigeerimise keelamine töötajatele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]