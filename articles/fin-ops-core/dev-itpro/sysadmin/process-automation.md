---
title: Protsessi automatiseerimine
description: Selles teemas kirjeldatakse üksikasju selle kohta, kuidas protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 06/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 2ab4e7510ff98b9fbf0223096b905e9de47f52e1
ms.sourcegitcommit: 1833c1e07a32c8ad41e4a1516e78100ae04a2156
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/26/2020
ms.locfileid: "3508181"
---
# <a name="process-automation"></a>Protsessi automatiseerimine

[!include[banner](../includes/banner.md)]

Protsessi automatiseerimine võimaldab pakktöötlusserveris käivitatavate protsesside lihtsat plaanimist. Plaanitud töö värskendatud kalendri vaade võimaldab lõppkasutajatel vaadata ja teha toiminguid plaanitud ja lõpule viidud tööga.

## <a name="administration"></a>Haldus

Kõigi protsessi automatiseerimiste keskse halduse lehe leiate süsteemihalduse mooduli menüü jaotisest **Häälestus**. Sellel lehel loetletakse kõik süsteemis seadistatud automatiseeritud protsessid (seeriad). Saate lisada ka uusi protsessi automatiseerimisi otse sellelt lehelt. Pärast seeria seadistamist saate selle loendi kaudu hallata kõiki seeriaid. Saate redigeerida tervet seeriat, kustutada, vaadata loendivaatest kõiki esinemisi või keelata seeria, kui soovite plaanitud töö teatud ajavahemikuks peatada. 

## <a name="calendar-view"></a>Kalendri vaade 
Protsessi automatiseerimise üks peamisi eeliseid on võimalus kuvada plaanitud tööd lihtsas kalendri vaates.  See vaade võimaldab teil kuvada tööd nädala kaupa. See vaade kuvatakse lehe **Protsessi automatiseerimine** paremal küljel. See asustatakse valitud seeria plaanitud tööga. 

[![Protsessi automatiseerimise kalender](./media/CalendarView2.png)](./media/CalendarView2.png)

## <a name="occurrence-changes"></a>Esinemiste muudatused
Igat esinemist saab muuta, mõjutamata teisi määratletud esinemisi, mis pärinevad sellest seeriast. Plaanitud töö esinemisi saab redigeerida kalendri vaates, valides nupu **Kuva/Redigeeri** ja valides **Esinemised**. See annab teile juurdepääsu kõigile seeria häälestuse viisardis algselt kuvatud sätetele ja annab võimaluse teha ühekordne muudatuse valitud esinemisele. Plaanitud töö esinemist saab ka välja lülitada, valides kalendri vaates nupu **Keela**. 

## <a name="developer-documentation"></a>Arendaja dokumentatsioon 
Arendaja dokumentatsiooni kirjutatakse praegu, et lubada arendajatele protsessi automatiseerimise raamistiku laiendamist. See dokumentatsioon annab teavet selle kohta, kuidas saate luua kohandatud protsesse, mida on vaja pakktöötlusserveris käitamiseks, mis on plaanitud protsessi automatiseerimise viisardis ja kuvatakse automaatselt kalendri vaates.