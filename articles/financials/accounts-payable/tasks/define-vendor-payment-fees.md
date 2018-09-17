--- 
title: "Hankija maksetasude määratlemine"
description: Hankija maksetasude seadistus.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f62d07ffa1ee4a525f0f266922bc88e5ac8d5ada
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="define-vendor-payment-fees"></a>Hankija maksetasude määratlemine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hankija maksetasude seadistus. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Ostureskontro > Makse seadistus > Maksetasu.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tasu ID.
    * Tasu ID peaks kirjeldama, millal seda tasu kasutatakse, näiteks EFT_Tasu.  
4. Sisestage väärtus väljale Nimi.
5. Sisestage väärtus väljale Tasu kirjeldus.
    * Lisage kirjeldus lisateabe pakkumiseks selle kohta, millal tasu määratakse.  
6. Valige väljal Tasu kas suvand Hankija või Pearaamat.
    * Pearaamatut kasutatakse, kui tasu kantakse teie organisatsiooni kuludesse.  Hankijat kasutatakse, kui tasu määratakse hankijale.  
7. Sisestage põhikonto, mille kuludesse tasu läheb.
    * See suvand on kasutatav ainult juhul, kui suvandi Tasu puhul on valitud Pearaamat.  
8. Sisestage tööleht, millel seda tasu saab kasutada. 
    * Hankija maksetasu puhul valiksite töölehe Maksed hankijale.  
9. Klõpsake nuppu Salvesta.
10. Klõpsake suvandit Maksetasu seadistus.
    * Jätkake maksetasu seadistusega, et määratleda, millal tuleks tasu teie valitud töölehele vaikimisi lisada.  
11. Valige kas suvand Tabel, Grupp või Kõik.
    * Tabelit kasutatakse ühe pangakonto valimiseks, gruppi kasutatakse pangagrupi valimiseks ja suvandit Kõik selle tasu seadistuse kasutamiseks kõigi pangakontode puhul  
12. Valige kas pangagrupp või pangakonto.
    * Otsing näitab pangagruppi, kui valisite suvandi Grupp ja pangakontosid, kui valisite suvandi Tabel.  
13. Valige makseviis, mis selle tasu puhul määratakse.
14. Valige valitud makseviisi puhul suvand Makse täpsustus.
    * Suvandit Makse täpsustus kasutatakse elektroonilise ülekande makseviisidega.  
15. Valige, kas tasu on protsent, summa või intervall.
16. Sisestage tasu protsent või summa.
    * Kui tasuks on protsent, sisestage protsent. Kui tasuks on summa, sisestage tasu summa. Kui tasuks on intervall, kasutage mitmetasandiliste tasude määratlemiseks vahekaarti Intervall.  
17. Valige väljal Tasu valuuta see valuuta, milles tasu määratakse.
    * See on tasu valuutakood. Makse valuutat kasutatakse määratlemaks, millal tasu reeglit tuleks määrata makse valuuta põhjal. Näiteks võib teie pank nõuda tasu, kui makse on tehtud eurodes, kuid kõikidele muudele maksetele pole tasu määratud.  
18. Klõpsake nuppu Salvesta.


