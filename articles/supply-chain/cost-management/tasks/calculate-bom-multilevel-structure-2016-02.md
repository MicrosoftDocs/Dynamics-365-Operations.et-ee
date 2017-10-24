--- 
title: Koosluse arvutamine mitmetasandilise struktuuri abil (ainult veebruar 2016)
description: "See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat mitmetasandilist koosnevust."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Koosluse arvutamine mitmetasandilise struktuuri abil (ainult veebruar 2016)

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat mitmetasandilist koosnevust. See on seitsmes ülesanne koosluse arvutamise seerias. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.

1. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
2. Otsige loendist ja valige soovitud kirje.
    * Valige toode BOM_1.  
3. Klõpsake toimingupaanil valikut Kulude haldamine.
4. Klõpsake nuppu Kauba hind.
5. Klõpsake nuppu Kauba kulu arvutamine.
    * Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.  
6. Väljal Kuluversioon sisestage või valige väärtus.
    * Valige kuluversioon 20, kuna see on kulutüüp Plaanitud ja režiim Koosnemine on Mitmetasemeline.   Mitmetasandilise koosnevuse režiim on mõeldud plaanitud kuludele ja simulatsioonidele. Seda ei kasutata standardkulu jaoks.  
7. Klõpsake nuppu OK.
8. Klõpsake suvandit Kuva arvutamise üksikasjad.
    * Peate vajaduse korral klõpsama kolmikpunkti (...), et näha seda suvandit peamenüüs.  Sellisel juhul pange tähele, kuidas BOM_2 on arvutatud, arvestades seeria algses tegevusejuhises aktiveeritud standardkulu 10 asemel toormaterjali, protsessi ja üldkulusid kogusummas 29,40.  
9. Klõpsake vahekaarti Kuluarvutustabel.
    * Liikudes vahekaardile Kuluarvutustabel, on kogusummad kulugrupi kohta eelmises tegevusejuhises tehtud arvutusega võrreldes erinevad.  
10. Väljal Tase valige Mitu.
    * Valides suvandi Mitu, klassifitseeritakse kulud BOM_2 koosnevuse järgi, kus 10 tuletatakse M1 kulugrupist (ITEM_C) ja 15,60 tuletatakse selle tootmisest, kus kulugrupp on L2. Kaudsed kulud varieeruvad samuti.  
11. Sulgege leht.
12. Sulgege leht.


