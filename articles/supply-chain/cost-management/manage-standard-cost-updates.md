---
title: Standardomahinna värskenduste haldus
description: 'Standardomahinna andmete värskendusi saab hallata kahte erinevat lähenemist kasutades: üheversiooniline lähenemine ja kaheversiooniline lähenemine.'
author: AndersGirke
ms.date: 01/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventItemPrice, InventParameters
audience: Application User
ms.reviewer: kamaybac
ms.custom: 69992
ms.assetid: 468de7af-c7b5-4345-bd5a-ba3aa5a900cc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d4ea62a680c9bcf68de29f3e0d4cec8d5001c1563e988cbbd49eb961604072c8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764130"
---
# <a name="manage-standard-cost-updates"></a>Standardomahinna värskenduste haldus

[!include [banner](../includes/banner.md)]

Standardomahinna andmete värskendusi saab hallata kahte erinevat lähenemist kasutades: üheversiooniline lähenemine ja kaheversiooniline lähenemine.

Üheversiooniline lähenemine kasutab üht kuluversiooni, mis sisaldab kõiki kulukirjeid. Need kirjed sisaldavad algseid kulusid ja kõiki kulu värskendusi.

Kaheversiooniline lähenemine kasutab üht versiooni, mis sisaldab algsete kulude kirjeid, ja teist versiooni, mis sisaldab kõiki kulude värskenduste kirjeid. Kaheversioonilise lähenemise peamiseks eeliseks on kulu värskenduste selge kirjeldus ja jälgimine eraldiolevas kuluversioonis ilma, et see mõjutaks originaalkuluversiooni. Kaheversioonilist lähenemist saab kasutada mitme järkjärgulise värskenduse tuvastamisel, kus igale järkjärgulisele värskendusele on eraldi järkjärgulisi kulukirjeid sisaldav kuluversioon.

## <a name="example"></a>Näide

Järgmine näide illustreerib, kuidas üheversioonilist ja kaheversioonilist lähenemist saab tootmiskeskkonnas standardomahinna värskendamiseks kasutada. Näiteks värskendused, mis kajastavad uusi kaupu või tõrke parandusi. Oletame, et üksik kuluversioon kajastab praeguse aasta standardomahindu. Selle versiooni kood on 2020‑STD. Versioon 2020-STD sisaldab kõikide kaupade praeguseid aktiivseid kulusid. Peale selle sisaldab see kõiki protsessiga seotud kulukategooriaid ja üldkulude arvutamisvalemeid, mida teati 2020. aasta alguses. 2020‑STD on algne kuluversioon.

- **Üheversiooniline lähenemine kuluandmete värskendustele** – üheversioonilise lähenemise puhul sisaldab algne kuluversioon 2020‑STD kõiki kulukirjeid. Kulu värskendused salvestatakse kuluversiooni 2020‑STD ning nende olekuks määratakse Ootel. Ootel kulusid saab käsitsi uute ostetud kaupade jaoks sisestada või arvutada toodetud kauba parandusi kajastama. Üheversioonilise lähenemise puhul ei ole nõutav koosluse arvutuste taande andmeallikas, kuna kõik aktiivsed kulud sisalduvad kuluversioonis. Ootel kulude aktiivseks saamise järgselt sisaldab algne kuluversioon 2020-STD taas kõiki praeguseid aktiivseid kulusid.
- **Kaheversiooniline lähenemine kuluandmete värskendustele** − kaheversiooniline lähenemine nõuab täiendavat kuluversiooni, mis sisaldab ainult kulu värskendusi. Selle versiooni kood on 2020‑STD‑MUUDATUSED. Kulu värskendused salvestatakse kuluversiooni 2020‑STD-CHANGES ning nende olekuks määratakse Ootel. Kaheversioonilise lähenemise puhul on nõutav toodetud kaupade ootel kulude taande andmeallikas. See on vajalik, kuna täiendav kuluversioon 2020‑STD‑MUUDATUSED sisaldab ainult kuluandmete alamkogumit. Taande saab esitada aktiivse kuluna või kuluversioonina 2020-STD, sest mõlemad tuvastavad kuluandmete allika, kui see ei sisaldu versioonis 2020-STD-MUUDATUSED. Ootel kulude aktiivseks saamise järgselt sisaldab kuluversioon 2020-STD-MUUDATUSED aktiivseid kulusid, mis kajastavad värskendusi, samas algset kuluversiooni 2020-STD see ei mõjuta. Kaheversioonilist lähenemist kasutades tuleks algse kuluversiooni blokeerimispoliitikad määrata värskendusi ennetama. Täiendava kuluversiooni jaoks tuleks määrata identsed blokeerimispoliitikad, v.a kindla alguskuupäeva ja värskenduste valikuliste blokeerimispoliitikate lubamise puhul. Määratud alguskuupäeva peab värskendama iga muudatuse korral, et kajastada plaanitud aktiveerimise kuupäeva.

Selles näites on aasta 2020 värskenduste haldamisel kasutatud täiendavat üht kuluversiooni. Kasutada saab rohkem kui üht täiendavat kuluversiooni, näiteks iga värskenduste partii puhul võib kasutada eraldi versiooni. Kui kasutusel on rohkem kui üks täiendav kuluversioon, peab taande esitama aktiivsete kuludena, sest need jaotatakse mitme kuluversiooni vahel.

## <a name="financial-dimensions-for-the-standard-cost-revaluation"></a>Standardse kulu ümberhindamise finantsdimensioonid

[!INCLUDE [preview-banner-section](../../includes/preview-banner-section.md)]

Uue standardhinna aktiveerimine hindab tavaliselt vaba kaubavaru väärtuse ümber standardse kulu ümberhindamise kannete alusel. Tavaliselt sisestatakse kauba finantsdimensioonid seejärel kannetele. Samas kui soovite kontrollida, kas ja kuidas finantsdimensioone sisestatakse, kasutage [funktsioonihaldust](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), et lülitada sisse funktsioon nimega *Finantsdimensioonide vaikevalikud varude standardkulu ümberhindamise jaoks*. Pärast selle funktsiooni lubamist avage suvand **Kuluhaldus > Laoarvestuse poliitikate seadistus > Parameetrid** ja määrake uus ripploend **Finantsdimensiooni päritolu** ühega järgmistest väärtustest.

- **Puudub** – ümberarvutamise kannetesse ei sisestata finantsdimensioone. Kui teie konto struktuur hõlmab nõutavat finantsdimensiooni, käivitatakse ümberarvutamise protsess endiselt, kuid see loob raamatupidamiskirjed ilma finantsdimensioonideta. Sel juhul saavad kasutajad enne hoiatusteate, et nad saaksid ümberhindamise vajaduse korral tühistada.
- **Tabel** – kauba finantsdimensioonid sisestatakse ümberhindamise kannetele. See on vaikesäte ja järjepidev algse süsteemi käitumisega, lülitamata sisse funktsiooni *Finantsdimensioonide vaikevalikud varude standardkulu ümberhindamise jaoks*.
- **Sisestamine** – ümber arvutatava kande finantsdimensioonid sisestatakse ümberarvutamise kannetesse. Vaikimisi kasutatakse finantsdimensioone algse kande laokontolt nii laokonto kui ümberhindamise konto puhul.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]