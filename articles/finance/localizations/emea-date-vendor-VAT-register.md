---
title: Hankija KM-registri kuupäev
description: See artikkel annab teavet funktsiooni kohta hankija KM-registri kuupäeva lubamiseks
author: anasyash
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: intro-internal
ms.search.region: global
ms.author: anasyash
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: b1368e0c7764bed42aa7549f36a6f4bcbb96eff4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849772"
---
# <a name="date-of-vendor-vat-register"></a>Hankija KM-registri kuupäev

Finantsversioonis Microsoft Dynamics 365 10.0.24 **on** hankija arvete jaoks saadaval uus hankija KM-registri välja kuupäev. See väli määrab ostu maksustatavate tarnete kuupäeva.

Uue välja lubamiseks minge funktsioonihalduse **tööruumi**, **otsige** ja valige hankija arvete funktsiooni hankija KM-registri kuupäev ja valige luba **kohe**.

Teie tarnijatelt saadud sissetulevatel arvetel võib olla kaks kuupäeva: kuupäev, mil hankija arve väljastas, ja maksustatava tarne kuupäev (s.h kuupäev, millal hankija esitas käibemaksu [KM] tasumisele kuuluv käibemaks). Mõnes stsenaariumis võivad need kaks kuupäeva erineda.

Saate ostuarve laekuva KM-summa maha arvata ja arve hiljem KM-i aruannetesse kaasata, mis erineb mõlemast varem nimetatud kuupäevast. Seda kuupäeva kontrollitakse kohalike seadusandluse reeglitega, mis käsitlevad mõne stsenaariumi edasilükatud sissetuleva käibemaksu mahaarvamist. See erineb riigiti või regiooniti.

Mõned KM-aruanded, nt [KM-i kontrollimise aruanne](emea-cze-vat-declaration-tax-declaration-model.md#vat-control-statement) Tšehhi Vabariigis, nõuavad, et ostudokumendile tuleb esitada maksustatavate tarnete kuupäev. See kuupäev tuleb esitada, et maksuametid saaksid ühitada käibemaksuaruandluse osapoolte vahel.

Finantsis saate määrata kuupäevad järgmistel väljadel:

- **Arve** kuupäev – kuupäev, mil tarnija väljastas arve.
- **KM-registri kuupäev** – ostuarve KM-summa mahaarvamise kuupäev.
- **Hankija KM-registri** kuupäev – hankija maksustatava tarne kuupäev.
- **Vastuvõtudokumendi kuupäev** – arve saamise kuupäev.

Need väljad on kaasatud järgmistel lehtedel:

- Hankija arve
- Hankija arve registreerimine
- Hankija arve kinnitamine
- Hankijaarvete tööleht

Pärast hankija arve sisestamist saate vaadata üle kuupäevad arve töölehel ja **hankija** kannete **lehekülgedel**.
