---
title: Mudelivastenduse konfiguratsioonide kasutamine koondarvutusteks andmebaasi tasemel
description: See protseduur annab teavet selle kohta, kuidas kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a462a3997644a494b5cea89c9530ddba67c32450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313631"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a>Mudelivastenduse konfiguratsioonide kasutamine koondarvutusteks andmebaasi tasemel

[!include [task guide banner](../../includes/task-guide-banner.md)]

See protseduur annab teavet selle kohta, kuidas kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks. Selles protseduuris loote konfiguratsiooni näidisettevõttele Litware, Inc. 

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need etapid saab lõpule viia ükskõik millise andmekomplekti abil.

 Toimingute tegemiseks tuleb esmalt lõpule viia protseduuri „ER parandab kogusumma arvutuste tõhusust, tehes neid andmebaasi tasemel (osa 1: konfiguratsioonide ettevalmistamine)” etapid.

1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut Intrastati mudel.
3. Tehke puul valik „Intrastati mudel\Intrastati näidisvastendamine”.
4. Klõpsake valikut Kujundaja.
5. Klõpsake valikut Kujundaja.
6. Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.
7. Klõpsake suvandit Juure lisamine.
    * Lisage uus andmeallikas, mis tähistab kirjeid, mille soovite grupeerida.  
8. Sisestage väljale Nimi suvand Kanded.
    * Kanded  
9. Väljale Tabel tippige „Intrastat”.
    * Intrastat  
10. Klõpsake nuppu OK.
11. Valige puul väärtus Funktsioonid\grupeerimisalus.
    * Seda tüüpi andmeallikat kasutatakse käitusajal uue andmeallika lisamiseks, et grupeerida kirjeid ja arvutada nõutavaid kogumeid.  
12. Klõpsake suvandit Juure lisamine.
13. Väljale Nimi tippige „TransactionsGroups”.
    * TransactionsGroups  
14. Klõpsake suvandit Grupi redigeerimise alus.
15. Valige puul suvand Kanded.
    * Valige lisatud andmeallikas tüübiga „Kirjete loend”, mis esindab kirjeid, mille soovite grupeerida.  
16. Klõpsake suvandit Lisa väli üksusele.
17. Klõpsake suvandit Mida grupeerida.
18. Laiendage puul suvandit Kanded.
19. Valige puul suvand „Kanded\Suund”.
20. Klõpsake suvandit Lisa väli üksusele.
21. Klõpsake suvandit Grupeeritud väljad.
    * Märkige väli, et määrata grupeerimise tase. Selle valiku põhjal tagastab andmeallikas käitusajal sama palju kannete gruppe kui on suunakoode, mida Intrastati tabelis täidetakse.  
22. Valige puul „Kanded\Arve summa (AmountMST)”.
    * Märkige ruut, et määrata kogumi arvutuse allikas.  
23. Klõpsake suvandit Lisa väli üksusele.
24. Klõpsake suvandit Kogumi väljad.
25. Märkige loendis valitud rida.
26. Valige väljal Meetod väärtus „Summa”.
    * Valige kogumi tüüp.  
27. Väljale Nimi tippige „SumOfAmountMST”.
    * Määrake kogumi nimi konfigureeritud andmeallikas.  
28. Klõpsake nuppu Salvesta.
    * Pange tähele, et väli „Käivitamine:” näitab, et grupeerimine toimub SQL-i andmebaasis käitusajal.  
29. Sulgege leht.
30. Klõpsake nuppu OK.
31. Laiendage puul väärtust „Kogusummad”.
32. Laiendage puul väärtust „TransactionsGroups”.
33. Laiendage puus väärtust „TransactionsGroups\koondatud”.
34. Valige puul „TransactionsGroups\aggregated\SumOfAmountMST”.
35. Valige puul „Kogusummad\Arve kogusumma (TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')”.
36. Klõpsake valikut Seo.
    * Sätte alusel arvutab andmeallikas iga kannete grupi jaoks välja „AmountMST” väärtuste summa. Kogumi arvutus on saadaval üksusena TransactionsGroups.aggregated.TotalAmount.  
37. Laiendage puul väärtust „TransactionsGroups”.
38. Valige puul väärtus „TransactionsGroups”.
39. Klõpsake nuppu Redigeeri.
40. Klõpsake suvandit Grupi redigeerimise alus.
41. Laiendage puul suvandit Kanded.
42. Valige puul „Kanded\Arve summa (AmountMST)”.
43. Klõpsake suvandit Lisa väli üksusele.
44. Klõpsake suvandit Kogumi väljad.
45. Märkige loendis valitud rida.
46. Valige väljal Meetod väärtus „Max”.
47. Väljale Nimi tippige „MaxOfAmountMST”.
48. Klõpsake nuppu Salvesta.
    * Andmeallikate GROUPBY käivitamist saab praegu üle kanda SQL-i andmebaasi tasemele teatud piirangutega. Ülekandmine on võimalik tüübiga „Kirjete loend” andmeallikate või avaldisena esitatud andmeallikate puhul, kasutades funktsiooni FILTER. Seda saab teha ainult juhul, kui grupeeritavate kirjete ühe välja jaoks on konfigureeritud ainult üks kogum.  
    * Pange tähele, et isegi juhul, kui väljal AmountMST konfigureeriti mitu kogumit, näitab väli „Käivitamine:” siiski, et grupeerimine toimub SQL-i andmebaasis käitusajal. Selle põhjuseks on see, et andmemudeli üksusega on seotud ainult üks kogumik, mida kasutatakse käitusajal sellest andmeallikast andmete toomiseks.  
49. Sulgege leht.
50. Klõpsake nuppu OK.
51. Laiendage puul väärtust „TransactionsGroups”.
52. Laiendage puus väärtust „TransactionsGroups\koondatud”.
53. Valige puul „TransactionsGroups\aggregated\MaxOfAmountMST”.
54. Valige puul „Kogusummad\Statistiline väärtus kokku (TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')”.
55. Klõpsake valikut Seo.
56. Laiendage puul väärtust „TransactionsGroups”.
57. Valige puul väärtus „TransactionsGroups”.
58. Klõpsake nuppu Redigeeri.
59. Klõpsake suvandit Grupi redigeerimise alus.
    * Pange tähele, et väli „Käivitamine:” näitab, et grupeerimine toimub käitusajal mälus, kuna mõlemad sama välja kogumid on seotud andmemudeli üksustega.   
60. Märkige või tühjendage loendis kõik read.
61. Klõpsake käsku Kustuta.
62. Klõpsake nuppu Jah.
63. Klõpsake käsku Kustuta.
64. Klõpsake nuppu Jah.
65. Klõpsake suvandit Lisa väli üksusele.
66. Klõpsake suvandit Mida grupeerida.
67. Laiendage puul valikut „Kauba kirje (Intrastat)”.
68. Klõpsake nuppu Salvesta.
    * Pange tähele, et väli „Käivitamine:” näitab, et grupeerimine toimub käitusajal mälus, isegi kui ükski kogum ei ole määratud ja valitud andmeallikas tüübiga „Tabeli kirjed” viitab samale tabelile „Intrastat”. Põhjuseks on see, et andmeallikas sisaldab mõningaid arvutatud välju, mida ei saa veel SQL-i andmebaasi tasemele üle kanda.  

