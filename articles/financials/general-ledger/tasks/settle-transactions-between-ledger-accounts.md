---
title: Pearaamatukontode kannete tasakaalustamine
description: See protseduur selgitab, kuidas tasakaalustada kandeid pearaamatu kontode vahel ja tühistada pearaamatu tasakaalustust.
author: aprilolson
manager: AnnBe
ms.date: 10/03/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement, LedgerTrialBalanceListPage, LedgerTrialBalanceListPageBalanceParms, LedgerTransAccount, LedgerTransSettled
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4aff64fa1c017f295752e913de7fb320f0662ef8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568116"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="84982-103">Pearaamatukontode kannete tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="84982-103">Settle transactions between ledger accounts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="84982-104">See protseduur selgitab, kuidas tasakaalustada kandeid pearaamatu kontode vahel ja tühistada pearaamatu tasakaalustust.</span><span class="sxs-lookup"><span data-stu-id="84982-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="84982-105">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="84982-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="84982-106">Kande tasakaalustamine pearaamatukontode vahel</span><span class="sxs-lookup"><span data-stu-id="84982-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="84982-107">Minge jaotisesse Pearaamat > Perioodilised ülesanded > Pearaamatu tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="84982-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="84982-108">Leidke loendist kanne, mille soovite tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="84982-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="84982-109">Summa saldo peab olema null.</span><span class="sxs-lookup"><span data-stu-id="84982-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="84982-110">Klõpsake suvandit Kaasa.</span><span class="sxs-lookup"><span data-stu-id="84982-110">Click Include.</span></span>
4. <span data-ttu-id="84982-111">Klõpsake suvandit Nõustu.</span><span class="sxs-lookup"><span data-stu-id="84982-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="84982-112">Pearaamatu tasakaalustamise tühistamine</span><span class="sxs-lookup"><span data-stu-id="84982-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="84982-113">Minge jaotisse Pearaamat > Päringud ja aruanded > Proovibilanss.</span><span class="sxs-lookup"><span data-stu-id="84982-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="84982-114">Klõpsake suvandit Parameetrid rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="84982-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="84982-115">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="84982-115">Click Update.</span></span>
4. <span data-ttu-id="84982-116">Leidke loendist konto, millel on tasakaalustatud kanne.</span><span class="sxs-lookup"><span data-stu-id="84982-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="84982-117">Klõpsake suvandit Kõik kanded.</span><span class="sxs-lookup"><span data-stu-id="84982-117">Click All transactions.</span></span>
6. <span data-ttu-id="84982-118">Loendist hõlpsasti kande leidmiseks kasutage filtrit.</span><span class="sxs-lookup"><span data-stu-id="84982-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="84982-119">Klõpsake suvandit Pearaamatu tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="84982-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="84982-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="84982-120">In the list, mark the selected row.</span></span>

