---
title: Kliendimaksete deponeerimine
description: Hoiustage kliendimaksed.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f58cebce20e8516dc918e0bad1e020ffd7f791ee
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313378"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="67a3b-103">Kliendimaksete deponeerimine</span><span class="sxs-lookup"><span data-stu-id="67a3b-103">Deposit customer payments</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67a3b-104">Hoiustage kliendimaksed.</span><span class="sxs-lookup"><span data-stu-id="67a3b-104">Deposit customer payments.</span></span> <span data-ttu-id="67a3b-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="67a3b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="67a3b-106">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="67a3b-106">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="67a3b-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67a3b-107">Click New.</span></span>
3. <span data-ttu-id="67a3b-108">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="67a3b-108">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="67a3b-109">Valige makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="67a3b-109">Select the payment journal.</span></span> 
5. <span data-ttu-id="67a3b-110">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="67a3b-110">Click Lines.</span></span>
6. <span data-ttu-id="67a3b-111">Valige väljalt Konto klient, kelle puhul makse registreerite.</span><span class="sxs-lookup"><span data-stu-id="67a3b-111">In the Account field, select the Customer for whom you are recording the payment.</span></span>
7. <span data-ttu-id="67a3b-112">Sisestage makse summa väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="67a3b-112">In the Credit field, enter the amount of the payment.</span></span>
    * <span data-ttu-id="67a3b-113">Saate valida summa tühjaks jätmise ja lasta selle süsteemil arvutada, valides makstud arved.</span><span class="sxs-lookup"><span data-stu-id="67a3b-113">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
8. <span data-ttu-id="67a3b-114">Sisestage väärtus väljale Makse viide.</span><span class="sxs-lookup"><span data-stu-id="67a3b-114">In the Payment reference field, type a value.</span></span>
    * <span data-ttu-id="67a3b-115">Makse viiteks võib olla sisestatava makse tšeki number.</span><span class="sxs-lookup"><span data-stu-id="67a3b-115">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="67a3b-116">Makse viide on vajalik makse kaasamiseks deposiitkviitungile.</span><span class="sxs-lookup"><span data-stu-id="67a3b-116">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
9. <span data-ttu-id="67a3b-117">Märkige ruut Kasuta deposiitkviitungit.</span><span class="sxs-lookup"><span data-stu-id="67a3b-117">Mark the box Use a deposit slip.</span></span>
    * <span data-ttu-id="67a3b-118">Kui makse tuleks deposiiti kaasata, muutke sätte väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="67a3b-118">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
10. <span data-ttu-id="67a3b-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="67a3b-119">Click New.</span></span>
11. <span data-ttu-id="67a3b-120">Valige järgmise makse klient väljalt Konto.</span><span class="sxs-lookup"><span data-stu-id="67a3b-120">In the Account field, select the Customer for the next payment.</span></span>
12. <span data-ttu-id="67a3b-121">Sisestage maksesumma väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="67a3b-121">In the Credit field, enter the payment amount.</span></span>
13. <span data-ttu-id="67a3b-122">Sisestage väärtus väljale Makse viide.</span><span class="sxs-lookup"><span data-stu-id="67a3b-122">In the Payment reference field, type a value.</span></span>
14. <span data-ttu-id="67a3b-123">Märkige ruut Kasuta deposiitkviitungit.</span><span class="sxs-lookup"><span data-stu-id="67a3b-123">Mark the box Use a deposit slip.</span></span>
15. <span data-ttu-id="67a3b-124">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="67a3b-124">Click Post.</span></span>
    * <span data-ttu-id="67a3b-125">Maksed tuleb sisestada enne deposiitkviitungi loomist.</span><span class="sxs-lookup"><span data-stu-id="67a3b-125">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="67a3b-126">See tagab, et maksed pärast deposiitkviitungi loomist ei muutuks.</span><span class="sxs-lookup"><span data-stu-id="67a3b-126">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
16. <span data-ttu-id="67a3b-127">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="67a3b-127">Click Functions.</span></span>
17. <span data-ttu-id="67a3b-128">Klõpsake suvandit Deposiitkviitung.</span><span class="sxs-lookup"><span data-stu-id="67a3b-128">Click Deposit slip.</span></span>
18. <span data-ttu-id="67a3b-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="67a3b-129">Click OK.</span></span>
    * <span data-ttu-id="67a3b-130">Esimest lehte kasutatakse deposiitkviitungi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="67a3b-130">The first page is used to create the deposit slip.</span></span>  
19. <span data-ttu-id="67a3b-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="67a3b-131">Click OK.</span></span>
    * <span data-ttu-id="67a3b-132">Teise etapina tuleb deposiitkviitung printida, kuid see etapp pole nõutav.</span><span class="sxs-lookup"><span data-stu-id="67a3b-132">The second step is to print the deposit slip, but this step is not required.</span></span>  

