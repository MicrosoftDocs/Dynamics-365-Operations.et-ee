---
title: Finance and Operationsi ning Common Data Service’i esialgse sünkroonimise täitmise järjekord
description: Selles peatükis kirjeldatakse sünkroonimise järjekorda, mida peate järgima esialgsete andmete loomisel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873124"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Finance and Operationsi ning Common Data Service’i esialgse sünkroonimise täitmise järjekord

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Enne andmete integratsiooni peate looma klientide, tarnijate ja kontaktide puhul kohustuslikud esialgsed andmed. Näiteks tahate luua uut üksust **Tarnija rühm** ja määrata selle **Maksetingimused** väärtuseks **Net30**. Sel juhul peate enne **Tarnija rühma** üksuse loomise üritust veenduma, et **Net30** on olemas nii Microsoft Dynamics 365 for Finance and Operationsis kui ka Common Data Service’is. (Tulevikus väljastab Microsoft topeltkirjutamise platvormi „Algne sünkroonimine“. See funktsioon sünkroniseerib Finance and Operationsi ning Common Data Service’i andmeid omavahel ühe korra topeltkirjutamise seadistuse osana.)

> [!TIP]
> Microsoft väljastab topeltkirjutamise kaardi kõikidele viiteandmetele, sealhulgas **maksetingimustele** (maksetingimused). Kui teil on juba esialgsed andmed ühes süsteemis, võib väike värskenduse toiming kirjel käivitada selle kirje topeltkirjutamise.

Peate järgima järgmist tähtsuse järjekorda ja veenduge, et esialgsed andmed oleksid saadaval nii Finance and Operationsis kui ka Common Data Service’is.

## <a name="vendor"></a>Tarnija

Siin on üksuse **Tarnija** käivitusjärjekord:

1. Tarnijagrupp

    1. Maksetingimused

        1. Maksepäev ja selle read
        2. Maksegraafik

2. Tarnija makseviis

## <a name="customer-organization"></a>Kliendi organisatsioon

Siin on üksuse **Klient** käivitusjärjekord:

1. Kliendigrupp

    1. Maksetingimused

        1. Maksepäev ja selle read
        2. Makse 

2. Kliendi makseviis

## <a name="contact-person"></a>Kontaktisik

Siin on üksuse **Kontakt** käivitusjärjekord:

1. Klient
2. Tarnija
