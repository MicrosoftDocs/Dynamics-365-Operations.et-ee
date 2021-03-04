---
title: Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (2. osa – andmemudeli laiendamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5923a14f4ba544154bf40391896d29826d3ce1b1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681802"
---
# <a name="er-use-document-management-files-in-format-outputs-part-2---extend-data-model"></a>Elektrooniline aruandlus. Dokumendihalduse failide kasutamine vormingu väljundites (2. osa – andmemudeli laiendamine)

[!include [banner](../../includes/banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpule viimiseks peate esmalt lõpetama etapid tegevuse juhendis „Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (1. osa: andmemudeli ettevalmistamine)”.

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="extend-data-model-to-present-the-document-management-files-in-it"></a>Laiendage andmemudelit, et esitada selles dokumendihalduse faile
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Laiendage puul valikut Kliendiarve mudel.
4. Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud).
5. Klõpsake valikut Kujundaja.
6. Valige puult Kliendiarve(InvoiceCustomer).
    * Laiendame seda andmemudelit, näidates seda mis tahes failides, mis on manustatud müügitellimusele, mis on seotud elektrooniliselt töödeldava arvega.  
7. Rippdialoogi avamiseks klõpsake valikut Uus.
8. Tippige Arve manused väljale Nimi.
    * Arve manused  
9. Valige väljalt Kaubakood suvand Kirjete loend.
10. Klõpsake vahekaarti Lisa.
11. Rippdialoogi avamiseks klõpsake valikut Uus.
12. Tippige Faili sisu väljale Nimi.
    * Faili sisu  
13. Valige väljalt Kauba tüüp väärtus Konteiner.
14. Klõpsake vahekaarti Lisa.
15. Rippdialoogi avamiseks klõpsake valikut Uus.
16. Tippige Faili nimi väljale Nimi.
    * Faili nimi  
17. Valige väljalt Kaubakood suvand String.
18. Klõpsake vahekaarti Lisa.

## <a name="map-new-data-model-elements-to-data-sources"></a>Uue andmemudeli elementide vastendamine andmeallikatega
1. Klõpsake suvandit Mudeli vastendamine andmeallikaga.
2. Kasutage kiirfiltrit, et filtreerida väljal Definitsioon väärtusega InvoiceCustomer.
    * InvoiceCustomer  
    * Vastendame uued mudelielemendid sobivate andmeallikatega.  
3. Klõpsake valikut Kujundaja.
4. Valige puult Arve manused.
5. Laiendage puul valikut Arve manused.
6. Valige puult Arve manused \ Faili nimi.
7. Klõpsake nuppu Redigeeri.
8. Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'originalFileName()'  
9. Klõpsake nuppu Salvesta.
10. Sulgege leht.
11. Valige puult Arve manused \ Faili sisu.
12. Klõpsake nuppu Redigeeri.
13. Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'.'getFileContentAsContainer()'  
14. Klõpsake nuppu Salvesta.
15. Sulgege leht.
16. Valige puult Arve manused.
17. Klõpsake nuppu Redigeeri.
18. Sisestage väljale Valem väärtus 'CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents''.
    * CustInvoiceJour.'>Relations'.SalesTable.'<Relations'.'<Documents'  
19. Klõpsake nuppu Salvesta.
20. Sulgege leht.
21. Klõpsake nuppu Salvesta.
22. Sulgege leht.
23. Sulgege leht.
24. Sulgege leht.
25. Klõpsake valikut Muuda olekut.
26. Klõpsake valikut Valmis.
27. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]