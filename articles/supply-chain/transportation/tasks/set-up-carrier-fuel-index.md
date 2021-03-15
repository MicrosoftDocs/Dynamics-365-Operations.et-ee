---
title: Vedaja kütuseindeksi seadistamine
description: See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 772468fa73e18a02331f877a375a5bd089ece6be
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004923"
---
# <a name="set-up-a-carrier-fuel-index"></a>Vedaja kütuseindeksi seadistamine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]