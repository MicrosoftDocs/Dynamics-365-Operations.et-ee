---
title: Ruudustiku võimalused
description: See artikkel kirjeldab mitut ruudustiku juhtelemendi võimast funktsiooni. Nende võimaluste kasutamiseks peate lubama uue ruudustiku funktsiooni.
author: jasongre
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: a8968a1263dfafd67b07b4beb78c51493e95756e
ms.sourcegitcommit: 47534a943f87a9931066e28f5d59323776e6ac65
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/11/2022
ms.locfileid: "9258943"
---
# <a name="grid-capabilities"></a>Ruudustiku võimalused

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Uus ruudustiku juhtelement pakub mitmeid kasulikke ja võimsaid võimalusi, mida saate kasutada kasutaja tootlikkuse suurendamiseks, teie andmetest huvitavate vaadete loomiseks ja sisukate ülevaadete hankimiseks andmete jaoks. Selles artiklis tutvustatakse järgmisi võimalusi. 

- Arvutatud väärtuste kuvamine 
- Süsteemist eespool tippimine
- Matemaatiliste avaldiste hindamine 
- Tabeldusandmete grupeerimine (lubatud eraldi, kasutades grupeerimist **ruudustikes**)
- Veergude külmutamine (lubatud eraldi, kasutades funktsiooni **Külmutamise veerud ruudustikus**)
- Veeru laiuse automaatkorrekteerimine
- Venitatavad veerud

## <a name="showing-calculated-values"></a>Arvutatud väärtuste kuvamine
Finantside ja toimingute rakendustes saavad kasutajad vaadata arvutatud väärtust iga numbriveeru kohta ruudustikus. Neid arvutatud väärtusi näitab jaluse sektsioon ruudustiku allosas.

[![Kuvatakse arvutatud väärtused ruudustikes.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Versioonides enne 10.0.29 on arvutatud väärtus kokku ainus toetatud. Versiooni 10.0.29 **puhul** saavad kasutajad pärast laiendatud ruudustiku liitmise funktsiooni lubamist valida järgmise nelja arvutatud väärtuse seast:

- Miinimum
- Maksimum
- Kokku
- Keskmine

Üks veerg saab näidata ainult üht tüüpi arvutatud väärtust. Kuid iga tabeli veergu saab konfigureerida nii, et see näitaks erinevat tüüpi arvutatud väärtust.

### <a name="showing-the-grid-footer"></a>Ruudustiku jaluse kuvamine
Finantside ja operatsioonide rakenduste iga vahekaardi allosas on jaluse ala. Jalus näitab olulist teavet, mis on seotud ruudustikus kuvatavate andmetega. Siin on mõned näited sellest teabest.

- Valitud ridade arv tabelis (kui valite rohkem kui ühe kirje)
- Arvutatud väärtused konfigureeritud veergude allosas, numbrilised veerud (nt kogusummad)
- Andmekogumi ridade arv 

See jalus on vaikimisi peidetud, kuid saate selle sisse lülitada. Ruudustiku jaluse kuvamiseks paremklõpsake **ruudustiku valikute** nuppu ruudustiku päises ja valige suvand **Kuva jalus**. Kui olete konkreetse ruudustiku jaluse sisse lülitanud, peetakse see seadistus meeles, kuni kasutaja otsustab jaluse peita. Jaluse peitmiseks valige suvand **Peida jalus** **Ruudustiku valikute** menüüs.

### <a name="specifying-columns-with-calculated-values"></a>Arvutatud väärtustega veergude määramine
Praegu ei näita ükski veerg arvutatud väärtusi vaikimisi. Selle asemel peetakse seadistust üheks tegevuseks, nagu näiteks veergude laiuste korrigeerimine ruudustikes. Pärast seda, kui olete määranud, et soovite vaadata veeru arvutatud väärtust, jääb see säte alles järgmisel lehel käies.

Arvutatud väärtuse näitamiseks veeru konfigureerimiseks on kaks viisi:

- Valige ja hoidke all (või paremklõpsake) veerus, mille arvutatud väärtust soovite vaadata. Kui laiendatud **ruudustiku liitmise võimaluse** funktsioon on lubatud, valige **suvand Kuva** veeru kogusummad ja seejärel valige soovitud arvutatud väärtus. Kui see funktsioon pole lubatud, valige suvand **Summeeri see veerg**. See tegevus põhjustab kolme sündmuse toimumist.

    1. Ruudustiku jalus muutub nähtavaks. 
    2. Teie eelistus veeru arvutatud väärtuse vaatamiseks on salvestatud. 
    3. Soovitud arvutus käivitatakse veeru ja teiste eelnevalt konfigureeritud arvutatud väärtuse kuvamiseks konfigureeritud veergude puhul. Arvutatud väärtuste näitamiseks vajalik aeg sõltub andmekomplekti mahust.

- Kui jalus on nähtaval, valige kokkuvõtte kuvamine (**·** **või valige arvutatud väärtus, kui laiendatud ruudustiku liitmise funktsioon on lubatud) veeru allosas jaluse alas**, **mille** kohta soovite arvutatud väärtust vaadata. Kui konfigureeritud veerge pole, on see nupp saadaval kõigi numbriveergude jaluses.

    Kui arvutatud väärtuse näitamiseks on konfigureeritud vähemalt üks veerg, **on** nupp Kuva kogusumma (**või** Vali arvutatud väärtus) saadaval ainult hoveris või fookuses. Nupu valimise toiming salvestab teie eelistuse arvutatud väärtuse vaatamiseks veerus, nii et eelistust rakendatakse tulevastele leheküljekülastustele. Jaluses näitab seda olekut veerus ilmuv kriips. (Pange tähele, et arvutatud väärtus ilmub kohe, kui andmekogum on piisavalt väike.)

Kui teete vea ja ei soovi enam konkreetses **veerus arvutatud väärtust vaadata, valige ja hoidke all (või paremklõpsake)** veerus ja seejärel valige suvand Peida **kogusumma (või \> kuva veeru kogusummad Pole, kui** **laiendatud** ruudustiku liitmise funktsioon on lubatud). Teise võimalusena valige **selle veeru jaluses** **suvand Peida kogusumma** (või Peida arvutatud väärtus). See eelistus salvestatakse ka tulevastele lehekülastuste jaoks. 

### <a name="calculating-aggregate-values"></a>Kokkuvõtteväärtuste arvutamine
Kui te lähete leheküljele, kus jalus on nähtaval ja veerud on juba konfigureeritud arvutatud väärtusi kuvama, ei pruugi need väärtused jaluses näha. Käitumine sõltub leheküljel oleva andmekomplekti mahust. Kui andmekogum on piisavalt väike, kuvatakse arvutatud väärtused automaatselt koos andmekomplekti ridade arvuga. Kui teie konfigureeritud veergude all on jaluses mõttekriipsud, on andmekomplekti väärtus süsteemi jaoks liiga suur, et arvutatud väärtusi kohe näidata. Sellisel juhul on väärtuste arvutamiseks vajalik selgesõnaline tegevus. Väärtuste arvutamiseks klõpsake jaluses **nuppu** Arvuta. Teise võimalusena valige ja hoidke all (või paremklõpsake) veerus, mille kogusummasid soovite vaadata ja **seejärel** valige suvand Summeeri see veerg (**või** Kuva veeru kogusummad ja seejärel **soovitud** arvutatud väärtus, kui laiendatud ruudustiku liitmise funktsioon on lubatud).

Kui arvutuse läbimine võtab kaua aega, saate operatsiooni igal ajal tühistada, kui valite **Tühista**. Mõnikord on andmekogumid liiga suured, et arvutada koondväärtusi (teie organisatsiooni kehtestatud limiit). Sel juhul teavitatakse teid hoopis, et andmeid rohkem filtreerida.

> [!NOTE]
> Süsteemiadministraatorid **saavad** **muuta** kokkuvõtte arvutamiseks saadaoleva kirjete arvu limiiti, kohandades igale kliendi jõudluse suvandite lehel olevale ruudustiku parameetrile kohalike kirjete maksimaalset arvu. Vaikeväärtus on 25 000 kirjet. Administraatorid peaksid seda väärtust korrigeerides olema ettevaatlik, sest liiga suur väärtus võib kasutajale saadaoleva mälu oma arvutisse lisada. Soovitame, et väärtus ei ületaks 50 000 kirjet.

Arvutatud väärtused uuendatakse andmekomplekti ridade uuendamisel, kustutamisel või loomisel automaatselt.

## <a name="typing-ahead-of-the-system"></a>Süsteemist eespool tippimine
Paljudes äriolukordades on väga oluline, et andmed sisestataks kiiresti süsteemi. Enne uue ruudustiku juhtelemendi sissejuhatust saavad kasutajad muuta andmeid ainult praegusel real. Seetõttu ei saanud kasutajad pärast reas muudatuste tegemist lülituda ümber teise reale ega luua uut rida enne, kui süsteem on praeguses reas tehtud muudatused edukalt kinnitanud ja (rea loomise puhul) käivitanud kogu loogika, mis on seotud uue rea loomisega. Selleks, et aidata vähendada kasutajate poolt nende toimingute lõpuleviidud ootamise aega ja aidata kasutaja tööviljakust parandada, kohandab uus ruudustik neid tegevusi asünkroonseks. Kasutajad saavad luua uusi ridu või teisaldada neid teistele ridadele, et teha muudatusi, kui eelmised rea kinnitamised ja rea loomise loogika on ootel. 

[![Süsteemist ees tippimine.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Selle uue funktsiooni toetamiseks on rea valimise veeru paremasse osasse lisatud uus veerg, kui ruudustik on redigeerimisrežiimis. See veerg näitab üht järgmistest olekutest.

- **Tühi** – olekukujutise puudumine näitab, süsteem on rea edukalt salvestanud.
- **Ootel töötlemine** – see olek näitab, et rea muudatusi pole veel serverisse salvestatud, aga need on töötlemist vajavate muudatuste järjekorras. Enne väljaspool ruudustikku toimingu tegemist peate ootama, kuni kõik ootel muudatused töödeldakse. Lisaks on nende ridade tekst kaldkirjas, et näidata ridade salvestamata olekut. 
- **Kehtetu olek** – see olek näitab, et rea töötlemine käivitas mingisuguse hoiatuse või teate ja see võis takistada süsteemil selle rea muudatuste salvestamist. Kui salvestamistoiming nurjus, siis suunati teid vanas ruudustikus tagasi rea juurde, et probleem kohe lahendada. Uues ruudustikus aga teavitatakse teid kinnitamisprobleemist, kuid te saate otsustada, millal soovite rea probleeme parandada. Kui olete valmis probleemi lahendama, saate fookuse käsitsi tagasi reale viia. Teise võimalusena saate valida toimingu **Probleemi lahendamine**. See tegevus viib kohe fookuse tagasi probleemsele reale ja võimaldab teil teha muudatusi ruudustiku sees või väljaspool seda. Pange tähele, et järgnevate ootel ridade töötlemine peatatakse seni, kuni see kinnitamise hoiatus on lahendatud. 
- **Peatatud** – see olek näitab, et serveris on töötlemine peatatud, kuna rea kinnitamine käivitas hüpikdialoogiboksi, mis nõuab kasutaja tähelepanu. Kuna kasutaja võib olla sisestamas andmeid mõnele muule reale, ei kuvata kasutajale hüpikdialoogiboksi kohe. Selle asemel kuvatakse see siis, kui kasutaja valib töötlemise jätkamise. Olekule on lisatud teatis, milles teavitatakse kasutajat olukorrast. Teatis sisaldab tegevust **Jätka töötlemist**, mis käivitab hüpikdialoogiboksi.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Erinevused süsteemist ette andmete sisestamisel
Kui sisestate andmed enne süsteemi töötlemist, võite andmesisestuskogemuses oodata mõnda muudatust.

- Te märkate, et puuduvad otsingu ripploendid, väljaväärtusi ei kontrollita pärast sama rea teise veergu teisaldamist ja veergudel ei näidata algselt vaikeväärtusi. Selline käitumine ilmneb siis, kui loote või värskendate süsteemist ees. Kuid pärast seda, kui süsteem asub kohani, kus te praegu redigeerite, jätkub standardne kogemus. Kui tegite muudatusi väljale, mis tavaliselt võtab vastu vaikeväärtuse, alistavad teie muudatused välja vaikeväärtuse, kui server hakkab rida töötlema.
- Kui loote allanooleklahvi abil uue **rea**, kuvatakse kõik ruudustiku veerud redigeeritavaks. Vaikimisi seatakse fookus uue rea esimesse veergu. See veerg ei pruugi olla sama veerg, mis sai algse fookuse pärandruudustikus või sama veerg, mis saab fookuse pärast nupu **Uus** klõpsamist. Teie organisatsioon saab kohandada süsteemi ja muuta veergu, mis võtab vastu algse fookuse, kui **on valitud alla-noole** võti. Lisateavet vt jaotisest Veeru määramine, [mis võtab vastu algse fookuse uute ridade loomisel, kasutades alla-noole klahvi jaotist](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Sõltumata sellest, saate kasutada isikupärastamist iga andmesisestusruudustiku optimeerimiseks. Konkreetselt saate ümber tellida välju nii, et esimene veerg on veerg, kuhu soovite andmeid sisestada. Te soovite võib-olla ka üldises andmesisestuses välju ümber tellida, et vähendada vahekaartide peatusi ja peita väljad, mis ei ole selles vaates andmesisestuses nõutavad.

### <a name="pasting-from-excel"></a>Kleepimine Excelist
Kasutajatel on alati olnud võimalik finantside ja toimingute rakenduste ruudustike andmeid Microsoft Excel eksportida, **kasutades Excelisse eksportimise mehhanismi**. Kuid võimalus sisestada andmeid süsteemist ette võimaldab uuel ruudustikul toetada tabelite kopeerimist Excelist ja nende otse finantside ja toimingute rakenduste ruudustikke. Ruudustiku lahter, millelt kleepimistoimingut alustati, määrab, kuhu kopeeritud tabel kleebitakse. Ruudustiku sisu kirjutatakse kopeeritud tabeli sisuga üle, välja arvatud kahel järgmisel juhul.

- Kui kopeeritud tabeli veergude arv ületab kleepimise asukohast alates ruudustikku jäävate veergude arvu, teavitatakse kasutajat, et lisaveergusid eirati. 
- Kui kopeeritud tabeli ridade arv ületab kleepimise asukohast alates ruudustiku ridade arvu, kirjutatakse olemasolevad lahtrid kleebitud sisuga üle ja kõik kopeeritud tabeli lisaread lisatakse ruudustiku allossa uute ridadena. 

## <a name="evaluating-math-expressions"></a>Matemaatiliste avaldiste hindamine
Tootlikkuse tõstmiseks saavad kasutajad sisestada ruudustiku numbrilahtritesse matemaatilisi valemeid. Nad ei pea tegema arvutust süsteemivälises rakenduses. Näiteks kui sisestate **=15\*4** ja vajutate siis väljalt välja liikumiseks **tabeldusklahvi**, hindab süsteem avaldist ja salvestab välja jaoks väärtuse **60**.

[![oma avaldiste hindamine;](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Selleks et süsteem tuvastaks avaldise väärtuse, käivitage väärtus võrdusmärgiga (**=**). Lisateavet toetatud tehtemärkide ja süntaksi kohta vt teemast [Toetatud matemaatilised sümbolid](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Versiooni 10.0.29 kohaselt on võimalus hinnata numbrilistes juhtelementides avaldisi ja on nüüd saadaval ka väljaspool ruudustikku.

## <a name="grouping-tabular-data"></a>Tabeli andmete grupeerimine
Ärikasutajad peavad sageli tegema andmete sihtanalüüsi. Kuigi seda analüüsi Microsoft Excel saab teha andmete eksportimisel liigendtabelitabelisse ja kasutades seda, **võimaldab grupeerimine ruudustikes funktsioon, mis sõltub uuest ruudustiku juhtelemendi funktsioonist, võimaldab kasutajatel organiseerida oma tabeldusandmeid huvitavatel viisidel finantside ja toimingute rakenduste piires**. Kuna see funktsioon laiendab **arvutatud** väärtuste funktsiooni, **võimaldab** grupeerimine saada otstarbekaid vihjeid andmete kohta, pakkudes grupi tasemel arvutatud väärtusi (nt vahesummasid).

[![Grupeerimisandmed ruudustikus.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Selle funktsiooni kasutamiseks paremklõpsake veergu, mille alusel soovite rühmitada, ja valige käsk **Rühmita selle veeru järgi**. See tegevus sordib andmed valitud veeru alusel, lisab uue veeru **Rühmitamisalus** ruudustiku algusse ja lisab iga grupi algusesse päise read. Need päise read annavad iga grupi kohta järgmist teavet.

- Grupi andmete väärtus 
- Veeru nimi (see teave on eriti kasulik, kui teil on rühmitamise mitu taset.)
- Selles grupis olevate andmeridade arv
- Arvutatud väärtused mis tahes konfigureeritud veeru jaoks (nt vahesummad, kui veerg on konfigureeritud kuvama kogusummat)

Kui [salvestatud](saved-views.md) vaated on lubatud, saate grupeerimise salvestada osana lehtede vaatest, mis võimaldab päringuid vaadetesse salvestada. Näiteks suure vaatevalijatega. Lisateavet vt [jaotisest Vaadete](saved-views.md#switching-between-views) vahetamine. 

### <a name="multiple-levels-of-grouping"></a>Rühmitamise mitu taset
Kui olete andmed ühe veeru kaupa rühmitanud, saate andmed rühmitada erineva veeru alusel, valides soovitud veerus suvandi **Rühmita selle veeru järgi**. Seda protsessi saab korrata seni, kuni teil on 5 pesastatud rühmitamise taset, mis on maksimaalne toetatud sügavus. Praegusel hetkel ei saa te enam täiendavate veergude alusel rühmitada.

Saate igal ajal teisaldada rühmitamise mis tahes veerule paremklõpsates seda veergu ja valides suvandi **Tühista rühmitamine**. Saate rühmitamise kõikidelt veergudelt eemaldada, kui valite suvandi **Ruudustiku suvandid** ja seejärel **Tühista kõikide rühmitamine**.

### <a name="sorting-grouped-data"></a>Grupeeritud andmete sortimine
Pärast andmete grupeerimist ühe või mitme veeru järgi saate vastava veerupäise kaudu muuta mis tahes grupeerimisveeru sortimissuunda. 

Grupeerimata veeru sortimisel jääb grupeerimine alles. Andmed sorditakse igas grupis valitud veeru alusel.

### <a name="expanding-and-collapsing-groups"></a>Gruppide laiendamine ja ahendamine
Andmete algsel grupeerimisel on kõik grupid laiendatud. Andmete summeeritud vaateid saate luua üksikute rühmade ahendamise abil või kasutada andmete navigeerimisel grupi laiendamist ja ahendamist. Grupi laiendamiseks või ahendamiseks valige vastava grupi päisereal nupp Rööpnool (>). Pange tähele, et üksikute gruppide laiendamis-/ahendamisolek on **pole** salvestatud isikupärastamise võimalustes.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Ridade valimine ja valiku tühistamine grupi tasemel
Samamoodi nagu ruudustiku kõigi ridade valimiseks (või valiku tühistamiseks) saate märkida ruudustiku esimese veeru ülaosas oleva ruudu, saate kiiresti valida (või valiku tühistada) kõik grupi read, kui märgite vastava grupi päiserea ruudu. Grupi päiserea märkeruut kajastab alati selle grupi ridade praegust valikuolekut, olenemata sellest, kas kõik read on valitud, ühtegi rida pole valitud või on valitud ainult mõned read.

### <a name="hiding-column-names"></a>Veeru nimede peitmine
Andmete grupeerimisel kuvatakse veeru nimi grupi päisereal vaikimisi. Te saate veeru nime grupi päiseridades peita, valides **Ruudustiku suvandid** > **Peida grupi veeru nimi**.

### <a name="grouping-on-date-and-time-columns"></a>Grupeerimine kuupäeva ja kellaaja veergudel
Kui grupeerite väljadel Kuupäev või Kuupäev/kellaaeg, saate grupeerida aasta, kuu või päeva järgi. Vastava päiserea grupp "väärtus" vastab selle välja vormingule. Lisaks saate väljade DateTime ja Time puhul grupeerida tunni, minuti või teise järgi.

> [!IMPORTANT]
> Kasutajad ei saa praegu grupeerimisveeru pärast kuupäeva- või kellaajaveeru segmendile grupeerimist lisada.

## <a name="freezing-columns"></a>Veergude külmutamine
Mõned ruudustiku veerud võivad olla piisavalt olulised konteksti jaoks, et te ei soovi neid vaatest välja kerida. Selle asemel võite soovida, et väärtused nendes veergudes oleks alati nähtavad. Ruudustiku **külmutamise veergude funktsioon** pakub kasutajatele paindlikkust. 

[![Veergude külmutamine ruudustikus.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Veeru külmutamiseks paremklõpsake veeru päist ja valige seejärel suvand **Külmuta veerg**. Selle sammu esmakordsel lõpuleviimisel muutub valitud veerg esimeseks veeruks ja ei keri enam vaatest välja. Kõik järgmised külmutatud veerud lisatakse viimasest külmutatud veerust paremale. Saate külmutatud veergude järjestuse vastavalt vajadusele muutmiseks kasutada tavalist liigutamise funktsiooni. Samas ei saa külmutatud veerge liigutada nii, et need ilmuksid külmutamata veergude hulgas. Sarnaselt ei saa külmutamata veerge liigutada nii, et need ilmuksid külmutatud veergude hulgas.

Veeru külmutamisest vabastamiseks paremklõpsake külmutatud veeru päist ja valige seejärel suvand **Vabasta veerg külmutamisest**. 

Pange tähele, et uue ruudustiku rea valiku ja rea oleku veerud on esimeses kahes veerus alati külmutatud. Kui need veerud on ruudustikku kaasatud, on nad seetõttu alati kasutajatele nähtavad hoolimata ruudustiku horisontaalsest kerimisasukohast. Nende kahe veeru järjestust ei saa muuta.

## <a name="autofit-column-width"></a>Veeru laiuse automaatkorrekteerimine
Nagu Excelis, saavad kasutajad muuta veeru suurust automaatselt, võttes aluseks praegu kuvatud sisu. Topeltklõpsake (või topeltklõpsake) veerus soovitud suuruse muutmise pidemeid. Teise võimalusena asetage fookus veeru päisesse ja seejärel valige **A-võti** (automaatseks tarbeks).

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kuidas lubada uut ruudustiku juhtelementi oma keskkonnas? 

Funktsioon **Uus ruudustiku juhtelement** on kõikides keskkondades saadaval otse funktsioonihalduses. Pärast funktsioonihalduse funktsiooni lubamist kasutavad kõik järgnevad kasutajaseansid uut ruudustiku juhtelementi. 

See funktsioon algas vaikimisi versioonis 10.0.21. See on mõeldud kohustuslikuks muutumist 2022. aasta oktoobers.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Arendajatele] Üksikutelt lehtedelt ruudustiku eemaldamine 
Kui teie organisatsioon avastab lehekülje, millel on uue ruudustiku kasutamisega probleeme, saate kasutada API-t, et lubada üksikul vormil kasutada ruudustiku pärandjuhtelementi ja samas lubada ülejäänud süsteemil kasutada uut ruudustiku juhtelementi. Et eemaldada ruudustik üksikult lehelt, lisage kutse `super()` vormi meetodile `run()`.

```this.forceLegacyGrid();```

Pärandruudustiku juhtelemendi eemaldamiseks on API lõpuks mittetaunitav. Kuid see jääb alles vähemalt 12 kuuks pärast selle amortiseerumist. Kui mõne probleemi korral on vaja kasutada seda API-d, teatage sellest Microsoftile.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Lehe sundimine kasutama uut ruudustikku pärast ruudustikust varem loobumist
Kui olete uue ruudustiku kasutamisest loobunud, võite soovida hiljem uue ruudustiku uuesti lubada pärast põhiprobleemide lahendamist. Selleks peate lihtsalt eemaldama kutse üksusesse `forceLegacyGrid()`. Muudatus ei jõustub enne, kui toimub üks järgmisest:

- **Keskkonna ümberpaigutamine**: kui keskkonda värskendatakse ja juurutatakse uuesti, siis tühjendatakse automaatselt tabel, mis talletab lehed, mis on uuest ruudustikust (FormControlReactGridState) automaatselt loobunud.
- **Tabeli käsitsi tühjendamine**: juurutamisstsenaariumide jaoks, kui teil tuleb kasutada SQL-i FormControlReactGridState tabeli tühjendamiseks ja seejärel taaskäivitada AOS. See tegevuste kombinatsioon lähtestab uuest ruudustikust keeldunud lehekülgede vahemälustuse.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Arendaja] Üksikute ruudustike tippimine süsteemivõimalustest ees
Mõned stsenaariumid on tekkinud, mis ei laena *end* ruudustiku süsteemivõimalustest ette tippimiseks. (Näiteks mõni kood, mis käivitatakse, kui rida kinnitatakse, käivitab andmeallika uuringute käivitamise ja uurimine võib seejärel rikkuda olemasolevate ridade kinnitamata redigeerimisi.) Kui teie organisatsioon avastab sellise stsenaariumi, on saadaval API, mis võimaldab arendajal asünkroonsest rea kinnitamisest individuaalse ruudustiku valida ja pärandkäitumise taastada.

Kui asünkroonne rea kinnitamine on ruudustikus keelatud, ei saa kasutajad uut rida luua ega teisaldada ruudustikus muule olemasolevale reale, kui praeguses reas on kinnitamisprobleeme. Selle tegevuse kõrval ei saa tabeleid Excelist finantsidesse ja toimingute ruudustikes kleepida.

Üksiku ruudustiku asünkroonsest rea kinnitamisest loobumiseks lisage vormi meetodile `super()` järgmine `run()` kutse.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Seda kutset tuleks kutsuda ainult erandlikel juhtudel ja see ei tohiks olla kõigi ruudustike norm.
> - Me ei soovita seda API-d pärast vormi koormamist käitusajal sisse lülitada.

## <a name="developer-size-to-available-width-columns"></a>[Arendajale] Saadaoleva laiusega veerud
Kui arendaja seab uue ruudustiku veergude puhul atribuudi **WidthMode** väärtuseks **SizeToAvailable**, on neil veergudel esialgu sama laius, mis neil oleks siis, kui atribuudi väärtuseks oleks seatud **SizeToContent**. Sellest hoolimata venitatakse neid, et kasutada ruudustikus saadaolevat lisalaiust. Kui atribuudi väärtuseks on seatud **SizeToAvailable** mitme veeru puhul, jagavad kõik need veerud ruudustikus saadaolevat lisalaiust. Kui kasutaja muudab ühe sellise veeru suurust aga käsitsi, muutub veerg staatiliseks. Selle laius jääb samaks ja seda ei venitata, et kasutada ruudustikus saadaolevat lisalaiust.

## <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Arendaja] Veeru määramine, mis võtab vastu algse fookuse uute ridade loomisel alla-noole klahviga
[Nagu](#differences-when-entering-data-ahead-of-the-system) on süsteemijaost ees andmeid sisestades esitatud erinevustes, siis kui võimalus "Süsteemist ette tippimine" **on** lubatud ja kasutaja loob allanooleklahvi abil uue rea, on vaikekäitumine panna fookus uue rea esimesse veergu. See kogemus võib erineda pärandruudustiku kogemusest või kui **valitakse** nupp Uus.

Kasutajad ja organisatsioonid saavad luua andmesisestustele optimeeritud salvestatud vaateid. (Näiteks saate veerge ümber järjestada nii, et esimene veerg on see, kuhu soovite andmeid sisestada.) Lisaks saab organisatsioonid versiooni 10.0.29 **kohaselt seda käitumist korrigeerida meetodiga selectedControlOnCreate(**). See meetod võimaldab arendajal määrata veeru, mis peaks saama algse fookuse uue rea loomisel alla-noole **klahvi** abil. Sisendina võtab see API juhtelemendi ID, mis vastab veerule, mis peaks vastu võtma algse fookuse.

## <a name="known-issues"></a>Teadaolevad probleemid
See jaotis sisaldab uue ruudustiku juhtelemendi teadaolevate probleemide loendit.

### <a name="open-issues"></a>Lahendamata probleemid
- Pärast funktsiooni **Uus ruudustiku juhtelement** kasutatakse mõnel lehel jätkuvalt olemasolevat ruudustiku juhtelementi. See juhtub järgmistes olukordades.
 
    - Lehel on kaardiloend, mida renderdatakse mitmes veerus.
    - Lehel on rühmitatud kaartide loend.
    - Ruudustiku veerus on mittereageeriv laiendatav juhtelement.

    Kui kasutaja seisab ühega neist olukordadest esimest korda silmitsi, kuvatakse teade lehe värskendamise kohta. Pärast selle teate kuvamist jätkab leht olemasoleva ruudustiku kasutamist kõigi kasutajate puhul kuni järgmise tooteversiooni värskenduseni. Nende stsenaariumide paremat käsitlemist, et uut ruudustikku saaks kasutada, kaalutakse tulevases värskenduses.

- [KB 4582758] Kirjed on udused, kui muudate suumi 100 pealt mis tahes teisele protsendile

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

