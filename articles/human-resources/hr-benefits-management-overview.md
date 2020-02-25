---
title: Soodustuste haldamise ülevaade
description: Rakenduse Dynamics 365 Human Resources soodustuste haldamise eelvaatefunktsiooni eelvaade. Pakkuge oma töötajatele hõlpsasti kasutatava võrgukasutuskogemusega laiendatud soodustuste võimalusi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029459"
---
# <a name="benefits-management-overview"></a>Soodustuste haldamise ülevaade

[!include [banner](includes/preview-feature.md)]

Konkurentsivõime säilitamiseks peate pakkuma parimate töövõtjate meelitamiseks ja säilitamiseks rikkalikku soodustuste komplekti. Lisaks tavapärastele soodustustele, nagu ravi- ja hambaravikindlustus, võite tahta pakkuda ka laiendatud teenuseid, nagu abi adopteerimisel, vabaajaprogrammid ja toetus töörõivaste jaoks. Rakenduse Microsoft Dynamics 365 Human Resources soodustuste halduse eelvaatefunktsioon pakub paindlikku lahendust, mis toetab mitmesuguseid soodustuste võimalusi. Human Resources sisaldab ka hõlpsasti kasutatavat töövõtja kogemust, mis teie pakutavat tutvustab.

- Täiustatud soodustuse plaanid võimaldavad teil luua ja hallata ainulaadseid soodustuse plaane ning toetada keerukaid soodustuse tabeleid ja pesastatud tasemeid. Saate lihtsama töövõtja kogemuse jaoks hõlpsalt luua soodustusprogramme, kogumeid ja automaatse registreerimise reegleid.

- Paindliku krediidiga programmid võimaldavad proportsionaalselt jaotada pensioni- ja teiste elusündmuste toetusi.

- Ulatuslikud sobivusreeglid tagavad, et muudate õigeid soodustused kättesaadavaks õigetele töötajatele.

- Veebipõhine soodustuste registreerimine tagab teie töövõtjatele lihtsa kogemuse.

- Kvalifitseeritud elusündmuse töötlemine integreerib töötaja iseteenindusega ja toetab ka tulevasi elusündmusi.

Kui soovite ligipääsu demoandmetelel, peate oma liivakastikeskkonna uuesti juurutama.

Saate anda otsest tagasisidet või teatada probleemidest järgmisel meiliaadressil: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Soodustuste halduse teadaolevad probleemid

### <a name="eligibility-processing"></a>Sobivuse töötlemine

Kui käitate soodustusteks sobilikkust, mis kasutavad kindlustussummat 1–5 × palk, Protsent palgast ja Kindel summa, peate määrama kuupäeva **Soodustuse üksikasjad** väärtusele **Tööhõive alguskuupäev** suvandis **Tööhõive ajalugu**. Lisaks peate kaasama suvandid **Töötatud tunnid**, **Maksesagedus** ja **Aastase soodustuse palgasumma**. Kui töötajal on põhipalk, sisestage väärtused **Töötatud tunnid** ja **Maksesagedus**. Aastane palgasumma arvutatakse.  Kui töövõtja on kuupalgaline, ei pea te väärtust **Töötatud tunnid** sisestama. Soovitame uute töötajate loomisel sisestada esmalt põhipalk. Soodustuse üksikasjade kirje värskendamine navigeerige asukohta **Töötaja > Töötaja ajalugu > Tööhõive üksikasjad**. Muutke tööshõive alguskuupäeva.

### <a name="employee-self-service"></a>Töövõtja iseteenindus

Töövõtja summat ei arvutata elukindlustuse katvussumma värskendamisel. Näiteks kui töövõtjale pakutakse elukindlustuse plaani, saavad nad valida katvuse kuni 50 000 dollarit hinnaga 0,36 dollarit 1000 dollari kohta.  Kui töövõtja uuendab katvussummat, jääb töövõtja seotud kulu nulli.

Soodustuse plaani jaoks, mis lubab ainult ühe selle plaani tüübi valiku, kuvatakse kasutajale viga, kui nad proovivad plaanist pärast plaani valimist loobuda. Näiteks valib kasutaja meditsiiniplaani ja lisab selle oma ostukorvi. Seejärel valib kasutaja teise meditsiiniplaani jaoks suvandi **Loobu**. Kasutajale kuvatakse viga.

## <a name="enable-benefits-management"></a>Soodustuste halduse lubamine

Soodustuste haldus on eelvaatefunktsioon ja on saadaval ainult keskkondades **Liivakast**. Need artiklid kirjeldavad, kuidas eelvaatefunktsioone rakenduses Human Resources sisse lülitada. Lisaks annavad need teada, millised rakenduse Human Resources olemasolevad funktsioonid soodustuste haldamine asendab või keelab, kui lülitate soodustuste haldamise sisse.

- [Funktsioonide haldamine](hr-admin-manage-features.md)
- [Eelvaatefunktsioon: soodustuste haldus](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Soodustuste halduse konfigureerimine

Enne kui saate oma töötajate jaoks soodustuse plaane luua, tuleb teil plaanide valikud konfigureerida.

- [Soodustuste halduse parameetrite määramine](hr-benefits-setup-parameters.md)
- [Sobivusreeglite ja suvandite konfigureerimine](hr-benefits-setup-eligibility-rules.md)
- [Isikliku kontakti sobivuse suvandite konfigureerimine](hr-benefits-setup-contact-eligibility-options.md)
- [Katvussuvandite loomine](hr-benefits-setup-coverage-options.md)
- [Maksesageduste seadistamine](hr-benefits-setup-payment-frequencies.md)
- [Elusündmuste tüüpide konfigureerimine](hr-benefits-setup-life-event-types.md)
- [Plaani tüüpide loomine](hr-benefits-setup-plan-types.md)
- [Põhjusekoodide häälestamine](hr-benefits-setup-reason-codes.md)
- [Taseme koodide seadistamine](hr-benefits-setup-tier-codes.md)
- [Määrade konfigureerimine](hr-benefits-setup-rates.md)
- [Mahaarvamiste konfigureerimine](hr-benefits-setup-deductions.md)
- [Ootepäevade konfigureerimine](hr-benefits-setup-waiting-days.md)
- [Ooteaegade konfigureerimine](hr-benefits-setup-waiting-periods.md)
- [Ümardamisreeglite seadistamine](hr-benefits-setup-rounding-rules.md)
- [Tööhõive kategooriate loomine](hr-benefits-setup-employment-categories.md)
- [Tööhõive tüüpide seadistamine](hr-benefits-setup-employment-types.md)
- [Töövõtja iseteeninduse konfigureerimine](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Soodustuse plaanide loomine

Need artiklid näitavad, kuidas luua soodustuse plaane, kaasa arvatud kogumid ja paindliku krediidiga programmid.

- [Soodustuse plaanide seadistamine](hr-benefits-plans-setup.md)
- [Töötaja soodustuse plaanide loomine](hr-benefits-plans-worker.md)
- [Paindliku krediidiga programmide seadistamine](hr-benefits-plans-flex-credit-programs.md)
- [Tulevaste elusündmuste konfigureerimine](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Soodustuse plaanide töötlemine

Nende aktiivseks muutmiseks peate osasid muudatusi töötlema.

- [Registreerimise sobivuse töötlemine](hr-benefits-process-enrollment-eligibility.md)
- [Elusündmuste töötlemine](hr-benefits-process-life-events.md)
- [Elusündmuste muutuste töötlemine](hr-benefits-process-life-event-changes.md)
- [Elusündmuse sobivuse töötlemine](hr-benefits-process-life-event-eligibility.md)
- [Määrade muudatuste töötlemine](hr-benefits-process-rate-changes.md)

