---
title: Välisvaluuta ümberarvutamine pangakontode jaoks
description: Selles teemas kirjeldatakse välisvaluuta ümberarvutamist pangakontode jaoks.
author: ShylaThompson
manager: AnnBe
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Czech Republic, Estonia, Latvia, Lithuania, Poland
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3cc02e12e619342097891fdd0c851176ee0bcd4d
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/03/2019
ms.locfileid: "2552352"
---
# <a name="foreign-currency-revaluation-for-bank-accounts"></a><span data-ttu-id="2de40-103">Välisvaluuta ümberarvutamine pangakontode jaoks</span><span class="sxs-lookup"><span data-stu-id="2de40-103">Foreign currency revaluation for bank accounts</span></span>

[!include [banner](../includes/banner.md)]

## <a name="revalue-foreign-currency-amounts-for-bank-account-transactions"></a><span data-ttu-id="2de40-104">Välisvaluuta summade ümberarvutamine pangakonto kannete jaoks</span><span class="sxs-lookup"><span data-stu-id="2de40-104">Revalue foreign currency amounts for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2de40-105">See jaotis kehtib ainult nende juriidiliste isikute puhul, kelle esmane aadress on Poolas.</span><span class="sxs-lookup"><span data-stu-id="2de40-105">This section applies only to legal entities that have a primary address in Poland.</span></span>

<span data-ttu-id="2de40-106">Välisvaluuta summasid saate pangakonto kannete jaoks ümber arvutada.</span><span class="sxs-lookup"><span data-stu-id="2de40-106">You can revalue foreign currency amounts for bank transactions.</span></span> <span data-ttu-id="2de40-107">Seejärel saate luua aruande, et vaadata pangakandeid, mille puhul on tehtud välisvaluuta ümberarvutamise korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="2de40-107">You can then create a report to view the bank transactions that have adjustments for foreign currency revaluations.</span></span>

1. <span data-ttu-id="2de40-108">Valige **Sularaha- ja pangahaldus** &gt; **Perioodilised ülesanded** &gt; **Pank – vahetuskursi korrigeerimine (FIFO/LIFO)**.</span><span class="sxs-lookup"><span data-stu-id="2de40-108">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Bank - Exchange adjustment (FIFO/LIFO)**.</span></span>
2. <span data-ttu-id="2de40-109">Sisestage väljale **Kuupäeval** ümberarvutamise lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="2de40-109">In the **On date** field, enter an end date for the revaluation.</span></span> <span data-ttu-id="2de40-110">Arvutamisse kaasatakse ainult kanded, mille kuupäev on varasem määratud kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="2de40-110">The calculation includes only transactions that have a date that is before the specified date.</span></span>
3. <span data-ttu-id="2de40-111">Pangakonto lisamiseks valige **Kaasatavad kirjed** &gt; **Filtreeri** &gt; **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2de40-111">Select **Records to include** &gt; **Filter** &gt; **Add** to add a bank account.</span></span> <span data-ttu-id="2de40-112">Kui te ei määra pangakontot, hinnatakse kõikide pangakontode summad ümber.</span><span class="sxs-lookup"><span data-stu-id="2de40-112">If you don't specify a bank account, amounts are revalued for all bank accounts.</span></span>
4. <span data-ttu-id="2de40-113">Päringulehe sulgemiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2de40-113">Select **OK** to close the query page.</span></span>
5. <span data-ttu-id="2de40-114">Kõigi avatud perioodide välisvaluuta summade ümberarvutamiseks valige lehel **Välisvaluuta ümberarvutamine** märkeruut **Ümberarvutus**.</span><span class="sxs-lookup"><span data-stu-id="2de40-114">On the **Foreign currency revaluation** page, select the **Recalculation** check box to revalue foreign currency amounts for all open periods.</span></span>

## <a name="create-a-report-to-view-bank-transactions-that-have-adjustments-for-foreign-currency-revaluations"></a><span data-ttu-id="2de40-115">Aruande loomine, et vaadata pangakandeid, mille puhul on tehtud välisvaluuta ümberarvutamise korrigeerimisi</span><span class="sxs-lookup"><span data-stu-id="2de40-115">Create a report to view bank transactions that have adjustments for foreign currency revaluations</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2de40-116">See jaotis kehtib ainult nende juriidiliste isikute puhul, kelle esmane aadress on Poolas.</span><span class="sxs-lookup"><span data-stu-id="2de40-116">This section applies only to legal entities that have a primary address in Poland.</span></span>

1. <span data-ttu-id="2de40-117">Valige **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Pank – valuutakursi korrigeerimisaruanne**.</span><span class="sxs-lookup"><span data-stu-id="2de40-117">Select **Cash and bank management** &gt; **Inquiries and reports** &gt; **Bank - Exchange adjustment report**.</span></span>
2. <span data-ttu-id="2de40-118">Ühe või mitme pangakonto teabe vaatamiseks valige **Kaasatavad kirjed** &gt; **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="2de40-118">Select **Records to include** &gt; **Filter** to find one or more bank accounts to view information for.</span></span>
3. <span data-ttu-id="2de40-119">Valikuline: valige pangakonto väljal **Pangakonto**.</span><span class="sxs-lookup"><span data-stu-id="2de40-119">Optional: In the **Bank account** field, select a bank account.</span></span> <span data-ttu-id="2de40-120">Kui jätate selle välja tühjaks, kaasatakse aruandesse kõigi pangakontode pangakannete üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="2de40-120">If you leave this field blank, the report includes bank transaction details for all bank accounts.</span></span>
4. <span data-ttu-id="2de40-121">Aruande loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2de40-121">Select **OK** to generate the report.</span></span> 

## <a name="calculate-exchange-rate-adjustments-for-bank-account-transactions"></a><span data-ttu-id="2de40-122">Vahetuskursi korrigeerimiste arvutamine pangakonto kannete jaoks</span><span class="sxs-lookup"><span data-stu-id="2de40-122">Calculate exchange rate adjustments for bank account transactions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2de40-123">See jaotis kehtib ainult nende juriidiliste isikute puhul, kelle esmane aadress on Tšehhi Vabariigis, Eestis, Leedus või Lätis.</span><span class="sxs-lookup"><span data-stu-id="2de40-123">This section applies only to legal entities that have a primary address in the Czech Republic, Estonia, Lithuania, or Latvia.</span></span>

<span data-ttu-id="2de40-124">Teil tuleb ümber hinnata ja reguleerida pangakontosid, kui arvestusvaluuta ja aruandlusvaluuta vahetuskurss erinevad.</span><span class="sxs-lookup"><span data-stu-id="2de40-124">You must revalue and adjust bank accounts if there is a difference in the exchange rate between the accounting currency and the reporting currency.</span></span> <span data-ttu-id="2de40-125">See ülesanne aitab teil arvutada õige saldo pangakontode arvestusvaluuta ja aruandlusvaluuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="2de40-125">This task helps you calculate the correct balance in both the accounting currency and the reporting currency for the bank accounts.</span></span>

1. <span data-ttu-id="2de40-126">Valige **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2de40-126">Select **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span>
2. <span data-ttu-id="2de40-127">Valige vahekaardi **Numbriseeriad** väljal **Viide** numbriseeria viitele **Pank - vahetuskursi korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="2de40-127">On the **Number sequences** tab, in the **Reference** field, select a number sequence for the **Bank - Exchange adjustment** reference.</span></span>
3. <span data-ttu-id="2de40-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2de40-128">Close the page.</span></span>
4. <span data-ttu-id="2de40-129">Valige **Pearaamat** &gt; **Seadistus** &gt; **Valuuta** &gt; **Valuuta vahetuskursi määrad**.</span><span class="sxs-lookup"><span data-stu-id="2de40-129">Select **General ledger** &gt; **Setup** &gt; **Currency** &gt; **Currency exchange rates**.</span></span> <span data-ttu-id="2de40-130">Lehel **Valuuta vahetuskursi määrad** saate määrata kahe valuuta või valuutapaari vahetuskursi.</span><span class="sxs-lookup"><span data-stu-id="2de40-130">On the **Currency exchange rates** page, you can define the exchange rate between two currencies or a currency pair.</span></span>
5. <span data-ttu-id="2de40-131">Kui olete lõpetanud, sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2de40-131">When you've finished, close the page.</span></span>
6. <span data-ttu-id="2de40-132">Valige **Pearaamat** &gt; **Seadistus** &gt; **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="2de40-132">Select **General ledger** &gt; **Setup** &gt; **Ledger**.</span></span> <span data-ttu-id="2de40-133">Valige väljadel **Realiseerimata kasum** ja **Realiseerimata kahjum** peamine konto, mille jaoks vahetuskursse sisestate.</span><span class="sxs-lookup"><span data-stu-id="2de40-133">In the **Unrealized gain** and **Unrealized loss** fields, select the main account that the exchange rates are posted for.</span></span>
7. <span data-ttu-id="2de40-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="2de40-134">Close the page.</span></span>
8. <span data-ttu-id="2de40-135">Valige **Sularaha- ja pangahaldus** &gt; **Perioodilised ülesanded** &gt; **Välisvaluuta ümberarvutamine**.</span><span class="sxs-lookup"><span data-stu-id="2de40-135">Select **Cash and bank management** &gt; **Periodic tasks** &gt; **Foreign currency revaluation**.</span></span>
9. <span data-ttu-id="2de40-136">Väljal **Kuupäeval** valige ümberarvutamise või korrigeerimise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="2de40-136">In the **On date** field, select the revaluation date or adjustment date.</span></span>
10. <span data-ttu-id="2de40-137">Valige praegune valuutakood väljal **Valuutast**.</span><span class="sxs-lookup"><span data-stu-id="2de40-137">In the **From currency** field, select the current currency code.</span></span> <span data-ttu-id="2de40-138">Valige valuuta, millesse korrigeerimine tuleks teha, väljal **Valuutaks**.</span><span class="sxs-lookup"><span data-stu-id="2de40-138">In the **To currency** field, select the currency that the adjustment should be made to.</span></span>
11. <span data-ttu-id="2de40-139">Valige pangakonto leidmiseks **Kaasatavad kirjed** &gt; **Filtreeri** ja seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="2de40-139">Select **Records to include** &gt; **Filter** to find the bank account, and then select **OK**.</span></span>
12. <span data-ttu-id="2de40-140">Tehke lehel **Välisvaluuta ümberarvutamine** valik **OK**.</span><span class="sxs-lookup"><span data-stu-id="2de40-140">On the **Foreign currency revaluation** page, select **OK**.</span></span> <span data-ttu-id="2de40-141">Arvutatakse valitud kuupäeva pangakonto kannete korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="2de40-141">The adjustment for the bank account transactions on the selected date is calculated.</span></span>

> [!NOTE]
> <span data-ttu-id="2de40-142">Pearaamatus saate vaadata kahte eraldiseisvat kannet: üks on arvestusvaluuta ja teine aruandlusvaluuta jaoks.</span><span class="sxs-lookup"><span data-stu-id="2de40-142">In the general ledger, you can view two separate transactions: one for the accounting currency and one for the reporting currency.</span></span>
