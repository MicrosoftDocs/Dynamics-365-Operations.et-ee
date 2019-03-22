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
ms.openlocfilehash: 5326642553c7efcebc6c6af953e2dafe9e62e9ec
ms.sourcegitcommit: f6fc90585632918d9357a384b27028f2aebe9b5a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/11/2019
ms.locfileid: "832191"
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
- [Veebirakendused](#web-applications)
- [Veebiteenuse sätted](#web-service-settings)
- [Sõnumi töötlemise tegevused](#message-processing-actions)
- [Elektronsõnumi töötlemine](#electronic-message-processing)

Järgmised jaotised annavad iga elemendi kohta lisateavet.

### <a name="number-sequences"></a>Numbriseeriad

Saate seadistada numbriseeriad nii sõnumite kui ka sõnumiüksuste jaoks. Numbriseeriaid kasutatakse sõnumite ja sõnumiüksuste automaatseks nummerdamiseks ja määratud numbreid kasutatakse süsteemis sõnumite ja sõnumiüksuste ainuidentifikaatoritena. Saate elektroonilise sõnumside jaoks numbriseeriad seadistada lehel **Pearaamatu parameetrid** (**Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**).

### <a name="message-item-types-and-statuses"></a>Sõnumiüksuste tüübid ja olekud

Sõnumiüksuste tüübid tuvastavad kirjete tüübid, mida kasutatakse elektronsõnumites. Saate sõnumiüksuste tüübid seadistada lehel **Sõnumiüksuste tüübid** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste tüübid**).

Sõnumiüksuste tüübid tuvastavad olekud, mis rakenduvad sõnumiüksustele teie seadistataval töötlemisel. Saate sõnumiüksuste tüübid seadistada lehel **Sõnumiüksuste olekud** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumiüksuste olekud**).

Sõnumiüksuse oleku parameeter **Luba kustutamine** määrab selle, kas kasutajal on lubatud vormi **Elektronsõnumid** või **Elektronsõnumi üksused** kaudu sellises olekus sõnumiüksust kustuta. 

### <a name="message-statuses"></a>Sõnumite olekud

Saate seadistada sõnumite olekud, mis peaksid sõnumite töötlemisel kättesaadavad olema. Saate sõnumite olekud seadistada lehel **Sõnumite olekud** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumite olekud**).

Väljade kirjeldused

| Välja nimi           | Kirjeldus |
|----------------------|-------------|
|Teate olek        | Elektronsõnumi oleku kordumatu nimi, mis iseloomustab sõnumi olekut igal hetkel. See nimi kuvatakse vormil Elektronsõnumid ja elektronsõnumiga seotud logis. |
|Kirjeldus           | Elektronsõnumi olekuga seotud kirjeldus      |
|Vastuse tüüp         | Töötluse mõned tegevused võivad anda enam kui üht tüüpi vastuseid. Näiteks tegevus **Veebiteenus** võib olenevalt selle täitmise tulemusest anda vastuseks **Edukalt täidetud** või **Tehniline tõrge**. Sel juhul peab määrama sõnumi oleku mõlema vastusetüübi korral. Lisateavet tegevuse tüüpide ja nendega seotud vastusetüüpide kohta vt jaotisest [Sõnumi töötlemise tegevuse tüübid](#message-processing-action-types). |
|Sõnumiüksuse olek   |Esineb juhtumeid, mille korral elektronsõnumi olek peab mõjutama vastavalt seotud sõnumiüksuste olekuid. Sellise sõnumiüksuse oleku seostamiseks sellel väljal valige see otsingust. |
|Luba kustutamine          | Elektronsõnumi oleku parameeter **Luba kustutamine** määrab selle, kas kasutajal on lubatud vormi **Elektronsõnumid** kaudu sellises olekus elektronsõnumit kustutada.            |

### <a name="additional-fields"></a>Lisaväljad

Elektronsõnumite funktsioon võimaldab teil asustada kirjeid kandetabelist. Sel viisil saate kirjed aruandluseks ette valmistada ja seejärel need esitada. Mõnikord pole kandetabelis piisavalt teavet kirje esitamiseks aruande nõuete kohaselt. Saate täita kogu teabe, mis tuleb kirje kohta esitada, seadistades lisaväljad. Lisaväljad saab seostada nii sõnumite kui ka sõnumiüksustega. Saate seadistada lisaväljad lehel **Lisaväljad** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Lisaväljad**).

Alljärgnevas tabelis kirjeldatakse lehe **Lisaväljad** üldisi välju.

| Väli                | Kirjeldus |
|----------------------|-------------|
| Välja nimi           | Saate sisestada protsessiga seotud sõnumiüksuste täiendava atribuudi nime. See nimi kuvatakse kasutajaliideses, kui töötate protsessiga. Seda saab kasutada ka protsessiga seotud ER-i konfiguratsioonides. |
| Kirjeldus          | Saate sisestada protsessiga seotud sõnumiüksuste täiendava atribuudi kirjelduse. |
| Kasutaja redigeerimine            | Juhul kui kasutaja peab saama muuta kasutajaliidese abil lisavälja väärtust, märkige ruut **Jah**, muul juhul **Ei**. |
| Loendur              | Kui lisaväli peab sisaldama elektronsõnumis olevat seerianumbrit, märkige see ruut. Lisaväljale sisestatakse väärtused automaatselt elektroonilise aruandluse eksportimise tegevuse sooritamise ajal.  |
| Peidetud               | Kui lisaväli peab olema kasutajaliideses peidetud, märkige see ruut.  |

Iga lisaväli võib olla töötlemise tarbeks eri väärtustega. Need väärtused saate määrata kiirkaardil Väärtused.

| Väli                | Kirjeldus |
|----------------------|-------------|
| Välja väärtus          | Saate sisestada aruandluse ajal seoses sõnumi või sõnumiüksusega kasutatava väljaväärtuse. |
| Välja kirjeldus    | Saate sisestada aruandluse ajal seoses sõnumi või sõnumiüksusega kasutatava väljaväärtuse kirjelduse. |
| Konto tüüp         | Mõned lisaväljade väärtused võivad olla piiratud kindlate kontotüüpidega. Valige üks järgmistest väärtustest: **Kõik**, **Klient** või **Hankija**. |
| Konto kood         | Kui valisite väljal **Konto tüüp** väärtuse **Klient** või **Hankija**, saate täiendavalt piirata välja väärtuste kasutamist kindla grupi või tabeliga. |
| Konto/grupi number | Kui valisite väljal **Konto tüüp** väärtuse **Klient** või **Hankija** ja sisestasite väljale **Konto kood** grupi või tabeli, saate sellele väljale sisestada kindla grupi või vastaspoole. |
| Jõustunud            | Saate määrata kuupäeva, mil väärtust tuleks arvestama hakata. |
| Aegumine           | Saate määrata kuupäeva, mil väärtuse arvestamine tuleks lõpetada. |

Väljadel **Konto/grupi number**, **Konto kood**, **Jõustunud**, **Aegumine** määratud kriteeriumide kombinatsioonid ei mõjuta vaikimisi väärtuse valikut lisaväljale, kuid neid saab kasutada täidetavas klassis, et rakendada mõnda lisavälja väärtuse spetsiifilist arvutusloogikat.

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

Mõnel täidetaval klassil võivad olla kohustuslikud parameetrid, mille peab määrama enne täidetava klassi esmakordset käivitamist. Selliste parameetrite määramiseks klõpsake toimingupaanil nuppu **Parameetrid**, määrake dialoogiaknas vastavad väärtused ja väljad ning klõpsake nuppu **OK**. Nupu **OK** klõpsamine siin on oluline, kuna muidu parameetreid alusesse ei salvestata ja täidetavat klassi ei kutsuta õigesti.

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

### <a name="web-applications"></a>Veebirakendused

Veebirakenduste lehte saate kasutada veebirakenduse parameetrite määramiseks, et toetada avatud standardit OAuth 2.0, mis võimaldab kasutajatel anda enda nimel rakendusele „turvaline delegeeritud juurdepääs” ilma oma juurdepääsumandaati jagamata. Samuti saate sellel lehel läbi teha autoriseerimisprotsessi ja saada autoriseerimiskoodi ja pääsutõendi. Veebirakenduse sätteid saate määrata lehel **Veebirakendused** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebirakendused**).

Alljärgnevas tabelis kirjeldatakse lehe **Veebirakendused** välju.

| Väli                         | Kirjeldus |
|-------------------------------|-------------|
| Rakenduse nimi              | Saate sisestada veebirakenduse nime. |
| Kirjeldus                   | Saate sisestada veebirakenduse kirjelduse. |
| Baas-URL                      | Saate sisestada veebirakenduse Interneti-baasaadressi. |
| Autoriseerimise URL-i tee        | Saate määrata tee autoriseerimiseks vajaliku URL-i koostamiseks.  |
| Loa URL-i tee                | Saate määrata tee tõendiks vajaliku URL-i koostamiseks.  |
| Ümbersuunamis-URL                  | Saate sisestada ümbersuunamis-URL-i.  |
| Kliendi ID                     | Saate sisestada veebirakenduse kliendi ID.  |
| Kliendi saladus                 | Saate sisestada veebirakenduse kliendi saladuse.  |
| Serveri luba                  | Saate sisestada veebirakenduse serveritõendi.  |
| Autoriseerimise vormingu vastendamine  | Saate valida autoriseerimise taotluse loomiseks kasutatava elektroonilise aruandluse (ER) vormingu.   |
| Impordi loa mudelivastendus    | Saate valida pääsutõendi salvestamiseks kasutatava elektroonilise aruandluse importimismudeli vastendamise.  |
| Antud ulatus      Pääsutõend aegub  | Seda välja värskendatakse automaatselt. Selle väärtus näitab, millises ulatuses saab veebirakendusele taotlusi teha.  |
| Aktsepteeri                        | Saate määrata veebitaotluse aktsepteerimisatribuudi. Näiteks „application/vnd.hmrc.1.0+json”.  |
| Sisutüüp           | Saate määrata sisu tüüpi. Näiteks „application/json”.  |

Lehel **Veebirakendused** on autoriseerimisprotsessi toetamiseks saadaval järgmised funktsioonid:
-   **Hangi autoriseerimiskood** – veebirakenduse autoriseerimise käivitamiseks.
-   **Hangi pääsutõend** – pääsutõendi hankimise käivitamiseks.
-   **Värskenda pääsutõendit** – pääsutõendi värskendamiseks.

Kui süsteemi andmebaasi salvestatud veebirakenduse pääsutõend on krüptitud kujul, saab seda kasutada veebiteenusele tehtavate taotluste jaoks. Turvalisuse tagamiseks peab juurdepääs pääsutõendile olema antud ainult neile turberollidele, mis peavad saama nende taotlustega tegeleda. Kui turberühma mittekuuluv kasutaja üritab mõne taotlusega tegeleda, teavitab erand kasutajat, et tal ei ole lubatud valitud veebirakenduse kaudu tegutseda.
Valige Maks > Seadistamine > Elektronsõnumid > Veebirakendused, et kasutada kiirtabelit **Turberollid**, et määrata rollid, millel peab olema juurdepääs pääsutõendile. Kui turberolle pole veebirakenduse jaoks määratud, saab ainult süsteemiadministraator selle veebirakenduse kaudu tegutseda.

### <a name="web-service-settings"></a>Veebiteenuse sätted

Saate veebiteenuse sätteid kasutada otsese andmeedastuse seadistamiseks veebiteenusele. Veebiteenuse sätted saate seadistada lehel **Veebiteenuse sätted** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Veebiteenuse sätted**).

Järgmises tabelis kirjeldatakse lehe **Veebiteenuse sätted** välju.

| Väli                   | Kirjeldus |
|-------------------------|-------------|
| Veebiteenus             | Saate sisestada veebiteenuse nime. |
| Kirjeldus             | Saate sisestada veebiteenuse kirjelduse. |
| Interneti-aadress        | Saate sisestada veebiteenuse Interneti-aadressi. Kui veebirakendus on määratud veebiteenusele ja selle Interneti-aadress peaks olema sama mis valitud veebirakendusele määratud aadress, klõpsake veebirakendusest pärineva **baas-URL-i** kopeerimiseks veebiteenuse väljale **Interneti-aadress** nuppu **Kopeeri baas-URL**.  |
| Tunnistus             | Saate valida eelnevalt seadistatud võtmehoidla serdi. |
| Veebirakendus         | Saate valida eelnevalt seadistatud võtmehoidla serdi. |
| Vastuse tüüp – XML | Määrake selle suvandi väärtuseks **Jah**, kui vastuse tüüp on XML. |
| Päringu meetod          | Saate määrata päringu meetodi. HTTP määrab päringu meetodite komplekti, mis näitavad toimingut, mis tuleb antud ressursiga teha. Meetod võib olla **HANGI**, **POSTITA** või muu HTTP meetod. |
| Päringu päised         | Saate määrata päringu päised. Päringu päis on HTTP-päis, mida saab kasutada HTTP-päringus ja see pole sõnumi sisuga seotud. |
| Aktsepteeri                  | Saate määrata veebitaotluse aktsepteerimisatribuudi. |
| Aktsepteeri kodeering         | Saate määrata taotluse Aktsepteeri kodeering. Taotluse Aktsepteeri kodeering HTTP-päis reklaamib sisu kodeeringut, millest klient saab aru. See sisu kodeering on tavaliselt tihendamise algoritm. |
| Sisu tüüp            | Saate määrata sisu tüübi. Sisu tüübi üksuse päis tähistab ressursi meediumitüüpi. |
| Edukas vastuse kood   | Saate määrata HTTP olekukoodi, mis näitab, et taotlus õnnestus. |
| Taotluse päiste vorminguvastendus  | Saate valida elektroonilise aruandluse vormingu veebitaotluste päiste loomiseks. |

### <a name="message-processing-actions"></a>Sõnumi töötlemise tegevused

Saate kasutada sõnumi töötlemise tegevusi, et luua oma protsesside jaoks tegevusi ja seadistada nende parameetreid. Saate sõnumi töötlemise tegevusi seadistada lehel **Sõnumi töötlemise tegevused** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Sõnumi töötlemise tegevused**).

Järgmistes tabelites kirjeldatakse lehel **Sõnumi töötlemise tegevused** olevaid väljasid.

#### <a name="general-fasttab"></a>Kiirkaart Üldine

| Väli                   | Kirjeldus |
|-------------------------|-------------|
| Tegevuse tüüp             | Saate valida tegevuse tüübi. Lisateavet saadaolevate valikute kohta vt jaotisest [Sõnumi töötlemise tegevuse tüübid](#message-processing-action-types). |
| Vormingu vastendamine          | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimine**, **Elektroonilise aruandluse importimine**, **Elektroonilise aruandluse eksportimissõnum**. |
| Vorminguvastendus URL-i tee jaoks | Saate valida ER-i vormingu, mis tuleb tegevuse jaoks kutsuda. See väli on saadaval ainult nende tegevuste jaoks, mille tüüp on **Veebiteenus**, ja seda kasutatakse valitud veebiserveri jaoks määratud Interneti-baasaadressile lisatava URL-aadressi tee koostamiseks. |
| Sõnumiüksuse tüüp       | Saate valida kirjete tüübid, mille saamiseks tegevust tuleb hinnata. See väli on saadaval tegevuste jaoks, mille tüüp on **Sõnumiüksuse käivitamise tase**, **Elektroonilise aruandluse eksportimine** ja **Elektroonilise aruandluse importimine**, **Veebiteenus** jne. Kui jätate selle välja tühjaks, hinnatakse kõiki sõnumiüksuse tüüpe, mis on sõnumi töötlemiseks määratletud. |
| Täidetav klass        | Saate valida eelnevalt loodud täidetava klassi sätted. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Sõnumi täitmise tase** ja **Sõnumiüksuse täitmise tase**. |
| Kirjete asustamise tegevus | Saate valida eelnevalt seadistatud kirjete asustamise tegevuse. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Kirjete asustamine**. |
| Veebiteenus  | Saate valida varem seadistatud veebiteenuse. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus**.  |
| Faili nimi  | Saate määrata nime failile, mis tekib veebiserveri vastuse või aruande loomise tulemusel. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Veebiteenus** ja **Elektroonilise aruandluse eksportimissõnum**.   |
| Kuva dialoog  | Märkige see ruut, kui enne aruande loomist peab kasutaja nägema dialoogi. See väli on saadaval ainult tegevuste jaoks, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**.   |

##### <a name="message-processing-action-types"></a>Sõnumi töötlemise tegevuse tüübid

Väljal **Tegevuse tüüp** on saadaval järgmised suvandid.

- **Loo sõnum** – kasutage seda tüüpi, et kasutajad saaksid lehel **Elektronsõnum** käsitsi sõnumeid koostada. Seda tüüpi tegevuse jaoks ei saa esialgset olekut seadistada.
- **Kirjete asustamine** – eelnevalt peab olema seadistatud tegevus **kirjete asustamine**. Seostage see tegevusega, mille tüüp on **Kirjete asustamine**, et lubada selle kaasamine töötlemisse. Eeldatakse, et seda tegevuse tüüpi kasutatakse kas sõnumitöötluse esimeseks tegevuseks (kui pole ühtegi varem loodud elektronsõnumit) või tegevusena, millega lisatakse sõnumiüksuseid varem loodud sõnumile (tegevusega, mille tüüp on **Loo sõnum**). Seetõttu saab seda tüüpi tegevuse jaoks seadistada ainult sõnumiüksuste tulemuse oleku. Esialgse oleku saab seadistada ainult sõnumi jaoks.
- **Sõnumi täitmise tase** – kasutage seda tüüpi, et seadistada täidetav klass, mida tuleb hinnata sõnumi tasemel.
- **Sõnumiüksuse täitmise tase** – kasutage seda tüüpi, et seadistada täidetav klass, mida tuleb hinnata sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimine** – kasutage seda tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval ER-i konfiguratsioonil sõnumiüksuse tasemel.
- **Elektroonilise aruandluse eksportimissõnum** – kasutage seda tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb eksporditaval ER-i konfiguratsioonil sõnumi tasemel (näiteks kui sõnumil pole sõnumiüksusi).
- **Elektroonilise aruandluse importimine** – kasutage seda tüüpi tegevuste jaoks, mis peavad looma aruande, mis põhineb imporditaval ER-i konfiguratsioonil.
- **Kasutaja töötlemine sõnumi tasemel** – kasutage seda tüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab midagi käsitsi tegema. Näiteks võib kasutaja uuendada sõnumite olekut.
- **Kasutaja töötlemine** – kasutage seda tüüpi tegevuste jaoks, mis eeldavad, et kasutaja peab midagi käsitsi tegema. Näiteks võib kasutaja uuendada sõnumiüksuste olekut.
- **Veebiteenus** – kasutage seda tüüpi tegevuste jaoks, mis peavad loodud aruande edastama veebiteenusele. Seda tegevuse tüüpi ei kasutata itaalia ostu- ja müügiarvete suhtluse aruandluse jaoks. Tegevuste jaoks, mille tüüp on **Veebiteenus**, saate lehe **Sõnumi töötlemise tegevused** kiirkaardil **Mitmesugused andmed** määrata suvandi **Kinnitustekst**. See kinnitustekst kuvatakse kasutajale enne valitud veebiteenusele tehtud taotlusega tegelemist.
- **Kinnitamise taotlemine** – kasutage seda tüüpi kinnitamise taotlemiseks serverist.

#### <a name="initial-statuses-fasttab"></a>Kiirkaart Algolekud

> [!NOTE]
> Kiirkaart **Algolekud** pole saadaval tegevuste jaoks, mille esialgne tüüp on **Loo sõnum**.

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

Alljärgnev tabel näitlikustab, millised tulemuse olekud peab tegevuste tüüpidega seoses seadistatud.

| Elektronsõnumi tegevuse tüüp / Vastuse tüüp  | Täitmine õnnestus  | Äritõrge  | Tehniline tõrge  | Kasutaja määratud  | Loobu  |
|-------------------------------------------------|--------------|---------|-------|-----|-----------------|
| Loo sõnum                                  | X            |         |       |     |                 |
| Elektroonilise aruandluse eksportimine                     | X            |         |       |     |                 |
| Elektroonilise aruandluse importimine                     |              |         |       |     |                 |
| Veebiteenus                                     | X            |         | X     |     |                 |
| Kasutaja töötlemine                                 |              |         |       |     |                 |
| Sõnumi käivitamise tase                         |              |         |       |     |                 |
| Asustamiskirjed                                |              |         |       |     |                 |
| Sõnumiüksuse käivitamise tase                    |              |         |       |     |                 |
| Päringu kinnitamine                            | X            |  X      | X     |     |                 |
| Elektroonilise aruandluse eksportimissõnum             | X            |         |       |     |                 |
| Kasutaja töötlemine sõnumi tasemel                   |              |         |       |     |                 |

### <a name="electronic-message-processing"></a>Elektronsõnumi töötlemine

Elektronsõnumi töötlemine on elektronsõnumite funktsiooni põhikontseptsioon. See koondab tegevused, mida tuleb elektronsõnumi saamiseks hinnata. Tegevusi saab siduda esialgse oleku ja tulemuse oleku kaudu. Teise võimalusena saab tüübiga **Kasutaja töötlemine** tegevusi alustada sõltumatult. Samuti saate lehel **Elektronsõnumi töötlemine** (**Maks** \> **Seadistamine** \> **Elektronsõnumid** \> **Elektronsõnumi töötlemine**) valida lisavälju, mida tuleb töötlemise jaoks toetada kas sõnumi tasemel või sõnumiüksuste tasemel.

Kiirkaart **Tegevus** võimaldab teil töötlemisele lisada eelmääratletud tegevusi. Saate määrata, kas tegevus peab käivitama eraldi või kas selle saab käivitada töötlemisega. Selleks, et määrata tegevuse käivitamine ainult kasutaja poolt, märkige töötluses oleva tegevuse jaoks ruut **Käivita eraldi**. Eemaldage parameetri **Käivita eraldi** ruudust märge, kui soovite, et töötlemine käivitaks tegevuse, kui sõnumid või sõnumiüksused on olekus, mis on määratud selle tegevuse esialgseks olekuks. Tegevust, mille tüüp on **Kasutaja tegevus**, peab ainult käivitama eraldi. 

Mõnikord võib olla seda vaja mitme tegevuse koondamiseks jadasse, isegi kui esimene neist on määratud eraldi käivituma. Näiteks kui on nõutud, et aruande loomise peab käivitama kasutaja, kuid loodud aruande peab kohe saatma veebiteenusele ja veebiteenuselt saadud vastus peab kajastuma süsteemis. Selleks saate kasutada suvandit **Eraldamatu jada**. Selleks klõpsake lehe **Elektronsõnumi töötlemine** kiirkaardi **Tegevus** toimingupaani nuppu **Eraldamatu jada**, looge jada ja valige see veerust **Eraldamatu jada** nende tegevuste jaoks, mis peavad alati koos käivituma. Sellisel juhul saab seadistada esimese tegevuse parameetriks **Käivita eraldi**, aga mitte ülejäänutel.

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
- **Kogu andmeid** – see nupp on seotud tegevusega, mille tüüp on **Kirjete asutamine**.
- **Loo aruanne** – see nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse eksportimissõnum**.
- **Saada aruanne** – see nupp on seotud tegevustega, mille tüüp on **Veebiteenus**.
- **Impordi vastus** – see nupp on seotud tegevustega, mille tüüp on **Elektroonilise aruandluse importimine**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine sõnumi tasemel**.
- **Sõnumiüksused** – avab lehe **Elektronsõnumi üksused**.

Kiirkaart **Tegevuste logi** kuvab teabe kõigi tegevuste kohta, mis on valitud sõnumi jaoks käivitatud. Kui tegevuse tulemusel tekkis tõrge, lisatakse teave tõrke kohta seotud tegevuse logireale. Valige rida ja klõpsake tõrke kohta teabe vaatamiseks lehe ülemises paremas nurgas asuvat nuppu **Klipp**.

Kiirkaart **Sõnumi lisaväljad** kuvab kõik lisaväljad, mis on sõnumite jaoks määratletud töötlemise seadistuses. See kuvab ka nende lisaväljade väärtused.

Kiirkaart **Sõnumiüksused** kuvab kõik sõnumiüksused, mis on seotud valitud sõnumiga. Iga sõnumiüksuse jaoks saab olenevalt sõnumiüksuse olekust kasutada järgmisi funktsioone:

- **Kustuta** – see nupp on saadaval, kui valitud sõnumiüksuse praeguse oleku jaoks on valitud märkeruut **Luba kustutamine**.
- **Värskenda olekut** – see nupp on seotud tegevustega, mille tüüp on **Kasutaja töötlemine**.
- **Algdokument** – see nupp võimaldab kasutajal avada lehel, millel on valitud sõnumi algdokument.

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
