---
title: Finantsperioodi hulgisulgemine
description: Selles teemas näidatakse, kuidas panna periood ootele või sulgeda periood lõplikult korraga rohkem kui ühel juriidilisel isikul.
author: aprilolson
manager: AnnBe
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 398a62e575010501291af3016553fc72fbc891de
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914626"
---
# <a name="mass-financial-period-close"></a>Finantsperioodi hulgisulgemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas näidatakse, kuidas panna periood ootele või sulgeda periood lõplikult korraga rohkem kui ühel juriidilisel isikul. Lisaks näitab see ülesanne, kuidas piirata kasutajagrupil konkreetsetesse moodulitesse sisestamist.

1. Avage navigeerimispaanil **Moodulid > Pearaamat > Perioodi sulgemine > Pearaamatu kalendrid**. Pange tähele, et kuvatav juriidiliste isikute loend oleneb lehel valitud rahanduskalendrist. Kuvatakse ainult valitud rahanduskalendrit kasutavad juriidilised isikud.
2. Valige suvand **Redigeeri**.
3. Valige periood, mille olekut soovite muuta.
4. Valige juriidilised isikud, mille olekut soovite muuta. Võite valida kiiresti kõik juriidilised isikud, valides ruudustiku ülemisel vasakul poolel küsimärgi.  
5. Valitud mooduli sisestamise juurdepääsu määramiseks valige suvand **Värskenda mooduli juurdepääsu**. Mooduli olekut saab muuta ka ühekaupa, muutes ruudustiku kirjeid. Nupust on abi siis, kui soovite muuta kiiresti juriidilise isiku mitut kirjet.  
6. Valige moodulis **Rakendus** see moodul, mille olekut soovite värskendada. Klõpsake **Vali**.
7. Valige **Juurdepääsu** tasemel kas **Kõik**, **Mitte keegi** või konkreetne kasutajate rühm. Klõpsake **Vali**. Suvand Kõik näitab, et kõik mooduli redigeerimisõigusega kasutajad saavad sisestada, kui periood on avatud. Suvand Mitte ükski näitab, et kasutajad ei saa moodulisse sisestada, kui periood on avatud. Kindel kasutajagrupp näitab, et ainult selles grupis olevad kasutajad saavad moodulisse sisestada, kui periood on avatud.  
8. Tehke valik **Värskenda**.
9. Valige oleku uuendamiseks teine periood.
10. Valige juriidilised isikud, mille perioodi olekut soovite muuta.
11. Valige suvand **Värskenda perioodi olek** ja seadistage olekuks kas **Ootel**, **Avatud** või **Jäädavalt suletud**. **Avatud** näitab, et perioodi saab sisestada, kui kasutajal on juurdepääs. **Ootel** tähendab, et perioodi ei saa sisestada, aga perioodi saab uuesti avada. **Jäädavalt suletud** tähendab, et periood on suletud ja seda ei saa kunagi avada. Korrigeerimisi ei saa sisestada. Me ei soovita seadistada perioodi olekuks **Jäädavalt suletud** enne, kui kõik kohandused ja auditid on lõpetatud.  
12. Tehke valik **Värskenda**.

