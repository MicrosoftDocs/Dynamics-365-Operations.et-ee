---
title: Koondplaneerimine ostulepingutega
description: Selles teemas kirjeldatakse, kuidas planeerimise optimeerimine võib leida ostulepingute seas leitud parima hinna ja täitmisaja alusel planeeritud tellimuse hankija ja/või täitmisaja.
author: ChristianRytt
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 4f50dfa5c2914ce2131cdc44582588be69b35335
ms.sourcegitcommit: 2eb7a9ae544f504155657c5c584cbac66c21dba4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/29/2021
ms.locfileid: "5961701"
---
# <a name="master-planning-with-purchase-trade-agreements"></a>Koondplaneerimine ostulepingutega

[!include [banner](../../includes/banner.md)]

Selles teemas kirjeldatakse, kuidas planeerimise optimeerimine võib leida kõigi konkreetse toote jaoks täpsustatud ostulepingute seas leitud parima hinna ja täitmisaja alusel planeeritud tellimuse hankija ja/või täitmisaja.

## <a name="turn-on-the-purchase-trade-agreements-for-planning-optimization-feature"></a>Planeerimise optimeerimise funktsiooni jaoks ostulepingute sisse lülitamine

Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama. Administraatorid saavad kasutada [funktsioonihalduse](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada. Seega on funktsioon loetletud järgmisel viisil.

- **Moodul:** *Koondplaneerimine*
- **Funktsiooni nimi:** *Ostulepingud planeerimise optimeerimiseks*

## <a name="prepare-your-system-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Süsteemi ettevalmistamine ostulepingute hindamiseks koondplaneerimise ajal

Toimige süsteemi konfigureerimiseks järgmiselt, et rakendada ostulepinguid hindav planeerimise optimeerimise funktsioon.

1. Avage **Koondplaneerimine \> Seadistus \> Koondplaneerimise parameetrid**. Seadke vahekaardil **Planeeritud tellimused** jaotises **Hankija** järgmised väärtused.

    - **Leia ostuleping** – seadke suvandi väärtuseks **Jah**, et hõlmata koondplaneerimisse ostulepingud.
    - **Otsingukriteerium** – valige tegur, mida soovite iga ostulepingu suhtes prioritiseerida: **Minimaalne täitmisaeg** või **Madalaim ühikuhind**.

1. Avage **Hanked \> Seadistus \> Hinnad ja allahindlused \> Hinna/allahindluse aktiveerimine** ja veenduge, et suvandi **Hankija** väärtuseks on seatud **Jah**.
1. Avage **Tooteteabe haldus \> Seadistus \> Dimensiooni- ja variandigrupid \> Laoala dimensioonigrupid** ja valige laoala dimensioonigrupp, mis rakendub toodetele, mille ostulepinguid peaks koondplaneerimine hindama. Veenduge, et grupi iga laoala dimensiooni puhul on veerus **Ostuhindadele** märgitud linnuke. Korrake seda sammu iga asjakohase laoala dimensioonigrupi jaoks.

## <a name="prepare-a-released-product-to-evaluate-purchase-trade-agreements-during-master-planning"></a>Väljastatud toote ettevalmistamine ostulepingute hindamiseks koondplaneerimise ajal

Pärast seda, kui teie süsteem on eelmises jaotises kirjeldatu kohaselt ette valmistatud, peaksite toimima järgmiselt, veendumaks, et iga toode, mida soovite antud funktsiooni raames kasutada, on korrektselt seadistatud.

1. Avage **Tooteteabe haldus \> Tooted \> Väljastatud tooted** ja avage sihttoode.
1. Veenduge kiirkaardil **Ost**, et väljas **Hankija** ei ole määratud ühtki hankijat.
1. Valige vahekaardi **Plaan** jaotises **Laovarude** grupp suvand **Kauba laovarud**, et avada valitud toote jaoks leht **Kauba laovarud**. Kontrollige järgmisi sätteid.

    - Te saate vahekaardil **Üldine** seadistada hankija alistamisi. Kui soovite, et planeerimise optimeerimine kasutaks ostulepinguid hankija valimiseks, peaksite ennetama hankija alistamised, eemaldades linnukese märkekastist **Kasutuskohane säte**.
    - Te saate vahekaardil **Täitmisaeg** seadistada täitmisaja alistamisi. Kui soovite, et planeerimise optimeerimine kasutaks ostulepinguid täitmisaegade valimiseks, siis peaksite ennetama täitmisaja alistamisi. Eemaldage märkekastist linnuke iga täitmisaja puhul, mille soovite valida ostulepingute abil ( **Ost**, **Tootmine** ja/või **Ülekanne**).

1. Valitud toote üksikasjade lehele naasmiseks sulgege leht **Kauba laovarud**.
1. Valige toimingupaanil vahekaardil **Plaan** grupis **Prognoos** suvand **Tarneprognoos**, et avada leht **Tarneprognoos**. Veenduge, et siin ei kuvata ühtki rida, mille kohta on seatud väärtus veerus **Hankija konto**.
1. Valitud toote üksikasjade lehele naasmiseks sulgege leht **Tarneprognoos**.
1. Seejärel valige toimingupaanil vahekaardi **Ost** grupis **Kaubanduslepingud** suvand **Kaubanduslepingute kuvamine**. Veenduge, et kõik asjakohased ostulepingud on loetletud. Samuti veenduge, et suvandi **Täitmisaja eiramine** väärtuseks on seatud **Ei** iga lepingu jaoks, mille puhul tahate, et planeerimise optimeerimisel kasutataks vastava lepingu jaoks sätestatud täimisaega.
1. Valige vahekaardi **Plaan** grupis **Tellimuse sätted** suvand **Tellimuse vaikesätted**, et avada valitud toote jaoks leht **Tellimuse vaikesätted**. Kuvage kiirkaardil **Ostutellimus** välja **Ostu täitmisaeg** väärtus. Kui ühtki kauba laovarude täitmisaja alistumist ei ole määratletud, siis kasutatakse planeerimise optimeerimisel antud väärtust, valides kaubanduslepingud, kus suvandi **Täitmisaja eiramine** väärtuseks on seatud **Jah**. Seega peaksite seda väärtust vastavalt vajadusele muutma.
1. Korrake seda toimingut iga asjakohase toote puhul.

> [!NOTE]
> Planeerimise optimeerimine toetab mitme valuutaga ostu-müügilepinguid. Kui otsite ostu-müügilepingut **Madalaima ühiku hinna** suvandi abil, arvestab süsteem arvestab erinevate valuutadega ostu-müügilepingute ridu tingimusel, et ostu-müügilepingu rea valuuta ja juriidilise isiku arvestusvaluuta vahel on kindlaks määratud vahetuskurss. Vastasel juhul eiratakse ostu-müügilepingu rida ja üldplaneerimisel kuvatakse tõrketeade. Seetõttu sisaldab üldplaneerimine teavet kõigilt asjakohastelt ostu-müügilepingutelt, kus saab hindu arvestusvaluutasse ümber arvutada.

## <a name="examples-of-how-planning-optimization-finds-vendor-and-lead-times"></a>Näited, kuidas planeerimise optimeerimisel tuvastatakse hankija ja täitmisajad

Järgmises tabelis on toodud näited, kuidas väljastatud toote ja sellega seotud ostulepingute mitmesugused sätted mõjutavad saadud plaanitud ostutellimuses leitavaid väärtusi. Kahe parempoolse veeru **paksud** väärtused on planeerimise optimeerimise käigus valitud väärtused. Muude veergude **_paksud ja kaldkirjas_** väärtused näitavad sätteid, mille tulemusel iga rea tulemused loodi.

| Väljastatud toode: hankija | Tellimuse vaikesätted: täitmisaeg | Kauba laovarud: alista hankija | Kauba laovarud: alista täitmisaeg | Kaubandusleping: hankija | Kaubandusleping: täitmisaeg | Kaubandusleping: täitmisaja eiramine | Saadud hankija | Saadud täitmisaeg |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| ***US001** _ | _*_1_*_ | Ei | Ei | US003 | 3 | Ei | _ *US001** | **1** |
| US001 | 1 | ***Jah: US002** _ | _*_Jah: 2_*_ | US003 | 3 | Ei | _ *US002** | **2** |
| *(tühi)* | 1 | Ei | Ei | ***US003** _ | _*_3_*_ | Ei | _ *US003** | **3** |
| *(tühi)* | ***1** _ | Ei | Ei | _*_US003_*_ | 3 | Jah | _ *US003** | **1** |
| *(tühi)* | ***1** _ | _*_Jah: US002_*_ | Ei | US003 | 3 | Ei | _ *US002** | **1** |
| *(tühi)* | ***1** _ | _*_Jah: US002_*_ | Ei | US003 | 3 | Ei | _ *US002** | **1** |
| *(tühi)* | 1 | Ei | Jah: 2 | ***US003** _ | _*_3_*_ | Ei | _ *US003** | **3** |
| *(tühi)* | 1 | Ei | ***Jah: 2** _ | _*_US003_*_ | 3 | Jah | _ *US003** | **2** |

## <a name="additional-resources"></a>Lisaressursid

[Ostulepingud](../../procurement/purchase-agreements.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
