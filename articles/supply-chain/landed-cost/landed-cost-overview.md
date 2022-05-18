---
title: Tarnehinna moodul
description: Tarnehinna moodul aitab ettevõtetel muuta sissetulevaid lähetustoiminguid, andes kasutajatele täieliku finants- ja logistilise kontrolli imporditud veose üle, tootjalt lattu.
author: Weijiesa
ms.date: 12/07/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: aa6f3baf6e6d980ac3c15e2045d1fcdef08ec296
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/04/2022
ms.locfileid: "8694623"
---
# <a name="landed-cost-module"></a>Tarnehinna moodul

[!include [banner](../../includes/banner.md)]

**Tarnehinna** moodul aitab ettevõtetel muuta sissetulevaid lähetustoiminguid, andes kasutajatele täieliku finants- ja logistilise kontrolli imporditud veose üle, tootjalt lattu. Imporditud kaupade puhul võivad tarnehinnad ulatuda 40 või enam protsendini iga imporditud kauba kogukulust. Seetõttu peab rakendus andma täpsed hinnangud tarnehindade kohta.

Ettevõtted saavad tarnehindasid kasutada järgmiste ülesannete täitmiseks:

- Hinnata tarnehindasid reisi loomisel.
- Väljastatavate kulude kulude ülekandmine mitmele kaubale ja ostutellimustele või üleviimistellimustele ühe reisi jooksul.
- Toetada kaupade üleviimist füüsiliste asukohtade vahel, hinnates tarnehindasid.
- Saate tuvastada transiidis kaupade viitvõlad.

Tarnehind annab täpsed ja kiired kuluhinnangud tarnehindade lisakuludele. Samal ajal pakub see suurendatud finants- ja logistilist nähtavust laiendatud tarneahelas. Samuti aitab see vähendada omahinnaarvestuse ja kuluarvestuse vigade haldust.

## <a name="highlights"></a>Tähtsündmused

### <a name="voyages"></a>Reisid

Tarnehinna puhul on reis eristatav liikumine väljastusasukohast läbi kindlate sihtkohtade kindlaksmääratud perioodil kindlaksmääratud saabumislao asukohta. Ostutellimusi ja tellimuse ridu saab reisi jaoks lisada kas ühele konteinerile või mitmele konteinerile ja kulud eraldatakse kaubareale õigesti. 

### <a name="item-ownership"></a>Kauba omand

Microsoft Dynamics 365 Supply Chain Management süsteemis on kaubad tavaliselt vastu võetud laos ja seejärel arveldatud. Kuid enamiku rahvusvaheliste kaubanduslepete raames võtab ettevõte kaupade omandi alates algsest sadamast lahkumise ajast, enne kui need on füüsiliselt kätte saadud. Tarnehind võimaldab ettevõtetel kaupadega arveldada enne, kui nad on füüsiliselt kätte saadud. Seda kontseptsiooni nimetatakse kaubad transiittellimuses. See loob uut tüüpi tellimuse, et hallata kaupade vastuvõtmist pärast algse ostutellimuse arveldamist.

### <a name="costs"></a>Kulud

Kui loote reisi tarnehinns, saab sellele automaatselt kulusid lisada. Need kulud seadistatakse Tarnehinnas ja nende jaoks on saadaval erinevad kuluvalikud ja kulualused. Iga kulu saab seadistada reisi erinevatele tasemetele ja jaotada kaubatasemele jaotamisreeglite kaudu, mis toetavad kogust, mahtu, kaalu, summat ja määratletud mahulisi jagajaid. Need arvestuslikud kulud annavad täpse hinnangu reisikulude kohta.

Tarnehind hõlmab seejärel hinnanguliste saabumiskulude esialgset kirjendamist, et tagada, et reisi loomise ajal esitatakse täpne hinnanguliste kulude arvutus. Kuna need automaatsed kulud arveldatakse, tühistatakse hinnangulised kulud ja asendatakse tegelike kuludega, mis põhinevad kuluarvetel.

Tegelikud kulud on ümberpööratud hinnangulised kulud, mis sisestatakse kuluarvelduse ajal, kasutades arvelduskontosid, mis on seadistatud iga kulu tüübi jaoks (nt maks, veos ja kindlustus). Need sisestused järgivad sisestuskäitumist, mis on seotud konkreetse kaubaga. Need uuendavad automaatselt lao sisestusi, olenemata sellest, kas sisestamistüüp on "esimene sisse, esimesena välja" (FIFO), "viimasena sisse, esimesena välja" (LIFO), liikuv kaalutud keskmine või liikuv keskmine. Toetatakse kõiki laomudeligrupi sisestamistüüpe. Liikuva keskmise ja standardkulu sisestamiseks on saadaval ostuhinna hälbekontod, et sisestada hinnanguliste kulude ja tegelike kulude vahelised erinevused.

### <a name="item-and-order-tracking"></a>Kauba ja tellimuse jälgimine

Kui reis liigub lähteasukohast lõppsihtlattu, saavad kasutajad vajadusel uuendada iga etappi või selle *sammu* teekonnast vastavalt soovile. Iga etapi puhul tuvastatakse täitmisaeg ja saadetise olek. Samuti tuvastatakse liikumise kinnitatud tarnekuupäevad reisi järgmisesse etappi. Koos annavad need tarnekuupäevad hinnangulise kaupade tarnekuupäeva sissetulevasse lattu. Kasutajad saavad neid tarnekuupäevi muuta. Sel juhul uuendatakse kaupade eeldatav tarnekuupäev automaatselt, põhinedes reisi etappide täitmisaegadel. Reisi ja laeva transiidis oleva kauba nähtavus on saadaval konteineri kohta enne kaupade sissetulekut. Kuna kuupäevad uuendatakse igal ostutellimuse real, on ettevõtetel logistika ja lao plaaneerimise üle rohkem kontrolli.

## <a name="landed-cost-concepts"></a>Tarnehinna mõisted

Järgmine tabel võtab kokku mõned tarnehinna põhimõisted.

| Mõiste | Kirjeldus |
|---|---|
| Reis | Tavaliselt on reisiks üks laev. Olenevalt teie tavadest ja protseduuridest võib see olla üks hankija või üks ostutellimus. Selle mõiste kasutamist ei piirata. |
| Foolio | Foolio määratakse sageli kindlaks tollieeskirjadega. See võib koosneda ühe hankija kaubast ühe üksuse/ettevõtte ja saadetise kohta. Kaubad lehel võivad olla ühes konteineris või jagatud mitme konteineri vahel. |
| Saatmiskonteiner | Konteineritesse on paigutatud ostutellimuste ridade kaubad. Nende tase on saadetise tasemest allpool. Neid kasutatakse tavaliselt juhul, kui kulud jagatakse kaupadele konteinerite kaupa või kui vastuvõtt toimub konteineri kohta. |
| Saatmiskonteineri tüüp | Saadetise konteineri tüübid võivad määrata kulutüübi hinna (nt veokulud). Need pakuvad ka kasulikku tarneteavet. |
| Kulu tüüp | Kulutüübid määratlevad impordiga seotud kulud, nt maks, veos ja kindlustus. |
| Automaatne kulu | Automaatsed kulud töötavad nagu kaubanduslepped. Automaatne kulu lingitakse reisi tasemega. |
| Sadam | Sadamad on piirkonnad, kust kaubad vastu võetakse ja üle antakse. |
| Laev | Laev on kaupade (nt laev või lennuk) transportimiseks kasutatav kandja. |
| Transiidis olevad kaubad | Sõltuvalt sätetest pannakse kaubad pärast arve uuendamist transiidilattu. |
| Tegevus | Tegevusi saab kasutada iga olulise reisi etapi salvestamiseks kahe sadama vahel. Neid saab kasutada kuupäevade uuendamiseks. |
| Teekonna mall | Reisimallid on teekonnad, mida kaubad kahe sadama vahel läbivad. |

**Tarnehinna** ja **Transpordihalduse** (TMS) moodulite terminoloogia ja funktsioonide võrdlemiseks vaadake [Tarnehind vs Transpordihaldus](landed-cost-vs-tms.md).
