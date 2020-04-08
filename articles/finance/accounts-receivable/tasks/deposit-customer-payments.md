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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1d903f557fbaeb720dd4a34dc1c772be0dcb56eb
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140172"
---
# <a name="deposit-customer-payments"></a><span data-ttu-id="db53b-103">Kliendimaksete deponeerimine</span><span class="sxs-lookup"><span data-stu-id="db53b-103">Deposit customer payments</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db53b-104">Hoiustage kliendimaksed.</span><span class="sxs-lookup"><span data-stu-id="db53b-104">Deposit customer payments.</span></span> <span data-ttu-id="db53b-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="db53b-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="db53b-106">Avage **Navigeerimispaan > Moodulid > Müügireskontro > Maksed > Maksete töölehed**.</span><span class="sxs-lookup"><span data-stu-id="db53b-106">Go to **Navigation pane > Modules > Accounts receivable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="db53b-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="db53b-107">Select **New**.</span></span>
3. <span data-ttu-id="db53b-108">Väljal **Nimi** valige rippmenüüst **CustPay**.</span><span class="sxs-lookup"><span data-stu-id="db53b-108">In the **Name** field, select **CustPay** in the drop-down menu.</span></span>
4. <span data-ttu-id="db53b-109">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="db53b-109">Select **Lines**.</span></span>
5. <span data-ttu-id="db53b-110">Väljal **Konto** valige klient, kelle jaoks registreerite makset.</span><span class="sxs-lookup"><span data-stu-id="db53b-110">In the **Account** field, select the customer for whom you are recording the payment.</span></span>
6. <span data-ttu-id="db53b-111">Väljale **Kreedit** sisestage maksesumma.</span><span class="sxs-lookup"><span data-stu-id="db53b-111">In the **Credit** field, enter the amount of the payment.</span></span> <span data-ttu-id="db53b-112">Saate valida summa tühjaks jätmise ja lasta selle süsteemil arvutada, valides makstud arved.</span><span class="sxs-lookup"><span data-stu-id="db53b-112">You can choose to leave the amount blank, and have the system calculate it by selecting the invoices which were paid.</span></span>  
7. <span data-ttu-id="db53b-113">Väljale **Makse viide** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="db53b-113">In the **Payment reference** field, type a value.</span></span> <span data-ttu-id="db53b-114">Makse viiteks võib olla sisestatava makse tšeki number.</span><span class="sxs-lookup"><span data-stu-id="db53b-114">The payment reference could be the check number for the payment you are entering.</span></span> <span data-ttu-id="db53b-115">Makse viide on vajalik makse kaasamiseks deposiitkviitungile.</span><span class="sxs-lookup"><span data-stu-id="db53b-115">The payment reference is required in order to include the payment on a deposit slip.</span></span>  
8. <span data-ttu-id="db53b-116">Märkige ruut Kasuta deposiitkviitungit.</span><span class="sxs-lookup"><span data-stu-id="db53b-116">Mark the box Use a deposit slip.</span></span> <span data-ttu-id="db53b-117">Kui makse tuleks deposiiti kaasata, muutke sätte väärtuseks Jah.</span><span class="sxs-lookup"><span data-stu-id="db53b-117">If the payment should be included in the deposit, change this setting to Yes.</span></span>  
9. <span data-ttu-id="db53b-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="db53b-118">Select **New**.</span></span>
10. <span data-ttu-id="db53b-119">Väljal **Konto** valige klient järgmise makse jaoks.</span><span class="sxs-lookup"><span data-stu-id="db53b-119">In the **Account** field, select the customer for the next payment.</span></span>
11. <span data-ttu-id="db53b-120">Väljale **Kreedit** sisestage maksesumma.</span><span class="sxs-lookup"><span data-stu-id="db53b-120">In the **Credit** field, enter the payment amount.</span></span>
12. <span data-ttu-id="db53b-121">Väljale **Makse viide** sisestage väärtus.</span><span class="sxs-lookup"><span data-stu-id="db53b-121">In the **Payment reference** field, type a value.</span></span>
13. <span data-ttu-id="db53b-122">Märkige ruut **Kasuta deposiitkviitungit**.</span><span class="sxs-lookup"><span data-stu-id="db53b-122">Mark the box **Use a deposit slip**.</span></span>
14. <span data-ttu-id="db53b-123">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="db53b-123">Select **Post**.</span></span> <span data-ttu-id="db53b-124">Maksed tuleb sisestada enne deposiitkviitungi loomist.</span><span class="sxs-lookup"><span data-stu-id="db53b-124">Payments must be posted before the deposit slip can be generated.</span></span> <span data-ttu-id="db53b-125">See tagab, et maksed pärast deposiitkviitungi loomist ei muutuks.</span><span class="sxs-lookup"><span data-stu-id="db53b-125">This is to ensure that the payments don't change after the deposit slip is generated.</span></span>  
15. <span data-ttu-id="db53b-126">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="db53b-126">Select **Functions**.</span></span>
16. <span data-ttu-id="db53b-127">Valige **Deposiitkviitung**.</span><span class="sxs-lookup"><span data-stu-id="db53b-127">Select **Deposit slip**.</span></span>
17. <span data-ttu-id="db53b-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="db53b-128">Select **OK**.</span></span> <span data-ttu-id="db53b-129">Esimest lehte kasutatakse deposiitkviitungi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="db53b-129">The first page is used to create the deposit slip.</span></span>  
18. <span data-ttu-id="db53b-130">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="db53b-130">Select **OK**.</span></span> <span data-ttu-id="db53b-131">Teise etapina tuleb deposiitkviitung printida, kuid see etapp pole nõutav.</span><span class="sxs-lookup"><span data-stu-id="db53b-131">The second step is to print the deposit slip, but this step is not required.</span></span>  

