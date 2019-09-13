---
title: Veebimüügi ja -maksete sisestamine
description: See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d42b585a61214628980cd45a859215443ed55b5
ms.sourcegitcommit: c461758290d7ddc19f0b60701368937c35ef78b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/06/2019
ms.locfileid: "1864149"
---
# <a name="posting-of-online-sales-and-payments"></a>Veebimüügi ja -maksete sisestamine

[!include[task guide banner](../includes/task-guide-banner.md)]

See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.

Internetimüügi ja maksete sisestamine on kaheosaline protsess.

- Interneti jaemüügitehingute toomine peakontorisse.
- Tellimuste sünkroonimine müügitellimuse loomiseks peakontoris.

Interneti jaemüügitehingute andmete toomist võib teha kas käsitsi, käivitades P-töö, või luues korduva pakett-töö.

### <a name="manually-running-the-p-job"></a>P-töö käivitamine käsitsi

1. Avage Kõik töökohad > Jaemüügi IT.
2. Klõpsake valikul Turustamisgraafik.
3. Valige P-0001.
4. Reguleerige vajadusel kanali andmebaasi rühmasid.
5. Klõpsake valikut Käivita kohe.
6. Klõpsake nuppu Jah.

### <a name="scheduling-a-recurring-p-job"></a>Kordiva P-töö ajastamine

1. Avage Kõik töökohad > Jaemüügi IT.
2. Klõpsake valikul Turustamisgraafik.
3. Valige P-0001.
4. Klõpsake käsku Pakett-töö loomine.
5. Klõpsake käsku Käivita taustal.
5. Luba Pakett-töötlus.
6. Klõpsake valikut Korduvus..
7. Valige suvand Lõppkuupäev puudub.
8. Sisestage väljale Loenda käitamistevaheline intervall minutites. Tavaliselt peaks see olema 5-10.
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.

Tellimusi saab sünkroonida kas käsitsi, käivitades töö "Sünkrooni tellimused" või luues korduva pakett-töö.

### <a name="manually-running-order-synchronization"></a>Käsitsi tellimuste sünkroonimise käivitamine 

Toimige ühekordseks töö "Sünkrooni tellimused" käsitsi käivitamiseks järgmiselt.

1. Avage Kõik tööruumid > Jaekaupluse rahandus.
2. Klõpsake suvandit Tellimuste sünkroonimine.
3. Valige väljal Organisatsiooni hierarhia suvand Jaekauplused piirkonniti.
    * Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.  
    * Klõpsake valiku lisamiseks noolt.  
4. Klõpsake vahekaarti Käivita taustal.
5. Keela Pakett-töötlus
6. Klõpsake valikut Korduvus.
7. Valige suvand Lõpeta pärast
8. Sisestage väljale Lõpetage pärast väärtus 1.
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.

### <a name="scheduling-recurring-order-synchronization"></a>Korduva tellimuste sünkroonimise ajastamine

See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks. Protseduur kasutab demoettevõtte USRT andmeid.

1. Avage Kõik tööruumid > Jaekaupluse rahandus.
2. Klõpsake suvandit Tellimuste sünkroonimine.
3. Valige väljal Organisatsiooni hierarhia suvand Jaekauplused piirkonniti.
    * Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.  
    * Klõpsake valiku lisamiseks noolt.  
4. Klõpsake vahekaarti Käivita taustal.
5. Luba Pakett-töötlus
6. Klõpsake valikut Korduvus.
7. Valige suvand Lõppkuupäev puudub.
8. Sisestage väljale Loenda käitamistevaheline intervall minutites. Tavaliselt peaks see olema 2-20
9. Klõpsake nuppu OK.
10. Klõpsake nuppu OK.

## <a name="data-entities-involved-in-the-process"></a>Protsessiga seotud andmeüksused

- RetailTransactionTable
- RetailTransactionAddressTrans
- RetailTransactionInfocodeTrans
- RetailTransactionTaxTrans
- RetailTransactionSalesTrans
- RetailTransactionTaxMeasure
- RetailTransactionDiscountTrans
- RetailTransactionTaxTransGTE
- RetailTransactionMarkupTrans
- RetailTransactionPaymentTrans
- RetailTransactionAttributeTrans
