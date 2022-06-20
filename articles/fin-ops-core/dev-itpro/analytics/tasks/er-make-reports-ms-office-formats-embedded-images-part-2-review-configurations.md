---
title: Konfiguratsioonide ülevaatamine aruannete loomiseks Office’i vormingus koos manuspiltidega
description: See artikkel kirjeldab, kuidas kujundada aruandluse konfiguratsioone, et luua elektroonilisi dokumente, mis sisaldavad manustatud pilte. (1. osa – näitajate häälestamine).
author: NickSelin
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 365debc2713a7e3ef56b294bade07352fc2089b4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886610"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Konfiguratsioonide ülevaatamine aruannete loomiseks Office’i vormingus koos manuspiltidega

[!include [banner](../../includes/banner.md)]

Toimingute teostamiseks peab esmalt täitma juhendis „ER MS Office'i vormingutes manuspiltidega aruannete koostamine (1. osa: parameetrite häälestamine)” toodud toimingud.

See toiming kirjeldab Microsoft Excelis ja Microsoft Wordis manuspilte sisaldavate elektrooniliste dokumentide loomiseks elektroonilise aruandluse (ER) konfiguratsioonide kujundamist. Selles näites vaatate üle näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse konfiguratsioonid. 

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia USMF-i andmekomplekti abil.


## <a name="review-the-imported-data-model"></a>Vaadake üle imporditud andmemudel
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Valige puus väärtus Tšekkide mudel.
3. Klõpsake valikut Kujundaja.
    * See mudel on ette nähtud maksetšekkide tähistamiseks ettevõtte seisukohast ja selle mudeli vastendamiseks rakenduse andmeallikatega. Vaadake see mudel üle ER-i operatsioonide kujundaja abil. Vaadake esitatud mudelielementide atribuute: struktuur, nimi, kirjeldus, andmetüüp jne.   
4. Laiendage puul valikut „root".
5. Tehke puul valik „root\cheques".
6. Laiendage puul valikut „root\cheques"
7. Laiendage puul valikut „root\cheques\attributes".
8. Laiendage puul valikut „root\payer".
9. Tehke puul valik „root\istestrun".
10. Tehke puul valik „root\layout".
    * Selle mudeli paigutuselement tähistab valitud pangakontoga seotud tšeki printimise vormi paigutuse üksikasju. See hõlmab piltide salvestamiseks ka kaht andmetüübi Konteiner sõlme.   
11. Laiendage puul valikut „root\layout".
12. Tehke puul valik „root\layout\company logo".
13. Laiendage puul valikut „root\layout\company logo".
14. Tehke puul valik „root\layout\company logo\image".
15. Tehke puul valik „root\layout\company logo\isprinted".
16. Tehke puul valik „root\layout\signature"
17. Laiendage puul valikut „root\layout\signature".
18. Tehke puul valik „root\layout\signature\image".
19. Tehke puul valik „root\layout\signature\isprinted".
    * Pange tähele, et kaks pildi andmemudeli elementi on seotud nende tabelite väljadega, mis sisaldavad binaarvormingus ettevõtte logo ja volitatud isiku allkirja.  
20. Laiendage puul valikut „root\layout\watermark".
21. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
22. Klõpsake valikut Kujundaja.
23. Laiendage puul valikut „chequesselected".
24. Laiendage puus valik layout.
25. Laiendage puul valikut „layout\company logo".
26. Laiendage puus valik „layout\signature“.
27. Laiendage puul valikut „layout\watermark".
28. Lülitage nupp Kuva üksikasjad sisse.
    * Pange tähele, et tšekkide andmemudeli element on seotud tabeliga TmpChequePrintout, mis sisaldab käitusajal nende tšekkide kirjeid, mille kasutaja on valinud printimiseks.   
29. Sulgege leht.
30. Sulgege leht.
31. Sulgege leht.

## <a name="review-the-imported-format"></a>Vaadake üle imporditud vorming
1. Laiendage puus valik Tšekkide mudel.
2. Valige puus „Model for cheques\Cheques printing format“.
3. Klõpsake valikut Kujundaja.
4. Klõpsake suvandit Manused.
5. Klõpsake valikut Ava.
    * Avage manustatud aruande mall Excelis.  
    * Vaadake läbi manustatud aruande Exceli mall, mida kasutatakse tšekkide printimiseks. Mall sisaldab kaht tšekki lehe kohta ja see on mõeldud tšekkide printimiseks eelprinditud vormile. Võtke arvesse, et kaks tühja pilti on manustatud. Tühjad pildid on ette nähtud ettevõtte logo ja makse autoriseerija allkirja jaoks. Veenduge, et piltidel on Excelis vastavalt nimed CompLogo ja SignatureImage.   
6. Sulgege leht.
7. Laiendage puul valikut „Report".
8. Laiendage puul valikut „Report\ChequeLines".
9. Tehke puul valik „Report\ChequeLines\CompLogo".
10. Lülitage nupp Kuva üksikasjad sisse.
    * Pange tähele, et pildi „CompLogo” vormingu lahtrielement tähistab Exceli üksust, mille abil täidetakse aruandes ettevõtte logo pilt. See vorming on seotud pildi andmemudeli elemendiga, mis sisaldab käitusajal ettevõtte logo binaarvormingus pilti.   
11. Klõpsake vahekaarti Vastendus.
12. Klõpsake valikut Redigeerimine on lubatud.
    * Pange tähele, et saate luua „CompLogo" vormingu lahtrielemendi sel viisil, et see pole enam lubatud. Sel juhul peidab Exceli seotud pildielement loodud aruandes ettevõtte logo. Kui lubatud avaldis tagastab väärtuse TRUE ja määratletud seos ei kuva pilti, kuvab Exceli seotud pildielement Exceli malli salvestatud pilti.   
13. Sulgege leht.
14. Laiendage puul valikut „labels: Container".
    * Mõned eelprinditud tšekivormidel olevad sildid kaasatakse aruandesse selle testimise eesmärgil loomisel. Neid silte aga ei prindita reaalse printimise ajal, kuna eelprinditud vorm juba sisaldab neid.  
15. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]