---
title: Finance and Operationsi rakenduste ja teenuse Common Data Service esialgse sünkroonimise täitmise järjekord
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
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019740"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Finance and Operationsi rakenduste ja teenuse Common Data Service esialgse sünkroonimise täitmise järjekord

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Enne andmete integratsiooni peate looma klientide, tarnijate ja kontaktide puhul kohustuslikud esialgsed andmed. Näiteks tahate luua uut üksust **Tarnija rühm** ja määrata selle **Maksetingimused** väärtuseks **Net30**. Sel juhul peate enne **Tarnija rühma** üksuse loomise üritust veenduma, et **Net30** on olemas nii rakenduses kui ka Common Data Service’is. (Tulevikus väljastab Microsoft topeltkirjutamise platvormi „Algne sünkroonimine“. See funktsioon sünkroniseerib rakenduse ning Common Data Service’i andmeid omavahel ühe korra topeltkirjutamise seadistuse osana.)

> [!TIP]
> Microsoft väljastab topeltkirjutamise kaardi kõikidele viiteandmetele, sealhulgas **maksetingimustele** (maksetingimused). Kui teil on juba esialgsed andmed ühes süsteemis, võib väike värskenduse toiming kirjel käivitada selle kirje topeltkirjutamise.

Peate järgima järgmist tähtsuse järjekorda ja veenduge, et esialgsed andmed oleksid saadaval nii rakenduses kui ka Common Data Service’is.

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
