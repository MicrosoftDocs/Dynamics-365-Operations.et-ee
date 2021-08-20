---
title: Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.
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
ms.openlocfilehash: cc5167be43cccfd024ffdc65eb5f4dcac7e187288522d95be2385f8e7fdf106e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718643"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist

[!include [banner](../../includes/banner.md)]

See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.

## <a name="description"></a>Kirjeldus

See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.

## <a name="resolution"></a>Eraldusvõime

### <a name="configure-manual-capture-for-e-commerce-payments-in-the-adyen-portal"></a>Konfigureerige e-kaubanduse maksete käsitsi hõivamine Aydeni portaalis

Et konfigureerida e-kaubanduse maksete käsitsi hõivamine Adyeni portaalis, järgige järgmisi samme.

1. Logige sisse Adyeni portaali.
1. Valige ülemises parempoolses nurgas oma e-äri kanali kaupmehekonto.
1. Ülemisel navigeerimisribal valige **Konto** ja seejärel valige **Sätted**.
1. Väljal **Salvestamise viivitus** valige **käsitsi**.

    ![Viivitussätte hõivamine Adyen`i portaalis.](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Lisaressursid

[Adyeni maksekonnektor](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 Payment Connector Adyeni jaoks](../dev-itpro/adyen-connector.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.adyen.com/plugins/microsoft-dynamics)
