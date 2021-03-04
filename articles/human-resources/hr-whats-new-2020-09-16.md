---
title: Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (16. september 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 16. septembri 2020 uusi või muutunud funktsioone.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3bb6b809560688a7849b60c15a01fd89038e843
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527430"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (16. september 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi või muutunud funktsioone. Muudatused rakenduvad versioonile number 8.1.3557. Sulgudes olevad numbrid mõne funktsiooni kõrval viitavad toenumbritele teenuses Lifecycle Services (LCS).

## <a name="included-in-this-release"></a>Väljalase hõlmab järgmisi funktsioone

-  [Salvestatud vaated – üldine kättesaadavus](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Lisateavet leiate teemast [Salvestatud vaated](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views). 

- Vormil **Ametikoha tegevus** on värskendatud dimensioonide võrgustik ja uus dialoog (469495).

- Kui seate **Human Resourcesi jagatud parameetrite** **täiustatud juurdepääsus** suvandi **Piira juurdepääsu töötaja teabele** väärtuseks jah, kuvatakse soodustuste vormides ainult asjakohaseid töötajaid (393384).

- Uued kalendri loomise suvandid üksuses **WorkCalendar** (477055).<br>- Vaikelõppaeg<br>-    Vaikealgusaeg<br>- Kas reede on tööpäev?<br>- Kas esmaspäev on tööpäev?<br>- Kas laupäev on tööpäev?<br>- Kas pühapäev on tööpäev?<br>- Kas neljapäev on tööpäev?<br>- Kas teisipäev on tööpäev?<br>- Kas kolmapäev on tööpäev?<br>- Töökalendri pühade ID

- Üksus **LeaveBankTransactionV1** sisaldab nüüd põhjusekoodi (477823).

- Nüüd saate salvestada tegevuse salvestisi (492923).

- Andmeid avaldatakse nüüd üksusest **HCMWorkerContactEntity** edukalt (427620).

- Kiirkaardil **Palk** kuvatakse nüüd vormis **Töötaja tegevused** töövõtja töötaja tüüpi (482494).

- Väljad **Tase** ja **Plaan** on nüüd kohustuslikud, kui seadistate suvandi **Põhipalk**. Kui jätate need väljad tühjaks, kuvatakse tõrketeade (482497).

- Väli **Plaani tüüp** on nüüd jaotises **Soodustused** ripploend (488768).

- Süsteemiadministraatorid saavad nüüd teatise, kui kohandatud väli kustutatakse rakendusest Human Resources (481408).

- Töötajaga lepingu lõpetamise protsessi käigus käitub rakendus Human Resources ootuspäraselt ja ei muuda valitud ettevõtet pärast näilist lukustumist (479877). 

- Juhatajad ei saa enam lisada numbriveerge isikupärastamise kaudu (485317).

- Juhatajad ei saa enam eemaldada andmevahemiku filtrit aeguvatest ID-numbritest (485321).

- Kui väli **Annab aru** on tühi, kuvatakse ametikoha üksikasjad selle kohal hõljudes ikkagi (433328).

- Töövõtjad saavad nüüd vaadata soodustuste plaani teavet töövõtja iseteenindusest (481676).

- Töövõtjad saavad nüüd vaadata kõiki registreeritud kursusi (429048).

- Nüüd saate piirata lehel **Professionaalsed sertifikaadid** vaatamissuvandeid. Saate piirata vaatamissuvandeid kõikidele peale praegusele juriidilisele isikule, töötaja oleku põhjal ja töötaja tüübi põhjal (451501). 


## <a name="in-preview"></a>Eelvaates

### <a name="human-resources-app-in-teams"></a>Rakendus Human Resources Teamsis

Töötajad saavad kuvada ja taotleda töölt eemaoleku aega rakenduses Microsoft Teams. Nad saavad suhelda botiga, et luua puhkusetaotlusi. Lisateabe saamiseks vt:

- [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 1 plaanis
- [Teamsi rakendus Human Resources](https://go.microsoft.com/fwlink/?linkid=2127841) rakenduse Human Resources dokumentatsioonis

### <a name="human-resources-app-in-teams-preview-features"></a>Rakendus Human Resources Teamsis eelversioonifunktsioonid
 
-  **Teatised**: vaba aja taotluste esitajaid ja kinnitajaid teavitatakse Teamsi rakenduses Human Resources. Kinnitajad saavad eemalolekuajataotlusi heaks kiita või tagasi lükata. Kui taotlus on heaks kiidetud või tagasi lükatud, teavitatakse sellest edastajat. Lisateabe saamiseks vt:
   - [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
   - [Teamsi rakenduse Human Resources teatiste lubamine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) rakenduse Human Resources dokumentatsioonis
   - [Üksikutele kasutajate jaoks Teamsi teatiste sisse- või väljalülitamine](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) Rakenduse Human Resources dokumentatsioonis
   - [Teamsi teatised](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) rakenduse Human Resources dokumentatsioonis
   - [Oma töörühma puhkusekalendri vaatamine](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis
 
- **Juhataja eemalolekuaja kalender**: juhatajad saavad vaadata oma otseste alluvate kinnitatud ja ootel eemalolekuaegu kalendrivaates. Selle vaate abil näeb hõlpsalt, millal nende meeskonnaliikmed töölt puuduvad. Lisateabe saamiseks vt:
   - [Töövõtja puhkuse ja puudumise kogemus rakenduses Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis
   - [Oma töörühma puhkusekalendri vaatamine](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) rakenduse Human Resources dokumentatsioonis

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks (477004)

Nüüd on saadaval uus suvand loendi **Mulle määratud tööüksused** paigutamiseks armatuurlaua parempoolsesse veergu. Selle muudatusega kuvatakse kõik tööüksused ja ülesandeloendid samas alas. Lubage see funktsioon, lülitades funktsioonihalduses sisse suvandi **Eelversioon – töövoo kasutuskogemuse täiustused**. Lisateavet eelvaatefunktsioonide sisselülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

See funktsioon pakub ka töövoosuvandeid, mis kuvatakse personalitoimingute vormidel. Töövoosuvandid kuvatakse kiireks juurdepääsuks ka tegevuse kiirkaardi kohal. Lisateabe saamiseks vt: 

- [Organisatsiooni ja personalijuhtimise töövoo kasutuskogemuse täiustused](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) Dynamics 365 2020. aasta väljalaskevoo 2 plaanis

![Mulle määratud tööüksused](./media/hr-workflow-work-items-assigned-to-me.png)

![Töövoo üksuste kiirjuurdepääs](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Puhkuste ja puudumiste kalender

See väljalase sisaldab täiendavaid kalendrisuvandeid puhkuste ja puudumiste kalendrite jaoks. Lisateavet leiate teemast [Meeskonna ja ettevõtte kalendrite kuvamine](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).

## <a name="coming-soon"></a>Peagi tulekul

### <a name="checklist-entities-included-in-common-data-service"></a>Common Data Service'is kaasatud kontroll-loendi üksused

Kontroll-loendi üksused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Common Data Service'is.

### <a name="benefits-management-reason-codes"></a>Soodustuste halduse põhjusekoodid

Soodustuste halduse põhjusekoodid kombineeritakse peagi Human Resourcesi olemasolevate põhjusekoodidega. Kui lõite soodustuste halduses põhjusekoodid, mis on pikemad kui 15 tähemärki, peate soodustuste halduse vormil **Põhjusekoodid** muutma põhjusekoodi nime nii, et see poleks pikem kui 15 tähemärki. Pärast nime värskendamist kuvatakse põhjusekood personalihalduse olemasoleva põhjusekoodi vormi all. See muudatus on saadaval tulevikus ja see ei mõjuta olemasolevaid funktsioone.

## <a name="see-also"></a>Vt ka

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2019. aasta väljalaskevoo 2 ülevaade](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]