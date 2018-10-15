--- 
title: "Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks"
description: "See juhend näitab, kuidas seadistada eelmääratletud tootevariantidele tootenumbri nomenklatuuri ja kuidas määrata seda sobivale tootedimensioonigrupile."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductDimensionGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4b49e96677b94d5f669ea41861f64e62e118938c
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-product-number-nomenclature-for-predefined-product-variants"></a>Tootenumbri nomenklatuuri loomine eelmääratletud tootevariantide jaoks

[!include [task guide banner](../../includes/task-guide-banner.md)]

See juhend näitab, kuidas seadistada eelmääratletud tootevariantidele tootenumbri nomenklatuuri ja kuidas määrata seda sobivale tootedimensioonigrupile. Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid. Uus tootenumbri nomenklatuur on määratud tootedimensioonigrupile Värv ja Suurus. Enamasti teeb selle toimingu toote koostaja.


## <a name="create-a-product-number-nomenclature"></a>Tootenumbri nomenklatuuri loomine
1. Klõpsake valikut Tootevariandi mudeli määratlus.
2. Klõpsake valikut Tootenomenklatuur.
3. Klõpsake valikut Uus.
4. Sisestage väljale Nimi nomenklatuuri nimi, mis aitab tuvastada siht-tootedimensioonigruppi, nt ColorSize.
5. Sisestage väljale Kirjeldus soovitud väärtus.
6. Klõpsake vahekaarti Lisa.
7. Klõpsake valikut Tooteetaloni number.
8. Klõpsake vahekaarti Lisa.
9. Klõpsake valikut Tekstikonstant.
10. Sisestage väärtus väljale Tekst.
11. Klõpsake vahekaarti Lisa.
12. Klõpsake valikut Värv.
13. Klõpsake vahekaarti Lisa.
14. Klõpsake valikut Tekstikonstant.
15. Sisestage väärtus väljale Tekst.
16. Klõpsake vahekaarti Lisa.
17. Klõpsake valikut Suurus.
18. Sulgege leht.

## <a name="assign-the-nomenclature-to-a-product-master"></a>Nomenklatuuri määramine tooteetalonile
1. Klõpsake valikut Tootedimensioonigrupid.
2. Valige tootedimensioonigrupp SizeCol.
3. Klõpsake nuppu Redigeeri.
4. Tehke väljal Kasuta nomenklatuuri valik Jah.
5. Sisestage või valige väärtus väljal Tootevariandi numbri nomenklatuur.
6. Sulgege leht.


