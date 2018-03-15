--- 
title: "Konfiguratsioonide kujundus sissetulevate dokumentide sõelumiseks avalduse andmete värskendamiseks (ER)"
description: "Protseduur näitab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone sissetuleva elektroonilise dokumendi sõelumiseks."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 96c9397c6a83d61b679492f66f4aa6661f1f8621
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="design-configurations-to-parse-incoming-documents-for-application-data-updates-er"></a>Konfiguratsioonide kujundus sissetulevate dokumentide sõelumiseks avalduse andmete värskendamiseks (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Protseduur näitab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone sissetuleva elektroonilise dokumendi sõelumiseks. Selles protseduuris selgitatakse, kuidas importida näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone ja neid kasutada sissetulevate elektrooniliste dokumentide sõelumiseks. Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.

Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. 

Need etapid saab lõpule viia ükskõik millise andmekomplekti abil. Enne alustamist laadige alla ja salvestage teemas „Sissetulevate dokumentide sõelumine avalduse andmete värskendamiseks“ (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents) loetletud failid. Failid on järgmised: EFSTA model.xml EFSTA format.xml Response1.xml Response2.xml Response3.xml, Response4.xml.

1. Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.
    * Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena. Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.  
2. Klõpsake valikut Aruandluse konfiguratsioonid.
    * Järgmise stsenaariumiga demonstreeritakse sissetulevate XML-vormingus elektrooniliste dokumentide sõelumisfunktsioone: ERP-rakendus (Dynamics 365 for Finance and Operations) taotleb andmeid veebiteenusest (nt http://efsta.org/ EFSTA finantsteenus) ja sõelub sissetulevad vastused, et värskendada sobival moel avalduse andmeid. Kõige tõhusamaks sõelumiseks kasutatakse üht ER-i vormingut olenemata eeldatavate sissetulevate XML-vormingus dokumentide erinevast struktuurist.   

## <a name="import-and-review-er-configurations"></a>ER-i konfiguratsioonide importimine ja ülevaatamine
Importige ER-i mudeli konfiguratsioon, mis sisaldab näidisandmemudelit, mis on mõeldud sissetuleva faili andmete talletamiseks.  
1. Klõpsake nuppu Vahetus.
2. Klõpsake nuppu Laadi XML-failist.
    * Klõpsake käsku Sirvi ja vali EFSTA fail model.xml.  
3. Klõpsake nuppu OK.
4. Valige puul väärtus „EFSTA mudel”.
5. Klõpsake valikut Kujundaja.
    * Vaadake üle imporditud andmemudeli struktuur. Pange tähele, et loetelu enumType määratletakse järgmist tüüpi teenuse vastuste tuvastamiseks: kande esitamise kinnituse saamiseks, viimase esitatud kande kohta teabe saamiseks ja toetamata vastusetüüpide tuvastamiseks.   
6. Laiendage puul väärtust „Vastus”.
    * Pange tähele, et juurüksus „Vastus” määratletakse selleks, et määrata, millist tüüpi andmeid tuleb toetatud teenuse vastusest hankida, et avalduse andmeid värskendada.   
7. Sulgege leht.
    * Impordite ER-i vormingu konfiguratsiooni, mis määrab, kuidas  sissetulevaid dokumente sõelutakse ER-i andmemudelisse andmete talletamiseks.   
8. Klõpsake nuppu Vahetus.
9. Klõpsake nuppu Laadi XML-failist.
    * Klõpsake käsku Sirvi ja vali EFSTA fail format.xml.  
10. Klõpsake nuppu OK.
11. Laiendage puul väärtust „EFSTA mudel”.
12. Valige puul väärtus „EFSTA mudel\EFSTA vorming”.
13. Klõpsake valikut Kujundaja.
14. Klõpsake nuppu Laienda/ahenda.
    * Pange tähele, et vormingus CASE elementi kasutatakse juurena ja see sisaldab kolme pesastatud elementi FILE, mis tähendab, et see vorming on loodud mitmes vormingus sissetulevate failide sõelumiseks.  
15. Valige puul väärtus „Vastused\Kande lõpuleviimine\TraC”.
    * Pange tähele, et esitatud kande vastus algab juurelemendist „TraC”.   
16. Valige puul „Vastused\Viimane kande taotlus\Tra”.
    * Pange tähele, et viimasena esitatud kande vastus algab juurelemendist „Tra”.   
17. Valige puul „Vastused\Ootamatu vastus\Tekst”.
    * Lisati kolmas element FILE pesastatud elemendiga TEXT, et tuvastada muud tüüpi vastuseid, mis erinevad ülalmainitust.   
18. Klõpsake nuppu Vormingu vastendamine mudeliga.
    * Mudeli vastendus sisaldab andmevoo definitsiooni, millega talletada sõelutud sissetuleva dokumendi üksikasju, kasutades andmemudeli üksusi.  
19. Klõpsake valikut Kujundaja.
20. Laiendage puul valikut „format”.
21. Laiendage puul valikut „format\Responses: Case(Responses)”.
    * Vaadake üle andmeallika „Vorming” struktuur. Pange tähele, et kõiki kolme vastusetüüpi pakutakse eraldi.   
22. Valige puul „format\Responses: Case(Responses)\aType”.
    * Lisati andmeallika üksus „aType”, et näidata vastuse tüüpi. See on seotud andmemudeli üksusega „Tüüp”.  
23. Klõpsake vahekaarti Kinnitused.
24. Valige puul „Type = format.Responses.aType”.
    * Pange tähele, et ER-i kinnitamine on konfigureeritud selleks, et teavitada kasutajat olukorrast, kui vastuse struktuur ei ühti kande esitamise kinnitusega või viimati esitatud kande teabega (toetamata vastuse puhul).   
25. Sulgege leht.

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a>Sissetulevate failide sõelumiseks konfigureeritud ER-i vormingu mudelivastenduse käitamine
Käivitate loodud mudeli vastendamise testimise eesmärgil, et vaadata, kuidas konfigureeritud ER-i vorming sõelub sissetulevaid teenuse vastuseid. See etapp kasutab erinevaid XML-faile, et simuleerida veebiteenuste vastuste eri tüüpe.   
1. Avage fail Response1.xml XML-lugeris, nt veebibrauseris. Pange tähele, et fail sisaldab lõpuleviidud kande kinnituse üksikasju (juurelement on „TraC”).   
2. Klõpsake nuppu Käivita.
    * Klõpsake käsku Sirvi ja vali fail Response1.xml.  
3. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et vastusetüüp on õigesti tuvastatud ja sõelutud (ERModelEnumDataSourceHandler#EFSTA model#enumType#C tähendab kande lõpuleviimise juhtumit).   
    * Avage fail Response2.xml XML-lugejas. Pange tähele, et fail sisaldab viimase lõpuleviidud kande teavet (juurelement on „Tra”).   
4. Klõpsake nuppu Käivita.
    * Klõpsake käsku Sirvi ja vali fail Response2.xml.  
5. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et vastusetüüp on õigesti tuvastatud ja sõelutud (ERModelEnumDataSourceHandler#EFSTA model#enumType#R tähendab süsteemi taaskäivitamise juhtumit).   
    * Avage fail Response3.xml XML-lugejas. Pange tähele, et faili algab juurüksusest TraZ ja seda struktuuri ei konfigureeritud ER-i vormingus.   
6. Klõpsake nuppu Käivita.
    * Klõpsake käsku Sirvi ja vali fail Response3.xml.  
7. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et vastusetüüp on õigesti tuvastatud kui toetamata (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Vastav teade lisati teabelogisse (ER-i kinnitamissätte kohaselt) ja enamik andmemudelist pole täidetud.   
    * Avage fail Response4.xml XML-lugejas. Pange tähele, et selle faili struktuur on peaaegu sama mis sõelutud failil Response1.xml, v.a juurelemendi „TraC” pesastatud elementide seeria.   
8. Klõpsake nuppu Käivita.
    * Klõpsake käsku Sirvi ja valige fail Response4.xml.  
9. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et vastusetüüp on õigesti tuvastatud kui toetamata (ERModelEnumDataSourceHandler#EFSTA model#enumType#U). Vastav teade lisati teabelogisse ja enamik andmemudelist pole täidetud. Selle põhjuseks ons ee, et ER-i vormingu praegune säte eeldab sissetuleva faili juurüksuse pesastatud elementide teatud jada.   
10. Sulgege leht.
11. Valige puul väärtus „Vastused\Kande lõpuleviimine\TraC”.
12. Väljal Pesastatud elementide sõelumise järjekord valige „Kõik”.
    * Väljal „Pesastatud elementide sõelumise järjestus” valige Mis tahes, et lubada XML-juurüksuse jaoks pesastatud elementide mis tahes seeria.  
13. Klõpsake nuppu Salvesta.
14. Klõpsake nuppu Vormingu vastendamine mudeliga.
15. Klõpsake nuppu Käivita.
    * Klõpsake käsku Sirvi ja valige fail Response4.xml.  
16. Klõpsake nuppu OK.
    * Vaadake loodud väljundit. Pange tähele, et vastusetüüpi on nüüd tuvastatud õigesti failiga Response1.xml võrdsena.  


