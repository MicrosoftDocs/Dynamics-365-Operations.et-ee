---
title: Protsesside loomine (veebruar 2016)
description: See ülesanne keskendub valmistoote ja pooltoote jaoks tootmisprotsesside loomisele.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "354088"
---
# <a name="create-routes-february-2016"></a>Protsesside loomine (veebruar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

See ülesanne keskendub valmistoote ja pooltoote jaoks tootmisprotsesside loomisele. See on viies ülesanne koosluse arvutamise seerias. Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.


## <a name="create-a-route-for-a-semi-finished-product"></a>Marsruudi loomine pooleldi lõpetatud tootele
1. Avage Tooteteabe haldus > Tooted > Väljastatud tooted.
2. Klõpsake loendis valitud real olevat linki.
    * Valige kaubakood BOM_2.  
3. Klõpsake toimingupaanil suvandit Projekteeri.
4. Klõpsake valikut Protsess.
5. Klõpsake valikut Uus.
6. Klõpsake nuppu Protsess ja protsessi versioon.
7. Sisestage väljale Kirjeldus soovitud väärtus.
    * Näiteks tippige ROUTE_2.  
8. Sisestage või valige väärtus väljal Koht.
    * Selles snäites sisestage või valige Sait 1.  
9. Klõpsake nuppu OK.
10. Klõpsake valikut Uus.
11. Sisestage või valige väärtus väljal Toiming.
    * Selles näites valige Assembler.  
12. Sisestage number väljale Käitusaeg.
    * Tippige näiteks 1. Käitusajad on sageli osa kauba puhul arvutatavast hinnast.  
13. Sisestage või valige väärtus väljal Protsessigrupp.
    * Selles näites valige Std.  
14. Klõpsake vahekaarti Seadistus.
15. Sisestage või valige väärtus väljal Seadistuse kategooria.
    * Selles näites valige Assembler.  
16. Klõpsake vahekaarti Ajad.
17. Väljale Häälestusaeg sisestage number.
    * Selles näites tippige 1. Häälestusajad on sageli osa hinnast, mis kauba puhul arvutatakse.  
18. Tegevuspaanil klõpsake nuppu Protsessi versioon.
19. Klõpsake nuppu Kinnita.
20. Valikus Kas soovite ka protsessi kinnitada? tehke valik Jah. valik Jah.
21. Klõpsake nuppu OK.
22. Tegevuspaanil klõpsake nuppu Protsessi versioon.
23. Klõpsake käsku Aktiveeri.
24. Sulgege leht.
25. Sulgege leht.

## <a name="create-a-route-for-a-finished-product"></a>Marsruudi loomine lõpetatud tootele
1. Klõpsake loendis valitud real olevat linki.
    * Valige kaubakood BOM_1.  
2. Klõpsake toimingupaanil suvandit Projekteeri.
3. Klõpsake valikut Protsess.
4. Klõpsake valikut Uus.
5. Klõpsake nuppu Protsess ja protsessi versioon.
6. Sisestage väljale Kirjeldus soovitud väärtus.
    * Selles näites tippige ROUTE_1.  
7. Sisestage või valige väärtus väljal Koht.
    * Selles snäites sisestage või valige Sait 1.  
8. Klõpsake nuppu OK.
9. Klõpsake valikut Uus.
10. Sisestage või valige väärtus väljal Toiming.
    * Selles näites valige Pakkimine.  
11. Sisestage number väljale Käitusaeg.
    * Selles näites tippige 1.  
12. Sisestage või valige väärtus väljal Protsessigrupp.
    * Selles näites valige Std.  
13. Klõpsake vahekaarti Seadistus.
14. Sisestage või valige väärtus väljal Seadistuse kategooria.
    * Selles näites valige Pakkimine.  
15. Klõpsake vahekaarti Ajad.
16. Väljale Häälestusaeg sisestage number.
    * Selles näites tippige 1.  
17. Tegevuspaanil klõpsake nuppu Protsessi versioon.
18. Klõpsake nuppu Kinnita.
19. Klõpsake nuppu OK.
20. Tegevuspaanil klõpsake nuppu Protsessi versioon.
21. Klõpsake käsku Aktiveeri.
22. Sulgege leht.
23. Sulgege leht.

## <a name="enable-automatic-consumption-of-setup-time"></a>Häälestusaja automaatse tarbimise lubamine
1. Avage Tootmise juhtimine > Häälestamine > Marsruudid > Protsessigrupid.
2. Otsige loendist ja valige soovitud kirje.
    * Valige loendist Std.  
3. Klõpsake nuppu Redigeeri.
4. Väljal Häälestusaeg valige Jah.
    * Häälestusajad on sageli osa hinnast, mis kauba puhul arvutatakse.  
5. Klõpsake nuppu Salvesta.
6. Sulgege leht.

