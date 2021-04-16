---
title: Elektrooniline sõnumside
description: Selles teemas antakse elektroonilise sõnumside ülevaade ja seadistusteave rakenduses Microsoft Dynamics 365 Finance.
author: ShylaThompson
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 42896c85fe72690aadafb878eb7e899c6fe10c32
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823784"
---
# <a name="electronic-messaging"></a>Elektronsõnumid

[!include [banner](../includes/banner.md)]

Selles teemas antakse elektroonilise sõnumside ülevaade ja seadistusteave.

Hiljuti kehtestasid erinevate riikide ja piirkondade valitsused ja seadusandlikud asutused üle kogu maailma aruandlusnõuded ettevõtetele, kes on nendes riikides või piirkondades registreeritud. Nende nõuete eesmärk on hankida nendelt ettevõtetelt elektroonilises vormingus andmeid, otse süsteemist, kus neid arvutatakse, hoiustatakse ja töödeldakse.

Elektroonilise sõnumside funktsionaalsus rakenduses Rahandus toetab erinevaid protsesse elektrooniliseks koostalitluseks rakenduse Rahandus ning süsteemide vahel, mida valitsused ja seadusandlikud asutused pakuvad ametliku teabe aruandluseks, esitamiseks ja saamiseks.

Elektroonilise sõnumside funktsionaalsus on integreeritud **elektroonilise aruandluse** (ER) mooduliga. Seetõttu saate elektronsõnumite jaoks seadistada ER-vormingud. Lisateabe saamiseks vt [Elektrooniline aruandlus (ER)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

Elektrooniline sõnumside põhineb järgmistel üksustel:

- **Elektronsõnum** – aruanne või deklaratsioon, mis tuleb esitada ja/või edastada ettevõtte siseselt. Näiteks, aruanne, mis saadetakse maksuametile.
- **Elektronsõnumi üksused** – kirjed, mis tuleb kaasata esitatavasse sõnumisse.
- **Elektronsõnumi töötlemine** – tegevuste ahel, mis tuleb käivitada vajalike andmete kogumiseks, aruannete loomiseks, andmete talletamiseks Microsoft Azure’i bloobimälus, aruannete edastamiseks väljapoole süsteemi, vastuste saamiseks väljastpoolt süsteemi ning andmebaasi värskendamiseks saadud teabe põhjal. Ahela tegevused võivad olla lingitud või linkimata

Järgmine joonis näitab elektroonilise sõnumside andmevoogu.

![Elektroonilise sõnumside andmevoog](media/electronic-messaging-data-flow.png)

Elektronsõnumite funktsioon toetab järgmisi stsenaariume:

- Sõnumite loomine ja aruannete koostamine, mis põhinevad eri tüüpi seostatud eksportimise ER-vormingutel: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst ja Microsoft Word.
- Sõnumite, mis põhinevad teabel, mida taotleti ja saadi asutuselt seostatud importimise ER-vormingu kaudu, automaatne loomine ja töötlemine.
- Teabe kogumine ja töötlemine andmeallikast sõnumiüksustena. Andmeallikas on rakenduse Rahandus tabel.
- Täiendava teabe talletamine ja erinevate väärtuste hindamine, kutsudes eraldi määratletud täidetavad klassid seoses sõnumite või sõnumiüksustega.
- Teabe koondamine, mis on kogutud sõnumiüksustes, selle teabe tükeldamine sõnumite järgi ja aruannete loomine, mis on seotud eksporditavate ER-vormingutega.
- Koostatud aruannete edastamine veebiteenusele, kasutades turbeteavet, mis on talletatud rakendusse Azure Key Vault.
- Vastuse saamine veebiteenuselt, vastuse tõlgendamine ja andmete värskendamine rakenduses Rahandus vajadust mööda.
- Loodud aruannete talletamine ja ülevaatamine.
- Kogu logiteabe talletamine ja ülevaatamine, mis on seotud tegevustega, mis käivitatakse sõnumi või sõnumiüksuse jaoks.
- Töötlemise kontrollimine erinevate sõnumi ja sõnumiüksuse olekutega.

## <a name="set-up-electronic-messaging"></a>Elektroonilise sõnumside seadistamine

Elektroonilise sõnumside abil saate hallata erinevaid elektroonilise aruandluse protsesse erinevate dokumenditüüpide jaoks. Mõnes keerukamas stsenaariumis seadistatakse elektrooniline sõnumside mitme sõnumi olekute, sõnumiüksuste olekute, tegevuste, lisaväljade ja täidetavate klasside kombinatsioonina. Nende stsenaariumide jaoks on importimiseks saadaval andmeüksuste paketid. Kui te kasutate neid andmeüksuse pakette, peate need importima juriidilisse isikusse, kasutades andmehalduse tööriista. Lisateavet andmehalduse tööriista kasutamise kohta vt jaotisest [Andmehaldus](../../dev-itpro/data-entities/data-entities-data-packages.md).

Kui te ei impordi andmeüksuse paketti, saate elektronsõnumite funktsiooni seadistada käsitsi. Sel juhul peate seadistama järgmised elemendid:

- [Numbriseeriad](#number-sequences)
- [Sõnumiüksuste tüübid ja olekud](#message-item-types-and-statuses)
- [Sõnumite olekud](#message-statuses)
- [Lisaväljad](#additional-fields)
- [Täidetava klassi sätted](#executable-class-settings)
- [Kirjete asustamise tegevused](#populate-records-actions)
- [Veebirakendused](#web-applications)
- [Veebiteenuse sätted](#web-service-settings)
- [Sõnumi töötlemise tegevused](#message-processing-actions)
- [Elektronsõnumi töötlemine](#electronic-message-processing)

Järgmised jaotised annavad iga elemendi kohta lisateavet.

### <a name="number-sequences"></a>Numbriseeriad

Saate seadistada numbriseeriad nii sõnumite kui ka sõnumiüksuste jaoks. Numbriseeriaid kasutatakse sõnumite ja sõnumiüksuste automaatseks nummerdamiseks. Määratud numbreid kasutatakse süsteemis sõnumite ja sõnumiüksuste kordumatute identifikaatoritena. Saate elektroonilise sõnumside jaoks numbriseeriad seadistada lehel **Pearaamatu parameetrid** (**Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**).

### <a name="message-item-types-and-statuses"></a>Sõnumiüksuste tüübid ja olekud

Sõnumiüksuste tüübid tuvastavad kirjete tüübid, mida kasutatakse elektronsõnumites. Saate sõnumiüksuste tüübid seadistada lehel **Sõnumiüksuste tüübid** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste tüübid**).

Sõnumiüksuste tüübid tuvastavad olekud, mis rakenduvad sõnumiüksustele teie seadistataval töötlemisel. Saate sõnumiüksuste tüübid seadistada lehel **Sõnumiüksuste olekud** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste olekud**).

Sõnumiüksuse oleku parameeter **Luba kustutamine** määrab selle, kas kasutajad saavad lehel **Elektronsõnumid** või **Elektronsõnumi üksused** selle olekuga sõnumiüksuseid kustutada.

### <a name="message-statuses"></a>Sõnumite olekud

Saate seadistada sõnumite olekud, mis peaksid sõnumite töötlemisel kättesaadavad olema. Saate sõnumite olekud seadistada lehel **Sõnumite olekud** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumite olekud**).

Järgmises tabelis kirjeldatakse lehe **Sõnumite olekud** välju.

| Välja nimi          | Kirjeldus |
|---------------------|-------------|
| Teate olek      | Saate sisestada sõnumi olekule kordumatu nime. Sõnumiolekuid kasutatakse elektronsõnumi oleku iseloomustamiseks igal ajahetkel. Sisestatud nimi kuvatakse lehel **Elektronsõnumid** ja elektronsõnumitega seotud logis. |
| Kirjeldus         | Saate sisestada sõnumi oleku kirjelduse. |
| Vastuse tüüp       | Saate valida sõnumi oleku vastuse tüübi. Töötluse mõned tegevused võivad anda enam kui üht tüüpi vastuseid. Näiteks tegevused tüübiga **Veebiteenus** võib olenevalt selle täitmise tulemusest anda vastuseks tüübi **Edukalt täidetud** või **Tehniline tõrge**. Sel juhul peate määratlema sõnumi oleku mõlema vastusetüübi korral. Lisateavet tegevusetüüpide ja nendega seotud vastusetüüpide kohta vt jaotisest [Sõnumi töötlemise tegevusetüübid](#message-processing-action-types). |
| Sõnumiüksuse olek | Mõnikord peab elektronsõnumi olek mõjutama seotud sõnumiüksuste olekut. Valige sellel väljal sõnumiüksuse olek, mille soovite sõnumi olekuga seostada. |
| Luba kustutamine        | Märkige see ruut, kui kasutajatel peab olema võimalik kustutada elektronsõnumeid, millel on lehel **Elektronsõnumid** see olek. |

### <a name="additional-fields"></a>Lisaväljad

Elektronsõnumite funktsioon võimaldab teil täita kirjeid kandetabelist. Sel viisil saate kirjed aruandluseks ette valmistada ja seejärel need esitada. Mõnikord pole aga kandetabelites piisavalt teavet, et täita kirjeid aruandluse nõuetele vastaval viisil. Kogu teabe täitmiseks, mis tuleb kirje kohta esitada, saate seadistada lisaväljad. Lisaväljad saab seostada nii sõnumite kui ka sõnumiüksustega. Saate seadistada lisaväljad lehel **Lisaväljad** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Lisaväljad**).

Järgmises tabelis kirjeldatakse lehe **Lisaväljad** üldisi välju.

| Väli       | Kirjeldus |
|-------------|-------------|
| Välja nimi  | Saate sisestada protsessiga seotud sõnumiüksuste täiendava atribuudi nime. See nimi kuvatakse kasutajaliideses, kui töötate protsessiga. Seda saab kasutada ka protsessiga seotud ER-i konfiguratsioonides. |
| Kirjeldus | Saate sisestada lisavälja kirjelduse. |
| Kasutaja redigeerimine   | Valige selle suvandi sätteks **Jah**, kui kasutajatel peab olema võimalik lisavälja väärtust kasutajaliideses muuta. |
| Loendur     | Valige selle suvandi sätteks **Jah**, kui lisaväli peab sisaldama elektronsõnumis numbriseeriat. Lisaväljale sisestatakse väärtused automaatselt tegevuse **Elektroonilise aruandluse eksport** ajal. |
| Peidetud      | Valige selle suvandi sätteks **Jah**, kui lisaväli peab olema kasutajaliideses peidetud. |

Iga lisaväli võib olla töötlemise tarbeks eri väärtustega. Saate need väärtused määratleda kiirkaardil **Väärtused**. Järgmises tabelis kirjeldatakse välju.

| Väli                | Kirjeldus |
|----------------------|-------------|
| Välja väärtus          | Saate sisestada aruandluse ajal sõnumi või sõnumiüksusega kasutatava väljaväärtuse. |
| Kirjeldus          | Saate sisestada välja väärtuse kirjelduse. |
| Konto tüüp         | Mõni välja väärtus võib olla piiratud kindla kontotüübiga. Valige üks järgmistest väärtustest: **Kõik**, **Klient** või **Hankija**. |
| Konto kood         | Kui valisite väljal **Konto tüüp** suvandi **Klient** või **Hankija**, saate täiendavalt piirata välja väärtuse kasutamist kindla grupi või tabeliga. |
| Konto/grupi number | Kui valisite väljal **Konto tüüp** väärtuse **Klient** või **Hankija** ja sisestasite väljale **Konto kood** grupi või tabeli, saate sellele väljale sisestada kindla grupi või vastaspoole. |
| Jõustunud            | Saate määrata kuupäeva, mil väärtust tuleks arvestama hakata. |
| Aegumine           | Saate määrata kuupäeva, mil väärtuse arvestamine tuleks lõpetada. |

Vaikimisi ei mõjuta väljadega **Konto/grupi number**, **Konto kood**, **Jõustunud** ja **Aegumine** määratletud kriteeriumide kombinatsioonid lisaväljade väärtuste valikut. Siiski saab neid kombinatsioone kasutada täidetavas klassis, et rakendada kindlat loogikat, mis arvutab lisaväljade väärtused.

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

Mõnel täidetaval klassil võivad olla kohustuslikud parameetrid, mille peab määrama enne täidetava klassi esmakordset käivitamist. Nende parameetrite määratlemiseks valige toimingupaanil suvand **Parameetrid**, määrake avanevas dialoogiboksis väljad ja seejärel valige **OK**. Kindlasti tuleb valida **OK**. Muidu ei salvestata parameetreid andmebaasis ja täidetavat klassi ei kutsuta õigesti.

### <a name="populate-records-actions"></a>Kirjete asustamise tegevused

Saate kasutada kirjete asustamise tegevusi, et seadistada tegevusi, mis lisavad kirjed sõnumiüksuste tabelisse, et neid saaks lisada elektronsõnumile. Näiteks kui teie elektronsõnum peab teatama kliendiarveid, peate seadistama kirjete asustamise tegevuse, mis on lingitud tabeli Kliendiarve tööleht väljaga **Andmeallikas**. Saate seadistada kirjete asustamise tegevused lehel **Kirjete asustamise tegevus** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Kirjete asustamise tegevused**). Looge uus kirje iga tegevuse jaoks, mis peaks lisama kirjeid tabelisse, ja määrake järgmised väljad.

| Väli       | Kirjeldus |
|-------------|-------------|
| Nimi        | Saate sisestada nime tegevusele, mis täidab teie protsessis kirjed. |
| Kirjeldus | Saate sisestada kirjete asustamise tegevuse kirjelduse. |

Kiirkaardil **Andmeallikate seadistus** lisage rida iga andmeallika jaoks, mida protsessis kasutatakse, ja määrake järgmised väljad.

| Väli                  | Kirjeldus |
|------------------------|-------------|
| Nimi                   | Saate andmeallikale sisestada nime. |
| Sõnumiüksuse tüüp      | Saate valida sõnumiüksuse tüübi, mida tuleb kasutada, kui andmeallika jaoks luuakse kirjeid. |
| Konto tüüp           | Saate valida konto tüübi, mis tuleb seostada andmeallika kirjetega. |
| Peatabeli nimi      | Saate valida tabeli, mis peab olema andmeallikas. |
| Dokumendi numbriväli  | Saate valida välja, millelt tuleks valitud tabelis võtta dokumendi number. |
| Dokumendi kuupäevaväli    | Saate valida välja, millelt tuleks valitud tabelis võtta dokumendi kuupäev. |
| Dokumendi kontoväli | Saate valida välja, millelt tuleks valitud tabelis võtta dokumendi konto. |
| Kasutaja päring             | Kui see märkeruut on valitud, saate seadistada päringu, valides ruudustiku kohal suvandi **Redigeeri päringut**. Muidu täidetakse kõik kirjed valitud andmeallika põhjal. |

### <a name="web-applications"></a>Veebirakendused

Veebirakenduse sätetega saate seadistada veebirakenduse nii, et see toetab Open Authorization (OAuth) 2.0. OAuth on avatud standard, mis võimaldab kasutajatel anda rakendusele enda nimel turvalise delegeeritud juurdepääsu identimisteavet jagamata. Samuti saate läbi teha autoriseerimisprotsessi, hankides autoriseerimiskoodi ja pääsutõendi. Veebirakenduse sätteid saate määrata lehel **Veebirakendused** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebirakendused**).

Alljärgnevas tabelis kirjeldatakse lehe **Veebirakendused** välju.

| Väli                        | Kirjeldus |
|------------------------------|-------------|
| Rakenduse nimi             | Saate sisestada veebirakenduse nime. |
| Kirjeldus                  | Saate sisestada veebirakenduse kirjelduse. |
| Baas-URL                     | Saate sisestada veebirakenduse Interneti-baasaadressi. |
| Autoriseerimise URL-i tee       | Saate määrata tee, mida kasutatakse autoriseerimiseks vajaliku URL-i koostamiseks. |
| Loa URL-i tee               | Saate määrata tee, mida kasutatakse tõendi jaoks vajaliku URL-i koostamiseks. |
| Ümbersuunamis-URL                 | Saate sisestada ümbersuunamis-URL-i. |
| Kliendi ID                    | Saate sisestada veebirakenduse kliendi ID. |
| Kliendi saladus                | Saate sisestada veebirakenduse kliendi saladuse. |
| Serveri luba                 | Saate sisestada veebirakenduse serveritõendi. |
| Autoriseerimise vormingu vastendamine | Saate valida elektroonilise aruandluse vormingu, mida kasutatakse autoriseerimistaotluse loomiseks. |
| Impordi loa mudelivastendus   | Saate valida elektroonilise aruandluse importimismudeli vastenduse, mida kasutatakse pääsutõendi salvestamiseks. |
| Antud ulatus                | Rakendusetaotluste jaoks antud ulatus. Seda välja värskendatakse automaatselt. |
| Juurdepääsuloa aegumiseni on jäänud  | Pääsutõendi aegumiseni jäänud aeg. | 
| Aktsepteeri                       | Saate määrata veebitaotluse atribuudi **Aktsepteeri**. Näiteks sisestage **application/vnd.hmrc.1.0+json**. |
| Sisutüüp                 | Saate määrata sisu tüübi. Näiteks sisestage **application/json**. |

Peale selle on lehe **Veebirakendused** toimingupaanil saadaval järgmised nupud autoriseerimisprotsessi toetamiseks.

- **Hangi autoriseerimiskood** – veebirakenduse autoriseerimise käivitamiseks.
- **Hangi pääsutõend** – pääsutõendi hankimise protsessi käivitamiseks.
- **Värskenda pääsutõendit** – pääsutõendi värskendamiseks.

Kui süsteemi andmebaasi salvestatud veebirakenduse pääsutõend on krüptitud kujul, saab seda kasutada veebiteenusele tehtavate taotluste jaoks. Turvalisuse tagamiseks peab juurdepääs pääsutõendile olema piiratud turberollidega, mis peavad saama nende taotlustega tegeleda. Kui taotlusega püüavad tegeleda turbegruppi mittekuuluvad kasutajad, saavad nad tõrketeate, et neil pole lubatud valitud veebirakenduse kaudu tegutseda. Selleks et seadistada turberollid, millel peab olema juurdepääs pääsutõendile, kasutage kiirkaart **Turberollid** lehel **Veebirakendused**. Kui turberolle pole veebirakenduse jaoks määratletud, saab ainult süsteemiadministraator selle veebirakenduse kaudu tegutseda.

### <a name="web-service-settings"></a>Veebiteenuse sätted

Saate veebiteenuse sätteid kasutada otsese andmeedastuse seadistamiseks veebiteenusele. Veebiteenuse sätted saate seadistada lehel **Veebiteenuse sätted** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebiteenuse sätted**).

Järgmises tabelis kirjeldatakse lehe **Veebiteenuse sätted** välju.

| Väli                          | Kirjeldus |
|--------------------------------|-------------|
| Veebiteenus                    | Saate sisestada veebiteenuse nime. |
| Kirjeldus                    | Saate sisestada veebiteenuse kirjelduse. |
| Interneti-aadress               | Saate sisestada veebiteenuse Interneti-aadressi. Kui veebiteenusele on määratud veebirakendus ja veebiteenuse Interneti-aadress peaks olema sama mis valitud veebirakenduse puhul määratletud aadress, valige suvand **Kopeeri baas-URL**, et kopeerida veebirakendusest pärinev baas-URL sellele väljale. |
| Tunnistus                    | Saate valida eelnevalt seadistatud võtmehoidla serdi. |
| Veebirakendus                | Saate valida eelnevalt seadistatud võtmehoidla serdi. |
| Vastuse tüüp – XML        | Määrake selle suvandi väärtuseks **Jah**, kui vastuse tüüp on XML. |
| Päringu meetod                 | Saate määrata päringu meetodi. HTTP määrab päringu meetodite komplekti, mis näitavad toimingut, mis tuleb antud ressursiga teha. Taotlusmeetod võib olla **HANGI**, **POSTITA** või muu HTTP-meetod. |
| Päringu päised                | Saate määrata päringu päised. Päringu päis on HTTP-päis, mida saab kasutada HTTP-päringus ja see pole sõnumi sisuga seotud. |
| Aktsepteeri                         | Saate määrata veebitaotluse atribuudi **Aktsepteeri**. |
| Aktsepteeri kodeering                | Saate määrata suvandi **Aktsepteeri kodeering** väärtuse. Taotluse Aktsepteeri kodeering HTTP-päis reklaamib sisu kodeeringut, millest klient saab aru. See sisu kodeering on tavaliselt tihendamise algoritm. |
| Sisutüüp                   | Saate määrata sisu tüübi. Sisutüübi üksuse HTTP-päis tähistab ressursi meediumitüüpi. |
| Edukas vastuse kood       | Saate määrata HTTP olekukoodi, mis näitab, et taotlus õnnestus. |
| Taotluse päiste vorminguvastendus | Saate valida elektroonilise aruandluse vormingu, mida kasutatakse veebitaotluse päiste loomiseks. |

### <a name="message-processing-actions"></a>Sõnumi töötlemise tegevused

Saate kasutada sõnumi töötlemise tegevusi, et luua oma protsesside jaoks tegevusi ja seadistada nende parameetreid. Saate sõnumi töötlemise tegevusi seadistada lehel **Sõnumi töötlemise tegevused** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumi töötlemise tegevused**).

Järgmistes tabelites kirjeldatakse lehel **Sõnumi töötlemise tegevused** olevaid väljasid.

#### <a name="general-fasttab"></a>Kiirkaart Üldine

| Väli                       | Kirjeldus |
|-----------------------------|-------------|
| Tegevuse tüüp                 | Saate valida tegevuse tüübi. Lisateavet saadaolevate valikute kohta vt jaotisest [Sõnumi töötlemise tegevuse tüübid](#message-processing-action-types). |
| Vormingu vastendamine              | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimine**, **Elektroonilise aruandluse importimine** ja **Elektroonilise aruandluse eksportimissõnum**. |
| Vorminguvastendus URL-i tee jaoks | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus**. Seda kasutatakse URL-aadressi tee koostamiseks, mis lisatakse valitud veebiserveri jaoks määratavale Interneti baasaadressile. |
| Sõnumiüksuse tüüp           | Saate valida kirjete tüübid, mille saamiseks tegevust tuleb hinnata. See väli on saadaval tegevuste jaoks, mille tüüp on **Sõnumiüksuse täitmise tase**, **Elektroonilise aruandluse eksportimine** ja **Elektroonilise aruandluse importimine**, **Veebiteenus** jne. Kui jätate selle välja tühjaks, hinnatakse kõiki sõnumiüksuse tüüpe, mis on sõnumi töötlemiseks määratletud. |
| Täidetav klass            | Saate valida eelnevalt loodud täidetava klassi sätted. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Sõnumi täitmise tase** ja **Sõnumiüksuse täitmise tase**. |
| Kirjete asustamise tegevus     | Saate valida eelnevalt seadistatud kirjete asustamise tegevuse. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Kirjete asustamine**. |
| Veebiteenus                 | Saate valida varem seadistatud veebiteenuse. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus**. |
| Faili nimi                   | Saate määrata tegevuse tulemfaili nime. See fail võib olla vastus veebiserverilt või loodud aruanne. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus** ja **Elektroonilise aruandluse eksportimissõnum**. |
| Kuva dialoog                 | Valige selle suvandi sätteks **Jah**, kui enne aruande loomist tuleb kasutajale kuvada dialoogiboks. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**. |

##### <a name="message-processing-action-types"></a>Sõnumi töötlemise tegevuse tüübid

Väljal **Tegevuse tüüp** on saadaval järgmised suvandid.

- **Sõnumi loomine** – kasutage seda tegevusetüüpi, et kasutajad saaksid lehel **Elektronsõnum** käsitsi sõnumeid koostada. Seda tüüpi tegevuse jaoks ei saa esialgset olekut seadistada.
- **Kirjete asustamine** – eelnevalt peab olema seadistatud tegevus tüübiga **kirjete asustamine**. Seostage see tegevusetüüp kirjete asustamise tegevusega, et lubada selle kaasamine töötlemisse. Eeldatakse, et seda tegevusetüüpi kasutatakse kas sõnumitöötluse esimese tegevuse puhul (kui varem loodud elektronsõnumeid pole) või tegevuse puhul, millega lisatakse sõnumiüksuseid varem loodud sõnumile tegevusega, mille tüüp on **Sõnumi loomine**. Seetõttu saab seda tüüpi tegevuse jaoks seadistada ainult sõnumiüksuste tulemuse oleku.Seetõttu saab seda tüüpi tegevuste puhul määrata tulemoleku ainult sõnumiüksuste puhul. Esialgse oleku saab seadistada ainult sõnumite puhul.
- **Sõnumi täitmise tase** – kasutage seda tegevusetüüpi, et seadistada täidetav klass, mida tuleb hinnata sõnumi tasemel.
- **Sõnumiüksuse täitmise tase** – kasutage seda tegevuse, et seadistada täidetav klass, mida tuleb hinnata sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimine** – kasutage seda tegevusetüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval elektroonilise aruandluse konfiguratsioonil sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimissõnum** – kasutage seda tegevusetüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval elektroonilise aruandluse konfiguratsioonil sõnumi tasemel, näiteks kui sõnumil pole sõnumiüksusi.
- **Elektroonilise aruandluse importimine** – kasutage seda tegevuse tegevuste jaoks, mis peavad looma aruande, mis põhineb imporditaval elektroonilise aruandluse konfiguratsioonil.
- **Kasutaja töötlemine sõnumi tasemel** – kasutage seda tegevusetüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab tegema mõne käsitsi tegevuse sõnumi tasemel. Näiteks võib kasutaja uuendada sõnumite olekut.
- **Kasutaja töötlemine** – kasutage seda tegevusetüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab tegema mõne käsitsi tegevuse sõnumiüksuse tasemel. Näiteks võib kasutaja uuendada sõnumiüksuste olekut.
- **Veebiteenus** – kasutage seda tegevusetüüpi tegevuste jaoks, mis peavad loodud aruande edastama veebiteenusele. Seda tegevuse tüüpi ei kasutata itaalia ostu- ja müügiarvete suhtluse aruandluse jaoks. Tegevuste puhul tüübiga **Veebiteenus** sisaldab leht **Sõnumi töötlemise tegevuse** kiirkaarti **Mitmesugused üksikasjad**, kus saate määrata kinnitusteksti. See kinnitustekst kuvatakse kasutajatele enne valitud veebiteenusele tehtud taotlusega tegelemist.
- **Kinnituse taotlemine** – kasutage seda tegevusetüüpi kinnituse taotlemiseks serverist.

#### <a name="initial-statuses-fasttab"></a>Kiirkaart Algolekud

> [!NOTE]
> Kiirkaart **Algolekud** pole saadaval tegevuste jaoks, mille esialgne tegevusetüüp on **Sõnumi loomine**.

| Väli               | Kirjeldus |
|---------------------|-------------|
| Sõnumiüksuse olek | Saate valida sõnumiüksuse oleku, mille saamiseks valitud sõnumi töötlemise tegevust tuleb hinnata. |
| Kirjeldus         | Valitud sõnumiüksuse oleku kirjeldus. |

#### <a name="result-statuses-fasttab"></a>Kiirkaart Tulemi olekud

| Väli               | Kirjeldus |
|---------------------|-------------|
| Teate olek      | Saate valida sõnumite olekud, mille saamiseks valitud sõnumi töötlemise tegevust tuleb hinnata. See väli on saadaval ainult sõnumi töötlemise tegevuse jaoks, mida hinnatakse sõnumi tasemel. Näiteks on see saadaval tegevustele tüübiga **Elektroonilise aruandluse eksportimine** ja **Elektroonilise aruandluse importimine**, kuid see pole saadaval tegevustele tüübiga **Kasutaja töötlemine** ja **Sõnumiüksuse täitmistase**. |
| Kirjeldus         | Valitud sõnumi oleku kirjeldus. |
| Vastuse tüüp       | Valitud sõnumi oleku vastuse tüüp. |
| Sõnumiüksuse olek | Saate valida tulemuseks saavad olekud, mis peaksid olema saadaval pärast seda, kui valitud sõnumi töötlemise tegevus on hinnatud. See väli on saadaval ainult sõnumi töötlemise tegevuse jaoks, mida hinnatakse sõnumiüksuse tasemel. Näiteks on see saadaval tegevuste jaoks, mille tüüp on **Kasutaja töötlemine** ja **Sõnumiüksuse käivitamise tase**. Sõnumi töötlemise tegevuste jaoks, mida hinnatakse sõnumi tasemel, kuvab see väli sõnumiüksuse oleku, mis seadistati valitud sõnumi oleku jaoks. |

Järgmises tabelis on näidatud tulemolekud, mis tuleb seadistada eri tegevusetüüpidele ja vastusetüüpidele.

| Elektronsõnumi tegevusetüüp / vastusetüüp | Täitmine õnnestus | Äritõrge | Tehniline tõrge | Kasutaja määratud | Loobu |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Loo sõnum                               | X                     |                |                 |              |        |
| Elektroonilise aruandluse eksportimine                  | X                     |                |                 |              |        |
| Elektroonilise aruandluse importimine                  |                       |                |                 |              |        |
| Veebiteenus                                  | X                     |                | X               |              |        |
| Kasutaja töötlemine                              |                       |                |                 |              |        |
| Sõnumi käivitamise tase                      |                       |                |                 |              |        |
| Asustamiskirjed                             |                       |                |                 |              |        |
| Sõnumiüksuse käivitamise tase                 |                       |                |                 |              |        |
| Päringu kinnitamine                         | X                     | X              | X               |              |        |
| Elektroonilise aruandluse eksportimissõnum          | X                     |                |                 |              |        |
| Kasutaja töötlemine sõnumi tasemel                |                       |                |                 |              |        |

### <a name="electronic-message-processing"></a>Elektronsõnumi töötlemine

Elektronsõnumi töötlemine on elektronsõnumite funktsiooni põhikontseptsioon. See koondab tegevused, mida tuleb elektronsõnumi saamiseks hinnata. Tegevusi saab siduda esialgse oleku ja tulemuse oleku kaudu. Teise võimalusena saab tüübiga **Kasutaja töötlemine** tegevusi alustada sõltumatult. Samuti saate lehel **Elektronsõnumi töötlemine** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Elektronsõnumi töötlemine**) valida lisavälju, mida tuleb töötlemise jaoks toetada kas sõnumi tasemel või sõnumiüksuste tasemel.

Kiirkaart **Tegevus** võimaldab teil töötlemisele lisada eelmääratletud tegevusi. Saate määrata, kas tegevus peab käivitama eraldi või kas selle saab käivitada töötlemisega. Selleks et määrata, et töötlemisel saab tegevuse käivitada ainult kasutaja, valige selle tegevuse puhul välja **Käivita eraldi** sätteks **Jah**. Kui tegevus tuleb käivitada, töödeldes sõnumeid või sõnumiüksusi, mis on tegevuse algse olekuna määratletud olekus, valige välja **Käivita eraldi** sätteks **Ei**. Tegevused tüübiga **Kasutaja tegevus** tuleb alati eraldi käivitada.

Mõnikord tuleb mitu tegevust koondada järjekorda, isegi kui esimene tegevus on seadistatud nii, et see käivitub eraldi. Näiteks peab kasutaja käivitama aruande loomise, kuid kohe pärast aruande loomist tuleb see saata veebiteenusele ja süsteemis tuleb kajastada veebiteenusest saadud vastust. Sel juhul saate luua eraldamatu jada tegevustele, mis tuleb käivitada alati koos. Valige kiirkaardil **Tegevus** ruudustiku kohal suvand **Eraldamatud jadad** ja looge jada. Seejärel valige kõigi tegevuste jaoks, mis tuleb koos käivitada, jada väljal **Eraldamatu jada**. Sellisel juhul saab jada esimese tegevuse puhul valida välja **Käivita eraldi** sätteks **Jah**, kuid kõigi teiste tegevuste puhul **Ei**.

Kiirkaart **Sõnumiüksuse lisaväljad** võimaldab teil lisada eelmääratletud lisavälju, mis on seotud sõnumiüksustega. Peata lisama lisaväljad iga sõnumiüksuse tüübi jaoks, millega väljad on seotud.

Kiirkaart **Sõnumi lisaväljad** võimaldab teil lisada eelmääratletud lisavälju, mis on seotud sõnumitega.

Kiirkaart **Turberollid** võimaldab teil seadistada turberolle, mis on süsteemis eelmääratletud spetsiifilise töötlemise jaoks. Kasutajad, kellel on kindel roll, näevad ainult töötlemist, mis on määratletud selle rolli jaoks.

Kiirkaart **Partii** võimaldab teil seadistada töötlemist partiirežiimis.

## <a name="work-with-the-electronic-messages-functionality"></a>Töötamine elektronsõnumite funktsiooniga

Kui töötate sõnumi tasemel, on leht **Elektronsõnumid** (**Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumid**) kasulikum. Kui tegutsete andmete kogumise (sõnumiüksuse) tasemel, on leht **Elektronsõnumi üksused** (**Maks** \> **Päringud ja aruanded** \> **Elektronsõnumid** \> **Elektronsõnumi üksused**) kasulikum.

### <a name="electronic-messages"></a>Elektronsõnumid

Leht **Elektronsõnumid** võimaldab töötlemist, mis on teie rolli põhjal teile saadaval. Turberollid on seostatud töötlemisega selle töötlemise seadistuses. Iga töötlemise jaoks, mis on teile saadaval, kuvab leht elektronsõnumid ja nendega seotud teabe.

Kiirkaardil **Sõnumid** kuvatakse elektronsõnumid valitud töötlemise jaoks. Olenevalt valitud sõnumi olekust ja eelmääratletud töötlemisest saate käivitada teatud tegevusi, kasutades ruudustiku kohal olevaid nuppe.

- **Uus** – see nupp on seotud tegevustega, mille tüüp on **Loo sõnum**.
- **Kustuta** – see nupp on saadaval, kui valitud sõnumi praeguse oleku jaoks on valitud märkeruut **Luba kustutamine**.
- **Kogu andmeid** – see nupp on seotud tegevustega, mille tüüp on **Kirjete asutamine**.
- **Loo aruanne** – see nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**.
- **Saada aruanne** – see nupp on seotud tegevustega, mille tüüp on **Veebiteenus**.
- **Impordi vastus** – see nupp on seostatud tegevustega, mille tüüp on **Elektroonilise aruandluse importimine**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine sõnumi tasemel**.
- **Sõnumiüksused** – avab lehe **Elektronsõnumi üksused**.

Kiirkaart **Tegevuste logi** kuvab teabe kõigi tegevuste kohta, mis on valitud sõnumi jaoks käivitatud. Kui tegevus põhjustas tõrke, lisatakse teave tõrke kohta ruudustikus seotud reale. Tõrke kohta teabe vaatamiseks valige ruudustikus rida ja seejärel valige lehe ülanurgas nupp **Manus** (kirjaklambrisümbol).

Kiirkaart **Sõnumi lisaväljad** kuvab kõik lisaväljad, mis on sõnumite jaoks määratletud töötlemise seadistuses. See kuvab ka nende lisaväljade väärtused.

Kiirkaart **Sõnumiüksused** kuvab kõik sõnumiüksused, mis on seotud valitud sõnumiga. Olenevalt valitud sõnumiüksuse olekust saate käivitada teatud tegevusi, kasutades ruudustiku kohal olevaid nuppe.

- **Kustuta** – see nupp on saadaval, kui valitud sõnumiüksuse praeguse oleku jaoks on valitud märkeruut **Luba kustutamine**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine**.
- **Algdokument** – saate avada lehe, millel kuvatakse valitud sõnumiüksuse algdokument.

Kõik sõnumi puhul juba loodud ja vastu võetud aruanded on sellele sõnumile manustatud. Sõnumiga seotud manuste vaatamiseks valige sõnum ja seejärel valige lehe ülanurgas nupp **Manus** (kirjaklambrisümbol).

![Nupp Manus](media/attachment-icon.png)

Lehel **Manused** kuvatakse kõik valitud sõnumiga seotud manused. Faili vaatamiseks valige see vasakul olevast loendist ja seejärel valige toimingupaanil nupp **Ava**.

![Nupp Ava](media/open-button.png)

Saate ka vaadata manuseid, mis on seotud sõnumi puhul varem käivitatud konkreetse tegevusega. Valige lehe **Elektronsõnumid** kiirkaardil **Sõnumid** soovitud sõnum, kiirkaardil **Tegevuselogi** soovitud tegevus ja seejärel valige lehe paremas ülanurgas nupp **Manus**.

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
<td>Kliendi või hankija kontonumber (või muu välja väärtus, olenevalt väljast, mis on määratletud kirjete asustamise tegevuses). Selle välja saab täita automaatselt ainult siis, kui arve lisatakse sõnumiüksuste tabelisse.</td>
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

Valige toimingupaanil **Töötlemise käivitamine**, et käivitada sõnumiüksuste töötlemine. Kindla tegevuse käivitamiseks määrake dialoogiboksis **Töötlemise käivitamine** suvandi **Vali tegevus** sätteks **Jah** ja seejärel valige tegevus. Kogu töötlemise käivitamiseks jätke suvandi **Vali tegevus** sätteks **Ei**.

#### <a name="generate-report"></a>Aruande loomine

Valige aruande loomiseks toimingupaanil **Loo aruanne**. See nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimine**.

#### <a name="update-status"></a>Oleku värskendamine

Valige toimingupaanil **Värskenda olekut**, et värskendada ühe või mitme sõnumiüksuse olekut. Dialoogiboksis **Värskenda olekut** kasutage kiirkaarti **Kaasatavad kirjed**, et valida värskendatavad sõnumiüksused. Veenduge, et määratleksite valikukriteeriumid õigesti, sest sõnumiüksuse olekud värskendatakse nende kriteeriumide, valitud tegevuse esialgse oleku ja teie määratud väärtuse **Uus olek** järgi. Kui oleku värskendamine on lõpule viidud, on keeruline määratleda, milliseid üksusi just värskendati. Seetõttu on olekuvärskendust raske tagasi võtta.

#### <a name="electronic-messages"></a>Elektronsõnumid

Valige toimingupaanil suvand **Elektronsõnumid**, et vaadata üle valitud sõnumiüksusega seotud elektronsõnum.

Saate üle vaadata ka kõik kindla sõnumiüksusega seotud failid. Valige sõnumiüksuse väli **Sõnum** või valige toimingupaanil suvand **Elektronsõnumid**. Seejärel valige lehel **Elektronsõnum** sõnum, mille faile soovite üle vaadata, ja seejärel valige lehe ülanurgas nupp **Manus** (kirjaklambrisümbol).

![Nupp Manus](media/attachment-icon.png)

Lehel **Manused** kuvatakse kõik manused, mis on sõnumiga seotud. Faili vaatamiseks valige see vasakul olevast loendist ja seejärel valige toimingupaanil nupp **Ava**.

![Nupp Ava](media/open-button.png)

#### <a name="original-document"></a>Algdokument

Valige toimingupaanil **Algdokument**, et avada valitud sõnumiüksuse algdokument.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Näide. Töötlemise seadistamine ja käivitamine elektroonilise aruandluse lihtsa ekspordivormingu kutsumiseks, et luua Exceli aruanne

Kui olete oma ER-i vormingu loonud, vastendanud selle andmeallikatega ja selle lõpule viinud, saate selle käivitada, kasutades tööruumi **Elektrooniline aruandlus**. Luuakse aruanne, mille saate lokaalselt salvestada.

Aruandluse protsessi järgmiste aspektide kontrollimiseks peate seadistama elektroonilise aruandluse töötlemise:

- Logima teabe selle kohta, kes aruande lõi.
- Logima teabe selle kohta, millal aruanne loodi.
- Salvestama eelmiste perioodide jaoks loodud aruanded.

Sellest jaotisest leiate näite, mis näitab teile, kuidas saate seadistada elektroonilise sõnumside, et luua aruanne, mis põhineb eksporditaval ER-i vormingul Exceli jaoks. Kui soovite seda näidet järgida, peab ER-i Exceli ekspordivorming juba olema loodud, andmeallikatega vastendatud ja lõpule viidud. Samuti peab elektroonilise sõnumside jaoks numbriseeria juba seadistatud olema.

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
    - Lisage kiirkaardil **Tulemolekud** eraldi rida kummagi sõnumioleku jaoks (**Ettevalmistatud** ja **Uus**). Valige mõlema rea puhul välja **Vastuse tüüp** sätteks **Edukalt käivitatud**.

#### <a name="electronic-message-processing"></a>Elektronsõnumi töötlemine

Selles näites tuleb kõik tegevused seadistada, et need käivituks eraldi. Eeldatakse, et kasutaja käivitab iga toimingu.

1. Avage **Maks \> Seadistamine \> Elektronsõnumid \> Elektronsõnumi töötlemine**.
2. Lisage oma töötlemisele kirje ning lisage kõik eelnevalt määratletud tegevused ja lisaväli.
3. Valikuline: määratlege kiirkaardil **Turberollid** oma töötlemise jaoks turberollid, et piirata juurdepääsu kindlale aruandlusele.
4. Avage **Maks \> Päringud ja aruanded \> Elektronsõnumid \> Elektronsõnumid**.
5. Valige **Uus**, et luua uus sõnum. Selles punktis saate lisada kuupäevi ja kirjelduse. Saate vajaduse korral värskendada ka lisavälja väärtust.

    ![Elektronsõnumi loomine](media/create-electronic-message.png)

Kiirkaardil **Tegevuste logi** olev ruudustik täidetakse automaatselt kõigi sõnumiga tehtud tegevuste logiga.

Saate nüüd sõnumi oleku kas kustutada või seda värskendada. Sõnumi oleku värskendamiseks valige suvand **Värskenda olekut**. Valige väljal **Uus olek** suvand **Ettevalmistatud** ja seejärel valige **OK**.

![Sõnumi oleku värskendamine](media/update-status.png)

Sõnumi olek värskendatakse väärtusele **Ettevalmistatud** ja te saate nüüd aruande luua, valides **Loo aruanne**. Aruanne luuakse ning sõnumi olekut ja tegevuste logi värskendatakse. Loodud aruande vaatamiseks valige lehe paremas ülanurgas nupp **Manus** (kirjaklambrisümbol).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]