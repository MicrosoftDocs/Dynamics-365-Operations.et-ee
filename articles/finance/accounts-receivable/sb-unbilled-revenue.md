---
title: Arveldamata tulu
description: See teema kirjeldab, kuidas seadistada kaupu ja kontosid, et kasutada arveldamata tulu funktsiooni kordustellimuse arvelduses.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 4a5bd016649957d90876d4eb50c358cd9d6fba80
ms.sourcegitcommit: 836695c0e95d366ba993f34eee30f57191f356d8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2022
ms.locfileid: "8629700"
---
# <a name="unbilled-revenue"></a>Arveldamata tulu

See teema kirjeldab arveldamata tulu funktsiooni, mis võimaldab teil kaasata bilansile summad kogu arveldusgraafiku jaoks. Need summad on kaasatud arveldamata tulu kontole ja arveldamata tulu vastaskontole ja lepingu eest arveldatakse osamaksetena.

## <a name="set-up-unbilled-revenue"></a>Saate häälestada segmentimata tulu.

Segmentimata tulu seadistamiseks järgige neid samme.

- **Korduva lepingu arveldusparameetrite** lehel seadke väljad jaotises **Arveldamata** tulu.
- Segmentimata tulu funktsiooni saab kasutada kaupade puhul, mille välja **Kauba tüüp väärtuseks** on seatud **Standardne**. Seda saab kasutada ka viitvõla kaupade puhul. Arveldamata tulu kasutamiseks lühiajalise funktsiooniga seadistage **lühiajalised valikud korduvate lepingu arveldusparameetrite** lehel.

Kaupade häälestamiseks, et kasutada segmentimata tulu, järgige neid samme.

1. Vahekaardil Kaubad **valige vahekaardilt Lisa**, saate kuvada **kuluga segmendis** seadistatud **tulu**.
2. Valige kaubakood uuel **real** kaubakoodis.
3. **Väljal Kauba seos** valige kauba seos.
4. Ridade lisamiseks korrake neid samme.
5. Valige käsk **Salvesta**.

Kaupade ja saateleheta tulukontode häälestamiseks järgige neid samme.

1. Valige vahekaardil **Kontod valikuGa** Lisa, saate kuvada **kuluarvestamata** tulu häälestuslehe **.**
2. Valige kaubakood uuel **real** kaubakoodis.
3. **Väljal Kauba seos** valige kauba seos.
4. Saate valida tasakaalustamata tulu, skonto ja tasakaalustamata tulu vastaskonto kontod. Lühiajalise konto kasutamiseks **peate määrama lühiajalise tasumata meetodi väljaks Perioodide jooksvaks või Fikseeritud** **·** **·** **aastaks korduva lepingu arveldusparameetrite** lehel.
5. Ridade lisamiseks korrake neid samme.
6. Valige käsk **Salvesta**.

## <a name="use-unbilled-revenue"></a>Kasuta segmentimata tulu

1. Looge lehel **Kõik arveldusgraafikud** arveldusgraafik.
2. Kui kaup ei ole veel seadistatud kasutama arveldamata tulu, märkige **arveldusgraafiku** real ruut Arveldamata tulu.
3. Seadke valikuLiga **stamata tulu väärtuseks** **Jah**. Seejärel vaadake üle ja redigeerige vastavalt vajadusele kogumata tulu, allahindluse ja tulu vastaskontod.
4. Arveldamisgraafikus valige **arveldamata tulu** töötlemise all suvand Loo töölehe sisestus, **et** luua algne töölehe kanne arveldamata tulu jaoks. See samm tuleb lõpule viia enne arveldusgraafiku arveldamist.
5. Pärast algse töölehe sisestuse loomist valige käsk **Loo** arve müügitellimuste loomiseks ja sisestage arveldusgraafikute arved.
6. Pärast arvete sisestamist saate üle vaadata **auditi teabe vahekaardil Uuendamised** lehel **Kõik arveldusgraafikud**.

### <a name="milestone-billing"></a>Etapiviisiline arveldus

Vahe-eesmärgi arveldus töötab arveldamata tuluga järgmistel tingimustel:

- Kui vahe-eesmärgi emakaup on arveldamata (**ruut** Arveldamata tulu on märgitud) ja vahe-eesmärgi tütarüksuste eest arveldatakse (**arveldamata tulu märkeruut on tühi), peavad emakauba algus- ja lõppkuupäevad** olema määratud. Neid kuupäevi kasutatakse algse töölehe sisestuse loomiseks.
- Kui vahe-eesmärgi emakaup on arveldamata (**märkeruut** Arveldamata tulu on tühi) ja vahe-eesmärgi tütarüksuste eest arveldatakse (**on** märgitud ruut Arveldamata tulu), peab lõppkuupäeva määrama ainult tütarüksuste puhul, millele soovite töölehe esialgse kirje luua.

Iga vahe-eesmärgi tütarüksust saab eraldi töödelda. Lõppkuupäevi saab määrata siis, kui olete valmis looma algse töölehe sisestuse.

> [!NOTE]
> Kui vahe-eesmärgi emakauba või tütarkauba algne töölehe kirje on juba loodud või arve on loodud, ei saa algus- ja lõppkuupäevi redigeerida.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Segmentimata tulu koos lineaalse viitvõlaga

Segmentimata tulu kasutamiseks koos lineaalse viitvõlagraafikutega järgige neid samme.

1. Looge lehel **Kõik arveldusgraafikud** arveldusgraafik.
2. Lisage kaup arveldusgraafiku ridadele.
3. Valige **reale viitvõlad**.
4. Lehel Kande **viitvõlg** järgige neid samme.

    1. Määrake suvandi **Edasi lükatud** väärtuseks **Jah**.
    2. Muutke kontosid vastavalt vajadusele.
    3. Valige jaotises **Graafik** suvand **Linesioon ja** redigeerige muid väärtusi vastavalt vajadusele.
    4. Valige nupp **OK**.

5. Valige **reale tulu, mis** pole seotud arvega, ja järgige seejärel järgmisi samme:

    1. Seadke valikuLiga **stamata tulu väärtuseks** **Jah**.
    2. Valige kontod, mida kasutada tulu, allahindluse ja tulu vastaskontona.

6. Valige arveldusgraafiku jaotises Arveldamata **tulu töötlemine** suvand Loo **töölehe kanne**. Teise võimalusena kasutage **töölehe sisestuse loomiseks lehteBilled** revenue masstöötlus.
7. Luuakse viitvõlagraafik. Kõik viitvõlagraafikute **lehel olevad üksikasjad saate üle** vaadata. Pärast viitvõlagraafiku loomist saate redigeerida erinevaid väärtusi arveldusgraafiku reaüksuse jaoks. Näiteks saate redigeerida ühiku hinda, kogust või kuupäevi.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Saateleheta tulu koos sündmusepõhiste viitvõlgadega

Segmentimata tulu kasutamiseks koos sündmusepõhiste viitvõlagraafikutega järgige neid samme.

1. Looge lehel **Kõik arveldusgraafikud** arveldusgraafik.
2. Lisage kaup arveldusgraafiku ridadele.
3. Valige **reale viitvõlad**.
4. Lehel Kande **viitvõlg** järgige neid samme.

    1. Määrake suvandi **Edasi lükatud** väärtuseks **Jah**.
    2. Muutke kontosid vastavalt vajadusele.
    3. Valige jaotises **Graafik** suvand **Sündmusepõhine**, Mall **,** Eraldamise **tüüp ja** **Aegumiskonto**.
    4. Valige nupp **OK**.

5. Valige **reale tulu, mis** pole seotud arvega, ja järgige seejärel järgmisi samme:

    - Seadke valikuLiga **stamata tulu väärtuseks** **Jah**.
    - Valige kontod, mida kasutada tulu, allahindluse ja tulu vastaskontona.

6. Valige arveldusgraafiku jaotises Arveldamata **tulu töötlemine** suvand Loo **töölehe kanne**. Teise võimalusena kasutage **töölehe sisestuse loomiseks lehteBilled** revenue masstöötlus.
7. Luuakse viitvõlagraafik. Kõik viitvõlagraafikute **lehel olevad üksikasjad saate üle** vaadata. Pärast viitvõlagraafiku loomist saate redigeerida erinevaid väärtusi arveldusgraafiku reaüksuse jaoks. Näiteks saate redigeerida ühiku hinda, kogust või kuupäevi. Viitvõlagraafik arvutatakse uute väärtuste alusel ümber.

Jaotused arvutatakse ümber valitud eraldustüübi alusel (**Protsent**, **Valmimisprotsent või** Võrdsed **summad**). Muutuvate **summade** eraldamise tüübi puhul arvutatakse jaotus ümber sündmuse algväärtuse protsentuaalse ekvivalenti alusel. Ühiku alghind on näiteks $100.00 protsent algväärtusest on $55.00 (55 protsenti). Kui ühiku hind muudetakse ühiku $200.00, muutub sündmuse muutuvsumma $110.00 (ikka 55 protsenti).

> [!NOTE]
> Kui viitvõlagraafiku read on tuvastatud, ei saa arveldusgraafiku rea kaupa redigeerida. Reaüksuse redigeerimiseks peate esmalt tuvastatud read tühistama. Seejärel saab arveldusgraafiku rida uuendada.

### <a name="unbilled-revenue-and-top-billing"></a>Arveldamata tulu ja ülemine arveldus

Arveldusgraafik sisestatakse kolm aastat ja arveid arveldatakse kord aastas kolme aasta jooksul. Kogu lepingu summa kirjendatakse arveldamata tulukontole, mille põhjal aastaarved luuakse. Vastaskonto on tulu või viittulu konto.

Pidage meeles, et ülemine arveldamine ja arveldamata tulu ei tööta koos, kuna vastavusseviimise probleemid võivad esineda pearaamatus. Näiteks seadistatakse kaubagrupp **A** **kaubagrupi seadistuse lehel nii, et ülemise rea numbri välja** väärtuseks on **seatud 2**. **Arveldusgraafikute lehel** lisatakse kolm üksust. Kõik kolm kaupa kuuluvad kaubagruppi A. Kui tasumata tulu funktsiooni jaoks luuakse algne töölehe kirje, töödeldakse kõigi kolme kauba summat tasumata kontole. Kui luuakse arveldusgraafiku arve, kaasatakse ainult kahe ülemise kauba summad. Seetõttu ei vasta arve summa summale, mida on töödeldud arveldamata tulu kontole ja vastavusseviimise väljaminekud tekivad pearaamatus.

Kui soovite kasutada kulumata tulu, **jätke** kaubagrupi seadistusleht tühjaks või seadistage kõik kaubagrupid nii, **·** **et ülemise rea välja numbriks on seatud 0** (null). Kui soovite kasutada ülemist arveldust, pole ühtegi arveldamata tulutoimingut saadaval.

### <a name="examples"></a>Näited

Versiooni 10.0.27 puhul tutvustatakse uusi kontosid, kui kasutatakse segmentimata tulu. Kui sisestatakse algne **töölehe sisestamise** protsessi loomine, krediteeritakse uuele tasakaalustamata tulu vastaskontole. Seda kontot kasutatakse tulukonto asemel, sest sama väärtus tuleb arveldusgraafiku arveldamisel tühistada. Kui ilmneb vahetuskurss või ümardamiserinevused, võivad arve loomise protsessi **käigus arvutatud summad** olla erinevad. See käitumine tagab, et kontode netosumma on 0 (null).

See näide näitab, kuidas kasutada tasumata tulu kogu lepingu summa äratundmiseks bilansilehel tasumata tuluna. Kande teine pool on tasakaalustamata tulu vastaskonto. Kliendiga arveldamisel tühistatakse arveldamata tulu ja arveldamata tulu vastaskonto. Tulu tuvastamine toimub arveldamisel või vastavalt seadistatud viitvõla tuvastamise graafikule.

#### <a name="assumptions"></a>Eeldused

- Selle aasta 1. jaanuaril allkirjastab klient lepingu kolme aasta $390.
- Leping sisaldab kahte osa: litsentsid ja hooldusleping.
- Litsentsitasu müügihind on $300 kliendile arveldatakse iga lepinguaasta 1. $100 alusel. Litsentsi $300 tasu võetakse tuluna lepingu allkirjastamisel.
- Hooldustasu müügihinda $90 kliendile arveldatakse $30 1. jaanuaril. Hooldustasu $90 edasi lükatud ja $2.50 tuvastatakse lepingu iga kuu kohta.
- Kliendile arveldatakse arve $130 (1. jaanuar) igast lepingu kolmest aastast.

#### <a name="steps"></a>Etapid

1. Saate seadistada kaks vabastatud üksust saateleheta kaupadeks. Kasutage lehteBilled **revenue häälestus**, et seadistada kaubad ja kontod, mis kasutavadbilled tulu.
2. Selles näites on hooldustasu edasi lükatud. Kaup nõuab viitvõlamalli, mis on seadistatud viitvõla **mallide** lehel. Mallil on kuuperioodi **sagedus** ja tunnustusperioodi pikkus on 36 kuud. Seetõttu on tulu kuu kohta $2.50.
3. Vaikimisi lehel **Kaupade edasi lükatud** seadke välja **Hooldustasu väärtuseks** **Viitvõlgnev kaup**. See ja järgmine samm põhjustavad hooldustasu kauba edasilükkumise, kui seda müüakse või kaasatakse arveldusgraafikusse.
4. Valige **viitvõla vaikemall** \> **ning** lisage hooldustasule kaup ja lineaalne mall sammust 2. Hooldustasu kaup lingitakse 36 kuu viitvõlagraafikuga.
5. Looge arveldusgraafik, mis sisaldab kahte arveldamata üksust. Lepingu arveldusgraafik on seadistatud järgmiste üksustega.

    | Kaup | Alguskuupäev | Lõpukuupäev | Summa | Arveldamissagedus | Viitvõla kaup | Arveldamata tulu | Kirjeldus |
    |---|---|---|---|---|---|---|---|
    | Litsents | 01. jaanuar, APRIL | 31. detsember: KIRI+2 | $100.00 | Kord aastas | Nr | Jah | Kliendile arveldatakse arve $100.00 aastal. Kogusumma $300.00 bilanssi kirjendatakse eelnevalt tasakaalustamata tuluna ning tuluna tuluna kasumist ja kahjumist. Iga arve vähendab arveldamata summat. |
    | Hooldus | 01. jaanuar, APRIL | 31. detsember: KIRI+2 | $30.00 | Kord aastas | Jah | Jah | Kliendile arveldatakse arve $30.00 aastal. Kogusumma $90.00 eelnevalt kirjendatakse tasakaalustamata tuluna ja viittuluna bilansis. Iga arve vähendab arveldamata summat. Edasilükatud tulu tuvastatakse kord kuus üle 36 kuu. |

6. Kasutage lehel **Kõik arveldusgraafikud** töölehe **sisestamise** protsessi, et sisestada lepingu väärtus bilansilehele arveldamata tuluna.

Luuakse kaks töölehe kirjet, üks arvegraafiku iga rea kohta.

| Arveldamata tulu konto | Arveldamata tulude vastaskonto | Deebetsumma | Kreeditsumma |
|---|---|---|---|
| Arveldamata tulu konto | | $300.00 | |
| | Arveldamata tulude vastaskonto | | $300.00 |

| Arveldamata tulu konto | Edasilükatud tulu | Deebetsumma | Kreeditsumma |
|---|---|---|---|
| Arveldamata tulu konto | | $90.00 | |
| |Edasilükatud hooldustulu | | $90.00 |

Esimene töölehe kirje sisestatakse tasakaalustamata tulu vastaskontole ja teine sisestatakse viittulu kontole. Kui arveldusreal on nii arveldamata tulu kui ka viittulu, kasutatakse viittulu kontot, mitte arveldamata tulu vastaskontot. Leping nõuab, et kliendi arve loodaks iga aasta alguses. **Arve loomiseks** kasutage arve loomise protsessi. Arve loomisel luuakse järgmised töölehekanded.

| Põhikonto | Arveldamata tulu konto | Deebetsumma | Kreeditsumma |
|---|---|---|---|
| Tasakaalustamata tulu vastaskonto | | $100.00 | |
| | Arveldamata tulu konto | | $100.00 |
| Müügireskontro | | $100.00 | |
| | Tulukonto | | $100.00 |

| Põhikonto | Arveldamata tulu konto | Deebetsumma | Kreeditsumma |
|---|---|---|---|
| Edasilükatud hoolduse tulu konto | | $30.00 | |
| | Arveldamata tulu konto | | $30.00 |
| Müügireskontro | | $30.00 | |
| | Edasilükatud hoolduse tulu konto | | $30.00 |

Sama töölehekanne luuakse arvetega, mis sisestatakse järgmise kahe aasta alguses. Edasilükatud tulu konto netosumma on 0 (null), kuna ümardamise ega vahetuskursi erinevused puuduvad. Edasilükatud tulu peab olema tühistatud täpselt nii, nagu see kredit oli töölehe sisestuse **loomise protsessis**. Kuna tulu on endiselt edasi lükatud ja hiljem tuvastatakse, toimub edasilükatud tulu konto kreedit uuesti.

Viimases sammus luuakse tunnustuse töölehe sisestus igal kuul, et tuvastada edasilükatud hooldustasu tulu. Töölehe sisestuse saab luua, kasutades tunnustuse **töötlemise** lehte. Selle saab luua ka valides viitvõlagraafiku **lehekülgedel** ridade jaoks **väärtuse** Ära.

| Edasi lükatud tulude konto | Tulukonto | Deebetsumma | Kreeditsumma |
|---|---|---|---|
| Edasilükatud hooldustulu | | $2.50 | |
| | Hooldustulu | | $2.50 |

See töölehekirje luuakse iga kord, kui tuvastamisprotsessi selle edasilükatud kauba puhul käitatakse (kokku 36 korda).

#### <a name="short-term-fixed-year"></a>Lühiajaline: fikseeritud aasta

Arveldamata tulu saate **kasutada** **koos** lühiajalise funktsiooniga, seadistades korduva lepingu arveldusparameetrite lehel välja Lühiajaline arveldamata. Järgmine näide näitab kalkulatsioone, mis tehakse, kui vaba tulu kasutatakse koos fikseeritud **aasta** lühiajalise stamata meetodiga.

Luuakse arveldusgraafik, kus on järgmised kriteeriumid:

- **Alguskuupäev:** 1. juuni 2020
- **Lõppkuupäev:** 31. detsember 2021
- **Ühiku hind:** $100
- **Sagedus: kord** kuus

**Lehel Kõik arveldusgraafikud** loob algse töölehe sisestuse töölehe **sisestuse protsessiga**. Praegused lühiajalised ja pikaajalised summad arvutatakse järgmiselt:

- **Praegune lühiajaline tulusumma:** $700
- **Praegune pikaajaline tasumata tulusumma:** $1,200

Arve luuakse arveldusperioodiks 1. juunil 2020 kuni 30. novembrini 2020. Praegused lühiajalised ja pikaajalised summad arvutatakse järgmiselt:

- **Praegune lühiajaline tulusumma:** $100
- **Praegune pikaajaline tasumata tulusumma:** $1,200

Arve luuakse arveldusperioodiks 1. detsembrist 2020 kuni 31. detsembrini 2020. Praegused lühiajalised ja pikaajalised summad arvutatakse järgmiselt:

- **Praegune lühiajaline tulusumma:** $1,200
- **Praegune pikaajaline tasumata tulusumma:** $0

#### <a name="short-term-rolling-periods"></a>Lühiajaline: perioodide jooksvaks mine

Arveldamata tulu saate kasutada **koos lühiajalise funktsiooniga, seadistades lühiajalise arveldamata meetodi korduva lepingu arveldusparameetrite** lehel. Järgmine näide näitab kalkulatsioone, **mis** on tehtud, kui vaba tulu kasutatakse koos jooksvate perioodide lühiajalise stamata meetodiga.

Luuakse arveldusgraafik, kus on järgmised kriteeriumid:

- **Alguskuupäev:** 1. juuni 2020
- **Lõppkuupäev:** 31. detsember 2021
- **Ühiku hind:** $100
- **Sagedus: kord** kuus

**Lehel Kõik arveldusgraafikud** loob algse töölehe sisestuse töölehe **sisestuse protsessiga**. Praegused lühiajalised ja pikaajalised summad arvutatakse järgmiselt:

- **Praegune lühiajaline tulusumma:** $1,200
- **Praegune pikaajaline tasumata tulusumma:** $700

Arve luuakse arveldusperioodiks 1. juunil 2020 kuni 30. novembrini 2020. Praegused lühiajalised ja pikaajalised summad arvutatakse järgmiselt:

- **Praegune lühiajaline tulusumma:** $1,200
- **Praegune pikaajaline tasumata tulusumma:** $100

Arve luuakse arveldusperioodiks 1. detsembrist 2020 kuni 31. detsembrini 2020. Praegused lühiajalised ja pikaajalised summad arvutatakse järgmiselt:

- **Praegune lühiajaline tulusumma:** $1,200
- **Praegune pikaajaline tasumata tulusumma:** $0

### <a name="items-with-revenue-allocation"></a>Tulueraldusega kaubad

Arveldusgraafikusse lisatakse kaks üksust, erineva arveldussagedusega. Mõlemad kasutavad segmentimata tulu ja on viittulud.

- **Kaubakood 1000:** Surface Pro 128GB

    - **Arveldussagedus:** üks kord
    - **Ühiku hind:** $1,500
    - **Eraldiseisev müügihind:** $1,600
    - **Lepingu tulu:** $1,465.26

- **Kaubakood S0021:** kindlustus, mida müüakse koos kaubakoodiga 1000

    - **Arveldussagedus:** kord kuus 12 kuu jooksul
    - **Ühiku hind:** $20 kuu kohta
    - **Eraldiseisev müügihind:** $25
    - **Lepingu tulu:** $264.74

Kuna mõlemad kaubad kasutavad tasumata tulu ja tulu eraldamist, on uuendamisreal lepingu kogusumma 0 (null). Lisatakse **veerg Lepingu** tulu ja kuvatakse lepingu tulu summa.

Järgmises tabelis on näidatud kaupade ja arve algne töölehesisestus.

| Arveldamata tulu konto | Edasi lükatud tulude konto | Deebetsumma | Kreeditsumma |
|---|---|---|---|
| **Kauba 1000 töölehe sisestus** | | | |
| Tasumata tulu deebetkonto (401250) | | $1,465.26 | |
| | Viittulu kreeditkonto (250600) | | $1,465.26 |
| **Kaup 0021 Töölehe kirje** | | | |
| Tasumata tulu deebetkonto (401250) | | $274.74 | |
| | Viittulu kreeditkonto (250600) | | $274.74 |
| **Arve** | | | |
| | Saate krediteeritud tulu konto | | $1,465.26 |
| | Saate krediteeritud tulu konto | | $274.74 |
| Deebet-AR-konto (130100) | | $1,488.16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Arveldusgraafiku rea, arvelduse üksikasjarea või tulu eralduse muudatused

Kui ühiku hinda või kogust muudetakse, tuleb uuendada iga kauba, mis on tulueralduse osa, lepingu tulusummat. Seetõttu arvutatakse töölehe kanne ümber.

Näiteks kauba 1000 ühiku hind muudetakse ühikuhinnast $1,500 ühiku $1,600. Sellisel juhul arvutatakse lepingu tulusumma automaatselt ümber $1,549.47. Kauba S0021 lepingutulu arvutatakse ümber tuluna $290.53.

Kui muudetud on kinnitatud ja kooskõlastatud, tühistatakse mõlema kauba algne töölehe sisestus ja luuakse uued töölehe sisestused:

- **Kaup 1000:** algse algse töölehe $1,465.26 on tühistatud. Töölehele luuakse $1,549.47 kirje.
- **Kaup S0021:** algse algse $274.74 sisestamine on tühistatud Kande jaoks luuakse $290.53 töölehe kirje.

#### <a name="termination"></a>Lõpetamine

Kaubal S0021 on alguskuupäev 2020. aasta jaanuaris ja lõppkuupäev detsembris 2020, kuid lõpetatakse juunis 2020. Mõlema kauba lepingu tulu summa tuleb ümber arvutada:

- **Kaup 1000:** lepingu tulu arvutatakse ümber $1,567.67.
- **Kaup S0021:** lepingu tulu arvutatakse ümber $124.00.

Lõpetamisega reale luuakse korrigeerimist vajav töölehe kirje. Töölehe kanne reale, mis kuulub samasse mitme elemendi kokkuleppe (MEA) numbrisse, tühistatakse ja luuakse uus töölehe kanne:

- **Kaup 1000:** algse algse töölehe $1,465.26 on tühistatud. Korrigeerimist töölehe kirje $1,549.47 jaoks luuakse.
- **Kaup S0021:** algse algse $274.74 sisestamine on tühistatud Kande jaoks luuakse $124.00 töölehe kirje.
