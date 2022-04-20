---
title: Ruudustiku võimalused
description: Selles teemas kirjeldatakse ruudustiku juhtelemendi mitmeid võimsaid funktsioone. Nende võimaluste kasutamiseks peate lubama uue ruudustiku funktsiooni.
author: jasongre
ms.date: 03/21/2022
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
ms.openlocfilehash: 08348185a424d20b6da1563189496b7dd51944d9
ms.sourcegitcommit: edc887e0526c415466e9691e642028ecd97cdbe7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2022
ms.locfileid: "8602958"
---
# <a name="grid-capabilities"></a>Ruudustiku võimalused

[!include [banner](../includes/banner.md)]

Uus ruudustiku juhtelement pakub mitmeid kasulikke ja võimsaid võimalusi, mida saate kasutada kasutaja tootlikkuse suurendamiseks, teie andmetest huvitavate vaadete loomiseks ja sisukate ülevaadete hankimiseks andmete jaoks. Selles artiklis tutvustatakse järgmisi võimalusi. 

- Summade arvutamine
- Süsteemist eespool tippimine
- Matemaatiliste avaldiste hindamine 
- Tabeldusandmete grupeerimine (lubatud eraldi, kasutades grupeerimist **ruudustikes**)
- Veergude külmutamine (lubatud eraldi, kasutades funktsiooni **Külmutamise veerud ruudustikus**)
- Veeru laiuse automaatkorrekteerimine
- Venitatavad veerud

## <a name="calculating-totals"></a>Summade arvutamine
Finantside ja toimingute rakendustes on kasutajatel võimalus näha kogusummasid ruudustike numbriveergude all. Ruudustiku allosas olev jaluse jaotis näitab neid kogusummasid. 

### <a name="showing-the-grid-footer"></a>Ruudustiku jaluse kuvamine
Finantside ja toimingute rakenduste iga vahekaardi allosas on jaluse ala. Jalus näitab olulist teavet, mis on seotud ruudustikus kuvatavate andmetega. Siin on mõned näited sellest teabest.

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

Kui arvutuse lõpuleviimiseks kulub palju aega, saate toimingu tühistada, klõpsates nuppu **Tühista**. Mõnikord on andmekogumi kogusummade arvutamiseks liiga suur (teie organisatsiooni kehtestatud piirang) ja teid teavitatakse hoopis andmete rohkem filtreerimiseks. 

> [!NOTE]
> Süsteemihaldused **saavad** **muuta** kogusummade arvutamiseks saada oleva kirjete arvu limiiti, kohandades kliendi jõudluse suvandite lehel iga ruudustiku parameetri kohalike kirjete maksimaalset arvu. Vaikeväärtus on 25 000 kirjet. Administraatorid peaksid selle väärtuse korrigeerimisel olema ettevaatlik, kuna liiga suur väärtus võib kasutajale saadaoleva mälu vormindada. Soovitus ei tohi ületada 50 000 kirjet.   

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
Kasutajatel on alati olnud võimalik finantside ja toimingute rakenduste ruudustike andmeid eksportida Microsoft Excel, **kasutades Excelisse eksportimise mehhanismi**. Kuid võimalus sisestada andmeid süsteemist ette võimaldab uuel ruudustikul toetada tabelite kopeerimist Excelist ja nende otse finantside ja toimingute rakenduste ruudustikke. Ruudustiku lahter, millelt kleepimistoimingut alustati, määrab, kuhu kopeeritud tabel kleebitakse. Ruudustiku sisu kirjutatakse kopeeritud tabeli sisuga üle, välja arvatud kahel järgmisel juhul.

- Kui kopeeritud tabeli veergude arv ületab kleepimise asukohast alates ruudustikku jäävate veergude arvu, teavitatakse kasutajat, et lisaveergusid eirati. 
- Kui kopeeritud tabeli ridade arv ületab kleepimise asukohast alates ruudustiku ridade arvu, kirjutatakse olemasolevad lahtrid kleebitud sisuga üle ja kõik kopeeritud tabeli lisaread lisatakse ruudustiku allossa uute ridadena. 

## <a name="evaluating-math-expressions"></a>Matemaatiliste avaldiste hindamine
Tootlikkuse tõstmiseks saavad kasutajad sisestada ruudustiku numbrilahtritesse matemaatilisi valemeid. Nad ei pea tegema arvutust süsteemivälises rakenduses. Näiteks kui sisestate **=15\*4** ja vajutate siis väljalt välja liikumiseks **tabeldusklahvi**, hindab süsteem avaldist ja salvestab välja jaoks väärtuse **60**.

Selleks et süsteem tuvastaks avaldise väärtuse, käivitage väärtus võrdusmärgiga (**=**). Lisateavet toetatud tehtemärkide ja süntaksi kohta vt teemast [Toetatud matemaatilised sümbolid](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Tabeli andmete grupeerimine
Ärikasutajatel on sageli vaja teha andmete ad-hoc-analüüsi. Ehkki seda Microsoft Excel saab teha andmete eksportimisel liigendtabelisse ja kasutades seda, **võimaldab grupeerimine ruudustikes funktsioon, mis sõltub uuest ruudustiku juhtelemendi funktsioonist, võimaldab kasutajatel organiseerida oma tabelandmeid huvitavatel viisidel Finantside ja toimingute rakendustes**. Kuna see funktsioon laiendab funktsiooni **Kogusummad**, võimaldab **Rühmitamine** teil saada ka sisukaid ülevaateid oma andmetest, pakkudes vahesummasid grupi tasandil.

Selle funktsiooni kasutamiseks paremklõpsake veergu, mille alusel soovite rühmitada, ja valige käsk **Rühmita selle veeru järgi**. See tegevus sordib andmed valitud veeru alusel, lisab uue veeru **Rühmitamisalus** ruudustiku algusse ja lisab iga grupi algusesse päise read. Need päise read annavad iga grupi kohta järgmist teavet.

- Grupi andmete väärtus 
- Veeru nimi (see teave on eriti kasulik, kui teil on rühmitamise mitu taset.)
- Selles grupis olevate andmeridade arv
- Kogusummade kuvamiseks konfigureeritud veergude vahesummad

Kui [Salvestatud vaated](saved-views.md) on lubatud, saab selle rühmitamise isikupärastamisena järgmiseks lehekülastuseks salvestada, et saada kiirjuurdepääs.

### <a name="multiple-levels-of-grouping"></a>Rühmitamise mitu taset
Kui olete andmed ühe veeru kaupa rühmitanud, saate andmed rühmitada erineva veeru alusel, valides soovitud veerus suvandi **Rühmita selle veeru järgi**. Seda protsessi saab korrata seni, kuni teil on 5 pesastatud rühmitamise taset, mis on maksimaalne toetatud sügavus. Praegusel hetkel ei saa te enam täiendavate veergude alusel rühmitada.

Saate igal ajal teisaldada rühmitamise mis tahes veerule paremklõpsates seda veergu ja valides suvandi **Tühista rühmitamine**. Saate rühmitamise kõikidelt veergudelt eemaldada, kui valite suvandi **Ruudustiku suvandid** ja seejärel **Tühista kõikide rühmitamine**.

### <a name="sorting-grouped-data"></a>Grupeeritud andmete sortimine
Pärast andmete grupeerimist ühe või mitme veeru järgi saate vastava veerupäise kaudu muuta mis tahes grupeerimisveeru sortimissuunda. 

Käitumine grupeerimata veergude sortimisel sõltub teie tooteversioonist:

- Versioonis 10.0.24 ja varasemas versioonis, kui sordite mitte grupeeritud veeru järgi, eemaldatakse grupeerimine kõikidelt veergudelt ja andmed sorditakse valitud veeru alusel. 
- Kui sordite versioonis 10.0.25 ja hiljem grupeerimata veeru järgi, jääb grupeerimine alles ja andmed sorditakse igas grupis valitud veeru alusel.

### <a name="expanding-and-collapsing-groups"></a>Gruppide laiendamine ja ahendamine
Andmete algsel grupeerimisel on kõik grupid laiendatud. Andmete summeeritud vaateid saate luua üksikute rühmade ahendamise abil või kasutada andmete navigeerimisel grupi laiendamist ja ahendamist. Grupi laiendamiseks või ahendamiseks valige vastava grupi päisereal nupp Rööpnool (>). Pange tähele, et üksikute gruppide laiendamis-/ahendamisolek on **pole** salvestatud isikupärastamise võimalustes.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Ridade valimine ja valiku tühistamine grupi tasemel
Samamoodi nagu ruudustiku kõigi ridade valimiseks (või valiku tühistamiseks) saate märkida ruudustiku esimese veeru ülaosas oleva ruudu, saate kiiresti valida (või valiku tühistada) kõik grupi read, kui märgite vastava grupi päiserea ruudu. Grupi päiserea märkeruut kajastab alati selle grupi ridade praegust valikuolekut, olenemata sellest, kas kõik read on valitud, ühtegi rida pole valitud või on valitud ainult mõned read.

### <a name="hiding-column-names"></a>Veeru nimede peitmine
Andmete grupeerimisel kuvatakse veeru nimi grupi päisereal vaikimisi. Te saate veeru nime grupi päiseridades peita, valides **Ruudustiku suvandid** > **Peida grupi veeru nimi**.

### <a name="grouping-on-date-and-time-columns"></a>Grupeerimine kuupäeva ja kellaaja veergudel
Versiooni 10.0.24 puhul on väljade Date või DateTime suvand lisatud grupeerimiseks aasta, kuu või päeva järgi. Vastava päiserea grupp "väärtus" vastab selle välja vormingule. Lisaks saate väljade DateTime ja Time puhul grupeerida tunni, minuti või teise järgi. 

## <a name="freezing-columns"></a>Veergude külmutamine
Mõned ruudustiku veerud võivad olla piisavalt olulised konteksti jaoks, et te ei soovi neid vaatest välja kerida. Selle asemel võite soovida, et väärtused nendes veergudes oleks alati nähtavad. Ruudustiku **külmutamise veergude funktsioon** pakub kasutajatele paindlikkust. 

Veeru külmutamiseks paremklõpsake veeru päist ja valige seejärel suvand **Külmuta veerg**. Selle sammu esmakordsel lõpuleviimisel muutub valitud veerg esimeseks veeruks ja ei keri enam vaatest välja. Kõik järgmised külmutatud veerud lisatakse viimasest külmutatud veerust paremale. Saate külmutatud veergude järjestuse vastavalt vajadusele muutmiseks kasutada tavalist liigutamise funktsiooni. Samas ei saa külmutatud veerge liigutada nii, et need ilmuksid külmutamata veergude hulgas. Sarnaselt ei saa külmutamata veerge liigutada nii, et need ilmuksid külmutatud veergude hulgas.

Veeru külmutamisest vabastamiseks paremklõpsake külmutatud veeru päist ja valige seejärel suvand **Vabasta veerg külmutamisest**. 

Pange tähele, et uue ruudustiku rea valiku ja rea oleku veerud on esimeses kahes veerus alati külmutatud. Kui need veerud on ruudustikku kaasatud, on nad seetõttu alati kasutajatele nähtavad hoolimata ruudustiku horisontaalsest kerimisasukohast. Nende kahe veeru järjestust ei saa muuta.

## <a name="autofit-column-width"></a>Veeru laiuse automaatkorrekteerimine
Sarnaselt Excel`iga saavad kasutajad automaatselt veeru suurust muuta, võttes aluseks selles veerus praegu kuvatud sisu. Selleks topeltklõpsake veeru suuruse muutmise pidemeid või asetage fookus veeru päisesse ja vajutage nuppu **A** (automaatseks korrektsiooniks). See võimalus on saadaval alates versioonist 10.0.23.

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kuidas lubada uut ruudustiku juhtelementi oma keskkonnas? 

Funktsioon **Uus ruudustiku juhtelement** on kõikides keskkondades saadaval otse funktsioonihalduses. Pärast funktsioonihalduse funktsiooni lubamist kasutavad kõik järgnevad kasutajaseansid uut ruudustiku juhtelementi. 

See funktsioon lubatakse vaikimisi versioonis 10.0.21 ja selle eesmärk on muutuda kohustuslikuks oktoober 2022.  

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Arendajatele] Üksikutelt lehtedelt ruudustiku eemaldamine 
Kui teie organisatsioon avastab lehekülje, millel on uue ruudustiku kasutamisega probleeme, saate kasutada API-t, et lubada üksikul vormil kasutada ruudustiku pärandjuhtelementi ja samas lubada ülejäänud süsteemil kasutada uut ruudustiku juhtelementi. Et eemaldada ruudustik üksikult lehelt, lisage kutse `super()` vormi meetodile `run()`.

```this.forceLegacyGrid();```

See API tasutakse seni, kuni uus ruudustiku juhtelement muutub kohustuslikuks. See muudatus on praegu mõeldud oktoober 2022. Kui mõne probleemi korral on vaja kasutada seda API-d, teatage sellest Microsoftile.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Lehe sundimine kasutama uut ruudustikku pärast ruudustikust varem loobumist
Kui olete uue ruudustiku kasutamisest loobunud, võite soovida hiljem uue ruudustiku uuesti lubada pärast põhiprobleemide lahendamist. Selleks peate lihtsalt eemaldama kutse üksusesse `forceLegacyGrid()`. Muudatus ei jõustub enne, kui toimub üks järgmisest:

- **Keskkonna ümberpaigutamine**: kui keskkonda värskendatakse ja juurutatakse uuesti, siis tühjendatakse automaatselt tabel, mis talletab lehed, mis on uuest ruudustikust (FormControlReactGridState) automaatselt loobunud.
- **Tabeli käsitsi tühjendamine**: juurutamisstsenaariumide jaoks, kui teil tuleb kasutada SQL-i FormControlReactGridState tabeli tühjendamiseks ja seejärel taaskäivitada AOS. See tegevuste kombinatsioon lähtestab uuest ruudustikust keeldunud lehekülgede vahemälustuse.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Arendaja] Üksikute ruudustike tippimine süsteemivõimalustest ees
Mõned stsenaariumid on tekkinud, mis ei laena *end* ruudustiku süsteemivõimalustest ette tippimiseks. (Näiteks mõni kood, mis käivitatakse, kui rida kinnitatakse, käivitab andmeallika uuringute käivitamise ja uurimine võib seejärel rikkuda olemasolevate ridade kinnitamata redigeerimisi.) Kui teie organisatsioon avastab sellise stsenaariumi, on saadaval API, mis võimaldab arendajal asünkroonsest rea kinnitamisest individuaalse ruudustiku valida ja pärandkäitumise taastada.

Kui asünkroonne rea kinnitamine on ruudustikus keelatud, ei saa kasutajad uut rida luua ega teisaldada ruudustikus muule olemasolevale reale, kui praeguses reas on kinnitamisprobleeme. Selle tegevuse kõrval ei saa tabeleid Excelist finantside ja toimingute ruudustike alla kleepida.

Üksiku ruudustiku asünkroonsest rea kinnitamisest loobumiseks lisage vormi meetodile `super()` järgmine `run()` kutse.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Seda kutset tuleks kutsuda ainult erandlikel juhtudel ja see ei tohiks olla kõigi ruudustike norm.
> - Me ei soovita seda API-d pärast vormi koormamist käitusajal sisse lülitada.

## <a name="developer-size-to-available-width-columns"></a>[Arendajale] Saadaoleva laiusega veerud
Kui arendaja seab uue ruudustiku veergude puhul atribuudi **WidthMode** väärtuseks **SizeToAvailable**, on neil veergudel esialgu sama laius, mis neil oleks siis, kui atribuudi väärtuseks oleks seatud **SizeToContent**. Sellest hoolimata venitatakse neid, et kasutada ruudustikus saadaolevat lisalaiust. Kui atribuudi väärtuseks on seatud **SizeToAvailable** mitme veeru puhul, jagavad kõik need veerud ruudustikus saadaolevat lisalaiust. Kui kasutaja muudab ühe sellise veeru suurust aga käsitsi, muutub veerg staatiliseks. Selle laius jääb samaks ja seda ei venitata, et kasutada ruudustikus saadaolevat lisalaiust.

## <a name="known-issues"></a>Teadaolevad probleemid
See jaotis sisaldab uue ruudustiku juhtelemendi teadaolevate probleemide loendit.

### <a name="open-issues"></a>Lahendamata probleemid
- Pärast funktsiooni **Uus ruudustiku juhtelement** kasutatakse mõnel lehel jätkuvalt olemasolevat ruudustiku juhtelementi. See juhtub järgmistes olukordades.
 
    - Lehel on kaardiloend, mida renderdatakse mitmes veerus.
    - Lehel on rühmitatud kaartide loend.
    - Ruudustiku veerus on mittereageeriv laiendatav juhtelement.

    Kui kasutaja seisab ühega neist olukordadest esimest korda silmitsi, kuvatakse teade lehe värskendamise kohta. Pärast selle teate kuvamist jätkab leht olemasoleva ruudustiku kasutamist kõigi kasutajate puhul kuni järgmise tooteversiooni värskenduseni. Nende stsenaariumide paremat käsitlemist, et uut ruudustikku saaks kasutada, kaalutakse tulevases värskenduses.

- [KB 4582758] Kirjed on udused, kui muudate suumi 100 pealt mis tahes teisele protsendile
- [KB 4592012] Ootamatu kliendi tõrge IE11-s mitme rea kleepimisel Excelist

    Microsoft ei oma probleemile parandust


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
