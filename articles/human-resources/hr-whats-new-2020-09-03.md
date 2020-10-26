---
title: Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (03. september 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 3. septembri 2020 uusi või muutunud funktsioone.
author: Darinkramer
manager: tfehr
ms.date: 9/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 24799e304c27b57375640a5bf6a024a22b757bec
ms.sourcegitcommit: a47a4652a29fdb567a8ba67c4f914a8698e8c48c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/03/2020
ms.locfileid: "3765021"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (3. september 2020)

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3504. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Lifecycle Services (LCS).

Lisateavet rakenduse Human Resources tulevaste funktsioonide kohta vt teemast [Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Rakenduse Human Resources värskendamisprotsessi kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>Selles väljalaskes

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Uued finantsdimensioonide vaikeruudustik ja dialoogi vaikemuster rakenduses Human Resources (469495)

Finantsdimensioonide uus muster on nüüd saadaval järgmistes valdkondades.

- Ametikoha tegevused (vorm: **HcmPositionActionDetail**)
- Palga tulukoodid (vorm: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Kirjeid ei kuvata ettevõtte puhkusekalendris, kui „Puhkuse- ja puudumiste kalendri täiustused” pole lubatud (484406)

See väljalase parandab probleemi, mille korral ettevõtte puhkusekalendris ei kuvata puhkusekandeid. See probleem ilmneb ainult siis, kui funktsioonihalduse suvand **Puhkuse- ja puudumiste kalendri täiustused** pole lubatud.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity probleem (467597)

See väljalase parandab üksusega **BenefitsPlanEmployee** seotud probleemi. Töötaja registreerimiste importimisel määratakse nüüd suvandid **Planeerimise kood** ja **Plaani tüübi kood** õigesti. Selle probleemi tõttu kuvatakse vormil **Töövõtja soodustuste plaan** ja vormil **Registreerimise avamine** töövõtjate soodustuste plaanid valesti.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Elektroonilise faili 1094-C väljundi puuduv tähemärk XML-is (435190)

See muudatus parandab probleemi, mille korral puudub väljundfailis 1094-C vajalik märk IRS-ile edastamisel.

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Töövõtja ergutussüsteemi tabel, mis on vastendatud fikseeritud hüvituse vormiga (476117)

See muudatus viib fikseeritud hüvituse väljad vastavusse fikseeritud hüvituse vormiga. Ergutussüsteemi väljad on nüüd saadaval ainult koos ergutussüsteemi vormiga.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Puhkusetaotlused on lubatud enne registreerimist, kui selle puhkuse tüübi minimaalne saldo on negatiivne (469917)

See muudatus keelab puhkusetaotluste sisestamise enne plaani registreerimist, isegi kui registreerimisel on negatiivne miinimaalne saldo. Saate sisestada või esitada taotlusi ainult siis, kui plaan on aktiivne.

### <a name="document-templates-dont-download-457279"></a>Dokumendimalle ei saa alla laadida (457279)

Selle muudatuse abil saate nüüd kõik dokumendimallid alla laadida. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Andmed kuvatakse hüvituse plaani aruande välja Palgamäär ridade asemel veerupäises (476077)

Analüüsi aruanne kuvab nüüd jaotises **Palgamäär** õiget teavet.

## <a name="in-preview"></a>Eelvaates

### <a name="human-resources-application-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateabe saamiseks vt:

- [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis
- [Teamsi rakendus Human Resources](https://go.microsoft.com/fwlink/?linkid=2127841) rakenduse Human Resources dokumentatsioonis

### <a name="human-resources-app-in-teams-preview-features"></a>Rakendus Human Resources Teamsis eelversioonifunktsioonid
 
-  **Teatised**: vaba aja taotluste esitajaid ja kinnitajaid teavitatakse Teamsi rakenduses Human Resources. Kinnitajad saavad puhkeajataotlusi heaks kiita või tagasi lükata. Kui taotlus on heaks kiidetud või tagasi lükatud, teavitatakse sellest edastajat. Lisateabe saamiseks vt:
   - [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
   - [Teamsi rakenduse Human Resources teatiste lubamine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) rakenduse Human Resources dokumentatsioonis
   - [Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) Rakenduse Human Resources dokumentatsioonis
   - [Teamsi teatised](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) rakenduse Human Resources dokumentatsioonis
   - [Oma töörühma puhkusekalendri vaatamine](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis
 
- **Juhi vaba aja kalender**: juhid saavad vaadata oma otseste alluvate kinnitatud ja ootel vabu aegu kalendrivaates. Selle vaate abil näeb hõlpsalt, millal nende meeskonnaliikmed töölt puuduvad. Lisateabe saamiseks vt:
   - [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
   - [Oma töörühma puhkusekalendri vaatamine](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks (477004)

Nüüd on saadaval uus suvand loendi **Mulle määratud tööüksused** paigutamiseks armatuurlaua parempoolsesse veergu. Selle muudatusega kuvatakse kõik tööüksused ja ülesandeloendid samas alas. Lubage see funktsioon, lülitades funktsioonihalduses sisse suvandi **Eelversioon – töövoo kasutuskogemuse täiustused**. Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

See funktsioon pakub ka töövoosuvandeid, mis kuvatakse personalitoimingute vormidel. Töövoosuvandid kuvatakse kiireks juurdepääsuks ka tegevuse kiirkaardi kohal. Lisateabe saamiseks vt: 

- [Organisatsiooni ja personalijuhtimise töövoo kasutuskogemuse täiustused](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis

![Mulle määratud tööüksused](./media/hr-workflow-work-items-assigned-to-me.png)

![Töövoo üksuste kiirjuurdepääs](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Peagi tulekul

### <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service'is kaasatud kontroll-loendi üksused

Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Common Data Service'is.

### <a name="benefits-management-reason-codes"></a>Soodustuste halduse põhjusekoodid

Soodustuste halduse põhjusekoodid kombineeritakse peagi Human Resourcesi olemasolevate põhjusekoodidega. Kui lõite soodustuste halduses põhjusekoodid, mis on pikemad kui 15 tähemärki, peate soodustuste halduse vormil **Põhjusekoodid** muutma põhjusekoodi nime nii, et see poleks pikem kui 15 tähemärki. Pärast nime värskendamist kuvatakse põhjusekood personalihalduse olemasoleva põhjusekoodi vormi all. See muudatus on tulevikus saadaval ja see ei mõjuta olemasolevaid funktsioone.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)