---
title: Maksetüübiks peab olema müügitellimuse lehel märgitud krediitkaarditõrge
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui müügitellimuse lehel kuvatakse tõrketeade pärast tellimuse sünkroonimist.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 71c5cbaf574866c74e222f4d67132004327db8fe
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285628"
---
# <a name="payment-type-must-be-credit-card-error-on-the-sales-order-page"></a>"Maksetüübiks peab olema müügitellimuse lehel märgitud krediitkaarditõrge

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui müügitellimuse lehel kuvatakse tõrketeade pärast tellimuse sünkroonimist.

## <a name="description"></a>Kirjeldus

Kui avate müügitellimuse lehe pärast tellimuse sünkroonimist, kuvatakse järgmine tõrketeade: "Maksetüüp peab olema krediitkaart, kuna krediitkaardi number on määratud."

![Makse tüüp peab olema krediitkaardi tõrge.](media/payment-type-must-be-credit-card.jpg)

## <a name="resolution"></a>Lahendus

### <a name="set-the-payment-type-in-commerce-headquarters"></a>Häälestage maksetüüp Commerce Headquarters`is

1. Avage **Müügireskontro \> Maksete seadistus \> Maksetingimused**.
1. Valige vasakul navigeerimisribal oma maksetingimused.
1. Veenduge, et **Maksetüüp** väljal on **Krediitkaart** valitud.

## <a name="additional-resources"></a>Lisaressursid

[Veebimüügi ja -maksete sisestamine](../tasks/posting-online-sales-payments.md)
