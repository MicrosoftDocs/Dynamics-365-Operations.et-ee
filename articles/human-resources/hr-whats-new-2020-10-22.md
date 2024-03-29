---
title: Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (22. oktoober 2020)
description: See artikkel kirjeldab funktsioone, mis on Dynamics 365 Human Resources microsoftis uued või muutunud 22. oktoober 2020 jaoks.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b183ea08a2decc2696ca3bc3997b5cf7f04652d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068057"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Mis on Dynamics 365 Human Resourcesis uut või mida on muudetud (22. oktoober 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



See artikkel kirjeldab funktsioone, mis on uued, muutunud või tulevad varsti Dynamics 365 Human Resources. Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3680.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tulevad üldiselt kättesaadavaks järgmised funktsioonid.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Platform update 10.0.14(38) | -- | [Platvormi värskendused versioonile 10.0.14 finantside ja toimingute rakendustest (november 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| Organisatsiooni ja personalihalduse töövoogude kasutuskogemuse täiustused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

> [!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Võime seda artiklit värskendada, et kaasata vigaparandused, mis muutsid selle järku pärast selle artikli algset avaldamist.

| Väljaande number| Probleem  | Kirjeldus|
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
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Rakenduses Dataverse for Human Resources saadaolevad virtuaalüksused | [Dynamics 365 Human Resourcesi põhiandmete laiendamine Dataverse'is](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse'i virtuaalüksuste konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md) |
| LinkedIn talent Hubiga integreerimine | [LinkedIn talent Hubiga integreerimine](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [LinkedIn talent Hubiga integreerimine](./hr-admin-integration-linkedin.md) |
| Kohandatud lingid juhi iseteeninduses | [Kohandatud lingid juhi iseteeninduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Kohandatud lingid juhi iseteeninduses](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>Peagi tulekul

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2020. aasta väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
