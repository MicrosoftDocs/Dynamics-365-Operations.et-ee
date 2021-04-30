---
title: Tühistatud sisestustööleht
description: See teema kirjeldab võimeid, mis võimaldavad kandeid kannete loendist või finantslehtedelt tagasi võtta.
author: MikeFalkner
ms.date: 10/08/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: roschloma
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ab53f4b8888f77cd41ccbd7956ed307ba1b54ff
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897132"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="04b25-103">Tühistatud sisestustööleht</span><span class="sxs-lookup"><span data-stu-id="04b25-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04b25-104">See teema kirjeldab võimalusi lahenduses Microsoft Dynamics 365 Finance, mis lubavad teil kogu töölehe tagasi võtta või ühe või mitu kannet kannete loendist tagasi võtta, sõltumata nende päritolust.</span><span class="sxs-lookup"><span data-stu-id="04b25-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal, or reverse one or more vouchers from the voucher transaction list, regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="04b25-105">Töölehtede tühistamine</span><span class="sxs-lookup"><span data-stu-id="04b25-105">Reversing journals</span></span>

<span data-ttu-id="04b25-106">Töölehe ridu saate ükshaaval muuta.</span><span class="sxs-lookup"><span data-stu-id="04b25-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="04b25-107">Tühistatud töölehe sisestamisega saate ka kogu Finantstöölehe tagasi võtta.</span><span class="sxs-lookup"><span data-stu-id="04b25-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="04b25-108">Töölehe tühistamine:</span><span class="sxs-lookup"><span data-stu-id="04b25-108">To reverse a journal:</span></span> 

- <span data-ttu-id="04b25-109">Avage finantstööleht ja sisestatud töölehtede filter.</span><span class="sxs-lookup"><span data-stu-id="04b25-109">Open the financial journal and filter on posted journals.</span></span>
- <span data-ttu-id="04b25-110">Valige lehe ülaosas olevas menüüs **Storneeri**.</span><span class="sxs-lookup"><span data-stu-id="04b25-110">Select the **Reverse** menu at the top of the page.</span></span>
- <span data-ttu-id="04b25-111">Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat</span><span class="sxs-lookup"><span data-stu-id="04b25-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="04b25-112">Valige **Jah**, et kasutada olemasolevaid kande kuupäevi, või **Ei**, et sisestada uus.</span><span class="sxs-lookup"><span data-stu-id="04b25-112">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="04b25-113">Mõnel juhul võib algse kande perioodi sulgeda ja tühistamise jaoks tuleb sisestada uue kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04b25-113">In some cases, the period of the original transaction may be closed and you must enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="04b25-114">Kui valisite **Ei**, sisestage tühistamise kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04b25-114">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="04b25-115">Sisestage kommentaar, mida soovite tühistamise kandele lisada.</span><span class="sxs-lookup"><span data-stu-id="04b25-115">Enter a comment that you want added to the reversal transaction.</span></span>
- <span data-ttu-id="04b25-116">Valige nupp **Storneeri**.</span><span class="sxs-lookup"><span data-stu-id="04b25-116">Select the **Reverse** button.</span></span>

<span data-ttu-id="04b25-117">Kanded tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="04b25-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="04b25-118">Kui kande on üle 100 rea, käivitatakse tühistamise protsess pakktöötluse abil.</span><span class="sxs-lookup"><span data-stu-id="04b25-118">If the voucher contains more than 100 lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="04b25-119">Tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös.</span><span class="sxs-lookup"><span data-stu-id="04b25-119">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="04b25-120">Kõik kanded, mida ei saanud tühistada, loetletakse pakett-töö ajaloos.</span><span class="sxs-lookup"><span data-stu-id="04b25-120">Any transactions that couldn't be reversed will be listed in the batch job history.</span></span>

<span data-ttu-id="04b25-121">Kui kandes on kuni 100 rida, käivitub tühistamise protsess kohe.</span><span class="sxs-lookup"><span data-stu-id="04b25-121">If the voucher contains 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="04b25-122">Tulemused esitatakse dialoogiboksis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, koos põhjusega, miks seda ei saanud tühistada.</span><span class="sxs-lookup"><span data-stu-id="04b25-122">The results will be presented in a dialog box that shows any voucher that could not be reversed, along with the reason why it could not be reversed.</span></span> <span data-ttu-id="04b25-123">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="04b25-123">Select **OK** to close the dialog box.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="04b25-124">Kande tühistamine kannete loendist.</span><span class="sxs-lookup"><span data-stu-id="04b25-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="04b25-125">Samuti saate kandeid **kannete loendist** tagasi võtta kõigis pearaamatutes.</span><span class="sxs-lookup"><span data-stu-id="04b25-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="04b25-126">Lisaks saate ümber nimetada rohkem kui ühe kande korraga.</span><span class="sxs-lookup"><span data-stu-id="04b25-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="04b25-127">Ühe või mitme kande tühistamine:</span><span class="sxs-lookup"><span data-stu-id="04b25-127">To reverse one or more vouchers:</span></span> 

- <span data-ttu-id="04b25-128">Valige lehe ülaosas olevas menüüs **Storneeri**</span><span class="sxs-lookup"><span data-stu-id="04b25-128">Select the **Reverse** menu at the top of the page</span></span>
- <span data-ttu-id="04b25-129">Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat.</span><span class="sxs-lookup"><span data-stu-id="04b25-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed.</span></span>
- <span data-ttu-id="04b25-130">Valige **Jah**, et kasutada olemasolevaid kande kuupäevi, või **Ei**, et sisestada uus.</span><span class="sxs-lookup"><span data-stu-id="04b25-130">Select **Yes** to use the existing transaction dates or **No** to enter a new one.</span></span> <span data-ttu-id="04b25-131">Mõnel juhul võib algse kande perioodi sulgeda ja selle tühistamiseks tuleb sisestada uue kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04b25-131">In some cases, the period of the original transaction may be closed and you must enter a new transaction date to reverse it.</span></span>
- <span data-ttu-id="04b25-132">Kui valisite **Ei**, sisestage tühistamise kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="04b25-132">If you select **No**, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="04b25-133">Saate sisestada märkuse tühistuskande kirjeldamiseks.</span><span class="sxs-lookup"><span data-stu-id="04b25-133">Enter a comment to describe the reversal transaction.</span></span>
- <span data-ttu-id="04b25-134">Valige nupp **Storneeri**.</span><span class="sxs-lookup"><span data-stu-id="04b25-134">Select the **Reverse** button.</span></span>

<span data-ttu-id="04b25-135">Kanded tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="04b25-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="04b25-136">Kui kandes on üle 100 rea, käivitatakse tühistamise protsess pakktöötluse abil.</span><span class="sxs-lookup"><span data-stu-id="04b25-136">If there are more than 100 voucher lines, the reversal process will run using the batch process.</span></span> <span data-ttu-id="04b25-137">Tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös.</span><span class="sxs-lookup"><span data-stu-id="04b25-137">You can review the results by viewing the comments in the batch job.</span></span> <span data-ttu-id="04b25-138">Kõik kanded, mida ei saanud tühistada, tuuakse ära pakett-töö ajaloos.</span><span class="sxs-lookup"><span data-stu-id="04b25-138">Any transactions that couldn't be reversed will be noted in the batch job history.</span></span>

<span data-ttu-id="04b25-139">Kui kanderidade arv on kuni 100, käivitub tühistamise protsess kohe.</span><span class="sxs-lookup"><span data-stu-id="04b25-139">If the number of voucher lines is 100 lines or fewer, the reversal process will run immediately.</span></span> <span data-ttu-id="04b25-140">Tulemused kuvatakse dialoogiboksis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, koos põhjusega.</span><span class="sxs-lookup"><span data-stu-id="04b25-140">The results will display in a dialog box that shows any voucher that couldn't be reversed, along with the reason why.</span></span> <span data-ttu-id="04b25-141">Valige dialoogiboksi sulgemiseks suvand **OK**.</span><span class="sxs-lookup"><span data-stu-id="04b25-141">Select **OK** to close the dialog box.</span></span>

<span data-ttu-id="04b25-142">Kandeid saab tühistada ainult juhul, kui need vastavad nende tühistamise ärireeglitele.</span><span class="sxs-lookup"><span data-stu-id="04b25-142">Transactions can be reversed only if they meet the business rules for reversing them.</span></span> <span data-ttu-id="04b25-143">Hankija makseid ei saa muuta, kasutades selles teemas kirjeldatud võimalusi.</span><span class="sxs-lookup"><span data-stu-id="04b25-143">Vendor payments cannot be reversed using the capability described in this topic.</span></span> <span data-ttu-id="04b25-144">Hankija maksed tuleb tagasi võtta, järgides juhiseid, mis on toodud teemas [Hankija makse storneerimine](../accounts-payable/reverse-vendor-payment.md).</span><span class="sxs-lookup"><span data-stu-id="04b25-144">Vendor payments must be reversed by following the steps listed in [Reverse a vendor payment](../accounts-payable/reverse-vendor-payment.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]