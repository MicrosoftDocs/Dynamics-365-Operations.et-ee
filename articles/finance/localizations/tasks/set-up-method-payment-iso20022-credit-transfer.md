---
title: Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks
description: See protseduur näitab, kuidas seadistada ISO20022 kreeditülekande või mis tahes muu maksetüübi puhul hankija makseviisi, kasutades faili loomiseks elektroonilist aruandlust.
author: mrolecki
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 643be31db625d0db12f1df18b9e797013da98ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832468"
---
# <a name="set-up-method-of-payment-for-iso20022-credit-transfer"></a>Makseviisi seadistamine ISO20022 kreeditkorralduse jaoks

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]