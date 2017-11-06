--- 
title: "Elektroonilise aruandluse (ER) andmemudeli laiendamine dokumendihalduse failide kasutamiseks vormingu väljundites"
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: f3d494cc83b273eef071b23d0948b283ba85c17e
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="extend-data-model-to-use-document-management-files-in-format-outputs-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) andmemudeli laiendamine dokumendihalduse failide kasutamiseks vormingu väljundites

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha igas ettevõttes.

Nende etappide lõpetamiseks peate esmalt lõpetama etapid tegevuse juhendis Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (1. osa: andmemudeli ettevalmistamine).

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

## <a name="map-new-data-model-elements-to-dynamics-365-for-finance-and-operations-enterprise-edition-data-sources"></a>Uute andmemudeli elementide vastendamine rakenduse Dynamics 365 for Finance and Operations, Enterprise edition andmeallikatega
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

