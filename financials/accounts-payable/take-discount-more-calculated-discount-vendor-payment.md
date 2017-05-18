---
title: "Hankija makse arvutatud skontost suurema skonto võtmine"
description: "See artikkel juhatab teid läbi stsenaariumi, kus skonto võetakse summast, mis on suurem kui algselt arvel olev allahindlus. See stsenaarium võib ilmneda juhul, kui organisatsioon lepib müüjaga kokku arvel väiksema summa maksmises."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 9840b22a72a3ab05d5e6e4145b1e78c9381057ff
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


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




