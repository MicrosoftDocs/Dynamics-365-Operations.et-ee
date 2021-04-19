---
title: Dynamics 365 Supply Chain Managementi eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Supply Chain Managementis.
author: kamaybac
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 2e41510f1f5810dde9683235384f89008f888471
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821269"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Managementi eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema uuendatakse, kui uued eemaldatud või aegunud funktsioonid on Dynamics 365 Supply Chain Managementi jaoks dokumenteeritud.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://docs.microsoft.com/dynamics/s-e/). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Supply Chain Managementi väljalaskest 10.0.18 eemaldatud või aegunud funktsioonid

### <a name="dynamics-365-for-finance-and-operations---warehousing-the-warehouse-app"></a>Dynamics 365 for Finance and Operations– ladustamine (lao rakendus)

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib 2021. aasta aprillil, *Dynamics 365 for Finance and Operations – ladustamine* (laorakendus) on iganenud ja seda ei toetata pärast 2022. aasta aprilli. See asendati nüüd *mobiilirakendusega Warehouse Management*, mis anti välja Supply Chain Management versiooniga 10.0.17. Uus rakendus on täielik asendus, kuid kasutab sama alusraamistikku, mis muudab migreerimise lihtsaks. Vajadusel saab neid kahte rakendust kõrvuti kasutada, et aidata kasutajatel uue rakenduse õppimisel järk-järgult kohaneda.<br><br>Lisateavet uue laohalduse mobiilirakenduse Warehouse Management kohta vt jaotisest [Mobiilirakenduse Warehouse Management](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) ja [Mobiilirakenduse Warehouse Management installimine ja ühendamine](../warehousing/install-configure-warehouse-management-app.md). |
| **Asendatud teise funktsiooniga?**   | Jah, asendatud uue laohalduse mobiilirakendusega Warehouse Management. |
| **Mõjutatud tootealad**         | Supply Chain Management – lao rakendus |
| **Juurutamissuvand**              | Pilves ja kohapealne |
| **Olek**                         | Aegunud. Laorakendus saab tuge vigade ja turvaparandustega, kuid funktsioonide täiustusi enam ei pakuta. Pärast 2022. aasta aprilli ei toetata enam vanat laorakendust ja klientidel palutakse kolida uude laohalduse mobiilirakendusse Warehouse Management. Seejärel eemaldatakse vana laorakendus Microsofti poest ja Google Play poest.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Managementi väljalaskest 10.0.15 eemaldatud või aegunud funktsioonid

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Dynamics 365 tugi on iganenud

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib alates 2020. detsembrist, Microsoft Internet Explorer 11 tugi kõigile Dynamics 365 toodetele on iganenud ja Internet Explorer 11 ei toetata pärast 2021. aasta augustit.<br><br>See mõjutab kliente, kes kasutavad Dynamics 365 tooteid, mis on mõeldud kasutamiseks Internet Explorer 11 liidese kaudu. Pärast 2021. aasta augustit, Internet Explorer 11 ei toetata selliste Dynamics 365 toodete puhul. |
| **Asendatud teise funktsiooniga?**   | Soovitame klientide minna üle Microsoft Edge-le.|
| **Mõjutatud tootealad**         | Kõik Dynamics 365 tooted |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Aegunud. Internet Explorer 11 ei toetata pärast 2021. aasta augustit.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Supply Chain Managementi sisseehitatud koondplaneerimise mootori kasutamine tootmisstsenaariumite jaoks

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudluse suurendamiseks ja SQL-andmebaasi koormuse minimeerimiseks koondplaneerimise käitamisel asendatakse Supply Chain Managementi sisseehitatud koondplaneerimise mootor planeerimise optimeerimisega. Planeerimise optimeerimine võimaldab kiiret planeerimise käitamist, mida saab teostada ka töövälisel ajal. See võimaldab planeerijatel kohe nõudluse ja planeerimise parameetrite muutustele reageerida. |
| **Asendatud teise funktsiooniga?**   | Jah, planeerimise optimeerimine asendab Supply Chain Managementi olemasoleva sisseehitatud koondplaneerimise mootori. |
| **Mõjutatud tootealad**         | Supply Chain Management – Koondplaneerimine |
| **Juurutamissuvand**              | Ainult pilv. Kohapealsed juurutamised ei toeta planeerimise optimeerimist. |
| **Olek**                         | Aegunud. Alates 2021. aasta 1. oktoobrist ei toeta tootmisstsenaariumid enam Dynamics 365 Supply Chain Management-i sisseehitatud koondplaneerimise mootorit. Kliendid peavad tootmisstsenaariumite puhul kasutama koondplaneerimise arvutustes planeerimise optimeerimist. Lisateavet vt [Planeerimise optimeerimise dokumentatsioon](https://go.microsoft.com/fwlink/?linkid=2105830). Kliendid, kellel on Dynamics 365 Supply Chain Management-i kohapealsed juurutused, võivad jätkata Supply Chain Managementi koondplaneerimise mootori kasutamist tootmisstsenaariumite jaoks ka pärast 2021. aasta oktoobrit. Funktsioonitäiustusi aga enam tulevikus ei pakuta. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Managementi väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Supply Chain Managementi sisseehitatud koondplaneerimise mootori kasutamine jaotusstsenaariumite jaoks

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudluse suurendamiseks ja SQL-andmebaasi koormuse minimeerimiseks koondplaneerimise käitamisel asendatakse Supply Chain Managementi sisseehitatud koondplaneerimise mootor planeerimise optimeerimisega. Planeerimise optimeerimine võimaldab kiiret planeerimise käitamist, mida saab teostada ka töövälisel ajal. See võimaldab planeerijatel kohe nõudluse ja planeerimise parameetrite muutustele reageerida. |
| **Asendatud teise funktsiooniga?**   | Jah, planeerimise optimeerimine asendab Supply Chain Managementi olemasoleva sisseehitatud koondplaneerimise mootori. |
| **Mõjutatud tootealad**         | Supply Chain Management – Koondplaneerimine |
| **Juurutamissuvand**              | Ainult pilv. Kohapealsed juurutamised ei toeta planeerimise optimeerimist. |
| **Olek**                         | Aegunud. Alates 2021. aasta 1. aprillist ei toeta jaotamisstsenaariumid enam Dynamics 365 Supply Chain Management-i sisseehitatud koondplaneerimise mootorit. Kliendid peavad jaotamisstsenaariumite puhul kasutama koondplaneerimise arvutustes planeerimise optimeerimist. Lisateavet vt [Planeerimise optimeerimise dokumentatsioon](https://go.microsoft.com/fwlink/?linkid=2105830). Kliendid, kellel on Dynamics 365 Supply Chain Management-i kohapealsed juurutused, võivad jätkata Supply Chain Managementi koondplaneerimise mootori kasutamist jaotamisstsenaariumite jaoks ka pärast 2021. aasta aprilli. Funktsioonitäiustusi aga enam tulevikus ei pakuta. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest

Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
