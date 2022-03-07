---
title: Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: See protseduur näitab, kuidas seadistada hankija ja hankijakohase pangakonto teavet, mis on nõutav ISO20022 kreeditülekande või mis tahes muu hankija maksefaili loomiseks.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, VendBankAccounts
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f7a901591f9f3d1a892c29f92e59dc96c1f172143cae6bec571da33b4a50d274
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6723715"
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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]