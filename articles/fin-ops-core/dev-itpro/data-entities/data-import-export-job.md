---
title: Andmeimpordi ja -ekspordi tööde ülevaade
description: Kasutage andmeimpordi ja -ekspordi tööde jaoks andmehalduse tööruumi.
author: peakerbl
ms.date: 08/26/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a03f8fd0fa05a1400c69a2da8867dee135ad06a1
ms.sourcegitcommit: 7bcaf00a3ae7e7794d55356085e46f65a6109176
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/26/2022
ms.locfileid: "9357587"
---
# <a name="data-import-and-export-jobs-overview"></a>Andmete importimis- ja eksportimistööde ülevaade

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Andmete impordi- ja eksporditööde loomiseks ning haldamiseks kasutage tööruumi **Andmehaldus**. Vaikimisi loob andmeimpordi ja -ekspordi protsess igale sihtandmebaasi üksusele koondamistabeli. Koondamistabelid võimaldavad andmeid enne teisaldamist kontrollida, puhastada või teisendada.

> [!NOTE]
> See artikkel eeldab, et olete andmeüksustega [tutvunud](data-entities.md).

## <a name="data-importexport-process"></a>Andmete importimis-/eksportimisprotsess
Siin on toimingud andmete importimiseks või eksportimiseks.

1. Looge impordi- või eksporditöö, kus tuleb teha järgmised toimingud.

    - Määratlege projekti kategooria.
    - Näidake ära imporditavad või eksporditavad üksused.
    - Määrake töö andmevorming.
    - Järjestage üksused nii, et neid töödeldaks loogiliste rühmadena ja mõistlikus järjekorras.
    - Määrale, kas kasutada koondamistabeleid.

2. Kontrollige, kas lähte- ja sihtandmed on õigesti vastendatud.
3. Kontrollige impordi- või eksporditöö turvalisust.
4. Käivitage impordi- või eksporditöö.
5. Kontrollige, et töö toimus õigesti, vaadates üle töö ajaloo.
6. Puhastage koondamistabelid.

Selle artikli ülejäänud jaotised annavad rohkem üksikasju protsessi iga sammu kohta.

> [!NOTE]
> Andmete importimise/eksportimise vormi värskendamiseks ja uusima edenemise kuvamiseks kasutage vormi värskendamise ikooni. Brauseritasemel värskendamine pole soovitatav, kuna see katkestab kõik impordi- või eksporditööd, mida ei käitata partiidena.

## <a name="create-an-import-or-export-job"></a>Impordi- või eksporditöö loomine
Andmete impordi- või eksporditöö saab käitada ühe korra või palju kordi.

### <a name="define-the-project-category"></a>Projekti kategooria määratlemine
Soovitame võtta aega, et valida impordi- või eksporditööle sobiv projektikategooria. Projektikategooriate abil saate seotud töid hallata.

### <a name="identify-the-entities-to-import-or-export"></a>Imporditavate või eksporditavate üksuste tähistamine
Saate lisada impordi- või eksporditööle konkreetseid üksusi või valida rakendamiseks malli. Mallid täidavad töö üksuste loendiga. Valik **Rakenda mall** on saadaval, kui olete tööle nime andnud ja selle salvestanud.

### <a name="set-the-data-format-for-the-job"></a>Töö andmevormingu määramine
Kui valite üksuse, peate valima eksporditavate või imporditavate andmete vormingu. Vorminguid saab määratleda paani **Andmeallikate seadistus** kaudu. Lähteandmete vorming on **tüübi**, **failivormingu**, **reaeraldaja** ja **veerueraldaja** kombinatsioon. On ka muid atribuute, kuid need on kõige olulisemad. Järgmises tabelis on toodud kehtivad kombinatsioonid.

| Failivorming            | Rea-/veerueraldaja                       | XML-i laad                 |
|------------------------|--------------------------------------------|---------------------------|
| Excel                  | Excel                                      | \-Pole-                     |
| XML                    | \-Pole-                                      | XML-element XML-atribuut |
| Eraldatud, fikseeritud laius | Koma, semikoolon, vahekaart, vertikaalriba, koolon | \-Pole-                     |

> [!NOTE]
> Oluline on valida õige väärtus , veerueraldaja ja teksti täpifikaatori jaoks, kui failivormingu suvand on **reaeraldaja**, **veerueraldaja**, ja **teksti täpifikaatori** jaoks kui **Faili vormaat** väärtus on seatud väärtusele **Eraldatud**. Kontrollige, et teie andmed ei sisaldaks eraldajana või täpindina kasutatavat märki, kuna see võib importimise ja eksportimise ajal põhjustada tõrkeid.

> [!NOTE]
> XML-põhiste failivormingute puhul kasutage kindlasti ainult õigusmärke. Lisateavet kehtivate märkide kohta vt XML [1.0 kehtivast märgist](https://www.w3.org/TR/2006/REC-xml-20060816/Overview.html#charsets/). XML 1.0 ei luba juhtmärke peale vahekaartide, tagastuste ja rea söötmete. Lubamatute märkide näited on nurksulud, curly sulgud ja kaldkriipsud. 

Andmete importimiseks või eksportimiseks kasutage kindla koodilehe asemel Unicode’i. See aitab anda kõige ühtsemaid tulemusi ja eemaldada andmehalduse tööd nurjumise tõttu, sest need sisaldavad Unicode’i märke. Süsteemi määratletud lähteandmete vormingutes, mis kasutavad Unicode’i vorminguid, **on lähtenimes Unicode’i** vormingus. Unicode-vormingu valite vahekaardil Regional settings (Piirkonnasätted) koodilehena Unicode’i kodeerimise **ANSI** **koodilehe**. Valige Unicode’i jaoks üks järgmistest koodilehtedest:

| Koodileht | Kuvatav nimi                |
|-----------|-----------------------------|
| 1200      | Unicode                     |
| 12000     | Unicode (UTF-32)            |
| 12001     | Unicode (UTF-32 Big-Endian) |
| 1201      | Unicode (Big-Endian)        |
| 65000     | Unicode (UTF-7)             |
| 65001     | Unicode (UTF-8)             |

Lisateavet koodilehtede kohta vt Koodilehe [ID-dest](/windows/win32/intl/code-page-identifiers/).

### <a name="sequence-the-entities"></a>Üksuste järjestamine
Üksusi saab järjestada andmemallis või impordi- ja eksporditöödes. Kui käivitate mitut andmeüksust sisaldava töö, peate veenduma, et andmeüksused oleksid õiges järjestuses. Üksused järjestatakse peamiselt nii, et saaksite käsitleda funktsionaalseid sõltuvusi üksuste vahel. Kui üksustel pole ühtegi funktsionaalset sõltuvust, saab need plaanida paralleelseks impordiks või ekspordiks. 

#### <a name="execution-units-levels-and-sequences"></a>Käivitamise ühikud, tasemed ja järjestused
Üksuse käivitamise ühik, tase käivitamise ühikus ja järjekord aitavad juhtida andmete eksportimise või importimise järjekorda.

- Erinevate käivitamise ühikute üksusi töödeldakse paralleelselt.
- Igas käivitamise ühikus töödeldakse üksusi paralleelselt, kui neil on sama tase.
- Igal tasemel töödeldakse üksusi nende järjekorranumbri alusel sellel tasemel.
- Kui üks tase on töödeldud, töödeldakse järgmine tase.

#### <a name="resequencing"></a>Ümberjärjestamine
Üksusi võib olla vaja ümber järjestada järgmistes olukordades.

- Kui kõigi muudatuste jaoks kasutatakse ainult ühte andmetööd, võite kasutada ümberjärjestamise valikuid terve töö läbiviimise aja optimeerimiseks. Nendel juhtudel võite kasutada käivitamise ühikut mooduli tähistamiseks, taset mooduli funktsiooniala tähistamiseks ja järjekorda üksuse tähistamiseks. Selle lähenemisega saate töötada moodulite lõikes paralleelselt, kuid mooduli sees ikka järjekorras. Tagamaks, et paralleelsed toimingud õnnestuksid, tuleb arvestada kõiki sõltuvusi.
- Kui kasutatakse mitut andmetööd (näiteks ühte tööd iga mooduli jaoks), võite optimaalseks läbiviimiseks kasutada järjestust, mis mõjutab üksuste taset ja järjekorda.
- Kui sõltuvusi polegi, võite maksimaalseks optimeerimiseks järjestada üksused erinevatel käivitamise ühikutel.

Menüü **Ümberjärjestamine** on saadaval, kui valitud on mitu üksust. Ümber saab järjestada käivitamise ühiku, taseme või järjekorravalikute alusel. Saate määrata vahemiku valitud üksuste ümberjärjestamiseks. Igale üksusele valitud ühikut, taset ja/või järjekorranumbrit muudetakse määratud vahemiku võrra.

#### <a name="sorting"></a>Sortimine
Valikut **Sortimisalus:** saab kasutada üksuste loendi vaatamiseks järjekorras.

### <a name="truncating"></a>Kärpimine
Saate projektide importimisel enne importimist üksuste kirjeid kärpida. See on kasulik, kui kirjeid on vaja importida tühjadesse tabelitesse. Vaikimisi on see säte välja lülitatud.

## <a name="validate-that-the-source-data-and-target-data-are-mapped-correctly"></a>Kontrollimine, kas lähte- ja sihtandmed on õigesti vastendatud
Vastendamine on funktsioon, mida rakendatakse nii impordi- kui ka eksporditööde puhul.

- Imporditöö kontekstis kirjeldab vastendus, millistest lähtefaili veergudest saavad koondamistabeli veerud. Seetõttu saab süsteem määratleda, millised lähtefaili veeruandmed tuleb kopeerida millisesse koondamistabeli veergu.
- Eksporditöö kontekstis kirjeldab vastendus, millistest koondamistabeli (st allika) veergudest saavad sihtfaili veerud.

Kui koondamistabeli ja faili veergude nimed ühtivad, loob süsteem nimede põhjal automaatselt vastenduse. Kuid kui nimed erinevad, ei vastendata veerge automaatselt. Sellistel juhtudel tuleb teha vastendamine, tehes valiku **Kuva kaart** andmetöö üksusel.

Vastendamisvaateid on kaks: **Vastendamise visualiseering**, mis on vaikevaade, ja **Vastendamise üksikasjad**. Punane tärn (\*) tähistab üksuse kohustuslikke välju. Need väljad tuleb vastendada, enne kui saate üksusega töötada. Teiste väljade vastendusi saab üksusega töötades soovi kohaselt tühistada. Välja vastenduse tühistamiseks valige väli veerust **Üksus** või veerust **Allikas** ja valige siis **Kustuta valik**. Valige **Salvesta** muudatuste salvestamiseks ja sulgege siis leht projekti juurde naasmiseks. Sama protsessi abil saab redigeerida välja vastendust lähtetabelist koondamistabelisse pärast importimist.

Lehel saab luua vastenduse, valides **Allika vastendamise loomine**. Loodud vastendus toimib nagu automaatne vastendus. Seega tuleb vastendamata väljad käsitsi vastendada.

![Andmetüüpide vastendamine.](./media/dixf-map.png)

## <a name="verify-the-security-for-your-import-or-export-job"></a>Impordi- või eksporditöö turvalisuse kontrollimine
Juurdepääsu tööruumile **Andmehaldus** saab piirata, et mitte-administraatorist kasutajad pääseksid juurde ainult konkreetsetele andmetöödele. Juurdepääs andmetööle tähendab täielikku juurdepääsu selle töö läbiviimise ajaloole ja juurdepääsu koondamistabelitele. Seetõttu tuleb veenduda, et andmetöö loomisel oleksid paigas sobivad juurdepääsu kontrollimismehhanismid.

### <a name="secure-a-job-by-roles-and-users"></a>Töö kaitsmine rollide ja kasutajatega
Menüü **Rakendatavad rollid** abil saate piirata töö ühe või mitme turberolliga. Ainult nende rollidega kasutajad pääsevad tööle juurde.

Samuti saab töö teha kättesaadavaks ainult konkreetsetele kasutajatele. Kui töö turve põhineb kasutajatel, mitte rollidel, on kontroll suurem, kui ühele rollile on määratud mitu kasutajat.

### <a name="secure-a-job-by-legal-entity"></a>Töö turve juriidilise isiku alusel
Andmetööd on olemuselt globaalsed. Seetõttu, kui juriidilises isikus loodi andmetöö ja seda kasutati seal, on see töö süsteemi teistes juriidilistes isikutes näha. Mõnes rakenduse stsenaariumis võib see vaikekäitumine eelistatud olla. Näiteks organisatsioonis, kus arveid imporditakse andmeüksuste abil, võib olla tsentraalne arveid töötlev töörühm, mis vastutab kõigi organisatsiooni divisjonide arvetel olevate vigade eest. Selles stsenaariumis on abiks, kui tsentraalne arveid töötlev töörühm pääseb juurde kõigi juriidiliste isikute arvete imporditöödele. Seetõttu vastab vaikekäitumine juriidilise isiku vaatepunktist vajadustele.

Kuid organisatsioon võib soovida, et arvete töötlemise töörühmad oleksid juriidilise isiku põhised. Sel juhul peaks juriidilise isiku töörühmal olema juurdepääs ainult oma juriidilise isiku arve imporditööle. Selle nõude täitmiseks võite konfigureerida juriidilise isiku põhise juurdepääsukontrolli andmetöödele, kasutades andmetöös menüüd **Kohaldatavad juriidilised isikud**. Pärast konfigureerimist näevad kasutajad ainult töid, mis on saadaval selles juriidilises isikus, kuhu nad parajasti on sisse logitud. Teise juriidilise isiku tööde vaatamiseks peavad kasutajad minema sellesse juriidilisse isikusse.

Töö saab kaitsta korraga rollide, kasutajate ja juriidiliste isikute kaudu.

## <a name="run-the-import-or-export-job"></a>Impordi- või eksporditöö käivitamine
Töö saab käivitada ühe korra, valides pärast töö määratlemist nupu **Impordi** või **Ekspordi**. Korduva töö seadistamiseks valige **Korduva andmetöö loomine**.

> [!NOTE]
> Importimis- või eksportimistööd saab käivitada, kui valite nupu **Impordi** või **Ekspordi**. See ajastab ainult üks kord käitatava pakett-töö. Töö ei pruugi kohe käivituda, kui partii teenus on partii teenuse koorma tõttu ahendatud. Töid saab käivitada ka sünkroonselt, kui valite nupu **Impordi kohe** või **Ekspordi kohe**. See käivitab töö kohe ja on kasulik siis, kui pakett ahendamise tõttu kohe ei käivitu. Tööde käivitamine on võimalik ajastada ka hilisemaks. Seda saab teha, kui valite suvandi **Käivita partiina**. Paketiressursid kuuluvad ahendamisele, seega pakett-töö ei tarvitse kohe käivituda. Partii kasutamine on soovitatav valik, sest see aitab ka suurte andmehulkade korral, mis on vaja importida või eksportida. Pakett-töid saab planeerida käivituma kindlate paketigruppide korral, mis koormuse ühtlustamise seisukohast võimaldab suuremat kontrolli.

## <a name="validate-that-the-job-ran-as-expected"></a>Kontrollimine, et töö toimus õigesti
Töö ajalugu on tõrkeotsinguks ja uurimiseks saadaval nii impordi- kui ka eksporditööde puhul. Varasemad töötsüklid on korraldatud ajavahemike alusel.

![Töö ajaloo vahemikud.](./media/dixf-job-history.md.png)

Iga töötsükli puhul kuvatakse järgmised andmed.

- Käivitamise üksikasjad
- Käivituslogi

Käivitamise üksikasjad näitavad iga töös töödeldud andmeüksuse olekut. Seetõttu leiate kiiresti järgmise teabe.

- Milliseid üksusi töödeldi
- Üksuse puhul – mitu kirjet töödeldi edukalt ja mitu ebaõnnestus
- Iga üksuse koondamiskirjed

Koondamisandmed saab laadida eksporditööde puhul alla failina või impordi- ja eksporditööde puhul paketina.

Käivitamise üksikasjadest saab avada ka käivituslogi.

## <a name="parallel-imports"></a>Paralleelne importimine
Andmete importimise kiirendamiseks saab lubada faili importimise paralleelse töötlemise, kui üksus toetab paralleelset importimist. Üksuse paralleelse importimise konfigureerimiseks tuleb järgida järgmisi samme.

1. Minge jaotisse **Süsteemihaldus \> Tööruumid \> Andmehaldus**.
2. Valige jaotises **Import/eksport** paan **Raamistiku parameetrid**, et avada leht **Andmete importimise/eksportimise raamistiku parameetrid**.
3. Valige vahekaardil **Üksuse sätted** suvand **Konfigureeri üksuse käivitamise parameetrid**, et avada leht **Üksuse importimise käivitamise parameetrid**.
4. Üksuse paralleelse importimise konfigureerimiseks määrake järgmised väljad.

    - Valige üksus väljal **Üksus**.
    - Sisestage imporditavate kirjete piirarv väljale **Imporditavate kirjete piirarv**. See määratleb kirjete arvu, mida lõim töötlema hakkab. Kui failis on 10 000 kirjet, siis tähendab kirjete arv 2500 ja ülesannete arv 4, et iga lõim töötleb 2500 kirjet.
    - Sisestage importimisülesannete arv väljale **Importimisülesannete arv**. See ei tohi ületada jaotises **Süsteemihaldus \>Serveri konfiguratsioon** pakktöötluseks eraldatud maksimaalset pakktöötluslõimede arvu.

## <a name="job-history-clean-up"></a>Tööde ajaloo tühjendamine 
Tööajaloo puhastamise funktsiooni tuleb andmehaldustöös kasutada käivitusajaloo perioodilise puhastuse planeerimiseks. See funktsioon asendab eelmise koondamistabeli puhastamise funktsiooni, mis on nüüd aegunud. Puhastamise käigus puhastatakse järgmised tabelid.

-   Kõik koondamistabelid

-   DMFSTAGINGVALIDATIONLOG

-   DMFSTAGINGEXECUTIONERRORS

-   DMFSTAGINGLOGDETAIL

-   (DMFSTAGINGLOG)

-   DMFDEFINITIONGROUPEXECUTIONHISTORY

-   DMFEXECUTION

-   DMFDEFINITIONGROUPEXECUTION

Funktsioon **Käivitusajaloo puhastamine** peab olema funktsioonide halduses lubatud ja seejärel pääseb sellele ligi kohast **Andmehaldus \> Tööde ajaloo puhastamine**.

### <a name="scheduling-parameters"></a>Parameetrite planeerimine

Puhastamise protsessi planeerimisel tuleb täpsustada puhastuse kriteeriumite järgmised parameetrid.

-   **Ajaloo säilitamise päevade arv** – seda sätet kasutatakse säilitatava käivitusajaloo hulga kontrollimiseks. Väljal määratud päevade arv. Kui puhastustöö on ajastatud korduva pakett-tööna, siis see säte tegutseb nagu pidevalt teisaldatav aken, jättes alati määratud päevade arvu puutumata kui ülejäänud kustutatakse. Vaikeväärtus on 7.

-   **Töö täitmiseks minevate tundide arv** – sõltuvalt puhastatavad ajaloo kogusest võib puhastustöö täitmisaeg varieeruda mõnest minutist kuni mõne tunnini. See parameeter peab olema seatud tundide arvule, mis töö täitmiseks kulub. Pärast seda, kui puhastamise töö on määratud arv tunde töötanud, töö väljub ja jätkab puhastamist järgmine kord, mil see kordumise graafiku põhjal käitatakse.

    Maksimaalse käivitusaja saab määrata, sätestades maksimumpiirangu tundide arvule, mille jooksul töö peab selle sätte abil käivitama. Puhastamise loogika läbib ühe töö käivituse ID korraga kronoloogiliselt korraldatud jadas, millest seotud tööajaloo vanim puhastatakse esimesena. See lõpetab uute käivituse ID-de valimise puhastamiseks, kui järelejäänud täitmise kestus on määratus kestuse viimase 10% sees. Mõnel juhul eeldatakse, et puhastamise töö kestab kauem kui määratud maksimaalne aeg. See sõltub suurel määral praeguse käivituse ID-ga kustutatavate kirjete arvust, mis käivitati enne 10% künnise saavutamist. Alustatud puhastamine tuleb lõpule viia, et tagada andmete terviklikkus, mis tähendab, et puhastamine jätkub, vaatamata määratud piirmäärangu ületamisele. Kui see on lõpule jõudnud, uusi käivituse ID-sid pole valitud ja puhastamise töö viiakse lõpule. Järelejäänud täitmise ajalugu, mida ei puhastata piisava täitmisaja puudumise tõttu, võetakse tööle järgmisel korral, kui puhastamine on sätestatud. Selle sätte vaikeväärtus ja miinimumväärtus on seatud 2 tunniks.

-   **Korduvpartii** – puhastamise tööd saab käitada ühekordse käsitsi käivitusena või seda saab ajastada ka korduva partii käivitamise jaoks. Partiid saab ajastada, kasutades seadistusi **Käivita taustal**, mis on standardne partiikomplekt.

> [!NOTE]
> Kui vahetabelite kirjeid täielikult ei puhastata, veenduge, et puhastamise töö oleks plaanitud käivituma korduvalt. Nagu eespool selgitatud, siis mis tahes puhastamise käivitamisel töö puhastab ainult nii palju käivitamise ID-sid, nagu on ettenähtud maksimaalsete tundide jooksul võimalik. Mis tahes allesjäänud vahekirjete puhastamise jätkamiseks peab töö olema ajastatud töötama perioodiliselt.

## <a name="job-history-clean-up-and-archival"></a>Tööajaloo puhastamine ja arhiivimine 
Tööde ajaloo puhastamise ja arhiveerimise funktsioon asendab puhastamise funktsioonide varasemad versioonid. Selles jaotises selgitatakse neid uusi võimalusi.

Üks põhilistest puhastamise funktsiooni muudatustest on ajaloo puhastamiseks süsteemi pakett-töö kasutamine. Süsteemi pakett-töö kasutamine võimaldab finantside ja toimingute rakendustel puhastada pakett-töö automaatselt ja käivituda niipea, kui süsteem on valmis. Pakett-tööd ei pea enam käsitsi planeerima. Selle vaikimisi käivitamise režiimis käivitub pakett-töö iga tund alates keskööl ja säilitab viimase seitsme päeva käivitamise ajaloo. Likvideeritud ajalugu arhiveeritakse tulevikus toomiseks. Alates versioonist 10.0.20 on see funktsioon alati sees.

Puhastustoimingu protsessi teine muudatus on likvideeritud käivitamise ajaloo arhiveerimine. Puhastamise töö arhiveerib kustutatud kirjed bloobimällu, mida DIXF kasutab regulaarsete integratsioonide jaoks. Arhiveeritud fail on DIXF-i paketi vormingus ja see on bloobimälus 7 päeva jooksul saadaval, mille jooksul saab selle alla laadida. Arhiivitud faili vaikimisi säilimisaega 7 päeva saab muuta parameetrites maksimaalselt 90 päevaks.

### <a name="changing-the-default-settings"></a>Vaikesätete muutmine
See funktsioon on praegu eelvaates ja see tuleb selgesõnaliselt sisse lülitada, lubades eelväljaande DMFEnableExecutionHistoryCleanupSystemJob. Ajastamise puhastamise funktsiooni tuleb samuti funktsiooni halduses sisse lülitada.

Arhiveeritud faili säilitamisaja vaikesätte muutmiseks minge dokumendihalduse tööruumi ja valige **Tööajaloo puhastamine**. Määrake suvand **Paketi bloobimälus talletamise päevade arv** väärtusele vahemikus 7 kuni 90 (kaasa arvatud). See jõustub arhiivides, mis luuakse pärast selle muudatuse tegemist.

### <a name="downloading-the-archived-package"></a>Arhiveeritud paketi allalaadimine
See funktsioon on praegu eelvaates ja see tuleb selgesõnaliselt sisse lülitada, lubades eelväljaande DMFEnableExecutionHistoryCleanupSystemJob. Ajastamise puhastamise funktsiooni tuleb samuti funktsiooni halduses sisse lülitada.

Arhiveeritud käivitamise ajaloo allalaadimiseks minge dokumendihalduse tööruumi ja valige **Tööajaloo puhastamine**. Valige suvand **Paketi varundamise ajalugu**, et avada ajaloo vorm. Sellel vormil kuvatakse kõigi arhiveeritud pakettide loend. Arhiivi saab valida ja alla laadida, valides suvandi **Allalaadimise pakett**. Allalaaditud pakett on DIXF-i paketi vormingus ja sisaldab järgmisi faile.

-   Üksuse koondtabeli fail
-   DMFDEFINITIONGROUPEXECUTION
-   DMFDEFINITIONGROUPEXECUTIONHISTORY
-   DMFEXECUTION
-   DMFSTAGINGEXECUTIONERRORS
-   (DMFSTAGINGLOG)
-   DMFSTAGINGLOGDETAILS
-   DMFSTAGINGVALIDATIONLOG



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

