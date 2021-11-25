---
title: Numbriseeriate ülevaade
description: Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid.
author: SunilGarg
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: NumberSequenceTableListPage, NumberSequenceConfiguration
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom:
- "15461"
- intro-internal
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d65eb3824cfa158e6b382ee7bae2c86aab9396b
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778325"
---
# <a name="number-sequences-overview"></a>Numbriseeriate ülevaade

[!include [banner](../includes/banner.md)]

Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid. Koondandmete kirjet või kandekirjet, mis nõuab ID-d, nimetatakse *viiteks*.

Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma. Soovitame numbriseeriate häälestamiseks kasutada lehti jaotises **Organisatsiooni haldus**. Kui moodulipõhised sätted on nõutavad, saate mooduli parameetrite lehega määrata mooduli viidete numbriseeriad. Näiteks jaotises **Müügireskontro** ja **Ostureskontro** saate häälestada numbriseeriate grupid, et eraldada numbriseeriad konkreetsetele klientidele või hankijatele.

Kui häälestate numbriseeria, tuleb teil määrata ulatus, mis määratleb, milline organisatsioon numbriseeriat kasutab. Ulatus võib olla **Jagatud**, **Ettevõte**, **Juriidiline isik** või **Tootmisüksus**. Ulatused **Juriidiline isik** ja **Ettevõte** saab kombineerida atribuudiga **Rahanduskalendri periood** veelgi täpsemate numbriseeriate loomiseks.

Numbriseeria vorming koosneb segmentidest. Numbriseeriad, mille ulatus ei ole **Jagatud**, võivad sisaldada ulatusele vastavaid segmente. Näiteks numbriseeria, mille ulatus on **Juriidiline isik**, võib sisaldada juriidilise isiku segmenti. Kui kaasate numbriseeria vormingus ulatuse segmendi, saate kirje numbri alusel määrata konkreetse kirje ulatuse.

Peale ulatustele vastavate segmentide võivad numbriseeriate vormingud sisaldada segmente tüübiga **Konstantne** ja **Tähe- ja numbrimärkidest koosnevad segmendid**. Segment **Konstantne** sisaldab tähtede, numbrite või sümbolite muutumatut kogumit. **Tähe- ja numbrimärkidest** koosnev segment sisaldab tähtede või numbrite kogumit, mis suureneb iga kord, kui numbrit kasutatakse. Kasvavate numbrite tähistamiseks kasutage numbriosundit (\#), kasvavate tähtede jaoks ampersandi. Näiteks vorming \#\#\#\#\#\_ 2017 loob seeria 00001\_ 2017, 00002\_ 2017 jne.

## <a name="number-sequence-examples"></a>Numbriseeriate näidised

Järgmised näited selgitavad, kuidas kasutada segmente numbriseeriate vormingute loomiseks. Täpsemalt kajastavad näited ulatuse segmentide kasutamise mõju.

### <a name="expense-report-numbers"></a>Kuluaruande numbrid

Järgmises näites on kuluaruande numbrid häälestatud juriidilise isiku jaoks, mis kannab nime **CS**.

- **Ala:** Reisimine ja kulud
- **Viide:** kuluaruande number
- **Ulatus:** juriidiline isik
- **Juriidiline isik:** CS

| Segmendid  | Segmendi tüüp | Väärtus     |
|-----------|--------------|-----------|
| 1. segment | Juriidiline isik | CS        |
| 2. segment | Konstant     | -EXPENSE- |
| 3. segment | Tärk | \#\#\#\#  |

**Vormindatud numbri näide**: CS-EXPENSE-0039

Saate häälestada sarnased numbriseeriavormingud muude juriidiliste isikute jaoks. Näiteks kui muudate juriidilise isiku **RW** puhul ainult juriidilise isiku segmendi väärtust, on vormindatud number RW-EXPENSE-0039. Samuti saate muuta tervet numbriseeriavormingut muude juriidiliste isikute jaoks. Näiteks saate välistada juriidilise isiku ulatuse segmendi, et luua vormindatud number, näiteks Exp-0001.

### <a name="sales-order-numbers"></a>Müügitellimuste numbrid

Järgmises näites on müügitellimuse numbrid häälestatud ettevõttele, mille ID on **CEU**.

- **Ala:** müük
- **Viide:** müügitellimus
- **Ulatus:** ettevõte
- **Ettevõte:** CEU

| Segmendid  | Segmendi tüüp | Väärtus    |
|-----------|--------------|----------|
| 1. segment | Konstant     | SO-      |
| 2. segment | Tärk | \#\#\#\# |

**Vormindatud numbri näide**: SO-0029

Kuigi vorming ei hõlma ulatuse segmenti, alustatakse nummerdamist uuesti iga ettevõtte ID puhul. Kui kasutate sama vormingut kõikide ettevõtete ID-de puhul, kasutatakse iga ettevõtte jaoks samu numbreid. Näiteks müügitellimuse numbrit SO-0029 kasutatakse iga ettevõtte puhul. Samuti saate muuta tervet numbriseeriavormingut muude ettevõtete ID-de jaoks.

### <a name="purchase-requisition-numbers"></a>Ostutaotluse numbrid

Järgmises näites kehtivad ostutaotluse numbrid kogu organisatsioonis.

- **Ala:** ost
- **Viide:** ostutaotlus
- **Ulatus:** ühiskasutatud

| Segmendid  | Segmendi tüüp | Väärtus    |
|-----------|--------------|----------|
| 1. segment | Konstant     | Req      |
| 2. segment | Tärk | \#\#\#\# |

**Vormindatud numbri näide**: Req0052

Kula ulatus on **Ühine**, kasutatakse numbriseeria vormingut kogu organisatsioonis. Te ei saa organisatsiooni erinevate osade jaoks häälestada erinevaid numbriseeria vorminguid.

## <a name="performance-considerations-for-number-sequences"></a>Numbriseeriate jõudluse kaalutlused

Enne numbriseeriate häälestamist võtke arvesse järgmist teavet selle kohta, kuidas numbriseeriate konfiguratsioon võib mõjutada süsteemi jõudlust.

### <a name="continuous-and-non-continuous-number-sequences"></a>Pidevad ja mittepidevad numbriseeriad

Numbriseeriad võivad olla pidevad ja mittepidevad. Pidev numbriseeria ei jäta vahele ühtki numbrit, kuid numbreid ei saa kasutada järjest. Mittepideva numbriseeria numbreid kasutatakse järjest, kuid numbriseeria võib numbreid vahele jätta. Näiteks kui kasutaja tühistab kande, luuakse number, kuid seda ei kasutata. Pidevas numbriseerias kasutatakse numbrit hiljem. Mittepidevas numbriseerias ei kasutata numbrit.

Pidevad numbriseeriad on tavaliselt nõutavad väliste dokumentide, näiteks ostutellimuste, müügitellimuste ja arvete puhul. Pidevad numbriseeriad võivad aga süsteemi reageerimist aeglustada, kuna süsteem peab taotlema numbrit andmebaasist iga kord, kui luuakse uus dokument või kirje.

Kui kasutate mittepidevat numbriseeriat, saate lubada valiku **Eelnev eraldamine** kiirkaardil **Jõudlus** lehel **Numbriseeriad**. Kui määrate eelnevalt eraldatavate numbrite koguse, valib süsteem numbrid ja talletab need mällu. Uusi numbreid taotletakse andmebaasist vaid pärast eelnevalt eraldatud koguse kasutamist.

Kui te ei pea eeskirjade kohaselt kasutama pidevaid numbriseeriaid, soovitame parema jõudluse huvides kasutada mittepidevaid numbriseeriaid.

### <a name="automatic-cleanup-of-number-sequences"></a>Numbriseeriate automaatne puhastamine

Toitekatkestuse, rakenduse tõrke või muu ootamatu vea puhul ei saa süsteem pidevate numbriseeriate numbreid automaatselt taaskasutada. Kaotsiläinud numbrite taastamiseks saate puhastamisprotsessi käsitsi või automaatselt käitada.

Puhastamisprotsessi plaanimisel võtke kindlasti arvesse serveri koormust. Soovitame puhastamist teha pakett-tööna tipptundidevälisel ajal.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
