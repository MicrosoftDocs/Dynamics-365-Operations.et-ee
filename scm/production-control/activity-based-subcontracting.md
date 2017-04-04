---
title: "Tegevuspõhine alltöövõtu"
description: "Selles teemas kirjeldatakse üksikasjalikult, kuidas kasutada allhankijana tootmise voolu kulusäästlik töötamine."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 8e57c53ca894aa44b71e15c1f66bd7c722ea8a81
ms.lasthandoff: 03/31/2017


---

# <a name="activity-based-subcontracting"></a>Tegevuspõhine alltöövõtu

Selles teemas kirjeldatakse üksikasjalikult, kuidas kasutada allhankijana tootmise voolu kulusäästlik töötamine.

Microsoft Dynamics 365 toiminguteks on kaks lähenemist alltöövõtuga: tootmistellimuste ja kulusäästlik töötamine. Kulusäästlik töötamine lähenemisviisi modelleeritud allhange töö teenusena, seotud tegevust tootmise voolu. Eri tüüpi kulude rühma tüüp nimega **vahetut välistõlgete tellimist** sisse viidud ja selle betoonitööde ei ole enam osa koosluse (BOM). Kuluarvestuse alltöövõtu töö on täielikult integreeritud kulusäästlik töötamine maksavad lahendus.

## <a name="production-flows-that-involve-subcontractors"></a>Tootmise vood, mis on seotud alltöövõtjad
Tootmise voolu põhimõtet ei muutuks tegevuse rakendamiseks on sõlmitud allhankeleping. Materjal ikka voolab asukoha vahel, protsessi tegevuse teisendada materjali tooted ja tegevused liikuda materjali või tooteid ühest kohast teise. Mudel asukohad ja tööta lahtrid hankija hallatavas määrate hankijakood, lattu või ressursirühmi ressurss.  

Vastavalt neid oskusi, kulusäästlik töötamine ei nõua mingeid eripärasid materjali ja toodete liikumise toetamiseks. Kõik võimalikud stsenaariumid, mis on seotud müüjad nagu tootmis- või transpordi teenuste osutajatele saab modelleerida põhineb tootmisprotsesside ja arhitektuur.  

Näiteks töötab alltöövõtja alltöövõtja asub toidukauplus kokku. Kui ventilatsiooniseadmetel on tühjendada alltöövõtja, tagastada kanban kaart koos järgmine lahter assamblee. Seejärel täiendatakse kell alltöövõtja supermarket. Ülekanded ja sealt alltöövõtja võib modelleerida nagu otsene edastamine komplekteerimine ja saadetise lähetamises toetamiseks. Kui selgesõnalise registreeringu ei pea füüsiliselt transportides toetamiseks, üleandmise tegevuse võib ära jätta.  

Alltöövõtja saab koormuse tasakaalu tootmise voolu üldist suutlikkust. Näiteks tootmise voolu modelleeritud ajastatud kanban reeglite abil. Planeerija kasutab planeerimise ajakava ja koormuse tase kanban mõlemas lahtris töö nõudmisel. Planeerija jälgib ka supermarket konsolideeritud tarnimise ajakava kohta on **tarnimise ajakava** lehel. Mitu alltöövõtjate saab modelleerida ühe või mitu tootmise voolude ja võib esineda mitu kanban reeglid, mida saab kasutada sama toodet eri tegevuste kaudu samasse asukohta pakkuma. Planeerija saate teisendada kanbans alternatiivsete kanban reegel ajatada kanban, mis loodi algselt toote alternatiivsed protsessi. Tegelikult alltöövõtu laadi töö lahtrit ei mõjuta tootmise voolu. Töö see kehtib kahe paralleelse töösisekorra lahtri või kahte alltöövõtu lahtrisse.   

Tootmise voolu muude tegevustega, nagu allhankijana tarbida ja tarnida surnukstunnistamise, töötada inventarinimekirjadesse kandmata (lõpetamata töö \[lõpetamata toodangu\]), ja pool materjale ja tooteid. Igal juhul planeerimine ja täitmise allhankijana protsessid on samad. Lisaks need samad protsessid sisemise töö protsessi.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Müügiprotsessi allhankijana (teenused)
Allhankijana ostu protsess põhineb füüsilise sisendite, nt kanban töö areng, registreeritud, alustada või lõpetada. Rahaline vool, näiteks alltöövõtu tööde maksumus on sekundaarse voolu, mis järgneb tegelikku liikumist. Samal ajal ostu protsess on sõltumatu protsess, mis võimaldab käsitsi täpsustamist ostudokumentide igal sammul. Siin on müügiprotsessi lepingulised tegevused:

1.  Luua ostu-müügileping. Müügileping on loodud teenuse ja seotud tegevust tootmise voolu.
2.  Looge ostutellimus. Ostu väljalaskeorderi loomist teenuse vastavalt planeeritud kanban töökohti. Töö sama teenuse rühmitamiseks ostutellimuse ridadele, päeva, nädala või kuu. Ridade loomist pärast kanban töökohtade loomine. Pärast seda saab luua ostutellimuse read. See tavaliselt valik kui alltöövõtja osutab täiendavaid teatamata, põhineb kanbans või kanban kaardid, mida alltöövõtja saab. Sel juhul on võimalik minimeerida kõrvalekalded ostutellimuse ja arve vahel.
3.  Tekitada kanban kaardid, materjali ja komplekteerimislehe saata alltöövõtja valmistada töötlemiseks. Vastavalt tootmise voolu Detailne modelleerimine, koostamisel on tehtud kanban juhatuse protsessidega seotud tegevuste komplekteerimislehe ja ettevalmistamise funktsiooni abil. Teise võimalusena tehakse kasutades komplekteerimislehe ja alustamise või lõpetamise kanban juhatuse ülekandmise töö ettevalmistamine. Inventarinimekirjadesse kantud materjali korral võib toetada mõlemad protsessid WMS korjamine ja saadetise lähetamises. Nõudmisel saab luua veokirja.
4.  Luua kanban ventilatsiooniseadmetel ja kanban kaardid. Töötlemisel saadud kaardid on tagastanud alltöövõtja. Kaardid sisaldavad tavaliselt, kättetoimetamisteatis, mis määrab füüsilise materjali, mis on juba lähetatud. Osutatavate teenuste viide ei ole nõutav. Materjali või toote kliendi saabumist registreeritakse kanban pardal, sõltuvalt kanban kaardid. (Kanban juhatuse protsessi tegevuseks või ülekandmise töö kanban juhatuse kasutatakse, olenevalt modelleeritud tegevuste.).
5.  Luua tarne nõuandev. Selle nõuandva kasutatakse asendada on saatelehe dokumendi saadud teenuste eest. Kätte teated majandustarkvara vastavalt täidetud kanban töökohti allhange tegevuseks valitud perioodil. Iga töö saamise teated luuakse seotud ostutellimuse rea. Nõuandva kätte saaks trükkida ja saatnud allhankijale kättesaamistõendi.
6.  Loo arve.

Protsess lõpeb alltöövõtja arveldamisel jooksul. Arve mängu teha vastu kviitungi teateid, mis on loodud. Kätte teated kujuta täpse füüsilise sissetuleku materjali, kolm-viis sobitamine on lihtsustatud.

## <a name="configuring-activities-for-subcontracting"></a>Alltöövõtuga tegevuste seadistamine
Järgmistes punktides kirjeldatakse, kuidas seadistada tegevuse alltöövõtuga.

### <a name="subcontracted-services"></a>Allhankelepinguid teenuste

Makse mida kasutatakse tegevuspõhise alltöövõtu peab olema toode, mis on järgmised omadused:

-   **Toote tüüp:** teenus
-   **Laomudeligrupi:** Non varuta

See nõue jõustab esimene kasutamine on esimene FIFO Laomudel. **Märkus:** toodete omahinna arvutamine nõuab määratleda teenuse standardkulu. Hankija lepingu nõutakse. Muul juhul teenust ei saa kasutada tegevuspõhise alltöövõtuga.

### <a name="subcontracted-process-activities"></a>Alltöövõtu protsessidega seotud tegevuste

Protsessi tegevuse alltöövõtu tegevusena konfigureerimiseks toimige järgmiselt.

1.  Konfigureerige alltöövõtu töö lahtrit. Töö raku nagu allhankeleping konfigureerimiseks peate looma ressurss on **hankija** tüüp ja siduda selle töö raku (ressursirühma). Käitusaja kulukategooria kohta ning **vahetut välistõlgete tellimist** kulu tüüp tuleks määrata töö lahtrit. Kulukategooriate seadistamine ja kogus ei ole vajalik.
2.  Pärast protsessi aktiivsus on loodud ja alltöövõtu töö lahtrit seotud, peate konfigureerima teenuse tegevuse enne tootmise voolu versioon aktiveerimist. Selle juhise kohta ning **tegevuse****andmed** lehel. Tegevuseks, mis on seotud alltöövõtu töö lahtrit, mille **teenuse tingimuste** FastTab näidatakse. Lisage see FastTab vaiketeenus, mis kehtib kogu toodangu kaupade puhul. Kui konkreetsete kaupade erinevate teenuste ja erinevate teenuse arvutuse parameetrid (nt erinevaid suhe), saate lisada muud teenused tegevuse.

## <a name="subcontracted-transfer-activities"></a>Alltöövõtu tegevused
On tegevusele on konfigureeritud alltöövõtu tegevusena, sõltuvalt selle **Freighted poolt** seadmine tegevuse üle. Valikud on järgmised:

-   **Saatja** -tegevus on allhankeleping kui lattu üleviimine haldab hankija (nagu on määratletud atribuudiga ladu). Kõik valitud ostulepingud teenused peavad olema sama tarnija ID ladu.
-   **Saaja** – tegevus on allhankeleping kui ülekanne lattu haldab hankija (nagu on määratletud atribuudiga ladu). Kõik valitud ostulepingud teenused peavad olema sama tarnija ID ladu.
-   **Vedaja** – tegevus on suhtes mis tahes teenuse pakkuja sõlmida allhankelepinguid. Osalema vedaja peab loodud varade ja peab olema määratud hankija konto.

Protsessidega seotud tegevuste, nagu peate konfigureerima vaiketeenust alltöövõtu tegevused on **teenuse tingimused** FastTab ja selle **tegevuse****üksikasjad** lehekülg.

## <a name="service-quantity-calculation"></a>Teenuse koguse arvutamine
Kogu müügiprotsessi põhineb kauba viide teenuse eest. Selle üksuse viide mõõdetakse teenuse mõõtühik. Teenuste mõõdetakse tavaliselt teenuste (üksuste) arv ega aeg. Teenuse kogus, vastavalt registreeritud lõppemisel kanban töökohti, kasutage järgmisi meetodeid:

-   **Arvutus, mis põhineb töökohtade arv** – ühe kanban töö võrdub *n* üksuste kohta, sõltumata toodete kogus, mis on saadaval. Kulusäästlik töötamine, ühe töö vastab üks käitlemise üksuses. See arvutusmeetod kehtib kõiki teenuseid, mis on eest käitlemise üksuses. Seda meetodit kasutatakse seetõttu tavaliselt tegevusi edasi. Aga see võib ka otsust protsessi töödelda kogu ventilatsiooniseadmetel.
-   **Arvutamise aluseks oleva toote kogus** – teenuse kogus on võrreldes on planeeritud/tarnitud tootekogus. Tarnitud toote koguse arvutamisel viga kogused võivad kas või. See arvutusmeetod kehtib kõikidel juhtudel, kui töödeldud toote ühiku teenuse hind on kokku lepitud.
-   **Arvutus, mis põhineb tegevuse aeg** – arvutatakse teoreetilise tegevuse korda, töötlemise aja tegevusele kogu töödeldud koguse ja töödeldud toote läbilaskevõime suhe. See arvutusmeetod kehtib tund maksab teenuste ja on dispersioon ajal töödeldud toote kohta.

## <a name="cost-accounting-of-subcontracted-services"></a>Kuluarvestuse allhankelepinguid teenuste
Nõustamise saamise või sisestamisel ostutellimuse kohta tootmisprotsesside (teisisõnu, ostutellimus loodi põhineb kanban tööd alltöövõtu) loodi hankija konteerimisel sissetuleku väärtus aastal lõpetamata toodangu kontod tootmise voolu. Kõrvalekaldeid arved kajastatakse ka tootmise voolu. Kulukategooria alltöövõtu töö on kasutusele võetud. Kulukategooria võimaldavad läbipaistva jälgida alltöövõtu töö, mis on eraldatud lõpetamata toodangu ja tarbimise, mil väärtust.  

Tagasivool omahinna arvutamist lean tootmise omahinna arvutamise perioodi lõpus arvutab tegeliku dispersiooniga, mis toodetakse voolu tootmise omahinna arvutamise perioodi jooksul.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Modelleerimine ülekandeid kui alltöövõtu
Inimesed leiavad sageli transpordi mittetootlike ja arvan, et see lisab väärtust. Alltöövõtu kulud võrreldes tootmise maksumust pidada transpordi kulud. Tootmisprotsesside, hõlmab eri kohtades ja vajava teenuseid tuleks mudel transpordikulude osa maksumus kliendile toodete tarnimisel. 

Tegevuspõhine Metallitööstusele kulusäästlik töötamine võimaldab teil integreerida vedajate ja transportida müüjad, et liikuda materjali ja toodete tootmise voolu asukoha vahel. Modelleerimine on tegevusele, mida saate määrata vedaja või hankija. Tegevus/töö üleandmise põhineb teenuseid ja ostu lepingu ja saate luua ostutellimused ja saamise teateid, vastavalt tegelikku tööd. See funktsioon on sama funktsionaalsus alltöövõtu protsessi tegevusi.  

Seetõttu Dynamics 365 operatsioonide nüüd toetab Koosluse kalkulatsiooni, mis sisaldab teenuste loomine seotud ostutellimuste, integreeritud saamise registreerimise, ja võtta transporti teenuse kulusid arvesse tootmise voolu omahinna.


