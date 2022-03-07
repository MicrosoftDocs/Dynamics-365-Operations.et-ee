---
title: Jaemüügikande süsteemsuskontrolli reeglite keelamine
description: Selles teemas kirjeldatakse kande süsteemsuskontrolli reeglite keelamise funktsiooni teenuses Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 381bc8534d4b0a06a50c8c18b3f78aba9d43a1f497bfd271361216ed1dee9197
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6746657"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a>Jaemüügikande süsteemsuskontrolli reeglite keelamine 

[!include [banner](../includes/banner.md)]

Jaemüüjatel võib olla kordumatuid äristsenaariume ja protsesse. Seetõttu ei kehti kõigi jaemüüjate kohta kõik reeglid, mis on kaubanduse kande süsteemsuskontrolli vaikimisi kaasatud. Nende muudatustega arvestamiseks sisaldab Microsoft Dynamics 365 Commerce funktsiooni, mida saab kasutada mittekohaldatavate reeglite keelamiseks.

Kui soovite näha loendit reeglitest, mis on teie keskkonnas kande süsteemsuskontrollis saadaval, ja soovite vaadata iga reegli olekut, avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid** ja valige vahekaart **Kande kinnitamine**.

Vaikimisi on iga reegli olekuks seatud **Lubatud**. Nii kasutatakse kannete kontrollimiseks, enne kui need kaubanduse väljavõtetesse lisatakse, kõiki reegleid. Reegli keelamiseks seadke selle olekuks **Keelatud**. Keelatud reegleid ei võeta arvesse, kui kandeid väljavõtte arvutamise protsessi ajal kontrollitakse.

Kogu kontrollimisprotsessist möödumiseks (olenemata lubatud reeglitest) avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid** ja siis määrake vahekaardil **Kande kinnitamine** suvandi **Keela kaubanduse kannete süsteemsuskontroll** olekuks **Jah**. Kui selle suvandi olekuks on seatud **Ei**, ei saa seda kasutajaliidese kaudu seada tagasi olekusse **Jah**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]