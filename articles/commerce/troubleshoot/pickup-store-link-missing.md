---
title: Järeleminemise valikut ei kuvata ostukorvi või toote üksikasjade lehtedel
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui kaupluses oleva kauba pickupsuvand ei ilmu ostukorvi lehele või toote üksikasjade lehtedele.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
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
ms.openlocfilehash: 88367e13b4d079edb0816e301901828b65c437ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900304"
---
# <a name="pick-this-up-option-doesnt-appear-on-cart-or-product-details-pages"></a>"Järeleminemise" valikut ei kuvata ostukorvi või toote üksikasjade lehtedel

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui kaupluses oleva kauba pickupsuvand ei ilmu ostukorvi lehele või toote üksikasjade lehtedele.

## <a name="description"></a>Kirjeldus

**Järeleminemise** nuppu ei kuvata ostukorvi või toote üksikasjade lehtedel.

Järgmine illustratsioon näitab näidet lehekülje kohta, mis sisaldab **Järeleminemise** nuppu.

![Järeleminemise nupp.](media/pickup-button-missing.jpg)

## <a name="resolution"></a>Lahendus

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
