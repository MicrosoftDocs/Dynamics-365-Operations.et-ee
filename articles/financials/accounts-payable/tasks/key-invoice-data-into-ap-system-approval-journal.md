---
title: Arve põhiandmed AP-süsteemi, kasutades kinnitamise töölehte
description: Selles tegevuse juhises näitlikustatakse, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutada kinnitamise töölehte kulukontode värskendamiseks.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0faece510cc85fd86113d8b62d54b71f3014b1db
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837033"
---
# <a name="key-invoice-data-into-ap-system-using-approval-journal"></a><span data-ttu-id="92171-103">Arve põhiandmed AP-süsteemi, kasutades kinnitamise töölehte</span><span class="sxs-lookup"><span data-stu-id="92171-103">Key invoice data into AP system using approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92171-104">Selles tegevuse juhises näitlikustatakse, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutada kinnitamise töölehte kulukontode värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="92171-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="92171-105">Arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="92171-105">Create and post and invoice</span></span>
1. <span data-ttu-id="92171-106">Avage Ostureskontro > Arved > Arveregister.</span><span class="sxs-lookup"><span data-stu-id="92171-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="92171-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="92171-107">Click New.</span></span>
3. <span data-ttu-id="92171-108">Valige selle arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="92171-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="92171-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="92171-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="92171-110">Registri avamiseks ja kuluridade sisestamiseks klõpsake nuppu Read.</span><span class="sxs-lookup"><span data-stu-id="92171-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="92171-111">Valige hankija.</span><span class="sxs-lookup"><span data-stu-id="92171-111">Select a vendor.</span></span> <span data-ttu-id="92171-112">Näiteks sisestage või valige US‑104</span><span class="sxs-lookup"><span data-stu-id="92171-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="92171-113">Sisestage väärtus väljale Arve.</span><span class="sxs-lookup"><span data-stu-id="92171-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="92171-114">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="92171-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="92171-115">Sisestage arv väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="92171-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="92171-116">Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="92171-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="92171-117">Tõstke kinnitaja esile ja klõpsake nuppu Vali, et see kinnitaja valida.</span><span class="sxs-lookup"><span data-stu-id="92171-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="92171-118">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="92171-118">Click Post.</span></span>
13. <span data-ttu-id="92171-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="92171-119">Close the page.</span></span>
14. <span data-ttu-id="92171-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="92171-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="92171-121">Arve heakskiitmine</span><span class="sxs-lookup"><span data-stu-id="92171-121">Approve an invoice</span></span>
1. <span data-ttu-id="92171-122">Avage Ostureskontro > Arved > Arve kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="92171-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="92171-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="92171-123">Click New.</span></span>
3. <span data-ttu-id="92171-124">Valige soovitud arve kinnitamise töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="92171-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="92171-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="92171-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="92171-126">Klõpsake valikud Read, et kuvada lehekülg, kus saate valida kinnitatavad arved.</span><span class="sxs-lookup"><span data-stu-id="92171-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="92171-127">Valige Kannete otsimine, et kuvada kõiki arveid, mis on kinnitamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="92171-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="92171-128">Märkige loodud arve.</span><span class="sxs-lookup"><span data-stu-id="92171-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="92171-129">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="92171-129">Click Select.</span></span>
    * <span data-ttu-id="92171-130">Ülal valitud kanded viiakse sellesse loendisse pärast nende valimist.</span><span class="sxs-lookup"><span data-stu-id="92171-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="92171-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="92171-131">Click OK.</span></span>
10. <span data-ttu-id="92171-132">Arvele kulukonto lisamiseks klõpsake kontonumbri väljal.</span><span class="sxs-lookup"><span data-stu-id="92171-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="92171-133">Sisestage kontonumber ja klõpsake väljapool välja.</span><span class="sxs-lookup"><span data-stu-id="92171-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="92171-134">Näiteks sisestage 600120.</span><span class="sxs-lookup"><span data-stu-id="92171-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="92171-135">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="92171-135">Click Post.</span></span>
13. <span data-ttu-id="92171-136">Sisestatud kannete kuvamiseks klõpsake valikut Kanne.</span><span class="sxs-lookup"><span data-stu-id="92171-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="92171-137">Kinnituse ootel arvete konto tühistatakse ja asendatakse tegeliku kulukontoga.</span><span class="sxs-lookup"><span data-stu-id="92171-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

