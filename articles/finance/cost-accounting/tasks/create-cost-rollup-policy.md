---
title: Kulukomplekti poliitika loomine
description: See protseduur näitab, kuidas luua kulukomplekti poliitikat ja selle jaoks reegleid.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fd7a390ced7b7b4997d9c86b9218f1fa83ee14729e450e1ae1cb53dbbd605edb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755662"
---
# <a name="create-a-cost-rollup-policy"></a>Kulukomplekti poliitika loomine

[!include [banner](../../includes/banner.md)]

See protseduur näitab, kuidas luua kulukomplekti poliitikat ja selle jaoks reegleid. Selle protseduuri loomiseks kasutati demoandmeid USP2.


## <a name="create-a-policy"></a>Poliitika loomine
1. Valige Kuluarvestus > Poliitikad > Kulukomplekti poliitikad.
2. Klõpsake valikut Uus.
3. Tippige väärtus väljale Poliitika nimi.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia.
    * Valige suvand Kulukomplekt CC.  
6. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia.
    * Valige suvand Kulukomplekt CC.  
7. Klõpsake nuppu Salvesta.

## <a name="create-rules-for-the-cost-rollup-policy"></a>Poliitika jaoks reeglite loomine
1. Klõpsake valikut Uus.
2. Märkige loendis valitud rida.
3. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
    * Valige 007.  
4. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.
    * Valige suvand Kulukomplekt CE.  
5. Sisestage või valige väärtus väljal Teisene kuluelement.
    * Näiteks vastendage teisene kuluelement CC-007 kulukeskusega.  
6. Klõpsake valikut Uus.
7. Märkige loendis valitud rida.
8. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
    * Valige 008.  
9. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.
    * Valige suvand Kulukomplekt CE.  
10. Sisestage või valige väärtus väljal Teisene kuluelement.
    * Näiteks vastendage teisene kuluelement CC-008 kulukeskusega.  
11. Klõpsake valikut Uus.
12. Märkige loendis valitud rida.
13. Sisestage või valige väärtus väljal Kuluobjekti dimensioonihierarhia sõlm.
    * Valige 009.  
14. Sisestage või valige väärtus väljal Kuluelemendi dimensioonihierarhia sõlm.
    * Valige suvand Kulukomplekt CE.  
15. Sisestage või valige väärtus väljal Teisene kuluelement.
    * Näiteks vastendage teisene kuluelement CC-009 kulukeskusega.  
    * Jätkake, kuni kõik kulukeskused on vastendatud vastavate teiseste kuluelementidega.  
16. Klõpsake nuppu Salvesta.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]