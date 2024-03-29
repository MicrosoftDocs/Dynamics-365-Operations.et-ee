---
title: Loodud ER-aruannete ja võrdluste alusväärtuste abil jälgimise tulemuste täiustused
description: See artikkel kirjeldab ER-i Microsoft Dynamics põhifunktsiooni parendusi versioonis 365 Finantsversioon 10.0.3 (juuni 2019).
author: kfend
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.openlocfilehash: d0f64c459ee72ffa2b0e540d4194ca887502780f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279056"
---
# <a name="improve-tracing-the-results-of-generated-er-reports-to-compare-with-baseline-values"></a>Loodud ER-aruannete ja võrdluste alusväärtuste abil jälgimise tulemuste täiustused

[!include[banner](../includes/banner.md)]

See artikkel kirjeldab esimest parenduste kogum, mis on tehtud elektroonilise aruandluse (ER) raamistiku põhifunktsioonile. Need parendused on saadaval Microsoft Dynamics versioonis 365 Finance 10.0.3 (juuni 2019) ja hilisemas versioonis.

## <a name="automate-the-setting-of-baseline-rules"></a>Alusreeglite seadistamise automatiseerimine

Jälitus [genereeritud aruande tulemused ja](er-trace-reports-compare-baseline.md) võrrelge neid alusväärtuste artikliga selgitab, kuidas konfigureerida ER-raamistikku, et koguda teavet ER-vormingu käivitamiste kohta ja hinnata nende käivitamiste tulemusi. Selles artiklis toodud näites kuvatakse sammud, mis tuleb lõpule viia.

Siin on mõned neist etappidest.

- Käivitage elektroonilise aruandluse vorming väljamineva faili loomiseks ja salvestage fail lokaalselt.
- Lisage lokaalselt salvestatud fail manusena alusele, mis lisati elektroonilise aruandluse vormingu jaoks.
- Konfigureerige alusreeglit lisatud aluse jaoks. See konfiguratsioon sisaldab järgmisi etappe.

    - Määrake elektroonilise aruandluse vormingu element, mida kasutatakse väljamineva faili loomiseks.
    - Valige manus, mis viitab loodud väljaminevale failile.

> [!NOTE]
> Need sammud tuleb läbida käsitsi, kuigi elektroonilise aruandluse uute võimalustega on neid võimalik automatiseerida. Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.

## <a name="example-automate-the-setting-of-baseline-rules"></a>Näide. Alusreeglite seadistamise automatiseerimine

Selle näite [sammude lõpuleviimiseks peate esmalt täitma sammud näites Jälgi](er-trace-reports-compare-baseline.md) loodud aruandesse ja võrdlema neid alusväärtuste artikliga, mis asub jaotises "Lisa loodud ER-vormingu jaoks uus alusjoon".

### <a name="review-added-baseline"></a>Lisatud aluse ülevaatamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige suvand **Alused**.

    > [!NOTE]
    > Nupp **Alused** toimingupaanil on saadaval vaid siis, kui elektroonilise aruandluse kasutaja parameeter **Käivita silumisrežiimis** on praeguse ettevõtte jaoks sisse lülitatud.

Alus on lisatud valitud vormingu **Vorming elektroonilise aruandluse aluste õppimiseks** jaoks, aga alusreegleid pole veel selle aluse jaoks lisatud.

![Elektroonilise aruandluse vormingu aluste leht, reegleid veel pole.](media/GER-BaselineSample-AddBaseline2.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")

### <a name="make-a-new-baseline-rule"></a>Uue alusreegli tegemine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel**.
3. Valige puus suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.
4. Kiirkaardil **Versioonid** valige käsk **Käivita**.
5. Sisestage väljale **Sisestage ID** väärtus **1**.
6. Määrake suvand **Alusfailide tegemine** valikule **Jah**.
7. Valige nupp **OK**.
8. Valige suvand **Alused**.

    ![Elektroonilise aruandluse vormingu alusleht, alusväärtused on valitud.](media/GER-BaselineSample-ReviewAddedBaselineLine.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")

    Loodud väljaminev fail manustatakse automaatselt käivitatud elektroonilise aruandluse vormingu alusele. Alusreegel on sellele alusele automaatselt lisatud ja sisaldab ka viidet manustatud failile.

9. Väljale **Nimi** sisestage **Alus 1**.
10. Sisestage väljale **Failinime mask** väärtus **.xml**.
11. Valige käsk **Salvesta**.

### <a name="run-the-format"></a>Vormingu käivitamine

Olete nüüd [valmis](er-trace-reports-compare-baseline.md) täitma näites Jälitus loodud aruande ülejäänud etappe ja võrdlema neid alusväärtuste artikliga, alustades jaotisest "Käivita kujundatud ER-vorming ja vaadake logi tulemuste analüüsimiseks üle".

> [!NOTE]
> Kui kustutate automaatselt lisatud alusreegli kiirkaardilt **Alused**, ei kustutata viidatud manust automaatselt.

## <a name="configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Aluse konfigureerimine nii, et see eiraks elektroonilise aruandluse väljundi pidevalt muutuvaid osasid

Kui elektroonilise aruandluse vorming on kujundatud sisaldama teavet, mis muutub vormingu käivitamisel, peab vormingul olema kohustus kasutada elektroonilise aruandluse alusfunktsiooni loodud tulemuste võrdlemiseks alusväärtustega. Näiteks võib teave olla töötlemiskuupäev ja -kellaaeg või eri vormingutes loodud dokumendi kordumatu ID (globaalne ainuidentifikaator \[GUID\] jne). Elektroonilise aruandluse uue võimalusega saate konfigureerida alusreeglit nii, et see eirab elektroonilise aruandluse vormingu muudetavaid elemente, kui vormingut käivitatakse eesmärgiga võrrelda alusväärtusi vormingu käivitamise tulemustega. Lisateabe saamiseks selle funktsiooni kohta läbige järgmine näide.

## <a name="example-configure-the-baseline-so-that-it-ignores-constantly-changing-parts-of-the-er-output"></a>Näide. Aluse konfigureerimine nii, et see eiraks elektroonilise aruandluse väljundi pidevalt muutuvaid osasid

Selle näite sammude lõpuleviimiseks peate esmalt täitma [sammud näites Jälitus loodud aruande tulemused ja võrdlema neid põhiväärtuste artikliga](er-trace-reports-compare-baseline.md).

### <a name="modify-a-configured-er-format"></a>Konfigureeritud elektroonilise aruandluse vormingu muutmine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel**.
3. Valige puus suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.
4. Valige **Kujundaja**.
5. Valige puul suvand **Väljund\\Dokument**.
6. Valige **Lisa**.
7. Dialoogiakna ripploendist puul valige suvandid **XML\\Atribuut**.
8. Välja **Nimi** sisestage väärtus **ProcessingDateTime**.
9. Valige nupp **OK**.
10. Vahekaardilt **Vastendamine** puul valige suvandid **Väljund\\Dokument\\ProcessingDateTime**.
11. Valige **Valemi redigeerimine**.
12. Sisestage väljale **Valem** järgmine avaldis: **DATETIMEFORMAT(NOW(), "O")**
13. Valige nupp **Salvesta** ja seejärel suvand **Katse**.
14. Valige uuesti suvand **Katse**, et konfigureeritud avaldist uuesti kontrollida.

    ![Valemikoostaja leht.](media/GER-BaselineSample-DefineProcessingDTExpression.PNG "Valemikoostaja lehe kuvatõmmis")

    > [!NOTE]
    > Vahekaardil **Katsetulemus** näidatakse, et konfigureeritud avaldis annab käivitamisel alati tulemuseks erineva kuupäeva ja kellaaja väärtuse.

15. Sulgege leht **Valemikoostaja** ja valige käsk **Salvesta**.

    ![Vormingukujundaja leht.](media/GER-BaselineSample-FormatMappingDesign2.PNG "Vormingu koostaja lehe kuvatõmmis")

16. Sulgege **Vormingu kujundaja** leht.

### <a name="remove-an-existing-baseline-rule"></a>Olemasoleva alusreegli eemaldamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige suvand **Alused**.
3. Aluste loendist valige alus, mis on konfigureeritud vormingu **Vorming elektroonilise aruandluse aluste õppimiseks** jaoks.
4. Kiirkaardilt **Alused** valige käsk **Kustuta**, et eemaldada varem konfigureeritud alusreegel.

![Elektroonilise aruandluse vormingu aluste leht, kustutatud.](media/GER-BaselineSample-AddBaseline3.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")

### <a name="define-replacements-for-bindings-of-designed-er-format"></a>Kujundatud elektroonilise aruandluse vormingu sidumiste asenduste määratlemine

1. Valige lehel **Konfiguratsioonid** kiirkaardil **Asendused** suvand **Komponentide valimine**.
2. Laiendage Vormingu komponentide puul suvandit **Väljund**, laiendage suvandeid **Väljund\\Dokument** ja seejärel valige suvandi **Väljund\\Dokument\\ProcessingDateTime** märkeruut.
3. Valige nupp **OK**.

![Elektroonilise aruandluse vormingu aluste leht, komponendid.](media/GER-BaselineSample-AddBaseline4.PNG "Elektroonilise aruandluse vormingu aluste lehe kuvatõmmis")

Valitud elektroonilise aruandluse vormingu komponent on lisatud komponentide loendisse kiirkaardil **Asendused**. Kui aluse elektroonilise aruandluse vorming käivitatakse silumisrežiimis, asendatakse vormingu sidumine iga komponendi jaoks veerus **Sidumine** kuvatud sidumisega. Kiirkaardil **Asendused** loendatud komponendi vaikesidumise muutmiseks valige nupp **Redigeeri**.

### <a name="make-a-new-baseline-rule"></a>Uue alusreegli tegemine

Järgige selle artikli varasemas jaotises "Näide: alusreeglite seadistamise automatiseerimine" toodud etappe. Teatis hoiatab teid, et väljaminev fail on loodud, kasutades alussätteid, ja et tekkinud on vormingu sidumiste sundasendamine.

![Teatis lehel Konfiguratsioonid.](media/GER-BaselineSample-FormatRunToMakeBaselineFile4.PNG "Kuvatõmmis teatisest lehel Konfiguratsioonid")

### <a name="suppress-warnings-about-the-replacement-of-format-bindings"></a>Vormingu sidumiste asendamise hoiatuste peitmine

Konkreetsete elektroonilise aruandluse parameetrite seadistamisega saate peita teatiseid, mis annavad hoiatusi vormingu sidumiste asendamise kohta. See võib olla kasulik, kui vormingu sidumised asendatakse järelevalveta režiimis, kasutades tööriista Regression Suite Automation Tool. Sellisel juhul võib hoiatust pidada käimasoleva testjuhtumi tõrkeks.

1. Valige lehe **Konfiguratsioonid** toimingupaani vahekaardilt **Konfiguratsioonid** suvand **Kasutaja parameetrid**.
2. Seadistage suvand **Aluse hoiatuste peitmine** valikule **Jah** ja klõpsake nuppu **OK**.

### <a name="review-the-generated-baseline-file"></a>Vaadake genereeritud alusfail üle.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Valige suvand **Alused**.
3. Valige suvand **Manused**.
    > [!NOTE]
    > Loodud fail sisaldab töötlemise kuupäeva ja kellaaja teksti (**"#"**) sidumisest, mis konfigureeriti lisatud alusreeglis, mitte vormingu sidumisest.
    
4. Sulgege leht **Manused**.

### <a name="run-the-designed-er-format-and-review-the-log-to-analyze-the-results"></a>Kujundatud elektroonilise aruandluse vormingu käitamine ja logi ülevaatamine tulemuste analüüsimiseks

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage puul suvandit **Elektroonilise aruandluse aluste õppimise mudel**.
3. Valige puus suvandid **Elektroonilise aruandluse aluste õppimise mudel\\Vorming elektroonilise aruandluse aluste õppimiseks**.
4. Kiirkaardil **Versioonid** valige käsk **Käivita**.
5. Sisestage väljale **Sisestage ID** väärtus **1**.
6. Valige nupp **OK**.
7. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsiooni silumislogid**.

Käivituslogi sisaldab teavet loodud faili ja konfigureeritud aluse võrdluse tulemusi. Logi näitab, et loodud fail ja alus on võrdsed, kuigi käivitatud vorming sisaldab sidumist pidevalt muutuva kuupäeva ja kellaaja väärtuse sisestamiseks väljaminevasse faili.

> [!NOTE]
> Kuigi väljaminev fail on loodud, kasutades alussätteid, mis käivitavad vormingu sidumiste sundasenduse, ei saa te asendamise kohta hoiatusi.

## <a name="exchange-baseline-settings-between-environments"></a>Alussätete vahetamine keskkondade vahel

### <a name="export-baseline-settings"></a>Alussätete eksportimine

Elektroonilise aruandluse uute võimalustega saate eksportida alussätteid valitud elektroonilise aruandluse vormingu jaoks praegusest keskkonnast ja salvestada need XML-failidena. 

Alussätete eksportimiseks valige lehel **Elektroonilise aruandluse vormingu alused** käsk **Ekspordi**.

### <a name="import-baseline-settings"></a>Impordi alussätted

Eksporditud alussätteid saab importida teise keskkonda. Keskkond tuleb kõigepealt importida elektroonilise aruandluse vorminguna. Seejärel saate importida alussätteid.

Alussätete importimiseks lokaalselt salvestatud XML-failist valige lehel **Elektroonilise aruandluse vormingu alused** käsk **Impordi** ja seejärel käsk **Sirvi**, et valida XML-fail.

![Alussätete importimise dialoogiaken.](media/GER-BaselineSample-ImportBaseline1.PNG "Kuvatõmmis dialoogiaknast Alussätete importimine")

Alussätete importimiseks Microsoft SharePoint Serverisse salvestatud XML-failist praeguste dokumendihalduse sätete ja valitud dokumendi tüübi põhjal valige lehel **Elektroonilise aruandluse vormingu alused** käsk **Impordi allikast**. Seejärel valige dokumendi tüüp ja XML-fail. SharePointi kaustale ligipääsemiseks vajalik dokumendi tüüp peab olema varem konfigureeritud.

![Allikast importimise dialoogiaken.](media/GER-BaselineSample-ImportBaseline2.PNG "Kuvatõmmis dialoogiaknast Allikast importimine")

> [!NOTE]
> Dialoogiaknast **Allikast importimine** vajaliku dokumendi tüübi ja faili nime valimise etappide salvestamiseks saate kasutada tegevuse salvestajat. Nii saate säilitada vajalikke alussätteid SharePointi serveris ja seejärel need automaatselt importida, esitades tegevuse salvestist automaatsete katsete käivitamisel tööriistaga Regression Suite Automation Tool.

## <a name="additional-resources"></a>Lisaressursid

- [Loodud aruandetulemite jälgimine ja nende võrdlemine alusväärtustega](er-trace-reports-compare-baseline.md)
- [Tegevuse salvestaja ressursid](../user-interface/task-recorder.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

