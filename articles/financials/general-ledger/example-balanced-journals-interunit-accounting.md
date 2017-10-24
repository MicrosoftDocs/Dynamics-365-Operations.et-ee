---
title: "Tasakaalustatud töölehed sisekäibe jaoks"
description: "See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15791
ms.assetid: 301bd80e-f8b1-4f12-8194-e6d7de736084
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f45d180dc8dcafb0579e76b890dd5d516df5b8c0
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="balanced-journals-for-interunit-accounting"></a>Tasakaalustatud töölehed sisekäibe jaoks

[!include[banner](../includes/banner.md)]


See artikkel näitab, kuidas töölehte automaatselt tasakaalustatakse, kui lehel Pearaamat valitakse tasakaalustav finantsdimensioon. 

Kui kontokirjed ei tasakaalust finantsdimensiooni väärtuste tasandil, luuakse automaatselt täiendavad kontokirjed, et töölehte tasakaalustada. Need kontokirjed kasutavad lehel **Automaatsete kannete kontod** sisestustüüpe **Üksustevaheline – deebet** ja**Üksustevaheline – kreedit**, et määrata põhikonto. Näiteks on tasakaalustava finantsdimensioonina valitud Haru, mis on pearaamatukonto teine segment, ja loomisel on järgmised raamatupidamiskirjed.

|                      |           |
|----------------------|-----------|
| 6100 – MSP – OU\_256 | 100.00 DR |
| 6100 – NY – OU\_249  | 100.00 DR |
| 2100 – MSP – OU\_256 | 200.00 CR |

Sellisel juhul määratakse järgmised saldod.

-   Osakond MSP = 100,00 CR
-   Haru NY = 100,00 DR

Seega luuakse järgmised raamatupidamiskirjed automaatselt, et tasakaalustada tööleht finantsdimensiooni väärtuste tasemel.

|                                   |           |
|-----------------------------------|-----------|
| (Üksustevaheline deebet) – MSP – OU\_256 | 100.00 DR |
| (Üksustevaheline kreedit) – NY – OU\_249 | 100.00 CR |






