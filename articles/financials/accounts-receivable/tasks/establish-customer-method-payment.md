--- 
title: "Kliendi makseviisi määramine"
description: Looge kliendimaksete makseviis.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ef3cad6538d9efbd1c1881f4b7d771382d9b1ba8
ms.openlocfilehash: 0ba359567126efaa8274644444a8a261e24c6621
ms.contentlocale: et-ee
ms.lasthandoff: 10/26/2017

---
# <a name="establish-customer-method-of-payment"></a>Kliendi makseviisi määramine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Looge kliendimaksete makseviis. See ülesanne kasutab demoettevõtte USMF andmeid.

1. Avage Müügireskontro > Maksete seadistus > Makseviisid.
2. Klõpsake valikut Uus.
3. Sisestage makseviisi ID väljale Makseviis.
    * Makseviisi ID kuvatakse arvetel ja maksetel, nii et muutke see piisavalt kirjeldavaks, et saada aru, millist tüüpi makse ja millise pangakonto puhul registreeritakse.  
4. Sisestage kirjeldus väljale Kirjeldus.
5. Valige, milline makse olek on maksete sisestamiseks vajalik.
    * Kliendimakse loomisel saab seda sisestada ainult siis, kui makse olek ühtib makse olekuga, mille siin määratlete.  
6. Valige, kuidas klientide makseid arvete puhul luua.
    * Seda suvandit kasutatakse ainult maksesoovituse käitamisel. Maksesoovitust saab kasutada kliendimaksete puhul otsekorralduste tegemisel ja vahendite eraldamisel kliendi pangakontodelt.  
7. Valige makse tüüp.
    * Makse tüüp aitab tuvastada, kas maksel toimub kinnitamine või mitte.  
8. Valige, millisele konto tüübile maksed sisestatakse.
    * Tavaliselt oleks selle suvandi puhul valitud väärtus Pank.  
9. Valige pangakonto, kuhu makse kirjendatakse.
10. Sisestage pangakande tüüp, et tuvastada teie panga kasutatav makse tüüp.
    * Pangakande tüüpi kasutatakse panga vastavusse viimise protsessi käigus ja see võib vastavusse viimist lihtsustada.  
11. Valige, kas see makse sisestatakse ajutiselt vahekontole.
    * Kui soovite proovida panga tühistamiseks makse puhul ujuvaega, kasutage funktsiooni Vahekonto. Makse sisestatakse ajutiselt pearaamatukontole, kuni see panga tühistab, mil makse liigub pangakontole, mille siin määratlesite.  
12. Valige vahekontole sisestamiseks kasutatav põhikonto.
    * See on põhikonto, millele makse vahekonto kasutamisel ajutiselt sisestatakse.  
13. Vahekaardi Failivorming abil saate määratleda sätte elektrooniliste maksete puhul.
14. Kasutage kohustuslike väljade määratlemiseks vahekaarti Makse kontroll.
    * Näiteks kui vajate kõikide selle makseviisiga maksete deponeerimist, saate selle suvandi sellel vahekaardil valida.  
15. Kasutage vahekaarti Makse atribuudid, määratlemaks, milliseid makse atribuute soovite selle makseviisi puhul kasutada.
16. Klõpsake nuppu Salvesta.


