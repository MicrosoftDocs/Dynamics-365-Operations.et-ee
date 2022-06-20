---
title: Uute klientide loomisel tervitusmeili ei saadeta
description: See artikkel pakub tõrkeotsingu juhiseid, mis aitavad, kui tervituse meiliteatist ei saadeta, kui luuakse uus klient Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/24/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 8e95b33d4b8a9af13c613ab89dd33de6b4934694
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853679"
---
# <a name="welcome-email-is-not-sent-when-new-customers-are-created"></a>Uute klientide loomisel tervitusmeili ei saadeta

[!include [banner](../../includes/banner.md)]

See artikkel pakub tõrkeotsingu juhiseid, mis aitavad, kui tervituse meiliteatist ei saadeta, kui luuakse uus klient Microsoft Dynamics 365 Commerce.

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
