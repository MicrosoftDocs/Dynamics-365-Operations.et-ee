---
title: Protsessi automatiseerimine
description: See artikkel annab üksikasju selle kohta, kuidas protsessi automatiseerimine võimaldab pakktöötluse serveri käitatud protsesside lihtsat planeerimist.
author: RyanCCarlson2
ms.date: 06/29/2022
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
ms.openlocfilehash: c0015b65f1ff00cfce19139cb8aaa248512d070b
ms.sourcegitcommit: 3d2c0a39c4f987e9ac71df2f2fa6df0f64f10b2b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9114931"
---
# <a name="process-automation"></a>Protsessi automatiseerimine

[!include[banner](../includes/banner.md)]

Protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist. Plaanitud töö värskendatud kalendri vaade võimaldab lõppkasutajatel vaadata ja teha toiminguid plaanitud ja lõpule viidud tööga.

## <a name="administration"></a>Haldus

Kõigi protsessi automatiseerimiste keskse halduse lehe leiate süsteemihalduse mooduli menüü jaotisest **Häälestus**. Sellel lehel loetletakse kõik süsteemis seadistatud automatiseeritud protsessid (seeriad). Saate lisada ka uusi protsessi automatiseerimisi otse sellelt lehelt. Pärast seeria seadistamist saate selle loendi kaudu hallata kõiki seeriaid. Saate redigeerida tervet seeriat, seda kustutada, vaadata loendivaatest kõiki esinemisi või keelata seeria, kui soovite plaanitud töö mõneks ajaks peatada. 

Funktsioonihalduses keelatud protsesse ei näidata, kui funktsioon on keelatud. Lisaks ei ajasta protsessi automatiseerimise ajastamise mootor keelatud funktsiooni jaoks ühtegi esinemiskorda ega taustaprotsessi. Funktsiooni uuesti lubamisel käivitatakse kohe varem ajastatud esinemiskorrad või taustaprotsessid. Protsessi automatiseerimise plaanimise mootor põhineb süsteemi pakett-tööl **Protsessi automatiseerimise pollimissüsteemi töö** käitamisel. Tööd ei tohi suvalisel ajal muuta ega sellega manipuleerida. Kui see pakett-töö ei tööta või on see tõrke olekus, valige pakett-töö **lähtestamiseks** suvand Lähtesta protsessi automatiseerimine. See lähtestamine tagab kõigi rakenduse uuemas versioonis väljastatud uute automatiseerimiste lähtestamise. 

## <a name="calendar-view"></a>Kalendri vaade

Protsessi automatiseerimise üks peamisi eeliseid on võimalus kuvada plaanitud tööd lihtsas kalendri vaates.  See vaade võimaldab teil kuvada tööd nädala kaupa. See vaade kuvatakse lehe **Protsessi automatiseerimine** paremal küljel. See asustatakse valitud seeria plaanitud tööga. 

[![Protsessi automatiseerimise kalender.](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Esinemiste muudatused

Igat esinemist saab muuta, mõjutamata teisi määratletud esinemisi, mis pärinevad sellest seeriast. Plaanitud töö esinemisi saab redigeerida kalendri vaates, valides nupu **Kuva/Redigeeri** ja valides **Esinemised**. See leht annab teile juurdepääsu kõigile seeria häälestuse viisardis algselt kuvatud sätetele ja annab võimaluse muuta valituid esinemisi üks kord. Plaanitud töö esinemist saab ka välja lülitada, valides kalendri vaates nupu **Keela**.

## <a name="developer-documentation"></a>Arendaja dokumentatsioon

Protsessi automatiseerimise raamistik võimaldab arendajatel laiendada protsessi automatiseerimise raamistikku. [Protsessi automatiseerimise raamistiku](../process-automation/process-automation-framework.md) dokumentatsioonis antakse teavet selle kohta, kuidas saate luua kohandatud protsesse, mida on vaja pakktöötlusserveris käitamiseks, mis on plaanitud protsessi automatiseerimise viisardis ja kuvatakse automaatselt kalendri vaates.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
