---
title: Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks
description: See ülesanne annab ülevaate ettevõttekohase pangakonto teabe seadistamise kohta, mis on nõutav kliendi maksefailide loomiseks.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 652d8aa8f78d9a12ee390d23904f2c94d9bcf684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442287"
---
# <a name="set-up-company-bank-accounts-for-iso20022-direct-debits"></a>Ettevõtte pangakontode seadistamine ISO20022 otsekorralduste jaoks

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]