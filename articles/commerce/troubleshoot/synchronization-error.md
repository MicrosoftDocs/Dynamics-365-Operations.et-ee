---
title: Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.
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
ms.openlocfilehash: 45eeae751051b58e1c9e725eb4ed4b5240026e7f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801431"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.

## <a name="description"></a>Kirjeldus

Võrgutellimuse sünkroonimisel kuvatakse järgmine tõrketeade: "Krediitkaarditehingute töötlemiseks peab olema vaikemakseteenus."

![Puuduv vaikimisi makseteenuse tõrge](media/default-payment-method-error.jpg)

## <a name="resolution"></a>Eraldusvõime

### <a name="confirm-or-set-the-default-payment-service-in-commerce-headquarters"></a>Commerce Headquartersi vaikimisi makseteenuse kinnitamine või seadistamine

Commerce Headquarters`i vaikimisi makseteenuse kinnitamine või seadistamine, järgi järgmisi samme.

1. Avage **Müügireskontro \> Maksete seadistus \> Makseteenused**.
1. Veenduge, et **Uute krediitkaartide suvandi vaikeprotsessor** on seadistatud valikule **Jah** ühe makseteenuse puhul.

## <a name="additional-resources"></a>Lisaressursid

[Krediitkaardi seadistamine, autoriseerimine ja hõivamine](https://docs.microsoft.com/dynamics365/finance/accounts-receivable/credit-card-authorizations)
