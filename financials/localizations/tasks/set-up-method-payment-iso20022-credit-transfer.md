--- 
title: Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks
description: "See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust."
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
ms.openlocfilehash: cc30912d15549c9519133c6ea12ee4d8edea7214
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks

[!include[task guide banner](../../includes/task-guide-banner.md)]

See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust. 

Enne selle ülesande lõpetamist tuleb eksportida vormingu konfiguratsioonid ja seadistada maksekontod.

Selle ülesande loomisel kasutati demoettevõtte DEMF andmeid.

See on kolmas viiest protseduurist, mis illustreerib hankija makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone. See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

1. Avage Ostureskontro > Makse seadistus > Makseviisid.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Makseviis väärtuse SEPA CT järgi.
3. Klõpsake nuppu Redigeeri.
4. Valige väljal Periood suvand Kokku.
5. Valige väljalt Makse tüüp suvand Elektrooniline makse.
6. Laiendage jaotist Failivormingud.
7. Valige väljal Üldine elektrooniline aruandlus suvand Jah.
8. Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.
    * Valige loendist väärtus ISO20022 kreeditiülekanne (DE). Kui loend on tühi, siis pole imporditud ja aktiivset hankija makse ekspordivormingu konfiguratsiooni.  
9. Valige väljalt Konto tüüp suvand Pank.
10. Täpsustage väljal Maksekonto väärtusi DEMF OPER.
11. Klõpsake nuppu Salvesta.


