---
title: Vabas vormis arve malli määramine kliendile
description: See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 49074c11659ae30fd2decdb93b4721441edff2c5
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780236"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Vabas vormis arve malli määramine kliendile

[!include [banner](../../includes/banner.md)]

See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall. See ülesanne kasutab demoettevõtet USMF ja on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.

1. **Navigeerimispaan** il avage **Moodulid > Müügireskontro > Kliendid > Kõik kliendid**.
2. Otsige loendist ja valige soovitud kirje.
3. Paanil **Toimingupaan** klõpsake **Arve**.
4. Klõpsake **Korduvad arved**. Kasutage seda lehte klientidele vabas vormis arve määramiseks ja määratlemaks, kui sageli arveid kliendile saadetakse.  
5. Klõpsake **Uus**, et määrata kliendile uus mall.
6. Väljal **Mall** valige vabas vormis arve mall, mille soovite kliendile määrata.
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Väljale **Arvelduse alguskuupäev** sisestage kuupäev, millal koostatakse esimene arve.
10. Jaotisesse **Kordumise lõpp** sisestage kordumise lõppkuupäev.  
    Valige üks järgmistest. 
    - **Lõppkuupäev puudub** – arved luuakse piiramatult seni, kuni mall kliendikontolt eemaldatakse.
    - **Arvelduse lõppkuupäev** – valige see suvand ja sisestage viimane kuupäev, millal arvet saab luua.  
11. Väljale **Maksimaalne kumulatiivne summa** sisestage maksimaalne kumulatiivne summa, pärast mida lõpetatakse arve koostamine. Sisestage maksimaalne kumulatiivne summa, mille saab valitud malli abil saavutada. Näiteks kui sisestate 1000,00 ja loote iga kuu puhul 100,00 arvet, peatatakse arvete loomine pärast kümnenda arve loomist.  
12. Jaotises **Loo korduvaid arved, kasutades vaikeväärtusi** valige kas vabas vormis arve mall või kliendi konto. Valige, kas kasutada vaba teksti arve malli või kliendi kontot, et määrata keele, sisestusreeglite, käibemaksugrupi, loendikoodi, tarneriigi/-piirkonna, valuuta, maksetingimuste, makseviisi, maksetäpsustuse, maksegraafiku, skonto, finantsdimensioonide ja maksekorralduse vaikeväärtused arvete koostamisel.  
13. Väljal **Kordumissagedus** valige kordumissagedus.
    - **Igapäevane** – valige see suvand ja sisestage päevade arv väljale Per. Näiteks kui sisestate 15, koostatakse arve sellele kliendile iga 15 päeva tagant.
    - **Kord** nädalas – valige see suvand ja sisestage nädalate arv väljale Nädala kohta. Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe nädala tagant.
    - **Igakuine** : valige see suvand ja sisestage kuude arv väljale Igakuine. Näiteks kui sisestate 6, koostatakse arve sellele kliendile iga kuue kuu tagant.
    - **Kord aastas** : valige see suvand ja sisestage väljale Aastate arv. Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe aasta tagant.  
14. Väljale **Kohta** sisestage arv.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
