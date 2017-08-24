--- 
title: "Hankija maksetingimuste määratlemine"
description: Seadistage hankija arvete maksetingimused.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: cbac3b27c25377abff341c4bf259e553c14a4ae8
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="define-vendor-payment-terms"></a>Hankija maksetingimuste määratlemine

[!include[task guide banner](../../includes/task-guide-banner.md)]

Seadistage hankija arvete maksetingimused. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Ostureskontro > Makse seadistus > Maksetingimused.
2. Klõpsake valikut Uus.
    * Lehte Maksetingimused kasutatakse määratlemaks, kuidas tähtaega arvutatakse. Seda ei kasutata määratlemaks, kuidas skonto kuupäeva arvutatakse.  
3. Sisestage väärtus väljale Maksetingimused.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage number väljale Päevad.
    * Siin sisestatud numbrit kasutatakse tähtajale või makseviisis määratletud perioodi lõppu lisamiseks. Näiteks kui valite Neto, lisatakse number tähtajale. Praeguse kuu valimisel lisatakse tähtaja arvutamiseks number praeguse kuu viimasele päevale.  
6. Klõpsake nuppu Salvesta.
7. Sulgege leht.
8. Avage Ostureskontro > Makse seadistus > Skontod.
9. Klõpsake valikut Uus.
10. Sisestage ID väljale Skonto.
11. Sisestage väljale Kirjeldus soovitud väärtus.
12. Kui hankija pakub mitmetasandilist allahindlust, valige järgmine skonto pärast praeguse aegumist.
13. Sulgege leht.
14. Sisestage number väljale Päevad.
    * Väljale Päevad sisestatud kogust kasutatakse skonto kuupäeva arvutamiseks selle põhjal, milline suvand väljal Neto/praegune valiti. Neto valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale. Praeguse kuu valimisel lisatakse skonto kuupäeva määramiseks kogus praeguse kuu lõppu.  
15. Sisestage skonto protsent väljale Allahindlus. 
16. Sisestage põhikonto, millele skonto kliendiarvete puhul sisestatakse.
17. Sisestage põhikonto, millele skonto hankija arvete puhul sisestatakse.
    * Kui suvand Allahindluse vastaskontod on seatud valikule Kasuta hankija allahindluse jaoks põhikontot, siis kasutatakse põhikontot.  Kui suvand on seatud valikule Kontod arve real, sisestatakse skonto arve ridadel vara/kulu kontodele.  
18. Klõpsake nuppu Salvesta.


