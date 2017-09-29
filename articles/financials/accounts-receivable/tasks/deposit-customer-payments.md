--- 
title: Kliendimaksete deponeerimine
description: Hoiustage kliendimaksed.
author: ShivamPandey-msft
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
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: dbf21bd5df70cd80e4fe3f2f5d699aa82b62423b
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="deposit-customer-payments"></a><span data-ttu-id="390c2-103">Kliendimaksete deponeerimine</span><span class="sxs-lookup"><span data-stu-id="390c2-103">Deposit customer payments</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="390c2-104">Hoiustage kliendimaksed.</span><span class="sxs-lookup"><span data-stu-id="390c2-104">Deposit customer payments.</span></span> <span data-ttu-id="390c2-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="390c2-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="390c2-106">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="390c2-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="390c2-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="390c2-107">Click New.</span></span>
3. <span data-ttu-id="390c2-108">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="390c2-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="390c2-109">Valige makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="390c2-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="390c2-110">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="390c2-110">Click Lines.</span></span>
6. <span data-ttu-id="390c2-111">Valige väljalt Konto klient, kelle puhul makse registreerite.</span><span class="sxs-lookup"><span data-stu-id="390c2-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="390c2-112">Sisestage makse summa väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="390c2-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="390c2-113">Saate valida summa tühjaks jätmise ja lasta selle süsteemil arvutada, valides makstud arved.</span><span class="sxs-lookup"><span data-stu-id="390c2-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="390c2-114">Sisestage väärtus väljale Makse viide.</span><span class="sxs-lookup"><span data-stu-id="390c2-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="390c2-115">Makse viiteks võib olla sisestatava makse tšeki number.</span><span class="sxs-lookup"><span data-stu-id="390c2-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="390c2-116">Makse viide on vajalik makse kaasamiseks deposiitkviitungile.</span><span class="sxs-lookup"><span data-stu-id="390c2-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="390c2-117">Märkige ruut Kasuta deposiitkviitungit.</span><span class="sxs-lookup"><span data-stu-id="390c2-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="390c2-118">Kui makse tuleks deposiiti kaasata, muutke sätte väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="390c2-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="390c2-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="390c2-119">Click New.</span></span>
11. <span data-ttu-id="390c2-120">Valige järgmise makse klient väljalt Konto.</span><span class="sxs-lookup"><span data-stu-id="390c2-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="390c2-121">Sisestage maksesumma väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="390c2-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="390c2-122">Sisestage väärtus väljale Makse viide.</span><span class="sxs-lookup"><span data-stu-id="390c2-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="390c2-123">Märkige ruut Kasuta deposiitkviitungit.</span><span class="sxs-lookup"><span data-stu-id="390c2-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="390c2-124">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="390c2-124">Click Post.</span></span>
    * <span data-ttu-id="390c2-125">Maksed tuleb sisestada enne deposiitkviitungi loomist.</span><span class="sxs-lookup"><span data-stu-id="390c2-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="390c2-126">See tagab, et maksed pärast deposiitkviitungi loomist ei muutuks.</span><span class="sxs-lookup"><span data-stu-id="390c2-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="390c2-127">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="390c2-127">Click Functions.</span></span>
17. <span data-ttu-id="390c2-128">Klõpsake suvandit Deposiitkviitung.</span><span class="sxs-lookup"><span data-stu-id="390c2-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="390c2-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="390c2-129">Click OK.</span></span>
    * <span data-ttu-id="390c2-130">Esimest lehte kasutatakse deposiitkviitungi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="390c2-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="390c2-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="390c2-131">Click OK.</span></span>
    * <span data-ttu-id="390c2-132">Teise etapina tuleb deposiitkviitung printida, kuid see etapp pole nõutav.</span><span class="sxs-lookup"><span data-stu-id="390c2-132">The second step is to print the deposit slip, but this step is not required.</span></span>  


