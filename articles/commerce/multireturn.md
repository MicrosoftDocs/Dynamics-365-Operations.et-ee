---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Commerce tagastusi mitme klienditellimuse ja -arve alusel.
author: josaw1
manager: AnnBe
ms.date: 03/05/2019
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
ms.openlocfilehash: c5f17424f0837344030f9ce2d2d037cde08c4e49
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004454"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Kaupade tagastamine mitme klienditellimuse ja -arve alusel

[!include [banner](includes/banner.md)]


Tagastamisi saab teha mitme tellimuse ja arve alusel. 

## <a name="configure-commerce-to-support-returns-across-multiple-customer-order-and-invoices"></a>Kaubanduse konfigureerimine mitme klienditellimuse ja -arve alusel tagastuste toetamiseks

1. Valige **Kaubanduse parameetrid \> Klienditellimused**.
1. Lülitage sisse parameeter **Luba mitme tellimuse tagastamine**. 

## <a name="process-returns"></a>Tagastuste töötlemine

Pärast seda, kui parameeter on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.

Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted. Kassapidaja võib seejärel valida tagastatavad tooted. Valitud toodete kohta luuakse üks tagastustellimus.
