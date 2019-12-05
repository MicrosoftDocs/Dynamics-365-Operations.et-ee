---
title: Mis on Dynamics 365 Talent-is uut või mida on muudetud (8. oktoober 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 496603731eb343a64be1e8d9482ac8d42e6aa79a
ms.sourcegitcommit: 7ef9e61f0388b5241894d40ff39f84a112232a5f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694402"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a>Mis on Dynamics 365 Talent-is uut või mida on muudetud (8. oktoober 2019)

[!include [banner](includes/banner.md)]

Selles teemas kirjeldatakse Microsoft Dynamics 365 Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Selles jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2542. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a>Soodustuste avatud registreerimise eemaldamine avalikust eelversioonist

Kooskõlas meie teadaandega ajaveebipostituses [Core HR-i strateegilised investeeringud parandavad tegevuse tõhusust](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) eemaldab Microsoft 18. oktoobril 2019 avalikust eelversioonist soodustuste avatud registreerimise funktsiooni. Selle asemel antakse tulevikus välja uued funktsioonid. Praegu avaliku eelversioonina saadaoleva soodustuste avatud registreerimise funktsiooni tootmiskeskkonnas kasutamist ei toetata. 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a>Teenuse Common Data Service integratsioon on nüüd uute ettevalmistamiste puhul vaikimisi välja lülitatud (343675)
 
Uute keskkondade ettevalmistamisel on teenuse Common Data Service integratsioon nüüd välja lülitatud. Lisateavet vt [Teenuse Common Data Service integratsiooni konfigureerimine](hr-common-data-service-integration.md).

### <a name="streamlined-employee-entry-and-navigation"></a>Sujuvam töötajate sisestamine ja navigeerimine

Töövõtja sisestus ja navigeerimine on nüüd saadaval kõikides keskkondades. Funktsiooni sisselülitamiseks valige **Süsteemihaldus \> Lingid \> Seadistus \> Süsteemi parameetrid \> Eelvaatefunktsioonid** ja valige **Täiustatud töötajate vorm ja navigeerimine**. Funktsioon lülitatakse seejärel sisse kõigi kasutajate jaoks. Võite selle suvandi igal ajal välja lülitada.

Lisateavet vt teemast [Sujuvam töötajate sisestamine ja navigeerimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry), rakenduse Dynamics 365: 2019. aasta väljalaskevoo plaanis 2.

### <a name="attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a>Attract ja Onboard loovad Core HR-is passiivseid töötajaid (380517)

Selle nädala väljaanne parandab probleemi, mille korral Attract ja Onboard loovad Core HR-is passiivseid töötajaid.

### <a name="the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a>Töövoog nurjub, kui haldur on töövõtja töösuhte lõpetamise ajal teise ettevõttesse sisse logitud (346852)

Töövoog ei saa enam nurjuda selle juriidilise isiku põhjal, millesse haldur on sisse logitud.

### <a name="missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a>Puuduv teave üksuse HcmOnboardingWorkerChecklistTaskEntity kohta (349591)

See väljalase sisaldab täiendavat teavet üksuse **HcmOnboardingWorkerChecklistTaskEntity** kohta. Järgmisena on toodud mõned näited.

- **Grupi nimi**, kui määratud tüüp on **grupp**
- **Töövõtja nimi**, kui määratud tüüp on **töövõtja**
- **Juhataja nimi**, kui määratud tüüp on **juhataja**

### <a name="entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a>Üksused pole teenuse Common Data Service halduses tähestikulises järjekorras (377414)

Üksused on lehel **CDS-i haldus** nüüd tähestikulises järjekorras.

### <a name="changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a>Tulevase kuupäevaga töösuhte tüübi muutmine ei luba ametikoha määramist (339958)

See muudatus lubab ametikoha määramist, kui muudetakse töötajatüüpe (nt töövõtjast peatöövõtjaks).

### <a name="updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a>Teenuse Common Data Service puhkuse pangakande üksuse värskendamine loob rakenduses Talent uue kirje (352938)

Puhkuse kanne uuendatakse nüüd teenuses Common Data Service puhkuse pangakannete uuendamise korral.

### <a name="the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a>Tagasisideüksuste manuste pealkirjades kuvatakse tagasiside kirjeldus (343765)

Tagasiside kirjeldust ei kuvata enam manuse pealkirjas.

### <a name="compensation-workflow-comments-field-shows-incorrect-content-339297"></a>Kompensatsiooni töövoo kommentaaride väljal on kuvatud vale sisu (339297)

See muudatus näitab välja **%HcmActionState.HcmWorkerActionComment.Comments%** sisu.

### <a name="workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a>WorkCalendarEntity ja WorkCalendarDayEntity ei ole OData kaudu kättesaadavad (376329)

Selles väljalaskes on **WorkCalendarEntity** ja **WorkCalendarDayEntity** nüüd avatud andmeprotokolli (OData) kaudu saadaval.

### <a name="hcmworkerentity-is-slow-when-odata-is-used-375221"></a>HCMWorkerEntity on aeglane, kui kasutatakse teenust OData (375221)

Muudatused parandavad üksuse **HCMWorkerEntity** jõudlust rakenduse Microsoft Excel töövihiku koostaja kasutamise korral.

### <a name="manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a>Juhi jõudluse töölehe sisestus kuvab tõrke pärast jõudluse töölehe kustutamist ja uue loomist (336061)

See väljalase parandab probleemi, mis ilmneb pärast ühe jõudluse töölehe kustutamist juhul, kui pärast seda luuakse kohe uus tööleht. See parandus muudab juhi iseteeninduse käitumist.

## <a name="coming-soon"></a>Peagi tulekul

### <a name="print-performance-reviews"></a>Jõudluse ülevaadete printimine

Vt [Jõudluse ülevaadete printimine](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews), rakenduse Dynamics 365 2019. aasta väljalaskevoo plaanis 2.
