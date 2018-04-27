---
title: Paindgrupid
description: "Selles teemas kirjeldatakse, kuidas tööajaarvestuses kasutatakse paindgruppe."
author: johanhoffmann
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgFlexGroup
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: e21a2de2f46c619f27eddad4d7cced260a90bbb8
ms.openlocfilehash: 20f317ff57fac25b5b5b0d702fe64845eb849e87
ms.contentlocale: et-ee
ms.lasthandoff: 04/09/2018

---

# <a name="flex-groups"></a>Paindgrupid

[!include[banner](../includes/banner.md)]

Paindlik tööaeg võimaldab ettevõtetel vähendada makseid ületunnitöö eest, pakkudes töötajatele täiendavat vaba aega perioodidel, mil töökoormus on väike. See funktsioon on oluline näiteks segmentides, milles toimuvad hooajalised muudatused töökoormuses.

Paindgruppide abil saate töötaja paindtundidele määrata järgmisi reegleid ja põhimõtteid.

- Paindeeskirjade reeglid
- Töötaja paindsaldo arvutamise põhimõte

## <a name="set-up-flexible-working-hours-in-flex-groups"></a>Paindliku tööaja seadistamine paindgruppides

- Valige **Tööajaarvestus** \> **Seadistus** \> **Grupid** \> **Paindgrupid**, et seadistada paindgruppe paindtundide jaoks.

## <a name="associate-workers-with-flex-groups"></a>Töötajate seostamine paindgruppidega

- Valige **Tööajaarvestus** \> **Seadistus** \> **Ajalise registreerimise töötajad**.

## <a name="rules-for-flex-regulations"></a>Paindeeskirjade reeglid

Saate kasutada paindeeskirjade reegleid, et määrata paindpiirid või minimaalse ja maksimaalse tundide arvu, mis on lubatud töötaja paindkontol. Paindpiirid seadistatakse paindgrupis. Paindpiiride ületamisel saab töötaja paindsaldot ja palka korrigeerida.

Kui töötaja lubatud paindmiinimumi ületatakse (st kui tundide arv paindkontol on allpool määratud miinimumi), saate kasutada neid meetodeid töötaja paindsaldo korrigeerimiseks, luues paindeeskirja.

- Töötaja paindkontot saab korrigeerida määratud lubatud miinimumini, kuid ilma töötaja palga mahaarvamiseta tundide eest, mil paindkonto on allpool lubatud miinimumi.
- Töötaja palga saab maha arvata tundide eest, mil paindkonto on allpool lubatud miinimumi. Selle mahaarvamise tegemiseks luuakse tasuüksused kindla tasutüübi kohta, millel on negatiivne või positiivne makseühik.

Kui töötaja lubatud paindmaksimumi ületatakse, saate kasutada neid meetodeid töötaja paindsaldo korrigeerimiseks, luues paindeeskirja.

- Töötaja paindkonto saab korrigeerida tagasi määratud lubatud maksimumini, kuid ilma töötaja palga kompenseerimiseta tundide eest, mil töötaja töötas üle lubatud maksimumi.
- Tundide arvu, mil töötaja töötas üle lubatud maksimumi, saab teisendada makseks. Selle teisendamise jaoks luuakse tasuüksused kindla tasutüübi kohta.

Saate korrigeerida paindsaldot järgmistel aegadel.

- Kui palgaandmetel põhinevat maksefaili eksporditakse töö **Tasu ülekandmine** abil. Palgaandmed luuakse töötaja registreeringu ülekandmisel lehelt **Kinnita**.
- Töö **Paindsaldo korrigeerimine** teostamisel.

> [!NOTE]
> Paindeeskirjad ei ilmne igapäevase kinnitamise ajal ja töötaja registreeringute ülekandmisel lehel **Kinnita**.

## <a name="principle-for-calculating-a-workers-flex-balance"></a>Töötaja paindsaldo arvutamise põhimõte

Põhimõte nende tundide arvutamiseks, mille järgi töötaja paindsaldot korrigeeritakse, seadistatakse paindgrupis. Valige **Tööajaarvestus** \> **Seadistus** \> **Grupid** \> **Paindgrupid**. 

Kasutada saab kaht järgmist põhimõtet.

- **Aeg** – töötaja paindtunnid arvutatakse ainult töötaja registreeritud kellaajast. Töötaja igapäevaste registreerimiste arvutamisel arvutatakse Paind+ ja Paind- töötunnid töötaja ajaprofiilis määratletud Paind+ ja Paind- tsoonidest.
- **Tasutüübid** – töötaja paindtunnid arvutatakse töötaja tasuleppes määratletud Paind+ ja Paind- tasutüüpide tulu põhjal. Tasulepe on seotud töötajale kellaaja registreerimisega. Võite soovida kasutada tasutüüpe paindkontode haldamiseks näiteks siis, kui soovite suurendada töötaja paindkontot kindla teguri võrra ühes või mitmes paindtsoonis.

### <a name="scenario-1-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-minimum-is-exceeded"></a>1. stsenaarium: töötaja tasu ja paindkonto korrigeerimine, sest lubatud paindmiinimumi on ületatud

Töötajal, kellel on paindlik tööaeg, on negatiivne paindkonto.

- **Paindkonto:** -4

Töötaja on seotud paindgrupiga, millel on järgmine konfiguratsioon:

- **Paindmiinimum:** -0,5
- **Miinimumtasu tüüp:** 1302
- **Tasutüübi tegur:** -1,00

Nagu erinevus töötaja paindkonto ja tema lubatud paindmiinimumi vahel näitab, on töötaja ületanud tema lubatud paindmiinimumi 3,5 tunni võrra.

Kui palgaarvestuse administraator kannab töötaja palgaandmed üle, käivitades töö **Tasumiseks ülekandmine** või **Paindkorrigeerimine**, tehakse järgmised korrigeerimised.

- Töötaja paindkontot korrigeeritakse 3,5 tunni võrra. Seetõttu korrigeeritakse paindsaldot -4,0 tundi töötaja lubatud paindmiinimumi -0,5 tundi järgi.
- Luuakse tasuüksus tasutüübi 1302 jaoks. Sellel tasuüksusel on tasuühik -3,5 tundi, mis arvatakse töötaja tasust maha. Sel juhul on tasuühik negatiivne arv, sest positiivne korrigeerimine 3,5 tundi korrutatakse negatiivse tasutüübi teguriga -1,0, mis on määratletud paindgrupis. See tasuüksus saab osaks maksefailist, mis luuakse tööga **Tasumiseks ülekandmine**.

### <a name="scenario-2-adjusting-a-workers-pay-and-flex-account-because-the-allowed-flex-maximum-is-exceeded"></a>2. stsenaarium: töötaja tasu ja paindkonto korrigeerimine, sest lubatud paindmaksimumi on ületatud

Töötajal, kellel on paindlik tööaeg, on positiivne paindkonto.

- **Paindkonto:** 6

Töötaja on seotud paindgrupiga, millel on järgmine konfiguratsioon:

- **Paindmaksimum:** 2.0
- **Miinimumtasu tüüp:** 1302
- **Tasutüübi tegur:** -1.0

Nagu erinevus töötaja paindkonto ja tema lubatud paindmaksimumi vahel näitab, on töötaja ületanud tema lubatud paindmaksimumi 4,0 tunni võrra.

Kui palgaarvestuse administraator kannab töötaja palgaandmed üle, käivitades töö **Tasumiseks ülekandmine** või **Paindkorrigeerimine**, tehakse järgmised korrigeerimised.

- Töötaja paindkontot korrigeeritakse -4,0 tunni võrra. Seetõttu korrigeeritakse paindsaldot 6,0 tundi töötaja lubatud paindmaksimumi 2,0 tundi järgi.
- Luuakse tasuüksus tasutüübi 1302 jaoks. Sellel tasuüksusel on tasuühik 4,0 tundi, mis lisatakse töötaja tasule. Sel juhul on tasuühik positiivne arv, sest negatiivne korrigeerimine 4,0 tundi korrutatakse negatiivse tasutüübi teguriga -1,0, mis on määratletud paindgrupis. See tasuüksus saab osaks maksefailist, mis luuakse tööga **Tasumiseks ülekandmine**.

### <a name="scenario-3-managing-a-workers-flex-balance-based-on-pay-types"></a>3. stsenaarium: töötaja paindsaldo haldamine tasutüüpide põhjal

Nagu selgitasime varem, saab paindkontosid hallata kas aja põhjal, mis on registreeritud töötaja ajaprofiilis määratletud Paind+ ja Paind- tsoonides, või töötaja tasulepingutes määratletud tasutüüpide põhjal. Tasutüüpide kasutamisel korrigeeritakse töötaja paindkontot makseüksuste järgi, mis luuakse töötaja registreeringute ülekandmisel lehelt **Kinnita**. Võite soovida kasutada tasutüüpe paindkontode haldamiseks näiteks siis, kui soovite suurendada töötaja paindkontot kindla teguri võrra ühes või mitmes paindtsoonis.

See stsenaarium kasutab järgmist paindprofiili, mis kujutab tööpäeva.

| Profiili tüüp  | Käivita    | Lõpp      |
|---------------|----------|----------|
| Paind+         | 12:00 | 08:00 |
| Sisseregistreerimine      | 08:00 | 08:00 |
| Paind-         | 08:00 | 09:00 |
| Standardaeg | 09:00 | 11:30 |
| Tasustatud vaheaeg    | 11:30 | 12:00 |
| Paind-         | 12:00 | 04:00 |
| Väljaregistreerimine     | 04:00 | 04:00 |
| Paind+         | 04:00 | 12:00 |

Praegusel juhul soovite hallata töötaja paindsaldot tasutüüpide põhjal. Seetõttu peate määrama töötaja paindgrupis suvandi **Tasutüüpidel põhinev** väärtuseks **Jah**.

Paindliku tööajaga arvestamiseks peata määratlema ka uue tasutüübi. Selles stsenaariumis on tasutüübi nimi **FlexCnt**.

| Tasu tüüp | Kirjeldus  |
|----------|--------------|
| FlexCnt  | Paindloendur |

Järgmiseks järgige neid etappe, et seadistada tasutüüp ja lisada uue tüübi read tasuprofiilile.

1. Valige **Tööajaarvestus** \> **Seadistus** \> **Grupid** \> **Paindgrupid** ja seejärel valige **Uus**.
2. Väljadel **Paind+** ja **Paind-** määratlege uus tasutüüp **FlexCnt**.
3. Valige **Tööajaarvestus** \> **Seadistus** \> **Tasulepped** ja seejärel valige **Lepingu read**.
4. Valiku **Esmaspäev** jaoks profiilitüübis **Flex+** lisage kolm järgmist rida.

    | Tasu tüüp | Kirjeldus  | Alates kellast | Kuni kellani  | Miinimum | Maksimum | Tegur |
    |----------|--------------|-----------|----------|---------|---------|--------|
    | FlexCnt  | Paindloendur | 12:00  | 06:00 | 00,00   | 00,00   | 1,00   |
    | FlexCnt  | Paindloendur | 06:00  | 12:00 | 00,00   | 02,00   | 1.50   |
    | FlexCnt  | Paindloendur | 06:00  | 12:00 | 02,00   | 06,00   | 2.00   |

    > [!NOTE]
    > Iga rida kasutatakse erineva ajaintervalli jaoks ja nendel on erinev tegur. Paindlik tööaeg, mille jooksul töötaja töötab ajaintervalli vältel, korrutatakse selle rea teguriga. Näiteks korrutatakse tunnid, mille jooksul töötatakse vahemikus 18:00 kuni 20:00, korrutatakse 1,50-ga. Tegur on määratletud väljal **Tegur** vahekaardil **Üldine** lehel **Tasuleppe read**.

Töötaja sisestab päeva jaoks järgmised registreerimised.

| Töölehe registreerimise tüüp | Käivita    | Lõpp      |
|---------------------------|----------|----------|
| Sisseregistreerimine                  | 07:00 | 07:00 |
| Tootmistöö            | 07:00 | 09:00 |
| Väljaregistreerimine                 | 09:00 | 09:00 |

Makstav summa arvutatakse lehel **Kinnita** töötaja registreeringu põhjal. Kui registreerimine on arvutatud, saate vaadata tulemus vahekaardil **Ajad**. Selles stsenaariumis olete huvitatud järgmistest väljadest.

| Paind+ | Paind– | Aeg  | Tasustatav aeg |
|--------|--------|-------|----------|
| 6,00   | 0,00   | 13,50 | 08,00    |

Paind+ tunde on kuus ja arvutus põhineb ajaprofiilis olevatel paindtsoonidel. See summa koosneb ühest Paind+ tunnist vahemikus 07:00 kuni 08:00 ja viiest Paind+ tunnist vahemikus 16:00 kuni 21:00.

Registreeringute ülekandmisel panete tähele, et Paind+ aeg muutub 6,0 tunnilt 8,0 tunniks.

| Paind+ | Paind– | Aeg  | Tasustatav aeg |
|--------|--------|-------|----------|
| 8.00   | 0,00   | 13,50 | 08,00    |

See muudatus leiab aset pärast ülekandmist, sest paindtunnid on arvutatud maksetüüpide, mitte aja põhjal. Järgnev tabel näitab, kuidas kaheksat tundi arvutatakse.

| Kust     | Sihtkoht:       | Aeg | Tegur    | Paindkonto |
|----------|----------|------|-----------|--------------|
| 07:00 | 08:00 | 1    | 1         | 1            |
| 04:00 | 06:00 | 2    | 1         | 2            |
| 06:00 | 08:00 | 2    | 1.5       | 3            |
| 08:00 | 09:00 | 1    | 2         | 2            |
|          |          |      | **Kogusumma** | **8**        |

