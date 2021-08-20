---
title: Tellimuste ooteloleku haldamine
description: See protseduur näitab, kuidas seada kliendi müügitellimusi ootele, kuidas töötada ootel tellimuse väljaregistreerimisega ja kuidas tellimuse ootelolekut eemaldada.
author: omulvad
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 38e5ea0dcec84704c9674412d12d0e857459975b3e928467a76e9fa677f6cbc1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771295"
---
# <a name="manage-order-holds"></a>Tellimuste ooteloleku haldamine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas seada kliendi müügitellimusi ootele, kuidas töötada ootel tellimuse väljaregistreerimisega ja kuidas tellimuse ootelolekut eemaldada. Tellimus võidakse ootele panna mitmel põhjusel. Näiteks võidakse tellimus ootele panna seni, kuni kliendi aadressi või makseviisi saab kinnitada või kuni haldur saab kliendi krediidilimiidi üle vaadata. Kui tellimus on ootel, ei saa ladu seda lähetamiseks töödelda. 

Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.


## <a name="set-up-order-holds"></a>Tellimuse ootelolekute häälestamine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Häälestamine > Müügitellimused > Tellimuse ooteloleku koodid**.
2. Klõpsake valikut **Uus**.
3. Tippige väärtus väljale **Ooteloleku kood**. Näiteks tippige „Helista tagasi”.  
4. Sisestage väärtus väljale **Kirjeldus**.
    - Näiteks Kliendi tagasihelistuse ootel hoitav tellimus.  
    - Valikuliselt valige märkeruut **Eemalda reserveeringud**, et selle ooteloleku koodi lisamisel eemaldada tellimuselt mis tahes füüsilised reserveerimised.  
5. Klõpsake valikut **Salvesta**.

## <a name="place-order-on-hold"></a>Tellimuse ootele seadmine
1. Avage **Navigeerimispaan > Moodulid > Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
2. Klõpsake valikut **Uus**.
3. Väljale **Kliendi konto** sisestage või valige väärtus.
4. Klõpsake valikut **OK**.
5. Sisestage või valige väärtus väljale **Kauba kood**.
6. Sisestage arv väljale **Kogus**.
7. Klõpsake **Tegevuspaanil** valikut **Müügitellimus**.
8. Klõpsake nuppu **Ootelolevad tellimused**.
9. Klõpsake valikut **Uus**.
10. Väljal **Ooteloleku kood** valige eelmises alamülesandes loodud kood.
11. Klõpsake valikut **Salvesta**.
12. Sulgege leht.
13. Avage **Müük ja turundus > Müügitellimused > Kõik müügitellimused**.
14. Märkige loendis valitud rida. Praegu ootelolevatel tellimustel on väljad „Ära töötle” ja „Pane ootele” märgitud.
15. Klõpsake tegevuspaanil valikut **Komplekteerimine ja pakkimine.**

## <a name="manage-order-holds"></a>Tellimuste ooteloleku haldamine
1. Avage **Müük ja turundus > Müügitellimused > Avatud tellimused > Ootelolevad tellimused**. **Ootelolevate tellimuste** lehekülg funktsioneerib töölauana, kus saate hankida ülevaate kõigist praegustest ja töödeldud ootelolekutest ning käsitleda neid ja seotud müügitellimusi.     
2. Märkige loendis valitud rida.
3. **Tegumiribal** klõpsake nuppu **Väljaregistreerimise ootelepanek**.
4. Klõpsake nuppu **Registreeri välja**.
5. Eemaldage loendis valitud realt märge. Väli **Väljaregistreerimine** näitab nüüd teie kasutaja ID-d.   
6. Klõpsake nuppu **Tühjenda väljaregistreerimine**.
7. **Tegumiribal** klõpsake nuppu **Eemalda ootelolek**.
    - Kui olete valmis ooteloleku eemaldama ja lubama tellimusel järgmisesse täitmise etappi liikuda, peate ooteloleku tühistama. Kui tellimus ei nõua muudatuste tegemist, saate käivitada toimingu Tühjenda ootelolekud. Siiski saate kasutada toimingut Eemalda ja muuda, kui pärast ooteloleku tühistamist tuleb tellimust värskendada.      
    - Toiming **Eemalda ja saada** on kohaldatav ainult siis, kui kasutate kõnekeskuse funktsiooni.  
8. Klõpsake nuppu **Tühjenda ootelolekud**. Ootelolek on nüüd tellimusest ja aktiivsete ootelolekute loendist eemaldatud. Nägemaks kõiki ootelolekuid ja nende alamkogumit konkreetse oleku järgi, muutke välja Kuva väärtust.     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]