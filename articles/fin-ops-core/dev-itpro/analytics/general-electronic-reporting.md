---
title: Elektroonilise aruandluse (ER) ülevaade
description: See artikkel annab ülevaate elektroonilise aruandluse tööriistast. See kirjeldab põhimõisteid, toetatud stsenaariume ja vorminguid, mis on lahenduse osaks.
author: NickSelin
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "58941"
- intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f3853e0c1da0a5abb3f92171370cc4aeabbd829
ms.sourcegitcommit: 3289478a05040910f356baf1995ce0523d347368
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 07/01/2022
ms.locfileid: "9109576"
---
# <a name="electronic-reporting-er-overview"></a>Elektroonilise aruandluse (ER) ülevaade

[!include [banner](../includes/banner.md)]

Artikkel annab ülevaate elektroonilise aruandluse (ER) tööriista kohta. Artikkel sisaldab teavet põhimõistete kohta, ER-i toetatavaid stsenaariume ja loendit vormingutest, mis on loodud ja välja antud lahenduse osana.

ER on konfigureeritav tööriist, mis aitab teil luua ja hallata regulatiivset elektroonilist aruandlust ja makseid. See põhineb kolmel mõistel:

- Kodeerimise asemel konfiguratsioon:

    - Konfiguratsiooni saab teha ärikasutaja ja see ei vaja arendajat.
    - Andmemudel on määratletud äritingimustes.
    - Visuaalseid redaktoreid kasutatakse ER-i konfiguratsiooni kõigi komponentide loomiseks.
    - Andmete teisendamiseks kasutatav keel sarnaneb kasutatava keelega Microsoft Excel.

- Üks konfiguratsioon mitmele Dynamics 365 finantsi väljalasele:

    - Hallake ühte domeeniomast ärieesmärgil määratletud andmemudelit.
    - Eralda rakenduse vabastamise üksikasjad vabastamissõltuvuse andmemudeli vastendustes.
    - Saate hallata andmemudelil põhinevat ühe vormingu konfiguratsiooni praeguse versiooni mitme väljaande jaoks.

- Lihtne või automaatne täiendamine:

    - Toetatakse ER-i konfiguratsioonide versioonimist.
    - Elutsükli Microsoft Dynamics teenuste (LCS) varateeki saab kasutada versioonivahetuseks ER-i konfiguratsioonide hoidlana.
    - Algsetel ER-konfiguratsioonidel põhinevaid lokaliseerimist saab juurutada tütarversioonidega.
    - ER-i konfiguratsioonipuud pakutakse tööriistana, mis aitab kontrollida versioonide sõltuvusi.
    - Erinevused lokaliseerimisel või delta konfiguratsioonil salvestatakse, et lubada algse ER-i konfiguratsiooni uuele versioonile automaatset täiendamist.
    - Lokaliseerimisversioonide automaatsel uuendamisel avastatud konflikte on lihtne käsitsi lahendada.

ER võimaldab teil määratleda elektroonilise vormingu struktuurid ja seejärel kirjeldada, kuidas struktuurid tuleb andmete ja algoritmide abil täita. Saate kasutada valemikeelt, mis sarnaneb andmeteisenduse Exceli keelele. Andmebaasi ja vormingu vastendamise hallatavamaks, taaskasutatavaks ja vormingumuudatustest sõltumatuks muutmisel tutvustatakse vahepealseid andmemudeli mõisteid. Mõiste võimaldab rakendusandmete peitmist vormingu vastenduses ja võimaldab ühte andmemudelit mitme vormingu vastenduse jaoks uuesti kasutada.

Saate ER-i kasutada nii sissetulevate kui väljaminevate elektrooniliste dokumentide vormingute konfigureerimiseks vastavalt erinevate riikide ja piirkondade juriidilistele nõuetele. ER võimaldab hallata neid vorminguid nende elutsükli jooksul. Näiteks saate võtta vastu õigusaktidega kehtestatud uusi nõudeid ja koostada nõutud vormingus äridokumente teabe elektrooniliseks vahetamiseks valitsusasutuste, pankade ja muude osapooltega.

ER-i mootor on suunatud arendajate asemel ärikasutajatele. Kuna seadistate koodi asemel vorminguid, on elektrooniliste dokumentide loomise ja kohandamise protsessid kiiremad ja lihtsamad.

ER toetab praegu töölehevorminguid TEXT, XML, JSON, Microsoft Word Microsoft Excel PDF, ja OPENXML.

## <a name="capabilities"></a>Võimalused

ER-i mootoril on järgmised võimalused.

- See esindab ühte ühiskasutuses tööriista elektroonilise aruandluse jaoks erinevates domeenides ja asendab üle 20 erineva mootori, mis teevad teatud tüüpi finantside ja toimingute elektroonilist aruandlust.
- See isoleerib aruande vormingu praegusest versioonist. Teisisõnu: seda vormingut saab rakendada erinevatele versioonidele.
- See toetab algsel vormingul põhineva kohandatud vormingu loomist. See sisaldab ka võimalusi kohandatud vormingu automaatseks versioonitäienduseks, kui algset vormingut muudetakse, kuna kasutusele on võetud lokaliseerimise/kohandamise nõuded.
- Sellest saab esmane standardtöövahend elektroonilise aruandluse lokaliseerimisnõuete toetamiseks – nii Microsofti kui ka Microsofti partnerite jaoks.
- See toetab võimalust levitada vorminguid partneritele ja klientidele Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu.

## <a name="key-concepts"></a>Põhimõisted

### <a name="main-data-flow"></a>Põhiandmete voog

[![ER-i põhiandmete voog.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="components"></a>Komponendid

ER toetab järgmist tüüpi komponente:

- Andmemudel
- Mudeli vastendamine
- Vorming
- Metaandmed

Lisateabe saamiseks vaadake [Elektroonilise aruandluse komponendid](er-overview-components.md).


#### <a name="component-versioning"></a>Komponendi versioonimine

ER-komponentide puhul toetatakse versioonimist. Järgmist töövoogu pakutakse ER-i komponentides muudatuste haldamiseks.

1. Algselt loodud versioon on märgitud versioonina **Mustand**. Seda versiooni saab redigeerida ja see on proovimiseks saadaval.
2. Versiooni **Mustand** saab teisendada versiooniks **Lõpule viidud**. Seda versiooni saab kasutada kohalikes aruandlusprotsessides.
3. Versiooni **Lõpule viidud** saab teisendada versiooniks **Jagatud**. See versioon avaldatakse LCS-is ja seda saab kasutada üldistes aruandlusprotsessides.
4. Versiooni **Jagatud** saab teisendada versiooniks **Katkestatud**. Seejärel saab selle versiooni kustutada.

Versioonid olekus **Lõpule viidud** või **Jagatud** on saadaval muuks andmevahetuseks. Nende olekutega komponentidega saab teha järgmisi toiminguid.

- Komponenti saab XML-vormingus järjestada ja eksportida XML-vormingus failina.
- Komponenti saab ümber järjestada ja importida rakenduse ER-komponendi uue versioonina.

#### <a name="component-date-effectivity"></a>Komponendi kehtivuskuupäev

ER-i komponendi versioonid on kehtivuskuupäevaga. ER-i komponendile saab määratleda kuupäeva **Kehtiv alates**, et määrata kuupäev, millal see komponent aruandlusprotsessides jõustub. Rakenduse seansi kuupäeva kasutatakse selleks, et määratleda, kas komponent kehtib käivitamiseks. Kui kindlal kuupäeval kehtib mitu versiooni, kasutatakse aruandlusprotsessides uusimat versiooni.

#### <a name="component-access"></a>Komponendi juurdepääs

Juurdepääs ER-i vormingu komponentidele sõltub ISO riigi/regiooni koodi seadistusest. Kui see seadistus on vormingu konfiguratsiooni valitud versiooni puhul tühi, on võimalik käitusajal igast ettevõttest vormingukomponendile juurde pääseda. kui see seadistus sisaldab ISO riigi/regiooni koode, siis on vormingukomponent saadaval ainult nendest ettevõtetest, millel on esmane aadress, mis on määratletud ühele vormingukomponendi ISO riigi/regiooni koodile.

Andmevormingu komponendi erinevatel versioonidel võivad olla erinevad ISO riigi/regiooni koodide sätted.

#### <a name="configuration"></a><a name="Configuration"></a>Konfiguratsioon

ER-i konfiguratsioon on konkreetse ER-i komponendi ümbris. See komponent võib olla andmemudeli komponent või vormingukomponent. Konfiguratsioon võib sisaldada ER-i komponendi erinevaid versioone. Iga konfiguratsiooni omanikuks on märgitud kindel konfiguratsiooni pakkuja. Konfiguratsiooni komponendi versiooni **Mustand** saab redigeerida, kui konfiguratsiooni omanik on valitud ER-i sätetes aktiivseks teenusepakkujaks.

Iga mudelikonfiguratsioon sisaldab andmemudeli komponenti. Uue vormingukonfiguratsiooni võib tuletada konkreetsest andmemudeli konfiguratsioonist. Loodud vormingukonfiguratsioon kuvatakse konfiguratsioonipuul algse andmemudeli konfiguratsiooni allüksusena.

Loodud vormingukonfiguratsioon sisaldab vormingukomponenti. Algse mudelikonfiguratsiooni andmemudeli komponent lisatakse vaike-andmeallikana automaatselt alamvormingu konfiguratsiooni vormingukomponenti.

Rakenduse ettevõtted jagavad ER-i konfiguratsiooni.

#### <a name="provider"></a><a name="Provider"></a>Pakkuja

ER-i pakkuja on osapoole ID, mida kasutatakse iga ER-i konfiguratsiooni autori (omaniku) tähistamiseks. ER võimaldab hallata konfiguratsioonipakkujate loendit. Vormingu konfiguratsioonid, mis vabastatakse elektrooniliste dokumentide jaoks finantside ja toimingute lahenduse osana, on märgitud Microsofti konfiguratsiooni pakkuja **omaks**.

Uue ER-i pakkuja registreerimise kohta saate juhised, kui esitate tegevusjuhise **Elektrooniline aruandlus. Konfiguratsioonipakkuja loomine ja aktiivseks märkimine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

#### <a name="repository"></a><a name="Repository"></a>Hoidla

ER-i hoidla talletab ER-i konfiguratsioone. Praegu toetatakse järgmisi elektroonilise aruandluse hoidlate tüüpe. 

- LCS-i ühine teek
- LCS-i projekt
- Failisüsteem
- RCS
- Operationsi ressursid
- Globaalne hoidla

**LCS-i ühise teegi** hoidla annab juurdepääsu konfiguratsioonide loendile teenuse Lifecycle Services (LCS) ühiste vahendite teegis. Seda tüüpi ER-i hoidlat saab registreerida ainult Microsofti pakkuja jaoks. LCS-i ühiste varade teegist saate importida ER-i konfiguratsioonide uusimaid versioone praegusesse eksemplari.

Hoidla **LCS-i projekt** võimaldab juurdepääsu konkreetsele LCS-i projekti konfiguratsiooniloendile (LCS-i projektivarade teegile), mis valiti hoidla registreerimisel. ER võimaldab ühiskasutatavate konfiguratsioonide üleslaadimist eksemplarist konkreetsesse hoidlasse **LCS-i projekt**. Konfiguratsioone saate LCS-projektihoidlast **importida** ka oma finantside ja toimingute rakenduste praegusesse eksemplari.

Hoidla **Failisüsteem** võimaldab juurdepääsu konfiguratsioonidele, mis asuvad XML-failidena AOS-i teenuse hostitud masina kohaliku failisüsteemi kindlas kaustas. Vajalik kaust valitakse hoidla registreerimise etapis. Saate importida konfiguratsioone hoidlast **Failisüsteem** praegusesse rakenduse eksemplari. 

Pange tähele, et hoidla tüübile pääseb juurde järgmistes keskkondades:

- arenduseks juurutatud pilves majutatavad keskkonnad (sisaldavad lisatud komplektide katsemudeleid)
- kohalikult juurutatud keskkonnad (kohapealsed)

Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) konfiguratsioonide importimine](./electronic-reporting-import-ger-configurations.md).

Hoidla **RCS-i** eksemplar võimaldab juurdepääsu konkreetsele [konfiguratsiooniteenuse (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) eksemplarile, mis valiti hoidla registreerimise etapis. ER võimaldab importida lõpule viidud või jagatud konfiguratsioone valitud RCS-i eksemplarist praeguse rakenduse eksemplarini, et saaksite neid kasutada elektrooniliseks aruandluseks.

Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) konfiguratsioonide importimine RCS-ist](./rcs-download-configurations.md).

**Globaalne hoidla** annab juurdepääsu globaalse hoidla [konfiguratsiooniteenuses](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) sisalduvate konfiguratsioonide loendile. Seda tüüpi ER-i hoidlat saab registreerida ainult Microsofti pakkuja jaoks. Globaalsest hoidlast saate importida ER-i konfiguratsioonide uusimaid versioone praegusesse eksemplari.

Lisateavet leiate teemast [Elektroonilise aruandluse (ER) konfiguratsioonide importimine konfiguratsiooniteenuse globaalsest hoidlast](./er-download-configurations-global-repo.md).

Hoidla **Operatsiooniressursid** võimaldab juurdepääsu konfiguratsioonide loendile, mille on algselt väljastanud Microsoft kui ER-i konfiguratsioonipakkuja rakenduse lahenduse osana. Need konfiguratsioonid saab importida praegusesse eksemplari ja kasutada elektroonilise aruandluse jaoks või ülesande näidisjuhiste esitamiseks. Neid saab kasutada ka täiendavaks lokaliseerimiseks ja kohandamiseks. Pange tähele, et Microsoft ER-i konfiguratsioonide uusimad versioonid tuleb importida LCS-i ühiste vahendite teegist, kasutades vastavat ER-i hoidlat.

Vajalikke hoidlaid **LCS-i projekt**, **Failisüsteem** ja **Regulatiivsed konfiguratsiooniteenused (RCS)** saab registreerida eraldi iga praeguse rakenduse eksemplari konfiguratsioonipakkuja kohta. Iga hoidla saab eraldada konkreetsele konfiguratsioonipakkujale.

## <a name="supported-scenarios"></a>Toetatud stsenaariumid

### <a name="building-a-data-model"></a>Andmemudeli loomine

ER pakub mudelikoosturit, mida saab kasutada konkreetsele äridomeenile andmemudeli koostamiseks. Kõiki domeenipõhiseid äriüksusi ja nendevahelisi suhteid saab esitleda andmemudelis hierarhilise struktuurina. 

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise andmemudeli kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="translating-data-model-content"></a>Andmemudeli sisu tõlkimine

Andmemudeli sisu (sildid ja kirjeldused) saab tõlkida teistesse keeltesse, mida rakendused toetavad. Andmemudeli sisu võib olla vaja tõlkida järgmistel põhjustel:

- selleks, et muuta see koostamisel arusaadavamaks teisi keeli rääkivatele vormingu koostajatele, kes kasutavad vormingukomponentide andmevastenduseks andmemudelit;
- et muuta sisu käitusajal kasutajasõbralikumaks, esitades viibad ja käitamisparameetrite spikri ning konfigureeritud kinnitusteated (tõrked ja hoiatused) sisselogitud kasutaja eelistatud keeles.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Andmemudeli vastenduste konfigureerimine väljaminevate dokumentide puhul

ER pakub mudelivastenduse koosturit, mis võimaldab kasutajatel vastendada koostatud andmemudeleid konkreetsete rakenduse andmeallikatega. Vastenduse põhjal imporditakse andmed käitusajal valitud andmeallikatest andmemudelisse. Seejärel kasutatakse andmemudelit väljaminevaid elektroonilisi dokumente loovate ER-vormingute abstraktse andmeallikana. 

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhised **Elektroonilise aruandluse mudeli vastenduse määratlemine ja andmeallikate valimine** ja **Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatega** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Andmemudeli vastenduste konfigureerimine sissetulevate dokumentide puhul

ER pakub mudelivastenduse koosturit, mis võimaldab kasutajatel vastendada koostatud andmemudeleid konkreetsete sihtüksustega. Näiteks saab andmemudeleid vastendada värskendatavate andmekomponentidega (tabelid, andmeüksused ja vaated). Vastenduse põhjal värskendatakse käitusajal andmeid, kasutades andmemudeli andmeid. ER-i vormingu abstraktse salvestusruumina on andmemudel täidetud sissetulevast elektroonilisest dokumendist imporditud andmetega. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Koostatud mudelikomponendi salvestamine mudelikonfiguratsioonina

ER suudab talletada koostatud andmemudeli koos seotud andmevastendustega praeguse eksemplari mudelikonfiguratsioonina. Järgmisel joonisel on näide seda tüüpi andmemudeli konfiguratsiooni (maksedomeeni andmemudeli konfiguratsiooni) kohta.

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatega** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Andmemudelit alusena kasutava vormingu koostamine

ER toetab vormingukoosturit, mida võite kasutada valitud äridomeenile elektroonilise dokumendi vormingu koostamiseks, valides aluseks mudelikomponendi. Sama ER-i vormingukoostur võimaldab teil vastendada vormingu, mille loote, valitud domeeni andmemudeli vastendusega andmeallikana. 

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise vormingu kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfiguratsiooni koostamine elektrooniliste dokumentide loomiseks töölehevormingus OPENXML

Elektroonilise dokumendi koostamiseks töölehevormingus OPENXML saab kasutada ER-i vormingukoosturit. 

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa). Malli importimise tegevusjuhise toimingu käigus kasutage mallina Exceli faili [Maksearuande mall (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Konfiguratsiooni koostamine elektrooniliste dokumentide loomiseks Wordi dokumendi vormingus

Elektroonilise dokumendi koostamiseks Wordi dokumendi vormingus saab kasutada ER-i vormingukoosturit. Järgmisel joonisel on näide seda tüüpi vormingu vastenduse kohta. Pange tähele, et see vorming taaskasutab olemasolevat elektroonilise aruandluse konfiguratsiooni, mis oli algselt mõeldud aruande väljundi loomiseks OPENXML-vormingus.

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis Elektrooniline aruandlus. Microsoft WORD-i vormingus aruannete loomiseks konfiguratsiooni koostamine (äriprotsessi 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) osa). Tegevusjuhise malli importimise toimingu käigus kasutage ER-vormingu mallidena järgmisi Wordi faile.

- [Maksearuande mall (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Maksearuande piiratud mall (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Konfiguratsiooni koostamine andmete importimiseks sissetulevatest elektroonilistest dokumentidest

ER-i vormingukoosturi abil saab kirjeldada elektroonilist dokumenti, mis on mõeldud andmete importimiseks XML- või tekstivormingus. Kavandatud vormingut kasutatakse sissetuleva dokumendi sõelumiseks. ER-i vormingu vastendamise koosturi abil saab määratleda kavandatud vormingu elementide sideme andmemudeliga. 

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis Nõutavate konfiguratsioonide loomine andmete importimiseks välisest failist (äriprotsessi 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) osa). Kasutage selle juhise esitamiseks järgmisi faile.

- [Elektroonilise aruandluse andmemudeli konfiguratsioon (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [Elektroonilise aruandluse vormingu konfiguratsioon (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [XML-vormingus sissetuleva dokumendi näidis (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Sissetuleva dokumendi andmete haldamise töövihiku näidis (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Koostatud vormingu komponendi talletamine vormingukonfiguratsioonis

ER suudab talletada koostatud vormingu koos konfigureeritud andmete vastendamistega praeguse eksemplari vormingukonfiguratsioonina. Eelneval joonisel on sellist tüüpi vormingukonfiguratsiooni näide (**BACS (UK)**, mis on konfiguratsiooni **Maksemudel** alamkonfiguratsioon). Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise vormingu kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Rahanduse konfigureerimine loodud vormingu ettevõttesiseseks kasutamiseks

Rakendust saab konfigureerida kasutama loodud vormingut elektrooniliste aruanne loomiseks. Viide loodud vormingu konfiguratsioonile tuleb määratleda konkreetse domeeni sätetes. Näiteks selleks, et hakata kasutama ER-i vormingukonfiguratsiooni elektrooniliste hankija maksete jaoks vormingus BACS, tuleb vormingukonfiguratsioonile viidata konkreetsetes makseviisides.

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses maksmiseks elektroonilise dokumendi loomiseks vormingu kasutamine** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

## <a name="handling-er-components"></a>ER-i komponentide käsitlemine

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER-i komponendi avaldamine LCS-is selle ettevõtteväliseks pakkumiseks (lokaliseerimine)

Loodud komponendi omanik (mudel või vorming) saab kasutada ER-i komponendi lõpule viidud versiooni avaldamiseks LCS-is. Selleks on vajalik praeguse ER-i konfiguratsiooni pakkuja hoidla tüüp **LCS-i projekt**. Kui komponendi lõpetatud versiooni olekuks on määratud väärtuse **LÕPULE VIIDUD** asemel väärtus **JAGATUD**, avaldatakse see versioon LCS-is. Kui komponent on LCS-i avaldatud, saab selle komponendi omanikust teenusepakkuja selle komponendi toetamiseks. Näiteks kui vormingukomponent on mõeldud juriidiliselt vajaliku elektroonilise dokumendi koostamiseks (nt lokaliseerimisstsenaariumi kohaselt), siis eeldatakse, et vorming hoitakse seadusemuudatustega kooskõlas ja teenusepakkuja väljastab komponendi uusi versioone, kui tekivad uued seadusandlikud nõudmised. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER-i komponendi importimine LCS-ist ettevõttesiseseks kasutamiseks

ER võimaldab importida ER-i komponente LCS-ist praegusesse eksemplari. Selleks on vajalik hoidla tüüp **LCS-i projekt**. Kui ER-i komponent on LCS-ist praegusesse eksemplari imporditud, saab selle eksemplari omanikust tarbija teenusele, mida pakub imporditud komponendi omanik (autor). Näiteks kui vormingukomponent on mõeldud rakenduse konkreetse elektroonilise dokumendi koostamiseks riigi-/regioonipõhises vormingus (lokaliseerimisstsenaarium), eeldatakse, et teenuse tarbija suudab hankida sellele vormingule tehtud värskendused, et hoida seda kooskõlas seaduse nõuetega. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Vormingu koostamine, valides aluseks muu vormingu (kohandamine)

ER võimaldab luua (tuletada) komponendi kehtivast LCS-ist imporditud versioonist (alusest) uue komponendi. Näiteks oletame, et kasutaja soovib tuletada uue vormingu mõne erinõude rakendamiseks elektroonilisele dokumendile (nt lisaväli või põhjalik kirjeldus), et toetada kohandamisstsenaariumi. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses vormingu versiooni uuendamine, kasutades selle alusversiooni** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Vormingu versiooni uuendamine, valides alusvormingu uue versiooni ( aluse muutmine)

ER võimaldab võtta automaatselt kasutusele aluskomponendi uusima versiooni muudatused praeguses tuletatud komponendi mustandiversioonis. Seda protsessi nimetatakse *aluse muutmiseks*. Näiteks uue seadusandluse muudatuse, mis on võetud kasutusele LCS-ist imporditud vormingu uusimas versioonis, saab ühendada automaatselt elektroonilise dokumendi kohandatud versiooniga. Kõiki muudatusi, mida ei saa automaatselt ühendada, käsitletakse konfliktidena. Need konfliktid esitatakse sobiva komponendi koosturis käsitsi lahendamiseks. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses vormingu versiooni värskendamine, kasutades selle vormingu alusversiooni** (osa äriprotsessist **7.5.5.3 Muudetud IT-teenuse/-lahenduse komponendi hankimine/arendamine (10683)**).

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Rakenduses Finance väljastatud ER-i konfiguratsioonide loend

Rakenduse Finance ER-i konfiguratsioonide loendit värskendatakse pidevalt. Avage [Globaalne hoidla](er-download-configurations-global-repo.md), et vaadata praegu toetatud ER-i konfiguratsioonide loendit. Kiirkaardil **Kasutuselt kõrvaldamise üksikasjad** saate vaadata läbi teabe konfiguratsioonide kohta, mis on kasutuselt kõrvaldatud või mida enam ei hooldata. 

![Globaalse hoidla sisu konfiguratsioonihoidla lehel.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) konfiguratsioonide loomine](electronic-reporting-configuration.md)
- [Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

