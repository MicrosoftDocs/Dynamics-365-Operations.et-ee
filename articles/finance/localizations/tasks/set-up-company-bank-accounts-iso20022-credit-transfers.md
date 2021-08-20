---
title: Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: See protseduur näitab, kuidas seadistada ettevõttekohase pangakonto teavet, mis on nõutav maksefaili loomiseks.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankAccountTable, OMLegalEntity, BankAccountTableLookUp
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a3b3b5ce9d7e24b2b7d3f76e4d770968df897b546df507ba9e3bde5aeac91715
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6780766"
---
# <a name="set-up-company-bank-accounts-for-iso20022-credit-transfers"></a>Ettevõtte pangakontode seadistamine ISO20022 kreeditkorralduste jaoks

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]