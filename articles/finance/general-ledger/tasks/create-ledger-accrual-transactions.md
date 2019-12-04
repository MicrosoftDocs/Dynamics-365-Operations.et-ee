---
title: Pearaamatu tekkepõhiste kannete loomine
description: See ülesandejuhend hõlmab pearaamatu tekkepõhiste kannete, mille aluseks on viitvõlgade skeemid, loomise etappe.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransAccrual, LedgerJournalTransAccrualTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06743ca3ed13906e3f65d3783db7a7f74fb53e3f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186183"
---
# <a name="create-ledger-accrual-transactions"></a><span data-ttu-id="79515-103">Pearaamatu tekkepõhiste kannete loomine</span><span class="sxs-lookup"><span data-stu-id="79515-103">Create ledger accrual transactions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="79515-104">See ülesandejuhend hõlmab pearaamatu tekkepõhiste kannete, mille aluseks on viitvõlgade skeemid, loomise etappe</span><span class="sxs-lookup"><span data-stu-id="79515-104">This task guide steps through generating ledger accrual transactions that are based on accrual schemes</span></span>

1. <span data-ttu-id="79515-105">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="79515-105">Go to General ledger > Journal entries > General journals.</span></span>
2. <span data-ttu-id="79515-106">Leidke ja valige loendist soovitud tööleht või looge uus.</span><span class="sxs-lookup"><span data-stu-id="79515-106">In the list, find and select the desired journal or create a new one.</span></span>
3. <span data-ttu-id="79515-107">Klõpsake linki väljal Töölehe partiinumber.</span><span class="sxs-lookup"><span data-stu-id="79515-107">Click to follow the link in the Journal batch number field.</span></span>
4. <span data-ttu-id="79515-108">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="79515-108">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="79515-109">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="79515-109">In the Account field, specify the desired values.</span></span>
    * <span data-ttu-id="79515-110">Selles näites määratleme kindlustuse kulu.</span><span class="sxs-lookup"><span data-stu-id="79515-110">In this example, we are defining the expense for the insurance.</span></span> <span data-ttu-id="79515-111">See muutub perioodiliseks kulusummaks.</span><span class="sxs-lookup"><span data-stu-id="79515-111">It will be come periodic expense amount.</span></span>  
6. <span data-ttu-id="79515-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="79515-112">In the Description field, type a value.</span></span>
7. <span data-ttu-id="79515-113">Sisestage arv väljale Deebet.</span><span class="sxs-lookup"><span data-stu-id="79515-113">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="79515-114">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="79515-114">In the Offset account field, specify the desired values.</span></span>
9. <span data-ttu-id="79515-115">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="79515-115">Click Functions.</span></span>
10. <span data-ttu-id="79515-116">Klõpsake suvandit Pearaamatu viitvõlad.</span><span class="sxs-lookup"><span data-stu-id="79515-116">Click Ledger accruals.</span></span>
11. <span data-ttu-id="79515-117">Klõpsake väljal Viitvõla ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="79515-117">In the Accrual identification field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="79515-118">Leidke ja valige loendist viitvõlaskeem, mille soovite rakendada.</span><span class="sxs-lookup"><span data-stu-id="79515-118">In the list, find and select the accural scheme you want to apply.</span></span>
13. <span data-ttu-id="79515-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="79515-119">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="79515-120">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="79515-120">In the Start date field, enter a date.</span></span>
15. <span data-ttu-id="79515-121">Klõpsake suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="79515-121">Click Transactions.</span></span>
16. <span data-ttu-id="79515-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="79515-122">Close the page.</span></span>
17. <span data-ttu-id="79515-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="79515-123">Click OK.</span></span>
18. <span data-ttu-id="79515-124">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="79515-124">Click Post.</span></span>
