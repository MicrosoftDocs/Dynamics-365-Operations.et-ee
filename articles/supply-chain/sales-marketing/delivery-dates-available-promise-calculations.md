---
title: Tellimuse lubamine
description: "See artikkel käsitleb tellimuse lubamist. Tellimuse lubamine aitab teil usaldusväärselt tarnekuupäevi klientidele lubada ja annab teile paindlikkuse, et saaksite neid kuupäevi täita."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesATP, SalesAvailableDlvDates
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 193933
ms.assetid: 676fc53a-fa25-4688-9f26-1005316763b8
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2c0b31f6e51de4489a35dbd91a6e9886e620f421
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="order-promising"></a>Tellimuse lubamine

[!include[banner](../includes/banner.md)]


See artikkel käsitleb tellimuse lubamist. Tellimuse lubamine aitab teil usaldusväärselt tarnekuupäevi klientidele lubada ja annab teile paindlikkuse, et saaksite neid kuupäevi täita.

Tellimuse lubamine arvutab varaseimad lähetamise ja vastuvõtmise kuupäevad ning põhineb tarnekuupäeva kontrollimeetodil ja transpordipäevadel. Saate valida nelja tarnekuupäeva kontrollimeetodi vahel.

-   **Müügi täitmisaeg** – müügi täitmisaeg on müügitellimuse koostamise ja kaupade lähetamise vaheline aeg. Tarnekuupäeva arvutamine põhineb päevade vaikearvul ega arvesta saadavust laos, teadaolevat nõudlust või plaanitud tarnet.
-   **ATP (saadaval lubamiseks)** – ATP on kaubakogus, mis on saadaval ja mida saab kliendile konkreetsel kuupäeval lubada. ATP arvutamine sisaldab kehtestamata laosaldot, täitmisaegu, plaanitud sissetulekuid ja väljaminekuid.
-   **ATP + väljamineku ohutusvaru** – tarnekuupäev on võrdne ATP kuupäevaga pluss kauba väljamineku ohutusvaru. Väljamineku ohutusvaru on aeg, mis on vajalik kaupade saatmiseks ettevalmistamiseks.
-   **CTP (lubamiseks võimeline)**– saadavus arvutatakse koosnevusarvutuse abil.

## <a name="atp-calculations"></a>ATP arvutused
ATP kogus arvutatakse meetodil „kumulatiivne plaanitav ATP”. Selle ATP arvutamise meetodi peamiseks eeliseks on see, et selle abil saab käsitleda juhtumeid, kus väljaminekute summa sissetulekute hulgas on suurem kui viimane sisstulek (näiteks kui nõude täitmiseks tuleb kasutada varasema sissetuleku kogust). Arvutusmeetod „kumulatiivne plaanitav ATP” sisaldab kõiki väljaminekuid, kuni kumulatiivne vastuvõetav kogus ületab kumulatiivse väljastatava koguse. Seetõttu hindab see ATP arvutusmeetod, kas mõne varasema perioodi kogust saab hilisemas perioodis kasutada.  

ATP kogus on esimese perioodi kehtestamata laosaldo. Tavaliselt arvutatakse see iga perioodi kohta, milles sissetulekut plaanitakse. Programm arvutab ATP perioodi päevades ja arvutab praeguse kuupäeva esimeseks ATP koguse kuupäevaks. Esimeses perioodis sisaldab ATP vaba kaubavaru, millest on lahutatud tähtajalised või tähtaja ületanud klienditellimused.  

ATP arvutamiseks kasutatakse järgmist valemit.  

ATP = eelmise perioodi ATP + praeguse perioodi sissetulekud – praeguse perioodi väljaminekud – netoväljamineku kogus iga tulevase perioodi jaoks kuni periood, millal kõikide tulevaste perioodide sissetulekute summa (kuni tulevaste perioodideni ja need kaasa arvatud) on suurem kui väljaminekute summa (kuni tulevaste perioodideni ja need kaasa arvatud).  

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

Kuna tarnekuupäeva kontrollimismeetod on ATP, arvutatakse ATP andmed varaseima võimaliku lähetuskuupäeva leidmiseks. Sätete põhjal arvestatakse hilinenud ostutellimust ja müügitellimust ning saadud ATP kogus praeguse kuupäeva kohta on 0. Homme, kui hilinenud ostutellimus peaks kohale jõudma, arvutatakse ATP koguseks rohkem kui 0 (praegusel juhul arvutatakse selleks 125). 10 päeva pärast, kui oodatakse täiendava 100 ühikuga ostutellimuse saabumist, saab aga ATP koguseks rohkem kui 150.  

Seetõttu määratakse tarnekuupäevaks ATP arvutuse alusel 10 päeva alates tänasest. Seetõttu saate kliendile öelda, et soovitud koguse saab tarnida 10 päeva pärast.




