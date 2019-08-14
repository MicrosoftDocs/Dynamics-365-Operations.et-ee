---
title: Ostureskontro kodulehekülg
description: Teema annab ülevaate ostureskontrost.
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 61599e13e783fef9753aadb768cf8e6cf6b5b6a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837442"
---
# <a name="accounts-payable-home-page"></a>Ostureskontro kodulehekülg

[!include [banner](../includes/banner.md)]

Teema annab ülevaate ostureskontrost. 

Saate sisestada hankija arveid käsitsi või võtta neid vastu elektrooniliselt andmeüksuse kaudu. Kui arved on sisestatud või vastu võetud, saate neid üle vaadata ja kinnitada, kasutades arve kinnitamise töölehte või lehte **Hankija arve**. Ülevaatusprotsessi automatiseerimiseks saate kasutada arvete võrdlemist, hankija arvepoliitikaid ja töövoogu, et teatud kriteeriumitele vastavad arved kinnitataks automaatselt ning ülejäänud arved märgistataks lipuga, et autoriseeritud kasutaja need üle vaataks.

**Äriprotsessid**

[![Äriprotsess](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Ostureskontro seadistamine

Seadistage hankijagruppe, hankijaid, sisestusreegleid, mitmesuguseid maksevalikuid ning hankijate, tasude, tarnete ja sihtkohtade parameetreid, võlatähti ja muud tüüpi ostureskontro teavet. 

[Ostureskontro konfigureerimine](accounts-payable-overview.md)

[Arvestuse jaotused ja alammooduli töölehe kirjed hankija arvete puhul](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Ostureskontro ja müügireskontro välisvaluuta ümberarvutamine](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Hankija arvete konfigureerimine

Kasutage ostureskontrot, et jälgida arveid ja hankijatele tehtud väljaminevaid kulusid.

[Ostureskontro arvete võrdlemine](accounts-payable-invoice-matching.md)

[Hankija sisestusreeglid](vendor-posting-profiles.md)

[Ostureskontro arvete võrdlemise seadistamine](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Kolmesuunalised vastavusse viimise poliitikad](three-way-matching-policies.md)

[Arve võrdlemine ja kontsernisisesed ostutellimused](invoice-matching-intercompany-purchase-orders.md)

[Lahknevuste lahendamine arve kogusummade võrdlemisel](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Hankija arve töölehtede ja arve kinnitustöölehtede vaikevastaskontod](default-offset-accounts-vendor-invoice-journals.md)

[Mobiilsed arvete heakskiidud](mobile-invoice-approvals.md)

[Hankija koostöö arve tööruum](vendor-portal-invoicing-workspace.md)

[Hankija arve automatiseerimine](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Hankijamaksete konfigureerimine 

Määrake igale kasutaja määratud makseviisile süsteemi määratud maksetüüp, nt tšekk, elektrooniline makse või võlatäht. Maksetüübid on valikulised, kuid kasulikud elektroonilist maksetüüpi kinnitades ja kui peate kiiresti otsustama, millist maksetüüpi makse kasutab. 

[Hankija maksete tööruum](vendor-payments-workspace.md)

[Hankija maksetasude määratlemine](tasks/define-vendor-payment-fees.md)

[Hankija maksetingimuste määratlemine](tasks/define-vendor-payment-terms.md)

[Positiivse makse ülevaade](positive-pay-overview.md)

[Positiivse makse failide seadistamine ja loomine](set-up-generate-positive-pay-files.md)

[Hankija maksete loomine maksesoovituse abil](create-vendor-payments-payment-proposal.md)

[Hankija osalises summas maksed](vendor-payments-partial-amount.md)

[Hankija makse arvutatud skontost suurema skonto võtmine](take-discount-more-calculated-discount-vendor-payment.md)

[Skonto võtmine väljaspool skonto perioodi](take-cash-discount-outside-cash-discount-timeframe.md)

[Hankija arvete elektrooniline aruandlus](electronic-reporting-sample-vendor-checks.md)

[Hankija makse storneerimine](reverse-vendor-payment.md)

[Ettemaksuarvete ja ettemaksete ülevaade](prepayments-invoices-vs-prepayments.md)

[Ostureskontro tsentraliseeritud maksed](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Tasakaalustused

Järgmised teemad annavad teavet tasakaalustuste kohta. Tasakaalustamine tähendab maksete tasakaalustamist arvetega. 

[Tasakaalustuse konfigureerimine](../cash-bank-management/configure-settlement.md)

[Osalise hankijamakse tasakaalustamine enne allahindluse kuupäeva](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Hankija osalise makse, millel on hankija kreeditarvetel allahindlusi, tasakaalustamine](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Mitme allahindlusperioodiga osalise hankijamakse tasakaalustamine](settle-partial-vendor-payment-multiple-discount-periods.md)

[Osalise hankijamakse või lõpliku makse tasakaalustamine enne allahindlust](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Üksik mitme kliendi- või hankijakirjega kanne](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Lisaressursid

#### <a name="whats-new-and-in-development"></a>Mis on uut ja mis on arendamisel?

Avage [Microsoft Dynamics 365 väljalaskemärkmed](https://go.microsoft.com/fwlink/?linkid=2010158), et näha, milliseid uusi funktsioone kavandatakse. 

#### <a name="blogs"></a>Ajaveebid

Arvamusi, uudiseid ja muud teavet ostureskontro ning muude lahenduste kohta leiate [Microsoft Dynamics 365 ajaveebist](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) ja [ajaveebist Microsoft Dynamics 365 Finance and Operations – Financials](https://community.dynamics.com/365/financeandoperations/b/financials).

[Microsoft Dynamics Operationsi partnerite kogukonna ajaveeb](https://community.dynamics.com/partner/b/operationspartnercommunityblog) on Microsoft Dynamicsi partnerite jaoks kõikehõlmav ressurss, kust nad saavad teada, mis on uut ja põnevat rakenduses MBS Operations.

#### <a name="community-blogs"></a>Kogukonna ajaveebid

[Võlgnevuste haldamine rakenduses Dynamics 365 for Finance and Operations](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Tegevusjuhised
Lisaspikker on saadaval Finance and Operationsis tegevusjuhistena. Tegevuse juhistele juurdepääsemiseks klõpsake ükskõik millisel lehel nuppu Spikker.

#### <a name="videos"></a>Videod

Vaadake õppevideoid, mis on saadaval [Microsoft Dynamics 365 YouTube’i kanalil](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).




