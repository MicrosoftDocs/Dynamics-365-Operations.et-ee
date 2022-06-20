---
title: Finantsperioodi hulgisulgemine
description: See artikkel näitab, kuidas panna periood ootele või jäädavalt sulgeda perioodi või mitu juriidilist isikut korraga.
author: aprilolson
ms.date: 08/16/2019
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
ms.openlocfilehash: 18e2418777e4f8a5f10b946d7cdc217e5e264318
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872437"
---
# <a name="mass-financial-period-close"></a>Finantsperioodi hulgisulgemine

[!include [banner](../../includes/banner.md)]

See artikkel näitab, kuidas panna periood ootele või jäädavalt sulgeda perioodi või mitu juriidilist isikut korraga. Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.

1. Navigeerimispaanil minge pearaamatusse **ja > sulgege > kalendrid**. Pange tähele, et kuvatav juriidiliste isikute loend oleneb lehel valitud rahanduskalendrist. Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.
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
11. Valige suvand **Värskenda perioodi olek** ja seadistage olekuks kas **Ootel**, **Avatud** või **Jäädavalt suletud**. **Avatud** näitab, et perioodi saab sisestada, kui kasutajal on juurdepääs. **Ootel** tähendab, et perioodi ei saa sisestada, aga perioodi saab uuesti avada. **Jäädavalt suletud** tähendab, et periood on suletud ja seda ei saa kunagi avada. Korrigeerimisi ei saa sisestada. Me ei soovita seadistada perioodi olekuks **Jäädavalt suletud** enne, kui kõik kohandused ja auditid on lõpetatud.  
12. Tehke valik **Värskenda**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
