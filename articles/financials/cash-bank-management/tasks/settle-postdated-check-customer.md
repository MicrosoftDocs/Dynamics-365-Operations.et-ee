--- 
title: "Kliendi hilisema kuupäevaga tšeki tasakaalustamine"
description: "Hilisema kuupäevaga dateeritud tšekki saab tasakaalustada pärast seda, kui pank on tšeki kinnitanud."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 95651e602bd4f576a7fcf96379f61252cdf392f6
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="002f3-103">Kliendi hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="002f3-103">Settle a postdated check from a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="002f3-104">Hilisema kuupäevaga dateeritud tšekki saab tasakaalustada pärast seda, kui pank on tšeki kinnitanud.</span><span class="sxs-lookup"><span data-stu-id="002f3-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="002f3-105">See finantskanne kinnitab vahekonto kande hilisema kuupäevaga dateeritud tšekkidele.</span><span class="sxs-lookup"><span data-stu-id="002f3-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="002f3-106">Enne alustamist peavad olema täidetud järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="002f3-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="002f3-107">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="002f3-107">Set up postdated checks</span></span>

2) <span data-ttu-id="002f3-108">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="002f3-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="002f3-109">Selle ülesandejuhendi roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="002f3-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="002f3-110">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="002f3-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="002f3-111">Minge jaotisse Krediidihaldus ja võlanõuded > Päringud ja aruanded > Maksed > Kliendi hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="002f3-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="002f3-112">Klõpsake suvandit Tasakaalustus.</span><span class="sxs-lookup"><span data-stu-id="002f3-112">Click Settle.</span></span>
3. <span data-ttu-id="002f3-113">Klõpsake suvandit Kliiringukirjete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="002f3-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="002f3-114">Tasakaalustage kliendi konto tšekikande jaoks.</span><span class="sxs-lookup"><span data-stu-id="002f3-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="002f3-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="002f3-115">Close the page.</span></span>
5. <span data-ttu-id="002f3-116">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="002f3-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="002f3-117">Valige suvand väljal Kuva.</span><span class="sxs-lookup"><span data-stu-id="002f3-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="002f3-118">Märkige või tühjendage ruut Kuva ainult kasutaja loodud.</span><span class="sxs-lookup"><span data-stu-id="002f3-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="002f3-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="002f3-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="002f3-120">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="002f3-120">Click Lines.</span></span>
10. <span data-ttu-id="002f3-121">Klõpsake suvandit Kanne.</span><span class="sxs-lookup"><span data-stu-id="002f3-121">Click Voucher.</span></span>
11. <span data-ttu-id="002f3-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="002f3-122">Close the page.</span></span>


