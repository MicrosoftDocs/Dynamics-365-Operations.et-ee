---
title: Uute klientide loomisel tervitusmeili ei saadeta
description: See artikkel pakub tõrkeotsingu juhiseid, mis aitavad, kui tervituse meiliteatist ei saadeta, kui luuakse uus klient Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 08/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-02-10
ms.openlocfilehash: 5aa7d864555f96194500989e2d7ad200d8892121
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2022
ms.locfileid: "9219400"
---
# <a name="welcome-email-isnt-sent-when-new-customers-are-created"></a>Uute klientide loomisel ei saadeta tervitusmeil

[!include [banner](../../includes/banner.md)]

See artikkel pakub tõrkeotsingu juhiseid, mis aitavad, kui tervituse meiliteatist ei saadeta, kui luuakse uus klient Microsoft Dynamics 365 Commerce.

## <a name="description"></a>Kirjeldus

Kui rakendusse Commerce Headquarters luuakse uus klient, ei saadeta kliendile tervitusmeil, kuigi meiliteatis on konfigureeritud **kliendi** loodud meiliteatise tüübi jaoks.

## <a name="resolution"></a>Lahendus

### <a name="associate-an-email-notification-profile-under-commerce-parameters"></a>Meiliteatise profiili seostamine Commerce’i parameetrite all

1. Peakontoris minge Rakenduse Retail ja **Commerce Headquarters häälestamise \> parameetrite \> commerce \> parameters General alla \>**.
2. Valige ripploendist **Meiliteatise** profiil, mis sisaldab vastendust kliendi loodud teatise tüübi ja kliendi loodud meilimalli vahel.  

> [!NOTE] 
> Kliendi loodud teatiste lubamisel saavad kõigis juriidilise isiku kanalites loodud kliendid kliendi loodud meili. Kliendi loodud teatisi ei saa praegu piirata ühele kanalile.

Lisateavet vt teemast Meilimallide [loomine kandesündmuste jaoks](../email-templates-transactions.md). 

## <a name="additional-resources"></a>Lisaressursid

[Meiliteatise profiili seadistamine](../email-notification-profiles.md)
