---
title: "Finantsperioodi sulgemise tööruum"
description: "Selles artiklis antakse ülevaade finantsperioodi sulgemise tööruumist ja sellega seotud konfiguratsioonist."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerPeriodCloseProjectWorkspace
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13791
ms.assetid: 6ee51758-639b-448e-9cb2-56cf1d804273
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ba0d709d123f56edb2a5287376c06c1f41181b1c
ms.lasthandoff: 03/31/2017


---

# <a name="financial-period-close-workspace"></a>Finantsperioodi sulgemise tööruum

Selles artiklis antakse ülevaade finantsperioodi sulgemise tööruumist ja sellega seotud konfiguratsioonist.

Finantsperioodi sulgemise tööruum

Selle **majandusperioodi lähedal** tööruum võimaldab jälgida ettevõtete, piirkondade ja inimeste rahaline sulgemise protsessi. Sõltuvalt teie arvates on **majandusperioodi lähedal** tööruumi, näete kas kõik ülesanded ja staatused sulgemise ajakava või teile määratud ülesanded. 

Esmalt valige sulgemise ajakava tööruumi ülaservas. Kõik andmed, mis on näidatud tööruumi filtreeritakse seejärel valitud sulgemise ajakava.

### <a name="summary-tiles"></a>Kokkuvõttepaanid

Paanid **Kokkuvõte** annavad ülevaate protsessist ja näidikud aitavad teil sulgemise protsessi jälgida. Näete ülesandeid, mis on viimase tähtaja, ülejäänud ülesannete täna, ülesanded, mille tähtaeg on täna, kuid blokeerib sõltuvuste tõttu ja kõik ülejäänud toimingud protsessi. See teave on kõik ettevõtted, mis sisalduvad valitud sulgemise ajakava.

### <a name="tasks-and-status-section"></a>Ülesannete ja oleku jaotis

Aastal ning **ülesannete ja staatuse** jagu, üldine seisund sulgemise ajakava on jaotatud mitmeti: staatus, staatuse lõikes, ja seisund, vastutava isiku. Saate vaadata olekut, sest kõik ülesanded sulgemise ajastamine, lihtsalt ülesanded, mille tähtaeg on täna, või ülesandeid, mis on ületanud muutes filtri kaart nimekirja ülaosas. Võite valida ka firma filtri oleku vaatamiseks konkreetse ettevõtte. Iga vahekaardi olek annab jaotatuna lõppu protsendile ja ülesandeid, mis jäävad. Klõpsake kaarti või **andmete** tegevuse üksikasjaliku tööülesannete loendi filtreerimiseks valitud kaardi. 

Viimase sakk on üksikasjaliku tööülesannete loendi. See nimekiri näitab täielikku tööülesandeloendis ja saate filtreerida nii, et see näitaks ainult ülesandeid, mis teid huvitab. Saate filtreerida mitmel viisil tööülesandeloendis. Näiteks saate filtreerida tööülesande tähtaeg, äriühingu ja seotud aladel. Samuti saate kuvada või peita lõpuleviidud tööülesandeid võib tööülesannete loendi. 

Ülesannete puhul kasutatakse kahte järgmist näidikut.

-   Hüüumärk ikoon näitab, et ülesanne on ületanud. Ülesandeid, mis on ületanud, tähtaeg on ka punasega.
-   Tabaluku ikoonil näitab, et ülesanne sõltub muid ülesandeid, mis ei ole veel lõpule. Ülesanne, mis blokeerib sõltuvuste ei saa märkida lõpuleviiduks. Saate ülesande sõltuvuste abil on **sõltuvuse määra** tegevus.

Toimingu nimi on Microsoft Dynamics 365 toimingute lehele või muu veebilehe hüperlingi, kui kasutaja peab käima töödega valmis. Saate määrata selle hüperlingi abil on **tööülesande link** välja kui redigeerida või luua tööülesande. 

Saate manustada faile, märkmeid, pilte ja URL-ide ülesande abil on **manuseid** tegevus. Näiteks saate viidata töölehe koodi, mida kasutatakse osa, kommentaare kohta teatud töö või ülesande prinditud aruanne faili. Ikoon kuvatakse ka **manuse** kui manuse ülesande veerg. 

Selle **ülesande lõpule** võimalus tuleb käsitsi valida pärast selle tööülesande lõpuleviimist. Kui tööülesanne on märgitud lõpuleviiduks, kui **täita kuupäev** väli uuendatakse automaatselt praegune kuupäev ja kellaaeg. Sõltuvus näitajad ka uuendatakse vastavalt vajadusele.

## <a name="all-financial-period-close-tasks-list-page"></a>Kõigi finantsperioodi sulgemisülesannete loendi leht
Kuvatakse kõik praeguse ja eelmise perioodi tihedas ülesanded: selle **kõik perioodi sulgeda ülesannete** loendi lehel. Selle loendi lehel on kõige otstarbekam kasutada ajaloolise analüüsi oma sulgumist, sest see sisaldab teavet regulaar tähtaeg, tegeliku lõpetamise kuupäev ja täitnud ülesande. Saate eksportida lihtsalt selle nimekirja leheküljel Microsoft Excel aruandluse ja kontrollimise eesmärgil.

## <a name="financial-period-close-configuration-page"></a>Finantsperioodi sulgemiskonfiguratsiooni leht
Enne kasutamist on **majandusperioodi lähedal** tööruumi, tuleb konfigureerida protsess Microsoft Dynamics 365 operatsioonide abil on **rahalise perioodi tihedas konfiguratsiooni** lehel. (Klõpsake **PR**&gt;**perioodi sulgeda**&gt;**rahalise perioodi tihedas konfiguratsiooni**.)

### <a name="resources"></a>Ressursid

Kohta ning **ressursside** jaotises saate määratleda inimesed, kes on sulgemise protsessidega seotud. Esmalt tuleb siin määrata töötaja, kes vastutab ülesande sulgemise. Määrake töötaja tööruumi ülevaate ka. Valikud on järgmised:

-   **Ainult määratud ülesanded** – kasutaja näeb ainult talle määratud ülesandeid.
-   **Kõik ülesanded ja olek** – kasutaja näeb kõiki sulgemisülesandeid ja üldise protsessi olekut.

Kasutajad, kellel on õigus vaadata ainult neile määratud ülesandeid, ei saa ülesandeid ülesannete loendisse lisada, neid redigeerida ega ülesannete loendist eemaldada.

### <a name="task-areas"></a>Ülesande alad

Kasutate ülesande alasid sulgemisülesannete grupeerimiseks teie organisatsiooni omandiõiguse loogilistesse aladesse. Näiteks võib ülesande aladena kasutada suvandeid Ostureskontro, Müügireskontro või Pearaamat.

### <a name="calendars"></a>Kalendrid

Luua ja redigeerida rahalise sulgemise kalendreid kasutades menüüd fail.  See on, kus määratletakse sulgemisel tööpäeva ja kasutab sulgemise toimingute ajastamiseks.  Loo uus kalender ning märkida ülesanne planeerimisel kasutatakse tööpäeva.  See on parim kalendri loomiseks pika aja jooksul, näiteks aasta või mitu aastat, kuna seda saate pärast loomist redigeerida.  Pärast kalendri loomist klõpsake nuppu Muuda värskendada kindla päeva, nagu pühad.  Ülesannete sulgemine planeeritakse päeva Millal juhtelement väärtuseks on seatud avatud.  Kui ülesannete sulgemine ei tohiks ajakava kindlal päeval, sel päeval peaks olema seatud suletud kontrollväärtust.

### <a name="templates"></a>Mallid

Rahaline tihedas malli abil saate määratleda kõik ülesanded, mis on osa sulgemise protsess. Sulgemise ülesandeks on korduva tööle asumiseks täita iga sulgemise käigus määratud isik. Malli, suhteline tähtaeg tuleb määratleda iga tegumi sulgemine. Suhteline tähtaeg on päevi enne või pärast kindlaksmääratud perioodi lõpu kuupäev, millal ülesande tähtaeg iga perioodi. Tähtaja kellaaeg määratakse samuti kõikidele. Tähtaja kellaaeg on seatud ajavöönd raames abil ja teisendatakse iga kasutaja jaoks. 

Ülesande malli saate määrata ühele või enamale äriühingule, kui selle ülesande täitmisel kohaldatakse. Kui teise isiku määratakse selle tööle asumiseks iga äriühingu lõpetamiseks, te võite leida selle kasulik luua mitu ülesannet sama tööle asumiseks. Looge iga ettevõtte puhul üks ülesanne. 

Selle **tööülesande link** menüükäsk on seotud ülesande tööle asumiseks ja saab minna otse seostatud lehekülg tööruumi link ülesanne. Näiteks sulgemise toimingu käivitada valuuta ümberhindamise protsessi maksmata arvete liidetav ühendamiseks seotud **välisvaluuta ümberhindluse** lehel Microsoft Dynamics 365 toiminguteks. Saate siduda ka välise URL-iga. 

> [! Vihje] kui soovite linkida mõne kindla juhtimise Reporter aruande rahalise perioodi tihedas ülesanne, saate aruande URL. Aruande URL avamiseks avage aruanne Aruandekujundaja ja seejärel klõpsake **faili**&gt;**aruannet** aruande avamiseks veebibrauseris. Seejärel saate brauseri aadressiribalt URL-i kopeerida ja kleepida selle väljale **Ülesande link** **URL**. 

Malli saate määratleda ülesande sõltuvused. Kui tööülesanne on loodud sõltub üks või rohkem, ei saa see ülesanne tähistatud kui lõpetatud enne kõik sõltuvused on täidetud. 

Saate luua mitu rahalise tihedas malle. Seejärel saate erinevate jälgida sulgemise protsesside perioodi erinevate nagu kuu lõppu või aasta lõpus, või ettevõtted, mis kasutavad erinevaid sulgemise protsesside jälgimiseks. Üks mall on loodud, saate kopeerida uus mall ja teha vajalikud muudatused. Määrake ainult üks Mall iga sulgemise ajakava.

### <a name="closing-schedules"></a>Sulgemisgraafikud

Sulgemise ajakava saate rahalise tihedas malli määrata kindlaks rahalise ajavahemikuks, mis tuleb sulgeda. Ülesannete mallist seejärel luuakse automaatselt kindlaksmääratud ajal ja uue sulgemise ajakava lisatakse tööruumi. Kui loote uue sulgemise ajakava, ning **järgneval päeval** välja abil kindlaks tegelikust tähtajast sulgemistegevusi, suhteline tähtaeg vastavalt kuupäevad kuupäev, millal määratakse rahaline tihedas malli. 

Määrata sobiv sulgemise ajakava tähistamiseks kasutatakse ülesanne sõiduplaani tööpäeva kalender. Kui te ei määratle täpse ajakava, tööülesande tähtaega kuupäevad on kasutada kogu päeva nädalas. 

Samuti tuleb määratleda ettevõtteid, mis ühendatakse sulgemise ajakava. Kui malli omistatud mitmele ettevõttele, luuakse iga ettevõtte on sulgemise ajakava ja määratud malli ülesanne eri ülesanded. 

Pärast sulgemise ajakava on valmis, valige selle **suletud** valida see. Tööülesande ajalugu on siiski saadaval ka **kõik perioodi sulgeda ülesannete** loendi lehel, kuid sulgemise ajakava eemaldatakse tööruumist. Pärast sulgemise ajakava märgitud **suletud**, ei saa ülesandeid lisada, redigeerida ülesannete või toimingute eemaldamiseks.


