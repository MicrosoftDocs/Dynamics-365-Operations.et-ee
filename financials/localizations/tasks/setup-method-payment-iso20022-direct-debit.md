--- 
title: Makseviisi seadistamine ISO20022 otsekorralduse jaoks
description: "See protseduur näitab, kuidas seadistada ISO20022 otsekorralduse või mis tahes muu maksetüübi puhul kliendi makseviisi, kasutades faili loomiseks elektroonilist aruandlust."
author: mrolecki
manager: AnnBe
ms.date: 10/13/2016
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 16ff0cc28b272add80b08ae43b9fe5b8e7370b70
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-method-of-payment-for-iso20022-direct-debit"></a>Makseviisi seadistamine ISO20022 otsekorralduse jaoks

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


