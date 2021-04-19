---
title: Tegevustepõhised allhanked
description: Selles teemas kirjeldatakse üksikasjalikult, kuidas kasutada allhanketegevusi kulusäästlikus tootmisvoos.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, PlanActivity, ReqSupplyDemandSchedule, PlanActivityServiceDetails, PlanActivityServiceWizard
audience: Application User
ms.reviewer: kamaybac
ms.custom: 267034
ms.assetid: 15c76a51-fa6d-42d2-994a-c67df6bae6a9
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: abe688ca4d81266efd632a53533ad17308a9bc5f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809250"
---
# <a name="activity-based-subcontracting"></a>Tegevustepõhised allhanked

[!include [banner](../includes/banner.md)]

Selles teemas kirjeldatakse üksikasjalikult, kuidas kasutada allhanketegevusi kulusäästlikus tootmisvoos.

Microsoft Dynamics 365 Supply Chain Management pakub allhangeteks kaht lähenemisviisi: tootmistellimused ja lean manufacturing (kulusäästlik tootmine). Kulusäästlikus tootmises on allhanketöö kujundatud teenusena, mis on seotud tootmisvoo tegevusega. Kasutusele on võetud kulugrupi eritüüp **Otse väljasttellimine** ja allhanketeenused ei ole enam koosluse osa. Allhanketöö kuluarvestus on täielikult integreeritud kulusäästliku tootmise kululahendusse.

## <a name="production-flows-that-involve-subcontractors"></a>Tootmisvood, mis hõlmavad allhankijaid
Tootmisvoo üldpõhimõte tegevuste allhankimisel ei muutu. Materjal liigub endiselt asukohtade vahel, protsessitegevused teisendavad materjali toodeteks ja ülekandetegevused liigutavad materjali või tooteid ühest asukohast teise. Saate kujundada asukohad ja töörakud hankija hallatavatena, määrates laole või ressursigruppi kuuluvale ressursile hankija konto.  

Nende võimaluste põhjal ei nõua kulusäästlik tootmine mingeid kindlaid funktsiooone materjali- ja tootevoo toetamiseks. Kõik võimalikud stsenaariumid, mis hõlmavad hankijaid tootmis- või transporditeenuste pakkujatena, saab kujundada tootmisvoo ja -tegevuste arhitektuuri põhjal.  

Näiteks töötab allhankija oma asukoha lõpplaost väljaspool. Kui materjali käsitlemisühikud tühjendatakse allhankija juures, tagastatakse kanban-kaardid koosterakule koos järgmise saadetisega. Seejärel täiendatakse allhankija juures asuvat lõppladu. Ülekannet allhankija juurde ja tema juurest saab kujundada sõnaselgete ülekandetegevustena toetamaks komplekteerimis- ja saatmisprotsessi. Kui sõnaselge registreerimine pole füüsilise transportimise toetamiseks nõutav, võib ülekandetegevused ära jätta.  

Allhankijat saab kasutada tootmisvoo üldvõimsuse koormuse tasakaalustamiseks. Näiteks kujundatakse tootmisvoog plaanitud kanban-reegleid kasutades. Plaanija kasutab mõlema tööraku nõudepõhiseks plaanimiseks ja tasakaalustamsieks kanbani plaanimistahvlit. Plaanija jälgib ka lõpplao konsolideeritud tarnegraafikut lehel **Tarnegraafik**. Mitu allhankijat saab kujundada ühes või mitmes tootmisvoos ja sama toote tarnimiseks samasse asukohta erinevate tegevuste kaudu võib kehtestatud olla mitu kanban-reeglit. Plaanija saab teisendada kanbanid alternatiivseks kanban-reegliks, et algselt sisemise tootmise jaoks loodud kanban alternatiivse protsessi jaoks ümber plaanida. Tööraku allhankeline loomus ei mõjuta mingil moel tootmisvoogu. Sama tööpõhimõte kehtib kahe paralleelse sisemise tööraku või kahe allhankeraku puhul.   

Nagu mis tahes muu tegevus tootmisvoos, võivad allhanketegevused tarbija ja tarnida inventeeritud, inventeerimata (lõpetamata töö \[WIP\]) ja poolvalmis materjale ning tooteid, Kõigil juhtudel on allhanketegevuste plaanimise ja käivitamise protsessid samad. Samuti on need protsessid samad mis sisetöö puhul.

## <a name="purchase-process-for-subcontracted-activities-services"></a>Allhanketegevuste (teenuste) ostuprotsess
Allhanketegevuste ostuprotsess põhineb füüsilisel materjalivool, mis on registreeritud kanban-töö edenemisega, näiteks Alustatud või Lõpetatud. Finantsvoog, näiteks allhanketöö kulu, on teine voog, mis järgneb füüsilisele voole. Samal ajal on ostuprotsess sõltumatu protsess, mis võimaldab ostudokumente igas etapis käsitsi korrigeerida. Allhanketegevuste ostuprotsess on järgmine.

1.  Looge ostuleping. Ostuleping luuakse teenuse kohta ja ühendatakse tootmisvoo tegevusega.
2.  Looge ostutellimus. Väljalaske ostutellimuse saab teenuse jaoks luua plaanitud kanban-tööde põhjal. Sama teenusega seotud tööd saab grupeerida ostutellimuse ridadele päeva, nädala või kuu alusel. Ostutellimuse ridu saab pärast kanban-tööde loomist luua igal ajal. Ostutellimuse ridu saab luua ka pärast fakti. See suvand valitakse tavaliselt siis, kui allhankija pakub teenuseid vastuvõetud kanbanide või kanban-kaartide alusel ilma lisateavituseta. Sellisel juhul saab ostutellimuse ja arve vahelised hälbed minimeerida.
3.  Looge kanban-kaardid, materjal ja komplekteerimisloend, mis saadetakse allhankijale töötlemise ettevalmistamiseks. Tootmisvoo üksikasjaliku kujunduse põhjal toimub ettevalmistus kanban-tahvlil, et töödelda tegevusi komplekteerimisloendi ja ettevalmistusfunktsiooni abil. Teine võimalus on ülekandetööd ette valmistada kanban-tahvlil, kasutades komplekteerimisloendit ja alustamist või lõpetamist. Inventeeritud materjali puhul saab mõlemat protsessi toetada WMS-i komplekteerimis- ja saatmisprotsessiga. Nõudmisel saab luua veokirja.
4.  Looge kanbani käsitlemisühikud ja kanban-kaardid. Pärast töötlemist tagastab allhankija kaardid. Tavaliselt sisaldavad kaardid tarneteadet, mis määrab saadetud füüsilise materjali. Viide pakutavatele teenustele pole nõutav. Materjali või toote saabumine kliendi juurde registeeritakse kanban-tahvlil olenevalt kanban-kaartidest. (Olenevalt kujundatud tegevustest kasutatakse kas protsessitegevuste kanban-tahvlit või ülekandetööde kanban-tahvlit.)
5.  Looge sissetulekunõuanne. Sissetulekunõuannet saab kasutada saatelehedokumendi asendamiseks vastuvõetud teenuste puhul. Sissetulekunõuandeid saab luua allhanketegevuse lõpetatud kanban-tööde põhjal valitud perioodi kohta. Iga töö sissetuleku puhul luuakse seotud ostutellimuse rea jaoks nõuandeid. Sissetulekunõuande saab välja printida ja saata vastuvõtukinnitusena allhankijale.
6.  Arve loomine.

Protsess lõpeb, kui allhankijale esitatakse perioodi kohta arve. Arvete võrdlemine tehakse loodud sissetulekunõuannete alusel. Kuna sissetulekunõuanded kujutavad endast materjali täpset füüsilist vastuvõttu, on kolmesuunaline võrdlus lihtsustatud.

## <a name="configuring-activities-for-subcontracting"></a>Allhanketegevuste konfigureerimine
Järgmised jaotised kirjeldavad, kuidas konfigureerida allhanketegevusi.

### <a name="subcontracted-services"></a>Allhanketeenused

Tegevusepõhises allhankes kasutatav maksekaup peab olema järgmiste atribuutidega toode.

-   **Toote tüüp:** teenus
-   **Laomudeligrupp:** mitteladustatav

See nõue jõustab FIFO-laomudeli (esimesena sisse, esimesena välja). **Märkus.** Toodete kuluarvestus nõuab teenuse standardkulu määratlemist. Nõutav on ostuleping hankijaga. Muidu ei saa teenust tegevusepõhiseks allhankeks kasutada.

### <a name="subcontracted-process-activities"></a>Allhankeprotsessi tegevused

Protsessi tegevuse konfigureerimiseks allhanketegevusena tehke järgmist.

1.  Konfigureerige allhanke töörakk. Tööraku konfigureerimiseks allhankena peate looma ressursi tüübiga **Hankija** ja seostama selle töörakuga (ressursigrupp). Töörakule tuleb määrata käitusaja kulukategooria, mille kulugrupi tüüp on **Otse väljasttellimine**. Kulukategooriad seadistamiseks ja kogus pole nõutavad.
2.  Kui protsessi tegevus on loodud ja seotud allhanke töörakuga, peate konfigureerima tegevuse jaoks teenuse, enne kui tootmisvoo versiooni saab aktiveerida. Seda saate teha lehel **Tegevuse** **üksikasjad**. Allhanke töörakuga seostatud tegevuste puhul kuvatakse kiirkaart **Teenusetingimused**. Sellel kiirkaardil saate lisada vaiketeenuse, mis kehtib kõigi väljastatavate kaupade puhul. Kui kindlad väljastatavad kaubad nõuavad teistsuguseid teenuseid või teistsuguseid teenuse arvutamise parameetreid (näiteks erinevat teenusesuhet), saate lisada tegevusele teisi teenuseid.

## <a name="subcontracted-transfer-activities"></a>Allhanke ülekandetegevused
Ülekandetegevus konfigureeritakse allhanke tegevusena olenevalt ülekandetegevuse sättest **Lastija**. Valikud on järgmised:

-   **Saatja** – tegevus määratakse allhankeks, kui ülekannet laost haldab hankija (nagu on määratletud lao atribuudiga). Kõigil teenuste jaoks valitud ostulepingutel peab olema sama hankija ID mis laol.
-   **Saaja** – tegevus määratakse allhankeks, kui ülekannet lattu haldab hankija (nagu on määratletud lao atribuudiga). Kõigil teenuste jaoks valitud ostulepingutel peab olema sama hankija ID mis laol.
-   **Vedaja** – tegevus määratakse allhankeks mis tahes hankijale, kes pakub teenust. Kehtivuse tagamiseks peab laohaldusele olema loodud vedaja ja määratud hankija konto.

Nagu protsessitegevuste puhul, peate konfigureerima allhanke ülekandetegevuste jaoks vaiketeenuse lehe **Tegevuse** **üksikasjad** kiirkaardil **Teenusetingimused**.

## <a name="service-quantity-calculation"></a>Teenuse koguse arvutamine
Kogu ostuprotsess põhineb teenuse kaubaviitel. Seda kaubaviidet mõõdetakse teenuse mõõtühikutes. Teenuseid mõõdetakse tavaliselt kas teenuste arvuna (ühikud) või ajana. Teenusekoguse arvutamiseks kanban-tööde registreeritud lõpetamise põhjal saate kasutada järgmisi meetodeid.

-   **Tööde arvu põhine arvutus** – üks kanban-töö võrdub *n* teenuseühikuga olenemata tarnitud tootekogusest. Kulusäästlikus tootmises vastab üks töö ühele materjali käsitlemisühikule. See arvutusmeetod kehtib kõigile teenustele, mille puhul on materjali käsitlemisühikul fikseeritud hind. Seetõttu kehtib see meetod tavaliselt ülekandetegevuste puhul. Siiski võib selle rakendada ka protsessitegevustele, mis töötlevad terveid materjali käsitlemisühikuid.
-   **Tootekoguse põhine arvutus** – teenusekogus on seotud plaanitud/tarnitud tootekogusega. Kui tarnitud tootekogus on arvutatud, saab vigased kogused kaasata või välistada. See arvutusmeetod kehtib kõigil juhtudel, kus teenuse hind töödeldud toote ühiku kohta on kokku lepitud.
-   **Tegevuseajal põhinev arvutus** – teoreetilised tegevuseajad arvutatakse tegevuse töötlemisaja, töödeldud koondkoguse ja töödeldud toote läbilaskemäära põhjal. See arvutusmeetod kehtib kõigile teenustele, mille eest tasutakse tunnihinna alusel ja millel on töödeldud toodete puhul erinev aeg.

## <a name="cost-accounting-of-subcontracted-services"></a>Allhanketeenuste kuluarvutus
Tootmisvoo jaoks loodud ostutellimusele (ehk allhanketegevuste kanban-tööde põhjal loodud ostutellimusele) sissetulekunõuande või hankija saatelehe sisestamisel arvestatakse sissetuleku väärtus tootmisvoo WIP-kontodes. Tootmisvoos arvestatakse ka arvete hälbeid. Kasutusele on võetud allhanketöö kulukategooria. See kulukategooria võimaldab WIP-le eraldatud ja perioodi jooksul tarbitud allhanketöö väärtuse läbipaistvat jälgimist.  

Kulusäästliku tootmise omahinna tagasiarvestus kuluperioodi lõpus arvutab kuluperioodi jooksul tootmisvoos toodetud toodete tegelikud hälbed.

## <a name="modeling-transfers-as-subcontracted-activities"></a>Ülekannete kujundamine allhanketegevustena
Transporti peetakse sageli mittetootlikuks ja arvatakse, et see ei lisa mingit väärtust. Kui aga allhankekulu võrrelda sisemise tootmise kuluga, tuleb arvesse võtta ka täiendavate transporditegevuste kulu. Tootmisvoog, mis ulatub üle mitme asukoha ja nõuab transporditeenuseid, peab kujundama transpordikulu osana toodete tarbijale tarnimise kulust. 

Tegevustepõhine allhange kulusäästlikus tootmises võimaldab integreerida vedajaid ja transpordihankijaid, kes liigutavad materjali ja tooteid tootmisvoo asukohtade vahel. Ülekandetegevuse kujundamisega saate määrata vedaja või hankija. Ülekandetegevused/-töö põhinevad teenusel ja ostulepingul ning te saate luua ostutellimusi ja sissetulekunõuandeid tegelike ülekandetööde põhjal. See funktsioon on sama mis allhanke protsessitegevuste funktsioon.  

Supply Chain Management toetab nüüd koosluse arvutamist, mis hõlmab transporditeenuseid, seotud ostutellimuste loomist, integreeritud sissetuleku registreerimist ja transporditeenuse kulude integreerimist tootmisvoo kuludesse.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]