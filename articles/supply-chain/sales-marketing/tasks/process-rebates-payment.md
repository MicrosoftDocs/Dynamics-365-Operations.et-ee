---
title: Makse tagasimaksete töötlemine
description: See protseduur näitab, kuidas teisendada kliendi kinnitatud ja töödeldud tagasimakseid kreeditarveteks.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 412e7df299a419642018a62e6e8febd5d59c65e1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148443"
---
# <a name="process-rebates-for-payment"></a><span data-ttu-id="074e5-103">Makse tagasimaksete töötlemine</span><span class="sxs-lookup"><span data-stu-id="074e5-103">Process rebates for payment</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="074e5-104">See protseduur näitab, kuidas teisendada kliendi kinnitatud ja töödeldud tagasimakseid kreeditarveteks.</span><span class="sxs-lookup"><span data-stu-id="074e5-104">This procedure demonstrates how to convert approved and processed customer rebates to credit notes.</span></span> <span data-ttu-id="074e5-105">Saate seda juhendit kasutada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="074e5-105">You can use this guide in the USMF demo company.</span></span> <span data-ttu-id="074e5-106">Selle juhendi eeltingimus on üks või mitu olemasolevat tagasimaksenõuet, mille olek on Märgi.</span><span class="sxs-lookup"><span data-stu-id="074e5-106">The precondition for this guide is to have one or more rebate claims which have a status of Mark.</span></span> <span data-ttu-id="074e5-107">USMF-i kasutamisel peaksite enne selle juhendi käivitamist käitama juhendit „Kliendi tagasimaksete loomine ja töötlemine”.</span><span class="sxs-lookup"><span data-stu-id="074e5-107">If you're using USMF you should run the "Generate and process customer rebates" guide before you start this guide.</span></span>


## <a name="convert-rebate-claims-to-credit-note"></a><span data-ttu-id="074e5-108">Tagasimaksenõuete teisendamine kreeditarveks</span><span class="sxs-lookup"><span data-stu-id="074e5-108">Convert rebate claims to credit note</span></span>
1. <span data-ttu-id="074e5-109">Minge jaotisse Kõik kliendid.</span><span class="sxs-lookup"><span data-stu-id="074e5-109">Go to All customers.</span></span>
2. <span data-ttu-id="074e5-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="074e5-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="074e5-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="074e5-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="074e5-112">Klõpsake toimingupaanil suvandit Sissenõudmine.</span><span class="sxs-lookup"><span data-stu-id="074e5-112">On the Action Pane, click Collect.</span></span>
5. <span data-ttu-id="074e5-113">Klõpsake suvandit Kannete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="074e5-113">Click Settle transactions.</span></span>
6. <span data-ttu-id="074e5-114">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="074e5-114">Click Functions.</span></span>
7. <span data-ttu-id="074e5-115">Klõpsake suvandit Tagasimakseprogramm.</span><span class="sxs-lookup"><span data-stu-id="074e5-115">Click Rebate program.</span></span>
    * <span data-ttu-id="074e5-116">Lehel Tagasimakse loetletakse tagasimaksenõuded, mida olete kliendi tagasimaksete töölaual töödelnud ja mille olek on Märgi.</span><span class="sxs-lookup"><span data-stu-id="074e5-116">The Rebate page lists the rebate claims that you have processed in the customer rebate workbench and that are in status Mark.</span></span>    
8. <span data-ttu-id="074e5-117">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="074e5-117">Click Edit.</span></span>
    * <span data-ttu-id="074e5-118">Märkige väli Märgi nende nõuete puhul, mille soovite kreeditarvesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="074e5-118">Set checkmarks in the Mark field for the claims that you want to include into credit note.</span></span>   
9. <span data-ttu-id="074e5-119">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="074e5-119">Click Functions.</span></span>
10. <span data-ttu-id="074e5-120">Klõpsake suvandit Loo kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="074e5-120">Click Create credit note.</span></span>
    * <span data-ttu-id="074e5-121">Kuvatakse teade, et tööleht on sisestatud (see on tööleht Müügireskontro tarbimine, nagu on määratud lehel Müügireskontro parameetrid).</span><span class="sxs-lookup"><span data-stu-id="074e5-121">A message appears to inform you that a journal has been posted (This is the Accounts receivable consumption journal, as specified in the Accounts receivable parameters page).</span></span> <span data-ttu-id="074e5-122">Selle tagajärjel teisaldatakse reaalkohustuse (krediidi) summa kliendi saldole.</span><span class="sxs-lookup"><span data-stu-id="074e5-122">This causes the real liability (credit) amount to be moved to the customer balance.</span></span> <span data-ttu-id="074e5-123">See tähendab, et kliendi konto on krediteeritud ja tagasimakse juurdekasvukonto on debiteeritud.</span><span class="sxs-lookup"><span data-stu-id="074e5-123">This means that the customer's account has been credited, and the Rebate accrual account has been debited.</span></span>  
11. <span data-ttu-id="074e5-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="074e5-124">Close the page.</span></span>
12. <span data-ttu-id="074e5-125">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="074e5-125">Click Cancel.</span></span>
    * <span data-ttu-id="074e5-126">See värskendab lehte, nii et näete värskendusi.</span><span class="sxs-lookup"><span data-stu-id="074e5-126">This refreshes the page so that you can see the updates.</span></span>  
13. <span data-ttu-id="074e5-127">Klõpsake toimingupaanil suvandit Sissenõudmine.</span><span class="sxs-lookup"><span data-stu-id="074e5-127">On the Action Pane, click Collect.</span></span>
14. <span data-ttu-id="074e5-128">Klõpsake suvandit Kannete tasakaalustamine.</span><span class="sxs-lookup"><span data-stu-id="074e5-128">Click Settle transactions.</span></span>
    * <span data-ttu-id="074e5-129">Pange tähele, et kliendi saldole on lisatud negatiivse summa kanne, mis tähistab tagasimakse kogusummat ilma arve viiteta.</span><span class="sxs-lookup"><span data-stu-id="074e5-129">Note that a transaction for negative amount, representing the total rebate amount, without invoice reference has been added to the customer balance.</span></span>   
15. <span data-ttu-id="074e5-130">Klõpsake valikut Tühista.</span><span class="sxs-lookup"><span data-stu-id="074e5-130">Click Cancel.</span></span>

