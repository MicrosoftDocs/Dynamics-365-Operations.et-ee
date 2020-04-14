---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa – arvutuste konfigureerimine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20188438a4ca623fc926e6c373fb002f148c3df4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142474"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a>Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa – arvutuste konfigureerimine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (1. osa: vormingu loomine)”.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a>Vormingukonfiguratsiooni loomine loendamise ja liitmise üksikasjade lisamiseks
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Laiendage puul valikut Intrastati mudel.
4. Valige puult Intrastati mudel \ Intrastat (DE).
    * Oletame, et teil on vaja kohandada Microsofti antud vormingut, lisades intrastati aruande lõppu ridu kokkuvõtte andmetega. Muudatuste tegemiseks tuleb seda teha, tuletades oma intrastati konfiguratsiooni eksemplari Microsofti eksemplarist.  
5. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
6. Sisestage väljale Uus üksus Tuleta nimest: intrastat (DE), Microsoft.
7. Tippige väljale Nimi tekst „Intrastat (DE) koos loendamise ja liitmisega“.
8. Klõpsake Loo konfiguratsioon.

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a>Saate konfigureerida selle aruande nii, et loendamine ja liitmine toimub väljundi andmete põhjal
1. Klõpsake valikut Kujundaja.
2. Tehke väljal Kogu väljundi üksikasjad valik Jah.
    * See lipp aktiveerib käitusajal väljundi üksikasjade kogumise protsessi intrastati faili loomiseks.  
    * Loendamine peab toimuma erinevate Intrastati suundade kohta, seega lisage spetsiaalne mudeli loetelu selle vormingukonfiguratsiooni andmeallikate loendile.  
3. Klõpsake vahekaarti Vastendus.
4. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
5. Valige puul väärtus Andmemudel \ Loetelu.
6. Tippige Suund väljale Nimi.
7. Sisestage või valige väärtus väljal Mudeli loetelu.
    * Valige väärtuseks Suund.  
8. Klõpsake nuppu OK.
9. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
10. Valige puul suvand Funktsioonid\arvutatud väli.
11. Tippige $BlockName väljale Nimi.
12. Klõpsake suvandit Muuda valemit.
13. Sisestage „plokk” väljale Valem.
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
16. Klõpsake nuppu OK.
17. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
18. Valige puul suvand Funktsioonid\arvutatud väli.
19. Tippige $RecName väljale Nimi.
20. Klõpsake suvandit Muuda valemit.
21. Sisestage „kirje” väljale Valem.
22. Klõpsake nuppu Salvesta.
23. Sulgege leht.
24. Klõpsake nuppu OK.
25. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
26. Valige puul suvand Funktsioonid\arvutatud väli.
27. Tippige $InvName väljale Nimi.
28. Klõpsake suvandit Muuda valemit.
29. Sisestage „InvoicedAmountEUR” väljale Valem.
30. Klõpsake nuppu Salvesta.
31. Sulgege leht.
32. Klõpsake nuppu OK.
33. Tehke puul valik Intrastat \ Andmed.
34. Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri
35. Klõpsake suvandit Andmeallika lisamine.
    * $BlockName  
36. Klõpsake nuppu Salvesta.
37. Sulgege leht.
38. Klõpsake välja Kogutud andmete võtme väärtus nuppu Redigeeri.
39. Sisestage väljale valem IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export").
    * IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")  
40. Klõpsake nuppu Salvesta.
41. Sulgege leht.
    * Loendage selle järjestuse ridade arv. Tulemusi kasutatakse nimega „plokk” erinevate suundade puhul eraldi. Väärtust „Import” kasutatakse igasuguste intrastati saabumiskannete puhul. Väärtust „Eksport” kasutatakse igasuguste intrastati lähetuskannete puhul. Vaadake seda kui virtuaalset Exceli arvutustabelit. Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport”.  
42. Laiendage puul valikut Intrastat \ Andmed: seeria.
43. Valige puult Intrastat \ Andmed: seeria \ Saabumised?.
44. Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.
    * Loendage selle järjestuse ridade arv. Tulemused jäetakse meelde, kasutades nime „kirje”.  
45. Valige puul väärtus $RecName.
46. Klõpsake suvandit Andmeallika lisamine.
47. Klõpsake nuppu Salvesta.
48. Sulgege leht.
49. Klõpsake välja „Kogutud andmete võtme väärtus ”nuppu Redigeeri
50. Sisestage väljale Valem Intrastat.CommodityRecord.CommodityCode.
51. Klõpsake nuppu Salvesta.
52. Sulgege leht.
    * Loendage selle järjestuse ridade arv. Tulemusi kasutatakse nimega „kirje” erinevate kaubakoodide puhul eraldi. Vaadake seda kui virtuaalset Exceli arvutustabelit. Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport” ja teine plokk „kirje” täidetakse kaubakoodi väärtusega.  
53. Valige puult Intrastat \ Andmed: seeria \ Lähetused?.
54. Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri
55. Valige puul väärtus $RecName.
56. Klõpsake suvandit Andmeallika lisamine.
57. Klõpsake nuppu Salvesta.
58. Sulgege leht.
59. Klõpsake välja „Kogutud andmete võtme väärtus” nuppu Redigeeri.
60. Sisestage väljale Valem Intrastat.CommodityRecord.CommodityCode.
61. Klõpsake nuppu Salvesta.
62. Sulgege leht.
63. Laiendage puul valikut Intrastat \ Andmed: seeria \ Lähetused: seeria?.
64. Laiendage puul valikut Intrastat \ Andmed: seeria \ Lähetused: seeria? \ Kirje =  Intrastat.CommodityRecord.
65. Klõpsake vahekaarti Vorming.
66. Valige puult Intrastat \ Andmed \ Lähetused \ Kirje \ Arve summa EUR.
67. Klõpsake vahekaarti Vastendus.
68. Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.
69. Valige puul väärtus $InvName.
70. Klõpsake suvandit Andmeallika lisamine.
71. Klõpsake nuppu Salvesta.
72. Sulgege leht.
    * Liitke selle järjestuse ridade arveldatud summade väärtused. Tulemusi kasutatakse nimega „InvoicedAmountEUR” erinevate intrastati suundade ja kaubakoodide puhul eraldi. Vaadake seda kui virtuaalset loomingut Exceli arvutustabelis. Iga kande puhul täidetakse rida, mille esimene veerg on „plokk”, vastavalt väärtustega „Import” ja „Eksport”. Teine plokk „kirje” täidetakse kaubakoodi väärtusega ja kolmas veerg „InvoicedAmountEUR” täidetakse arve summa väärtusega.  
73. Laiendage puul valikut Intrastat \ Andmed \ Saabumised?.
74. Laiendage puul valikut Intrastat \ Andmed \ Saabumised? \ Kirje =  Intrastat.CommodityRecord.
75. Klõpsake vahekaarti Vorming.
76. Valige puult Intrastat \ Andmed \ Saabumised \ Kirje \ Arve summa EUR.
77. Klõpsake vahekaarti Vastendus.
78. Klõpsake välja „Kogutud andmete võtme nimi” nuppu Redigeeri.
79. Valige puul väärtus $InvName.
80. Klõpsake suvandit Andmeallika lisamine.
81. Klõpsake nuppu Salvesta.
82. Sulgege leht.
83. Klõpsake nuppu Salvesta.
84. Sulgege leht.

