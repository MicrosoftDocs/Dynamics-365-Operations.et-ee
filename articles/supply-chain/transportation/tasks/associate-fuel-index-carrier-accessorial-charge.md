---
title: Kütuseindeksi seostamine vedajaga lisatasuna
description: See juhend näitab, kuidas luua lisade määramist, vedaja lisatasu, lisade koondandmeid kütuse lisatasu puhul ja kuidas seostada vedaja kütuseindeksit vedajaga.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c91d49c2ccdc274632e3acf94b836e19dc6cdaa8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016996"
---
# <a name="associate-a-fuel-index-with-a-carrier-as-an-accessorial-charge"></a>Kütuseindeksi seostamine vedajaga lisatasuna

[!include [banner](../../includes/banner.md)]

See juhend näitab, kuidas luua lisade määramist, vedaja lisatasu, lisade koondandmeid kütuse lisatasu puhul ja kuidas seostada vedaja kütuseindeksit vedajaga. Enne selle juhendi käivitamist peab teil olema vedaja kütuseindeks seadistatud. Saate selleks kasutada juhendit „Vedaja kütuseindeksi seadistamine”. Neid seadistustoiminguid teeb üldjuhul logistika haldur. Selle protseduuri loomiseks kasutati demoandmeid USMF.


## <a name="create-an-accessorial-master"></a>Lisade koondandmete loomine
1. Avage Transpordihaldus > Seadistus > Hinnang > Lisade koondandmed.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Lisade koondandmed.
4. Sisestage väärtus väljale Nimi.
5. Klõpsake nuppu Salvesta.

## <a name="create-a-carrier-accessorial-charge"></a>Vedaja lisatasu loomine
1. Avage Transpordihaldus > Seadistus > Hinnang > Vedaja lisatasud.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Vedaja lisade ID.
4. Klõpsake väljal Kättetoimetaja otsingu avamiseks ripploendi nuppu.
5. Otsige loendist ja valige soovitud kirje.
    * Selles näites valige veoki vedaja.  
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake väljal Vedaja teenus otsingu avamiseks ripploendi nuppu.
8. Klõpsake loendis valitud real olevat linki.
9. Klõpsake väljal Lisade koondandmed otsingu avamiseks ripploendi nuppu.
10. Otsige loendist ja valige soovitud kirje.
    * Selle näite puhul valige äsja loodud lisade koond.  
11. Klõpsake nuppu Salvesta.

## <a name="create-an-accessorial-assignment"></a>Lisade määrangu loomine
1. Klõpsake suvandit Lisade määrangud.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Nimi.
4. Laiendage jaotist Kriteeriumid.
    * Kriteeriumides saate alati valida kütuse lisatasu rakendamise või näiteks selle, et see kehtib ainult teatud regioonis.  
5. Sisestage väärtus väljale Sihtnumber alates.
6. Sisestage väärtus väljale Sihtnumber kuni.
7. Laiendage jaotist Arvutamine.
    * Arvutamise jaotises saate määrata, kuidas kütuse lisatasu arvutada. Arvutamine oleneb teie arvutuse aluseks valitud lisade ühikust.  
8. Valige väljal Lisatasu tüüp suvand Kütuse lisatasu.
9. Valige väljal Lisade ühik suvand Läbisõit.
10. Klõpsake väljal Regioon otsingu avamiseks ripploendi nuppu.
11. Klõpsake loendis valitud real olevat linki.
12. Klõpsake nuppu Salvesta.

## <a name="update-the-carrier-rating-profile"></a>Vedaja hinnanguprofiili värskendamine
1. Tehke valik Transpordi haldus > Seadistus > Vedajad > Kättetoimetajad.
2. Otsige loendist ja valige soovitud kirje.
3. Laiendage jaotist Hinnanguprofiilid.
4. Klõpsake nuppu Redigeeri.
5. Klõpsake väljal Vedaja kütuseindeks otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake nuppu Salvesta.

