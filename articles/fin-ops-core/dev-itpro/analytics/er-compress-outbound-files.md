---
title: Elektroonilises aruandluses loodavate suurte failide tihendamine
description: See artikkel selgitab, kuidas tihendada suuri dokumente, mille on loonud elektroonilise aruandluse (ER) vorming.
author: kfend
ms.date: 09/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: AX 10.0.9
ms.custom: 58771
ms.assetid: ''
ms.search.form: EROperationDesigner, ERFormatDestinationTable
ms.openlocfilehash: ebdd84cdf39e21bf3d4721b1f1545b29fe38440b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273274"
---
# <a name="compress-large-documents-that-are-generated-in-electronic-reporting"></a>Elektroonilises aruandluses loodavate suurte failide tihendamine 

[!include [banner](../includes/banner.md)]

Saate kasutada [elektroonilise aruandluse (ER) raamistikku](general-electronic-reporting.md), et konfigureerida lahendus, mis toob kandeandmed väljamineva dokumendi loomiseks. See loodud dokument võib olla üsna suur. Seda tüüpi dokumendi loomisel kasutatakse selle hoidmiseks [rakendusobjekti serveri (AOS)](../dev-tools/access-instances.md#location-of-packages-source-code-and-other-aos-configurations) mälu. Dokument tuleb seejärel alla laadida oma rakendusest Microsoft Dynamics 365 Finance. Praegu on ühe ER-is loodava dokumendi maksimaalne suurus 2 gigabaiti (GB). Lisaks on Finance'is praegu allalaaditud faili suuruse [piirang](https://fix.lcs.dynamics.com/Issue/Details?kb=4569432&bugId=453907&dbType=3) 1 GB. Seetõttu peate konfigureerima ER-i lahenduse, mis vähendab tõenäosust, et need piirangud ületatakse ja et teile näidatakse erandit **Voog oli liiga pikk** või **Ületäide või allakadu aritmeetikatehtes**.

Lahendust konfigureerides saate toimingute kujundajas ER-i vormingut kohandada, lisades juurelemendi, mille tüüp on **Kaust**, et tihendada sisu, mida selle pesastatud elemendid loovad. Tihendamine toimub „täpselt õigel ajal”, nii et maksimaalset kasutatavat mälumahtu ja allalaaditava faili suurust saab vähendada.

> [!NOTE]
> Faili tihendamine hõivab CPU kasutusest lisaprotsendi.

Lisateabe saamiseks selle lähenemise kohta viige näide selles artiklis lõpule.

## <a name="example-compress-an-outbound-document"></a>Näide: väljamineva dokumendi tihendamine

Selles näites on näha, kuidas kasutaja, kellele on määratud **süsteemiadministraatori** või **elektroonilise aruandluse funktsionaalse konsultandi** roll, saab konfigureerida ER-i vormingu loodud dokumendi tihendamiseks.

### <a name="prerequisites"></a>Eeltingimused

Enne selle artikli protseduuride sooritamist tuleb läbida järgmised sammud.

1. [Konfiguratsioonipakkuja aktiveerimine](er-defer-xml-element.md#activate-a-configuration-provider).
2. [ER-i näidiskonfiguratsioonide importimine](er-defer-xml-element.md#import-the-sample-er-configurations).
3. [Imporditud vormingu ülevaatamine](er-defer-xml-element.md#review-the-imported-format).

> [!NOTE]
> Praegu algab vormingustruktuur elemendist **Aruanne**, mille tüüp on **Fail**, ja sisaldab XML-elemente. Seetõttu luuakse väljaminev dokument XML-vormingus ja tihendamist ei kasutata.

### <a name="generate-an-er-format-to-get-an-uncompressed-document"></a>ER-i vormingu loomine tihendamata dokumendi saamiseks

1. [Imporditud vormingu käivitamine](er-defer-xml-element.md#run-the-imported-format).
2. Pange tähele, et XML-vormingus loodud dokumendi suurus on 3 kilobaiti (KB).

    ![Tihendamata väljamineva dokumendi eelvaade.](./media/er-compress-outbound-files1.png)

### <a name="modify-the-format-to-compress-the-generated-output"></a>Vormingu muutmine loodud väljundi tihendamiseks

1. Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.
2. Lehel **Konfiguratsioonid** laiendage konfiguratsioonipuus **Mudel teabe saamiseks edasilükatud elementide kohta**.
3. Valige konfiguratsioon **Vormindamine edasilükatud XML-elementide kohta teabe saamiseks**.
4. Valige **Kujundaja**, et vormingustruktuuri muuta.
5. Valige lehel **Vormingukujundaja** vahekaardil **Vorming** suvand **Lisa juur**, et lisada juure vorminguelement.
6. Valige dialoogiboksis **Lisamine** suvand **Common\\Folder**.
7. Valige **OK**, et kinnitada uue juurelemendi lisamine.
8. Valige käsk **Salvesta**.

> [!NOTE]
> Vormingustruktuur algab elemendist, mille tüüp on **Kaust**. See element loob väljundi tihendatud (ZIP-) failina. Kui elemendi **Aruanne** loodud dokument lisatakse väljaminevasse ZIP-faili, tihendatakse selle sisu väljamineva faili suuruse vähendamiseks.

### <a name="generate-an-er-format-to-get-a-compressed-document"></a>ER-i vormingu loomine tihendatud dokumendi saamiseks

1. Lehel **Vormingu kujundaja** valige suvand **Käivitamine**.
2. Laadige alla ZIP-fail, mida veebibrauseris pakutakse, ja avage see ülevaatamiseks.
3. Pange tähele, et ZIP-vormingus loodud dokumendi suurus on 1 KB.

    > [!NOTE] 
    > Selles ZIP-failis oleva XML-faili tihendusaste on 87 protsenti. Tihendusaste sõltub tihendatavatest andmetest.

    ![Tihendatud väljamineva dokumendi eelvaade.](./media/er-compress-outbound-files2.png)

> [!NOTE]
> Kui ER-i [sihtkoht](electronic-reporting-destinations.md) on konfigureeritud vorminguelemendi jaoks, mis loob väljundi (selles näites element **Aruanne**), jäetakse väljundi tihendamine vahele.

## <a name="additional-resources"></a>Lisaressursid

[Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md)

[Elektroonilise aruandluse (ER) sihtkohad](electronic-reporting-destinations.md)

[Elektroonilise aruandluse vormingus XML-elementide käivitamise edasilükkamine](er-defer-xml-element.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
