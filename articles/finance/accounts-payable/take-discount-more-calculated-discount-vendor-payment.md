---
title: Rohkem kui arvestatud allahindluse võtmine hankija maksel
description: See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus. See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cd74c6677f80a9075449908411350f1c81b95b02
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778353"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a>Rohkem kui arvestatud allahindluse võtmine hankija maksel

[!include [banner](../includes/banner.md)]

See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus. See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises. 

Hankija 3051 annab Fabrikamile 4% skontot, kui arve tasutakse seitsme päeva jooksul. April sisestab 29. juunil arve summas 1000,00. Hankija laseb Aprilil võtta skonto summas 60,00 vaikimisi arve jaoks saadaval oleva skonto 40,00 asemel. April kirjendab ühekordse makse, kasutades töölehte Ostureskontro makse. Ta sisestab makse jaoks hankija ja avab seejärel lehe **Kannete tasakaalustamine**. Ta märgib arve ja muudab välja **Skonto summa** väärtuseks **60,00**.

| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | Inv-10040 | 3051    | 6/29/2020 | 7/29/2020 | 10040   | 1,000.00                       | USA dollar      | 940,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.

| Väli                        | Väärtus     |
|------------------------------|-----------|
| Skonto kuupäev           | 7/12/2020 |
| Skonto summa         | 60.00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 60,00     |

April sisestab maksetöölehe. Arve on täielikult tasakaalustatud maksega summas 940,00 ja skontoga summas 60,00.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
