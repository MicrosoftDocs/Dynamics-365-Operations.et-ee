--- 
title: Elektroonilise aruandluse (ER) mudeli muutmine ja vastendamine avalduse andmete uuendamisega dokumentide genereerimiseks
description: "Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa – dokumentide genereerimine)“."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 5549534700360776ad409c2324a4d84bcde005f9
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) mudeli muutmine ja vastendamine avalduse andmete uuendamisega dokumentide genereerimiseks

[!include[task guide banner](../../includes/task-guide-banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (2. osa: dokumentide genereerimine)“. 

Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks. Käesolevas näites muudate ER konfiguratsioone, et hakata neid kasutama elektrooniliste dokumentide loomiseks avalduse andmete uuendamiseks. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.


## <a name="modify-data-model"></a>Andmemudeli muutmine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Tehke puul valik „Intrastat (model)".
    * Saate laiendada andmemudeli kasutamisviisi. Lisaks selle kasutamisele andmeallikana Intrastat-aruande loomiseks, kasutatakse andmemudelit üksikasjade kogumiseks Intrastat-aruandluse protsessi kohta. Üksikasju kasutatakse seejärel avalduse andmete uuendamiseks.   
3. Klõpsake valikut Kujundaja.
4. Rippdialoogi avamiseks klõpsake valikut Uus.
5. Väljale Uus sõlm kui sisestage „Mudeli juur”.
6. Tippige nime väljale tekst „For application data update".
    * Avalduse andmete uuendamiseks  
7. Klõpsake vahekaarti Lisa.
8. Tehke puul valik „For application data update".
    * See uus juurkaup lisatakse andmevoo määramiseks andmete teisaldamise jaoks Intrastat-aruandest (kasutatakse andmeallikana) avalduse tabelitesse (uuenduse sihtkoht). Pange tähele, et väljaminevasse dokumenti sisestatud andmete ja avalduse andmete uuendamiseks kasutatavast dokumendist andmete hankimiseks tuleb kasutada erinevaid juurkaupu.   
9. Rippdialoogi avamiseks klõpsake valikut Uus.
10. Sisestage nimeväljale Arhiivi päis.
    * Arhiivi päis  
11. Valige väljalt Kaubakood suvand Kirjete loend.
12. Klõpsake vahekaarti Lisa.
    * Kuna te loote kirje iga genereeritud Intrastat-aruande jaoks, peate looma selleks uue kauba.  
13. Rippdialoogi avamiseks klõpsake valikut Uus.
14. Tippige Faili nimi väljale Nimi.
    * Faili nimi  
15. Valige väljalt Kaubakood suvand String.
16. Klõpsake vahekaarti Lisa.
17. Rippdialoogi avamiseks klõpsake valikut Uus.
18. Sisestage nimeväljale tekst „Ridade arv".
    * Ridade arv  
19. Valige väljalt Kaubakood suvand DateTime.
20. Klõpsake vahekaarti Lisa.
    * Lisage see kaup nende Intrastat-kannete arvu tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.  
21. Rippdialoogi avamiseks klõpsake valikut Uus.
22. Sisestage nimeväljale „Arhiiviread".
    * Arhiiviread  
23. Valige väljalt Kaubakood suvand Kirjete loend.
24. Klõpsake vahekaarti Lisa.
    * Lisage see kaup selle Intrastat-kannete loendi tähistamiseks, mis kinnitati praeguse aruandlusprotsessi käigus.  
25. Rippdialoogi avamiseks klõpsake valikut Uus.
26. Sisestage väljale Nimi suvand Summa.
    * Summa  
27. Valige väljalt Kaubakood suvand Tegelik.
28. Klõpsake vahekaarti Lisa.
29. Rippdialoogi avamiseks klõpsake valikut Uus.
30. Sisestage nimeväljale valik „Commodity rec id”.
    * Kaubakirje ID  
31. Valige väljalt Kaubatüüp suvand Int64.
32. Klõpsake vahekaarti Lisa.
33. Rippdialoogi avamiseks klõpsake valikut Uus.
34. Sisestage nimeväljale tekst „Kaubakood”.
    * Kaubakood  
35. Valige väljalt Kaubakood suvand String.
36. Klõpsake vahekaarti Lisa.
37. Klõpsake nuppu Salvesta.
38. Sulgege leht.

## <a name="modify-model-mapping"></a>Mudelivastenduse muutmine
1. Laiendage puul valikut „Intrastat (model)".
2. Tehke puul valik „Intrastat (model)\Intrastat (mapping)".
    * Muutke olemasolevat mudelivastendust, et hakata seda kasutama avalduse andmete uuendamiseks ja Intrastat-aruande üksikasjade arhiivimiseks.  
3. Klõpsake valikut Kujundaja.
4. Klõpsake valikut Uus.
5. Sisestage nimeväljale „Uuenda arhiiv".
    * Arhiivi uuendamine  
6. Tehke suunaväljal valik „To destination".
7. Klõpsake nuppu Salvesta.
    * See uus vastendus määrab andmevoo andmete (Intrastat-aruande üksikasjad) teisaldamiseks andmemudelist avalduse tabelitesse (uuenduse sihtkoht). Pange tähele, et aruandlusprotsessi jaoks avaldusest hangitavate andmete ja andmemudeli andmete kasutamiseks avalduse andmete uuenduse jaoks tuleb kasutada mudeli erinevaid juurkaupu.   
8. Klõpsake valikut Kujundaja.
9. Tehke puul valik „Data model\Data model“.
    * Lisage nõutav andmeallikas. See on andmemudel, mis sisaldab arhiivitavate kinnitatud Antrastat-kannete üksikasju.  
10. Klõpsake suvandit Juure lisamine.
11. Sisestage nimeväljale „model”.
    * mudel  
12. Sisestage või valige definitsiooni väljal väärtus „For application data update”.
    * Avalduse andmete uuendamiseks  
13. Klõpsake nuppu OK.
14. Laiendage puus sõlme „model”.
15. Valige puul suvand Funktsioonid\arvutatud väli.
16. Tehke puul valik „model\Archive header“.
17. Klõpsake vahekaarti Lisa.
    * Kuna soovite nummerdada kinnitatud Intrastat-kandeid arhiivimiseks, peate lisama õige andmeallika.  
18. Sisestage nimeväljale tekst „Enumerated lines".
    * Nummerdatud read  
19. Klõpsake suvandit Muuda valemit.
20. Tehke puul valik „List\ENUMERATE“.
21. Klõpsake suvandit Funktsiooni lisamine.
22. Laiendage puus sõlme „model”.
23. Laiendage puul valikut „model\Archive header“.
24. Tehke puul valik „model\Archive header\Archive lines”.
25. Klõpsake suvandit Andmeallika lisamine.
26. Sisestage valemiväljale väärtus „ENUMERATE(model.'Archive header'.'Archive lines')”.
    * ENUMERATE(model.'Archive header'.'Archive lines')  
27. Klõpsake nuppu Salvesta.
28. Sulgege leht.
29. Klõpsake nuppu OK.
30. Klõpsake nuppu Lisa sihtkoht.
    * Lisage avalduse tabelid nõutavate sihtkohtadena, mis nõuavad kinnitatud Intrastat-kannete arhiiviüksikasjade uuendusi.  
31. Sisestage nimeväljale väärtus „Arhiiv”.
    * Arhiivi  
32. Sisestage tabelinime väljale väärtus „IntrastatArchiveGeneral”.
    * IntrastatArchiveGeneral  
    * Säilitage kirje toiming Sisesta, et saaksite kirjeid iga Intrastat-aruandluse protsessi üksikasjade arhiivimise ajal lisada.  
33. Valige Jah väljal Teabelogi kirjendamine.
    * Teabe hankimiseks avalduse andmete uuendamise probleemide kohta valige Jah.  
34. Valige Jah, kirjetegevuse kinnitamise vahelejätmine väljal.
    * Valige Jah, et tõkestada valideerimistõrkeid tühja "Intrastat-arhiivi ID" välja kohta. Seda tehakse pärast kirjete lisamist nende järjekorranumbrite sätte põhjal, mis konfigureeriti selle tabeli jaoks väliskaubandusparameetrite vormil.  
35. Klõpsake nuppu OK.
    * Siduge lisatud andmeallika (valitud juurkauba alusel filtreeritud mudel) elemendid lisatud sihtkoha elementidega.  
36. Laiendage puul valikut „Archive”.
37. Laiendage puul valikut „Archive\<Relations“.
38. Laiendage puul valikut „Archive\<Relations\IntrastatArchiveDetail”.
39. Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)”.
40. Laiendage puul valikut „model\Archive header\Enumerated lines”.
41. Laiendage puul valikut „model\Archive header\Enumerated lines\Value”.
42. Tehke puul valik „model\Archive header\Enumerated lines\Value\Amount”.
43. Klõpsake valikut Seo.
44. Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)”.
45. Tehke puul valik „model\Archive header\Enumerated lines\Value\Commodity rec id”.
46. Klõpsake valikut Seo.
47. Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)”.
48. Tehke puul valik „model\Archive header\Enumerated lines\Value\Item number”.
49. Klõpsake valikut Seo.
50. Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)”.
51. Tehke puul valik „model\Archive header\Enumerated lines\Number”.
52. Klõpsake valikut Seo.
53. Tehke puul valik „Archive\<Relations\IntrastatArchiveDetail”.
54. Tehke puul valik „model\Archive header\Enumerated lines”.
55. Klõpsake valikut Seo.
56. Tehke puul valik „Archive\File name(FileName)”.
57. Tehke puul valik „model\Archive header\File name”.
58. Klõpsake valikut Seo.
59. Tehke puul valik „Archive\Number of lines(NumberOfLines)”.
60. Tehke puul valik „model\Archive header\Number of lines”.
61. Klõpsake valikut Seo.
62. Valige puul väärtus „Archive”.
63. Tehke puul valik „model\Archive header“.
64. Klõpsake valikut Seo.
65. Klõpsake nuppu Salvesta.
66. Sulgege leht.
67. Sulgege leht.


