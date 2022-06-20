---
title: Hankija arve üksused
description: See artikkel annab teavet hankija arve üksuste kohta, mis võimaldavad kulutüübi koode konfigureerida sisemiste kulude või väliselt tuletatud kulude jaoks.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2022-05-27
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 171b383e1549babd76fd18e4932436a66aa62cc1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873923"
---
# <a name="vendor-invoice-entities"></a>Hankija arve üksused

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- KFM: Preview until GA with 10.0.28 -->

Väljaminev **kulumoodul** võimaldab kulutüübikoode konfigureerida sisemiste kulude või väliselt tuletatud kulude jaoks. Kui kulu on ettevõtteväline, eeldatakse arvet teenuse pakkujalt. See arve töödeldakse arve töölehena, mida saab seostada reisiga ja arve väärtust saab jaotada reisi ühe või mitme kulu vahel.

Hankija arve üksused võimaldavad tööleherea väärtuse jaotamist läbi reisi ühe või mitme kulutüübikoodiga kulu.

Kulu saab eraldada ainult siis, kui arve töölehe päis ja arve töölehe read on olemas.

## <a name="vendor-voyage-cost-allocations-itmledgerjournalcostlinesvoyagesentity"></a>Hankija reisikulude eraldamised (ITMLedgerJournalCostLinesVoyagesEntity)

Hankija reisi kulude eraldamiste andmeüksus võimaldab hankija arve rea eraldada läbi ühe või mitme reisi kulualale rakendatud kulu. Üksus toetab seda `ITMLedgerJournalCostLinesVoyagesEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Eraldatud summa | ITMLedgerJournalCostLines.Amount | Numbriline(32, 6) | Nr | Nr |
| Kulukande rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe rea number | ITMLedgerJournalCostLines.RefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe number | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jah** | Nr |
| Reis | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |

## <a name="vendor-shipping-container-cost-allocations-itmledgerjournalcostlinescontainersentity"></a>Hankija saadetise konteineri kulude eraldamised (ITMLedgerJournalCostLinesContainersEntity)

Hankija saadetise konteineri kulude eraldamise andmeüksus võimaldab hankija arve reale eraldada ühe või mitme saadetise konteineri kulualale rakendatud kulu vahel. Üksus toetab seda `ITMLedgerJournalCostLinesContainersEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Eraldatud summa | ITMLedgerJournalCostLines.Amount | Numbriline(32, 6) | Nr | Nr |
| Saatmiskonteiner | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |
| Kulukande rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe rea number | ITMLedgerJournalCostLines.RefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe number | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jah** | Nr |
| Reis | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |

## <a name="vendor-folio-cost-allocations-itmledgerjournalcostlinesfoliosentity"></a>Hankija foolio kulude eraldamised (ITMLedgerJournalCostLinesFo pealkirjadEntity)

Hankija foolio kulude eraldamise andmeüksus võimaldab hankija arve rea eraldada läbi ühe või mitme kulu, mida rakendatakse foolio kulualale. Üksus toetab seda `ITMLedgerJournalCostLinesFoliosEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Eraldatud summa | ITMLedgerJournalCostLines.Amount | Numbriline(32, 6) | Nr | Nr |
| Kulukande rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Foolio | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |
| Töölehe rea number | ITMLedgerJournalCostLines.RefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe number | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jah** | Nr |

## <a name="vendor-purchase-order-cost-allocations-itmledgerjournalcostlinespurchtableentity"></a>Hankija ostutellimuse kulude eraldamised (ITMLedgerJournalCostLinesPurchTableEntity)

Hankija ostutellimuse kulude eraldamise andmeüksus võimaldab hankija arve rea jaotada läbi ühe või mitme ostutellimuse kulualale rakendatud kulu. Üksus toetab seda `ITMLedgerJournalCostLinesPurchTableEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Eraldatud summa | ITMLedgerJournalCostLines.Amount | Numbriline(32, 6) | Nr | Nr |
| Kulukande rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe rea number | ITMLedgerJournalCostLines.RefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe number | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jah** | Nr |
| Ostutellimus | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |

## <a name="vendor-item-cost-allocations-itmledgerjournalcostlinespurchlineentity"></a>Hankija kauba kulude eraldamised (ITMLedgerJournalCostLinesPurchLineEntity)

Hankija kauba kulude eraldamise andmeüksus võimaldab hankija arve rea jaotada läbi ühe või mitme kulu, mida rakendatakse kauba kulualale. Kauba kuluala katab ostutellimuse rea kulusid. Üksus toetab seda `ITMLedgerJournalCostLinesPurchLineEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Eraldatud summa | ITMLedgerJournalCostLines.Amount | Numbriline(32, 6) | Nr | Nr |
| Kulukande rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe rea number | ITMLedgerJournalCostLines.RefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe number | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jah** | Nr |
| Ostutellimus | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |
| Ostutellimuse rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |

## <a name="vendor-transfer-order-line-cost-allocations-itmledgerjournalcostlinestransferlineentity"></a>Hankija üleviimistellimuse rea kulude eraldamised (ITMLedgerJournalCostLinesTransferLineEntity)

Hankija üleviimistellimuse rea kulude eraldamise andmeüksus võimaldab hankija arve rea eraldada üle ühe või mitme kulu, mida rakendatakse ülekanderea kulualale. Üksus toetab seda `ITMLedgerJournalCostLinesTransferLineEntity` funktsiooni. Järgmises tabelis loetletakse väljad ja vastendamised, mis selle üksuse teete.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Eraldatud summa | ITMLedgerJournalCostLines.Amount | Numbriline(32, 6) | Nr | Nr |
| Kulukande rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe rea number | ITMLedgerJournalCostLines.RefRecId | Numbriline(32, 16) | **Jah** | Nr |
| Töölehe number | ITMLedgerJournalCostLines.RefRecId | Nvarchar(20) | **Jah** | Nr |
| Üleviimistellimus | ITMLedgerJournalCostLines.CostTransRefRecId | Nvarchar(20) | **Jah** | Nr |
| Üleviimistellimuse rea number | ITMLedgerJournalCostLines.CostTransRefRecId | Numbriline(32, 16) | **Jah** | Nr |

### <a name="reference-table"></a>Viitetabel

Reisi kuluread on otseses seoses kulukande kirjega. Kirje sisaldab viitetabeli **ID väärtust**. See väärtus on kordumatu iga kuluala puhul (reisimine, konteineri lähetamine jne). Kui andmeüksuste abil loodud andmetele viidatakse kindlatele tabelinumbritele, tükeldatakse üksused viitetabeli **ID-väärtuste** alusel.

Viitetabeli () ja kandetüübi (`RefTableId``TransType`) väärtused on kas väljaminev omahinna osturea või väljaminev kulu üleviimisrea üksuse valikus vaikimisi.

## <a name="vendor-invoice-journal-lines-vendorinvoicejournallineentity"></a>Hankija arve töölehe read (VendorInvoiceJournalLineEntity)

Enne töölehe rea väärtuse eraldamist ühele või **mitmele** kulude moodulis Väljaminev kulu tuleb töölehe rida seostada kulualaga. Selle funktsiooni toetamiseks lisab väljaminev **kulumoodul** töölehe ridade tabelile () uued väljad`LedgerJournalTrans`.

### <a name="fields-added-to-the-vendor-invoice-journal-line-entity"></a>Hankija arve tööleherea üksusele lisatud väljad

Järgmises tabelis loetletakse väljad, mida **väljaminev** kulumoodul lisab hankija arve tööleherea üksusele (`VendorInvoiceJournalLineEntity`). Need väljad võimaldavad süsteemil luua tööleheridu ja eraldada neile kulusid.

| Nimi | Vastendamine | Andmetüüp | Võti | Kohustuslik |
|---|---|---|---|---|
| Kuluala | LedgerJournalTrans.ITMCostArea | Int | Nr | Nr |
| Kulutüübi kood | LedgerJournalTrans.ITMCostTypeId | Nvarchar(20) | Nr | Nr |

### <a name="mainoffset-account"></a>Põhi-/vastaskonto

Väljaminev kulu reisimine on seotud arve töölehe rea põhi-/vastaskonto määratletakse kulutüübi koodiga. Kui kulutüübi kood lisatakse arve töölehe reale, kasutatakse koodi kliiringukontot kas põhikontona või vastaskontona, sõltuvalt stsenaariumist:

- **Üherealine tööleht** – kui põhikonto (teisisõnu hankijakonto) on määratletud ja kulutüübi kood on antud, sisestatakse vastaskontole selle kulutüübi koodi kliiringukonto väärtus.
- **Mitme reaga tööleht** – kui põhikontot ei ole määratletud, kuid esitatakse kulutüübi kood, sisestatakse põhikontole selle kulutüübi koodi kliiringukonto väärtus. Hankijat kredittav töölehe rida ei viita kulutüübi koodile.

## <a name="sequencing"></a>Järjestus

Töölehe ja töölehe ridade tabelite vaheliste sõltuvuste tõttu tuleb esmalt luua reisikirje. Reisiridu saab luua ainult pärast reisi, konteineri saatmist ja fool konteineri loomist.

Reisiarve eraldamiseks peab süsteem töötlema üksused järgmises järjekorras:

1. Arve töölehe päis (`VendInvoiceJournalHeaderEntity`)
1. Arve töölehe rida (`VendInvoiceJournalLineEntity`)
1. Väljaminev kulueraldused (`ITMLedgerJournalEntities`)
