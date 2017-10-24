---
title: Pettuseteatiste seadistamine
description: "Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 09d80015298c3d0219b6ffb290dc456990536a62
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-fraud-alerts"></a>Pettuseteatiste seadistamine

[!include[banner](includes/banner.md)]


Selles teemas kirjeldatakse, kuidas seadistada reegleid, et tellimuste töötlemise käigus teavitada klienditeeninduse esindajaid potentsiaalsetest valeandmetest. Saate määratleda spetsiaalsed koodid, mida kasutatakse kahtlaste tellimust automaatselt või manuaalselt ootele panekuks. 

Enne kui saate seadistada ja kasutada pettuse kontrollimise reegleid, peate aktiveerima kõnekeskuse parameetrites pettuse kontrollimise ja määratlema põhilised pettuse kontrollimise väärtused. Pettuse reegleid on kaht tüüpi.

-   **Staatilised reeglid** kasutavad kindlat väärtust, nagu telefoninumber, mis on kantud musta nimekirja.
-   **Dünaamilised reeglid** saab koostada muutujatest ja tingimustest.

Enne dünaamilise reegli loomist peate looma muutujad ja tingimused, mis määravad, kellele reegel rakendub ja millal tuleb reegel rakendada. Näiteks soovite luua reegli, mis nõuab, et mis tahes müügitellimus, mille klient 1202 esitab väärtusega 1000,00 või rohkem, tuleb panna ootele, kuni kliendimakset saab kontrollida. Sel juhul on muutujateks klient 1202 ja tellimuse kogusumma 1000,00. Tingimus määrab, et kui klient 1202 esitab tellimuse ja tellimuse kogusumma on 1000,00 või suurem, tuleb müügitellimus ootele panna, kuni kliendi makset saab kontrollida.




