---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 28. jaanuar 2021
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 28. jaanuariks 2021.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46bbda21c3eb2b32030b93afc2a40785c22b124e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909755"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Mis on uut või mida on muudetud rakenduses Dynamics 365 Human Resources 28. jaanuar 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources.

Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3906.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Soodustuse põhjuste koodide integreerimine tööruumi **Personalihaldus** | -- | [Põhjusekoodide häälestamine](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.


| Väljaande number | Probleem |  Kirjeldus |
| --- | --- | --- |
| 539456 | Kalendris kuvatakse puhkuse tüüp, kus on lubatud lisateksti funktsioon, kui parameeter **Kuva ainult puudumist ilma üksikasjadeta** on lubatud. | Kui suvand **Kuva ainult puudumist ilma üksikasjadeta** on lubatud, kuvatakse üleminekul nüüd taotluse kuupäeva. |
| 528907 | Töötaja rollile juurdepääsu andmine juriidilisele isikule põhjustab selle, et haldurid ei näe töötajate puhkusesaldo toiminguid töötaja iseteeninduskeskuse alal **Minu meeskond**. |Nüüd võimaldab selle suvandi seadistamine halduritel jätkuvalt näha puhkusesaldo tegevust. |
| 526280 | Lubade tõrge olemites HcmWorkerEntity, HcmEmployeeEntity ja HcmContractorEntity. | Kasutajad, kes pole süsteemihalduri rollis, ei saanud välja NationalityCountryRegion õiguste tõrke tõttu all loetletud üksusi eksportida. Kasutajad vajavad selle teabe eksportimiseks endiselt järgmisi õigusi: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain ja HCMContractorEntityView. |
| 542147 | **Pangakonto numbri** ja **Protsessikoodi** väljad on kohustuslikud pangakonto sisestamisel töötaja iseteeninduskeskuse kaudu. | Oleme parandanud tõrke, mille puhul töötajad pidid pangakonto üksikasju lisades sisestama **Pangakonto numbri** ja **Protsessikoodi** . Need väljad pole uue pangakonto teabe salvestamisel enam kohustuslikud. |
| 543641 | Elektroonilises aruandluses ei täideta sihtnumbrit. | Parandatud on viga, kus sihtnumbrit ei täidetud ACA aruandes kindlustuskaitse koodide L kuni Q korral. |
| 545402 | 404-tõrgete eemaldamiseks lisatud marsruutimismuudatus faili UserBranding.js jaoks. | Kasutaja ei tohiks enam konsoolis 404 tõrget näha. |

## <a name="in-preview"></a>Eelvaates   

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Kogu ettevõtte puhkusete vaade juhtidele | [Kogu ettevõtte töövõtjate puhkuste vaade juhtidele](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Puhkuste ja puudumiste parameetrite konfigureerimine](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Peagi tulekul

| Funktsioon | Details |
| --- | --- |
| Soodustuste registreerimise meilikinnitus | Kui see funktsioon annab võimaluse saata töövõtjatele kinnitusmeili, kui nad registreerivad soodustuste registreerimise kogemuse töövõtja iseteeninduse kaudu. See funktsioon on saadaval 1. veebruaril. Lisateavet vaadake jaotisest [Soodustuste halduri parameetrite konfigureerimine ettevõtte alusel](hr-benefits-setup-parameters-per-company.md). |
| Töövoog saab automaatselt heaks kiita juhataja poolt töötajate jaoks sisestatud oskused. | Peagi tulekul. |

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2021. aasta 1. väljalaskevoo ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Microsoft Dataverse'i terminoloogia uuendused

Alates novembrist 2020, on Common Data Service nimetatud ümber rakenduseks [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Vt [ametlikku teadaannet](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) Power Appsi blogist. Seoses selle nime muudatusega on uuendatud mõnda Dataverse'i terminoloogiat. Näiteks *olem* on nüüd *tabel* ja *väli* on nüüd *veerg*. Lisateavet leiad artiklist [Terminoloogia uuendused](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Selles väljalaskes on Dynamics 365 Human Resources'i Dataverse'iga integreerimisega seotud terminoloogiat uuendatud kogu rakenduses, et kajastada neid muudatusi. Näiteks **Common Data Service'i integreerimisvorm** on nüüd **Microsoft Dataverse'i integratsioon**.

Rakenduse Dynamics 365 Human Resources rakendusega Microsoft Dataverse integreerimise kohta leiate lisateavet jaotisest [Microsoft Dataverse'i integratsiooni konfigureerimine](./hr-admin-integration-common-data-service.md) ja [Microsoft Dataverse'i virtuaalsete tabelite konfigureerimine](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resources 2021 väljalaskevoo 1 ülevaade](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]