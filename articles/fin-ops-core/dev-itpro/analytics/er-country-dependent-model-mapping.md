---
title: Riigi konteksti konfigureerimine sõltuvalt ER-i mudelivastendustest
description: Selles teemas selgitatakse, kuidas saate seadistada ER-i mudelivastendusi, et need sõltuksid nende kasutamist kontrolliva juriidilise isiku riigi/regiooni kontekstist.
author: NickSelin
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: 5b26c605bd64b8d8e5a90f4389261e8e56825111
ms.sourcegitcommit: 25b3dd639e41d040c2714f56deadaa0906e4b493
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2021
ms.locfileid: "7605367"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Riigi konteksti konfigureerimine sõltuvalt ER-i mudelivastendustest

[!include[banner](../includes/banner.md)]

Saate konfigureerida elektroonilise aruandluse (ER) mudelivastendused nii, et need juurutavad üldist ER-i andmemudelit, kuid on rakenduse Dynamics 365 Finance põhised. Selles teemas selgitatakse, kuidas kujundada ER-i andmemudelile mitut ER-i mudelivastendust, et juhtida, kuidas neid kasutatakse vastavate ER-i vormingute poolt, mida käitatakse erineva riigi/piirkonna kontekstiga ettevõtetest.

## <a name="prerequisites"></a>Eeltingimused

Selles teemas näidete lõpuleviimiseks peavad teil olema järgmised juurdepääsuõigused.

- Juurdepääs Rahanduse keskkonda ühe järgmise rolli jaoks:
    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on ette valmistatud sama rentniku jaoks, nagu rakendus Finance, ühe järgmise rolli jaoks.
    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

Mõned selle teema etapid nõuavad ER-vormingu käitamist. Mõnel juhul mõjutab ER-vormingu käitamist selle ettevõtte riigi/regiooni kontekst, kuhu olete hetkel sisse logitud. Saate käitada ER-vormingut praeguses RCS-i eksemplaris, kui ettevõttel, millel on nõutav riigi/regiooni kontekst, on RCS-is saadaval. Vastasel juhul tuleb teil laadida üles ER-i mudelivastenduse ja ER-vormingu konfiguratsioonide lõpetatud versioonid, mis kasutavad Finance’i eksemplari ER-i andmemudelit, ja käitada seejärel ER-vormingut selles Finance’i eksemplaris. Lisateavet selle kohta, kuidas RCS-is sisalduvaid konfiguratsioone Finance’i eksemplari importida, vt [Konfiguratsioonide importimine RCS-ist](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Ühe mudelivastendusega juhtum

Nõutud ER-komponentide kujundamiseks järgige etappe selle teema [lisas 1](#appendix1). Nüüd on teil mudelivastenduse konfiguratsioon **Vastendamine (üldine)**, mis sisaldab määratluse **Sisenemiskoht 1** mudelivastendust.

![ER konfiguratsioonide leht, vorming, et saada vastenduste konfiguratsioon.](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Konfigureeritud vormingu käitamine

1.  Valige **Konfiguratsioonide lehe** kiirkaardil **Versioonid** käsk **Käivita**.
2.  Valige nupp **OK**.

Pange tähele, et veebilehitseja pakub laadida alla tekstifaili, mis käivitatud ER-vormingus loodi. Kuna see vorming oli konfigureeritud kasutama määratlust **Sisenemiskoht 1** ja põhimudeli jaoks on hetkel saadaval ainult üks mudelivastendus, mis sisaldab selle määratluse vastendust, kasutas käivitatud ER-vorming andmeallikana mudelivastendust **Vastendamine (üldine)** konfiguratsioonis **Vastendamine (üldine)**. Seega sisaldab allalaaditud fail teksti **Lokaliseeritud funktsioon 1**.

## <a name="multiple-shared-model-mappings-case"></a>Mitme ühiskasutuses mudelivastendusega juhtum

Nõutud ER-komponentide kujundamiseks järgige etappe selle teema [lisas 2](#appendix2). Nüüd on teil mudelivastenduse konfiguratsioonid **Vastendamine (üldine)** ja **Vastendamise (üldine) kohandus**, mis sisaldavad määratluse **Sisenemiskoht 1** mudelivastendust.

![ER konfiguratsioonide leht, üldise kohandatud konfiguratsiooni vastendamine.](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Konfigureeritud vormingu käitamine

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vormindamine vastenduste õppimiseks**.
2.  Kiirkaardil **Versioonid** valige käsk **Käivita**.
3.  Valige nupp **OK**.

Pange tähele, et valitud ER-vormingu käivitamine ei õnnestu. Tõrketeade teavitab teid, et mudelil **Mudel vastenduste õppimiseks** on rohkem kui üks mudelivastendus ja määratlus **Sisenemiskoht 1** mudelivastenduse konfiguratsioonides **Vastendamine (üldine)** ja **Vastendamise (üldine) kohandus**. Samuti soovitab teade, et valite ühe nendest konfiguratsioonidest vaikimisi konfiguratsiooniks.

![ER konfiguratsioonide leht tõrketeatega.](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Vaikimisi vastenduskonfiguratsiooni määratlemine

Järgige neid etappe, et määratleda mudelivastenduse konfiguratsioon **Vastendamise (üldine) kohandus** vaikimisi konfiguratsiooniks, et selle vastendusi saaks kasutada andmeallikana ER-vormingu **Vormindamine vastenduste õppimiseks** jaoks.

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vastendamise (üldine) kohandus**.
2.  Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeerimiseks valmis.
3.  Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.
4.  Valige käsk **Salvesta**.

![ER konfiguratsioonide leht, vaikimisi on mudeli vastendamise liugur häälestatud väärtusele Jah.](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Konfigureeritud vormingu käitamine

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vormindamine vastenduste õppimiseks**.
2.  Kiirkaardil **Versioonid** valige käsk **Käivita**.
3.  Valige nupp **OK**.

Pange tähele, et valitud ER-vormingu käivitamine õnnestub. Veebilehitseja pakub laadida alla tekstifaili, mis käivitatud ER-vormingus loodi. Kuna see vorming oli konfigureeritud kasutama määratlust **Sisenemiskoht 1** ja vaikimisi konfiguratsiooniks oli valitud mudelivastenduse konfiguratsioon **Vastendamise (üldine) kohandus**, kasutas käivitatud ER-vorming andmeallikana mudelivastendust **Vastendamise (üldine) koopia** konfiguratsioonis **Vastendamise (üldine) kohandus**. Seega sisaldab allalaaditud fail teksti **Lokaliseeritud funktsiooni 1 kohandus**.

> [!NOTE]
> Kui muudate ettevõtet, kuhu olete praegu sisse logitud, ja käivitate selle ER-vormingu uuesti, saate loodud failis sama sisu, kuna vaikimisi ER-i mudelivastenduse konfiguratsioon ei sisalda ühtegi ettevõttest sõltuvat piirangut.

## <a name="multiple-mixed-model-mappings-case"></a>Mitme segatud mudelivastendusega juhtum

Nõutud ER-komponentide kujundamiseks järgige etappe selle teema [lisas 3](#appendix3). Nüüd on teil mudelivastenduse konfiguratsioonid **Vastendamine (üldine)** , **Vastendamise (üldine) kohandus** ja **Vastenduse (FR) mudelivastendus**, mis sisaldavad määratluse **Sisenemiskoht 1** mudelivastendust.

Pange tähele, et mudelivastenduse konfiguratsiooni **Vastendamine (FR)** 1. versioon konfigureeritakse nii, et see rakendub ainult mudeli **Mudel vastenduste õppimiseks** ER-vormingutele, mida käitatakse rakenduse Finance ettevõtetes, mille riigi/piirkonna kontekst on Prantsusmaa.

![ER konfiguratsioonide leht, mudeli vastendamise (FR) konfiguratsioon.](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Konfigureeritud vormingu käitamine

1.  Muutke ettevõte ettevõtteks **FRSI**.
2.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vormindamine vastenduste õppimiseks**.
3.  Kiirkaardil **Versioonid** valige käsk **Käivita**.
4.  Valige nupp **OK**.

Pange tähele, et valitud ER-vormingu käivitamine õnnestub. Veebilehitseja pakub laadida alla tekstifaili, mis käivitatud ER-vormingus loodi. Kuna see vorming oli konfigureeritud kasutama määratlust **Sisenemiskoht 1** ja vaikimisi konfiguratsiooniks oli valitud mudelivastenduse konfiguratsioon **Vastendamise (üldine) kohandus**, kasutas käivitatud ER-vorming andmeallikana mudelivastendust **Vastendamise (üldine) koopia** konfiguratsioonis **Vastendamise (üldine) kohandus**. Seega sisaldab allalaaditud fail teksti **Lokaliseeritud funktsiooni 1 kohandus**.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Prantsusmaale omase vastenduse konfiguratsiooni määratlemine vaikimisi konfiguratsiooniks

Järgige neid samme, et määratleda kohandatud mudelivastenduse konfiguratsioon **Vastendamine (FR)** vaikimisi konfiguratsiooniks. Pidage meeles, et kuna see vastendamine on omane Prantsusmaale, loetakse see vaikimisi vastenduseks kõikide mudelivastenduste konfiguratsioonide vahel, millel on määratud riigikoodiks **FR** väljal **ISO riigi/piirkonna koodid**.

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vastendamise (FR)**.
2.  Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeerimiseks valmis.
3.  Seadistage **Vaikimisi mudeli vastendamise** suvand väärtusele **Jah**.
4.  Valige käsk **Salvesta**.

![ER konfiguratsioonide leht, vastendamise (FR) konfiguratsioon, vaikimisi on mudeli vastendamise liugur häälestatud väärtusele Jah.](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Konfigureeritud vormingu käitamine

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vormindamine vastenduste õppimiseks**.
2.  Kiirkaardil **Versioonid** valige käsk **Käivita**.
3.  Valige nupp **OK**.

Pange tähele, et valitud ER-vormingu käivitamine õnnestub. Veebilehitseja pakub laadida alla tekstifaili, mis käivitatud ER-vormingus loodi. Kuna see vorming oli konfigureeritud kasutama määratlust **Sisenemiskoht 1** ja vaikimisi konfiguratsiooniks oli valitud mudelivastenduse konfiguratsioon **Vastendamine (FR)**, kasutas käivitatud ER-vorming andmeallikana mudelivastendust **Vastendamine (FR)** konfiguratsioonis **Vastendamine (FR)**. Seega sisaldab allalaaditud fail teksti **FR-i funktsioon 1**.

> [!NOTE]
> Kui muudate ettevõtet, millesse olete hetkel sisse loginud ja käitate selle ER-vormingut uuesti, sõltub väljund valitud ettevõtte riigi/regiooni kontekstist.

## <a name="other-model-mapping-cases"></a>Muud mudelivastendusega juhtumid

Nagu olete näinud, töötab mudelivastenduse valik ER-vormingu käitamiseks järgmisel viisil.

- Mudelivastenduse määratlus, mida ER-vorming kasutab, on määratud (selle teema näites **Sisenemiskoht 1**).
- Kõiki vastenduste konfiguratsioone, mis sisaldavad konkreetse määratlusega vastandust ja mis vastavad mis tahes konfigureeritud riigi/piirkonna kontekstipiirangutele, võib kasutada ER-vormingu käitamiseks (selle teema näidete puhul **Vastendamine (üldine)**, **Vastendamise (üldine) kohandus** ja **Vastendamine (FR)**).
- Mis tahes vaikimisi mudelivastendused, millel on riigi/piirkonna kontekstipiirangud, omavad valikus kõrgemat prioriteeti (selle teema näidetes **Vastendamine (FR)**).
- Mis tahes vaikimisi mudelivastendused, millel ei ole riigi/piirkonna kontekstipiirangut, omavad valikus järgmist kõrgemat prioriteeti (selle teema näidetes **Vastendamise (üldine) kohandus**).
- Mis tahes mudelivastendus, millel on riigi/piirkonna kontekstipiirangud olemas, omavad valikus kõrgemat prioriteeti, kui mudelivastendused, millel puuduvad riigi/piirkonna kontekstipiirangud.

Järgmine tabel annab teavet mudelivastenduste valiku tulemuste kohta kõigi võimalike mudelivastenduste seadistuste juhtumite puhul.

- Veerg 1 näitab, kas esimene mudelivastendus, millel ei ole riigi/piirkonna kontekstipiiranguid (näiteks jagatud vastendus **Vastendamine (üldine)**), on olemas ja kui jah, kas selle suvand **Mudelivastenduse vaikeväärtus** on seatud valikule **Jah**.
- Veerg 2 näitab, kas teine mudelivastendus, millel ei ole riigi/piirkonna kontekstipiiranguid (näiteks jagatud vastendus **Vastendamise (üldine) kohandus**), on olemas ja kui jah, kas selle suvand **Mudelivastenduse vaikeväärtus** on seatud valikule **Jah**.
- Veerg 3 näitab, kas esimene mudelivastendus, millel on riigi/piirkonna A kontekstipiirangud (näiteks Prantsusmaale omane vastendus **Vastendamine (FR)**), on olemas ja kui jah, kas selle suvand **Mudelivastenduse vaikeväärtus** on seatud valikule **Jah**.
- Veerg 4 näitab, kas teine mudelivastendus, millel on riigi/piirkonna A kontekstipiirangud, on olemas ja kui jah, kas selle suvand **Mudelivastenduse vaikeväärtus** on seatud valikule **Jah**.
- Veerus 5 on esitatud käitamise mudelivastenduse valiku tulemused ER-vormingus käitamisel ettevõtte juhtimise all, millel on riigi/piirkonna A kontekst.
- Veerus 6 on esitatud käitamise mudelivastenduse valiku tulemused ER-vormingus käitamisel ettevõtte juhtimise all, millel on riigi/piirkonna B kontekst.

Tabelis näitab plussmärk (+) mudelivastenduse konfiguratsiooni olemasolu teenuse Microsoft Azure praeguses eksemplaris, mida kasutatakse ER-vormingu käitamiseks (kas Finance või RCS).

| Kast | Mudelivastendus 1 ilma riigi/piirkonna kontekstita (MM1) | Mudelivastendus 2 ilma riigi/piirkonna kontekstita (MM2) | Mudelivastendus 1 koos riigi/piirkonna kontekstiga (MM1A) | Mudelivastendus 2 koos riigi/piirkonna kontekstiga (MM2A) | Käitamine ettevõtte kontrolli all, millel on riigi/piirkonna A kontekst | Käitamine ettevõtte kontrolli all, millel on riigi/piirkonna B kontekst |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Viga (vastendamine puudub)   | Viga (vastendamine puudub)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Viga (mitu vastendust) | Viga (mitu vastendust)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Viga (mitu vastendust) | MM1                        |
|     6   |     +   | vaikeväärtus |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | vaikeväärtus |         | MM1A                      | MM1                        |
|     8   |     +   |         | vaikeväärtus |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | vaikeväärtus | vaikeväärtus | Viga (mitu vastendust) | MM1                        |
|    10   | vaikeväärtus |         |         |         | MM1                       | MM1                        |
|    11   | vaikeväärtus |    +    |         |         | MM1                       | MM1                        |
|    12   | vaikeväärtus |         |    +    |         | MM1                       | MM1                        |
|    13   | vaikeväärtus | vaikeväärtus |         |         | Viga (mitu vastendust) | Viga (mitu vastendust)  |
|    14   | vaikeväärtus |         | vaikeväärtus |         | MM1A                      | MM1                        |
|    15   | vaikeväärtus |         | vaikeväärtus | vaikeväärtus | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | vaikeväärtus | vaikeväärtus | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Saage teada, millist vastendust ER-vormingu käitamisel kasutati

### <a name="configure-er-user-parameters"></a>Elektroonilise aruandluse kasutaja parameetrite konfigureerimine

1.  Valige lehe **Konfiguratsioonid** toimingupaani vahekaardilt **KONFIGURATSIOONID** suvand **Kasutaja parameetrid**.
2.  Määrake suvand **Käivita silumisrežiimis** valikule **Jah**.
4.  Valige **OK**.

### <a name="run-the-configured-format"></a>Konfigureeritud vormingu käitamine

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vormindamine vastenduste õppimiseks**.
2.  Kiirkaardil **Versioonid** valige käsk **Käivita**.
3.  Valige **OK**.

### <a name="review-the-er-debug-log"></a>Elektroonilise aruandluse silumislogi ülevaatamine

1.  Navigeerimispaanil avage **Moodulid \> Organisatsiooni haldus \> Elektrooniline aruandlus \> Konfiguratsiooni silumislogi**.
2.  Valige nupp **Laadi see leht uuesti**.

![Elektroonilise aruandluse käitamise logide leht.](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Pange tähele, et elektroonilise aruandluse silumislogisse on käitatud ER-vormingu jaoks lisatud uus kirje. Kuna selle kirje väli **Tase** on määratud suvandile **Teave**, on kirje teavituslik. Kuna vormingu komponendi väli on määratud suvandile **Vastenduse konfiguratsioon**, teavitab kirje teid mudelivastendustest, mida ER-vormingu **Vormindamine vastenduste õppimiseks** käitamise ajal kasutati (valitud väljal **Konfiguratsiooni nimi**). Välja **Loodud tekst** sisu teavitab teid, et vastenduskomponenti **Vastendamine (FR)**, mis asub konfiguratsioonis **Vastendamine (FR)**, on kasutatud selle aruande käitamiseks.

## <a name="appendix-1"></a><a name="appendix1"></a>Lisa 1

### <a name="configure-a-sample-data-model"></a>Näidisandmete mudeli konfigureerimine

Logige oma RCS-eksemplari sisse.

Selles näites loote konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Nende etappide läbimiseks peate kõigepealt RCS-is täitma teemas [Konfiguratsioonipakkuja loomine ja selle aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.

#### <a name="create-an-er-data-model-configuration"></a>ER-i andmemudeli konfiguratsiooni loomine

1.  Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.
2.  Valige paan **Aruandluse konfiguratsioonid**.
3.  Lehel **Konfiguratsioonid** valige suvand **Loo konfiguratsioon**.
4.  Dialoogiakna ripploendis sisestage välja **Nimi** suvand **Vastenduste õppimise mudel**.
5.  Valige **Konfiguratsiooni loomine**.
6.  Valige kiirkaart **Konfiguratsiooni komponendid**.

Pange tähele, et selle ER.konfiguratsiooni versiooni 1 mustand on redigeerimiseks valmis. See versioon sisaldab andmemudeli komponenti.

#### <a name="design-a-sample-data-model"></a>Näidisandmete mudeli kujundamine

1.  Lehel **Konfiguratsioonid** valige suvand **Kujundaja**.
2.  Valige suvand **Uus**.
3.  Dialoogiakna ripploendis väljal **Nimi** sisestage **Sisenemiskoht 1**.
4.  Valige **Lisa**.
5.  Valige suvand **Uus**.
6.  Dialoogiakna ripploendis väljale **Nimi** sisestage **Funktsiooni kirjeldus**.
7.  Valige **Lisa**.
8.  Valige suvand **Uus**.
9.  Dialoogiakna ripploendis valige väljagrupis **Uus sõlm** suvand **Mudeli juur**.
10. Väljale **Nimi** sisestage **Sisenemiskoht 2**.
11. Valige **Sisenemiskoht 2**.
12. Valige **Lisa**.
13. Valige suvand **Uus**.
14. Dialoogiakna ripploendis väljale **Nimi** sisestage **Funktsiooni kirjeldus**.
15. Valige **Lisa**.

    ![ER-i andmemudeli kujundaja leht.](./media/RCS-Context-specific-mapping-Model.PNG)

16. Valige käsk **Salvesta**.
17. Sulgege leht.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Mudelikonfiguratsiooni muudetud versiooni lõpetamine

1.  Valige lehe **Konfiguratsioonid** kiirkaardil **Versioonid** käsk **Muuda olekut**.

    > Muutke kavandatud mudelikonfiguratsiooni olek suvandist **Mustand** suvandile **Lõpetatud**, et seda saaks kasutada nõutavate mudelivastenduste ja -vormingute kujundamiseks.

2.  Valige **Lõpeta**.
3.  Valige nupp **OK**.

Pange tähele, et loodud konfiguratsioon on salvestatud kui lõpetatud versioon 1.

### <a name="configure-a-sample-model-mapping"></a>Näidisest mudelivastenduse konfigureerimine

#### <a name="create-an-er-model-mapping-configuration"></a>ER-i mudelivastenduse konfiguratsiooni loomine

1.  Lehel **Konfiguratsioonid** valige suvand **Loo konfiguratsioon**.
2.  Dialoogiakna rippmenüüs väljagrupil **Uus** valige suvand **Andmemudelil Vastenduste õppimise mudel põhinev mudelivastendus**.
3.  Väljal **Nimi** sisestage **Vastendamine (üldine)**.
4.  Väljal **Andmemudeli määratlus** valige **Sisenemiskoht 1**.
5.  Valige **Konfiguratsiooni loomine**.

Pange tähele, et selle ER.konfiguratsiooni versiooni 1 mustand on redigeerimiseks valmis. See versioon sisaldab mudelivastenduse komponenti.

#### <a name="design-a-sample-model-mapping"></a>Näidisest mudelivastenduse kujundamine

1.  Lehel **Konfiguratsioonid** valige suvand **Kujundaja**.

    Pange tähele, et suunatüübi **Mudelile** mudelivastendus on automaatselt lisatud selle komponendi määratlusele **Sisenemiskoht 1**.
    
2.  Valige **Kujundaja**, et hakata lisatud mudelivastendust redigeerima.
3.  Valige jaotises **Andmemudel** suvand **Redigeeri**.
4.  Sisestage väljale **Valem** tekst **Lokaliseeritud funktsioon 1**.
5.  Valige käsk **Salvesta**.
6.  Sulgege **Valemikoostaja** leht.

    ![ER-mudeli vastendamise kujundaja leht, sisestuspunkti 1 määratlus.](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Valige käsk **Salvesta**.
8.  Sulgege leht **Mudelivastenduse kujundaja**.
9.  Valige suvand **Uus**.
10. Väljal **Määratlus** valige **Sisenemiskoht 2**.
11. Väljal **Nimi** sisestage **Vastendamine (üldine) 2**.
12. Valige **Kujundaja**.
13. Valige jaotises **Andmemudel** suvand **Redigeeri**.
14. Sisestage väljale **Valem** tekst **Lokaliseeritud funktsioon 2**.
15. Valige käsk **Salvesta**.
16. Sulgege **Valemikoostaja** leht.

    ![ER-mudeli vastendamise kujundaja leht, sisestuspunkti 2 määratlus](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Valige käsk **Salvesta**.
18. Sulgege leht **Mudelivastenduse kujundaja**.

    ![ER -mudeli vastendusleht sisenemispunktide määratlustega.](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Sulgege leht **Mudelivastendused**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Mudelivastenduse konfiguratsiooni muudetud versiooni lõpetamine

1.  Valige **Konfiguratsioonide lehe** kiirkaardil **Versioonid** käsk **Muuda olekut**.

    > Muutke kavandatud mudelivastenduse konfiguratsiooni olek suvandist **Mustand** suvandile **Lõpetatud**, et ER-vormingud saaksid seda kasutada.

2.  Valige **Lõpeta**.
3.  Valige nupp **OK**.

Pange tähele, et loodud konfiguratsioon on salvestatud kui lõpetatud versioon 1.

### <a name="configure-a-sample-format"></a>Näidisvormingu konfigureerimine

#### <a name="create-an-er-format-configuration"></a>ER-vormingu konfiguratsiooni loomine

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudel vastenduste õppimiseks**.
2.  Valige **Konfiguratsiooni loomine**.
3.  Dialoogiakna rippmenüüs väljagrupil **Uus** valige suvand **Andmemudelil Mudel vastenduste õppimiseks põhinev vorming**.
4.  Sisestage väljal **Nimi** suvand **Vorming vastenduste õppimiseks**.
5.  Väljal **Andmemudeli määratlus** valige **Sisenemiskoht 1**.
6.  Valige **Konfiguratsiooni loomine**.

Pange tähele, et selle ER.konfiguratsiooni versiooni 1 mustand on redigeerimiseks valmis. See versioon sisaldab vormingu komponenti.

#### <a name="design-a-sample-format"></a>Näidisvormingu kujundamine

1.  Lehel **Konfiguratsioonid** valige suvand **Kujundaja**.
2.  Valige **Lisa juur**.
3.  Valige grupis **Tekst** üksus **String**.
4.  Valige nupp **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Vorminguelementide sidumine andmeallikaga

1.  Lehel **Vormingu koostaja** vahekaardil **Vastendamine** laiendage mudeliandmete allikat.
2.  Valige väli **Funktsiooni kirjeldus**.
3.  Valige **Seo**.

    ![ER-i vormingu koostaja leht.](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Valige käsk **Salvesta**.
5.  Sulgege leht.

## <a name="appendix-2"></a><a name="appendix2"></a>Lisa 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Näidisest mudelivastenduse konfigureerimine üldiseks kohandamiseks

Võite soovida kohandada mudelivastendust, mille konfiguratsiooni pakkuja (partner) teile andis, ja seejärel kasutada kohandatud versiooni oma ER-vormingute andmeallikana. Sel juhul peate looma kohandatud ER-i mudelivastenduse konfiguratsiooni, et teha olemasolevates mudelivastendustes vajalikud muudatused. Selles lisas kasutavad protseduurid näitena mudelivastendust **Vastendamine (üldine)**.

#### <a name="create-an-er-model-mapping-configuration"></a>ER-i mudelivastenduse konfiguratsiooni loomine

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vastendamine (üldine)**.
2.  Valige **Konfiguratsiooni loomine**.
3.  Dialoogiakna ripploendi väljagrupis **Uus** valige **Tuleta nimest: vastendamine (üldine), Litware, Inc.**.
4.  Väljal **Nimi** sisestage **Vastendamise (üldine) kohandus**.
5.  Valige **Konfiguratsiooni loomine**.

Pange tähele, et selle ER.konfiguratsiooni versiooni 1 mustand on redigeerimiseks valmis.

#### <a name="design-a-sample-model-mapping"></a>Näidisest mudelivastenduse kujundamine

1.  Lehel **Konfiguratsioonid** valige suvand **Kujundaja**.

    > Pange tähele, et põhikonfiguratsiooni mudelivastendused on sellele konfiguratsioonile automaatselt kopeeritud.

2.  Valige vastendus **Vastendamise (üldine) koopia**.
3.  Valige **Kujundaja**.
4.  Valige jaotises **Andmemudel** suvand **Redigeeri**.
5.  Sisestage väljale **Valem** tekst **Lokaliseeritud funktsiooni 1 kohandus**.
6.  Valige käsk **Salvesta**.
7.  Sulgege leht.

    ![ER-mudeli vastendamise kujundaja leht, üldise funktsiooni 1 kohandatud valem.](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Valige käsk **Salvesta**.
9.  Sulgege leht.
10. Valige vastendus **Vastendamise (üldine) 2 koopia**.
11. Valige **Kujundaja**.
12. Valige jaotises **Andmemudel** suvand **Redigeeri**.
13. Sisestage väljale **Valem** tekst **Lokaliseeritud funktsiooni 2 kohandus**.
14. Valige käsk **Salvesta**.
15. Sulgege leht.

    ![ER-mudeli vastendamise kujundaja leht, üldise funktsiooni 2 kohandatud valem.](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Valige käsk **Salvesta**.
17. Sulgege leht.

    ![ER-mudel andmeallika vastendamise lehega vastendamise (üldine) koopia vastendamiseks.](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Sulgege leht.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Mudelivastenduse konfiguratsiooni muudetud versiooni lõpetamine

1.  Valige lehe **Konfiguratsioonid** kiirkaardil **Versioonid** käsk **Muuda olekut**.

    > Muutke kavandatud mudelivastenduse konfiguratsiooni olek suvandist **Mustand** suvandile **Lõpetatud**, et ER-vormingud saaksid seda kasutada.

2.  Valige **Lõpeta**.
3.  Valige nupp **OK**.

Pange tähele, et loodud konfiguratsioon on salvestatud kui lõpetatud versioon 1.

## <a name="appendix-3"></a><a name="appendix3"></a>Lisa 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Näidisest mudelivastenduse konfigureerimine konkreetsele riigile/piirkonnale kohandamiseks

Mõne ER-vormingu puhul võivad andmete ettevalmistamisele kehtida konkreetsele riigile/piirkonnale omased nõuded. Sellisel juhul saate hallata eraldi ER-i mudelivastenduse konfiguratsiooni ja isoleerida need konkreetsele riigile/piirkonnale omased nõuded üldisest juurutamisest. Selle lisa protsessid kasutavad näitena ER-vormingut **Vorming vastenduste õppimiseks** ja konkreetselt Prantsusmaale omaseid nõudeid.

#### <a name="create-an-er-model-mapping-configuration"></a>ER-i mudelivastenduse konfiguratsiooni loomine

Esmalt looge uus ER-i mudelivastenduse konfiguratsioon konkreetsele riigile/piirkonnale omaste nõuete juurutamiseks. Kasutage oma kohandatud ER-i mudelivastenduse konfiguratsiooni alusena.

1.  Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Vastendamise (üldine) kohandus**.
2.  Valige **Konfiguratsiooni loomine**.
3.  Dialoogiakna ripploendi väljagrupis **Uus** valige **Tuleta nimest: vastendamise (üldine) kohandus, Litware, Inc.**.
4.  Väljal **Nimi** sisestage **Vastendamine (FR)**.
5.  Valige **Konfiguratsiooni loomine**.

Pange tähele, et selle ER.konfiguratsiooni versiooni 1 mustand on redigeerimiseks valmis.

#### <a name="design-a-sample-model-mapping"></a>Näidisest mudelivastenduse kujundamine

1.  Lehel **Konfiguratsioonid** valige suvand **Kujundaja**.

    > Pange tähele, et põhikonfiguratsiooni mudelivastendused on sellele konfiguratsioonile automaatselt kopeeritud.

2.  Valige vastendus **Vastendamise (üldine) koopia koopia**.
3.  Nimetage see ümber **Vastendamine (FR)**.
4.  Valige **Kujundaja**.
5.  Valige jaotises **Andmemudel** suvand **Redigeeri**.
6.  Sisestage väljale **Valem** tekst **FR-i funktsioon 1**.
7.  Valige käsk **Salvesta**.
8.  Sulgege leht.

    ![ER-mudeli vastendamise kujundaja leht, FR funktsiooni 1 valem.](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Valige käsk **Salvesta**.
10. Sulgege leht.
11. Valige vastendus **Vastendamise (üldine) 2 koopia koopia**.
12. Nimetage see ümber **Vastendamine (FR) 2**.
13. Valige **Kujundaja**.
14. Valige jaotises **Andmemudel** suvand **Redigeeri**.
15. Sisestage väljale **Valem** tekst **FR-i funktsioon 2**.
16. Valige käsk **Salvesta**.
17. Sulgege leht.

    ![ER-mudeli vastendamise kujundaja leht, FR funktsiooni 2 valem.](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Valige käsk **Salvesta**.
19. Sulgege leht.

    ![ER -mudel andmeallika vastendamise lehele.](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Sulgege leht.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Konkreetsele riigile/piirkonnale omaste kontekstipiirangute kasutamiseks määramine

1.  Valige lehel **Konfiguratsioonid** kiirkaardil **ISO riigi/piirkonna koodid** suvand **Uus**.
2.  Väljal **ISO** valige **FR**.
3.  Valige käsk **Salvesta**.

Pange tähele, et ER-vormingu käitamiseks peate logima rakenduses Finance konkreetsesse ettevõttesse sisse. Seega saab seda ettevõtet lugeda osapooleks, mis kontrollib nii ER-vormingu käitamist kui ka õige ER-i mudelivastenduse valimist aluseks oleva ER-i mudelivastenduse jaoks. Lisades riigikoodi **FR** te määrate, et see mudelivastendus on aluseks oleva andmemudeli ER-vormingu poolt valimiseks saadaval ainult siis, kui see vorming käivitatakse ettevõtte kontrolli all, millel on Prantsusmaa riigi/piirkonna kontekst.

Saate lisada ER-i mudelivastenduse konfiguratsiooni ühele versioonile mitu riigi/piirkonna koodi. Sel viisil saab mudelivastenduse konfiguratsioonis sisalduvaid mudelivastendusi kasutada ER-vormingu jaoks, mida käitatakse ettevõtete kontrolli all, millel on erinev riigi/piirkonna kontekst.

Pange tähele, et riigi/piirkonna koodide loend on toodud igas ER-i mudelivastenduse konfiguratsiooni versioonis ja võib versiooniti erineda.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Mudelivastenduse konfiguratsiooni muudetud versiooni lõpetamine

1.  Valige lehe **Konfiguratsioonid** kiirkaardil **Versioonid** käsk **Muuda olekut**.

    > Muutke kavandatud mudelivastenduse konfiguratsiooni olek suvandist **Mustand** suvandile **Lõpetatud**, et ER-vormingud saaksid seda kasutada.

2.  Valige **Lõpeta**.
3.  Valige nupp **OK**.

Pange tähele, et loodud konfiguratsioon on salvestatud kui lõpetatud versioon 1.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) mudelivastenduse haldamine eraldi ER-i konfiguratsioonides](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Riigi/regiooni konteksti rakendamine](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Konfigureerisin RCS-is kaks jagatud ER-i mudelivastenduse konfiguratsiooni ja märkisin ühe neist kui vaikimisi mudelivastenduse konfiguratsioon. Käitasin edukalt ER-vormingut, mis loodi sama aluseks olevas ER-i andmemudeli konfiguratsiooni jaoks, et testida mudelivastendusi. Seejärel importisin kogu ER-lahenduse (ER-i andmemudel, kaks ER-i mudelivastenduse konfiguratsiooni ja ER-vormingu konfiguratsioon) rakendusse Finance. Miks kuvatakse tõrketeade, kui proovin käitada sama ER-vormingut rakenduses Finance?
Vaikimisi mudelivastenduse säte sõltub keskkonnast. See on RCS-is konfigureeritud, kuid seda pole rakendusse Finance imporditud. Selle ER-vormingu edukaks käitamiseks peate märkima ühe ER-i mudelivastenduse konfiguratsioonidest ka rakenduses Finance kui vaikimisi mudelivastenduse konfiguratsioon.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Konfigureerisin ühe mudelivastenduse kui jagatud mudelivastendus ja lõpetasin selle mustandiversiooni. Seejärel lisasin samale andmemudelile uue mudelivastenduse konfiguratsiooni ja konfigureerisin selle kui konkreetselt Prantsusmaale omane. Miks valitakse ER-vormingu käitamisel jagatud mudelivastendus, olgugi see ER-vorming kasutab õiget juurmääratlust ja selle käivitamine toimub ettevõtte kontrolli all, millel on Prantsusmaa riigi/piirkonna kontekst?
Veenduge, et jagatud mudelivastenduse konfiguratsioon ei oleks märgitud vaikimisi mudelivastenduse konfiguratsiooniks. Vastasel juhul on sellel vastenduse valikul kõrgem prioriteet. Veenduge ka, et konkreetselt Prantsusmaale omane mudelivastenduse konfiguratsioon oleks arvesse võetud, kui ER-vormingu käivitamise ajal on valitud vastendamine. ER-i mudelivastenduse konfiguratsioon on valimiseks saadaval ainult siis, kui vähemalt üks järgmistest tingimustest on täidetud.
- Vähemalt üks ER-i mudelivastenduse konfiguratsiooni versioon on olekus **Lõpetatud** või **Jagatud**. Sel juhul kasutatakse ER-vormingu käivitamiseks versiooni, millel on kõrgem versiooninumber.
- ER-i mudelivastenduse konfiguratsiooni suvand **Käivita mustand** on sisse lülitatud. Sel juhul kasutatakse ER-vormingu käivitamiseks versiooni, mille olek on **Mustand**.
> Suvand **Käivita mustand** muutub lehel **Konfiguratsioonid** iga ER-i mudelivastenduse konfiguratsiooni jaoks kättesaadavaks siis, kui elektroonilise aruandluse kasutaja parameeter **Käivita säte** on sisse lülitatud.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
