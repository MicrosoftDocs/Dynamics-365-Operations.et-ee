---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (1. osa – andmemudeli koostamine)
description: See artikkel kirjeldab, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit, et kasutada finantsdimensioone ER-aruannete andmeallikana. (1. osa)
author: kfend
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
ms.openlocfilehash: 053b9cf9ea6b2845bef5d95e901c1c90fac964be
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290840"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a>Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (1. osa – andmemudeli koostamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraator või elektroonilise aruandluse arendaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana. Neid toiminguid saab teha igas ettevõttes.

Etappide lõpule viimiseks, peate esmalt läbima protseduuri „Pakkuja konfiguratsiooni loomine ning aktiivseks märkimine” etapid.


## <a name="create-a-new-data-model"></a>Uue andmemudeli loomine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et „Litware, Inc.“ pakkuja on saadaval ja märgitud aktiivseks.  
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
4. Tippige väljale Nimi tekst Finantsdimensioonide näidismudel.
5. Klõpsake Loo konfiguratsioon.
6. Klõpsake valikut Kujundaja.
7. Rippdialoogi avamiseks klõpsake valikut Uus.
8. Tippige väljale Nimi sõna Kirje.
9. Klõpsake vahekaarti Lisa.
10. Rippdialoogi avamiseks klõpsake valikut Uus.
11. Sisestage väljale Nimi suvand Ettevõte.
12. Klõpsake vahekaarti Lisa.
    * Lisame oma mudelile uue kirjete loendi. See loend toob välja (elektrooniliste aruannete puhul, kus seda mudelit andmeallikana kasutatakse) valitud finantsdimensioonide sätted. Iga finantsdimensioon esitatakse selles loendis kirjena, millel on vastavad dimensiooni sätet kajastavad väljad.  
13. Rippdialoogi avamiseks klõpsake valikut Uus.
14. Tippige Dimensioonide seadistamine väljale Nimi.
15. Valige väljalt Kaubakood suvand Kirjete loend.
16. Klõpsake vahekaarti Lisa.
17. Rippdialoogi avamiseks klõpsake valikut Uus.
18. Tippige Kood väljale Nimi.
19. Valige väljalt Kaubakood suvand String.
20. Klõpsake vahekaarti Lisa.
21. Rippdialoogi avamiseks klõpsake valikut Uus.
22. Sisestage väljale Nimi suvand Nimi.
23. Klõpsake vahekaarti Lisa.
24. Valige puul väärtus Kirje.
25. Rippdialoogi avamiseks klõpsake valikut Uus.
26. Tippige Tööleht väljale Nimi.
27. Valige väljalt Kaubakood suvand Kirjete loend.
28. Klõpsake vahekaarti Lisa.
29. Rippdialoogi avamiseks klõpsake valikut Uus.
30. Tippige Partii väljale Nimi.
31. Valige väljalt Kaubakood suvand String.
32. Klõpsake vahekaarti Lisa.
33. Rippdialoogi avamiseks klõpsake valikut Uus.
34. Tippige väljale Nimi valik Kanne.
35. Valige väljalt Kaubakood suvand Kirjete loend.
36. Klõpsake vahekaarti Lisa.
37. Rippdialoogi avamiseks klõpsake valikut Uus.
38. Tippige Kuupäev väljale Nimi.
39. Valige väljalt Kaubakood suvand Kuupäev.
40. Klõpsake vahekaarti Lisa.
41. Rippdialoogi avamiseks klõpsake valikut Uus.
42. Tippige Deebet väljale Nimi.
43. Valige väljalt Kaubakood suvand Tegelik.
44. Klõpsake vahekaarti Lisa.
45. Rippdialoogi avamiseks klõpsake valikut Uus.
46. Tippige Kreedit väljale Nimi.
47. Klõpsake vahekaarti Lisa.
48. Rippdialoogi avamiseks klõpsake valikut Uus.
49. Sisestage väljale Nimi suvand Valuuta.
50. Valige väljalt Kaubakood suvand String.
51. Klõpsake vahekaarti Lisa.
52. Rippdialoogi avamiseks klõpsake valikut Uus.
53. Tippige Kanne väljale Nimi.
54. Klõpsake vahekaarti Lisa.
55. Rippdialoogi avamiseks klõpsake valikut Uus.
56. Tippige Dimensioonide andmed väljale Nimi.
57. Valige väljalt Kaubakood suvand Kirjete loend.
58. Klõpsake vahekaarti Lisa.
    * Lisasime oma mudelile uue kirjete loendi. See loend toob välja (elektrooniliste aruannete puhul, kus seda mudelit andmeallikana kasutatakse) valitud finantsdimensioonide väärtused. Iga finantsdimensioon esitatakse selles loendis kirjena, millel on vastavad dimensiooni väärtusi kajastavad väljad. Selles kirjes esitatakse kasutatava väljana ka dimensiooni nimi, kui seda on valimiseks vaja.  
59. Rippdialoogi avamiseks klõpsake valikut Uus.
60. Tippige Kood väljale Nimi.
61. Valige väljalt Kaubakood suvand String.
62. Klõpsake vahekaarti Lisa.
63. Rippdialoogi avamiseks klõpsake valikut Uus.
64. Sisestage väljale Nimi suvand Kirjeldus.
65. Klõpsake vahekaarti Lisa.
66. Rippdialoogi avamiseks klõpsake valikut Uus.
67. Sisestage väljale Nimi suvand Nimi.
68. Klõpsake vahekaarti Lisa.
69. Klõpsake nuppu Salvesta.
70. Sulgege leht.

![ER-i andmemudeli kujundaja leht.](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
