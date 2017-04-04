---
title: "Jaemüügi välisseadmete ülevaade"
description: "Selles teemas selgitatakse välisseadmete jaemüük seotud. Selles kirjeldatakse erinevaid viise, et välisseadmete ühendamiseks müügikoha (POS) ja komponendid, mis on seoses tootjaorganisatsioonide eest vastutab."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 268444
ms.assetid: 2ea93e43-8019-49a0-a7f8-325565ebc52d
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 79a43c35691f16d773b88faad63c4ab79cb93f1f
ms.openlocfilehash: c6fb3922ba2c4b15f1043d0bcbac40ff2da9a469
ms.lasthandoff: 03/31/2017


---

# <a name="retail-peripherals-overview"></a>Jaemüügi välisseadmete ülevaade

Selles teemas selgitatakse välisseadmete jaemüük seotud. Selles kirjeldatakse erinevaid viise, et välisseadmete ühendamiseks müügikoha (POS) ja komponendid, mis on seoses tootjaorganisatsioonide eest vastutab.

<a name="concepts"></a>Mõisted
--------

### <a name="pos-registers"></a>Kassaregistrid

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**registreerib**. Müügikoht (POS) register on ettevõte, mis teil määratleda konkreetsete juhtude kohta tootjaorganisatsioonide omadused. Need omadused on riistvaraprofiili või jaemüügi välisseadmed, mida kasutatakse registri, registri vastendatud laos ja visuaalne kogemus registris sisse logib Kasutaja seadistamine.

### <a name="devices"></a>Seadmed

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**seadmed**. Seade on üksus, mis kajastab kassaregistriga vastendatud seadme füüsilist eksemplari. Kui seade on loodud, on vastendatud POS registrisse. Seadmeüksus jälgib teavet selle kohta, millal kassaregister aktiveeritakse, kasutatava kliendi tüübi kohta ja rakenduse paketi kohta, mis on konkreetse seadme puhul juurutatud. Seadmeid saab vastendada taotluse järgmisi: jaemüügi kaasaegne POS, Retail pilve POS, jaemüügi kaasaegne POS – Windows Phone, jaemüügi kaasaegne POS – Android ja jaemüügi kaasaegne POS – iOS.

### <a name="retail-modern-pos"></a>Uudne jaemüügikassa

Kaasaegne POS on POS programmi Microsoft Windows. Saab kasutada Windows 10 operatsioonisüsteemile (OSs).

### <a name="cloud-pos"></a>Cloud POS

Pilve POS on veebipõhine versioon kaasaegne POS programm, mida saab kasutada veebibrauseris.

### <a name="modern-pos-for-ios"></a>Kaasaegne POS, iOS

Kaasaegne POS iOS on kaasaegne POS programmi, mis loovad iOS seadmete iOS-põhine versioon.

### <a name="modern-pos-for-android"></a>Kaasaegne POS Android

Kaasaegne POS Android on Androidil versioon kaasaegne POS programmi, mida saab kasutada Android seadmeid.

### <a name="pos-peripherals"></a>POS välisseadmed

POS välisseadmed on seadmed, mis on otseselt toetatud POS funktsioone. Nende välisseadmed on tavaliselt jagatud liigi. Nende klassi kohta lisateabe saamiseks vt käesoleva teema jaotises "Seadme klassi".

### <a name="hardware-station"></a>Riistvarajaam

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanalite**&gt;**kauplustes**&gt;**kõik kauplustes**. Valige kauplus ja klõpsake siis kiirkaarti **Riistvarajaamad**. Selle **riistvara station** on kanali tasemel säte, mis võimaldab määratleda juhtumeid, kus juurutatakse jaemüügi perifeerne loogika. Selle kanali tasandil kasutavad riistvara station omaduste määramiseks. Seda kasutatakse ka nimekirja riistvara jaamad, mis on saadaval kaasaegne POS juhu konkreetses laos. Riistvara station on ehitatud kaasaegne POS programmi Windows. Eraldiseisva programmina Microsoft Internet Information Services (IIS) saab ka iseseisvalt kasutada riistvara station. Sel juhul see pääseb võrgu kaudu.

### <a name="hardware-profile"></a>Riistvaraprofiil

Navigeerimine: Klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara profiilid**. Riistvaraprofiili on seadmed, mis on konfigureeritud POS registrisse või riistvara station loetelu. Riistvara profiili saab vastendada otse POS registrisse või riistvara station.

## <a name="devices-classes"></a>Seadmete klassid
POS välisseadmed on tavaliselt jagatud klassidesse. Käesolevas osas kirjeldatakse ning annab ülevaate kaasaegne POS toetab seadmeid.

### <a name="printer"></a>Printer

Printerite hulgas olla traditsiooniline POS saamise ka kogu lehe printerid. Printer toetab objektide linkimist ja manustamist Retail POS (OPOS) ja Microsoft Windows driver liideste kaudu. Kuni kaks printerit saab samal ajal. Seda võimalust toetab stsenaariumi kui cash-and-carry kliendi laekumiste trükitakse kviitung printerid, arvestades klientide tellimused, mis kannavad lisateabe, trükitakse kogu lehe printer. Saamise printerid saab ühendada otse arvutiga USB kaudu, kaudu Ethernet võrku ühendatud või ühendatud Bluetoothi kaudu.

### <a name="scanner"></a>Skanner

Kuni kahe vöötkoodi skannerid kasutamist samal ajal. Seda võimalust toetab stsenaariumide kus skanner, mis on suurem suur või raske kaupade kontrollimiseks fikseeritud embedded skanner on kasutada standardsuuruses üksustele, kiirendada kassasse korda. Skannerid toetab OPOS, Universal platvormil (UWP) või klaviatuuri kiilu liidesed. Skanneri arvutiga saab kasutada USB või Bluetooth.

### <a name="msr"></a>Magnetribalugeja

OPOS juhtide abil saate seadistada ühe USB magnetriba lugeja (MSR). Kui soovite kasutada eraldiseisva DHJSI elektrooniliste vahendite ülekandmine (EFT) maksetehingud, tuleb makse connector liitmise hallata. Omaette MSRs sobib lojaalsus kande töötaja sisselogimine ja kingitus kaardi kande makse connector sõltumatult.

### <a name="cash-drawer"></a>Raha sahtlis

Kaks Kassasahtlid kinnitab riistvaraprofiili kohta. See võime võimaldab kaks aktiivset vahetust kohta registri kättesaadavaks samal ajal. Ühiskasutusega shift või raha sahtlis, mida kasutatakse mitme POS mobiilseadmete samal ajal lubatud ainult üks raha sahtlis on riistvaraprofiili kohta. Kassasahtlid saab ühendada otse arvutiga USB kaudu, võrku ühendatud või laekumine printer RJ12 kaudu ühendatud. Mõnikord Kassasahtlid saab ka ühendada Bluetoothi kaudu.

### <a name="line-display"></a>Rea kuva

Joon kuvab näitamiseks kasutatud toodete, tehingute saldod ja muu kasulik teave kliendile tehingu käigus. Ühe rea Kuva saab ühendada arvuti USB OPOS juhtide abil.

### <a name="signature-capture"></a>Allkirja hõivamine

Allkirja püüdmise seadmed saab ühendada otse arvutiga USB abil OPOS draiverid. Allkirja kogumise konfigureerimisel kliendi küsitakse Logi seadme. Pärast allkiri antakse, selgub kassast vastuvõtmiseks.

### <a name="scale"></a>Sobita

Kaalud saab ühendada USP arvuti abil OPOS draiverid. Kui toode, mis on märgitud kui "Weighed" toode lisatakse kande, tootjaorganisatsioonide loeb kaalu skaala, lisab toote tehingu ja kasutab kogust, et skaala.

### <a name="pin-pad"></a>PIN-klahvistik

Isiklik ID number (PIN) padjad on toetatud OPOS, kuid neid tuleb vähendada makse connector kaudu.

### <a name="secondary-display"></a>Lisaekraani

Täiendava ekraan on konfigureeritud, kasutatakse number 2 Windows Kuva põhiteave. Lisaekraani eesmärk toetada sõltumatut tarkvara müük (ISV) laiendamine, sest karbist, lisaekraani ei ole seadistatav ja näitab piiratud sisu.

### <a name="payment-device"></a>Makseseade

Makse seadme tugi on ellu makse connector. Makse seadmed on võimeline üks või muu seadme klassi ette funktsioonid. Näiteks olevas saab toimida MSR/kaardilugeja, line ekraan, allkirja hõiveseade või PIN pad. Abi maksmise seadmed on rakendada eraldi omaette seadme tugi, mis on ette nähtud muud seadmed, mis sisalduvad riistvaraprofiili.

## <a name="supported-interfaces"></a>Toetatavad liidesed
### <a name="opos"></a>OPOS

Tagamiseks, et suurim valik seadmeid saab kasutada Microsoft Dynamics 365 operatsioonide - jaemüük, POS tööstuse standard OLE on esmane jaemüügi välisseadme platvorm, mis toetab Microsoft Dynamics 365 toiminguteks - jaemüük. OLE POS Standard koostati poolt riigi jaemüügi Föderatsiooni (NRF), mis standardil põhinev protokollide jaemüügi välisseadmete jaoks. OPOS on laialt kasutusel OLE POS standardi rakendamise. See töötati välja 1990ndate keskel ja on korduvalt ajakohastatud ajast. OPOS pakub seadme draiveri arhitektuur, mis võimaldab kerge integratsiooni POS riistvara POS Windowsi-põhiste süsteemidega. OPOS kontrolli käepide side ühilduv riistvara ja tarkvara POS. OPOS kontroll koosneb kahest osast:

-   **Kontrolli objekti** – kontrolli objekti seadme klassi (nt line ekraanid) tagab tarkvara programmi. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) annab standardiseeritud OPOS kontrolli objektid, mis on tuntud kui ühise kontrolli objektid (CCOs). Kui CCOs kasutatakse katse Microsoft Dynamics 365 toiminguteks - Retail POS komponent. Seega katsetamine aitab tagada, et, kui Microsoft Dynamics 365 toiminguteks - jaemüügi toetab seadmeklass OPOS, paljusid seadmetüüpe kaudu saab toetada, tingimusel, et tootja annab objekti, mis on ehitatud OPOS. Ei ole otseselt katsetada iga seadme tüüp.
-   **Objekti** – teenuse objekti annab kontrolli objekti (CCO) ja seade. Tavaliselt on seade objekti pakub seadme tootja. Siiski mõnel juhul peate teenuse objekti alla laadida tootja veebisaidilt. Näiteks uuemate hooldusobjektide võidakse. Tootja veebisaidi aadressi leiate oma riistvara dokumentatsioonist.

[![Objekti ja objekti](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) OLE OPOS rakendamise toetamine POS aitab tagada, et, kui seadme tootjad ja POS kirjastajad rakendada õigesti standard, POS süsteemid ja toetatud seadmed koos töötada, isegi kui nad ei olnud varem testitud koos. **Märkus:** OPOS tugi ei taga kõik seadmed, mis on OPOS juhtide toetus. Operatsioonide - Microsoft Dynamics 365 jaemüügi peab esmalt toetama selle seadme tüüp või klass, OPOS kaudu. Lisaks teenindusjuhtumid ei pruugi alati olla up-to-date uusim versioon on CCOs. Sa peaksid olema teadlikud, et üldjuhul teenindusjuhtumid kvaliteet varieerub.

### <a name="windows"></a>&Aknad...

Tarne trükitavat tootjaorganisatsioonid on optimeeritud OPOS. OPOS on tavaliselt palju kiiremini kui Windows printimisel. Seetõttu on soovitatav kasutada OPOS, eriti jaemüügi keskkondades, kus 40-veeru laekumised on trükitud ja tehing peab olema kiire. Enamiku seadmete, kasutatakse OPOS kontrolli. Siiski mõned OPOS saamise printerid toetavad ka Windowsi draiverid. Windowsi draiveri abil pääsete Viimane fondid ja üks võrguprinteri jaoks mitu registrid. Siiski on puudused kasutama Windows draiverid. Siin on mõned näited need vead:

-   Kui kasutatakse Windowsi draiverid, muudab pilte enne printimist toimumist. Seega printimine sageli aeglasem kui see on OPOS kontrolli printerid.
-   Kaudu ("daisy-aheldatud") printer ühendatud seadmed ei pruugi Windowsi draiverite kasutamisel. Näiteks raha sahtlis võivad avaneda või saatelehe printer võib word ootuspäraselt.
-   OPOS toetab ka ulatuslikumaid jaemüügi Tshekiprinterid, nagu paberi lõikamine või saatelehtede seotud muutujad.

Kui OPOS juhtelemendid on saadaval Windows printerit, mida kasutate, printer peaks ikka õigesti töötada Microsoft Dynamics 365 toiminguteks - jaemüük.

### <a name="universal-windows-platform"></a>Universal Windows Platform

UWP, välisseadmete jaemüük puhul on seotud Windows toega seadmeid. Isehäälestuva seadme ühendamisel Windowsi Operatsioonisüsteemi versioon, mis toetavad neid seadme draiverit ei palutakse seadet kasutatakse ettenähtud viisil. Näiteks kui Windows tuvastab seadme Bluetooth kõlar, OS teab seade pole selle **kõneleja** klassi tüüp. Seetõttu, ja ta kohtleb seda seadet kõneleja. Mingit täiendavat seadistust on vaja. POS meditsiiniseadmete puhul paljud USB-seadmed võivad olla ühendatud ja Windows tunnistab neid Inimliidese seadmed (HID). Aga see ei pruugi määrata funktsioone, mille seade annab, sest seade ei määra klassi või seadme tüüp. Windows 10 seadme klassi vöötkoodi skannerid ja MSRs lisamist. Seega, kui seade teatab Windows 10 seade ühe nende rühmadega, Windows kuulavad süteliha seadmelt sobival ajal. Kaasaegne POS toetab UWP MSRs ja skannerid. Seetõttu, kui on valmis panust mõnda neist seadmetest ja seade, mis kuulub ühte nende klassi on ühendatud, saab seadet kasutada. Näiteks kui Windows 10 arvutiga ühendatud UWP Baar seadustiku skanner ja vöötkoodi sisselogimine on kaasaegne POS, vöötkoodi skanner aktiveerimiseks ekraanil sisselogimine. Mingit täiendavat seadistust on vaja. Klassi punkti teenuse UWP seadmed on lisatud Windows. Nende rühmadega, sealhulgas klassid Kassasahtlid ja Tshekiprinterid. Need uued seadmeklassid kaasaegne POS tugi on ootel.

### <a name="keyboard-wedge"></a>Klaviatuuri kiilu

Kui andmed olid sisestatud klaviatuuril saada klaviatuuri kiilu seadmete andmed arvutisse. Seetõttu tegutsevad tootjaorganisatsioonid väli vaikimisi saavad on skaneeritud või swiped andmeid. Selle tulemusena võib mõnikord vale tüüpi andmeid valesti väljale osasse. Näiteks vöötkoodi võib skaneerida välja, mis on mõeldud krediitkaardi andmete sisestamist. Paljudel juhtudel on loogika POS, mis määrab, kas andmed on skannitud või swiped on vöötkood või kaardi libistage. Seetõttu andmed on õigesti käsitseda. Siiski kui seadmed on OPOS asemel klaviatuuri kiilu seadmed, loodud on rohkem kontrolli, kuidas need seadmed andmeid saab tarbida, sest rohkem on "tuntud" andmed pärinevad seadme kohta. Näiteks vöötkoodi skanner andmed automaatselt tuvastatakse vöötkoodi ja seotud kirje andmebaasis leitakse kergemini ja kiiremini kui üldine string otsingu kasutati näiteks klaviatuuri kiilu seadmed.

### <a name="native-printer"></a>Emakeelena printer

Emakeelena (või "Seade" tüüp nimega riistvaraprofiili) printerid saab konfigureerida valida printer, mis on konfigureeritud arvuti kohta küsimine. Kui printer on selle **seadme** tüüp on konfigureeritud, kui kaasaegne POS kohtab print-käsku, kasutajalt küsitakse loendis Printeri valimine. Selline käitumine erineb käitumist Windows draiverid, sest selle **Windows** printeritüübi riistvaraprofiili ei Näita printerite loend. Selle asemel kohustab, et anda nimega printer on **seadme nimi** välja.

### <a name="windows"></a>&Aknad...

Selle **Windows** seadme tüüp kasutatakse ainult printerid. Kui Windows printerit on konfigureeritud riistvara profiili, tuleb esitada kindla printeri nimi. Kui kaasaegne POS kohtab Prindi üritused on konfigureeritud Windows printeri, kandub sündmuse määratud Windows printeri. Kasutajalt ei printerit valima.

### <a name="network"></a>Võrk

Võrgu adresseeritavad Kassasahtlid, tarne printerid ja makseautomaatides saab üle võrgu, kas otse läbi Interprocess side (IPC) riistvara station, mis on ehitatud kaasaegne POS kohta Windowsi rakendus või IIS riistvara station muu kaasaegne POS kliendile.

## <a name="hardware-station-deployment-options"></a>Riistvara station kasutamise võimalusi
### <a name="ipc-built-in"></a>IPC (sisseehitatud)

Interprocess side (IPC) riistvara station on ehitatud kaasaegne POS kohta Windowsi rakendus. IPC riistvara station kasutamiseks määrata riistvaraprofiili registri, mis kasutab kaasaegne POS kohta Windowsi rakendus. Looge riistvara station, on **pühendatud** liik, kus registrit kasutatakse poe. Kaasaegne POS käivitamisel IPC riistvara station on aktiivne, ja POS välisseadmed, mis Outlook on valmis kasutamiseks. Kui ajutiselt ei nõua kohaliku riistvara mingil põhjusel, et **hallata riistvara jaamad** toiming riistvara station funktsioonid välja lülitada. Kaasaegne POS kasutada ka IPC riistvara station võrgu välisseadmete otse suhelda.

### <a name="iis"></a>IIS-I

Kasutage IIS või autonoomse versiooni riistvara station kahel viisil. Kirjeldaja "IIS" tähendab seda, et POS rakendus loob riistvara station Microsoft Internet Information Services kaudu. POS rakendus ühendab IIS riistvara station kaudu, mis käivitada arvutis, kus seadmed on õigesti. IIS kasutamisel jaemüügi välisseadmed, mis on ühendatud riistvara station kasutamist poolt POS registrisse, mis on IIS riistvara station samas võrgus. Ainult kaasaegne POS for Windows sisaldab sisseehitatud toetus välisseadmete jaemüük, muud kaasaegne POS rakendused kasutama IIS riistvara station suhelda POS välisseadmed, mis on konfigureeritud riistvara profiili. Seega nõuab iga astme IIS riistvara station, arvuti, kus töötab veebiteenus ja rakendus, mis suhtleb seadmed. IIS-i riistvara station nõutakse kõigi mitte - Windows kaasaegne POS taotlustega.

#### <a name="dedicated"></a>Sihtotstarbeline

Kaasaegne POS kasutab riistvara jaamad on **pühendatud** tüüp tuvastada, et kui rakendus kasutab arvutiga otse ühendatud välisseadmed. Siiski on **pühendatud** tüüp sobib ka IIS riistvara jaamad. Traditsioonilised, fikseeritud POS stsenaariumi, mis kasutab pilve POS POS rakenduse selle **pühendatud** riistvara station tüüp kasutatakse IIS riistvara jaamad, mida kasutatakse samas arvutis, kus töötab pilve POS. Jaemüügi välisseadmete reguleerimiseks, parem on spetsiaalne IIS riistvara station jaemüügi perifeerne toetust traditsioonilised, fikseeritud POS stsenaariumid. Spetsiaalne riistvara jaamad toetavad kõik välisseadmed, mis toetab riistvara profiili.

#### <a name="shared"></a>Ühine

Jagatud jaamad on mõeldud kasutamiseks mitme POS seadmed läbi päeval muidugi riistvara. Jagatud riistvara jaamad on optimeeritud toetust vaid Kassasahtlid, tarne printerid ja makseautomaatides. Te ei saa otse eraldi vöötkoodi skannerid, MSRs, joon kuvab, kaalud või muud seadmed. Konflikte tekib, kui mitu POS seadmed püüavad väita nende välisseadmete samal ajal. Siin on, kuidas konfliktide juhitakse toetatud seadmetele:

-   **Rahasahtli** – raha sahtlis on avatud sündmus, mis saadetakse seade. Ainus asi, mis võib tekkida, kui raha sahtlis nimetatakse tekib siis, kui raha sahtlis on avatud. Jagatud riistvara jaamade, raha sahtlis seadma **jagatud** riistvara profiili. See säte takistab tootjaorganisatsioonid kontrollida, kas raha sahtlis on juba avatud, saadab avatud käske.
-   **Laekumine printer** – kui kaks kviitungi printimise käsud saadetakse riistvara station käske samal ajal ära kaduda, olenevalt seadmest. Mõnel seadmel on sisemälu või ühiseks kasutamiseks, et saate selle probleemi. Kui printimise käsk nurjub, kassast saab veateate, saate uuesti printimiskäsku tootjaorganisatsioonid:
-   **Tasu** – kui kassast üritab tehingu tasu, mis on juba kasutusel, pakkumise teade teavitab kassast et terminali kasutab ja küsib teenindaja proovida hiljem uuesti. Tavaliselt, Kassapidajad näevad, et terminali on juba kasutusel Oodake muu tehingu lõpuleviimist enne uuesti välja.

Valideerimine on planeeritud tulevase Väljalaske, tuvastada, kas toetuseta seadmed on loodud riistvara profiili, mis on vastendatud jagatud riistvara station. Kui toetuseta seadised, saab kasutaja vastuvõetud teade, et seadmed ei toeta ühiskasutusega riistvara jaamad. Jagatud riistvara jaamade ning **pakkumise korral valige** määrangu **Jah** registrite tasemel. POS siis kasutajalt soovitud riistvara station pakkumine valitakse tootjaorganisatsioonid tehingust. Riistvara station valimisel alati pakkumise kohta lisatakse riistvara station valik otse POS töövoo mobiilne stsenaariume. Kui lisahüve, terminali rea vaate ei kasutata jagatud stsenaariume. Terminali kasutamisel rea ekraaniks blokeeritava teistele kasutajatele terminali kasutada enne tehingu lõpuleviimist. Mobiilne juhtudel võidakse lisada read tehingu pikema aja jooksul. Seetõttu on **pakkumise korral valige** võimalus on vajalik, et tagada optimaalne seade.

### <a name="network-peripherals"></a>Võrgu välisseadmete

Võrgu nimetus seadmete puhul riistvaraprofiili võimaldab Kassasahtlid, tarne printerid ja makseautomaatides võrguühenduse kaudu ühendatud.

#### <a name="modern-pos-for-windows"></a>Kaasaegne POS, Windows

IP aadressid võrgu välisseadmete jaoks saate määrata kahes kohas. Kui kaasaegne POS personaalarvutite kasutab võrgu välisseadmete ühtsed, määrake nende seadmete IP-aadresside abil on **IP konfiguratsiooni** võimalus ise registri Updatehagi paani. Võrgu seadmeid, mis jagatakse seas POS registrid, riistvara profiili, mis on talle määratud võrguseadmed saab vastendada otse jagatud riistvara station. IP-aadresside määramiseks valige selle riistvara station on **kauplustes** lehekülg ja seejärel selle **IP konfiguratsiooni** failis on **riistvara jaamad** lõik võrguseadmed, mis on seotud selle riistvara station määramiseks. Riistvara jaamad, mis on ainult, ei ole riistvara station, ise juurutada. Sel juhul riistvara station on vajalik ainult selleks, et kontseptuaalselt rühmitada võrgu adresseeritavad seadmed vastavalt oma asukohale kauplusesse.

#### <a name="cloud-pos-modern-pos-for-ios-and-modern-pos-for-android"></a>Kaasaegne POS Android pilve POS ja kaasaegne POS iOS

Loogika, mis ajendab füüsiliselt ühendatud ja võrk adresseeritavad välisseadmete sisaldub riistvara station. Järelikult kõik POS kliendid, välja arvatud kaasaegne POS for Windows, IIS riistvara station tuleb kasutada ja aktiivne, et POS välisseadmed, olenemata sellest, kas nende välisseadmed on füüsiliselt ühendatud riistvara station või suunatud võrgu kaudu suhelda.

## <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine
### <a name="hardware-station-installation"></a>Riistvara station paigaldamine

Lisateavet [hulgi riistvara station konfiguratsiooni ja paigaldus](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Kaasaegne POS for Windows seadistamine ja konfigureerimine

Lisateavet [jaemüügi kaasaegne POS konfiguratsiooni ja paigaldus](retail-modern-pos-device-activation.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS seadme seadistamine ja konfigureerimine

OPOS komponentide kohta lisateabe saamiseks vt "Toetatud liidesed" osa käesolevas dokumendis. Tavaliselt OPOS draivereid pakub seadme tootja. OPOS seadme draiveri installimisel lisab võti Windows Registry ühes järgmistest kohtadest:

-   **32-bitine süsteem:** HKEY\_kohaliku\_MACHINESOFTWAREOLEforRetailServiceOPOS
-   **64-bitine süsteem:** HKEY\_kohaliku\_MACHINESOFTWAREWOW6432NodeOLEforRetailServiceOPOS

Asukohas ServiceOPOS registri konfigureeritud seadmed korraldatakse vastavalt OPOS seadme. Mitme seadme draiverid on salvestatud.

## <a name="supported-scenarios-by-hardware-station-type"></a>Toetatud stsenaariumid riistvara station tüübi järgi
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klienditugi-IPC riistvara station vs IIS riistvara station

Järgmises tabelis on topologies ja juurutamise stsenaariumide, mida toetatakse.

| Klient      | IPC riistvara station | IIS-i riistvara station |
|-------------|----------------------|----------------------|
| Windows rakendus | Jah                  | Jah                  |
| Cloud POS   | Ei                   | Jah                  |
| Android     | Ei                   | Jah                  |
| iOS         | Ei                   | Jah                  |

### <a name="network-peripherals"></a>Võrgu välisseadmete

Võrgu välisseadmete toetab otseselt riistvara station, mis on ehitatud kaasaegne POS kohta Windowsi rakendus. Kõik teised kliendid, peate juurutama IIS riistvara station.

| Klient      | IPC riistvara station | IIS-i riistvara station |
|-------------|----------------------|----------------------|
| Windows rakendus | Jah                  | Jah                  |
| Cloud POS   | Ei                   | Jah                  |
| Android     | Ei                   | Jah                  |
| iOS         | Ei                   | Jah                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Toetatud seadme tüüpi riistvara station tüübi järgi
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Kaasaegne POS for Windows koos IPC (sisseehitatud) riistvara station

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Toetatud seade klassi</th>
<th>Toetatavad liidesed</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiver</li>
<li>Seade</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printeri 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiver</li>
<li>Seade</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rea kuva</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Topeltkuva</td>
<td>Windows draiver</td>
</tr>
<tr class="odd">
<td>Magnetribalugeja</td>
<td><ul>
<li>OPOS</li>
<li>UWP (mingit seadistust on vaja.)</li>
<li>Klaviatuuri kiilu (mingit seadistust on vaja.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Koostaja</td>
<td><ul>
<li>OPOS</li>
<li>Võrgu <strong>Märkus:</strong> ainult ühe sahtli saab seadistada kui <strong>kasutada ühiskasutusega shift</strong> konfigureeritakse sahtlis.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Koostaja 2</td>
<td><ul>
<li>OPOS</li>
<li>Võrgu <strong>Märkus:</strong> ainult ühe sahtli saab seadistada kui <strong>kasutada ühiskasutusega shift</strong> konfigureeritakse sahtlis.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (mingit seadistust on vaja.)</li>
<li>Klaviatuuri kiilu (mingit seadistust on vaja.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (mingit seadistust on vaja.)</li>
<li>Klaviatuuri kiilu (mingit seadistust on vaja.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Sobita</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-klahvistik</td>
<td>OPOS (toetus on ette nähtud makse connector kohandamine.)</td>
</tr>
<tr class="even">
<td>Allkirja hõivamine</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Makseterminal</td>
<td><ul>
<li>Kohandatud seadme tugi</li>
<li>Võrgu (Lisateabe saamiseks vaadake makse connector dokumentatsioonist.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Kaasaegne POS klientidest, mis on pühendatud IIS riistvara station

**Märkus:** kui IIS-i riistvara station "eesmärk," on üks-ühele seos POS kliendi ja riistvara station.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Toetatud seade klassi</th>
<th>Toetatavad liidesed</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows driver <strong>Märkus:</strong> Windows printerid võrgus, riistvara station kasutaja peab olema õigus printeri.</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printeri 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiver</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Rea kuva</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Magnetribalugeja</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Koostaja</td>
<td><ul>
<li>OPOS</li>
<li>Võrgu <strong>Märkus:</strong> kui on võimalik luua ainult üks sahtel riistvara profiili kohta <strong>kasutada ühiskasutusega shift</strong> konfigureeritakse sahtlis.</li>
</ul></td>
</tr>
<tr class="even">
<td>Koostaja 2</td>
<td><ul>
<li>OPOS</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanner</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Skanner 2</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Sobita</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>PIN-klahvistik</td>
<td>OPOS (toetus on ette nähtud makse connector kohandamine.)</td>
</tr>
<tr class="odd">
<td>SIG saadud hõivamine</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Makseterminal</td>
<td><ul>
<li>Kohandatud seadme tugi</li>
<li>Võrgu (Lisateabe saamiseks vaadake makse connector dokumentatsioonist.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Kaasaegne POS klientidest, mis on jagatud IIS riistvara station

**Märkus:** kui IIS-i riistvara station "jagatakse," mitu seadet kasutada riistvara station samal ajal. Selle stsenaariumi puhul saab kasutada ainult seadmeid, mis on loetletud järgmises tabelis. Kui püüate seadmed, mida pole nimetatud siin, nagu vöötkoodi skannerid ja MSRs, tõrked võivad ilmneda kui mitu seadet väidavad sama perifeerse. Tulevikus selline konfiguratsioon on välistatud otseselt.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Toetatud seade klassi</th>
<th>Toetatavad liidesed</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Windows driver <strong>Märkus:</strong> Windows printerid võrgus, riistvara station kasutaja peab olema õigus printeri.</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printeri 2</td>
<td><ul>
<li>OPOS</li>
<li>Windows draiver</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Koostaja</td>
<td><ul>
<li>OPOS</li>
<li>Võrgu <strong>Märkus:</strong> kui on võimalik luua ainult üks sahtel riistvara profiili kohta <strong>kasutada ühiskasutusega shift</strong> konfigureeritakse sahtlis.</li>
</ul></td>
</tr>
<tr class="even">
<td>Koostaja 2</td>
<td><ul>
<li>OPOS</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Makseterminal</td>
<td><ul>
<li>Kohandatud seadme tugi</li>
<li>Võrgu (Lisateabe saamiseks vaadake makse connector dokumentatsioonist.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Toetatud stsenaariumid konfiguratsioon
Riistvaraprofiilide loomise kohta lisateabe saamiseks vt [määramine ja säilitada kanali klientidele ka registrite ja riistvara jaamad](define-maintain-channel-clients-registers-hw-stations.md). **Märkus:** Microsoft Dynamics 365 toiminguid versiooni 1611, station riistvaraprofiili ei kasutata enam. Atribuudid, mis olete varem seadistanud riistvaraprofiili station on nüüd osa riistvara station, ise.

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>Kaasaegne POS for Windows koos IPC (sisseehitatud) riistvara station

See konfiguratsioon on traditsioonilised, fikseeritud POS registrite kõige tüüpilisem konfiguratsiooni. Sellise stsenaariumi vastendatakse riistvara profiili andmeid otse ise registrisse. EFT terminali number seadma ka ise registrisse. Selle konfiguratsiooni seadmiseks toimige järgmiselt.

1.  Kui kõik vajalikud välisseadmed on konfigureeritud riistvara profiili loomiseks.
2.  Kaart riistvara profiili, POS registrile.
3.  Luua riistvara station, on **pühendatud** kauplusesse, kus kasutatakse POS registri jaoks. Kirjeldus pole kohustuslik. **Märkus:** ei ole riistvara station teiste atribuutide seadmiseks. Kogu nõutava teabe, näiteks riistvara profiili, tulevad ise registrist.
4.  Klõpsake **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**.
5.  Valige selle **1090** jaotus poodi uue riistvara profiili sünkroonimise ajakava. Klõpsake **praegu käivitada** sünkroonimise muutmiseni tootjaorganisatsioonid.
6.  Valige selle **1040** jaotus ajakava sünkroonida uue riistvara jaama poodi. Klõpsake **praegu käivitada** sünkroonimise muutmiseni tootjaorganisatsioonid.
7.  Install ja aktiveerimine Windows kaasaegne POS.
8.  Kaasaegne POS for Windows alustada ja hakata kasutama ühendatud välisseadmed.

### <a name="all-modern-pos-clients-that-have-a-dedicated-iis-hardware-station"></a>Kaasaegne POS klientidest, mis on pühendatud IIS riistvara station

Taoline konfiguratsioon sobib kõik kaasaegne POS kliente, mis on riistvara station, mida kasutab ainult üks POS registreerida. Selle konfiguratsiooni seadmiseks toimige järgmiselt.

1.  Kui kõik vajalikud välisseadmed on konfigureeritud riistvara profiili loomiseks.
2.  Luua riistvara station, on **pühendatud** kauplusesse, kus kasutatakse POS registri jaoks.
3.  Spetsiaalne riistvara station, seadke järgmised atribuudid:
    -   **Hosti nimi** – kui riistvara station töötab vastuvõtva arvuti nimi. **Märkus:** pilve POS võib lahendada **localhost** kohalikus arvutis, milles töötab pilve POS määramiseks. Siiski peab olema sertifikaat, mis on vajalik, et siduda pilve POS riistvara station "Localhost" kui arvuti nimi. Probleemide vältimiseks soovitame, et te nimekirja iga spetsiaalne riistvara station poe, vajadusel näiteks. Kõikide riistvara, tuleks hostinimi kindlat arvutinime, kus juurutatakse riistvara station.
    -   **Sadama** – kaasaegne POS kliendi suhtlemiseks kasutada riistvara station port.
    -   **Riistvaraprofiili** – kui riistvaraprofiili pole kui ise riistvara station, riistvara profiili, mis on seotud registri kasutab.
    -   **EFT POS number** – The EFT terminali ID EFT lubade saatmisel kasutada. See ID pakub krediitkaardi töötleja.
    -   **Paketi nimi** – riistvara station paketi kasutada riistvara station juurutamisel.

4.  Klõpsake **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**.
5.  Valige selle **1090** jaotus poodi uue riistvara profiili sünkroonimise ajakava. Klõpsake **praegu käivitada** sünkroonimise muutmiseni tootjaorganisatsioonid.
6.  Valige selle **1040** jaotus ajakava sünkroonida uue riistvara jaama poodi. Klõpsake **praegu käivitada** sünkroonimise muutmiseni tootjaorganisatsioonid.
7.  Installige riistvara station. Riistvara station installimise kohta lisateabe saamiseks vt [hulgi riistvara station konfiguratsiooni ja paigaldus](retail-hardware-station-configuration-installation.md).
8.  Install ja aktiveerimine kaasaegne POS. Kaasaegne POS installimise kohta lisateabe saamiseks vt [jaemüügi kaasaegne POS konfiguratsiooni ja paigaldus](retail-modern-pos-device-activation.md).
9.  Kaasaegne POS Logi ja valige **-sahtel toiminguid**.
10. Alustada ka **hallata riistvara jaamad** operatsiooni.
11. Klõpsake **hallata**.
12. Haldamise lehel riistvara station seada sisse riistvara station.
13. Valige riistvara station ja seejärel klõpsake **paar**.
14. Pärast seda, kui on ühendatud riistvara station, klõpsake **lähedal**.
15. Klõpsake lehel riistvara station valikut hiljuti valitud riistvara station selle aktiveerimiseks.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Kaasaegne POS klientidest, mis on jagatud IIS riistvara station

Taoline konfiguratsioon sobib kõik kaasaegne POS klientides riistvara jaamad ühiskasutusse muude seadmetega. Selle konfiguratsiooni seadmiseks toimige järgmiselt.

1.  Kus vajalikud välisseadmed on konfigureeritud riistvara profiili loomiseks.
2.  Luua riistvara station, on **jagatud** kauplusesse, kus kasutatakse POS registri jaoks.
3.  Jagatud riistvara station, seadke järgmised atribuudid:
    -   **Hosti nimi** – kui riistvara station töötab vastuvõtva arvuti nimi.
    -   **Kirjeldus** – tekst, mis aitab tuvastada riistvara station, näiteks **tagastab** või **poe ees**.
    -   **Sadama** – kaasaegne POS kliendi suhtlemiseks kasutada riistvara station port.
    -   **Riistvaraprofiili** – jagatud riistvara mõõtejaamade peaks iga riistvara station on riistvara profiili. Riistvara profiilid saate jagada riistvara jaamade vahel, kuid nad vastendada iga riistvara station. Lisaks soovitame kasutada jagatud vahetustega, kui mitu seadet kasutada sama ühiskasutusega riistvara station. Ühiskasutusega shift seadistamiseks klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**POS profiilid**&gt;**riistvara profiilid**. Iga jagatud riistvara profiili, valige raha sahtlis ja seadke selle **ühiskasutusega shift sahtlis** võimalus **Jah**.
    -   **EFT POS number** – The EFT terminali ID EFT lubade saatmisel kasutada. See ID pakub krediitkaardi töötleja.
    -   **Paketi nimi** – riistvara station paketi kasutada riistvara station juurutamisel.

4.  Korrake juhiseid 2 ja 3 iga täiendavat riistvara station, mis on vajalik poest.
5.  Klõpsake **hulgi- ja kaubanduse**&gt;**jaemüügi see**&gt;**jaotus ajakava**.
6.  Valige selle **1090** jaotus poodi uue riistvara profiili sünkroonimise ajakava. Klõpsake **praegu käivitada** sünkroonimise muutmiseni tootjaorganisatsioonid.
7.  Valige selle **1040** jaotus ajakava sünkroonida uue riistvara jaama poodi. Klõpsake **praegu käivitada** sünkroonimise muutmiseni tootjaorganisatsioonid.
8.  Installige riistvara station iga vastuvõtva arvuti, mis te luua juhiseid 2 ja 3. Riistvara station installimise kohta lisateabe saamiseks vt [hulgi riistvara station konfiguratsiooni ja paigaldus](retail-hardware-station-configuration-installation.md).
9.  Install ja aktiveerimine kaasaegne POS. Kaasaegne POS installimise kohta lisateabe saamiseks vt [jaemüügi kaasaegne POS konfiguratsiooni ja paigaldus](retail-modern-pos-device-activation.md).
10. Kaasaegne POS Logi ja valige **-sahtel toiminguid**.
11. Alustada ka **hallata riistvara jaamad** operatsiooni.

12. Klõpsake **hallata**.
13. Haldamise lehel riistvara station seada sisse riistvara station.
14. Valige riistvara station ja seejärel klõpsake **paar**.
15. Korrake juhiseid 14 kõikide mis kasutab kaasaegne POS riistvara.
16. Pärast vajaliku riistvara jaamad on ühendatud, klõpsake **lähedal**.
17. Klõpsake lehel riistvara station valikut hiljuti valitud riistvara station selle aktiveerimiseks. **Märkus:** kui seadmed kasutavad tihti erinevaid riistvara jaamad, soovitame konfigureerida kaasaegne POS kiire kassapidajate valida riistvara station, kui nad hakkavad pakkumise protsessi. Klõpsake **hulgi- ja kaubanduse**&gt;**kanali seaded**&gt;**POS seadistus**&gt;**registreerib**. Valige registrisse ja seadke selle **pakkumise korral valige** võimalus **Jah**. Kasutamine ning **1090** jaotus ajakava kanali andmebaasi muudatuste sünkroonimiseks.

## <a name="extensibility"></a>Laiendatavus
Teavet riistvara station laiendusstsenaariumite, leiate [riistvara Station laiendatavus](dev-itpro/hardware-station-extensibility.md).

## <a name="security"></a>Turvalisus
Kohaselt praeguse, järgmisi sätteid võib kasutada tootmise keskkond: **Märkus:** riistvara station installer automaatselt teeb need registri redigeerimist kaudu iseteenindusse installimise käigus.

-   Turvaline soklikiht (SSL) tuleb keelata.
-   Ainult transpordikihi turbe (TLS) 1.2 versiooni (või praeguse kõrgeima versiooni) tuleb lubatud ja kasutada. **Märkus:** vaikimisi SSL ja TLS, välja arvatud TLS 1.2 kõik versioon on keelatud. Redigeerida või need väärtused lubada, toimige järgmiselt.
    1.  Vajutage Windowsi logo klahv + R, et avada on **käivitage** akna.
    2.  Aastal ning **avatud** välja, tippige **Regedit**, ja seejärel klõpsake **OK**.
    3.  Kui on **kasutajakonto kontroll** sõnum ilmub, klõpsake **Jah**.
    4.  Aastal ning **Registry Editor** aknas liikuge **HKEY\_kohaliku\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Järgmised võtmed on automaatselt sisestatud lubada ainult TLS 1.2:
        -   TLS 1.2Server: lubatud = 1
        -   TLS 1.2Server:DisabledByDefault = 0
        -   TLS 1.2Client: lubatud = 1
        -   TLS 1.2Client:DisabledByDefault = 0
        -   TLS 1.1Server: lubatud = 0
        -   TLS 1.1Client: lubatud = 0
        -   TLS 1.0Server: lubatud = 0
        -   TLS 1.0Client: lubatud = 0
        -   SSL 3.0Server: lubatud = 0
        -   SSL 3.0Client: lubatud = 0
        -   SSL 2.0Server: lubatud = 0
        -   SSL 2.0Client: lubatud = 0
-   Ei ole täiendavaid võrguportide peaks olema avatud, kui neid vajatakse teada, määratud põhjustel.
-   Cross-päritolu ressursside jagamise tuleb keelata ja peab olema lubatud päritolu, mis on heaks kiidetud.
-   Omandada sertifikaate, mida kasutatakse arvutites, mis töötavad riistvara station võib kasutada ainult usaldusväärsete sertifitseerimiskeskused.

**Märkus:** on väga oluline vaadata turvalisuse juhised IIS ja makse kaart tööstus (PCI) nõuetele.

## <a name="peripheral-simulator"></a>Välisseadme simulaator
Lisateavet [jaemüügi perifeerne simulaatori](retail-peripheral-simulator.md).

## <a name="microsofttested-peripheral-devices"></a>Microsofttested tarvikud
### <a name="ipc-built-in-hardware-station"></a>IPC (sisseehitatud) riistvara station

Järgmine välisseadmete testiti IPC riistvara station, mis on ehitatud kaasaegne POS for Windows abil.

#### <a name="printer"></a>Printer

| Tootja | Mudel    | Liides | Kommentaarid                |
|--------------|----------|-----------|-------------------------|
| Epson        | TM-T88IV | OPOS      |                         |
| Epson        | TM-T88V  | OPOS      |                         |
| Star         | TSP650II | OPOS      |                         |
| Star         | TSP650II | Kohandatud    | Ühendatud võrgu kaudu   |
| Star         | mPOP     | OPOS      | Ühendatud Bluetoothi kaudu |
| HP           | F7M67AA  | OPOS      | Powered USB             |

#### <a name="bar-code-scanner"></a>Vöötkoodi skanner

| Tootja  | Mudel         | Liides | Kommentaarid |
|---------------|---------------|-----------|----------|
| Motorola      | DS9208        | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| Sümbol        | LS2208        | OPOS      |          |
| Integreeritud HP | E1L07AA       | OPOS      |          |
| Datalogic     | Magellan 8400 | OPOS      |          |

#### <a name="pin-pad"></a>PIN-klahvistik

| Tootja | Mudel  | Liides | Kommentaarid                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Nõuab makse connector kohandamine |

#### <a name="payment-terminal"></a>Makseterminal

| Tootja | Mudel | Liides | Kommentaarid                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Pööripäev      | L5300 | Kohandatud    | Nõuab makse connector kohandamine                                |
| VeriFone     | MX925 | Kohandatud    | Nõuab kohandamine makse connector; võrgu- ja USB kaudu |
| VeriFone     | MX915 | Kohandatud    | Nõuab kohandamine makse connector; võrgu- ja USB kaudu |

#### <a name="cash-drawer"></a>Raha sahtlis

| Tootja | Mudel     | Liides | Kommentaarid                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Ühendatud Bluetoothi kaudu |
| APG          | Atwood    | Kohandatud    | Ühendatud võrgu kaudu   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |

#### <a name="line-display"></a>Rea kuva

| Tootja  | Mudel   | Liides | Kommentaarid |
|---------------|---------|-----------|----------|
| Integreeritud HP | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Allkirja hõivamine

| Tootja | Mudel  | Liides | Kommentaarid |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Sobita

| Tootja | Mudel         | Liides | Kommentaarid |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magnetribalugeja

| Tootja | Mudel       | Liides | Kommentaarid |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="dedicated-iis-hardware-station"></a>Spetsiaalne IIS riistvara station

Järgmine välisseadmete testiti spetsiaalne (mitte ühiskasutuses) IIS riistvara jaama pilve POS ja kaasaegne POS for Windows abil.

#### <a name="printer"></a>Printer

| Tootja | Mudel    | Liides | Kommentaarid                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Kohandatud    | Ühendatud võrgu kaudu     |
| Star         | TSP100   | OPOS      | Nõuab TSP650II draiverid |
| HP           | F7M67AA  | OPOS      | Powered USB               |

#### <a name="bar-code-scanner"></a>Vöötkoodi skanner

| Tootja  | Mudel   | Liides | Kommentaarid |
|---------------|---------|-----------|----------|
| Motorola      | DS9208  | OPOS      |          |
| Sümbol        | LS2208  | OPOS      |          |
| Integreeritud HP | E1L07AA | OPOS      |          |

#### <a name="pin-pad"></a>PIN-klahvistik

| Tootja | Mudel  | Liides | Kommentaarid                                        |
|--------------|--------|-----------|-------------------------------------------------|
| VeriFone     | 1000SE | OPOS      | Nõuab makse connector kohandamine |

#### <a name="payment-terminal"></a>Makseterminal

| Tootja | Mudel | Liides | Kommentaarid                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| Pööripäev      | L5300 | Kohandatud    | Nõuab makse connector kohandamine                                |
| VeriFone     | MX925 | Kohandatud    | Nõuab kohandamine makse connector; võrgu- ja USB kaudu |
| VeriFone     | MX915 | Kohandatud    | Nõuab kohandamine makse connector; võrgu- ja USB kaudu |

#### <a name="cash-drawer"></a>Raha sahtlis

| Tootja | Mudel     | Liides | Kommentaarid              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Kohandatud    | Ühendatud võrgu kaudu |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

#### <a name="line-display"></a>Rea kuva

| Tootja  | Mudel   | Liides | Kommentaarid |
|---------------|---------|-----------|----------|
| Integreeritud HP | G6U79AA | OPOS      |          |
| Epson         | M58DC   | OPOS      |          |

#### <a name="signature-capture"></a>Allkirja hõivamine

| Tootja | Mudel  | Liides | Kommentaarid |
|--------------|--------|-----------|----------|
| Scriptel     | ST1550 | OPOS      |          |

#### <a name="scale"></a>Sobita

| Tootja | Mudel         | Liides | Kommentaarid |
|--------------|---------------|-----------|----------|
| Datalogic    | Magellan 8400 | OPOS      |          |

#### <a name="msr"></a>Magnetribalugeja

| Tootja | Mudel       | Liides | Kommentaarid |
|--------------|-------------|-----------|----------|
| Magtek       | 21073075    | UWP       |          |
| Magtek       | 21073062    | OPOS      |          |
| HP           | IDRA-334133 | OPOS      |          |

### <a name="shared-iis-hardware-station"></a>Jagatud IIS riistvara station

Järgmine välisseadmete testiti jagatud IIS riistvara station pilve POS ja kaasaegne POS for Windows abil. **Märkus:** ainult üks printer, Makseterminali ja rahasahtli on toetatud.

#### <a name="printer"></a>Printer

| Tootja | Mudel    | Liides | Kommentaarid                  |
|--------------|----------|-----------|---------------------------|
| Epson        | TM-T88IV | OPOS      |                           |
| Epson        | TM-T88V  | OPOS      |                           |
| Star         | TSP650II | OPOS      |                           |
| Star         | TSP650II | Kohandatud    | Ühendatud võrgu kaudu     |
| Star         | TSP100   | OPOS      | Nõuab TSP650II draiverid |
| HP           | F7M67AA  | OPOS      | Powered USB               |

#### <a name="payment-terminal"></a>Makseterminal

| Tootja | Mudel | Liides | Kommentaarid                                                                       |
|--------------|-------|-----------|--------------------------------------------------------------------------------|
| VeriFone     | MX925 | Kohandatud    | Nõuab kohandamine makse connector; võrgu- ja USB kaudu |
| VeriFone     | MX915 | Kohandatud    | Nõuab kohandamine makse connector; võrgu- ja USB kaudu |

#### <a name="cash-drawer"></a>Raha sahtlis

| Tootja | Mudel     | Liides | Kommentaarid              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Kohandatud    | Ühendatud võrgu kaudu |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |

## <a name="troubleshooting"></a>Tõrkeotsing
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Kaasaegne POS tuvastab riistvara station selle loendist valida, kuid see ei saa lõpule viia, sidumine

**Lahendus:** järgmist loendit võimalike ebaõnnestumist võrra:

-   Arvuti, kus töötab kaasaegne POS usaldab sertifikaat, mida kasutatakse arvuti, kus töötab riistvara station.
    -   Kontrollida sellise seadistuse veebibrauseris, külastage järgmist URL: https://&lt;arvuti nimi&gt;:&lt;pordinumber&gt;/HardwareStation/ping.
    -   See URL kasutab ping pääseb arvuti ja brauser näitab, kas sert on usaldusväärne. (Nt Internet Exploreris kuvatakse luku aadressiribal. Selle ikooni klõpsamisel Internet Exploreri kontrollib, kas sertifikaat on praegu usaldusväärne. Saate installida sertifikaadi kohalikus arvutis kuvatakse serdi üksikasjad.)
-   Arvuti, kus töötab riistvara station, port, mida kasutab riistvara station on avatud tulemüüri.
-   Riistvara station on õigesti installitud kaubanduskonto teavet Install kaupmees teabevahend, mis töötab riistvara station paigaldaja lõpus läbi.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Kaasaegne POS ei saa tuvastada riistvara station selle loendist valimiseks

**Lahendus:** kas järgmisi tegureid võib põhjustada selles küsimuses:

-   Riistvara station pole seadistatud õigesti peakorteris. Juhiste abil varemloodud Veenduge riistvara station profiili ja riistvara station õigesti sisestanud.
-   Töökohad ei ole käivitatud kanal konfiguratsiooni värskendamiseks. Sel juhul töö 1070 kanali konfigureerimiseks.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Kaasaegne POS ei kajasta uus raha sahtlis seaded

**Lahendus:** sulgeda avatud paketti. Muutused raha sahtlis ei värskendata kaasaegne POS, kuni praeguse partii on suletud.

### <a name="modern-pos-is-reporting-an-issue-with-a-retail-peripheral"></a>Kaasaegne POS on teatanud küsimus perifeerne jaemüük

**Lahendus:** siin on mõned tüüpilised põhjused probleemi:

-   Veenduge, et muud seadme draiveri jälgimisfunktsiooni on suletud. Kommunaalteenused on avatud, nad võivad takistada kaasaegne POS või riistvara station väites seade.
-   Kui jaemüügi perifeerse jagatakse mitme POS seadmetega, veenduge, et see kuulub ühte järgmistest kategooriatest:
    -   Raha sahtlis
    -   Laekumine printer
    -   Makseterminal

    Kui perifeerses ei kuulu kategooriasse, riistvara station ei ole mõeldud selleks, et perifeerse POS mitme seadme vahel.
-   Vahel seadme draiverid võivad põhjustada ühise kontrolli objektid (CCOs) õigesti töötamise. Kui seade on hiljuti installitud, kuid see ei tööta korralikult või märkate muid küsimusi, saate sageli lahendada probleemi uuesti ning CCOs. Selle CCOs allalaadimiseks külastage <http://monroecs.com/oposccos_current.htm>.
-   Kui muudate sageli perifeersete ajal testimiseks või tõrkeotsinguks, peate IIS-i lähtestamise asemel ootab vahemälu värskendada ennast. IIS lähtestamiseks toimige järgmiselt.
    1.  Alates on **käivitage** menüü, tüüp **CMD**.
    2.  Otsingu tulemused, paremklõpsake **käsuviiba**, ja seejärel klõpsake **Käivita administraatorina**.
    3.  Aastal ning **käsuviiba** aken, tüüp **iisreset /Restart** ja vajutage sisestusklahvi Enter.
    4.  Pärast IIS-i taaskäivitumist uuesti kaasaegne POS.
-   Tegemisel vaheldusid välisseadmete, et kui te sageli sisse- ja POS kliendi, dllhost protsess eelmise POS istungil võivad häirida seansi. Sel juhul seade ei pruugi olla kasutatavad,-teegi (DLL) host, mis haldab eelmine kord sulgemiseni. DLL vastuvõtva sulgemiseks toimige järgmiselt.
    1.  Alates on **käivitage** menüü, tüüp **Task manager**.
    2.  Otsingu tulemustes klõpsake **Task manager**.
    3.  Task Manager, linna ning **andmed** vahekaardil, klõpsake veerupäist, mis on märgistatud **nimi** sortida tabeli nime järgi tähestiku järjekorras.
    4.  Kerige, kuni leiate dllhost.exe.
    5.  Valige iga vastuvõtva DLL ja klõpsake **End task**.
    6.  Pärast suletud DLL hosts, taaskäivitage kaasaegne POS.


<a name="see-also"></a>Vt ka
--------

[Jaemüügi perifeerne simulaatori](retail-peripheral-simulator.md)


