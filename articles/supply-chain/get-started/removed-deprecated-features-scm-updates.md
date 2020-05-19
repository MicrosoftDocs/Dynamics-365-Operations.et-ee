---
title: Dynamics 365 Supply Chain Managementi eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Supply Chain Managementis.
author: kamaybac
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7502cd16129431d41d152508fb3b49ff85a5a9f8
ms.sourcegitcommit: f1db998ecfccca660eb15cc2739b12c8463fa54d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2020
ms.locfileid: "3331244"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Managementi eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema uuendatakse, kui uued eemaldatud või aegunud funktsioonid on Dynamics 365 Supply Chain Managementi jaoks dokumenteeritud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Managementi väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Supply Chain Managementi sisseehitatud koondplaneerimise mootori kasutamine jaotusstsenaariumite jaoks

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudluse suurendamiseks ja SQL-andmebaasi koormuse minimeerimiseks koondplaneerimise käitamisel asendatakse Supply Chain Managementi sisseehitatud koondplaneerimise mootor planeerimise optimeerimisega. Planeerimise optimeerimine võimaldab kiiret planeerimise käitamist, mida saab teostada ka töövälisel ajal. See võimaldab planeerijatel kohe nõudluse ja planeerimise parameetrite muutustele reageerida. |
| **Asendatud teise funktsiooniga?**   | Jah, planeerimise optimeerimine asendab Supply Chain Managementi olemasoleva sisseehitatud koondplaneerimise mootori. |
| **Mõjutatud tootealad**         | Supply Chain Management – Koondplaneerimine |
| **Juurutamissuvand**              | Ainult pilv. Kohapealsed juurutamised ei toeta planeerimise optimeerimist. |
| **Olek**                         | Aegunud. Alates 2021. aasta aprillist ei toeta jaotamisstsenaariumid enam Dynamics 365 Supply Chain Management-i sisseehitatud koondplaneerimise mootorit. Kliendid peavad jaotamisstsenaariumite puhul kasutama koondplaneerimise arvutustes planeerimise optimeerimist. Lisateavet vt [Planeerimise optimeerimise dokumentatsioon](https://go.microsoft.com/fwlink/?linkid=2105830). Kliendid, kellel on Dynamics 365 Supply Chain Management-i kohapealsed juurutused, võivad jätkata Supply Chain Managementi koondplaneerimise mootori kasutamist jaotamisstsenaariumite jaoks ka pärast 2021. aasta aprilli. Funktsioonitäiustusi aga enam tulevikus ei pakuta. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest

Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
