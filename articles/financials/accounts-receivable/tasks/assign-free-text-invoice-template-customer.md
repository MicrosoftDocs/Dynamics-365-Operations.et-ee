---
title: Vabas vormis arve malli määramine kliendile
description: See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 53bff33083a78c0bb1c7d243fe9965fb264d209e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843045"
---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Vabas vormis arve malli määramine kliendile

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesanne näitab, kuidas määrata kliendile vabas vormis arve mall. See ülesanne kasutab demoettevõtet USMF ja on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.

1. Avage Müügireskontro > Kliendid > Kõik kliendid.
2. Otsige loendist ja valige soovitud kirje.
3. Klõpsake toimingupaanil valikut Arve.
4. Klõpsake suvandit Korduvad arved.
    * Kasutage seda lehte klientidele vabas vormis arve määramiseks ja määratlemaks, kui sageli arveid kliendile saadetakse.  
5. Klõpsake kliendile uue malli määramiseks suvandit Uus.
6. Valige vabas vormis arve mall, mille soovite kliendile määrata.
7. Otsige loendist ja valige soovitud kirje.
8. Klõpsake loendis valitud real olevat linki.
9. Sisestage esimese arve loomise kuupäev.
    * Sisestage korduv lõppkuupäev.  
    * Valige üks järgmistest: Lõppkuupäev puudub – arveid luuakse lõputult, kuni mall kliendi kontolt eemaldatakse.  Arvelduse lõppkuupäev – valige see suvand viimase päeva sisestamiseks, millal arvet saab koostada.  
    * Maksimaalne kumulatiivne summa, mille järel arve loomine peatatakse.  
    * Sisestage maksimaalne kumulatiivne summa, mille saab valitud malli abil saavutada. Näiteks kui sisestate 1000,00 ja loote iga kuu puhul 100,00 arvet, peatatakse arvete loomine pärast kümnenda arve loomist.  
    * Looge korduvaid arveid, kasutades kas vabas vormis arve malli või kliendikonto vaikeväärtusi.  
    * Valige, kas kasutada vaba teksti arve malli või kliendi kontot, et määrata keele, sisestusreeglite, käibemaksugrupi, loendikoodi, tarneriigi/-piirkonna, valuuta, maksetingimuste, makseviisi, maksetäpsustuse, maksegraafiku, skonto, finantsdimensioonide ja maksekorralduse vaikeväärtused arvete koostamisel.  
10. Valige kordumismuster.
    * Iga päev – valige see suvand ja sisestage päevade arv väljale Kohta. Näiteks kui sisestate 15, koostatakse arve sellele kliendile iga 15 päeva tagant.  Iga nädal – valige see suvand ja sisestage nädalate arv väljale Kohta. Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe nädala tagant.  Iga kuu – valige see suvand ja sisestage kuude arv väljale Kohta. Näiteks kui sisestate 6, koostatakse arve sellele kliendile iga kuue kuu tagant.  Iga aasta – valige see suvand ja sisestage aastate arv väljale Kohta. Näiteks kui sisestate 2, koostatakse arve sellele kliendile iga kahe aasta tagant.  
11. Sisestage number väljale Kohta.

