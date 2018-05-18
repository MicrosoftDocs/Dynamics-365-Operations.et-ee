--- 
title: "Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks"
description: "See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d0eabdfdeb5ed7d0bdb6df87ebdfa0d41e87492
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks. Saate seadistada teabe, mis on vajalik ISO 20022 kreeditülekande vormingu loomiseks, kuid olenevalt vormingust võib olla vaja muud teavet, nt ettevõtte ID-d või sortimiskoodi. 

Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.

See on teine viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="set-up-iban-and-swift-code"></a>IBAN- ja SWIFT-koodi seadistamine
1. Avage Sularaha- ja pangahaldus > Pangakontod.
2. Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega DEMF OPER.
3. Klõpsake pangakonto üksikasjade avamiseks valikut DEMF OPER.
4. Klõpsake nuppu Redigeeri.
5. Laiendage jaotist Täiendav identifitseerimine.
6. Sisestage väljale IBAN väärtus DE89370400440532013000.
7. Sisestage väljale SWIFT-kood väärtus DEUTDEFF.
    * Pange tähele, et SWIFT\BIC pole paljude maksevormingute puhul nõutav, kuid soovitatav on see pangakonto jaoks registreerida.  
8. Klõpsake nuppu Salvesta.

## <a name="set-up-bank-account-for-the-legal-entity"></a>Juriidilise isiku pangakonto seadistamine
1. Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.
2. Klõpsake nuppu Redigeeri.
3. Laiendage jaotist Pangakonto teave.
4. Sisestage väärtus väljale Pangakonto või valige see.
5. Klõpsake nuppu Salvesta.


