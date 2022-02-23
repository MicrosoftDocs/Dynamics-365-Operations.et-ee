---
title: Mis on uut või mida on muudetud rakenduses Dynamics AX 7.0 (veebruar 2016)
description: Selles artiklis kirjeldatakse Microsoft Dynamics AX 7.0 uusi või muutunud funktsioone. See versioon sisaldab nii platvormi kui ka rakenduse funktsioone ja anti välja veebruaris 2016.
author: sericks007
manager: AnnBe
ms.date: 10/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91243
ms.assetid: 515bc6e7-a85d-4995-95c6-6cab6c8aa0f9
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c1b63ba623eb1699938476825a77fd40d838142
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797215"
---
# <a name="whats-new-or-changed-in-dynamics-ax-70-february-2016"></a>Mis on uut või mida on muudetud rakenduses Dynamics AX 7.0 (veebruar 2016)

[!include [banner](../includes/banner.md)]

Selles artiklis kirjeldatakse Microsoft Dynamics AX 7.0 uusi või muutunud funktsioone. See versioon sisaldab nii platvormi kui ka rakenduse funktsioone ja anti välja veebruaris 2016.

## <a name="cost-management"></a>Kuluhaldus

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate kiire ülevaate laosaldost, lõpetamata toodangu (WIP) laosaldost ja valitud finantsaasta lao sisse- ja väljavoolust.</td>
<td>Pole kohaldatav</td>
<td>Tööruumis <strong>Kuluhaldus</strong> on jaotis, kus on antud valitud rahandusperioodi WIP varude väljavõte. Väljavõte põhineb andmekogumi vahemälul, mida vaikimisi iga 24 tunni tagant uuendatakse. Andmekogumi vahemälu saab konfigureerida nii, et kasutajad saavad seda reaalajas aruandluse jaoks käsitsi värskendada. <strong>Andmete värskenduse oleku kaart</strong> tööruumis <strong>Kuluhaldus</strong> näitab, millal vahemälu viimati värskendati.</td>
<td>Kulude kontrollijad soovivad teada, kas varude või WIP varude väljavõtte saldo suureneb või väheneb ajas. Klassifitseerides väljavõttes tegevussündmusi, saab kulude kontrollija varude voost ülevaate. Kui varusid või WIP varusid hinnatakse standardkulude alusel, on näha ka üldist registreeritud hälvet.</td>
</tr>
<tr>
<td>Kasutage moodulit<strong> Kuluhaldus</strong>.</td>
<td>Pole kohaldatav</td>
<td>Kuluhaldust esitatakse domeenialana. Kulupõhine konfiguratsioon ja ülevaade olid hajutatud laohalduse, tootmise juhtimise ja ostureskontro vahel.</td>
<td>Kuna kõik kulude haldamisega seotud ülesanded on tsentraliseeritud ühe moodulisse, on kulu kontrollijatel lihtsam süsteemi hallata.</td>
</tr>
<tr>
<td>Varude arvestuse ja tootmise raamatupidamisega seotud sisestustüübid on uuendatud.</td>
<td>Sildid vormidel <strong>InventPosting</strong>, <strong>Ressurss</strong>, <strong>ResourceGroup</strong> ja <strong>ProductionGroup</strong> pole alati tegelikult kasutatavate siltidega <strong>LedgerPostingType</strong> kooskõlas. Siltidel kasutatavat terminoloogiat pole lihtne mõista.</td>
<td>Silte on uuendatud nii, et sildid lehtedel <strong>InventPosting</strong>, <strong>Ressurss</strong>, <strong>ResourceGroup</strong> ja <strong>ProductionGroup</strong> on tegelike siltidega <strong>LedgerPostingType</strong> kooskõlas. Kõik sildid on ka ümber nimetatud, nii et sildid on tegevuse sündmustega kooskõlas. Pange tähele, et tegelikku sisestusloogikat ei ole muudetud.</td>
<td>Süsteemi on lihtsam seadistada, kuna uued sildid on seotud seda sisestustüüpi kasutavate tegevuse sündmustega.</td>
</tr>
<tr>
<td>Saate importida/eksportida ostuhinna, kulu või müügihinna Microsoft Excelist kuluarvutuse versiooni või sealt ära.</td>
<td>Hindu või kulusid ei saa õigesti kuluarvutuse versiooni importida, kuna andmemudel nõuab InventDim ID-d.</td>
<td>Andmeüksuste kasutuselevõtmine võimaldab rakendada importimise/eksportimise funktsiooni. See funktsioon võimaldab kasutajatel importida või eksportida hindu või kulusid kuluarvutuse versiooni.
<ul>
<li>Importige ostuosakonnalt saadud järgmise aasta ostuhindade tervikloend.</li>
<li>Suunake kulud ja standardsed müügihinnad peakontorist ühe toiminguga ühte või mitmesse müügiettevõttesse.</li>
</ul></td>
<td>See võib säästa kulude kontrollijatel süsteemi haldamisel palju aega, eriti kui nad peavad haldama järgmise rahandusaasta eelmääratud kulusid.</td>
</tr>
<tr>
<td>Saate kiire ülevaate kuluobjekti laosaldost ja keskmisest ühiku maksumusest.</td>
<td>Kasutaja peab avama laoseisu vormi ja valima varude dimensioonid, mis kuluobjekti kajastavad. Seetõttu peab kasutaja teadma, millised laodimensioonid konkreetse toote finantsilise laovaru puhul märgiti.</td>
<td>Kasutusele on võetud uus leht <strong>Kuluobjekt</strong>. Sellel lehel kuvatakse vaikimisi kõik tootega seotud kuluobjektid. Lehel kuvatakse jooksev laokogus, väärtus ja keskmine ühikukulu kuluobjekti kohta.</td>
<td>See vähendab mõnevõrra keerukust ja lihtsustab kulu kontrollimist.</td>
</tr>
<tr>
<td>Kasutage inventuuri ajal uut lehte <strong>Kulukirjed</strong>.</td>
<td>Varude juhtimine võib olla registreeritud laokannete ja seotud tasakaalustuste puhul keeruline, kuna samad kanded võivad olla füüsilised või rahalised.</td>
<td>Lehel <strong>Kulukirjed</strong> pakutakse uut laokannete kuvamise viisi.
<ul>
<li>Kanded on kuvatud kronoloogilises järjestuses.</li>
<li>Kaasatakse ainult kanded, mis kulusid lisavad.</li>
<li>Puudub füüsiliste kulude või rahaliste kulude mõiste.</li>
<li>Puudub füüsilise koguse või rahalise koguse mõiste.</li>
<li>Kulud lisatakse järk-järgult.</li>
</ul></td>
<td>See võib säästa märkimisväärselt kulu kontrollijate aega, kui nad peavad kande tasandil varusid kontrollima.</td>
</tr>
<tr>
<td>Kasutage uut dialoogiboksi <strong>Toote WIP väljavõte</strong> konkreetse toote kogunenud kulude koondvaate nägemiseks.</td>
<td>Pole kohaldatav</td>
<td>WIP aruanne kuvab konkreetse tootmistellimuse WIP saldo kokkuvõtte, mis on rühmitatud sobivatesse kuluklassifikatsioonidesse. Diagramm näitab kronoloogilises järjekorras, kuidas tegevuste sisestused on WIP saldot mõjutanud.</td>
<td>See võib säästa kulu kontrollijatele märkimisväärselt aega, kui neil on vaja teada, milline on konkreetse tootmistellimuse WIP saldo või kui palju materjali tellimuses tarbitud on.</td>
</tr>
<tr>
<td>Kasutage tootmistellimuste puhul kasutusele võetud funktsiooni Kuva kulu võrdlus. See funktsioon hõlbustab tootmistellimusega seotud kulude võrdlemist.</td>
<td>Kasutaja saab võrrelda ainult eeldatavaid kulusid ja realiseeritud kulusid. Võrdluse saab teha madalaimal tasemel.</td>
<td>Kuluvõrdluse funktsioon võimaldab kulu kontrollijatel võrrelda järgmisi andmeid.
<ul>
<li>Aktiivne kulu vs hinnanguline kulu = plaanimise hälve</li>
<li>Hinnanguline kulu vs realiseeritud kulu = tootmise hälve</li>
<li>Plaanimise hälve + tootmise hälve = koguhälve</li>
</ul>
See funktsioon töötab toodetud kaubale määratud kuluarvestuse meetoditest sõltumatult. Vaikimisi kuvatakse diagrammil kulude võrdlus kulugrupi tüübi järgi. Diagramm võimaldab kasutajatel minna süvitsi detailsematele tasemetele.</td>
<td>See võimaldab kulu kontrollijatel või tootmisjuhtidel analüüsida, kust tootmishälbed pärinevad ja mis neid põhjustab.</td>
</tr>
</tbody>
</table>

## <a name="developer"></a>Arendaja

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Saate luua pilves veebipõhiseid lahendusi, millele pääseb juurde paljudelt seadmetelt. | Pole saadaval | Dynamics AX-i praegune versioon põhineb uuel veebipõhisel kliendil ja kliendiraamistikul. | Saate pakkuda oma lõppkasutajatele järgmise põlvkonna lahendusi. |
| Lahenduste väljatöötamine Microsoft Visual Studio abil. | Microsoft MorphX on peamine arenduskeskkond, kuid osa arendamisest toimub Visual Studios. | Visual Studio on ainus arenduskeskkond. | Selles on alles tuttavad Dynamics AX 2012 mõisted, mis on sujuvalt kohandatud Visual Studio raamistiku ja paradigmadega. See võimaldab standardset koostalitlust teiste .NET-keelte ja -projektidega. |
| Koostamiskeel Common Intermediate Language (CIL) kõigi funktsioonide jaoks. | X++ on kompileeritud pseudokoodiks. | Täiesti uus X++ kompilaator loob CIL-i kõigi funktsioonide jaoks. CIL on sama vahekeel, mida kasutavad muud. NET-põhised keeled. | CIL on kiirem, suudab tõhusalt viidata hallatud dünaamilise lingiga teekide (DLL-ide) klassidele ja suudab töötada .NET-utiliitide suures tööriistabaasis. |
| Saate manustada Microsoft Dynamics AX-i klienti äriteabe (BI) aruandeid ja visualiseerimisi. | Pole saadaval | Saate luua väga intuitiivseid ja sujuvaid visualiseerimisi. | See võimaldab BI-l põhinevaid otsustusülevaateid. |
| Microsoft Office’iga integreerimine. | Pole saadaval | Uute võimaluste hulka kuulub Exceli andmekonnektori rakendus, **töövihiku koostaja** leht, ekspordi API ja dokumendihaldus. | Saate luua oma lõppkasutajatele tööviljakuse lahendusi. |
| Saate koostamist, testimist ja juurutamist automatiseerida. | Osaliselt saadaval | Juurutage arendaja topoloogia, kasutades arendajat ja VM-i koostajat. Saate konfigureerida automaatselt VM-i koostajat, et avastada ja koostada mooduleid rakenduses Visual Studio Online (VSO) ning käitada teste. Toetatakse C\# ja X++ mooduli kompileerimist ja viiteid. | See suurendab arendaja tööviljakust, vähendades testimise ja valideerimise kulusid ning panust. |
| Kohandage ülekatte ja laiendustega. | Laiendused ei ole saadaval. | Dynamics AX-i praegusel versioonil on uus kohandamismudel. | Saate kohandada Microsofti või muude Microsofti partnerite tarnitud mudelielementide lähtekoodi ja metaandmeid. |
| Saate luua uusi juhtelemente ja kasutajaliidese elemente, kasutades X++ ja kaasaegset veebiraamistikku. | Kohandatud juhtelemendid sõltuvad välistest raamistikest, nt Microsoft ActiveX ja Windows Presentation Foundation (WPF). | Praeguses versioonis on lihtsam juhtelemente koostada. X++ raamistikku saab kasutada rakenduse käitumise ja äriloogika jaoks ning HTML/JavaScripti-põhine klient võimaldab kaasaegset visualiseerimist. | Teie juhtelementide välimuse ja toimimise saab kujundada sarnaselt Dynamics AX-i valmis (OOB) juhtelementidele. |
| Hinnake ja häälestage jõudlust uute tööriistade abil. | PerfSDK, Data Expansion Toolkit, Trace Parseri veebirakendus ja PerfTimer pole saadaval. | PerfSDK, Data Expansion Toolkit, Trace Parseri veebirakendus ja PerfTimer on uued. | Tarkvara arenduskomplekt (SDK) võimaldab kontrollida ja valideerida kõiki olulisi äriprotsesse ühe kasutajaga ja vajaduse korral mitme kasutajaga proovitsüklis. Data Expansion Toolkit võimaldab laiendada õigesti kõiki jõudlusteste, millel peavad olema koondandmed ja kandeandmed õigesti laiendatud. Trace Parser võimaldab valideerida ainukasutaja jõudlustesti mitme kasutajaga tsüklit. PerfTimeri abil saate vaadata, kas mõni päring või konkreetne meetodikutse põhjustab jõudlusprobleemi. Seega pole vaja kõike üksikasjalikult jälgida ja analüüsida. |
| Kuvage OData abil uuendatav vaade. | Pole saadaval | Dynamics AX-i praeguses versioonis on võetud kasutusele avalik OData teenuse lõpp-punkt, mis võimaldab ühtlast juurdepääsu Dynamics AX-i andmetele väga mitmesugustest klientidest. | Teie lahendused suudavad suhelda RESTfuli teenustega, jagada andmeid tuvastataval viisil ja võimaldavad ulatuslikku integratsiooni, kasutades HTTP virnaprotokolli. |
| Kasutage Business Connectorit äriloogika loomiseks ja integreerimisstsenaariumide toetamiseks. | Business connector on saadaval hallatavast koodist koodi X++ kutsumiseks. Soovitame teil kasutada Business Connectorit ainult äriloogika autoriõiguste andmiseks moodulis C\#, kuid mitte integreerimise stsenaariumide jaoks. | Business Connectorit ei toetata enam. Loomise nõude tingib asjaolu, et X++ on hallatavasse koodi kompileeritud. Seetõttu on interop lihtsam. Integreerimisstsenaariume täidetakse OData abil. | Business Connectorit ei saa edasi liikudes kasutada. |
| Valige skaala (st kümnendkohtade arv) tõelistel andmebaasiväljadel ja laiendatud andmetüüpidel (EDT-del). | Skaala 16 on vaikeskaala ja arendaja ei saa seda muuta. | EDT-del ja väljadel on nüüd skaala atribuut, mida saab rakendada üksikule väljale ja EDT-le. Vaikeväärtuseks on määratud 6, mitte 16. | NCCI tabelite kasutamisel (SQL-i mälu tugi) on kiirus suurte tellimuste puhul väiksema skaala kasutamisel suurem. Muutke skaalasid nii, nagu eraldi väljade kasutamisel vaja. |

## <a name="financial-management"></a>Finantshaldus

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Kontostruktuuride eksportimine Microsoft Excelisse.</td>
<td>Pole saadaval</td>
<td>Nüüd saate valida konto struktuuri ja eksportida selle Excelisse.</td>
<td>Paljud kliendid on soovinud võimalust eksportida konto struktuure hõlpsamaks filtreerimiseks Excelisse.</td>
</tr>
<tr>
<td>Saate kuvada konto struktuuriga seotud pearaamatud ja täpsemad reeglistruktuurid ühel lehel.</td>
<td> Kasutatava pearaamatu ja konto struktuuri vaatamiseks peab kasutaja minema mitmele vormile.</td>
<td>Konto struktuuri lehele on lisatud kiirinfo.</td>
<td>Kui konto struktuurid on määratletud ja redigeeritud, on olulisele teabele hõlpsam juurde pääseda.</td>
</tr>
<tr>
<td>Kuvage kontoplaaniga seotud pearaamatud ühel lehel.</td>
<td>Kasutaja peab minema iga ettevõtte juurde ja avama pearaamatu vormi, et näha pearaamatule määratud kontoplaani.</td>
<td>Lehele <strong>Kontoplaan</strong> on lisatud kiirinfo.</td>
<td> Kui kontoplaan on määratletud ja määratud, on olulisele teabele hõlpsam juurde pääseda.</td>
</tr>
<tr>
<td>Sulgemislehe korrektsioone ja sulgemiskandeid saate vaadata eraldi veergudes loendilehel <strong>Proovibilanss</strong>.</td>
<td>Kasutaja näeb mõlemat tüüpi kandeid ühes veerus.</td>
<td>Loendilehele <strong>Proovibilanss</strong> on lisatud täiendav parameeter.</td>
<td>See võimaldab täpsemat andmeanalüüsi ja see on vajalik ka regulatiivseks aruandluseks mõnes riigis/regioonis.</td>
</tr>
<tr>
<td>Kasutage uut lehte <strong>Üldine pearaamat</strong>.</td>
<td>Pole saadaval</td>
<td>Uus leht <strong>Üldine pearaamat</strong> pearaamatute sisestamiseks. Selle lehe õigused on lisatud rollile <strong>Raamatupidaja</strong>.</td>
<td>Võimaldab ühiskasutuses teenuse raamatupidajal siseneda ettevõtete lõikes pearaamatutesse, ilma et oleks vaja vormilt lahkuda või ettevõtte konteksti vahetada.</td>
</tr> 
<tr>
<td>Kasutage uut lehte <strong>Arvestusallika uurija </strong>.</td>
<td>Saadaval alates versioonist Dynamics AX 2012 R3 CU10.</td>
<td>Uus leht <strong>Arvestusallika uurija</strong> ja toimingud loendilehelt <strong>Proovisaldo</strong> ja lehelt <strong>Kande toimingud</strong> sinna liikumiseks.</td>
<td>Teeb võimalikuks kõige üksikasjalikuma teabe vaatamise proovisaldo või raamatupidamiskirje allika kohta pearaamatus või sihtanalüüsiks.</td>
</tr>
<tr>
<td>Lisage veel sisestuskihte.</td>
<td>Täiendavate sisestuskihtide lisamine oli arendaja töö.</td>
<td>Nüüd on saadaval kümme sisestuskihti.</td>
<td>Enamik kliente lisab veel sisestuskihte.</td>
</tr>
<tr>
<td>Kasutage valikut Seotud kanne.</td>
<td>Pole saadaval</td>
<td>Seotud kande valik on kasutajatele saadaval selleks, et kasutajad näeksid kannet vastaskonto ettevõttes, kui nad ettevõtete vahelisi kandeid sisestavad. Seotud kannete all saavad kasutajad klõpsata üksikasju ja liikuda kiiresti vastaskonto ettevõtte kandele.</td>
<td>Ettevõtete vaheliste kannete sisestamisel puudus kasutajatel võimalus vaadata või leida vastaskonto ettevõtte alla sisestatud kannet.</td>
</tr>
<tr>
<td>Hulgi finantsperioodi sulgemine</td>
<td>Pole saadaval</td>
<td>Kasutajad saavad mooduli juurdepääsu värskendada ja muuta perioodi olekut korraga mitme ettevõtte puhul.</td>
<td>Enne seda funktsiooni pidid kasutajad vahetama ettevõtet, kuhu nad olid sisse logitud, minema pearaamatu kalendri vormile ja värskendama käsitsi mooduli juurdepääsu ja perioodi olekut.</td>
</tr>
<tr>
<td>Laske Oandal vahetuskursse pakkuda.</td>
<td>Vahetuskursside pakkuja konfigureerimine kursside importimiseks Oandast oli arendaja töö.</td>
<td>Kui kasutajatel on Oanda kood, võivad nad selle vahetuskursside pakkuja konfigureerimisel sisestada.</td>
<td>Kasutajad saavad kasutada kasutusvalmis lahendust, lastes Oanda pakutavaid vahetuskursse regulaarselt importida.</td>
</tr>
<tr>
<td>Filtreerige finantsaruandeid (Management Reporter) dimensioonide, atribuutide, kuupäevade ja stsenaariumide alusel.</td>
<td> Management Reporteri aruannete filtreerimine toimub aruande ülesehituse kaudu. Näiteks kui kasutaja, kellel on vaatamisõigus, soovib vaadata mõne muu kuupäeva aruannet, peab aruande koostaja muudatuse tegema.</td>
<td>On lisatud aruande suvandid, et saaks rakendada erinevaid filtreid, kui kasutaja vaatab aruannet. Nende filtrite põhjal luuakse seejärel uus aruanne.</td>
<td>Finantsaruannete tarbijad saavad rakendada erinevaid dimensioonide, kuupäevade, atribuutide ja stsenaariumide filtreid, ilma et aruande ülesehituses oleks vaja muudatusi teha.</td>
</tr>
<tr>
<td>Saate vaadata finantsaruandeid (Management Reporter) Microsoft Dynamics AX-i kliendis.</td>
<td>Management Reporteri aruannete kuvamiseks kasutati eraldi veebiklienti.</td>
<td>Kõigile finantsaruannetele pääseb Dynamics AX-i kliendis juurde. Kasutaja valib vaatamiseks aruande ja aruanne kuvatakse kliendis.</td>
<td>Nüüd saate finantsaruandeid vaadata ilma teist klienti/rakendust avamata.</td>
</tr>
<tr>
<td>Saate printida finantsaruandeid (Management Reporter) Microsoft Dynamics AX-i kliendist.</td>
<td>Aruande printimisel kasutatakse printimiseks brauseri printimisvalikuid ja prinditakse ainult seda, mida kasutaja ekraanil näeb.</td>
<td>Kasutaja saab valida aruande üksikasjalikkuse taseme ja lehekülje paigutuse, kasutades Dynamics AX-i kliendis valikut Prindi.</td>
<td>Prinditud aruanded prinditakse veebilehe printimise asemel kasutaja soovitud viisil.</td>
</tr><tr>
<td>Saate finantsandmeid analüüsida, kasutades Power BI sisu „Finantsnäitajate jälgimine”.</td>
<td>Pole saadaval</td>
<td>Valige lehel PowerBI.com käsk <strong>Too andmed</strong> ja seejärel valige sisupakett <strong>Dynamics AX – finantsnäitajad</strong>. Sisestage oma Dynamics AX-i lõpp-punkti URL, et näha andmeid armatuurlaual.</td>
<td>3–4 hiireklõpsuga saavad organisatsioonid võtta kasutusele Power BI armatuurlaua, mis sisaldab olulisi finantsandmeid. Organisatsioon saab sisu isikupärastada.</td>
</tr>
<tr>
<td>Saate jälgida finantsperioodi sulgemise protsesse.</td>
<td>Pole saadaval</td>
<td>Sulgemismallid ja -graafikud saab koostada, kasutades finantsperioodi sulgemise konfiguratsiooni. Kasutage tööruumi <strong>Finantsperioodi sulgemine</strong> sulgemisgraafikute edenemise jälgimiseks mitmes ettevõttes.</td>
<td>Tööruum eemaldab manuaalsed süsteemid sulgemistegevuste määratlemiseks, plaanimiseks ja teavitamiseks. Seetõttu väheneb sulgemiseks vajalik päevade arv.</td>
</tr>
<tr>
<td>Saate jälgida eelarve ja tegelike väärtuste suhet ning koostada pearaamatu prognoose, kasutades tööruumi <strong>Pearaamatu eelarved ja prognoosid</strong> ja täiendavaid päringuvorme.</td>
<td>Pole saadaval</td>
<td> Tööruumi pääseb Dynamics AX-i armatuurlaualt. See sisaldab linke mitmele uuele päringulehele: <strong>Kokkuvõte: tegelik vs eelarve</strong>, <strong>Eelarve juhtimise statistika kokkuvõte</strong>, <strong>Eelarve registrikirjed</strong> ja <strong>Eelarveplaanid</strong>.</td>
<td>Uued päringulehed võimaldavad hõlpsat juurdepääsu eelarveteabele. Tööruum ühendab kõik eelarve haldamise ja jälgimise ülesanded ühte kohta, mida eelarvehalduritel või raamatupidamise juhtidel on lihtne kasutada.</td>
</tr>
<tr>
<td>Saate eelarveplaanide ja prognooside paigutusi koostada.</td>
<td>Dokument <strong>Eelarveplaan</strong> kuvatakse ridade loendina, millel on finantsdimensioonide kombinatsioonide kehtivuse kuupäevad ja summad. Kasutaja peab koostama ja kasutama Ecxeli malle eelarveplaani andmete kuvamiseks liigendtabelis.</td>
<td>Eelarveplaanide ja prognooside jaoks on saadaval piiramatu arv paigutusi. Saate kombineerida paigutuses valitud finantsdimensioone, kasutaja määratud veerge ja muid rea atribuute (nt kommentaare, projekte ja varasid). Kasutajad saavad käigu pealt eelarveplaani dokumendi paigutust vahetada ja igasugust valitud paigutust kasutades andmeid redigeerida. Eelarve planeerimise konfigureerimist lihtsustab stsenaariumi piirangute kaotamine ja paigutuste kasutamine määratlemiseks, milliseid andmeid igas eelarveplaani dokumendis kuvada ja redigeerida saab.</td>
<td>See annab paindlikkuse luua ja redigeerida eelarveplaane nii Excelis kui ka Dynamics AX-i kliendis. Exceli töövihikute malle saab koostada eelarveplaani paigutuse seadistuse abil.</td>
</tr>
<tr>
<td>Saate printida aruande <strong>Hankija arve kanded</strong>, kasutades aruande <strong>Üksikasjalik tähtajaloend</strong> andmeid, mis sisaldab tähtaja ületamise päevi.</td>
<td>Tuleb printida kaks erinevat aruannet: <strong>Üksikasjalik täheajaloend</strong> ja <strong>Hankija arve kanded</strong>.</td>
<td>Kahe aruande andmed on konsolideeritud aruandesse <strong>Hankija arve kanded</strong>. Aruanne <strong>Üksikasjalik tähtajaloend</strong> on aegunud.</td>
<td>See välistab kahe eraldi, kuid seotud aruande printimise vajaduse.</td>
</tr>
<tr>
<td>Regulatiivsete aruannete loomine otse PDF-vormingus.</td>
<td>Esmalt tuleb koostada ühes vormingud regulatiivne aruanne ja eksportida see siis PDF-vormingusse.</td>
<td>PDF-vorming on regulatiivsete aruannete vaikevorming.</td>
<td>See tagab ühtlase kuvamise nii arvutiekraanil kui ka prinditud pabereksemplaril.</td>
</tr>
<tr>
<td>Saate käivitada käibemaksu tasakaalustamise protsessi pakktöötlusena.</td>
<td>Pole saadaval</td>
<td>Lehel <strong>Käibemaksu tasakaalustusperiood</strong> saate määrata, et tasakaalustusprotsess peab toimuma pakktöötlusrežiimis.</td>
<td>Paljude maksukannetega perioodide puhul võib tasakaalustamise protsess olla aeganõudev ja võib olla parem käivitada protsess taustal pakktöötlusena.</td>
</tr>
</tbody>
</table>

## <a name="foundation"></a>Sihtasutus

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Pääsete kliendile alati kõikjal juurde.</td>
<td>AX 2012 töölauaklient pakub vormide tervikkomplekti, kuid see töötab ainult arvutites, milles on Microsoft Windows, ja nõuab installimist. Töölauakliendiga kasutatakse sageli terminaliserverit, et võimaldada juurdepääsu üle laivõrgu (WAN). Ettevõtteportaali veebiklient pakub väiksemat vormikomplekti.</td>
<td>Kaks AX 2012 klienti on asendatud ühe standarditel põhineva veebikliendiga, mis pakub terviklikku töölauakliendi funktsioonide kogumit koos ettevõtteportaali kliendi ulatusega.</td>
<td>See väldib arenduspanuse jagamist kahe kasutajaliidese platvormi vahel. Kasutades standardseid veebiliideseid, välistab see terminaliserveri vajaduse.</td>
</tr>
<tr>
<td>Olge uue tegevuse salvestaja abil produktiivsed.</td>
<td>AX 2012 tegevuse salvestaja nõuab otsejuurdepääsu rakendusobjekti serveri (AOS) arvutist ja suuremaid õigusi ega paku redigeerimisvalikuid.</td>
<td>Uut tegevuse salvestajat saab kasutada otse veebikliendist. Juurdepääs tegevuse salvestajale ei nõua administraatoriõigusi. Salvestatud toiminguid saab salvestamise ajal reaalajas vaadata, kasutusele on võetud uued redigeerimisvõimalused ja tegevuse salvestaja toetab rohkemaid stsenaariume lisaks olemasolevatele äriprotsesside modelleerija (BPM) stsenaariumidele.</td>
<td>Uus tegevuse salvestaja pakub sujuvamat kogemust ja lisab Dynamics AX-is uusi võimalusi. Mõned neist võimalustest on kohe saadaval ja edaspidi lisandub neid veel.</td>
</tr>
<tr>
<td>Aitab kasutajatel mõista paremini nende edasist tööd tööruumidega.</td>
<td>Rollikeskused annavad ülevaate teabest, mis puudutab kasutaja töö funktsiooni ettevõttes või organisatsioonis.</td>
<td>Tööruumid on Dynamics AX-is uus kontseptsioon, mis on mõeldud rollikeskuste asendamiseks peamise viisina ülesannete ja konkreetsete lehtede juurde liikumiseks. Need annavad ühel lehel ülevaate äritegevusest ja aitavad kasutajatel mõista jooksvat olekut, tulevast töökoormust ja protsessi või kasutaja sooritust. Tööruumid on AX 2012 rollikeskustest detailsemad ja kasutajatel võib olla juurdepääs mitmele tööruumile.</td>
<td>Tööruumid on mõeldud kasutaja tootlikkuse suurendamiseks. Arendajad peavad looma tööruumi igale tootes toetatud olulisele „tegevusele”. AX 2012 pärandrollikeskus asendatakse praeguses Dynamics AX-i versioonis tavaliselt mitme tööruumiga.</td>
</tr>
<tr>
<td>Saate panna vormid reageerima brauseri vaateavale või seadme suurusele.</td>
<td>AX 2012-s oli vormi sisu veergudega jäigalt paigutatud ja üldine vormi kõrgus/laius määrati suuresti vormil olevate juhtelementide põhjal.</td>
<td>Üleminekuga veebi Dynamics AX-i uusimas versioonis põhinevad vormi dimensioonid nüüd brauseri vaateava suurusel või seadmel. Juhtelemente ja paigutuse parameetreid on muudetud või lisatud, et reageerida paremini vaateava suuruse muudatustele.</td>
<td>Vormi sisu peab paremini reageerima, et kasutada optimaalselt brauseri või seadme saadaolevat kõrgust/laiust. Reageerimise saavutamine võib nõuda muudatusi vormi modelleerimise viisis.</td>
</tr>
<tr>
<td>Kasutage täiustatud vormi arendamise kogemuse saamiseks mustreid.</td>
<td>Vormi väljatöötamise lähtepunktidena AX 2012-s olid saadaval vormi laadil põhinevad vormimallid. Vormi laadi kontrollija, valikuline lisandmoodul, andis teavet selle kohta, mille poolest vorm vastavast mallist kõrvale kaldus.</td>
<td>Dynamics AX-i praeguses versioonis on võetud kasutusele vormimustrid. Vormimustrid kujutavad endast kombinatsioon vormimallidest ja vormi laadi kontrollijast, mis on arendamiseks omavahel tihedalt integreeritud. Mustrid on määratletud vormi tasandil (nagu AX 2012) täiendavate alammustritega, mis on nüüd rühma ja vahekaardi tasandil saadaval.</td>
<td>Mustreid järgivatel vormidel on palju eeliseid, sh järjepidevam kasutajaliides, lihtsam arendamine, hõlpsam vormi versioonitäienduse tee ja suurem kindlus vormi paigutuse reageerimises.</td>
</tr>
</tbody>
</table>

## <a name="help"></a>Spikker

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Protseduuride juhendava spikri (ülesande juhised) ja mõisteid kirjeldavad teemad saate avada, klõpsates jaotist <strong>Spikker</strong>.</td>
<td>AX 2012 spikrisüsteem osutab HTML-teemadele, mis on salvestatud kohalikku veebiserverisse. Kliendid ja partnerid saavad luua oma spikri.</td>
<td>Dynamics AX-i praeguse versiooni spikrisüsteemi kuvab tegevusjuhised, mis on salvestatud ja Microsoft Dynamicsi teenuse Lifecycle Services (LCS) BPM-i. Spikrisüsteem kuvab ka Microsofti dokumendisaid teemasid. Lisateavet vt <a href="help-overview.md" data-raw-source="[Help system](help-overview.md)">spikrisüsteemist</a> ja <a href="new-task-guides-available-february-2016.md" data-raw-source="[New task guides (February 2016)](new-task-guides-available-february-2016.md)">uutest tegevusjuhistest (veebruar 2016)</a>.</td>
<td>Ülesande juhised pakuvad juhendatud, interaktiivset kogemust, mis juhib teid läbi ülesande või äriprotsessi toimingute. Saate alla laadida ja kohandada Microsofti pakutavaid ülesande juhiseid. Teema pakub kiiremat ja paindlikumat viisi tootedokumentatsiooni loomiseks, edastamiseks ning värskendamiseks. Seetõttu aitab see tagada teile juurdepääsu uusimale tehnilisele teabele.</td>
</tr>
</tbody>
</table>

## <a name="human-capital-management"></a>Inimkapitali juhtimine

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate edastada klassi osalejatele kursuse lõpetamisel oskusi ja tunnistusi.</td>
<td>See on manuaalne protsess.</td>
<td>Kursuse lõppedes avaneb uus võimalus lisada osaleja andmetele uusi oskusi ja tunnistusi.</td>
<td>See võimaldab töötaja andmeid uuel ja tõhusal viisil värskendada.</td>
</tr>
<tr>
<td>Saate kiiresti töösuhet kontrollida.</td>
<td>See on manuaalne protsess.</td>
<td>Teie personaliosakond saab tööruumi või töötaja lehe abil kiiresti töösuhet kontrollida.</td>
<td>Teie personaliosakonnal pole enam vaja avada mitut lehte, et kontrollida töö alustamise kuupäeva, juhti, ametikohal töötatud kuid ja palgaandmeid.</td>
</tr>
<tr>
<td>Saate lasta töötajatel süsteemis andmeid vaadata, muuta ja kustutada.</td>
<td>See on võimalik, kuid piiratud vaatamise ja muutmise võimalustega.</td>
<td>See funktsioon on lubatud ja võimaldab töötajatel ning töövõtjatel vaadata suurt hulka isikuandmeid. Soovi korral saab töövoogu kasutada andmete loomisel, värskendamisel või kustutamisel.</td>
<td>See võimaldab töötajatel oma andmeid juhtida, kui on vaja aadressi või kontaktandmeid muuta, ametikohale kandideerida, küsitluses osaleda või pilti värskendada. Kui töövoog on aktiveeritud, saab kinnitaja teabe üle vaadata või selle saab automaatselt kinnitada, olenevalt teie äriprotsessidest.</td>
</tr>
<tr>
<td>Saate lasta juhtidel töötajate andmeid vaadata või muuta.</td>
<td>See on võimalik, kuid piiratud vaatamise ja muutmise võimalustega.</td>
<td>Olenevalt konfiguratsioonisätetest ja turbest saavad juhid töötajate andmeid vaadata või muuta.</td>
<td>See võimaldab juhtidel töötajate olulistele andmetele juurde pääseda, et nad saaksid teha paremaid otsuseid ressursiplaanimise, tulemuste ja töötaja arengu kohta.</td>
</tr>
<tr>
<td>Kasutage halduri iseteeninduse funktsiooni.</td>
<td>Pole saadaval</td>
<td>Juhid saavad nüüd esitada taotlusi uute palkamiste (töötajate ja alltöövõtjate), üleviimiste ja lõpetamiste (töösuhte lõpetamiste) kohta. Juhid võivad nõuda ka uut ametikohta, pikendada ametikohtade kestust või nõuda ametikoha muutmisi.</td>
<td>Need stsenaariumid olid varem saadaval ainult inimressurssidele. Nende stsenaariumide võimaldamine annab organisatsiooni juhtidele võimsad töövahendid. Õige ülevaatamise ja kinnitamise taseme tagamiseks võib lubada täiendavaid töövoogusid.</td>
</tr>
<tr>
<td>Pääsete juurde tasude töötlemise tulemustele.</td>
<td>Tulemused on saadaval ainult töötlemise ajal.</td>
<td>Tasu töötlemise tulemustele pääseb nüüd juurde igal ajal pärast protsessi käitamist.</td>
<td>See võimaldab suurepäraselt protsessi ja protsessi tulemusi auditeerida. See annab ka põhjaliku ülevaate andmetest enne töötaja kirjete uuendamist.</td>
</tr>
<tr>
<td>Pääsete juurde soodustuste töötlemise tulemustele.</td>
<td>Tulemused on saadaval ainult töötlemise ajal.</td>
<td>Soodustuste töötlemise tulemustele pääseb nüüd juurde igal ajal pärast protsessi käitamist.</td>
<td>See annab põhjaliku ülevaate andmetest, mida muudetakse soodustuse registreerimise ja kulude muutmisega.</td>
</tr>
<tr>
<td>Saate vaadata „Jõustumise kuupäeva” ajaskaala muudatusi.</td>
<td>Pole saadaval</td>
<td>See võrdlustööriist on saadaval töötajate, ametikohtade ja tööde kohta. See annab põhjaliku vaate ühe kirje versiooni muutmisest teiseks versiooniks.</td>
<td>See säästab aega, kui vaatate töötajate, ametikohtade ja tööde kirjetes aja jooksul toimunud muutusi. See võimaldab kirje kahte versiooni või kõiki aja jooksul sisestatud kirjeid kiiresti võrrelda.</td>
</tr>
<tr>
<td>Saate vaadata töötajaid ettevõtte järgi.</td>
<td>See on manuaalne protsess, mida tehakse filtreerimise kaudu.</td>
<td>Töötajate ja töövõtjate loendeid filtreeritakse automaatselt ettevõtte järgi, millesse olete sisse loginud.</td>
<td>See annab filtreeritud vaate sisselogitud ettevõttes töötavatest töötajatest. Kõigi töötajate ja töövõtjate filtreerimata vaate saamiseks on endiselt saadaval töötajate loend. Dynamics AX-i praeguses versioonis ei muuda süsteem ettevõtet loendist valitud töötaja alusel.</td>
</tr>
<tr>
<td>Saate kursusel osalejate loendit värskendada.</td>
<td>Pole saadaval</td>
<td>Kursusel osalejaid saab osalejate loendist eemaldada.</td>
<td>Sel viisil on lihtne ekslikult registreerunud kursusel osalejaid muuta.</td>
</tr>
<tr>
<td>Saate tasu sündmusi grupis hallata.</td>
<td>Pole saadaval</td>
<td>See funktsioon muudab töötajate tasu muutmise töötlemise sujuvamaks.</td>
<td>See pakub lihtsat ja sujuvat protsessi töötaja kirjete värskendamiseks tasu tööruumis ja seotud lehtedel.</td>
</tr>
</tbody>
</table>

## <a name="inventory-management"></a>Varude haldus

Uusi funktsioone ei ole lisatud.

## <a name="localization"></a>Lokaliseerimine

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate konfigureerida ja koostada elektroonilisi dokumente mitmesuguste riikide/regioonide seadusenõuete järgimiseks.</td>
<td>Elektroonilised dokumendid on püsiprogrammeeritud keelega X++ või XSLT-dokumendi teisendustena (Extensible Stylesheet Language Transformation, laiendatav vormingukeele teisendus). Vormingu korrigeerimine nõuab arendustegevusi. Juurdepääs andmetele ja vormingule pole eraldatud. Korrigeeritud kujul juurutamine nõuab uut Microsoft Dynamics AX-i kiirparanduse paketti, mis alistab olemasoleva vormingu. Iga vormingu kohandatud muudatused tuleb käsitsi teisaldada uue Microsoft Dynamics AX-i kiirparanduste paketi lähtekoodi.</td>
<td>Elektrooniline aruandlus (ER) on uus tööriist selliste elektrooniliste dokumentide konfigureerimiseks ja genereerimiseks, mis on mõeldud arendaja asemel ärikasutajale. ER-i abil saate seadistada andmemudeleid, mis on domeenipõhised ja mis on dokumendivormingute andmeallikatena Microsoft Dynamics AX-i andmebaasist sõltumatud. Ärikasutaja saab vorminguid nende domeenipõhiste andmemudelite põhjal konfigureerida (näiteks maksete, Intrastati aruannete või maksuaruannete puhul). Kasutaja konfigureerib vormingud, kasutades lihtsalt Excelile sarnanevaid visuaalseid tööriistu. ER toetab praegu elektrooniliste dokumentide koostamist teksti, XML-i ja Exceli vormingus. Neid dokumente saab koostada üheaegselt ja pakkida zip-failideks. Andmemudelid ja vormingud toetavad versioonimist. Vorminguversioonidel võivad olla kehtivusperioodid. Iga andmemudel või vorminguversioon talletatakse eraldi konfiguratsiooni ja jaotatakse partneritele ja klientidele LCS-i kaudu. Partnerid ja kliendid saavad kohandada Microsofti andmemudeleid ja vorminguid või luua enda omad. ER salvestab partneri ja kliendi konfiguratsioonimuudatused deltadena Microsofti konfiguratsioonidesse, mis lihtsustab täiendamist Microsofti konfiguratsioonide uuteks versioonideks. LCS-i abil saavad ka partnerid jagada oma andmemudelit ja vormingukonfiguratsioone teiste partnerite ja klientidega, kes saavad neid kohandada ja jagada. Delta kohandamist ja lihtsat versioonitäiendust toetatakse kogu kohandusahelas.</td>
<td>ER lihtsustab elektrooniliste dokumendivormingute loomist, haldamist ja täiendamist, et need vastaksid mitmesuguste riikide/regioonide seadusenõuetele. ER muudab elektrooniliste dokumendivormingute loomise või muutmise protsessi kiiremaks ja lihtsamaks. Neid muudatusi saavad teha arendajate asemel ärikasutajad. ER võimaldab partneritel ja klientidel kiiremini ja lihtsamalt vormingukohandusi uuteks Microsofti või muude partnerite välja antud vorminguversioonideks täiendada. ER annab Microsoftile ja partneritele ühe ühise viisi (LCS-i kaudu) elektrooniliste dokumendikonfiguratsioonide jaotamiseks teistele partneritele ja klientidele. ER hõlbustab ka partneritel ja klientidel elektroonilisi dokumendivorminguid konkreetsete ärivajaduste kohaselt kohandada, täiendada ja jaotada.</td>
</tr>
<tr>
<td>(MEX) Mehhiko regulatiivsete käibemaksuaruannete genereerimine.</td>
<td>Peate looma aruanded <strong>Müügi ja ostu käibemaks</strong>, kasutades realiseerimata käibemaksu funktsiooni nii, et kasutajad saaksid tuvastada oleku põhjal realiseeritud ja realiseerimata osadesse kuuluvad kanded.</td>
<td><strong>Müügi ja ostu käibemaksu</strong> aruandeid on muudetud ja nüüd arvestavad need tingimusliku käibemaksu funktsiooni realiseerimata ja realiseeritud käibemaksukoodide määratlemiseks ainult konkreetsete tasakaalustusperioodide abil.</td>
<td>Enne, kui kasutajad saavad neid aruandeid õigesti koostada, on vaja teha muudatusi käibemaksukoodide konfiguratsioonis. Nõutav on tingimusliku käibemaksu funktsioon ja kasutaja peab seadistama eraldi realiseeritud ja realiseerimata tasakaalustusperioodid seotud jaotisevaldkondades kannete tuvastamiseks.</td>
</tr>
<tr>
<td>(JPN) Jaapani põhivara kiirendatud kulumi deklaratsiooni dokumendi haldamine.</td>
<td>Pole saadaval</td>
<td>Oluline deklaratsiooni teave talletatakse paremaks haldamiseks tsentraalselt ühte dokumenti.</td>
<td>Dokumendi vastavus ja haldamise lihtsus aitavad auditite ja muude ülevaatuste käigus probleeme vähendada.</td>
</tr>
<tr>
<td>(JPN) Saate pangakonto JBA-märke kontrollida.</td>
<td>Pole saadaval</td>
<td>Saate kontrollida, et kana-nimeväljad sisaldaksid ainult JBA-pangavorminguga lubatud märke.</td>
<td>See aitab vähendada maksefaili genereerimise ajal kasutajate katkestusi sobimatute märkide tõttu.</td>
</tr>
<tr>
<td>(JPN) Jaapani põhivara vara sendierinevuse kompenseerimine rahandusaasta lõpus.</td>
<td>Pole saadaval</td>
<td>Lehel <strong>Põhivara parameetrid</strong> saate valida kompenseerimise rahandusperioodi või rahandusaasta lõpus.</td>
<td>See on kohalike tavade järgimiseks paindlikum võimalus.</td>
</tr>
<tr>
<td>(JPN) Saate koostada Jaapani ettevõtte maksudeklaratsiooni lisatud tabelite 16 seerias koondsummaga põhivara põhitüübi kaupa.</td>
<td>Pole saadaval</td>
<td>Saate otsustada põhivara väärtusmudelites põhitüübi järgi summeerida. Vaikimisi kasutatakse seda funktsiooni äsja loodud põhivara puhul.</td>
<td>Suurte ettevõtete puhul, millel on tuhandeid põhivarasid, vähendavad summeeritud aruanded oluliselt koostatava aruande mahtu.</td>
</tr>
<tr>
<td>(JPN) Saate alustada Jaapani põhivarade puhul erikulumi reservi eraldamist järgmisest rahandusaastast.</td>
<td>Pole saadaval</td>
<td>Sobiva erikulumi profiiliga põhivara väärtusmudelites saate valida eraldamise alustamise järgmisest rahandusperioodist või järgmisest rahandusaastast.</td>
<td>See on kohalike tavade järgimiseks paindlikum võimalus.</td>
</tr>
<tr>
<td>(JPN) Saate luua Jaapani tarbimismaksu aruande, mis sisaldab parandatud maksumäärasid.</td>
<td>Tarbimismaksu aruanne on saadaval maksumääraga 5 protsenti.</td>
<td>Tarbimismaksu aruanne sisaldab parandatud maksumäära osa (nt 8 protsenti).</td>
<td>Valitsus kuulutas selle paigutuse hiljuti välja.</td>
</tr>
<tr>
<td>(EL) ELi müüginimekirja ümardamise sätete konfigureerimine.</td>
<td>ELi müüginimekirja aruandluse ümardamissätted mitmesugustes riikides/regioonides on püsiprogrammeeritud keelega X++ või XSLT-dokumendi teisendustena (Extensible Stylesheet Language Transformation, laiendatav vormingukeele teisendus).</td>
<td>Väliskaubanduse parameetritele on lisatud ümardamise sätted. Saate konfigureerida ümardustäpsust, ümardusmeetodit, väljundi täpsust ja käitumist summade puhul, mis on ümardustäpsusest väiksemad.</td>
<td>See ühtlustab ja lihtsustab ELi müüginimekirja aruandluse konfiguratsiooni. Ümardamissätete korrigeerimine ei nõua enam arendaja pingutusi.</td>
</tr>
<tr>
<td>(EL) Pöördtasu rakendatavuse reeglite konfigureerimine.</td>
<td>Pöördtasu rakendatavuse reeglid on siseriikliku pöörmaksustamise stsenaariumi puhul püsiprogrammeeritud. Kohaldatavuse läve saab seadistada kaubagrupi kohta. Funktsioon on saadaval ainult Suurbritannias.</td>
<td>Saate konfigureerida pöörtasu rakendatavuse reegleid dokumenditüübi (ostu-/müügitellimus, hankija arve, vabas vormis arve jne) ja pöördtasu grupi kohta, mis ühendab kaupu, kaubagruppe ja ostu-/müügikategooriaid. Rakendatavuse reeglid on kehtivuskuupäevaga. Saate märkida pöördtasu rakendamiseks ka eraldi käibemaksukoode käibemaksugruppides. Müügiarve aruannet korrigeeritakse rakendatud pöördtasu üksikasjade kajastamiseks. See funktsiooni on saadaval kõigis Euroopa riikides/piirkondades.</td>
<td>See muudatus ühtlustab pöördtasu rakendatavuse reeglite konfiguratsiooni ja toetab siseriikliku pöördmaksustamise reeglite kohaldamist Euroopa riikides/piirkondades.</td>
</tr>
<tr>
<td>(DE) Saksamaa auditifaili loomine – GDPdUGoBD</td>
<td>Kasutajad saavad seadistada eksporditavaid finantsandmeid sisaldavate tabelite definitsiooni vormingusse, mida Saksamaa audiitorid ja ametiasutused aktsepteerivad.</td>
<td>Funktsioon on juurutatud elektroonilise aruandluse konfiguratsioonina. Funktsioon on saadaval Saksamaal ja Austrias.</td>
<td>See muudatus annab kasutajale palju rohkem võimalusi andmete vormindamiseks, teisendamiseks ja pakub ka kõiki eeliseid, mis tulenevad elektroonilise aruandluse konfiguratsiooni elutsükli haldamisest (nt lihtne konfiguratsiooni vahetamine, versioonid jne).</td>
</tr>
<tr>
<td>(FR) Aruanne Saldod grupi kokkuvõtete kontodega.</td>
<td>Saldod grupi kokkuvõtete kontodega on rakendatud SSRS-aruandena (LedgerAccountSum_FR).</td>
<td>Aruanne Saldod grupi kokkuvõtete kontodega on juurutatud Management Reporteri aruandena, mis on saadaval LCS-i varateegi lokaliseeritud finantsaruannete kaustas.</td>
<td>See võimaldab kasutajatel saada kasu kõigist kohandamise eelistest ja vabadustest finantsaruannete kasutamisel Management Reporteris.</td>
</tr>
<tr>
<td>(EL) Maksesoovitus, osalemismärkus ja maksete juhtimisaruanded.</td>
<td>Kõik need aruanded on juurutatud ja SSRS-aruanded.</td>
<td>Need aruanded on juurutatud Open XML-i mallidena kasutamiseks Microsoft Excelis.</td>
<td>Elektroonilised maksekonfiguratsioonid sisaldavad maksefaili vormingu seadistust ja malle. See võimaldab kasutajatel saada kasu kõigist aruande kohandamise eelistest ja vabadustest elektroonilise aruandluse kasutamisel.</td>
</tr>
<tr>
<td>(EL) Intrastati ümardamise sätete konfigureerimine.</td>
<td>Intrastati aruandluse ümardamissätted mitmesugustes riikides/regioonides on püsiprogrammeeritud keelega X++ või XSLT-dokumendi teisendustena (Extensible Stylesheet Language Transformation, laiendatav vormingukeele teisendus).</td>
<td>Väliskaubanduse parameetritele on lisatud ümardamise sätted. Saate konfigureerida ümardustäpsust, ümardusmeetodit, väljundi täpsust ja käitumist summade puhul, mis on ümardustäpsusest väiksemad.</td>
<td>See ühtlustab ja lihtsustab Intrastati aruandluse konfiguratsiooni. Ümardamissätete korrigeerimine ei nõua enam arendaja pingutusi.</td>
</tr>
<tr>
<td>(EL) Saate seadistada kategooriahierarhiates Intrastati kaubakoode.</td>
u<td>Intrastati kaubakoodid on eraldi nimekiri. Samas kui on olemas kategooriahierarhia tüüp Kaubakood, saab need kaubakoodid Retail HQ ja müügi kategooriates vaikeväärtustele seada.</td>
<td>Eraldi loend Intrastati kaubakoodidest ühendatakse tootehierarhiaga, mille tüüp on Kaubakood.</td>
<td>See ühendab müügidokumentides väljastatud toodetele ja kategooriatele kaubakoodide määramise lähenemise.</td>
</tr>
<tr>
<td>(EL) Saate registreerida Intrastatis koguse täiendavates ühikutes, kasutades ühiku teisendamise seadistust.</td>
<td>Intrastati kaubakoodil on tekstiväli täiendavate ühikute tähistamiseks ja kaardil<strong> Toode</strong> on väli täiendavate ühikute koguse näitamiseks kilogrammides.</td>
<td>Intrastati kaubakoodi täiendavad ühikud valitakse ühikute loendist. Täiendavate ühikute kogus arvutatakse ühiku teisendussätete kaudu.</td>
<td>See ühtlustab kandeühikutest täiendavateks ühikuteks ümberarvutamise lähenemise.</td>
</tr>
<tr>
<td>(EL) Määrake tarnerežiimile vaiketranspordiviis.</td>
<td>Pole saadaval</td>
<td>Tarnerežiimile lisatakse vaiketranspordiviisi väli.</td>
<td>See lihtsustab Intrastati aruandluse koostamist.</td>
</tr>
<tr>
<td>(EL) Saate märkida väljastatud toote Intrastati aruandesse mitte lisatavaks.</td>
<td>Pole saadaval</td>
<td>Väljastatud tootele lisatakse valik kauba väljajätmiseks Intrastati aruandlusest.</td>
<td>See lihtsustab Intrastati aruandluse koostamist.</td>
</tr>
</tbody>
</table>

## <a name="manufacturing"></a>Tootmine

| Mida saate teha? | Dynamics AX 2012 |
|------------------|------------------|
| Kontrollige materjali saadavust tootmistellimuste jaoks eraldi lehel, mis avaneb tööruumist **Tootmisosakonna haldus**. | Pole saadaval |
| Saate käivitada tootmistööd ja teatada nende edenemisest uue lehe **Töökaardi vahend** kaudu. | Vorm **Töö registreerimine** on mõeldud peamiselt suurte terminaliekraanide jaoks ja kasutajaliidesele pääseb tavaliselt juurde hiireklõpsudega. |

## <a name="master-planning-and-forecasting"></a>Koondplaneerimine ja eelarvestamine

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Hoiatage kasutajat, kui müügitellimus või tootmistellimus pole plaanitud kuupäevaks tarnimiseks valmis. | Koondplaneerimise loodud hoiatusi nimetatakse *tulevaste teadeteks*. *Tulevased* on kahe poole vaheline leping vara ostmiseks või müümiseks hinna eest, mis on täna kokku lepitud (*tulevane hind*), kuigi tarne ja maksmine toimuvad tulevikus (*tarnekuupäeval*). | *Tulevaste teated* ja *tulevaste kuupäevad* on nimetatud ümber *arvutatud hilinemisteks* ja *hilinemise kuupäevadeks*. | AX 2012-s kasutatud terminoloogia oli ebatäpne ja põhjustas valesid tõlkeid. |
| Saate kiirülevaateid koondplaneerimise tsükli olekust, pakilistest plaanitud tellimustest ja hilinemisi põhjustavatest plaanitud tellimustest. | Teave on saadaval, kuid see on hajutatud mitme vormi vahel. | Tööruum **Koondplaneerimine** annab kiiresti teavet selle kohta, millal viimane koondplaneerimise tsükkel lõppes, kas ilmnes tõrkeid, millised on pakilised plaanitud tellimused ja millised plaanitud tellimused põhjustavad hilinemisi. | Saate kasutada tööruumi antavat ülevaadet. Sobivad andmed on kokku pandud, juhendades koondplaneerimist ja aidates produktiivsust parandada. |
| Kasutage Excelit nõudluse prognooside värskendamiseks. | Pole saadaval | Saate kasutada sujuvat integratsiooni Exceliga, kui sisestate nõudluse prognoose, teete uuendusi ja kustutate nõudluse prognoose. | See aitab tõhusust ja produktiivsust suurendada. |
| Saate tulevast nõudlust hinnata ja luua varasemate kandeandmete põhjal nõudluse prognoose. | Rakenduses Microsoft Dynamics AX 2012 R3 kasutatakse nõudluse prognooside koostamiseks Microsoft SQL Serveri analüüsiteenuse prognoosimudeleid. | Saate prognoosida tulevast nõudlust, kasutades Microsoft Azure’i masinõppe pilveteenuse jõudu ja laiendatavust. Masinõppe prognoosimudeleid on kliendi vajaduste rahuldamiseks lihtne kasutada ja laiendada. Teenus valib parima sobiva mudeli ja pakub tulemuslikkuse võtmenäitajaid (KPI-sid), mida saab kasutada prognoosi täpsuse arvutamiseks. | Saate koostada masinõppe tehnikate abil täpsemaid prognoose. |
| Saate optimeerida tellimuse kuupäeva ja kogust, tuginedes seotud toimingute visuaalsele ülevaatele koondplaneerimise tsüklist. | Toimingute diagrammi ülevaade on saadaval, kuid kuvab kõik seotud toimingud. Kui toimingud rakendatakse, kaovad need kohe vaatest. | Toimingute diagramm annab parema ülevaate. See sisaldab valikuid, mis võimaldavad kuvada ainult rakendatud toimingud ja otseselt seotud toimingud. Kui toimingud rakendatakse, kuvatakse need tuhmina, kuid neid näidatakse siiski. Seega jääb ülevaade alles. Toimingute diagrammile lisatakse teavet andmete kuvamiseks ühel leheküljel. | Produktiivsuse täiustus on kasulik, kuna keskendutakse ainult asjakohastele tegevustele. |

## <a name="procurement-and-sourcing"></a>Hanked

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Kasutage tööruumi **Ostutellimuse ettevalmistamine** kiire ülevaate saamiseks koostatavate ostutellimuste olekust. | Ei toetata | Tööruum **Ostutellimuse ettevalmistamine** annab ülevaate tellimustest alates nende mustandina loomise ajast ning jälgib neid läbi töövoo heakskiitmise olekute kuni kinnitamiseni. | Ostuosakonna pole enam vaja otsida teavet mitmelt lehelt, vaid on võimalik toetuda tööruumi antavale ülevaatele. |
| Kasutage järeltegevuste käigus tööruumi **Ostutellimuste vastuvõtt ja järeltegevus** kiire ülevaate saamiseks ostutellimustest, mis on vastuvõtmise ootel. | Ei toetata | Tööruum **Ostutellimuste vastuvõtt ja järeltegevus** annab ülevaate kinnitatud ostutellimustest, millel on ootel sissetulekuid või lähetusi. Tööruum sisaldab loendit tähtaja ületanud sissetulekutest ja ootel sissetulekutest, mis aitab tarnijal neid proaktiivselt üle vaadata ja järeltegevusi teha. Tööruumis on loetletud ka ostutellimused, mis on laos saabunuks registreeritud, et aidata tagada sissetuleku sisestamine. Tagastatavad ostutellimused, mida pole veel teele pandud, on samuti ülevaatamiseks saadaval. | Ostuosakonnal on tööruumi pakutavast ülevaatest kasu. Sobivad andmed on kokku pandud, juhendades järeltegevusi ja aidates produktiivsust parandada. |
| Saate saata ostutellimusi kinnitamiseks Dynamics AX-i kliendis majutatavasse hankijaportaali. Lubage hankijal kinnitada või tagasi lükata. | Ei toetata | Hankijaportaali kasutajaliides võimaldab hankijatel ostutellimusi kinnitamiseks või tagasilükkamiseks vastu võtta. Samuti võimaldab see hankijal kõiki konto kinnitatud ostutellimusi üle vaadata. Ostuagent saab saata hankijale ostutellimuse, paludes kinnitust. Hankija peab olema Dynamics AX-is registreeritud Microsoft Azure Active Directory (Azure AD) kasutaja, hankija kontaktisik, ja tal peab olema spetsiaalne turberoll. | Teie ostuosakond saab kasu paberimajanduse ja ostutellimuste vastuste käsitsi jälgimise vähendamisest, kuna need andmed jooksevad otse süsteemi. Ühe tõe allika olemasolu vähendab kliendi ja hankija vahelisi arusaamatusi. |

## <a name="projects"></a>Projektid

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Saate töötajaid projektiressurssidena reserveerida. | Sarnaselt ressurssidele reserveeritakse projektidesse lisaks ressurssidele otse ka töötajaid. | Nüüd saab töötajate projektidesse ressurssidena reserveerimiseks kasutada töökeskuse tabelit, kus talletatakse tootmisressursse. | Projektide reserveerimisel tuleb reserveerida ainult ressursid. |

## <a name="retail-sales-marketing-and-customer-service"></a>Jaemüük, turundus ja klienditeenindus

### <a name="retail-hq"></a>Retail HQ

Microsoft Azure’is majutatav Retail HQ pakub veebikliendi kaudu kõigi kaubandustoimingute aspektide tsentraliseeritud juhtimist ja täielikku nähtavust.

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate teha turustustoiminguid.</td>
<td>Kasutajad peavad nende andmete haldamiseks mitut vormi kasutama.
<ul>
<li>Kategooriahaldus</li>
<li>Tootehaldus</li>
<li>Kanali toote atribuudid</li>
<li>Sortimendid</li>
<li>Tootekataloogi haldus</li>
<li>Komplektid</li>
<li>Hinnad &amp; allahindlused</li>
</ul></td>
<td>Tööruum <strong>Kategooria- ja tootehaldus</strong> võimaldab kasutada järgmisi funktsioone.
<ul>
<li>Sortimendi haldus.</li>
<li>Sortimendi elutsükli jälgimine.</li>
<li>Väljastatud toodete haldamine.</li>
</ul>
Tööruum <strong>Hindade ja allahindluste haldus</strong> võimaldab kasutada järgmisi funktsioone.
<ul>
<li>Antud kanali ja kategooria hinna ja allahindluse haldamine.</li>
<li>Kategooria hinnareegli haldamine.</li>
<li>Hinna ja allahindluse prioriteedid, mis võimaldavad määrate hinnagruppidele ja allahindlustele prioriteete, et saaksite juhtida nende rakendamise järjekorda.</li>
<li>Alluvuse ja kataloogi allahindluse haldamine.</li>
</ul>
Tööruum <strong>Kataloogihaldus</strong> võimaldab kasutada järgmisi funktsioone.
<ul>
<li>Aktiivsete kataloogide kokkuvõte.</li>
<li>Kataloogi elutsükli jälgimine ühes kohas.</li>
</ul></td>
<td><ul>
<li>Tööruumid parandavad töötajate tõhusust ja tööviljakust, lastes neil hallata tsentraalselt turustusrolliga seotud ülesandeid ja toiminguid.</li>
<li>Hinna ja allahindluse prioriteetide funktsioon annab klientidele suurema kontrolli hindade ja allahindluste kasutamise üle. See funktsioon võimaldab kasutada ka uusi stsenaariume, kus kaupluse kõrgemad hinnad alistavad standardhinnad.</li>
</ul></td>
</tr>
<tr>
<td>Jaemüügikanali juurutuste ja toimingute haldamine</td>
<td>Kasutajal peab olema juurdepääs mitmele vormile järgmiste toimingute tegemiseks.
<ul>
<li>Uute kanalite ja seotud üksuste loomine ja konfigureerimine.</li>
<li>Kaupluse igapäevaste tegevuste haldamine.</li>
<li>Jaemüügikannete töötlemine Microsoft Dynamics AX-is, jaemüügi väljavõtete koostamine ja Microsoft Dynamics AX-i varude ning finantsandmete uuendamine.</li>
</ul>
</td>
<td>Tööruum <strong>Kanali juurutamine</strong> võimaldab teha järgmist.
<ul>
<li>Uute kanalite ja seotud üksuste loomine.</li>
<li>Jaekaupluse konfigureerimise edenemise jälgimine.</li>
<li>Tehke vajalikud sammud ülesande täitmiseks või edastage teave ülesande täitmiseks.</li>
<li>Saate jälgida seadmete olekut ja programmi Retail Modern POS (MPOS) installifaili kauplustes otse valideerida ning alla laadida.</li>
<li>Pääsete kõigile seotu lehtedele.</li>
</ul>Tööruum 
<strong>Jaekaupluse haldus</strong> võimaldab teha järgmist.
<ul>
<li>Hallata töötajaid ja töötajate kassa (POS) õigusi.</li>
<li>Jälgida antud kaupluse või kaupluste grupi vahetuse olekut.</li>
<li>Valideerida otse ja laadida alla MPOS-i programmi installifaile kauplustes.</li>
<li>Printida aruandeid ja juurdepääsuga seotud lehti.</li>
</ul>Tööruum 
<strong>Jaekaupluse rahandus</strong> võimaldab teha järgmist.
<ul>
<li>Luua, arvutada ja sisestada antud kanali väljavõtteid.</li>
<li>Plaanida pakett-töid varude uuendamiseks ning väljavõtete arvutamiseks ja sisestamiseks.</li>
<li>Jälgida avatud väljavõtteid.</li>
<li>Jälgida antud kaupluse või kaupluste grupi vahetuse olekut.</li>
<li>Printida aruandeid ja pääseda kiiresti juurde kõigile seotud lehtedele.</li>
</ul></td>
<td>Tööruumid parandavad töötajate tõhusust ja tööviljakust, lastes neil hallata tsentraalselt enamikku nende kanali juurutamise, kaupluse halduse ja finantsandmetega seotud ülesandeid ja toiminguid.</td>
</tr>
<tr>
<td>Saate hallata jaemüügi IT-toiminguid.</td>
<td>Kasutaja peab kasutama mitut vormi.</td>
<td>Tööruum <strong>Retail IT</strong> võimaldab antud kanali puhul Commerce Data Exchange’i päringuid ühest kohast, et saaksite teha järgmist.
<ul>
<li>Seansse alla laadida.</li>
<li>Seansse üles laadida.</li>
<li>Jälgida nurjunud seansse ja neid uuesti käivitada või läbida.</li>
<li>Tulevasi töid vaadata või käitada.</li>
</ul></td>
<td>Tööruumid parandavad töötajate tõhusust ja tööviljakust, lastes neil hallata tsentraalselt jaemüügi IT-tegevustega seotud ülesandeid ja toiminguid.</td>
</tr>
<tr>
<td>Saate andmeüksuste abil andmeid importida/eksportida.</td>
<td>AX 2012 toetab valmis süsteemi Microsoft Dynamics Retail Management System (RMS) migreerimist andmete importimise/eksportimise raamistiku kaudu.</td>
<td>Jaemüügi andmeüksusi on laiendatud nii, et need toetaksid kõiki jaemüügiga seotud koond- ja viiteandmeid. Olemas on ka täiustatud andmeüksuste tugi kogu Dynamics AX-i lahenduse lõikes.</td>
<td>Andmeüksused võimaldavad klientidel andmeid metaandmete alusel importida ja eksportida. OData üksused võimaldavad klientidel integreerida Dynamics AX-i ka muude tootjate programmidega.</td>
</tr>
<tr>
<td>Saate teha intelligentset analüüsi, kasutades Dynamics Microsoft AX-i ja kassa kliendi äriteabe aruandeid.</td>
<td>Saadaval on üle 25 kontoriaruande ja viis kanalipoolset aruannet.</td>
<td>Saadaval on üle 30 kontoriaruande ja 10 kanalipoolset aruannet.</td>
<td>Need aruanded võimaldavad klientidel saada rohkem äriandmeid suundumuste prognoosimiseks, ülevaadete avamiseks ja pidevalt tippvõimsusel töötamiseks.</td>
</tr>
<tr>
<td>Saate analüüsida jaemüügikanali müügiandmeid, kasutades Power BI sisu „Jaemüügikanali näitajate jälgimine”.</td>
<td>Pole saadaval</td>
<td>Valige lehel PowerBI.com käsk <strong>Too andmed</strong> ja seejärel valige sisupakett <strong>Dynamics AX – jaemüügikanali näitajad</strong>. Sisestage oma Dynamics AX-i lõpp-punkti URL, et näha andmeid armatuurlaual.</td>
<td>3–4 hiireklõpsuga saavad organisatsioonid võtta kasutusele Power BI armatuurlaua, mis sisaldab olulisi finantsandmeid. Organisatsioon saab sisu isikupärastada. Peale selle saavad kasutajad manustada Power BI armatuurlaua paanid Dynamics AX-i isikupärastatud tööruumidesse, et saada analüüsiandmetest kiire ülevaate.</td>
</tr>
<tr>
<td>Tarbija lubade konfigureerimine.</td>
<td>Pole saadaval</td>
<td>Kliendid saavad valida, kas kassatoimingud on lõppkasutajatele kättesaadavad. Jaemüügiserver kasutab liidese Application Programming Interface (API) kutsete jaoks lubasid.</td>
<td>See võimaldab konfigureerida tarbija tasandi lubasid.</td>
</tr>
<tr>
<td>Saate hallata ja kinnitada üksuse konfiguratsioone.</td>
<td>Pole saadaval</td>
<td>Konfiguratsioonihalduri ja validaatori funktsioon võimaldab kasutada järgmisi funktsioone.
<ul>
<li>Hulgikonfiguratsiooni andmete üleslaadimine</li>
<li>Äriüksuse valideerimine</li>
</ul></td>
<td>See annab konfiguratsiooni alglaadimise võimaluse ja võimaldab valideerida konfiguratsiooni oleku ja terviklikkuse erinevaid konfiguratsioonielemente silmas pidades.</td>
</tr>
</tbody>
</table>

### <a name="retail-hardware-station"></a>Jaemüügi riistvarajaama valimine

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Saate lubada kassaseadmetel luua ühenduse välisseadmetega, nt printerite, kassasahtlite või makseseadmetega. | Kasutatavate seadmete määramiseks kasutatakse MPOS-i riistvaraprofiili. | Lisatud riistvaraprofiil toetab suuremat hulka mitmesugust riistvara ühest jaamast teiseni. Uus riistvarajaama profiil toetab kordumatut terminali ID-d iga riistvarajaama puhul, kui töödeldakse elektroonilise ülekande (EFT) kandeid. EFT tugi on ühendatud riistvarajaama, et vähendada MPOS-i seotust EFT maksete töötlemisega. | See tagab juurutamiseks suurema paindlikkuse. Samuti suurendab see turvalisust ja vähendab kokkupuudet krediitkaardiandmetega. |

### <a name="retail-server-and-data-management"></a>Jaemüügiserver ja andmehaldus

Jaemüügiserver ja andmehaldus võimaldavad tarbijatel ja ettevõtetel luua ühiskanali ostukogemuse veebi, kaupluse ja kõnekeskuse kanalite lõikes.

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Looge ühendus Commerce Runtime’i (CRT) andmebaasiga, mis salvestab kanali äriandmeid, kasutades CRT-teenuseid.</td>
<td>Toetatakse OData versiooni V3.</td>
<td>Toetatakse OData versiooni V4.</td>
<td>See aitab kliendil OData standarditega kursis püsida. Samuti loob see tugeva ühiskanali kogemuse, integreerides kaupluse, mobiilsete ja veebikanalite müügi.</td>
</tr>
<tr>
<td>Jaemüügiteenuste tugi majutatava teenusekogumina.</td>
<td>Jaemüügiserver ei toeta e-kaubanduse API-d.</td>
<td>E-kaubanduse API on nüüd jaemüügiserveri kaudu saadaval veebistsenaariumide toetamiseks.</td>
<td>See pakub majutatud ja skaleeritavaid e-kaubanduse teenuseid, mida saab kasutada muude osapoolte veebipoodidega.</td>
</tr>
<tr>
<td>Saate teisaldada andmeid Microsoft Dynamics AX-i kontori ja kanalite vahel, kasutades rakendust Commerce Data Exchange.</td>
<td>Commerce Data Exchange on süsteem, mis edastab andmeid Microsoft Dynamics AX-i ja jaemüügikanalite (nt veebipoed või traditsioonilised kauplused) vahel. Lisateavet vt teemast <a href="https://technet.microsoft.com/library/dn741440.aspx">Commerce Data Exchange [AX 2012]</a>.</td>
<td>On olemas funktsionaalne paarsus rakendusega Microsoft Dynamics AX 2012 CU8. Kuid arvestage järgmist.
<ul>
<li>Commerce Data Exchange on ümber korraldatud pilve jaoks.</li>
<li>Teenus Async kasutab otsest andmebaasi juurdepääsu kanali andmebaasile.</li>
<li>Commerce Data Exchange: reaalajas teenus majutatakse Microsoft Dynamics AX-i kohandatud teenusena.</li>
<li>MPOS haldab ühenduseta andmebaaside ja jaemüügiserveri vahelist sünkroonimist.</li>
</ul></td>
<td>Commerce Data Exchange on ümber korraldatud pilveplatvormi jaoks. See haldab jätkuvalt andmete edastamist Microsoft Dynamics AX-i ja jaemüügikanalite (nt veebipoed või traditsioonilised kauplused) vahel.</td>
</tr>
<tr>
<td>Saate toetada isehäälestuvat, poolintegreeritavat kanalitevahelist maksetöötlust, kasutades makse SDK-d.</td>
<td>AX 2012 pakub järgmisi funktsioone.
<ul>
<li>Kõigi kanalite tugi: kassa, e-kaubandus ja kõnekeskus.</li>
<li>Kaardi olemasolu ja mitteolemasolu tugi.</li>
<li>Makse kinnitamise leht.</li>
<li>Välisseadmete tugi LS5300 ja MX925 puhul jaemüügi SDK näidiskoodina.</li>
</ul></td>
<td>Dynamics AX-i praegune versioon toetab kõiki olemasolevaid Microsoft Dynamics AX 2012 krediit-/deebetkaardi funktsioone ja nelja uut täiustust.</td>
<td>See võimaldab kliendil töödelda maksete krediit-/deebetkaardi kandeid.</td>
</tr>
<tr>
<td>Saate aktiveerida seadmed Microsofti kontoga (Microsoft Azure Active Directory (Azure AD)).</td>
<td>Pole saadaval</td>
<td>Pakutakse järgmisi funktsioone.
<ul>
<li>Suurem turvalisus pilve Azure AD-põhise aktiveerimisega.</li>
<li>Suurem turvalisus lubade haldamiseks.</li>
<li>Täiustatud töökindlus, tõrkeotsing ja tõrketeadete edastamine aktiveerimise ajal</li>
<li>Lihtsustatud aktiveerimisega seotud IT-halduse ülesanded.</li>
<li>Uuendatud ohumudel ja kõrvaldatud turbeprobleemid.</li>
</ul></td>
<td>See pakub järgmisi eeliseid.
<ul>
<li>Turvet on tõhustatud Azure AD ja seadme loa/ID abil (RS-kutsed, mis kasutavad luba, kasutajapõhine rakenduse salvestamine).</li>
<li>Peatab MPOS-i loata kaugkasutuse (seadme kasutuks muutmise).</li>
<li>See jälgib MPOS-seadmeid PCI järgimise eesmärgil.</li>
<li>Vastendab füüsilised seadmed äriüksusega (registriga), kasutades seadme luba.</li>
<li>Lähtestab sätted tõrgeteta MPOS-funktsiooni tagamiseks (numbriseeriad ja riistvaraprofiilid) MPOS-i esimese puutepunktina.</li>
<li>Edastab peakontorist seadme teabe.</li>
</ul></td>
</tr>
<tr>
<td>Saate hallata rikast meediasisu autorluseks ja edastamiseks meediumigalerii kaudu.</td>
<td>Pole saadaval</td>
<td><ul>
<li>Saate toetada piltide üleslaadimist ning samuti vaadata, hallata ja kustutada meediumigaleriist nii väljaspool majutatud kui ka jaemüügis majutatud piltide puhul.</li>
<li>Saate toetada piltide üleslaadimist ja vaatamist üksuse lehtedelt (<strong>Tooted</strong>, <strong>Kataloogid</strong> jne), sidudes galeriist pildi ja laadides pildi töölaualt üles.</li>
<li>Saate optimeerida pilte pisipildi, kohandatud suuruse ja originaalina.</li>
<li>Saate üksusi hulgi linkida, kasutades hulgiseostamiseks malli ja taustatöid.</li>
<li>Microsoft Exceliga integreerimine kirjutab üle nimemääramisreeglite ja eelmääratud teede atribuudigrupi piirangu.</li>
<li>Saate toetada ühenduseta pilte ja kaitsta pilte isiku tuvastamist võimaldava teabe (PII) sisu puhul, nt jaemüügis majutatud töötajate ja klientide pildid.</li>
</ul></td>
<td><ul>
<li>See lahendab väljaspool majutatud piltidega seotud murekohad, et saaksite vältida edasi-tagasi liikumist ja hallata üksusi selle asemel ühest kohast.</li>
<li>See tagab üleslaaditud ja väljaspool majutatud piltide võimsa sisuhalduse meediumigalerii kaudu ning võimaldab kasutada filtreerimist piltide leidmiseks.</li>
<li>See võimaldab teil luua hõlpsasti hulgiseoseid väliselt majutatud piltide ja üksuste (nt toodete ja kataloogide) vahel.</li>
<li>See toetab piltide jaemüügis majutatud salvestusruumi ja Exceli integratsiooni hõlpsaks uuendamiseks.</li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="rich-clientele-experience"></a>Rikkaliku klientuuri kogemus

Jaemüük pakub kõikjal, alati ja igal seadmel kõikehõlmavat mobiilset kogemust. See funktsioon võimaldab täiustatud ostu- ja kauplusekogemusi kõigi kanalite lõikes.

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate tooteid otsida, sirvida või skannida, lisada neid ostukorvi, nõustuda maksega ja maksta, kasutades MPOS-il intuitiivset, puutesõbralikku, rikkalikku ja kõikehõlmavat kasutajakogemust.</td>
<td>AX 2012 võimaldab kasutada järgmisi funktsioone.
<ul>
<li>Müük, tagastused ja tühistamised.</li>
<li>Klienditellimuste loomine, muutmine ja pealevõtmine.</li>
<li>Vahetuse ja kassa toimingud.</li>
<li>Tellimuste komplekteerimine ja vastuvõtmine ning inventuuri tegemine.</li>
<li>Kaupluse aruannete vaatamine.</li>
</ul></td>
<td>Pakutakse funktsionaalset paarsust AX 2012 MPOS-iga. See hõlmab järgmisi funktsioone.
<ul>
<li>Kliendi otsing kaupluste/kanalite lõikes.</li>
<li>Võimalus koostada klientide tellimusi reaalajas teenust avamata.</li>
<li>Täiustatud seadme aktiveerimise töövood, oleku- ja tõrketeated.</li>
<li>Laiendatavuse täiustused nagu sisestamiseelsed päästikud ja tegevuse tugi kohandamise parandamiseks.</li>
</ul></td>
<td>Müügipersonal saab töödelda müügikandeid ja klienditellimusi ning teha igapäevaseid toiminguid ja hallata varusid, kasutades mobiilseid seadmeid kõikjal kaupluses.</td>
</tr>
<tr>
<td>Saate avada kassa veebirakendusena pilve kassa kaudu.</td>
<td>Pole saadaval</td>
<td>Pakutakse funktsionaalset paarsust MPOS-iga. See hõlmab järgmisi funktsioone.
<ul>
<li>Seadme aktiveerimine AAD abil</li>
<li>Hästi reageeriv paigutus</li>
<li>Edge’i, Internet Exploreri ja Chrome’i brauserite tugi.</li>
</ul></td>
<td>See pakub veebirakenduse kassat, mille funktsioonid ühilduvad MPOS-iga ja mida saab kasutada platvormide ja brauserite lõikes ilma juurutuskuluta.</td>
</tr>
<tr>
<td>Saate integreerida sisuhalduse süsteemidega, et luua ühiskanali e-kaubanduse veebisait.</td>
<td>Toetatakse Microsoft SharePointi ja muude tootjate fassaade.</td>
<td>Pakutakse e-kaubanduse platvormi, mis toetab muude osapoolte fassaade. Platvorm sisaldab järgmisi funktsioone.
<ul>
<li>Rikkalik tarbija API.</li>
<li>Autentimise integreerimine igasuguse muust osapoolest avatud ID pakkujaga.</li>
<li>Makse integreerimine.</li>
</ul></td>
<td>Klientidel on nüüd võimalik paindlikult oma valitud sisuhaldussüsteemi kasutada.</td>
</tr>
<tr>
<td>Pöörduge klientide poole meilitellimuse kataloogidega ja kiirendage toiminguid tellimuse kiire sisestamise ning müügi ja täitmise käigus abistamisega, kasutades kõnekeskust.</td>
<td><ul>
<li>Kõnekeskuse kanal</li>
<li>Postimüügikorralduste kataloogid</li>
<li>Kiire tellimuse sisestamine ja abistamisega müük</li>
<li>Täiustatud tellimuse täitmine</li>
<li>Klienditeenindus</li>
<li>Integreeritud hinnad ja kampaaniad/allahindlused</li>
</ul></td>
<td>Saadaval on funktsiooni paarsus AX 2012 kõnekeskuse lahendusega, mille erandiks on hinna alistamised.</td>
<td>Kõnekeskused on jaemüügikanali tüüp, mis võimaldab töötajatel võtta klientide tellimusi vastu telefoni teel ja koostada müügitellimusi.</td>
</tr>
</tbody>
</table>

### <a name="commerce-essentials"></a>Commerce’i põhitõed

Jaemüügile ja kaubandusele keskendunud konfiguratsioonisuvand aitab jaemüügipõhiseid juurutusi kiirendada.

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Kasutage armatuurlauda Commerce’i põhitõed. | Saadaval on ala leht menüüelementide linkidega. | Armatuurlaual Commerce’i põhitõed on lingid sagedaste toimingute juurde, sh lingid tööruumide, Power BI veebi juhtelemendi, lemmikute, hiljutiste lehtede ja praeguste tööüksuste juurde. | Täiustatud armatuurlaud muudab töötajad tõhusamaks ja annab igasugusele jaemüügipõhisele ülesandele paindliku lähtepunkti. |
| Kasutage konto muudatustele juurdepääsemiseks andmeüksusi. | Konto muudatused eksporditakse failisüsteemi kausta. | Konto muudatustele pääseb juurde andmeüksuste kaudu. | See funktsioon tagab andmete liigutamisel erinevate süsteemide vahel suurema paindlikkuse. Seda funktsiooni saab täiustada ka OData rakenduste kaudu. |
| Kasutage pilve kassat ja MPOS-i. | Valmislahendusena toetatakse ainult rakendust Enterprise POS (EPOS). | MPOS ja pilve kassa asendavad EPOS-i kliendi. Vaikimisi on Commerce’i põhiüksuste hulka lisatud ka e-kaubanduse kanal. | See funktsioon võimaldab ulatuslikumat valmiskanalite tuge kiiresti juurutatavate kassa klientidega. |
| Kaheastmelise arhitektuuri kasutuselevõtmine ja säilitamine. | Andmete importimise/eksportimise raamistik võimaldab liigutada andmeid AX 2012 ja muude tootjate süsteemide vahel. | Andmeüksused on loodud kaheastmelise arhitektuuri toe täiustamiseks. | Andmeüksused ja OData rakendused pakuvad abstraktsioonikihti, et muuta kaheastmeliste stsenaariumide rakendamine ja haldamine lihtsamaks. |
| Saate vorme lihtsustada. | Kasutajaliidese lihtsustamiseks on vajalik kohandatud kood. | Vormi ja menüü laiendused lihtsustavad standardiseeritud kasutajaliidest. | See funktsioon annab kiirema ja lihtsama viisi vorme jaemüüja vajaduste põhjal peenhäälestada. |

### <a name="pos-task-recorder"></a>Kassa ülesande salvestaja

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate luua ja jagada rakenduse Modern POS ülesande juhiseid ja dokumente.</td>
<td>Pole saadaval</td>
<td>MPOS-i ülesande salvestaja toetab järgmisi funktsioone.
<ul>
<li>Ülesande salvestuste loomine mitmesuguste MPOS-is tehtavate toimingute puhul.</li>
<li>Etappe ja ekraanipilte sisaldava dokumendi loomine ja selle seostamine äriprotsessi mudeli sõlmega.</li>
</ul></td>
<td>Partnerid ja sõltumatud tarkvaramüüjad (ISV-d) saavad MPOS-e kohandada ja edastada toetavaid dokumente oma kasutajate koolitamiseks.</td>
</tr>
</tbody>
</table>

### <a name="extensibility"></a>Laiendatavus

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Toetatakse laiendatavaid ja hõlpsasti juurutatavaid jaemüügikomponente HQ, kõnekeskuse, e-kaubanduse ja kassa lõikes.</td>
<td>Komponente saab laiendada jaemüügi SDK abil. Ühtegi pakendamise ja juurutamine võimalust ei toetata.</td>
<td>Laiendamissüsteeme on mitmesuguste komponentide lõikes parandatud, et need toetaksid koodi isoleerimist ja kasutuskõlblikkust. Siin on mõned lisatud funktsioonid.
<ul>
<li>Töövoog, tegevus ja toiming.</li>
<li>Eel- ja järelpäästikud, mis võimaldavad hõlpsasti töövoogu laiendada.</li>
<li>Rakenduse ja toimingu päästikud.</li>
</ul>
Peale selle on saadaval raamistik, mis võimaldab teil luua ja pakkida neid komponente MSBuildi abil ning seejärel teie kohandust teenuste Microsoft Dynamics Lifecycle Services (LCS) kaudu sujuvalt juurutada.</td>
<td>Jaemüüjatel on väga konkreetsed vertikaallahendustel ja tegevuspiirkondadel põhinevad nõuded. Pakkudes lihtsalt laiendatav platvormi, võimaldame kasutust vertikaallahenduste ja turgude lõikes. Kuna jaemüügil on väga mitmeks osaks jaotatud arhitektuur, parandab sujuva juurutamise võimalus oluliselt produktiivsust.</td>
</tr>
</tbody>
</table>

### <a name="lifecycle-management"></a>Elutsükli haldus

Lifecycle Services (LCS) pakub teenuste kogumit, mida partnerid ja kliendid saavad kasutada süsteemi elutsükli haldamiseks registreerumisest kuni igapäevaste toiminguteni.

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate hallata programmi pilve juurutusteenuste kaudu.</td>
<td>Pole saadaval</td>
<td>Pilves saab juurutada järgmisi topoloogiad.
<ul>
<li>Jaemüügi ühe kastiga proovitopoloogia.</li>
<li>Jaemüügi mitme kastiga hea kättesaadavusega topoloogia.</li>
<li>Arendaja topoloogia jaemüügi SDK-ga.</li>
</ul>
Iseteeninduse installimise kaudu on olemas parem „vähese puudutusega” klientkomponent.
<ul>
<li>Retail Modern POS.</li>
<li>Retail Hardware Station.</li>
<li>Kohandatud pakettide üleslaadimise ja levitamise tugi iseteeninduse installimise kaudu.</li>
</ul></td>
<td>Pilve juurutusteenused annavad järgmisi eeliseid.
<ul>
<li>Oluliselt väiksem pingutus juurutamisel ja HQ jaemüügikomponentide väiksem keerukus.</li>
<li>Juurutamine Microsoft Azure’i avalikku pilve.</li>
<li>Poes olevate komponentide täiustatud iseteeninduse kaudu installimine konfiguratsiooni lihtsamaks ja selgemaks muutmiseks</li>
</ul></td>
</tr>
<tr>
<td>Saate jälgida süsteemi seisundit ja diagnoosida tõrkeid ning probleeme.</td>
<td>See funktsioon nõuab <a href="https://www.microsoft.com/download/details.aspx?id=42636">System Center 2012 Management Packi rakendusele Microsoft Dynamics AX 2012 R3 CU8 Retail</a>.</td>
<td>Jaemüügi komponentide jälgimine ja diagnostika on nüüd saadaval LCS-i armatuurlaual <strong>Tegevusülevaated</strong>.</td>
<td>Armatuurlaud <strong>Tegevusülevaated</strong> on pilvepõhine jälgimisportaal, mis asendab vajaduse laadida alla System Center Operations Manageri (SCOM) infrastruktuur.</td>
</tr>
<tr>
<td>Saate iseteeninduse abil luua, konfigureerida, laadida alla ja installida jaemüügi riistvarajaama ja seadmed.</td>
<td>Installipakkijat ja ettevõtteportaali kasutades saab kasutaja kõiki konkreetses arvutis vajalikke komponente automaatselt installida ja konfigureerida, tuginedes määratletud topoloogiale.</td>
<td>Kuna installipakkijaid on ainult kaks (üks MPOS-i kliendile ja teine jaemüügi riistvarajaama komponendile), on iseteenindus vähendanud töö hulka, mis on vajalik igal tasandil nende klientkomponentide installimiseks.</td>
<td>Iseteeninduse eesmärk on vähendada nõudeid ja muuta installimine kasutaja jaoks lihtsamaks.</td>
</tr>
</tbody>
</table>

## <a name="sales"></a>Müük

<table>
<thead>
<tr>
<th>Mida saate teha?</th>
<th>Dynamics AX 2012</th>
<th>Dynamics AX 7.0</th>
<th>Miks on see oluline?</th>
</tr>
</thead>
<tbody>
<tr>
<td>Saate kiirülevaate tarnevõimalustest, kui klientidele tellimusi lubate.</td>
<td>Kui toote saadavusel on piiranguid ja kliendi soovitud tarnekuupäeva ei saa vähemalt ühe toote puhul täita, muutub tellimuse lubamise ülesanne väljakutseks. Alternatiivide leidmiseks, mis võiksid kohandada saadavust ja tarneaja probleeme nii, et kliendi soovitud kuupäeva on võimalik täita, või pakkuda klientidele tarnelahendust, millega nad saavad nõustuda ja mida usaldada, võib töötlejal olla vaja avada mitu vormi, millest igaühes on ainult vajaliku teabe alamkogum. Täpsemalt: ühel vormil kuvatakse laokogus laoalade lõikes, teisel vormil kuvatakse laokogus kontsernisiseses sättes, kolmandal vormil saab kasutaja arvutada varaseima saadavuskuupäeva ühe laoala/variandi kohta korraga ja neljandal vormil on tarnetellimused. Seetõttu ei saa kasutajad olla kindlad, et nad on arvestanud kõiki asjakohaseid võimalusi, mitte valinud lihtsalt käepärase, kuid mitte optimaalse lahenduse. Samuti ei tunne kasutajad, et nende töö on tulemuslik, kuna tellimuse lubamise voos on mitmeid katkestusi, kui nad mitmeid lehti avavad ja sulgevad ning ülevaateid ja suvandeid kombineerivad.</td>
<td>Olemasolevate tarnekuupäeva arvutamise algoritmide põhjal pakub leht <strong>Tarnealternatiivid </strong>tellimuse lubamiseks uut kasutajakogemust.
<ul>
<li>See konsolideerib olulise teabe mitmelt vormilt ühte ruumi.</li>
<li>See pakub valmis alternatiivseid tarnepakette, näiteks kombinatsiooni tegevuskoha / ladustamine / variandi / transpordirežiimi kombinatsioonina, mis põhineb kiireimal tarnekriteeriumil (varaseim saadavuskuupäev), mille kasutaja saab valida.</li>
<li>See võimaldab kasutajal valida simulatsiooniliidesest variante ja kanda neid müügitellimuse reale üle.</li>
</ul></td>
<td>Ettevõtted, mis soovivad pakkuda kvaliteetset klienditeenindust, kasutades varude optimeerimise strateegiat, peavad suutma lubada tellimusi usaldusväärselt ja konkurentsivõimeliselt. Ka nende klientide äritegevus nõuab toodete õigeaegset kättesaadavust. Ülesandeleht <strong>Tarnealternatiivid</strong> muudab tellimuse lubamise ülesande kiiremaks, lihtsamaks ja süsteemsemaks, tuvastades ja soovitades parimaid alternatiivseid tellimuse tarnekuupäevi ühes interaktiivses kohas.</td>
</tr>
</tbody>
</table>

## <a name="service-management"></a>Teenuste halduse

Uusi funktsioone ei ole lisatud.

## <a name="transportation-management"></a>Transpordihaldus

Uusi funktsioone ei ole lisatud.

## <a name="travel-and-expense"></a>Reisimine ja kulud

Uusi funktsioone ei ole lisatud.

## <a name="warehouse-management"></a>Laohaldus

| Mida saate teha? | Dynamics AX 2012 | Dynamics AX 7.0 | Miks on see oluline? |
|------------------|------------------|-----------------|------------------------|
| Saate lao mobiilsete seadmete portaali alla laadida, installida ja konfigureerida. | Saate laadida, installida ja konfigureerida portaali Microsoft Dynamics AX-i installimisprotsessi käigus standardse seadistuse kaudu. See on mõeldud ise toimivaks asutusesiseseks juurutamiseks ja konfigureerimiseks. | Autonoomse installiprogrammi saate laadida alla menüüelemendi kaudu moodulis Laohaldus. See on mõeldud ise toimivaks asutusesiseseks juurutamiseks ja konfigureerimiseks. | Kui seadistate mobiilse seadme funktsiooni, tuleb lao mobiilsete seadmete portaal kohalikult installida ja konfigureerida ning luua ühendus Dynamics AX-iga pilves. |

## <a name="additional-resources"></a>Lisaressursid

[Mis on uut või muudetud Finance and Operationsi avalehel](whats-new-changed.md)

[Uued tegevusjuhised (veebruar 2016)](new-task-guides-available-february-2016.md)
