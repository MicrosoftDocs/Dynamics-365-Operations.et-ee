---
title: Kulujaotuspoliitika loomine ja määramine kulujuhtimisüksusele
description: Kulujaotuse reeglite abil jaotatakse kulusid, mis on finantsiliselt koondkulukeskuses loendatud.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d040f9495c7fb36985b5f96c15ac43aa226da24
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841317"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Kulujaotuspoliitika loomine ja määramine kulujuhtimisüksusele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kulujaotuse reeglite abil jaotatakse kulusid, mis on finantsiliselt koondkulukeskuses loendatud. Kuluarvestaja tagab kulude jaotamise kulukeskustele valitud eraldamisaluse põhjal. Kulude juhtseadmele määratakse poliitika ja vastavad reeglid. Selles tegevusjuhises näidatakse näite abil, kuidas luua kulude jaotamise poliitikat ja vastavaid reegleid.


## <a name="create-a-policy"></a>Poliitika loomine
1. Avage Kuluarvestus > Poliitikad > Kulude jaotamise poliitikad.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Poliitika nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.
    * Valige suvand Organisatsioon.  
6. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia.
    * Valige CDS P/L.  
7. Sisestage või valige väärtus väljal Statistiline dimensioon.
    * Valige suvand Statistilised elemendid.  
8. Klõpsake nuppu Salvesta.

## <a name="create-rules-for-the-policy"></a>Poliitika jaoks reeglite loomine
1. Klõpsake valikut Uus.
2. Märkige loendis valitud rida.
3. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
    * Laiendage hierarhia väärtuse 094 valimiseks.  
4. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.
    * Valige suvand Muud tegevuskulud ja seejärel 605110 Puhastus.  
5. Valige suvand väljal Kulukäitumine.
    * Valige suvand Fikseeritud omahind.  
6. Sisestage või valige väärtus väljal Eraldamise alus.
7. Klõpsake valikut Uus.
8. Märkige loendis valitud rida.
9. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
    * Laiendage hierarhia väärtuse 094 valimiseks.  
10. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.
    * Valige suvand Muud tegevuskulud ja seejärel 605150 Üür.  
11. Valige suvand väljal Kulukäitumine.
    * Valige suvand Fikseeritud omahind.  
12. Sisestage või valige väärtus väljal Eraldamise alus.
13. Klõpsake nuppu Salvesta.

## <a name="assign-rules-to-a-cost-control-unit"></a>Reeglite määramine kulu juhtseadmele
1. Klõpskae kulu juhtseadme suvandit Poliitikamäärangud.
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Sisestage kuupäev väljale Aruandluse alguskuupäev.
    * Valige sobiva finantsaasta 1. september.  
5. Sisestage või valige väärtus väljal Kulu juhtseade.
6. Klõpsake nuppu Salvesta.

