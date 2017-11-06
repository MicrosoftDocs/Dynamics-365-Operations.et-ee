--- 
title: "Elektroonilise aruandluse (ER) vormingu käitamine loendamiseks ja liitmiseks"
description: "Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal."
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
ms.openlocfilehash: 9f5520dc4e1eddc2fc52a05e5dc386b982d8f5ad
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a>Elektroonilise aruandluse (ER) vormingu käitamine loendamiseks ja liitmiseks

[!include[task guide banner](../../includes/task-guide-banner.md)]

Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutaja saab konfigureerida elektroonilise aruandluse (ER) vormingu loendamiseks ja liitmiseks juba loodud tekstiväljundi andmete põhjal. Neid toiminguid saab teha DEMF ettevõttes.

Nende etappide lõpetamiseks peate esmalt lõpetama etapid protseduuris Elektrooniline aruandlus Vormingu konfigureerimine loendamiseks ja liitmiseks (3. osa: arvutuste kasutamine väljundi koostamiseks).

See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a>Proovige seda konfiguratsiooni intrastati aruannete koostamiseks
1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
2. Klõpsake valikut Aruandluse konfiguratsioonid.
3. Laiendage puul valikut Intrastati mudel.
4. Laiendage puul valikut Intrastati mudel \ Intrastat (DE).
5. Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.
6. Klõpsake tegumiribal valikut Konfiguratsioonid.
7. Klõpsake valikut Kasutaja parameetrid.
8. Tehke väljal Käivita sätted valik Jah.
9. Klõpsake nuppu OK.
10. Klõpsake nuppu Redigeeri.
11. Tehke väljal Käivita mustand valik Jah.
12. Klõpsake nuppu Salvesta.
13. Minge jaotisse Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid.
14. Laiendage jaotist Elektrooniline aruandlus.
15. Valige konfiguratsioon „Intrastat (DE) koos loendamise ja liitmisega”.
16. Valige konfiguratsioon „Intrastat (DE) koos loendamise ja liitmisega”.
17. Klõpsake nuppu Salvesta.
18. Sulgege leht.
19. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.
20. Klõpsake suvandit Väljund.
21. Klõpsake vahekaarti Aruanne.
    * Käivitage intrastati aruande koostamise protsess.  
22. Määrake väljal Alguskuupäev kuupäevaks 2000/01/01.
    * Määratlege aruandeperioodi algus- ja lõpukuupäevad, mis hõlmavad vormil olevaid kandeid.  
23. Määrake väljal Lõppkuupäev kuupäevaks 31.12.2022.
    * Määratlege aruandeperioodi algus- ja lõpukuupäevad, mis hõlmavad vormil olevaid kandeid.  
24. Valige Saabumised väljalt Suund.
25. Valige Jah väljal Loo fail.
26. Klõpsake nuppu OK.
    * Vaadake loodud väljund ja lõpus olevad kokkuvõtteread üle.  
27. Klõpsake valikut Uus.
28. Märkige loendis valitud rida.
29. Valige Lähetused väljalt Suund.
30. Sisestage või valige väärtus väljal Kaubakood.
31. Sisestage või valige väärtus väljal Kaup.
32. Määrake valiku Kaal väärtuseks 10.
33. Määrake valiku Arve summa väärtuseks 10 000.
34. Määrake valiku Statistiline summa väärtuseks 10 000.
35. Klõpsake suvandit Väljund.
36. Klõpsake vahekaarti Aruanne.
37. Valige Lähetused väljalt Suund.
38. Klõpsake nuppu OK.
    * Vaadake loodud väljund ja lõpus olevad kokkuvõtteread üle. Pange tähele, et seda on esimese tsükliga võrreldes muudetud.  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a>Käivitage konfiguratsioon silumisrežiimis kogutud loendamise ja liitmise andmete ülevaatamiseks
1. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
2. Laiendage puul valikut Intrastati mudel.
3. Laiendage puul valikut Intrastati mudel \ Intrastat (DE).
4. Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.
5. Klõpsake tegumiribal valikut Konfiguratsioonid.
6. Klõpsake valikut Kasutaja parameetrid.
7. Valige välja Käivita silumisrežiimis väärtuseks Jah.
8. Klõpsake nuppu OK.
9. Sulgege leht.
10. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.
11. Klõpsake suvandit Väljund.
12. Klõpsake vahekaarti Aruanne.
13. Klõpsake nuppu OK.
14. Sulgege leht.
15. Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.
16. Laiendage puul valikut Intrastati mudel.
17. Laiendage puul valikut Intrastati mudel \ Intrastat (DE).
18. Valige puult „Intrastati mudel\Intrastat (DE)\Intrastat (DE) koos loendamise ja liitmisega“.
19. Klõpsake nuppu Silumislogid.
    * Pange tähele, et valitud konfiguratsiooni käivitamiseks on loodud siluri logikirje.  
20. Klõpsake suvandit Manusta.
21. Klõpsake valikut Ava.
    * Vaadake üle loodud XML-fail, mis sisaldab valitud konfiguratsiooni käitamise ajal kogutud loendamise ja liitmise üksikasju.  

