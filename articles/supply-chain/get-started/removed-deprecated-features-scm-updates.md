---
title: Dynamics 365 Supply Chain Managementi eemaldatud või iganenud funktsioonid
description: See artikkel kirjeldab funktsioone, mis on eemaldatud või mida plaanitakse eemaldada Dynamics 365 Supply Chain Management
author: kamaybac
ms.date: 06/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 722b34e89a54715db39259549c11a78d69d2b4d3
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739866"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-supply-chain-management"></a>Dynamics 365 Supply Chain Managementi eemaldatud või iganenud funktsioonid

[!include [banner](../includes/banner.md)]

Seda artiklit värskendatakse, kuna uued eemaldatud või aegunud funktsioonid on dokumenteeritud Dynamics 365 Supply Chain Management.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.

> [!NOTE]
> Finantside ja toimingute rakenduste objektide üksikasjaliku teabe leiate tehnilistest [viitearuannetest](/dynamics/s-e/). Saate võrrelda nende aruannete erinevaid versioone, et saada teavet objektide kohta, mida on igas finantsi ja toimingute rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10029-release"></a>Supply Chain Managementi väljalaskest 10.0.29 eemaldatud või aegunud funktsioonid

### <a name="stock-transfer-orders-that-have-tax-on-the-transfer-price"></a>Lao üleviimistellimused, mille sisehinnale kehtib maks

| &nbsp;  | &nbsp;  |
|---|---|
| **Aegumise/eemaldamise põhjus** | Lao [üleviimistellimused, mille ülekande hinnafunktsioonil](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) on maks, asendatakse Lao [üleviimistellimustega India funktsioonide](../../finance/localizations/apac-ind-stock-transfer.md) jaoks. |
| **Asendatud teise funktsiooniga?**   | Jah, lao [üleviimistellimused, mille makse on ülekande hinna](../../finance/localizations/apac-ind-gst-stock-transfer-transactions.md) funktsioonil, asendatakse Lao [üleviimistellimustega India funktsioonide](../../finance/localizations/apac-ind-stock-transfer.md) jaoks. |
| **Mõjutatud tootealad** | Tarneahela haldus – varud |
| **Juurutamissuvand** | Pilves ja kohapealne |
| **Olek** | <p>Taunitud. Lao *üleviimistellimused, mis on ülekande hinna* funktsioonil maksuga, ei saa tuge vigaste paranduste ja turbeparandustega.</p><p>Pärast 2023. aasta aprilli palutakse klientidel vaikimisi kasutada täiustatud funktsioone – *lao üleviimistellimusi India* puhul. Pärast 2023. aasta oktoober pole laoülekandetellimused, *mis omavad* ülekande hinna funktsioonil maksu, *enam saadaval olla ja klientidel palutakse india funktsiooni puhul teisaldada täiustatud lao üleviimistellimused*.</p><p>Lisateavet vt Lao üleviimistellimustest [India jaoks](../../finance/localizations/apac-ind-stock-transfer.md).</p> |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10019-release"></a>Supply Chain Managementi väljalaskest 10.0.19 eemaldatud või aegunud funktsioonid

### <a name="job-card-device"></a>Töökaardi vahend

| &nbsp;  | &nbsp;  |
|---|---|
| **Aegumise/eemaldamise põhjus** | [Töökaardi seadet](../production-control/config-job-card-device.md) asendab uus [tootmispinna käivitamise liides](../production-control/production-floor-execution-configure.md). |
| **Asendatud teise funktsiooniga?**   | Jah, [töökaardi seadet](../production-control/config-job-card-device.md) asendab uus [tootmispinna käivitamise liides](../production-control/production-floor-execution-configure.md). |
| **Mõjutatud tootealad** | Supply Chain Management – tootmise juhtimine |
| **Juurutamissuvand** | Pilves ja kohapealne |
| **Olek** | Aegunud. Töökaardi seade saab tuge vigade ja turvaparandustega, kuid funktsioonide täiustusi enam ei pakuta. Pärast 2022. aasta aprilli ei toetata enam vana töökaardi seadet ja klientidel palutakse kolida uude tootmispinna käivitamise liidesesse. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10018-release"></a>Supply Chain Managementi väljalaskest 10.0.18 eemaldatud või aegunud funktsioonid

### <a name="supply-chain-management--warehousing-the-warehouse-app"></a><a name="wma"></a> Tarneahela haldus – ladustamine (laorakendus)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib 2021. aasta aprillis *,* tarneahela haldus – ladustamine (laorakendus) on taunitav ja seda ei toetata pärast 2022. aasta aprilli. See asendati nüüd *mobiilirakendusega Warehouse Management*, mis anti välja Supply Chain Management versiooniga 10.0.17. Uus rakendus on täielik asendus, kuid kasutab sama alusraamistikku, mis muudab migreerimise lihtsaks. Vajadusel saab neid kahte rakendust kõrvuti kasutada, et aidata kasutajatel uue rakenduse õppimisel järk-järgult kohaneda.<br><br>Lisateavet uue laohalduse mobiilirakenduse Warehouse Management kohta vt jaotisest [Mobiilirakenduse Warehouse Management](/dynamics365-release-plan/2021wave1/finance-operations/dynamics365-supply-chain-management/warehouse-management-mobile-application) ja [Mobiilirakenduse Warehouse Management installimine ja ühendamine](../warehousing/install-configure-warehouse-management-app.md). |
| **Asendatud teise funktsiooniga?**   | Jah, asendatud uue laohalduse mobiilirakendusega Warehouse Management. |
| **Mõjutatud tootealad**         | Supply Chain Management – lao rakendus |
| **Juurutamissuvand**              | Pilves ja kohapealne |
| **Olek**                         | Aegunud. Laorakendus saab tuge vigade ja turvaparandustega, kuid funktsioonide täiustusi enam ei pakuta. Pärast 2022. aasta aprilli ei toetata enam vanat laorakendust ja klientidel palutakse kolida uude laohalduse mobiilirakendusse Warehouse Management. Seejärel eemaldatakse vana laorakendus Microsofti poest ja Google Play poest.  |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10015-release"></a>Supply Chain Managementi väljalaskest 10.0.15 eemaldatud või aegunud funktsioonid

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Dynamics 365 tugi on iganenud

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib alates 2020. detsembrist, Microsoft Internet Explorer 11 tugi kõigile Dynamics 365 toodetele on iganenud ja Internet Explorer 11 ei toetata pärast 2021. aasta augustit.<br><br>See mõjutab kliente, kes kasutavad Dynamics 365 tooteid, mis on mõeldud kasutamiseks Internet Explorer 11 liidese kaudu. Pärast 2021. aasta augustit, Internet Explorer 11 ei toetata selliste Dynamics 365 toodete puhul. |
| **Asendatud teise funktsiooniga?**   | Soovitame klientide minna üle Microsoft Edge-le.|
| **Mõjutatud tootealad**         | Kõik Dynamics 365 tooted |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Aegunud. Internet Explorer 11 ei toetata pärast 2021. aasta augustit.|

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-manufacturing-scenarios"></a>Supply Chain Managementi sisseehitatud koondplaneerimise mootori kasutamine tootmisstsenaariumite jaoks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudluse suurendamiseks ja SQL-andmebaasi koormuse minimeerimiseks koondplaneerimise käitamisel asendatakse Supply Chain Managementi sisseehitatud koondplaneerimise mootor planeerimise optimeerimisega. Planeerimise optimeerimine võimaldab kiiret planeerimise käitamist, mida saab teostada ka töövälisel ajal. See võimaldab planeerijatel kohe nõudluse ja planeerimise parameetrite muutustele reageerida. |
| **Asendatud teise funktsiooniga?**   | Jah, planeerimise optimeerimine asendab Supply Chain Managementi olemasoleva sisseehitatud koondplaneerimise mootori. |
| **Mõjutatud tootealad**         | Supply Chain Management – Koondplaneerimine |
| **Juurutamissuvand**              | Ainult pilv. Kohapealsed juurutamised ei toeta planeerimise optimeerimist. |
| **Olek**                         | Aegunud. 1. aprilliks 2022 ei toetata tootmisstsenaariume enam integreeritud tarneahela halduse koondplaneerimise mootori puhul. Alates sellest kuupäevast peatab Microsoft kõik aktiivsed arendused tootmisstsenaariumites integreeritud plaanimismootori jaoks, ei vabasta uusi funktsioone ja vabastab ainult kriitilised vigaparandused. Pärast seda kuupäeva peavad kõik tootmisstsenaariume vajavad ettevõtted koondplaneerimise arvutustes kasutama plaanimise optimeerimist. Plaanimise optimeerimine peaks tootmisstsenaariume täielikult toetama 2022. aasta oktooberks. Lisateavet vt aegunud [koondplaneerimise ülevaatest](../master-planning/deprecated-master-planning-overview.md).<br><br>Ettevõtted, kus on tarneahela halduse valdustes juurutamised, võivad jätkata pärast 2022. aasta aprilli tootmisstsenaariumide integreeritud koondplaneerimise mootori kasutamist. Funktsioonitäiustusi aga enam tulevikus ei pakuta. |

## <a name="features-removed-or-deprecated-in-the-supply-chain-management-10011-release"></a>Supply Chain Managementi väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid

### <a name="use-of-built-in-supply-chain-management-master-planning-engine-for-distribution-scenarios"></a>Supply Chain Managementi sisseehitatud koondplaneerimise mootori kasutamine jaotusstsenaariumite jaoks

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jõudluse suurendamiseks ja SQL-andmebaasi koormuse minimeerimiseks koondplaneerimise käitamisel asendatakse Supply Chain Managementi sisseehitatud koondplaneerimise mootor planeerimise optimeerimisega. Planeerimise optimeerimine võimaldab kiiret planeerimise käitamist, mida saab teostada ka töövälisel ajal. See võimaldab planeerijatel kohe nõudluse ja planeerimise parameetrite muutustele reageerida. |
| **Asendatud teise funktsiooniga?**   | Jah, planeerimise optimeerimine asendab Supply Chain Managementi olemasoleva sisseehitatud koondplaneerimise mootori. |
| **Mõjutatud tootealad**         | Supply Chain Management – Koondplaneerimine |
| **Juurutamissuvand**              | Ainult pilv. Kohapealsed juurutamised ei toeta planeerimise optimeerimist. |
| **Olek**                         | Aegunud. Alates 2021. aasta 1. aprillist ei toeta jaotamisstsenaariumid enam Dynamics 365 Supply Chain Management-i sisseehitatud koondplaneerimise mootorit. Kliendid peavad jaotamisstsenaariumite puhul kasutama koondplaneerimise arvutustes planeerimise optimeerimist. Lisateavet vt aegunud [koondplaneerimise ülevaatest](../master-planning/deprecated-master-planning-overview.md). Kliendid, kellel on Dynamics 365 Supply Chain Management-i kohapealsed juurutused, võivad jätkata Supply Chain Managementi koondplaneerimise mootori kasutamist jaotamisstsenaariumite jaoks ka pärast 2021. aasta aprilli. Funktsioonitäiustusi aga enam tulevikus ei pakuta. |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest

Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

