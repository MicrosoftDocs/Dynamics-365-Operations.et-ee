--- 
title: Tellimuste ooteloleku haldamine
description: "See protseduur näitab, kuidas seada kliendi müügitellimusi ootele, kuidas töötada ootel tellimuse väljaregistreerimisega ja kuidas tellimuse ootelolekut eemaldada."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 3edb8d2fe0fda6634bc2edb8e3bafc5a60344b7a
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="manage-order-holds"></a>Tellimuste ooteloleku haldamine

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seada kliendi müügitellimusi ootele, kuidas töötada ootel tellimuse väljaregistreerimisega ja kuidas tellimuse ootelolekut eemaldada. Tellimus võidakse ootele panna mitmel põhjusel. Näiteks võidakse tellimus ootele panna seni, kuni kliendi aadressi või makseviisi saab kinnitada või kuni haldur saab kliendi krediidilimiidi üle vaadata. Kui tellimus on ootel, ei saa ladu seda lähetamiseks töödelda. 

Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="set-up-order-holds"></a>Tellimuse ootelolekute häälestamine
1. Avage Müük ja turundus > Häälestamine > Müügitellimused > Tellimuse ooteloleku koodid.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Ooteloleku kood.
    * Näiteks tippige Helista tagasi.  
4. Sisestage väljale Kirjeldus soovitud väärtus.
    * Näiteks Kliendi tagasihelistuse ootel hoitav tellimus.  
    * Valikuliselt valige märkeruut Eemalda reserveeringud, et selle ooteloleku koodi lisamisel eemaldada tellimuselt mis tahes füüsilised reserveerimised.  
5. Klõpsake nuppu Salvesta.

## <a name="place-order-on-hold"></a>Tellimuse ootele seadmine
1. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
2. Klõpsake valikut Uus.
3. Valige või sisestage väärtus väljal Kliendi konto.
4. Klõpsake nuppu OK.
5. Sisestage või valige väärtus väljal Kaubakood.
6. Sisestage arv väljale Kogus.
7. Klõpsake toimingupaanil valikut Müügitellimus.
8. Klõpsake nuppu Ootelolevad tellimused.
9. Klõpsake valikut Uus.
10. Väljal Ooteloleku kood valige eelmises alamülesandes loodud kood.
11. Klõpsake nuppu Salvesta.
12. Sulgege leht.
13. Avage Müük ja turundus > Müügitellimused > Kõik müügitellimused.
14. Märkige loendis valitud rida.
    * Praegu ootelolevatel tellimustel on väljad „Ära töötle” ja „Pane ootele” märgitud.    
15. Klõpsake toimingupaanil valikut Komplekteerimine ja pakkimine.

## <a name="manage-order-holds"></a>Tellimuste ooteloleku haldamine
1. Avage Müük ja turundus > Müügitellimused > Avatud tellimused > Ootelolevad tellimused.
    * Ootelolevate tellimuste lehekülg funktsioneerib töölauana, kus saate hankida ülevaate kõigist praegustest ja töödeldud ootelolekutest ning käsitleda neid ja seotud müügitellimusi.      
2. Märkige loendis valitud rida.
3. Tegumiribal klõpsake nuppu Väljaregistreerimise ootelepanek.
4. Klõpsake nuppu Registreeri välja.
5. Eemaldage loendis valitud realt märge.
    * Väli Väljaregistreerimine näitab nüüd teie kasutaja ID-d.   
6. Klõpsake nuppu Tühjenda väljaregistreerimine.
7. Tegumiribal klõpsake nuppu Eemalda ootelolek.
    * Kui olete valmis ooteloleku eemaldama ja lubama tellimusel järgmisesse täitmise etappi liikuda, peate ooteloleku tühistama. Kui tellimus ei nõua muudatuste tegemist, saate käivitada toimingu Tühjenda ootelolekud. Siiski saate kasutada toimingut Eemalda ja muuda, kui pärast ooteloleku tühistamist tuleb tellimust värskendada.      
    * Toiming Eemalda ja saada on kohaldatav ainult siis, kui kasutate kõnekeskuse funktsiooni.  
8. Klõpsake nuppu Tühjenda ootelolekud.
    * Ootelolek on nüüd tellimusest ja aktiivsete ootelolekute loendist eemaldatud. Nägemaks kõiki ootelolekuid ja nende alamkogumit konkreetse oleku järgi, muutke välja Kuva väärtust.     


