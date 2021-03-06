---
title: Protsessi automatiseerimine
description: Selles teemas kirjeldatakse üksikasju selle kohta, kuidas protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920825"
---
# <a name="process-automation"></a>Protsessi automatiseerimine

[!include[banner](../includes/banner.md)]

Protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist. Plaanitud töö värskendatud kalendri vaade võimaldab lõppkasutajatel vaadata ja teha toiminguid plaanitud ja lõpule viidud tööga.

## <a name="administration"></a>Haldus

Kõigi protsessi automatiseerimiste keskse halduse lehe leiate süsteemihalduse mooduli menüü jaotisest **Häälestus**. Sellel lehel loetletakse kõik süsteemis seadistatud automatiseeritud protsessid (seeriad). Saate lisada ka uusi protsessi automatiseerimisi otse sellelt lehelt. Pärast seeria seadistamist saate selle loendi kaudu hallata kõiki seeriaid. Saate redigeerida tervet seeriat, seda kustutada, vaadata loendivaatest kõiki esinemisi või keelata seeria, kui soovite plaanitud töö mõneks ajaks peatada. 

Funktsioonihalduses keelatud protsesse ei näidata, kui funktsioon on keelatud. Lisaks ei ajasta protsessi automatiseerimise ajastamise mootor keelatud funktsiooni jaoks ühtegi esinemiskorda ega taustaprotsessi. Funktsiooni uuesti lubamisel käivitatakse kohe varem ajastatud esinemiskorrad või taustaprotsessid. Protsessi automatiseerimise plaanimise mootor põhineb süsteemi pakett-tööl **Protsessi automatiseerimise pollimissüsteemi töö** käitamisel. Tööd ei tohi suvalisel ajal muuta ega sellega manipuleerida. 

## <a name="calendar-view"></a>Kalendri vaade

Protsessi automatiseerimise üks peamisi eeliseid on võimalus kuvada plaanitud tööd lihtsas kalendri vaates.  See vaade võimaldab teil kuvada tööd nädala kaupa. See vaade kuvatakse lehe **Protsessi automatiseerimine** paremal küljel. See asustatakse valitud seeria plaanitud tööga. 

[![Protsessi automatiseerimise kalender](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Esinemiste muudatused

Igat esinemist saab muuta, mõjutamata teisi määratletud esinemisi, mis pärinevad sellest seeriast. Plaanitud töö esinemisi saab redigeerida kalendri vaates, valides nupu **Kuva/Redigeeri** ja valides **Esinemised**. See leht annab teile juurdepääsu kõigile seeria häälestuse viisardis algselt kuvatud sätetele ja annab võimaluse muuta valituid esinemisi üks kord. Plaanitud töö esinemist saab ka välja lülitada, valides kalendri vaates nupu **Keela**.

## <a name="developer-documentation"></a>Arendaja dokumentatsioon

Protsessi automatiseerimise raamistik võimaldab arendajatel laiendada protsessi automatiseerimise raamistikku. [Protsessi automatiseerimise raamistiku](../process-automation/process-automation-framework.md) dokumentatsioonis antakse teavet selle kohta, kuidas saate luua kohandatud protsesse, mida on vaja pakktöötlusserveris käitamiseks, mis on plaanitud protsessi automatiseerimise viisardis ja kuvatakse automaatselt kalendri vaates.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
