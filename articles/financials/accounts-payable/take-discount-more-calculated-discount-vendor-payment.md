---
title: "Hankija makse arvutatud skontost suurema skonto võtmine"
description: "See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus. See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 39830014593b7b1bc2868afffcca0f77a0c8a029
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="take-a-discount-that-is-more-than-the-calculated-discount-for-a-vendor-payment"></a>Hankija makse arvutatud skontost suurema skonto võtmine

[!include[banner](../includes/banner.md)]


See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus. See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises. 

Hankija 3051 annab Fabrikamile 4% skontot, kui arve tasutakse seitsme päeva jooksul. April sisestab 29. juunil arve summas 1000,00. Hankija laseb Aprilil võtta skonto summas 60,00 vaikimisi arve jaoks saadaval oleva skonto 40,00 asemel. April kirjendab ühekordse makse, kasutades töölehte Ostureskontro makse. Ta sisestab makse jaoks hankija ja avab seejärel lehe **Kannete tasakaalustamine**. Ta märgib arve ja muudab välja **Skonto summa** väärtuseks **60,00**.
| Märge     | Kasuta skontot | Kanne   | Konto | Kuupäev      | Tähtaeg  | Arve | Summa kandevaluutas | Valuuta | Tasakaalustatav summa |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valitud | Tavaline            | Inv-10040 | 3051    | 29.06.2015 | 29.07.2015 | 10040   | 1 000,00                       | USA dollar      | 940,00           |

Teave märgitud arve allahindluse kohta kuvatakse lehe **Kannete tasakaalustamine** allosas.
|                              |           |
|------------------------------|-----------|
| Skonto kuupäev           | 12.07.2015 |
| Skonto summa         | 60,00     |
| Kasuta skontot            | Tavaline    |
| Võetud skonto          | 0,00      |
| Skonto summa võtmiseks | 60,00     |

April sisestab maksetöölehe. Arve on täielikult tasakaalustatud maksega summas 940,00 ja skontoga summas 60,00.




