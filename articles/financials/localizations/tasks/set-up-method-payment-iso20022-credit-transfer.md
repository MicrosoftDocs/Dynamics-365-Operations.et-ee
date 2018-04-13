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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bed51f8749dfa0264ad39f51f9ceb295ac46fe93
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

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


