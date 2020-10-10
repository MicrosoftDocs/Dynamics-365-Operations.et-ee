---
title: Ruudustiku võimalused
description: Selles teemas kirjeldatakse ruudustiku juhtelemendi mitmeid võimsaid funktsioone. Nende võimaluste kasutamiseks tuleb uus ruudustikufunktsioon lubada.
author: jasongre
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 1f1c27444b38360072beb5277c445161983a2480
ms.sourcegitcommit: 28a771d81322e72d88db63a20ff360de084a6087
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/22/2020
ms.locfileid: "3835082"
---
# <a name="grid-capabilities"></a>Ruudustiku võimalused

[!include [banner](../includes/banner.md)]

Uus ruudustiku juhtelement pakub mitmeid kasulikke ja võimsaid võimalusi, mida saab kasutada kasutaja tootlikkuse suurendamiseks, teie andmetest huvitavate vaadete loomiseks ja sisukate ülevaadete hankimiseks andmete jaoks. Selles artiklis tutvustatakse järgmisi võimalusi. 

-  Summade arvutamine
-  Süsteemist eespool tippimine
-  Matemaatiliste avaldiste hindamine 
-  Tabeli andmete grupeerimine (lubatud eraldi kasutades **(eelvaade) grupeerimist võrkude** funktsioonis)
-  Kinnitatud süsteemiveerud

## <a name="calculating-totals"></a>Summade arvutamine
Rakendustes Finance and Operations on kasutajatel võimalik ruudustiku numbriveergude allosas näha kogusummasid. Need kogusummad kuvatakse ruudustiku allosas jaluse jaotises. 

### <a name="showing-the-grid-footer"></a>Ruudustiku jaluse kuvamine
Finance and Operationsi rakendustes on igas tabeliruudustikus allosas jaluse ala. Jalus näitab olulist teavet, mis on seotud ruudustikus kuvatavate andmetega. Siin on mõned näited sellest teabest.

- Valitud ridade arv tabelis (kui on valitud rohkem kui üks kirje)
- Konfigureeritud arvveergude allosas olevad kogusummad
- Andmekogumi ridade arv 

See jalus on vaikimisi peidetud, kuid seda saab hõlpsasti sisse lülitada. Ruudustiku jaluse kuvamiseks paremklõpsake ruudustiku veeru päist ja valige suvand **Kuva jalus**. Kui jalus on teatud ruudustiku puhul sisse lülitatud, jäetakse see säte meelde, kuni kasutaja otsustab jaluse peita. Seda saab teha, paremklõpsates veeru päises ja valides käsu **Peida jalus**.  Pange tähele, et toimingu **Kuva jalus / peida jalus** paigutust plaanitakse edasistes värskendustes muuta. 

### <a name="specifying-columns-with-totals"></a>Veergude määramine kogusummade abil
Praegu ei konfigureerita kogusummade vaikimisi kuvamiseks ühtegi veergu. Selle asemel loetakse seda ühekordse häälestuse toiminguks, mis on sarnane veergude laiuste kohandamisega ruudustikes. Kui olete määranud, et soovite näha veeru kogusummasid, kuvatakse teile seda sätet järgmisel lehekülastusel.  

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
Kasutajad on alati saanud eksportida andmeid Finance and Operationsi rakendustest rakendusse Excel, kasutades suvandit **Ekspordi Excelisse**. Kuna andmeid saab sisestada enne süsteemi, toetab uus ruudustik tabelite kopeerimist Excelist ja nende kleepimist otse Finance and Operationsi rakenduste ruudustikesse. Ruudustiku lahter, millelt kleepimistoimingut alustati, määrab, kuhu kopeeritud tabel kleebitakse. Ruudustiku sisu kirjutatakse kopeeritud tabeli sisuga üle, välja arvatud kahel järgmisel juhul.

- Kui kopeeritud tabeli veergude arv ületab kleepimise asukohast alates ruudustikku jäävate veergude arvu, teavitatakse kasutajat, et lisaveergusid eirati. 
- Kui kopeeritud tabeli ridade arv ületab kleepimise asukohast alates ruudustiku ridade arvu, kirjutatakse olemasolevad lahtrid kleebitud sisuga üle ja kõik kopeeritud tabeli lisaread lisatakse ruudustiku allossa uute ridadena. 

## <a name="evaluating-math-expressions"></a>Matemaatiliste avaldiste hindamine
Tootlikkuse tõstmiseks saavad kasutajad sisestada ruudustiku numbrilahtritesse matemaatilisi valemeid. Nad ei pea tegema arvutust süsteemivälises rakenduses. Näiteks kui sisestate **=15\*4** ja vajutate siis väljalt välja liikumiseks **tabeldusklahvi**, hindab süsteem avaldist ja salvestab välja jaoks väärtuse **60**.

Selleks et süsteem tuvastaks avaldise väärtuse, käivitage väärtus võrdusmärgiga (**=**). Lisateavet toetatud tehtemärkide ja süntaksi kohta vt teemast [Toetatud matemaatilised sümbolid](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

## <a name="grouping-tabular-data"></a>Tabeli andmete grupeerimine
[!include [preview banner](../includes/preview-banner.md)]

Ärikasutajatel on sageli vaja teha andmete ad-hoc-analüüsi. Üks võimalus selle tegemiseks on eksportida andmeid Microsoft Excelisse ja kasutada liigendtabeleid, kuid **(eelvaade) grupeerimine võrkude** funktsioon, mis sõltub uuest ruudustiku juhtelemendi funktsioonist, võimaldab kasutajatel oma tabeli andmeid põnevatel viisidel Finance and Operationsi rakendustes korraldada. Kuna see funktsioon laiendab funktsiooni **Kogusummad**, võimaldab **Rühmitamine** teil saada ka sisukaid ülevaateid oma andmetest, pakkudes vahesummasid grupi tasandil.

Selle funktsiooni kasutamiseks paremklõpsake veergu, mille alusel soovite rühmitada, ja valige käsk **Rühmita selle veeru järgi**. See tegevus sordib andmed valitud veeru alusel, lisab uue **grupi veeru järgi** ruudustiku algusse ja lisab iga grupi algusesse päise read. Need päise read annavad iga grupi kohta järgmist teavet. 
-  Grupi andmete väärtus 
-  Veeru nimi (see teave on eriti kasulik pärast seda, kui toetatud on rühmitamise mitu taset.)  
-  Selles grupis olevate andmeridade arv
-  Kogusummade kuvamiseks konfigureeritud veergude vahesummad

Kui [Salvestatud vaated](saved-views.md) on lubatud, saab selle rühmitamise isikupärastamisena järgmiseks lehekülastuseks salvestada, et saada kiirjuurdepääs.  

Kui valite käsu **Rühmita selle veeru alusel** mõnes teises veerus, asendatakse algne rühmitamine, kuna versioonis 10.0.9 platvormivärskendusega 33 on toetatud ainult üks rühmitamise tase.

Rühmitamise tagasivõtmiseks ruudustikus paremklõpsake rühmitataval veerul ja valige käsk **Tühista rühmitamine**.  

### <a name="expanding-and-collapsing-groups"></a>Gruppide laiendamine ja ahendamine
Andmete algsel grupeerimisel on kõik grupid laiendatud. Andmete summeeritud vaateid saate luua üksikute rühmade ahendamise abil või kasutada andmete navigeerimisel grupi laiendamist ja ahendamist. Grupi laiendamiseks või ahendamiseks valige vastava grupi päisereal nupp Rööpnool (>). Pange tähele, et üksikute gruppide laiendamis-/ahendamisolek on **pole** salvestatud isikupärastamise võimalustes.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Ridade valimine ja valiku tühistamine grupi tasemel
Samamoodi nagu ruudustiku kõigi ridade valimiseks (või valiku tühistamiseks) saate märkida ruudustiku esimese veeru ülaosas oleva ruudu, saate kiiresti valida (või valiku tühistada) kõik grupi read, kui märgite vastava grupi päiserea ruudu. Grupi päiserea märkeruut kajastab alati selle grupi ridade praegust valikuolekut, olenemata sellest, kas kõik read on valitud, ühtegi rida pole valitud või on valitud ainult mõned read.

### <a name="hiding-column-names"></a>Veeru nimede peitmine
Andmete grupeerimisel kuvatakse veeru nimi grupi päisereal vaikimisi. Alates versioonist 10.0.14/Platvormi värskendusega nr 38 saate veeru nime grupi päiseridades peita, valides **Ruudustiku suvandid** > **Peida grupi veeru nimi**.

## <a name="pinned-system-columns"></a>Kinnitatud süsteemiveerud
Rea valimise veerg ja rea oleku veerg on uues ruudustikus kinnitatud või külmutatud ruudustiku vasakpoolses osas. Kui need veerud on ruudustikku kaasatud, on nad seetõttu alati kasutajale nähtavad hoolimata ruudustiku horisontaalsest kerimisasukohast.   

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Kuidas lubada uut ruudustiku juhtelementi oma keskkonnas? 

**10.0.9 / platvormi värskendus 33 või hilisem**

Funktsioon **Uus ruudustiku juhtelement** on kõikides keskkondades saadaval otse funktsioonihalduses. Sarnaselt teistele avaliku eelvaate funktsioonidele kehtib selle funktsiooni tootmisse lubamisele [täiendav kasutustingimuste leping](https://go.microsoft.com/fwlink/?linkid=2105274).  

**10.0.8 / Platvormi värskendus 32 ning 10.0.7 / platvormi värskendus 31**

Funktsiooni **Uus ruudustiku juhtelement** saab lubada 1. taseme (arendamine/testimine) ja 2. taseme (liivakast) keskkondades, et pakkuda täiendavat testimist ja kujundusmuudatusi, järgides alltoodud juhiseid.

1.  **Luba lend**: Käivitage järgmine SQL-lause: 

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, enabled, FLIGHTSERVICEID, PARTITION) VALUES('CLIReactGridEnableFeature', 1, 0, 5637144576);`

2. **Lähtesta IIS**, et tühjendada staatilise eelväljaande vahemälu. 

3.  **Leia funktsioon**: avage tööruum **Funktsiooni haldus**. Kui funktsiooni **Uus ruudustiku juhtelement** ei kuvata kõigi funktsioonide loendis, tehke valik **Otsi värskendusi**.   

4.  **Luba funktsioon**: leidke funktsioon **Uus ruudustiku juhtelement** funktsioonide loendist ja valige üksikasjade paanilt suvand **Luba nüüd**. Pidage meeles, et brauseri värskendamine on nõutav. 

Kõik järgmised kasutajaseansid algavad lubatud uue ruudustiku juhtelemendiga.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Arendajatele] Üksikutelt lehtedelt ruudustiku eemaldamine 
Kui teie organisatsioon avastab lehekülje, millel on uue ruudustiku kasutamisega probleeme, saate kasutada alates versioonist 10.0.13 / platvormi värskendusest 37 saadaolevat API-t, et lubada üksikul vormil kasutada ruudustiku pärandjuhtelementi ja samas lubada ülejäänud süsteemil kasutada uut ruudustiku juhtelementi. Et eemaldada ruudustik üksikult lehelt, lisage kutse `super()` vormi meetodile `run()`.

 ```this.forceLegacyGrid();```

Seda API-d saab kasutada kuni 2021. aasta oktoobri väljalaskeni, mil uus ruudustiku juhtelement muutub kohustuslikuks. Kui mõne probleemi korral on vaja kasutada seda API-d, teatage sellest Microsoftile.

## <a name="developer-size-to-available-width-columns"></a>[Arendajale] Saadaoleva laiusega veerud
Kui arendaja seab uue ruudustiku veergude puhul atribuudi **WidthMode** väärtuseks **SizeToAvailable**, on neil veergudel esialgu sama laius, mis neil oleks siis, kui atribuudi väärtuseks oleks seatud **SizeToContent**. Sellest hoolimata venitatakse neid, et kasutada ruudustikus saadaolevat lisalaiust. Kui atribuudi väärtuseks on seatud **SizeToAvailable** mitme veeru puhul, jagavad kõik need veerud ruudustikus saadaolevat lisalaiust. Kui kasutaja muudab ühe sellise veeru suurust aga käsitsi, muutub veerg staatiliseks. Selle laius jääb samaks ja seda ei venitata, et kasutada ruudustikus saadaolevat lisalaiust.  

## <a name="known-issues"></a>Teadaolevad probleemid
Selles jaotises on toodud uue ruudustiku juhtelemendi teadaolevate probleemide loend, kuni funktsioon on eelvaate olekus.  

### <a name="open-issues"></a>Lahendamata probleemid
-  Pärast funktsiooni **Uus ruudustiku juhtelement** kasutatakse mõnel lehel jätkuvalt olemasolevat ruudustiku juhtelementi. See juhtub järgmistes olukordades.  
    -  Lehel on kaardiloend, mida renderdatakse mitmes veerus.
    -  Lehel on rühmitatud kaartide loend.
    -  Ruudustiku veerus on mittereageeriv laiendatav juhtelement.

    Kui kasutaja seisab ühega neist olukordadest esimest korda silmitsi, kuvatakse teade lehe värskendamise kohta. Pärast selle teate kuvamist jätkab leht olemasoleva ruudustiku kasutamist kõigi kasutajate puhul kuni järgmise tooteversiooni värskenduseni. Nende stsenaariumide paremat käsitlemist, et uut ruudustikku saaks kasutada, kaalutakse tulevases värskenduses.     

### <a name="fixed-as-part-of-10013"></a>Parandatud versioonis 10.0.13

-  [Programmiviga 470173] Passiivsete ridade märkeruudud täidetakse/tühjendatakse, kui lahtris klõpsatakse tühemikku
-  [Programmiviga 474848] Ruudustikega täiustatud eelvaateid ei kuvata
-  [Programmiviga 474851] Viitegrupi juhtelementides ei tööta hüperlingid 
-  [Programmiviga 471777] Mobiilirakenduse redigeerimiseks või loomiseks ei saa ruudustikus välju valida
-  [KB 4569441] Mitme veeruga kaardiloendite, piltide kohtspikrite ja mõnel väljal kuvamisvalikutega seotud probleemid
-  [KB 4575279] Pearaamatust ei kustutata kõiki märgitud ridasid
-  [KB 4575233] Kuvamisvalikuid ei taastata pärast teisele reale üleminemist
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
- [KB 4562645] Serverite kaughalduse tööriistade (RSAT) testide käitamisel esineb otsingu avamisel erand.

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
