---
title: Elektrooniline aruandlus. Finantsdimensioonide kasutamine andmeallikana (4. osa – aruande käivitamine)
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 917eae141bbb8792f02d3323054e2a4096dae551
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "345279"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-4-run-the-report"></a>Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (4. osa: aruande käivitamine)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) mudeli finantsdimensioonide kasutamiseks elektrooniliste aruannete andmeallikana. Neid toiminguid saab teha DEMF ettevõttes.

Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Finantsdimensioonide kasutamine andmeallikana (3. osa: aruande koostamine). Peate konfigureerima ka dokumentide vaiketüübid lehel Elektroonilise aruande parameetrid. Dokumentide vaiketüübid määratakse ka siis, kui mõne elektroonilise aruandluse konfiguratsiooni alla laadite ja impordite. 


## <a name="run-report"></a>Aruande käitamine
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul jaotist Finantsdimensioonide näidismudel.
3. Valige puult Finantsdimensioonide näidismudel \ Pearaamatu töölehe aruanne.
4. Klõpsake käsku Käita.
5. Sisestage või valige väärtus väljal Dimensiooni nimi.
    * Kõigi praeguse ettevõtte dimensioonide valimiseks sisestage järgmine: BusinessUnit;CostCenter;Department;ItemGroup;MainAccount;Project  
6. Jaotise kaasamiseks laiendage kirjeid.
7. Klõpsake käsku Filtreeri.
8. Valige tabeli Pearaamatu tööleht rida ja väli Töölehe partiinumber.
9. Tippige väärtus 00057 väljale Kriteeriumid.
10. Klõpsake nuppu OK.
11. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et iga valitud partii kande puhul esitatakse vastava finantsdimensioonikogumi finantsdimensioonid. Käivitage see aruanne ja valige teistsugused dimensioonid, et näeksite, et aruanne ei sõltu valitud dimensioonide arvust ega rakenduse Dynamics 365 for Finance and Operations, Enterprise edition selle eksemplari jaoks konfigureeritud dimensioonide arvust.  

