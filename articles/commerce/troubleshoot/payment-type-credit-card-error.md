---
title: Maksetüübiks peab olema müügitellimuse lehel märgitud krediitkaarditõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui müügitellimuse lehel näidatakse tõrketeadet, pärast tellimuse sünkroonimist.
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
ms.openlocfilehash: 20f18507dee330fd1affedeee092b3dfa7cc10bc
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585286"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>"Maksetüübiks peab olema müügitellimuse lehel märgitud krediitkaarditõrge

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui müügitellimuse lehel näidatakse tõrketeadet, pärast tellimuse sünkroonimist.

## <a name="description"></a>Kirjeldus

Kui avate müügitellimuse lehe pärast tellimuse sünkroonimist, kuvatakse järgmine tõrketeade: "Maksetüüp peab olema krediitkaart, kuna krediitkaardi number on määratud."

![Makse tüüp peab olema krediitkaardi tõrge](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Eraldusvõime

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Häälestage maksetüüp Commerce Headquarters`is

1. Avage **Müügireskontro \> Maksete seadistus \> Maksetingimused**.
1. Valige vasakul navigeerimisribal oma maksetingimused.
1. Veenduge, et **Maksetüüp** väljal on **Krediitkaart** valitud.

## <a name="additional-resources"></a>Lisaressursid

[Veebimüügi ja -maksete sisestamine](../tasks/posting-online-sales-payments.md)
