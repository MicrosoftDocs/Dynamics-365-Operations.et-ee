---
title: Kohustuse-, vara- ja kulukannete kuvamine
description: Selles teemas selgitatakse, kuidas vaadata renditud vara kandeid. Nende kannete hulka kuuluvad rendikohustise kanded ja täitmisele kuuluvad sisestatud kulukanded.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7008891d194dc990d13a9f56db155c6990aae0c0
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442579"
---
# <a name="view-liability-asset-and-expense-transactions"></a><span data-ttu-id="91665-104">Kohustuse-, vara- ja kulukannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="91665-104">View liability, asset, and expense transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91665-105">Selles teemas selgitatakse, kuidas vaadata renditud vara kandeid.</span><span class="sxs-lookup"><span data-stu-id="91665-105">This topic explains how to view transactions for a leased asset.</span></span> <span data-ttu-id="91665-106">Nende kannete hulka kuuluvad rendikohustise kanded ja täitmisele kuuluvad sisestatud kulukanded.</span><span class="sxs-lookup"><span data-stu-id="91665-106">These transactions include lease liability transactions and executory expense transactions that have been posted.</span></span> <span data-ttu-id="91665-107">Kohustise ja kasutamisõiguse esemeks oleva vara bilansilisi väärtusi kasutatakse mitmetes aruannetes.</span><span class="sxs-lookup"><span data-stu-id="91665-107">The carrying values of the liability and right-of-use (ROU) asset are used on several reports.</span></span> <span data-ttu-id="91665-108">Neid kasutatakse ka korrigeerimise väärtuste arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="91665-108">They are also used to calculate adjustment values.</span></span>

## <a name="liability-transactions"></a><span data-ttu-id="91665-109">Kohustisekanded</span><span class="sxs-lookup"><span data-stu-id="91665-109">Liability transactions</span></span>

<span data-ttu-id="91665-110">Rendikohustise kannete vaatamiseks valige rent lehel **Rendi kokkuvõte** ja seejärel valige **Raamatud**, et avada rendikirjega seotud raamatud.</span><span class="sxs-lookup"><span data-stu-id="91665-110">To view the lease liability transactions, select a lease on the **Lease summary** page, and then select **Books** to open the books that are attached to the lease record.</span></span> <span data-ttu-id="91665-111">Pärast algset tunnustamist ja arve või intressi töölehe sisestamist valige **Kohustise tehingud**.</span><span class="sxs-lookup"><span data-stu-id="91665-111">After an initial recognition, an invoice, or an interest journal has been posted, select **Liability transactions**.</span></span>

<span data-ttu-id="91665-112">Lehel **Kohustise tehingud** kuvatakse tehinguid, mis kas suurendavad või vähendavad rendikohustist.</span><span class="sxs-lookup"><span data-stu-id="91665-112">The **Liability transactions** page shows the transactions that either increase or decrease the lease liability.</span></span> <span data-ttu-id="91665-113">Sellel lehel olevad negatiivsed summad tähistavad kreeditkandeid standardses rakenduses.</span><span class="sxs-lookup"><span data-stu-id="91665-113">Negative amounts on this page represent credit transactions in the standard application.</span></span> <span data-ttu-id="91665-114">Intressi laekumised kuvatakse negatiivsete väärtustena ja need tõstavad rendikohustise summat.</span><span class="sxs-lookup"><span data-stu-id="91665-114">Any interest accruals are shown as negative values and increase the total lease liability.</span></span> <span data-ttu-id="91665-115">Kõik rendi korrigeerimised kuvatakse kas positiivsete või negatiivsete väärtustena, sõltuvalt rendiraamatu olemusest ja mõjust.</span><span class="sxs-lookup"><span data-stu-id="91665-115">Any lease adjustments are shown as positive or negative values, depending on the nature and impact of the lease book.</span></span> <span data-ttu-id="91665-116">Valitud rendilepingu praegust rendikohustise kogusaldot kuvatakse lehe vasakus allääres.</span><span class="sxs-lookup"><span data-stu-id="91665-116">The current net total balance of the lease liability for the selected lease is shown at the bottom left of the page.</span></span>

## <a name="asset-transactions"></a><span data-ttu-id="91665-117">Vara kanded</span><span class="sxs-lookup"><span data-stu-id="91665-117">Asset transactions</span></span>

<span data-ttu-id="91665-118">Rendi varade kannete vaatamiseks valige rent lehel **Rendi kokkuvõte** ja seejärel valige **Raamatud**, et avada rendikirjega seotud rendiraamatud.</span><span class="sxs-lookup"><span data-stu-id="91665-118">To view the lease asset transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="91665-119">Seejärel valige suvand **Vara kanded**.</span><span class="sxs-lookup"><span data-stu-id="91665-119">Then select **Asset transactions**.</span></span>

<span data-ttu-id="91665-120">Lehel **Vara kanne** kuvatakse kandeid, mis kas suurendavad või vähendavad rendivara ja akumuleeritud kulumi kontosid.</span><span class="sxs-lookup"><span data-stu-id="91665-120">The **Asset transaction** page shows the transactions that either increase or decrease the lease asset and accumulated depreciation accounts.</span></span> <span data-ttu-id="91665-121">Deebetid kuvatakse positiivsete väärtustena ja kreeditid kuvatakse negatiivsete väärtustena nagu lehel **Kohustiste kanded**.</span><span class="sxs-lookup"><span data-stu-id="91665-121">Debits are shown as positive values, and credits are shown as negative values, as on the **Liability transactions** page.</span></span> <span data-ttu-id="91665-122">Sisestatud esialgne tunnustamine ja akumuleeritud kulumi järgmine summa kuvatakse vara saldona lehe allosas.</span><span class="sxs-lookup"><span data-stu-id="91665-122">The posted initial recognition and the next of accumulated depreciation are shown at the bottom left of the page as the asset balance.</span></span> 

## <a name="expenses-transactions"></a><span data-ttu-id="91665-123">Kulukanded</span><span class="sxs-lookup"><span data-stu-id="91665-123">Expenses transactions</span></span>

<span data-ttu-id="91665-124">Rendi kulukannete vaatamiseks valige rent lehel **Rendi kokkuvõte** ja seejärel valige **Raamatud**, et avada rendikirjega seotud rendiraamatud.</span><span class="sxs-lookup"><span data-stu-id="91665-124">To view the lease expense transactions, select a lease on the **Lease summary** page, and then select **Books** to open the lease books that are attached to the lease record.</span></span> <span data-ttu-id="91665-125">Seejärel valige **Kulukanded**.</span><span class="sxs-lookup"><span data-stu-id="91665-125">Then select **Expense transactions**.</span></span>

<span data-ttu-id="91665-126">Lehel **Kulukanded** kuvatakse kõik kulud, mis on rendi suhtes sisestatud, nt intressikulud, kulumi kulud ja mistahes täitekulud.</span><span class="sxs-lookup"><span data-stu-id="91665-126">The **Expense transactions** page shows all the expenses that have been posted against the lease, such as interest expenses, depreciation expenses, and any executory costs.</span></span>
