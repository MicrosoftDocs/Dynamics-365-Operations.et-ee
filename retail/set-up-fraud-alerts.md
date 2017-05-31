---
title: Pettuseteatiste seadistamine
description: "Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 7255f2b7e49f56a731d0e3745b4752091013668b
ms.contentlocale: et-ee
ms.lasthandoff: 05/25/2017


---

# <a name="set-up-fraud-alerts"></a>Pettuseteatiste seadistamine

[!include[banner](includes/banner.md)]


Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks. 

Enne kui saate seadistada ja kasutada pettuse kontrollimise reegleid, peate aktiveerima kõnekeskuse parameetrites pettuse kontrollimise ja määratlema põhilised pettuse kontrollimise väärtused. Pettuse reegleid on kaht tüüpi.

-   **Staatilised reeglid** kasutavad kindlat väärtust, nagu telefoninumber, mis on kantud musta nimekirja.
-   **Dünaamilised reeglid** saab koostada muutujatest ja tingimustest.

Enne dünaamilise reegli loomist peate looma muutujad ja tingimused, mis määravad, kellele reegel rakendub ja millal tuleb reegel rakendada. Näiteks soovite luua reegli, mis nõuab, et mis tahes müügitellimus, mille klient 1202 esitab väärtusega 1000,00 või rohkem, tuleb panna ootele, kuni kliendimakset saab kontrollida. Sel juhul on muutujateks klient 1202 ja tellimuse kogusumma 1000,00. Tingimus määrab, et kui klient 1202 esitab tellimuse ja tellimuse kogusumma on 1000,00 või suurem, tuleb müügitellimus ootele panna, kuni kliendi makset saab kontrollida.




