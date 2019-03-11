---
title: Vormingute käitamine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse vormingu dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenInvoicesListPage, CustInvoiceJournal, SalesTable, ERSolutionTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e87dbb0fa890f4d554c3e2ff09566fb2b1f3206b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "364783"
---
# <a name="run-formats-to-use-document-management-files-in-er-output"></a>Vormingute käitamine dokumendihalduse failide kasutamiseks elektroonilise aruandluse väljundis

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu dokumendihalduse failide (manuste) kasutamiseks elektroonilise aruandluse väljundis. Neid toiminguid saab teha DEMF ettevõttes.

Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Dokumendihalduse failide kasutamine vormingu väljundites (3. osa: vormingu loomine).

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="add-necessary-attachments-for-sales-order-of-a-single-invoice"></a>Vajalike manuste lisamine ühe arvega müügitellimusele
1. Avage Müügireskontro > Arved > Kliendiarvete avamine.
2. Saate kirjete leidmiseks kasutada valikut Kiirfilter. Näiteks saate filtrida välja Arve alusel väärtusega CIV-000148.
    * CIV-000148  
3. Klõpsake valitud arve lingi järgimiseks.
    * CIV-000148  
4. Klõpsake, et järgida linki väljal Müügitellimus.
    * 000148  
5. Valige Päis väljalt Read või päis.
    * Valige Päis, näitamaks, et see on manuste lisamise eesmärk.  
6. Klõpsake suvandit Manusta.
    * Lisage sellele müügitellimusele manusena mõned failid. Kasutage faile, mille tüüpe dokumendihalduse moodul toetab (faililaiendid DOCX, DPF, XML, JPG jne). Sirvige ja valige manustatavad failid, mida töödeldakse täiendavalt koos seotud arvega elektroonilise aruandluse elektroonilises sõnumis.  
7. Klõpsake valikut Uus.
8. Klõpsake suvandit Fail.
9. Klõpsake valikut Uus.
10. Klõpsake suvandit Fail.
11. Sulgege leht.
12. Sulgege leht.
13. Sulgege leht.
14. Sulgege leht.

## <a name="run-the-designed-report-for-the-selected-invoice"></a>Käivitage valitud arvele koostatud aruanne
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut Kliendiarve mudel.
3. Laiendage puul valikut Kliendiarve mudel \ Kliendiarve mudel (kohandatud).
4. Valige puult Kliendiarve mudel \ Kliendiarve mudel (kohandatud) \ Elektroonilise arve näidissõnum.
5. Klõpsake nuppu Käivita.
6. Jaotise () kaasamiseks laiendage kirjeid.
7. Klõpsake käsku Filtreeri.
8. Valige töölehe Kliendiarve ja välja Müügitellimus rida.
9. Tippige väärtus 000148 väljale Kriteeriumid.
    * Tippige kriteeriumiväljale Müügitellimus tellimuse number 000148.  
10. Klõpsake nuppu OK.
11. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et igale manusele on loodud üks XML-sõlm. Manuse sisu lisatakse XML-väljundile tekstivormingus MIME (base64).  

