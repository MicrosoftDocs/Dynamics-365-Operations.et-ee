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
ms.author: ''
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 6f1a1c7329f0936147fb8f7a8e0e9fea14f7dd4b
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173011"
---
# <a name="integrated-ledger"></a><span data-ttu-id="cb2b4-103">Integreeritud pearaamat</span><span class="sxs-lookup"><span data-stu-id="cb2b4-103">Integrated ledger</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="cb2b4-104">Ärirakenduses määratlevad pearaamatu andmed põhiseadistuse, kuidas ettevõtte äri ajab.</span><span class="sxs-lookup"><span data-stu-id="cb2b4-104">In a business application, ledger data defines the core set up for how a company does business.</span></span> <span data-ttu-id="cb2b4-105">Näiteks kirjeldavad pearaamatu andmed finantsaastat, mida ettevõte järgib, valuutasid, milles see arveldab, ja kontosid, mida see kasutab.</span><span class="sxs-lookup"><span data-stu-id="cb2b4-105">For example, ledger data describes the fiscal year the company follows, the currencies it transacts in, and the accounts it uses.</span></span> <span data-ttu-id="cb2b4-106">Selles teemas kirjeldatakse nende põhiliste finantsandmete integreerimist.</span><span class="sxs-lookup"><span data-stu-id="cb2b4-106">This topic describes the integration of this core financial data.</span></span>

## <a name="templates"></a><span data-ttu-id="cb2b4-107">Mallid</span><span class="sxs-lookup"><span data-stu-id="cb2b4-107">Templates</span></span>

<span data-ttu-id="cb2b4-108">Pearaamatu andmed sisaldavad põhiliste finantsiliste olemikaartide kogumit, mis töötavad andmete suhtluse ajal koos, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="cb2b4-108">Ledger data includes a collection of core financial entity maps that work together during data interaction, as shown in the following table.</span></span>

<span data-ttu-id="cb2b4-109">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="cb2b4-109">Finance and Operations apps</span></span>      | <span data-ttu-id="cb2b4-110">Mudeljuhitud Dynamics 365 rakendus</span><span class="sxs-lookup"><span data-stu-id="cb2b4-110">Model-driven app in Dynamics 365</span></span> | <span data-ttu-id="cb2b4-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="cb2b4-111">Description</span></span>
---------------------------------|----------------------------------|------------
<span data-ttu-id="cb2b4-112">Valuutad</span><span class="sxs-lookup"><span data-stu-id="cb2b4-112">Currencies</span></span>                       | <span data-ttu-id="cb2b4-113">transactioncurrencies</span><span class="sxs-lookup"><span data-stu-id="cb2b4-113">transactioncurrencies</span></span>            |
<span data-ttu-id="cb2b4-114">FiscalCalendar</span><span class="sxs-lookup"><span data-stu-id="cb2b4-114">FiscalCalendar</span></span>                   | <span data-ttu-id="cb2b4-115">msdyn\_fiscalcalendars</span><span class="sxs-lookup"><span data-stu-id="cb2b4-115">msdyn\_fiscalcalendars</span></span>        |
<span data-ttu-id="cb2b4-116">FiscalCalendarYear</span><span class="sxs-lookup"><span data-stu-id="cb2b4-116">FiscalCalendarYear</span></span>               | <span data-ttu-id="cb2b4-117">msdyn\_fiscalcalendaryears</span><span class="sxs-lookup"><span data-stu-id="cb2b4-117">msdyn\_fiscalcalendaryears</span></span>        |
<span data-ttu-id="cb2b4-118">ExchRateType</span><span class="sxs-lookup"><span data-stu-id="cb2b4-118">ExchRateType</span></span>                     | <span data-ttu-id="cb2b4-119">msdyn\_exchangeratetypes</span><span class="sxs-lookup"><span data-stu-id="cb2b4-119">msdyn\_exchangeratetypes</span></span>        |
<span data-ttu-id="cb2b4-120">ExchangeRateCurrencyPair</span><span class="sxs-lookup"><span data-stu-id="cb2b4-120">ExchangeRateCurrencyPair</span></span>         | <span data-ttu-id="cb2b4-121">msdyn\_currencyexchangeratepairs</span><span class="sxs-lookup"><span data-stu-id="cb2b4-121">msdyn\_currencyexchangeratepairs</span></span>        |
<span data-ttu-id="cb2b4-122">FiscalPeriodEntity</span><span class="sxs-lookup"><span data-stu-id="cb2b4-122">FiscalPeriodEntity</span></span>               | <span data-ttu-id="cb2b4-123">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="cb2b4-123">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="cb2b4-124">MainAccountCategory</span><span class="sxs-lookup"><span data-stu-id="cb2b4-124">MainAccountCategory</span></span>              | <span data-ttu-id="cb2b4-125">msdyn\_mainaccountcategory</span><span class="sxs-lookup"><span data-stu-id="cb2b4-125">msdyn\_mainaccountcategory</span></span>        |
<span data-ttu-id="cb2b4-126">MainAccount</span><span class="sxs-lookup"><span data-stu-id="cb2b4-126">MainAccount</span></span>                      | <span data-ttu-id="cb2b4-127">msdyn\_mainaccounts</span><span class="sxs-lookup"><span data-stu-id="cb2b4-127">msdyn\_mainaccounts</span></span>        |
<span data-ttu-id="cb2b4-128">Pearaamat</span><span class="sxs-lookup"><span data-stu-id="cb2b4-128">Ledger</span></span>                           | <span data-ttu-id="cb2b4-129">msdyn\_ledgers</span><span class="sxs-lookup"><span data-stu-id="cb2b4-129">msdyn\_ledgers</span></span>        |
<span data-ttu-id="cb2b4-130">ExchangeRates</span><span class="sxs-lookup"><span data-stu-id="cb2b4-130">ExchangeRates</span></span>                    | <span data-ttu-id="cb2b4-131">msdyn\_currencyexchangerates</span><span class="sxs-lookup"><span data-stu-id="cb2b4-131">msdyn\_currencyexchangerates</span></span>        |
<span data-ttu-id="cb2b4-132">FinancialCalendarPeriod</span><span class="sxs-lookup"><span data-stu-id="cb2b4-132">FinancialCalendarPeriod</span></span>          | <span data-ttu-id="cb2b4-133">msdyn\_fiscalcalendarperiods</span><span class="sxs-lookup"><span data-stu-id="cb2b4-133">msdyn\_fiscalcalendarperiods</span></span>        |
<span data-ttu-id="cb2b4-134">DimensionAttributeEntity</span><span class="sxs-lookup"><span data-stu-id="cb2b4-134">DimensionAttributeEntity</span></span>         | <span data-ttu-id="cb2b4-135">msdyn\_dimensionattributes</span><span class="sxs-lookup"><span data-stu-id="cb2b4-135">msdyn\_dimensionattributes</span></span>        |
<span data-ttu-id="cb2b4-136">DimensionIntegrationFormatEntity</span><span class="sxs-lookup"><span data-stu-id="cb2b4-136">DimensionIntegrationFormatEntity</span></span> | <span data-ttu-id="cb2b4-137">msdyn\_financialdimensionformats</span><span class="sxs-lookup"><span data-stu-id="cb2b4-137">msdyn\_financialdimensionformats</span></span>        |
<span data-ttu-id="cb2b4-138">LedgerChartOfAccounts</span><span class="sxs-lookup"><span data-stu-id="cb2b4-138">LedgerChartOfAccounts</span></span>            | <span data-ttu-id="cb2b4-139">msdyn\_chartofaccounts</span><span class="sxs-lookup"><span data-stu-id="cb2b4-139">msdyn\_chartofaccounts</span></span>        |


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




