---
title: Finantsperioodi hulgisulgemine
description: See artikkel näitab, kuidas panna periood ootele või jäädavalt sulgeda perioodi või mitu juriidilist isikut korraga.
author: aprilolson
ms.date: 11/16/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a85d512842b27f2d74507be16a8f2819f483e0d
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779806"
---
# <a name="mass-financial-period-close"></a>Finantsperioodi hulgisulgemine

[!include [banner](../../includes/banner.md)]

See artikkel näitab, kuidas panna periood ootele või jäädavalt sulgeda perioodi või mitu juriidilist isikut korraga. Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.

1. Navigeerimispaanil minge pearaamatusse **ja > sulgege > kalendrid**. 

>[!NOTE]
> Kuvatud juriidiliste isikute loend sõltub leheküljel valitud rahanduskalendrist. Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.

2. Valige suvand **Redigeeri**.
3. Valige periood, mille olekut soovite muuta.
4. Valige juriidilised isikud, mille olekut soovite muuta. Võite valida kiiresti kõik juriidilised isikud, valides ruudustiku ülemisel vasakul poolel küsimärgi.  
5. Valitud mooduli sisestamise juurdepääsu määramiseks valige suvand **Värskenda mooduli juurdepääsu**. Mooduli olekut saab muuta ka ühekaupa, muutes ruudustiku kirjeid. Nupust on abi siis, kui soovite muuta kiiresti juriidilise isiku mitut kirjet.  
6. Valige moodulis **Rakendus** see moodul, mille olekut soovite värskendada. Klõpsake **Vali**.
7. Valige **Juurdepääsu** tasemel kas **Kõik**, **Mitte keegi** või konkreetne kasutajate rühm. Klõpsake **Vali**.  
- **Kõik** – kõik kasutajad, kellel on moodulile redigeerimise juurdepääs, saavad sisestada, kui periood on avatud. 
- **Pole** - kasutajad ei saa moodulisse sisestada, kui periood on avatud. Kindel kasutajagrupp näitab, et ainult selles grupis olevad kasutajad saavad moodulisse sisestada, kui periood on avatud.  
8. Valige **uuendamine**, 
9. Valige oleku uuendamiseks teine periood.
10. Valige juriidilised isikud, mille perioodi olekut soovite muuta.
11. Valige suvand **Värskenda perioodi olek** ja seadistage olekuks kas **Ootel**, **Avatud** või **Jäädavalt suletud**. **Avatud** näitab, et perioodi saab sisestada, kui kasutajal on juurdepääs. **Ootel** tähendab, et perioodi ei saa sisestada, aga perioodi saab uuesti avada. **Jäädavalt suletud** tähendab, et periood on suletud ja seda ei saa kunagi avada. Korrigeerimisi ei saa sisestada. Me ei soovita perioodi seadistada väärtusele Jäädavalt **suletud enne**, kui kõik korrigeerimised ja auditid on lõpetatud.  
12. Tehke valik **Värskenda**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
