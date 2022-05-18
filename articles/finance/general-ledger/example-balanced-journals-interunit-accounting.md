---
title: Tasakaalustatud töölehed sisekäibe jaoks
description: See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon.
author: kweekley
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 38a7d88602dcd0121eb331dab8bf35a815287f8c
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8712310"
---
# <a name="balanced-journals-for-interunit-accounting"></a>Tasakaalustatud töölehed sisekäibe jaoks

[!include [banner](../includes/banner.md)]

See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon. 

Kui kontokirjed ei tasakaalust finantsdimensiooni väärtuste tasandil, luuakse automaatselt täiendavad kontokirjed, et töölehte tasakaalustada. Need kontokirjed kasutavad lehel **Automaatsete kannete kontod** sisestustüüpe **Üksustevaheline – deebet** ja **Üksustevaheline – kreedit**, et määrata põhikonto. Näiteks on tasakaalustava finantsdimensioonina valitud Äriüksus, mis on pearaamatukonto teine segment, ja loomisel on järgmised raamatupidamiskirjed.

| &nbsp;               | &nbsp;    |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

Sellisel juhul määratakse järgmised saldod.

-   Äriüksusele MSP = 100.00 CR
-   Äriüksusele NY = 100.00 DR

Seega luuakse järgmised raamatupidamiskirjed automaatselt, et tasakaalustada tööleht finantsdimensiooni väärtuste tasemel.

| &nbsp;                            | &nbsp;    |
|-----------------------------------|-----------|
| (Üksustevaheline deebet) – MSP – OU\_256 | 100.00 DR |
| (Üksustevaheline kreedit) – NY – OU\_249 | 100.00 CR |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
