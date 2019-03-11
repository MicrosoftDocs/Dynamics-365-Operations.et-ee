---
title: Kulueraldamispoliitika loomine ja määramine kulujuhtimisüksusele
description: Selle protseduuri abil saate luua ja määrata kulude eraldamise poliitika ja vastavad reeglid kulu juhtseadmele.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92f41eb99b84bbc596e79b413971f9d92f2555b6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "324395"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Kulueraldamispoliitika loomine ja määramine kulujuhtimisüksusele

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuri abil saate luua ja määrata kulude eraldamise poliitika ja vastavad reeglid kulu juhtseadmele. See salvestis kasutab USP2 demoandmete ettevõtet.


## <a name="create-a-policy"></a>Poliitika loomine
1. Avage Kuluarvestus > Poliitikad > Kulude eraldamise poliitikad.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Poliitika nimi.
4. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.
    * Valige suvand Organisatsioon.  
5. Sisestage või valige väärtus väljal Statistiline dimensioon.
6. Klõpsake nuppu Salvesta.

## <a name="create-allocation-rules"></a>Eraldusreeglite loomine
1. Klõpsake valikut Uus.
2. Märkige loendis valitud rida.
3. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
4. Valige väljal Kulukäitumine väärtus Kokku.
5. Sisestage või valige väärtus väljal Eraldamise alus.
6. Klõpsake valikut Uus.
7. Märkige loendis valitud rida.
8. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
9. Valige väljal Kulukäitumine väärtus Kokku.
10. Sisestage või valige väärtus väljal Eraldamise alus.
11. Klõpsake valikut Uus.
12. Märkige loendis valitud rida.
13. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
14. Valige väljal Kulukäitumine väärtus Kokku.
15. Sisestage või valige väärtus väljal Eraldamise alus.
    * Jätkake, kuni olete kõik reeglid loonud.  
16. Klõpsake nuppu Salvesta.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Poliitika määramine kulu juhtseadmele
1. Klõpskae kulu juhtseadme suvandit Poliitikamäärangud.
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Sisestage kuupäev väljale Aruandluse alguskuupäev.
    * Reeglite kehtivus sõltub kuupäevast. Kasutaja või süsteem saab muuta reeglid aegunuks, kui luuakse uuem versioon.  
5. Sisestage või valige väärtus väljal Kulu juhtseade.
6. Klõpsake nuppu Salvesta.

