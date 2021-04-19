---
title: Eelmääratletud tootevariantide loomine
description: Selles protseduuris juhendatakse teid looma tooteetalonidele tootevariante, kasutades tootedimensioonide kombinatsioone.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions, EcoResProductVariantsPendingReleaseFormPart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8340d295ffd072c95d9b174507ef4203131c8165
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809346"
---
# <a name="create-predefined-product-variants"></a>Eelmääratletud tootevariantide loomine

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]