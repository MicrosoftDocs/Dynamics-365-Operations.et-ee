---
title: Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist
description: See artikkel annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.
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
ms.openlocfilehash: 6fdaf48600edc22b5423e0167177616758e2dc6e
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282703"
---
# <a name="payments-are-automatically-settled-before-orders-are-invoiced-or-shipped"></a>Maksed tasakaalustatakse automaatselt enne tellimuste arveldamist või saatmist

[!include [banner](../../includes/banner.md)]

See artikkel annab tõrkeotsingu juhised, mis aitavad, kui makse on Portaalis tasakaalustatud kohe pärast tellimuse sisestamist, isegi kui müügitellimus on arveldamata või saadetud.

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
