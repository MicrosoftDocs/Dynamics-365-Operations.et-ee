---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Commerce tagastusi mitme klienditellimuse ja -arve alusel.
author: josaw1
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 4a64794a0e04516441fab628d441640e4d154b8d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796885"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Kaupade tagastamine mitme klienditellimuse ja -arve alusel

[!include [banner](includes/banner.md)]


Selles artiklis kirjeldatakse kaht funktsiooni, millega optimeeritakse klienditellimuse tagastusi mitme arve korral. 

## <a name="enable-refunds-over-multiple-captures"></a>Tagasimaksete lubamine mitme hõive korral

See funktsioon võimaldab mitut lingitud tagasimakset sama klienditellimuse alusel. 

1. Avage tööruum **Funktsioonihaldus** ja otsige märksõna **Tagasimaksete lubamine mitme hõive korral**.
2. Valige **Tagasimaksete lubamine mitme tellimuse korral** ja seejärel klõpsake nuppu **Luba**. 

## <a name="enable-proper-tax-calculation-for-returns-with-partial-quantity"></a>Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus

Funktsioon tagab selle, et kui tellimus tagastatakse mitme arvega, võrduvad maksud lõpuks algselt tasutud maksusummaga. 

1. Avage tööruum **Funktsioonihaldus** ja otsige märksõna **Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus**.
2. Valige **Luba osalise kogusega tagastuste korral nõuetekohane maksuarvutus** ja klõpsake seejärel nuppu **Luba**. 


## <a name="process-returns"></a>Tagastuste töötlemine

Pärast seda, kui need funktsioonid on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.

Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted. Kassapidaja võib seejärel valida tagastatavad tooted. Valitud toodete kohta luuakse üks tagastustellimus.

Kui tellimus on täielikult tagastatud, võrdub kliendile tagastatav maksude summa algselt tasutud maksusummaga.



[!INCLUDE[footer-include](../includes/footer-banner.md)]