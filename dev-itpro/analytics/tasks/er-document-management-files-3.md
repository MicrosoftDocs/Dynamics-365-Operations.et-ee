--- 
title: "Elektroonilise aruandluse (ER) vormingu loomine dokumendihalduse failide kasutamiseks vormingu väljundites"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.openlocfilehash: 47c7bea976d1052f537068b6bcf79c78ac3befbf
ms.contentlocale: et-ee
ms.lasthandoff: 07/27/2017

---
# <a name="create-format-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) vormingu loomine dokumendihalduse failide kasutamiseks vormingu väljundites

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (2. osa: andmemudeli laiendamine).

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="create-a-format-to-process-invoices"></a>Vormingu loomine arvete töötlemiseks
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Laiendage puul valikut Kliendiarve mudel.
4. Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).
    * Saate luua vormi elektrooniliste sõnumite loomiseks teabega mis tahes failide kohta, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.  
5. Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.
6. Sisestage väljale Uus valik Vorming põhineb andmemudelil Kliendiarve mudel (kohandatud).
7. Tippige väljale Nimi tekst Elektroonilise arve näidissõnum.
    * Elektroonilise arve näidissõnum  
8. Sisestage või valige väärtus väljal Andmemudeli definitsioon.
    * InvoiceCustomer  
9. Klõpsake Loo konfiguratsioon.

## <a name="design-a-format-to-populate-attachments-into-generating-a-message-in-mime-format"></a>Kujundage vorming manuste lisamiseks, tekitades MIME-vormingus sõnumi
1. Klõpsake valikut Kujundaja.
2. Klõpsake suvandit Lisa juur rippdialoogi avamiseks.
3. Valige puul suvand XML\Element.
4. Tippige Arve väljale Nimi.
    * Arve  
5. Klõpsake nuppu OK.
6. Klõpsake valikut Lisa rippdialoogi avamiseks.
7. Valige puul suvand XML\Attribute.
8. Tippige SalesOrder väljale Nimi.
    * SalesOrder  
9. Klõpsake nuppu OK.
10. Klõpsake valikut Lisa atribuut.
11. Tippige InvoiceNumber väljale Nimi.
    * InvoiceNumber  
12. Klõpsake nuppu OK.
13. Klõpsake valikut Lisa atribuut.
14. Tippige InvoiceAmount väljale Nimi.
    * InvoiceAmount  
15. Klõpsake nuppu OK.
16. Klõpsake valikut Lisa rippdialoogi avamiseks.
17. Valige puul suvand XML\Element.
18. Tippige EnclosedDocs väljale Nimi.
    * EnclosedDocs  
19. Klõpsake nuppu OK.
20. Valige puult Arve \ EnclosedDocs.
21. Klõpsake käsku Lisa element.
22. Tippige Dokument väljale Nimi.
    * Dokument   
23. Klõpsake nuppu OK.
24. Valige puult Arve \ EnclosedDocs \ Dokument.
25. Klõpsake valikut Lisa rippdialoogi avamiseks.
26. Valige puul suvand XML\Attribute.
27. Tippige FileName väljale Nimi.
    * FileName  
28. Klõpsake nuppu OK.
29. Klõpsake valikut Lisa rippdialoogi avamiseks.
30. Valige puul suvand XML\Element.
31. Tippige FileContent väljale Nimi.
    * FileContent  
32. Klõpsake nuppu OK.
33. Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent.
34. Klõpsake valikut Lisa rippdialoogi avamiseks.
35. Valige puul väärtus Tekst \ Base64.
36. Klõpsake nuppu OK.

## <a name="map-format-elements-to-data-model-as-data-source"></a>Vorminguelementide vastendamine andmemudeliga andmeallikana
1. Valige puult Arve \ SalesOrder.
2. Klõpsake vahekaarti Vastendus.
3. Laiendage puus sõlme „model”.
4. Valige puult mudel \ Müügitellimuse number (SalesId).
5. Klõpsake valikut Seo.
6. Valige puult Arve \ InvoiceNumber.
7. Laiendage puul valikut mudel \ Alusarve (InvoiceBase).
8. Valige puult mudel \ Alusarve (InvoiceBase) \ Arve number (Id).
9. Klõpsake valikut Seo.
10. Valige puult Arve \ InvoiceAmount.
11. Valige puult mudel \ Alusarve (InvoiceBase) \ Arve summa (summa).
12. Klõpsake valikut Seo.
13. Laiendage puul valikut mudel \ Arve manused.
14. Valige puult mudel \ Arve manused \ Faili sisu.
15. Valige puult Arve \ EnclosedDocs \ Dokument \ FileContent \Base64.
16. Klõpsake valikut Seo.
17. Valige puult mudel \ Arve manused \ Faili nimi.
18. Valige puult Arve \ EnclosedDocs \ Dokument \ FileName.
19. Klõpsake valikut Seo.
20. Valige puult mudel \ Arve manused.
21. Valige puult Arve \ EnclosedDocs \ Dokument.
22. Klõpsake valikut Seo.
23. Klõpsake nuppu Salvesta.
24. Sulgege leht.

