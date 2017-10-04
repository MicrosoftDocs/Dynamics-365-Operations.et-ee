--- 
title: "Põhivara tükeldamine"
description: "See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5aea1aab9f6b084bd0c5bd2119639bff3555bb8a
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="split-a-fixed-asset"></a>Põhivara tükeldamine

[!include[task guide banner](../../includes/task-guide-banner.md)]

See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse.  See kasutab raamatupidaja rolli ja USMF-i demoandmeid.


## <a name="create-a-new-fixed-asset"></a>Uue põhivara loomine
1. Minge jaotisse Põhivarad > Põhivarad > Põhivarad.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.
4. Märkige põhivara kood hilisemaks tükeldamisprotsessis kasutamiseks üles.
5. Sisestage väärtus väljale Nimi.
6. Sulgege vorm.

## <a name="split-a-fixed-asset"></a>Põhivara tükeldamine
1. Leidke loendist tükeldatav põhivara ja valige see.
2. Klõpsake loendis valitud real olevat linki.
3. Klõpsake valikut Raamatud.
    * Valige uuele varale tükeldatav raamat.  
4. Klõpsake suvandit Funktsioonid.
5. Klõpsake suvandit Tükelda põhivara.
6. Sisestage väärtus väljale Põhivarasse või valige sellelt väljalt.
7. Klõpsake väljal Raamatusse otsingu avamiseks ripploendi nuppu.
8. Sisestage kuupäev väljale Kande kuupäev.
9. Sisestage number väljale Protsent.
10. Valige või sisestage väärtus väljal Töölehe nimi.
11. Klõpsake nuppu OK.

## <a name="post-the-journal-transaction"></a>Töölehekande sisestamine
1. Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.
2. Valige loendist tükeldamise protsessis loodud tööleht.
3. Klõpsake valikut Read.
    * Kontrollige loodud töölehe ridu.  Soetamise korrigeerimiskanne luuakse algse vara puhul väärtuse vähendamiseks tükeldamisprotsessis määratud protsendi võrra.  Soetamiskanne luuakse uue vara puhul samas summas.  
4. Klõpsake valikut Sisesta.

