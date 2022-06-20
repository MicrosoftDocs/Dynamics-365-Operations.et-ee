---
title: Elektrooniline aruandlus Elektrooniliste dokumentide loomine vormingu konfiguratsiooni kasutavate maksete jaoks
description: See artikkel kirjeldab, kuidas kasutada uut elektroonilise aruandluse (ER) vormingu konfiguratsiooni maksete töötlemiseks elektrooniliste dokumentide loomiseks.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a79c32372402fcd49f20c855cbfa8d9bcd8ba524
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864597"
---
# <a name="er-generate-electronic-documents-for-payments-using-a-format-configuration"></a>Elektrooniline aruandlus Elektrooniliste dokumentide loomine vormingu konfiguratsiooni kasutavate maksete jaoks

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]