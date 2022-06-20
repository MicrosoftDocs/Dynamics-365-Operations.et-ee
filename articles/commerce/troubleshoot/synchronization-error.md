---
title: Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge
description: See artikkel annab tõrkeotsingu juhised, mis aitavad lahendada tõrke, mis võib ilmneda võrgutellimuse sünkroonimisel.
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
ms.openlocfilehash: 49d16c39fdcee0a22d1cabe14cd9b6d124d6f04d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901672"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad lahendada tõrke, mis võib ilmneda võrgutellimuse sünkroonimisel.

## <a name="description"></a>Kirjeldus

Võrgutellimuse sünkroonimisel kuvatakse järgmine tõrketeade: "Krediitkaarditehingute töötlemiseks peab olema vaikemakseteenus."

![Vaikimisi puuduva makseteenuse tõrge.](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Lahendus

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Commerce Headquartersi vaikimisi makseteenuse kinnitamine või seadistamine

Commerce Headquarters`i vaikimisi makseteenuse kinnitamine või seadistamine, järgi järgmisi samme.

1. Avage **Müügireskontro \> Maksete seadistus \> Makseteenused**.
1. Veenduge, et **Uute krediitkaartide suvandi vaikeprotsessor** on seadistatud valikule **Jah** ühe makseteenuse puhul.

## <a name="additional-resources"></a>Lisaressursid

[Krediitkaardi seadistamine, autoriseerimine ja hõivamine](../../finance/accounts-receivable/credit-card-authorizations.md)