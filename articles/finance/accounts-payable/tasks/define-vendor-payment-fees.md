---
title: Hankija maksetasude määratlemine
description: Hankija maksetasude seadistus.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109816"
---
# <a name="define-vendor-payment-fees"></a>Hankija maksetasude määratlemine

[!include [banner](../../includes/banner.md)]

Hankija maksetasude seadistus. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Minge > **makse > seadistusse**.
2. Klõpsake valikut **Uus**.
3. **Tippige väärtus väljale Tasu ID**.
    * Tasu **ID peaks** kirjeldama, millal seda tasu kasutatakse, nt "EFT_Fee".  
4. Sisestage väärtus väljale **Nimi**.
5. **Tippige väärtus** väljale Tasu kirjeldus.
    * Lisage kirjeldus lisateabe pakkumiseks selle kohta, millal tasu määratakse.  
6. Väljal Tasu **valige hankija või** **pearaamat** **.**
    * **Pearaamatut** kasutatakse siis, kui tasu läheb teie organisatsiooni kuludesse. **Hankijat** kasutatakse siis, kui tasu hinnatakse hankijale.  
7. Sisestage põhikonto, mille kuludesse tasu läheb.
    * See valik on saadaval ainult siis, kui **valite** suvandi **Maks valiku Pearaamat**.  
8. Sisestage tööleht, millel seda tasu saab kasutada. 
    * Hankija maksetasu puhul valiksite töölehe Maksed hankijale.  
9. Klõpsake käsku **Salvesta**.
10. Klõpsake **Makse maksu seadistamine**.
    * Jätkake maksetasu **seadistusega,** et määratleda, millal tasu peaks vaikimisi olema valitud töölehel.  
11. Valige **tabel**, grupp **või** **kõik**.
    * **Tabelit** kasutatakse üksiku pangakonto valimiseks. **Gruppi** kasutatakse pangagrupi valimiseks ja kõik **on selleks,** et kasutada seda tasuseadistust kõigi pangakontode puhul.  
12. Valige kas pangagrupp või pangakonto.
    * Otsing näitab pangagruppi, kui valisite Grupi **ja kui valisite Tabeli, kuvatakse pangakontod** **.**  
13. Valige makseviis, mis selle tasu puhul määratakse.
14. Saate valida **valitud** makseviisi makse täpsustuse.
    * Makse **spetsifikatsiooni** kasutatakse elektrooniliste fondi ülekande makseviiside puhul.  
15. Valige, kas tasu on protsent, summa või intervall.
16. Sisestage tasu protsent või summa.
    * Kui tasu **on** protsent, sisestage protsent. **Kui tasu** on summa, sisestage tasu summa. Kui tasu **on** intervall, kasutage mitmetasandiliste **tasude** määratlemiseks vahekaarti Intervall.  
17. **Väljal Tasu** valuuta valige valuuta, milles tasu hinnatakse.
    * See on tasu valuutakood. Makse valuutat kasutatakse määratlemaks, millal tasu reeglit tuleks määrata makse valuuta põhjal. Näiteks võib teie pank nõuda tasu, kui makse on tehtud eurodes, kuid kõikidele muudele maksetele pole tasu määratud.  
18. Klõpsake nuppu **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
