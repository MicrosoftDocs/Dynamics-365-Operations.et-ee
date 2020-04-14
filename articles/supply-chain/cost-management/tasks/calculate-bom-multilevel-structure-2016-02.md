---
title: Koosluse arvutamine mitmetasandilise struktuuri abil (veebruar 2016)
description: See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat mitmetasandilist koosnevust.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7c35d2b2d5c0fdd14c7e0a35316d482b2e3ffb49
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150430"
---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016"></a>Koosluse arvutamine mitmetasandilise struktuuri abil (veebruar 2016)

[!include [banner](../../includes/banner.md)]

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

