---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (5. november 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
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
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c4068cf81782d2f9559179b91da31e049c006059
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527116"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a>Mis on Dynamics 365 Talent-is uut või mida on muudetud (5. november 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Selles teemas kirjeldatakse Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2598. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="copy-a-core-hr-instance"></a>Core HR-i eksemplari kopeerimine

Selle nädala väljaandes saate kasutada portaali Microsoft Dynamics Lifecycle Services (LCS), et kopeerida Microsoft Dynamics 365 Talent: Core HR-i andmebaas liivakastikeskkonda. Kui teil on teine liivakastikeskkond, saate kopeerida andmebaasi ka sellest keskkonnast sihtkohaks olevasse liivakastikeskkonda. Lisateabe saamiseks vt:

- [Laiem keskkonnahaldus](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) Dynamics 365: 2019 väljalaskevoo plaanis 2.

- [Core HR-i eksemplari kopeerimine](hr-copy-instance.md) Talenti dokumentatsioonis

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a>Common Data Service’i integratsiooni pakett-töid ei looda, kui Common Data Service’i integratsioon on lubatud (388030)

See muudatus loob pakett-tööd Common Data Service’iga integreerimiseks kui see on lubatud.

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a>HcmPersonImageEntity ei muuda üleslaadimisel inimese pildi suurust (369469)

Selle nädala väljaanne muudab viisi, kuidas andmehalduse kaudu importimisel muudetakse paremaks jõudluseks piltide suurust.

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a>Ametikoha määramiseks saadaval kuupäev võib olla varasem kui aktiveerimise kuupäev (340103)

Selle muudatusega kuvatakse hoiatus, kui valite **Määramiseks saadaval kuupäeva**, mis on varasem kui ametikoha **Aktiveerimise kuupäev**.

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a>Kompenseerimise muutmise taotlust ei saa töövõtja iseteeninduses etapipõhiste plaanide jaoks luua (376872)

See väljaanne parandab tõrke kompensatsiooni muutmise taotlemisel läbi töövõtja iseteeninduse etapipõhiste plaanide jaoks. 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a>Põhjuse koodi ei sünkroonita Common Data Service’iga, kui kirjeldus on pikem kui 30 tähemärki, Core HR lubab 60 (352682)

Selle muudatusega värskendatakse Common Data Service’is põhjuse koode, millel on rohkem kui 30 tähemärki. Common Data Service’is tehtud muudatused kajastuvad Talentis.

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a>Aadressi integratsioon Talent-ist Finance and Operations-i (351961)

See väljaanne lahendab probleemi, kus Talent-is värskendatud aadresse ei värskendatud Finance and Operations rakenduses. Aadressiploki muudatusi nüüd värskendatakse.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.

### <a name="feature-management-workspace"></a>Funktsioonihalduse tööruum

Igale väljalaskele lisatakse funktsioone ja nende uuendusi. Funktsioonihalduskeskkond pakub tööruumi, kus saate vaadata igale väljalaskele lisatud funktsioonide loendit. Vaikimisi on uued funktsioonid välja lülitatud. Saate kasutada tööruumi funktsioonide sisselülitamiseks ja nende dokumentatsiooni vaatamiseks.

Lisateavet tulevaste funktsioonihaldusega seotud muudatuste kohta vt teemast [Funktsioonihalduse ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).
