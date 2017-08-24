--- 
title: "Elektroonilise aruandluse (ER) konfiguratsiooni üles laadimine teenusesse Lifecycle Services"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni ja laadida selle teenusesse Microsoft Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: e0681ff81ea673e90b3d281a8e8836e0afb9f5f0
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) konfiguratsiooni üles laadimine teenusesse Lifecycle Services

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue elektroonilise aruandluse (ER) konfiguratsiooni ja laadida selle teenusesse Microsoft Lifecycle Services (LCS).

Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. ja laadite selle üles LCS-i. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised. Etappide lõpuleviimiseks, peate esmalt läbima protseduuri Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine etapid. Juurdepääs LCS-i on nõutav ka nende toimingute lõpetamiseks.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Valige Litware, inc. ja määrake see aktiivseks.
3. Klõpsake suvandit Konfiguratsioonid.

## <a name="create-a-new-data-model-configuration"></a>Uue andmemudeli konfiguratsiooni loomine
1. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
    * Loote konfiguratsiooni, mis sisaldab elektrooniliste dokumentide andmemudeli näidist. Selle andmemudeli konfiguratsioon laaditakse hiljem LCS-i.  
2. Tippige väljale Nimi tekst Mudeli konfiguratsiooni näide.
    * Mudeli konfiguratsiooni näide  
3. Tippige väljale Kirjeldus tekst Mudeli konfiguratsiooni näide.
    * Mudeli konfiguratsiooni näide  
4. Klõpsake Loo konfiguratsioon.
5. Klõpsake suvandit Mudeli koostaja.
6. Klõpsake valikut Uus.
7. Tippige väljale Nimi tekst Sisestuspunkt.
    * Sisestuspunkt  
8. Klõpsake vahekaarti Lisa.
9. Klõpsake nuppu Salvesta.
10. Sulgege leht.
11. Klõpsake valikut Muuda olekut.
12. Klõpsake valikut Valmis.
13. Klõpsake nuppu OK.

## <a name="register-a-new--repository"></a>Uue hoidla registreerimine
1. Sulgege leht.
2. Klõpsake valikut Hoidlad.
    * See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.  
3. Klõpsake valikut Lisa rippdialoogi avamiseks.
    * See võimaldab lisada uue hoidla.  
4. Tehke väljal Konfiguratsioonihoidla tüüp valik LCS.
5. Klõpsake käsku Loo hoidla.
6. Valige või sisestage väärtus väljal Projekt.
    * Valige soovitud LCS-i projekt. Teil peab olema juurdepääs projektile.  
7. Klõpsake nuppu OK.
    * Täitke uus hoidla kirje.  
8. Märkige loendis valitud rida.
    * Valige LCS-i hoidla kirje.  
    * Pange tähele, et registreeritud hoidla on praeguse pakkuja tähistatud, mis tähendab, et sellesse hoidlasse saab paigutada ja valitud LCS-projekti üles laadida ainult need konfiguratsioonid, mille omanik see pakkuja on.  
9. Klõpsake valikut Ava.
    * Avage hoidla ER-i konfiguratsioonide loendi vaatamiseks. See on tühi, kui seda projekti pole veel kasutatud ER-i konfiguratsioonide ühiskasutuseks.  
10. Sulgege leht.
11. Sulgege leht.

## <a name="upload-configuration-into-lcs"></a>Konfiguratsiooni üleslaadimine LCS-i
1. Klõpsake suvandit Konfiguratsioonid.
2. Valige puul väärtus Mudeli konfiguratsiooni näide.
    * Valige loodud konfiguratsioon, mis on juba lõpule viidud.  
3. Otsige loendist ja valige soovitud kirje.
    * Valige valitud konfiguratsiooni versioon, mille olek on Lõpule viidud.  
4. Klõpsake valikut Muuda olekut.
5. Klõpsake nuppu Jaga.
    * Konfiguratsiooni olek muutub olekust Lõpule viidud olekuks Ühiskasutuses, kui see avaldatakse LCS-is.  
6. Klõpsake nuppu OK.
7. Otsige loendist ja valige soovitud kirje.
    * Valige konfiguratsiooni versioon olekuga Ühiskasutuses.  
    * Pange tähele, et valitud versiooni olek on muudetud olekus Lõpule viidud olekuks Ühiskasutuses.  
8. Sulgege leht.
9. Klõpsake valikut Hoidlad.
    * See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.  
10. Klõpsake valikut Ava.
    * Valige LCS-hoidla ja avage see.  
    * Pange tähele, et valitud konfiguratsiooni näidatakse valitud LCS-i projekti varana.  
    * Avage LCS, kasutades aadressi https://lcs.dynamics.com. Avage projekt, mida kasutasite varem hoidla registreerimiseks, avage projekti varateek ja laiendage GER-i konfiguratsiooni vara tüübi sisu – üleslaaditud ER-i konfiguratsioon on saadaval. Pange tähele, et üleslaaditud LCS-i konfiguratsiooni saab importida teise Microsoft Dynamics 365 for Finance and Operations, Enterprise edition eksemplari, kui teenuse pakkujatel on juurdepääs sellele LCS-i projektile.  


