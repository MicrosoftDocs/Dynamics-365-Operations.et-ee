---
title: Materjalikulu arvutamine
description: See artikkel annab teavet mitmesuguste valikute kohta, mis on seotud materjalikulu arvutamisega.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: acccc677c855fc675d52814d7f6f0a5141bbc8af
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001661"
---
# <a name="calculate-material-consumption"></a>Materjalikulu arvutamine

[!include [banner](../includes/banner.md)]

See artikkel annab teavet mitmesuguste valikute kohta, mis on seotud materjalikulu arvutamisega. 

Lehe **Kooslus** kiirkaardil **Rea üksikasjad** vahekaartidel **Seadistus** ja **Etapiviisiline tarbimine** on saadaval järgmised materjalitarbimise arvutamisega seotud suvandid.

## <a name="variable-and-constant-consumption"></a>Muutuv ja konstantne tarbimine
Väljal **Tarbimine on** saate valida, kas tarbimine tuleks arvutada konstantse koguse või muutuva kogusena. Valige suvand **Konstantne**, kui tootmiseks on nõutav fikseeritud kogus või maht, olenemata toodetavast kogusest. Valige suvand **Muutuv**, mis on vaikesäte, kui materjali nõutav kogus valmiskaupades on toodetavate valmiskaupade arvuga proportsionaalne.

## <a name="calculating-consumption-from-a-formula"></a>Tarbimise arvutamine valemi põhjal
Väljal **Valem** saate seadistada erinevaid valemeid materjalitarbimise arvutamiseks. Kui kasutate vaikeväärtust, **Standardne**, ei arvutata tarbimist valemi põhjal. Väljadega **Kõrgus**, **Laius**, **Sügavus**, **Tihedus** ja **Konstant** toimivad järgmised valemid.

-   Kõrgus \* Konstant
-   Kõrgus \* Laius \* Konstant
-   Kõrgus \* Laius \* Sügavus \* Konstant
-   (Kõrgus \* Laius \* Sügavus / Tihedus) \* Konstant

## <a name="rounding-up-and-multiples"></a>Ümardamine ja kordsed
Väljad **Ümardamine** ja **Kordsed** võimaldavad ümardada materjalitarbimise väärtust. Näiteks saate ümardada väärtuse materjali käsitlemisühiku järgi, milles toormaterjali tootmisse komplekteeritakse. Väljal **Ümardamine** on saadaval järgmised valikud: **Kogus**, **Mõõt** ja **Tarbimine**.

### <a name="quantity"></a>Kogus

Kui valite ümardamismehhanismiks suvandi **Kogus**, peab kogus olema määratud koguse kordne. Näiteks, kui nõutavad on täisarvud, valige väljal **Kordsed** väärtus **1**. Arvud ümardatakse seejärel koguseni, mis jaguvad on 1.

### <a name="measurement"></a>Mõõtmine

Tavaliselt valite ümardamismehhanismiks suvandi **Mõõt**, kui toormaterjalil on kindlad mõõtmed. Näiteks on valmistoote jaoks nõutav 2-meetrine metalltoru ja metalltorusid hoiundatakse 4,5-meetri pikkustena. Sellisel juhul saab ümardusmehhanismiga **Mõõt** arvutada, kui palju metalltorusid on vaja kindla arvu valmistoodete tootmiseks. Selles näites on välja **Valem** väärtuseks seatud **Kõrgus \* Konstant**. Välja **Kõrgus** väärtuseks on seatud **2**, mis näitab valmiskauba jaoks vajaliku toru pikkust. Välja **Kordne** väärtuseks on seatud **4,5**, mis näitab, et toru komplekteeritakse pikkustes 4,5 meetrit. Arvutuskäik on järgmine.

1.  10 ühiku valmiskauba jaoks vajalike kordühikute arv: 10 ÷ 2 = 5 tk
2.  Kogutarbimine: 4.5 × 5 = 22,5 meetrit metalltoru

Eeldatakse, et 0,5-meetrine toruosa kantakse iga viie tarrbitud toru kohta maha.

### <a name="consumption"></a>Tarbimine

Tavaliselt valite ümardamismehhanismi suvandiks **Tarbimine**, kui toormaterjali komplekteeritakse toote kindla materjali käsitlemisühiku täielikes kogustes. Näiteks kasutatakse ühe valmistoote tootmiseks 2 liitrit värvi ja värvi komplekteeritakse 25-liitristes tünnides. Selles näites saab ümardamismehhanismiga **Tarbimine** ümardada tarbimise täisarvu, 25-liitristes tünnideni. Värvi, mis on vajalik, kui 180 lõpetatud kauba ühikut, tuleb esitada arvutusmeetodid järgnevalt:

1.  Vajalik värv, v.a praak: 180 × 2 = 360 liitrit
2.  Tünnide arv: 360 ÷ 25 = 14,4, ümardatuna 15
3.  Vajalik värv, k.a praak: 15 × 25 = 375 liitrit

## <a name="step-consumption"></a>Sammu tarbimine
Etapiviisilist tarbimist kasutatakse koguseintervalliga konstantse tarbimise arvutamiseks. Kui teete vahekaardi **Seadistus** väljal **Valem** valiku **Etapiviisiline tarbimine**, saate lisada teavet etappide kohta vahekaardile **Etapiviisiline tarbimine**. Fikseeritud tarbitud koguse saab seadistada toodetud koguse intervalliga. Näiteks seadistatakse etapiviisiline tarbimine nii, nagu kirjeldatud allolevas tabelis.

| Seeriatest | Kogus |
|-------------|----------|
| 0,00        | 10,0000  |
| 100,00      | 20.0000  |
| 200,00      | 40.0000  |

Koosluse kogus on 1 ja tootmiskogus 110. Tarbimise valem on Lähteseeria (kogus) = tarbimine. Kuna tootmiskogus on 110, jääb see vahemikku „Alates 100 seeriast”. Seega on kogus 20.



