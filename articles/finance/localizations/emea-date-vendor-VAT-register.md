---
title: Hankija KM-registri kuupäev
description: See artikkel annab teavet funktsiooni kohta hankija KM-registri kuupäeva lubamiseks
author: AdamTrukawka
ms.date: 01/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: global
ms.author: atrukawk
ms.search.validFrom: 2022-01-15
ms.dyn365.ops.version: AX 10.0.24
ms.custom: intro-internal
ms.openlocfilehash: 4af770427f5b19eaf2a129b26d54aeacc6c2f148
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278274"
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
