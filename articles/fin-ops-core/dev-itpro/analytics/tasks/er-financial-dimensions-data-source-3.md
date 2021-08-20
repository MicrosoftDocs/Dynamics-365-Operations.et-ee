---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) mudelit kasutama finantsdimensioone andmeallikana ER-i aruannetele. (3. osa)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 548eec45739a52d4eb168a80660540196225b2ed482d2104a4cd0d00503109dd
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6773784"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a>Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (3. osa – aruande koostamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpule viimiseks peate esmalt viima lõpule etapid protseduuris „Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine)”.


## <a name="design-a-report-to-present-financial-dimensions"></a>Aruande koostamine finantsdimensioonide esitamiseks
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Valige puult Finantsdimensioonide näidismudel.
3. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
4. Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.
    * Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.  
5. Tippige väljale Nimi tekst Pearaamatu töölehe aruanne.
6. Tehke väljal Andmemudeli definitsioon valik Kirje.
7. Klõpsake Loo konfiguratsioon.
8. Klõpsake valikut Kujundaja.
9. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
10. Valige puul suvand XML\Element.
11. Tippige Juur väljale Nimi.
12. Klõpsake nuppu OK.
13. Klõpsake valikut Lisa rippdialoogi avamiseks.
14. Valige puul suvand XML\Attribute.
15. Sisestage väljale Nimi suvand Ettevõte.
16. Klõpsake nuppu OK.
17. Klõpsake valikut Lisa rippdialoogi avamiseks.
18. Valige puul suvand XML\Element.
19. Tippige Tööleht väljale Nimi.
20. Klõpsake nuppu OK.
21. Valige puult Juur: XML-element \ Tööleht: XML-element.
22. Klõpsake valikut Lisa rippdialoogi avamiseks.
23. Valige puul suvand XML\Attribute.
24. Tippige Partii väljale Nimi.
25. Klõpsake nuppu OK.
26. Klõpsake valikut Lisa rippdialoogi avamiseks.
27. Valige puul suvand XML\Element.
28. Tippige väljale Nimi valik Kanne.
29. Klõpsake nuppu OK.
30. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.
31. Klõpsake valikut Lisa rippdialoogi avamiseks.
32. Valige puul suvand XML\Attribute.
33. Tippige Kanne väljale Nimi.
34. Klõpsake nuppu OK.
35. Klõpsake valikut Lisa atribuut.
36. Tippige Kuupäev väljale Nimi.
37. Klõpsake nuppu OK.
38. Klõpsake valikut Lisa atribuut.
39. Sisestage väljale Nimi suvand Valuuta.
40. Klõpsake nuppu OK.
41. Klõpsake valikut Lisa atribuut.
42. Tippige Dt väljale Nimi.
43. Klõpsake nuppu OK.
44. Klõpsake valikut Lisa atribuut.
45. Tippige Ct väljale Nimi.
46. Klõpsake nuppu OK.
47. Klõpsake valikut Lisa rippdialoogi avamiseks.
48. Valige puul suvand XML\Element.
49. Tippige Dimensioonid väljale Nimi.
50. Klõpsake nuppu OK.
51. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.
52. Klõpsake valikut Lisa rippdialoogi avamiseks.
53. Valige puul suvand XML\Attribute.
54. Tippige Kood väljale Nimi.
55. Klõpsake nuppu OK.
56. Klõpsake valikut Lisa atribuut.
57. Tippige Väärtus väljale Nimi.
58. Klõpsake nuppu OK.
59. Klõpsake valikut Lisa atribuut.
60. Tippige Desc väljale Nimi.
61. Klõpsake nuppu OK.
![ER-i toimingute koostaja leht.](../media/er-financial-dimensions-guides-format1.png)

## <a name="map-report-elements-to-data-sources"></a>Aruande elementide vastendamine andmeallikatega
1. Klõpsake vahekaarti Vastendus.
2. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.
3. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.
4. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.
5. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.
6. Valige puult Juur: XM-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Desc: XML-atribuut.
7. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kirjeldus: string.
8. Klõpsake valikut Seo.
9. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Väärtus: XML-atribuut.
10. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.
11. Klõpsake valikut Seo.
12. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element \ Kood: XML-atribuut.
13. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Nimi: string.
14. Klõpsake valikut Seo.
15. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.
16. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dimensioonid: XML-element.
17. Klõpsake valikut Seo.
18. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Ct: XML-atribuut.
19. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.
20. Klõpsake valikut Seo.
21. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Dt: XML-atribuut.
22. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.
23. Klõpsake valikut Seo.
24. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Valuuta: XML-atribuut.
25. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.
26. Klõpsake valikut Seo.
27. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kuupäev: XML-atribuut.
28. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.
29. Klõpsake valikut Seo.
30. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element \ Kanne: XML-atribuut.
31. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.
32. Klõpsake valikut Seo.
33. Valige puult Juur: XML-element \ Tööleht: XML-element \ Kanne: XML-element.
34. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.
35. Klõpsake valikut Seo.
36. Valige puult Juur: XML-element \ Tööleht: XML-element \ Partii: XML-atribuut.
37. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.
38. Klõpsake valikut Seo.
39. Valige puult Juur: XML-element \ Tööleht: XML-element.
40. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.
41. Klõpsake valikut Seo.
42. Valige puult Juur: XML-element \ Ettevõte: XML-atribuut.
43. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.
44. Klõpsake valikut Seo.
45. Klõpsake nuppu Salvesta.
46. Sulgege leht.
![ER-i toimingute koostaja leht.](../media/er-financial-dimensions-guides-format2.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]