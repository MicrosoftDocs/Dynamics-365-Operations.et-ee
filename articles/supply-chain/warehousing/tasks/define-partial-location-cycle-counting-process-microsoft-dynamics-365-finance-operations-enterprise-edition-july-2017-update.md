--- 
title: "Osalise asukoha tsüklilise inventuuriprotsessi määratlemine "
description: "Kui kasutate inventuuri jaoks tsüklilise inventuuri plaane, saate juhtida tegelikke inventuuritöid, kui taotlete, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 507a1147fea62c12490291362d365224efeda97e
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="define-partial-location-cycle-counting-process"></a>Osalise asukoha tsüklilise inventuuriprotsessi määratlemine  

[!include[task guide banner](../../includes/task-guide-banner.md)]

Kui kasutate inventuuri jaoks tsüklilise inventuuri plaane, saate juhtida tegelikke inventuuritöid, kui taotlete, et asukohas loendataks kogu vaba kaubavaru asemel ainult konkreetseid tooteid ja tootevariante. Konkreetseid tooteid filtreerides saab laojuht vähendada ülevaatamise üldkulusid, vältida konsolideerimisvigu ja säästa aega. Tavaliselt teostab seadistusülesanded laojuhataja. Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.


## <a name="create-a-cycle-counting-work-template"></a>Tsüklilise inventuuri malli loomine
1. Avage Laohaldus > Seadistus > Töö > Töömallid.
2. Tehke väljal Töötellimuse tüüp valik „Tsükliline inventuur”.
3. Klõpsake valikut Uus.
4. Sisestage number väljale Seerianumber.
    * Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini. Väärtus peab olema suurem kui 0 (null).  
5. Märkige loendis valitud rida.
6. Sisestage väärtus väljale Töömall.
7. Tippige väärtus väljale Töömalli kirjeldus.
8. Sisestage või valige väärtus väljal Töökausta ID.
9. Sisestage arv väljale Töö prioriteet.
10. Klõpsake nuppu Salvesta.
11. Klõpsake valikut Uus.
12. Märkige loendis valitud rida.
13. Valige Töö tüübi väljal „Inventuur”.
14. Sisestage või valige väärtus väljal Tööklassi ID.
15. Klõpsake nuppu Salvesta.
16. Klõpsake valikut Töörea jaotused.
17. Klõpsake valikut Uus.
18. Sisestage number väljale Seerianumber.
    * Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini. Väärtus peab olema suurem kui 0 (null).  
19. Klõpsake nuppu Salvesta.
20. Sulgege leht.
21. Sulgege leht.

## <a name="create-a-cycle-counting-plan"></a>Tsükliline inventuuri plaani loomine
1. Avage Laohaldus > Seadistus > Tsükliline inventuur > Tsüklilise inventuuri plaanid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Tsüklilise inventuuri plaani ID.
4. Sisestage väärtus väljale Kirjeldus.
5. Sisestage number väljale Tsükliliste inventuuride maksimumarv.
6. Sisestage või valige väärtus väljal Töömall.
7. Klõpsake valikut Uus.
8. Sisestage number väljale Seerianumber.
    * Sortimisjärjestus on kõige väiksemast numbrist suurima numbrini. Väärtus peab olema suurem kui 0 (null).  
9. Sisestage väljale Kirjeldus soovitud väärtus.
10. Klõpsake nuppu Salvesta.
11. Klõpsake valikut Määratle tootepäring.
12. Märkige loendis valitud rida.
13. Sisestage või valige väärtus väljal Kriteeriumid.
14. Klõpsake nuppu OK.
15. Sulgege leht.


