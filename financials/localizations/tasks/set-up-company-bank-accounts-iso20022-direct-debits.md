--- 
title: "Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks"
description: "See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks."
author: mrolecki
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 741d8ddca24e5fe083b4ddf775bb7f2d65a56fee
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks

[!include[task guide banner](../../includes/task-guide-banner.md)]

See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks. Protseduur kasutab näitena ISO-20022 otsekorralduse vormingut. Muud vormingud võivad nõuda täiendavat seadistusteavet nagu Ettevõtte ID või Sortimiskood.



Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.



See on teine viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.


## <a name="set-up-the-iban-and-swift-codes"></a>IBAN- ja SWIFT-koodide seadistamine
1. Avage Sularaha- ja pangahaldus > Pangakontod.
2. Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.
3. Klõpsake loendis valitud real olevat linki.
    * Näiteks klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.  
4. Klõpsake nuppu Redigeeri.
5. Laiendage või ahendage jaotist Täiendav identifitseerimine.
6. Sisestage väärtus väljale IBAN.
    * Näiteks sisestage DE89370400440532013000.  
7. Sisestage väärtus väljale SWIFT-kood.
    * Näiteks sisestage DEUTDEFF.    Pange tähele, et SWIFT \ BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.  
8. Klõpsake nuppu Salvesta.

## <a name="set-up-a-bank-account-for-the-legal-entity"></a>Juriidilise isiku pangakonto seadistamine
1. Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.
2. Klõpsake nuppu Redigeeri.
3. Laiendage või ahendage jaotist Pangakonto teave.
4. Klõpsake väljal Pangakonto otsingu avamiseks ripploendi nuppu.
5. Klõpsake loendis valitud real olevat linki.
    * Näiteks valige pangakonto DEMF OPER.  
6. Klõpsake nuppu Salvesta.


