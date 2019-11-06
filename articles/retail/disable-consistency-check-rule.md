---
title: Jaemüügikande süsteemsuskontrolli reeglite keelamine
description: Selles teemas kirjeldatakse jaemüügikande süsteemsuskontrolli reeglite keelamise funktsiooni teenuses Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586293"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Jaemüügikande süsteemsuskontrolli reeglite keelamine 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Jaemüüjatel võib olla kordumatuid äristsenaariume ja protsesse. Seetõttu ei kehti kõigi jaemüüjate kohta kõik reeglid, mis on jaemüügikande süsteemsuskontrolli vaikimisi kaasatud. Nende muudatustega arvestamiseks sisaldab Microsoft Dynamics 365 Retail funktsiooni, mida saab kasutada mittekohaldatavate reeglite keelamiseks.

Kui soovite näha loendit reeglitest, mis on teie keskkonnas jaemüügikande süsteemsuskontrollis saadaval, ja soovite vaadata iga reegli olekut, avage **Retail \> Peakontori seadistamine \> Parameetrid \> Jaemüügi parameetrid** ja valige vahekaart **Kande kinnitamine**.

Vaikimisi on iga reegli olekuks seatud **Lubatud**. Nii kasutatakse jaemüügikannete kontrollimiseks, enne kui need jaemüügi väljavõtetesse lisatakse, kõiki reegleid. Reegli keelamiseks seadke selle olekuks **Keelatud**. Keelatud reegleid ei võeta arvesse, kui jaemüügikandeid väljavõtte arvutamise protsessi ajal kontrollitakse.

Kogu kontrollimisprotsessist möödumiseks (olenemata lubatud reeglitest) avage **Retail \> Peakontori seadistamine \> Parameetrid \> Jaemüügi parameetrid** ja siis määrake vahekaardil **Kande kinnitamine** suvandi **Keela jaemüügikannete süsteemsuskontroll** olekuks **Jah**. Kui selle suvandi olekuks on seatud **Ei**, ei saa seda kasutajaliidese kaudu seada tagasi olekusse **Jah**.
