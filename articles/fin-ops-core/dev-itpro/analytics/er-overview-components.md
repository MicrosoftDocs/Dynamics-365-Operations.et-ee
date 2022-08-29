---
title: Elektroonilise aruandluse komponendid
description: See artikkel kirjeldab elektroonilise aruandluse (ER) komponente.
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285027"
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


## <a name="component-versioning"></a>Komponendi versioonimine

ER-komponentide puhul toetatakse versioonimist. Järgmist töövoogu pakutakse ER-i komponentides muudatuste haldamiseks.

1. Algselt loodud versioon on märgitud **mustandversioonina**. Seda versiooni saab redigeerida ja see on proovimiseks saadaval.
2. Versiooni **Mustand** saab teisendada versiooniks **Lõpule viidud**. Seda versiooni saab kasutada kohalikes aruandlusprotsessides.
3. Versiooni **Lõpule viidud** saab teisendada versiooniks **Jagatud**. See versioon avaldatakse Microsoft Dynamics Lifecycle Services (LCS) platformil ja seda saab kasutada üldistes aruandlusprotsessides.
4. Versiooni **Jagatud** saab teisendada versiooniks **Katkestatud**. Selle versiooni saab kustutada.

Versioonid olekus **Lõpule viidud** või **Jagatud** on saadaval muuks andmevahetuseks. Nende olekutega komponentidega saab teha järgmisi toiminguid.

- Komponenti saab XML-vormingus järjestada ja eksportida XML-vormingus failina.
- Komponenti saab ümber järjestada ja importida rakenduse ER-komponendi uue versioonina.

Lisateavet vt Jaotisest Uue [andmemudeli konfiguratsiooni importimine](er-quick-start1-new-solution.md#ImportDataModel) ja [tuletatud vormingu ekspordi lõpetatud versioon](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Mustandi versioonid käitusajal

Oma isiklike kasutaja parameetrites ER-raamistiku jaoks saate lubada suvandi, mis võimaldab teil määratleda, kas ER-i konfiguratsiooni mustandversiooni tuleb käitusajal kasutada. Lisateavet selle kohta, kuidas suvand **Käita** mustand teha ER-i konfiguratsioonide jaoks kättesaadavaks, vt [Märgi kohandatud vorming käivitatavaks](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER-i kasutaja parameetrid on ettevõttepõhised ja kasutajapõhised.

### <a name="draft-format-versions-at-runtime"></a>Mustandi vormingu versioonid käitusajal

ER-lahenduse käivitamisel ignoreeritakse vaikimisi selle vormingukomponentide mustandversioone. Selle asemel kasutatakse ainult asjakohast versiooni, mille olek pole **Mustand**. Mõnikord võite soovida, et ER kasutaks käitusajal oma ER-vormingu konfiguratsiooni mustandversiooni. Näiteks pärast vajalike muudatuste tegemist mustandi versiooni saate kasutada seda mustandversiooni testi käivitamiseks. Sel viisil saate kinnitada oma muudatuste õigsust. Mustandvormingu versiooni kasutamise alustamiseks tuleb [vastava](er-quick-start2-customize-report.md#MarkFormatRunnable)**ER**-i konfiguratsiooni suvand Käita mustand seada väärtusele **Jah.**

### <a name="draft-model-mapping-versions-at-runtime"></a>Mustandi mudeli vastendamise versioonid käitusajal

ER-lahenduse käivitamisel kasutatakse vaikimisi alati selle mudeli vastendamise komponentide mustandversioone. Mõnikord võite soovida, et ER ignoreeriks käitusajal teie ER-mudeli vastendamise konfiguratsiooni mustandversiooni. Versioonis **10.0.29** **ja uuemates versioonides saate lubada suvandi Käivita mustand, et ER-mudeli vastenduste funktsioonil juhtida käitusajal** kasutatavat mudeli vastendamise versiooni. Kui see funktsioon on lubatud, ilmneb järgmine käitumine:

- Kui suvand **Käita mustand** on mudeli **vastendamise** konfiguratsioonis seatud valikule Ei, kasutatakse käitusajal selle konfiguratsiooni kõrgeimat mitte-mustandversiooni. Kui konfiguratsioon ei ole praeguses finantseksemplaris saadaval, ilmneb erand.
- Kui suvand **Käita mustand** on mudeli **vastendamise** konfiguratsioonis seatud väärtusele Jah, kasutatakse käitusajal selle konfiguratsiooni mustandversiooni.

## <a name="component-date-effectivity"></a>Komponendi kehtivuskuupäev

ER-vormingu komponendiversioonid on kehtivusega. ER-vormingu komponendile saate seada "kehtib alates" kuupäeva, et määrata kuupäev, mil komponent aruandlusprotsessides jõustub. Rakenduse seansi kuupäeva kasutatakse selleks, et määratleda, kas komponent kehtib käivitamiseks. Kui kindlal kuupäeval kehtib mitu versiooni, kasutatakse aruandlusprotsessides uusimat versiooni.

## <a name="component-access"></a>Komponendi juurdepääs

Juurdepääs ER-vormingule ja mudeli vastendamise komponentidele käitusajal sõltub Rahvusvahelise Standardiorganisatsiooni (ISO) riigi-/regioonikoodi sättest. Kui see säte on tühi vormingu või mudeli vastendamise konfiguratsiooni valitud versiooni puhul, pääseb vormingu või mudeli vastendamise komponendi juurde mis tahes ettevõttelt käitusajal. Kui säte sisaldab ISO riigi-/regioonikoode, on vormingu või mudeli vastendamise komponent saadaval ainult ettevõtetelt, mille peamine aadress on määratletud ühe vormingukomponendi ISO riigi-/regioonikoodi jaoks.

Vormingu või mudeli vastendamise komponendi erinevatel versioonidel võivad ISO riigi-/regioonikoodide jaoks olla erinevad sätted.

Lisateavet vt riigi kontekstist sõltuvate [ER-mudeli vastendamiste konfigureerimine](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

