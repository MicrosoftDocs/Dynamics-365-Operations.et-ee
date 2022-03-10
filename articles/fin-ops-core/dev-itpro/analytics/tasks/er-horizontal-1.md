---
title: Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (1. osa – vormingu koostamine)
description: Selles teemas kirjeldatakse, kuidas konfigureerida elektroonilise aruandluse (ER) vorming looma aruandeid OPENXML töölehtede (Excel) failidena. (1. osa)
author: NickSelin
ms.date: 04/23/2021
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
ms.openlocfilehash: ab360c259af37ce3995d3cd2560bc2e765e0bceb
ms.sourcegitcommit: e3290eb58ae569a59d6ae2e6922e7d8be8f1980f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2021
ms.locfileid: "7551772"
---
# <a name="er-use-horizontally-expandable-ranges-to-dynamically-add-columns-in-excel-reports-part-1---design-format"></a>Elektrooniline aruandlus. Horisontaalselt laiendatavate vahemike kasutamine veergude dünaamiliseks lisamiseks Exceli aruannetes (1. osa – vormingu koostamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas kasutaja, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll, saab konfigureerida elektroonilise aruandluse vormingut, et luua aruandeid OPENXML-i töölehtede (Exceli) failidena, milles saab luua dünaamiliselt vajalikke veerge horisontaalselt laiendatavate vahemikena. Neid toiminguid saab teha igas ettevõttes.

Toimingute teostamiseks tuleb esmalt läbida järgmised kolm tööjuhist.

„ER Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks”

„Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (1. osa – andmemudeli koostamine)”

„Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (2. osa – mudeli vastendamine)”

Samuti peate alla laadima ja salvestama malli kohaliku koopia näidisaruandega, mis on saadaval siin: [Finantsdimensioonide veebiteenuse näidisaruanne](https://download.microsoft.com/download/3/1/3/313e2090-bc0a-421f-bf96-c58da9bc0dea/SampleFinDimWsReport.xlsx).

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.

## <a name="create-a-new-report-configuration"></a>Uue aruandekonfiguratsiooni loomine

1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Valige puul suvand `Financial dimensions sample model`.
3. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
4. Väljal „Uus” sisestage `Format based on data model Financial dimensions sample model`.
    * Kasutage oma uue aruande andmeallikana eelnevalt loodud mudelit.  
5. Trükkige nime väljale `Sample report with horizontally expandable ranges`.
    * Prooviaruanne horisontaalselt laiendatavate vahemikega  
6. Kirjutage väljale „Kirjeldus” `To make Excel output with dynamically adding columns`.
    * Exceli väljundi koostamiseks veergude dünaamilise lisamisega  
7. Tehke väljal Andmemudeli definitsioon valik Kirje.
8. Klõpsake Loo konfiguratsioon.

## <a name="design-the-report-format"></a>Aruande vormingu kujundamine

1. Klõpsake valikut Kujundaja.
2. Lülitage sisse nupp `Show details`.
3. Klõpsake toimingupaanil nuppu Impordi.
4. Klõpsake käsku Impordi Excelist.
5. Klõpsake suvandit Manused.
    * Aruandemalli importimine. Kasutage selleks alla laaditud Exceli faili.  
6. Klõpsake Uus.
7. Klõpsake suvandit Fail.
8. Sulgege leht.
9. Sisestage või valige väärtus väljal Mall.
    * Valige alla laaditud mall.  
10. Klõpsake nuppu OK.
    * Lisage uus vahemik finantsdimensioonidele Exceli väljundi dünaamiliseks loomiseks valitud veergude arvuga (kasutaja dialoogi vormil). Iga veeru iga lahter tähistab ühe finantsdimensiooni nime.  
11. Klõpsake valikut Lisa rippdialoogi avamiseks.
12. Valige puul suvand `Excel\Range`.
13. Tippige väljale „Exceli vahemik” väärtus `DimNames`.
    * DimNames  
14. Valige väljalt „Edastamise suund” väärtus `Horizontal`.
15. Klõpsake nuppu OK.
16. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
17. Klõpsake nuppu Ülespoole.
18. Valige puul suvand `Excel = "SampleFinDimWsReport"\Cell<DimNames>`.
19. Klõpsake käsku Lõika.
20. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
21. Klõpsake käsku Kleebi.
22. Laiendage puul valikut `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
23. Laiendage puul valikut `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
24. Laiendage puul valikut `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
25. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
    * Lisage uus vahemik finantsdimensioonidele Exceli väljundi dünaamiliseks loomiseks valitud veergude arvuga (kasutaja dialoogi vormil). Iga veeru iga lahter tähistab ühe finantsdimensiooni väärtust iga aruande kande kohta.  
26. Klõpsake nuppu Lisa vahemik.
27. Tippige väljale „Exceli vahemik” väärtus `DimValues`.
    * DimValues  
28. Valige väljalt „Edastamise suund” väärtus `Horizontal`.
29. Klõpsake nuppu OK.
30. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<DimValues>`.
31. Klõpsake käsku Lõika.
32. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
33. Klõpsake käsku Kleebi.
34. Laiendage puul valikut `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.

## <a name="map-format-elements-to-data-sources"></a>Vorminguelementide vastendamine andmeallikatega

1. Klõpsake vahekaarti Vastendus.
2. Laiendage puul valikut `model: Data model Financial dimensions sample model`.
3. Laiendage puul valikut `model: Data model Financial dimensions sample model\Journal: Record list`.
4. Laiendage puul valikut `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
5. Laiendage puul valikut `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
6. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal\Cell<DimValues>`.
7. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String`.
8. Klõpsake valikut Seo.
9. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Range<DimValues>: Horizontal`.
10. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list`.
11. Klõpsake valikut Seo.
12. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Credit>`.
13. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real`.
14. Klõpsake valikut Seo.
15. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Debit>`.
16. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real`.
17. Klõpsake valikut Seo.
18. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<Currency>`.
19. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String`.
20. Klõpsake valikut Seo.
21. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransDate>`.
22. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date`.
23. Klõpsake valikut Seo.
24. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransVoucher>`.
25. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String`.
26. Klõpsake valikut Seo.
27. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical\Cell<TransBatch>`.
28. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
29. Klõpsake valikut Seo.
30. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Range<TransactionLine>: Vertical`.
31. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list`.
32. Klõpsake valikut Seo.
33. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical\Cell<Batch>`.
34. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list\Batch: String`.
35. Klõpsake valikut Seo.
36. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<JournalLine>: Vertical`.
37. Valige puul suvand `model: Data model Financial dimensions sample model\Journal: Record list`.
38. Klõpsake valikut Seo.
39. Laiendage puul valikut `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
40. Valige puul suvand `model: Data model Financial dimensions sample model\Dimensions setting: Record list\Code: String`.
41. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal\Cell<DimNames>`.
42. Klõpsake valikut Seo.
43. Valige puul suvand `model: Data model Financial dimensions sample model\Dimensions setting: Record list`.
44. Valige puul suvand `Excel = "SampleFinDimWsReport"\Range<DimNames>: Horizontal`.
45. Klõpsake valikut Seo.
46. Valige puul suvand `Excel = "SampleFinDimWsReport"\Cell<CompanyName>`.
47. Valige puul suvand `model: Data model Financial dimensions sample model\Company: String`.
48. Klõpsake valikut Seo.
49. Klõpsake nuppu Salvesta.
50. Sulgege leht.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
