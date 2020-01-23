---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (29. oktoober 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: e2d79ee9e182df4a4efe65beb685567b1e7446ce
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897438"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a>Mis on Dynamics 365 Talent-is uut või mida on muudetud (29. oktoober 2019)

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2586. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a>Ilma rollideta osapoolte kustutamine peaks vaikimisi olema sees (371233)

Talentis uut keskkonda ette valmistades on suvand **Ilma eksisteerivate rollideta osapoolte kustutamine** vaikimisi sisse lülitatud. Töötaja kustutamisel ei eemaldata töötajaga seotud osapoolt, välja arvatud juhul, kui see säte on sisse lülitatud. See muudatus piirab globaalses aadressiraamatus kattuvaid kirjeid, kui peate töötajaid importima, muutma või uuesti importima.

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a>Puhkusetaotluste mustandeid ja tühistusi peaks olema võimalik Common Data Service’is kustutada (376999)

Selle muudatusega saate nüüd kustutada puhkusetaotlusi, mille olek on Common Data Service’is **Mustand** või **Tühistatud**.

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Täiendavaid kohandatud väljade loendi väärtuseid ei kajastata Common Data Service’is pärast rakendusnupu vajutamist kohandatud väljade vormil (379599)

Kui lisate uue loendi väärtused olemasolevale kohandatud väljale, mis on juba Common Data Service’iga sünkroonitud, on need nüüd Common Data Service’is saadaval pärast muudatuste rakendamist vormil **Kohandatud väljad**.

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a>Värbamise kontroll-loendi rakendamine juriidilistele isikutele, kui eksisteerib rohkem kui üks töösuhe (371270)

Selle nädala väljaandes saate rakendada kontroll-loendeid töötajatele, kellel on suvandis **Töötaja vorm > Kontroll-loendid** rohkem kui üks töösuhe.

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a>Soodustuste avatud registreerimise eelvaatefunktsioon on eemaldatud

Kooskõlas meie teadaandega ajaveebipostituses [Core HR-i strateegilised investeeringud parandavad tegevuse tõhusust](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence), eemaldas Microsoft avalikust eelversioonist soodustuste avatud registreerimise funktsiooni. Tulevikus antakse välja uued funktsioonid. Soodustuste avatud registreerimise funktsiooni tootmisest kasutamist ei toetata.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.

### <a name="feature-management-workspace"></a>Funktsioonihalduse tööruum

Igale väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduskeskkond pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

Lisateavet tulevaste funktsioonihaldusega seotud muudatuste kohta vt teemast [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
