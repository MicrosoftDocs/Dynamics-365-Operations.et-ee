---
title: EUR-00002 ELi Intrastati deklaratsiooni loomine
description: Selles protseduuris selgitatakse vajalikke toiminguid Intrastati deklaratsiooni eksportimise kohta elektroonilises failivormingus ja deklaratsiooni andmete eelvaatamist Exceli vormingus.
author: AdamTrukawka
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: atrukawk
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
ms.openlocfilehash: b14134763da262fabe533b2864a5472abaeb01c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283820"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a>EUR-00002 ELi Intrastati deklaratsiooni loomine

[!include [banner](../../includes/banner.md)]

Selles protseduuris selgitatakse vajalikke toiminguid Intrastati deklaratsiooni eksportimise kohta elektroonilises failivormingus ja deklaratsiooni andmete eelvaatamist Exceli vormingus. 

Enne kui saate selle protseduuri lõpule viia, peate kandma kanded Intrastati. 

Protseduuri loomisel kasutati demoettevõtte DEMF andmeid.


## <a name="import-configurations-with-settings"></a>Konfiguratsioonide importimine sätetega
1. Avage Tööruumid > Elektrooniline aruandlus
2. Klõpsake valikut Määra aktiivseks.
3. Klõpsake valikut Hoidlad.
4. Klõpsake valikut Ava.
5. Avage veeru filter Konfiguratsiooni nimi.
6. Rakendage väljal Konfiguratsiooni nimi filtrit väärtusega Intrastat (DE), kasutades filtri tehtemärki „algab üksusega”.
    * Peate valima konfiguratsiooni nime, mis on rakendatav teie juriidilise isiku riigile. Selles protseduuris kasutatakse näitena Saksamaa juriidilist isikut (DEMF), seetõttu tuleks teha valik Intrastat (DE).  
    * Klõpsake nuppu Impordi ja seejärel nuppu Jah.  
7. Avage veeru filter Konfiguratsiooni nimi.
8. Rakendage väljal Konfiguratsiooni nimi filtrit väärtusega Intrastati aruanne kasutades filtri tehtemärki „algab üksusega”.
    * Klõpsake nuppu Impordi ja seejärel nuppu Jah.  

## <a name="set-up-foreign-trade-parameters"></a>Väliskaubanduse parameetrite seadistamine
1. Avage Maks > Seadistus > Väliskaubandus > Väliskaubanduse parameetrid
2. Laiendage jaotist Elektrooniline aruandlus.
3. Sisestage või valige väärtus Intrastat (DE) väljal Failivormingu vastendamine
4. Sisestage või valige väärtus Intrastati aruanne väljal Aruandevormingu vastendamine
5. Laiendage jaotist Ümardamisreeglid.
    * Peate seadistama ümardamisreeglid, mis kehtivad teie riigis/regioonis Intrastati aruandluse puhul.  
6. Sisestage number väljale Ümardamisreegel
    * Sisestage ümardamistäpsus, näiteks 0,01.  
7. Sisestage number väljale Summa kümnendkohtade arv.
    * Sisestage näiteks 2.  
8. Valige suvand väljal Ümardamine alla 1 kg.
    * Valige näiteks Ümardamine kuni 1 kg-ni.  
9. Sisestage number väljale Ümardamisreegel
    * Sisestage näiteks 1 kaalu ümardamise kohta täisarvuni.  
10. Laiendage jaotist Alampiir.
11. Sisestage number väljale Kaal.
    * Sisestage minimaalseks kaaluks näiteks 10.  
12. Sisestage number väljale Summa.
    * Sisestage miinimumsummaks näiteks 200.  
13. Sisestage või valige väärtus väljal Kaup.

## <a name="set-up-compression-of-intrastat"></a>Intrastati tihendamise seadistamine
1. Avage Maks > Seadistus > Väliskaubandus > Intrastati tihendamine.
2. Klõpsake nuppu Eemalda.
3. Otsige loendist ja valige soovitud kirje.
    * Valige jaotises Saadaval näiteks Kaup.  
4. Klõpsake vahekaarti Lisa.

## <a name="generate-intrastat-declaration"></a>Intrastati deklaratsiooni loomine
1. Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat
2. Klõpsake suvandit Kinnita.
    * Kinnitamine tehakse vastavalt väljale Kontrolli seadistust lehel Väliskaubanduse parameetrid.  
3. Klõpsake nuppu OK.
4. Klõpsake käsku Uuenda.
5. Klõpsake suvandit Alampiir.
6. Sisestage kuupäev väljale Alguskuupäev.
    * Sisestage näiteks 1. jaanuar 2015.  
7. Tehke väljal Tihendamine valik Jah.
8. Sisestage kuupäev väljale Lõppkuupäev.
    * Sisestage näiteks 31. jaanuar 2015.  
9. Klõpsake nuppu OK.
10. Klõpsake käsku Uuenda.
11. Klõpsake käsku Tihenda.
    * See tihendamine toimub vastavalt sellele, kuidas te seadistate Intrastati tiheduse sätted.  
12. Sisestage kuupäev väljale Alguskuupäev.
    * Sisestage näiteks 1. jaanuar 2015.  
13. Sisestage kuupäev väljale Lõppkuupäev.
    * Sisestage näiteks 31. jaanuar 2015.  
14. Klõpsake nuppu OK.
15. Klõpsake käsku Uuenda.
16. Klõpsake käsku Loo uued järjekorranumbrid.
17. Klõpsake nuppu OK.
18. Klõpsake suvandit Väljund.
19. Klõpsake vahekaarti Aruanne.
20. Sisestage väljale Alates kuupäevast aruandlusperioodi esimene kuupäev.
    * Määrake kuupäevaks näiteks 1. jaanuar 2015.  
21. Sisestage kuupäev väljale Lõpukuupäev.
    * Sisestage näiteks 31. jaanuar 2015.  
22. Valige Jah väljal Loo fail.
23. Sisestage väärtus väljale Faili nimi.
24. Valige Jah väljal Loo aruanne.
25. Tippige väärtus väljale Aruandefaili nimi.
26. Valige suvand väljal Suund.
    * Tehke näiteks valik Kauba lähetamine.  
27. Klõpsake nuppu OK.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
