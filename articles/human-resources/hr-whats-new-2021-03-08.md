---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 8. märtsil 2021?
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 8. märtsil 2021 lisatud uusi või muudetud funktsioone.
author: marcelbf
ms.date: 03/08/2021
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
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 133cfffadabade8f7770b4853e14b769c5b961370546e3104d6db26bc0c6331a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719064"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 08. märtsil 2021?

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.4017.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Kogu ettevõtte puhkusete vaade juhtidele | [Kogu ettevõtte töövõtjate puhkuste vaade juhtidele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Puhkuste ja puudumiste parameetrite konfigureerimine](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta |  Kirjeldus |
| --- | --- | --- |
| 486611 | Puhkus kuvatakse puhkusekalendris, ehkki säte **Keela puhkus kõigis kalendrites** on lubatud | Kui säte **Keela puhkus kõigis kalendrites** on sisse lülitatud, ei kuvata puhkuseteavet enam kalendris, kui puhkuste ja puudumiste kalendritäienduste funktsioon on lubatud.|
| 508972 | Puhkuste ja puudumiste pangakande üksuses pole registreerimist kinnitatud | Puhkuste ja puudumiste pangakande üksuse kasutamise korral ei saa töötajaid, kes pole plaani registreeritud, enam importida. |
| 554854 | Kalendri värskendamisel tööhõive üksuses ilmneb tõrge, kui kasutajavalikutes on vaikimisi määratud mõni muu juriidiline isik | Töötaja kalendri värskendamine tööhõive üksuse kaudu ei põhjusta enam tõrget, kui kasutajavalikutes on vaikimisi määratud mõni muu juriidiline isik. |
| 558347 | Avalehe laadimisel kuvatakse tõrketeade „Vormikonfiguratsioonides ei saa kirjet luua (FormRunConfiguration)“. | Avalehe laadimisel põhjustavad isikupärastamised tõrketeate „Vormikonfiguratsioonides ei saa kirjet luua (FormRunConfiguration)“ kuvamise. |
| 557327 | Soodustuste halduse tööruum: ruudustiku kohal kuvatakse vahe. | Lahendatud on kasutuskeskkonna probleem, mille korral soodustuste tööruumis kuvati tabeliruudustiku ääristes soovimatu vahe. |
| 557334 | Soodustuste halduse tööruum: valikuripploend **Periood** peaks kuvatama ainult vahekaardil **Kokkuvõte** | Soodustuste valikuripploend **Periood** kuvatakse ainult juhul, kui vahekaart **Kokkuvõte** on soodustuste tööruumis aktiivne, mitte aga jaotistes **Protsessi tulemused** ja **Lingid**. |
| 557336 | Soodustuste halduse tööruum: tekst **Ava registreerumine välja registreeritud plaanidega** on paanivaates kärbitud | Vajaliku konteksti kärpimise vältimiseks on uus tekst paanivaates **Välja registreeritud plaanid...ava registreerumine**. |

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