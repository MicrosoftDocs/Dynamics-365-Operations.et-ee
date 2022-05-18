---
title: Kulueraldamispoliitika loomine ja määramine kulujuhtimisüksusele
description: Selle protseduuri abil saate luua ja määrata kulude eraldamise poliitika ja vastavad reeglid kulu juhtseadmele.
author: twheeloc
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostAccountingLedgerPolicyAssignment
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5082f4e80958ddb1e4a79bfe46df4a621f10fc40
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734243"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a>Kulueraldamispoliitika loomine ja määramine kulujuhtimisüksusele

[!include [banner](../../includes/banner.md)]

Selle protseduuri abil saate luua ja määrata kulude eraldamise poliitika ja vastavad reeglid kulu juhtseadmele. See salvestis kasutab USP2 demoandmete ettevõtet.


## <a name="create-a-policy"></a>Poliitika loomine
1. Minge kuluarvestuse **poliitikate > > kulude eraldamise poliitikate kohta**.
2. Klõpsake valikut **Uus**.
3. **Tippige väärtus väljale** Poliitika nimi.
4. Sisestage **või valige väärtus väljale** Kuluobjekti dimensioonihierarhia.
    * Valige suvand Organisatsioon.  
5. Sisestage **või valige** väärtus väljal Statistiline dimensioon.
6. Klõpsake nuppu **Salvesta**.

## <a name="create-allocation-rules"></a>Eraldusreeglite loomine
1. Klõpsake valikut **Uus**.
2. Märkige loendis valitud rida.
3. Sisestage **või valige väärtus väljal Kuluobjekti** dimensioonihierarhia sõlm.
4. **Väljal Kulu käitumine** valige "Kokku".
5. Sisestage **või valige** väärtus väljal Eraldamise alus.
6. Klõpsake valikut **Uus**.
7. Märkige loendis valitud rida.
8. Sisestage **või valige väärtus väljal Kuluobjekti** dimensioonihierarhia sõlm.
9. **Väljal Kulu käitumine** valige "Kokku".
10. Sisestage **või valige** väärtus väljal Eraldamise alus.
11. Klõpsake valikut **Uus**.
12. Märkige loendis valitud rida.
13. Sisestage **või valige väärtus väljal Kuluobjekti** dimensioonihierarhia sõlm.
14. **Väljal Kulu käitumine** valige "Kokku".
15. Sisestage **või valige** väärtus väljal Eraldamise alus.
    * Jätkake, kuni olete kõik reeglid loonud.  
16. Klõpsake nuppu **Salvesta**.

## <a name="assign-the-policy-to-a-cost-control-unit"></a>Poliitika määramine kulu juhtseadmele
1. Klõpsake **kulujuhtimise üksuse poliitika määranguid**.
2. Klõpsake valikut **Uus**.
3. Märkige loendis valitud rida.
4. Sisestage **kuupäev väljale Kehtiv** raamatupidamiskuupäevast.
    * Reeglite kehtivus sõltub kuupäevast. Kasutaja või süsteem saab muuta reeglid aegunuks, kui luuakse uuem versioon.  
5. Sisestage **või valige väärtus** väljal Kulujuhtimise ühik.
6. Klõpsake nuppu **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
