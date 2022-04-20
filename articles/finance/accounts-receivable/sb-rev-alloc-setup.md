---
title: Mitme elemendiga tulu eraldamise seadistamine
description: See teema kirjeldab, kuidas seadistada parameetreid mitme elemendi tulu eraldamiseks kordustellimuse arvelduses.
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
ms.openlocfilehash: e422b16d1c4505b2837bb282918ecada902b806e
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2022
ms.locfileid: "8566563"
---
# <a name="set-up-multiple-element-revenue-allocation"></a>Mitme elemendiga tulu eraldamise seadistamine

Mitme elemendi tulu eraldamine võimaldab teil seadistada erinevaid malle, mida kasutatakse tulu arvutamiseks ja eraldamiseks mitme kauba vahel. See funktsioon aitab teil järgida raamatupidamisstandardite kodeerimise teemat 606 (ASC 606) ja/või rahvusvahelise finantsaruandluse standardiga 15 (IFRS 15).

## <a name="multiple-element-revenue-allocation-parameters"></a>Mitme elemendiga tulu eraldamise parameetrid

Kasutage mitme **elemendi tulu eralduse** parameetrite lehte, et seadistada mitme elemendi tulu eralduse parameetrid.

### <a name="standalone-selling-price-origin"></a>Eraldiseisva müügihinna lähtekoht

Eraldiseisev **müügihinna päritolu väli** määrab, kust eraldiseisev müügihind pärineb. Väärtust saate uuendada kauba **eraldi müügihinna lehel** ja kandel. Saadaval on järgmised suvandid.

| Suvand | Kirjeldus |
|--------|-------------|
| Summa | Eraldiseisev müügihind on summa, mille määrate rohkem kui 0 (null). Summa teisendatakse vastavalt vajadusele funktsionaalsete ja algsete valuutade vahel. |
| Baasmüügihind | Eraldiseisev müügihind vastab kauba baasmüügihinnale. |
| Arve hind | Eraldiseisev müügihind vastab kauba arvehinnale. |
| Kauba protsent | Eraldiseisev müügihind määratakse protsendi väärtusena ja see arvutatakse kauba hinna alusel. Selle suvandi valimisel määrake vaikeprotsent. |
| Jääksumma eraldamine | <p>Eraldioleva müügihinna päritolu arvutatakse *emakauba kogu lepinguväärtusena* – *tütarüksuste eraldiseisev müügihind kokku*:</p><ul><li>*Emakauba kogu lepinguväärtus* on neto- või arveldatud summa.</li><li>*Tütarüksuste eraldiseisev* müügihind kokku on kõigi tütarüksuste laiendatud või lepingu eraldi müügihinna summa, v.a tütarkaup, mis kasutab seda eraldiolevat müügihinna päritolu.</li></ul><p>Kui arvutatud summa on negatiivne väärtus, seatakse summaks 0 (null).</p><p>**Märkus:** seda valikut saab tulu tükeldades valida ainult ühe tütarkauba puhul.</p> |
| Pole | Eraldi müügihinna päritolu põhineb tütarüksustel. See valik kehtib kaupadele, mis on määratletud tulu tükeldamismallis emaüksustena. Kui on **märgitud ruut** Tulu tükeldamine, valitakse see suvand automaatselt ning sätet ei saa muuta. |
| Ülemarve hinna protsent | Eraldiseisev müügihinna päritolu on protsent emakauba arvehinnast. Vaikeväärtust saate muuta. See valik on saadaval ainult tulu tükeldamismallis tütarüksuste puhul. |
| Ülemise standardhinna protsent | Eraldiseisev müügihinna päritolu on protsent emakauba standardhinnast. Vaikeväärtust saate muuta. See valik on saadaval ainult tulu tükeldamismallis tütarüksuste puhul. See on tütarüksuste vaikevalik. Kui **tütarkauba** **·** **·** **valik** muudetakse emastandardi hinna protsendist emaarvehinna protsendiks või emaarve hinna protsendiks emastandardi hinna protsendiks, uuendatakse ka arvutatud väärtused. |

### <a name="account-for-revenue-allocation-rounding-differences"></a>Tulu eraldamise ümardamise erinevuste konto

Tulueralduse **ümardamiserinevuste** konto väljal määratakse konto, mida kasutatakse lepingu tulusumma ümardamise korrektsioonide kirjendamiseks. See on saadaval korduva lepingu arvelduse kasutamisel.

## <a name="item-standalone-selling-price"></a>Kauba eraldiseisev müügihind

Kasutage kauba **eraldiseisev müügihinna lehte** kauba päritolu ja eraldiseisev müügihinna määramiseks. Sellel lehel määratud väärtusi kasutatakse vaikeväärtustena **tulu** eraldamise lehel mitme elemendi tulu eraldamises ja korduvas lepingu arvelduses.

### <a name="specify-item-standalone-selling-price"></a>Määrake kauba eraldiseisev müügihind

Kauba eraldi hinna määramiseks järgige neid samme.

1. **Eraldiseisev müügihinna** **lehe väljal Eraldiseisev** müügihinna päritolu valige eraldiseisev müügihinna päritolu.
2. Järgige ühte järgmistest sammudest, sõltuvalt väärtusest, mille valisite **väljal Eraldiseisev müügihinna** päritolu:

    * Kui valisite **kauba protsendi**, määrake protsent väljal **Protsent**.
    * Kui valisite **summa**, määrake summa **eraldiseisev müügihinna väljal**.

2. Iga loendisse lisatata kauba puhul valige lisa **.**
3. **Valige kaubakood** väljal Kaubakood. **Väljal Kauba seos** valige kauba seos. Kaupade puhul, mille **märkeruudu** Tulu tükeldamine tühjendatakse, peab kaubakoodi ja kaubaseose valitud kombinatsioon olema kordumatu.
4. Muutke vastavalt vajadusele eraldi müügihinna, eraldiseisev **·** **müügihinna või protsendivälja vaikeväärtust.** **·**
5. Iga emaüksuse puhul, mille soovite loendisse lisada, valige **lisa**.
6. **Valige kaubakood** väljal Kaubakood. **Väljal Kauba seos** valige kauba seos.
7. Märkige ruut **Tulu tükeldamine**.
8. **Väljal Kauba seos** valige kauba seos. Loendit uuendatakse emaüksuse ja kõigi tütarüksustega.
9. Alamkauba puhul **muutke eraldi müügihinna päritolu vaikeväärtust,** **emastandardi hinna protsent,** **·** **emaarve hinna protsent või eraldage kogusumma väli vastavalt vajadusele.**
10. Mitme kauba korraga lisamiseks valige suvand **Lisa kaupu**.
11. Saate päringut uuendada, et valida lisatavate üksuste vahemik.
12. Valige **OK**, vaadake üle lisatud kaupade loend ja valige **OK**.

### <a name="fields"></a>Väljad

Kauba **eraldiseisev müügihinna lehekülg** sisaldab järgmisi välju.

| Väli | Kirjeldus |
|-------|-------------|
| Eraldiseisva müügihinna lähtekoht | <p>Valige eraldi müügihinna päritolu:</p><ul><li>**Summa** – eraldiseisev müügihind on summa, mille määrate rohkem kui 0 (null). Summa teisendatakse vastavalt vajadusele funktsionaalsete ja algsete valuutade vahel.</li><li>**Baasmüügihind** – eraldiseisev müügihind vastab kauba baasmüügihinnale.</li><li>**Arve hind** – eraldiseisev müügihind vastab kauba arvehinnale.</li><li>**Kauba** protsent – eraldiseisev müügihind määratakse protsendi väärtusena ja arvutatakse kauba hinna alusel. Selle suvandi valimisel määrake vaikeprotsent.</li></ul>**Eraldage järelejääv** summa *– eraldi müügihinna päritolu arvutatakse emakauba kogu lepinguväärtusena* – *tütarüksuste eraldiseisev müügihind kokku*:</p><ul><li>*Emakauba kogu lepinguväärtus* on neto- või arveldatud summa.</li><li>*Tütarüksuste eraldiseisev* müügihind kokku on kõigi tütarüksuste laiendatud või lepingu eraldi müügihinna summa, v.a tütarkaup, mis kasutab seda eraldiolevat müügihinna päritolu.</li></ul><p>Kui arvutatud summa on negatiivne väärtus, seatakse summaks 0 (null).</p><p>**Märkus:** seda valikut saab tulu tükeldades valida ainult ühe tütarkauba puhul.</p></li><li>**Pole** – eraldi müügihinna päritolu põhineb tütarüksustel. See valik kehtib kaupadele, mis on määratletud tulu tükeldamismallis emaüksustena. Kui on **märgitud ruut** Tulu tükeldamine, valitakse see suvand automaatselt ning sätet ei saa muuta.</li><li>**Emaarve hinna** protsent – eraldi müügihinna päritolu on emakauba arvehinna protsent. Vaikeväärtust saate muuta. See valik on saadaval ainult tulu tükeldamismallis tütarüksuste puhul.</li><li>**Emastandardi** protsent – eraldi müügihinna päritoluks on emakauba standardhinna protsent. Vaikeväärtust saate muuta. See valik on saadaval ainult tulu tükeldamismallis tütarüksuste puhul. See on tütarüksuste vaikevalik. Kui **tütarkauba** **·** **·** **valik** muudetakse emastandardi hinna protsendist emaarvehinna protsendiks või emaarve hinna protsendiks emastandardi hinna protsendiks, uuendatakse ka arvutatud väärtused.</li></ul> |
| Eraldiseisev müügihind | Määrake kauba eraldiseisev müügihind. See väli on saadaval, kui **eraldi müügihinna päritolu väljal** on seatud väärtus **Summa**. |
| Protsent | Määrake eraldiseisev müügihinna protsent. See väli on saadaval, **kui eraldi müügihinna** **päritolu** välja väärtuseks on seatud Kauba protsent, **Emaarve** hinna protsent või **emastandardi hinna protsent.** |
| Tulujaotus | <p>Määrake, kas rida kasutab tulude tükeldamist:</p><ul><li>**Valitud** : väljal Kaubaseose saab valida ainult neid kaupu, mille jaoks on seadistatud tulude **tükeldamise** mall. Selle ruudu saate valida ainult tulu tükeldamise malli emaüksuste puhul.</li><li>**Tühjendatud** : kaup on standardkaup, mis ei kasuta tulu tükeldamist.</li></ul> |
| Seos | Sümbol näitab, kas kaup on tulu tükeldamises ema- või tütarüksus. |
| Üksuse kood | <p>Valige kaubakood: tabel **või** **grupp**.</p><p>Kui on **märgitud ruut** Tulu tükeldamine, on selle välja väärtuseks **seatud Tabel** ja väärtust ei saa muuta.</p> |
| Kauba seos | <p>Saate valida kaubakoodi.</p><p>Kui on **valitud märkeruut** Tulu tükeldamine, on valida ainult need kaubad, mis on emaüksused, mille jaoks on seadistatud tulu tükeldamise mall. Emakauba valimisel uuendatakse loendit automaatselt selle emakauba tütarüksustega.</p> |
| Ülemkaup | Emakauba puhul kuvatakse sellel väljal kaubakood. Tulu tükeldatud tütarüksuste puhul kuvatakse sellel põhikauba kaubakood. |

## <a name="mea-templates"></a>MEA mallid

**Kasutage MEA mallide lehte** mitme elemendi loomiseks ja redigeerimiseks (MEA) malli ID-sid. Neid ID-sid kasutatakse tulude **eraldamise lehel** kaupade grupeerimiseks.

### <a name="create-a-template"></a>Malli loomine

MEA malli häälestamiseks järgige neid samme.

1. **VALIGE MEA mallide** lehel suvand **Uus**.
1. Sisestage **MEA malli ID väljale** kordumatu ID.
1. Väljale **Kirjeldus** sisestage kirjeldus.
1. Väljal Viitlepingu **tulukonto** valige konto, mida soovite kasutada töölehe sisestuste jaoks MEA lepingu arve loomisel. See väli on saadaval, kui korduv lepingu arveldus on lubatud ja kasutusel.
1. Valige käsk **Salvesta**.
