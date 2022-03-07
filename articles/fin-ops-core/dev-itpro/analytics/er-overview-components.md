---
title: Elektroonilise aruandluse komponendid
description: Selles teemas kirjeldatakse elektroonilise aruandluse (ER) komponente.
author: nselin
ms.date: 09/28/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.topic: overview
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1a24aa52c805722c20045b6227ceac0103cfbe6b
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8324031"
---
# <a name="electronic-reporting-components"></a>Elektroonilise aruandluse komponendid

[!include [banner](../includes/banner.md)]

Elektrooniline aruandlus (ER) toetab järgmist tüüpi komponente:

- Andmemudel
- Mudeli vastendamine
- Vorming
- Metaandmed

## <a name="data-model-component"></a>Andmemudeli komponent

Andmemudeli komponent on andmestruktuuri abstraktne kujutis. See kirjeldab konkreetse äridomeeni piirkonna piisavalt üksikasjalikult, et rahuldada selle domeeni aruandlusvajadusi. Andmemudeli komponent koosneb järgmistest osadest:

- **Andmemudel** – Domeenipõhiste äriüksuste kogum ja nende üksuste vaheline hierarhiliselt struktureeritud suhtemääratlus.
- **Mudeli kaardistamine** – Valitud rakenduste andmeallikad on lingitud andmemudeli üksikute elementidega, mis määravad käitusajal andmevoo ja reeglid äriandmete sisestamiseks andmemudeli komponenti.

Andmemudeli äriüksus on esindatud konteineri või kirjena. Äriüksuse atribuudid on esindatud andmeüksuste, väljadena. Igal andmeüksusel on kordumatu nimi, silt, kirjeldus ja väärtus. Iga andmeüksuse väärtus võib olla sellise ülesehitusega, et see tuvastatakse stringi, täisarvu, reaalarvu, kuupäeva, loendi (summa) või loogikaväärtusena. Lisaks võib andme kaup olla ka teine kirje või kirjete loend.

Üksik andmemudeli komponent võib sisaldada mitut domeenipõhiste äriüksuste hierarhiat. See võib sisaldada ka mudelivastendusi, mis toetavad käitusajal aruandepõhist andmevoogu. Hierarhiaid eristatakse ühe kirjega, mis on valitud mudelivastenduse juurena. Näiteks võib maksedomeeni ala andmemudel toetada järgmisi vastendusi:


- Ettevõte \> Hankija \> AP-domeeni maksekanded
- Klient \> Ettevõte \> AR-domeeni maksekanded

Äriüksused, näiteks äri- ja maksetehingud, on kavandatud ainult üks kord. Erinevad kaardistused saavad neid vajadusel uuesti kasutada.

## <a name="model-mapping-component"></a>Mudelivastenduse komponent

Mudeli kaardistamine seob avalduse andmeallikad andmemudeli üksikute elementidega, mis määravad käitusajal andmevoo ja reeglid äriandmete sisestamiseks andmemudeli komponendis.

Väljaminevaid elektroonilisi dokumente toetaval mudelivastendusel on järgmised võimalused.

- See võib kasutada andmemudeli andmeallikatena erinevaid andmetüüpe. Need andmetüübid hõlmavad tabeleid, andmeüksusi, meetodeid ja summasid.
- See toetab kasutaja sisendparameetreid, mida saab määratleda andmemudeli andmeallikatena, kui mõningad andmed on vaja määratleda käitusajal.
- See toetab andmete teisendamist vajalikesse gruppidesse. Te saate ka filtreerida, sorteerida ja summeerida andmeid ning lisada loogilisi arvutatud välju, mis on kavandatud Microsoft Exceli valemitele sarnanevate valemite kaudu. Lisateabe saamiseks vaadake [Valemikoostaja elektroonilises aruandluses (ER)](general-electronic-reporting-formula-designer.md).

Sissetulevaid elektroonilisi dokumente toetaval mudelivastendusel on järgmised võimalused.

- See saab kasutada sihtidena erinevaid värskendatavaid andmeelemente. Nende andmeelementide hulka kuuluvad tabelid, andmeüksused ja vaated. Andmeid saab uuendada sissetulevate elektrooniliste dokumentide andmete abil. Ühe mudeli vastenduses saab kasutada mitut sihtüksust.
- See toetab kasutaja sisendparameetreid, mida saab määratleda andmemudeli andmeallikatena, kui mõningad andmed on vaja määratleda käitusajal.

Andmemudeli komponent on loodud igale äridomeenile, mida kasutatakse aruandluses ühtse andmeallikana. Ühtne andmeallikas eraldab andmeallikate füüsilisest rakendamisest aruandmist. See komponent kajastab domeenipõhiseid ärikontseptsioone ja funktsioone sellisel kujul, mis teeb aruandlusvormingu algse koostamise ja edasise haldamise tõhusamaks.

## <a name="format-component"></a>Vormingu komponent

### <a name="format-components-for-outgoing-electronic-documents"></a>Väljaminevate elektrooniliste dokumentide vormingukomponendid

Vormingu komponent on käitusajal loodava aruandlusväljundi skeem. Skeem koosneb järgmistest osadest:

- Vorming, mis määratleb käitusajal loodud väljamineva elektroonilise dokumendi struktuuri ja sisu.
- andmeallikad kasutaja väljundi parameetrite ja domeenipõhise andmemudeli kogumina, mis kasutab valitud mudelivastendust;
- Vormingu vastendamine vormingu andmeallikate seoste kogumina, millel on vormingu üksikud elemendid, mis määravad käitusajal andmevoo ja vormingu väljundi loomise reeglid.
- Vormingu kinnitamine konfigureeritavate reeglite kogumina, mis juhib käitamisel aruande loomist olenevalt käitatavast kontekstist. Näiteks võib olla olemas reegel, mis peatab hankija maksete väljundi loomise ja annab erandi, kui valitud hankija konkreetsed atribuudid (nt pangakonto number) on puudu.

Vormingukomponent toetab järgmisi funktsioone.

- Aruandluse väljundi loomine eraldi failidega mitmesugustes vormingutes, nt tekst, XML, Microsoft Wordi dokument või tööleht
- Mitme faili eraldi loomine ja nende failide kapseldamine zip-failidesse

Vormingukomponent võimaldab manustada konkreetseid faile, mida saab aruandlusväljundis järgmiselt kasutada:

- Exceli töövihikud, mis sisaldavad töölehte, mida saab kasutada töölehevormingu OPENXML väljundi mallina;
- Wordi failid, mis sisaldavad dokumenti, mida saab kasutada Microsoft Wordi dokumendivormingu väljundi mallina;
- muud failid, mida saab vormingu väljundisse eelmääratletud failidena lisada.

Järgmine illustratsioon näitab, kuidas andmed nende vormingute puhul liiguvad.

[![Sissetulevate vormingukomponentide andmevoog.](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Ühe ER-vormingukonfiguratsiooni käitamiseks, et importida andmeid sissetulevast elektroonilisest dokumendist, tuleb tuvastada vormingukonfiguratsiooni soovitud vastendus ja samuti mudeli vastenduse integratsioonipunkt. Sama mudeli vastendust ja sihtkohti saab kasutada koos erinevate vormingutega erinevat tüüpi sissetulevate dokumentide puhul.

## <a name="component-versioning"></a>Komponendi versioonimine

ER-komponentide puhul toetatakse versioonimist. Järgmist töövoogu pakutakse ER-i komponentides muudatuste haldamiseks.

1. Algselt loodud versioon on märgitud versioonina **Mustand**. Seda versiooni saab redigeerida ja see on proovimiseks saadaval.
2. Versiooni **Mustand** saab teisendada versiooniks **Lõpule viidud**. Seda versiooni saab kasutada kohalikes aruandlusprotsessides.
3. Versiooni **Lõpule viidud** saab teisendada versiooniks **Jagatud**. See versioon avaldatakse Microsoft Dynamics Lifecycle Services (LCS) platformil ja seda saab kasutada üldistes aruandlusprotsessides.
4. Versiooni **Jagatud** saab teisendada versiooniks **Katkestatud**. Selle versiooni saab kustutada.

Versioonid olekus **Lõpule viidud** või **Jagatud** on saadaval muuks andmevahetuseks. Nende olekutega komponentidega saab teha järgmisi toiminguid.

- Komponenti saab XML-vormingus järjestada ja eksportida XML-vormingus failina.
- Komponenti saab ümber järjestada ja importida rakenduse ER-komponendi uue versioonina.

## <a name="component-date-effectivity"></a>Komponendi kehtivuskuupäev

ER-i komponendi versioonid on kehtivuskuupäevaga. ER-i komponendile saab määratleda kuupäeva „Kehtiv alates”, et määrata kuupäev, millal see komponent aruandlusprotsessides jõustub. Rakenduse seansi kuupäeva kasutatakse selleks, et määratleda, kas komponent kehtib käivitamiseks. Kui kindlal kuupäeval kehtib mitu versiooni, kasutatakse aruandlusprotsessides uusimat versiooni.

## <a name="component-access"></a>Komponendi juurdepääs

Juurdepääs ER-vormingu komponentidele sõltub Rahvusvahelise Standardiorganisatsiooni (ISO) riigi/regiooni koodi sättest. Kui see seadistus on vormingu konfiguratsiooni valitud versiooni puhul tühi, on võimalik käitusajal igast ettevõttest vormingukomponendile juurde pääseda. kui see seadistus sisaldab ISO riigi/regiooni koode, siis on vormingukomponent saadaval ainult nendest ettevõtetest, millel on esmane aadress, mis on määratletud ühele vormingukomponendi ISO riigi/regiooni koodile.

Andmevormingu komponendi erinevatel versioonidel võivad olla erinevad ISO riigi/regiooni koodide sätted.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

