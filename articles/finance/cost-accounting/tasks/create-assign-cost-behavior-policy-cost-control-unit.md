---
title: Kulukäitumispoliitika loomine ja määramine kulujuhtimisüksusele
description: Kulukäitumine on kulude liigitamine fikseerituks või muutuvaks.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735138"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Kulukäitumispoliitika loomine ja määramine kulujuhtimisüksusele

[!include [banner](../../includes/banner.md)]

Kulukäitumine on kulude liigitamine fikseerituks või muutuvaks. Poliitika ja vastavad reeglid tuleb poliitika jõustamiseks määrata kulu juhtseadmele. Selle protseduuri abil saate luua poliitika ja seejärel määrata selle kulu juhtseadmele.


## <a name="create-a-cost-behavior-hierarchy"></a>Kulukäitumise hierarhia loomine
1. Minge dimensioonide **> kuluarvestusse > dimensioonihierarhiatega**.
2. Klõpsake valikut **Uus**.
3. Klõpsake käsku **Loo**.
4. **Tippige dimensiooni hierarhia nime** väljale Kulukäitumise hierarhia.
5. Sisestage **või** valige väärtus väljal Dimensioon.
    * Valige suvand Kuluelemendid.  
6. Klõpsake nuppu **Salvesta**.
7. Klõpsake **käsku Kuva hierarhia**.
8. Klõpsake valikut **Uus**.
9. **Tippige väärtus väljale Sõlme** nimi.
    * Sisestage fikseeritud omahind.  
10. Valige puus väärtus Kulukäitumise hierarhia.
11. Klõpsake valikut **Uus**.
12. **Tippige väärtus väljale Sõlme** nimi.
    * Sisestage muutuv kulu.  
13. Klõpsake nuppu **Salvesta**.
14. Valige puus väärtus Kulukäitumise hierarhia\Fikseeritud omahind.
15. Klõpsake valikut **Uus**.
16. Märkige loendis valitud rida.
17. Sisestage **või valige väärtus** väljal Dimensiooni liikmelt.
    * Dimensiooni liikmete vahemik võib sisaldada tühikuid, kuid liikmed ei tohi kattuda.  
18. Sisestage **või valige väärtus** väljal Dimensiooni liikmeni.
    * Dimensiooni liikmete vahemik võib sisaldada tühikuid, kuid liikmed ei tohi kattuda.  
19. Valige puus väärtus Kulukäitumise hierarhia\Muutuv kulu.
20. Klõpsake valikut **Uus**.
21. Märkige loendis valitud rida.
22. Sisestage **või valige väärtus** väljal Dimensiooni liikmelt.
    * Dimensiooni liikmete vahemik võib sisaldada tühikuid, kuid liikmed ei tohi kattuda.  
23. Sisestage **või valige väärtus** väljal Dimensiooni liikmeni.
    * Dimensiooni liikmete vahemik võib sisaldada tühikuid, kuid liikmed ei tohi kattuda.  
24. Klõpsake nuppu **Salvesta**.

## <a name="create-the-policy-and-rules"></a>Poliitika ja reeglite loomine
1. Minge kuluarvestuse **poliitikate > > kulukäitumise poliitikate kohta**.
2. Klõpsake valikut **Uus**.
3. **Tippige väärtus väljale** Poliitika nimi.
4. Sisestage **või valige väärtus väljal** Kuluelemendi dimensioonihierarhia.
    * Valige äsja loodud poliitikahierarhia.  
5. Sisestage **või valige väärtus väljale** Kuluobjekti dimensioonihierarhia.
    * Valige suvand Organisatsioon.  
6. Klõpsake nuppu **Salvesta**.
7. Klõpsake valikut **Uus**.
8. Märkige loendis valitud rida.
9. Sisestage **või valige väärtus väljal Kuluelemendi** dimensioonihierarhia sõlm.
    * Laiendage hierarhia, et valida väärtus Muutuv kulu.  
10. Sisestage **või valige väärtus väljal Kuluobjekti** dimensioonihierarhia sõlm.
    * Vaikimisi on muutuja 100 protsenti.  
11. Klõpsake **kulujuhtimise üksuse poliitika määranguid**.
12. Klõpsake valikut **Uus**.
13. Märkige loendis valitud rida.
14. Sisestage **kuupäev väljale Kehtiv** raamatupidamiskuupäevast.
    * Reeglite kehtivus sõltub kuupäevast ja kasutaja või süsteem saab muuta reegli aegunuks, kui luuakse uuem versioon.  
15. Sisestage **või valige väärtus** väljal Kulujuhtimise ühik.
16. Klõpsake nuppu **Salvesta**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
