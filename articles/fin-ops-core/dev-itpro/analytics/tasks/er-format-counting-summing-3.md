---
title: Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa – arvutuste kasutamine väljundi koostamiseks)
description: See artikkel kirjeldab, kuidas konfigureerida elektroonilise aruandluse vormingut nii, et loendamine ja summeerimine põhineb juba loodud tekstiväljundi andmetel. (3. osa)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 82a0a404467ff73260ea9725fc0e79ff09833f41
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881422"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a>Elektrooniline aruandlus. Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa – arvutuste kasutamine väljundi koostamiseks)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (2. osa: arvutuste konfigureerimine)”.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="configure-this-report-to-use-counting-and-summing-info"></a>Selle aruande konfigureerimine loendamise ja liitmise teabe kasutamiseks
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Laiendage puul valikut Intrastati mudel.
4. Laiendage puul valikut Intrastati mudel \ Intrastat (DE).
5. Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.
6. Klõpsake valikut Kujundaja.
7. Klõpsake vahekaarti Vastendus.
8. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
    * Lisage uus andmeallikas meelde jäetud plokkide loendi saamiseks.  
9. Valige puul suvand Funktsioonid\arvutatud väli.
10. Tippige $BlocksList väljale Nimi.
    * $BlocksList  
11. Klõpsake suvandit Muuda valemit.
12. Valige puult Andmekogumi funktsioonid \ COLLECTEDLIST.
13. Klõpsake suvandit Funktsiooni lisamine.
14. Klõpsake suvandit Andmeallika lisamine.
15. Sisestage väljale Valem COLLECTEDLIST('$BlockName', .
    * COLLECTEDLIST('$BlockName',  
16. Sisestage väljale Valem COLLECTEDLIST('$BlockName', "*").
    * COLLECTEDLIST('$BlockName', "*")  
17. Klõpsake nuppu Salvesta.
    * Muster „*” tähendab, et kõik plokid lisatakse selle kirje loendisse.  
18. Sulgege leht.
19. Klõpsake nuppu OK.
20. Klõpsake vahekaarti Vorming.
21. Tehke puul valik Intrastat \ Andmed.
22. Klõpsake valikut Lisa rippdialoogi avamiseks.
23. Valige puult Tekst \ Seeria.
24. Tippige väljale Nimi valik Kogusummad plokkide alusel.
    * Kogusummad plokkide alusel  
25. Valige väljal Erimärgid Uus rida – Windows (CR LF).
26. Klõpsake nuppu OK.
27. Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel.
28. Klõpsake valikut Lisa rippdialoogi avamiseks.
29. Valige puul suvand Tekst\String.
30. Tippige Ploki kood väljale Nimi.
    * Ploki kood  
31. Klõpsake nuppu OK.
32. Klõpsake käsku Lisa string.
33. Tippige väljale Nimi valik Ridade loendamine.
    * Ridade loendamine  
34. Klõpsake nuppu OK.
35. Klõpsake käsku Lisa string.
36. Tippige väljale Nimi valik Kogusumma.
    * Kogusumma  
37. Klõpsake nuppu OK.
38. Klõpsake vahekaarti Vastendus.
39. Valige puul väärtus $BlocksList.
40. Klõpsake valikut Seo.
    * Looge iga meelde jäetud ploki kohta kokkuvõtte rida.  
41. Klõpsake vahekaarti Vorming.
42. Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ploki kood.
43. Klõpsake vahekaarti Vastendus.
44. Klõpsake suvandit Muuda valemit.
45. Sisestage väljale Valem tekst „"Block id: " & “.
    * "Block id: " &  
46. Laiendage puul väärtust $BlocksList.
47. Valige puult $BlocksList\Väärtus.
48. Klõpsake suvandit Andmeallika lisamine.
49. Klõpsake nuppu Salvesta.
50. Sulgege leht.
51. Klõpsake vahekaarti Vorming.
52. Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Ridade loendamine.
53. Klõpsake vahekaarti Vastendus.
54. Klõpsake suvandit Muuda valemit.
    * Looge iga selles aruandes esitatud ploki ridade arvu kohta väljund.  
55. Sisestage väljale Valem „"Number of lines in this block: " & ”.
    * "Number of lines in this block: " &  
56. Sisestage väljale Valem "Number of lines in this block: " & TEXT(.
    * "Number of lines in this block: " & TEXT(  
57. Valige puult Andmekogumi funktsioonid \ COUNTIFS'.
58. Klõpsake suvandit Funktsiooni lisamine.
59. Klõpsake suvandit Andmeallika lisamine.
60. Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',  
61. Laiendage puul väärtust $BlocksList.
62. Valige puult $BlocksList\Väärtus.
63. Klõpsake suvandit Andmeallika lisamine.
64. Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,  
65. Valige puul väärtus $RecName.
66. Klõpsake suvandit Andmeallika lisamine.
67. Sisestage väljale Valem "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*")).
    * "Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
68. Klõpsake nuppu Salvesta.
69. Sulgege leht.
70. Klõpsake vahekaarti Vorming.
71. Valige puult Intrastat \ Andmed \ Kogusummad plokkide alusel \ Kogusumma.
72. Klõpsake vahekaarti Vastendus.
73. Klõpsake suvandit Muuda valemit.
    * Looge väljund, mis on iga selles aruandes esitatud ploki arveldatud summa koguväärtus.  
74. Sisestage väljale Valem "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*")).
    * "Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "*"))  
75. Klõpsake nuppu Salvesta.
76. Sulgege leht.
77. Klõpsake nuppu Salvesta.
78. Sulgege leht.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]