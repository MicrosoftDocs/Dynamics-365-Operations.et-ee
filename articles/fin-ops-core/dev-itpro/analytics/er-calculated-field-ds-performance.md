---
title: Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad
description: See artikkel selgitab, kuidas saate aidata parandada elektroonilise aruandluse (ER) lahenduste jõudlust, lisades parameetrilised ARVUTATUD VÄLJA andmeallikad.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c2c0499ac3d41c9bb6026cc05f971087799c28f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850110"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad

[!include [banner](../includes/banner.md)]

See artikkel [selgitab](trace-execution-er-troubleshoot-perf.md)[, kuidas te saate käitada elektroonilise aruandluse (ER)](general-electronic-reporting.md) vormingute jõudlusjälgi ja **seejärel** kasutada nende jälgede teavet jõudluse parandamiseks, konfigureerides parameetrina arvutatud välja andmeallika.

Üks osa ER-i konfiguratsioonide kujundamisest äridokumentide loomise jaoks on määratleda meetod, mida kasutatakse andmete saamiseks avaldusest, ja sisestada see loodud väljundisse. **Arvutatud välja** tüübi parameeteriseeritud ER-i andmeallika kujundamisega saate vähendada andmebaasi kutsete arvu ning vähendada oluliselt aega ja kulu, mis on seotud ER-i vormingu täitmise üksikasjade kogumisega.

## <a name="prerequisites"></a>Eeltingimused

- Selle artikli näidete lõpuleviimiseks peab teil olema juurdepääs ühele järgmistest [rollidest](../sysadmin/tasks/assign-users-security-roles.md):

    - Elektroonilise aruandluse arendaja
    - Elektroonilise aruandluse funktsionaalne konsultant
    - Süsteemiadministraator

- Ettevõtte sätteks peab olema seatud **DEMF**.
- Järgige selle artikli [lisa 1](#appendix1) samme, et laadida alla microsofti ER-i näidislahenduse komponendid, mis on vajalikud selles artiklis näidete lõpetamiseks.
- Järgige selle [artikli 2](#appendix2) . lisa samme minimaalse ER-parameetrite komplekti konfigureerimiseks, mida on vaja ER-raamistiku kasutamiseks, et parandada Microsoft ER-i näidislahenduse jõudlust.

## <a name="import-the-sample-er-solution"></a>ER-i näidislahenduse importimine

Oletame, et peate kujundama uue ER-i lahenduse, et luua uus hankija kandeid esitav aruanne. Praegu leiate valitud hankija kanded lehel **Hankija kanded** (avage **Ostureskontro** \> **Hankijad** \> **Kõik hankijad**, valige hankija ja seejärel valige toimingupaanil vahekaardi **Hankija** grupis **Kanded** suvand **Kanded**). Kuid teil on vaja, et kõik hankija kanded oleksid samal ajal ühes elektroonilises dokumendis XML-vormingus. See lahendus koosneb mitmest ER-i konfiguratsioonist, mis sisaldavad nõutud andmemudelit, mudeli vastendust ja vormingu komponente.

Esimese etapina tuleb importida ER-i näidislahendus hankija kannete aruande loomiseks.

1. Logige sisse teie ettevõtte jaoks ettesätestatud Microsoft Dynamics 365 Finantside eksemplari.
2. Selles artiklis loote ja muudate konfiguratsioone **Ettevõtte Litware, Inc.** näidisettevõtte jaoks. Veenduge, et see konfiguratsiooni pakkuja oleks teie Finance'i eksemplari lisatud ja on aktiivsena märgitud. Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.
4. Importige lehel **Konfiguratsioonid** ER-i konfiguratsioonid, mille eeltingimusena Finance'i alla laadisite, järgmises järjestuses: andmemudel, mudeli vastendus, vorming. Toimige iga konfiguratsiooni puhul järgmiselt.

    1. Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.
    2. Valige käsk **Sirvi** ja valige ER-i konfiguratsiooni jaoks sobiv fail XML-vormingus.
    3. Valige nupp **OK**.

![Imporditud konfiguratsioonid konfiguratsioonide lehel.](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>ER-i näidislahenduse ülevaatamine

### <a name="review-the-model-mapping"></a>Mudeli vastendamise läbivaatamine

1. Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Jõudlustäiustuse mudel** ja seejärel valige **Jõudlustäiustuse vastendamine**.
2. Valige toimingupaanil valik **Koostaja**.
3. Tehke lehe **Mudelist andmeallikasse vastendamine** tegevuse paanil valik **Kujundaja**.

    See ER-mudeli vastendus on ette nähtud selleks, et teha järgmist.

    - Saate tuua tabelis VendTrans (andmeallikas **Kanded**) talletatud hankija kannete loendi.
    - Iga kande korral tooge tabelist VendTable selle hankija kirje, kelle jaoks kanne on sisestatud (andmeallikas **\#Hankija**).

    > [!NOTE]
    > Andmeallikas **\#Hankija** on konfigureeritud tooma vastavat hankija kirjet, kasutades olemasolevat üks-ühele seost **\@.'\>Relations'.VendTable\_AccountNum**.

    Selle konfiguratsiooni mudeli vastendamine rakendab põhiandmete mudelit selle mudeli jaoks loodud ER-vormingute korral, mida kasutatakse rakenduses Finance. Selle tulemusena on andmeallika **Kanded** sisu avatud ER-vormingute, näiteks abstraktsete **andmemudeli** allikate korral.

    ![Kanded andmeallikas mudeli vastenduse koostaja lehel.](media/er-calculated-field-ds-performance-mapping-1.png)

4. Sulgege leht **Mudelivastenduse kujundaja**.
5. Sulgege leht **Mudelist andmeallikasse vastendamine**.

### <a name="review-format"></a>Läbivaatuse vorming

1. Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Jõudlustäiustuse mudel** ja seejärel valige **Jõudlustäiustuse vorming**.
2. Valige toimingupaanil valik **Koostaja**.
3. Tehke lehe **Vormingu kujundaja** vahekaardil **Vastendamine** valik **Laienda/ahenda**.
4. Laiendage üksusi **Mudel**, **Andmed** ja **Kanne**.

    See ER-vorming on loodud hankija kannete aruande loomiseks XML-vormingus.

    ![Vorminguelementide andmeallikate ja konfigureeritud sidumiste vormindamine vormingu koostaja lehel.](media/er-calculated-field-ds-performance-format.png)

5. Sulgege **Vormingu kujundaja** leht.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Muudetud ER-i näidislahenduse kasutamine täitmise jälituseks

Oletame, et olete lõpetanud ER-i lahenduse esimese versiooni kujundamise. Nüüd soovite lahendust testida oma rakenduse Finance eksemplaris ja analüüsida täitmise jõudlust.

### <a name="turn-on-the-er-performance-trace"></a>ER-i jõudluse jälituse sisselülitamine

1. Valige ettevõte **DEMF**.
2. Järgige teemas [ER-i jõudluse jälituse sisselülitamine](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) toodud juhiseid, et luua jõudluse jälitus ER-vormingu käivitamisel.

    ![Kasutaja parameetrite dialoogiaken.](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>ER-vormingu käivitamine

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vorming**.
3. Valige toimingupaanil käsk **Käivita**.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Jõudluse jälituse kasutamine mudeli vastenduse jõudluse analüüsimiseks

1. Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vastendamine**.
2. Valige toimingupaanil valik **Koostaja**.
3. Tehke lehe **Mudeli vastendused** tegevuse paanil valik **Kujundaja**.
4. Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.
5. Valige viimati loodud jälitus ja seejärel valige **OK**.

Praeguse mudeli vastenduse mõne andmeallika üksuse kohta on kättesaadav uus teave.

- Tegelik aeg, mis kulus andmeallika abil andmete toomisele
- Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu mudelivastenduse käitamise peale

![Käivitamise aja üksikasjad Mudeli vastenduse koostaja lehel.](./media/er-calculated-field-ds-performance-mapping-2.png)

Ruudustik **Jõudluse statistika** näitab, et andmeallikas **Kanded** kutsub tabeli VendTrans ühel korral. Andmeallika **Kanded** väärtus **\[265\]\[Q:265\]** näitab, et avalduse tabelist on toodud 265 hankija kannet ja need on tagastatud andmemudelisse.

Ruudustik **Jõudluse statistika** näitab ka, et praegune mudelivastendus dubleerib andmebaasi taotlusi, samal ajal kui käivitatakse andmeallikas **\#Hankija**. Dubleerimine toimub järgmistel põhjustel.

- Hankija tabelit kutsutakse iga 265 itereeritud hankija kande korral kaks korda; kokku on 530 kutset.

    - Üks kutse tehakse hankija kontonumbri sisestamiseks.
    - Üks kutse tehakse hankija nime sisestamiseks.

- Hankija tabelit kutsutakse iga itereeritud hankija kande korral, kuigi toodud kanded on sisestatud ainult viie hankija kohta. 530 kutsest 525 on duplikaadid. Järgmisel illustratsioonil on kujutatud teade, mis kuvatakse duplikaatkutsete (andmebaasitaotluste) kohta.

![Teade dubleeritud andmebaasi taotluste kohta mudelivastenduse koostaja lehel.](./media/er-calculated-field-ds-performance-mapping-2a.png)

Pange tähele, et mudelivastenduse käivitamise koguajast (ligikaudu kaheksa sekundit) on kulunud rohkem kui 80 protsenti (ligikaudu kuus sekundit) avalduse tabelist VendTable väärtuste toomisele. See protsent on viie hankija kahe atribuudi jaoks liiga suur, võrreldes avalduse tabelist VendTrans pärit andmete mahuga.

Hankija teabe saamiseks iga tehingu kohta tehtud kutsete arvu vähendamiseks ja mudelivastenduse jõudluse parandamiseks saate kasutada andmeallika **\#Hankija** vahemällu salvestamist.

> [!NOTE]
> Andmeallikas **Kanne\\\#Hankija** salvestatakse vahemällu käitusajal andmeallika **Kanne** praeguse kande ulatuses.

Andmeallika **\#Hankija** vahemällu salvestades vähendate dubleeritud kutsete arvu 525-lt 260-le, kuid te ei kõrvalda dubleerimist täielikult. Dubleerimise täielikuks kõrvaldamiseks saate konfigureerida uue parameetritega andmeallika, mille tüüp on **Arvutatud väli**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Mudelivastenduse parandamine täitmise jälitusest saadud teabe põhjal

### <a name="change-the-logic-of-the-model-mapping"></a>Mudelivastenduse loogika muutmine

Järgige järgmisi juhiseid vahemällu salvestamise ja tüübiga **Arvutatud väli** andmeallika kasutamiseks, et vältida andmebaasi duplikaatkutseid.

1. Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vastendamine**.
2. Valige toimingupaanil valik **Koostaja**.
3. Tehke lehe **Mudeli vastendused** tegevuse paanil valik **Kujundaja**.
4. Lehel **Mudelivastenduse koostaja** tehke järgmist, et lisada tüübiga andmeallikas **Tabeli kirjed** avalduse tabeli VendTable kirjetele juurdepääsemiseks.

    1. Laiendage paanil **Andmeallika tüübid** teenust **Dynamics 365 for Operations** ja valige suvand **Tabeli kirjed**.
    2. Valige **Lisa juur**.
    3. Sisestage dialoogiboksis väljale **Nimi** väärtus **Hankija**.
    4. Sisestage väljale **Tabel** väärtus **VendTable**.
    5. Valige nupp **OK**.

5. Tüübiga **Arvutatud väljad** andmeallikate kutsed saate parametriseerida ainult juhul, kui need andmeallikad asuvad konteineris. Seetõttu tehke järgmist, et lisada tüübiga **Tühi konteiner** andmeallikas, et säilitada uus tüübiga **Arvutatud väli** parametriseeritud andmeallikas.

    1. Laiendage paanil **Andmeallika tüübid** suvandit **Üldine** ja valige **Tühi konteiner**.
    2. Valige **Lisa juur**.
    3. Sisestage dialoogiboksis väljale **Nimi** väärtus **Väli**.
    3. Valige nupp **OK**.

    ![Ruudu välja andmeallikas mudeli vastenduse koostaja lehel.](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Tüübiga **Arvutatud väli** parametriseeritud andmeallika lisamiseks tehke järgmist.

    1. Tehke paanil **Andmeallikad** valik **Väli**.
    2. Laiendage paanil **Andmeallika tüübid** üksust **Funktsioonid** ja valige üksus **Arvutatud väli**.
    3. Valige **Lisa**.
    4. Sisestage dialoogiboksis väljale **Nimi** väärtus **Hankija**.
    5. Valige **Valemi redigeerimine**.
    6. Tehke lehel **Valemikoostaja** valik **Parameetrid**, et määrata parameetrid, mis tuleb selle andmeallika kutsumisel esitada.
    7. Tehke dialoogiaknas **Parameetrid** valik **Uus**.
    8. Sisestage väljale **Nimi** väärtus **parmVendAccNumber**.
    9. Valige väljalt **Tüüp** suvand **String**.
    10. Valige nupp **OK**.
    11. Sisestage väljale **Valem** tekst **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Valige **Salvesta** ja sulgege leht **Valemikoostaja**.
    13. Uue andmeallika lisamiseks valige **OK**.

7. Kui soovite, et lisatud andmeallikas oleks käivitamise ajal vahemällu salvestatud, toimige järgmiselt.

    1. Valige paanil **Andmeallikad** suvand **Väli\\Hankija**.
    2. Valige suvand **Vahemälu**.

    > [!NOTE]
    > Andmeallikas **Väli\\Hankija** salvestatakse vahemällu käitusajal andmeallika **Hankija** kõigi hankija kannete ulatuses.

8. Pesastatud andmeallika **Kanne\\\#Hankija** värskendamiseks nii, et see kasutaks andmeallikat **Väli\\Hankija**, tehke järgmist.

    1. Laiendage paanil **Andmeallikad** suvandit **Kanne**.
    2. Valige andmeallikas **Kanne\\\#Hankija** ja seejärel valige **Redigeerimine** \> **Redigeeri valemit**.
    3. Sisestage lehe **Valemikoostaja** väljale **Valem** tekst **Box.Vend(\@.AccountNum)**.
    4. Valige käsk **Salvesta** ja sulgege leht **Valemikoostaja**.
    5. Valitud andmeallika muudatuste lõpuleviimiseks valige **OK**.

9. Valige käsk **Salvesta**.

    ![Hankija andmeallikas mudeli vastenduse koostaja lehel.](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Sulgege leht **Mudelivastenduse kujundaja**.
11. Sulgege leht **Mudelivastendused**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>ER-i mudelivastenduse muudetud versiooni lõpetamine

1. Valige lehe **Konfiguratsioonid** kiirkaardil **Versioonid** konfiguratsiooni **Jõudlustäiustuse vastendamine** versioon **1.2**.
2. Valige **Muuda olekut** \> **Valmis** ja seejärel valige **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Muudetud ER-i lahenduse kasutamine täitmise jälituseks

Korrake selle artikli varasema [ER-vormingu](#run-format) sektsiooni samme uue jõudluse jälituse loomiseks.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Jõudluse jälituse kasutamine mudeli vastenduse korrigeerimiste analüüsimiseks 

1. Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vastendamine**.
2. Valige toimingupaanil valik **Koostaja**.
3. Tehke lehe **Mudeli vastendused** tegevuse paanil valik **Kujundaja**.
4. Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.
5. Valige viimati loodud jälitus ja seejärel valige **OK**.

Pange tähele, et kohandused, mida tegite mudelivastendusele, on eemaldanud dubleeritud päringud andmebaasile. Vähendatud on ka selle mudelivastenduse kutsete arvu andmebaasi tabelitele ja andmeallikatele.

![Kande teave mudeli vastenduse koostaja lehel 1.](./media/er-calculated-field-ds-performance-mapping-5.png)

Täitmisaega on vähendatud umbes 20 korda (umbes 8 sekundilt 400 millisekundini). See on parandanud kogu ER-lahenduse jõudlus.

![Kande teave mudeli vastenduse koostaja lehel 2.](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Lisa 1: laadige alla Microsofti ER-näidislahenduse komponendid

Peate alla laadima ja kohalikult talletama järgmised failid.

| Fail                                        | Sisu |
|---------------------------------------------|---------|
| Jõudlustäiustuse mudel, versioon 1     | [ER-i andmemudeli konfiguratsiooni näide](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Jõudlustäiustuse vastendamine, versioon 1.1 | [ER-i mudelivastenduse konfiguratsiooni näide](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Jõudlustäiustuse vorming, versioon 1.1  | [ER-vormingu konfiguratsiooni näide](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Lisa 2: ER-raamistiku konfigureerimine

Enne kui saate hakata kasutama ER-raamistikku, et parandada Microsofti ER-näidislahenduse jõudlust, peate konfigureerima ER-i parameetrite minimaalse kogumi.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Elektroonilise aruandluse parameetrite konfigureerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Elektroonilise aruandluse parameetrid**.
3. Valige lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** sätteks **Jah**.
4. Vahekaardil **Manused** määrake järgmised parameetrid.

    - Valige väljal **Konfiguratsioonid** tüüp **Fail** ettevõttele **DEMF**.
    - Valige väljadel **Töö arhiiv**, **Ajutine**, **Alus** ja **Muud** tüüp **Fail**.

Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

Kõigile lisatud ER-konfiguratsioonidele on märgitud omanikuks ER-konfiguratsiooni pakkuja. Sel eesmärgil kasutatakse tööruumis **Elektrooniline aruandlus** aktiveeritud ER-konfiguratsiooni pakkujat. Seega enne ER-konfiguratsioonide lisamist või redigeerimist peate aktiveerima tööruumis **Elektrooniline aruandlus** ER-konfiguratsiooni pakkuja.

> [!NOTE]
> ER-konfiguratsiooni saab redigeerida ainult konfiguratsiooni omanik. Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>ER-konfiguratsiooni pakkujate loendi ülevaatamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkuja tabel** on igal pakkuja kirjel kordumatu nimi ja URL. Vaadake üle selle lehe sisu. Kui üksuse **Litware, Inc.** kirje on juba olemas, jätke järgmine protseduur vahele, vt [Uue ER-vormingu konfiguratsioonipakkuja lisamine](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Uue ER-konfiguratsiooni pakkuja lisamine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.
3. Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.
4. Väljale **Nimi** sisestage väärtus **Litware, Inc.**
5. Sisestage väljale **Interneti-aadress** `https://www.litware.com`.
6. Valige käsk **Salvesta**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>ER-konfiguratsiooni pakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Vailge lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Litware, Inc.** ja seejärel valige **Määra aktiivne**.

Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse ülevaade](general-electronic-reporting.md)
- [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsingu tegemiseks](trace-execution-er-troubleshoot-perf.md)
- [Arvutatud väljatüübi ER-andmeallikate parameetritega kõned](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
