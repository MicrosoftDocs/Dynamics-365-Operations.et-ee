---
title: Elektrooniline aruandlus (ER)
description: Teema annab ülevaate elektroonilise aruandluse (ER) tööriista kohta. Artikkel sisaldab teavet põhimõistete kohta, ER-i toetatavaid stsenaariume ja loendit vormingutest, mis on loodud ja välja antud lahenduse osana.
author: NickSelin
manager: AnnBe
ms.date: 03/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9504af391656e2515d34d18a15fab74f1698fa2
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849481"
---
# <a name="electronic-reporting-er"></a>Elektrooniline aruandlus (ER)

[!include [banner](../includes/banner.md)]

Teema annab ülevaate elektroonilise aruandluse (ER) tööriista kohta. Artikkel sisaldab teavet põhimõistete kohta, ER-i toetatavaid stsenaariume ja loendit vormingutest, mis on loodud ja välja antud lahenduse osana.

ER on tööriist, mille abil saate seadistada nii sissetulevate kui ka väljaminevate elektrooniliste dokumentide vorminguid mitmesuguste riikide/regioonide seadusenõuete kohaselt. ER võimaldab hallata neid vorminguid nende elutsükli jooksul. Näiteks saate võtta vastu õigusaktidega kehtestatud uusi nõudeid ja koostada nõutud vormingus äridokumente teabe elektrooniliseks vahetamiseks valitsusasutuste, pankade ja muude osapooltega.

ER-i mootor on suunatud arendajate asemel ärikasutajatele. Kuna seadistate koodi asemel vorminguid, on elektrooniliste dokumentide loomise ja kohandamise protsessid kiiremad ja lihtsamad.

ER toetab praegu töölehevorminguid TEXT, XML, Microsoft Wordi dokument ja OPENXML. Kuid laiendusliides toetab täiendavaid vorminguid.

## <a name="capabilities"></a>Võimalused
ER-i mootoril on järgmised võimalused.

- See on üks ühiskasutatav tööriist elektrooniliseks aruandluseks erinevates domeenides ja asendab enam kui 20 erinevat mootorit, mis rakenduses Microsoft Dynamics 365 for Finance and Operations teatud tüüpi elektroonilise aruandlusega tegelevad.
- See isoleerib aruande vormingu praegusest rakenduse Finance and Operations juurutusest. Teisisõnu saab seda vormingut rakendada Finance and Operations erinevatele versioonidele.
- See toetab algsel vormingul põhineva kohandatud vormingu loomist. See sisaldab ka võimalusi kohandatud vormingu automaatseks versioonitäienduseks, kui algset vormingut muudetakse, kuna kasutusele on võetud lokaliseerimise/kohandamise nõuded.
- Sellest saab esmane standardtöövahend elektroonilise aruandluse lokaliseerimisnõuete toetamiseks – nii Microsofti kui ka Microsofti partnerite jaoks.
- See toetab võimalust levitada vorminguid partneritele ja klientidele Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu.

## <a name="key-concepts"></a>Põhimõisted
### <a name="components"></a>Komponendid

ER toetab kahte tüüpi komponente: **Andmemudel** ja **Vorming**.

#### <a name="data-model-components"></a>Andmemudeli komponendid

Andmemudeli komponent on andmestruktuuri abstraktne kujutis. Seda kasutatakse konkreetse äridomeeni piirkonna kirjeldamiseks piisavalt üksikasjalikult, et rahuldada selle domeeni aruandlusvajadusi. Andmemudeli komponent koosneb järgmistest osadest:

- andmemudel domeenipõhiste äriüksuste kogumina ja nende üksuste vaheline hierarhiliselt struktureeritud suhtemääratlus;
- mudeli vastendus, mis seob valitud Finance and Operationsi andmeallikad andmemudeli eraldi elementidega, mis määrab käitusajal andmemudelikomponendile andmevoo ja äriandmete asustamise reeglid.

Andmemudeli äriüksus on esindatud konteinerina (kirje). Äriüksuse atribuudid on esindatud andmeüksustena (väljad). Igal andmeüksusel on kordumatu nimi, silt, kirjeldus ja väärtus. Iga andmeüksuse väärtus võib olla sellise ülesehitusega, et see tuvastatakse stringi, täisarvu, reaalarvu, kuupäeva, loetelu, kahendväärtusena jne. See võib olla ka teine kirje või kirjete loend.

Üksik andmemudeli komponent võib sisaldada mitut domeenipõhiste äriüksuste hierarhiat. See võib sisaldada ka mudelivastendusi, mis toetavad käitusajal aruandepõhist andmevoogu. Hierarhiaid eristatakse ühe kirjega, mis on valitud mudelivastenduse juurena. Näiteks võib maksedomeeni ala andmemudel toetada järgmisi vastendusi:

- Ettevõte \> Hankija \> AP-domeeni maksekanded
- Klient \> Ettevõte \> AR-domeeni maksekanded

Arvestage, et äriüksused (nt ettevõte ja maksekanded) kavandatakse ühe korra. Seejärel kasutavad neid erinevad vastendused.

Väljaminevaid elektroonilisi dokumente toetaval mudelivastendusel on järgmised võimalused.

- See võib kasutada andmemudeli andmeallikatena erinevaid Finance and Operationsi andmetüüpe. Näiteks võib see kasutada tabeleid, andmeüksus, meetodeid või loetelusid.
- See toetab kasutaja sisendparameetreid, mida saab määratleda andmemudeli andmeallikatena, kui mõningad andmed on vaja määratleda käitusajal.
- See toetab Finance and Operationsi andmete teisendamist vajalikesse gruppidesse. Samuti võimaldab see filtreerida, sortida ja summeerida andmeid ning lisada loogilisi arvutatud välju, mis on kavandatud Microsoft Exceli valemitele sarnanevate valemite kaudu, nagu on näidatud järgmisel illustratsioonil. Lisateavet leiate jaotisest [Valemikoostaja elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)).

[![Valemikoostaja](./media/ER-overview-01.png)](./media/ER-overview-01.png)

Sissetulevaid elektroonilisi dokumente toetaval mudelivastendusel on järgmised võimalused.

- See saab kasutada sihtidena erinevaid värskendatavaid andmeelemente. Nende andmeelementide hulka kuuluvad tabelid, andmeüksused ja vaated. Andmeid saab uuendada sissetulevate elektrooniliste dokumentide andmete abil. Ühe mudeli vastenduses saab kasutada mitut sihtüksust.
- See toetab kasutaja sisendparameetreid, mida saab määratleda andmemudeli andmeallikatena, kui mõningad andmed on vaja määratleda käitusajal.

Andmemudeli komponent on kavandatud igale äridomeenile, mida tuleks kasutada ühtlustatud andmeallikana aruandluse jaoks, mis eraldab aruandluse andmeallikate füüsilisest juurutusest. See kajastab domeenipõhiseid ärikontseptsioone ja funktsioone sellisel kujul, mis teeb aruandlusvormingu algse koostamise ja edasise haldamise tõhusamaks.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Väljaminevate elektrooniliste dokumentide vormingukomponendid

Vormingu komponent on käitusajal loodava aruandlusväljundi skeem. Skeem koosneb järgmistest osadest:

- vorming, mis määratleb käitusajal loodud väljamineva elektroonilise dokumendi struktuuri ja sisu;
- andmeallikad kasutaja väljundi parameetrite ja domeenipõhise andmemudeli kogumina, mis kasutab valitud mudelivastendust;
- vormingu vastendamine vormingu andmeallikate seoste kogumina, millel on vormingu üksikud elemendid, mis määravad käitusajal andmevoo ja vormingu väljundi loomise reeglid;
- vormingu kinnitamine konfigureeritavate reeglite kogumina, mis juhib käitamisel aruande loomist olenevalt käitatavast kontekstist. Näiteks võib olla olemas reegel, mis peatab hankija maksete väljundi loomise ja annab erandi, kui valitud hankija konkreetsed atribuudid (nt pangakonto number) on puudu.

Vormingukomponent toetab järgmisi funktsioone.

- Aruandluse väljundi loomine eraldi failidega mitmesugustes vormingutes, nt tekst, XML, Microsoft Wordi dokument või tööleht.
- Mitme faili eraldi loomine ja nende failide kapseldamine zip-failidesse.

Vormingukomponent võimaldab manustada konkreetseid faile, mida saab aruandlusväljundis järgmiselt kasutada:

- Exceli töövihikud, mis sisaldavad töölehte, mida saab kasutada töölehevormingu OPENXML väljundi mallina;
- Wordi failid, mis sisaldavad dokumenti, mida saab kasutada Microsoft Wordi dokumendivormingu väljundi mallina;
- muud failid, mida saab vormingu väljundisse eelmääratletud failidena lisada.

Järgmine illustratsioon näitab, kuidas andmed nende vormingute puhul liiguvad.

[![Väljaminevate vormingukomponentide andmevoog](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Ühe ER-vormingukonfiguratsiooni käitamiseks ja väljamineva elektroonilise dokumendi koostamiseks tuleb tuvastada vormingukonfiguratsiooni vastendus.

#### <a name="format-components-for-incoming-electronic-documents"></a>Sissetulevate elektrooniliste dokumentide vormingukomponendid
Vormingukomponent on käitusajal imporditava sissetuleva dokumendi skeem. Skeem koosneb järgmistest osadest:

- vorming, mis määratleb käitusajal imporditud andmeid sisaldava sissetuleva elektroonilise dokumendi struktuuri ja sisu. Vormingukomponenti kasutatakse sissetuleva dokumendi sõelumiseks mitmesugustes vormingutes, nt tekst ja XML.
- Vormi vastendus, mis seob eraldi vormielemente domeenipõhise andmemudeli elementidega. Käitusajal määravad andmemudeli elemendid andmevoo ja reeglid andmete importimiseks sissetulevast dokumendist ning salvestavad siis andmed andmemudelisse.
- Vormingu kinnitamine konfigureeritavate reeglite kogumina, mis juhib käitamisel andmete importimist olenevalt käitatavast kontekstist. Näiteks võib olla olemas reegel, mis peatab hankija maksetega pangaväljavõtte andmeimpordi ja annab erandi, kui hankija konkreetsed atribuudid (nt hankija ID-kood) on puudu.

Järgmine illustratsioon näitab, kuidas andmed nende vormingute puhul liiguvad.

[![Sissetulevate vormingukomponentide andmevoog](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Ühe ER-vormingukonfiguratsiooni käitamiseks, et importida andmeid sissetulevast elektroonilisest dokumendist, tuleb tuvastada vormingukonfiguratsiooni soovitud vastendus ja samuti mudeli vastenduse integratsioonipunkt. Sama mudeli vastendust ja sihtkohti saab kasutada koos erinevate vormingutega erinevat tüüpi sissetulevate dokumentide puhul.

#### <a name="component-versioning"></a>Komponendi versioonimine

ER-komponentide puhul toetatakse versioonimist. Järgmist töövoogu pakutakse ER-i komponentides muudatuste haldamiseks.

1. Algselt loodud versioon on märgitud versioonina **Mustand**. Seda versiooni saab redigeerida ja see on proovimiseks saadaval.
2. Versiooni **Mustand** saab teisendada versiooniks **Lõpule viidud**. Seda versiooni saab kasutada kohalikes aruandlusprotsessides.
3. Versiooni **Lõpule viidud** saab teisendada versiooniks **Jagatud**. See versioon avaldatakse LCS-is ja seda saab kasutada üldistes aruandlusprotsessides.
4. Versiooni **Jagatud** saab teisendada versiooniks **Katkestatud**. Seejärel saab selle versiooni kustutada.

Versioonid olekus **Lõpule viidud** või **Jagatud** on saadaval muuks andmevahetuseks. Nende olekutega komponentidega saab teha järgmisi toiminguid.

- Komponenti saab XML-vormingus järjestada ja eksportida XML-vormingus failina.
- Komponenti saab ümber järjestada ja importida Finance and Operationsi ER-komponendi uue versioonina.

#### <a name="component-date-effectivity"></a>Komponendi kehtivuskuupäev

ER-i komponendi versioonid on kehtivuskuupäevaga. ER-i komponendile saab määratleda kuupäeva **Kehtiv alates**, et määrata kuupäev, millal see komponent aruandlusprotsessides jõustub. Finance and Operationsi seansi kuupäeva kasutatakse selleks, et määratleda, kas komponent kehtib käivitamiseks. Kui kindlal kuupäeval kehtib mitu versiooni, kasutatakse aruandlusprotsessides uusimat versiooni.

#### <a name="component-access"></a>Komponendi juurdepääs

Juurdepääs ER-i vormingu komponentidele sõltub ISO riigi/regiooni koodi seadistusest. Kui see seadistus on vormingu konfiguratsiooni valitud versiooni puhul tühi, on võimalik käitusajal igast ettevõttest vormingukomponendile juurde pääseda. kui see seadistus sisaldab ISO riigi/regiooni koode, siis on vormingukomponent saadaval ainult nendest ettevõtetest, millel on esmane aadress, mis on määratletud ühele vormingukomponendi ISO riigi/regiooni koodile.

Andmevormingu komponendi erinevatel versioonidel võivad olla erinevad ISO riigi/regiooni koodide sätted.

#### <a name="configuration"></a>Konfiguratsioon

ER-i konfiguratsioon on konkreetse ER-i komponendi ümbris. See komponent võib olla andmemudeli komponent või vormingukomponent. Konfiguratsioon võib sisaldada ER-i komponendi erinevaid versioone. Iga konfiguratsiooni omanikuks on märgitud kindel konfiguratsiooni pakkuja. Konfiguratsiooni komponendi versiooni **Mustand** saab redigeerida, kui konfiguratsiooni omanik on valitud Finance and Operationsi ER-i sätetes aktiivseks teenusepakkujaks.

Iga mudelikonfiguratsioon sisaldab andmemudeli komponenti. Uue vormingukonfiguratsiooni võib tuletada konkreetsest andmemudeli konfiguratsioonist. Loodud vormingukonfiguratsioon kuvatakse konfiguratsioonipuul algse andmemudeli konfiguratsiooni allüksusena.

Loodud vormingukonfiguratsioon sisaldab vormingukomponenti. Algse mudelikonfiguratsiooni andmemudeli komponent lisatakse vaike-andmeallikana automaatselt alamvormingu konfiguratsiooni vormingukomponenti.

Finance and Operationsi ettevõtted kasutavad ER-i konfiguratsiooni ühiselt.

#### <a name="provider"></a>Pakkuja

ER-i pakkuja on osapoole ID, mida kasutatakse iga ER-i konfiguratsiooni autori (omaniku) tähistamiseks. ER võimaldab hallata konfiguratsioonipakkujate loendit. Elektroonilistele dokumentidele Finance and Operationsi lahenduse osana väljastatud vormingukonfiguratsioonide omanikuks märgitakse konfiguratsioonipakkuja **Microsoft**.

Uue ER-i pakkuja registreerimise kohta saate juhised, kui esitate tegevusjuhise **Elektrooniline aruandlus. Konfiguratsioonipakkuja loomine ja aktiivseks märkimine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

#### <a name="repository"></a>Hoidla

ER-i hoidla talletab ER-i konfiguratsioone. Praegu toetatakse järgmisi elektroonilise aruandluse hoidlate tüüpe. 

- LCS-i ühine teek
- LCS-i projekt
- Failisüsteem
- Regulatory Configuration Services (RCS)
- Operationsi ressursid


**LCS-i ühise teegi** hoidla annab juurdepääsu konfiguratsioonide loendile teenuse Lifecycle Services (LCS) ühiste vahendite teegis. Seda tüüpi ER-i hoidlat saab registreerida ainult Microsofti pakkuja jaoks. LCS-i ühiste varade teegist saate importida ER-i konfiguratsioonide uusimaid versioone praegusesse Finance and Operationsi eksemplari.

Hoidla **LCS-i projekt** võimaldab juurdepääsu konkreetsele LCS-i projekti konfiguratsiooniloendile (LCS-i projektivarade teegile), mis valiti hoidla registreerimise etapis. ER võimaldab ühiskasutatavate konfiguratsioonide üleslaadimist Finance and Operationsi eksemplarist konkreetsesse hoidlasse **LCS-i projekt**. Saate importida konfiguratsioone ka **LCS-i projekti** hoidlast praegusesse Finance and Operationsi eksemplari.

Hoidla **Failisüsteem** võimaldab juurdepääsu konfiguratsioonidele, mis asuvad XML-failidena AOS-i teenuse hostitud masina kohaliku failisüsteemi kindlas kaustas. Vajalik kaust valitakse hoidla registreerimise etapis. Saate importida konfiguratsioone hoidlast **Failisüsteem** praegusesse rakenduse Finance and Operations eksemplari. 

Pange tähele, et hoidla tüübile pääseb juurde järgmistes Dynamics 365 for Finance and Operationsi keskkondades:

- arenduseks juurutatud pilves majutatavad keskkonnad (sisaldavad lisatud komplektide katsemudeleid)
- kohalikult juurutatud keskkonnad (kohapealsed)

Lisateabe saamiseks vt teemat [Elektroonilise aruandluse (ER) konfiguratsioonide importimine](./electronic-reporting-import-ger-configurations.md).

Hoidla **RCS-i eksemplar** võimaldab juurdepääsu konkreetsele RCS-i eksemplarile, mis valiti hoidla registreerimise etapis. ER võimaldab importida lõpule viidud või jagatud konfiguratsioone valitud RCS-i eksemplarist praeguse rakenduse Finance and Operations eksemplarini, et saaksite neid kasutada elektrooniliseks aruandluseks.

Lisateavet leiate teemast [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](./rcs-download-configurations.md).

Hoidla **Operatsiooniressursid** võimaldab juurdepääsu konfiguratsioonide loendile, mille on algselt väljastanud Microsoft kui ER-i konfiguratsioonipakkuja Finance and Operationsi lahenduse osana. Need konfiguratsioonid saab importida praegusesse Finance and Operationsi eksemplari ja kasutada elektroonilise aruandluse jaoks või ülesande näidisjuhiste esitamiseks. Neid saab kasutada ka täiendavaks lokaliseerimiseks ja kohandamiseks. Pange tähele, et Microsoft ER-i konfiguratsioonide uusimad versioonid tuleb importida LCS-i ühiste vahendite teegist, kasutades vastavat ER-i hoidlat.

Vajalikke hoidlaid **LCS-i projekt**, **Failisüsteem** ja **Regulatiivsed konfiguratsiooniteenused (RCS)** saab registreerida eraldi iga praeguse rakenduse Finance and Operations eksemplari konfiguratsioonipakkuja kohta. Iga hoidla saab eraldada konkreetsele konfiguratsioonipakkujale.

## <a name="supported-scenarios"></a>Toetatud stsenaariumid
### <a name="building-a-data-model"></a>Andmemudeli loomine

ER pakub mudelikoosturit, mida saab kasutada konkreetsele äridomeenile andmemudeli koostamiseks. Kõiki domeenipõhiseid äriüksusi ja nendevahelisi suhteid saab esitleda andmemudelis hierarhilise struktuurina. Järgmisel joonisel on näide seda tüüpi andmemudeli (maksedomeeni andmemudeli) kohta.

[![Maksedomeeni andmemudel](./media/ER-overview-04.png)](./media/ER-overview-04.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise andmemudeli kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="translating-data-model-content"></a>Andmemudeli sisu tõlkimine

Andmemudeli sisu (sildid ja kirjeldused) saab tõlkida teistesse keeltesse, mida Finance and Operations toetab. Andmemudeli sisu võib olla vaja tõlkida järgmistel põhjustel:

- selleks, et muuta see koostamisel arusaadavamaks teisi keeli rääkivatele vormingu koostajatele, kes kasutavad vormingukomponentide andmevastenduseks andmemudelit;
- et muuta sisu käitusajal kasutajasõbralikumaks, esitades viibad ja käitamisparameetrite spikri ning konfigureeritud kinnitusteated (tõrked ja hoiatused) sisselogitud kasutaja eelistatud keeles.

Järgmisel joonisel on näide, milles andmemudeli sisu on tõlgitud inglise keelest jaapani keelde.

[![Andmemudeli sisu inglise keeles](./media/ER-overview-05.png)](./media/ER-overview-05.png)

[![Jaapani keelde tõlgitud andmemudeli sisu](./media/ER-overview-06.png)](./media/ER-overview-06.png)

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Andmemudeli vastenduste konfigureerimine väljaminevate dokumentide puhul

ER pakub mudelivastenduse koosturit, mis võimaldab kasutajatel vastendada koostatud andmemudeleid konkreetsete Finance and Operationsi andmeallikatega. Vastenduse põhjal imporditakse andmed käitusajal valitud andmeallikatest andmemudelisse. Seejärel kasutatakse andmemudelit väljaminevaid elektroonilisi dokumente loovate ER-vormingute abstraktse andmeallikana. Järgmisel illustratsioonil on sellise andmemudeli vastendamise näidis (**SEPA kreeditiülekande** mudeli vastendus maksedomeeni andmemudeliga).

[![Andmemudeli vastenduse näide](./media/ER-overview-07.png)](./media/ER-overview-07.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhised **Elektroonilise aruandluse mudeli vastenduse määratlemine ja andmeallikate valimine** ja **Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatega** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Andmemudeli vastenduste konfigureerimine sissetulevate dokumentide puhul
ER pakub mudelivastenduse koosturit, mis võimaldab kasutajatel vastendada koostatud andmemudeleid konkreetsete sihtüksustega. Näiteks saab andmemudeleid vastendada Finance and Operationsi värskendatavate andmekomponentidega (tabelid, andmeüksused ja vaated). Vastenduse põhjal värskendatakse käitusajal Finance and Operationsi andmeid, kasutades andmemudeli andmeid. ER-i vormingu abstraktse salvestusruumina on andmemudel täidetud sissetulevast elektroonilisest dokumendist imporditud andmetega. Järgmisel joonisel on näide seda tüüpi andmemudeli vastenduse kohta. Selles näites kasutatakse maksedomeeni andmemudeli mudelivastendust **NETS-i impordivastendus** Norra NETS-i vormingus pangaväljavõtete importimise toetamiseks.

[![Impordivastendus NETS-i andmemudeli näite puhul](./media/ER-overview-08.png)](./media/ER-overview-08.png)

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Koostatud mudelikomponendi salvestamine mudelikonfiguratsioonina

ER suudab talletada koostatud andmemudeli koos seotud andmevastendustega praeguse Finance and Operationsi eksemplari mudelikonfiguratsioonina. Järgmisel joonisel on näide seda tüüpi andmemudeli konfiguratsiooni (maksedomeeni andmemudeli konfiguratsiooni) kohta.

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatega** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Andmemudelit alusena kasutava vormingu koostamine

ER toetab vormingukoosturit, mida võite kasutada valitud äridomeenile elektroonilise dokumendi vormingu koostamiseks, valides aluseks mudelikomponendi. Sama ER-i vormingukoostur võimaldab teil vastendada vormingu, mille loote, valitud domeeni andmemudeli vastendusega andmeallikana. Järgmisel illustratsioonil on seda tüüpi vormingu näide (vormingukonfiguratsioon, mis toetab Ühendkuningriigi maksevormingut **BACS**).

[![Vormingu näide, mille alus on andmemudel](./media/ER-overview-09.png)](./media/ER-overview-09.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise vormingu kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfiguratsiooni koostamine elektrooniliste dokumentide loomiseks töölehevormingus OPENXML

Elektroonilise dokumendi koostamiseks töölehevormingus OPENXML saab kasutada ER-i vormingukoosturit. Järgmisel illustratsioonil on sellist tüüpi vormingu näide (vormingukonfiguratsioon OPENXML-töölehe loomiseks valitud maksetöölehe andmetega).

[![Pic-ER-format-Excel](./media/ER-overview-10.png)](./media/ER-overview-10.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa). Malli importimise tegevusjuhise toimingu käigus kasutage mallina Exceli faili [Maksearuande mall (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202).

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Konfiguratsiooni koostamine elektrooniliste dokumentide loomiseks Wordi dokumendi vormingus
Elektroonilise dokumendi koostamiseks Wordi dokumendi vormingus saab kasutada ER-i vormingukoosturit. Järgmisel joonisel on näide seda tüüpi vormingu vastenduse kohta. Pange tähele, et see vorming taaskasutab olemasolevat elektroonilise aruandluse konfiguratsiooni, mis oli algselt mõeldud aruande väljundi loomiseks OPENXML-vormingus.

[![Pic-ER-format-Word](./media/ER-overview-11.png)](./media/ER-overview-11.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis Elektrooniline aruandlus. Microsoft WORD-i vormingus aruannete loomiseks konfiguratsiooni koostamine (äriprotsessi 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) osa). Tegevusjuhise malli importimise toimingu käigus kasutage ER-vormingu mallidena järgmisi Wordi faile.

- [Maksearuande mall (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Maksearuande piiratud mall (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Konfiguratsiooni koostamine andmete importimiseks sissetulevatest elektroonilistest dokumentidest
ER-i vormingukoosturi abil saab kirjeldada elektroonilist dokumenti, mis on mõeldud andmete importimiseks XML- või tekstivormingus. Kavandatud vormingut kasutatakse sissetuleva dokumendi sõelumiseks. ER-i vormingu vastendamise koosturi abil saab määratleda kavandatud vormingu elementide sideme andmemudeliga. Järgmistel joonistel on näide seda tüüpi vormingu ja vorminguvastenduse kohta. Selles näites imporditakse NETS-i pangaväljavõtted, mis sisaldavad hankija makseandmeid teksti kujul.

[![ER-format-designer](./media/ER-overview-12.png)](./media/ER-overview-12.png)

[![ER-model-mapping-designer](./media/ER-overview-13.png)](./media/ER-overview-13.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis Nõutavate konfiguratsioonide loomine andmete importimiseks välisest failist (äriprotsessi 7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677) osa). Kasutage selle juhise esitamiseks järgmisi faile.

- [Elektroonilise aruandluse andmemudeli konfiguratsioon (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Elektroonilise aruandluse vormingu konfiguratsioon (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [XML-vormingus sissetuleva dokumendi näidis (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Sissetuleva dokumendi andmete haldamise töövihiku näidis (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Koostatud vormingu komponendi talletamine vormingukonfiguratsioonis

ER suudab talletada koostatud vormingu koos konfigureeritud andmete vastendamistega praeguse Finance and Operationsi eksemplari vormingukonfiguratsioonina. Eelneval joonisel on sellist tüüpi vormingukonfiguratsiooni näide (**BACS (UK)**, mis on konfiguratsiooni **Maksemudel** alamkonfiguratsioon). Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise vormingu kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="configuring-finance-and-operations-to-start-to-use-a-created-format-internally"></a>Finance and Operationsi konfigureerimine loodud vormingu ettevõttesiseseks kasutamiseks

Finance and Operationsit saab konfigureerida kasutama loodud vormingut elektrooniliste aruanne loomiseks. Viide loodud vormingu konfiguratsioonile tuleb määratleda konkreetse domeeni sätetes. Näiteks selleks, et hakata kasutama ER-i vormingukonfiguratsiooni elektrooniliste hankija maksete jaoks vormingus BACS, tuleb vormingukonfiguratsioonile viidata konkreetsetes makseviisides, nagu on näidatud järgmistel illustratsioonidel.

[![BACS (UK) vormingukonfiguratsioon](./media/ER-overview-14.png)](./media/ER-overview-14.png)

[![Vormingule BACS (UK) viitamine makseviisis](./media/ER-overview-15.png)](./media/ER-overview-15.png)

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses maksmiseks elektroonilise dokumendi loomiseks vormingu kasutamine** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

## <a name="handling-er-components"></a>ER-i komponentide käsitlemine
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER-i komponendi avaldamine LCS-is selle ettevõtteväliseks pakkumiseks (lokaliseerimine)

Loodud komponendi omanik (mudel või vorming) saab kasutada ER-i komponendi lõpule viidud versiooni avaldamiseks LCS-is. Selleks on vajalik praeguse ER-i konfiguratsiooni pakkuja hoidla tüüp **LCS-i projekt**. Kui komponendi lõpetatud versiooni olekuks on määratud väärtuse **LÕPULE VIIDUD** asemel väärtus **JAGATUD**, avaldatakse see versioon LCS-is. Kui komponent on LCS-i avaldatud, saab selle komponendi omanikust teenusepakkuja selle komponendi toetamiseks. Näiteks kui vormingukomponent on mõeldud juriidiliselt vajaliku elektroonilise dokumendi koostamiseks (nt lokaliseerimisstsenaariumi kohaselt), siis eeldatakse, et vorming hoitakse seadusemuudatustega kooskõlas ja teenusepakkuja väljastab komponendi uusi versioone, kui tekivad uued seadusandlikud nõudmised. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER-i komponendi importimine LCS-ist ettevõttesiseseks kasutamiseks

ER võimaldab importida ER-i komponente LCS-ist praegusesse Finance and Operationsi eksemplari. Selleks on vajalik hoidla tüüp **LCS-i projekt**. Kui ER-i komponent on LCS-ist praegusesse Finance and Operationsi eksemplari imporditud, saab selle eksemplari omanikust tarbija teenusele, mida pakub imporditud komponendi omanik (autor). Näiteks kui vormingukomponent on mõeldud Finance and Operationsist konkreetse elektroonilise dokumendi koostamiseks riigi-/regioonipõhises vormingus (lokaliseerimisstsenaarium), eeldatakse, et teenuse tarbija suudab hankida sellele vormingule tehtud uuendused, et hoida seda kooskõlas seaduse nõuetega. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Vormingu koostamine, valides aluseks muu vormingu (kohandamine)

ER võimaldab luua (tuletada) komponendi kehtivast LCS-ist imporditud versioonist (alusest) uue komponendi. Näiteks oletame, et kasutaja soovib tuletada uue vormingu mõne erinõude rakendamiseks elektroonilisele dokumendile (nt lisaväli või põhjalik kirjeldus), et toetada kohandamisstsenaariumi. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses vormingu versiooni uuendamine, kasutades selle alusversiooni** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Vormingu versiooni uuendamine, valides alusvormingu uue versiooni ( aluse muutmine)

ER võimaldab võtta automaatselt kasutusele aluskomponendi uusima versiooni muudatused praeguses tuletatud komponendi mustandiversioonis. Seda protsessi nimetatakse *aluse muutmiseks*. Näiteks uue seadusandluse muudatuse, mis on võetud kasutusele LCS-ist imporditud vormingu uusimas versioonis, saab ühendada automaatselt elektroonilise dokumendi kohandatud versiooniga. Kõiki muudatusi, mida ei saa automaatselt ühendada, käsitletakse konfliktidena. Need konfliktid esitatakse sobiva komponendi koosturis käsitsi lahendamiseks. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses vormingu versiooni värskendamine, kasutades selle vormingu alusversiooni** (osa äriprotsessist **7.5.5.3 Muudetud IT-teenuse/-lahenduse komponendi hankimine/arendamine (10683)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-and-operations-solution"></a>Finance and Operationsi lahenduses pakutavate ER-i konfiguratsioonide loend

| Valdkonnapõhise andmemudeli konfiguratsioonid: pealkiri | Domeen                | Andmemudel – sõltuva vormingu konfiguratsioonid: pealkiri | Kirjeldus                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Auditifaili mudel                                 | Finantsaudit       |                                                   |                                                                    |
|                                                  |                       | Auditifail (NL)                                   | Hollandi auditifaili vorming                                  |
| BAS-mudel                                        | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | Austraalia vorming BAS                                           |
| Ehitustööstuse skeemi mudel               | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | SRÜ igakuine tagastus (UK)                           | SRÜ igakuise tagastuse vorming Ühendkuningriigi puhul                   |
| Märgukirja mudel                          | Elektrooniline arveldamine  |                                                   |                                                                    |
|                                                  |                       | OIOUBL-i märgukiri (DK)                     | OIOUBL-i märgukirja vorming Taani puhul                        |
| Elektrooniline pearaamatu arvestusmudel (MX)          | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | Täiendav pearaamatu XML (MX)                         | Täiendavad pearaamatukanded kontoaruande vormingu kohta Mehhiko puhul |
|                                                  |                       | Kontoplaani XML (MX)                         | Kontoplaani aruande vorm Mehhiko puhul                          |
|                                                  |                       | Töölehtede XML (MX)                                 | Töölehekannete aruande vorm Mehhiko puhul                      |
|                                                  |                       | Proovibilansi XML (MX)                            | Proovibilansi aruande vorm Mehhiko puhul                             |
| Elsteri mudel                                     | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elsteri vorming Saksamaa puhul                                          |
| EL-i käibearuande mudel                              | Kaubandusaruanne       |                                                   |                                                                    |
|                                                  |                       | EL-i käibearuanne (DE)                                | EL-i käibearuande TXT-vorming Saksamaa puhul                               |
|                                                  |                       | EL-i käibearuanne (DK)                                | EL-i käibearuande TXT-vorming Taani puhul                               |
|                                                  |                       | EL-i käibearuanne (FR)                                | EL-i käibearuande XML-vorming Prantsusmaa puhul                                |
|                                                  |                       | EL-i käibearuanne (NL)                                | EL-i käibearuande XML-vorming Hollandi puhul                           |
|                                                  |                       | EL-i käibearuande TXT (UK)                            | EL-i käibearuande TXT-vorming Ühendkuningriigi puhul                    |
|                                                  |                       | EL-i käibearuande XML (UK)                            | EL-i käibearuande XML-vorming Ühendkuningriigi puhul                    |
|                                                  |                       | EL-i käibearuanne veergude kaupa                   | EL-i käibearuanne veergude kaupa                                    |
|                                                  |                       | EL-i käibearuanne ridade kaupa                      | EL-i käibearuanne ridade kaupa                                       |
| FEC arvestusmudel (FR)                        | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | FEC raamatupidamisandmete XML (FR)                      | FEC raamatupidamisandmete ekspordi XML-vorming Prantsusmaa puhul                   |
| Saksamaa auditifail                                | Finantsaudit       |                                                   |                                                                    |
|                                                  |                       | Saksamaa auditifaili väljund                          | Auditifaili väljund Saksamaa ja Austria puhul                          |
| Intrastati mudel                                  | Kaubandusaruanne       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastati vorming Saksamaa puhul                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastati vorming Taani puhul                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastati vorming INTRACOM Prantsusmaa puhul                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastati vorming SAISUNIC Prantsusmaa puhul                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastati vorming Hollandi puhul                               |
|                                                  |                       | Intrastat (UK)                                    | Intrastati vorming Ühendkuningriigi puhul                            |
|                                                  |                       | Intrastat-aruanne                                  | Intrastati Exceli kontrollaruanne                                     |
| Kliendiarve mudel                           | Elektrooniline arveldamine  |                                                   |                                                                    |
|                                                  |                       | OIOUBL-i projekti kreeditarve (DK)                   | OIOUBL-i projekti kreeditarve vorming Taani puhul                      |
|                                                  |                       | OIOUBL-i projektiarve (DK)                       | OIOUBL-i projektiarve vorming Taani puhul                          |
|                                                  |                       | OIOUBL-i müügi kreeditarve (DK)                     | OIOUBL-i müügi kreeditarve vorming Taani puhul                        |
|                                                  |                       | OIOUBL-i müügiarve (DK)                         | OIOUBL-i müügiarve vorming Taani puhul                            |
| OB deklaratsiooni mudel                             | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | OB deklaratsiooni number (NL)                               | OB deklaratsiooni vorming Hollandi puhul                          |
| Maksemudel                                    | Maksed              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice’i maksevorming Taani puhul                        |
|                                                  |                       | Käskveksli rahaülekanne (FR)                  | Käskveksli rahaülekande vorming Prantsusmaa puhul                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91 hankija maksevorming Hollandi puhul                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB otsekorralduse maksevorming Prantsusmaa puhul                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB siseriikliku hankija maksevorming Prantsusmaa puhul                    |
|                                                  |                       | Nordea hankija (DK)                                | Nordea Corporate Netbanki hankija maksevorming Taani puhul         |
|                                                  |                       | ANZ otsekreediti teenus (AU)                    | ANZ otsekreediti teenuse vorming Austraalia puhul                 |
|                                                  |                       | CBA otsekreediti teenus (AU)                    | CBA otsekreediti teenuse vorming Austraalia puhul                 |
|                                                  |                       | NAB otsekreediti teenus (AU)                    | NAB otsekreediti teenuse vorming Austraalia puhul                 |
|                                                  |                       | STG otsekreediti teenus (AU)                    | STG otsekreediti teenuse vorming Austraalia puhul                 |
|                                                  |                       | WBC otsesisestuse süsteem (AU)                      | WBC otsesisestuse süsteemi vorming Austraalia puhul                   |
|                                                  |                       | DirectLink (NZ)                                   | DirectLinki vorming Uus-Meremaa puhul                              |
|                                                  |                       | JBA maksefail (JP)                             | JBA maksevorming Jaapani puhul                                       |
|                                                  |                       | ISO20022 kreeditiülekanne                          | SEPA kreeditiülekande vorming Euroopa puhul                             |
|                                                  |                       | ISO20022 kreeditiülekanne (FR)                     | SEPA kreeditiülekande vorming Prantsusmaa puhul                             |
|                                                  |                       | ISO20022 kreeditiülekanne (DE)                     | SEPA kreeditiülekande vorming Saksamaa puhul                            |
|                                                  |                       | ISO20022 kreeditiülekanne (NL)                     | SEPA kreeditiülekande vorming Hollandi puhul                    |
|                                                  |                       | ISO20022 otsedeebet                             | SEPA otsedeebeti vorming Euroopa puhul                                |
|                                                  |                       | ISO20022 otsedeebet (FR)                        | SEPA otsedeebeti vorming Prantsusmaa puhul                                |
|                                                  |                       | ISO20022 otsedeebet (DE)                        | SEPA otsedeebeti vorming Saksamaa puhul                               |
|                                                  |                       | ISO20022 otsedeebet (NL)                        | SEPA otsedeebeti vorming Hollandi puhul                       |
|                                                  |                       | BACS (UK)                                         | Hankija makse BACS-vorming Ühendkuningriigi puhul                  |
| Pöördtasu                                   | Maksuaruanne         |                                                   |                                                                    |
|                                                  |                       | Pöördtasu müügiloend                         | Pöördtasu müügiloendi vorming                                   |
| Hollandi integreerimismudel XBRL                     | XBRL-aruandlus        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Hollandi ekspordivorming Semansys XBRL                    |
| GAF-mudel (MY)                                   | Finantsaudit       |                                                   |                                                                    |
|                                                  |                       | GAF-fail (MY)                                     | Malaisia vorming GAF                                         |
| Hankija ajalise jaotuse aruanne (CN)                         | Hankija andmete analüüs |                                                   |                                                                    |
|                                                  |                       | Hankija ajalise jaotuse aruande vorming (CN)                   | Hankija ajalise jaotuse aruande vorming Hiina puhul                               |
| Hankija arve deklaratsiooni mudel                 | Hankija andmete analüüs |                                                   |                                                                    |
|                                                  |                       | Hankija arve deklaratsioon (IS)                   | Hankija arve deklaratsiooni vorm Islandi puhul                      |
|                                                  |                       | Hankija arve deklaratsiooni aruanne (IS)            | Hankija arve deklaratsiooni aruanne Islandi puhul                      |

## <a name="additional-resources"></a>Lisaressursid

- [Lokaliseerimisnõuded – Elektroonilise aruandluse konfiguratsiooni loomine](electronic-reporting-configuration.md)
- [Elektroonilise aruandluse konfiguratsiooni elutsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md)
