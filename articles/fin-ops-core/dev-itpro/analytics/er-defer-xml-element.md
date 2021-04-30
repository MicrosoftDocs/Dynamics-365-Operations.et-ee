---
title: Lükka edasi XML-elementide käivitamine ER-vormingus
description: Selles teemas selgitatakse, kuidas lükata XML-elemendi käivitamine elektroonilise aruandluse (ER) vormingus.
author: NickSelin
ms.date: 03/17/2020
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
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 361e16b0dba3aa46c71477efaa89a2661a3bcd75
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894048"
---
# <a name="defer-the-execution-of-xml-elements-in-er-formats"></a>Lükka edasi XML-elementide käivitamine ER-vormingus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Saate kasutada [Elektroonilise aruandluse (ER)](general-electronic-reporting.md) raamistiku operatsioonide kujundajat, et [konfigureerida](./tasks/er-format-configuration-2016-11.md) ER lahenduse [vormingukomponent](general-electronic-reporting.md#FormatComponentOutbound), mida kasutatakse väljamineva dokumendi loomiseks XML-vormingus. Konfigureeritud vormingukomponendi hierarhiline struktuur koosneb erinevate tüüpide vorminguelementidest. Neid vorminguelemente kasutatakse loodud dokumentide täitmiseks nõutava teabega käitusaja ajal. Vaikimisi, kui käitate ER-vormingut, käitatakse vorminguelemente samas järjekorras, nagu need on esitatud vorminguhierarhias: ükshaaval, ülevalt alla. Kuid kujundusrežiimis saate muuta konfigureeritud vormingu komponendi mis tahes XML-elementide käivitamise järjestust.

Kui konfigureeritud vormingus <a name="DeferredXmlElementExecution"></a> XML-elemendi **Edasilükatud käivitamise** suvandi sisse lülitada, saate selle elemendi käivitamise edasi lükata (edasi lükata). Sel juhul element ei käivitu enne, kui kõik teised ülemastme elemendid on käivitatud.

Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.

## <a name="limitations"></a>Kitsendused

**Edasilükatud käivitamise** suvandit toetatakse ainult XML-elementide puhul, mis on konfigureeritud ER-vormingus, mida kasutatakse **väljamineva** dokumendi loomiseks XML-vormingus.

**Edasilükatud käivitamise** suvandit toetatakse ainult XML-elementide puhul, mis asuvad ainult ühes teises XML-elemendis. Seetõttu ei kohaldata seda XML-elementide puhul, mis asuvad muudes vormingu elementides (nt **XML-seeria** elemendis).

**Edasilükatud käivitamise** suvandit ei toetata XML-elementide puhul, mis asuvad **Ühises\\failivormingu** elemendis, kui **Tükeldatud faili** suvand on seatud väärtusele **Jah**. Rohkem teavet selle kohta, kuidas tükeldada XML-faile, vt teemast [Loodud XML-failide tükeldamine failimahu ja sisuüksuste koguse alusel](er-split-files.md).

## <a name="example-defer-the-execution-of-an-xml-element-in-an-er-format"></a><a name="Example"></a>Näide: XML-elemendi käivitamise edasilükkamine ER-vormingus

Järgmised sammud selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsionaalse nõustaja kasutaja [roll](../sysadmin/tasks/assign-users-security-roles.md) saab konfigureerida ER-vormingut, mis sisaldab XML-elementi, kus täitmise järjekord erineb järjekorrast vormingu hierarhias.

Need toimingud saab teha **USMF** ettevõttes rakenduses Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Eeltingimused

Selle näite läbimiseks peab teil olema juurdepääs rakendusele **USMF** ettevõttele rakenduses Finance ühega järgmistest rollidest.

- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Kui te pole veel lõpule viinud näidet teemas [ER-vormingu elementide järjestuse käivitamise edasilükkamine](er-defer-sequence-element.md#Example), laadige alla järgmised proovi ER-lahenduse [konfiguratsioonid](general-electronic-reporting.md#Configuration).

| Sisu kirjeldus            | Faili nimi |
|--------------------------------|-----------|
| ER-i andmemudeli konfiguratsioon    | [Mudel edasilükatud XML elements.version.1.xml õppimiseks](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| ER mudelivastenduse konfiguratsioon | [Vastendus edasilükatud elements.version.1.1.xml kohta teabe saamiseks](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Enne alustamist tuleb teil oma kohalikku arvutisse alla laadida ja salvestada ka proovi ER-lahenduse järgmine konfiguratsioon.

| Sisu kirjeldus     | Faili nimi |
|-------------------------|-----------|
| Elektroonilise aruandluse vormingu konfiguratsioon | [Vorming edasilükatud XML elements.version.1.1.xml õppimiseks](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>ER-i konfiguratsioonide näidise importimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Lehel **Konfiguratsioonid**, kui konfiguratsioon **Mudel teabe saamiseks edasilükatud elementide kohta** ei ole saadaval konfiguratsioonipuus, importige ER-andmemudeli konfiguratsioon:

    1. Valige **Vahetus** ja seejärel valige **Laadi XML-failist**.
    2. Valige **Sirvi** otsige ja valige fail **Mudel teabe saamiseks edasilükatud XML elements.1.xml kohta** ja seejärel valige **OK**.

4. Kui konfiguratsioon **Mudel teabe saamiseks edasilükatud elementide kohta** ei ole saadaval konfiguratsioonipuus, importige ER-mudeli vastenduse konfiguratsioon:

    1. Valige **Vahetus** ja seejärel valige **Laadi XML-failist**.
    2. Valige **Sirvi**, otsige ja valige fail **Vastendamine teabe saamiseks edasilükatud elements.1.1.xml kohta** ja seejärel valige **OK**.

5. ER-vormingu konfiguratsiooni importimine:

    1. Valige **Vahetus** ja seejärel valige **Laadi XML-failist**.
    2. Valige **Sirvi** otsige ja valige **Vorming, et tutvuda lükatud XML elements.1.1 XML** failiga ja seejärel valige **OK**.

6. Konfiguratsioonipuus laiendage valikut **Mudel teabe saamiseks edasilükatud elementide kohta**.
7. Vaadake imporditavate ER konfiguratsioonide loendit konfiguratsioonipuus.

    ![Imporditud ER-konfiguratsioonid lehel Konfiguratsioonid](./media/ER-DeferredXml-Configurations.png)

### <a name="activate-a-configuration-provider"></a>Konfiguratsioonipakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Veenduge lehe **Lokalistasiooni konfiguratsioonid** jaotises **Konfiguratsiooni pakkujad**, et [konfiguratsiooni pakkuja](general-electronic-reporting.md#Provider) näidisettevõttele Litware, Inc. (`http://www.litware.com`) oleks loendis ja tähistatud kui aktiivne. Kui seda konfiguratsioonipakkujat ei ole loendis või kui see pole märgitud aktiivseks, järgige juhiseid teemas [Looge konfiguratsioonipakkuja ja märkige see aktiivseks](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Litware, Inc. näidisettevõte lokaliseerimise konfiguratsioonide lehel](./media/ER-DeferredXml-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Vaadake üle imporditud mudelivastendus

Vaadake üle ER mudeli vastendamise komponendi sätted, mis on konfigureeritud juurdepääsuks maksukannetele ja mille puhul on taotlusel juurdepääs andmetele.

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Valige **Aruandluse konfiguratsioonid**.
3. Lehel **Konfiguratsioonid** laiendage konfiguratsioonipuus **Mudel teabe saamiseks edasilükatud elementide kohta**.
4. Valige konfiguratsioon **Vastendamine teabe saamiseks edasilükatud elementide kohta**.
5. Valige **Koostaja**, et avada vastenduste loend.
6. Valige **Koostaja**, et vaadata üle vastendamise üksikasjad.
7. Valige **Üksikasjade näitamine**.
8. Vaadake üle andmeallikad, mis on konfigureeritud juurdepääsuks maksukannetele:

    - Andmeallikas **Kanded** tüübis *Tabelikirjed* konfigureeritakse juurdepääsuks **TaxTrans** kirjete rakendustabelile.
    - Andmeallikas **Kanded** tüübis *Arvutatud väli* konfigureeritakse, et tagastada vajalikud kandekoodid (**INV-10000349** ja **INV-10000350**) kandeloendina.
    - Andmeallikas **Filtreeritud** tüübis *Arvutatud väli* konfigureeritakse, et valida, andmeallikast **Kanded**, ainult nõutud kannete maksukanded.
    - Väli **\$TaxAmount** tüübis *Arvutatud väli* lisatakse andmeallikale **Filtreeritud**, et esitada maksuväärtus, millel on vastupidine märk.
    - Andmeallikas **Rühmitatud** tüübis *Rühmitusalus* konfigureeritakse, et rühmitada andmeallika **Filtreeritud** filtreeritud maksukanded.
    - Summaväli **TotalSum** andmeallikas **Rühmitatud** konfigureeritakse, et summeerida välja **\$TaxAmount** väärtused andmeallikas **Filtreeritud** selle andmeallika kõigi filtreeritud maksukannete osas.

        ![TotalSum summeerimise väli üksuse GroupBy redigeerimisparameetrite lehel](./media/ER-DeferredXml-GroupByParameters.png)

9. Vaadake, kuidas konfigureeritud andmeallikad on andmemudeliga seotud ja kuidas nad võimaldavad juurdepääsu andmetele, et teha need kättesaadavaks ER vormingus:

    - **Filtreeritud** andmeallikas on seotud andmemudeli väljaga **Data.List**.
    - Väli **\$TaxAmount** andmeallikas **Filtreeritud** on seotud andmemudeli väljaga **Data.List.Value**.
    - Väli **TotalSum** andmeallikas **Rühmitatud** on seotud andmemudeli väljaga **Data.Summary.Total**.

    ![Mudelivastenduse koostaja leht](./media/ER-DeferredXml-ModelMapping.png)

10. Sulgege **Mudelivastendamise kujundaja** ja **Mudelivastenduste** lehed.

### <a name="review-the-imported-format"></a>Vaadake üle imporditud vorming

1. Lehel **Konfiguratsioonid** valige konfiguratsiooni puus **Vorming edasiste XML-elementidega tutvumiseks** konfiguratsioon.
2. Valige **Koostaja**, et vaadata üle vormingu üksikasjad.
3. Valige **Üksikasjade näitamine**.
4. Vaadake üle ER-vormingu komponentide sätted, mis on konfigureeritud looma väljaminevat dokumenti XML-vormingus, mis sisaldab maksude kannete üksikasju.

    - **Aruande\\teate** XML-element on konfigureeritud täitma väljaminevat dokumenti ühe sõlmega, mis sisaldab pesastatud XML-elemente (**Päis**, **Kirje** ja **Kokkuvõte**).
    - **Aruande\\teate\\päise** XML-element on konfigureeritud täitma väljaminevat dokumenti ühe päisesõlmega, mis näitab töötlemise alustamise kuupäeva ja kellaaega.
    - **Aruande \\teate\\kirje** XML-element on konfigureeritud täitma väljaminevat dokumenti ühe kirjesõlmega, mis näitab ühe maksukande üksikasju.
    - **Aruande\\teate\\kokkuvõtte** XML-element on konfigureeritud täitma väljaminevat dokumenti ühe kokkuvõtva sõlmega, mis sisaldab maksude väärtuste summat töödeldud maksukannetest.

    ![Sõnumi XML-element ja pesastatud XML-elemendid vormingu kujundaja lehel](./media/ER-DeferredXml-Format.png)

5. Vahekaardil **Vastendamine** vaadake üle järgmised üksikasjad:

    - **Aruande\\teate\\päise** element ei pea olema seotud allikaga, et luua üksik sõlm väljaminevas dokumendis.
    - **ExecutionDateTime** atribuut loob päisesõlme lisamisel kuupäeva ja kellaaja (sh millisekundid).
    - **Aruande\\teate\\kirje** element on seotud loendiga **mudel.Andmed.Loend**, et luua üks kirjesõlm iga kirje puhul seotud loendist.
    - **TaxAmount** atribuut on seotud loendiga **mudel.Andmed.Loend.Väärtus** (mis kuvatakse kujul **\@. Väärtus** suhtelise tee vaates), et luua praeguse maksukande maksusumma.
    - **RunningTotal** atribuut on maksusummade jooksva kogusumma kohatäide. Praegu ei ole sellel atribuudil väljundit, kuna selle jaoks ei ole konfigureeritud ega vaikimisi määratud väärtust.
    - **ExecutionDateTime** atribuut loob praeguse kande töötlemisel selles aruandes kuupäeva ja kellaaja (sh millisekundid).
    - **Aruande\\teate\\kokkuvõtte** element ei pea olema seotud andmeallikaga, et luua üksik sõlm väljaminevas dokumendis.
    - **TotalTaxAmount** atribuut on seotud objektiga **model.Data.Summary.Total**, et luua töödeldud maksukannete summa.
    - **ExecutionDateTime** atribuut loob summa sõlme lisamisel kuupäeva ja kellaaja (sh millisekundid).

    ![Vormingu kujundaja vahekaart Vastendamine](./media/ER-DeferredXml-Format2.png)

### <a name="run-the-imported-format"></a>Imporditud vormingu käivitamine

1. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
2. Laadige alla fail, mida veebilehitseja pakub, ja avage see läbivaatuseks.

    ![Allalaaditud fail](./media/ER-DeferredXml-Run.png)

Pange tähele, et kokkuvõtte sõlm esitab töödeldud kannete maksu väärtuste summa. Kuna vorming on konfigureeritud kasutama **model.Data.Summary.Total**-it, mis on siduv selle summa tagastamiseks, arvutatakse summa, kutsudes välja mudeli vastendamises **TotalSum** summeerimiseks **Rühmitatud** andmeallika, *Rühmitusaluse* tüübi. Selle summeerimise arvutamiseks mudeli vastendamine itereerib üle kõigi kannete, mis on valitud **Filtreeritud** andmeallikas. Võrdledes kokkuvõtte sõlme ja viimase kirje sõlme käivitamise aegu, saate kindlaks teha, et summa arvutamiseks kulus 12 millisekundit (ms). Võrreldes esimese ja viimase kirje sõlmede käivitamise aega, saate kindlaks määrata, et kõigi kirje sõlmede loomine võttis 9 ms. Seetõttu vajati kokku 21 ms.

### <a name="modify-the-format-so-that-the-calculation-is-based-on-generated-output"></a>Vormingu muutmine nii, et arvutus põhineb loodud väljundil

Kui kande maht on praeguse näite mahust palju suurem, võib kalkulatsiooni aeg suureneda ja põhjustada jõudluse probleeme. Vormingu sätte muutmisega saate aidata vältida nende jõudluse probleeme. Kuna teil on juurdepääs maksu väärtustele, et kaasata need loodud aruandesse, saate seda teavet kasutada maksude väärtuste arvutamiseks. Lisateavet vt jaotisest [Vormingu konfigureerimine inventuuri tegemiseks ja summeerimiseks](./tasks/er-format-counting-summing-1.md).

1. Lehel **Vormingukujundaja** vahekaardil **Vorming** valige failielement **Aruanne** vormingupuus.
2. Seadke **Väljundi üksikasjade sissenõudmise** väärtuseks **Jah**. Nüüd saate seda vormingut konfigureerida, kasutades loodud aruande sisu andmeallikaks, millele pääseb juurde, kasutades [andmete kogumise](er-functions-category-data-collection.md) kategoorias sisseehitatud ER funktsioone.
3. Vahekaardil **Vastendamine** valige XML-element **Aruanne\\Sõnum\\Kirje**.
4. Konfigureerige avaldis **Kogutud andmevõtme nimi** kui `WsColumn`.
5. Konfigureerige avaldis **Kogutud andmevõtme väärtus** kui `WsRow`.

    ![Salvestage XML-element vormingukujundaja lehel](./media/ER-DeferredXml-Format3.png)

6. Valige atribuut **Aruanne\\Sõnum\\Kirje\\MaksuSumma**.
7. Konfigureerige avaldis **Kogutud andmete võtme nimi** kui `SummingAmountKey`.

    ![Atribuut TaxAmount vormingukujundaja lehel](./media/ER-DeferredXml-Format4.png)

    Selle sättega saate arvestada virtuaalse töölehe täitmist, mille puhul on lahtri A1 väärtus lisatud iga töödeldud maksu kande maksusumma väärtusele.

8. Valige atribuut **Report\\Message\\Record\\RunningTotal** ja seejärel valige **Radigeeri valemit**.
9. Konfigureerige `SUMIF(SummingAmountKey, WsColumn, WsRow)` avaldis sisemise [SUMIF](er-functions-datacollection-sumif.md) ER funktsiooni abil ja seejärel valige **Salvesta**.

    ![SUMIF avaldis](./media/ER-DeferredXml-FormulaDesigner.png)

10. Sulgege **Valemikoostaja** leht.
11. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
12. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail](./media/ER-DeferredXml-Run1.png)

    Viimase kirje sõlm sisaldab kõigi töödeldud kannete puhul arvutatud maksude väärtuste jooksvat kogusummat, kasutades loodud väljundit andmeallikana. See andmeallikas algab aruande algusest ja jätkub kuni viimase maksu kandeni. Kokkuvõtte sõlm sisaldab kõigi töödeldud kannete maksuväärtuste summat, mis arvutatakse mudeli vastendamisel, kasutades *Rühmitusaluse* tüüpi andmeallikat. Pange tähele, et need väärtused on võrdsed. Seetõttu saab üksuse **Rühmitusalus** asemel kasutada väljundi baasil summeerimist. Võrreldes esimese kirjesõlme ja kokkuvõttesõlme käivitamise aega, saate kindlaks määrata, et kõigi kirjesõlmede loomine ja summeerimine võttis 11 ms. Seetõttu on kirje sõlmede loomise ja maksu väärtuste summeerimise osas muudetud vorming umbes kaks korda kiirem kui algne vorming.

13. Valige atribuut **Report\\Message\\Summary\\TotalTaxAmount** ja seejärel valige **Redigeeri valemit**.
14. Sisestage avaldis `SUMIF(SummingAmountKey, WsColumn, WsRow)` olemasoleva avaldise asemel.
15. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
16. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail](./media/ER-DeferredXml-Run2.png)

    Pange tähele, et viimase kirje sõlme maksude väärtuste jooksev kogusumma võrdub nüüd kokkuvõtte sõlme summaga.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Sisestage aruande päisesse väljundil põhineva summeerimise väärtused

Kui näiteks peate oma aruande päises esitama maksude väärtuste summa, saate muuta oma vormingut.

1. Lehel **Vormingukujundaja** vahekaardil **Vorming** valige **Report\\Message\\Summary** XML-element.
2. Valige **Nihuta üles**.
3. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
4. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail](./media/ER-DeferredXml-Run3.png)

    Pange tähele, et maksu väärtuste summa kokkuvõtte sõlmes võrdub nüüd 0 (null), kuna see summa arvutatakse loodud väljundi põhjal. Kui luuakse esimene kirje sõlm, ei sisalda loodud väljund veel kirje sõlme, millel on kande üksikasjad. Saate konfigureerida selle vormingu, et lükata edasi **Report\\Message\\Summary** elemendi käivitamine, kuni **Report\\Message\\Record** element on käivitatud kõigi maksukannete puhul.

### <a name="defer-the-execution-of-the-summary-xml-element-so-that-the-calculated-total-is-used"></a>Lükka edasi kokkuvõtte XML-elemendi käivitamine nii, et arvutatud kogusummat kasutatakse

1. Lehel **Vormingukujundaja** vahekaardil **Vorming** valige **Report\\Message\\Summary** XML-element.
2. Määrake suvand **Edasilükatud täitmine** valikule **Jah**.

    ![Kokkuvõtte XML-elemendi edasilükatud käivitamise suvand vormingu kujundaja lehel](./media/ER-DeferredXml-Format5.png)

3. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
4. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail](./media/ER-DeferredXml-Run4.png)

    **Report\\Message\\Summary** elementi käivitatakse nüüd ainult siis, kui kõik muud üksused, mis on pesastatud selle peamise elemendi  **Report\\Message** alusel, on käivitatud. Seetõttu käivitatakse see pärast **Report\\Message\\Record** elemendi käivitamist  **model.Data.List** andmeallika kõigi maksukannete puhul.. Esimese ja viimase kirje sõlmede ja päise ja kokkuvõtte sõlmede käivitamise ajad näitavad seda fakti.

## <a name="additional-resources"></a>Lisaressursid

- [Vormingu konfigureerimine loendamiseks ja liitmiseks](./tasks/er-format-counting-summing-1.md)
- [ER-vormingu täitmise jälitus jõudluse probleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md)
- [Lükka edasi elementide käivitamise järjestus ER-vormingus](er-defer-sequence-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]