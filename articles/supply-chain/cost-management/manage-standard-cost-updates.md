---
title: Standardomahinna värskenduste haldus
description: 'Standardomahinna andmete värskendusi saab hallata kahte erinevat lähenemist kasutades: üheversiooniline lähenemine ja kaheversiooniline lähenemine.'
author: AndersGirke
manager: tfehr
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a7beeafa6d0bb22a687278ccebc3127409e1ee0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214732"
---
# <a name="manage-standard-cost-updates"></a>Standardomahinna värskenduste haldus

[!include [banner](../includes/banner.md)]

Standardomahinna andmete värskendusi saab hallata kahte erinevat lähenemist kasutades: üheversiooniline lähenemine ja kaheversiooniline lähenemine. 

Üheversiooniline lähenemine kasutab üht kuluversiooni, mis sisaldab kõiki kulukirjeid. Need kirjed sisaldavad algseid kulusid ja kõiki kulu värskendusi.

Kaheversiooniline lähenemine kasutab üht versiooni, mis sisaldab algsete kulude kirjeid, ja teist versiooni, mis sisaldab kõiki kulude värskenduste kirjeid. Kaheversioonilise lähenemise peamiseks eeliseks on kulu värskenduste selge kirjeldus ja jälgimine eraldiolevas kuluversioonis ilma, et see mõjutaks originaalkuluversiooni. Kaheversioonilist lähenemist saab kasutada mitme järkjärgulise värskenduse tuvastamisel, kus igale järkjärgulisele värskendusele on eraldi järkjärgulisi kulukirjeid sisaldav kuluversioon. 

**Näide** 

Järgmine näide illustreerib, kuidas üheversioonilist ja kaheversioonilist lähenemist saab tootmiskeskkonnas standardomahinna värskendamiseks kasutada. Näiteks värskendused, mis kajastavad uusi kaupu või tõrke parandusi. Oletame, et üksik kuluversioon kajastab praeguse aasta standardomahindu. Selle versiooni kood on 2016‑STD. Versioon 2016-STD sisaldab kõikide kaupade praeguseid aktiivseid kulusid. Peale selle sisaldab see kõiki protsessiga seotud kulukategooriaid ja üldkulude arvutamisvalemeid, mida teati 2016. aasta alguses. 2016‑STD on algne kuluversioon.

-   **Üheversiooniline lähenemine kuluandmete värskendustele** – üheversioonilise lähenemise puhul sisaldab algne kuluversioon 2016‑STD kõiki kulukirjeid. Kulu värskendused salvestatakse kuluversiooni 2016‑STD ning nende olekuks määratakse Ootel. Ootel kulusid saab käsitsi uute ostetud kaupade jaoks sisestada või arvutada toodetud kauba parandusi kajastama. Üheversioonilise lähenemise puhul ei ole nõutav koosluse arvutuste taande andmeallikas, kuna kõik aktiivsed kulud sisalduvad kuluversioonis. Ootel kulude aktiivseks saamise järgselt sisaldab algne kuluversioon 2016-STD taas kõiki praeguseid aktiivseid kulusid.
-   **Kaheversiooniline lähenemine kuluandmete värskendustele** − kaheversiooniline lähenemine nõuab täiendavat kuluversiooni, mis sisaldab ainult kulu värskendusi. Selle versiooni kood on 2016‑STD‑MUUDATUSED. Kulu värskendused salvestatakse kuluversiooni 2016‑STD-CHANGES ning nende olekuks määratakse „Ootel”. Kaheversioonilise lähenemise puhul on nõutav toodetud kaupade ootel kulude taande andmeallikas. See on vajalik, kuna täiendav kuluversioon 2016‑STD‑MUUDATUSED sisaldab ainult kuluandmete alamkogumit. Taande saab esitada aktiivse kuluna või kuluversioonina 2016-STD, sest mõlemad tuvastavad kuluandmete allika, kui see ei sisaldu versioonis 2016-STD-MUUDATUSED. Ootel kulude aktiivseks saamise järgselt sisaldab kuluversioon 2016-STD-MUUDATUSED aktiivseid kulusid, mis kajastavad värskendusi, samas algne kuluversioon 2016-STD jääb puutumata. Kaheversioonilist lähenemist kasutades tuleks algse kuluversiooni blokeerimispoliitikad määrata värskendusi ennetama. Täiendava kuluversiooni jaoks tuleks määrata identsed blokeerimispoliitikad, v.a kindla alguskuupäeva ja värskenduste valikuliste blokeerimispoliitikate lubamise puhul. Määratud alguskuupäeva peab värskendama iga muudatuse korral, et kajastada plaanitud aktiveerimise kuupäeva.

Selles näites on aasta 2016 värskenduste haldamisel kasutatud täiendavat üht kuluversiooni. Kasutada saab rohkem kui üht täiendavat kuluversiooni, näiteks iga värskenduste partii puhul võib kasutada eraldi versiooni. Kui kasutusel on rohkem kui üks täiendav kuluversioon, peab taande esitama aktiivsete kuludena, sest need jaotatakse mitme kuluversiooni vahel.





