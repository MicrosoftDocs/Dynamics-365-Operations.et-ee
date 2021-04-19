---
title: Laota kaupu saab välja registreerida
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendid saavad lisada ostukorvi laost väljas kaupu ja jätkata väljaregistreerimist.
author: Reza-Assadi
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
ms.openlocfilehash: af44def901d3aa7d4b24ab6abfac60d066a8d1a3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801743"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Laota kaupu saab välja registreerida

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui kliendid saavad lisada ostukorvi laost väljas kaupu ja jätkata väljaregistreerimist.

## <a name="description"></a>Kirjeldus

Kasutajad saavad lisada ostukorvi kauba, kuigi kaupluses puudub vaba kaubavaru, ja siis siirduge väljaregistreerimise lehele.

## <a name="resolution"></a>Eraldusvõime

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Commerce'i saidi koostajas laotõrgete näitamise lubamine

Commerce'i saidi koostajas **laotõrgete näitamise** lubamine, jälgi neid samme.

1. Valige sait, millel te töötate.
1. Valige vasakpoolsel navigeerimispaanil suvand **Lehed**.
1. Valige **CartPage** avamiseks.
1. Valige ostukorvi **1 pesa**, sealt valige käsk **redigeeri** ja siis valige atribuutide paanil märkeruut **Näita laotõrkeid**.
1. Salvestage ja avaldage leht.

## <a name="additional-resources"></a>Lisaressursid

[Varude sätete rakendamine](../inventory-settings.md)

[Varude saadavuse arvutamine jaemüügikanalite jaoks](../calculated-inventory-retail-channels.md)

[Varude puhvrite ja varude tasemete konfigureerimine](../inventory-buffers-levels.md)
