--- 
title: "Arve põhiandmed ostureskontrosse kinnitamise töölehe abil"
description: "Selles tegevuse juhises näitlikustatakse, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutada kinnitamise töölehte kulukontode värskendamiseks."
author: abruer
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: d50ad27dc70a053dbe0b6d73688cd95f09cefd11
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="d91bd-103">Arve põhiandmed ostureskontrosse kinnitamise töölehe abil</span><span class="sxs-lookup"><span data-stu-id="d91bd-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d91bd-104">Selles tegevuse juhises näitlikustatakse, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kasutada kinnitamise töölehte kulukontode värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d91bd-104">This task guide will show you how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>


## <a name="create-and-post-and-invoice"></a><span data-ttu-id="d91bd-105">Arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="d91bd-105">Create and post and invoice</span></span>
1. <span data-ttu-id="d91bd-106">Avage Ostureskontro > Arved > Arveregister.</span><span class="sxs-lookup"><span data-stu-id="d91bd-106">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="d91bd-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d91bd-107">Click New.</span></span>
3. <span data-ttu-id="d91bd-108">Valige selle arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="d91bd-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="d91bd-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d91bd-109">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d91bd-110">Registri avamiseks ja kuluridade sisestamiseks klõpsake nuppu Read.</span><span class="sxs-lookup"><span data-stu-id="d91bd-110">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="d91bd-111">Valige hankija.</span><span class="sxs-lookup"><span data-stu-id="d91bd-111">Select a vendor.</span></span> <span data-ttu-id="d91bd-112">Näiteks sisestage või valige US‑104</span><span class="sxs-lookup"><span data-stu-id="d91bd-112">For example, enter or select US-104</span></span>
7. <span data-ttu-id="d91bd-113">Sisestage väärtus väljale Arve.</span><span class="sxs-lookup"><span data-stu-id="d91bd-113">In the Invoice field, type a value.</span></span>
8. <span data-ttu-id="d91bd-114">Sisestage väärtus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d91bd-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="d91bd-115">Sisestage arv väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="d91bd-115">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="d91bd-116">Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d91bd-116">In the Approved by field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="d91bd-117">Tõstke kinnitaja esile ja klõpsake nuppu Vali, et see kinnitaja valida.</span><span class="sxs-lookup"><span data-stu-id="d91bd-117">Highlight an approver and click Select to select that approver.</span></span>
12. <span data-ttu-id="d91bd-118">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="d91bd-118">Click Post.</span></span>
13. <span data-ttu-id="d91bd-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d91bd-119">Close the page.</span></span>
14. <span data-ttu-id="d91bd-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d91bd-120">Close the page.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="d91bd-121">Arve heakskiitmine</span><span class="sxs-lookup"><span data-stu-id="d91bd-121">Approve an invoice</span></span>
1. <span data-ttu-id="d91bd-122">Avage Ostureskontro > Arved > Arve kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="d91bd-122">Go to Accounts payable > Invoices > Invoice approval.</span></span>
2. <span data-ttu-id="d91bd-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d91bd-123">Click New.</span></span>
3. <span data-ttu-id="d91bd-124">Valige soovitud arve kinnitamise töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="d91bd-124">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="d91bd-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d91bd-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="d91bd-126">Klõpsake valikud Read, et kuvada lehekülg, kus saate valida kinnitatavad arved.</span><span class="sxs-lookup"><span data-stu-id="d91bd-126">Click lines to display a page where you will be able to select the invoices that you want to approve.</span></span>
6. <span data-ttu-id="d91bd-127">Valige Kannete otsimine, et kuvada kõiki arveid, mis on kinnitamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="d91bd-127">Select Find Vouchers to display all of the invoices that are ready for approval.</span></span>
7. <span data-ttu-id="d91bd-128">Märkige loodud arve.</span><span class="sxs-lookup"><span data-stu-id="d91bd-128">Mark the invoice that you created.</span></span>
8. <span data-ttu-id="d91bd-129">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="d91bd-129">Click Select.</span></span>
    * <span data-ttu-id="d91bd-130">Ülal valitud kanded viiakse sellesse loendisse pärast nende valimist.</span><span class="sxs-lookup"><span data-stu-id="d91bd-130">The vouchers that you selected above are moved to this list after you select them.</span></span>  
9. <span data-ttu-id="d91bd-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d91bd-131">Click OK.</span></span>
10. <span data-ttu-id="d91bd-132">Arvele kulukonto lisamiseks klõpsake kontonumbri väljal.</span><span class="sxs-lookup"><span data-stu-id="d91bd-132">Click on the account number field to add an expense account to the invoice.</span></span>
11. <span data-ttu-id="d91bd-133">Sisestage kontonumber ja klõpsake väljapool välja.</span><span class="sxs-lookup"><span data-stu-id="d91bd-133">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="d91bd-134">Näiteks sisestage 600120.</span><span class="sxs-lookup"><span data-stu-id="d91bd-134">For example, enter 600120.</span></span>
12. <span data-ttu-id="d91bd-135">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="d91bd-135">Click Post.</span></span>
13. <span data-ttu-id="d91bd-136">Sisestatud kannete kuvamiseks klõpsake valikut Kanne.</span><span class="sxs-lookup"><span data-stu-id="d91bd-136">Click Voucher to view the entries that were posted.</span></span>
    * <span data-ttu-id="d91bd-137">Kinnituse ootel arvete konto tühistatakse ja asendatakse tegeliku kulukontoga.</span><span class="sxs-lookup"><span data-stu-id="d91bd-137">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  


