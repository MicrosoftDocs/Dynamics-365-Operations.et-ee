---
title: Soodustuste halduse ülevaade
description: Rakenduse Dynamics 365 Human Resources soodustuste haldamise funktsiooni eelvaade. Pakkuge oma töötajatele hõlpsasti kasutatava võrgukasutuskogemusega laiendatud soodustuste võimalusi.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ae4270f3185f8795753ecdb209515ecd6e86486
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112267"
---
# <a name="benefits-management-overview"></a>Soodustuste haldamise ülevaade

Konkurentsivõime säilitamiseks peate pakkuma parimate töövõtjate meelitamiseks ja säilitamiseks rikkalikku soodustuste komplekti. Lisaks tavapärastele soodustustele, nagu ravi- ja hambaravikindlustus, võite tahta pakkuda ka laiendatud teenuseid, nagu abi adopteerimisel, vabaajaprogrammid ja toetus töörõivaste jaoks. Rakenduse Microsoft Dynamics 365 Human Resources soodustuste haldus pakub paindlikku lahendust, mis toetab mitmesuguseid soodustuste võimalusi. Human Resources sisaldab ka hõlpsasti kasutatavat töövõtja kogemust, mis teie pakutavat tutvustab.

- Täiustatud soodustuse plaanid võimaldavad teil luua ja hallata ainulaadseid soodustuse plaane ning toetada keerukaid soodustuse tabeleid ja pesastatud tasemeid. Saate lihtsama töövõtja kogemuse jaoks hõlpsalt luua soodustusprogramme, kogumeid ja automaatse registreerimise reegleid.

- Paindliku krediidiga programmid võimaldavad proportsionaalselt jaotada pensioni- ja teiste elusündmuste toetusi.

- Ulatuslikud sobivusreeglid tagavad, et muudate õigeid soodustused kättesaadavaks õigetele töötajatele.

- Veebipõhine soodustuste registreerimine tagab teie töövõtjatele lihtsa kogemuse.

- Kvalifitseeritud elusündmuse töötlemine toetab tulevasi elusündmusi.

Kui soovite ligipääsu demoandmetelel, peate oma liivakastikeskkonna uuesti juurutama.

## <a name="enable-benefits-management"></a>Soodustuste halduse lubamine

Selles teemas kirjeldatakse, kuidas funktsioone rakenduses Human Resources sisse lülitada. Lisaks annab see teada, millised rakenduse Human Resources olemasolevad funktsioonid soodustuste haldamine asendab või keelab, kui lülitate soodustuste haldamise sisse.

> [!IMPORTANT]
> Keskkonnas **Tootmine** ei saa soodustuste haldust keelata, kui olete selle lubanud. Enne soodustuste halduse keskkonnas **Tootmine** lubamist soovitame lubada ja testida soodustuste haldust keskkonnas **Liivakast**. Olemasolevate pärandsoodustuse funktsioonide ja uute pärandsoodustuse funktsioonide vahel on olulisi erinevusi, mis vajavad täiendavat seadistamist ja mida tuleks enne tootmise alustamist testida.

- [Funktsioonide haldamine](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Töötaja teabe konfigureerimine

Enne eeliste andmist töötajatele peate sisestama nõutava teabe. Peate töötaja lisama **põhipalgaplaanile** nende töötamise alguskuupäeval ning vormi **Töötaja** väljal **Tööhõive üksikasjad** peate valima **Soodustuse maksesagedus**.

Kui teil on töötaja, kes saab lisahüvitust (nt komisjonitasud), saate lisada summa **Soodustuste aastane palgasumma** töövõtja kirjesse. Human Resources kasutab summat **Soodustuse aastane palgasumma** kindlustussummade määramiseks aastase põhipalga summa asemel. **Soodustuste aastane palgasumma** peab kehtima alates töövõtja alustamise kuupäevast või soodustuse perioodi algusest, olenevalt sellest, kumb on hilisem. Kui töövõtja kohta kirjendatakse nii põhipalk soodustuste aastane palgasumma, kasutatakse kindlustuse summade määramisel soodustuste aastast palgasummat.

Kui loote soodustusplaani, mis kasutab sool või vanusel põhinevaid määrasid, peate soodustuse maksumuse arvutamiseks sisestama töötaja sünnikuupäeva ja soo.

## <a name="configure-benefits-management"></a>Soodustuste halduse konfigureerimine

Enne kui saate oma töötajate jaoks soodustuse plaane luua, tuleb teil plaanide valikud konfigureerida.

- [Soodustuste halduse parameetrite määramine](hr-benefits-setup-parameters.md)
- [Sobivusreeglite ja suvandite konfigureerimine](hr-benefits-setup-eligibility-rules.md)
- [Isiklike kontaktide sobivuse suvandite konfigureerimine](hr-benefits-setup-contact-eligibility-options.md)
- [Katvuse suvandite loomine](hr-benefits-setup-coverage-options.md)
- [Maksesageduste häälestamine](hr-benefits-setup-payment-frequencies.md)
- [Elusündmuse tüüpide konfigureerimine](hr-benefits-setup-life-event-types.md)
- [Plaani tüüpide loomine](hr-benefits-setup-plan-types.md)
- [Põhjusekoodide häälestamine](hr-benefits-setup-reason-codes.md)
- [Järgukoodide häälestamine](hr-benefits-setup-tier-codes.md)
- [Määrade konfigureerimine](hr-benefits-setup-rates.md)
- [Mahaarvamiste konfigureerimine](hr-benefits-setup-deductions.md)
- [Ootepäevade konfigureerimine](hr-benefits-setup-waiting-days.md)
- [Ooteperioodide konfigureerimine](hr-benefits-setup-waiting-periods.md)
- [Ümardamisreeglite häälestus](hr-benefits-setup-rounding-rules.md)
- [Töötajate kategooriate loomine](hr-benefits-setup-employment-categories.md)
- [Tööhõive tüüpide seadistamine](hr-benefits-setup-employment-types.md)
- [Töövõtja iseteeninduse konfigureerimine](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Soodustuse plaanide loomine

Need artiklid näitavad, kuidas luua soodustuse plaane, kaasa arvatud kogumid ja paindliku krediidiga programmid.

- [Soodustusplaanide seadistamine](hr-benefits-plans-setup.md)
- [Paindkrediidi programmide seadistamine](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Soodustusplaanide töötlemine

Nende aktiivseks muutmiseks peate osasid muudatusi töötlema.

- [Registreerimise sobivuse töötlemine](hr-benefits-process-enrollment-eligibility.md)
- [Elusündmuste töötlemine](hr-benefits-process-life-events.md)
- [Elusündmuste muutuste töötlemine](hr-benefits-process-life-event-changes.md)
- [Elusündmuse sobivuse töötlemine](hr-benefits-process-life-event-eligibility.md)
- [Määrade muudatuste töötlemine](hr-benefits-process-rate-changes.md)

