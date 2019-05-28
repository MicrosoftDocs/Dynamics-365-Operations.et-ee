---
title: Kohaldatavate hindade ja allahindluste otsimine
description: See protseduur näitab, kuidas leida kindlale kliendile kehtivat toote hinda ja/või allahindlust ilma müügitellimust loomata.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ba95e651898da0e0fbd1221f61436ffac59db09e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549240"
---
# <a name="look-up-applicable-prices-and-discounts"></a>Kohaldatavate hindade ja allahindluste otsimine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas leida kindlale kliendile kehtivat toote hinda ja/või allahindlust ilma müügitellimust loomata. Protseduur selgitab konkreetse näite kaudu, kuidas valida vajalikud väärtused, kasutades demoettevõtte USMF andmeid.


## <a name="find-the-applicable-price"></a>Kohalduva hinna leidmine
1. Avage Müük ja turundus > Hinnad ja allahindlused > Hindade otsimine.
2. Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.
3. Leidke ja valige loendist klient US-001.
4. Klõpsake loendis valitud real olevat linki.
5. Sisestage väljale Kaubakood tüüp T0004.
    * Vaikimisi on välja Kogus väärtuseks määratud 1. Kui aga teate, kui suurt tellimust soovib klient kõnealusele tootele teha, sisestage see väärtus. See teave on oluline, kui kliendiga sõlmitud kaubanduslepetel on kogusekatkestusi, mis tähendab, et toote hind sõltub minimaalsest ostetud kogusest.  
6. Sisestage väljale Kuupäev see kuupäev, millal klient soovib tellimuse esitada. 
    * Kuupäev võib olla täna või millal tahes tulevikus.  
    * Süsteem tagastab nüüd hinna, mis kehtib valitud tootele, kui valitud klient on selle ostnud valitud kuupäeval ja määratud koguses. Selles näites: kui klient US-001 ostis täna 1 ühiku toodet T0004, peab ta maksma 350 Kanda dollarit ühiku eest. Hind tuleneb kliendiga sõlmitud olemasolevast ja aktiivsest kaubandusleppest.      Lehe muud väljad pakuvad lisateavet toote hinna ja toote kulu kohta (kui need on tooteetalonis seadistatud) ning arvutatud tulususe.  
    * Kui valitud on suvand Kuva seotud tootevariandid, tähendab see, et toote variantide kohta on olemas täiendavad kaubanduslepped.  
7. Märkige ruut Kuva seotud tootevariandid.
    * Kuvatakse tootevariantide loend koos teabega nende dimensioonide kohta.  
8. Märkige loendis valget värvi tähistav rida.
    * Pange tähele, et toote hind erineb nüüd varem kuvatust, kui see polnud veel dimensiooni kohta määratud.  
9. Klõpsake suvandit Kuva müügihinnad.
    * Lehel Hind (müük) kuvatakse kõik toote, k.a selle variantide puhul kehtivad kaubanduslepped.  
10. Sulgege leht.

## <a name="find-the-applicable-discount"></a>Kohalduva allahindluse leidmine
    * Veenduge, et väli Kliendi konto sisaldab kliendinumbrit US-001.    
1. Sisestage väljale Kaubakood tüüp T0012.
    * Veenduge, et välja Kogus väärtuseks oleks määratud 1.  
    * Järgmised toote T0012 kohta kuvatavad hinnakujunduse üksikasjad pärinevad ühest või mitmest kaubandusleppest. Ühiku hind on 1000 Kanada dollarit ja allahindlusprotsent 5.  
2. Määrake koguse väärtuseks 20.
    * Tellimuse koguse suurendamisel pakutakse kliendile rea allahindlust 5 protsendilt 7-le.  
    * Netosumma arvutatakse ühiku hinna, allahindluse ja lõpliku koguse alusel.  
3. Klõpsake suvandit Kuva rea allahindlus.
    * Tootel T0012 on kaks rea allahindluse lepet, mis määrab 5-protsendise allahindluse tellimuserea kogusele 1 kuni 10 ja 7-protsendise allahindluse tellimuse kogustele üle 10. Pange tähele, et allahindlused rakenduvad tootegrupile, siinses näiteks grupile koodiga 01, millesse toode T0012 kuulub.  
4. Sulgege leht.

