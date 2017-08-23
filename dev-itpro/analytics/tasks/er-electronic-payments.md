--- 
title: Elektroonilise aruandluse (ER) elektrooniliste dokumentide genereerimine maksete jaoks vormingu konfiguratsiooni abil
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kasutada uue elektroonilise aruandluse (ER) vormingu konfiguratsiooni elektrooniliste dokumentide loomiseks maksete töötlemise puhul."
author: NickSelin
manager: AnnBe
ms.date: 11/10/2016
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
ms.openlocfilehash: 95da806cc2844dc946e809f1afecef25a7b520e5
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="generate-electronic-documents-for-payments-using-a-format-configuration-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) elektrooniliste dokumentide genereerimine maksete jaoks vormingu konfiguratsiooni abil

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad kasutada uue elektroonilise aruandluse (ER) vormingu konfiguratsiooni elektrooniliste dokumentide loomiseks maksete töötlemise puhul. Neid toiminguid saab teha GBSI näidisettevõttes.

Etappide lõpuleviimiseks peate esmalt läbima etapid protseduuris Maksedokumendi vorminguga konfiguratsiooni loomine.


## <a name="change-the-configuration-of-the-electronic-payment-method"></a>Elektrooniline makseviisi konfiguratsiooni muutmine
1. Avage Ostureskontro > Makse seadistus > Makseviisid.
2. Vajaduse korral vajutage jaotise Failivorming lülitusnuppu, et seda laiendada.
3. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks filtreerige välja Makseviis väärtusega Elektrooniline.
4. Klõpsake nuppu Redigeeri.
5. Määrake välja Üldine elektrooniline aruandlus väärtuseks Jah.
    * Tehke valik Jah, et kasutada üldist elektroonilise aruandluse mustrit maksefailide loomiseks.  
6. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
7. Valige BACS-i (UK fiktiivne) vormingu konfiguratsioon.
8. Klõpsake nuppu Salvesta.
9. Sulgege leht.

## <a name="test-the-format-of-generated-payment-files"></a>Loodud maksefailide vormingu testimine
1. Avage Ostureskontro > Maksed > Makse tööleht.
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
    * Tehke valik VendPay.  
6. Klõpsake nuppu Salvesta.
7. Klõpsake valikut Read.
8. Tippige väljale Ettevõte väärtus DEMF.
    * DEMF  
9. Määrake väljal Konto 'DE-01001' väärtused.
    * DE – 01001  
10. Tippige väljale Kirjeldus väärtus Makse.
    * Makse  
11. Sisestage arv väljale Deebet.
    * 1000  
12. Klõpsake vahekaarti Makse.
13. Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.
14. Otsige loendist ja valige soovitud kirje.
    * Valige elektrooniline väärtus.  
15. Klõpsake loendis valitud real olevat linki.
16. Klõpsake nuppu Salvesta.
17. Klõpsake valikut Loo maksed.
18. Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.
19. Otsige loendist ja valige soovitud kirje.
    * Valige elektrooniline väärtus.  
20. Klõpsake loendis valitud real olevat linki.
    * Valige elektrooniline väärtus.  
21. Sisestage väärtus väljale Faili nimi.
    * Tippige näiteks väärtus Maksed.  
22. Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.
23. Klõpsake loendis valitud real olevat linki.
    * Valige väärtus GBSI OPER.  
24. Klõpsake nuppu OK.
25. Klõpsake nuppu OK.
    * Analüüsige loodud maksefaili XML-vormingus. Võrrelge seda koostatud dokumendi paigutusega ja määratletud maksekande atribuutidega.  


