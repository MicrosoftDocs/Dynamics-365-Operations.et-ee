---
title: Käibemaksu täpsustus pearaamatu kannete aruande alusel
description: See teema selgitab, kuidas kasutada käibemaksu täpsustust pearaamatu kannete aruande alusel, et vaadata ja printida teavet pearaamatu kannete kohta, mille jaoks käibemaks arvutatakse.
author: ericwang
manager: Ann Beebe
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-19
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b90ae491605bf59b93137936a2804c4b84c6e1b7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204878"
---
# <a name="sales-tax-specification-by-ledger-transaction-report"></a><span data-ttu-id="94b3e-103">Käibemaksu täpsustus pearaamatu kannete aruande alusel</span><span class="sxs-lookup"><span data-stu-id="94b3e-103">Sales tax specification by ledger transaction report</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="94b3e-104">See teema selgitab, kuidas kasutada **käibemaksu täpsustust pearaamatu kannete** aruande alusel, et vaadata ja printida teavet pearaamatu kannete kohta, mille jaoks käibemaks arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="94b3e-104">This topic explains how to use the **Sales tax specification by ledger transaction** report to view and print information about ledger transactions that sales tax is calculated for.</span></span>

## <a name="tax-accounts-vs-non-tax-accounts"></a><span data-ttu-id="94b3e-105">Maksukontod vs mitte-maksukontod</span><span class="sxs-lookup"><span data-stu-id="94b3e-105">Tax accounts vs. non-tax accounts</span></span>

<span data-ttu-id="94b3e-106">**Käibemaksu täpsustus pearaamatu kannete** aruande alusel näitab nii maksukontode kui ka mitte-maksukontode kandeid.</span><span class="sxs-lookup"><span data-stu-id="94b3e-106">The **Sales tax specification by ledger transaction** report shows tax transactions for both tax accounts and non-tax accounts.</span></span> <span data-ttu-id="94b3e-107">Need kontod on kategoriseeritud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="94b3e-107">These accounts are categorized in the following way:</span></span>

- <span data-ttu-id="94b3e-108">**Maksukonto** – kontot peetakse maksukontoks, kui maksukanne on sisestatud ja **Käibemaksu** töölehe real olev põhikonto on maksukonto, nt tasumisele kuuluva käibemaksu konto või saadaoleva käibemaksu konto.</span><span class="sxs-lookup"><span data-stu-id="94b3e-108">**Tax account** – An account is considered a tax account when a tax transaction is posted, and the main account on the **Sales Tax** journal line is a tax account, such as a sales tax payable account or a sales tax receivable account.</span></span>
- <span data-ttu-id="94b3e-109">**Mitte-maksukonto** – kontot peetakse mitte-maksukontoks, kui maksukanne on sisestatud ja algse kande põhikonto on mitte-maksukonto, näiteks ja Käibemaksu töölehe real olev põhikonto on maksukonto, nt tulukonto või kulukonto.</span><span class="sxs-lookup"><span data-stu-id="94b3e-109">**Non-tax account** – An account is considered a non-tax account when a tax transaction is posted, and the main account on the original transaction is a non-tax account, such as a revenue account or an expense account.</span></span>

<span data-ttu-id="94b3e-110">Maksukontode korral näitavad veerud **Päritolu**, **Saadaolev käibemaks** ja **Tasumisele kuuluv käibemaks** aruandel väärtust **0** (null).</span><span class="sxs-lookup"><span data-stu-id="94b3e-110">For tax accounts, the **Origin**, **Sales tax receivable**, and **Sales tax payable** columns on the report show **0** (zero).</span></span> <span data-ttu-id="94b3e-111">Mitte-maksukontodekorral näitavad need veerud summasid.</span><span class="sxs-lookup"><span data-stu-id="94b3e-111">For non-tax accounts, those columns show amounts.</span></span>

## <a name="filtering-the-data-on-the-report"></a><span data-ttu-id="94b3e-112">Aruande andmete filtreerimine</span><span class="sxs-lookup"><span data-stu-id="94b3e-112">Filtering the data on the report</span></span>

<span data-ttu-id="94b3e-113">Aruande loomisel on saadaval järgmised vaikeväljad.</span><span class="sxs-lookup"><span data-stu-id="94b3e-113">When you generate the report, the following default fields are available.</span></span> <span data-ttu-id="94b3e-114">Saate neid välju kasutada aruandel kuvatavate andmete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="94b3e-114">You can use these fields to filter the data that is shown on the report.</span></span>

| <span data-ttu-id="94b3e-115">Väli</span><span class="sxs-lookup"><span data-stu-id="94b3e-115">Field</span></span>                      | <span data-ttu-id="94b3e-116">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="94b3e-116">Description</span></span> |
|----------------------------|-------------|
| <span data-ttu-id="94b3e-117">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="94b3e-117">Date</span></span>                       | <span data-ttu-id="94b3e-118">Kasutage jaotiste **Alates** ja **Kuni** välju, et määratleda maksukannete kuupäevavahemik.</span><span class="sxs-lookup"><span data-stu-id="94b3e-118">Use the fields in the **From** and **To** sections to define a date range for the tax transactions.</span></span> |
| <span data-ttu-id="94b3e-119">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="94b3e-119">Main account</span></span>               | <span data-ttu-id="94b3e-120">Kasutage jaotiste **Alates** ja **Kuni** välju, et määratleda põhikontode vahemik.</span><span class="sxs-lookup"><span data-stu-id="94b3e-120">Use the fields in the **From** and **To** sections to define a range of main accounts.</span></span> |
| <span data-ttu-id="94b3e-121">Käibemaksukood</span><span class="sxs-lookup"><span data-stu-id="94b3e-121">Sales tax code</span></span>             | <span data-ttu-id="94b3e-122">Kasutage jaotiste **Alates** ja **Kuni** välju, et määratleda käibemaksukoodide vahemik.</span><span class="sxs-lookup"><span data-stu-id="94b3e-122">Use the fields in the **From** and **To** sections to define a range of sales tax codes.</span></span> |
| <span data-ttu-id="94b3e-123">Grupeerimine</span><span class="sxs-lookup"><span data-stu-id="94b3e-123">Grouping</span></span>                   | <span data-ttu-id="94b3e-124">Valige, kas aruanne peaks olema grupeeritud pearaamatu konto või käibemaksukoodi järgi.</span><span class="sxs-lookup"><span data-stu-id="94b3e-124">Select whether the report should be grouped by ledger account or sales tax code.</span></span> |
| <span data-ttu-id="94b3e-125">Vahesumma käibemaksukoodide kaupa</span><span class="sxs-lookup"><span data-stu-id="94b3e-125">Subtotal by sales tax code</span></span> | <span data-ttu-id="94b3e-126">Seadistage see suvand olekusse **Jah**, et kuvada vahesummad käibemaksukoodide kaupa.</span><span class="sxs-lookup"><span data-stu-id="94b3e-126">Set this option to **Yes** to show subtotals by sales tax code.</span></span> |
| <span data-ttu-id="94b3e-127">Ainult kogusummad</span><span class="sxs-lookup"><span data-stu-id="94b3e-127">Totals only</span></span>                | <span data-ttu-id="94b3e-128">Seadistage see suvand olekusse **Jah**, et kuvada ainult kogusummasid.</span><span class="sxs-lookup"><span data-stu-id="94b3e-128">Set this option to **Yes** to show only totals.</span></span> |
| <span data-ttu-id="94b3e-129">Ainult põhikontod</span><span class="sxs-lookup"><span data-stu-id="94b3e-129">Main accounts only</span></span>         | <span data-ttu-id="94b3e-130">Seadistage see suvand olekusse **Jah**, et kaasata aruandesse ainult põhikontod.</span><span class="sxs-lookup"><span data-stu-id="94b3e-130">Set this option to **Yes** to include only main accounts on the report.</span></span> |

## <a name="showing-only-non-tax-accounts-on-the-report"></a><span data-ttu-id="94b3e-131">Aruandes ainult mitte-maksukontode kuvamine</span><span class="sxs-lookup"><span data-stu-id="94b3e-131">Showing only non-tax accounts on the report</span></span>

<span data-ttu-id="94b3e-132">Aruandes ainult mitte-maksukontode kuvamiseks seadistage filtri tingimus, nt asterisk (\*), nii nagu näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="94b3e-132">To show only non-tax accounts on the report, set up a filter condition, such as an asterisk (\*), as shown in the following illustration.</span></span>

![Mitte-maksukontosid näitav aruanne](media/taxspecperledgertrans.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]