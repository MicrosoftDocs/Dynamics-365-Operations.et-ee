---
title: Kasuta elektroonilise aruandluse vormingutes ANDMEKOGUMI andmeallikaid
description: Selles teemas selgitatakse, kuidas saate kasutada elektroonilises aruandluses DATA COLLECTION andmeallikaid.
author: NickSelin
ms.date: 08/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-01-01
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: f001734baf9aee59f0a61d21ca5a99af0c55b56f
ms.sourcegitcommit: 7e32e5e39e762a4b1606161cb603a450d13b5251
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2021
ms.locfileid: "7413590"
---
# <a name="use-data-collection-data-sources-in-electronic-reporting-formats"></a>Kasuta elektroonilise aruandluse vormingutes ANDMEKOGUMI andmeallikaid

[!include [banner](../includes/banner.md)]

Saate kasutada operatsioonide kujundajat [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) raamistiku jaoks et [vormida](general-electronic-reporting.md#FormatComponentOutbound) komponent, mida kasutatakse väljamineva dokumendi loomiseks eri vormingutes. Konfigureeritud vormingukomponendi hierarhiline struktuur koosneb erinevate tüüpide vorminguelementidest. Neid vorminguelemente kasutatakse loodud dokumentide täitmiseks nõutava teabega käitusaja ajal. Vaikimisi, kui käitate ER-vormingut, käitatakse vorminguelemente samas järjekorras, nagu need on esitatud vorminguhierarhias: ükshaaval, ülevalt alla.

Kui ER käitab vorminguelementi, mis sisaldab sidumist, käitatakse selle sidumise valemit ja vorminguelement lisab väärtuse loodud dokumendile. Näiteks võib sidumine edastada [andmemudeli](general-electronic-reporting.md#data-model-and-model-mapping-components) välja väärtuse vorminguelemendile. Saate konfigureerida andmeallikat DATA COLLECTION, et koguda käitusajal andmemudeli väljade väärtusi, teha väärtuste summeerimist ja täita loodud dokument kogutud väärtustega. Selle lähenemise kasutamiseks muutke esmane sidumine nii, et konfigureeritud DATA COLLECTION andmeallikat kasutatakse andmemudeli välja väärtuse edastamiseks vorminguelemendile. Väärtuste edastamisel andmeallikast DATA COLLECTION saate koguda nõutavaid üksikasju edasiseks kasutamiseks.

Andmeallika DATA COLLECTION konfigureerimisel määrake andmeallikas hallatav väärtuse tüüp. Praegu toetatakse järgmisi [andmetüüpe](er-formula-supported-data-types-primitive.md) väärtuste kogumiseks:

- Loogiline
- Kuupäev
- DateTime
- GUID
- Int64
- Täisarv
- Tegelik
- String
- Kellaaeg

Võite kasutada andmeallika `Collect(Value)`DATA COLLECTION meetodit, et edastada väärtus kogumiseks andmeallikale. Selles meetodis on argument kas konstant või vastava `Value`andmetüübiga andmeallika välja kehtiv tee.

Kasutage `Result` atribuuti andmeallika DATA COLLECTION kogutud väärtuste loendile juurde pääsemiseks. See atribuut tagastab [kirjeloendi](er-formula-supported-data-types-composite.md#record-list). Kirjeloendi kirjed sisaldavad välja, `Value`, mida saate kasutada kogutud väärtustele juurdepääsemiseks.

Vaikimisi kogub andmeallikas DATA COLLECTION ainult kordumatuid väärtusi.

Kõigi väärtuste kogumiseks määrake **Kogu kõiki väärtusi** välja konfigureeritud DATA COLLECTION andmeallika väärtuseks **Jah**. Kui välja **Kõigi väärtuste kogumine** väärtuseks on seatud **Jah**, muutub `Sum(Flag)` parameeteriseeritud atribuut kättesaadavaks. Selle atribuudi abil saate saada kõigi praegu kogutud väärtuste kogusumma. Selles atribuudis on `Flag` argument [Kahendmuutuja](er-formula-supported-data-types-primitive.md#boolean) väärtus, mida kasutatakse selle näitamiseks, kas koguväärtus tuleb lähtestada.

- Kui väärtus **Väär** on loodud, jätkatakse summeerimist eelnevalt kogutud summast.
- Kui väärtus **Tõene** on antud, alustatakse uut summeerimist.

Praegu toetatakse järgmisi andmetüüpe väärtuste summeerimiseks:

- Int64
- Täisarv
- Tegelik

Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.

## <a name="example-configure-an-er-format-to-do-counting-and-summing-by-using-a-data-collection-data-source"></a>Näide: ER-vormingu konfigureerimine loendamiseks ja summeerimiseks, kasutades andmeallikat DATA COLLECTION

See näide näitab, kuidas kasutaja süsteemiadministraatoris või elektroonilise aruandluse funktsiooninõustaja rollis saab konfigureerida ER-vormingut, mille andmeallikas on DATA COLLECTION, mida kasutatakse jooksvate kogusummade arvutamiseks ja summeeritud väärtuste kogumiseks.

Kõik selle teema ülesanded saab täita ettevõttes USMF rakenduses Microsoft Dynamics 365 Finance.

### <a name="upload-and-use-the-provided-er-solution"></a>Esitatud ER-lahenduse üleslaadimine ja kasutamine

1. [ER-i näidiskonfiguratsioonide importimine](er-defer-sequence-element.md#import-the-sample-er-configurations).
2. [Konfiguratsioonipakkuja aktiveerimine](er-defer-sequence-element.md#activate-a-configurations-provider).
3. [Vaadake üle imporditud mudelivastendus](er-defer-sequence-element.md#review-the-imported-model-mapping).
4. [Imporditud vormingu ülevaatamine](er-defer-sequence-element.md#review-the-imported-format).
5. [Imporditud vormingu käivitamine](er-defer-sequence-element.md#run-the-imported-format).

### <a name="run-the-format-of-the-provided-er-solution"></a>Pakutava ER-i lahenduse vormingu käitamine

1. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
2. Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.
3. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail, mis sisaldab algse vormingu käivitamise tulemusi](./media/er-data-collection-data-sources-01.png)

### <a name="modify-the-format-of-the-er-solution-to-calculate-the-running-tax-total"></a>ER-lahenduse vormingu muutmine jooksva maksu kogusumma arvutamiseks

Kui kannete maht on praeguse näite mahust palju suurem, võib summeerimise aeg suureneda ja põhjustada jõudluse probleeme. Vormingu sätte muutmisega saate aidata vältida nende jõudluse probleeme. Kuna teil on juurdepääs maksu väärtustele, et kaasata need loodud aruandesse, saate seda teavet kasutada maksude väärtuste summeerimiseks.

1. Tehke lehe **Vormingu kujundaja** vahekaardil **Vastendamine** valik **Lisa juur**.
2. Valige **Andmeallika lisamine** dialoogiboksis suvand **Funktsioonid** \> **Andme kogum**.
3. **'Andmete kogumine' andmeallika atribuudi** dialoogiboksis järgige neid samme:

    1. Väljale **Nimi** sisestage **KogutudMaksuVäärtus**.
    2. Väljal **Üksuse tüüp** valige **Tegelik**.
    3. Väljal **Kaasa kõik väärtused** valige **Jah**.
    4. Valige nupp **OK**.

4. Valige **Aruanne\\Read\\Kirje\\MaksuHulk** numbri vormielement.

    > [!NOTE]
    > Praegu on `@.Value` sidumine konfigureeritud selle elemendi jaoks. Seetõttu luuakse dokument, kui see täidetakse välja `model.Data.List.Value` maksuväärtustega.

5. Valige **Valemi redigeerimine**.
6. Tehke lehel **Valemi kujundaja** järgmist:

    1. **Valemi** väljal asendage `@.Value` järgmisega `CollectedTaxValues.Collect(@.Value)`.
    2. Salvestage muudatused ja sulgege leht.

    > [!NOTE]
    > Uus sidumine annab sama maksuväärtuse loodud dokumendile. Kuid neid väärtusi kogutakse ka andmeallikas **KogutudMaksuVäärtus**.

7. Valige **Aruanne\\Read\\Kirje\\KäitaKõik** numbri vormielement.
8. Valige **Valemi redigeerimine**.
9. Tehke lehel **Valemi kujundaja** järgmist:

    1. Sisestage **Valem** väljale `CollectedTaxValues.Sum(false)`.
    2. Salvestage muudatused ja sulgege leht.

    > [!NOTE]
    > Uus sidumine annab loodud dokumendile üle juba sisestatud maksuväärtuste kogusumma.

    ![Numbrilised elemendid, mis on vormingukujundaja lehel värskendatud sidumisi](./media/er-data-collection-data-sources-02.png)

10. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
11. Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.
12. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail, mis sisaldab algse vormingu käivitamise tulemusi](./media/er-data-collection-data-sources-03.png)

### <a name="modify-the-format-to-evaluate-the-list-of-collected-tax-values"></a>Muutke vormingut kogutud maksuväärtuste loendi hindamiseks

1. Valige **vormingukujundaja** lehe vahekaardil **Vorming** valige **Aruanne\\Read\\Kirje\\KäitaKõik** numbrivormingu element ja järgige seejärel neid samme:

    1. Väljal **Numbriline tüüp** muutke väärtus **Tegelik** asemel **Täisarvuks**.
    2. Muutke **Numbriline väärtus** väljal **F2** **F0** väärtuseks.

3. Valige vahekaardil **Vastendus** suvand **Redigeeri vorming**.
4. Tehke lehel **Valemi kujundaja** järgmist:

    1. Sisestage **Valem** väljale `COUNT(CollectedTaxValues.Result)`.
    2. Salvestage muudatused ja sulgege leht.

    > [!NOTE]
    > Uus sidumine annab loodud dokumendile edasi maksuväärtuste kogumise loendi kirjete arvu.

5. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
6. Valige dialoogiaknas **Elektroonilise aruandluse parameetrid** suvand **OK**.
7. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail, mis sisaldab algse vormingu käivitamise tulemusi](./media/er-data-collection-data-sources-04.png)

## <a name="frequently-asked-questions"></a>Korduma kippuvad küsimused

### <a name="if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions"></a>Kui ma soovin arvutada jooksvaid kogusummasid ja koguda andmeid, siis milline on erinevus andmeallika DATA COLLECTION ja sisseehitatud DATA COLLECTION funktsioonide kasutamise vahel?

Nii andmeallikat DATA COLLECTION kui ka sisseehitatud [DATA COLLECTION](er-functions-category-data-collection.md) funktsioone saab kasutada andmete kogumiseks, summeerimiseks ja loendamiseks, mis põhineb loodud väljaminevale dokumendile edastatud teabele. Kuid kui proovite otsustada, millist tehnikat kasutada, peate arvestama järgmiste punktidega.

| Andmeallikas | Sisseehitatud funktsioonid |
|-------------| ------------------ |
| Kogutakse ainult väärtusi. | <p>Kogutakse nimetatud väärtusi. Seetõttu saab summad arvutada eraldi väärtusegruppide jaoks.</p><p>Lisaks saab gruppe ekstraktida loendina.</p><p>Koguda saab ka tekstiväärtusi.</p> |
| Kordumatud väärtused kogutakse automaatselt. | Kogutud väärtustest kordumatute väärtuste loendi ekstraktimiseks on vajalikud lisasätted. |
| Jõudlus sõltub kogutud väärtuste mahust. | Praktikas ei sõltu jõudlus kogutud väärtuste mahust. |
| See tehnika töötab igat tüüpi väljaminevate dokumentide puhul. | See tehnika töötab ainult teksti ja XML-dokumentide puhul. |

## <a name="additional-resources"></a>Lisaressursid

- [Vormingu konfigureerimine loendamiseks ja liitmiseks](./tasks/er-format-counting-summing-1.md)
- [Elektroonilise aruandluse vormingus järjestuselementide käivitamise edasilükkamine](er-defer-sequence-element.md#Example)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
