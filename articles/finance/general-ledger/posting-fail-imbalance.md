---
title: Töölehe sisestamise tõrge tasakaalustamatuse tõttu
description: See artikkel selgitab, miks deebeteid ja krediite ei pruugita kandekannetes tasakaalustada, nii et kandeid ei saa sisestada. Artikkel sisaldab ka probleemi parandamise samme.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f5afded3d5c42f8dab465b668e4c1fcdaed8c215
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861325"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Töölehe sisestamise tõrge tasakaalustamatuse tõttu

[!include [banner](../includes/banner.md)]

See artikkel selgitab, miks deebeteid ja krediite ei pruugita kandekannetes tasakaalustada, nii et kandeid ei saa sisestada. Artikkel sisaldab ka probleemi parandamise samme.

## <a name="symptom"></a>Sümptom

Mõnel juhul ei saa töölehte sisestada ja kuvatakse järgmine teade: „Konkreetse kande kanded ei ole kindla kuupäeva seisuga tasakaalus (arvestusvaluuta: 0,01 – aruandlusvaluuta: 0,06)”. Miks ei saa töölehte sisestada?

## <a name="resolution"></a>Lahendus

Pearaamatusse sisestamisel peab iga kanne olema tasakaalustatud kandevaluutas, arvestusvaluutas ja aruandlusvaluutas, kui need valuutad on lehel **Pearaamatu seadistus** määratletud. (Kanded on tasakaalus, kui deebetite kogusumma võrdub kreeditite kogusummaga.)

Töölehe ridade lehe allosas kuvatakse kogusummad arvestusvaluutas ja aruandlusvaluutas. Neid **ei** kuvata kandevaluutas välisvaluuta kannete puhul. Samuti näitab tõrketeade, mille kasutajad simulatsiooni või sisestamise ajal saavad, ainult arvestusvaluuta ja aruandlusvaluuta erinevusi. See ei näita neid kandevaluutas, kuna ühel kandel võib olla rohkem kui üks kandevaluuta ja tööleht võib sisaldada kandeid eri kandevaluutades. Seetõttu on oluline käsitsi üle kontrollida, et iga kande, millel on ainult üks kandevaluuta, summad oleks tasakaalus.

### <a name="transaction-currency"></a>Kande valuuta

Simulatsiooni ja sisestamise ajal kontrollib süsteem, et iga kanne, millel on ainult üks kandevaluuta, oleks kandevaluutas tasakaalus. Iga sisestatud kande puhul võib kandevaluuta jaoks olla üks või mitu valuutat. Näiteks võib pearaamatus sisestatud kandel olla kaks kandevaluutat, kui sularaha kantakse üle pangakontolt, mis kasutab eurosid (EUR) pangakontole, mis kasutab Kanada dollareid (CAD).

Kui kandel on ainult üks kandevaluuta, peab selle kande puhul deebetite kogusumma võrduma kandevaluuta kreeditite kogusummaga. Klientidel on esinenud järgmiseid stsenaariume, kus sisestamine nurjus õigesti, kuna kandevaluuta summad polnud tasakaalus.

- Deebetite ja kreeditite kogusummad **ei** olnud kandevaluutas tasakaalustatud, kuid need olid tasakaalus arvestusvaluuta ning aruandlusvaluuta jaoks. Klient eeldas, et kanne ikkagi sisestatakse. Kuid eeldus oli vale. **Kande kandevaluuta summad peavad olema alati tasakaalus, kui kõikidel kande ridadel on sama kandevaluuta.**
- Kanne imporditi andmeüksusega andmehalduse raamistiku (DMF) kaudu ja kasutaja sai aru, et kande valuutasummad tasakaalustati. Imporditud failil olid mõned summa rohkem kui kaks kümnendkohta ja importimisel kaasati rohkem kui kaks kümnendkohta. Seetõttu ei olnud deebetid ja kreeditid võrdsed, kuna need erinesid sendi murdosa võrra. Tööleht ei peegeldanud seda erinevust kanderidadel, kuna kuvatavatel summadel on ainult kaks kümnendkohta.
- Kanne imporditi DMF-i kaudu koos andmeolemiga ja kasutaja arvas, et kandevaluuta summad olid tasakaalus. Kuigi **kanne** oli tasakaalus, olid mõnedel kanderidadel erinevad kandekuupäevad. Kui lisasite kandevaluuta deebetite ja kreeditite kogusummad **kande ja kandekuupäeva** kohta, ei olnud need tasakaalus. Nõue jõustatakse, kui sisestate kande süsteemi pearaamatu kaudu. Ent seda ei jõustata, kui kanne imporditakse DMF-i kaudu koos andmeüksusega.

Ühes toetatud stsenaariumis võib kandel olla rohkem kui üks kandevaluuta. Sel juhul süsteem **ei** kontrolli, et deebetid oleksid kandevaluutas kreedititega võrdsed, kuna valuutad ei kattu. Selle asemel kontrollib süsteem, et arvestusvaluuta ja aruandlusvaluuta summad oleksid tasakaalustatud.

### <a name="accounting-currency"></a>Arvestusvaluuta

Kui kande kõigil ridadel on sama kandevaluuta ja kui kandevaluuta summad on tasakaalustatud, kontrollib süsteem, et arvestusvaluuta summad oleks tasakaalustatud. Kui kanne sisestatakse välisvaluutas, kasutatakse kanderidade vahetuskurssi kandevaluuta summade teisendamiseks arvestusvaluutasse. Kõigepealt teisendatakse iga kanderida ja ümardatakse kahe komakohani. Seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusummad. Kuna iga rida on teisendatud, ei pruugi deebetite ja kreeditite kogusummad tasakaalus olla. Sellest hoolimata, kui erinevuse absoluutväärtus jääb lehel **Pearaamatu parameetrid** määratletud väärtuse **Suurim sendierinevus** sisse, kanne sisestatakse ja erinevus sisestatakse automaatselt sendierinevuse kontole.

Kui kandel on rohkem kui üks kandevaluuta, teisendatakse kande iga rida arvestusvaluutasse kahe komakohani ja seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusumma. Tasakaalustamiseks tuleb deebetid ja kreeditid tasakaalustada arvestusvaluutas.  Sendierinevuse kontot ei lisata kunagi arvestusvaluutas kandele deebetite ja kreeditite saldosse viimiseks. 

### <a name="reporting-currency"></a>Aruandlusvaluuta

Kui kande kõigil ridadel on sama kandevaluuta ja kui kandevaluuta summad on tasakaalustatud, kontrollib süsteem, et aruandlusvaluuta summad oleks tasakaalustatud. Kui kanne sisestatakse välisvaluutas, kasutatakse kanderidade vahetuskurssi kandevaluuta summade teisendamiseks aruandlusvaluutasse. Kõigepealt teisendatakse iga kanderida ja ümardatakse kahe komakohani. Seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusummad. Kuna iga rida on teisendatud, ei pruugi deebetite ja kreeditite kogusummad tasakaalus olla. Sellest hoolimata, kui erinevus jääb lehel **Pearaamatu parameetrid** määratletud väärtuse **Suurim sendiümardus aruandlusvaluutas** sisse, kanne sisestatakse ja erinevus sisestatakse automaatselt sendierinevuse kontole.

Kui kandel on rohkem kui üks kandevaluuta, teisendatakse kande iga rida aruandlusvaluutasse kahe komakohani ja seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusumma. Tasakaalustamiseks tuleb deebetid ja kreeditid tasakaalustada aruandlusvaluutas.  Sendierinevuse kontot ei lisata kunagi aruandlusvaluutas kandele deebetite ja kreeditite saldosse viimiseks.

### <a name="example-for-an-accounting-currency-imbalance"></a>Arvestusvaluuta tasakaalustumatuse näide

> [!NOTE]
> Aruandlusvaluuta summa arvutatakse kandevaluuta summast samamoodi, nagu ka arvestusvaluuta summa.

Vahetuskurss: 1,5

| Rida | Vautšer | Konto | Valuuta | Deebet (kanne) | Kreedit (kanne) | Deebit (arvestus) | Kreedit (arvestus) |
|---|---|---|---|---|---|---|---|
| 1 | 001 | 1101-01 | EUR | 3.33 | | 5,00 (4,995) | |
| 2 | 001 | 1101-02 | EUR | 3.33 | | 5,00 (4,995) | |
| 3 | 001 | 1101-03 | EUR | 3.34 | | 5.01 | |
| 4 | 001 | 4101- | EUR | | 10.00 | | 15.00 |
| **Kokku** | | | | **10.00** | **10.00** | **15.01** | **15.00** |

Arvestusvaluuta on tasakaalust väljas 0,01-ga. Kui aga suurim sendi ümardamine arvestusvaluutas on vähemalt 0,01, sisestatakse erinevus automaatselt sendierinevuse kontole ja kanne sisestatakse edukalt.
