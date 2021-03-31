---
title: Kliendimaksete deponeerimine
description: Hoiustage kliendimaksed.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransCustPaym, CustTableLookup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7357683e46df04c3dedd7e22607748512c9de94a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220247"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="d938a-103">Kliendimaksete deponeerimine</span><span class="sxs-lookup"><span data-stu-id="d938a-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d938a-104">Hoiustage kliendimaksed.</span><span class="sxs-lookup"><span data-stu-id="d938a-104">Deposit customer payments.</span></span> <span data-ttu-id="d938a-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d938a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="d938a-106">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksed > Maksete töölehed**.</span><span class="sxs-lookup"><span data-stu-id="d938a-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="d938a-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d938a-107">Select **New**.</span></span>
3. <span data-ttu-id="d938a-108">Väljal **Nimi** valige rippmenüüst **CustPay**.</span><span class="sxs-lookup"><span data-stu-id="d938a-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="d938a-109">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="d938a-109">Select **Lines**.</span></span>
5. <span data-ttu-id="d938a-110">Väljal **Konto** valige klient, kelle jaoks registreerite makset.</span><span class="sxs-lookup"><span data-stu-id="d938a-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="d938a-111">Väljale **Kreedit** sisestage maksesumma.</span><span class="sxs-lookup"><span data-stu-id="d938a-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="d938a-112">Saate valida summa tühjaks jätmise ja lasta selle süsteemil arvutada, valides makstud arved.</span><span class="sxs-lookup"><span data-stu-id="d938a-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="d938a-113">Väljale **Makse viide** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="d938a-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="d938a-114">Makse viiteks võib olla sisestatava makse tšeki number.</span><span class="sxs-lookup"><span data-stu-id="d938a-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="d938a-115">Makse viide on vajalik makse kaasamiseks deposiitkviitungile.</span><span class="sxs-lookup"><span data-stu-id="d938a-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="d938a-116">Märkige ruut Kasuta deposiitkviitungit.</span><span class="sxs-lookup"><span data-stu-id="d938a-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="d938a-117">Kui makse tuleks deposiiti kaasata, muutke sätte väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="d938a-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="d938a-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d938a-118">Select **New**.</span></span>
10. <span data-ttu-id="d938a-119">Väljal **Konto** valige klient järgmise makse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d938a-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="d938a-120">Väljale **Kreedit** sisestage maksesumma.</span><span class="sxs-lookup"><span data-stu-id="d938a-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="d938a-121">Väljale **Makse viide** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="d938a-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="d938a-122">Märkige ruut **Kasuta deposiitkviitungit**.</span><span class="sxs-lookup"><span data-stu-id="d938a-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="d938a-123">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="d938a-123">Select **Post**.</span></span> <span data-ttu-id="d938a-124">Maksed tuleb sisestada enne deposiitkviitungi loomist.</span><span class="sxs-lookup"><span data-stu-id="d938a-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="d938a-125">See tagab, et maksed pärast deposiitkviitungi loomist ei muutuks.</span><span class="sxs-lookup"><span data-stu-id="d938a-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="d938a-126">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d938a-126">Select **Functions**.</span></span>
16. <span data-ttu-id="d938a-127">Valige **Deposiitkviitung**.</span><span class="sxs-lookup"><span data-stu-id="d938a-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="d938a-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d938a-128">Select **OK**.</span></span> <span data-ttu-id="d938a-129">Esimest lehte kasutatakse deposiitkviitungi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="d938a-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="d938a-130">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d938a-130">Select **OK**.</span></span> <span data-ttu-id="d938a-131">Teise etapina tuleb deposiitkviitung printida, kuid see etapp pole nõutav.</span><span class="sxs-lookup"><span data-stu-id="d938a-131">The second step is to print the deposit slip, but this step is not required.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]