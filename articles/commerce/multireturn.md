---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Commerce tagastusi mitme klienditellimuse ja -arve alusel.
author: josaw1
manager: AnnBe
ms.date: 08/27/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: e95f06ffaaf2d250b02a8458faa2d9e0b5ef5631
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760246"
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

