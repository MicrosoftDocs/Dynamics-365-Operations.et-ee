---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (22. oktoober 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 22. oktoobri 2020 uusi või muutunud funktsioone.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 642250fa34ee87065f4ed2cf8f3893390d271007
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464786"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (22. oktoober 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone. Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3680.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Platform update 10.0.14(38) | -- | [Finance and Operationsi platvormi versiooni 10.0.14 uuendused (november 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Organisatsiooni ja personalihalduse töövoogude kasutuskogemuse täiustused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime värskendada seda teemat, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number| Väljasta  | Kirjeldus|
| --- | --- | --- |
| 437922 | FMLA tundide importimine DMF-üksuse abil põhjustab kirjutuskaitstud tõrke. | FMLA tundide üksuse kasutamine FMLA juhtumiga seostatud tundide importimiseks nurjus. Lisasime loogika tagamaks, et imporditud tunnid ei ületaks juhtumi järelejäänud tunde. |
| 512019 | Vale **Viimase edasikandmise** summa. | Lehel **Vaba aeg** väärtuse **Kuupäevaga** muutmine järgmise eelarveperioodi esimesele päevale, kuvab vale **Viimase edasikandmise** summa tüübile **Iga-aastane puhkus**. Nüüd kuvatakse õige summa. |
| 458639 | Üksus **Töötaja kontaktid** ei toeta muudatuste jälgimise režiimi. | Uuendasime üksust **Töötaja kontaktid**, et saaksite seda kasutada oma andmebaasi toomise (BYOD) stsenaariumites.|
| 505347 | Koolitusjuhid võivad esitada töövõtja puhkusetaotlust, kui funktsioon Sujuvam töötaja on lubatud. | Töövõtjate vaba aja taotlusi tohivad esitada ainult personaliosakonna assistendi või personaliosakonna juhi rollid. |
| 513490 | Soodustuste halduse logimine: saate lisada logimise lepingutele, millel pole katvuse suvandeid. | Lubasime logimise tulemused **Lepingutele ilma katvuse suvanditeta**. Neid kuvatakse nüüd tabelis **Protsessi tulemused** ja sorditakse õigesti, et kuvada ülaosas. |
| 517021 | Mitut lepingut sama koodiga **Lepingu tüüp** ei saa valida, kui **Lepingu tüübil** on üks registreerimine tüübi kohta. | Muutsime piirangut lepingute valimiseks, kus on ainult üks registreerimine lubatud. Piirangud on nüüd tasemel **Lepingu tüübi kood**, mitte **Lepingu tüüp**. See muudatus lubab selliseid lepinguid, nagu HSA ja FSA, mis on sama tüübiga, kuid saate määrata neile erineva **Lepingu tüübi koodi**. Nii saate valida mõlemad sama registreerimise perioodi kohta. |
| 444791 | Hüvitust ei saa kuvada töövõtja iseteeninduses, kui suvand **Juurdepääsu piiramine** on hüvituseplaanis sisse lülitatud. | Töövõtja iseteeninduse kaardil **Hüvitused** kuvati praeguse hüvituse summa ja suurendusprotsendi väärtuseks „0”, kui töötaja oli registreeritud plaanis, kus oli suvand **Juurdepääsu piiramine** sisse lülitatud ja on määratud kindlatele rollidele. Lahendasime selle probleemi nii, et töövõtja ja juht näevad alati enda ja oma otseste alluvate hüvituse üksikasju. |
| 457542 | Kursuse üksikasjade värskendamine pärast kursuse sulgemist ei värskenda seda teavet töövõtja kohta, kes selle kursuse läbis. | Töövõtja teavet värskendatakse nüüd õigesti, kui muudate kursuse üksikasju pärast kursuse sulgemist ja uuesti avamist. |
| 515342 | Üksuse **CDSLeaveRequestDetailEntity** kaudu ei saa andmeid sisestada. Ettevõtet ei leitud või seda pole olemas. | Nüüd saate kasutada üksust **CDSLeaveRequestDetailEntity** andmete sisestamiseks. |
| 514743 | Tõrge vormis **Meiliparameeter** Microsoft Exchange'i kasutamisel. | Teade „Faile või komplekti ei saanud laadida...” kuvatakse lehel **Meiliparameetrid**, kui meiliteenuse pakkujaks oli seatud **Exchange**. See parandus võimaldab ka lehte **Meiliparameetrid** ootuspäraselt laadida ja salvestada. |


## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Rakenduses Dataverse for Human Resources saadaolevad virtuaalüksused | [Dynamics 365 Human Resourcesi põhiandmete laiendamine Dataverse'is](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse'i virtuaalüksuste konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md) |
| LinkedIn talent Hubiga integreerimine | [LinkedIn talent Hubiga integreerimine](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn talent Hubiga integreerimine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Kohandatud lingid juhi iseteeninduses | [Kohandatud lingid juhi iseteeninduses](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Kohandatud lingid juhi iseteeninduses](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2020. aasta väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]