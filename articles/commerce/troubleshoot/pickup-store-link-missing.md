---
title: Järeleminemise valikut ei kuvata ostukorvi või toote üksikasjade lehtedel
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluses oleva kauba saatmisvalikut ei kuvata ostukorvi leheküljel või toote üksikasjade lehtedel.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c78dee7289931cecd0f2d7c09caf7881eb8cfd23
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585282"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>"Järeleminemise" valikut ei kuvata ostukorvi või toote üksikasjade lehtedel

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui kaupluses oleva kauba saatmisvalikut ei kuvata ostukorvi leheküljel või toote üksikasjade lehtedel.

## <a name="description"></a>Kirjeldus

**Järeleminemise** nuppu ei kuvata ostukorvi või toote üksikasjade lehtedel.

Järgmine illustratsioon näitab näidet lehekülje kohta, mis sisaldab **Järeleminemise** nuppu.

![Järeleminemise nupp](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Eraldusvõime

### <a name="enable-the-bopis-extension-in-commerce-site-builder"></a>BOPIS-i laiendi lubamine Commerce'i saidi koostajas

Commerce'i saidi koostajas "võrgus ostmise" lubamiseks, järgige neid samme.

1. Valige sait.
1. Valige **Saidi sätted** ja seejärel valige suvand **Laiendused**.
1. Veenduge, et **Keela BOPIS** valik on tühi.

### <a name="configure-modes-of-delivery-in-commerce-headquarters"></a>Tarneviiside konfigureerimine Commerce Headquarters`is

Commerce headquarters`is kannete redigeerimiseks toimige järgmiselt.

1. Minge jaotisse **Ostmine ja hankimine \> Seadistamine \> Tarneviis**.
1. Veenduge, et **kliendi järeletulek** tarneviisina on loodud ja tooted ja aadressid on määratud.
1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi seadistamine \> Parameetrid**.
1. Valige vasakpoolsel navigeerimispaanil suvand **Kliendi tellimused**.
1. Veenduge, et **Järeleminemise tarneviis** on õigesti konfigureeritud.

### <a name="configure-customer-orders-payments"></a>Klienditellimuste maksete konfigureerimine

Commerce headquarters`is kannete redigeerimiseks toimige järgmiste sammudega.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi seadistamine \> Parameetrid**.
1. Valige vasakpoolsel navigeerimispaanil suvand **Kliendi tellimused**.
1. Veenduge, et **Maksed** kiirkaardil on **Maksetingimused** ja **Makseviisi** väljad on õigesti seatud.

## <a name="additional-resources"></a>Lisaressursid

[BOPIS-i konfigureerimine](../cpe-bopis.md)

[Klienditellimuste korral mitme järeletulemisega tarneviisi lubamine](../multiple-pickup-modes.md)

[Omnikanali Commerce'i tellimuste maksed](../dev-itpro/commerce-payments.md)

[Kaupluse valimise moodul](../store-selector.md)
