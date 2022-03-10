---
title: Vooeraldus
description: See teema kirjeldab, kuidas seadistada vooeralduse samme, k.a paralleeltöötluse lubamine.
author: Mirzaab
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 527bd24d7f2e9a05f6e617c222005186520f9968
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103784"
---
# <a name="wave-allocation"></a>Vooeraldus

[!include [banner](../includes/banner.md)]

Voo töötlemine võib olla aeganõudev ning suurem osa töötlemisajast kulub eraldamise sammus ja töö loomise etapis.

Nüüd on võimalik käivitada kõik need sammud paralleelselt, mis võib parandada voo töötluse jõudlust ja võimaldada suurema voogude läbilaske samas laos. See teema kirjeldab, kuidas seadistada voo eraldusviisi paralleelselt käitamiseks. Lisateavet selle kohta, kuidas seadistada töö loomine paralleelselt käivituma, vaadake teemast [Planeeritud töö loomine voo ajal](configure-wave-schedule-work-creation.md).

Varem oli võimalik eraldada korraga ainult üks voog laos. See piirang on eemaldatud ja asendatud uue piiranguga, mis lukustab ainult selle üksuse ja mõõtmed, mis asuvad reserveerimishierarhias asukohast kõrgemal. Asukohast ülalpool asuvates dimensioonides on alati tootedimensioonid. Näiteks kui kaup on konfigureeritud *värvi* abil, saab igat varianti (*punase*, *sinise* ja *kollase*) töödelda paralleelselt.

See tähendab, et kui sama voog, millel on samad mõõtmed asukoha kohal, eraldatakse ühe voo poolt, peavad teised vood ootama sama elemendi ja mõõtmete lukustumist. Kui lukustada õigeaegselt ei saa, ilmneb tõrge ja voo töötlemine nurjub.

Paralleeltöötluse kasutamiseks tuleb voog käivitada partiina.

## <a name="performance-improvements"></a>Jõudluse parendused

Paralleeltöötluse jõudluse eeliseid saab jagada kahte kategooriasse.

- **Täiustatud läbilask** – voogude läbilaskevõime parandab tavaliselt isegi siis, kui paralleeltöötlust ei konfigureerita, eriti stsenaariumite puhul, kus kaubad voogudes ei kattu.
- **Ühe voo eralduse parandamine** – kliendi andmete testimine on pärast paralleeleraldusse lülitumist kuvanud 50% jõudluse kasvu. Paralleelne töötlemine toimub asukoha kohal asuvate üksuste ja mõõtmete kohta, nii et täiustused sõltuvad sellest, kui palju erinevaid elemente voog sisaldab, olemasolevast infrastruktuurist ja eraldamise kestusest versus töö loomise kestus.

## <a name="configure-parallel-allocation"></a>Paralleeleralduse konfigureerimine

### <a name="warehouse-management-parameters"></a>Laohalduse parameetrid

Paralleelse eraldamistöötluse kasutamiseks minge **Laohaldus > Häälestus > Laohalduse parameetrid**, avage vahekaart **Voo töötlemine** ja seadistage järgmiselt.

- **Voo töötlemise partiigrupp** – valige partiigrupp, mida voogude esmane töötlemine peaks kasutama. Järgnevat eraldamise töötlemist saab teha erinevate partiigruppide abil.
- **Voogude töötlemine partiina** – paralleeltöötluse kasutamiseks määrake selle väärtuseks *Jah*.
- **Lukustuse ooteaeg (ms)** - sisestage aeg (millisekundites), mille jooksul ootab eraldamise etapp süsteemiressurssi, mille on lukustanud muu eraldamise etapp. Kui aeg ületatakse, siis voogu ei töödelda ja kuvatakse tõrketeade. Soovitame teil lubada vähemalt mõned sekundid ühe loogilise üksuse eraldamise lõpetamiseks.

Teavet nende ja muude voo töötlemise valikute kohta lehel **Laohalduse parameetrid** vt [Voo töötlemise laoparameetrid](wave-warehouse-parameters.md).

## <a name="wave-process-methods"></a>Voo töötlemise meetodid

Paralleeltöötluse seadistamiseks toimige järgmiselt.

1. Avage jaotis **Laohaldus > Seadistus > Vood > Voo protsessi meetodid**.
1. Valige ruudustiku `allocateWave` meetod.
1. Valige toimingupaanilt suvand **Ülesande konfiguratsioon**.
1. Avaneb leht **Voo sisestamismeetodi ülesande konfiguratsioon**. See ruudustik loetleb iga lao, kus te `allocateWave` meetodi konfigureerinud olete. Paralleeltöötlust kasutatakse ainult loetletud ladudes. Vastavalt vajadusele saate toimingupaani nuppe kasutada ladude lisamiseks või nende eemaldamiseks. 
1. Iga lao jaoks seadistage järgnev.
    - **Partiiülesannete maksimaalne arv** – määrake partiiülesannete arv, mida peaks valitud lao puhul eraldamisel kasutada. Partiiülesannete optimaalne arv sõltub saadaolevast infrastruktuurist ja sellest, milliseid muid partiitöid serveris töödeldakse. Katsed nelja põhikeskkonnaga, mida voo töötlemiseks tehti, näitavad, et kaheksa ülesande kasutamine on andnud hea tulemuse.
    - **Voo töötlemise partiigrupp** – eri ladude puhul saab kasutada kindlaid partiigruppe, et lubada eraldamistöötlust lao laiendamiseks.

## <a name="enable-or-disable-parallelization-across-all-legal-entities"></a>Paralleelsuse lubamine või keelamine kõigi juriidiliste isikute lõikes

Soovitame seadistada meetodi `allocateWave` käivituma paralleelselt kõigi juriidiliste isikute vahel, sest see aitab parandada voo töötluse jõudlust. Hankeahela halduse versioonis 10.0.17 *käivitatakse* voo paralleelsuse funktsioon Voo eraldamise meetodi funktsiooni jaoks vaikimisi sisse lülitatud kõigi uute ja uuendatud installide puhul ning seda ei saa enam välja lülitada. Pärast selle funktsiooni lubamist leiab aset järgmine.

- `allocateWave` meetodit värskendatakse, et kaasata ülesande konfiguratsiooni säte, mis võimaldab teil kasutada lehte **Vooprotsessi meetodid**, et määrata üheaegselt käitatud ülesannete arv, mis on võrdne paralleelprotsesside arvuga. Seetõttu vähendatakse voo eraldamise sammus kasutatud aega (mis on tavaliselt 30% kuni 60% kogu töötlemisajast) ülesannete arvuga ligikaudselt võrdse teguri võrra. Võimalik on valida ka, milline partii määratakse nende ülesannete töötlemiseks. Oluline on märkida, et kõik teie juriidilised isikud konfigureeritakse töötlema voogusid pakktöötluseks. Ladude puhul, mis on juba konfigureeritud töötlema laineid partiitöötlusena ja ladude puhul, mis on juba konfigureeritud kasutama meetodit `allocateWave` paralleelselt, säilitatakse olemasolev konfiguratsioon.
- Vaikimisi konfigureeritakse kõik uued juriidilised isikud töötlema voogusid partiitöötlusena. Kõigil uutel **laohaldusprotsesside** suvandiga lubatud ladudel on meetod `allocateWave` konfigureeritud käivituma vaikimisi paralleelselt.
- Lehel **Laohalduse parameetrid** on **partiitööna töötlemiseks salvestatud** väärtuseks seatud *Jah* ja **lukustuse ooteaja (ms)** väärtuseks on seatud vaikimisi 15 sekundit. See tähendab, et kõik vood käivitatakse partiitöötlusega. Kui voog töötab, omandab see lukustuse kauba ja mõõtude kohta eraldamise etapis. Kui järgnev voogtöötlemise ülesanne püüab omandada identsele kirjele sama lukku, on see blokeeritud, kuni praegune protsess pole lõppenud. **Lukustuse ooteaja (ms)** sätted loovad maksimumaja, mida süsteem ootab enne luku vabastamist.

Paralleelse eraldamise töötlemine nõuab voo töötlemist partii kaupa. Seega vähendate voo töötlemise jõudlust, kui lülitate välja sätte **Töötluse salvestamine partiina**, eriti kui voo töötlemine kasutab paralleelprotsessi, mille määras ülesande konfiguratsioon asjakohaste voomeetodite jaoks.

Vajadusel saate tagasi võtta kõik vaikimisi tehtud sätted, kui funktsioon *Voo paralleeliseerimine voo eraldamise meetodi jaoks* on teie eksemplari jaoks automaatselt lubatud. Selleks tehke järgmist.

- Avage **Laohaldus \> Seadistus \> Laohalduse parameetrid**. Vahekaardil **Voo töötlemine** rakendatakse soovituslikud väärtused suvanditele **Voogude töötlemine pariina** ja **Lukustuse ooteaeg (ms)**.
- Avage jaotis **Laohaldus \> Seadistus \> Vood \> Voo protsessi meetodid**. Valige `allocateWave` meetod. Tegumiribal valige **Toimingu konfiguratsioon**, et avada lehekülg, mis loetleb iga lao, kus meetod on seadistatud paralleelseks. Vajadusel muutke või kustutage iga loetletud lao partiiülesannete arv ja määratud voo grupp.

## <a name="troubleshooting"></a>Tõrkeotsing

### <a name="troubleshoot-using-the-infolog"></a>Teabelogi tõrkeotsing

Kuna kasutatakse partii raamistikku, fikseeritakse voo töötlemisel ilmnevad tõrked partiitööde teabelogide osana. Vooga seotud partiitööde lugemine.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Siin saate valida voo, mida soovite uurida.
1. Valige toimingupaanil vahekaart **Voog** ning valige rühmas **Voog** suvand **Partiitööd**.

Voo töötlemine on enesemääratlemine, seega tuleks mis tahes töötlemise käigus tuvastatud tõrkest teatada teabelogi abil.

Paralleeltöötlusega seotud tavaline tõrge võib olla see, et kaks voogu proovivad eraldada sama kaupa korraga ja üks ei lõpeta seda nii, et teine voog ei suuda määratud aja jooksul lukustada. Kui selline olukord ilmneb, sisaldab partiitööde logi teavet, mis ütleb, et kauba lukku ei saanud hankida. Sel juhul tuleb nurjunud voogu uuesti töödelda.

Kuna töötlemine toimub paralleelselt, tuleb andmeid töötlemise oleku jälgimiseks säilitada erinevates tabelites. See tähendab, et partiitööde logid võivad sisaldada vigu, nagu duplikaatvõtme tõrked.

Partiiülesannete tõrked on ka partiitööde logi osa. Kõige olulisem teave on tavaliselt allosas.

Harvadel juhtudel, nt SQL-i ühenduse katkemisel, võib voo töötlemine lõppeda vastuolus olekus, kus partiitöö töötab, kuid töötlemine on peatatud. Voog ei saa sellist tõrkeid käsitseda, seega püütakse järgmise voo käitamisel nurjunud voogusid puhastada. Teise võimalusena, kui praegune voog on vastuolus olekus, tehke järgmist.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Valige puhastatav voog.
1. Valige toimingupaanil vahekaart **Voog** ning valige rühmas **Voog** suvand **Vooandmete puhastamine**.

### <a name="troubleshoot-using-the-wave-progress-log"></a>Voo protsessi logi tõrkeotsing

Kui suvand **Loo voo edenemise logi** on lehel **Laohalduse parameetrid** lubatud, luuakse logikirje iga kord, kui kauba jaoks eraldamine toimub ja selle dimensioonid algavad ja lõpevad. Lubage see logi ainult siis, kui vajate seda nt algsel testimisel või tõrkeotsingul. Kui see suvand on lubatud, saate logi vaadata järgmiste sammude abil.

1. Avage **Laohaldus \> Väljaminevad vood \> Saadetise vood \> Kõik vood**.
1. Siin saate valida voo, mida soovite uurida.
1. Avage tegumiriba vahekaart **Voog** ja grupis **Voog** valik **Progress**.
