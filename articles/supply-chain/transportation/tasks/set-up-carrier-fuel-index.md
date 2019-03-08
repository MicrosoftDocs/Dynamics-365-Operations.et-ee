---
title: Vedaja kütuseindeksi seadistamine
description: See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b6f72de7ad54a2b2dc1bf40fd8cb86d8b055e2d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "366577"
---
# <a name="set-up-a-carrier-fuel-index"></a>Vedaja kütuseindeksi seadistamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit. Kütuseindeksi regioon määrab, millisele regioonile tuleks kütuseindeksit rakendada ja kütuseindeks määrab kütuse hinna teatud aja jooksul. Kütusehinna muudatuste kajastamiseks aja jooksul saate vedajaga seostada mitu kütuseindeksit.  Neid ülesandeid teeb üldjuhul transpordikoordinaator. Saate selle protseduuriga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.


## <a name="create-a-fuel-index-region"></a>Kütuseindeksi regiooni loomine
1. Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksi regioonid.
    * Esmalt peate looma erinevad regioonid, kus töötada, ja arvutama erinevad kütuse lisatasud.  
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Regioon.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake nuppu Salvesta.

## <a name="create-a-fuel-index"></a>Saate luua ka kütuseindeks
1. Avage Transpordihaldus > Seadistus > Kütuseindeksid > Kütuseindeksid.
    * Seadistatud regioonide puhul peate sisestama kütuse praegused hinnad.  
2. Klõpsake valikut Uus.
3. Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage number väljale Galloni hind.
6. Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.
7. Klõpsake nuppu Salvesta.

## <a name="create-a-carrier-fuel-index"></a>Vedaja kütuseindeksi loomine
1. Avage Transpordihaldus > Seadistus > Kütuseindeksid > Vedaja kütuseindeksid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Vedaja kütuseindeks.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake Uus.
6. Sisestage kuupäev ja kellaaeg väljale Jõustumise alguskuupäev ja -kellaaeg.
7. Sisestage number väljale Galloni hind alates.
    * Selles näites saate seadistada välja Galloni hind alates väärtusele 1,95.  
8. Sisestage number väljale Galloni hind kuni.
    * Selles näites saate seadistada välja Galloni hind kuni väärtusele 2.  
9. Sisestage number väljale Protsent.
    * Selles näites saate seadistada protsendi väärtusele 3.  
10. Klõpsake väljal Valuuta otsingu avamiseks ripploendi nuppu.
11. Otsige loendist ja valige soovitud kirje.
12. Klõpsake loendis valitud real olevat linki.
13. Klõpsake nuppu Salvesta.

