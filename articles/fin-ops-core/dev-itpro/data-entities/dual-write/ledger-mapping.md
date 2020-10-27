---
title: Integreeritud pearaamat
description: Selles teemas kirjeldatakse pearaamatu andmete integreerimist rakenduse Finance and Operations ja teiste Dynamics 365 rakenduste vahel teenust Common Data Service kasutades.
author: robinarh
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: rhaertle
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 20c038d0d4fe8ec3e07219862f98aef970882f26
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985241"
---
# <a name="integrated-ledger"></a>Integreeritud pearaamat

[!include [banner](../../includes/banner.md)]



Ärirakenduses määratlevad pearaamatu andmed põhiseadistuse, kuidas ettevõtte äri ajab. Näiteks kirjeldavad pearaamatu andmed finantsaastat, mida ettevõte järgib, valuutasid, milles see arveldab, ja kontosid, mida see kasutab. Selles teemas kirjeldatakse nende põhiliste finantsandmete integreerimist.

## <a name="templates"></a>Mallid

Pearaamatu andmed sisaldavad põhiliste finantsiliste olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.

Finance and Operations rakendused      | Mudeljuhitud Dynamics 365 rakendus | Kirjeldus
---------------------------------|----------------------------------|------------
Valuutad                       | transactioncurrencies            |
FiscalCalendar                   | msdyn\_fiscalcalendars        |
FiscalCalendarYear               | msdyn\_fiscalcalendaryears        |
ExchRateType                     | msdyn\_exchangeratetypes        |
ExchangeRateCurrencyPair         | msdyn\_currencyexchangeratepairs        |
FiscalPeriodEntity               | msdyn\_fiscalcalendarperiods        |
MainAccountCategory              | msdyn\_mainaccountcategory        |
MainAccount                      | msdyn\_mainaccounts        |
Pearaamat                           | msdyn\_ledgers        |
ExchangeRates                    | msdyn\_currencyexchangerates        |
FinancialCalendarPeriod          | msdyn\_fiscalcalendarperiods        |
DimensionAttributeEntity         | msdyn\_dimensionattributes        |
DimensionIntegrationFormatEntity | msdyn\_financialdimensionformats        |
LedgerChartOfAccounts            | msdyn\_chartofaccounts        |


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Currency](includes/Currencies-transactioncurrencies.md)]

[!include [Fiscal calendar](includes/FiscalCalendar-msdyn-fiscalcalendars.md)]

[!include [Fiscal calendar year](includes/FiscalCalendarYear-msdyn-fiscalcalendaryears.md)]

[!include [Exchange rate types](includes/ExchRateType-msdyn-exchangeratetypes.md)]

[!include [Exchange rate pair](includes/ExchangeRateCurrencyPair-msdyn-currencyexchangeratepairs.md)]

[!include [Ledger fiscal periods](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Main account category](includes/MainAccountCategory-msdyn-mainaccountcategory.md)]

[!include [Main account](includes/MainAccount-msdyn-mainaccounts.md)]

[!include [Ledger](includes/Ledger-msdyn-ledgers.md)]

[!include [Exchange rates](includes/ExchangeRates-msdyn-currencyexchangerates.md)]

[!include [Financial Calendar Period](includes/FiscalPeriodEntity-msdyn-fiscalcalendarperiods.md)]

[!include [Dimension attribute](includes/DimensionAttributeEntity-msdyn-dimensionattributes.md)]

[!include [Dimension integration format](includes/DimensionIntegrationFormatEntity-msdyn-financialdimensionformats.md)]

[!include [Chart Of Account](includes/LedgerChartOfAccounts-msdyn-chartofaccounts.md)]




