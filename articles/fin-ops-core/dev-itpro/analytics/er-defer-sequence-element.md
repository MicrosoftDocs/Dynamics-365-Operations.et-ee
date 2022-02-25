---
title: Lükka edasi elementide käivitamise järjestus ER-vormingus
description: Selles teemas selgitatakse, kuidas lükata järjestuse elemendi käivitamine elektroonilise aruandluse (ER) vormingus.
author: NickSelin
ms.date: 04/23/2021
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
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 19d1cf0aa6e9b40a0e72a3a74acda6e2579d6ee2
ms.sourcegitcommit: d5d6b81bd8b08de20cc018c2251436065982489e
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323686"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Lükka edasi elementide käivitamise järjestus ER-vormingus

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Ülevaade

Saate kasutada elektroonilise [aruandluse (ER)](general-electronic-reporting.md)[raamistiku](tasks/er-format-configuration-2016-11.md) toimingute kujundajat, et konfigureerida ER-lahenduse vormingukomponenti, mida kasutatakse väljaminevate dokumentide loomiseks tekstivormingus. Konfigureeritud vormingukomponendi hierarhiline struktuur koosneb erinevate tüüpide vorminguelementidest. Neid vorminguelemente kasutatakse loodud dokumentide täitmiseks nõutava teabega käitusaja ajal. Vaikimisi, kui käitate ER-vormingut, käitatakse vorminguelemente samas järjekorras, nagu need on esitatud vorminguhierarhias: ükshaaval, ülevalt alla. Kuid kujundusrežiimis saate muuta konfigureeritud vormingu komponendi mis tahes järjestuselementide käivitamise järjestust.

Kui konfigureeritud vormingus <a name="DeferredSequenceExecution"></a> järjestusvormingu elemendi **Edasilükatud käivitamise** suvandi sisse lülitada, saate selle elemendi käivitamise edasi lükata (edasi lükata). Sel juhul element ei käivitu enne, kui kõik teised ülemastme elemendid on käivitatud.

Lisateabe saamiseks selle funktsiooni kohta läbige siinse teema näide.

## <a name="limitations"></a>Kitsendused

**Edasilükatud käivitamise** suvandit toetatakse ainult järjestuselementide puhul, mis on konfigureeritud ER-vormingus, mida kasutatakse **väljamineva** dokumendi loomiseks tekstivormingus.

**Edasilükatud täitmise** suvand ei rakendu järjestustele, mis on konfigureeritud trimmitud järjestusena, kus maksimaalne pikkus on piiratud.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Näide: Järjestuselemendi käivitamise edasilükkamine ER-vormingus

Järgmised sammud selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsionaalse nõustaja kasutaja [roll](../sysadmin/tasks/assign-users-security-roles.md) saab konfigureerida ER-vormingut, mis sisaldab järjestuselementi, kus täitmise järjekord erineb järjekorrast vormingu hierarhias.

Need toimingud saab teha **USMF** ettevõttes rakenduses Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Eeltingimused

Selle näite läbimiseks peab teil olema juurdepääs rakendusele **USMF** ettevõttele rakenduses Finance ühega järgmistest rollidest.

- Elektroonilise aruandluse funktsionaalne konsultant
- Süsteemiadministraator

Kui te pole veel lõpule viinud näidet teemas [ER-vormingu XML-elementide käivitamise edasilükkamine](er-defer-xml-element.md#Example), laadige alla järgmised proovi ER-lahenduse [konfiguratsioonid](general-electronic-reporting.md#Configuration).

| Sisu kirjeldus            | Faili nimi |
|--------------------------------|-----------|
| ER-i andmemudeli konfiguratsioon    | [Mudel edasilükatud XML elements.version.1.xml õppimiseks](https://download.microsoft.com/download/7/6/0/760933ca-4ac3-4f50-bc0c-c35e596ee066/Modeltolearndeferredelements.version.1.xml) |
| ER mudelivastenduse konfiguratsioon | [Vastendus edasilükatud elements.version.1.1.xml kohta teabe saamiseks](https://download.microsoft.com/download/c/9/c/c9c4b9dd-b700-4385-a087-a84ce9fc1d0f/Mappingtolearndeferredelements.version.1.1.xml) |

Enne alustamist tuleb teil alla laadida ja salvestada ka proovi ER-lahenduse järgmine konfiguratsioon.

| Sisu kirjeldus     |Faili nimi |
|-------------------------|----------|
| Elektroonilise aruandluse vormingu konfiguratsioon | [Vorming edasilükatud sequences.version.1.1.xml kohta teabe saamiseks](https://download.microsoft.com/download/0/f/5/0f55c341-8285-4d92-a46d-475d9a010927/Formattolearndeferredsequences.version.1.1.xml) |

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
    2. Valige **Sirvi**, otsige ja valige fail **Vorming teabe saamiseks edasilükatud sequences.1.1.xml kohta** ja seejärel valige **OK**.

6. Konfiguratsioonipuus laiendage valikut **Mudel teabe saamiseks edasilükatud elementide kohta**.
7. Vaadake imporditavate ER konfiguratsioonide loendit konfiguratsioonipuus.

    ![Imporditud ER-konfiguratsioonid Konfiguratsioonide lehel.](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Konfiguratsioonide pakkuja aktiveerimine

1. Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.
2. Veenduge lehe **Lokalistasiooni konfiguratsioonid** jaotises **Konfiguratsiooni pakkujad**, et [konfiguratsiooni pakkuja](general-electronic-reporting.md#Provider) näidisettevõttele Litware, Inc. (`http://www.litware.com`) oleks loendis ja tähistatud kui aktiivne. Kui seda konfiguratsioonipakkujat ei ole loendis või kui see pole märgitud aktiivseks, järgige juhiseid teemas [Looge konfiguratsioonipakkuja ja märkige see aktiivseks](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Litware, Inc. näidisettevõte lokaliseerimise konfiguratsioonide lehel.](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

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

        ![TotalSum summeerimise väli üksuse GroupBy redigeerimisparameetrite lehel.](./media/ER-DeferredSequence-GroupByParameters.png)

9. Vaadake, kuidas konfigureeritud andmeallikad on andmemudeliga seotud ja kuidas nad võimaldavad juurdepääsu andmetele, et teha need kättesaadavaks ER vormingus:

    - **Filtreeritud** andmeallikas on seotud andmemudeli väljaga **Data.List**.
    - Väli **\$TaxAmount** andmeallikas **Filtreeritud** on seotud andmemudeli väljaga **Data.List.Value**.
    - Väli **TotalSum** andmeallikas **Rühmitatud** on seotud andmemudeli väljaga **Data.Summary.Total**.

    ![Mudelivastenduse koostaja leht.](./media/ER-DeferredSequence-ModelMapping.png)

10. Sulgege **Mudelivastendamise kujundaja** ja **Mudelivastenduste** lehed.

### <a name="review-the-imported-format"></a>Vaadake üle imporditud vorming

1. Lehel **Konfiguratsioonid** valige konfiguratsioonipuus konfiguratsioon **Vorming edasilükatud elementidega tutvumiseks**.
2. Valige **Koostaja**, et vaadata üle vormingu üksikasjad.
3. Valige **Üksikasjade näitamine**.
4. Vaadake üle ER-vormingu komponentide sätted, mis on konfigureeritud looma väljaminevat dokumenti tekstivormingus, mis sisaldab maksude kannete üksikasju.

    - Järjestuse vorminguelement **Report\\Lines** on konfigureeritud täitma väljunddokumendi ühe reaga, mis on loodud pesastatud järjestuselementidest (**Päis**, **Kirje** ja **Kokkuvõte**).

        ![Ridade järjestuse vorminguelement ja pesastatud elemendid vormingu kujundaja lehel.](./media/ER-DeferredSequence-Format.png)

    - Järjestuse vorminguelement **Report\\Lines\\Header** on konfigureeritud täitma väljaminevat dokumenti ühe päisereaga, mis näitab töötlemise alustamise kuupäeva ja kellaaega.
    - Järjestuse vorming **Report\\Lines\\Record** on konfigureeritud täitma väljaminevat dokumenti ühe reaga, mis näitab ühe maksukande üksikasju. Need maksukanded eraldatakse semikooloniga.

        ![Kirje jada vormingu element, mis kasutab eraldajana semikoolonit.](./media/ER-DeferredSequence-Format1.png)

    - Järjestuse vorminguelement **Report\\Lines\\Summary** on konfigureeritud täitma väljaminevat dokumenti ühe kokkuvõtva reaga, mis sisaldab maksude väärtuste summat töödeldud maksukannetest.

4. Vahekaardil **Vastendamine** vaadake üle järgmised üksikasjad:

    - Element **Report\\Lines\\Header** ei pea olema seotud andmeallikaga, et luua üksik sõlm väljaminevas dokumendis.
    - Element **Prefix1** loob **P1**-sümbolid, mis näitavad, et lisatud rida on aruande päise rida.
    - **ExecutionDateTime** element loob päiserea lisamisel kuupäeva ja kellaaja (sh millisekundid).
    - **Report\\Lines\\Record** element on seotud loendiga **model.Data.List**, et luua üks rida iga kirje puhul seotud loendist.
    - Element **Prefix2** loob **P2**-sümbolid, mis näitavad, et rida on lisatud maksukannete üksikasjadele.
    - **TaxAmount** element on seotud loendiga **model.Data.List.Value** (mis kuvatakse kujul **\@.Value** suhtelise tee vaates), et luua praeguse maksukande maksusumma.
    - **RunningTotal** element on maksusummade jooksva kogusumma kohatäide. Praegu ei ole sellel elemendil väljundit, kuna selle jaoks ei ole konfigureeritud ega vaikimisi määratud väärtust.
    - **ExecutionDateTime** element loob praeguse kande töötlemisel selles aruandes kuupäeva ja kellaaja (sh millisekundid).
    - Element **Report\\Lines\\Summary** ei pea olema seotud andmeallikaga, et luua üksik sõlm väljaminevas dokumendis.
    - Element **Prefix3** loob **P3**-sümbolid, mis näitavad, et lisatud rida sisaldab kogu maksuväärtust.
    - **TotalTaxAmount** element on seotud objektiga **model.Data.Summary.Total**, et luua töödeldud maksukannete summa.
    - **ExecutionDateTime** element loob kokkuvõtterea lisamisel kuupäeva ja kellaaja (sh millisekundid).

    ![Vormingu kujundaja vahekaart Vastendamine.](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Imporditud vormingu käivitamine

1. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
2. Laadige alla fail, mida veebilehitseja pakub, ja avage see läbivaatuseks.

    ![Allalaaditud näidisaruande fail.](./media/ER-DeferredSequence-Run.png)

Pange tähele, et kokkuvõtte rida 22 esitab töödeldud kannete maksu väärtuste summa. Kuna vorming on konfigureeritud kasutama **model.Data.Summary.Total**-it, mis on siduv selle summa tagastamiseks, arvutatakse summa, kutsudes välja mudeli vastendamises **TotalSum** summeerimiseks **Rühmitatud** andmeallika, *Rühmitusaluse* tüübi. Selle summeerimise arvutamiseks mudeli vastendamine itereerib üle kõigi kannete, mis on valitud **Filtreeritud** andmeallikas. Ridade 21 ja 22 käivitamise kordade võrdlemisel saate määratleda, et summa arvutamisel kulus 10 millisekundit (MS). Ridade 2 ja 21 käivitamise kordade võrdlemisel saate määratleda, et kõikide kanderidade loomisel kulus 7 millisekundit. Seetõttu vajati kokku 17 ms.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Vormingu muutmine nii, et summeerimine põhineb loodud väljundil

Kui kannete maht on praeguse näite mahust palju suurem, võib summeerimise aeg suureneda ja põhjustada jõudluse probleeme. Vormingu sätte muutmisega saate aidata vältida nende jõudluse probleeme. Kuna teil on juurdepääs maksu väärtustele, et kaasata need loodud aruandesse, saate seda teavet kasutada maksude väärtuste summeerimiseks. Lisateavet vt jaotisest [Vormingu konfigureerimine inventuuri tegemiseks ja summeerimiseks](./tasks/er-format-counting-summing-1.md).

1. Lehel **Vormingukujundaja** vahekaardil **Vorming** valige failielement **Aruanne** vormingupuus.
2. Seadke **Väljundi üksikasjade sissenõudmise** väärtuseks **Jah**. Nüüd saate seda vormingut konfigureerida, kasutades olemasoleva aruande sisu andmeallikaks, millele pääseb juurde, kasutades [andmete kogumise](er-functions-category-data-collection.md) kategoorias sisseehitatud ER funktsioone.
3. Vahekaardil **Vastendamine** valige **Report\\Lines** järjestuselement.
4. Konfigureerige avaldis **Kogutud andmevõtme nimi** kui `WsColumn`.
5. Konfigureerige avaldis **Kogutud andmevõtme väärtus** kui `WsRow`.

    ![Rea järjestuse element vormingukujundaja lehel.](./media/ER-DeferredSequence-Format3.png)

6. Valige **Report\\Lines\\Record\\TaxAmount** numbrielement.
7. Konfigureerige avaldis **Kogutud andmete võtme nimi** kui `SummingAmountKey`.

    ![TaxAmount numbrielement vormingukujundaja lehel.](./media/ER-DeferredSequence-Format4.png)

    Selle sättega saate arvestada virtuaalse töölehe täitmist, mille puhul on lahtri A1 väärtus lisatud iga töödeldud maksu kande maksusumma väärtusele.

8. Valige numbrielement **Report\\Lines\\Record\\RunningTotal** ja seejärel valige **Radigeeri valemit**.
9. Konfigureerige avaldis `SUMIF(SummingAmountKey, WsColumn, WsRow)`, kasutades sisseehitatud [SUMIF](er-functions-datacollection-sumif.md) ER funktsiooni.
10. Valige käsk **Salvesta**.

    ![SUMIF avaldis.](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Sulgege **Valemikoostaja** leht.
12. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
13. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail – summeeritud maksuväärtused.](./media/ER-DeferredSequence-Run1.png)

    Rida 21 sisaldab kõigi töödeldud kannete puhul arvutatud maksude väärtuste jooksvat kogusummat, kasutades loodud väljundit andmeallikana. See andmeallikas algab aruande algusest ja jätkub kuni viimase maksu kandeni. Rida 22 sisaldab kõigi töödeldud kannete maksuväärtuste summat, mis arvutatakse mudeli vastendamisel, kasutades *Rühmitusaluse* tüüpi andmeallikat. Pange tähele, et need väärtused on võrdsed. Seetõttu saab üksuse **Rühmitusalus** asemel kasutada väljundi baasil summeerimist. Ridade 2 ja 21 käivitamise kordade võrdlemisel saate määratleda, et kõikide kanderidade loomiseks ja summeerimiseks kulus 9 millisekundit. Seetõttu on üksikasjalike ridade loomise ja maksu väärtuste summeerimise osas muudetud vorming umbes kaks korda kiirem kui algne vorming.

14. Valige numbrielement **Report\\Lines\\Summary\\TotalTaxAmount** ja seejärel valige **Redigeeri valemit**.
15. Sisestage avaldis `SUMIF(SummingAmountKey, WsColumn, WsRow)` olemasoleva avaldise asemel.
16. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
17. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail koos redigeeritud valemiga.](./media/ER-DeferredSequence-Run2.png)

    Pange tähele, et viimase kande üksikasjade rea maksude väärtuste jooksev kogusumma võrdub nüüd kokkuvõtte rea summaga.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Sisestage aruande päisesse väljundil põhineva summeerimise väärtused

Kui näiteks peate oma aruande päises esitama maksude väärtuste summa, saate muuta oma vormingut.

1. Lehe **Vormingukujundaja** vahekaardil **Vorming** valige **Report\\Lines\\Summary** järjestuselement.
2. Valige **Nihuta üles**.
3. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
4. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail summeerimiseks aruande päise tarbeks.](./media/ER-DeferredSequence-Run3.png)

    Pange tähele, et maksu väärtuste summa kokkuvõtte real 2 võrdub nüüd 0 (null), kuna see summa arvutatakse loodud väljundi põhjal. Kui luuakse rida 2, ei sisalda loodud väljund veel kirje ridu, millel on kande üksikasjad. Saate konfigureerida selle vormingu, et lükata edasi **Report\\Lines\\Summary** järjestuselemendi käivitamine, kuni **Report\\Message\\Record** element on käivitatud kõigi maksukannete puhul.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Lükka edasi kokkuvõtte järjestuselemendi käivitamine nii, et arvutatud kogusummat kasutatakse

1. Lehe **Vormingukujundaja** vahekaardil **Vorming** valige **Report\\Lines\\Summary** järjestuselement.
2. Määrake suvand **Edasilükatud täitmine** valikule **Jah**.

    ![Kokkuvõtte järjestuselemendi edasilükatud käivitamise suvand vormingu kujundaja lehel.](./media/ER-DeferredSequence-Format5.png)

3. Valige nupp **Salvesta** ja seejärel suvand **Käivita**.
4. Laadige alla fail, mida veebilehitseja pakub, ja vaadale läbi.

    ![Allalaaditud fail – edasi lükatud käivitamine.](./media/ER-DeferredSequence-Run4.png)

    **Report\\Lines\\Summary** järjestuselementi käivitatakse nüüd ainult siis, kui kõik muud üksused, mis on pesastatud selle peamise elemendi **Report\\Lines** alusel, on käivitatud. Seetõttu käivitatakse see pärast **Report\\Lines\\Record** järjestuselemendi käivitamist **model.Data.List** andmeallika kõigi maksukannete puhul. See asjaolu näitab ridade 1, 2 ja 3 ning viimase rea täitmise aegu 22.

## <a name="additional-resources"></a>Lisaressursid

- [Vormingu konfigureerimine loendamiseks ja liitmiseks](./tasks/er-format-counting-summing-1.md)
- [ER-vormingu täitmise jälitus jõudluse probleemide tõrkeotsinguks](trace-execution-er-troubleshoot-perf.md)
- [XML-elementide käivitamise edasilükkamine ER-vormingus](er-defer-xml-element.md#Example)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
