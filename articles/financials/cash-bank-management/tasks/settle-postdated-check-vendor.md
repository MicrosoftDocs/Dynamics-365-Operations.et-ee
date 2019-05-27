---
title: Hankija hilisema kuupäevaga tšeki tasakaalustamine
description: Tasakaalustage hankijale väljastatud hilisema kuupäevaga tšekk, kui pank on tšeki kande tasaarvestanud pärast seda, kui tšeki tasumine hilines ja panga poolt läbi lasti.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e46b419ab613425ae2d758f80105ac94f1ec5cc2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565968"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="d24f8-103">Hankija hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="d24f8-103">Settle a postdated check for a vendor</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d24f8-104">Tasakaalustage hankijale väljastatud hilisema kuupäevaga tšekk, kui pank on tšeki kande tasaarvestanud pärast seda, kui tšeki tasumine hilines ja panga poolt läbi lasti.</span><span class="sxs-lookup"><span data-stu-id="d24f8-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="d24f8-105">Viige enne selle toimingu alustamist järgmised protseduurid lõpule.</span><span class="sxs-lookup"><span data-stu-id="d24f8-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="d24f8-106">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d24f8-106">Set up postdated checks</span></span>

2) <span data-ttu-id="d24f8-107">Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="d24f8-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="d24f8-108">Selle protseduuri roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="d24f8-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="d24f8-109">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="d24f8-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="d24f8-110">Avage Ostureskontro > Maksed > Hankija hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="d24f8-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="d24f8-111">Klõpsake suvandit Tasakaalustus.</span><span class="sxs-lookup"><span data-stu-id="d24f8-111">Click Settle.</span></span>
3. <span data-ttu-id="d24f8-112">Klõpsake suvandit Kliiringukirjete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="d24f8-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="d24f8-113">Tasakaalustage hankija konto tšekikande jaoks.</span><span class="sxs-lookup"><span data-stu-id="d24f8-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="d24f8-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d24f8-114">Close the page.</span></span>
5. <span data-ttu-id="d24f8-115">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="d24f8-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="d24f8-116">Valige väljal Kuva suvand „Kõik”.</span><span class="sxs-lookup"><span data-stu-id="d24f8-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="d24f8-117">Märkige või tühjendage ruut Kuva ainult kasutaja loodud.</span><span class="sxs-lookup"><span data-stu-id="d24f8-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="d24f8-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d24f8-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d24f8-119">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="d24f8-119">Click Lines.</span></span>
10. <span data-ttu-id="d24f8-120">Klõpsake suvandit Kanne.</span><span class="sxs-lookup"><span data-stu-id="d24f8-120">Click Voucher.</span></span>
11. <span data-ttu-id="d24f8-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d24f8-121">Close the page.</span></span>

