---
title: Vedaja kütuseindeksi seadistamine
description: See juhend näitab, kuidas luua kütuseindeksi regiooni, kütuseindeksit ja vedaja kütuseindeksit.
author: Weijiesa
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb976369f9e8254f76a4de18df619d4420cf0538
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672678"
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