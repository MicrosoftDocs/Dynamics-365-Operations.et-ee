---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (23. oktoober 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-10-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 66419d9093cff68aa6109b22ab57bcb46ac6c718
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772892"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-23-2019"></a>Mis on Dynamics 365 Talent-is uut või mida on muudetud (23. oktoober 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis
See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2569. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-30-for-finance-and-operations-apps"></a>Lahenduse Finance and Operations rakenduste platvormivärskendus 30

Lisateavet leiate teemast [Lahenduse Finance and Operations rakenduste platvormivärskenduse 30 uued või muudetud funktsioonid (november 2019)](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/whats-new-platform-update-30).

### <a name="remove-benefits-open-enrollment-preview-feature"></a>Soodustuste avatud registreerimise eelvaatefunktsiooni eemaldamine

Kooskõlas meie teadaandega ajaveebipostituses [Core HR-i strateegilised investeeringud parandavad tegevuse tõhusust](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) eemaldab Microsoft 18. oktoobril 2019 avalikust eelversioonist soodustuste avatud registreerimise funktsiooni. Selle asemel antakse tulevikus välja uued funktsioonid. Praegu avaliku eelversioonina saadaoleva soodustuste avatud registreerimise funktsiooni tootmiskeskkonnas kasutamist ei toetata.

### <a name="error-while-selecting-the-countryregion-on-the-worker-form-a-second-time-350294"></a>Tõrge töötaja riigi/regiooni teistkordsel valimisel (350294)

Selle nädala väljalaskega on parandatud probleem, mis ilmnes vormis **Töötaja** riigi/regiooni valimisel.

### <a name="financial-dimension-values-default-to-the-combination-display-field-when-do-not-allow-manual-entry-is-set-to-true-340097"></a>Finantsdimensiooni väärtused lähtestuvad vaikimisi kombinatsioon kuvamise väljale, kui atribuudi „Ära luba käsitsi sisestamist“ väärtuseks on määratud „Tõene“ (340097)

Kui seadistate selle muudatuse järel finantsdimensioone ja kasutate käsitsi sisestamise keelamise suvandit, lähtestab süsteem dimensiooniväärtuse vaikimisi õigesti väljale **Kombinatsiooni kuvamine**.

### <a name="new-relationship-types-should-be-added-to-relationship-lookup-in-the-personal-contacts-form-347691"></a>Uued seosetüübid tuleks lisada isiklike kontaktide vormi seoste otsingusse (347691)

See väljalase sisaldab uusi võimalusi uute seosetüüpide lisamiseks tabelis **Seosetüübid** ja kajastab neid muudatusi isiklike kontaktide seoste otsingus.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-379599"></a>Kohandatud väljade täiendavad loendiväärtused ei kajastu teenuses Common Data Service (379599)

Selle nädala väljalaskes teenusega Common Data Service juba sünkroonitud olemasolevale kohandatud väljale uue loendiväärtuse lisamise korral kuvatakse nüüd uued komplekteerimislehe väärtused pärast üksusele muudatuste rakendamist.

### <a name="on-the-terms-of-employment-page-all-employees-terms-of-employment-appear-after-selecting-open-in-excel-348073"></a>Tööhõivetingimuste lehel kuvatakse pärast käsu „Ava Excelis“ valimist kõigi töötajate tööhõivetingimused (348073)

Selle väljalaskega avatakse Excelis ainult valitud töötajate tööhõivetingimused. Samuti võetakse arvesse kogu ettevõtte turvet.

### <a name="the-association-between-the-work-calendar-holiday-entity-and-the-work-calendar-entity-is-missing-in-common-data-service-324178"></a>Töökalendri puhkuseüksuse ja töökalendri üksuse vaheline seos puudub teenuses Common Data Service (324178)

See seos on lisatud selle väljalaskega. See muudatus võimaldab töövõtja tööpäevade kuvamist PowerAppsis. 

### <a name="error-when-using-employee-self-service-workflows-with-configurable-hierarchies-370132"></a>Tõrge töövõtjate iseteeninduslike töövoogude kasutamisel koos konfigureerivate hierarhiatega (370132)

Selles väljalaskes on saadaval selgem teave selle kohta, kuidas konfigureerida töövoogusid konfigureeritavate hierarhiate kasutamise korral. 

### <a name="system-allows-creation-of-new-positions-where-the-available-for-assignment-date-is-earlier-than-the-activation-date-340103"></a>Süsteem võimaldab luua uusi positsioone, mille atribuudi „Määramiseks saadaval“ kuupäev on aktiveerimiskuupäevast varasem (340103)

See muudatus kuvab hoiatuse, kui atribuudi **Määramiseks saadaval** kuupäev on enne positsiooni atribuudi **Aktiveerimine** kuupäeva.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.

### <a name="feature-management-workspace"></a>Funktsioonihalduse tööruum

Igale väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduskeskkond pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

Lisateavet tulevaste funktsioonihaldusega seotud muudatuste kohta vt teemast [Funktsioonihalduse ülevaade](https://docs.microsoft.com/en-us/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
