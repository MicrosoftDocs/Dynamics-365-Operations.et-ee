---
title: Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge
description: See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.
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
ms.openlocfilehash: 6f8e0ea7675ffc5cbada36207422b410234e33afcaec90636e90e573a90ac484
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715232"
---
# <a name="order-synchronization-error-related-to-the-default-payment-service"></a>Vaikemakseteenusega seotud tellimuse sünkroonimise tõrge

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad parandada tõrget, mis võib ilmneda võrgutellimuse sünkroonimisel.

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