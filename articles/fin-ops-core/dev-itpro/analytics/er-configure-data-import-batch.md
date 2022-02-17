---
title: Andmete importimine käsitsi valitud failidest partiirežiimis
description: Selles teemas selgitatakse, kuidas importida andmeid käsitsi valitud failidest partiirežiimis.
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
ms.openlocfilehash: 8615b5a0623fd696c64f4ec03e481a2bcb16c0ac
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075742"
---
# <a name="import-data-from-manually-selected-files-in-batch-mode"></a>Andmete importimine käsitsi valitud failidest partiirežiimis

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Elektroonilise aruandluse (ER) raamistiku kasutamiseks [andmete importimiseks käsitsi valitud sissetulevatest failidest partiirežiimis konfigureerige importi toetav ER-vorming](general-electronic-reporting.md)[.](er-overview-components.md#format-component) Seejärel käivitage [tüübi sihtkohta](er-overview-components.md#model-mapping-component) mudelivastendus **·**, mis kasutab seda vormingut andmeallikana. Andmete importimiseks sirvige failini, mida soovite importida, ja valige need käsitsi. 

Uus ER-i võimalus, mis toetab andmete importimist partiirežiimis, võimaldab seda protsessi konfigureerida järelevalveta. Andmeimpordi tegemiseks saate kasutada ER-i konfiguratsioone, planeerides uue pakett-töö ER-i kasutajaliidesest (UI).

Selles teemas selgitatakse, kuidas käsitsi valitud failist partiirežiimis andmete importimist lõpule viia. Näidetes on kasutatud äriandmetena hankija kandeid. Nende näidete samme saab täita USMF-i **ettevõttes**. Koodi pole vaja kirjutada.

## <a name="prerequisites"></a>Eeltingimused

Selles teemas näidete lõpuleviimiseks peavad teil olema järgmised juurdepääsuõigused.

- Üks järgmistest rollidest:

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- ER-vorming ja mudeli konfiguratsioonid 1099 maksete jaoks

### <a name="create-the-required-er-configurations"></a>Vajalike ER-konfiguratsioonide loomine

Vajalike ER-konfiguratsioonide loomiseks ja muude eeltingimuste saamiseks tehke järgmist.

- Vaadake tegevusjuhiseid **Elektrooniline aruandlus: andmete importimine Microsoft Exceli failist**, mis on osa äriprotsessist **7.5.4.3 IT-teenuse/-lahenduse komponentide hankimine/arendamine (10677)**. Need ülesandejuhendid selgitavad teile ER-i konfiguratsioonide kujundamise ja kasutamise protsessi, mis interaktiivselt impordivad hankijakandeid failidest Microsoft Excel. Lisateavet vt [Sissetulevate dokumentide sõelumine Exceli vormingus](parse-incoming-documents-excel.md).
- Täitke näited jaotises [Andmete importimise konfigureerimine rakendusest SharePoint](er-configure-data-import-sharepoint.md). Need näited selgitavad teile ER-i konfiguratsioonide kujundamise ja kasutamise protsessi, mis interaktiivselt impordivad hankijakandeid kausta salvestatud SharePoint Exceli failidest.

### <a name="download-the-required-er-configurations"></a>Vajalike ER-konfiguratsioonide allalaadimine

1. Laadige alla järgmised ER-i konfiguratsioonid ja salvestage need kohapeal.

    | Sisu kirjeldus | Fail |
    |---------------------|------|
    | **1099 Maksete mudeli** ER andmemudeli konfiguratsioon | [1099model.xml](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml) |
    | **Hankijate kannete importimiseks (Excel)** ER-vormingu konfiguratsioon | [1099format-import-from-excel.xml](https://download.microsoft.com/download/b/3/8/b38faf0a-fbaf-4e9e-84c2-dedae7464880/1099format-import-from-excel.xml) |

2. [Kasutage suvandit Laadi XML-failist](er-defer-sequence-element.md#import-the-sample-er-configurations) ER allalaaditud ER-i konfiguratsioonide importimiseks oma eksemplari Dynamics 365 Finance järgmises järjekorras.

    1. ER-i andmemudeli konfiguratsioon
    2. Elektroonilise aruandluse vormingu konfiguratsioon

### <a name="download-the-required-excel-files"></a>Vajalike Exceli failide allalaadimine

- Laadige alla järgmine näidisandmekogumik ja salvestage see kohapeal.

    | Sisu kirjeldus | Fail |
    |---------------------|------|
    | Sissetulev **1099import-data.xlsx fail,** mis sisaldab importimiseks näidisandmeid | [1099import-data.xlsx](https://download.microsoft.com/download/f/f/4/ff4dbce9-8364-4391-adee-877945ff01f7/1099import-data.xlsx) |

### <a name="review-the-prerequisites"></a>Eeltingimuste ülevaatamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. **Vaadake lehel Konfiguratsioonid üle ettevalmistatud** ER-lahendus andmete importimiseks partiirežiimis.
3. **Vaadake üle hankijate kannete importimise (Exceli)** vormingu konfiguratsioon.

    - Selle konfiguratsiooni vormingukomponent on mõeldud sissetuleva Exceli faili sõelumiseks.
    - Selle konfiguratsiooni mudelivastenduse komponenti kasutatakse põhiandmemudeli täitmiseks sõelutud Exceli faili andmete abil.

    ![ER-vormingu konfiguratsioon andmete importimiseks partiirežiimis ER-kasutajaliidesest.](./media/er-configure-data-import-batch-configurations-1.png)

4. **Vaadake üle 1099 Maksete mudeli** andmemudeli konfiguratsioon.

    - Selle konfiguratsiooni mudelikomponent esindab andmemudeli struktuuri, mida kasutatakse andmete edastamiseks töötavate ER-komponentide vahel.
    - Selle konfiguratsiooni mudelivastenduse komponenti kasutatakse andmete tõmbamiseks käivitatud vormingu komponendist ja seejärel rakendustabelite värskendamiseks.

    ![ER-andmemudeli konfiguratsioon andmete importimiseks partiirežiimis ER kasutajaliidesest.](./media/er-configure-data-import-batch-configurations-2.png)

5. Avage Excelis **1099iimport-data.xlsx** fail.

    ![Exceli faili näidis koos andmetega importimiseks partiirežiimis.](./media/er-configure-data-import-batch-excel-content.png)

## <a name="enable-batch-data-import-for-er-from-the-ui"></a>ER-i partiiandmete importimise lubamine kasutajaliidesest

1. Minge jaotisse **Süsteemihaldus** \> **Tööruumid** \> **Funktsioonihaldus**.
2. **Valige** tööruumis Funktsioonihaldus **käsitsi üleslaaditud dokumentide importimine partiifunktsioonis** ja seejärel valige **Luba kohe**.

## <a name="import-data-from-manually-selected-excel-files"></a>Andmete importimine käsitsi valitud Exceli failidest

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. **Valige** lehel Konfiguratsioonid **1099-i maksemudeli** andmemudeli konfiguratsioon.
3. Valige kiirkaardil **Konfiguratsiooni komponendid** link 1099 käsitsikannete impordi jaoks **.**
4. **Lehel** Mudel andmeallikate vastendamine **on eelvalikul 1099 käsitsikannete impordimudeli** vastendamine. Valige käsk **Käitus**.
5. Klõpsake **menüüs Parameetrid** nuppu **Sirvi**. Otsige üles ja valige **fail 1099import-data.xlsx** ja seejärel valige **OK**.
6. Sisestage väljale **Sisesta** kande ID **tekst V-00001**.
7. **Seadke** vahekaardil Käivita taustal **suvand Partii töötlemine** valikuks **Jah**.

    Pange tähele, et **välja Ülesande kirjeldus** on seatud mudeli vastendamise käivitamiseks **"1099 käsitsikannete importimiseks", konfiguratsioonile "1099 Maksete mudel"**. See väärtus näitab, et valitud mudelivastenduse käivitamine plaanitakse uue pakett-tööna.

    ![Andmeimporti üksikasjade määramine pakett-režiimis dialoogiboksis Elektroonilised aruandeparameetrid.](./media/er-configure-data-import-batch-execution-parameters.png)

8. Valige nupp **OK**. Teade teavitab teid, et uus pakett-töö on ajastatud.

    ![Sõnum uue ajastatud pakktöö kohta mudeli ja andmeallika vastendamise lehel.](./media/er-configure-data-import-batch-scheduled-job-info.png)

## <a name="review-the-data-import-results-on-the-batch-job-page"></a>Vaadake andmete importimise tulemused lehel Paketttöö

1. Avage jaotis **Üldine** \> **Päringud** \> **Pakett-tööd** \> **Minu pakett-tööd**.
2. peal **Partiitöö** lehel, filtreerige ajastatud partii leidmiseks paketttööde loend ja seejärel valige see.
3. Valige **Töö ID** link töö üksikasjade ülevaatamiseks.
4. peal **Pakettülesanded** FastTab, valige **Logi sisse**.

    ![Logi nupp paketttöö lehel.](./media/er-configure-data-import-batch-scheduled-job-record.png)

5. Vaadake üle täitmise üksikasjad.

    ![Ajastatud paketttöö täitmislogi lehel Paketttöö.](./media/er-configure-data-import-batch-scheduled-job-log.png)

## <a name="change-the-data-import-parameters"></a>Muutke andmete impordi parameetreid

Kui teie partii on ajastatud ja seda pole veel käivitatud, saate ajastatud andmete importimise parameetreid muuta.

1. Avage jaotis **Üldine** \> **Päringud** \> **Pakett-tööd** \> **Minu pakett-tööd**.
2. peal **Partiitöö** lehel, filtreerige ajastatud partii leidmiseks paketttööde loend ja seejärel valige see.
3. Valige käsk **Muuda olekut**.
4. Aastal **Valige uus olek** dialoogiboksis valige **Hoia kinni** ja seejärel valige **Okei**.
5. Valige **Töö ID** link töö üksikasjadele juurdepääsuks.
6. peal **Pakettülesanded** FastTab, valige **Parameetrid**.
7. Aastal **Elektroonilise aruande parameetrid** dialoogiboksis järgige neid samme:

    1. Valige **Sirvige** et valida andmete importimiseks alternatiivne fail.
    2. Valige **Sisesta vautšeri ID** hankija tehingute importimise vautšeri numbri muutmiseks.

        ![Ajastatud pakktöö andmete importimise parameetrite muutmine dialoogiboksis Elektroonilise aruande parameetrid.](./media/er-configure-data-import-batch-scheduled-job-parameters.png)

    3. Valige nupp **OK**.

8. Veenduge, et partii on endiselt valitud, ja seejärel valige **Muuda olekut** uuesti.
9. Aastal **Valige uus olek** dialoogiboksis valige **Ootan** ja seejärel valige **Okei**.

## <a name="review-the-data-import-results-on-the-er-source-page"></a>Vaadake andmete importimise tulemused üle ER-i lähtelehel

1. Minema **Organisatsiooni administreerimine** \> **Elektrooniline aruandlus** \> **Elektrooniline aruandlusallikas**.
2. Valige **Müüjate tehingute importimiseks (Excel)** kirje, mis loodi andmete importimise käigus automaatselt.

    ![Kirje elektroonilise aruandluse allika lehel oleva konfiguratsiooni Hankijate tehingute importimiseks (Excel) jaoks.](./media/er-configure-data-import-batch-files-source-1.png)

3. Valige **Allikate failiolekud**.
4. peal **Failid** ja **Impordivormingu lähtelogid** FastTabs, vaadake üle impordi üksikasjad.
5. peal **Failid** FastTab, valige kirje. Pange tähele, et imporditud fail on lisatud sellele kirjele.

    ![Imporditud fail, mis on lisatud kirjele allikate lehel Faili olekud.](./media/er-configure-data-import-batch-files-source-2.png)

6. Valige **Manused** imporditud faili ülevaatamiseks.

    ![Imporditud fail lehel Dokumendivaade.](./media/er-configure-data-import-batch-files-source-3.png)

    > [!TIP]
    > Nende manuste säilitamiseks kasutab ER-i raamistik dokumenditüüpi, mis on [seatud](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) praeguse ettevõtte jaoks **teised** ER parameetrite väljale.

## <a name="review-the-data-import-results-on-the-vendor-settlement-for-1099s-page"></a>Vaadake üle andmete importimise tulemused lehel Tarnija arveldus 1099s

1. Minema **Makstavad arved** \> **Perioodilised ülesanded** \> **Maksud 1099** \> **Müüja arveldus 1099s**.
2. Aastal **Kuupäevast** väljale, sisestage **31.12.2017** (31. detsember 2017).
3. Valige **Käsitsi 1099 tehingut**.

    ![Imporditud hankija tehingud lehel Tax 1099 tehingud.](./media/er-configure-data-import-batch-imported-data.png)

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
