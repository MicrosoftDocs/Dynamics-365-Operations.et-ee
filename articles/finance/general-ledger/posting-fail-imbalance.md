---
title: Töölehe sisestamise tõrge tasakaalustamatuse tõttu
description: Teemas selgitatakse, miks deebetid ja kreeditid ei pruugi kandekannetes tasakaalustatud olla, mistõttu ei saa kandeid sisestada. Teema sisaldab ka etappe probleemi lahendamiseks.
author: kweekley
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-8-03
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a59724ff698b6ad0e84b0642240da5f8953ab3d1
ms.sourcegitcommit: 9642494da87c0d237f9fcbe15df14315d9e88fa2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/15/2021
ms.locfileid: "7385719"
---
# <a name="journal-posting-failure-because-of-imbalance"></a>Töölehe sisestamise tõrge tasakaalustamatuse tõttu

[!include [banner](../includes/banner.md)]

Teemas selgitatakse, miks deebetid ja kreeditid ei pruugi kandekannetes tasakaalustatud olla, mistõttu ei saa kandeid sisestada. Teema sisaldab ka etappe probleemi lahendamiseks.

## <a name="symptom"></a>Sümptom

Mõnel juhul ei saa töölehte sisestada ja kuvatakse järgmine teade: „Konkreetse kande kanded ei ole kindla kuupäeva seisuga tasakaalus (arvestusvaluuta: 0,01 – aruandlusvaluuta: 0,06)”. Miks ei saa töölehte sisestada?

## <a name="resolution"></a>Lahendus

Pearaamatusse sisestamisel peab iga kanne olema tasakaalustatud kandevaluutas, arvestusvaluutas ja aruandlusvaluutas, kui need valuutad on lehel **Pearaamatu seadistus** määratletud. (Kanded on tasakaalus, kui deebetite kogusumma võrdub kreeditite kogusummaga.)

Töölehe ridade lehe allosas kuvatakse kogusummad arvestusvaluutas ja aruandlusvaluutas. Neid **ei** kuvata kandevaluutas välisvaluuta kannete puhul. Samuti näitab tõrketeade, mille kasutajad simulatsiooni või sisestamise ajal saavad, ainult arvestusvaluuta ja aruandlusvaluuta erinevusi. See ei näita neid kandevaluutas, kuna ühel kandel võib olla rohkem kui üks kandevaluuta ja tööleht võib sisaldada kandeid eri kandevaluutades. Seetõttu on oluline kontrollida, et iga kande kandevaluuta summad oleks tasakaalus.

### <a name="transaction-currency"></a>Kande valuuta

Simulatsiooni ja sisestamise ajal kontrollib süsteem, et iga kanne oleks kandevaluutas tasakaalus. Iga sisestatud kande puhul võib kandevaluuta jaoks olla üks või mitu valuutat. Näiteks võib pearaamatus sisestatud kandel olla kaks kandevaluutat, kui sularaha kantakse üle pangakontolt, mis kasutab eurosid (EUR) pangakontole, mis kasutab Kanada dollareid (CAD).

Kui kandel on ainult üks kandevaluuta, peab selle kande puhul deebetite kogusumma võrduma kreeditite kogusummaga. Klientidel on esinenud järgmiseid stsenaariume, kus sisestamine nurjus õigesti, kuna kandevaluuta summad polnud tasakaalus.

- Deebetite ja kreeditite kogusummad **ei** olnud kandevaluutas tasakaalustatud, kuid need olid tasakaalus arvestusvaluuta ning aruandlusvaluuta jaoks. Klient eeldas, et kanne ikkagi sisestatakse. Kuid eeldus oli vale. **Kande kandevaluuta summad peavad olema alati tasakaalus, kui kõikidel kande ridadel on sama valuuta.**
- Kanne imporditi Microsoft Exceli kaudu ja kasutaja arvas, et kandevaluuta summad olid tasakaalus. Exceli töövihikus olid imporditud summad seadistatud **numbriliste** väärtustena, mitte **valuuta** väärtustena. Selles stsenaariumis oli töövihiku numbrisummadel rohkem kui kaks kümnendkohta ja importimisel kaasati rohkem kui kaks kümnendkohta. Seetõttu ei olnud deebetid ja kreeditid võrdsed, kuna need erinesid sendi murdosa võrra. Tööleht ei peegeldanud seda erinevust kanderidadel, kuna kuvatavatel summadel on ainult kaks kümnendkohta.
- Kanne imporditi Exceli kaudu ja kasutaja arvas, et kandevaluuta summad olid tasakaalus. Kuigi kanne oli tasakaalus, olid mõnedel kanderidadel erinevad kandekuupäevad. Kui lisasite deebetite ja kreeditite kogusummad kande ja kandekuupäeva kohta, ei olnud need tasakaalus. Nüüd süsteem ennetab seda stsenaariumi. Kandel võib olla ainult üks kandekuupäev. Nõue jõustatakse, kui sisestate kande süsteemi pearaamatu kaudu. Algselt seda ei jõustatud, kui kanne imporditi Exceli kaudu.

Ühes toetatud stsenaariumis võib kandel olla rohkem kui üks kandevaluuta. Sel juhul süsteem **ei** kontrolli, et deebetid oleksid kandevaluutas kreedititega võrdsed, kuna valuutad ei kattu. Selle asemel kontrollib süsteem, et arvestusvaluuta summad oleksid tasakaalustatud.

### <a name="accounting-currency"></a>Arvestusvaluuta

Kui kande kõigil ridadel on sama kandevaluuta ja kui kandevaluuta summad on tasakaalustatud, kontrollib süsteem, et arvestusvaluuta summad oleks tasakaalustatud. Kui kanne sisestatakse välisvaluutas, kasutatakse kanderidade vahetuskurssi kandevaluuta summade teisendamiseks arvestusvaluutasse. Kõigepealt teisendatakse iga kanderida. Seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusummad. Kuna iga rida on teisendatud, ei pruugi deebetite ja kreeditite kogusummad tasakaalus olla. Sellest hoolimata, kui erinevus jääb lehel **Pearaamatu parameetrid** määratletud väärtuse **Suurim sendierinevus** sisse, kanne sisestatakse ja erinevus sisestatakse automaatselt sendierinevuse kontole.

Kui kandel on rohkem kui üks kandevaluuta, teisendatakse kande iga rida arvestusvaluutasse ja seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusumma. Tasakaalustamise kehtivaks lugemiseks peavad deebetid ja kreeditid olema tasakaalus ning sendiümarduse erinevusi ei tohi olla.

### <a name="reporting-currency"></a>Aruandlusvaluuta

Kui kande kõigil ridadel on sama kandevaluuta ja kui kandevaluuta summad on tasakaalustatud, kontrollib süsteem, et aruandlusvaluuta summad oleks tasakaalustatud. Kui kanne sisestatakse välisvaluutas, kasutatakse kanderidade vahetuskurssi kandevaluuta summade teisendamiseks aruandlusvaluutasse. Kõigepealt teisendatakse iga kanderida. Seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusummad. Kuna iga rida on teisendatud, ei pruugi deebetite ja kreeditite kogusummad tasakaalus olla. Sellest hoolimata, kui erinevus jääb lehel **Pearaamatu parameetrid** määratletud väärtuse **Suurim sendiümardus aruandlusvaluutas** sisse, kanne sisestatakse ja erinevus sisestatakse automaatselt sendierinevuse kontole.

Kui kandel on rohkem kui üks kandevaluuta, teisendatakse kande iga rida aruandlusvaluutasse ja seejärel read summeeritakse, et määrata deebetite ja kreeditite kogusumma. Tasakaalustamise kehtivaks lugemiseks peavad deebetid ja kreeditid olema tasakaalus ning sendiümarduse erinevusi ei tohi olla.
