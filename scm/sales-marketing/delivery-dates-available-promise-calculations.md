---
title: Tellimuse lubamine
description: "See artikkel käsitleb tellimuse lubamist. Tellimuse lubamine aitab teil usaldusväärselt tarnekuupäevi klientidele lubada ja annab teile paindlikkuse, et saaksite neid kuupäevi täita."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8aa0a58b03ee18e42ca7770ea3e22311c1ddba67
ms.lasthandoff: 03/31/2017


---

# <a name="order-promising"></a>Tellimuse lubamine

See artikkel käsitleb tellimuse lubamist. Tellimuse lubamine aitab teil usaldusväärselt tarnekuupäevi klientidele lubada ja annab teile paindlikkuse, et saaksite neid kuupäevi täita.

Tellimuse lubamine arvutab varaseimad lähetamise ja vastuvõtmise kuupäevad ning põhineb tarnekuupäeva kontrollimeetodil ja transpordipäevadel. Saate valida nelja tarnekuupäeva kontrollimeetodi vahel.

-   **Müügi** – müügi täitmisaeg on ajavahemik müügitellimuse loomine ja kaupade lähetamine. Kohaletoimetamise kuupäeva arvutamine põhineb vaikimisi mitu päeva ja ei pea varude kättesaadavuse, tuntud nõue või plaanitud tarne.
-   **ATP (saadaval lubamiseks)** – ATP on kaup, mis on saadaval ja saate lubas kliendile kindlal kuupäeval. ATP arvutamine sisaldab kehtestamata laosaldot, täitmisaegu, plaanitud sissetulekuid ja väljaminekuid.
-   **ATP + väljamineku ohutusvaru ** – tarnekuupäev on võrdne ATP kuupäevaga pluss kauba väljamineku ohutusvaru. Väljamineku ohutusvaru on aeg, mis on vajalik kaupade saatmiseks ettevalmistamiseks.
-   **CTP (lubamiseks võimeline) **– saadavus arvutatakse koosnevusarvutuse abil.

## <a name="atp-calculations"></a>ATP arvutused
ATP kogus arvutatakse "kumulatiivne ATP etteplaneerimise" meetodi abil. Selle ATP arvutamise meetodi peamine eelis on lennukitega küsimustest sissetulekute summa on rohkem kui viimase sissetuleku (näiteks kogus varasemat kättesaamist tuleb kasutada nõue). "Kumulatiivne ATP etteplaneerimise" arvutamise meetod hõlmab kõiki küsimusi enne kumulatiivne kogus, väljastamise kumulatiivne kogus. Seetõttu hindab see ATP arvutusmeetod, kas mõne varasema perioodi kogust saab hilisemas perioodis kasutada.  

ATP kogus on esimese perioodi kehtestamata laosaldo. Tavaliselt arvutatakse see iga perioodi kohta, milles sissetulekut plaanitakse. Programm arvutab ATP perioodi päevades ja arvutab praeguse kuupäeva esimeseks ATP koguse kuupäevaks. Esimeses perioodis sisaldab ATP vaba kaubavaru, millest on lahutatud tähtajalised või tähtaja ületanud klienditellimused.  

ATP arvutamiseks kasutatakse järgmist valemit.  

ATP = ATP eelmise perioodi + sissetulekute praeguse perioodi-probleemid praeguse perioodi – Väljalaske puhasväärtuse koguse iga tulevase perioodi kuni perioodi, millal kõikide tulevaste perioodide, kuni ja kaasa arvatud tulevase perioodi kohta ületab küsimusi summa kuni ja sealhulgas tulevase perioodi.  

Kui rohkem väljaminekuid ja sissetulekuid ei ole, on järgmiste kuupäevade ATP kogus sama, mis viimane kalkuleeritud ATP.  

Kui kõiki kaubale kasutatud dimensioonide ei ole ATP kontrolliks esitatud, võidakse need siiski määrata väljaminekutele ja sissetulekutele. Sel juhul peavad ATP arvutamisel olema väljaminekud ja sissetulekud olemasoleva dimensiooniga liidetud, et vähendada ATP arvutuses kasutatavaid väljaminekute ja sissetulekute ridasid.  

Kuvatav ATP kogus on alati suurem kui 0 (null) või sellega võrdne. Kui arvutus tagastab negatiivse ATP koguse (nt kui eelnevalt lubatud kogus ületab saadaoleva koguse), määrab programm koguseks automaatselt **0**.

### <a name="example"></a>Näide

Väli **ATP tagasiulatuv nõudluse ajapiir** juhib, kui kaugele hilinenud nõudluse tellimuste või lao väljaminekute otsimisel ajas tagasi minnakse. Väli **ATP tagasiulatuv tarne ajapiir** juhib, kui kaugele hilinenud tarnetellimuste või lao sissetulekute otsimisel ajas tagasi minnakse. Näiteks kui tellimusi, mis on hilinenud ainult seitse päeva, peaks ATP arvutamisel arvestama, tuleb mõlemale väljale määrata väärtus **7**.  

Väljad **ATP hilinenud nõudluse viivituse aeg** ja **ATP hilinenud tarne viivituse aeg** juhivad, millal hilinenud nõudlust või tarnet ATP arvutamisel arvestatakse. Näiteks kui hilinenud tarnet ja nõudlust tuleks arvestada ATP arvutamisel ülehomme, tuleb mõlemale väljale määrata väärtus **2**. Väärtus **2** tähendab, et kauba kogust hilinenud ostutellimusel, mida ATP arvutamisel arvestada tuleks, nähakse saadaval olevana kaks päeva pärast praegust kuupäeva.  

Järgmises näites sisestatakse **7** väljadele **ATP tagasiulatuv nõudluse ajapiir** ja **ATP tagasiulatuv tarne ajapiir** ja **1** sisestatakse väljadele **ATP hilinenud nõudluse viivituse aeg** ja **ATP hilinenud tarne viivituse aeg**.  

Ostutellimust 200 tooteühikule, mis oleks pidanud jõudma kohale kolm päeva tagasi, pole veel vastu võetud. Seetõttu pole müügitellimuse rida sama toote 75 ühikule, mis oleks tulnud eile teele panna, veel teele pandud.  

Klient helistab ja soovib tellida 150 ühikut sama toodet. Kui kontrollite toote saadavust, siis leiate, et teine ostutellimus 100 tooteühikule tarnitakse 10 päeva hiljem.  

Loote tootele müügitellimuse rea ja sisestate koguseks **150**.  

Kuna tarnekuupäeva kontrollimismeetod on ATP, arvutatakse ATP andmed varaseima võimaliku lähetuskuupäeva leidmiseks. Vastavalt sätetele, peetakse hilinenud ostutellimuse ja müügitellimuse ja praeguse kuupäeva tekkinud ATP kogus on 0. Homme, kui hilinenud ostutellimuse peaks laekuma, ATP kogus arvutatakse üle 0 (sel juhul arvestatakse 125). Kuid 10 päeva alates nüüd, kuna täiendavaid ostutellimuse 100 ühikut peaks laekuma, ATP kogus muutub rohkem kui 150.  

Seetõttu lähetuskuupäev on seadistatud 10 päeva pärast, vastavalt ATP arvutamisel. Seetõttu saate kliendile öelda, et soovitud koguse saab tarnida 10 päeva pärast.


