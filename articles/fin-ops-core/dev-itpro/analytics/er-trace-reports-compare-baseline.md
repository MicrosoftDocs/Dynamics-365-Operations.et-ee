---
title: Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega
description: See teema selgitab, kuidas võrrelda loodud elektroonilise aruandluse aruannete tulemusi aruande alusväärtustega.
author: NickSelin
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: a8609cb026e7738eab96980bc9fe4a53340272eb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743577"
---
# <a name="trace-generated-report-results-and-compare-them-with-baseline-values"></a>Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega

[!include[banner](../includes/banner.md)]

Saate jälgida väljaminevaid elektroonilisi dokumente loovate elektroonilise aruandluse vormingute tulemusi. Kui jälje loomine on sisse lülitatud (kasutades elektroonilise aruandluse parameetrit **Käita silumisrežiimis**), luuakse elektroonilise aruandluse vormingu täitmislogis uus jälituskirje iga kord, kui elektroonilise aruandluse aruannet käitatakse. Igasse loodud jälge salvestatakse järgmised üksikasjad.

- Kõik valideerimisreeglitega loodud hoiatused
- Kõik valideerimisreeglitega loodud tõrked
- Kõik jälituskirje manustena salvestatud loodud failid

Saate salvestada mis tahes elektroonilise aruandluse vormingu puhul eraldi rakenduse alusfailid. Faile loetakse alusfailideks, kui need kirjeldavad käitatud aruannete oodatud tulemusi. Kui alusfail on saadaval elektroonilise aruandluse vormingu puhul, mis käitatakse, kui jälje loomine on sisse lülitatud, salvestab jälg peale eespool nimetatud üksikasjade ka loodud elektroonilise dokumendi ja alusfaili võrdluse tulemuse. Saate ühe klõpsuga tuua loodud elektroonilise dokumendi ja selle alusfaili ühe zip-failina. Seejärel saate teha üksikasjaliku võrdluse, kasutades välist tööriista, nt WinDiff.

Saate jälge hinnata, et analüüsida, kas loodud elektroonilised dokumendid sisaldavad oodatud sisu. Nüüd saate teha selle hindamise kasutaja vastuvõtu testimise (UAT) keskkonnas, kui koodi alus on muutunud (näiteks kui läksite üle rakenduse uuele eksemplarile, installisite kiirparanduspakette või juurutasite koodimuudatusi). Sel moel saate kindel olla, et hindamine ei mõjuta kasutatud elektroonilise aruandluse aruannete täitmist. Paljude elektroonilise aruandluse aruannete puhul saab hindamist teha järelevalveta režiimis.

Selle funktsiooni kohta lisateabe saamiseks vaadake tegevusejuhiseid **Elektrooniline aruandlus, aruannete loomine ja tulemuste võrdlemine (1. osa)** ning **Elektrooniline aruandlus: aruannete loomine ja tulemuste võrdlemine (2. osa)**, mis on osa äriprotsessist **7.5.4.3 IT-teenuste/-lahenduste testimine (10679)** ja mille saab alla laadida [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684). Need tegevusejuhised selgitavad teile elektroonilise aruandluse konfigureerimise protsessi alusfailide kasutamiseks loodud elektrooniliste dokumentide hindamiseks.

## <a name="example-trace-generated-report-results-and-compare-them-with-baseline-values"></a>Näide. Loodud aruandetulemite jälgimine ja võrdlemine alusväärtustega

See protseduur selgitab, kuidas konfigureerida elektroonilise aruandluse raamistikku teabe kogumiseks elektroonilise aruandluse vormingu käivitamiste kohta ja seejärel hinnata nende käivitamiste tulemusi. Osana sellest hindamisest võrreldakse loodud dokumente nende alusfailidega. Selles näites loote näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll. Need etapid saab lõpule viia ükskõik millise andmekomplekti abil.

Selle näite etappide lõpuleviimiseks peate esmalt läbima etapid teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Lehel **Lokalisatsiooni konfiguratsioonis** jaotises **Konfiguratsiooni pakkujad** veenduge, et näidisettevõtte Litware, Inc. konfiguratsiooni pakkuja oleks loendis ja tähistatud märkega **Aktiivne**. Kui te ei näe seda konfiguratsioonipakkujat, järgige etappe teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-document-management-parameters"></a>Dokumendihalduse parameetrite konfigureerimine

1. Valige **Organisatsiooni haldus** \> **Dokumendihaldus** \> **Dokumenditüübid** ja looge uus dokumenditüüp alusfailide salvestamiseks.
2. Sisestage väljale **Klass** suvand **Lisa fail**.
3. Sisestage väljale **Grupp** suvand **Fail**.

![Dokumenditüüpide leht](media/GER-BaselineSample-SetupDocumentType.PNG "Dokumenditüüpide lehe kuvatõmmis")

> [!NOTE]
> Uus dokumenditüüp, millel on sama nimi, tuleb konfigureerida iga andmekogumi jaoks, kus plaanite kasutada elektroonilise aruandluse alusfunktsiooni.

### <a name="configure-er-parameters-to-start-to-use-the-baseline-feature"></a>Elektroonilise aruandluse parameetrite konfigureerimine alusfunktsiooni kasutamise alustamiseks

1. Tööruumis **Elektrooniline aruandlus** jaotisest **Seotud lingid** valige suvand **Elektroonilise aruandluse parameetrid**.

    ![Elektroonilise aruandluse tööruum](media/GER-BaselineSample-ERWorkspace.PNG "Elektroonilise aruandluse tööruumi kuvatõmmis")

2. Vahekaardil **Manused** väljas **Alus** sisestage või valige äsja loodud dokumenditüüp.

    ![Elektroonilise aruandluse parameetrite lehe vahekaart Manused](media/GER-BaselineSample-ERParameters.PNG "Elektroonilise aruandluse parameetrite kuvatõmmis")

3. Valige käsk **Salvesta** ja seejärel sulgege leht **Elektroonilise aruandluse parameetrid**.

### <a name="add-a-new-er-model-configuration"></a>Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine

1. Valige tööruumis **Elektrooniline aruandlus** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.
2. Valige toimingupaanilt suvand **Loo konfiguratsioon**.
3. Dialoogiakna ripploendis sisestage välja **Nimi** suvand **Elektroonilise aruandluse aluste õppimise mudel**.
4. Valige suvand **Loo konfiguratsioon** uue elektroonilise aruandluse andmemudeli kirje loomise kinnitamiseks.

![Konfiguratsiooni loomise rippmenüü dialoogiaken](media/GER-BaselineSample-ModelAdd.PNG "Konfiguratsiooni loomise rippmenüü dialoogiakna kuvatõmmis")

### <a name="design-a-data-model"></a>Andmemudeli kujundamine

1. Lehel **Konfiguratsioonid** valige toimingupaanilt suvand **Kujundaja**.
2. Valige suvand **Uus**.
3. Dialoogiakna ripploendis sisestage välja **Nimi** suvand **Juur**.
4. Valige **Lisa**.
5. Valige suvand **Juure viide**.
6. Valige nupp **OK** ja seejärel käsk **Salvesta**.
7. Sulgege leht **Mudeli koostaja**.
8. Valige käsk **Muuda olekut**.
9. Valige suvand **Valmis** ja seejärel nupp **OK**.

![Konfiguratsioonide leht](media/GER-BaselineSample-ModelComplete.PNG "Konfiguratsioonide lehe kuvatõmmis")

### <a name="add-a-new-er-format-configuration"></a>Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine

1. Lehel **Konfiguratsioonid** valige toimingupaanilt suvand **Loo konfiguratsioon**.
2. Dialoogiakna rippmenüüs väljagrupil **Uus** valige suvand **Andmemudelil Elektroonilise aruandluse aluste õppimise mudel põhinev vorming**.
3. Sisestage välja **Nimi** suvand **Vorming elektroonilise aruandluse aluste õppimiseks**.
4. Valige suvand **Loo konfiguratsioon** uue elektroonilise aruandluse vormingu kirje loomise kinnitamiseks.

![Konfiguratsiooni loomise rippmenüü dialoogiaken](media/GER-BaselineSample-FormatAdd.PNG "Konfiguratsiooni loomise rippmenüü dialoogiakna kuvatõmmis")

### <a name="design-a-format"></a>Vormingu kujundamine

Selles näites loote lihtsa elektroonilise aruandluse vormingu XML-dokumentide loomiseks.

1. Lehel **Konfiguratsioonid** valige toimingupaanilt suvand **Kujundaja**.
2. Valige **Lisa juur**.
2. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. Valige puul suvand **Üldine\\Fail**.
    2. Väljale **Nimi** sisestage **Väljund**.
    3. Valige nupp **OK**.

3. Valige **Lisa**.
4. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. Valige puul suvand **XML\\Element**.
    2. Väljale **Nimi** sisestage suvand **Dokument**.
    3. Valige nupp **OK**.

5. Valige puul suvand **Väljund\\Dokument**.
6. Valige **Lisa**.
7. Dialoogiakna ripploendis järgige allolevaid etappe.

    1. Valige puul suvand **XML\\Atribuut**.
    2. Sisestage **ID** väljale **Nimi**.
    3. Valige nupp **OK**.

    ![Vormingu koostaja leht](media/GER-BaselineSample-FormatLayoutDesign.PNG "Vormingu koostaja lehe kuvatõmmis")

8. Valige vahekaardil **Vastendamine** käsk **Kustuta**.
9. Valige **Lisa juur**.
10. Valige puul dialoogiakna ripploendist suvandid **Üldine\\Kasutaja sisendparameeter** ja seejärel järgige allolevaid etappe.

    1. Sisestage **ID** väljale **Nimi**.
    2. Sisestage väljale **Silt** suvand **Sisestage ID**.
    3. Valige nupp **OK**.

11. Valige puul suvand **Väljund\\Dokument\\ID**.
12. Valige suvand **Seo** ja seejärel käsk **Salvesta**.

![Vormingu koostaja leht](media/GER-BaselineSample-FormatMappingDesign.PNG "Vormingu koostaja lehe kuvatõmmis")

Kujundatud struktuuri põhjal loob konfigureeritud vorming XML-faili. See XML sisaldab elementi **Juur**, millel on atribuut **ID**, mis seatakse väärtusele, mille kasutaja sisestab elektroonilise aruandluse käitusaja dialoogiboksi.

### <a name="generate-a-new-baseline-file-for-a-designed-er-format"></a>Uue alusfaili loomine kujundatud elektroonilise aruandluse vormingu jaoks

1. Valige lehel **Konfiguratsioonid** kiirkaardil **Versioonid** käsk **Käivita**.
2. Sisestage väljale **Sisestage ID** väärtus **1**.
3. Valige nupp **OK**.

    ![Elektroonilise aruande parameetrite dialoogiaken](media/GER-BaselineSample-FormatRunToMakeBaselineFile1.PNG "Elektroonilise aruande parameetrite dialoogiakna kuvatõmmis")

4. Salvestage loodud failist **out.Admin.xml** kohalik koopia, et saaksite seda hiljem kasutada selle elektroonilise aruande vormingu alusena.

    ![Teatis konfiguratsioonide lehel loodud faili kohta](media/GER-BaselineSample-FormatRunToMakeBaselineFile2.PNG "Kuvatõmmis teatisest konfiguratsioonide lehel loodud faili kohta")

### <a name="configure-er-parameters-to-use-the-baseline-feature"></a>Elektroonilise aruandluse parameetrite konfigureerimine alusfunktsiooni kasutamiseks

1. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardilt **Konfiguratsioonid** suvand **Kasutaja parameetrid**.
2. Määrake suvand **Käivita silumisrežiimis** valikule **Jah**.
3. Valige nupp **OK**.

![Kasutaja parameetrite dialoogiaken](media/GER-BaselineSample-ERUserParameters.PNG "Kasutaja parameetrite dialoogiakna kuvatõmmis")

### <a name="add-a-new-baseline-for-designed-er-format"></a>Uue alusfaili lisamine kujundatud elektroonilise aruande vormingu jaoks

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Toimingupaanil valige nupp **Alused**.

    ![Nupp Algväärtused konfiguratsioonide lehel](media/GER-BaselineSample-OpenBaselinePage.PNG "Kuvatõmmis nupust Algväärtused konfiguratsioonide lehel")

3. Valige toimingupaanil nupp **Uus**.
4. Valige varem loodud elektroonilise aruandluse vorming **Vorming elektroonilise aruandluse aluste õppimiseks**.
5. Valige käsk **Salvesta**.

![Elektroonilise aruandluse vormingu aluste leht](media/GER-BaselineSample-AddBaseline.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")

Alus lisatakse vormingule **Vorming elektroonilise aruandluse aluste õppimiseks**.

### <a name="configure-a-baseline-rule-for-the-added-baseline"></a>Alusreegli konfigureerimine lisatud aluse jaoks

1. Lehel **Elektroonilise aruandluse vormingu alused** valige toimingupaanil nupp **Manused** (kirjaklambrisümbol).
2. Toimingupaanil valige suvandid **Uus** \> **Fail**. Elektroonilise aruandluse parameetrites peab olema varem valitud dokumendi tüüp **Fail** dokumendi tüübiks, mida kasutatakse alusfailide salvestamiseks.
3. Valige nupp **Sirvi** ja valige fail **out.Admin.xml**, mis loodi varem konfigureeritud elektroonilise aruandluse vormingut käitades.

    ![Manuste leht](media/GER-BaselineSample-UploadBaselineFile.PNG "Manuste lehe kuvatõmmis")

4. Sulgege leht **Manused**.
5. Kiirkaardil **Alused** valige suvand **Uus**.
6. Väljale **Nimi** sisestage **Alus 1**.
7. Väljale **Faili komponendi nimi** sisestage suvand **Väljund** või valige see. See väärtus näitab, et konfigureeritud alust võrreldakse failiga, mis loodi vorminguelementi **Väljund** kasutades.
8. Sisestage väljale **Failinime mask** väärtus **\*.xml**.

    > [!NOTE]
    > Failinime maski saab määratleda. Kui failinime mask on määratletud, kasutatakse aluskirjet loodud väljundi hindamiseks ainult siis, kui loodud väljundfaili nimi vastab maskile.

9. Kui konfigureeritud alust tuleb kasutada ainult siis, kui elektroonilise aruandluse vormingu **Vorming elektroonilise aruandluse aluste õppimiseks** käitavad kasutajad, kes on sisse logitud konkreetsetesse ettevõtetesse, valige need ettevõtted väljas **Ettevõtted**.
10. Väljale **Alus** sisestage manus **out.Admin** või valige see.
11. Valige käsk **Salvesta**.

![Elektroonilise aruandluse vormingu aluste leht](media/GER-BaselineSample-SetupBaselineLine.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kujundatud elektroonilise aruandluse vormingu käitamine ja logi ülevaatamine tulemuste analüüsimiseks

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel** ja valige suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.
3. Kiirkaardil **Versioonid** valige käsk **Käivita**.
4. Sisestage väljale **Sisestage ID** väärtus **1**.
5. Valige nupp **OK**.
6. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsiooni silumislogid**.

    ![Elektroonilise aruandluse käitamise logide leht](media/GER-BaselineSample-ReviewBaselineComparison1.PNG "Elektroonilise aruandluse käitamise logide lehe kuvatõmmis")

    > [!NOTE]
    > Käivituslogi sisaldab teavet loodud faili ja konfigureeritud aluse võrdluse tulemusi. Selles näites näitab logi, et loodud fail ja alus on võrdsed.

7. Valige käsk **Kustuta kõik**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kujundatud elektroonilise aruandluse vormingu käitamine ja logi ülevaatamine tulemuste analüüsimiseks

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel** ja valige suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.
3. Kiirkaardil **Versioonid** valige käsk **Käivita**.
4. Sisestage väljale **Sisestage ID** väärtus **2**.
5. Valige nupp **OK**.
6. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsiooni silumislogid**.

    ![Elektroonilise aruandluse käitamise logide leht](media/GER-BaselineSample-ReviewBaselineComparison2.PNG "Elektroonilise aruandluse käitamise logide lehe kuvatõmmis")

    > [!NOTE]
    > Käivituslogi sisaldab teavet loodud faili ja konfigureeritud aluse võrdluse tulemusi. Selles näites näitab logi, et loodud fail ja alus on erinevad.

7. Valige käsk **Võrdle**.

> [!NOTE]
> Loodud faili ja alusfaili pakutakse ZIP-failina. Võite failide võrdlemiseks ja erinevuste ülevaatamiseks kasutada välist võrdlustööriista, nt WinDiff.

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse (ER) raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]