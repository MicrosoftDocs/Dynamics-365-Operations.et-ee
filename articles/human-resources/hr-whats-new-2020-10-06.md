---
title: Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (6. oktoober 2020)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Human Resourcesi 6. oktoobri 2020 uusi või muutunud funktsioone.
author: jcart1106
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 090533a4391488f4ec0929dd4866e55a478ee6e639563ad37a6819592e91b23c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739199"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Mis on Dynamics 365 Human Resources-is uut või mida on muudetud (6. oktoober 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Human Resourcesi uusi, muutunud või peatselt tulevaid funktsioone. Meie värskendamisprotsessi ja graafiku kohta lisateabe saamiseks vt teemat [Värskendamisprotsess](hr-admin-setup-update-process.md).

Lisateavet uute funktsioonide ja nende eeldatava üldise kättesaadavuse kuupäevade kohta leiate teemast [Dynamics 365 Human Resourcesi 2020. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Selles väljalaskes

See väljaanne sisaldab järgmisi uusi funktsioone ja veaparandusi. Muudatused rakenduvad versioonile number 8.1.3636.

### <a name="new-features"></a>Uued funktsioonid

Selle väljalaskega tuleb üldiselt kättesaadavaks järgmine funktsioon.

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Täiendav ülevaade puhkusekalendritest | [Täiendava ülevaate andmine puhkusekalendrite vaadetest](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Meeskonna ja ettevõtte kalendri kuvamine](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Veaparandused

See väljalase hõlmab järgmisi veaparandusi.

>[!NOTE]
> Meie eesmärk on edastada teile see teave esimesel võimalusel. Seda teemat võidakse värskendada, et lisada sellesse versioonijärku pärast selle teema esialgset avaldamist tehtud veaparandusi.

| Väljaande number | Väljasta | Kirjeldus |
| --- | --- | --- |
| 448806 | **Vaike-ID-tüüp** eksporditakse HCM-i parameetrites üksusena **RecID** | Selle Human Resourcesi parameetrite üksuse muudatusega lisatakse täiendav veerg, kus kuvatakse **Vaike-ID tüüp**. |
| 492923 | Tegevuse salvestisi ei salvestata Lifecycle Servicesis (LCS) | Tegevuse salvestised saab nüüd LCS-i salvestada. |
| 429950 | Põhipalk ei aegu õigesti ametikoha muutmisel | Töötaja ametikoha muutmisel lehel **Töötaja ülekandmine** määrati kompensatsiooni lõpetamise kuupäev üks päev enne ametikoha lõppu. Kompensatsiooni lõppkuupäev on nüüd sama, mis ametikoha lõppkuupäev. |
| 467214 | **Põhipalga analüüs** kuvatakse ainult siis, suvandi **Palgamäära teisendamise nimi** väärtuseks on seatud **Iga-aastane** | Kompensatsiooni analüüsis ei kuvatud teisi põhipalga maksmise sagedusi, kui **Iga-aastane**. Selle värskendusega kasutab kompensatsiooni analüüs nüüd kõiki maksmise sageduse teisendusi. Kui käitate aruandeid väärtuste **Tunnitasu** või **Palk** alusel, lisatakse filtrisse **Palk** ainult tunnitasu perioodi kasutavad maksmise sageduse teisendused. Filtrisse **Tunnitasu** lisatakse ainult perioodi **Tunnitasu** maksmise sagedused. |
| 482464 | Vaates **Üksikasjad** suvandi **Ülevaated** kuvamisel ei muudeta ruudustiku vaadet pärast filtri rakendamist | Pärast filtri rakendamist kuvatakse ruudustiku ülevaated ootuspäraselt. |
| 483184 | Human Resources ei loo puhkuse viitvõlgasid, kui valite **Taseme alusena** väärtuse **Korrigeeritud alguskuupäev** kirjes **Puhkuse registreerimine** |**Kohandatud alguskuupäev** asustatakse ja seda kasutatakse puhkuse viitvõlgade loomisel.  |
| 509731 | Tulevase lepingu lõpetamise kuupäevaga töötaja vaba aja taotlusel ilmneb probleem, kui ta taotleb vaba aega pärast lõpetamise kuupäeva | Vaba aja taotlusi saab nüüd esitada tulevase lepingu lõpetamise kuupäevaga töötajatele, kui taotlus on enne lõpetamise kuupäeva. |
| 510716 | Kompensatsiooni analüüs sisaldab nii mees- kui ka naissoost töötajaid üksuses **Meeste keskmine tunnipalk** | Kompensatsiooni analüüsis sisaldas **Kompensatsiooni demograafiline analüüsi** jaotis **Meeste keskmine palk** ka naiste keskmist palka. Nüüd sisaldab see ainult meestöötajaid. |
| 511348 | Soodustuste iseteenindus peaks kuvama soodustusplaane, mis kehtivad tänasest soodustuse perioodi lõpuni | Lehel **Soodustuste registreerimine** kuvati töövõtjatele aegunud soodustustplaane. Selle parandusega eemaldatakse need plaanid. |
| 512706 | Seadistage järgmised väljad kirjutuskaitstuks:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Dimensiooni üksikasjade nupud **Lisa** ja **Eemalda** olid pärast tegevuse lõpuleviimist valesti lubatud. See lehe **Ametikoha tegevuse üksikasjad** värskendus keelab väljade redigeerimise pärast tegevuse lõpuleviimist. |

## <a name="in-preview"></a>Eelvaates

Järgmised uued funktsioonid on eelversioonis. Lisateavet funktsioonide sisse- või väljalülitamise kohta vt teemast [Funktsioonide haldamine](hr-admin-manage-features.md).

| Funktsioon | Väljaandmisplaan | Dokumentatsioon |
| --- | --- | --- |
| Rakendus Human Resources Microsoft Teamsis | [Töövõtja puhkuste ja puudumiste kogemus Microsoft Teamsis](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Rakendus Human Resources Teamsis](./hr-admin-teams-leave-app.md)<br>[Puhkusetaotluste haldamine Teamsis](hr-teams-leave-app.md) |
| Täiustatud töövoo taotlused ja kinnitused | [Organisatsiooni ja personalihalduse töövoo kasutuskogemuse täiustused](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfiguratsiooni suvand loendi „Mulle määratud tööüksused” paigutamiseks](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Rakenduses Dataverse for Human Resources saadaolevad virtuaalüksused | [Dynamics 365 Human Resourcesi põhiandmete laiendamine Dataverse'is](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse'i virtuaalüksuste konfigureerimine](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Peagi tulekul

Järgmised uued funktsioonid on planeeritud tulevaste väljaannete jaoks:

- **Dataverse'i kontroll-loendi üksused**: kontroll-loendi ükdused Kasutuselevõtt, Kõrvaldamine, Ülekanded ja Äriprotsessid on peagi saadaval Dataverse'is.

- **Soodustuste halduse põhjusekoodid**: soodustuste halduse põhjusekoodid kombineeritakse peagi Human Resourcesi olemasolevate põhjusekoodidega. Kui lõite soodustuste halduses põhjusekoodid, mis on pikemad kui 15 tähemärki, peate soodustuste halduse vormil **Põhjusekoodid** muutma põhjusekoodi nime nii, et see poleks pikem kui 15 tähemärki. Pärast nime värskendamist kuvatakse põhjusekood personalihalduse olemasoleva põhjusekoodi vormi all. See muudatus on saadaval tulevikus ja see ei mõjuta olemasolevaid funktsioone.

- **Kohandatud lingid juhi iseteeninduses**: juhtide toetamiseks laiendame juhi iseteeninduse võimalusi. Lisame kohandatud linkide lisamise võimaluse vahekaardil **Minu meeskond**. See funktsioon sarnaneb kohandatud linkide funktsiooniga töövõtja iseteeninduse **Minu teabe vahekaardil**. Lisateavet leiate teemast [Kohandatud lingid juhi iseteeninduses](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Plaanitud funktsioonide täieliku loendi ja nende kavandatud väljaannete kohta leiate teavet teemast [Dynamics 365 Human Resourcesi 2019. aasta 2. väljalaskevoo ülevaade](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Lisaressursid

[Mis on uut või mida on muudetud rakenduses Human Resources?](hr-admin-whats-new.md)</br>
[Dynamics 365 Human Resourcesi 2020. aasta väljalaskevoo 2 ülevaade](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Värskendamisprotsess](hr-admin-setup-update-process.md)</br>
[Funktsioonide haldamine](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]