---
title: Välisseadmed
description: See artikkel selgitab Commerce Peripheralsiga seotud mõisteid.
author: BrianShook
ms.date: 09/08/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: josaw
ms.custom:
- "268444"
- intro-internal
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: b3113626b18ad7f074c808d7631d13b09071bef2
ms.sourcegitcommit: f88273627ba105ede27f28fe67ccec2d7f78261c
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459988"
---
# <a name="peripherals"></a>Välisseadmed

[!include[banner](includes/banner.md)]

See artikkel selgitab kaupluse välisseadmetega seotud mõisteid. See kirjeldab mitmesuguseid viise, kuidas välisseadmed saab kassaga ühendada, ja kassaga ühenduse haldamise eest vastutavaid komponente.

## <a name="concepts"></a>Mõisted

### <a name="pos-registers"></a>Kassaregistrid

Navigeerimine: minge jaemüügi ja **ärikanali häälestamise \> kassa häälestusregistritele \>\>**. Kassaregister on üksus, mida kasutatakse kassa konkreetse eksemplari omaduste määratlemiseks. Nende omaduste hulka kuuluvad registris kasutatav riistvaraprofiil või välisseadmed, registriga vastendatud kauplus ja sellesse registrisse sisse logiva kasutaja visuaalne kogemus.

### <a name="devices"></a>Seadmed

Navigeerimine: minge jaemüügi ja ärikanali häälestamise kassa häälestusseadmetesse **\>\>.\>** Seade on üksus, mis kajastab kassaregistriga vastendatud seadme füüsilist eksemplari. Seadme loomisel vastendatakse see kassaregistriga. Seadmeüksus jälgib teavet selle kohta, millal kassaregister aktiveeritakse, kasutatava kliendi tüübi kohta ja rakenduse paketi kohta, mis on konkreetse seadme puhul juurutatud. 

Seadmeid saab vastendada järgmiste rakendusetüüpidega: Retail Modern POS Retail Cloud POS, Retail Modern POS – Android ja Retail Modern POS – iOS.

### <a name="modern-pos"></a>Modern POS

Modern POS on Microsoft Windowsi kassaprogramm. Seda saab juurutada operatsioonisüsteemides Windows 10 ja Windows 11.

### <a name="cloud-pos"></a>Pilve kassa

Cloud POS on programmi Modern POS brauseripõhine versioon, millele pääseb juurde veebibrauserist.

### <a name="modern-pos-for-ios"></a>Modern POS iOS-ile

Modern POS iOS-ile on programmi Modern POS iOS-i põhine versioon, mida saab juurutada iOS-i seadmetel.

### <a name="modern-pos-for-android"></a>Modern POS Androidile

Modern POS Androidile on Modern POS-i programmi Androidi-põhine versioon, mida saab juurutada Androidi seadmetes.

### <a name="pos-peripherals"></a>Kassa välisseadmed

Kassa välisseadmed on seadmed, millel selgelt kassafunktsioone toetatakse. Need välisseadmed on tavaliselt jagatud konkreetsetesse klassidesse. Lisateavet nende klasside kohta vt selle artikli jaotisest "Seadme klassid".

### <a name="hardware-station"></a>Riistvarajaam

Navigeerimine: minge jaemüügi ja **äri kanalite kauplustesse \>\> Kõik \> kauplused**. Valige kauplus ja seejärel valige kiirkaart **Riistvara kiirkaart**. Säte **Riistvarajaam** on kanali tasandi säte, mida kasutatakse eksemplaride määratlemiseks, kui kasutatakse välisseadme loogikat. Seda sätet kasutatakse kanali tasandil riistvarajaama omaduste määramiseks. Samuti kasutatakse seda antud kaupluses Modern POS-i puhul saadaolevate riistvarajaamade loetlemiseks. Riistvarajaam on integreeritud Modern POS-i programmidesse Windowsile ja Androidile. Riistvarajaama saab juurutada ka iseseisvalt autonoomse teenuse Microsoft Internet Information Services (IIS) programmina. Sellisel juhul pääseb selleni võrgu kaudu.

### <a name="hardware-profile"></a>Riistvaraprofiil

Navigeerimine: minge jaemüügi ja ärikanali häälestamise **kassa häälestuse \>\> kassaprofiilide \> riistvaraprofiilidele \>.** Riistvaraprofiil on kassaregistri või riistvarajaama jaoks konfigureeritud seadmete loend. Riistvaraprofiili saab vastendada otse kassaregistri või riistvarajaamaga.

## <a name="devices-classes"></a>Seadmete klassid
Kassa välisseadmed on tavaliselt jagatud klassidesse. Selles jaotises kirjeldatakse seadmeid, mida Modern POS toetab, ja antakse neist ülevaade.

### <a name="printer"></a>Printer

Printerite hulka kuuluvad tavapärased kassa kviitungiprinterid ja kogu lehe printerid. Printereid toetab Retail POS-i (OPOS) Microsoft Windows ja draiveriliideste objekti linkimine ja manustamine. Korraga saab kasutada kuni kahte printerit. See võimalus toetab stsenaariume, kus sularahaklientide kviitungid prinditakse kviitungiprinteritest, samas kui klientide teaberohkemad arved prinditakse kogu lehe printeritest. Kviitungiprinterid saab ühendada USB kaudu otse arvutiga, Etherneti kaudu võrguga või Bluetoothi kaudu.

### <a name="scanner"></a>Skanner

Korraga saab kasutada kuni kahte vöötkoodiskannerit. See võimalus toetab stsenaariume, kus on vaja mobiilsemat skannerit, et skannida suuri või raskeid kaupu, samas kui enamiku tavasuuruses kaupade jaoks kasutatakse fikseeritud manustatud skannerit, et väljaregistreerimist kiirendada. Skannereid võidakse toetada OPOS-i, universaalse Windowsi platvormi (UWP) või klaviatuuri kiilliideste kaudu. Skanneri ühendamiseks arvutiga võib kasutada USB-d või Bluetoothi.

### <a name="msr"></a>Magnetribalugeja

OPOS-i draiverite abil saab seadistada ühe USB-magnetribalugeja (MSR). Kui soovite kasutada maksmiskannete jaoks elektroonilise ülekande (EFT) kaudu autonoomset MSR-i, peab MSR-i haldama makseliides. Autonoomseid MSR-e saab kasutada püsikliendi sisestamise, töötaja sisselogimise ja kinkekaardi sisestamise jaoks, makseliidesest sõltumatult.

### <a name="cash-drawer"></a>Sularahasahtel

Toetada on võimalik kahte sularahasahtlit riistvaraprofiili kohta. Nii on võimalik kasutada korraga kahte aktiivset vahetust registri kohta. Jagatud vahetuse või sularahasahtli korral, mida kasutab korraga mitu mobiilset kassaseadet, lubatakse riistvaraprofiili kohta ainult ühte sularahasahtlit. Sularahasahtlid saab ühendada USB kaudu otse arvutiga, võrguga või liidese RJ12 kaudu kviitungiprinteriga. Mõnel juhul saab sularahasahtlid ühendada ka Bluetoothi kaudu.

### <a name="line-display"></a>Rea kuva

Ridade kuvareid kasutatakse toodete, kandesaldode ja muu kasuliku teabe kuvamiseks kliendile kande ajal. Ühe ridade kuvari saab USB kaudu arvutiga ühendada, kasutades OPOS-i draivereid.

### <a name="signature-capture"></a>Allkirja hõivamine

Allkirja hõivamise seadmed saab USB kaudu otse arvutiga ühendada, kasutades OPOS-i draivereid. Kui allkirja hõive on konfigureeritud, kuvatakse kasutajale viip seadmesse logimiseks. Pärast allkirja edastamist näidatakse seda kassapidajale kinnitamiseks.

### <a name="scale"></a>Mõõtkava

Kaalud saab ARVUTIga ÜHENDADA USB kaudu, kasutades OPOS-i draivereid. Kui kandele lisatakse toode, mis on märgitud „kaalutavaks” tooteks, loeb kassa kaalult kaalu, lisab toote kandesse ja kasutab kaalu antud kogust.

### <a name="pin-pad"></a>PIN-klahvistik

OPOS toetab PIN-koodi (PIN) klahvistikke, kuid neid tuleb hallata makseliidese kaudu.

### <a name="secondary-display"></a>Sekundaarne kuvar

Kui on konfigureeritud sekundaarne kuvar, kasutatakse põhiteabe kuvamiseks Windowsi kuvarit nr 2. Vaikimisi ei ole teisene kuva konfigureeritav ja kuvatakse piiratud sisu. Teisese kuva eesmärk on toetada sõltumatu tarkvara hankija (ISV) laiendust. 

### <a name="payment-device"></a>Makseseade

Makseseadme tugi juurutatakse makseliidese kaudu. Makseseadmed võivad täita ühte või paljusid funktsioone, mida pakuvad teised seadmeklassid. Näiteks võib makseseade toimida MSR-i/kaardilugejana, ridade kuvarina, allkirja jäädvustamise seadmena või PIN-klahvistikuna. Makseseadmete tugi juurutatakse sõltumatult autonoomse seadme toest, mida pakutakse teistele riistvaraprofiilis sisalduvatele seadmetele.

## <a name="supported-interfaces"></a>Toetatud liidesed
### <a name="opos"></a>OPOS

Selleks, et Commerce’iga saaks kasutada suurimat seadmevalikut, on valdkonna standard objektilinkimine ja -manustamine müügikohas peamine toetatud välisseadmete platvorm. Standardi Objektilinkimine ja -manustamine müügikohas looja on organisatsioon National Retail Federation (NRF), mis kehtestab välisseadmetele standardsed sideprotokollid. OPOS on standardi Objektilinkimine ja -manustamine müügikohas laialdaselt kasutatav juurutus. See töötati välja 1990. aastate keskel ja seda on sestsaadik mitu korda uuendatud. OPOS pakub seadmedraiveri arhitektuuri, mis võimaldab kassa riistvara hõlpsat integreerimist Windowsi-põhiste kassasüsteemidega. OPOS-i juhtelemendid tegelevad ühilduva riistvara ja kassatarkvara vahelise sidega. OPOS-i juhtelement koosneb kahest osast.

-   **Juhtimisobjekt** – seadmeklassi (nt ridade kuvarite) juhtimisobjekt pakub tarkvaraprogrammi liidest. Monroe Consulting Services ([www.monroecs.com](http://www.monroecs.com/)) pakub standardset OPOS-i juhtimisobjektide kogumit, mida tuntakse kui üldisi juhtimisobjekte (CCO-sid). CCO-sid kasutatakse Commerce’i kassakomponendi testimiseks. Seega aitab testimine tagada, et kui Commerce toetab OPOS-i kaudu seadmeklassi, siis saab toetada paljusid seadmetüüpe eeldusel, et tootja pakub OPOS-i jaoks loodud hooldusobjekti. Iga seadmetüüpi pole vaja otseselt testida.
-   **Hooldusobjekt** – hooldusobjekt tagab juhtimisobjekti (CCO) ja seadme vahelise side. Tavaliselt annab seadme hooldusobjekti seadme tootja. Kuid mõnel juhul võib teil olla vaja hooldusobjekt tootja veebisaidilt alla laadida. Näiteks võib olla saadaval uuem hooldusobjekt. Tootja veebisaidi aadressi leiate oma riistvara dokumentidest.

[![Kontrolli objekti ja teenuse objekti.](./media/retail_peripherals_overview01.png)](./media/retail_peripherals_overview01.png) Juhtimisobjekt ja hooldusobjekt kassa OLE OPOS-i juurutuse tugi aitab tagada, et kui seadme tootjad ja kassa avaldajad juurutavad standardi õigesti, siis töötavad kassasüsteemid ja toetatud seadmed koos, isegi, kui neid eelnevalt koos ei testitud. 

> [!NOTE]
> OPOS-i tugi ei garanteeri kõigi OPOS-i draiveritega seadmete tuge. Commerce peab seda seadmetüüpi või klassi esmalt OPOS-i kaudu toetama. Lisaks ei pruugi hooldusobjektid CCO-de viimase versiooni suhtes alati ajakohased olla. Peaksite arvestama ka seda, et üldjuhul on hooldusobjektide kvaliteet erinev.

### <a name="windows"></a>Windows

Kassas kviitungite printimine on OPOS-i jaoks optimeeritud. OPOS on tavaliselt palju kiirem kui Windowsi kaudu printimine. Seega tasub OPOS-i kasutada, eelkõige keskkondades, kus prinditakse 40 veerust koosnevaid kviitungeid ja kande aeg peab olema lühike. Enamiku seadmete puhul saate kasutada OPOS-juhtelemente. Kuid mõned OPOS-i kviitungiprinterid toetavad ka Windowsi draivereid. Windowsi draiverit kasutades pääsete juurde uusimatele fontidele ja esimese võrgu printerile mitme registri puhul. Kuid Windowsi draiverite kasutamisel on miinuseid. Siin on mõned näited neist miinustest.

-   Windowsi draiverite kasutamisel esitatakse pildid enne printimist. Seega kipub printimine olema aeglasem kui OPOS-i juhtelementidega printeritel.
-   Printeri kaudu ühendatud (pärgühendusega) seadmed ei pruugi Windowsi draiverite kasutamisel õigesti töötada. Näiteks ei pruugi sularahasahtel avatud olla või ei pruugi kviitungiprinter nii, nagu te eeldate.
-   OPOS toetab alati ulatuslikumat kviitungiprinterite põhiste muutujate kogumit, nt paberi lõikamist või kviitungi printimist.
-   Windowsi printereid ei toetata IIS-i riistvarajaama kaudu. 

Kui OPOS-i juhtelemendid on kasutatava Windowsi printeri puhul saadaval, peaks printer ikkagi Commerce’iga õigesti töötama.

### <a name="plug-and-play-devices"></a>Ühenda ja esita seadmeid

Kui pistik ja seade on ühendatud Seda tüüpi seadet toetava Windowsi operatsioonisüsteemi versiooniga, pole vaja draivereid nii, nagu ette nähtud. Kui Windows näiteks tuvastab ekraanikõlariseadme, siis operatsioonisüsteem teab, et seadme klassitüüp onKõlar, ja käsitleb seda seadetkõlarina. Täiendavat seadistamist pole vaja. 

Kassaseadmete puhul võib Windows OS-i mäluseadmeid (HID-d) sisse ja tuvastada mitu USB-seadet. Kuid windows ei pruugi saada määratleda võimalusi, mis seadmel on, sest seade ei määra seadme klassi või tüüpi. Windows 10-s on lisatud vöötkoodiskannerite ja MSR-ide seadmeklassid. Seetõttu, kui seade kinnitab Windows 10-le, et ta on mõne sellise klassi seade, kuulab Windows sobivatel aegadel seadme sündmusi.

Modern POS toetab UWP MSR-e ja skannereid. Seega, kui Modern POS on valmis ühe neist seadmetest sisestamiseks ja seade, mis kuulub ühte seadme klassi on ühendatud, saab kasutada seda seadet. Näiteks kui pistik ja vöötkoodiskanner on ühendatud Windows 10 arvutiga ja vöötkoodi sisselogimine on Konfigureeritud Modern POS-i jaoks, muutub vöötkoodiskanner sisselogimislehel aktiivseks. Täiendavat seadistamist pole vaja.

Windowsile lisatakse kassaseadmete lisaklasse, nt sularahasahtlite ja kviitungiprinterite klassid. Nende uute seadmeklasside tugi Modern POS-is on ootel.

> [!NOTE] 
> Teatud USB-seadmed võivad muutuda mitterespondiivseks või ebausaldusväärseks, kui seda haldab Windows 10 võimsushalduse funktsioon nimega [USB Selective Suspend](/windows-hardware/drivers/usbcon/usb-selective-suspend). Kui USB-välisseade ei reageeri, võib olla vajalik keelata selle seadme valikuline peatamine. Lisateavet vt Valikulise peatamise [lubamine](/windows-hardware/drivers/usbcon/usb-selective-suspend#enabling-selective-suspend). 

### <a name="keyboard-wedge"></a>Klaviatuurikiil

Klaviatuurikiilu seadmed saadavad andmeid arvutisse, justkui need andmed oleksid klaviatuuri kaudu sisestatud. Seega võtab skannitud või kaarditõmbega sisestatud andmed vaikimisi vastu väli, mis on kassas aktiivne. Mõnikord põhjustab see vale tüüpi andmete skannimise valele väljale. Näiteks võidakse vöötkood skannida väljale, mis on mõeldud krediitkaardi andmete sisestamiseks. Paljudel juhtudel on kassas loogika, mis määrab, kas skannitud või läbi kantud andmed on vöötkood või kaardi tõmmake. Seega käsitsetakse andmeid õigesti. Kuid kui seadmed on seadistatud OPOS-ina klaviatuuri wedge seadmete asemel, on kontrollitav, kuidas nende seadmete andmeid saab tarbida, sest on teada rohkem "tuntud" seadme kohta, kust andmed pärinevad. Näiteks vöötkoodiskannerist pärinevad andmed tuvastatakse automaatselt vöötkoodina ning seotud kirje andmebaasis leitakse hõlpsamini ja kiiremini kui üldise stringiotsingu kasutamisel (nagu klaviatuurikiilu seadmete puhul).

> [!NOTE]
> Kui müügikohas kasutatakse klaviatuuri kiiluskannereid, peavad need olema programmeeritud saatma veotagastuse või **Enteri** sündmuse pärast viimast skannitud märki. Kui see konfiguratsioon pole tehtud, ei tööta klaviatuuri kiiluskannerid korralikult. Lisateavet tagasisõidusündmuse lisamise kohta leiate seadme tootja dokumentatsioonist.  

### <a name="device-printers"></a>Seadme printerid

Printerit, mille tüüp on Seade, saab konfigureerida nii, et kasutajalt küsitakse arvuti jaoks konfigureeritud printerit. Kui tüübi "Seade" printer on konfigureeritud, kui Modern POS-i kohtab prindikäsku, palutakse kasutajal valida loendis printer. See käitumine erineb Windowsi draiverite käitumisest, kuna Windowsi printeritüüp, mida riistvaraprofiil ei näita kasutajale printerite loendit. Selle asemel nõuab see, et väljal **Seadme nimi** oleks antud nimega printer.

### <a name="network"></a>Võrk

Võrguaadressiga sularahasahtleid, kviitungiprintereid ja makseterminale saab kasutada üle võrgu kas otse rakendusse Modern POS Windowsile integreeritud protsessisisese side (IPC) riistvarajaama kaudu või IIS-i riistvarajaama kaudu teiste Modern POS-i klientide jaoks.

## <a name="hardware-station-deployment-options"></a>Riistvarajaama juurutusvõimalused

### <a name="dedicated"></a>Sihtotstarbeline

Modern POS-i kliendid Windowsi ja Androidi jaoks hõlmavad **sihtotstarbelisi** või sisseehitatud riistvarajaamu. Need kliendid saavad suhelda välisseadmetega otse, kasutades äriloogikat, mis on rakendustesse sisse ehitatud. Androidi rakendus toetab ainult võrguseadmeid. Lisateabe saamiseks Androidi välisseadmete toe kohta külastage artiklit [Rakenduse POS Hybrid seadistamine Androidis ja iOS-is](./dev-itpro/hybridapp.md).

Selleks, et kasutada sihtotstarbelist riistvarajaama, järgige neid samme.

1. Määrake riistvaraprofiil registrile, mis kasutab Windowsi või rakenduse Modern POS-i Android.
1. Looge riistvarajaam tüübiga Sihtotstarbeline poe jaoks, kus kassaaparaati kasutatakse. 
1. Avage Modern POS kassavälises režiimis ja **kasutage riistvarajaama** võimaluste sisse lülitamiseks riistvara väliste seadmete haldamise toimingut. Sihtotstarbeline riistvarajaam on vaikimisi aktiivne. 
1. Logige Modern POS-st välja. Seejärel logige tagasi sisse ja avage vahetus. Riistvaraprofiilis konfigureeritud välisseadmeid saab nüüd kasutada. 

### <a name="shared"></a>Ühine

Vahel nimetatakse ka "IIS" riistvarajaamaks, "IIS", mis viitab sellele, et kassarakendus ühendub riistvarajaamaga Microsoft Internet Information Servicesi kaudu. Kassarakendus loob IIS-i riistvarajaamaga ühenduse veebiteenuste kaudu, mis töötavad arvutis, millega seadmed on ühendatud. Ühise riistvarajaama kasutamisel saab riistvarajaamaga ühendatud välisseadmeid kasutada iga kassaregister, mis on IIS-i riistvarajaamaga samas võrgus. Kuna ainult Modern POS Windowsile ja Androidile sisaldavad integreeritud välisseadmete tuge, peavad kõik Modern POS-i rakendused kasutama riistvaraprofiilis konfigureeritud kassa välisseadmetega suhtlemiseks IIS-i riistvarajaama. Seega nõuab iga IIS-i riistvarajaama eksemplar arvutit, millel töötab veebiteenus ja seadmetega suhtlev rakendus. 

Ühiskasutatava riistvarajaama abil saab lubada mitmele müügikliendile välisseadmeid jagada või hallata ühe müügipunkti kooskõlastatud seadmete kogumeid. 

Kui riistvarajaama kasutatakse mitme kassa kliendi vahel välisseadmete jagamise toetamiseks, tuleks kasutada ainult sularahasahtleid, kviitungiprintereid ja makseterminale. Võimalik on ühendada otse autonoomsed vöötkoodiskannerid, MSR-id, ridade kuvarid, kaalud või muud seadmed. Muidu tekivad konfliktid, kui mitu kassaseadet püüab korraga neid välisseadmeid kätte saada. Toetatud seadmete konfliktide haldamine toimub siin:

-   **Sularahasahtel** – sularahasahtel avatakse seadmesse saadetava sündmuse kaudu. Probleemid võivad ilmneda, kui sularahasahtlit kutsutakse ajal, kui sahtel on juba avatud. Ühises riistvarajaama konfiguratsioonis kasutatav sularahasahtel tuleks riistvaraprofiilis **seada** väärtusele Ühiskasutuses. Selle sätte korral ei kontrolli kassa avamiskäsu saatmisel, kas sularahasahtel on juba lahti.
-   **Kviitungiprinter** – kui korraga saadetakse riistvarajaama kaks kviitungi printimise käsku, võib seadmest olenevalt üks käsk kaotsi minna. Mõne seadme sisemälu või ühendamine võib seda probleemi vältida. Kui printimiskäsk ei õnnestu, saab kassapidaja tõrketeate ja võib printimiskäsku kassas uuesti proovida.
-   **Makseterminal** – kui kassapidaja püüab teha kannet makseterminalis, mis on juba kasutusel, kuvatakse talle teade, et terminal on kasutusel, ja palutakse tal hiljem uuesti proovida. Tavaliselt näevad kassapidajad, et terminal on juba kasutusel, ja ootavad enne uut katset, kuni teine tehing on lõpetatud.

Tulevases väljaandes on plaanis kontrollimine, mis tuvastab, kas ühiskasutuses riistvarajaamaga vastendatud riistvaraprofiilile on seadistatud toetuseta seadmeid. Kui tuvastatakse toetuseta seadmeid, saab kasutaja teate, mis ütleb, et neid seadmeid ei toetata ühiskasutuses riistvaraprofiilide puhul. Ühiskasutuses riistvarajaamade puhul on valiku **Valige maksmisel** väärtuseks määratud registri tasandil **Jah**. Kassa kasutajal palutakse seejärel valida riistvarajaam, kui kassas on kande jaoks maksevahend valitud. Kui riistvarajaam valitakse alles maksmise ajal, lisatakse riistvarajaam mobiilsete stsenaariumide puhul otse kassa töövoogu. Lisaeelisena ei kasutata ühiskasutuse stsenaariumide puhul makseterminali ridade kuvarit. Kui makseterminali kasutatakse ridade kuvarina, võidakse teistel kasutajatel blokeerida selle terminali kasutamine kande lõpetamiseni. Mobiilsete stsenaariumide puhul võidakse kandele pika aja jooksul ridu lisada. Seega on vajalik valik **Valige maksmisel**, et tagada optimaalne seadme kättesaadavus.

### <a name="network-peripherals"></a>Võrgu välisseadmed

Riistvaraprofiili seadmete võrgutähistus võimaldab ühendada sularahasahtlid, kviitungiprinterid ja makseterminalid võrguühenduse kaudu.

#### <a name="modern-pos-for-windows"></a>Modern POS Windowsile

Võrgu välisseadmetele saab määrata IP-aadresse kahest kohast. Kui Modern POS-i Windowsi klient kasutab ühte võrgu välisseadmete kogumit, tuleb neile seadmetele määrata IP-aadressid valikuga **IP konfigureerimine** registri enda toimingupaanil. Võrguseadmete puhul, mis on kassaregistrite seas ühiskasutuses, saab riistvaraprofiili, millele on määratud võrguseadmeid, vastendada otse ühiskasutuses riistvarajaamaga. IP-aadresside määramiseks valige lehelt **Kauplused** riistvarajaam ja kasutage siis valikut **IP konfigureerimine** jaotises **Riistvarajaamad** sellele riistvarajaamale määratud võrguseadmete määramiseks. Ainult võrguseadmetega riistvarajaamade puhul pole vaja riistvarajaama ennast juurutada. Sellisel juhul on riistvarajaam vajalik ainult võrguaadressiga seadmete põhimõtteliseks grupeerimiseks nende asukoha järgi poes.

#### <a name="cloud-pos-and-modern-pos-for-ios"></a>Pilvekassa ja tänapäevane kassa iOS-ile

Füüsiliselt ühendatud ja võrguaadressiga välisseadmete juhtimise loogika sisaldub riistvarajaamas. Seetõttu peab kõigi kassa klientide puhul, v.a Modern POS Windowsile ja Androidile, olema juurutatud ja aktiivne IIS-i riistvarajaam, et kassa saaks välisseadmetega suhelda, olenemata sellest, kas need välisseadmed on füüsiliselt riistvarajaamaga ühendatud või võrgu kaudu adresseeritud.

## <a name="setup-and-configuration"></a>Seadistamine ja konfigureerimine
### <a name="hardware-station-installation"></a>Riistvarajaama paigaldamine

JUHENDIT SELLE kohta, kuidas IIS-i riistvarajaama installida, vt [konfigureerige ja installige riistvarajaama](retail-hardware-station-configuration-installation.md).

### <a name="modern-pos-for-windows-setup-and-configuration"></a>Rakenduse Modern POS Windowsile seadistamine ja konfigureerimine

Teavet vt [Modern POS-i (MPOS) konfigureerimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md).

### <a name="modern-pos-for-android-and-ios-setup-and-configuration"></a>Modern POS Androidile ja iOS-ile seadistamine ja konfigureerimine

Teavet vt [Rakenduse POS Hybrid seadistamine Androidis ja iOS-is](./dev-itpro/hybridapp.md).

### <a name="opos-device-setup-and-configuration"></a>OPOS-i seadme seadistamine ja konfigureerimine

Lisateavet OPOS-i komponentide kohta leiate selle dokumendi jaotisest „Toetatud liidesed”. Tavaliselt annab OPOS-i draiverid seadme tootja. Kui OPOS-i seadme draiver on installitud, lisab see Windowsi registrisse ühte järgmisse asukohta võtme.

-   **32-bitine süsteem:** HKEY\_ LOCAL\_ MACHINE\SOFTWARE\KIRJEEforRetail\ServiceOPOS
-   **64-bitine süsteem:** HKEY\_ LOCAL\_ MACHINE\SOFTWARE\OTSTARBEL6432Node\KIRJEEforRetail\ServiceOPOS

Registri asukoha ServiceOPOS puhul korraldatakse konfigureeritud seadmed OPOS-i seadmeklassi järgi. Salvestatakse mitu seadmedraiverit.

## <a name="supported-scenarios-by-hardware-station-type"></a>Toetatud stsenaariumid riistvarajaama tüübi järgi
### <a name="client-support--ipc-hardware-station-vs-iis-hardware-station"></a>Klienditugi – IPC riistvarajaam võrreldes IIS-i riistvarajaamaga

Järgmises tabelis on näidatud toetatud topoloogiaid ja juurutusstsenaariume.

| Klient      | IPC riistvarajaam | IIS-i riistvarajaam |
|-------------|----------------------|----------------------|
| Windowsi rakendus | Jah                  | Jah                  |
| Pilve kassa   | Ei                   | Jah                  |
| Android     | Jah                  | Jah                  |
| iOS         | Ei                   | Jah                  |

### <a name="network-peripherals"></a>Võrgu välisseadmed

Võrgu välisseadmeid saab toetada otse Windowsi ja Androidi rakenduste Modern POS-i integreeritud riistvarajaama kaudu. Kõigi teiste klientide puhul tuleb juurutada IIS-i riistvarajaam.

| Klient      | IPC riistvarajaam | IIS-i riistvarajaam |
|-------------|----------------------|----------------------|
| Windowsi rakendus | Jah                  | Jah                  |
| Pilve kassa   | Ei                   | Jah                  |
| Android     | Jah                  | Jah                  |
| iOS         | Ei                   | Jah                  |

## <a name="supported-device-types-by-hardware-station-type"></a>Toetatud seadmetüübid riistvarajaama tüübi järgi
### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>IPC (integreeritud) riistvarajaamaga Modern POS Windowsile

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Toetatud seadmeklass</th>
<th>Toetatud liidesed</th>
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
<td>Printer 2</td>
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
<li>UWP (Seadistus pole vajalik.)</li>
<li>Klaviatuurikiil (Seadistus pole vajalik.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Koostaja</td>
<td><ul>
<li>OPOS</li>
<li>Võrk </br><strong>Märkus.</strong> Seadistada saab ainult ühe sahtli, kui sahtlil on konfigureeritud valik <strong>Kasuta ühist vahetust</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Koostaja 2</td>
<td><ul>
<li>OPOS</li>
<li>Võrk </br><strong>Märkus.</strong> Seadistada saab ainult ühe sahtli, kui sahtlil on konfigureeritud valik <strong>Kasuta ühist vahetust</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Skanner</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Seadistus pole vajalik.)</li>
<li>Klaviatuurikiil (Seadistus pole vajalik.)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skanner 2</td>
<td><ul>
<li>OPOS</li>
<li>UWP (Seadistus pole vajalik.)</li>
<li>Klaviatuurikiil (Seadistus pole vajalik.)</li>
</ul></td>
</tr>
<tr class="even">
<td>Sobita</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>PIN-klahvistik</td>
<td>OPOS (Tuge pakutakse makseliidese kohandamise kaudu.)</td>
</tr>
<tr class="even">
<td>Allkirja hõivamine</td>
<td>OPOS</td>
</tr>
<tr class="odd">
<td>Makseterminal</td>
<td><ul>
<li>Kohandatud seadme tugi</li>
<li>Võrk (Lisateavet leiate makseliidese dokumentidest.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Kõik Modern POS-i kliendid, millel on kooskõlastatud ühine IIS-i riistvarajaam

> [!NOTE]
> Kui IIS-i riistvarajaam on kooskõlastatud, on kassa kliendi ja riistvarajaama vahel üks-ühele suhe.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Toetatud seadmeklass</th>
<th>Toetatud liidesed</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
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
<li>Võrk </br><strong>Märkus.</strong> Seadistada saab ainult ühe sahtli riistvaraprofiili kohta, kui sahtlil on konfigureeritud valik <strong>Kasuta ühist vahetust</strong>.</li>
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
<td>OPOS (Tuge pakutakse makseliidese kohandamise kaudu.)</td>
</tr>
<tr class="odd">
<td>Sig. hõivamine</td>
<td>OPOS</td>
</tr>
<tr class="even">
<td>Makseterminal</td>
<td><ul>
<li>Kohandatud seadme tugi</li>
<li>Võrk (Lisateavet leiate makseliidese dokumentidest.)</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="all-modern-pos-clients-that-share-an-iis-hardware-station"></a>Kõik Modern POS-i kliendid, kes jagavad IIS-i riistvarajaama

> [!NOTE]
> Kui IIS-i riistvarajaam on ühine, saab seda kasutada korraga mitu seadet. Selle stsenaariumi puhul tuleks kasutada ainult järgmises tabelis loetletud seadmeid. Kui püüate anda ühiskasutusse seadmeid, mida siin kirjas ei ole (nt vöötkoodiskannereid ja MSR-e), tekivad tõrked, kui sama välisseadet püüab kasutada mitu seadet. Tulevikus on selline konfiguratsioon selgelt välistatud.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Toetatud seadmeklass</th>
<th>Toetatud liidesed</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Printer</td>
<td><ul>
<li>OPOS</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="even">
<td>Printer 2</td>
<td><ul>
<li>OPOS</li>
<li>Võrk</li>
</ul></td>
</tr>
<tr class="odd">
<td>Koostaja</td>
<td><ul>
<li>OPOS</li>
<li>Võrk </br><strong>Märkus.</strong> Seadistada saab ainult ühe sahtli riistvaraprofiili kohta, kui sahtlil on konfigureeritud valik <strong>Kasuta ühist vahetust</strong>.</li>
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
<li>Võrk (Lisateavet leiate makseliidese dokumentidest.)</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="configuration-for-supported-scenarios"></a>Toetatud stsenaariumide konfigureerimine
Lisateavet riistvaraprofiilide loomise kohta leiate teemast [Välisseadmete ühendamine kassaga (POS)](define-maintain-channel-clients-registers-hw-stations.md). 

### <a name="modern-pos-for-windows-with-an-ipc-built-in-hardware-station"></a>IPC (integreeritud) riistvarajaamaga Modern POS Windowsile

See konfiguratsioon on tavapäraste fikseeritud kassaregistrite puhul kõige levinum. Selle stsenaariumi puhul on riistvaraprofiili teave vastendatud otse registri endaga. EFT terminali number tuleb samuti registril enesel määrata. Selle konfiguratsiooni seadistamiseks tehke järgmist.

1.  Looge riistvaraprofiil, kus on konfigureeritud kõik vajalikud välisseadmed.
2.  Vastendage riistvaraprofiil kassaregistriga.
3.  Looge poele, kus kassa registrit kasutatakse, riistvarajaam tüübiga **Sihtotstarbeline**. Kirjeldus on vabatahtlik. 

    > [!NOTE]
    > Te ei pea riistvarajaamale ühtegi muud atribuuti määrama. Kogu muu vajalik teave (nt riistvaraprofiil) tuleb registrist endast.

4.  Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
5.  Valige jaotusgraafik **1090** uue riistvaraprofiili sünkroonimiseks kauplusega. Valige **käsk Käivita kohe**, et kassa muudatused sünkroonida.
6.  Valige jaotusgraafik **1040** uue riistvarajaama sünkroonimiseks kauplusega. Valige **käsk Käivita kohe**, et kassa muudatused sünkroonida.
7.  Installige ja aktiveerige Modern POS Windowsile.
8.  Käivitage Modern POS Windowsile ja alustage ühendatud välisseadmete kasutamist.

### <a name="modern-pos-for-android-with-an-ipc-built-in-hardware-station"></a>IPC (integreeritud) riistvarajaamaga Modern POS Androidile

**Uus 10.0.8** – Epsoni võrguprinterid ja DK-pordi kaudu nende printeritega ühendatud sularahasahtlid on nüüd Modern POS-i rakenduse jaoks Android toetatud. Üksikasjade jaoks külastage teemat [Rakenduse POS Hybrid seadistamine Androidis ja iOS-is](./dev-itpro/hybridapp.md).

### <a name="all-modern-pos-clients-that-have-a-committed-shared-iis-hardware-station"></a>Kõik Modern POS-i kliendid, millel on kooskõlastatud ühine IIS-i riistvarajaam

Seda konfiguratsiooni saab kasutada kõigi Modern POS-i klientide puhul, millel on riistvarajaam, mida kasutab ainult üks kassaregister. Selle konfiguratsiooni seadistamiseks tehke järgmist.

1.  Looge riistvaraprofiil, kus on konfigureeritud kõik vajalikud välisseadmed.
2.  Looge poele, kus kassa registrit kasutatakse, riistvarajaam tüübiga **Sihtotstarbeline**.
3.  Määrake sihtotstarbelisel riistvarajaamal järgmised atribuudid.
    -   **Hosti nimi** – hostarvuti nimi, kus riistvarajaam töötab. 
    
        > [!NOTE]
        > Pilvekassa saab lahendada hosti **localhost**, et määrata kohalik arvuti, kus pilvekassa töötab. Kuid serdil, mis on vajalik pilvekassa sidumiseks riistvarajaamaga, peab samuti olema arvuti nimi „Localhost”. Probleemide vältimiseks soovitame loetleda kaupluse jaoks iga vajaliku sihtotstarbelise riistvarajaama eksemplari. Iga riistvarajaama puhul peab hosti nimi olema selle konkreetse arvuti nimi, kus riistvarajaam juurutatakse.
    
    -   **Port** – port, mida riistvarajaam kasutab Modern POS-i kliendiga suhtlemiseks.
    -   **Riistvaraprofiil** – kui riistvaraprofiili pole riistvarajaamal enesel antud, kasutatakse registrile määratud riistvaraprofiili.
    -   **EFT kassa number** – EFT terminali ID, mida EFT volituste saatmisel kasutada. Selle ID annab krediitkaardiprotsessor.
    -   **Paketi nimi** – riistvarajaama pakett, mida riistvarajaama juurutamisel kasutada.

4.  Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
5.  Valige jaotusgraafik **1090** uue riistvaraprofiili sünkroonimiseks kauplusega. Valige **käsk Käivita kohe**, et kassa muudatused sünkroonida.
6.  Valige jaotusgraafik **1040** uue riistvarajaama sünkroonimiseks kauplusega. Valige **käsk Käivita kohe**, et kassa muudatused sünkroonida.
7.  Riistvarajaama paigaldamine. Lisateavet riistvarajaama paigaldamise kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md).
8.  Installige ja aktiveerige Modern POS. Lisateavet Modern POS-i installimise kohta vt teemast [Modern POS-i (MPOS) konfigureerimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md).
9.  Logige Modern POS-i sisse ja valige **Kassaväliste toimingute tegemine**.
10. Käivitage toiming **Riistvarajaamade haldamine**.
11. Valige **suvand Haldamine**.
12. Määrake riistvarajaama haldamise lehel riistvarajaama sisselülitamise valik.
13. Valige kasutamiseks riistvarajaam ja seejärel **paar**.
14. Kui riistvarajaam on ühendatud, valige **sule**.
15. Riistvarajaama valikulehel valige viimati valitud riistvarajaam, et see aktiivseks muuta.

### <a name="all-modern-pos-clients-that-have-a-shared-iis-hardware-station"></a>Kõik Modern POS-i kliendid, millel on ühine IIS-i riistvarajaam

Seda konfiguratsiooni saab kasutada kõigi Modern POS-i klientide puhul, mis kasutavad riistvarajaamu teiste seadmetega ühiselt. Selle konfiguratsiooni seadistamiseks tehke järgmist.

1.  Looge riistvaraprofiil, kus on konfigureeritud vajalikud välisseadmed.
2.  Looge poele, kus kassa registrit kasutatakse, riistvarajaam tüübiga **Ühiskasutuses**.
3.  Määrake ühisel riistvarajaamal järgmised atribuudid.
    -   **Hosti nimi** – hostarvuti nimi, kus riistvarajaam töötab.
    -   **Kirjeldus** – tekst, mis aitab riistvarajaama tuvastada, nt **Tagastused** või **Kaupluse ees**.
    -   **Port** – port, mida riistvarajaam kasutab Modern POS-i kliendiga suhtlemiseks.
    -   **Riistvaraprofiil** – ühiskasutuses riistvarajaamade puhul peab igal riistvarajaamal olema riistvaraprofiil. Riistvarajaamad võivad riistvaraprofiile ühiselt kasutada, kuid need peavad olema vastendatud iga riistvarajaamaga. Lisaks soovitame kasutada ühiseid vahetusi, kui sama ühist riistvarajaama kasutab mitu seadet. Ühiskasutusega vahetuse seadistamiseks minge Rakenduse Retail ja **Commerce Channel häälestamise \>\> kassa häälestuse \> kassaprofiilidele \> Riistvaraprofiilid**. Valige iga ühise riistvaraprofiili jaoks sularahasahtel ja määrake valiku **Ühise vahetuse sahtel** väärtuseks **Jah**.
    -   **EFT kassa number** – EFT terminali ID, mida EFT volituste saatmisel kasutada. Selle ID annab krediitkaardiprotsessor.
    -   **Paketi nimi** – riistvarajaama pakett, mida riistvarajaama juurutamisel kasutada.

4.  Korrake samme 2 ja 3 iga täiendava riistvarajaamaga, mida kaupluses vaja on.
5.  Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.
6.  Valige jaotusgraafik **1090** uue riistvaraprofiili sünkroonimiseks kauplusega. Valige **käsk Käivita kohe**, et kassa muudatused sünkroonida.
7.  Valige jaotusgraafik **1040** uue riistvarajaama sünkroonimiseks kauplusega. Valige **käsk Käivita kohe**, et kassa muudatused sünkroonida.
8.  Installige riistvarajaam igasse hostarvutisse, mille toimingutes 2 ja 3 seadistasite. Lisateavet riistvarajaama paigaldamise kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md).
9.  Installige ja aktiveerige Modern POS. Lisateavet Modern POS-i installimise kohta vt teemast [Modern POS-i (MPOS) konfigureerimine, installimine ja aktiveerimine](retail-modern-pos-device-activation.md).
10. Logige Modern POS-i sisse ja valige **Kassaväliste toimingute tegemine**.
11. Käivitage toiming **Riistvarajaamade haldamine**.

12. Valige **suvand Haldamine**.
13. Määrake riistvarajaama haldamise lehel riistvarajaama sisselülitamise valik.
14. Valige kasutamiseks riistvarajaam ja seejärel **paar**.
15. Korrake toimingut 14 iga riistvarajaamaga, mida Modern POS kasutab.
16. Kui kogu nõutav riistvara on ühendatud, valige suvand **Sule**.
17. Riistvarajaama valikulehel valige viimati valitud riistvarajaam, et see aktiivseks muuta. 

> [!NOTE]
> Kui seadmed kasutavad sageli erinevaid riistvarajaamu, siis soovitame konfigureerida Modern POS-i paluma kassapidajatel maksmisprotsessi alustamisel riistvarajaama valida. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Registrid**. Valige register ja määrake siis valiku **Valige maksmisel** väärtuseks **Jah**. Kasutage jaotusgraafikut **1090** muudatuste sünkroonimiseks kanali andmebaasiga.

## <a name="extensibility"></a>Laiendatavus
Teavet riistvarajaama laiendatavuse stsenaariumide kohta leiate jaotisest [POS Integreerimine uue riistvaraseadmega ja laienduste paigaldaja genereerimine](dev-itpro/hardware-device-extension.md).

## <a name="security"></a>Turvalisus
Praeguste turvastandardite kohaselt tuleks kasutada tootmiskeskkonnas järgmisi sätteid: 

### <a name="hardware-station-installer"></a>Riistvarajaama paigaldaja
Riistvara jaama installer teeb automaatselt registri redigeerimist installimise käigus iseteeninduse kaudu.

-   Turvalinke soklikiht (SSL) peab olema keelatud.
-   Lubatud ja kasutusel tohib olla ainult transpordikihi turbe (TLS) versioon 1.2 (või kehtiv kõrgeim versioon). 

### <a name="ssl-and-tls"></a>SSL ja TLS
Vaikimisi on SSL ja kõik TLS-i versioonid (v.a TLS 1.2) keelatud. Nende väärtuste muutmiseks või lubamiseks tehke järgmist.
    1.  Vajutage Windowsi logo nuppu + R akna **Käivita** avamiseks.
    2.  Tippige väljale **Avatud** käsk Regedit **ja** seejärel valige **OK**.
    3.  Kui kuvatakse **kasutajakonto juhtelemendi** teateaken, valige **Jah**.
    4.  Minge aknas **Registriredaktor** asukohta **HKEY\_LOCAL\_MACHINESystemCurrentControlSetSecurityProvidersSCHANNELProtocols**. Järgmised koodid on automaatselt sisestatud, et lubada ainult TLS 1.2:
        -   TLS 1.2Server:Enabled=1
        -   TLS 1.2Server:DisabledByDefault=0
        -   TLS 1.2Client:Enabled=1
        -   TLS 1.2Client:DisabledByDefault=0
        -   TLS 1.1Server:Enabled=0
        -   TLS 1.1Client:Enabled=0
        -   TLS 1.0Server:Enabled=0
        -   TLS 1.0Client:Enabled=0
        -   SSL 3.0Server:Enabled=0
        -   SSL 3.0Client:Enabled=0
        -   SSL 2.0Server:Enabled=0
        -   SSL 2.0Client:Enabled=0
-   Rohkem võrguporte ei tohi avada, välja arvatud juhul, kui need on nõutavad teadaolevatel põhjustel.
-   Ressursside ühiskasutus lähtekohtade lõikes peab olema keelatud ja peab määratlema aktsepteeritavad lubatud lähtekohad.
-   Riistvarajaama käitavatel arvutitel kasutatavate sertide hankimiseks tuleb kasutada ainult usaldusväärseid sertifitseerimisasutusi.

> [!NOTE]
> On väga tähtis vaadata üle IIS-i ja Payment Card Industry (PCI) nõuete turbepõhimõtted.

## <a name="peripheral-simulator"></a>Välisseadme simulaator
Teavet leiate jaotisest [Commerce’i välisseadme simulaator](dev-itpro/retail-peripheral-simulator.md).

## <a name="microsoft-tested-peripheral-devices"></a>Microsofti testitud välisseadmed
### <a name="ipc-built-in-hardware-station"></a>IPC (integreeritud) riistvarajaam

Järgmisi välisseadmeid testiti rakendusse Modern POS Windowsile integreeritud IPC riistvarajaama abil.

#### <a name="printer"></a>Printer

| Tootja | Mudel    | Liides | Kommentaarid                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300 <a1/&.     | OPOS      | USB-toitel             |
| Star         | TSP650II | Kohandatud    | Võrgu kaudu ühendatud   |
| Star         | mPOP     | OPOS      | Bluetoothi kaudu ühendatud |
| Toshiba      | HSP100 <a1/&.   | OPOS      |                         |
| Toshiba      | HSP150 <a1/&.   | OPOS      |                         |

> [!NOTE]
> Täheprinterit TSP 100 ei toetata integreeritud riistvarajaama puhul. Integreeritud riistvarajaamas kasutatakse 64-bitiset protsessi, mis ei ühildu olemasoleva Star TP 100 draiveriga. 

#### <a name="bar-code-scanner"></a>Vöötkoodilugeja

| Tootja  | Mudel         | Liides | Kommentaarid |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| Honeywell     | 1900          | UWP       |          |
| HP integreeritud | E1L07AA       | OPOS      |          |
| Sümbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Makseterminalid ja PIN-klahvistikud

Dynamics 365 Commerce Rakendus <a0/& pakub väljaminev lahendus integreerimaks makseteenuste Mileeniga. [Dynamics 365 makseühendus Puhvri](dev-itpro/adyen-connector.md) jaoks kasutab seadme-agnostic [Puhvri makseterminali rakenduse programmeerimisliidest (API)](https://www.adyen.com/blog/introducing-the-terminal-api) ja saab suhelda kõigi makseterminaldega, mida SEE API toetab. Toetatud makseterminalide täieliku loendi leiate [Terminen POS-i terminalidest](https://www.adyen.com/pos-payments/terminals).

Saate kohandatud ühenduse loomisega kasutada ka muid Dynamics 365 Commerce maksepakkujaid. Kõiki maksepakkuja toetatud makseterminale saab kasutada koos Dynamics 365 Commerce. Samamoodi võimaldab see mis tahes makseseadme integreerimismudelit, Dynamics 365 Commerce mida maksepakkuja toetab, nt kohalik IP, pilve API või otseühendus (nt USB kaudu) kassasse. Lisateavet vt teemast [Makseterminali lõpp-lõpu makse integratsiooni loomine](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Sularahasahtel

| Tootja | Mudel     | Liides | Kommentaarid                |
|--------------|-----------|-----------|-------------------------|
| Star         | mPOP      | OPOS      | Bluetoothi kaudu ühendatud |
| APG          | Atwood    | Kohandatud    | Võrgu kaudu ühendatud   |
| Star         | SMD2-1317 | OPOS      |                         |
| HP           | QT457AA   | OPOS      |                         |
| Epson        |           | Kohandatud    | Ühendatud DK-pordi kaudu Epsoni võrguprinteriga |

#### <a name="line-display"></a>Rea kuva

| Tootja | Mudel    | Liides | Kommentaarid |
| ------------ | -------- | --------- | -------- |
| Epson        | Dm-D110  | OPOS      |          |
| HP           | T-seeria | OPOS      |          |

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

### <a name="dedicated-iis-hardware-station"></a>Sihtotstarbeline IIS-i riistvarajaam

Järgmisi välisseadmeid testiti, kasutades sihtotstarbelist (mitte ühist) IIS-i riistvarajaama koos Modern POS-iga Windowsile ja pilvekassaga.

#### <a name="printer"></a>Printer

| Tootja | Mudel    | Liides | Kommentaarid                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300 <a1/&.     | OPOS      | USB-toitel             |
| Star         | TSP650II | Kohandatud    | Võrgu kaudu ühendatud   |
| Star         | mPOP     | OPOS      | Bluetoothi kaudu ühendatud |
| Toshiba      | HSP100 <a1/&.   | OPOS      |                         |
| Toshiba      | HSP150 <a1/&.   | OPOS      |                         |

#### <a name="bar-code-scanner"></a>Vöötkoodilugeja

| Tootja  | Mudel         | Liides | Kommentaarid |
| ------------- | ------------- | --------- | -------- |
| Datalogic     | Magellan 8400 | OPOS      |          |
| HP integreeritud | E1L07AA       | OPOS      |          |
| Sümbol        | LS2208        | OPOS      |          |

#### <a name="payment-terminals-and-pin-pads"></a>Makseterminalid ja PIN-klahvistikud

Dynamics 365 Commerce Rakendus <a0/& pakub väljaminev lahendus integreerimaks makseteenuste Mileeniga. [Dynamics 365 makse konnektor Puhvri](dev-itpro/adyen-connector.md) jaoks kasutab seadme-agnostic [Puhvri makseterminali API-d](https://www.adyen.com/blog/introducing-the-terminal-api) ja saab suhelda kõigi makseterminaldega, mida see API toetab. Toetatud makseterminalide täieliku loendi leiate [Terminen POS-i terminalidest](https://www.adyen.com/pos-payments/terminals).

Saate kohandatud ühenduse loomisega kasutada ka muid Dynamics 365 Commerce maksepakkujaid. Kõiki maksepakkuja toetatud makseterminale saab kasutada koos Dynamics 365 Commerce. Samamoodi võimaldab see mis tahes makseseadme integreerimismudelit, Dynamics 365 Commerce mida maksepakkuja toetab, nt kohalik IP, pilve API või otseühendus (nt USB kaudu) kassasse. Lisateavet vt teemast [Makseterminali lõpp-lõpu makse integratsiooni loomine](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Sularahasahtel

| Tootja | Mudel     | Liides | Kommentaarid              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Kohandatud    | Võrgu kaudu ühendatud |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Kohandatud    | Ühendatud DK-pordi kaudu Epsoni võrguprinteriga |

#### <a name="line-display"></a>Rea kuva

| Tootja  | Mudel   | Liides | Kommentaarid |
|---------------|---------|-----------|----------|
| HP integreeritud | G6U79AA | OPOS      |          |
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

### <a name="shared-iis-hardware-station"></a>Ühiskasutuses IIS-i riistvarajaam

Järgmisi välisseadmeid testiti, kasutades ühist IIS-i riistvarajaama koos Modern POS-iga Windowsile ja pilvekassaga. 

> [!NOTE]
> Toetatakse ainult printerit, makseterminali ja sularahasahtlit.

#### <a name="printer"></a>Printer

| Tootja | Mudel    | Liides | Kommentaarid                |
| ------------ | -------- | --------- | ----------------------- |
| Epson        | TM-T88V  | OPOS      |                         |
| Epson        | TM-T88IV | OPOS      |                         |
| HP           | H300 <a1/&.     | OPOS      | USB-toitel             |
| Star         | mPOP     | OPOS      | Bluetoothi kaudu ühendatud |
| Toshiba      | HSP100 <a1/&.   | OPOS      |                         |
| Toshiba      | HSP150 <a1/&.   | OPOS      |                         |

#### <a name="payment-terminal"></a>Makseterminal

Dynamics 365 Commerce Rakendus <a0/& pakub väljaminev lahendus integreerimaks makseteenuste Mileeniga. [Dynamics 365 makse konnektor Puhvri](dev-itpro/adyen-connector.md) jaoks kasutab seadme-agnostic [Puhvri makseterminali API-d](https://www.adyen.com/blog/introducing-the-terminal-api) ja saab suhelda kõigi makseterminaldega, mida see API toetab. Toetatud makseterminalide täieliku loendi leiate [Terminen POS-i terminalidest](https://www.adyen.com/pos-payments/terminals).

Saate kohandatud ühenduse loomisega kasutada ka muid Dynamics 365 Commerce maksepakkujaid. Kõiki maksepakkuja toetatud makseterminale saab kasutada koos Dynamics 365 Commerce. Samamoodi võimaldab see mis tahes makseseadme integreerimismudelit, Dynamics 365 Commerce mida maksepakkuja toetab, nt kohalik IP, pilve API või otseühendus (nt USB kaudu) kassasse. Lisateavet vt teemast [Makseterminali lõpp-lõpu makse integratsiooni loomine](dev-itpro/end-to-end-payment-extension.md).

#### <a name="cash-drawer"></a>Sularahasahtel

| Tootja | Mudel     | Liides | Kommentaarid              |
|--------------|-----------|-----------|-----------------------|
| APG          | Atwood    | Kohandatud    | Võrgu kaudu ühendatud |
| Star         | SMD2-1317 | OPOS      |                       |
| HP           | QT457AA   | OPOS      |                       |
| Epson        |           | Kohandatud    | Ühendatud DK-pordi kaudu Epsoni võrguprinteriga |


## <a name="troubleshooting"></a>Tõrkeotsing
### <a name="modern-pos-can-detect-the-hardware-station-in-its-list-for-selection-but-it-cant-complete-the-pairing"></a>Modern POS suudab tuvastada oma valikuloendis riistvarajaama, kuid ei suuda sidumist läbi viia

**Lahendus.** Kontrollige järgmist võimalike probleemikohtade loendit.

-   Arvuti, millel Modern POS töötab, usaldab serti, mida kasutatakse riistvarajaama käitavas arvutis.
    -   Selle seadistuse kontrollimiseks minge veebibrauseris järgmisele URL-ile: https://&lt;Computer Name&gt;:&lt;Port Number&gt;/HardwareStation/ping.
    -   See URL kasutab pingimist kontrollimiseks, et arvutile on võimalik juurde pääseda, ja brauser näitab, kas serti usaldatakse. (Näiteks kuvatakse aadressiribal Internet Explorer luku sümbol. Kui valite selle sümboli, kontrollib see, Internet Explorer kas sert on praegu usaldusväärne. Serdi saab kohalikku arvutisse installida, vaadates kuvatud serdi üksikasju.)
-   Riistvarajaama käitavas arvuti tulemüüris avatakse port, mida riistvarajaam kasutab.
-   Riistvarajaamal on õigesti installitud kaupmehe konto andmed tööriista Kaupmehe teabe installimine kaudu, mis riistvarajaama installiprogrammi lõpus käivitub.

### <a name="modern-pos-cant-detect-the-hardware-station-in-its-list-for-selection"></a>Modern POS ei suuda oma valikuloendis riistvarajaama tuvastada

**Lahendus.** Seda probleemi võib põhjustada kumbki järgmistest teguritest.

-   Riistvarajaam pole peakontoris õigesti häälestatud. Lisateavet vt jaemüügi riistvarajaama [konfigureerimine ja installimine](retail-hardware-station-configuration-installation.md#troubleshooting). 
-   Kanali konfiguratsiooni uuendamiseks pole töid käivitatud. Sellisel juhul käivitage töö 1070 kanali konfigureerimiseks.

### <a name="modern-pos-doesnt-reflect-new-cash-drawer-settings"></a>Modern POS ei kajasta uusi sularahasahtli sätteid

**Lahendus.** Sulgege see partii. Sularahasahtli muudatusi ei uuendata Modern POS-is enne praeguse partii sulgemist.

### <a name="modern-pos-is-reporting-an-issue-with-a-peripheral"></a>Modern POS teatab probleemist välisseadmega

**Lahendus.** Siin on mõned selle probleemi tüüpilised põhjused.

-   Veenduge, et muud seadmedraiveri konfiguratsiooniutiliidid oleksid suletud. Kui need utiliidid on avatud, võivad need takistada Modern POS-il või riistvarajaamal seadmele juurdepääsemist.
-   Kui välisseade on mitme kassaseadmega ühiskasutuses, siis veenduge, et see kuuluks ühte järgmistest kategooriatest.
    -   Sularahasahtel
    -   Kviitungiprinter
    -   Makseterminal

    Kui välisseade nendesse kategooriatesse ei kuulu, siis ei ole riistvarajaam mõeldud selle välisseadme ühiskasutuseks mitme kassaseadme hulgas.
-   Mõnikord võivad seadmedraiverid takistada üldiste juhtimisobjektide (CCO-de) õiget töötamist. Kui seade on hiljuti installitud, kuid ei tööta korralikult või märkate muid probleeme, saab selle probleemi sageli CCO-de uuesti installimisega lahendada. CCO-de allalaadimiseks külastage veebisaiti <http://monroecs.com/oposccos_current.htm>.
-   Kui vahetate testimise või tõrkeotsingu ajal sageli välisseadmeid, siis võib olla vaja IIS lähtestada, selle asemel, et oodata, millal vahemälu end värskendab. IIS-i lähtestamiseks tehke järgmist.
    1.  Sisestage menüüsse **Start** tekst **CMD**.
    2.  Otsingutulemustes paremklõpsake käsuviiba **ja** valige käsk Käivita **administraatorina**.
    3.  Sisestage aknasse **Käsuviip** tekst **iisreset /Restart** ja vajutage siis klahvi Enter.
    4.  Pärast IIS-i taaskäivitumist taaskäivitage Modern POS.
-   Kui muudate sageli välisseadmeid ja selle käigus POS-i klienti sageli käivitate ja sulete, võib eelmise kassaseansi protsess dllhost praegust seanssi häirida. Sellisel juhul ei pruugi seade olla kasutatav enne, kui sulgete dünaamilise lingiga teegi (DLL-i) hosti, mis eelmist seanssi haldab. DLL-i hosti sulgemiseks tehke järgmist.
    1.  Sisestage menüüsse **Start** tekst **Tegumihaldur**.
    2.  Otsingutulemustes valige **ülesandehaldur**.
    3.  Tööülesande halduri vahekaardil Üksikasjad **valige** veeru päis, **mis on sildiga Nimi**, et sortida tabeli tähestikuliselt nime järgi.
    4.  Kerige alla, kui leiate nime dllhost.exe.
    5.  Valige iga DLL-host ja seejärel käsk **Lõpeta ülesanne**.
    6.  Kui DLL-i hostid on suletud, taaskäivitage Modern POS.


## <a name="additional-resources"></a>Lisaressursid

[Commerce’i välisseadme simulaator](dev-itpro/retail-peripheral-simulator.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
