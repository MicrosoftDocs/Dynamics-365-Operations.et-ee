---
title: Pangaväljavõtte faili importimise tõrkeotsing
description: See artikkel selgitab, kuidas probleeme lahendada väikesed erinevused panga väljavõtte failis.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: kfend
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 422b2df6c4de3a948b0e62bfb70f99b12e04a8f9
ms.sourcegitcommit: 04e6c1c9400e1b582180cf3e0e4767434e736c26
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2022
ms.locfileid: "8711169"
---
# <a name="bank-statement-file-import-troubleshooting"></a>Pangaväljavõtte faili importimise tõrkeotsing

[!include [banner](../includes/banner.md)]

Oluline on, et panga väljavõtte fail ühtiks paigutusega, mida Microsoft Dynamics 365 Finantsid toetavad. Pangaväljavõtete rangete standardite tõttu töötavad enamik integratsioone õigesti. Mõnikord ei saa väljavõttefaili importida või on sel valed tulemused. Tüüpiliselt põhjustavad neid probleeme väikesed erinevused pangaväljavõtte failis. See artikkel selgitab, kuidas neid erinevusi parandada ja probleeme lahendada.

## <a name="what-is-the-error"></a>Mis on tõrge?

Kui olete proovinud importida pangaväljavõtte faili, minge tõrke leidmiseks andmehalduse töö ajalukku ja selle käivitamise üksikasjadesse. Tõrge võib aidata, osutades väljavõttele, saldole või väljavõtte reale. Siiski on ebatõenäoline, et see annab piisavalt teavet aitamaks teil tuvastada probleemi põhjustavat välja või elementi.

> [!NOTE]
> Imporditud pangaväljavõtted võivad kattuda ainult ühe ajapunkti puhul.  Näiteks kui väljavõte lõpeb 1. jaanuaril 2021 kell 00.00, võib järgmise väljavõtte alguskuupäev olla 00.00 1. jaanuaril 2021 00:00:00.

## <a name="what-are-the-differences"></a>Millised on erinevused?
Võrrelge panga faili paigutuse määratlust Finance'i impordi määratlusega ja pange tähele mis tahes võimalikke erinevusi väljades ja elementides. Võrrelge pangaväljavõtte faili seotud Finance'i näidisfailiga. ISO20022 failides peaks võimalikke erinevusi lihtne märgata olema.

## <a name="time-zone-differences-on-imported-bank-statements"></a>Ajavöönd on imporditud pangaväljavõtetes erinev
Impordifaili kuupäeva-kellaaja väärtused võivad erineda Finance and Operationsis kuvatavatest kuupäeva-kellaaja väärtustest. Selle lahknevuse vältimiseks sisestage ajavööndi eelistus lehele **Andmeallika konfigureerimine**. Lisateavet ajavööndi eelistuste sisestamise kohta leiate teemast [Täpsema panga vastavusseviimise importimisprotsessi seadistamine](set-up-advanced-bank-reconciliation-import-process.md).

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

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  Kopeerige pangaväljavõtte faili sisu ja kleepige need XML-faili, et need asendaks teksti **PASTESTATEMENTFILEHERE**.

### <a name="debug-the-xslt"></a>XSLT silumine

Lisateavet vt <https://msdn.microsoft.com/library/ms255605.aspx>.

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

Korrigeerige teisendust, et saada sobiv väli või element pangaväljavõtte failis. Seejärel vastendage see väli või element sobiva Finance'i elemendiga.

### <a name="debitcredit-indicator"></a>Deebeti/kreediti indikaator

Mõnikord võib deebetid importida kreedititena ja kreediteid võib importida deebetitena. Selle probleemi lahendamiseks peate muutma sobivat XSLT-d. Kui pangaväljavõtted tulevad mitmest pangast, veenduge, et need kõik kasutavad sama deebeti/kreediti lähenemist, või looge eraldi teisendused.

-   BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator mall
-   ISO20022XML-to-Reconcilation.xslt GetCreditDebit mall
-   MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator mall

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a>Näited pangaväljavõtte vormingutest ja tehnilistest paigutustest
Järgmises tabelis on esitatud näited tehnilise paigutuse määratlustest täiustatud panga vastavusseviimise impordifailide ja kolme seotud pangaväljavõtte näidisfailide puhul. Näidisfailid ja tehnilised paigutused saab laadida alla siit: [Impordifaili näited](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)  

| Tehnilise paigutuse määratlus                             | Pangaväljavõtte näidisfail          |
|---------------------------------------------------------|--------------------------------------|
| DynamicsAXMT940Layout                                   | [MT940StatementExample](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| DynamicsAXISO20022Layout                                | [ISO20022StatementExample](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| DynamicsAXBAI2Layout                                    | [BAI2StatementExample](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
