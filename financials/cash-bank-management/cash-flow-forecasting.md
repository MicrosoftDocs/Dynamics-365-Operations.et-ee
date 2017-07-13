---
title: Likviidsuse plaanimine
description: "Selles teemas antakse ülevaade rahavoo prognoosimise protsessist. Samuti selgitatakse, kuidas rahavoogude prognoosimine on integreeritud teiste süsteemi moodulitega."
author: saraschi
manager: AnnBe
ms.date: 05/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: sarasch
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 3abf4b151b177095b71d44e9a6c9fd8541eaa64e
ms.openlocfilehash: a8ccd99431178c3cb4e73e7cd199de8e0845d716
ms.contentlocale: et-ee
ms.lasthandoff: 06/14/2017


---

# <a name="cash-flow-forecasting"></a>Likviidsuse plaanimine

[!include[banner](../includes/banner.md)]

Rahavoogude prognoosimise tööriistu saab kasutada tulevase rahavoo ja valuuta vajaduste analüüsimiseks, et saaksite hinnata ettevõtte tulevast sularahavajadust. Rahavoo prognoosi saamiseks tuleb teha järgmised toimingud.

- Määrata ja loetleda kõik likviidsuskontod. Likviidsuskontod on ettevõtte sularaha või sularaha ekvivalentide kontod.
- Konfigureerige ettevõtte likviidsuskontosid mõjutavate kannete prognooside käitumine.

Kui olete need toimingud teinud, võite arvutada ja analüüsida rahavooprognoose ja tulevasi valuutavajadusi.

## <a name="cash-flow-forecasting-integration"></a>Rahavooprognoosi integreerimine

Rahavoo prognoosimise saab integreerida pearaamatu, ostureskontro, müügireskontro, eelarvestamise ja varude haldusega. Prognoosimisprotsess kasutab kandeandmeid, mis sisestatakse süsteemi, ja arvutusprotsess prognoosib iga kande eeldatava mõju sularahale. Rahavoo arvutamisel arvestatakse järgmisi kandetüüpe.

- **Müügitellimused** – müügitellimused, mida ei ole veel arveldatud ja mille tulemuseks on füüsiline või rahaline müük.
- **Ostutellimused** – ostutellimused, mida ei ole veel arveldatud ja mille tulemuseks on füüsiline või rahaline ost.
- **Müügireskontro** – avatud kliendikanded (arved, mis on alles maksmata).
- **Ostureskontro** – avatud hankijakanded (arved, mis on alles maksmata).
- **Pearaamatukanded** – kanded, mille puhul on määratud tulevikus sisestamine.
- **Eelarve registrikirjed** – eelarve registrikirjed, mis on valitud likviidsuse plaanimiseks.
- **Nõudluse prognoosid** – laoprognoosi mudeli read, mis on valitud likviidsuse plaanimiseks.
- **Tarneprognoosid** – laoprognoosi mudeli read, mis on valitud likviidsuse plaanimiseks.

Kuigi puudub integratsioon projektihalduse ja raamatupidamisega, on mitu võimalust projektikannete lisamiseks likviidsuse plaanimisse. Sisestatud projektiarved lisatakse prognoosi avatud kliendikannete osana. Projekti algatatud müügitellimused ja ostutellimused lisatakse prognoosi avatud tellimustena pärast nende sisestamist süsteemi. Projekti prognoose saab viia üle ka pearaamatu eelarvemudelisse. See pearaamatu eelarvemudel lisatakse siis likviidsuse plaanimisse eelarveregistri kirjete osana.

## <a name="configuration"></a>Konfiguratsioon

Kasutage likviidsuse plaanimise protsessi konfigureerimiseks lehte **Likviidsuse plaanimise seadistus**. Sellel lehel saate määrata jälgitavad likviidsuskontod ja iga valdkonna prognoosimise vaikekäitumise.

### <a name="general-ledger"></a>Pearaamat

Peate määratlema likviidsuskontod, mida soovite likviidsuse plaanimise kaudu jälgida. Tavaliselt on need likviidsuskontod põhikontod, mis on seotud pangakontodega, millel sularaha vastu võetakse ja millelt seda välja makstakse. Lehel **Likviidsuse plaanimise seadistus** vahekaardil **Pearaamat** saate valida põhikontod, mida prognoosimisel arvestada. Kui pangakonto on lehel **Pangakonto** põhikontoga seostatud, kuvatakse see väljal **Pangakonto**.

Saate määrata põhikontost sõltuva likviidsuse planeerimise, mis sisaldab kandeid, mis on otseselt seotud teise põhikonto kannetega. Iga rida, mille jaotisse **Sõltuvatel kontodel** lisate, loob sõltuval põhikontol likviidsuse plaanimise summa. Summa on rahavoogude summade protsent valitud peamise põhikonto suhtes.

Määrake kõigepealt väljale **Põhikonto** peamine põhikonto, kus kanded peaksid algselt toimuma. Määrake väljale **Sõltuv põhikonto** konto, mida peamise põhikonto suhtes tehtav algne kanne mõjutab. Määrake sobivad väärtused teistele rea väljadele. Väljal **Protsent** olevat väärtust saab muuta, nii et see kajastaks peamise põhikonto mõju sõltuvale põhikontole. Müügi- või ostueelarve jaoks valige väärtus **Maksetingimused**, mis on tüüpiline enamiku klientide või hankijate puhul. Määrake väljale **Sisestustüüp** likviidsuse plaanimisega seotud eeldatav sisestustüüp.

### <a name="accounts-payable"></a>Ostureskontro

Saate arvutada ostude prognoosi, kasutades seadistusvalikuid vahekaardil **Ostureskontro** lehel **Likviidsuse plaanimise seadistus**. Enne, kui saate konfigureerida likviidsuse plaanimist ostureskontro jaoks, peate konfigureerima maksetingimused, hankijagrupid ja hankija sisestusreeglid.

Jaotisest **Ostuprognoosi vaikesätted** saate valida vaike-ostukäitumised likviidsuse plaanimiseks. Kolm välja määravad sularahale mõju avaldamise aja: **Aeg tarnekuupäeva ja arve kuupäeva vahel**, **Maksetingimused** ja **Aeg arve tähtaja ja maksekuupäeva vahel**. Prognoos kasutab välja **Maksetingimused** vaikesätteid ainult juhul, kui kandel pole väärtust määratud. Kasutage maksetingimusi iga protsessi osa puhul kõige tüüpilisema päevade arvu kirjeldamiseks.

Väli **Maksete likviidsuskontod** määratleb likviidsuskonto, mida kõige sagedamini maksete jaoks kasutatakse. Kasutage välja **Likviidsuse plaanimisse eraldatav summa protsent** määramiseks, kas prognoosimisel tuleks kasutada summade protsente. Jätke see väli tühjaks, kui prognoosimise ajal tuleks kasutada terveid kandesummasid.

Välja **Aeg arve tähtaja ja maksekuupäeva vahel** vaikeseadistuse saab konkreetsete hankijagruppide puhul alistada. Prognoos kasutab vaikeväärtust jaotisest **Ostuprognoosi vaikesätted**, kui kande hankijaga seotud hankijagrupile pole määratud teistsugust väärtust. Vaikeväärtuse alistamiseks valige hankijagrupp ja määrake siis väljale **Ostmise aeg** uus väärtus.

Välja **Likviidsuskonto** vaikeseadistuse saab konkreetsete hankija sisestusreeglite puhul alistada. Prognoos kasutab vaikeväärtust jaotisest **Ostuprognoosi vaikesätted**, kui kande hankijaga seotud sisestusreeglitele pole määratud teist likviidsuskontot. Vaikeväärtuse alistamiseks valige sisestusreeglid ja määrake siis likviidsuskonto, mida võidakse eeldatavasti mõjutada.

### <a name="accounts-receivable"></a>Müügireskontro

Saate arvutada müügiprognoosi, kasutades seadistusvalikuid vahekaardil **Müügireskontro** lehel **Likviidsuse plaanimise seadistus**. Enne, kui saate konfigureerida likviidsuse plaanimist müügireskontro jaoks, peate konfigureerima maksetingimused, kliendigrupid ja kliendi sisestusreeglid.

Jaotisest **Müügiprognoosi vaikesätted** saate valida vaike-müügikäitumised likviidsuse plaanimiseks. Kolm välja määravad sularahale mõju avaldamise aja: **Aeg lähetuskuupäeva ja arve kuupäeva vahel**, **Maksetingimused** ja **Aeg arve tähtaja ja maksekuupäeva vahel**. Prognoos kasutab välja **Maksetingimused** vaikesätteid ainult juhul, kui kandel pole väärtust määratud. Kasutage maksetingimusi iga protsessi osa puhul kõige tüüpilisema päevade arvu kirjeldamiseks. 

Väli **Maksete likviidsuskontod** määratleb likviidsuskonto, mida kõige sagedamini maksete jaoks kasutatakse. Kasutage välja **Likviidsuse plaanimisse eraldatav summa protsent** määramiseks, kas prognoosimisel tuleks kasutada summade protsente. Jätke see väli tühjaks, kui prognoosimise ajal tuleks kasutada terveid kandesummasid.

Välja **Aeg arve tähtaja ja maksekuupäeva vahel** vaikeseadistuse saab konkreetsete kliendigruppide puhul alistada. Prognoos kasutab vaikeväärtust jaotisest **Müügiprognoosi vaikesätted**, kui kande kliendiga seotud kliendigrupile pole määratud teistsugust väärtust. Vaikeväärtuse alistamiseks valige kliendigrupp ja määrake siis väljale **Müügi aeg** uus väärtus.

Välja **Likviidsuskonto** vaikeseadistuse saab konkreetsete kliendi sisestusreeglite puhul alistada. Prognoos kasutab vaikeväärtust jaotisest **Müügiprognoosi vaikesätted**, kui kande kliendiga seotud sisestusreeglitele pole määratud teist likviidsuskontot. Vaikeväärtuse alistamiseks valige sisestusreeglid ja määrake siis likviidsuskonto, mida võidakse eeldatavasti mõjutada.

### <a name="budgeting"></a>Eelarvestamine

Likviidsuse plaanimisse saab lisada eelarvemudelite põhjal loodud eelarveid. Valige vahekaardilt **Eelarvestamine** lehel **Likviidsuse plaanimise seadistus** eelarvemudelid, mida prognoosi lisada. Vaikimisi lisatakse uued eelarve registrikirjed prognoosidesse pärast eelarvemudeli lubamist likviidsuse plaanimiseks. Likviidsuse plaanimisse lisamise saab eraldi eelarve registrikirjete puhul üle kirjutada.

### <a name="inventory-management"></a>Varud

Likviidsuse plaanimisse saab lisada varude pakkumise ja nõudluse prognoosid. Valige vahekaardilt **Varude haldus** lehel **Likviidsuse plaanimise seadistus** prognoosi mudel, mida likviidsuse plaanimisse lisada. Likviidsuse plaanimisse lisamise saab eraldi pakkumise ja nõudluse prognoosi ridadel üle kirjutada.

### <a name="calculation"></a>Kalkulatsioon

Enne likviidsuse prognoosi analüüsi vaatamist peate käivitama rahavoo arvutamise protsessi. Arvutusprotsess näitab sisestatud kannete tulevast mõju sularahale.

Likviidsuse plaanimise saab arvutada lehe **Likviidsuse plaanide arvutamine** abil. Saate arvutada terve likviidsuse plaani või astmelise likviidsuse plaani. 

- Kõigi likviidsuse plaanimise kannete eemaldamiseks ja ümber arvutamiseks määrake välja **Likviidsuse plaanimise arvutusmeetod** väärtuseks **Kokku**. Soovitame kasutada seda lähenemist, kui te pole pikka aega likviidsuse plaane uuendanud. 
- Olemasoleva rahavoogude teabe uuendamiseks ainult uute kannete puhul määrake välja **Likviidsuse plaanimise arvutusmeetod** väärtuseks **Uus**. Sellel lehel kuvatakse rahavoo viimase arvutamise kuupäev.

Likviidsuse plaanimiseks saab kasutada ka pakktöötlust. Likviidsuse plaanimise analüüsi regulaarse uuendamise tagamiseks seadistage likviidsuse plaanide arvutamiseks korduv pakktöötlus.

### <a name="reporting"></a>Aruandlus

Pärast likviidsuse plaani arvutamist tuleb seotud üksuse andmeid analüütiliseks aruandluseks uuendada. Valige lehelt **Üksuse kauplus** mõõt **LedgerCovLiquidityMeasurement kokku** ja klõpsake siis nuppu **Värskenda**.

On olemas kaks tööruumi, mis sisaldavad likviidsuse plaanimise andmeid. Ühes tööruumis on kõigi ettevõtete andmed ja teises tööruumis on andmed ainult praeguse ettevõtte kohta.

Kõigi ettevõtete juurdepääsu tööruumile juhitakse kohustusega **Kõikide ettevõtete likviidsuse tööruumi kuvamine**. Vaikimisi on tööruum **Kassa ülevaade – kõik ettevõtted** saadaval järgmistele rollidele:

- Tegevjuht
- Finantsdirektor
- Finantskontroller

Praeguse ettevõtte juurdepääsu tööruumile juhitakse tööruumi kohustusega **Praeguse ettevõtte likviidsuse tööruumi kuvamine**. Vaikimisi on tööruum **Kassa ülevaade – praegune ettevõte** saadaval järgmistele rollidele:

- Raamatupidaja
- Pearaamatupidaja
- Raamatupidaja
- Ostureskontro juht
- Müügireskontro haldur

Tööruum **Kassa ülevaade – kõik ettevõtted** näitab likviidsuse plaanimise analüüsi süsteemi valuutas. Süsteemi valuuta ja süsteemi vahetuskursi tüüp, mida analüüsiks kasutatakse, on määratletud lehel **Süsteemiparameetrid**. Selles tööruumis kuvatakse ülevaade likviidsuse plaanimisest ja pangakontode saldodest kõigi ettevõtete kohta. Sularaha sissetulekute ja väljaminekute diagramm annab ülevaate tulevastest sularaha liikumistest ja saldodest süsteemi valuutas, koos prognoositavate kannete üksikasjalike andmetega. Võimalik on vaadata ka prognoositavaid valuutasaldosid.

Tööruumis **Kassa ülevaade – praegune ettevõte** näidatakse likviidsuse plaanimise analüüsi ettevõtte määratletud arvestusvaluutas. Analüüsiks kasutatav arvestusvaluuta on määratletud lehel **Pearaamat**. Selles tööruumis kuvatakse ülevaade likviidsuse plaanimisest ja pangakontode saldodest praeguse ettevõtte kohta. Sularaha sissetulekute ja väljaminekute diagramm annab ülevaate tulevastest sularaha liikumistest ja saldodest arvestusvaluutas, koos prognoositavate kannete üksikasjalike andmetega. Võimalik on vaadata ka prognoositavaid valuutasaldosid.

Lisateavet likviidsuse plaanimise analüüsi kohta leiate Power BI sisuteemast Kassa ülevaade.

Lisaks saate vaadata likviidsuse plaanimise andmeid konkreetsete kontode, tellimuste ja üksuste kohta järgmistelt lehtedelt.

- **Proovibilanss**: valige **Likviidsuse plaanimine** valitud põhikonto tulevaste rahavoogude vaatamiseks.
- **Kõik müügitellimused**: tehke vahekaardil **Arve** valik **Likviidsuse plaanimine** valitud müügitellimuse prognoositava mõju vaatamiseks sularahale.
- **Kõik ostutellimused**: tehke vahekaardil **Arve** valik **Likviidsuse plaanimine** valitud ostutellimuse prognoositava mõju vaatamiseks sularahale.
- **Pakkumise prognoos**: valige **Likviidsuse plaanid** valitud üksuse pakkumise prognoosiga seotud tulevaste rahavoogude vaatamiseks.
- **Nõudluse prognoos**: valige **Likviidsuse plaanid** valitud üksuse nõudluse prognoosiga seotud tulevaste rahavoogude vaatamiseks.


