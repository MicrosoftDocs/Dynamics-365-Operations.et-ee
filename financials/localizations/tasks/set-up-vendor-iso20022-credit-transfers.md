--- 
title: Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks
description: "See protseduur näitab, kuidas seadistada hankija ja hankijakohase pangakonto teavet, mis on nõutav ISO20022 kreeditülekande või mis tahes muu hankija maksefaili loomiseks."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 147d8fa82bf15c984ad263cada42789038fa7371
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Hankijate ja hankija pangakontode seadistamine ISO20022 kreeditkorralduste jaoks

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


