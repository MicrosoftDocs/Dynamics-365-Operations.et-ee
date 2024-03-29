---
title: Likviidsuse plaanimine
description: See artikkel annab ülevaate likviidsuse prognoosimise protsessist. Samuti selgitatakse, kuidas rahavoogude prognoosimine on integreeritud teiste süsteemi moodulitega.
author: angelad116
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: d76e47fc1456dfab7606f337f070a149b0c8e586
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151936"
---
# <a name="cash-flow-forecasting"></a>Likviidsuse plaanimine

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Rahavoogude prognoosimise tööriistu saab kasutada tulevase rahavoo ja valuuta vajaduste analüüsimiseks, et saaksite hinnata ettevõtte tulevast sularahavajadust. Rahavoo prognoosi saamiseks tuleb teha järgmised toimingud.

- Määrata ja loetleda kõik likviidsuskontod. Likviidsuskontod on ettevõtte sularaha või sularaha ekvivalentide kontod.
- Konfigureerige ettevõtte likviidsuskontosid mõjutavate kannete prognooside käitumine.

Kui olete need toimingud teinud, võite arvutada ja analüüsida rahavooprognoose ja tulevasi valuutavajadusi.

## <a name="cash-flow-forecasting-integration"></a>Rahavooprognoosi integreerimine

Rahavoo prognoosimise saab integreerida pearaamatu, ostureskontro, müügireskontro, eelarvestamise ja varude haldusega. Prognoosimisprotsess kasutab kandeandmeid, mis sisestatakse süsteemi, ja arvutusprotsess prognoosib iga kande eeldatava mõju sularahale. Rahavoo arvutamisel arvestatakse järgmisi kandetüüpe.

- **Müügitellimused** – müügitellimused, mida ei ole veel arveldatud ja mille tulemuseks on füüsiline või rahaline müük.
- **Vabas vormis arved – vabas vormis arved, mida pole veel sisestatud ja mille tulemuseks** on finantsmüük. 
- **Ostutellimused** – ostutellimused, mida ei ole veel arveldatud ja mille tulemuseks on füüsiline või rahaline ost.
- **Müügireskontro** – avatud kliendikanded (arved, mis on alles maksmata).
- **Ostureskontro** – avatud hankijakanded (arved, mis on alles maksmata).
- **Pearaamatukanded** – kanded, mille puhul on määratud tulevikus sisestamine.
- **Eelarve registrikirjed** – eelarve registrikirjed, mis on valitud likviidsuse plaanimiseks.
- **Nõudluse prognoosid** – laoprognoosi mudeli read, mis on valitud likviidsuse plaanimiseks.
- **Tarneprognoosid** – laoprognoosi mudeli read, mis on valitud likviidsuse plaanimiseks.
- **Väline andmeallikas** – välised andmed, mis on sisestatud või imporditud rahavooprognoosidesse arvutustabeli mallide abil.
- **Projekti eelarved** – Projektihalduse ja raamatupidamise eelarved eelarvemudeli abil.
- **Rahavoo käibemaksu halduri maksed** – prognoositud käibemaksuhalduri maksesummad ja ajastus, mille tulemuseks on finantsmaksed. Lubage funktsioon Rahavoo käibemaksu halduri maksed.

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

Likviidsuse plaanimisse saab lisada eelarvemudelite põhjal loodud eelarveid. Valige **Rahavoo prognoosi seadistamine** lehel **Eelarvestamine** vahekaardilt eelarvemudelid, mida prognoosi lisada. Vaikimisi lisatakse uued eelarve registrikirjed prognoosidesse pärast eelarvemudeli lubamist likviidsuse plaanimiseks.

Eelarve registrikirjeid saab rahavoogude prognoosi lisada individuaalselt isikupärastamise kaudu. Kui lisate lehele **Eelarve registrikirje** veeru „Lisa rahavoogude prognoosidesse“, kirjutab süsteem **Rahavoo prognoosi seadistus** lehe seaded üle, et lisada üksik eelarve registrikirje prognoos.


### <a name="inventory-management"></a>Varud

Likviidsuse plaanimisse saab lisada varude pakkumise ja nõudluse prognoosid. Valige vahekaardilt **Varude haldus** lehel **Likviidsuse plaanimise seadistus** prognoosi mudel, mida likviidsuse plaanimisse lisada. Likviidsuse plaanimisse lisamise saab eraldi pakkumise ja nõudluse prognoosi ridadel üle kirjutada.

### <a name="setting-up-dimensions-for-cash-flow-forecasting"></a>Rahavoo prognoosimise jaoks dimensioonide seadistamine
Uus vahekaart likviidsuse prognoosimise **seadistamise** lehel võimaldab **teil kontrollida, milliseid finantsdimensioone kasutatakse rahavoo prognoosimise tööruumi filtreerimiseks** . See vahekaart kuvatakse ainult siis, kui likviidsuse prognoosimise funktsioon on lubatud.

Vahekaardil **Dimensioonid** tehke dimensioonide loendis filtreerimiseks valik ja kasutage nooleklahve, et liigutada need parempoolsesse veergu. Rahavoo prognoosimise andmete filtreerimiseks saab valida ainult kaks dimensiooni. 

### <a name="setting-up-external-source"></a>Välise allika seadistamine
Kui finantside vihjed on konfigureeritud, saab väliseid andmeid sisestada või importida likviidsuse prognoosi. Enne välisandmete sisestamist või importimist tuleb seadistada välisallikad. Seadistage **vahekaardil Välisallikas** välised rahavoo kategooriad. Kategooria võib olla Väljaminev **või** Sissetulev **·**. **Likviidsuse** peaks olema sisestustüübiks valitud. Valige juriidilise **isiku sätete ruudustikus** juriidilised isikud ja vastavad põhikontod, mille suhtes välised rahavookategooriad kehtivad.

Lisateavet vt välisandmetest [likviidsuse prognoosides](../../finance/finance-insights/external-data-in-cash-flow.md). 

### <a name="project-management-and-accounting"></a>Projektihaldus ja -arvestus

Versioonis 10.0.17 võimaldab uus funktsioon integreerimist projektijuhtimise ning raamatupidamise ja likviidsuse prognoosimisega. **Funktsioonihalduse** tööruumis lülitage **Likviidsuse projekti prognoosi** funktsioon sisse, et kaasata prognoositud kulud ja tulud likviidsuse prognoosi. Valige **Projektihaldus ja raamatupidamine** vahekaardilt lehekülg **Rahavoo prognoosi seadistus** , valige projektitüüpja kandetüübid, mis peavad olema rahavoo prognoosi kaasatud. Seejärel valige projekti eelarvemudel. Vähendamise tüübi alammudel töötab kõige paremini. Likviidsuskontod, mis on sisestatud kontode müügikontro seadistusse likviidsuse vaikekontodena. Seetõttu ei pea te rahavoogu prognoosides likviidsuse vaikekontosid sisestama. Kasutada saab ka eelarvemudelit, kuid projektihalduse ja raamatupidamise lehel **Rahavoo prognoosimise seades** saab valida vaid ühe tüübi. Prognoosimudel pakub kõige rohkem paindlikkust siis, kui kasutate Projektihaldust ja raamatupidamist või Project Operations -it.

Peale Rahavoo projekti prognoosi funktsiooni sisselülitamist, saab rahavoo prognoosi iga projekti jaoks näha lehel **Kõik projektid** . Toimingupaani vahekaardil **Plaan** rühmas **Prognoos** valige suvand **Rahavoo prognoos**. Sularaha ülevaate **tööruumides** ([vt](#reporting) selle artikli jaotist Aruandlus) näitab projekti eelarve kandetüüp sissetulekuid (projekti eelarve tulu) ja väljaminekuid (projekti eelarve kulud). Summasid saab kaasata ainult siis, kui **Projekti etapi** väli **Sularaha ülevaate** tööruumis väärtuseks on seatud **Töös**.

Projektikandeid kaasatakse rahavoo prognoosi mitmel viisil, sõltumata sellest, kas **Rahavoo projekti prognoos** funktsioon on sisse lülitatud. Sisestatud projektiarved lisatakse prognoosi avatud kliendikannete osana. Projekti algatatud müügitellimused ja ostutellimused lisatakse prognoosi avatud tellimustena pärast nende sisestamist süsteemi. Projekti prognoose saab viia üle ka pearaamatu eelarvemudelisse. See pearaamatu eelarvemudel lisatakse siis likviidsuse plaanimisse eelarveregistri kirjete osana. Kui olete **Rahavoo projekti prognoosi** funktsiooni sisse lülitanud, siis ärge kandke projekti prognoose üle pearaamatu eelarvemudelisse, sest see tegevus põhjustab seda, et projekti prognoose loetakse kaks korda.

### <a name="sales-tax-authority-payments"></a>Käibemaksuhalduri maksed 

Rahavoo käibemaksu halduri maksete funktsioon prognoosib käibemaksu maksete rahavoo mõju. Kasutab maksmata käibemaksukandeid, maksu tasakaalustusperioode ja maksuperioodi maksetähtaega, et prognoosida rahavoo maksete kuupäeva ja summat. 

### <a name="calculation"></a>Arvutus

Enne likviidsuse prognoosi analüüsi vaatamist peate käivitama rahavoo arvutamise protsessi. Arvutusprotsess näitab sisestatud kannete tulevast mõju sularahale.

Likviidsuse plaanimise saab arvutada lehe **Likviidsuse plaanide arvutamine** abil. Saate arvutada terve likviidsuse plaani või astmelise likviidsuse plaani. 

- Kõigi likviidsuse plaanimise kannete eemaldamiseks ja ümber arvutamiseks määrake välja **Likviidsuse plaanimise arvutusmeetod** väärtuseks **Kokku**. Soovitame kasutada seda lähenemist, kui te pole pikka aega likviidsuse plaane uuendanud. 
- Olemasoleva rahavoogude teabe uuendamiseks ainult uute kannete puhul määrake välja **Likviidsuse plaanimise arvutusmeetod** väärtuseks **Uus**. Sellel lehel kuvatakse rahavoo viimase arvutamise kuupäev.

Likviidsuse plaanimiseks saab kasutada ka pakktöötlust. Plaanimise analüüsi regulaarse uuendamise tagamiseks seadistage likviidsuse plaanide arvutamiseks korduv pakktöötlus.

Versioonis 10.0.13 anti välja arvutusprotsessi täiustus, mis kasutab protsessi automatiseerimise raamistikku, et ajastada likviidsuse arvutamise tööd. Selle saab lubada funktsiooni **Likviidsuse plaanimise automatiseerimine**, mis asub tööruumis **Funktsioonihaldus**. Kui see on lubatud, valige link **Likviidsuse plaanimise automatiseerimine**, et kuvada uus automatiseerimise leht, kus saate ajastada likviidsuse arvutamise protsessi. Uue likviidsuse plaanimise graafiku loomiseks valige **Loo uus protsessi automatiseerimine** ja seejärel valige rippmenüüst **Graafiku tüüp** suvand **Likviidsuse plaanimise automatiseerimine**. Peate määrama graafiku igale ettevõttele, mille puhul te likviidsuse plaanimise andmeid uuendate.  Sellel leheküljel on ka näha, millised likviidsuse plaanimise automatiseerimise tööd on ootel ja millal viimane töö lõpetati.  

> [!NOTE] 
> Kui likviidsuse plaanimiseks on juba ajastatud olemasolevad pakett-tööd, kuvatakse tõrketeade ja te ei saa seda funktsiooni lubada. Enne selle funktsiooni lubamist tuleb olemasolevad pakett-tööd tühjendada. 

Lisateavet vt teemast [Protsessi automatiseerimine](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

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

Tööruumis **Sularaha ülevaade – praegune ettevõte** näidatakse rahavoo prognoosi analüüsi ettevõtte määratletud arvestusvaluutas. Analüüsiks kasutatav arvestusvaluuta on määratletud lehel **Pearaamat**. Selles tööruumis kuvatakse ülevaade likviidsuse plaanimisest ja pangakontode saldodest praeguse ettevõtte kohta. Sularaha sissetulekute ja väljaminekute diagramm annab ülevaate tulevastest sularaha liikumistest ja saldodest arvestusvaluutas, koos prognoositavate kannete üksikasjalike andmetega. Võimalik on vaadata ka prognoositavaid valuutasaldosid.

Lisateabe saamiseks likviidsuse plaanimise analüüsi kohta vaadake [Kassa ülevaate Power BI sisu](Cash-Overview-Power-BI-content.md).

Lisaks saate vaadata likviidsuse plaanimise andmeid konkreetsete kontode, tellimuste ja üksuste kohta järgmistelt lehtedelt.

- **Proovibilanss**: valige **Likviidsuse plaanimine** valitud põhikonto tulevaste rahavoogude vaatamiseks.
- **Kõik müügitellimused**: tehke vahekaardil **Arve** valik **Likviidsuse plaanimine** valitud müügitellimuse prognoositava mõju vaatamiseks sularahale.
- **Kõik ostutellimused**: tehke vahekaardil **Arve** valik **Likviidsuse plaanimine** valitud ostutellimuse prognoositava mõju vaatamiseks sularahale.
- **Pakkumise prognoos**: valige **Likviidsuse plaanid** valitud üksuse pakkumise prognoosiga seotud tulevaste rahavoogude vaatamiseks.
- **Nõudluse prognoos**: valige **Likviidsuse plaanid** valitud üksuse nõudluse prognoosiga seotud tulevaste rahavoogude vaatamiseks.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
