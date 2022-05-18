---
title: Koosluse arvutamine mitmetasandilise struktuuri abil (veebruar 2016)
description: See protseduur näitab, kuidas arvutada lõpetatud toote kulu, kasutades kuluarvutustabelis põhinevat mitmetasandilist koosnevust.
author: JennySong-SH
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f5bfacbcf4238102c5f9f26fdf1a30f5da27fc
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672146"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]