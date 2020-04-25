---
title: Dynamics 365 Financei eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Finance'ist.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: aebce032d7d780b296ba74fea4467425a3cbe1a7
ms.sourcegitcommit: 4e9b3746790355f9f72bbfddc099c4065a49ad63
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/30/2020
ms.locfileid: "3175104"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Dynamics 365 Financei eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Finance'ist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Finance'i väljalaskest 10.0.12 eemaldatud või aegunud funktsioonid

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Poola SSRS-i aruanded: arvestatud käibemaksu register, sisendkäibemaksu register, EL-i koondkäibemaksu register – funktsiooni viide PL-00014

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Juriidiliselt pole vajalik.  |
| **Asendatud teise funktsiooniga?**   | Jah (Exceli vorming standardse auditifaili jaoks KM-i deklaratsiooniga – JPK_VDEK) |
| **Mõjutatud tootealad**         | Rakendus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegub 1. juuliks 2021, plaanime mitte enam toetada SSRS-i aruandeid: **arvestatud käibemaksu register, sisendkäibemaksu register, EL-i koondkäibemaksu register – funktsiooni viide PL-00014**. Selle asemel võetakse kasutusele Exceli vormingu standardse auditifaili näide koos KM-i deklaratsiooniga (JPK_VDEK). |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Finance'i väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid

### <a name="norwegian-standard-main-accounts"></a>Norwegian Standardi põhikontod

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Ümberkujundamine  |
| **Asendatud teise funktsiooniga?**   | Jah (asendatud ER-i vormingu rakendusekohaste parameetritega) |
| **Mõjutatud tootealad**         | Rakendus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates 2021. a 1. aprillist ei kavatse me enam toetada standardsete põhikontodega seotud funktsioone: viiteväli, seotud tabel, andmeüksus. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Finance'i väljalaskest 10.0.7 eemaldatud või aegunud funktsioonid

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Töövoo taotluse muutmise dialoogiboks ei sisalda enam kasutaja valiku ripploendit
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Muudetud funktsiooniks, mis sisaldab konto gruppide valikut.  |
| **Asendatud teise funktsiooniga?**   | Jah |
| **Mõjutatud tootealad**         | Töövoog |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegub: 1. detsembril 2020. Me ei plaani enam toetada Hiina kandetüüpide seadistust ilma konto gruppide valikuta. Lisateavet uue kujunduse kohta leiate teemast [Mis on uut versioonis 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest
Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
