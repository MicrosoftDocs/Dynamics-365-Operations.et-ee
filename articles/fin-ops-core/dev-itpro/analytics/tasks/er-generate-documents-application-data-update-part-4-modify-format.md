---
title: Vormingute muutmine rakendusandmetega dokumentide loomiseks
description: See artikkel kirjeldab, kuidas kujundada aruandluse konfiguratsioone elektroonilise dokumendi loomiseks ja rakendusandmete värskendamiseks.
author: kfend
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ecd301b60f804328f3b6652df8c38edf42eb79f0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290480"
---
# <a name="modify-formats-to-generate-documents-that-have-application-data"></a>Vormingute muutmine rakendusandmetega dokumentide loomiseks

[!include [banner](../../includes/banner.md)]

Selle protseduuri toimingute lõpule viimiseks peate esmalt teostama protseduuri „ER Avalduse andmete värskendusega dokumentide genereerimine (3. osa: mudeli ja vastendamise muutmine)“.

Selles protseduuris demonstreeritakse, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone elektroonilise dokumendi genereerimiseks ja avalduse andmete uuendamiseks. Käesolevas näites muudate ER konfiguratsioone, et hakata neid kasutama nii elektrooniliste dokumentide loomiseks kui ka avalduse andmete uuendamiseks. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need toimingud saab lõpule viia DEMF-i andmekomplekti abil.


## <a name="modify-format-to-collect-details-of-reporting"></a>Vormingu muutmine aruandluse üksikasjade kogumiseks
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut „Intrastat (model)".
3. Tehke puul valik „Intrastat (model)\Intrastat (format)".
4. Klõpsake valikut Kujundaja.
5. Laiendage puul väärtust „File”.
6. Laiendage puul valikut „File\Declaration”.
7. Tehke puul valik „File\Declaration\Data”.
8. Valige kordsuse väljal „One many”.
    * Konfigureerige see vorminguelement Intrastat-aruandluse protsessi üksikasjade arhiivimiseks. Selle kaup esindab arhiivi päisekirjet.  
9. Laiendage puul valikut „File\Declaration\Data”.
10. Tehke puul valik "File\Declaration\Data\Item”.
11. Valige kordsuse väljal „Zero many”.
    * Konfigureerige see vorminguelement Intrastat-aruandluse protsessi üksikasjade arhiivimiseks. See kaup esindab arhiivitus ridade loendit.  
12. Laiendage puul valikut „File\Declaration\Data\Item”.
13. Tehke puul valik „File\Declaration\Data\Item\Dim1“.
14. Valige Jah väljal Välistatud.
    * Neid andmeid te ei arhiivi ja seega saate selle vorminguelemendi Intrastat-aruandluse andmete andmeallikas välistada.  
15. Laiendage puul valikut „File\Declaration\Data\Item\Dim1”.
16. Tehke puul valik „File\Declaration\Data\Item\Dim1\property“.
17. Valige Jah väljal Välistatud.
18. Tehke puul valik „File\Declaration\Data\Item\Dim1\date“.
19. Valige Jah väljal Välistatud.
20. Tehke puul valik „File\Declaration\Data\Item\Dim2“.
21. Valige Jah väljal Välistatud.
22. Laiendage puul valikut „File\Declaration\Data\Item\Dim2”.
23. Tehke puul valik „File\Declaration\Data\Item\Dim2\property“.
24. Valige Jah väljal Välistatud.
25. Tehke puul valik „File\Declaration\Data\Item\Dim2\code“.
26. Valige Jah väljal Välistatud.
27. Tehke puul valik „File\Declaration\Data\Item\Dim3“.
    * Mitmel vorminguelemendil võib olla sama nimi. Nt Dim. Kui kasutate seda vormingut Intrastat-aruande üksikasjade arhiivimisel andmeallikana, ei tunne te neid kohe ära ja seega peate nendele vorminguelementidele alternatiivsed nimed määrama.   
28. Sisestage väljale Nimi suvand Summa.
    * Summa  
29. Valige kordsuse väljal „Exactly one”.
30. Tehke puul valik „File\Declaration\Data\Item\Dim4“.
31. Sisestage väljale Nimi suvand Kaup.
    * Kaup  
32. Valige kordsuse väljal „Exactly one”.
    * Lisaks kujunduse vormingu elementidele, tuleb arhiivida ka järgmised Intrastat-aruandluse üksikasjad: iga esitatud artiklikauba kirje kordumatu ID ja genereeritud faili nimi. Kuna neid andmeid ei asustata Intrastat-aruandes, peate nende üksikasjadega seotud vormingu lisama andmeallika kaupadena.  
33. Tehke puul valik „File\Declaration\Data”.
34. Klõpsake valikut Lisa rippdialoogi avamiseks.
35. Tehke puul valik „Data source\Item”.
36. Tippige Faili nimi väljale Nimi.
    * Faili nimi  
37. Valige väljalt Andmetüüp suvand String.
38. Klõpsake nuppu OK.
39. Tehke puul valik "File\Declaration\Data\Item”.
40. Klõpsake käsku Lisa kaup.
41. Sisestage nimeväljale valik „Kaubakirje ID”.
    * Kaubakirje ID  
42. Valige väljalt Andmetüüp suvand Int64.
43. Klõpsake nuppu OK.
44. Klõpsake vahekaarti Vastendus.
45. Tehke puul valik "File\Declaration\Data\File name”.
46. Klõpsake valikut Seo.
47. Laiendage puus sõlme „model”.
48. Laiendage puul valikut „model\Transactions“.
49. Tehke puul valik „File\Declaration\Data\Item = model.Transactions\Commodity rec ID”.
50. Tehke puul valik „model\Transactions\Commodity rec ID”.
51. Klõpsake valikut Seo.
52. Klõpsake nuppu Salvesta.

## <a name="modify-format-to-memorize-details-of-reporting"></a>Vormingu muutmine aruandluse üksikasjade meeldejätmiseks

1. Klõpsake nuppu Vormingu vastendamine mudeliga.
2. Klõpsake Uus.
3. Sisestage või valige väljal Definitsioon juurkaup „Avalduse andmete uuendamiseks”.
    * Avalduse andmete uuendamiseks.
4. Sisestage nimeväljale valik „Vastendamine andmete uuendamiseks”.
    * Vastendamise andmete uuendamiseks  
5. Klõpsake nuppu Salvesta.
    * Vastendus määratleb, kuidas Intrastat-aruande üksikasju kogutakse andmemudelis, mille struktuur on määratud valitud juurkauba poolt „Avalduse andmete uuendamiseks”. Neid üksikasju, sama juurkaubaga „Avalduse andmete uuendamiseks” vastendamist ja suunda „Sihtkohani" kasutatakse avalduse andmete uuendamiseks. Avalduse andmete uuendamine käivitatakse kohe pärast väljamineva Intrastat-aruande genereerimist. Avalduse andmete uuendamise võib käitusajal vahele jätta, aga andmemudel peab olema tühi (sisaldab tühja kirjeloendit).
6. Klõpsake valikut Kujundaja.
    * Väljamineva Intrastat-aruande vorming lisatakse vaikimisi selle mudelivastenduse andmeallikana.  
    * Siduge loodud aruande elemendid (esitatud andmeallikana) andmemudeli elementidega, mis on filtreeritud valitud mudeli juurkauba alusel.  
7. Laiendage puul väärtust „Archive header”.
8. Laiendage puul valikut „Archive header\Archive lines”.
9. Laiendage puul valikut „format”.
10. Laiendage puul valikut „format\Declaration: XML Element(Declaration)”.
11. Laiendage puul valikut „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)”.
12. Laiendage puul valikut „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)”.
13. Laiendage puul valikut „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)”.
14. Laiendage puul valikut „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)”.
15. Tehke puul valik „Archive header\Number of lines”.
16. Klõpsake nuppu Redigeeri.
17. Tehke puul valik „List\COUNT”.
18. Klõpsake suvandit Funktsiooni lisamine.
19. Laiendage puul valikut „format”.
20. Laiendage puul valikut „format\Declaration: XML Element(Declaration)”.
21. Laiendage puul valikut `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
22. Valige puul suvand `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
23. Klõpsake suvandit Andmeallika lisamine.
24. Sisestage valemi väljale väärtus „COUNT(format.Declaration.Data.Item)”.
    * COUNT(format.Declaration.Data.Item)  
25. Klõpsake nuppu Salvesta.
26. Sulgege leht.
27. Tehke puul valik „Archive header\File name”.
28. Tehke puul valik „format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name)”.
29. Klõpsake valikut Seo.
30. Valige puul suvand `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)`.
31. Tehke puul valik „Archive header\Archive lines\Item number”.
32. Klõpsake valikut Seo.
33. Valige puul suvand `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)`.
34. Tehke puul valik „Archive header\Archive lines\Amount”.
35. Klõpsake valikut Seo.
36. Valige puul suvand `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec ID: Item Int64(Commodity rec ID)`.
37. Tehke puul valik „Archive header\Archive lines\Commodity rec ID”.
38. Klõpsake valikut Seo.
39. Tehke puul valik „Archive header\Archive lines”.
40. Valige puul suvand `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)`.
41. Klõpsake valikut Seo.
42. Tehke puul valik „Archive header”.
43. Valige puul suvand `format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)`.
44. Klõpsake valikut Seo.
45. Klõpsake nuppu Salvesta.
46. Sulgege leht.
47. Sulgege leht.
48. Sulgege leht.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
