---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Microsoft Dynamics 365 for Retail tagastada mitme klienditellimuse ja -arved alusel.
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
ms.openlocfilehash: c201311028b11121d626e93859a2b98497c047d1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565296"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Kaupade tagastamine mitme klienditellimuse ja -arve alusel

[!include [banner](includes/banner.md)]


Teenuse Dynamics 365 for Finance and Operations versioonis 10.0 saab tagastusi teha mitme tellimuse ja arve alusel, ent varasemates versioonides sai tagastusi töödelda korraga ühe arve alusel. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Retaili konfigureerimine mitme klienditellimuse ja -arve alusel tagastuste toetamiseks

1. Valige **Jaemüügi parameetrid \> Klienditellimused**.
1. Lülitage sisse parameeter **Luba mitme tellimuse tagastamine**. 

## <a name="process-returns"></a>Tagastuste töötlemine

Pärast seda, kui parameeter on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.

Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted. Kassapidaja võib seejärel valida tagastatavad tooted. Valitud toodete kohta luuakse üks tagastustellimus.
