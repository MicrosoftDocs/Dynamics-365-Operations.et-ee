---
title: Vabas vormis arve malli määramine kliendile
description: See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d9535a4678ea0c68227a54cf3c5d1b06b116a288
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916342"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Vabas vormis arve malli määramine kliendile

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall. See ülesanne kasutab demoettevõtet USMF ja on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.

1. **Navigeerimispaan**il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.
2. Otsige loendist ja valige soovitud kirje.
3. Paanil **Toimingupaan** klõpsake **Arve**.
4. Klõpsake **Korduvad arved**. Kasutage seda lehte klientidele vabas vormis arve määramiseks ja määratlemaks, kui sageli arveid kliendile saadetakse.  
5. Klõpsake **Uus**, et määrata kliendile uus mall.
6. Väljal **Mall** valige vabas vormis arve mall, mille soovite kliendile määrata.
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Väljale **Arvelduse alguskuupäev** sisestage kuupäev, millal koostatakse esimene arve.
10. Jaotisesse **Kordumise lõpp** sisestage kordumise lõppkuupäev.  
    * Valige üks järgmistest: Lõppkuupäev puudub – arveid luuakse lõputult, kuni mall kliendi kontolt eemaldatakse.
    * Arvelduse lõppkuupäev – valige see suvand ja sisestage viimane kuupäev, millal arvet saab koostada.  
11. Väljale **Maksimaalne kumulatiivne summa** sisestage maksimaalne kumulatiivne summa, pärast mida lõpetatakse arve koostamine. Sisestage maksimaalne kumulatiivne summa, mille saab valitud malli abil saavutada. Näiteks kui sisestate 1000,00 ja loote iga kuu puhul 100,00 arvet, peatatakse arvete loomine pärast kümnenda arve loomist.  
12. Jaotises **Loo korduvaid arved, kasutades vaikeväärtusi** valige kas vabas vormis arve mall või kliendi konto. Valige, kas kasutada vaba teksti arve malli või kliendi kontot, et määrata keele, sisestusreeglite, käibemaksugrupi, loendikoodi, tarneriigi/-piirkonna, valuuta, maksetingimuste, makseviisi, maksetäpsustuse, maksegraafiku, skonto, finantsdimensioonide ja maksekorralduse vaikeväärtused arvete koostamisel.  
13. Väljal **Kordumissagedus** valige kordumissagedus.
    + Iga päev – valige see suvand ja sisestage päevade arv väljale Kohta. Näiteks kui sisestate 15, koostatakse arve sellele kliendile iga 15 päeva tagant.
    + Iga nädal – valige see suvand ja sisestage nädalate arv väljale Kohta. Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe nädala tagant.
    + Iga kuu – valige see suvand ja sisestage kuude arv väljale Kohta. Näiteks kui sisestate 6, koostatakse arve sellele kliendile iga kuue kuu tagant.
    + Iga aasta – valige see suvand ja sisestage aastate arv väljale Kohta. Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe aasta tagant.  
14. Väljale **Kohta** sisestage arv.

