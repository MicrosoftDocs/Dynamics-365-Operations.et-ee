--- 
title: " Tootepakendite loomine ostutellimuste jaoks"
description: See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist.
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 695460415f81d65ec35eeee60209358b722c9244
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="create-product-packages-for-purchase-orders"></a> Tootepakendite loomine ostutellimuste jaoks

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur selgitab tootepaketi loomist ja ostutellimusel kasutamist. Ostutellimust kasutatakse tellimuse loomiseks eelmääratletud tootekogumi kohta. Protseduur kasutab demoettevõtte USRT andmeid.


## <a name="create-a-product-package"></a>Tootepaketi loomine
1. Avage Jaemüük ja kaubandus > Varude haldus > Täiendamine > Tootepakendid.
2. Klõpsake valikut Uus.
3. Sisestage väärtus väljale Paketi number.
4. Sisestage väljale Kirjeldus soovitud väärtus.
5. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
6. Klõpsake loendis valitud real olevat linki.
7. Klõpsake vahekaarti Lisa.
8. Sisestage väljale Kaubakood väärtus 0160.
9. Klõpsake väljal Suurus otsingu avamiseks ripploendi nuppu.
10. Klõpsake loendis valitud real olevat linki.
11. Sisestage arv väljale Kogus.
12. Klõpsake vahekaarti Lisa.
13. Sisestage väljale Kaubakood väärtus 0160.
14. Klõpsake väljal Variandi number otsingu avamiseks ripploendi nuppu.
15. Klõpsake loendis valitud real olevat linki.
16. Sisestage arv väljale Kogus.
17. Klõpsake vahekaarti Lisa.
18. Sisestage väljale Kaubakood väärtus 0175.
19. Sisestage arv väljale Kogus.
20. Klõpsake nuppu Salvesta.
21. Sulgege leht.

## <a name="add-package-to-puchase-order"></a>Paketi lisamine ostutellimusele
1. Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.
2. Klõpsake valikut Uus.
3. Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.
4. Valige loendist sama hankija, kelle jaoks tootepakett viimati hankija valimisel loodi.
5. Lülitage jaotise Üldine laiendamist.
6. Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.
7. Klõpsake loendis valitud real olevat linki.
8. Klõpsake väljal Ladu otsingu avamiseks ripploendi nuppu.
9. Klõpsake loendis valitud real olevat linki.
10. Klõpsake nuppu OK.
11. Lülitage jaotise Rea üksikasjad laiendamist.
12. Klõpsake vahekaarti Tootepaketid.
13. Klõpsake suvandit Ostutellimuse rida.
14. Klõpsake suvandit Loo paketist read.
15. Leidke ja valige loendist eelmises etapis loodud tootepakett.
16. Sisestage arv väljale Kogus.
17. Klõpsake käsku Loo.
18. Klõpsake nuppu Salvesta.


