---
title: Kaupade tagastamine mitme klienditellimuse ja -arve alusel
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teenuses Dynamics 365 Retail tagastada mitme klienditellimuse ja -arved alusel.
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
ms.openlocfilehash: 25a1081e5f903076e23089c41dda7437f8a70124
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2017985"
---
# <a name="return-items-across-multiple-customer-orders-and-invoices"></a>Kaupade tagastamine mitme klienditellimuse ja -arve alusel

[!include [banner](includes/banner.md)]


Tagastamisi saab teha mitme tellimuse ja arve alusel. 

## <a name="configure-retail-to-support-returns-across-multiple-customer-order-and-invoices"></a>Retaili konfigureerimine mitme klienditellimuse ja -arve alusel tagastuste toetamiseks

1. Valige **Retaili parameetrid \> Klienditellimused**.
1. Lülitage sisse parameeter **Luba mitme tellimuse tagastamine**. 

## <a name="process-returns"></a>Tagastuste töötlemine

Pärast seda, kui parameeter on sisse lülitatud ja muudatused on kauplustega sünkroonitud, võib kaupluse kassapidaja tagastamiseks valida mitu kliendi müügitellimust.

Tellimuste valimisel kuvatakse kõikide tellimuste arvete kõik tagastatavad tooted. Kassapidaja võib seejärel valida tagastatavad tooted. Valitud toodete kohta luuakse üks tagastustellimus.
