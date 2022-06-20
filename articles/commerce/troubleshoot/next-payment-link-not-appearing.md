---
title: Salvestamine järgmise makse suvandi jaoks ei ilmu
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui märkeruut Salvesta minu järgmisele maksele ei ilmu maksemeetodi all e-äri saidi väljaregistreerimise lehel.
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
ms.openlocfilehash: efa04c87f78c376fd00da1b26aedb9e8b428dfa5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871551"
---
# <a name="save-for-my-next-payment-option-doesnt-appear"></a>"Salvestamine järgmise makse suvandi jaoks ei ilmu

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu **juhised** **·**, mis aitavad, kui märkeruut Salvesta minu järgmisele maksele ei ilmu maksemeetodi all e-äri saidi väljaregistreerimise lehel.

## <a name="description"></a>Kirjeldus

Märkeruut **Salvesta minu järgmise makse** jaoks ei ilmu maksemeetodi jaotises **Makseviis** e-kaubanduse saidi väljaregistreerimise lehel.

Järgmine näide näitab väljaregistreerimise lehe näidet, mis sisaldab märkeruutu **Salvesta minu järgmise makse** jaoks.

![Salvesta minu järgmise makse märkeruudu jaoks maksemoodulis.](media/payment-module-save-payment.jpg)

## <a name="resolution"></a>Lahendus

### <a name="verify-that-the-dynamics-365-payment-connector-for-adyen-is-correctly-configured-in-commerce-headquarters"></a>Veenduge, et Dynamics 365 Payment Connector Puhvri jaoks on Commerce Headquartersis õigesti konfigureeritud

Veenduge, et Dynamics 365 Payment Connector Puhvri jaoks on Commerce Headquartersis õigesti konfigureeritud, järgige järgmisi samme.

1. Avage **Jaemüük ja kaubandus \> Kanalid \> Veebipoed**.
1. Valige veebikauplus.
1. Kiirkaardil **Maksekontod** veenduge, et välja **Luba makseteabe salvestamine e-äris** väärtuseks on seatud **Tõene**.

![Luba e-commerce peakontori e-commerce'i väljale makseteabe salvestamine.](media/payment-connector-save-payment.jpg)

## <a name="additional-resources"></a>Lisaressursid

[Maksemoodul](../payment-module.md)

[Veebimaksevahendite salvestamine Adyeni konnektori abil](../dev-itpro/adyen-connector-listPI.md)
