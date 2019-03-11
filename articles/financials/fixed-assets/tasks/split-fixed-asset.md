---
title: Põhivara tükeldamine
description: See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333365"
---
# <a name="split-a-fixed-asset"></a>Põhivara tükeldamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

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

