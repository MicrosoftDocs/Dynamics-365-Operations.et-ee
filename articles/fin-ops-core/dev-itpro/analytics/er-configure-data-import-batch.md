---
title: Partiirežiimis käsitsi valitud failidest andmete importimine
description: See artikkel selgitab, kuidas importida andmeid käsitsi valitud failidest pakkrežiimis.
author: NickSelin
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERImportFormatSourceTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: Release 10.0.25
ms.openlocfilehash: 2dec838439876fd8e57ea4a7078d97267e5ea1a2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890179"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Partiirežiimis käsitsi valitud failidest andmete importimine

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Elektroonilise aruandluse [(ER)](general-electronic-reporting.md) raamistiku kasutamiseks andmete importimiseks käsitsi valitud sissetulevatest failidest pakett-režiimis, konfigureerige importimist toetav ER-vorming [...](er-overview-components.md#format-component). Seejärel käivitage [mudeli vastendamine](er-overview-components.md#model-mapping-component) tüübiga **Sihtkoht**, mis kasutab seda vormingut andmeallikana. Andmete importimiseks sirvige failini, mida soovite importida ja valige see käsitsi. 

Uus ER-i võimalus, mis toetab andmete importimist pakett-režiimis, võimaldab seda protsessi konfigureerida kui "unattended". Saate kasutada ER-i konfiguratsioone andmete importimiseks, planeerides uue pakett-töö ER-i kasutajaliidesest (UI).

See artikkel selgitab, kuidas lõpetada andmete importimist partiirežiimis käsitsi valitud failist. Näidetes on kasutatud äriandmetena hankija kandeid. Nende näidete sammud saab USMF-ettevõttes **lõpule** viia. Koodi pole vaja kirjutada.

## <a name="prerequisites"></a>Eeltingimused

Selle artikli näidete lõpetamiseks peab teil olema järgmine juurdepääs:

- Üks järgmistest rollidest:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- 1099-maksete ER-vorming ja mudeli konfiguratsioonid

### <a name="create-the-required-er-configurations"></a>Vajalike ER-i konfiguratsioonide loomine

Nõutud ER-i konfiguratsioonide loomiseks ja muude eeltingimuste hankimiseks järgige ühte järgmistest sammudest.

- Vaadake tegevusjuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**. Need ülesandejuhendid selgitavad teile ER-i konfiguratsioonide kujundamise ja kasutamise protsessi, mis interaktiivselt impordivad hankijakandeid failidest Microsoft Excel. Lisateavet vt [Sissetulevate dokumentide sõelumine Exceli vormingus](parse-incoming-documents-excel.md).
- Viige näited lõpule käsku Andmete [importimise konfigureerimine asukohast SharePoint](er-configure-data-import-sharepoint.md). Need näited selgitavad teile ER-i konfiguratsioonide kujundamise ja kasutamise protsessi, mis interaktiivselt impordivad hankijakandeid Exceli failidest, mis on kausta SharePoint salvestatud.

### <a name="download-the-required-er-configurations"></a>Laadi nõutavad ER-i konfiguratsioonid alla

1. Laadige alla järgmised ER-i konfiguratsioonid ja salvestage need kohalikult.

    | Sisu kirjeldus | Fail |
    |---------------------|------|
    | **1099 Maksete mudeli** ER andmemudeli konfiguratsioon | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Hankijakannete importimiseks (Excel) ER-vormingu** konfiguratsioon | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. Kasutage valikut [Laadi XML-faili](er-defer-sequence-element.md#import-the-sample-er-configurations) ER-ist allalaaditud ER-i konfiguratsioonide importida oma Dynamics 365 finantside eksemplari järgmises järjekorras:

    1. ER-i andmemudeli konfiguratsioon
    2. Elektroonilise aruandluse vormingu konfiguratsioon

### <a name="download-the-required-excel-files"></a>Laadige alla nõutavad Exceli failid

- Laadige alla järgmine näidisandmekomplekt ja salvestage see kohalikult.

    | Sisu kirjeldus | Fail |
    |---------------------|------|
    | Sissetulev **1099import-data.xlsx fail**, mis sisaldab importimiseks näidisandmeid | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Eeltingimuste ülevaatamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. **Vaadake konfiguratsioonide lehel** pakkrežiimis andmete importimiseks ettevalmistatud ER-lahendus üle.
3. Vaadake üle **hankijakannete (Exceli)** vormingu konfiguratsiooni importimiseks.

    - Selle konfiguratsiooni vormingu komponent on loodud sõeluma sissetulevat Exceli faili.
    - Selle konfiguratsiooni mudeli vastendamise komponenti kasutatakse põhiandmete mudeli täitmiseks sõelutud Exceli failist pärit andmete abil.

    ![ER-vormingu konfiguratsioon andmete importimiseks ER-i kasutajaliidesest pakett-režiimis.](./media/er-configure-data-import-batch-configurations-1.png)

4. Vaadake üle **1099-maksete mudeli andmemudeli** konfiguratsioon.

    - Selle konfiguratsiooni mudelikomponent esindab andmemudeli struktuuri, mida kasutatakse andmete läbimiseks käitatud ER-i komponentide vahel.
    - Selle konfiguratsiooni mudeli vastendamise komponenti kasutatakse andmete tõmbamiseks täidetud vormingu komponendist ja seejärel rakendustabelite uuendamiseks.

    ![ER-andmemudeli konfiguratsioon andmete importimiseks ER-i kasutajaliidesest pakett-režiimis.](./media/er-configure-data-import-batch-configurations-2.png)

5. Avage Exceli **fail 1099import-data.xlsx**.

    ![Exceli näidisfail andmetega impordiks pakett-režiimis.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>Partiiandmete importimise lubamine ER-i jaoks kasutajaliidesest

1. Minge jaotisse **Süsteemihaldus** \> **Tööruumid** \> **Funktsioonihaldus**.
2. Funktsioonihalduse **tööruumis** valige pakett-töös **käsitsi üleslaaditud dokumentide ER-i** importimine pakett-tööna ja seejärel valige luba **kohe**.

## <a name="import-data-from-manually-selected-excel-files"></a>Andmete importimine käsitsi valitud Exceli failidest

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. **Lehel Konfiguratsioonid** valige **1099 Maksete mudeli andmemudeli** konfiguratsioon.
3. **Valige konfiguratsiooni komponentide** kiirkaardil link **1099 käsitsi kannete importimiseks**.
4. Mudeli ja **andmeallika vastendamise lehel** on **1099 käsitsi kannete impordimudeli** vastendamine eelnevalt valitud. Valige käsk **Käitus**.
5. **Valige vahekaardil Parameetrid** suvand **Sirvi**. Otsige ja valige **fail 1099import-data.xlsx** ning seejärel valige **OK**.
6. Sisestage **väljale Kande ID** väärtus **V-00001**.
7. Seadke vahekaardil **Käivita taustal valiku** Pakktöötlus **väärtuseks** **Jah**.

    Pange tähele **, et ülesande** kirjelduse väli on **seatud käitama mudeli vastendust "1099 käsitsi kannete importimiseks", konfiguratsioonile '1099 Maksete mudel'**. See väärtus näitab, et valitud mudeli vastendamise käivitamine planeeritakse uue pakett-tööna.

    ![Andmete importimise üksikasjade määramine pakett-režiimis elektroonilise aruande parameetrite dialoogiboksis](./media/er-configure-data-import-batch-execution-parameters.png)

8. Valige nupp **OK**. Teade teavitab teid, et uus pakett-töö on planeeritud.

    ![Teade uue plaanitud pakett-töö kohta lehel Mudeli andmeallika vastendamine](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Vaadake andmete importimise tulemused üle pakett-töö lehel.

1. Avage jaotis **Üldine** \> **Päringud** \> **Pakett-tööd** \> **Minu pakett-tööd**.
2. Pakett-tööde **lehel** filtreerige pakett-tööde loend, et leida planeeritud pakett-töö, ja seejärel valige see.
3. Valige töö **üksikasjade ülevaatamiseks töö ID** link.
4. Valige pakett-tööde **kiirkaardil** logi **·**.

    ![Pakett-töö lehel logimisnupp.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Vaadake käivitamise üksikasjad üle.

    ![Plaanitud pakett-töö käivitamislogi pakett-töö lehel.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Muuda andmete importimise parameetreid

Pärast seda, kui teie partii on plaanitud ja seda pole veel käitatud, saate muuta planeeritud andmete importimise parameetreid.

1. Avage jaotis **Üldine** \> **Päringud** \> **Pakett-tööd** \> **Minu pakett-tööd**.
2. Pakett-tööde **lehel** filtreerige pakett-tööde loend, et leida planeeritud pakett-töö, ja seejärel valige see.
3. Valige käsk **Muuda olekut**.
4. Dialoogiaknas **Vali uus** olek valige Kinni **pidada ja** seejärel valige **OK**.
5. Valige töö **üksikasjadele juurdepääsemiseks töö ID** link.
6. Valige pakett-tööde **kiirkaardil** parameetrid **·**.
7. Dialoogiaknas **Elektroonilise aruande parameetrid** järgige neid samme.

    1. Valige **Sirvi**, et valida andmete importimiseks alternatiivfail.
    2. Hankijakannete **importimiseks kande** numbri muutmiseks valige käsk Sisesta kande ID.

        ![Planeeritud pakett-töö andmete importimise parameetrite muutmine elektroonilise aruande parameetrite dialoogiaknas.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Valige nupp **OK**.

8. Kontrollige, kas partii on endiselt valitud, ja valige seejärel uuesti **olek** Muuda olekut.
9. Dialoogiboksis Vali **uus olek** valige Ootel **ja** seejärel valige **OK**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Andmete importimise tulemuste ülevaatamine ER-i lähtelehel

1. Minge organisatsiooni **halduse elektroonilise** \> **aruandluse elektroonilise** \> **aruandluse allika juurde**.
2. Valige andmete **importimise ajal automaatselt loodud hankijakannete (Exceli)** kirje.

    ![Hankijakannete (Exceli) konfiguratsiooni importimise kirje elektroonilise aruandluse lähtelehel](./media/er-configure-data-import-batch-files-source-1.png)

3. Valige **allikatest faili asukohad**.
4. Impordi vormingu **kiirkaartide** **failides ja allikalogides** vaadake impordi üksikasjad üle.
5. **Valige failide** kiirkaardil kirje. Pange tähele, et imporditud fail on selle kirjega seotud.

    ![Imporditud fail, mis on lisatud allikate lehel olevale failis olevale kirjele](./media/er-configure-data-import-batch-files-source-2.png)

6. Valige **manused** imporditud faili ülevaatamiseks.

    ![Dokumendi kuvalehel imporditud fail.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Manuste säilitamiseks kasutab ER-raamistik [...](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents)**dokumenditüüpi**, mis on määratud praegusele ettevõttele ER-parameetrite väljal Muud.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>1099-lehe hankija tasakaalustuse andmete imporditulemuste ülevaade

1. Minge **ostureskontro** \> **perioodiliste ülesannete** \> **maksu 1099 hankija** \> **tasakaalustuse 1099-dele.**
2. Väljale Kuupäevast **sisestage** **31/12/2017** (31. detsember 2017).
3. Valige **käsitsi 1099-kanded**.

    ![Imporditud hankijakanded maksu 1099 kannete lehel.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
