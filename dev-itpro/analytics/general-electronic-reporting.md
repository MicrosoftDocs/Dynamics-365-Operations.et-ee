---
title: "Elektroonilise aruandluse ülevaade"
description: "Artikkel annab ülevaate elektroonilise aruandluse (ER) tööriista kohta. Artikkel sisaldab teavet põhimõistete kohta, ER-i toetatavaid stsenaariume ja loendit vormingutest, mis on loodud ja välja antud lahenduse osana."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: abe9212372fb7429d68c1fb6b32ec1d15c20a6d7
ms.contentlocale: et-ee
ms.lasthandoff: 04/25/2017


---

# <a name="electronic-reporting-overview"></a>Elektroonilise aruandluse ülevaade

[!include[banner](../includes/banner.md)]


Artikkel annab ülevaate elektroonilise aruandluse (ER) tööriista kohta. Artikkel sisaldab teavet põhimõistete kohta, ER-i toetatavaid stsenaariume ja loendit vormingutest, mis on loodud ja välja antud lahenduse osana.

Elektrooniline aruandlus (ER) on vahend, mille abil saate seadistada elektrooniliste dokumentide vorminguid mitmesuguste riikide/regioonide seadusenõuete kohaselt. ER võimaldab hallata neid vorminguid nende elutsükli jooksul. Näiteks saate võtta vastu õigusaktidega kehtestatud uusi nõudeid ja koostada nõutud vormingus äridokumente teabe elektrooniliseks vahetamiseks valitsusasutuste, pankade ja muude osapooltega. ER-i mootor on suunatud arendajate asemel ärikasutajatele. Kuna seadistate vorminguid ja mitte koodi, on elektrooniliste dokumentide loomise ja kohandamise protsessid kiiremad ja lihtsamad. ER toetab praegu töölehevorminguid TEXT, XML ja OPENXML. Kuid laiendusliides toetab suuremat vormingute arvu.

## <a name="capabilities"></a>Võimalused
ER-i mootoril on järgmised võimalused.

-   See on üks ühtne tööriist elektrooniliseks aruandluseks erinevates domeenides ja asendab enam kui 20 erinevat mootorit, mis Microsoft Dynamics 365 for Operationsis teatud tüüpi elektroonilise aruandlusega tegelevad.
-   See isoleerib aruande vormingu praegusest Dynamics 365 for Operationsi versioonist. (Teisisõnu: seda vormingut saab rakendada Dynamics 365 for Operationsi erinevatele versioonidele.)
-   See toetab algsel vormingul põhineva kohandatud vormingu loomist. See sisaldab võimalusi kohandatud vormingu automaatseks versioonitäienduseks, kui algses vormingus tehakse muudatusi, kuna kasutusele on võetud lokaliseerimise/kohandamise nõuded.
-   Sellest saab esmane standardtöövahend elektroonilise aruandluse lokaliseerimisnõuete toetamiseks – nii Microsofti kui ka Microsofti partnerite jaoks.
-   See toetab võimalust levitada vorminguid partneritele ja klientidele Microsoft Dynamicsi teenuse Lifecycle Services (LCS) kaudu.

## <a name="concepts"></a>Mõisted
### <a name="components"></a>Komponendid

ER toetab kahte tüüpi komponente: **Andmemudel**ja **Vorming**.

#### <a name="data-model-components"></a>Andmemudeli komponendid

Andmemudeli komponent on andmestruktuuri abstraktne esitus ja seda kasutatakse teatud äridomeeni piirkonna kirjeldamiseks piisava üksikasjalikkusega, et rahuldada selle domeeni aruandluse nõudeid. Andmemudeli komponent koosneb järgmistest osadest:

-   andmemudel domeenipõhiste äriüksuste kogumina ja nende üksuste vaheline hierarhiliselt struktureeritud suhtemääratlus;
-   mudeli vastendus, mis seob valitud Microsoft Dynamics 365 for Operationsi andmeallikad andmemudeli eraldi elementidega, mis määrab käitusajal andmemudelikomponendile andmevoo ja äriandmete populatsiooni reeglid.

Andmemudeli äriüksus on esindatud konteinerina (kirje). Äriüksuse atribuudid on esindatud andmeüksustena (väljad). Igal andmeüksusel on kordumatu nimi, silt, kirjeldus ja väärtus. Iga andmeüksuse väärtus võib olla sellise ülesehitusega, et see tuvastatakse stringi, täisarvu, reaalarvu, kuupäeva, loetelu tüübi, kahendväärtusena jne, . See võib olla ka teine kirje või kirjete loend. Üksik andmemudelikomponent võib sisaldada mitmeid domeenipõhiste äriüksuste hierarhiaid ja mudelivastendusi, mis toetavad käitamisel konkreetse aruande põhist andmevoogu. Hierarhiaid eristatakse ühe kirjega, mis on valitud mudelivastenduse juurena. Näiteks võib maksedomeeni ala andmemudel toetada järgmisi vastendusi:

-   ettevõte -&gt; hankija -&gt; AP-domeeni maksekanded
-   klient -&gt; ettevõte -&gt; AR-domeeni maksekanded

Arvestage, et äriüksused (nt ettevõte ja maksekanded) kavandatakse ühe korra. Seejärel kasutavad neid erinevad vastendused. Mudelivastendusel on järgmised võimalused.

-   See võib kasutada andmemudeli andmeallikatena erinevaid Dynamics 365 for Operationsi andmetüüpe. Näiteks võib see kasutada tabeleid, andmeüksus, meetodeid või loetelusid.
-   See toetab kasutaja sisendparameetreid, mida saab määratleda andmemudeli andmeallikatena, kui mõningad andmed on vaja määratleda käitusajal.
-   See toetab Dynamics 365 for Operationsi andmete teisendamist vajalikesse rühmadesse, filtreerides, sortides ja summeerides andmeid ning sidudes neid loogiliste arvutatud väljadega, mis on koostatud Microsoft Exceli sarnaste valemite kaudu (lisateavet leiate jaotisest [Valemikoostur elektroonilises aruandluses](general-electronic-reporting-formula-designer.md)).

[![Exceli sarnane valemiredaktor](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Igale äridomeenile on koostatud andmemudeli komponent, mida tuleb kasutada ühtse andmeallikana aruandluseks, mis eraldab aruandlust Microsoft Dynamics 365 for Operationsi andmeallikate füüsilisest juurutamisest ja kajastab domeenipõhiseid ärikontseptsioone ja funktsioone vormis, mis teeb aruandluse vormingu algse kujunduse ja edaspidise hooldamise tõhusamaks.

#### <a name="format-components"></a>Vormingu komponendid

Vormingu komponent on käitusajal loodava aruandlusväljundi skeem. Skeem koosneb järgmistest osadest:

-   vorming, mis määratleb käitusajal loodud elektroonilise aruandluse dokumendi struktuuri ja sisu;
-   andmeallikad kasutaja väljundi parameetrite ja domeenipõhise andmemudeli kogumina, mis kasutab valitud mudelivastendust;
-   vormingu vastendamine vormingu andmeallikate seoste kogumina, millel on vormingu üksikud elemendid, mis määravad käitusajal andmevoo ja vormingu väljundi loomise reeglid;
-   Vormingu kinnitamine konfigureeritavate reeglite kogumina, mis juhivad käitusajal aruande koostamist, olenevalt jooksvast kontekstist (nt reegel, mis peatab hankija maksete väljundi koostamise ja annab erandi, kui valitud hankija konkreetsed atribuudid (nt pangakonto) puuduvad).

Vormingukomponent toetab järgmisi funktsioone.

-   Aruandluse väljundi loomine eraldi failidega mitmesugustes vormingutes: tekst, XML või tööleht
-   Mitme faili eraldi loomine ja nende failide kapseldamine zip-failidesse

Vormingukomponent annab võimaluse manustada konkreetseid faile, mida saab aruandlusväljundis järgmiselt kasutada:

-   Exceli töövihikud, mis sisaldavad töölehte, mida saab kasutada töölehevormingu OPENXML väljundi mallina;
-   muud failid, mida saab vormingu väljundisse eelmääratletud failidena lisada.

#### <a name="component-versioning"></a>Komponendi versioonimine

ER-komponentide puhul toetatakse versioonimist. Järgmist töövoogu pakutakse ER-i komponentides muudatuste haldamiseks.

-   Algselt loodud versioon on märgitud versioonina **MUSTAND**. Seda versiooni saab redigeerida ja see on proovimiseks saadaval.
-   Versiooni**MUSTAND** saab teisendada versiooniks **LÕPULE VIIDUD**. Seda versiooni saab kasutada kohalikes aruandlusprotsessides.
-   Versiooni **LÕPULE VIIDUD** saab teisendada versiooniks **JAGATUD**. See versioon avaldatakse LCS-is ja seda saab kasutada üldistes aruandlusprotsessides. See versioon avaldatakse LCS-is ja seda saab kasutada üldistes aruandlusprotsessides.
-   Versiooni **JAGATUD**saab teisendada versiooniks **KATKESTATUD**. Seejärel saab selle versiooni kustutada.

Versioonid olekus** LÕPULE VIIDUD** või **JAGATUD** on saadaval muuks andmevahetuseks. Nende olekutega komponentidega saab teha neid toiminguid:

-   neid saab XML-vormingus järjestada ja eksportida Dynamics 365 for Operationsist XML-vormingus failina.
-   Neid saab ümber järjestada ja importida Dynamics 365 for Operationsi ER-komponendi uue versioonina.

#### <a name="component-date-effectivity"></a>Komponendi kehtivuskuupäev

ER-i komponendi versioonid on kehtivuskuupäevaga. ER-i komponendile saab määratleda kuupäeva**Kehtiv alates,**et määrata kuupäev, millal see komponent aruandlusprotsessides jõustub. Dynamics 365 for Operationsi seansi kuupäeva kasutatakse selleks, et määratleda, kas komponent kehtib käivitamiseks. Kui kindlal kuupäeval kehtib mitu versiooni, kasutatakse aruandlusprotsessides uusimat versiooni.

#### <a name="component-access"></a>Komponendi juurdepääs

Juurdepääs ER-i vormingu komponentidele sõltub ISO riigi/regiooni koodi seadistusest. Kui see seadistus on vormingu konfiguratsiooni valitud versiooni puhul tühi, on võimalik käitusajal igast Dynamics 365 for Operationsi ettevõttest vormingukomponendile juurde pääseda. kui see seadistus sisaldab ISO riigi/regiooni koode, siis on vormingukomponent saadaval ainult nendest Dynamics 365 for Operationsi ettevõtetest, millel on esmane aadress, mis on määratletud ühele vormingukomponendi ISO riigi/regiooni koodile. Andmevormingu komponendi erinevatel versioonidel võivad olla erinevad ISO riigi/regiooni koodide sätted.

#### <a name="configuration"></a>Konfiguratsioon

ER-i konfiguratsioon on konkreetse ER-i komponendi ümbris: kas **Andmemudel**või **Vorming**. Konfiguratsioon võib sisaldada kindla ER-i komponendi erinevaid versioone. Iga konfiguratsiooni omanikuks on märgitud kindel konfigurasiooni pakkuja. Konfiguratsiooni komponendi versiooni **MUSTAND** saab redigeerida, kui konfiguratsiooni omanik on valitud Dynamics 365 for Operationsi ER-i sätetes aktiivseks teenusepakkujaks. Iga mudelikonfiguratsioon sisaldab komponenti **Andmemudel**. Uus vormingukonfiguratsioon võib pärineda (olla tuletatud) konkreetsest andmemudeli konfiguratsioonist. Loodud vormingukonfiguratsioon esitatakse konfiguratsioonipuul algse andmemudeli konfiguratsiooni allüksusena. Loodud vormingukonfiguratsioon sisaldab komponenti **Vorming**. Algse mudelikonfiguratsiooni komponent **Andmemudel** lisatakse vaike-andmeallikana automaatselt alamvormingu konfiguratsiooni komponenti **Vorming**. Dynamics 365 for Operationsi ettevõtted jagavad ER-i konfiguratsiooni.

#### <a name="provider"></a>Pakkuja

ER-i pakkuja on osapoole ID, mida kasutatakse iga ER-i konfiguratsiooni autori (omaniku) tähistamiseks. ER võimaldab hallata konfiguratsioonipakkujate loendit. Elektroonilistele dokumentidele Dynamics 365 for Operationsi lahenduse osana väljastatud vormingukonfiguratsioonide omanikuks märgitakse konfiguratsioonipakkuja **Microsoft**.

#### <a name="repository"></a>Hoidla

ER-i hoidla talletab ER-i konfiguratsioone. Praegu toetatakse järgmisi elektroonilise aruandluse hoidlate tüüpe: **operatsiooniressursid** ja **LCS-i projekt**. Hoidla** Operatsiooniressursid** võimaldab juurdepääsu konfiguratsioonide loendile, mis on väljastatud Microsofti kui ER-i konfiguratsioonipakkuja Dynamics 365 for Operationsi lahenduse osana. Need konfiguratsioonid saab praegusesse Dynamics 365 for Operationsi eksemplari importida ja elektroonilise aruandluse jaoks kasutada. Neid saab kasutada ka täiendavaks lokaliseerimiseks/kohandamiseks. Hoidla **LCS-i projekt**võimaldab juurdepääsu konkreetsele LCS-i projekti konfiguratsiooniloendile (LCS-i projektivarade teegile), mis valiti hoidla registreerimise etapis. ER võimaldab ühiskasutatavate konfiguratsioonide üleslaadimist Dynamics 365 for Operationsi eksemplarist konkreetsesse hoidlasse **LCS-i projekt**. Saate importida konfiguratsioone ka konkreetsest hoidlast **LCS-i projekt** praegusesse Dynamics 365 for Operationsi eksemplari. Vajalikke hoidlaid **LCS-i projekt** saab registreerida eraldi iga praeguse Dynamics 365 for Operationsi eksemplari konfiguratsioonipakkuja kohta. Iga hoidla saab eraldada konkreetsele konfiguratsioonipakkujale.

## <a name="supported-scenarios"></a>Toetatud stsenaariumid
### <a name="building-a-data-model"></a>Andmemudeli loomine

ER pakub mudelikoosturit, mida saab kasutada konkreetsele äridomeenile andmemudeli koostamiseks. Kõiki domeenipõhiseid äriüksusi ja nendevahelisi suhteid saab esitleda andmemudelis hierarhilise struktuurina. Järgmisel joonisel on näide seda tüüpi andmemudeli (maksedomeeni andmemudeli) kohta. [![Andmemudeli näide](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise andmemudeli kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="translating-data-model-content"></a>Andmemudeli sisu tõlkimine

Andmemudeli sisu (sildid ja kirjeldused) saab tõlkida teistesse keeltesse, mida Dynamics 365 for Operations toetab. Andmemudeli sisu võib olla vaja tõlkida järgmistel põhjustel:

-   selleks, et muuta see koostamisel arusaadavamaks teist keelt rääkivatele vormingu koostajatele, kes kasutavad vormingukomponentide andmevastenduseks andmemudelit;
-   et muuta sisu käitusajal kasutajasõbralikumaks, esitades viibad ja käitamisparameetrite spikri ning konfigureeritud kinnitusteated (tõrked ja hoiatused) Dynamics 365 for Operationsisse sisselogitud kasutaja eelistatud keeles.

Järgmisel joonisel on näide selle kohta, kuidas andmemudeli sisu saab tõlkida inglise keelest jaapani keelde. [![Andmemudeli sisu inglise keeles](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png) [![Jaapani keelde tõlgitud andmemudeli sisu](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Andmemudeli vastendamiste konfigureerimine

ER pakub mudelivastenduse koosturit, mis võimaldab kasutajatel vastendada koostatud andmemudeleid konkreetsete Dynamics 365 for Operationsi andmeallikatega. Järgmisel illustratsioonil on sellise andmemudeli vastendamise näidis (**SEPA kreeditiülekande** mudeli vastendus maksedomeeni andmemudeliga). [![Andmemudeli vastenduse näide ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhised **Elektroonilise aruandluse mudeli vastenduse määratlemine ja andmeallikate valimine** ja **Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatega** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Koostatud mudelikomponendi salvestamine mudelikonfiguratsioonina

ER suudab talletada koostatud andmemudeli koos seotud andmevastendustega praeguse Microsoft Dynamics 365 for Operationsi eksemplari mudelikonfiguratsioonina. Järgmisel joonisel on näide seda tüüpi andmemudeli konfiguratsiooni (maksedomeeni andmemudeli konfiguratsiooni) kohta. [![Andmemudeli konfiguratsiooni näide](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse andmemudeli vastendamine valitud andmeallikatega** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Andmemudelit alusena kasutava vormingu koostamine

ER toetab vormingukoosturit, mida võite kasutada valitud äridomeenile konkreetse elektroonilise dokumendi vormingu koostamiseks, valides aluseks mudelikomponendi. Sama ER-i vormingukoostur võimaldab teil vastendada vormingu, mille loote, valitud domeeni andmemudeli vastendusega andmeallikana. Järgmisel illustratsioonil on seda tüüpi vormingu näide (vormingukonfiguratsioon, mis toetab Ühendkuningriigi maksevormingut **BACS**). [![Vormingu näide, mille alus on andmemudel](./media/pic-format-1024x690.png)](./media/pic-format.png) Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektrooniline aruandlus. Domeenikohase vormingu koostamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Konfiguratsiooni koostamine elektrooniliste dokumentide loomiseks töölehevormingus OPENXML

Konkreetse elektroonilise dokumendi koostamiseks töölehevormingus OPENXML saab kasutada ER-i vormingukoosturit. Järgmisel illustratsioonil on sellist tüüpi vormingu näide (vormingukonfiguratsioon OPENXML-töölehe loomiseks valitud maksetöölehe andmetega):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa). Kasutage allpool nimetatud Exceli faili mallina ER-i vormingu kujundamisel vormingumalli importimise etapi läbimiseks selles tegevusjuhises: [Maksearuande mall (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Koostatud vormingu komponendi talletamine vormingukonfiguratsioonis

ER suudab talletada koostatud vormingu koos konfigureeritud andmete vastendamistega praeguse Dynamics 365 for Operationsi eksemplari vormingukonfiguratsioonina. Eelneval joonisel on sellist tüüpi vormingukonfiguratsiooni näide (**BACS (UK)**, mis on konfiguratsiooni **Maksemudel**alamkonfiguratsioon). Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruandluse domeenipõhise vormingu kujundamine** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Dynamics 365 for Operationsi konfigureerimine loodud vormingu ettevõttesiseseks kasutamiseks

Dynamics 365 for Operationsit saab konfigureerida kasutama loodud vormingut elektrooniliste aruanne loomiseks. Viide loodud vormingu konfiguratsioonile tuleb määratleda konkreetse domeeni sätetes. Näiteks selleks, et hakata kasutama ER-i vormingukonfiguratsiooni elektrooniliste hankija maksete jaoks vormingus BACS, tuleb vormingukonfiguratsioonile viidata konkreetsetes makseviisides, nagu on näidatud järgmistel illustratsioonidel. 

[![BACS (UK) vormingukonfiguratsioon](media/ger-bacs-uk-format-configuration.png) 

[![Vormingule BACS (UK) viitamine makseviisis](media/ger-bacs-uk-format-method.png) 

Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses maksmiseks elektroonilise dokumendi loomiseks vormingu kasutamine** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

## <a name="handling-er-components"></a>ER-i komponentide käsitlemine
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>ER-i komponendi avaldamine LCS-is selle ettevõtteväliseks pakkumiseks (lokaliseerimine)

Loodud komponendi omanik (mudel või vorming) saab kasutada ER-i komponendi lõpule viidud versiooni avaldamiseks LCS-is. Selleks on vajalik praeguse ER-i konfiguratsiooni pakkuja hoidla tüüp **LCS-i projekt**. Kui komponendi lõpetatud versiooni olekuks on määratud väärtuse **LÕPULE VIIDUD** asemel väärtus **JAGATUD**, avaldatakse see versioon LCS-is. Kui komponent on LCS-i avaldatud, saab selle komponendi omanikust teenusepakkuja selle komponendi toetamiseks. Näiteks kui vormingukomponent on mõeldud juriidiliselt vajaliku elektroonilise dokumendi koostamiseks (nt lokaliseerimisstsenaariumi kohaselt), siis eeldatakse, et vorming hoitakse seadusemuudatustega kooskõlas ja teenusepakkuja väljastab komponendi uusi versioone, kui tekivad uued seadusandlikud nõudmised. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruande konfiguratsiooni üleslaadimine teenusesse Lifecycle Services** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>ER-i komponendi importimine LCS-ist ettevõttesiseseks kasutamiseks

ER võimaldab importida ER-i komponente LCS-ist praegusesse Dynamics 365 for Operationsi eksemplari. Selleks on vajalik hoidla tüüp **LCS-i projekt**. Kui ER-i komponent on LCS-ist praegusesse Dynamics 365 for Operationsi eksemplari imporditud, saab selle eksemplari omanikust tarbija teenusele, mida pakub imporditud komponendi omanik (autor). Näiteks kui vormingukomponent on mõeldud Dynamics 365 for Operationsist konkreetse elektroonilise dokumendi koostamiseks riigi-/regioonipõhises vormingus (lokaliseerimisstsenaarium), eeldatakse, et teenuse tarbija suudab hankida sellele vormingule tehtud värskendused, et hoida seda kooskõlas seaduse nõuetega. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilise aruande konfiguratsiooni importimine teenusest Lifecycle Services** (äriprotsessi **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)** osa).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Vormingu koostamine, valides aluseks muu vormingu (kohandamine)

ER võimaldab luua (tuletada) komponendi kehtivast LCS-ist imporditud versioonist (alusest) uue komponendi. Näiteks oletame, et kasutaja soovib tuletada uue vormingu mõne erinõude rakendamiseks elektroonilisele dokumendile (nt lisaväli või põhjalik kirjeldus), et toetada kohandamisstsenaariumi. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses vormingu versiooni uuendamine, kasutades selle alusversiooni** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Vormingu versiooni uuendamine, valides alusvormingu uue versiooni ( aluse muutmine)

ER võimaldab võtta automaatselt kasutusele aluskomponendi uusima versiooni muudatused praeguses tuletatud komponendi mustandiversioonis. Seda protsessi nimetatakse *aluse muutmiseks*. Näiteks uue seadusandluse muudatuse, mis on võetud kasutusele LCS-ist imporditud vormingu uusimas versioonis, saab ühendada automaatselt elektroonilise dokumendi kohandatud versiooniga. Kõiki muudatusi, mida ei saa automaatselt ühendada, käsitletakse konfliktidena. Need konfliktid esitatakse sobiva komponendi koosturis käsitsi lahendamiseks. Selle stsenaariumi üksikasjadega tutvumiseks käivitage tegevusjuhis **Elektroonilises aruandluses vormingu versiooni uuendamine, kasutades selle alusversiooni** (osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Dynamics 365 for Operationsi lahenduses pakutavate ER-i konfiguratsioonide loend
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



<a name="see-also"></a>Vt ka
--------

[Lokaliseerimisnõuded – Elektroonilise aruandluse konfiguratsiooni loomine](electronic-reporting-configuration.md)

[Elektroonilise aruandluse konfiguratsiooni elutsükli haldamine](general-electronic-reporting-manage-configuration-lifecycle.md)




