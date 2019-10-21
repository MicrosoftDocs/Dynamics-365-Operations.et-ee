---
title: Arve põhiandmed ostureskontrosse kinnitamise töölehe abil
description: See teema selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kinnituslehte kulukontode värskendamiseks.
author: abruer
manager: AnnBe
ms.date: 08/08/2019
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
ms.openlocfilehash: fb690769a33f88e63ab8f54cec69a5e927fd324c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177412"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a><span data-ttu-id="b6c99-103">Arve põhiandmed ostureskontrosse kinnitamise töölehe abil</span><span class="sxs-lookup"><span data-stu-id="b6c99-103">Key invoice data into accounts payable using an approval journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b6c99-104">See teema selgitab, kuidas kasutada arveregistrit arvete loomiseks ja seejärel kinnituslehte kulukontode värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="b6c99-104">This topic explains how to use the invoice register to create invoices and then use the approval journal to update the expense accounts.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="b6c99-105">Arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="b6c99-105">Create and post and invoice</span></span>
1. <span data-ttu-id="b6c99-106">Minge navigeerimispaanil jaotisse **Moodulid > Ostureskontro > Arved > Arveregister**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-106">In the navigation pan, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="b6c99-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-107">Select **New**.</span></span>
3. <span data-ttu-id="b6c99-108">Valige selle arveregistri nimi, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="b6c99-108">Select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="b6c99-109">Registri avamiseks ja kuluridade sisestamiseks valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-109">Select **Lines** to open the register and enter expense lines.</span></span>
5. <span data-ttu-id="b6c99-110">Valige hankija.</span><span class="sxs-lookup"><span data-stu-id="b6c99-110">Select a vendor.</span></span> <span data-ttu-id="b6c99-111">Näiteks sisestage või valige `US-104`.</span><span class="sxs-lookup"><span data-stu-id="b6c99-111">For example, enter or select `US-104`.</span></span>
6. <span data-ttu-id="b6c99-112">Sisestage väärtus väljale **Arve**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-112">In the **Invoice** field, type a value.</span></span>
7. <span data-ttu-id="b6c99-113">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-113">In the **Description** field, type a value.</span></span>
8. <span data-ttu-id="b6c99-114">Sisestage number väljale **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-114">In the **Credit** field, enter a number.</span></span>
9. <span data-ttu-id="b6c99-115">Väljal **Kinnitaja** valige rippmenüüst kinnitaja.</span><span class="sxs-lookup"><span data-stu-id="b6c99-115">In the **Approved by** field, select an approver from the drop-down menu.</span></span>
10. <span data-ttu-id="b6c99-116">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-116">Select **Post**.</span></span>

## <a name="approve-an-invoice"></a><span data-ttu-id="b6c99-117">Arve heakskiitmine</span><span class="sxs-lookup"><span data-stu-id="b6c99-117">Approve an invoice</span></span>
1. <span data-ttu-id="b6c99-118">Avage navigeerimispaanil **Moodulid > Ostureskontro > Arved > Arve kinnitus**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-118">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice approval**.</span></span>
2. <span data-ttu-id="b6c99-119">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-119">Select **New**.</span></span>
3. <span data-ttu-id="b6c99-120">Valige soovitud arve kinnitamise töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="b6c99-120">Select the name of the invoice approval journal that you want to use.</span></span>
4. <span data-ttu-id="b6c99-121">Valige **Read**, et kuvada leht, kus saate valida arved, mille soovite kinnitada.</span><span class="sxs-lookup"><span data-stu-id="b6c99-121">Select **Lines** to display a page where you will be able to select the invoices that you want to approve.</span></span>
5. <span data-ttu-id="b6c99-122">Valige **Leia vautšerid**, et kuvada kõik kinnitamiseks valmis olevad arved.</span><span class="sxs-lookup"><span data-stu-id="b6c99-122">Select **Find Vouchers** to display all of the invoices that are ready for approval.</span></span>
6. <span data-ttu-id="b6c99-123">Märkige loodud arve ja klõpsake siis **Vali**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-123">Mark the invoice that you created, then click **Select**.</span></span> <span data-ttu-id="b6c99-124">Ülal valitud kanded viiakse sellesse loendisse pärast nende valimist.</span><span class="sxs-lookup"><span data-stu-id="b6c99-124">The vouchers that you selected above are moved to this list after you select them.</span></span>  
7. <span data-ttu-id="b6c99-125">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-125">Select **OK**.</span></span>
8. <span data-ttu-id="b6c99-126">Valige **konto numbri** väli, et lisada arvele kulukonto.</span><span class="sxs-lookup"><span data-stu-id="b6c99-126">Select the **account number** field to add an expense account to the invoice.</span></span>
9. <span data-ttu-id="b6c99-127">Sisestage kontonumber ja klõpsake väljapool välja.</span><span class="sxs-lookup"><span data-stu-id="b6c99-127">Enter an account number and tab off of the field.</span></span> <span data-ttu-id="b6c99-128">Sisestage näiteks `600120`.</span><span class="sxs-lookup"><span data-stu-id="b6c99-128">For example, enter `600120`.</span></span>
10. <span data-ttu-id="b6c99-129">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-129">Select **Post**.</span></span>
11. <span data-ttu-id="b6c99-130">Postitatud kirjete vaatamiseks valige **Vautšer**.</span><span class="sxs-lookup"><span data-stu-id="b6c99-130">Select **Voucher** to view the entries that were posted.</span></span> <span data-ttu-id="b6c99-131">Kinnituse ootel arvete konto tühistatakse ja asendatakse tegeliku kulukontoga.</span><span class="sxs-lookup"><span data-stu-id="b6c99-131">The Invoice Pending Approval account is reversed and replaced with the actual expense account.</span></span>  

