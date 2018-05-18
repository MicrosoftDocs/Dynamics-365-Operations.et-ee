---
title: "Pangaväljavõtte faili importimise tõrkeotsing"
description: "On oluline, et pangaväljavõtte fail pangast vastaks paigutusele, mida Microsoft Dynamics 365 for Finance and Operations toetab. Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti. Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused. Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis. See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada."
author: twheeloc
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: c408f30c783d58766ab93b13c589079c3ef375de
ms.contentlocale: et-ee
ms.lasthandoff: 03/26/2018

---

# <a name="bank-statement-file-import-troubleshooting"></a>Pangaväljavõtte faili importimise tõrkeotsing

[!include [banner](../includes/banner.md)]

On oluline, et pangaväljavõtte fail pangast vastaks paigutusele, mida Microsoft Dynamics 365 for Finance and Operations toetab. Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti. Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused. Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis. See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada.

<a name="what-is-the-error"></a>Mis on tõrge?
------------------

Kui olete proovinud importida pangaväljavõtte faili, minge tõrke leidmiseks andmehalduse töö ajalukku ja selle käivitamise üksikasjadesse. Tõrge võib aidata, osutades väljavõttele, saldole või väljavõtte reale. Siiski on ebatõenäoline, et see annab piisavalt teavet aitamaks teil tuvastada probleemi põhjustavat välja või elementi.

## <a name="what-are-the-differences"></a>Millised on erinevused?
Võrrelge panga faili paigutuse määratlust Finance and Operationsi impordi määratlusega ja pange tähele mis tahes võimalikke erinevusi väljades ja elementides. Võrrelge pangaväljavõtte faili seotud Finance and Operationsi näidisfailiga. ISO20022 failides peaks võimalikke erinevusi lihtne märgata olema.

## <a name="transformations"></a>Teisendused
Tüüpiliselt tuleb muudatus teha ühes kolmest teisendusest. Iga teisendus on kirjutatud spetsiifilise standardi jaoks.

| Ressursi nimi                                         | Faili nimi                          |
|-------------------------------------------------------|------------------------------------|
| BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt            | BAI2CSV-to-BAI2XML.xslt            |
| BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt | ISO20022XML-to-Reconciliation.xslt |
| BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt          | MT940TXT-to-MT940XML.xslt          |

## <a name="debugging-transformations"></a>Silumise teisendused
### <a name="adjust-the-bai2-and-mt940-files"></a>BAI2 ja MT940 failide korrigeerimine

BAI2 ja MT940 failid on tekstipõhised failid ja nõuavad korrigeerimist, et lubada XSLT-dokumendi teisenduste (Extensible Stylesheet Language Transformations) silumist Programm teeb selle korrigeerimise faili importimisel.

1.  Looge XML-fail ja kopeerige järgmine tekst sellesse.

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  Kopeerige pangaväljavõtte faili sisu ja kleepige need XML-faili, et need asendaks teksti **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>XSLT silumine

Lisateavet vt <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.

1.  Käivitage Microsoft Visual Studio.
2.  Looge konsooli rakendus.
3.  Avage sobiv XSLT.
4.  Klõpsake XLST ja selle atribuutide lehekülge.
5.  Määrake sisend pangaväljavõtte faili asukohale.
6.  Määratlege väljundi asukoht ja faili nimi.
7.  Määrake nõutud murdepunktid.
8.  Menüüs klõpsake valikuid **XML** &gt; **Käivita XSLT silumine**.

### <a name="format-the-xslt-output"></a>XSLT-väljundi vormindamine

Teisenduse käitamisel loob see väljundfaili, mida saate vaadata Visual Studios. Kasutage otseteid Ctrl+A, Ctrl+K ja Ctrl+D, et väljundfaili kiiresti vormindada.

### <a name="adjust-the-transformation"></a>Teisenduse korrigeerimine

Korrigeerige teisendust, et saada sobiv väli või element pangaväljavõtte failis. Seejärel vastendage see väli või element sobiva Finance and Operationsi elemendiga.

### <a name="debitcredit-indicator"></a>Deebeti/kreediti indikaator

Mõnikord võib deebetid importida kreedititena ja kreediteid võib importida deebetitena. Selle probleemi lahendamiseks peate muutma sobivat XSLT-d. Kui pangaväljavõtted tulevad mitmest pangast, veenduge, et need kõik kasutavad sama deebeti/kreediti lähenemist, või looge eraldi teisendused.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator mall
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit mall
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator mall

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest
Järgmises tabelis on esitatud näited tehnilise paigutuse määratlustest täiustatud panga vastavusseviimise impordifailide ja kolme seotud pangaväljavõtte näidisfailide puhul. Näidisfailid ja tehnilised paigutused saab laadida alla siit: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts  


| Tehnilise paigutuse määratlus                             | Pangaväljavõtte näidisfail          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | MT940StatementExample                |
| DynamicsAXISO20022Layout                                | ISO20022StatementExample             |
| DynamicsAXBAI2Layout                                    | BAI2StatementExample                 |






