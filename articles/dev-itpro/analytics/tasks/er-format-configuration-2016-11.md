--- 
title: Elektroonilise aruandluse (ER) vormingukonfiguratsiooni loomine
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a>Elektroonilise aruandluse (ER) vormingukonfiguratsiooni loomine

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad vormindada konfiguratsiooni elektroonilise aruandluse (ER) puhul. See vormingu konfiguratsioon määrab elektrooniliste dokumentide vormingu, mida maksete töötlemisel kasutatakse. Selles näites loote vormingu konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide lõpuleviimiseks peate kõigepealt läbima etapid protseduuris Andmemudeli vastendamine valitud andmeallikatega.


## <a name="create-a-new-format-configuration"></a>Uue vormingu konfiguratsiooni loomine
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Valige puul suvand Maksed (lihtsustatud mudel).
4. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
5. Sisestage väljale Uus suvand Andmemudelil PaymentModel põhinev vorming.
6. Sisestage väljale Nimi suvand BACS (UK fiktiivne).
    * BACS (UK fiktiivne)  
7. Sisestage väljale Kirjeldus suvand BACS-i hankija maksevorming (UK fiktiivne).
    * BACS-i hankija maksevorming (UK fiktiivne)  
    * Aktiivne konfiguratsiooni pakkuja sisestatakse siia automaatselt. See pakkuja saab seda konfiguratsiooni hallata. Muud pakkujad saavad seda konfiguratsiooni kasutada, kuid ei saa seda hallata.  
    * Määratleda saab elektroonilise dokumendi kindla vormingu. Jätke see väli tühjaks, kui soovite valida vormingu käitusajal.  
8. Sisestage või valige väärtus väljal Andmemudeli definitsioon.
9. Klõpsake Loo konfiguratsioon.
    * Uus konfiguratsioon on loodud. Mustandversiooni saab kasutada vormingu kujunduse salvestamiseks elektrooniliste dokumentide haldamise puhul.  

## <a name="design-format-of-electronic-document"></a>Elektroonilise dokumendi vormingu kujundus
1. Klõpsake valikut Kujundaja.
2. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
3. Valige puul suvand Common\File.
4. Sisestage väljale Nimi suvand XML.
    * Xml  
5. Sisestage väljale Kodeerimine suvand UTF-8.
    * UTF-8  
6. Klõpsake nuppu OK.
7. Klõpsake valikut Lisa rippdialoogi avamiseks.
8. Valige puul suvand XML\Element.
9. Sisestage väljale Nimi suvand Teade.
    * Teade  
10. Klõpsake nuppu OK.
11. Puuvaates valige „Xml\Teade”
12. Klõpsake käsku Lisa element.
13. Sisestage väljale Nimi suvand ProcessingDate.
    * ProcessingDate  
14. Klõpsake nuppu OK.
15. Klõpsake käsku Lisa element.
16. Sisestage väljale Nimi suvand MessageId.
    * MessageId  
17. Klõpsake nuppu OK.
18. Klõpsake käsku Lisa element.
19. Sisestage väljale Nimi suvand Maksed.
    * Maksed  
20. Klõpsake nuppu OK.
21. Puuvaates valige „Xml\Teade\Maksed”.
22. Klõpsake käsku Lisa element.
23. Sisestage väljale Nimi suvand Kaup.
    * Kaup  
24. Klõpsake nuppu OK.
25. Puuvaates valige „Xml\Teade\Maksed\Kaup”.
26. Klõpsake valikut Lisa rippdialoogi avamiseks.
27. Valige puul suvand XML\Attribute.
28. Sisestage väljale Nimi suvand Id.
    * ID  
29. Klõpsake nuppu OK.
30. Klõpsake valikut Lisa rippdialoogi avamiseks.
31. Valige puul suvand XML\Element.
32. Sisestage väljale Nimi suvand Hankija.
    * Tarnija  
33. Klõpsake nuppu OK.
34. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija”.
35. Klõpsake käsku Lisa element.
36. Sisestage väljale Nimi suvand Nimi.
    * Nimi  
37. Klõpsake nuppu OK.
38. Klõpsake käsku Lisa element.
39. Sisestage väljale Nimi suvand Pank.
    * Pank  
40. Klõpsake nuppu OK.
41. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank”.
42. Klõpsake käsku Lisa element.
43. Sisestage väljale Nimi suvand RoutingNumber.
    * RoutingNumber  
44. Klõpsake nuppu OK.
45. Klõpsake käsku Lisa element.
46. Sisestage väljale Nimi suvand AccountNumber.
    * AccountNumber  
47. Klõpsake nuppu OK.
48. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija”.
49. Klõpsake käsku Kopeeri.
50. Puuvaates valige „Xml\Teade\Maksed\Kaup”.
51. Klõpsake käsku Kleebi.
52. Sisestage väljale Nimi suvand Maksja.
    * Maksja  
53. Puuvaates valige „Xml\Teade\Maksed\Kaup”.
54. Klõpsake käsku Lisa element.
55. Sisestage väljale Nimi suvand Valuuta.
    * Valuuta  
56. Klõpsake nuppu OK.
57. Klõpsake käsku Lisa element.
58. Sisestage väljale Nimi suvand Kirjeldus.
    * Kirjeldus  
59. Klõpsake nuppu OK.
60. Klõpsake käsku Lisa element.
61. Sisestage väljale Nimi suvand TransDate.
    * TransDate  
62. Klõpsake nuppu OK.
63. Klõpsake käsku Lisa element.
64. Sisestage väljale Nimi suvand Summa.
    * Summa  
65. Klõpsake nuppu OK.

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a>Vormingu komponentide ettevalmistamine andmemudeli elementidega vastendamiseks
1. Puuvaates valige „Xml\Teade\ProcessingDate”.
2. Klõpsake valikut Lisa rippdialoogi avamiseks.
3. Puuvaates valige „Tekst\DateTime”.
4. Sisestage väljale Vorming suvand aaaa-KK-pp.
    * aaaa-KK-pp  
5. Klõpsake nuppu OK.
6. Puuvaates valige „Xml\Teade\Maksed\Kaup\TransDate”
7. Klõpsake valikut Add DateTime.
8. Sisestage väljale Vorming suvand aaaa-KK-pp.
    * aaaa-KK-pp  
9. Tüübi väljal DateTime valige „Kuupäev”.
10. Klõpsake nuppu OK.
11. Puuvaates valige „Xml\Teade\MessageId”
12. Klõpsake valikut Lisa rippdialoogi avamiseks.
13. Valige puul suvand Tekst\String.
14. Klõpsake nuppu OK.
15. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Nimi”.
16. Klõpsake käsku Lisa string.
17. Klõpsake nuppu OK.
18. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\RoutingNumber”.
19. Klõpsake käsku Lisa string.
20. Klõpsake nuppu OK.
21. Puuvaates valige „Xml\Teade\Maksed\Kaup\Hankija\Pank\AccountNumber”.
22. Klõpsake käsku Lisa string.
23. Klõpsake nuppu OK.
24. Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksed\Nimi”.
25. Klõpsake käsku Lisa string.
26. Klõpsake nuppu OK.
27. Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\RoutingNumber”.
28. Klõpsake käsku Lisa string.
29. Klõpsake nuppu OK.
30. Puuvaates valige „Xml\Teade\Maksed\Kaup\Maksja\Pank\AccountNumber”.
31. Klõpsake käsku Lisa string.
32. Klõpsake nuppu OK.
33. Puuvaates valige „Xml\Teade\Maksed\Kaup\Valuuta”.
34. Klõpsake käsku Lisa string.
35. Klõpsake nuppu OK.
36. Puuvaates valige „Xml\Teade\Maksed\Kaup\Kirjeldus”.
37. Klõpsake käsku Lisa string.
38. Klõpsake nuppu OK.
39. Puuvaates valige „Xml\Teade\Maksed\Kaup\Summa”.
40. Klõpsake käsku Lisa string.
41. Klõpsake nuppu OK.
42. Klõpsake nuppu Salvesta.
43. Sulgege leht.


