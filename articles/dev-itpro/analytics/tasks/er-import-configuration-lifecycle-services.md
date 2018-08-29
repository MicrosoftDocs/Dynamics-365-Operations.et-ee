--- 
title: Elektroonilise aruandluse konfiguratsioonide importimine teenusest Lifecycle Services
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Lifecycle Services (LCS)."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f3b8cdb722cf49194faccc19fbb95265a230d48b
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="import-electronic-reporting-configurations-from-lifecycle-services"></a>Elektroonilise aruandluse konfiguratsioonide importimine teenusest Lifecycle Services

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida uue elektroonilise aruandluse (ER) konfiguratsiooni teenusest Microsoft Lifecycle Services (LCS).

Selles näites valite soovitud ER-i konfiguratsiooni ja impordite selle näidisettevõttele Litware, Inc. Neid etappe saab läbida mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtete seas ühiskasutuses. Etappide lõpuleviimiseks, peate esmalt läbima protseduuri ER-i konfiguratsiooni üleslaadimine teenusesse Lifecycle Services etapid. Juurdepääs LCS-i on nõutav ka nende toimingute lõpetamiseks.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake suvandit Konfiguratsioonid.

## <a name="delete-a-shared-version-of-data-model-configuration"></a>Andmemudeli konfiguratsiooni ühiskasutuses versiooni kustutamine
1. Valige puul väärtus Mudeli konfiguratsiooni näide.
    * Andmemudeli konfiguratsiooni esimene versioon on loodud ja avaldatud LCS-is protseduuri ER-i konfiguratsiooni üleslaadimine teenusesse Lifecycle Services ajal. Selle protseduuri käigus kustutate selle ER-i konfiguratsiooni versiooni. See andmemudeli näidiskonfiguratsiooni versioon imporditakse hiljem LCS-ist.  
2. Otsige loendist ja valige soovitud kirje.
    * Valige selle konfiguratsiooni versioon, mis on olekus Ühiskasutuses. See olek näitab, et konfiguratsioon on avaldatud LCS-is.  
3. Klõpsake valikut Muuda olekut.
4. Klõpsake nuppu Katkesta.
    * Muutke valitud versiooni olek Ühiskasutuses olekuks Katkestatud, et muuta see kustutamiseks kättesaadavaks  
5. Klõpsake nuppu OK.
6. Otsige loendist ja valige soovitud kirje.
    * Valige selle konfiguratsiooni versioon, mille olek on Katkestatud.  
7. Klõpsake  Kustuta.
8. Klõpsake nuppu Jah.
    * Pange tähele, et saadaval on ainult valitud andmemudeli konfiguratsiooni mustandversioon 2.  
9. Sulgege leht.

## <a name="import-a-shared-version-of-data-model-configuration-from-lcs"></a>Andmemudeli konfiguratsiooni ühiskasutuses versiooni importimine LCS-ist
1. Märkige loendis valitud rida.
    * Avage ettevõtte Litware, Inc. hoidlate loend. konfiguratsiooni pakkuja jaoks.  
2. Klõpsake valikut Hoidlad.
3. Klõpsake valikut Ava.
    * Valige LCS-hoidla ja avage see.  
4. Märkige loendis valitud rida.
    * Valige versiooni loendist suvandi Mudeli konfiguratsiooni näide esimene versioon.  
5. Klõpsake Import.
6. Klõpsake nuppu Jah.
    * Kinnitage valitud versiooni import LCS-ist.  
    * Pange tähele, et tebeteade (vormi kohal) kinnitab valitud versiooni impordi lõpuleviimise.  
7. Sulgege leht.
8. Sulgege leht.
9. Klõpsake suvandit Konfiguratsioonid.
10. Valige puul väärtus Mudeli konfiguratsiooni näide.
11. Otsige loendist ja valige soovitud kirje.
    * Valige selle konfiguratsiooni versiooni, mille olek on Ühiskasutuses.  
    * Pange tähele, et nüüd on saadaval ka valitud andmemudeli konfiguratsiooni ühiskasutatav versioon 1.  


