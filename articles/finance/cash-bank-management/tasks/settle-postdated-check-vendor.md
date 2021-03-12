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
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 08cf4ec805e632470ef778f31beb87597e0ca096
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976187"
---
# <a name="settle-a-postdated-check-for-a-vendor"></a><span data-ttu-id="f983a-103">Hankija hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="f983a-103">Settle a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f983a-104">Tasakaalustage hankijale väljastatud hilisema kuupäevaga tšekk, kui pank on tšeki kande tasaarvestanud pärast seda, kui tšeki tasumine hilines ja panga poolt läbi lasti.</span><span class="sxs-lookup"><span data-stu-id="f983a-104">Settle a postdated check issued to a vendor when the bank has cleared the check transaction after the check has been overdue and cleared by the bank.</span></span> 

<span data-ttu-id="f983a-105">Viige enne selle toimingu alustamist järgmised protseduurid lõpule.</span><span class="sxs-lookup"><span data-stu-id="f983a-105">Complete the following procedures before you start this one.</span></span>

1) <span data-ttu-id="f983a-106">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="f983a-106">Set up postdated checks</span></span>

2) <span data-ttu-id="f983a-107">Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="f983a-107">Register and post a postdated check for a vendor</span></span>



<span data-ttu-id="f983a-108">Selle protseduuri roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="f983a-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="f983a-109">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f983a-109">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="f983a-110">Avage Ostureskontro > Maksed > Hankija hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="f983a-110">Go to Accounts payable > Payments > Vendor postdated checks.</span></span>
2. <span data-ttu-id="f983a-111">Klõpsake suvandit Tasakaalustus.</span><span class="sxs-lookup"><span data-stu-id="f983a-111">Click Settle.</span></span>
3. <span data-ttu-id="f983a-112">Klõpsake suvandit Kliiringukirjete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="f983a-112">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="f983a-113">Tasakaalustage hankija konto tšekikande jaoks.</span><span class="sxs-lookup"><span data-stu-id="f983a-113">Settle the vendor account for the check transaction.</span></span>  
4. <span data-ttu-id="f983a-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f983a-114">Close the page.</span></span>
5. <span data-ttu-id="f983a-115">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="f983a-115">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="f983a-116">Valige väljal Kuva suvand „Kõik”.</span><span class="sxs-lookup"><span data-stu-id="f983a-116">In the Show field, select 'All'.</span></span>
7. <span data-ttu-id="f983a-117">Märkige või tühjendage ruut Kuva ainult kasutaja loodud.</span><span class="sxs-lookup"><span data-stu-id="f983a-117">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="f983a-118">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f983a-118">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="f983a-119">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="f983a-119">Click Lines.</span></span>
10. <span data-ttu-id="f983a-120">Klõpsake suvandit Kanne.</span><span class="sxs-lookup"><span data-stu-id="f983a-120">Click Voucher.</span></span>
11. <span data-ttu-id="f983a-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f983a-121">Close the page.</span></span>

