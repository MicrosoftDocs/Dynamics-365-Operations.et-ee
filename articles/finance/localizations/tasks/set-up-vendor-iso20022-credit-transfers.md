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
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4809a352f87cc3d88429461a06dfe36189ed5f31
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138965"
---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks

[!include [banner](../../includes/banner.md)]

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

