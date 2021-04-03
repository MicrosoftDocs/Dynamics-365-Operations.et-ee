---
title: Elektrooniline aruandlus Elektrooniliste dokumentide loomine vormingu konfiguratsiooni kasutavate maksete jaoks
description: Selles teemas kirjeldatakse, kuidas kasutada uut elektroonilise aruandluse (ER) vormingu konfiguratsiooni, et luua maksete töötlemiseks elektrooniline dokument.
author: NickSelin
manager: AnnBe
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
ms.openlocfilehash: 6dd39b3faba90b38b837cd5167b216f9faa31d82
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570212"
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