---
title: Kliendi hilisema kuupäevaga tšeki tasakaalustamine
description: Hilisema kuupäevaga dateeritud tšekki saab tasakaalustada pärast seda, kui pank on tšeki kinnitanud.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 86cefaac99a1ce5aa777f4f62456c3248045cc27
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565991"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="52966-103">Kliendi hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="52966-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52966-104">Hilisema kuupäevaga dateeritud tšekki saab tasakaalustada pärast seda, kui pank on tšeki kinnitanud.</span><span class="sxs-lookup"><span data-stu-id="52966-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="52966-105">See finantskanne kinnitab vahekonto kande hilisema kuupäevaga dateeritud tšekkidele.</span><span class="sxs-lookup"><span data-stu-id="52966-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="52966-106">Enne alustamist peavad olema täidetud järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="52966-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="52966-107">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="52966-107">Set up postdated checks</span></span>

2) <span data-ttu-id="52966-108">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="52966-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="52966-109">Selle ülesandejuhendi roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="52966-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="52966-110">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="52966-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="52966-111">Minge jaotisse Krediidihaldus ja võlanõuded > Päringud ja aruanded > Maksed > Kliendi hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="52966-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="52966-112">Klõpsake suvandit Tasakaalustus.</span><span class="sxs-lookup"><span data-stu-id="52966-112">Click Settle.</span></span>
3. <span data-ttu-id="52966-113">Klõpsake suvandit Kliiringukirjete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="52966-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="52966-114">Tasakaalustage kliendi konto tšekikande jaoks.</span><span class="sxs-lookup"><span data-stu-id="52966-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="52966-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52966-115">Close the page.</span></span>
5. <span data-ttu-id="52966-116">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="52966-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="52966-117">Valige suvand väljal Kuva.</span><span class="sxs-lookup"><span data-stu-id="52966-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="52966-118">Märkige või tühjendage ruut Kuva ainult kasutaja loodud.</span><span class="sxs-lookup"><span data-stu-id="52966-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="52966-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="52966-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="52966-120">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="52966-120">Click Lines.</span></span>
10. <span data-ttu-id="52966-121">Klõpsake suvandit Kanne.</span><span class="sxs-lookup"><span data-stu-id="52966-121">Click Voucher.</span></span>
11. <span data-ttu-id="52966-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="52966-122">Close the page.</span></span>

