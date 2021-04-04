---
title: Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist
description: See teema annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.
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
ms.openlocfilehash: 788854a3119eb9ffaf839beb93a5bc15cdcd6387
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585285"
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

    ![Viivitussätte hõivamine Adyeni portaalis](media/adyen-capture-delay.jpg)

## <a name="additional-resources"></a>Lisaressursid

[Adyeni maksekonnektor](https://docs.adyen.com/point-of-sale/capturing-payments)

[Dynamics 365 maksekonnektor Adyeni jaoks](../dev-itpro/adyen-connector.md)

[Dynamics 365 maksekonnektor Adyeni jaoks](https://docs.adyen.com/plugins/microsoft-dynamics)
