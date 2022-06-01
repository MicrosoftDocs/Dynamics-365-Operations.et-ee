---
title: Parandada ER-lahenduste jõudlust käitusajal toodud tabeliväljade arvu vähendamise abil
description: See teema selgitab, kuidas saate jõudlust parandada, vähendades käitusajal toodud tabeliväljade arvu.
author: NickSelin
ms.date: 05/12/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd192a7718ac4fd8bcb636ede6c005ca29ee5f08
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811829"
---
# <a name="improve-performance-of-er-solutions-by-reducing-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Parandada ER-lahenduste jõudlust käitusajal toodud tabeliväljade arvu vähendamise abil

[!include[banner](../includes/banner.md)]

Saate kujundada elektroonilise [aruandluse](general-electronic-reporting.md) (ER) vorminguid [,](er-overview-components.md#format-components-for-outgoing-electronic-documents) mis loovad väljaminevaid dokumente erinevates vormingutes. Dokumendi loomisel kutsub ER-vorming andmeallikaid, mis on konfigureeritud vastavas ER-mudeli [vastendamisel](er-overview-components.md#model-mapping-component). Rakenduse tabelitele, päringutele või kirjete toomise üksustele juurdepääsu konfigureerimiseks saate kasutada ER-i andmeallikaid tüübiga *Tabelikirjed*. Vaikimisi toob tabelikirjete tüübi *andmeallikas* soovitud kirjete kõigi väljade väärtused. Seda tüüpi andmeallikaid saab siiski konfigureerida nii, et toodaks ainult ER-vormingu jaoks vajalikud väljaväärtused. See konfiguratsioon aitab vähendada rakendusserveri mälu tarbimist, mis teeb andmete toomise ja edasise salvestuse vahemällu salvestuse.

Lisateavet selle kohta, kuidas piirata tabelikirjete *tüübiga* Andmeallikate toodavad väljad, viige lõpule selles teemas toodud näide.

## <a name="example-reduce-the-number-of-table-fields-that-are-fetched-at-runtime"></a>Näide: vähendage käitusajal toodud tabeliväljade arvu

Järgmised protseduurid näitavad, kuidas kasutaja süsteemiadministraatoris või elektroonilise aruandluse arendaja rollis saab konfigureerida ER-mudeli vastendamise nii, et see toob ainult ER-vormingu käivitamiseks vajalikud väljad, et vähendada rakendusserveri mälu tarbimist.

Need protseduurid saab lõpetada USMF-ettevõttes **·** Microsoft Dynamics 365 Finances. Koodi pole vaja kirjutada.

Selle näite lõpuleviimiseks peab teil olema juurdepääs USMF-ettevõttele **ühel** järgmistest rollidest:

- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Selles näites [kasutate ER konfiguratsioone](general-electronic-reporting.md#Configuration), mis on antud näidisettevõttele **Litware, Inc**. Veenduge, et konfiguratsioonipakkuja **Litware, Inc.** (`http://www.litware.com`) näidisettevõttele on esitatud ER raamistikus ja et see on märgitud **aktiivseks**. Kui seda konfiguratsioonipakkujat pole loendis või **kui** see pole märgitud aktiivseks, [järgige konfiguratsioonipakkuja loomise juhiseid ja märkige see aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="configure-the-er-framework"></a>ER-raamistiku konfigureerimine

Minimaalsete [ER-i parameetrite konfigureerimine](er-quick-start2-customize-report.md#ConfigureFramework), mis on vajalikud ER-i raamistiku kasutamiseks. Enne ER-raamistiku kasutamist tuleb antud ER-lahenduse andmeallikate muutmiseks see häälestus lõpule viia.

### <a name="import-the-sample-er-configurations"></a>ER-i konfiguratsioonide näidise importimine

Kui te pole veel [uue ER-i](er-quick-start1-new-solution.md) lahenduse kujundamises näidet lõpule viinud, et printida kohandatud aruandeteema, laadige alla ja salvestage XML-failid järgmistesse antud ER-lahenduse konfiguratsioonidesse.

| Sisu kirjeldus            | Failinimi |
|--------------------------------|-----------|
| ER-i andmemudeli konfiguratsioon    | [Küsimustike mudel.version.1.xml](https://download.microsoft.com/download/b/6/3/b633bd34-d200-4422-96d9-8f62eb5218f8/Questionnaires_model.version.1.xml) |
| ER mudelivastenduse konfiguratsioon | [Küsimustike vastendamine.version.1.1.xml](https://download.microsoft.com/download/7/b/2/7b258e4e-4bd5-46a4-8114-27419ae4acd8/Questionnaires_mapping.version.1.1.xml) |
| Elektroonilise aruandluse vormingu konfiguratsioon        | [Küsimustike vorming.version.1.1.xml](https://download.microsoft.com/download/1/b/a/1ba39ec2-257a-44d8-972f-25bf7d18fb41/Questionnaires_format.version.1.1.xml) |

Seejärel järgige neid samme, et laadida antud ER-lahenduse konfiguratsioonid üles oma finantseksemplari.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Importige **konfiguratsioonilehel** ER-andmemudeli konfiguratsioon.

    1. Valige **Vahetus** ja seejärel valige **Laadi XML-failist**.
    2. Valige **fail** Sirvi, leidke ja valige **mudel Küsimustikud.version.1.xml** ning seejärel valige **OK**.

4. Saate importida ER-mudeli vastendamise konfiguratsiooni.

    1. Valige **Vahetus** ja seejärel valige **Laadi XML-failist**.
    2. Valige **sirvimisfail**, otsige ja valige küsimustike **vastendamine.1.1.xml** fail ja seejärel valige **OK**.

5. Importige ER-vormingu konfiguratsioon.

    1. Valige **Vahetus** ja seejärel valige **Laadi XML-failist**.
    2. Valige **sirvimisvorming**, otsige ja valige **ankeete vorming.1.1.xml** ning seejärel valige **OK**.

6. Konfiguratsioonipuus laiendage valikut **Küsimustike mudel**.
7. Vaadake imporditavate ER konfiguratsioonide loendit konfiguratsioonipuus.

    ![Konfiguratsioonide lehel imporditud ER-i konfiguratsioonide loendi läbivaatamine.](./media/er-reduce-fetched-fields-number-configurations.png)

### <a name="review-the-provided-er-model-mapping"></a>Esitatud ER-mudeli vastendamise ülevaade

1. **Leheküljel Konfiguratsioonid** valige küsimustike **vastendamine**.
2. Valige toimingupaanil valik **Koostaja**.
3. Valige lehel **Mudeli ja andmeallika vastendamine** suvand **Kujundaja**.
4. Valige tegevuspaanil **mudeli** vastendamise kujundaja lehel grupivaade, **et kuva** Grupp sisse **lülitada**.
5. Laiendage **andmemudeli** paanil valikut **Küsimustik**.

    Pange tähele, **et** küsimustiku andmeallikas on rakenduse tabelile juurdepääsuks `KMCollection` konfigureeritud.

6. Laiendage andmeallikate **paanil** valikut Tabelikirjed **Küsimustiku** \> **väljad.** \> **·**

    Pange tähele, kui palju rakendusetabeli `KMCollection` välju kuvatakse **tabelikirjete** tüübi küsimustiku *andmeallikas*.

    ![Antud mudeli vastendamise ülevaatamine mudeli vastendamise kujundaja lehel, kui grupivaade on sisse lülitatud.](./media/er-reduce-fetched-fields-number-mapping1.png)

7. Tegevuspaanil valige uuesti Grupi vaade **, et** lülitada vaade **Grupp** välja ja seejärel valige **suvand Näita ainult** \> **vastendatud kuva**.

    Pange tähele, et mõned rakenduse tabeli `KMCollection` väljad on kasutusel küsimustiku **kirjeloendi** täitmiseks ER andmemudelis:

    - `Active`
    - `Description`
    - `questionMode`
    - `kmCollectionId`

    ![Antud mudeli vastendamise ülevaatamine mudeli vastendamise kujundaja lehel, kui grupivaade on välja lülitatud.](./media/er-reduce-fetched-fields-number-mapping2.png)

### <a name="turn-on-the-er-performance-trace"></a>ER-i jõudluse jälituse sisselülitamine

Järgige ER-i [jõudluse jälituse](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) sisselülitamistoiminguid, et seadistada ER-i kasutajaparameetrid, mis võimaldavad jälgida ER-i komponentide käivitamist.

### <a name="run-the-provided-er-format-by-using-the-provided-model-mapping"></a>Esitatud ER-vormingu käitamine esitatud mudelivastenduse abil

Konfiguratsioonilehe üksiku [küsimustiku antud ER-vormingu käivitamiseks järgige ER-i](er-quick-start1-new-solution.md#RunFormatFromER)**loodud vormingu käivitamiseks juhiseid**.

### <a name="review-the-execution-trace-of-the-first-run"></a>Vaadake üle esimese käituse täitmisjälg.

1. Minge organisatsiooni **halduse elektroonilise** \> **aruandluse konfiguratsioonidesse \>**.
2. Laiendage **lehel** Konfiguratsioonid mudel **Küsimustikud ja** valige küsimustike **vastendamine**.

    > [!NOTE]
    > Versioonide kiirkaardi üksikasjad **näitavad**, et valisite küsimustike vastendamise **konfiguratsiooni mustandversiooni**. Seetõttu saate muuta selle mudeli vastendamise sisu.

3. Valige toimingupaanil valik **Koostaja**.
4. Valige lehel **Mudeli ja andmeallika vastendamine** suvand **Kujundaja**.
5. Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.
6. Valige dialoogiboksis **Jõudluse jälituse** tulemuse sätted viimase vormingu käivitamisel loodud jälitus.

    ![Jälje valimine jõudluse jälituse tulemuse sätete dialoogiboksis](./media/er-reduce-fetched-fields-number-select-trace-1.png)

7. Valige nupp **OK**. 
8. Filtreerige **kiirkaardil** Üksikasjad küsimustiku **tee**, mis viitab küsimustiku **andmeallikale**.
9. Vaadake üle küsimustiku andmeallika kutsumisel loodud andmebaasipäringu **üksikasjad**.

    Pange tähele, et kõik rakenduse `KMCollection` tabeli väljad toetati käitusajal, kui **kutsuti** küsimustiku andmeallikas.

    ![Andmebaasipäringu üksikasjade ülevaatamine mudeli vastendamise kujundaja lehel.](./media/er-reduce-fetched-fields-number-query1.png)

### <a name="modify-the-provided-er-model-mapping"></a>Esitatud ER-mudeli vastendamise muutmine

1. Valige mudeli **vastendamise** kujundaja lehel **andmeallikate** paanil Küsimustiku **andmeallikas**.
2. Valige andmeallikate **paanil** käsk **Redigeeri**.
3. Valige dialoogiboksis **Andmeallika atribuudid** suvand Vali **väljad**`KMCollection`, et määrata viidatud rakendusetabeli väljade loend, **mis** ilmub käitusajal redigeeritava küsimustiku andmeallika käivitamisel.

    ![Kui soovite, et käivitate dialoogiboksis Andmeallika atribuudid valiku Vali väljad, et konfigureerida rakendustabelist toodavate väljade loendit redigeeritava andmeallika abil.](./media/er-reduce-fetched-fields-number-select-fields1.png)

4. Valige lehel **Vali väljad** suvand **Automaatne täitmine**.

    Valitud **väljade** loend täidetakse automaatselt mudeli vastendamise eelkonfigureeritud artefaktide põhjal. Kõik viidatud tabeli väljad ja seosed, mida on mainitud mudeli vastendamise mis tahes sidumis-, valemi- või andmeallikas, lisatakse loendisse.

    ![Väljade loendi konfigureerimine, mis toodatakse rakenduse tabelist lehel Vali väljad.](./media/er-reduce-fetched-fields-number-select-fields2.png)

5. Valige **Salvesta** ja sulgege leht **Vali väljad**.
6. Valige **OK**, et talletada andmeallika sätetes tehtud muudatused.
7. Tegevuspaanil valige suvand **Näita kõiki**.

    Küsimustiku andmeallikas **näitab** nüüd teksti **\<Fields are filtered\>**. See tekst näitab, et andmeallikas on konfigureeritud tooma piiratud arvu välju viidatud rakenduse tabelist.

    ![Värskendatud mudelivastenduse ülevaatamine mudeli vastendamise kujundaja lehel](./media/er-reduce-fetched-fields-number-mapping3.png)

8. Valige **salvestamine**, et talletada muudatused, mida olete redigeeritavale mudeli vastendamisele teinud.

    > [!NOTE]
    > Käitusajal analüüsib ER lisatud suhteid ja lisab kõik andmebaasi päringus kasutatavad väljad, isegi kui neid välju ei lisatud konstruktsiooni ajal selgesõnaliselt toodanud väljade loendisse.

### <a name="run-the-provided-er-format-by-using-the-updated-model-mapping"></a>Esitatud ER-vormingu käitamine värskendatud mudelivastenduse abil

Konfiguratsioonilehe üksiku [küsimustiku antud ER-vormingu käivitamiseks järgige ER-i](er-quick-start1-new-solution.md#RunFormatFromER)**loodud vormingu käivitamiseks juhiseid**.

### <a name="review-the-execution-trace-of-the-second-run"></a>Vaadake üle teise käituse täitmisjälg.

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Laiendage **lehel** Konfiguratsioonid mudel **Küsimustikud ja** valige küsimustike **vastendamine**.
3. Valige toimingupaanil valik **Koostaja**.
4. Valige lehel **Mudeli ja andmeallika vastendamine** suvand **Kujundaja**.
5. Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.
6. Valige dialoogiboksis **Jõudluse jälituse** tulemuse sätted viimase vormingu käivitamisel loodud jälitus.
7. Valige nupp **OK**.
8. Filtreerige **kiirkaardil** Üksikasjad küsimustiku **tee**, mis viitab küsimustiku **andmeallikale**.
9. Vaadake üle küsimustiku andmeallika kutsumisel loodud andmebaasipäringu **üksikasjad**.

    Pange tähele, et küsimustiku andmeallika `KMCollection`**käivitamisel toetati käitusajal rakenduse tabelist ainult andmeallika täitmiseks nõutavad** väljad.

    > [!NOTE]
    > Mõned väljad, nt sektsiooni ID väljad, andmeala ID ja kirje ID, lisab automaatselt rakenduse Finance andmehalduse raamistik.

    ![Uuendatud mudelivastenduse andmebaasipäringu üksikasjade ülevaatamine mudeli vastendamise kujundaja lehel.](./media/er-reduce-fetched-fields-number-query2.png)

Saate kasutada seda tehnikat, et vähendada toodanud kirjete arvu, kui peate vähendama mälu tarbimist käitatud ER-mudeli vastendamise ja ER-vormingu abil.

## <a name="limitations"></a>Kitsendused

*Kui* piirate toodavate väljade arvu tabelikirjete tüübi andmeallika jaoks, ei saa te kasutada rakendustabeli meetodeid, millele andmeallikas viitab, sest rakenduse metaandmed ei anna teavet tabeliväljade kohta, mis on vajalikud nende meetodite kutsumiseks.

## <a name="usage-notes"></a>Kasutamise märkused

Kuigi automaatse **täitmise** käsk lisab automaatselt välju, ei kustuta see automaatselt varem lisatud välju, isegi kui neid ei kasutata enam redigeeritava mudeli vastenduse sidumistes, valemites ega andmeallikates.

Kui valite **automaatse täitmise**, analüüsib ER sidumisi, valemeid ja andmeallikaid, mis redigeeritava mudeli vastenduse avasite selle redigeerimiseks. Redigeeritava mudeli vastenduse sidumiste, **valemite** ja andmeallikate muutmisel ja automaatse täitmise käsu kasutamisel sulgege mudeli vastenduse kujundaja ja avage see mudelivastenduse redigeerimiseks uuesti. 

## <a name="additional-resources"></a>Lisaressursid

- [Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md)
- [Jõudlusprobleemide tõrkeotsing ER-i konfiguratsioonides](er-troubleshoot-perf-issues-in-configurations.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
