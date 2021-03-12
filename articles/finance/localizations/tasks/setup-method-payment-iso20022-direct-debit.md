---
title: Makseviisi seadistamine ISO20022 otsekorralduse puhul
description: See protseduur näitab, kuidas seadistada ISO20022 otsekorralduse või mis tahes muu maksetüübi puhul kliendi makseviisi, kasutades faili loomiseks elektroonilist aruandlust.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPaymMode
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2cd5c174b0f3e3e15678513cecade020705beda
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982125"
---
# <a name="setup-method-of-payment-for-iso20022-direct-debit"></a>Makseviisi seadistamine ISO20022 otsekorralduse puhul

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas seadistada ISO20022 otsekorralduse või mis tahes muu maksetüübi puhul kliendi makseviisi, kasutades faili loomiseks elektroonilist aruandlust. 



Enne selle ülesande lõpetamist tuleb seadistada ekspordivormingu konfiguratsioonid ja maksekontod.



Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.



See on kolmas viiest protseduurist, mis näitab kliendi makseprotsessi, kasutades elektroonilise aruandluse konfiguratsioone.

1. Avage Müügireskontro > Maksete seadistus > Makseviisid.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Makseviis väärtuse ELECTRONIC järgi.
3. Klõpsake nuppu Redigeeri.
4. Täpsustage väljal Maksekonto väärtusi DEMF OPER.
5. Laiendage jaotist Failivormingud.
6. Valige väljal Üldine elektrooniline aruandlus suvand Jah.
7. Sisestage väärtus väljale Ekspordivormingu konfiguratsioon või valige see.
    * Valige loendist ISO20022 otsekorraldus (DE).  Kui loend on tühi, siis pole imporditud ja aktiivset kliendi makse ekspordivormingu konfiguratsiooni.  
8. Valige väljal Nõua luba suvand Jah.
    * Valige parameeter Nõua luba kliendi maksevormingutele, mis nõuavad loa teabe lisamist makseteatele (nt SEPA otsekorraldus).  
9. Klõpsake nuppu Salvesta.

