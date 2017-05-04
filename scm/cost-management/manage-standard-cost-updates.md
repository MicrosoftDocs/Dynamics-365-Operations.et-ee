---
title: "Standardomahinna värskenduste haldus"
description: "Standardomahinna andmete värskendusi saab hallata kahte erinevat lähenemist kasutades: üheversiooniline lähenemine ja kaheversiooniline lähenemine."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 7e0f0817ff37c82ed98a51f10bcdde7e785a19a3
ms.lasthandoff: 03/31/2017


---

# <a name="manage-standard-cost-updates"></a>Standardomahinna värskenduste haldus

[!include[banner](../includes/banner.md)]


Standardomahinna andmete värskendusi saab hallata kahte erinevat lähenemist kasutades: üheversiooniline lähenemine ja kaheversiooniline lähenemine. 

Üheversiooniline lähenemine kasutab üht kuluversiooni, mis sisaldab kõiki kulukirjeid. Need kirjed sisaldavad algseid kulusid ja kõiki kulu värskendusi.
Kaheversiooniline lähenemine kasutab üht versiooni, mis sisaldab algsete kulude kirjeid, ja teist versiooni, mis sisaldab kõiki kulude värskenduste kirjeid. Kaheversioonilise lähenemise peamiseks eeliseks on kulu värskenduste selge kirjeldus ja jälgimine eraldiolevas kuluversioonis ilma, et see mõjutaks originaalkuluversiooni. Kaheversioonilist lähenemist saab kasutada mitme järkjärgulise värskenduse tuvastamisel, kus igale järkjärgulisele värskendusele on eraldi järkjärgulisi kulukirjeid sisaldav kuluversioon. **Näide.** Järgnev näide illustreerib, kuidas üheversioonilist ja kaheversioonilist lähenemist saab tootmiskeskkonnas standardomahinna värskendamiseks kasutada. Näiteks värskendused, mis kajastavad uusi kaupu või tõrke parandusi. Oletame, et üksik kuluversioon kajastab praeguse aasta standardomahindu. Selle versiooni kood on 2016‑STD. Versioon 2016-STD sisaldab kõikide kaupade praeguseid aktiivseid kulusid. Peale selle sisaldab see kõiki protsessiga seotud kulukategooriaid ja üldkulude arvutamisvalemeid, mida teati 2016. aasta alguses. 2016‑STD on algne kuluversioon.
-   **Üheversiooniline lähenemine kuluandmete värskendustele** – üheversioonilise lähenemise puhul sisaldab algne kuluversioon 2016‑STD kõiki kulukirjeid. Kulu värskendused salvestatakse kuluversiooni 2016‑STD ning nende olekuks määratakse Ootel. Ootel kulusid saab käsitsi uute ostetud kaupade jaoks sisestada või arvutada toodetud kauba parandusi kajastama. Üheversioonilise lähenemise puhul ei ole nõutav koosluse arvutuste taande andmeallikas, kuna kõik aktiivsed kulud sisalduvad kuluversioonis. Ootel kulude aktiivseks saamise järgselt sisaldab algne kuluversioon 2016-STD taas kõiki praeguseid aktiivseid kulusid.
-   **Kaheversiooniline lähenemine kuluandmete värskendustele** − kaheversiooniline lähenemine nõuab täiendavat kuluversiooni, mis sisaldab ainult kulu värskendusi. Selle versiooni kood on 2016‑STD‑MUUDATUSED. Kulu värskendused salvestatakse kuluversiooni 2016-STD-MUUDATUSED ning neile määratakse olek Ootel. Kaheversioonilise lähenemise puhul on nõutav toodetud kaupade ootel kulude taande andmeallikas. See on vajalik, kuna täiendav kuluversioon 2016‑STD‑MUUDATUSED sisaldab ainult kuluandmete alamkogumit. Taande saab esitada aktiivse kuluna või kuluversioonina 2016-STD, sest mõlemad tuvastavad kuluandmete allika, kui see ei sisaldu versioonis 2016-STD-MUUDATUSED. Kui ootel kulud muutuvad aktiivseks, sisaldab 2016-STD-CHANGES praegusi aktiivseid kulusid, mis kajastavad värskendusi, samas kui algne kuluarvestuse versioon 2016-STD jääb muutmata. Kui kasutatakse kahe versiooniga lähenemist, tuleb algse kuluarvestuse versiooni blokeerimispoliitikad seadistada nii, et need väldiksid värskendusi. Täiendava kuluversiooni jaoks tuleks määrata identsed blokeerimispoliitikad, v.a kindla alguskuupäeva ja värskenduste valikuliste blokeerimispoliitikate lubamise puhul. Määratud alguskuupäeva peab värskendama iga muudatuse korral, et kajastada plaanitud aktiveerimise kuupäeva.

Selles näites on aasta 2016 värskenduste haldamisel kasutatud täiendavat üht kuluversiooni. Kasutada saab rohkem kui üht täiendavat kuluversiooni, näiteks iga värskenduste partii puhul võib kasutada eraldi versiooni. Kui kasutusel on rohkem kui üks täiendav kuluversioon, peab taande esitama aktiivsete kuludena, sest need jaotatakse mitme kuluversiooni vahel.






