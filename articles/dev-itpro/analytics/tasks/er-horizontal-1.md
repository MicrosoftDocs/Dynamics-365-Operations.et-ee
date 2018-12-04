--- 
title: "Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (1. osa – vormingu koostamine)"
description: "Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 7f0481a09e2ff4ae06fc53011067050c3373d6bc
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1-design-format"></a>Elektrooniline aruandlus Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (1. osa: vormingu koostamine)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena. Neid toiminguid saab teha igas ettevõttes.

Toimingute teostamiseks tuleb esmalt läbida järgmised kolm tööjuhist. 

„ER Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks“

„ER Finantsdimensioonide kasutamine andmeallikana (1. osa: andmemudeli koostamine)“

„ER Finantsdimensioonide kasutamine andmeallikana (2. osa: mudeli vastendamine)“

Samuti peate alla laadima ja salvestama malli kohaliku koopia näidisaruandega, mis on saadaval siin: [Finantsdimensioonide veebiteenuse näidisaruanne](https://go.microsoft.com/fwlink/?linkid=862266).

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-a-new-report-configuration"></a>Uue aruandekonfiguratsiooni loomine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Valige puult Finantsdimensioonide näidismudel.
3. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
4. Sisestage väljale Uus valik Vorming põhineb andmemudelil Finantsdimensioonide näidismudel.
    * Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.  
5. Tippige väljale Nimi tekst Prooviaruanne horisontaalselt laiendatavate vahemikega.
    * Prooviaruanne horisontaalselt laiendatavate vahemikega  
6. Tippige väljale Kirjeldus tekst Exceli väljundi koostamiseks veergude dünaamilise lisamisega.
    * Exceli väljundi koostamiseks veergude dünaamilise lisamisega  
7. Tehke väljal Andmemudeli definitsioon valik Kirje.
8. Klõpsake Loo konfiguratsioon.

## <a name="design-the-report-format"></a>Aruande vormingu kujundamine
1. Klõpsake valikut Kujundaja.
2. Lülitage sisse nupp Näita üksikasju.
3. Klõpsake toimingupaanil nuppu Impordi.
4. Klõpsake käsku Impordi Excelist.
5. Klõpsake suvandit Manused.
    * Aruandemalli importimine. Kasutage selleks alla laaditud Exceli faili.  
6. Klõpsake valikut Uus.
7. Klõpsake suvandit Fail.
8. Sulgege leht.
9. Sisestage või valige väärtus väljal Mall.
    * Valige alla laaditud mall.  
10. Klõpsake nuppu OK.
    * Lisage uus vahemik finantsdimensioonidele Exceli väljundi dünaamiliseks loomiseks valitud veergude arvuga (kasutaja dialoogi vormil). Iga veeru iga lahter tähistab ühe finantsdimensiooni nime.  
11. Klõpsake valikut Lisa rippdialoogi avamiseks.
12. Valige puult Excel \ Vahemik.
13. Tippige väljale Exceli vahemik väärtus DimNames.
    * DimNames  
14. Valige väljalt Edastamise suund väärtus Horisontaalne.
15. Klõpsake nuppu OK.
16. Valige puult „Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal“.
17. Klõpsake nuppu Ülespoole.
18. Valige puult „Excel = "SampleFinDimWsReport"\Cell<DimNames>“.
19. Klõpsake käsku Lõika.
20. Valige puult „Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal“.
21. Klõpsake käsku Kleebi.
22. Laiendage puul valikut „Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal“.
23. Laiendage puul valikut „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical.
24. Laiendage puul valikut Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical.
25. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical“.
    * Lisage uus vahemik finantsdimensioonidele Exceli väljundi dünaamiliseks loomiseks valitud veergude arvuga (kasutaja dialoogi vormil). Iga veeru iga lahter tähistab ühe finantsdimensiooni väärtust iga aruande kande kohta.  
26. Klõpsake nuppu Lisa vahemik.
27. Tippige väljale Exceli vahemik väärtus DimValues.
    * DimValues  
28. Valige väljalt Edastamise suund väärtus Horisontaalne.
29. Klõpsake nuppu OK.
30. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>“.
31. Klõpsake käsku Lõika.
32. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal“.
33. Klõpsake käsku Kleebi.
34. Laiendage puul valikut „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal“.

## <a name="map-format-elements-to-data-sources"></a>Vorminguelementide vastendamine andmeallikatega
1. Klõpsake vahekaarti Vastendus.
2. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel.
3. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.
4. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.
5. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.
6. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>“.
7. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend \ Kood: string.
8. Klõpsake valikut Seo.
9. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal“.
10. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Dimensioonide andmed: kirjete loend.
11. Klõpsake valikut Seo.
12. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>“.
13. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kreedit: tegelik.
14. Klõpsake valikut Seo.
15. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>“.
16. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Deebet: tegelik.
17. Klõpsake valikut Seo.
18. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>“.
19. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Valuuta: string.
20. Klõpsake valikut Seo.
21. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>“.
22. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kuupäev: kuupäev.
23. Klõpsake valikut Seo.
24. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>“.
25. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend \ Kanne: string.
26. Klõpsake valikut Seo.
27. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>“.
28. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.
29. Klõpsake valikut Seo.
30. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical“.
31. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Kanne: kirjete loend.
32. Klõpsake valikut Seo.
33. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>“.
34. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend \ Partii: string.
35. Klõpsake valikut Seo.
36. Valige puult „Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical“.
37. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Tööleht: kirjete loend.
38. Klõpsake valikut Seo.
39. Laiendage puul valikut mudel: andmemudel Finantsdimensioonide näidismudel \ Dimensioonide seadistus: kirjete loend.
40. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Dimensioonide seadistus: kirjete loend \ Kood: string.
41. Valige puult „Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>“.
42. Klõpsake valikut Seo.
43. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Dimensioonide seadistus: kirjete loend.
44. Valige puult „Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal“.
45. Klõpsake valikut Seo.
46. Valige puult „Excel = "SampleFinDimWsReport"\Cell<CompanyName>“.
47. Valige puult mudel: andmemudel Finantsdimensioonide näidismudel \ Ettevõte: string.
48. Klõpsake valikut Seo.
49. Klõpsake nuppu Salvesta.
50. Sulgege leht.


