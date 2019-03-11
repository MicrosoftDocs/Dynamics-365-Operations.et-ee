---
title: Elektrooniline sõnumside
description: Selles teemas antakse elektroonilise sõnumside ülevaade ja seadistusteave rakenduses Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357929"
---
# <a name="electronic-messaging"></a>Elektronsõnumid

[!include [banner](../includes/banner.md)]

Selles teemas antakse elektroonilise sõnumside ülevaade ja seadistusteave rakenduses Microsoft Dynamics 365 for Finance and Operations.

Hiljuti kehtestasid erinevate riikide ja piirkondade valitsused ja seadusandlikud asutused üle kogu maailma aruandlusnõuded ettevõtetele, kes on nendes riikides või piirkondades registreeritud. Nende nõuete eesmärk on hankida nendelt ettevõtetelt elektroonilises vormingus andmeid, otse süsteemist, kus neid arvutatakse, hoiustatakse ja töödeldakse.

Elektroonilise sõnumside funktsionaalsus rakenduses Finance and Operations toetab erinevaid protsesse elektrooniliseks koostalitluseks rakenduse Finance and Operations ning süsteemide vahel, mida valitsused ja seadusandlikud asutused pakuvad ametliku teabe aruandluseks, esitamiseks ja saamiseks.

Elektroonilise sõnumside funktsionaalsus on integreeritud **elektroonilise aruandluse** (ER) mooduliga. Seetõttu saate elektronsõnumite jaoks seadistada ER-vormingud. Lisateabe saamiseks vt [Elektrooniline aruandlus (ER)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektrooniline sõnumside põhineb järgmistel üksustel:

- **Elektronsõnum** – aruanne või deklaratsioon, mis tuleb esitada ja/või edastada ettevõtte siseselt. Näiteks, aruanne, mis saadetakse maksuametile.
- **Elektronsõnumi üksused** – kirjed, mis tuleb kaasata esitatavasse sõnumisse.
- **Elektronsõnumi töötlemine** – seotud või mitteseotud tegevuste ahel, mis tuleb käivitada vajalike andmete kogumiseks, aruannete loomiseks, andmete talletamiseks Microsoft Azure’i bloobimälus, aruannete edastamiseks väljastpoolt süsteemi, vastuste saamiseks väljastpoolt süsteemi ning andmebaasi uuendamiseks, tuginedes saadud teabele.

Järgmine joonis näitab elektroonilise sõnumside andmevoogu.

![Elektroonilise sõnumside andmevoog](media/electronic-messaging-data-flow.png)

Elektronsõnumite funktsioon toetab järgmisi stsenaariume:

- Sõnumite loomine ja aruannete koostamine, mis põhinevad erinevat tüüpi seotud eksportimise ER-vormingutel: Microsoft Excell, XML, JavaScript Object Notation (JSON), PDF, tekst ja Microsoft Word.
- Sõnumite, mis põhinevad teabel, mida taotleti ja hangiti asutuselt seotud importimise ER-vormingu kaudu, automaatne loomine ja töötlemine.
- Teabe kogumine ja töötlemine andmeallikast (Finance and Operationsi tabel) sõnumiüksustena.
- Täiendava teabe talletamine ja erinevate väärtuste hindamine, kutsudes eraldi määratletud täidetavad klassid seoses sõnumite või sõnumiüksustega.
- Teabe koondamine, mis on kogutud sõnumiüksustes, selle teabe tükeldamine sõnumite järgi ja aruannete loomine, mis on seotud eksporditavate ER-vormingutega.
- Loodud aruannete edastamine veebiteenusele, kasutades turbeteavet, mis on talletatud rakendusse Azure Key Vault.
- Vastuse saamine veebiteenuselt, vastuse tõlgendamine ja andmete uuendamine rakenduses Finance and Operations, nagu vajalik.
- Loodud aruannete talletamine ja ülevaatamine.
- Kogu logiteabe talletamine ja ülevaatamine, mis on seotud tegevustega, mis käivitatakse sõnumi või sõnumiüksuse jaoks.
- Töötlemise kontrollimine erinevate sõnumi ja sõnumiüksuse olekutega.

## <a name="set-up-electronic-messaging"></a>Elektroonilise sõnumside seadistamine

Elektroonilise sõnumside abil saate hallata erinevaid elektroonilise aruandluse protsesse erinevate dokumenditüüpide jaoks. Mõnes keerukamas stsenaariumis seadistatakse elektrooniline sõnumside mitme sõnumi oleku, sõnumiüksuse oleku, tegevuse, lisavälja ja täidetava klassi kombinatsioonina. Nende stsenaariumide jaoks on importimiseks saadaval andmeüksuste paketid. Kui te kasutate neid andmeüksuse pakette, peate need importima juriidilisse isikusse, kasutades andmehalduse tööriista. Lisateavet andmehalduse tööriista kasutamise kohta vt jaotisest [Andmehaldus](../../dev-itpro/data-entities/data-entities-data-packages.md).

Kui te ei impordi andmeüksuse paketti, saate elektronsõnumite funktsiooni seadistada käsitsi. Sel juhul peate seadistama järgmised elemendid: 

- [Numbriseeriad](#number-sequences)
- [Sõnumiüksuste tüübid ja olekud](#message-item-types-and-statuses)
- [Sõnumite olekud](#message-statuses)
- [Lisaväljad](#additional-fields)
- [Täidetava klassi sätted](#executable-class-settings)
- [Kirjete asustamise tegevused](#populate-records-actions)
- [Veebiteenuse sätted](#web-service-settings)
- [Sõnumi töötlemise tegevused](#message-processing-actions)
- [Elektronsõnumi töötlemine](#electronic-message-processing)

Järgmised jaotised annavad iga elemendi kohta lisateavet.

### <a name="number-sequences"></a>Numbriseeriad

Saate seadistada numbriseeriad nii sõnumite kui ka sõnumiüksuste jaoks. Numbriseeriaid kasutatakse sõnumite ja sõnumiüksuste automaatseks nummerdamiseks ja määratud numbreid kasutatakse süsteemis sõnumite ja sõnumiüksuste ainuidentifikaatoritena. Saate elektroonilise sõnumside jaoks numbriseeriad seadistada lehel **Pearaamatu parameetrid** (**Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**).

### <a name="message-item-types-and-statuses"></a>Sõnumiüksuste tüübid ja olekud

Sõnumiüksuste tüübid tuvastavad kirjete tüübid, mida kasutatakse elektronsõnumites. Saate sõnumiüksuste tüübid seadistada lehel **Sõnumiüksuste tüübid** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste tüübid**).

Sõnumiüksuste tüübid tuvastavad olekud, mis rakenduvad sõnumiüksustele teie seadistataval töötlemisel. Saate sõnumiüksuste tüübid seadistada lehel **Sõnumiüksuste olekud** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste olekud**).

### <a name="message-statuses"></a>Sõnumite olekud

Saate seadistada sõnumite olekud, mis peaksid sõnumite töötlemisel kättesaadavad olema. Saate sõnumite olekud seadistada lehel **Sõnumite olekud** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumite olekud**).

### <a name="additional-fields"></a>Lisaväljad

Elektronsõnumite funktsioon võimaldab teil asustada kirjeid kandetabelist. Sel viisil saate kirjed aruandluseks ette valmistada ja seejärel need esitada. Mõnikord pole kandetabelis piisavalt teavet kirje esitamiseks aruande nõuete kohaselt. Saate täita kogu teabe, mis tuleb kirje kohta esitada, seadistades lisaväljad. Lisaväljad saab seostada nii sõnumite kui ka sõnumiüksustega. Saate seadistada lisaväljad lehel **Lisaväljad** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Lisaväljad**).

Järgmises tabelis kirjeldatakse lehe **Lisaväljad** välju.

| Väli                | Kirjeldus |
|----------------------|-------------|
| Välja nimi           | Saate sisestada protsessiga seotud sõnumiüksuste täiendava atribuudi nime. See nimi kuvatakse kasutajaliideses, kui töötate protsessiga. Seda saab kasutada ka protsessiga seotud ER-i konfiguratsioonides. |
| Kirjeldus          | Saate sisestada protsessiga seotud sõnumiüksuste täiendava atribuudi kirjelduse. |
| Välja väärtus          | Saate sisestada välja väärtuse, mida kasutada aruandluse ajal seoses sõnumiüksusega. |
| Välja kirjeldus    | Saate sisestada välja väärtuse kirjelduse, mida kasutada aruandluse ajal seoses sõnumiüksusega. |
| Konto tüüp         | Mõned lisaväljade väärtused võivad olla piiratud kindlate kontotüüpidega. Valige üks järgmistest väärtustest: **Kõik**, **Klient** või **Hankija**. |
| Konto kood         | Kui valisite väljal **Konto tüüp** väärtuse **Klient** või **Hankija**, saate täiendavalt piirata välja väärtuste kasutamist kindla grupi või tabeliga. |
| Konto/grupi number | Kui valisite väljal **Konto tüüp** väärtuse **Klient** või **Hankija** ja sisestasite väljale **Konto kood** grupi või tabeli, saate sellele väljale sisestada kindla grupi või vastaspoole. |
| Jõustunud            | Saate määrata kuupäeva, mil väärtust tuleks arvestama hakata. |
| Aegumine           | Saate määrata kuupäeva, mil väärtuse arvestamine tuleks lõpetada. |

### <a name="executable-class-settings"></a>Täidetava klassi sätted

Täidetav klass on X++ meetod või klass, mida elektronsõnumite töötlemine saab seoses tegevusega kutsuda, kui protsessi jaoks on vajalik hindamine.

Saate täidetava klassi käsitsi seadistada lehel **Täidetava klassi sätted** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Täidetava klassi sätted**). Looge rida ja määrake järgmised väljad.

| Väli                 | Kirjeldus |
|-----------------------|-------------|
| Täidetav klass      | Saate sisestada nime, mida kasutatakse, kui seadistatakse sõnumi töötlemise tegevust, millega seoses seda klassi kutsutakse. |
| Kirjeldus           | Saate sisestada täidetava klassi kirjelduse. |
| Täidetava klassi nimi | Saate valida X++ täidetava klassi. |
| Käivitamise tase       | See väli määratakse automaatselt, sest väärtus peab valitud täidetava klassi jaoks olema eelmääratletud. See väli piirab taset, millel seotud hindamine käivitatakse. |
| Klassi kirjeldus     | See väli määratakse automaatselt, sest väärtus peab valitud täidetava klassi jaoks olema eelmääratletud. |

### <a name="populate-records-actions"></a>Kirjete asustamise tegevused

Saate kasutada kirjete asustamise tegevusi, et seadistada tegevusi, mis lisavad kirjed sõnumiüksuste tabelisse, et neid saaks lisada elektronsõnumile. Näiteks, kui teie elektronsõnum peab teatama kliendiarveid, peate seadistama tegevuse **Kirjete asustamine**, mis on seotud tabelis **Kliendiarvete tööleht** (väljal**Andmeallikas**). Saate seadistada kirjete asustamise tegevused lehel **Kirjete asustamise tegevus** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Kirjete asustamise tegevused**). Looge uus kirje iga tegevuse jaoks, mis peaks lisama kirjeid tabelisse, ja määrake järgmised väljad.

| Väli       | Kirjeldus                                                               |
|-------------|---------------------------------------------------------------------------|
| Nimi        | Saate sisestada nime tegevusele, mis asustab teie protsessis kirjed.       |
| Kirjeldus | Saate sisestada kirjelduse tegevusele, mis asustab teie protsessis kirjed. |

Kiirkaardil **Andmeallikate seadistus** lisage rida iga andmeallika jaoks, mida protsessis kasutatakse, ja määrake järgmised väljad.

| Väli                  | Kirjeldus |
|------------------------|-------------|
| Nimi                   | Saate andmeallikale sisestada nime. |
| Sõnumiüksuse tüüp      | Saate valida sõnumiüksuse tüübi, mida tuleb kasutada, kui andmeallika jaoks luuakse kirjeid. |
| Konto tüüp           | Saate valida konto tüübi, mis tuleb seostada andmeallika kirjetega. |
| Peatabeli nimi      | Saate rakenduses Finance and Operations valida tabeli, mis peab olema andmeallikas. |
| Dokumendi numbriväli  | Saate valida välja, millelt tuleks valitud tabelis võtta dokumendi number. |
| Dokumendi kuupäevaväli    | Saate valida välja, millelt tuleks valitud tabelis võtta dokumendi kuupäev. |
| Dokumendi kontoväli | Saate valida välja, millelt tuleks valitud tabelis võtta dokumendi konto. |
| Kasutaja päring             | Kui see märkeruut on valitud, saate seadistada päringu, valides ruudustiku kohal suvandi **Redigeeri päringut**. Vastasel juhul asustatakse kõik kirjed andmeallikast. |

### <a name="web-service-settings"></a>Veebiteenuse sätted

Saate veebiteenuse sätteid kasutada otsese andmeedastuse seadistamiseks veebiteenusele. Veebiteenuse sätted saate seadistada lehel **Veebiteenuse sätted** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebiteenuse sätted**).

Järgmises tabelis kirjeldatakse lehe **Veebiteenuse sätted** välju.

| Väli                   | Kirjeldus |
|-------------------------|-------------|
| Veebiteenus             | Saate sisestada veebiteenuse nime. |
| Kirjeldus             | Saate sisestada veebiteenuse kirjelduse. |
| Interneti-aadress        | Saate sisestada veebiteenuse Interneti-aadressi. |
| Tunnistus             | Saate valida eelnevalt seadistatud võtmehoidla serdi. |
| Vastuse tüüp – XML | Määrake selle suvandi väärtuseks **Jah**, kui vastuse tüüp on XML. |
| Päringu meetod          | Saate määrata päringu meetodi. HTTP määrab päringu meetodite komplekti, mis näitavad toimingut, mis tuleb antud ressursiga teha. Meetod võib olla **HANGI**, **POSTITA** või muu HTTP meetod. |
| Päringu päised         | Saate määrata päringu päised. Päringu päis on HTTP-päis, mida saab kasutada HTTP-päringus ja see pole sõnumi sisuga seotud. |
| Aktsepteeri kodeering         | Saate määrata taotluse Aktsepteeri kodeering. Taotluse Aktsepteeri kodeering HTTP-päis reklaamib sisu kodeeringut, millest klient saab aru. See sisu kodeering on tavaliselt tihendamise algoritm. |
| Sisu tüüp            | Saate määrata sisu tüübi. Sisu tüübi üksuse päis tähistab ressursi meediumitüüpi. |

### <a name="message-processing-actions"></a>Sõnumi töötlemise tegevused

Saate kasutada sõnumi töötlemise tegevusi, et luua oma protsesside jaoks tegevusi ja seadistada nende parameetreid. Saate sõnumi töötlemise tegevusi seadistada lehel **Sõnumi töötlemise tegevused** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumi töötlemise tegevused**).

Järgmistes tabelites kirjeldatakse lehel **Sõnumi töötlemise tegevused** olevaid väljasid.

#### <a name="general-fasttab"></a>Kiirkaart Üldine

| Väli                   | Kirjeldus |
|-------------------------|-------------|
| Tegevuse tüüp             | Saate valida tegevuse tüübi. Lisateavet saadaolevate valikute kohta vt jaotisest [Sõnumi töötlemise tegevuse tüübid](#message-processing-action-types). |
| Vormingu vastendamine          | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimine**, **Elektroonilise aruandluse importimine** ja **Elektroonilise aruandluse eksportimissõnum**. |
| Sõnumiüksuse tüüp       | Saate valida kirjete tüübid, mille saamiseks tegevust tuleb hinnata. See väli on saadaval tegevuste jaoks, mille tüüp on **Sõnumiüksuse käivitamise tase**, **Elektroonilise aruandluse eksportimine** ja **Elektroonilise aruandluse importimine** ja veel mõned muud tüübid. Kui jätate selle välja tühjaks, hinnatakse kõiki sõnumiüksuse tüüpe, mis on sõnumi töötlemiseks määratletud. |
| Täidetav klass        | Saate valida eelnevalt loodud täidetava klassi sätted. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Sõnumi täitmise tase** ja **Sõnumiüksuse täitmise tase**. |
| Kirjete asustamise tegevus | Saate valida eelnevalt seadistatud kirjete asustamise tegevuse. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Kirjete asustamine**. |

##### <a name="message-processing-action-types"></a>Sõnumi töötlemise tegevuse tüübid

Väljal **Tegevuse tüüp** on saadaval järgmised suvandid.

- **Kirjete asustamine** – eelnevalt peab olema seadistatud tegevus **kirjete asustamine**. Seostage see tegevusega, mille tüüp on **Kirjete asustamine**, et lubada selle kaasamine töötlemisse. Eeldatakse, et seda tegevuse tüüpi kasutatakse esimese tegevuse jaoks sõnumi töötlemisel. Seetõttu saab seda tüüpi tegevuse jaoks seadistada ainult tulemuse oleku. Esialgset olekut ei saa seadistada.
- **Loo sõnum** – kasutage seda tüüpi, et kasutajad saaksid lehel **Elektronsõnum** käsitsi sõnumeid koostada. Seda tüüpi tegevuse jaoks ei saa esialgset olekut seadistada.
- **Sõnumi täitmise tase** – kasutage seda tüüpi, et seadistada täidetav klass, mida tuleb hinnata sõnumi tasemel.
- **Sõnumiüksuse täitmise tase** – kasutage seda tüüpi, et seadistada täidetav klass, mida tuleb hinnata sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimine** – kasutage seda tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval ER-i konfiguratsioonil sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimissõnum** – kasutage seda tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval ER-i konfiguratsioonil sõnumi tasemel (näiteks kui sõnumil pole sõnumiüksusi).
- **Elektroonilise aruandluse importimine** – kasutage seda tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb imporditaval ER-i konfiguratsioonil.
- **Kasutaja töötlemine sõnumi tasemel** – kasutage seda tüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab midagi käsitsi tegema. Näiteks võib kasutaja uuendada sõnumite olekut.
- **Kasutaja töötlemine** – kasutage seda tüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab midagi käsitsi tegema. Näiteks võib kasutaja uuendada sõnumiüksuste olekut.
- **Veebiteenus** – kasutage seda tüüpi tegevuste jaoks, mis peavad loodud aruande edastama veebiteenusele. Seda tegevuse tüüpi ei kasutata itaalia ostu- ja müügiarvete suhtluse aruandluse jaoks.
- **Kinnitamise taotlemine** – kasutage seda tüüpi kinnitamise taotlemiseks serverist.

#### <a name="initial-statuses-fasttab"></a>Kiirkaart Algolekud

> [!NOTE]
> Kiirkaart **Algolekud** pole saadaval tegevuste jaoks, mille esialgne tüüp on **Kirjete asustamine** või **Loo sõnum**.

| Väli               | Kirjeldus                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Sõnumiüksuse olek | Saate valida sõnumiüksuse oleku, mille saamiseks valitud sõnumi töötlemise tegevust tuleb hinnata. |
| Kirjeldus         | Valitud sõnumiüksuse oleku kirjeldus.                                                  |

#### <a name="result-statuses-fasttab"></a>Kiirkaart Tulemi olekud

| Väli               | Kirjeldus |
|---------------------|-------------|
| Teate olek      | Saate valida sõnumite olekud, mille saamiseks valitud sõnumi töötlemise tegevust tuleb hinnata. See väli on saadaval ainult sõnumi töötlemise tegevuse jaoks, mida hinnatakse sõnumi tasemel. Näiteks on see saadaval tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimine** ja **Elektroonilise aruandluse importimine**. See pole saadaval tegevuste jaoks, mille tüüp on **Kasutaja töötlemine** ja **Sõnumiüksuse käivitamise tase**. |
| Kirjeldus         | Valitud sõnumi oleku kirjeldus. |
| Vastuse tüüp       | Valitud sõnumi oleku vastuse tüüp. |
| Sõnumiüksuse olek | Saate valida tulemuseks saavad olekud, mis peaksid olema saadaval pärast seda, kui valitud sõnumi töötlemise tegevus on hinnatud. See väli on saadaval ainult sõnumi töötlemise tegevuse jaoks, mida hinnatakse sõnumiüksuse tasemel. Näiteks on see saadaval tegevuste jaoks, mille tüüp on **Kasutaja töötlemine** ja **Sõnumiüksuse käivitamise tase**. Sõnumi töötlemise tegevuste jaoks, mida hinnatakse sõnumi tasemel, kuvab see väli sõnumiüksuse oleku, mis seadistati valitud sõnumi oleku jaoks. |

### <a name="electronic-message-processing"></a>Elektronsõnumi töötlemine

Elektronsõnumi töötlemine on elektronsõnumite funktsiooni põhikontseptsioon. See koondab tegevused, mida tuleb elektronsõnumi saamiseks hinnata. Tegevusi saab siduda esialgse oleku ja tulemuse oleku kaudu. Teise võimalusena saab tüübiga **Kasutaja töötlemine** tegevusi alustada sõltumatult. Lehel **Elektronsõnumi töötlemine** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Elektronsõnumi töötlemine**) saate valida ka täiendavaid välju, mida tuleb töötlemise jaoks toetada.

Kiirkaart **Tegevus** võimaldab teil töötlemisele lisada eelmääratletud tegevusi. Saate määrata, kas tegevus peab käivitama eraldi või kas selle saab käivitada töötlemisega. (Kasutaja tegevused tuleb käivitada eraldi.)

Kiirkaart **Sõnumiüksuse lisaväljad** võimaldab teil lisada eelmääratletud lisavälju, mis on seotud sõnumiüksustega. Peata lisama lisaväljad iga sõnumiüksuse tüübi jaoks, millega väljad on seotud.

Kiirkaart **Sõnumi lisaväljad** võimaldab teil lisada eelmääratletud lisavälju, mis on seotud sõnumitega.

Kiirkaart **Turberollid** võimaldab teil seadistada turberolle, mis on süsteemis eelmääratletud spetsiifilise töötlemise jaoks. Kasutajad, kellel on kindel roll, näevad ainult töötlemist, mis on määratletud selle rolli jaoks.

Kiirkaart **Partii** võimaldab teil seadistada töötlemist partiirežiimis.

## <a name="work-with-electronic-messages-functionality"></a>Töötamine elektronsõnumite funktsiooniga

Kui töötate sõnumi tasemel, on leht **Elektronsõnumid** (**Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumid**) kasulikum. Kui tegutsete andmete kogumise (sõnumiüksuse) tasemel, on leht **Elektronsõnumi üksused** (**Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumi üksused**) kasulikum.

### <a name="electronic-messages"></a>Elektronsõnumid

Leht **Elektronsõnumid** võimaldab töötlemist, mis on teie rolli põhjal teile saadaval. Turberollid on seostatud töötlemisega selle töötlemise seadistuses. Iga töötlemise jaoks, mis on teile saadaval, kuvab leht elektronsõnumid ja nendega seotud teabe.

Kiirkaardil **Sõnumid** kuvatakse elektronsõnumid valitud töötlemise jaoks. Olenevalt valitud sõnumi olekust ja eelmääratletud töötlemisest saate käivitada teatud tegevusi, valides ruudustiku kohal olevad nupud:

- **Uus** – see nupp on seotud tegevustega, mille tüüp on **Loo sõnum**.
- **Kustuta** – see nupp on saadaval, kui valitud sõnumi praeguse oleku jaoks on valitud märkeruut **Luba kustutamine**.
- **Loo aruanne** – see nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**.
- **Saada aruanne** – see nupp on seotud tegevustega, mille tüüp on **Veebiteenus**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine sõnumi tasemel**.
- **Sõnumiüksused** – avab lehe **Elektronsõnumi üksused**.

Kiirkaart **Tegevuste logi** kuvab teabe kõigi tegevuste kohta, mis on valitud sõnumi jaoks käivitatud.

Kiirkaart **Sõnumi lisaväljad** kuvab kõik lisaväljad, mis on sõnumite jaoks määratletud töötlemise seadistuses. See kuvab ka nende lisaväljade väärtused.

Kiirkaart **Sõnumiüksused** kuvab kõik sõnumiüksused, mis on seotud valitud sõnumiga.

Saate kõik valitud sõnumi manused läbi vaadata. Need manused on aruanded, mis on juba loodud ja vastu võetud. Valige sõnum, mille manuseid soovite läbi vaadata ja seejärel valige toimingupaanil nupp **Manus**.

![Nupp Manus](media/attachment-icon.png)

Lehel **Manused** kuvatakse kõik manused, mis on sõnumiga seotud. Faili vaatamiseks valige see vasakul olevast loendist ja seejärel valige toimingupaanil nupp **Ava**.

![Nupp Ava](media/open-button.png)

Et vaadata läbi manus, mis on seotud kindla tegevusega, mis käivitati eelnevalt sõnumi jaoks, valige sõnum lehel **Elektronsõnumid** ja seejärel valige kiirkaardil **Tegevuste logi** soovitud tegevus. Seejärel valige toimingupaanil nupp **Manus**.

Saate käivitada kas kogu töötlemise või ainult kindla tegevuse, valides toimingupaanil nupu **Käivita töötlemine**.

### <a name="electronic-message-items"></a>Elektronsõnumi üksused

Lehel **Elektronsõnumi üksused** on esitatud kõik sõnumiüksused ja iga sõnumiüksuse jaoks käivitatud tegevuste logi. Sellel kuvatakse ka lisaväljad, mis on sõnumiüksuste jaoks määratletud, ja nende lisaväljade väärtused.

Järgmises tabelis kirjeldatakse vahekaardi **Sõnumiüksused**.

<table>
<thead>
<tr>
<th>Väli</th>
<th>Kirjeldus</th>
</tr>
</thead>
<tbody>
<tr>
<td>Teostamine</td>
<td>Sõnumiüksuse loomiseks kasutatud töötlemise nimi.</td>
</tr>
<tr>
<td>Sõnumiüksus</td>
<td>Sõnumiüksuse ID. ID määratakse automaatselt, võttes aluseks numbriseeria <strong>Sõnumiüksus</strong> mis on määratletud lehel <strong>Pearaamatu parameetrid</strong>.</td>
</tr>
<tr>
<td>Sõnumiüksuse kuupäev</td>
<td>Sõnumiüksuse loomise kuupäev.</td>
</tr>
<tr>
<td>Sõnumiüksuse tüüp</td>
<td>Sõnumiüksuse tüüp. Sama töötlemise jaoks saab seadistada mitut tüüpi sõnumiüksusi (nt <strong>Sissetulevad arved</strong> ja <strong>Väljaminevad arved</strong>). Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
</tr>
<tr>
<td>Sõnumiüksuse olek</td>
<td>Sõnumiüksuse tegelik olek. Saadaolevad olekud on olenevalt sõnumiüksuse tüübist erinevad. Järgmisena on toodud mõned näited.
<ul>
<li><strong>Asustatud</strong> – kirje lisati sõnumiüksuste tabelisse.</li>
<li><strong>Hinnatud</strong> – sõnumiüksuse jaoks arvutati lisaatribuudid.</li>
<li><strong>Esitatud</strong> – sõnumiüksuse lisati aruandele.</li>
<li><strong>Välja jäetud</strong> – see olek võib olla kasulik, kui peate aruandest enne selle eksportimist mõned sõnumiüksused välja jätma.</li>
</ul>
</td>
</tr>
<tr>
<td>Edastuse kuupäev</td>
<td>Töötlemise jaoks, mis edastab loodud aruande automaatselt väljapoole süsteemi, sõnumiüksuse edastamise kuupäev.</td>
</tr>
<tr>
<td>Dokumendi number</td>
<td>See väli täidetakse kirjete asustamise tegevuse seadistuse alusel automaatselt. Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
</tr>
<tr>
<td>Konto number</td>
<td>Kliendi või hankija kontonumber (või muu välja väärtus, olenevalt väljast, mis on määratletud tegevuses <strong>Kirjete asustamine</strong>). Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
</tr>
<tr>
<td>Sõnum</td>
<td>Sõnumi kood. Kood määratakse automaatselt, võttes aluseks numbriseeria <strong>Sõnum</strong> mis on määratletud lehel <strong>Pearaamatu parameetrid</strong>.</td>
</tr>
<tr>
<td>Teate olek</td>
<td>Elektronsõnumi tegelik olek.</td>
</tr>
<tr>
<td>Järgmine tegevus</td>
<td>Järgmised tegevused, mille saab sõnumiüksuse praeguse oleku jaoks käivitada.</td>
</tr>
</tbody>
</table>

Vahekaart **Lisaväljad** kuvab lisaväljad valitud sõnumiüksuse jaoks, ja nende väärtused.

#### <a name="run-processing"></a>Töötlemise käivitamine

Valige toimingupaanil **Töötlemise käivitamine**, et käivitada sõnumiüksuste töötlemine. Kindla tegevuse käivitamiseks määrake dialoogiboksis **Töötlemise käivitamine** suvandi **Vali tegevus** väärtuseks **Jah** ja seejärel valige tegevus. Kogu töötlemise käivitamiseks jätka suvandi **Vali tegevus** väärtuseks **Ei**.

#### <a name="generate-report"></a>Aruande loomine

Valige aruande loomiseks toimingupaanil **Loo aruanne**. See nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimine**.

#### <a name="update-status"></a>Oleku värskendamine

Valige toimingupaanil **Värskenda olekut**, et värskendada ühe või mitme sõnumiüksuse olekut. Dialoogiboksis **Värskenda olekut** kasutage kiirkaarti **Kaasatavad kirjed**, et valida värskendatavad sõnumiüksused. Veenduge, et määratleksite valikukriteeriumid õigesti, sest sõnumiüksuse olekud värskendatakse nende kriteeriumide, valitud tegevuse esialgse oleku ja teie määratud väärtuse **Uus olek** järgi. Kui oleku värskendamine on lõpule viidud, on keeruline määratleda, milliseid üksusi just värskendati. Seetõttu on olekuvärskendusi raske tagasi võtta.

#### <a name="electronic-messages"></a>Elektronsõnumid

Valige toimingupaanil **Elektronsõnum**, et vaadata üle elektronsõnum, mis on seotud valitud sõnumiüksusega.

Saate üle vaadata ka kõik sõnumiüksusele vastavad failid. Valige sõnumiüksuse väli **Sõnum** või valige toimingupaanil **Elektronsõnum**. Lehel **Elektronsõnum** valige sõnum, mille aruannet soovite üle vaadata ja seejärel valige toimingupaanil nupp **Manus**.

![Nupp Manus](media/attachment-icon.png)

Lehel **Manused** kuvatakse kõik manused, mis on sõnumiga seotud. Faili vaatamiseks valige see vasakul olevast loendist ja seejärel valige toimingupaanil nupp **Ava**.

![Nupp Ava](media/open-button.png)

#### <a name="original-document"></a>Algdokument

Valige toimingupaanil **Algdokument**, et avada valitud sõnumiüksuse algdokument.

## <a name="example"></a>Näide

Kui olete oma ER-i vormingu loonud, vastendanud selle andmeallikatega ja selle lõpule viinud, saate selle käivitada, kasutades tööruumi **Elektrooniline aruandlus**. Luua aruanne, mille saate salvestada lokaalselt.

Aruandluse protsessi järgmiste aspektide kontrollimiseks peate seadistama elektroonilise aruandluse töötlemise:

- Logima teabe selle kohta, kes aruande lõi.
- Logima aruande loomise aja.
- Salvestama eelmiste perioodide jaoks loodud aruanded.

Sellest jaotisest leiate näite, mis näitab teile, kuidas saate seadistada elektronsõnumite funktsiooni aruandlusprotsessi loomiseks.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Töötlemise seadistamine ja käivitamine lihtsa ER-i eksporditava vormingu kutsumiseks, et luua Exceli aruanne

Sellest jaotisest leiate näite, mis näitab teile, kuidas saate seadistada elektroonilise sõnumside, et luua aruanne, mis põhineb eksporditaval ER-i vormingul Exceli jaoks. Selle näite järgimiseks peab ER-i Exceli eksporditav vorming juba olema loodud, andmeallikatega vastendatud ja lõpule viidud. Elektroonilise sõnumside jaoks peab numbriseeria juba seadistatud olema.

Kui koostate töötlemist, on kasulik, kui määratlete esmalt töötlemise tegevused ja olekud, mida hakatakse seadistama. Järgmisel joonisel on näidatud, kuidas töötlemine selle näite korral välja näeb.

![Töötlemise skeem](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Sõnumite olekute loomine

1. Avage **Maks \> Seadistamine \> Elektronsõnumid \> Sõnumite olekud**.
2. Looge järgmised sõnumite olekud:

    - Uus
    - Ettevalmistatud
    - Loodud

    ![Sõnumite olekud](media/message-statuses.png)

3. Real oleku **Uus** jaoks valige märkeruut **Luba kustutamine**, et kasutajad saaksid selle olekuga sõnumid kustutada.

#### <a name="create-additional-fields"></a>Lisaväljade loomine

1. Avage **Maks \> Seadistamine \> Elektronsõnumid \> Lisaväljad**.
2. Lisage lisaväli ja selle väärtused. Siin on näide.

    ![Lisaväljad](media/additional-fields.png)

3. Määrake suvandi **Kasutaja redigeerimine** väärtuseks **Jah**, et kasutajad saaksid seda välja redigeerida.

#### <a name="create-message-processing-actions"></a>Sõnumi töötlemise tegevuste loomine

Selle näite jaoks loote järgmised tegevused:

- **Loo sõnum**
- **Värskenda ettevalmistatuks**
- **Loo aruanne**
- **Värskenda esialgsele olekule** (valikuline)

1. Avage **Maks \> Seadistamine \> Elektronsõnumid \> Sõnumi töötlemise tegevused**.
2. Looge tegevus nimega **Loo sõnum**. Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Loo sõnum**.
3. Looge tegevus nimega **Värskenda ettevalmistatuks** ja määrake järgmised väljad:

    - Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Kasutaja töötlemine sõnumi tasemel**.
    - Kiirkaardil **Algolekud** väljal **Sõnumi olekud** valige **Uus**.
    - Kiirkaardil **Tulemi olekud** väljal **Sõnumi olekud** valige **Ettevalmistatud**. Väljal **Vastuse tüüp** sisestage **Edukalt täidetud**.

4. Looge tegevus nimega **Loo aruanne** ja määrake järgmised väljad:

    - Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Elektroonilise aruandluse eksportimine**. Väljal **Vormingu vastendamine** valige eksporditav ER-i vorming. Valikud on **Excel**, **XML**, **JSON**, **Tekst** ja **Muu**.
    - Kiirkaardil **Algolekud** väljal **Sõnumi olekud** valige **Ettevalmistatud**.
    - Kiirkaardil **Tulemi olekud** väljal **Sõnumi olekud** valige **Loodud**. Väljal **Vastuse tüüp** sisestage **Edukalt täidetud**.

    ![Aruande tegevuse loomine](media/generate-report-action.png)

5. Valikuline: et kasutajad saaksid aruannet mitu korda luua, saate luua tegevuse **Värskenda esialgsele olekule** ja määrata järgmised väljad.

    - Valige kiirkaardil **Üldine** väljal **Tegevuse tüüp** suvand **Kasutaja töötlemine sõnumi tasemel**.
    - Kiirkaardil **Algolekud** väljal **Sõnumi olekud** valige **Loodud**.
    - Kiirkaardil **Tulemi olekud** väljal **Sõnumi olekud** valige **Ettevalmistatud** või (ja) **Uus**. Väljal **Vastuse tüüp** sisestage **Edukalt täidetud**.

#### <a name="electronic-message-processing"></a>Elektronsõnumi töötlemine

Selles näites tuleb kõik tegevused seadistada, et need käivituks eraldi. Eeldatakse, et kasutaja lähtestab iga toimingu.

1. Avage **Maks \> Seadistamine \> Elektronsõnumid \> Elektronsõnumi töötlemine**.
2. Lisage oma töötlemisele kirje ning lisage kõik eelnevalt määratletud tegevused ja lisaväli.
3. Valikuline: kiirkaardil **Turberollid** määratlege oma töötlemise jaoks turberollid, et piirata juurdepääsu kindlale aruandlusele.
4. Avage **Maks \> Päringud ja aruanded \> Elektronsõnumid \> Elektronsõnumid**.
5. Valige **Uus**, et luua uus sõnum. Selles punktis saate lisada kuupäevi ja kirjelduse. Saate vajaduse korral värskendada ka lisavälja väärtust.

    ![Elektronsõnumi loomine](media/create-electronic-message.png)

Kiirkaardil **Tegevuste logi** olev ruudustik täidetakse automaatselt kõigi sõnumiga tehtud tegevuste logiga.

Saate nüüd sõnumi oleku kas kustutada või seda värskendada. Sõnumi oleku värskendamiseks valige **Värskenda olekut** ja seejärel väljal **Uus olek** valige **Ettevalmistatud**. Seejärel valige **OK**.

![Sõnumi oleku värskendamine](media/update-status.png)

Sõnumi olek värskendatakse väärtusele **Ettevalmistatud** ja te saate nüüd aruande luua, valides **Loo aruanne**. Aruanne luuakse ning sõnumi olekut ja tegevuste logi värskendatakse. Loodud aruande vaatamiseks valige toimingupaanil nupp **Manus**.
