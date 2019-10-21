---
title: Tühistatud sisestustööleht
description: See teema kirjeldab võimeid, mis võimaldavad kandeid kannete loendist või finantslehtedelt tagasi võtta.
author: MikeFalkner
manager: AnnBe
ms.date: 08/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransVoucher, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a5456e60f1f3cee5f83ac7f725f7e01ba5bd7a1
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2248581"
---
# <a name="reverse-journal-posting"></a><span data-ttu-id="a4f03-103">Tühistatud sisestustööleht</span><span class="sxs-lookup"><span data-stu-id="a4f03-103">Reverse journal posting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4f03-104">See teema kirjeldab võimeid Microsoft Dynamics 365 Finance, mis lubab teil kogu töölehe tagasi võtta või ühe või mitu kannet kannete loendist tagasi võtta, sõltumata nende päritolust.</span><span class="sxs-lookup"><span data-stu-id="a4f03-104">This topic describes capabilities Microsoft Dynamics 365 Finance that allows you to reverse an entire journal or reverse one or more vouchers from the voucher transaction list regardless of their origin.</span></span> 

## <a name="reversing-journals"></a><span data-ttu-id="a4f03-105">Töölehtede tühistamine</span><span class="sxs-lookup"><span data-stu-id="a4f03-105">Reversing journals</span></span>

<span data-ttu-id="a4f03-106">Töölehe ridu saate ükshaaval muuta.</span><span class="sxs-lookup"><span data-stu-id="a4f03-106">You can reverse journal lines individually.</span></span> <span data-ttu-id="a4f03-107">Tühistatud töölehe sisestamisega saate ka kogu Finantstöölehe tagasi võtta.</span><span class="sxs-lookup"><span data-stu-id="a4f03-107">With reverse journal posting, you can also reverse an entire financial journal.</span></span> <span data-ttu-id="a4f03-108">Töölehe tühistamine:</span><span class="sxs-lookup"><span data-stu-id="a4f03-108">To reverse a journal:</span></span> 
- <span data-ttu-id="a4f03-109">Finantstöölehe ja sisestatud töölehtede filtri avamine</span><span class="sxs-lookup"><span data-stu-id="a4f03-109">Open the financial journal and filter on posted journals</span></span>
- <span data-ttu-id="a4f03-110">Klõpsake vormi ülaosas olevas menüüs nuppu Tühista.</span><span class="sxs-lookup"><span data-stu-id="a4f03-110">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="a4f03-111">Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat</span><span class="sxs-lookup"><span data-stu-id="a4f03-111">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="a4f03-112">Valige Jah, et kasutada olemasolevaid kande kuupäevi või Ei, et sisestada uus.</span><span class="sxs-lookup"><span data-stu-id="a4f03-112">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="a4f03-113">Mõnel juhul võib algse kande perioodi sulgeda ja soovite sisestada uue kande kuupäeva tühistamisele.</span><span class="sxs-lookup"><span data-stu-id="a4f03-113">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="a4f03-114">Kui valisite Ei, sisestage tühistamise kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a4f03-114">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="a4f03-115">Sisestage kommentaar, mida soovite tühistamise kandele lisada.</span><span class="sxs-lookup"><span data-stu-id="a4f03-115">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="a4f03-116">Klõpsake nuppu Tühista.</span><span class="sxs-lookup"><span data-stu-id="a4f03-116">Click the Reverse button</span></span>

<span data-ttu-id="a4f03-117">Kanded tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="a4f03-117">The transactions will be reversed.</span></span> 

<span data-ttu-id="a4f03-118">Kui kanderidade arv ületab 100 rida, käivitatakse tühistamise protsess pakktöötluse abil.</span><span class="sxs-lookup"><span data-stu-id="a4f03-118">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="a4f03-119">Tühistamise tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös, mis käivitati.</span><span class="sxs-lookup"><span data-stu-id="a4f03-119">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="a4f03-120">Kõik tõrked märgitakse pakett-töö ajaloos.</span><span class="sxs-lookup"><span data-stu-id="a4f03-120">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="a4f03-121">Kui vutšeri ridade arv on 100 või vähem, käivitub tühistamise protsess kohe.</span><span class="sxs-lookup"><span data-stu-id="a4f03-121">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="a4f03-122">Tulemused esitatakse dialoogis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, ja põhjus, miks seda ei saanud tühistada.</span><span class="sxs-lookup"><span data-stu-id="a4f03-122">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="a4f03-123">Klõpsake OK, et dialoogiboksi sulgeda.</span><span class="sxs-lookup"><span data-stu-id="a4f03-123">Click on Ok to close the dialog.</span></span>

## <a name="reversing-vouchers-from-the-voucher-transaction-list"></a><span data-ttu-id="a4f03-124">Kande tühistamine kannete loendist.</span><span class="sxs-lookup"><span data-stu-id="a4f03-124">Reversing vouchers from the voucher transaction list.</span></span> 

<span data-ttu-id="a4f03-125">Samuti saate kandeid **kannete loendist** tagasi võtta kõigis pearaamatutes.</span><span class="sxs-lookup"><span data-stu-id="a4f03-125">You can also reverse vouchers from the **Voucher transaction list** across all subledgers.</span></span> <span data-ttu-id="a4f03-126">Lisaks saate ümber nimetada rohkem kui ühe kande korraga.</span><span class="sxs-lookup"><span data-stu-id="a4f03-126">In addition, you can reverse more than one voucher at a time.</span></span> 

<span data-ttu-id="a4f03-127">Ühe või mitme kande tühistamine:</span><span class="sxs-lookup"><span data-stu-id="a4f03-127">To reverse one or more vouchers:</span></span> 
- <span data-ttu-id="a4f03-128">Klõpsake vormi ülaosas olevas menüüs nuppu Tühista.</span><span class="sxs-lookup"><span data-stu-id="a4f03-128">Click on the Reverse menu at the top of the page</span></span>
- <span data-ttu-id="a4f03-129">Näete kannete ja kanderidade koguarvu, samuti tühistatud ridade kogusummat</span><span class="sxs-lookup"><span data-stu-id="a4f03-129">You will see the total number of vouchers and voucher lines as well as the total amount of the lines being reversed</span></span>
- <span data-ttu-id="a4f03-130">Valige Jah, et kasutada olemasolevaid kande kuupäevi või Ei, et sisestada uus.</span><span class="sxs-lookup"><span data-stu-id="a4f03-130">Select Yes to use the existing transaction dates or No to enter a new one.</span></span> <span data-ttu-id="a4f03-131">Mõnel juhul võib algse kande perioodi sulgeda ja soovite sisestada uue kande kuupäeva tühistamisele.</span><span class="sxs-lookup"><span data-stu-id="a4f03-131">In some cases, the period of the original transaction may be closed and you want to enter a new transaction date for the reversal.</span></span>
- <span data-ttu-id="a4f03-132">Kui valisite Ei, sisestage tühistamise kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a4f03-132">If you selected No, enter a transaction date for the reversal.</span></span> 
- <span data-ttu-id="a4f03-133">Sisestage kommentaar, mida soovite tühistamise kandele lisada.</span><span class="sxs-lookup"><span data-stu-id="a4f03-133">Enter a comment that you want added to the reversal transaction</span></span>
- <span data-ttu-id="a4f03-134">Klõpsake nuppu Tühista.</span><span class="sxs-lookup"><span data-stu-id="a4f03-134">Click the Reverse button</span></span>

<span data-ttu-id="a4f03-135">Kanded tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="a4f03-135">The transactions will be reversed.</span></span> 

<span data-ttu-id="a4f03-136">Kui kanderidade arv ületab 100 rida, käivitatakse tühistamise protsess pakktöötluse abil.</span><span class="sxs-lookup"><span data-stu-id="a4f03-136">If the number of voucher lines exceeds 100 lines, the reversal process will be run using the batch process.</span></span> <span data-ttu-id="a4f03-137">Tühistamise tulemusi saate üle vaadata, kui vaatate kommentaare pakett-töös, mis käivitati.</span><span class="sxs-lookup"><span data-stu-id="a4f03-137">You can review the results of the reversal by viewing the comments in the batch job that was run.</span></span> <span data-ttu-id="a4f03-138">Kõik tõrked märgitakse pakett-töö ajaloos.</span><span class="sxs-lookup"><span data-stu-id="a4f03-138">All failures will be noted in the batch job history.</span></span>

<span data-ttu-id="a4f03-139">Kui vutšeri ridade arv on 100 või vähem, käivitub tühistamise protsess kohe.</span><span class="sxs-lookup"><span data-stu-id="a4f03-139">If the number of voucher lines is 100 lines or less, the reversal process will run immediately.</span></span> <span data-ttu-id="a4f03-140">Tulemused esitatakse dialoogis, kus kuvatakse mis tahes kannet, mida ei saanud tühistada, ja põhjus, miks seda ei saanud tühistada.</span><span class="sxs-lookup"><span data-stu-id="a4f03-140">The results will be presented in a dialog that shows any voucher that could not be reversed and the reason why it could not be reversed.</span></span> <span data-ttu-id="a4f03-141">Klõpsake OK, et dialoogiboksi sulgeda.</span><span class="sxs-lookup"><span data-stu-id="a4f03-141">Click on Ok to close the dialog.</span></span>

