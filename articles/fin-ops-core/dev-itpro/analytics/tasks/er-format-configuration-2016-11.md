---
title: Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)
description: Selles teemas kirjeldatakse, kuidas rollis „Süsteemi administraator“ või „Elektroonilise aruandluse arendaja“ olev kasutaja saab luua elektroonilise aruandluse (ER) vormingu seadistuse.
author: NickSelin
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1fd41b1724eb2e0405c0e7a7e0ff0aea4a945e0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184941"
---
# <a name="er-create-a-format-configuration-november-2016"></a>Elektrooniline aruandlus. Vormingu konfiguratsiooni loomine (november 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Selles teemas kirjeldatakse, kuidas rollis „Süsteemi administraator“ või „Elektroonilise aruandluse arendaja“ olev kasutaja saab luua elektroonilise aruandluse (ER) vormingu seadistuse. See vormingu konfiguratsioon määrab elektrooniliste dokumentide vormingu, mida maksete töötlemisel kasutatakse. Selles näites loote vormingu konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Andmemudeli vastendamine valitud andmeallikatega.


## <a name="create-a-new-format-configuration"></a>Uue vormingu konfiguratsiooni loomine
1. Avage **Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus**.
2. Klõpsake valikut **Aruandluse konfiguratsioonid**.
3. Valige puul suvand **Maksed (lihtsustatud mudel)**.
4. Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.

 > [!NOTE]
 > Kui te ei näe valikut **Loo konfiguratsioon**, peate lubama kujundusrežiimi lehel **Elektroonilise aruandluse parameetrid**. 
 
5. Sisestage väljale **Uus suvand** **Andmemudelil PaymentModel põhinev vorming**.
6. Sisestage väljale **Nimi** suvand **BACS (UK fiktiivne)**.
7. Sisestage väljale **Kirjeldus** suvand **BACS-i hankija maksevorming (UK fiktiivne)**.
    * Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt. See pakkuja saab seda konfiguratsiooni hallata. Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.  
    * Määratleda saab elektroonilise dokumendi kindla vormingu. Jätke see väli tühjaks, kui soovite valida vormingu käitusajal.  
8. Sisestage või valige väärtus väljal **Andmemudeli definitsioon**.
9. Klõpsake **Loo konfiguratsioon**. Uus konfiguratsioon on loodud. Mustandversiooni saab kasutada vormingu kujunduse salvestamiseks elektrooniliste dokumentide haldamise puhul.  

## <a name="design-the-format-of-an-electronic-document"></a>Elektroonilise dokumendi vormingu kujundus
1. Klõpsake valikut **Kujundaja**.
2. Klõpsake suvandit **Lisa juur** rippdialoogi avamiseks.
3. Valige puul suvand **Üldine\Fail**.
4. Sisestage väljale **Nimi** suvand **Xml**.
5. Sisestage väljale **Kodeerimine** suvand **UTF-8**.
6. Klõpsake nupul **OK**.
7. Klõpsake vahekaarti **Lisa**.
8. Valige puul suvand **XML\Element**.
9. Sisestage väljale **Nimi** suvand **Teade**.
10. Klõpsake nupul **OK**.
11. Puuvaates valige **Xml\Teade**.
12. Klõpsake käsku **Lisa element**.
13. Sisestage väljale **Nimi** suvand **Töötlemiskuupäev**.
14. Klõpsake nupul **OK**.
15. Klõpsake käsku **Lisa element**.
16. Sisestage väljale Nimi suvand **TeateId**.
17. Klõpsake nupul **OK**.
18. Klõpsake käsku **Lisa element**.
19. Sisestage väljale **Nimi** suvand **Maksed**.
20. Klõpsake nupul **OK**.
21. Puuvaates valige **Xml\Teade\Maksed**.
22. Klõpsake käsku **Lisa element**.
23. Sisestage väljale **Nimi** suvand **Kaup**.
24. Klõpsake nupul **OK**.
25. Puuvaates valige **Xml\Teade\Maksed\Kaup**.
26. Klõpsake vahekaarti **Lisa**.
27. Valige puul suvand **XML\Atribuut**.
28. Sisestage väljale Nimi suvand **Id**.
29. Klõpsake nupul **OK**.
30. Klõpsake vahekaarti **Lisa**.
31. Valige puul suvand **XML\Element**.
32. Sisestage väljale Nimi suvand **Hankija**.
33. Klõpsake nupul **OK**.
34. Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija**.
35. Klõpsake käsku **Lisa element**.
36. Sisestage väljale Nimi suvand **Nimi**.
37. Klõpsake nupul **OK**.
38. Klõpsake käsku **Lisa element**.
39. Sisestage väljale **Nimi** suvand **Pank**.
40. Klõpsake nupul **OK**.
41. Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank**.
42. Klõpsake käsku **Lisa element**.
43. Sisestage väljale **Nimi** suvand **Marsruudinumber**.
44. Klõpsake nupul **OK**.
45. Klõpsake käsku **Lisa element**.
46. Sisestage väljale **Nimi** suvand **Kontonumber**.
47. Klõpsake nupul **OK**.
48. Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija**.
49. Klõpsake käsku **Kopeeri**.
50. Puuvaates valige **Xml\Teade\Maksed\Kaup**.
51. Klõpsake käsku **Kleebi**.
52. Sisestage väljale **Nimi** suvand **Maksja**.
53. Puuvaates valige **Xml\Teade\Maksed\Kaup**.
54. Klõpsake käsku **Lisa element**.
55. Sisestage väljale **Nimi** suvand **Valuuta**.
56. Klõpsake nupul **OK**.
57. Klõpsake käsku **Lisa element**.
58. Sisestage väljale **Nimi** suvand **Kirjeldus**.
59. Klõpsake nupul **OK**.
60. Klõpsake käsku **Lisa element**.
61. Sisestage väljale Nimi suvand **Transkuupäev**.
62. Klõpsake nupul **OK**.
63. Klõpsake käsku **Lisa element**.
64. Sisestage väljale Nimi suvand **Summa**.
65. Klõpsake nupul **OK**.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Vormingu komponentide ettevalmistamine andmemudeli elementidega vastendamiseks
1. Puuvaates valige **Xml\Teade\Töötlemiskuupäev**.
2. Klõpsake valikut **Lisa** rippdialoogi avamiseks.
3. Puuvaates valige **Tekst\Kuupäev**”.
4. Sisestage väljale **Vorming** suvand **aaaa-kk-pp**.
5. Klõpsake nupul **OK**.
6. Puuvaates valige **Xml\Teade\Maksed\Kaup\Transkuupäev**”
7. Klõpsake valikut **Lisa kuupäev**.
8. Sisestage väljale **Vorming** suvand **aaaa-kk-pp**.
9. Väljal **Kuupäev** valige **Kuupäev**.
10. Klõpsake nupul **OK**.
11. Puuvaates valige **Xml\Teade\TeateId**.
12. Klõpsake valikut **Lisa** rippdialoogi avamiseks.
13. Valige puul suvand **Tekst\String**.
14. Klõpsake nupul **OK**.
15. Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Nimi**.
16. Klõpsake käsku **Lisa string**.
17. Klõpsake nupul **OK**.
18. Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank\Marsruudinumber**.
19. Klõpsake käsku **Lisa string**.
20. Klõpsake nupul **OK**.
21. Puuvaates valige **Xml\Teade\Maksed\Kaup\Hankija\Pank\Kontonumber**.
22. Klõpsake käsku **Lisa string**.
23. Klõpsake nupul **OK**.
24. Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksed\Nimi**.
25. Klõpsake käsku **Lisa string**.
26. Klõpsake nupul **OK**.
27. Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksja\Pank\Marsruudinumber**.
28. Klõpsake käsku **Lisa string**.
29. Klõpsake nupul **OK**.
30. Puuvaates valige **Xml\Teade\Maksed\Kaup\Maksja\Pank\Kontonumber**.
31. Klõpsake käsku **Lisa string**.
32. Klõpsake nupul **OK**.
33. Puuvaates valige **Xml\Teade\Maksed\Kaup\Valuuta**.
34. Klõpsake käsku **Lisa string**.
35. Klõpsake nupul **OK**.
36. Puuvaates valige **Xml\Teade\Maksed\Kaup\Kirjeldus**.
37. Klõpsake käsku **Lisa string**.
38. Klõpsake nupul **OK**.
39. Puuvaates valige **Xml\Teade\Maksed\Kaup\Summa**.
40. Klõpsake käsku **Lisa string**.
41. Klõpsake nupul **OK**.
42. Klõpsake nuppu **Salvesta**.
43. Sulgege leht.

