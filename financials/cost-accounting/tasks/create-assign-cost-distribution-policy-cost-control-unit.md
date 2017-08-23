--- 
title: "Kulujaotuspoliitika loomine ja määramine kulujuhtimisüksusele"
description: Kulujaotuse reeglite abil jaotatakse kulusid, mis on finantsiliselt koondkulukeskuses loendatud.
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 492e4a94ec0caef8c51a691043a1ffb9e6a04758
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a>Kulujaotuspoliitika loomine ja määramine kulujuhtimisüksusele

[!include[task guide banner](../../includes/task-guide-banner.md)]

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


