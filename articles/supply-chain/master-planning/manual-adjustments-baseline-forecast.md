---
title: Alusprognoosis käsitsi korrigeerimiste tegemine
description: Selles teemas selgitatakse, kuidas alusprognoosi käsitsi korrigeerida ning prognoosi üksikasju kuvada.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dc5d1812fa926216a75b6fc4e3cf820ccc3ef6d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978144"
---
# <a name="make-manual-adjustments-to-the-baseline-forecast"></a>Alusprognoosis käsitsi korrigeerimiste tegemine

[!include [banner](../includes/banner.md)]

Selles teemas selgitatakse, kuidas alusprognoosi käsitsi korrigeerida ning prognoosi üksikasju kuvada. 

Enne käsitsi korrigeerimiste tegemist on oluline mõista mõnda põhimõtet erinevatel lehekülgedel.

## <a name="grid-on-the-adjusted-demand-forecast-page"></a>Korrigeeritud nõudluse prognoosi lehe ruudustik
Lehe **Korrigeeritud nõudluse prognoos** ruudustikul on järgmine struktuur.

-   Esimeses veerus kuvatakse kaubad, kauba eraldamisvõtmed, ettevõtted jms, mille jaoks prognoos loodi. Lehe alapealkiri kirjeldab ruudustikus kuvatatud praegusi prognoosi dimensioone. Näiteks kui lehe alapealkiri on **Ettevõte / Koht / Kauba eraldamisvõti** ja üks ruudustiku reapäiseid on **USMF / 1 / D\_Alloc**, näitab see rida, et tegemist on USMF-i ettevõtte, koha 1 ja **D\_Alloc** kauba eraldamisvõtme prognoosiga.
-   Järgnevad veerud esindavad prognoosivahemikke, mille jaoks prognoos on loodud. Iga veeru päis on veerus kuvatava prognoosivahemiku alguskuupäev.
-   Lahtrite väärtused esitavad ühe kauba, kauba eraldamisvõtme jm kindla prognoosivahemiku prognoosi.

## <a name="forecast-aggregation-and-de-aggregation"></a>Prognoosi koondamine ja jaotamine
Lehe alapealkiri näitab prognoosi koondamise taset. 

Näiteks, kui lehe alapealkiri on **Ettevõte / Koht / Eraldamisvõti / Kaubakood / Värv / Suurus / Konfiguratsioon / Stiil**, ei ole prognoosi koondatud ning seda kuvatakse kauba ja selle dimensioonide tasemel. Koondamise muutmiseks kasutage lehekülge **Prognoosi dimensioonide muutmine**, mille saate avada rakenduse menüüst. 

Prognoosi muutmiseks klõpsake mistahes saadaoleval lahtril ja sisestage sinna korrigeeritud prognoosi väärtus. Redigeeritud lahtri sisu pannakse paksu kirja, et näidata, et selles kuvatav prognoos ei ole nõudluse prognoosimise teenuse loodud prognoos, vaid seda on käsitsi korrigeeritud. 

Kui muudate koondamist selliselt, et lehel rohkem koondatud andmeid kuvada, saate leheküljelt **Nõudluse prognoosi read** koondatud prognoosi üksikuid prognoosi ridu vaadata. 

Näiteks lõite prognoosi kauba tasemel, kuid teate, et selle kauba nõudlus suureneb kampaania või muu taolise sündmuse tõttu kõigis kohtades. Sel juhul saate koondamise seada **Ettevõte / Kauba eraldamisvõti / Kaup** leheküljel **Prognoosi dimensioonide muutmine**. Kauba globaalselt prognoosi saate korrigeerida kõigis kohtades ruudustikus **Korrigeeritud nõudluse prognoos**. Tehtud muudatuste mõju nägemiseks kõigis kohtades avage lehekülg **Nõudluse prognoosi read**. Sellel lehel näete kaupa igas kohas eraldi real, korrigeeritud prognoosi kogust ja prognoosi algset kogust. 

Kui prognoositud kogust on korrigeeritud koondamise tasemel, kasutab süsteem kaalutud eraldamist, et jagada muudatus koondatud ridadele. 

Leheküljel **Nõudluse prognoosi read** saate ka käsitsi korrigeerimisi teha, muutes kas väärtust **Üldkogus** või jaotamise ruudustiku lahtreid **Kogus**.

## <a name="viewing-details-of-the-forecast"></a>Prognoosi üksikasjade vaatamine
Prognoosi kohta lisateabe saamiseks avage lehekülg **Nõudluse prognoosi üksikasjad**. 

Lehel **Nõudluse prognoosi üksikasjad** kuvatakse graafilises vormingus ja tabelina järgmist teavet:

-   prognoosi aluseks olev ajalooline nõudlus;
-   praegune prognoos, mida koondplaneerimises kasutatakse;
-   käsitsi korrigeeritud uued nõudluse prognoosi väärtused ja summad;
-   prognoositud väärtuste usaldusvahemik;
-   prognoosi loomiseks kasutatud prognoosimudel. Kui vaatate koondatud andmeid, näete loendit kõigist meetoditest, mida koondatud ajaseeriates kasutati;
-   mudeli sisemine täpsus (MAPE). Prognoosi täpsuse kohta lisateabe saamiseks vt [Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md).

**Märkused.**

-   Kui lubate funktsioonide halduses suvandi **Prognoosi mudeli valik nõudluse prognoosi üksikasjades**, saate valida ajaloolisesse prognoosi kaasatavad prognoosimudelid lehel **Nõudluse prognoosi üksikasjad**.
-   Jaotises **Prognoos** kuvatud usaldusvahemik tähistab usaldusvahemiku ülem- ja alampiiri erinevust. Ülem- ja alampiiri väärtuste vaatamiseks liikuge üle diagrammi jaotises **Varasem nõudlus ja prognoos graafiliselt**.
-   Kui kasutate nõudluse prognoosimise Microsoft Azure’i masinõpet, saate määrata loodava prognoosi usaldusväärsuse taseme protsendi. Usaldusvahemik koosneb väärtuste vahemikust, mille järgi on nõudluse prognoosi hea hinnata. Usaldusväärsuse tase 95% näitab, et on olemas 5% tõenäosus, et nõudluse prognoos jääb usaldusväärsusintervalli vahemikust välja.

Leheküljel **Nõudluse prognoosi üksikasjad** saate prognoosis käsitsi korrigeerimis teha, muutes väärtusi reas **Prognoos** jaotises **Prognoos**.

<a name="additional-resources"></a>Lisaressursid
--------

[Prognoosi täpsuse jälgimine](monitor-forecast-accuracy.md)

[Statistilise alusprognoosi loomine](generate-statistical-baseline-forecast.md)



