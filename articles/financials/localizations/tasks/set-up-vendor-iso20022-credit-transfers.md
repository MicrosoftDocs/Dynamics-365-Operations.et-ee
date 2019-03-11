---
title: Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: See protseduur näitab, kuidas seadistada hankija ja hankijakohase pangakonto teavet, mis on nõutav ISO20022 kreeditülekande või mis tahes muu hankija maksefaili loomiseks.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 13b3c37f5d013dd896a456018813f20e5e70350b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "311607"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada hankija ja hankijakohase pangakonto teavet, mis on nõutav ISO20022 kreeditülekande või mis tahes muu hankija maksefaili loomiseks. 

Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.
See on neljas viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="set-up-bank-details"></a>Panga üksikasjade seadistamine
1. Minge jaotisse Ostureskontrod > Hankijad > Kõik hankijad.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Hankija konto väärtuse DE-001 järgi.
3. Hankija üksikasjade avamiseks klõpsake DE-001.
4. Klõpsake toimingupaanil suvandit Hankija.
5. Klõpsake valikut Pangakontod.
6. Klõpsake nuppu Redigeeri.
    * Kui ühtegi pangakontot pole saadaval, peate looma uue.  
7. Sisestage väljale SWIFT-kood väärtus COBADEFFXXX.
8. Sisestage väljale IBAN väärtus DE36200400000628808808.
9. Sulgege leht.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Hankija makseviisi seadistamine
1. Klõpsake nuppu Redigeeri.
2. Laiendage või ahendage jaotist Makse.
3. Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.
4. Klõpsake loendis valitud real SEPA CT olevat linki.
5. Klõpsake nuppu Salvesta.

