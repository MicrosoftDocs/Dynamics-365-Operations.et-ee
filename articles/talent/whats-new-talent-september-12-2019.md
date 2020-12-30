---
title: Mis on Dynamics 365 for Talent-is uut või mida on muudetud (10. september 2019)
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 for Talenti uusi või muutunud funktsioone.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460917"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Mis on Dynamics 365 for Talent-is uut või mida on muudetud (10. september 2019)

Selles teemas kirjeldatakse Dynamics 365 for Talenti uusi või muutunud funktsioone.

## <a name="changes-in-attract"></a>Muutused Attractis

### <a name="candidate-e-mail-login"></a>Kandidaadi e-posti logimine

Kandidaadid saavad nüüd kasutada mis tahes meiliaadressi, et luua konto ja logida sisse Talenti karjäärisaidile, et kandideerida töödele ja vaadata oma avalduse olekut. See on lisaks juba võimalusele Talenti karjäärisaidile oma sotsiaalvõrgustike kontodega või oma organisatsiooni mandaatidega sisse logida.

### <a name="job-activation-and-posting"></a>Töö aktiveerimine ja sisestamine

Oleme teinud mõned muudatused töö aktiveerimisele ja sisestamisele. Peate aktiveerima tööd enne nende sisestamist Talenti karjäärisaidile või mis tahes välistele töösaitidele, sealhulgas LinkedIni või Broadbean.

## <a name="changes-in-onboard"></a>Muutused Onboardis

See väljaanne sisaldab väiksemaid vigadeparandusi rakendusele Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Core HR-i muudatused

Jaotises kirjeldatud muudatused rakenduvad järgunumbrile 8.1.2482. Sulgudes olevad numbrid mõnedes pealkirjades viitavad toenumbritele teenuses Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Te võite lubada eelvaate funktsioone liivakasti- ja testkeskkondades

Kui valmistate ette uue Talenti eksemplari, saate eksemplari tüübiks määrata Tootmine või Liivakast. Liivakasti tüübi eksemplarid võimaldavad uute funktsioonide varajast katsetamist. Kui soovite mõne olemasoleva eksemplari Liivakasti tüübile värskendada, võtke muudatuse taotlemiseks ühendust Toega.

Lisateavet muudatuste avaldamise kohta vt teemast [Talenti ettevalmistamine](./provisioning-talent.md).

### <a name="platform-update-29"></a>Platvormivärskendus update 29

Platvormivärskenduse 29 kohta lisainfo saamiseks vt [Dynamics 365 for Finance and Operations platvormivärskenduse 29 (oktoober 2019) funktsioonide eelvaade](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Uus töö põhiüksus on saadaval andmete halduse raamistikus (347202)

Selle väljalaskega on andmete importimiseks/eksportimiseks saadaval uus töö põhiüksus. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Töötaja täpsem turvapoliitika kuvab Positsioonide Hierarhias positsiooni valesti (354868)

Selle väljalaskega ei saa ametikohti enam kuvada „tühja“ töötajaga, kui kasutaja on juurdepääsu piiratud.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Töö vormi sulgemise kast ei sulgu teatud olukordades (342467)

See väljalase sisaldab muudatust, mis võimaldab töö vormi sulgeda kõigil juhtudel.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Töötaja kirje uus juhtum on lukustatud Personalijuhi rollile (337111)

Selle muudatusega ei ole juhtumite halduse vorm enam lukustatud, kui sellele minnakse töötaja vormilt.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Töösuhte lõpuaeg on alati vaikimisi 23:59:59 (351492)

Selle muudatusega saate töötamise aega muuta mõneks muuks ajaks kui 23:59:59, kui lõpetate töösuhte käsitsi.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Töötasu koodi aegumiskuupäeva ei saa andmehalduse kaudu seadistada (336604)

Selles väljalaskes saate seadistada aeguvad töötasu koodid üksuses **PayrollWorkerPositionEarningCodeEntity**.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Töötaja arenemise analüütiline aruanne ei kuva andmeid (348737)

Selle nädala väljalaskes on töötajate oskuste analüüsi uuendatud, et anda täpset aruandlust.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Töösuhte kuupäeva/kellaaja tingimused ei ole vaikimisi päeva alguses (349101)

Selle muudatusega on alguskuupäev/-kellaaeg nüüd vaikimisi päeva alguses ja lõppkuupäev/-kellaaeg vaikimisi päeva lõpus.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Töötaja tegevuse vormi töösuhte lõppkuupäeva muutmine kuvab tõrke (354092) 

See muudatus parandab probleemi, kui muudetakse töösuhte lõppkuupäeva töötaja tegevuse raames.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Palkamise kontroll-loendite rakendamine ettevõtetes (338433)

See väljalase pakub nüüd võimalust rakendada kontroll-loendit töötajatele, kes töötavad juriidilistes isikutes, mis erinevad sisselogitud juriidilisest isikust.

## <a name="in-preview"></a>Eelvaates

### <a name="streamlined-employee-entry-and-navigation"></a>Sujuvam töötajate sisestamine ja navigeerimine

See funktsioon on nüüd saadaval liivakasti keskkondades. Selle funktsiooni sisselülitamiseks liikuge valikule **Süsteemi administreerimine > Lingid > Häälestus > Süsteemiparameetrid > Eelvaate funktsioonid**. Valige **Täiustatud töötajate vorm ja navigeerimine**. See võimaldab neid muudatusi kõigile kasutajatele. Võite selle suvandi igal ajal välja lülitada.

Lisateavet leiate teemast [Sujuv töötajate sisestamine ja navigeerimine](./streamlined-employee-entry.md).
