--- 
title: "Eelmääratletud tootevariantide loomine"
description: Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c49d25004b19084276404cf887188e89200afa32
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="create-predefined-product-variants"></a>Eelmääratletud tootevariantide loomine

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone. Selle protseduuri jaoks kasutati demoettevõtet USMF.


## <a name="create-a-product-master"></a>Tooteetaloni loomine
1. Avage Tooteteabe haldus > Tooted > Tooteetalonid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Toote number.
    * Tootenumbri sisestamine käsitsi on kohustuslik ainult siis, kui tootenumbri välja jaoks pole numbriseeriat seadistatud. Teisisõnu, jätke see etapp vahele, kui väljale on numbriseeria määratud.  
4. Sisestage väärtus väljale Toote nimi.
5. Sisestage või valige väärtus väljal Tootedimensioonigrupp.
    * Valige tootedimensioonigrupp SizeCol (suurus ja värv).  
6. Klõpsake nuppu OK.

## <a name="add-product-dimensions"></a>Tootedimensioonide lisamine
1. Klõpsake suvandit Tootedimensioonid.
    * Selles näites kirjeldatakse, kuidas sisestada käsitsi tootedimensioone. Samuti saate valida suuruse, värvi või laadi grupi, mis sisaldab tootedimensioon iväärtusi, mida soovite kasutada.  
2. Klõpsake valikut Uus.
3. Märkige loendis valitud rida.
4. Sisestage või valige väärtus väljal Suurus.
5. Sisestage väärtus väljale Nimi.
6. Klõpsake Uus.
7. Märkige loendis valitud rida.
8. Sisestage või valige väärtus väljal Suurus.
9. Sisestage väärtus väljale Nimi.
10. Klõpsake vahekaarti Värvid.
11. Klõpsake valikut Uus.
12. Märkige loendis valitud rida.
13. Sisestage või valige väärtus väljal Värv.
14. Sisestage väärtus väljale Nimi.
15. Klõpsake Uus.
16. Märkige loendis valitud rida.
17. Sisestage või valige väärtus väljal Värv.
18. Sisestage väärtus väljale Nimi.
19. Klõpsake nuppu Salvesta.
20. Sulgege leht.

## <a name="generate-product-variants"></a>Tootevariantide loomine
1. Klõpsake suvandit Tootevariandid.
2. Klõpsake suvandit Variandisoovitused.
3. Klõpsake nuppu Vali kõik.
    * Selles näites on valitud kõik võimalikud variandid. K variantide loomiseks kasutatakse ainult alamkogumit võimalikest tootedimensioonide kombinatsioonidest, saate valida üksikuid kirjeid.  
4. Klõpsake käsku Loo.
    * Saate luua kirjeldused kõikidele oma variantidele tootedimensiooni väärtuste kombinatsiooni alusel. Kirjeldused on valikulised.  
5. Klõpsake nuppu Salvesta.


