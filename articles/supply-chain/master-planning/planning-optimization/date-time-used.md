---
title: Kuupäeva ja aja parameetrid, mida planeerimise optimeerimine ei kasuta
description: See artikkel annab teavet kuupäeva ja kellaaja parameetrite kohta, mida optimeerimine oma toimingu ajal kasutab.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-09-21
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 2ef78c73a1c7033735f9586229ff7ba21daaa5ef
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740900"
---
# <a name="date-and-time-parameters-used-by-planning-optimization"></a>Kuupäeva ja aja parameetrid, mida planeerimise optimeerimine ei kasuta

[!include [banner](../../includes/banner.md)]

See artikkel annab teavet kuupäeva ja kellaaja parameetrite kohta, mida optimeerimine oma toimingu ajal kasutab.

Kuigi taunitav koondplaneerimise mootor kasutab kõigis arvutustes kandekuupäevi, töötab planeerimise optimeerimine kuupäeva- ja kellaajaväärtustega, mis teisendatakse kuupäevadeks. Selline käitumise erinevus võib põhjustada olukordi, kus näiteks koondplaneerimise käivitamisel keskööl loodud eelarvekandeid ei kaasata, sest Planning Optimization arvestab, et need loodi enne praegust kuupäeva.

## <a name="parameters-for-issue-and-demand-transactions"></a>Väljaminev- ja nõudluskannete parameetrid

Järgmises tabelis loetletakse parameetrid, mida planeerimise optimeerimine kasutab väljamineku ja nõudluse kannete protsessides.

| Parameeter | Parameetri nimi planeerimise optimeerimises | Kirjeldus | Vastav väli rakenduses Microsoft Dynamics 365 Supply Chain Management (tabelis ReqTrans) |
|---|---|---|---|
| Plaanitud väljastamisaeg | `PlannedIssueTime` | Välja andmiseks plaanitud kuupäev. | **Kuni kuupäevani** (`FuturesDate`) ja **viivitusega kellaajani** (`FuturesTime`) |
| Taotletud väljastamisaeg | `RequestedIssueTime` | Kuupäev, mil kasutaja taotles väljalaset ja seadistas selle Supply Chain Management`is. See parameeter kehtib ainult vabastatud või kinnitatud plaanitud tellimuste korral. Plaanitud tellimuste puhul on see vaikimisi tühi. | **Nõutav kuupäev** (`ReqDateDlvOrig`) |
| Nõutav väljastamisaeg | `RequiredIssueTime` | Nõutav väljastamise kuupäev, mida korrigeerib plaanimise optimeerimine. Kui soovitud väljastamisaeg on optimeerimise käivitamisel möödas, korrigeeritakse nõutud väljastamisaeg esimesele avatud päevale, mis ei ole tänasest kuupäevast varasem. Kui soovitud väljastamisaeg on kalendris märgitud blokeerituks, korrigeeritakse nõutav väljastatav aeg esimesele avatud päevale enne seda kuupäeva. | **Vajaduse kuupäev** (`ReqDate`) ja **Vajaduse kellaaeg** (`ReqTime`) |
| Väljastamise aja viivitus | `IssueTimeDelay` | Ajaerinevus plaanitud väljastamisaja ja kinnitatud ning vabastatud tellimuste taotletud väljastamisaja või nõutava väljastamisaja vahel. | **Viivitus (päevades)** (`FuturesDays`) |

## <a name="parameters-for-receipt-and-supply-transactions"></a>Sissetuleku- ja tarnekannete parameetrid

Järgmises tabelis loetletakse parameetrid, mida planeerimise optimeerimine kasutab väljamineku ja nõudluse kannete protsessides.

| Parameeter | Parameetri nimi planeerimise optimeerimises | Kirjeldus | Samaväärne väli rakenduses Supply Chain Management (tabelis ReqTrans või ReqPO) |
|---|---|---|---|
| Plaanitud kättesaadavuse aeg | `PlannedAvailabilityTime` | Kuupäev, millal kviitung on kavandatud saadaval olema. | **Vajaduse kuupäev** (`ReqDate`) ja **Vajaduse kellaaeg** (`ReqTime`) |
| Plaanitud saabumisaeg | `PlannedReceiptTime` | Kuupäev, mil kviitung saabub asukohta. | **Lõpukuupäev** (`FuturesDate`), **Viivitusega aeg** (`FuturesTime`) ja **tarnekuupäev** (`ReqDateDlv`) või **Nõutav kuupäev** (`ReqDateDlvOrig`) tellimust pole veel vabastatud. |
| Nõutav kättesaadavuse aeg | `RequiredAvailabilityTime` | Nõutav saadavuse kuupäev, mida korrigeerib plaanimise optimeerimine. | **Vajaduse kuupäev** (`ReqDate`) ja **Vajaduse kellaaeg** (`ReqTime`) |
| Prognoositud kättesaamise aeg | `ExpectedReceiptTime` | Vabastatud sissetuleku eeldatav vastuvõtukuupäev. Väärtuse on määranud kasutaja rakenduses Supply Chain Management ja seda ei korrigeeri plaanimise optimeerimine. See parameeter kehtib ainult vabastatud sissetulekute kohta. | **Nõutav kuupäev** (`ReqDateDlvOrig`) |
| Nõutav vastuvõtuaeg | `RequiredReceiptTime` | Nõutav laekumise kuupäev, mida korrigeerib plaanimise optimeerimine. | **Vajaduse kuupäev** (`ReqDate`) ja **Vajaduse kellaaeg** (`ReqTime`) |
| Plaanitud tellimisaeg | `PlannedOrderingTime` | Tellimuse kuupäev, mille arvutab plaanimise optimeerimine. | **Tellimuse kuupäev** (`ReqDateOrder`) ja **tellimuse kellaaeg** (`ReqTimeOrder`) |
| Plaanitud tegevuse algusaeg | `PlannedActivityStartTime` | Kuupäev, mil selle sissetuleku tegevus peaks algama. | **Alguskuupäev** (`SchedFromDate`) |
| Vastuvõtuaja viivitus | `ReceiptTimeDelay` | Plaanitud vastuvõtuaja ja nõutava sissetulekuaja vaheline ajaerinevus. | **Viivitus (päevades)** (`FuturesDays`) ja **hilinenud ajani** (`FuturesTime`) |

## <a name="examples-of-date-parameter-use-by-planning-optimization"></a>Kuupäeva ja aja parameetri, te näited, mida Planning Optimization kasutab

Järgmiste illustratsioonide plaanid on päeva tasemel, kuid planeerimise optimeerimine käivitatakse üksikasjalikumal tasemel. Kuna veerised võivad olla näiteks tundides, võib planeerimisjärjestuse aeg olla 22. jaanuar 2021, kell 11:35 jne.

### <a name="example-1-simple-scenario"></a>Näide 1: lihtne stsenaarium

Üks 22. jaanuaril taotletud väljastamisajaga müügitellimus on kaetud ühe ostutellimusega. Kasutatud on järgmiseid sätteid:

- Juhtimisaega pole
- Kalendrit pole (kõik päevad on avatud.)
- Veerised puuduvad

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Näidisstsenaarium.](media/planning-service-dates-1-small.png)](media/planning-service-dates-1.png)

### <a name="example-2-lead-time-scenario"></a>Näide 2: täitmisaja stsenaarium

Üks 22. jaanuaril taotletud väljastamisajaga müügitellimus on kaetud ühe ostutellimusega. Kasutatud on järgmiseid sätteid:

- Täitmisaja kolm päeva
- Kalendrit pole (kõik päevad on avatud.)
- Veerised puuduvad

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Täitmisaja stsenaarium.](media/planning-service-dates-2-small.png)](media/planning-service-dates-2.png)

### <a name="example-3-margin-scenario"></a>Näide 3: marginaali stsenaarium

Üks 22. jaanuaril taotletud väljastamisajaga müügitellimus on kaetud ühe ostutellimusega. Kasutatud on järgmiseid sätteid:

- Täitmisaja kolm päeva
- Neljapäevane tellimise kasum
- Viiepäevane saadavusvaru
- Kalendrit pole (kõik päevad on avatud.)

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Marginaali stsenaarium.](media/planning-service-dates-3-small.png)](media/planning-service-dates-3.png)

### <a name="example-4-delay-scenario"></a>Näide 4: viivitusstsenaarium

Üks 22. jaanuaril taotletud väljastamisajaga müügitellimus on kaetud ühe ostutellimusega. Selles näites kasutatakse samu sätteid nagu näites 3, kuid planeerimiskuupäev on viidud 15. jaanuari. Tagasisuunas planeerimine (punased tähised) nurjub, kuna plaanitud tellimisaeg peaks olema tänasest kuupäevast varem. Seepärast tuleb koondplaneerimine planeerida edasisuunas ja esineda viivitusi.

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Viivitusstsenaarium.](media/planning-service-dates-4-small.png)](media/planning-service-dates-4.png)

### <a name="example-5-transfer-scenario"></a>Näide 5: edastusstsenaarium

Üks müügitellimus laost 1, mille väljastamisaeg on 22. jaanuaril taotletud, hõlmab üks lao 2 üleviimistellimus, mis on kaetud plaanitud ostutellimusega. Kasutatud on järgmiseid sätteid:

- Täitmisaja kolm päeva (ladu 1)
- Ostu sooritamise kaks päeva (ladu 2)
- Kalendrit pole (kõik päevad on avatud.)

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Ülekande stsenaarium.](media/planning-service-dates-5-small.png)](media/planning-service-dates-5.png)

### <a name="example-6-lead-time-with-calendars-scenario"></a>Näide 6: täitmisaeg kalendrite stsenaariumiga

Üks 22. jaanuaril taotletud väljastamisajaga müügitellimus on kaetud ühe ostutellimusega. Kasutatud on järgmiseid sätteid:

- Täitmisaja kolm päeva
- Väljastuskalender (reedel suletud)
- Kättesaadavuse kalender (suletud neljapäeval ja reedel)
- Vastuvõtukalender (suletud teisipäeval, kolmapäeval ja pühapäeval)
- Tarneaegade kalender (suletud neljapäeval ja reedel)
- Tellimiskalender (avatud esmaspäeval ja laupäeval)

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Täitmisaeg kalendrite stsenaariumiga.](media/planning-service-dates-6-small.png)](media/planning-service-dates-6.png)

### <a name="example-7-delay-with-calendars-scenario"></a>Näide 7: Viivitus kalendrite stsenaariumiga

Üks 22. jaanuaril taotletud väljastamisajaga müügitellimus on kaetud ühe ostutellimusega. Selles näites kasutatakse samu sätteid nagu näites 6, kuid planeerimiskuupäev on viidud 13. jaanuari. Tagasisuunas planeerimine (punased tähised) nurjub, kuna plaanitud tellimisaeg peaks olema tänasest kuupäevast varem. Seepärast tuleb koondplaneerimine planeerida edasisuunas ja esineda viivitusi.

Järgmisel illustratsioonil on näidatud see stsenaarium. (Valige illustratsioon, et avada suurem versioon.)

[![Viivitus kalendrite stsenaariumiga.](media/planning-service-dates-7-small.png)](media/planning-service-dates-7.png)
