---
title: Uute klientide loomisel tervitusmeil ei saadeta
description: See teema pakub tõrkeotsingu juhiseid, mis aitavad, kui tervituse meiliteatist ei saadeta, kui luuakse uus klient Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 1a4faf6cd189f69232e7f9ab8d0e79b320cfe2d9
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349925"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Uute klientide loomisel tervitusmeil ei saadeta

[!include [banner](../../includes/banner.md)]

See teema pakub tõrkeotsingu juhiseid, mis aitavad, kui tervituse meiliteatist ei saadeta, kui luuakse uus klient Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Kirjeldus

Kui rakendusse Commerce Headquarters luuakse uus klient, ei saadeta kliendile tervitusmeil, kuigi meiliteatis on konfigureeritud **kliendi** loodud meiliteatise tüübi jaoks.

## <a name="resolution"></a>Lahendus

### <a name="set-the-correct-email-id-value-for-the-customer-created-email-notification-type"></a>Seadke õige meili ID väärtus kliendi loodud meiliteatise tüübile

Kliendi loodud meiliteatise **tüübi õige** e-posti **ID** väärtuse häälestamiseks peakontoris järgige neid samme.

1. Minge rakenduse **Retail ja Commerce Headquarters häälestamise \> rakenduse \> Commerce meiliteatise profiili**.
1. Valige vasakul navigeerimispaanil meiliteatise profiil.
1. Jaemüügi **sündmuse teatiste sätetes** seadke **kliendi loodud meiliteatise** **tüübi korral välja Meili ID** väärtuseks **NewCust**.

## <a name="additional-resources"></a>Lisaressursid

[Meiliteatise profiili seadistamine](../email-notification-profiles.md)
