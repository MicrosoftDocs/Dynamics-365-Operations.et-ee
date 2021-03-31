---
title: Kliendi makseviisi määramine
description: Selles teemas kirjeldatakse, kuidas luua kliendi makseviisi.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7e60459c417c6018c4088009a323cf7f66616ef4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220199"
---
# <a name="establish-customer-method-of-payment"></a>Kliendi makseviisi määramine

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas luua kliendi makseviisi. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Navigeerimispaanil avage **Moodulid > Müügireskontro > Maksete seadistamine > Makseviisid**.
2. Valige suvand **Uus**.
3. Väljas **Makseviis** sisestage selle ID. Makseviisi ID kuvatakse arvetel ja maksetel, nii et muutke see piisavalt kirjeldavaks, et saada aru, millist tüüpi makse ja millise pangakonto puhul registreeritakse.  
4. Väljale **Kirjeldus** sisestage kirjeldus.
5. Valige, milline makse olek on maksete sisestamiseks vajalik. Kliendimakse loomisel saab seda sisestada ainult siis, kui makse olek ühtib makse olekuga, mille siin määratlete.  
6. Valige, kuidas klientide makseid arvete puhul luua. Seda suvandit kasutatakse ainult maksesoovituse käitamisel. Maksesoovitust saab kasutada kliendimaksete puhul otsekorralduste tegemisel ja vahendite eraldamisel kliendi pangakontodelt.  
7. Valige makse tüüp. Makse tüüp aitab tuvastada, kas maksel toimub kinnitamine või mitte.  
8. Valige, millisele konto tüübile maksed sisestatakse. Tavaliselt oleks selle suvandi puhul valitud väärtus Pank.  
9. Valige pangakonto, kuhu makse kirjendatakse.
10. Sisestage pangakande tüüp, et tuvastada teie panga kasutatav makse tüüp. Pangakande tüüpi kasutatakse panga vastavusse viimise protsessi käigus ja see võib vastavusse viimist lihtsustada.  
11. Valige, kas see makse sisestatakse ajutiselt vahekontole. Kui soovite proovida panga tühistamiseks makse puhul ujuvaega, kasutage funktsiooni Vahekonto. Makse sisestatakse ajutiselt pearaamatukontole, kuni see panga tühistab, mil makse liigub pangakontole, mille siin määratlesite.  
12. Valige vahekontole sisestamiseks kasutatav põhikonto. See on põhikonto, millele makse vahekonto kasutamisel ajutiselt sisestatakse.  
13. Elektrooniliste maksete seade määratlemiseks kasutage vahekaarti **Failivorming**
14. Kohustuslike väljade määratlemiseks kasutage vahekaarti **Makseviis**. Näiteks kui vajate kõikide selle makseviisiga maksete deponeerimist, saate selle suvandi sellel vahekaardil valida.  
15. Kasutage vahekaarti **Makse atribuudid**, määratlemaks, milliseid makse atribuute soovite selle makseviisi puhul kasutada.
16. Valige käsk **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]