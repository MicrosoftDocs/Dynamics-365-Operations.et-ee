---
title: Ruudustiku võimalused
description: Selles teemas kirjeldatakse ruudustiku juhtelemendi mitmeid võimsaid funktsioone. Nende võimaluste kasutamiseks peate lubama uue ruudustiku funktsiooni.
author: jasongre
ms.date: 10/25/2021
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
ms.openlocfilehash: a21a41399b5884fda9cce214f99851ffa93bbc43
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700133"
---
# <a name="grid-capabilities"></a>Ruudustiku võimalused

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Uus ruudustiku juhtelement pakub mitmeid kasulikke ja võimsaid võimalusi, mida saate kasutada kasutaja tootlikkuse suurendamiseks, teie andmetest huvitavate vaadete loomiseks ja sisukate ülevaadete hankimiseks andmete jaoks. Selles artiklis tutvustatakse järgmisi võimalusi. 

-  Summade arvutamine
-  Süsteemist eespool tippimine
-  Matemaatiliste avaldiste hindamine 
-  Tabeli andmete grupeerimine (lubatud eraldi kasutades **Grupeerimine võrkudes** funktsiooni)
-  Veergude külmutamine
-  Veeru laiuse automaatkorrekteerimine
-  Venitatavad veerud

## <a name="calculating-totals"></a>Summade arvutamine
Rakendustes Finance and Operations on kasutajatel võimalik ruudustiku numbriveergude allosas näha kogusummasid. Ruudustiku allosas olev jaluse jaotis näitab neid kogusummasid. 

### <a name="showing-the-grid-footer"></a>Ruudustiku jaluse kuvamine
Finance and Operationsi rakendustes on igas tabeliruudustikus allosas jaluse ala. Jalus näitab olulist teavet, mis on seotud ruudustikus kuvatavate andmetega. Siin on mõned näited sellest teabest.

- Valitud ridade arv tabelis (kui valite rohkem kui ühe kirje)
- Konfigureeritud arvveergude allosas olevad kogusummad
- Andmekogumi ridade arv 

See jalus on vaikimisi peidetud, kuid saate selle sisse lülitada. Ruudustiku jaluse kuvamiseks paremklõpsake **ruudustiku valikute** nuppu ruudustiku päises ja valige suvand **Kuva jalus**. Kui olete konkreetse ruudustiku jaluse sisse lülitanud, peetakse see seadistus meeles, kuni kasutaja otsustab jaluse peita. Jaluse peitmiseks valige suvand **Peida jalus** **Ruudustiku valikute** menüüs.  

### <a name="specifying-columns-with-totals"></a>Veergude määramine kogusummade abil
Praegu ei kuva ükski veerg kogusummat vaikimisi. Selle asemel loetakse seda ühekordse häälestuse toiminguks, mis on sarnane veergude laiuste kohandamisega ruudustikes. Kui olete määranud, et soovite näha veeru kogusummasid, kuvatakse teile seda sätet järgmisel lehekülastusel.  

Veeru konfigureerimiseks kogusumma kuvamiseks on kaks võimalust. 

- Paremklõpsake veergu, mille kogusummat soovite näha, ja valige seejärel suvand **Selle veeru kogusumma**. See tegevus põhjustab kolme sündmuse toimumist.

    1. Jalus muutub nähtavaks. 
    2. Teie eelistus selle veeru kogusumma nägemiseks salvestatakse. 
    3. Käivitatakse kogusummade arvutus selle veeru ja mis tahes teiste veergude jaoks, mille kogusummad konfigureerisite. Kogusumma kuvamiseks vajalik aeg sõltub andmekogumi suurusest, mille summeerite.

- Kui jalus on nähtav, valige veeru, mille kogusummat soovite näha, allosas jaluse alas suvandit **Kuva kogusumma**. Kui konfigureeritud veerge pole, on kõigi arvveergude jaoks saadaval nupp **Kuva kogusumma**. 

    Pärast seda, kui vähemalt üks veerg on kogusummade jaoks konfigureeritud, on nupud **Kuva kogusumma** saadaval ainult hõljumisel või fookustamisel. Suvandi **Kuva kogusumma** valimise tegevus ainult salvestab teie eelistused selle veeru kogusumma nägemiseks, nii et eelistus rakendatakse lehe tulevaste külastuste ajal. Jaluses näitab seda olekut veerus ilmuv kriips. (Teie võimalusena kui andmekomplekt on piisavalt väike, kuvatakse kogusumma kohe.)

Kui teete vea ega soovi enam kogusummat kindlas veerus näha, paremklõpsake veergu ja valige käsk **Peida kogusumma** või selle veeru jaluses nupp **Peida kogusumma**. See eelistus salvestatakse ka tulevastele lehekülastuste jaoks. 

### <a name="calculating-totals"></a>Summade arvutamine
Kui avate lehe, mille jalus on nähtav ja veerud on kogusummade jaoks juba konfigureeritud, võivad kogusummad olla jaluses kuvatud, kuid see ei pruugi nii olla. Käitumine oleneb leheküljel oleva andmekogumi suurusest. Kui andmekogum on piisavalt väike, kuvatakse kogusummad automaatselt koos andmekogumi ridade arvuga. Kui kogusummade jaoks konfigureeritud veergude all jaluses on kriipsud, siis on andmekogum süsteemi jaoks liiga suur, et kogusummasid kohe kuvada. Seetõttu on kogusummade arvutamiseks vaja selget toimingut. Selleks klõpsake jaluses nuppu **Arvuta** või paremklõpsake veerul, mida soovite kokku arvutada, ja valige käsk **Selle veeru kogusumma**.  

Kui arvutamine võtab liiga kaua aega, saate toimingu tühistada, klõpsates nuppu **Tühista**. Mõnikord on andmekogum kogusummade arvutamiseks siiski liiga suur (selle piiri kehtestab teie organisatsioon) ja teil palutakse andmeid rohkem filtreerida.

Kogusummasid värskendatakse automaatselt, kui uuendate, kustutate või loote andmekogumi ridu.  

## <a name="typing-ahead-of-the-system"></a>Süsteemist eespool tippimine
Paljudes äriolukordades on väga oluline, et andmed sisestataks kiiresti süsteemi. Enne uue ruudustiku juhtelemendi kasutuselevõttu said kasutajad muuta andmeid ainult praeguses reas. Enne uue rea loomist või teise rea avamist pidid nad ootama, kuni süsteem kõik muudatused edukalt kinnitas. Selleks et vähendada aega, mil kasutajad ootavad kinnituste lõpule viimist, ja parandada kasutajate tootlikkust, kohandab uus ruudustik neid kinnitusi asünkroonselt. Seetõttu saab kasutaja avada muudatuste tegemiseks teisi ridu, samal ajal kui eelmise rea muudatused on veel ootel. 

Selle uue funktsiooni toetamiseks on rea valimise veeru paremasse osasse lisatud uus veerg, kui ruudustik on redigeerimisrežiimis. See veerg näitab üht järgmistest olekutest.

- **Tühi** – olekukujutise puudumine näitab, süsteem on rea edukalt salvestanud.
- **Ootel töötlemine** – see olek näitab, et rea muudatusi pole veel serverisse salvestatud, aga need on töötlemist vajavate muudatuste järjekorras. Enne väljaspool ruudustikku toimingu tegemist peate ootama, kuni kõik ootel muudatused töödeldakse. Lisaks on nende ridade tekst kaldkirjas, et näidata ridade salvestamata olekut. 
- **Kehtetu olek** – see olek näitab, et rea töötlemine käivitas mingisuguse hoiatuse või teate ja see võis takistada süsteemil selle rea muudatuste salvestamist. Kui salvestamistoiming nurjus, siis suunati teid vanas ruudustikus tagasi rea juurde, et probleem kohe lahendada. Uues ruudustikus aga teavitatakse teid kinnitamisprobleemist, kuid te saate otsustada, millal soovite rea probleeme parandada. Kui olete valmis probleemi lahendama, saate fookuse käsitsi tagasi reale viia. Teise võimalusena saate valida toimingu **Probleemi lahendamine**. See tegevus viib kohe fookuse tagasi probleemsele reale ja võimaldab teil teha muudatusi ruudustiku sees või väljaspool seda. Pange tähele, et järgnevate ootel ridade töötlemine peatatakse seni, kuni see kinnitamise hoiatus on lahendatud. 
- **Peatatud** – see olek näitab, et serveris on töötlemine peatatud, kuna rea kinnitamine käivitas hüpikdialoogiboksi, mis nõuab kasutaja tähelepanu. Kuna kasutaja võib olla sisestamas andmeid mõnele muule reale, ei kuvata kasutajale hüpikdialoogiboksi kohe. Selle asemel kuvatakse see siis, kui kasutaja valib töötlemise jätkamise. Olekule on lisatud teatis, milles teavitatakse kasutajat olukorrast. Teatis sisaldab tegevust **Jätka töötlemist**, mis käivitab hüpikdialoogiboksi.  
    
Kui kasutajad sisestavad andmeid kohas, kuhu serveritöötlus pole veel jõudnud, võib nende andmesisestuskogemus olla halvem, näiteks puuduvad otsingud, kontrolli tasemel kinnitamine ja vaikeväärtuste sisestamine. Kasutajatel, kellel on väärtuse leidmiseks vaja ripploendit, soovitatakse oodata, kuni server jõuab praegusele reale. Kontrolli tasemel kinnitamist ja vaikeväärtuste sisestamist saab samuti teha, kui server töötleb seda rida.   

### <a name="pasting-from-excel"></a>Kleepimine Excelist
Kasutajad on alati saanud eksportida andmeid Finance and Operations`i rakendustest rakendusse Microsoft Excel kasutades suvandi **Ekspordi Excelisse** mehhanisme. Kuna andmeid saab sisestada enne süsteemi, toetab uus ruudustik tabelite kopeerimist Excelist ja nende kleepimist otse Finance and Operationsi rakenduste ruudustikesse. Ruudustiku lahter, millelt kleepimistoimingut alustati, määrab, kuhu kopeeritud tabel kleebitakse. Ruudustiku sisu kirjutatakse kopeeritud tabeli sisuga üle, välja arvatud kahel järgmisel juhul.

- Kui kopeeritud tabeli veergude arv ületab kleepimise asukohast alates ruudustikku jäävate veergude arvu, teavitatakse kasutajat, et lisaveergusid eirati. 
- Kui kopeeritud tabeli ridade arv ületab kleepimise asukohast alates ruudustiku ridade arvu, kirjutatakse olemasolevad lahtrid kleebitud sisuga üle ja kõik kopeeritud tabeli lisaread lisatakse ruudustiku allossa uute ridadena. 

## <a name="evaluating-math-expressions"></a>Matemaatiliste avaldiste hindamine
Tootlikkuse tõstmiseks saavad kasutajad sisestada ruudustiku numbrilahtritesse matemaatilisi valemeid. Nad ei pea tegema arvutust süsteemivälises rakenduses. Näiteks kui sisestate **=15\*4** ja vajutate siis väljalt välja liikumiseks **tabeldusklahvi**, hindab süsteem avaldist ja salvestab välja jaoks väärtuse **60**.

Selleks et süsteem tuvastaks avaldise väärtuse, käivitage väärtus võrdusmärgiga (**=**). Lisateavet toetatud tehtemärkide ja süntaksi kohta vt teemast [Toetatud matemaatilised sümbolid](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Tabeli andmete grupeerimine
Ärikasutajatel on sageli vaja teha andmete ad-hoc-analüüsi. Üks võimalus selle tegemiseks on eksportida andmeid Microsoft Excelisse ja kasutada liigendtabeleid, **Grupeerimine võrkudes** funktsioon, mis sõltub uuest ruudustiku juhtelemendi funktsioonist, võimaldab kasutajatel oma tabeli andmeid põnevatel viisidel Finance and Operationsi rakendustes korraldada. Kuna see funktsioon laiendab funktsiooni **Kogusummad**, võimaldab **Rühmitamine** teil saada ka sisukaid ülevaateid oma andmetest, pakkudes vahesummasid grupi tasandil.

Selle funktsiooni kasutamiseks paremklõpsake veergu, mille alusel soovite rühmitada, ja valige käsk **Rühmita selle veeru järgi**. See tegevus sordib andmed valitud veeru alusel, lisab uue veeru **Rühmitamisalus** ruudustiku algusse ja lisab iga grupi algusesse päise read. Need päise read annavad iga grupi kohta järgmist teavet. 
-  Grupi andmete väärtus 
-  Veeru nimi (see teave on eriti kasulik, kui teil on rühmitamise mitu taset.)  
-  Selles grupis olevate andmeridade arv
-  Kogusummade kuvamiseks konfigureeritud veergude vahesummad

Kui [Salvestatud vaated](saved-views.md) on lubatud, saab selle rühmitamise isikupärastamisena järgmiseks lehekülastuseks salvestada, et saada kiirjuurdepääs.  

### <a name="multiple-levels-of-grouping"></a>Rühmitamise mitu taset
Kui olete andmed ühe veeru kaupa rühmitanud, saate andmed rühmitada erineva veeru alusel, valides soovitud veerus suvandi **Rühmita selle veeru järgi**. Seda protsessi saab korrata seni, kuni teil on 5 pesastatud rühmitamise taset, mis on maksimaalne toetatud sügavus. Praegusel hetkel ei saa te enam täiendavate veergude alusel rühmitada.  

Saate igal ajal teisaldada rühmitamise mis tahes veerule paremklõpsates seda veergu ja valides suvandi **Tühista rühmitamine**. Saate rühmitamise kõikidelt veergudelt eemaldada, kui valite suvandi **Ruudustiku suvandid** ja seejärel **Tühista kõikide rühmitamine**.   

### <a name="expanding-and-collapsing-groups"></a>Gruppide laiendamine ja ahendamine
Andmete algsel grupeerimisel on kõik grupid laiendatud. Andmete summeeritud vaateid saate luua üksikute rühmade ahendamise abil või kasutada andmete navigeerimisel grupi laiendamist ja ahendamist. Grupi laiendamiseks või ahendamiseks valige vastava grupi päisereal nupp Rööpnool (>). Pange tähele, et üksikute gruppide laiendamis-/ahendamisolek on **pole** salvestatud isikupärastamise võimalustes.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Ridade valimine ja valiku tühistamine grupi tasemel
Samamoodi nagu ruudustiku kõigi ridade valimiseks (või valiku tühistamiseks) saate märkida ruudustiku esimese veeru ülaosas oleva ruudu, saate kiiresti valida (või valiku tühistada) kõik grupi read, kui märgite vastava grupi päiserea ruudu. Grupi päiserea märkeruut kajastab alati selle grupi ridade praegust valikuolekut, olenemata sellest, kas kõik read on valitud, ühtegi rida pole valitud või on valitud ainult mõned read.

### <a name="hiding-column-names"></a>Veeru nimede peitmine
Andmete grupeerimisel kuvatakse veeru nimi grupi päisereal vaikimisi. Te saate veeru nime grupi päiseridades peita, valides **Ruudustiku suvandid** > **Peida grupi veeru nimi**.

## <a name="freezing-columns"></a>Veergude külmutamine
Mõned ruudustiku veerud võivad olla piisavalt olulised konteksti jaoks, et te ei soovi neid vaatest välja kerida. Selle asemel võite soovida, et nende veergude väärtused oleks alati nähtaval. Funktsioon **Külmuta ruudustiku veerud** pakub kasutajatele seda paindlikkust. 

Veeru külmutamiseks paremklõpsake veeru päist ja valige seejärel suvand **Külmuta veerg**. Selle sammu esmakordsel lõpuleviimisel muutub valitud veerg esimeseks veeruks ja ei keri enam vaatest välja. Kõik järgmised külmutatud veerud lisatakse viimasest külmutatud veerust paremale. Saate külmutatud veergude järjestuse vastavalt vajadusele muutmiseks kasutada tavalist liigutamise funktsiooni. Samas ei saa külmutatud veerge liigutada nii, et need ilmuksid külmutamata veergude hulgas. Sarnaselt ei saa külmutamata veerge liigutada nii, et need ilmuksid külmutatud veergude hulgas.

Veeru külmutamisest vabastamiseks paremklõpsake külmutatud veeru päist ja valige seejärel suvand **Vabasta veerg külmutamisest**. 

Pange tähele, et uue ruudustiku rea valiku ja rea oleku veerud on esimeses kahes veerus alati külmutatud. Kui need veerud on ruudustikku kaasatud, on nad seetõttu alati kasutajatele nähtavad hoolimata ruudustiku horisontaalsest kerimisasukohast. Nende kahe veeru järjestust ei saa muuta.

## <a name="autofit-column-width"></a>Veeru laiuse automaatkorrekteerimine
Sarnaselt Excel`iga saavad kasutajad automaatselt veeru suurust muuta, võttes aluseks selles veerus praegu kuvatud sisu. Selleks topeltklõpsake veeru suuruse muutmise pidemeid või asetage fookus veeru päisesse ja vajutage nuppu **A** (automaatseks korrektsiooniks). See võimalus on saadaval alates versioonist 10.0.23.  

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kuidas lubada uut ruudustiku juhtelementi oma keskkonnas? 

Funktsioon **Uus ruudustiku juhtelement** on kõikides keskkondades saadaval otse funktsioonihalduses. Pärast funktsioonihalduse funktsiooni lubamist kasutavad kõik järgnevad kasutajaseansid uut ruudustiku juhtelementi. 

See funktsioon lubatakse vaikimisi versioonis 10.0.21 ja see on mõeldud kohustuslikuks versiooniga 10.0.25. 

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Arendajatele] Üksikutelt lehtedelt ruudustiku eemaldamine 
Kui teie organisatsioon avastab lehekülje, millel on uue ruudustiku kasutamisega probleeme, saate kasutada API-t, et lubada üksikul vormil kasutada ruudustiku pärandjuhtelementi ja samas lubada ülejäänud süsteemil kasutada uut ruudustiku juhtelementi. Et eemaldada ruudustik üksikult lehelt, lisage kutse `super()` vormi meetodile `run()`.

 ```this.forceLegacyGrid();```

See API tasutakse seni, kuni uus ruudustiku kontroll muutub kohustuslikuks, mis on praegu mõeldud aprillile 2022. Kui mõne probleemi korral on vaja kasutada seda API-d, teatage sellest Microsoftile.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Lehe sundimine kasutama uut ruudustikku pärast ruudustikust varem loobumist
Kui olete uue ruudustiku kasutamisest loobunud, võite soovida hiljem uue ruudustiku uuesti lubada pärast põhiprobleemide lahendamist. Selleks peate lihtsalt eemaldama kutse üksusesse `forceLegacyGrid()`. Muudatus ei jõustub enne, kui toimub üks järgmisest:

- **Keskkonna ümberpaigutamine**: kui keskkonda värskendatakse ja juurutatakse uuesti, siis tühjendatakse automaatselt tabel, mis talletab lehed, mis on uuest ruudustikust (FormControlReactGridState) automaatselt loobunud.

- **Tabeli käsitsi tühjendamine**: juurutamisstsenaariumide jaoks, kui teil tuleb kasutada SQL-i FormControlReactGridState tabeli tühjendamiseks ja seejärel taaskäivitada AOS. See tegevuste kombinatsioon lähtestab uuest ruudustikust keeldunud lehekülgede vahemälustuse.  

## <a name="developer-size-to-available-width-columns"></a>[Arendajale] Saadaoleva laiusega veerud
Kui arendaja seab uue ruudustiku veergude puhul atribuudi **WidthMode** väärtuseks **SizeToAvailable**, on neil veergudel esialgu sama laius, mis neil oleks siis, kui atribuudi väärtuseks oleks seatud **SizeToContent**. Sellest hoolimata venitatakse neid, et kasutada ruudustikus saadaolevat lisalaiust. Kui atribuudi väärtuseks on seatud **SizeToAvailable** mitme veeru puhul, jagavad kõik need veerud ruudustikus saadaolevat lisalaiust. Kui kasutaja muudab ühe sellise veeru suurust aga käsitsi, muutub veerg staatiliseks. Selle laius jääb samaks ja seda ei venitata, et kasutada ruudustikus saadaolevat lisalaiust.  

## <a name="known-issues"></a>Teadaolevad probleemid
See jaotis sisaldab uue ruudustiku juhtelemendi teadaolevate probleemide loendit.  

### <a name="open-issues"></a>Lahendamata probleemid
-  Pärast funktsiooni **Uus ruudustiku juhtelement** kasutatakse mõnel lehel jätkuvalt olemasolevat ruudustiku juhtelementi. See juhtub järgmistes olukordades.  
    -  Lehel on kaardiloend, mida renderdatakse mitmes veerus.
    -  Lehel on rühmitatud kaartide loend.
    -  Ruudustiku veerus on mittereageeriv laiendatav juhtelement.

    Kui kasutaja seisab ühega neist olukordadest esimest korda silmitsi, kuvatakse teade lehe värskendamise kohta. Pärast selle teate kuvamist jätkab leht olemasoleva ruudustiku kasutamist kõigi kasutajate puhul kuni järgmise tooteversiooni värskenduseni. Nende stsenaariumide paremat käsitlemist, et uut ruudustikku saaks kasutada, kaalutakse tulevases värskenduses.    
    
-  [KB 4582758] Kirjed on udused, kui muudate suumi 100 pealt mis tahes teisele protsendile
-  [KB 4592012] Ootamatu kliendi tõrge IE11-s mitme rea kleepimisel Excelist
    -  Microsoft ei oma probleemile parandust

### <a name="fixed-as-part-of-10016"></a>Parandatud versioonis 10.0.16

-  [KB 4598335] Mitmerealise stringi juhtelemendid ei arvesta loendite/kaartide kuvamiskõrgusega 
-  [KB 4591891] Ridade märkimise tühistamisel lähevad arve soovituse read kaduma
-  [KB 4592104] Kirjeid ei saa pärast nupu Lahenda probleem klõpsamist redigeerida ega liikuda teisele reale kinnitusprobleemi lahendamata
-  [KB 4594449] Kuupäeva valijas puuduvad nupud Mitte kunagi ja Tühjenda 
-  [KB 4594448] Uues ruudustikus koheldakse kellaaja sisestust erinevalt
-  [KB 4600059] Ootamatu kliendi tõrge meili ahendamisega
-  [KB 4574584] Kulude manuse eelvaade pole hiirega üle kviitungi ikooni liikumisel saadaval

### <a name="fixed-as-part-of-10015"></a>Parandatud versioonis 10.0.15    

-  (Kvaliteedivärskendus) [KB 4594444] Ootamatu klienditõrge segmenditud sisestamise juhtimise eelvaatega
-  [KB 4582723] Kuvamise valikuid ei kuvata, kui need tehakse vormi elutsüklis hiljem
-  [KB 4591988] Probleemid klaviatuuri kasutamisel otsingust ReferenceGroup väärtuse valimiseks
-  [KB 4588958] Regression Suite Automation Tool (RSAT) test nurjub tõrkega: TypeError: määratlemata atribuuti „tekst” ei saa lugeda
-  [KB 4591970] Ootamatu kliendi tõrge, kui Excelist kleepimine tehti kohe pärast ruudustikus klõpsamist
-  [KB 4591904] Andmete muudatusi ei salvestata, kui pärast juhtelemendi redigeerimist kasutaja klõpsas kohe ja avas teise juhtelemendi otsingu
-  [KB 4584752] Ootamatu kliendi tõrge projekti arve ettepanekute lehel
-  [KB 4584540] Ruudustikku ei saa pärast üksiku rea töölehe reale kleepimist jätta
-  [KB 4591908] Uue rea loomisel jääb fookus veergu, kus olite

### <a name="fixed-as-part-of-10014"></a>Parandatud versioonis 10.0.14

-  (Kvaliteedi uuendamine) [KB 4584752] Ootamatu kliendi tõrge projekti arve ettepanekute lehel
-  [KB 4583880] Tööriista Regression Suite Automation Tool (RSAT) katsed nurjuvad tegevuse OpenLookup puhul koos teatega „Ei saa lugeda määratlemata atribuuti RowIndex”
-  [KB 4583847] Ootamatu kliendi tõrge läbi otsingute navigeerimisel

### <a name="fixed-as-part-of-10013"></a>Parandatud versioonis 10.0.13

-  (Kvaliteedi uuendamine) [KB 4584752] Ootamatu kliendi tõrge projekti arve ettepanekute lehel
-  (Kvaliteedi uuendamine) [KB 4583880] Tööriista Regression Suite Automation Tool (RSAT) katsed nurjuvad tegevuse OpenLookup puhul koos teatega „Ei saa lugeda määratlemata atribuuti RowIndex”
-  (Kvaliteedi uuendamine) [KB 4583847] Ootamatu kliendi tõrge läbi otsingute navigeerimisel 
-  (Kvaliteedi uuendamine) [Programmiviga 471777] Mobiilirakenduse redigeerimiseks või loomiseks ei saa ruudustikus välju valida
-  [KB 4582727] Ruudustik külmub pärast seda, kui kasutaja saab dialoogi mitme kogusega kaupade jaoks
-  [Programmiviga 474851] Viitegrupi juhtelementides ei tööta hüperlingid 
-  [Programmiviga 474848] Ruudustikega täiustatud eelvaateid ei kuvata
-  [KB 4582726] Atribuudiga RotateSign ei arvestata  
-  [Programmiviga 470173] Passiivsete ridade märkeruudud täidetakse/tühjendatakse, kui lahtris klõpsatakse tühemikku
-  [Programmiviga 474848] Ruudustikega täiustatud eelvaateid ei kuvata
-  [Programmiviga 474851] Viitegrupi juhtelementides ei tööta hüperlingid 
-  [Programmiviga 471777] Mobiilirakenduse redigeerimiseks või loomiseks ei saa ruudustikus välju valida
-  [KB 4569441] Mitme veeruga kaardiloendite, piltide kohtspikrite ja mõnel väljal kuvamisvalikutega seotud probleemid
-  [KB 4575279] Pearaamatust ei kustutata kõiki märgitud ridasid
-  [KB 4575233] Kuvamisvalikuid ei taastata pärast teisele reale üleminemist
-  [Bug 477884] Otsingud tagastavad vale väärtuse/kirje, kui uue ruudustiku juhtelement on aktiveeritud
-  [KB 4571095] Toote sissetulek sisestatakse, kui kogemata vajutakse klahvi Enter (lehe vaiketegevuse õige käsitlemine)
-  [KB 4575437] Redigeeritavate juhtelementidega otsingud sulguvad ootamatult
-  [KB 4569418] Tarnegraafiku vormil loodi topeltrida
-  [KB 4575435] Täiustatud eelvaadet kuvatakse mõnikord ka siis, kui hiirekursor ei asu välja lähedal
-  [KB 4575434] Otsingut ei filtreerita, kui välja on muudetud
-  [KB 4575430] Ruudustikus ei peideta parooliväljade väärtuseid
-  [KB 4569438] Tarnijakannete tasakaalustamisel kuvatakse pärast ridade märkimist teade „Töötlemine peatati kontrollimisprobleemi tõttu”
-  [KB 4569434] Juriidiliste isikute vormi värskendamisel kuvatakse vähem kirjeid
-  [KB 4575297] Ruudustiku redigeerimisel ja vahekaartide avamisel viiakse fookus tegevuse salvestaja paanile
-  [KB 4566773] Paranduskandeid ei näidata kannete päringus negatiivsena 
-  [KB 4575288] Lihtsas loendis ridade vahel oleva äärise valimisel lähtestatakse fookus aktiivsele reale
-  [KB 4575287] Töölehtedes uue rea loomiseks allanoole nuppu kasutades ei viia fookust tagasi esimesele veerule
-  [KB 4564819] Vabas vormis arvel ei saa ridu kustutada (andmeallika ChangeGroupMode=ImplicitInnerOuter tõttu)
-  [KB 4563317] Piltide puhul ei kuvata kohtspikreid / täiustatud eelvaateid

### <a name="fixed-as-part-of-10012"></a>Parandatud versioonis 10.0.12

- [KB 4558545] Tabeli juhtelemendid ei värskenda kuvatud üksuste sisu.
- [KB 4558570] Pärast kirje kustutamist kuvatakse lehel endiselt üksusi.
- [KB 4558572] Loendipaneeliga **ExtendedStyle** seostatud stiili ei rakendata.
- [KB 4558573] Kinnitamise tõrkeid ei saa parandada, kui vajalik muudatus tuleb teha väljaspool ruudustikku.
- [KB 4558584] Negatiivseid numbreid ei renderdata õigesti.
- [KB 4560726] „Ootamatu klienditõrge“ leiab aset pärast loetelude vahel ümberlülitumise lõpetamist, kasutades loetelu vaate juhtelementi.
- [KB 4562141] Ruudustiku indeksid on pärast uue kirje lisamist paigast ära.
- [KB 4562151] Tegevuse salvestaja suvandid **Kinnita** ja **Kopeeri** pole kuupäeva/numbri juhtelementide jaoks saadaval. 
- [KB 4562153] Mitme valikuga märkeruudud ei ole loetelu/kaardi ruudustikes nähtaval.
- [KB 4562646] Vahel pole pärast ruudustikus mitme rea valimist võimalik väljaspool ruudustikku klõpsata.
- [KB 4562647] Fookus lähtestatakse pärast turberollide ruudustikus uue rea lisamist esimesele juhtelemendile dialoogiboksis **Avalda**.
- [KB 4563310] Täiustatud eelvaadet ei suleta pärast rea muutmist.
- [KB 4563313] Kui otsingus valitakse väärtus, siis esineb Internet Exploreris „ootamatu klienditõrge“.
- [KB 4564557] Otsingud ja rippmenüüd ei avane Internet Exploreris
- [KB 4563324] Navigeerimine ei tööta pärast tööruumi **Personalihaldus** avamist.

### <a name="fixed-as-part-of-10011"></a>Parandatud versioonis 10.0.11

- [Probleem 432458] Mõne tütarkogumi alguses kuvatakse tühjasid või dubleeritud ridasid.
- [KB 4549711] Maksesoovituse ridu ei saa pärast uue ruudustiku juhtelemendi lubamist õigesti eemaldada.
- [KB 4558374] Kirjeid, milleks on vaja polümorfse valija dialoogiboksi, ei saa luua.
- [KB 4558375] Uue ruudustiku veergudes ei kuvata spikriteksti.
- [KB 4558376] Loendipaneeli ruudustikke ei renderdata Internet Exploreris õigel kõrgusel.
- [KB 4558377] Liitboksi veerge, mille laius on **SizeToAvailable**, ei renderdata mõnel lehel.
- [KB 4558378] Süvitsimineku funktsioon avab mõnikord vale kirje.
- [KB 4558379] Ilmneb tõrge, kui avatakse otsingud, mille säte **ReplaceOnLookup**=**Ei**.
- [KB 4558380] Ruudustikus olevat vaba ruumi ei täideta kohe pärast lehe osa ahendamist.
- [KB 4558381] Negatiivseid numbreid ei renderdata õigesti / kasutajad ei saa mõnikord pärast kinnitamisprobleemide ilmnemist edasi liikuda.
- [KB 4558382] Ilmnevad ootamatud klienditõrked.
- [KB 4558383] Pärast viimase kirje kustutamist ei värskendata väljaspool ruudustikku olevaid juhtelemente.
- [KB 4558587] Viitegruppides, mille asendusväljadeks on liitboksid, ei kuvata väärtusi.
- [KB 4562143] Välju ei värskendata pärast rea muutmist / ruudustiku töötlemine takerdub pärast rea kustutamist.
- [KB 4562645] Tööriista Regression Suite Automation Tool (RSAT) testide käitamisel esineb otsingu avamisel erand.

### <a name="fixed-as-part-of-10010"></a>Parandatud versioonis 10.0.10

- [Probleem 414301] Uute ridade loomisel kaob osa eelmistest ridadest pärit andmetest.
- [Programmiviga 417044] Loendi tüüpi ruudustike jaoks pole tühja ruudustiku teadet.
- [KB 4539058] Mõnda ruudustikku (tavaliselt kiirkaarte) ei renderdata mõnikord (need renderdatakse, kui suumite välja).
- [KB 4549734] Aktiivseid ridu ei kohelda märgituna, kui märkimisveerg on peidetud.
- [KB 4549796] Väärtusi ei saa ruudustikus redigeerida, kui see on vaaterežiimis.
- [KB 4558367] Teksti valimine on ridade muutmisel ebajärjekindel.
- [KB 4558368] Klaviatuuri kaudu mitme valiku tegemine on ühe valiku tegemisel lubatud.
- [KB 4558369] Olekukujutised kaovad hierarhilises ruudustikus.
- [KB 4558370] Uut rida ei kerita vaatevälja.
- [KB 4558372] Uus ruudustik takerdub töötlemisrežiimis, kui kleebitud sisu veergude arv ületab ruudustiku järelejäänud veergude arvu.
- [KB 4562631] Kellaajaväärtused ei ole õigesti vormindatud.

### <a name="quality-update-for-1009platform-update-33"></a>Versiooni 10.0.9 kvaliteedivärskendus / platvormivärskendus 33

- [KB 4550367] Kellaajaväärtused ei ole õigesti vormindatud.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
