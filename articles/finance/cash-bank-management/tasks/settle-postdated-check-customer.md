---
title: Kliendi hilisema kuupäevaga tšeki tasakaalustamine
description: Hilisema kuupäevaga dateeritud tšekki saab tasakaalustada pärast seda, kui pank on tšeki kinnitanud.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPostDatedChecks, SystemDate, LedgerJournalTable, LedgerJournalTransDaily, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f714e41f47a31bce16424de18878d2f5acb5028d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834544"
---
# <a name="settle-a-postdated-check-from-a-customer"></a><span data-ttu-id="e747d-103">Kliendi hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="e747d-103">Settle a postdated check from a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e747d-104">Hilisema kuupäevaga dateeritud tšekki saab tasakaalustada pärast seda, kui pank on tšeki kinnitanud.</span><span class="sxs-lookup"><span data-stu-id="e747d-104">You can settle a postdated check after the check has been cleared by the bank.</span></span> <span data-ttu-id="e747d-105">See finantskanne kinnitab vahekonto kande hilisema kuupäevaga dateeritud tšekkidele.</span><span class="sxs-lookup"><span data-stu-id="e747d-105">This financial transaction also clears the bridge account transaction for the postdated check.</span></span> 

<span data-ttu-id="e747d-106">Enne alustamist peavad olema täidetud järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="e747d-106">The following tasks must be complete before you start this one.</span></span>

1) <span data-ttu-id="e747d-107">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="e747d-107">Set up postdated checks</span></span>

2) <span data-ttu-id="e747d-108">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="e747d-108">Register and post a postdated check for a customer</span></span> 



<span data-ttu-id="e747d-109">Selle ülesandejuhendi roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="e747d-109">The role of this task guides is Treasurer.</span></span>



<span data-ttu-id="e747d-110">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e747d-110">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="e747d-111">Minge jaotisse Krediidihaldus ja võlanõuded > Päringud ja aruanded > Maksed > Kliendi hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="e747d-111">Go to Credit and collections > Inquiries and reports > Payments > Customer postdated checks.</span></span>
2. <span data-ttu-id="e747d-112">Klõpsake suvandit Tasakaalustus.</span><span class="sxs-lookup"><span data-stu-id="e747d-112">Click Settle.</span></span>
3. <span data-ttu-id="e747d-113">Klõpsake suvandit Kliiringukirjete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="e747d-113">Click Settle clearing entries.</span></span>
    * <span data-ttu-id="e747d-114">Tasakaalustage kliendi konto tšekikande jaoks.</span><span class="sxs-lookup"><span data-stu-id="e747d-114">Settle the customer account for the check transaction.</span></span>  
4. <span data-ttu-id="e747d-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e747d-115">Close the page.</span></span>
5. <span data-ttu-id="e747d-116">Avage Pearaamat > Töölehe sisestused > Päevaraamatud.</span><span class="sxs-lookup"><span data-stu-id="e747d-116">Go to General ledger > Journal entries > General journals.</span></span>
6. <span data-ttu-id="e747d-117">Valige suvand väljal Kuva.</span><span class="sxs-lookup"><span data-stu-id="e747d-117">In the Show field, select an option.</span></span>
7. <span data-ttu-id="e747d-118">Märkige või tühjendage ruut Kuva ainult kasutaja loodud.</span><span class="sxs-lookup"><span data-stu-id="e747d-118">Select or clear the Show user-created only check box.</span></span>
8. <span data-ttu-id="e747d-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e747d-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e747d-120">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="e747d-120">Click Lines.</span></span>
10. <span data-ttu-id="e747d-121">Klõpsake suvandit Kanne.</span><span class="sxs-lookup"><span data-stu-id="e747d-121">Click Voucher.</span></span>
11. <span data-ttu-id="e747d-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e747d-122">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]