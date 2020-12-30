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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bb53e9fee35712343f034389f00f3d4539cc652d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442388"
---
# <a name="settle-transactions-between-ledger-accounts"></a><span data-ttu-id="5cad3-103">Pearaamatukontode kannete tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="5cad3-103">Settle transactions between ledger accounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5cad3-104">See protseduur selgitab, kuidas tasakaalustada kandeid pearaamatu kontode vahel ja tühistada pearaamatu tasakaalustust.</span><span class="sxs-lookup"><span data-stu-id="5cad3-104">This procedure shows how to settle transactions between ledger accounts and cancel a ledger settlement.</span></span> <span data-ttu-id="5cad3-105">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="5cad3-105">This procedure uses the USMF demo data company.</span></span>


## <a name="settle-transaction-between-ledger-accounts"></a><span data-ttu-id="5cad3-106">Kande tasakaalustamine pearaamatukontode vahel</span><span class="sxs-lookup"><span data-stu-id="5cad3-106">Settle transaction between ledger accounts</span></span>
1. <span data-ttu-id="5cad3-107">Minge jaotisesse Pearaamat > Perioodilised ülesanded > Pearaamatu tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="5cad3-107">Go to General ledger > Periodic tasks > Ledger settlements.</span></span>
2. <span data-ttu-id="5cad3-108">Leidke loendist kanne, mille soovite tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="5cad3-108">In the list, find the transaction that you want to settle.</span></span>
   > [!NOTE]
   > <span data-ttu-id="5cad3-109">Summa saldo peab olema null.</span><span class="sxs-lookup"><span data-stu-id="5cad3-109">The amount balance must be zero.</span></span>  
3. <span data-ttu-id="5cad3-110">Klõpsake suvandit Kaasa.</span><span class="sxs-lookup"><span data-stu-id="5cad3-110">Click Include.</span></span>
4. <span data-ttu-id="5cad3-111">Klõpsake suvandit Nõustu.</span><span class="sxs-lookup"><span data-stu-id="5cad3-111">Click Accept.</span></span>

## <a name="cancel-a-ledger-settlement"></a><span data-ttu-id="5cad3-112">Pearaamatu tasakaalustamise tühistamine</span><span class="sxs-lookup"><span data-stu-id="5cad3-112">Cancel a ledger settlement</span></span>

1. <span data-ttu-id="5cad3-113">Minge jaotisse Pearaamat > Päringud ja aruanded > Proovibilanss.</span><span class="sxs-lookup"><span data-stu-id="5cad3-113">Go to General ledger > Inquiries and reports > Trial balance.</span></span>
2. <span data-ttu-id="5cad3-114">Klõpsake suvandit Parameetrid rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5cad3-114">Click Parameters to open the drop dialog.</span></span>
3. <span data-ttu-id="5cad3-115">Klõpsake käsku Uuenda.</span><span class="sxs-lookup"><span data-stu-id="5cad3-115">Click Update.</span></span>
4. <span data-ttu-id="5cad3-116">Leidke loendist konto, millel on tasakaalustatud kanne.</span><span class="sxs-lookup"><span data-stu-id="5cad3-116">In the list, find the account that has the settled transaction.</span></span>
5. <span data-ttu-id="5cad3-117">Klõpsake suvandit Kõik kanded.</span><span class="sxs-lookup"><span data-stu-id="5cad3-117">Click All transactions.</span></span>
6. <span data-ttu-id="5cad3-118">Loendist hõlpsasti kande leidmiseks kasutage filtrit.</span><span class="sxs-lookup"><span data-stu-id="5cad3-118">Use a filter to easily find the transaction in the list.</span></span>
7. <span data-ttu-id="5cad3-119">Klõpsake suvandit Pearaamatu tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="5cad3-119">Click Ledger settlements.</span></span>
8. <span data-ttu-id="5cad3-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="5cad3-120">In the list, mark the selected row.</span></span>

