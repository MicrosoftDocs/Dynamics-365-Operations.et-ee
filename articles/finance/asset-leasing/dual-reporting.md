---
title: Topeltaruandlus
description: See teema juhendab teid läbi näite, mis näitab, kuidas saate täita nii rahvusvahelise finantsaruandluse standardi (IFRS) aruandlust kui ka vara rentimise kohustuslikku aruandlust.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6daa43178625316a40427728e7e4186691cc13c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229546"
---
# <a name="dual-reporting"></a><span data-ttu-id="91eda-103">Topeltaruandlus</span><span class="sxs-lookup"><span data-stu-id="91eda-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91eda-104">See teema juhendab teid läbi näite, mis näitab, kuidas saate täita nii rahvusvahelise finantsaruandluse standardi (IFRS) aruandlust kui ka vara rentimise kohustuslikku aruandlust.</span><span class="sxs-lookup"><span data-stu-id="91eda-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="91eda-105">Nõutav on rakenduses Microsoft Dynamics 365 Finance kihtide sisestamise kogemus ja see muudab näitest arusaamise lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="91eda-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="91eda-106">Näide</span><span class="sxs-lookup"><span data-stu-id="91eda-106">Example</span></span>

<span data-ttu-id="91eda-107">Järgmine näide kehtib rentimisele Itaalia seadusliku aruande korral, kasutades nii sularahapõhist meetodit kui ka IFRS-i aruandluse meetodeid.</span><span class="sxs-lookup"><span data-stu-id="91eda-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="91eda-108">Ettevõte peab looma kolm raamatut, et täita nii Itaalia seadusjärgsed nõuded kui ka IFRS 16 nõuded.</span><span class="sxs-lookup"><span data-stu-id="91eda-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="91eda-109">Üks raamat on vajalik IFRS 16 jaoks, üks raamat on nõutav kohustuslike nõuete jaoks ja üks raamat on nõutav seaduslike postituste automaatne tagasipööramine.</span><span class="sxs-lookup"><span data-stu-id="91eda-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="91eda-110">Raamatud häälestatakse, nagu järgmistes tabelites on näidatud.</span><span class="sxs-lookup"><span data-stu-id="91eda-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="91eda-111">**IFRS 16 raamat**</span><span class="sxs-lookup"><span data-stu-id="91eda-111">**IFRS 16 book**</span></span>

<span data-ttu-id="91eda-112">IFRS 16 raamat on häälestatud nii, et see vastab IFRS 16 raamatupidamise standardile.</span><span class="sxs-lookup"><span data-stu-id="91eda-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="91eda-113">Kõik sellesse raamatusse sisestatavad kirjed postitatakse kliendi kihis.</span><span class="sxs-lookup"><span data-stu-id="91eda-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="91eda-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="91eda-114">Name</span></span>                                    | <span data-ttu-id="91eda-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="91eda-116">Žurnaali tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-116">Book type</span></span>                               | <span data-ttu-id="91eda-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="91eda-117">IFRS 16</span></span>        |
| <span data-ttu-id="91eda-118">Raamatu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-118">Book description</span></span>                        | <span data-ttu-id="91eda-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="91eda-119">IFRS 16</span></span>        |
| <span data-ttu-id="91eda-120">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="91eda-120">Posting Layer</span></span>                           | <span data-ttu-id="91eda-121">Kohandatud kiht 1</span><span class="sxs-lookup"><span data-stu-id="91eda-121">Custom layer 1</span></span> |
| <span data-ttu-id="91eda-122">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-122">Lease Type</span></span>                              | <span data-ttu-id="91eda-123">Finance</span><span class="sxs-lookup"><span data-stu-id="91eda-123">Finance</span></span>        |
| <span data-ttu-id="91eda-124">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="91eda-124">Accounting Framework</span></span>                    | <span data-ttu-id="91eda-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="91eda-125">IFRS 16</span></span>        |
| <span data-ttu-id="91eda-126">Rendiperioodi / kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="91eda-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="91eda-127">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-127">0.00</span></span>           |
| <span data-ttu-id="91eda-128">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="91eda-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="91eda-129">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-129">0.00</span></span>           |
| <span data-ttu-id="91eda-130">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="91eda-130">Short-term threshold</span></span>                    | <span data-ttu-id="91eda-131">12</span><span class="sxs-lookup"><span data-stu-id="91eda-131">12</span></span>             |
| <span data-ttu-id="91eda-132">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="91eda-132">Low Value Threshold</span></span>                     | <span data-ttu-id="91eda-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-133">5,000.00</span></span>       |
| <span data-ttu-id="91eda-134">Hankijale tasumine</span><span class="sxs-lookup"><span data-stu-id="91eda-134">Pay to Vendor</span></span>                           | <span data-ttu-id="91eda-135">Ei</span><span class="sxs-lookup"><span data-stu-id="91eda-135">No</span></span>             |

<span data-ttu-id="91eda-136">**Kohustuslik raamat**</span><span class="sxs-lookup"><span data-stu-id="91eda-136">**Statutory book**</span></span>

<span data-ttu-id="91eda-137">Kohustuslik raamat on sularahal põhinev raamat, kus ettevõte arvestab rendikogemust kui sularaha summat, mis makstakse iga kuu rendiks.</span><span class="sxs-lookup"><span data-stu-id="91eda-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="91eda-138">See raamat ei tekita õiget kasutamisõiguse esemeks olevat vara või rendikohustist.</span><span class="sxs-lookup"><span data-stu-id="91eda-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="91eda-139">Nimi</span><span class="sxs-lookup"><span data-stu-id="91eda-139">Name</span></span>                                    | <span data-ttu-id="91eda-140">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="91eda-141">Žurnaali tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-141">Book type</span></span>                               | <span data-ttu-id="91eda-142">Seaduslik</span><span class="sxs-lookup"><span data-stu-id="91eda-142">Statutory</span></span>   |
| <span data-ttu-id="91eda-143">Raamatu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-143">Book description</span></span>                        | <span data-ttu-id="91eda-144">Kohalik GAAP</span><span class="sxs-lookup"><span data-stu-id="91eda-144">Local GAAP</span></span>  |
| <span data-ttu-id="91eda-145">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="91eda-145">Posting Layer</span></span>                           | <span data-ttu-id="91eda-146">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-146">Current</span></span>     |
| <span data-ttu-id="91eda-147">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-147">Lease Type</span></span>                              | <span data-ttu-id="91eda-148">Automaatne</span><span class="sxs-lookup"><span data-stu-id="91eda-148">Automatic</span></span>   |
| <span data-ttu-id="91eda-149">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="91eda-149">Accounting Framework</span></span>                    | <span data-ttu-id="91eda-150">Kassapõhine</span><span class="sxs-lookup"><span data-stu-id="91eda-150">Cash basis</span></span>  |
| <span data-ttu-id="91eda-151">Rendiperioodi / kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="91eda-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="91eda-152">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-152">0.00</span></span>        |
| <span data-ttu-id="91eda-153">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="91eda-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="91eda-154">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-154">0.00</span></span>        |
| <span data-ttu-id="91eda-155">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="91eda-155">Short-term threshold</span></span>                    | <span data-ttu-id="91eda-156">0</span><span class="sxs-lookup"><span data-stu-id="91eda-156">0</span></span>           |
| <span data-ttu-id="91eda-157">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="91eda-157">Low Value Threshold</span></span>                     | <span data-ttu-id="91eda-158">0</span><span class="sxs-lookup"><span data-stu-id="91eda-158">0</span></span>           |
| <span data-ttu-id="91eda-159">Hankijale tasumine</span><span class="sxs-lookup"><span data-stu-id="91eda-159">Pay to Vendor</span></span>                           | <span data-ttu-id="91eda-160">Ei</span><span class="sxs-lookup"><span data-stu-id="91eda-160">No</span></span>          |

<span data-ttu-id="91eda-161">**Kohustusliku tagasivõtmise raamat**</span><span class="sxs-lookup"><span data-stu-id="91eda-161">**Statutory reversal book**</span></span>

<span data-ttu-id="91eda-162">Kohustuslik tagasivõtmise raamat häälestatakse sarnaselt kohustuslikule raamatule.</span><span class="sxs-lookup"><span data-stu-id="91eda-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="91eda-163">Nimi</span><span class="sxs-lookup"><span data-stu-id="91eda-163">Name</span></span>                                    | <span data-ttu-id="91eda-164">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="91eda-165">Žurnaali tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-165">Book type</span></span>                               | <span data-ttu-id="91eda-166">Kohustuslik – tagasivõtmime</span><span class="sxs-lookup"><span data-stu-id="91eda-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="91eda-167">Raamatu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-167">Book description</span></span>                        | <span data-ttu-id="91eda-168">Kohustustusliku raamatu tagasivõtmise raamat</span><span class="sxs-lookup"><span data-stu-id="91eda-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="91eda-169">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="91eda-169">Posting Layer</span></span>                           | <span data-ttu-id="91eda-170">Kohandatud kiht 1</span><span class="sxs-lookup"><span data-stu-id="91eda-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="91eda-171">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-171">Lease Type</span></span>                              | <span data-ttu-id="91eda-172">Automaatne</span><span class="sxs-lookup"><span data-stu-id="91eda-172">Automatic</span></span>                      |
| <span data-ttu-id="91eda-173">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="91eda-173">Accounting Framework</span></span>                    | <span data-ttu-id="91eda-174">Kassapõhine</span><span class="sxs-lookup"><span data-stu-id="91eda-174">Cash basis</span></span>                     |
| <span data-ttu-id="91eda-175">Rendiperioodi / kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="91eda-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="91eda-176">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-176">0.00</span></span>                           |
| <span data-ttu-id="91eda-177">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="91eda-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="91eda-178">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-178">0.00</span></span>                           |
| <span data-ttu-id="91eda-179">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="91eda-179">Short-term threshold</span></span>                    | <span data-ttu-id="91eda-180">0</span><span class="sxs-lookup"><span data-stu-id="91eda-180">0</span></span>                              |
| <span data-ttu-id="91eda-181">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="91eda-181">Low Value Threshold</span></span>                     | <span data-ttu-id="91eda-182">0</span><span class="sxs-lookup"><span data-stu-id="91eda-182">0</span></span>                              |
| <span data-ttu-id="91eda-183">Hankijale tasumine</span><span class="sxs-lookup"><span data-stu-id="91eda-183">Pay to Vendor</span></span>                           | <span data-ttu-id="91eda-184">Ei</span><span class="sxs-lookup"><span data-stu-id="91eda-184">No</span></span>                             |

<span data-ttu-id="91eda-185">Selle näite puhul on loodud rendikirje, millel on vahekaartidel **Üldine** ja **Maksegraafiku read** järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="91eda-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="91eda-186">**Vahekaart Üldine**</span><span class="sxs-lookup"><span data-stu-id="91eda-186">**General tab**</span></span>

| <span data-ttu-id="91eda-187">Field</span><span class="sxs-lookup"><span data-stu-id="91eda-187">Field</span></span>                      | <span data-ttu-id="91eda-188">Väärtus</span><span class="sxs-lookup"><span data-stu-id="91eda-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="91eda-189">Alternatiivne laenuintressimäär</span><span class="sxs-lookup"><span data-stu-id="91eda-189">Incremental borrowing rate</span></span> | <span data-ttu-id="91eda-190">5%</span><span class="sxs-lookup"><span data-stu-id="91eda-190">5%</span></span>               |
| <span data-ttu-id="91eda-191">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="91eda-191">Commencement date</span></span>          | <span data-ttu-id="91eda-192">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="91eda-192">1/1/2020</span></span>         |
| <span data-ttu-id="91eda-193">Rendigrupp</span><span class="sxs-lookup"><span data-stu-id="91eda-193">Lease group</span></span>                | <span data-ttu-id="91eda-194">Hooned</span><span class="sxs-lookup"><span data-stu-id="91eda-194">Buildings</span></span>        |
| <span data-ttu-id="91eda-195">Tarnija</span><span class="sxs-lookup"><span data-stu-id="91eda-195">Vendor</span></span>                     | <span data-ttu-id="91eda-196">1001</span><span class="sxs-lookup"><span data-stu-id="91eda-196">1001</span></span>             |
| <span data-ttu-id="91eda-197">Vara õiglane väärtus</span><span class="sxs-lookup"><span data-stu-id="91eda-197">Fair value of the asset</span></span>    | <span data-ttu-id="91eda-198">245,000</span><span class="sxs-lookup"><span data-stu-id="91eda-198">245,000</span></span>          |
| <span data-ttu-id="91eda-199">Vara kasulik tööiga</span><span class="sxs-lookup"><span data-stu-id="91eda-199">Asset useful life</span></span>          | <span data-ttu-id="91eda-200">120</span><span class="sxs-lookup"><span data-stu-id="91eda-200">120</span></span>              |
| <span data-ttu-id="91eda-201">Annuiteedi tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-201">Annuity type</span></span>               | <span data-ttu-id="91eda-202">Harilik annuiteet</span><span class="sxs-lookup"><span data-stu-id="91eda-202">Ordinary annuity</span></span> |
| <span data-ttu-id="91eda-203">Liitmisintervall</span><span class="sxs-lookup"><span data-stu-id="91eda-203">Compounding interval</span></span>       | <span data-ttu-id="91eda-204">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="91eda-204">Monthly</span></span>          |

<span data-ttu-id="91eda-205">**Maksegraafiku ridade vahekaart**</span><span class="sxs-lookup"><span data-stu-id="91eda-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="91eda-206">Field</span><span class="sxs-lookup"><span data-stu-id="91eda-206">Field</span></span>             | <span data-ttu-id="91eda-207">Väärtus</span><span class="sxs-lookup"><span data-stu-id="91eda-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="91eda-208">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="91eda-208">Start date</span></span>        | <span data-ttu-id="91eda-209">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="91eda-209">1/1/2020</span></span>   |
| <span data-ttu-id="91eda-210">Perioodi intervall</span><span class="sxs-lookup"><span data-stu-id="91eda-210">Period interval</span></span>   | <span data-ttu-id="91eda-211">Kuud</span><span class="sxs-lookup"><span data-stu-id="91eda-211">Months</span></span>     |
| <span data-ttu-id="91eda-212">Perioodid</span><span class="sxs-lookup"><span data-stu-id="91eda-212">Periods</span></span>           | <span data-ttu-id="91eda-213">24</span><span class="sxs-lookup"><span data-stu-id="91eda-213">24</span></span>         |
| <span data-ttu-id="91eda-214">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="91eda-214">End date</span></span>          | <span data-ttu-id="91eda-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="91eda-215">12/31/2020</span></span> |
| <span data-ttu-id="91eda-216">Makse sagedus</span><span class="sxs-lookup"><span data-stu-id="91eda-216">Payment frequency</span></span> | <span data-ttu-id="91eda-217">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="91eda-217">Monthly</span></span>    |
| <span data-ttu-id="91eda-218">Maksesumma</span><span class="sxs-lookup"><span data-stu-id="91eda-218">Payment amount</span></span>    | <span data-ttu-id="91eda-219">1000</span><span class="sxs-lookup"><span data-stu-id="91eda-219">1,000</span></span>      |

<span data-ttu-id="91eda-220">Selle rendikirje kahe raamistiku põhjal arvestamiseks kasutate praegust sisestamiskihti ja kohandatud sisestamiskihti.</span><span class="sxs-lookup"><span data-stu-id="91eda-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="91eda-221">Järgmises tabelis on toodud iga töölehe kirje näide, mis on nõutavad rahandusasjade õiglaseks kajastamiseks iga aruandlusstandardi põhjal.</span><span class="sxs-lookup"><span data-stu-id="91eda-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="91eda-222">Hiljem lisatakse rendiperioodi esimese kuu jaoks iga töölehe kirje üksikasjalik kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="91eda-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="91eda-223">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="91eda-224">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="91eda-225">Kohustuslik raamat (praegune kiht)</span><span class="sxs-lookup"><span data-stu-id="91eda-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="91eda-226">Praeguse kihi kogusumma</span><span class="sxs-lookup"><span data-stu-id="91eda-226">Current layer total</span></span></th>
<th><span data-ttu-id="91eda-227">Tühistamise raamat (kohandatud kiht)</span><span class="sxs-lookup"><span data-stu-id="91eda-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="91eda-228">IFRS 16 raamat (kohandatud kiht)</span><span class="sxs-lookup"><span data-stu-id="91eda-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="91eda-229">Praeguse kihi + kohandatud kiht kokku</span><span class="sxs-lookup"><span data-stu-id="91eda-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91eda-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="91eda-230">JE-100</span></span></th>
<th><span data-ttu-id="91eda-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="91eda-231">JE-110</span></span></th>
<th><span data-ttu-id="91eda-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="91eda-232">JE-120</span></span></th>
<th><span data-ttu-id="91eda-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="91eda-233">JE-130</span></span></th>
<th><span data-ttu-id="91eda-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="91eda-234">JE-140</span></span></th>
<th><span data-ttu-id="91eda-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="91eda-235">JE-150</span></span></th>
<th><span data-ttu-id="91eda-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="91eda-236">JE-160</span></span></th>
<th><span data-ttu-id="91eda-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="91eda-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91eda-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="91eda-246">1</span><span class="sxs-lookup"><span data-stu-id="91eda-246">1</span></span></td>
<td><span data-ttu-id="91eda-247">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-247">Lease expense</span></span></td>
<td><span data-ttu-id="91eda-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-249">1,000.00</span></span></td>
<td><span data-ttu-id="91eda-250">–1000,00</span><span class="sxs-lookup"><span data-stu-id="91eda-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-251">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-252">2</span><span class="sxs-lookup"><span data-stu-id="91eda-252">2</span></span></td>
<td><span data-ttu-id="91eda-253">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="91eda-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-254">3.00</span><span class="sxs-lookup"><span data-stu-id="91eda-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-255">3.00</span><span class="sxs-lookup"><span data-stu-id="91eda-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-256">3.00</span><span class="sxs-lookup"><span data-stu-id="91eda-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-257">3</span><span class="sxs-lookup"><span data-stu-id="91eda-257">3</span></span></td>
<td><span data-ttu-id="91eda-258">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-259">5.00</span><span class="sxs-lookup"><span data-stu-id="91eda-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-260">5.00</span><span class="sxs-lookup"><span data-stu-id="91eda-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-261">5.00</span><span class="sxs-lookup"><span data-stu-id="91eda-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-262">4</span><span class="sxs-lookup"><span data-stu-id="91eda-262">4</span></span></td>
<td><span data-ttu-id="91eda-263">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-263">Clearing account</span></span></td>
<td><span data-ttu-id="91eda-264">–1000,00</span><span class="sxs-lookup"><span data-stu-id="91eda-264">-1,000.00</span></span></td>
<td><span data-ttu-id="91eda-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-266">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-266">0.00</span></span></td>
<td><span data-ttu-id="91eda-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-268">–1000,00</span><span class="sxs-lookup"><span data-stu-id="91eda-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-269">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-270">5</span><span class="sxs-lookup"><span data-stu-id="91eda-270">5</span></span></td>
<td><span data-ttu-id="91eda-271">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="91eda-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-272">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-272">-1,008.00</span></span></td>
<td><span data-ttu-id="91eda-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91eda-273">1,008.00</span></span></td>
<td><span data-ttu-id="91eda-274">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-275">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-276">6</span><span class="sxs-lookup"><span data-stu-id="91eda-276">6</span></span></td>
<td><span data-ttu-id="91eda-277">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="91eda-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-278">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="91eda-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="91eda-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-281">7</span><span class="sxs-lookup"><span data-stu-id="91eda-281">7</span></span></td>
<td><span data-ttu-id="91eda-282">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="91eda-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-283">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-284">–22 794,00</span><span class="sxs-lookup"><span data-stu-id="91eda-284">-22,794.00</span></span></td>
<td><span data-ttu-id="91eda-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-285">1,000.00</span></span></td>
<td><span data-ttu-id="91eda-286">–94,97</span><span class="sxs-lookup"><span data-stu-id="91eda-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-287">–21 888,87</span><span class="sxs-lookup"><span data-stu-id="91eda-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-288">8</span><span class="sxs-lookup"><span data-stu-id="91eda-288">8</span></span></td>
<td><span data-ttu-id="91eda-289">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-290">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-291">94.97</span><span class="sxs-lookup"><span data-stu-id="91eda-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-292">94.97</span><span class="sxs-lookup"><span data-stu-id="91eda-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-293">9</span><span class="sxs-lookup"><span data-stu-id="91eda-293">9</span></span></td>
<td><span data-ttu-id="91eda-294">Sularaha</span><span class="sxs-lookup"><span data-stu-id="91eda-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-295">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-295">-1,008.00</span></span></td>
<td><span data-ttu-id="91eda-296">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-297">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-298">10</span><span class="sxs-lookup"><span data-stu-id="91eda-298">10</span></span></td>
<td><span data-ttu-id="91eda-299">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-300">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-301">949.75</span><span class="sxs-lookup"><span data-stu-id="91eda-301">949.75</span></span></td>
<td><span data-ttu-id="91eda-302">949.75</span><span class="sxs-lookup"><span data-stu-id="91eda-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-303">11</span><span class="sxs-lookup"><span data-stu-id="91eda-303">11</span></span></td>
<td><span data-ttu-id="91eda-304">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="91eda-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-305">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-306">–949,75</span><span class="sxs-lookup"><span data-stu-id="91eda-306">-949.75</span></span></td>
<td><span data-ttu-id="91eda-307">–949,75</span><span class="sxs-lookup"><span data-stu-id="91eda-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="91eda-308">Nagu eelnev tabel näitab, tuleb nii kohustusliku aruandluse kui ka IFRS-i aruandluse põhjal esitada kolm raamatut.</span><span class="sxs-lookup"><span data-stu-id="91eda-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="91eda-309">Kohustuslik raamat kirjendab rendimaksed vastavalt sularahapõhise raamatupidamise praeguse kihi reeglitele.</span><span class="sxs-lookup"><span data-stu-id="91eda-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="91eda-310">Kohustuslik tagasivõtmise raamat pöörab kohustuslikud töölehe kanded ümber.</span><span class="sxs-lookup"><span data-stu-id="91eda-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="91eda-311">IFRS 16 raamat loob töölehe kirjed, mida nõutakse IFRS 16 alusel.</span><span class="sxs-lookup"><span data-stu-id="91eda-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="91eda-312">Peate sisestama rendi ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="91eda-312">You must enter a lease only one time.</span></span> <span data-ttu-id="91eda-313">Seejärel saate avada lehe **Raamatud**, et näha kõiki üürilepinguga seotud raamatuid.</span><span class="sxs-lookup"><span data-stu-id="91eda-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="91eda-314">Kui loote raamatud, peavad kõik kolm olema seotud sama rendikirjega.</span><span class="sxs-lookup"><span data-stu-id="91eda-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="91eda-315">Esimese töölehe kirje talletab kohustuslikku raamatusse rendikogemuse.</span><span class="sxs-lookup"><span data-stu-id="91eda-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="91eda-316">Makseid saate luua kas partiina või valides kohustuslikus raamatus maksegraafiku.</span><span class="sxs-lookup"><span data-stu-id="91eda-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="91eda-317">Käesolevas näites luuakse kohustusliku raamatu jaoks maksegraafikust järgmine töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="91eda-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="91eda-318">Rendimakse – 31.1.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="91eda-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="91eda-319">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-319">Account type</span></span> | <span data-ttu-id="91eda-320">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-320">Account number</span></span> | <span data-ttu-id="91eda-321">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-321">Layer</span></span>   | <span data-ttu-id="91eda-322">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-322">Account description</span></span> | <span data-ttu-id="91eda-323">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-323">Debit</span></span>    | <span data-ttu-id="91eda-324">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="91eda-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-325">Ledger</span></span>       | <span data-ttu-id="91eda-326">1</span><span class="sxs-lookup"><span data-stu-id="91eda-326">1</span></span>              | <span data-ttu-id="91eda-327">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-327">Current</span></span> | <span data-ttu-id="91eda-328">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-328">Lease expense</span></span>       | <span data-ttu-id="91eda-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-329">1,000.00</span></span> |          |
| <span data-ttu-id="91eda-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-330">Ledger</span></span>       | <span data-ttu-id="91eda-331">4</span><span class="sxs-lookup"><span data-stu-id="91eda-331">4</span></span>              | <span data-ttu-id="91eda-332">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-332">Current</span></span> | <span data-ttu-id="91eda-333">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-333">Clearing account</span></span>    |          | <span data-ttu-id="91eda-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-334">1,000.00</span></span> |

<span data-ttu-id="91eda-335">Ostureskontro ametnik kasutab standardset Dynamics 365 funktsiooni, et luua arve rendi eest maksmiseks väljaspool vara rentimist.</span><span class="sxs-lookup"><span data-stu-id="91eda-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="91eda-336">Kuid selle asemel, et valida deebeti kontona **Rendikulu**, valib ostureskontro ametnik konto, et luua järgmine kirje.</span><span class="sxs-lookup"><span data-stu-id="91eda-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="91eda-337">AP protsess – 31.1./2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="91eda-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="91eda-338">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-338">Account type</span></span> | <span data-ttu-id="91eda-339">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-339">Account number</span></span> | <span data-ttu-id="91eda-340">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-340">Layer</span></span>   | <span data-ttu-id="91eda-341">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-341">Account description</span></span> | <span data-ttu-id="91eda-342">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-342">Debit</span></span>    | <span data-ttu-id="91eda-343">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="91eda-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-344">Ledger</span></span>       | <span data-ttu-id="91eda-345">4</span><span class="sxs-lookup"><span data-stu-id="91eda-345">4</span></span>              | <span data-ttu-id="91eda-346">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-346">Current</span></span> | <span data-ttu-id="91eda-347">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-347">Clearing account</span></span>    | <span data-ttu-id="91eda-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-348">1,000.00</span></span> |          |
| <span data-ttu-id="91eda-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-349">Ledger</span></span>       | <span data-ttu-id="91eda-350">2</span><span class="sxs-lookup"><span data-stu-id="91eda-350">2</span></span>              | <span data-ttu-id="91eda-351">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-351">Current</span></span> | <span data-ttu-id="91eda-352">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="91eda-352">Bank fee</span></span>            | <span data-ttu-id="91eda-353">3.00</span><span class="sxs-lookup"><span data-stu-id="91eda-353">3.00</span></span>     |          |
| <span data-ttu-id="91eda-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-354">Ledger</span></span>       | <span data-ttu-id="91eda-355">3</span><span class="sxs-lookup"><span data-stu-id="91eda-355">3</span></span>              | <span data-ttu-id="91eda-356">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-356">Current</span></span> | <span data-ttu-id="91eda-357">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-357">VAT expense</span></span>         | <span data-ttu-id="91eda-358">5.00</span><span class="sxs-lookup"><span data-stu-id="91eda-358">5.00</span></span>     |          |
| <span data-ttu-id="91eda-359">Tarnija</span><span class="sxs-lookup"><span data-stu-id="91eda-359">Vendor</span></span>       | <span data-ttu-id="91eda-360">5</span><span class="sxs-lookup"><span data-stu-id="91eda-360">5</span></span>              | <span data-ttu-id="91eda-361">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-361">Current</span></span> | <span data-ttu-id="91eda-362">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="91eda-362">Accounts payable</span></span>    |          | <span data-ttu-id="91eda-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91eda-363">1,008.00</span></span> |

<span data-ttu-id="91eda-364">Kui hankijale edastatakse arve, järgite tavalist maksetoimingut.</span><span class="sxs-lookup"><span data-stu-id="91eda-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="91eda-365">Selle toimingu käigus luuakse järgmine töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="91eda-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="91eda-366">Sularahamakse – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="91eda-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="91eda-367">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-367">Account type</span></span> | <span data-ttu-id="91eda-368">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-368">Account number</span></span> | <span data-ttu-id="91eda-369">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-369">Layer</span></span>   | <span data-ttu-id="91eda-370">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-370">Account description</span></span> | <span data-ttu-id="91eda-371">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-371">Debit</span></span>    | <span data-ttu-id="91eda-372">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="91eda-373">Tarnija</span><span class="sxs-lookup"><span data-stu-id="91eda-373">Vendor</span></span>       | <span data-ttu-id="91eda-374">5</span><span class="sxs-lookup"><span data-stu-id="91eda-374">5</span></span>              | <span data-ttu-id="91eda-375">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-375">Current</span></span> | <span data-ttu-id="91eda-376">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="91eda-376">Accounts Payable</span></span>    | <span data-ttu-id="91eda-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91eda-377">1,008.00</span></span> |          |
| <span data-ttu-id="91eda-378">Pank</span><span class="sxs-lookup"><span data-stu-id="91eda-378">Bank</span></span>         | <span data-ttu-id="91eda-379">9</span><span class="sxs-lookup"><span data-stu-id="91eda-379">9</span></span>              | <span data-ttu-id="91eda-380">Praegune</span><span class="sxs-lookup"><span data-stu-id="91eda-380">Current</span></span> | <span data-ttu-id="91eda-381">Sularaha</span><span class="sxs-lookup"><span data-stu-id="91eda-381">Cash</span></span>                |          | <span data-ttu-id="91eda-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91eda-382">1,008.00</span></span> |

<span data-ttu-id="91eda-383">Selleks hetkeks on teil antud rendikirje kohustusliku aruandlusnõude alusel kõik raamatupidamistoimingud tehtud ja saate luua praegust kihti kasutades proovibilansi.</span><span class="sxs-lookup"><span data-stu-id="91eda-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="91eda-384">Süsteem tagastab proovibilansi, millel on järgmised arvud.</span><span class="sxs-lookup"><span data-stu-id="91eda-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="91eda-385">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="91eda-386">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="91eda-387">Kohustuslik raamat (praegune kiht)</span><span class="sxs-lookup"><span data-stu-id="91eda-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="91eda-388">Praeguse kihi kogusumma</span><span class="sxs-lookup"><span data-stu-id="91eda-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91eda-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="91eda-389">JE-100</span></span></th>
<th><span data-ttu-id="91eda-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="91eda-390">JE-110</span></span></th>
<th><span data-ttu-id="91eda-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="91eda-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91eda-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91eda-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91eda-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="91eda-395">1</span><span class="sxs-lookup"><span data-stu-id="91eda-395">1</span></span></td>
<td><span data-ttu-id="91eda-396">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-396">Lease expense</span></span></td>
<td><span data-ttu-id="91eda-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-399">2</span><span class="sxs-lookup"><span data-stu-id="91eda-399">2</span></span></td>
<td><span data-ttu-id="91eda-400">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="91eda-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-401">3.00</span><span class="sxs-lookup"><span data-stu-id="91eda-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-402">3.00</span><span class="sxs-lookup"><span data-stu-id="91eda-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-403">3</span><span class="sxs-lookup"><span data-stu-id="91eda-403">3</span></span></td>
<td><span data-ttu-id="91eda-404">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-405">5.00</span><span class="sxs-lookup"><span data-stu-id="91eda-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-406">5.00</span><span class="sxs-lookup"><span data-stu-id="91eda-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-407">4</span><span class="sxs-lookup"><span data-stu-id="91eda-407">4</span></span></td>
<td><span data-ttu-id="91eda-408">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-408">Clearing account</span></span></td>
<td><span data-ttu-id="91eda-409">–1000,00</span><span class="sxs-lookup"><span data-stu-id="91eda-409">-1,000.00</span></span></td>
<td><span data-ttu-id="91eda-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-411">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-412">5</span><span class="sxs-lookup"><span data-stu-id="91eda-412">5</span></span></td>
<td><span data-ttu-id="91eda-413">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="91eda-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="91eda-414">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-414">-1,008.00</span></span></td>
<td><span data-ttu-id="91eda-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91eda-415">1,008.00</span></span></td>
<td><span data-ttu-id="91eda-416">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-417">6</span><span class="sxs-lookup"><span data-stu-id="91eda-417">6</span></span></td>
<td><span data-ttu-id="91eda-418">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="91eda-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-419">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-420">7</span><span class="sxs-lookup"><span data-stu-id="91eda-420">7</span></span></td>
<td><span data-ttu-id="91eda-421">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="91eda-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-422">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-423">8</span><span class="sxs-lookup"><span data-stu-id="91eda-423">8</span></span></td>
<td><span data-ttu-id="91eda-424">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-425">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-426">9</span><span class="sxs-lookup"><span data-stu-id="91eda-426">9</span></span></td>
<td><span data-ttu-id="91eda-427">Sularaha</span><span class="sxs-lookup"><span data-stu-id="91eda-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-428">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-428">-1,008.00</span></span></td>
<td><span data-ttu-id="91eda-429">–1008,00</span><span class="sxs-lookup"><span data-stu-id="91eda-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-430">10</span><span class="sxs-lookup"><span data-stu-id="91eda-430">10</span></span></td>
<td><span data-ttu-id="91eda-431">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-432">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91eda-433">11</span><span class="sxs-lookup"><span data-stu-id="91eda-433">11</span></span></td>
<td><span data-ttu-id="91eda-434">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="91eda-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91eda-435">0,00</span><span class="sxs-lookup"><span data-stu-id="91eda-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="91eda-436">Kui soovite kasutada sama proovibilansi käitamiseks kasutada IFRS 16 andmeid, tuleb kohustusliku raamatupidamise töölehe kanded tagasi võtta ja IFRS 16 töölehe kanded tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="91eda-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="91eda-437">Kohustusliku töölehe kirjete tühistamiseks sisaldab see näide seadusjärgset tagasivõtmise raamatut, millel on sama seadistus kui kohustuslik raamat, kuid vastupidine sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="91eda-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="91eda-438">Näiteks, kohustuslik raamat *debiteerib* rendikulu kontot, kuid tagasivõtmise konto *krediteerib* seda kontot.</span><span class="sxs-lookup"><span data-stu-id="91eda-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="91eda-439">Need seosed on lihtne määratleda vara rentimise sisestamise kontol lehel **Vara rentimise parameetrid**(**Vara rentimine \> Seadistus \> Vara rentimise parameetrid**).</span><span class="sxs-lookup"><span data-stu-id="91eda-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="91eda-440">Kui tagasivõtmise raamatu puhul kasutataks kohustusliku raamatuga sama protsessi, loodaks järgmine töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="91eda-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="91eda-441">Erinevus seisneb selles, et tagasivõtmise raamat kirjendab kohustusliku raamatu tagastamise kirjed.</span><span class="sxs-lookup"><span data-stu-id="91eda-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="91eda-442">Tagasivõtmise kirjed tehakse ka kliendi kihis.</span><span class="sxs-lookup"><span data-stu-id="91eda-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="91eda-443">Kui proovibilanssi käitatakse praeguses kihis, siis tagasivõtmise töölehe kirjeid ei kaasataks.</span><span class="sxs-lookup"><span data-stu-id="91eda-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="91eda-444">Rendimakse – 31.1.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="91eda-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="91eda-445">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-445">Account type</span></span> | <span data-ttu-id="91eda-446">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-446">Account number</span></span> | <span data-ttu-id="91eda-447">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-447">Layer</span></span>  | <span data-ttu-id="91eda-448">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-448">Account description</span></span> | <span data-ttu-id="91eda-449">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-449">Debit</span></span>    | <span data-ttu-id="91eda-450">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="91eda-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-451">Ledger</span></span>       | <span data-ttu-id="91eda-452">4</span><span class="sxs-lookup"><span data-stu-id="91eda-452">4</span></span>              | <span data-ttu-id="91eda-453">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-453">Custom</span></span> | <span data-ttu-id="91eda-454">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-454">Clearing account</span></span>    | <span data-ttu-id="91eda-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-455">1,000.00</span></span> |          |
| <span data-ttu-id="91eda-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-456">Ledger</span></span>       | <span data-ttu-id="91eda-457">1</span><span class="sxs-lookup"><span data-stu-id="91eda-457">1</span></span>              | <span data-ttu-id="91eda-458">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-458">Custom</span></span> | <span data-ttu-id="91eda-459">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-459">Lease expense</span></span>       |          | <span data-ttu-id="91eda-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-460">1,000.00</span></span> |

<span data-ttu-id="91eda-461">Nüüd kui olete kohustusliku töölehe sisestused eemaldanud, kirjendate kõik töölehe kirjed, mida IFRS 16 nõuab, IFRS 16 raamatus.</span><span class="sxs-lookup"><span data-stu-id="91eda-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="91eda-462">Need kanded hõlmavad kasutamisõiguse esemeks oleva vara esialgset tunnustamist ning intressikirjet ja kulumi arvestust.</span><span class="sxs-lookup"><span data-stu-id="91eda-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="91eda-463">Esialgne tunnustamine – 1.1.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="91eda-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="91eda-464">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-464">Account type</span></span> | <span data-ttu-id="91eda-465">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-465">Account number</span></span> | <span data-ttu-id="91eda-466">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-466">Layer</span></span>  | <span data-ttu-id="91eda-467">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-467">Account description</span></span>      | <span data-ttu-id="91eda-468">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-468">Debit</span></span>     | <span data-ttu-id="91eda-469">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="91eda-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-470">Ledger</span></span>       | <span data-ttu-id="91eda-471">6</span><span class="sxs-lookup"><span data-stu-id="91eda-471">6</span></span>              | <span data-ttu-id="91eda-472">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-472">Custom</span></span> | <span data-ttu-id="91eda-473">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="91eda-473">ROU Asset</span></span>                | <span data-ttu-id="91eda-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="91eda-474">22,793.90</span></span> |           |
| <span data-ttu-id="91eda-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-475">Ledger</span></span>       | <span data-ttu-id="91eda-476">7</span><span class="sxs-lookup"><span data-stu-id="91eda-476">7</span></span>              | <span data-ttu-id="91eda-477">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-477">Custom</span></span> | <span data-ttu-id="91eda-478">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="91eda-478">Finance lease obligation</span></span> |           | <span data-ttu-id="91eda-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="91eda-479">22,793.90</span></span> |

<span data-ttu-id="91eda-480">Rendimakse sisestatakse sarnaselt teistele rendimaksetele.</span><span class="sxs-lookup"><span data-stu-id="91eda-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="91eda-481">Tühjendamise konto kasutamise põhjus on tagada, et sularaha krediteeritakse ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="91eda-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="91eda-482">Rendimakse – 31.1.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="91eda-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="91eda-483">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-483">Account type</span></span> | <span data-ttu-id="91eda-484">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-484">Account number</span></span> | <span data-ttu-id="91eda-485">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-485">Layer</span></span>  | <span data-ttu-id="91eda-486">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-486">Account description</span></span>      | <span data-ttu-id="91eda-487">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-487">Debit</span></span>    | <span data-ttu-id="91eda-488">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="91eda-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-489">Ledger</span></span>       | <span data-ttu-id="91eda-490">7</span><span class="sxs-lookup"><span data-stu-id="91eda-490">7</span></span>              | <span data-ttu-id="91eda-491">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-491">Custom</span></span> | <span data-ttu-id="91eda-492">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="91eda-492">Finance lease obligation</span></span> | <span data-ttu-id="91eda-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-493">1,000.00</span></span> |          |
| <span data-ttu-id="91eda-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-494">Ledger</span></span>       | <span data-ttu-id="91eda-495">4</span><span class="sxs-lookup"><span data-stu-id="91eda-495">4</span></span>              | <span data-ttu-id="91eda-496">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-496">Custom</span></span> | <span data-ttu-id="91eda-497">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-497">Clearing account</span></span>         |          | <span data-ttu-id="91eda-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91eda-498">1,000.00</span></span> |

<span data-ttu-id="91eda-499">Intressikulu töölehe kirje luuakse kohustise amortiseerimise graafikust.</span><span class="sxs-lookup"><span data-stu-id="91eda-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="91eda-500">Intressikulu – 31.1.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="91eda-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="91eda-501">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-501">Account type</span></span> | <span data-ttu-id="91eda-502">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-502">Account number</span></span> | <span data-ttu-id="91eda-503">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-503">Layer</span></span>  | <span data-ttu-id="91eda-504">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-504">Account description</span></span>      | <span data-ttu-id="91eda-505">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-505">Debit</span></span> | <span data-ttu-id="91eda-506">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="91eda-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-507">Ledger</span></span>       | <span data-ttu-id="91eda-508">8</span><span class="sxs-lookup"><span data-stu-id="91eda-508">8</span></span>              | <span data-ttu-id="91eda-509">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-509">Custom</span></span> | <span data-ttu-id="91eda-510">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-510">Interest expense</span></span>         | <span data-ttu-id="91eda-511">94.97</span><span class="sxs-lookup"><span data-stu-id="91eda-511">94.97</span></span> |        |
| <span data-ttu-id="91eda-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-512">Ledger</span></span>       | <span data-ttu-id="91eda-513">7</span><span class="sxs-lookup"><span data-stu-id="91eda-513">7</span></span>              | <span data-ttu-id="91eda-514">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-514">Custom</span></span> | <span data-ttu-id="91eda-515">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="91eda-515">Finance lease obligation</span></span> |       | <span data-ttu-id="91eda-516">94.97</span><span class="sxs-lookup"><span data-stu-id="91eda-516">94.97</span></span>  |

<span data-ttu-id="91eda-517">Kulumi kulu töölehe kirje luuakse vara kulumi graafikust.</span><span class="sxs-lookup"><span data-stu-id="91eda-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="91eda-518">Kulumi kulu – 31.1.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="91eda-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="91eda-519">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="91eda-519">Account type</span></span> | <span data-ttu-id="91eda-520">Konto number</span><span class="sxs-lookup"><span data-stu-id="91eda-520">Account number</span></span> | <span data-ttu-id="91eda-521">Kiht</span><span class="sxs-lookup"><span data-stu-id="91eda-521">Layer</span></span>  | <span data-ttu-id="91eda-522">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-522">Account description</span></span>      | <span data-ttu-id="91eda-523">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="91eda-523">Debit</span></span>  | <span data-ttu-id="91eda-524">Krediit</span><span class="sxs-lookup"><span data-stu-id="91eda-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="91eda-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-525">Ledger</span></span>       | <span data-ttu-id="91eda-526">10</span><span class="sxs-lookup"><span data-stu-id="91eda-526">10</span></span>             | <span data-ttu-id="91eda-527">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-527">Custom</span></span> | <span data-ttu-id="91eda-528">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-528">Depreciation expense</span></span>     | <span data-ttu-id="91eda-529">949.75</span><span class="sxs-lookup"><span data-stu-id="91eda-529">949.75</span></span> |        |
| <span data-ttu-id="91eda-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="91eda-530">Ledger</span></span>       | <span data-ttu-id="91eda-531">11</span><span class="sxs-lookup"><span data-stu-id="91eda-531">11</span></span>             | <span data-ttu-id="91eda-532">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="91eda-532">Custom</span></span> | <span data-ttu-id="91eda-533">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="91eda-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="91eda-534">949.75</span><span class="sxs-lookup"><span data-stu-id="91eda-534">949.75</span></span> |

<span data-ttu-id="91eda-535">Pärast kõikide nende töölehe kirjete loomist ja sisestamist näete järgmist „kohandatud kiht 1” väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="91eda-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="91eda-536">Pange tähele, et viimane veerg sisaldab pangatasu, käibemaksu (KM) kulu ja eelmise kihi sularaha vähendamist, kuid see ei sisalda kohustusliku aruandluse töölehe kandeid.</span><span class="sxs-lookup"><span data-stu-id="91eda-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="91eda-537">Seega saavutate tõelise topeltaruandluse võimalused.</span><span class="sxs-lookup"><span data-stu-id="91eda-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="91eda-538">Sel hetkel peab ettevõte lihtsalt käivitama oma proovibilansi ja kombineerima praeguse kihi ja kohandatud kihi, et luua IFRS-i prooviversioon.</span><span class="sxs-lookup"><span data-stu-id="91eda-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="91eda-539">Konto nr</span><span class="sxs-lookup"><span data-stu-id="91eda-539">Account No</span></span> | <span data-ttu-id="91eda-540">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="91eda-540">Description</span></span>              | <span data-ttu-id="91eda-541">Kohustuslik raamat\-Praegune tase\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-542">Kohustuslik raamat\-Praegune tase\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-543">Kohustuslik raamat\-Praegune tase\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-544">Praegune kiht \- kogusummad</span><span class="sxs-lookup"><span data-stu-id="91eda-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="91eda-545">Tühistamise raamat\-Kohandatud kiht\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-546">IFRS 16 raamat\-kohandatud kiht \-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-547">IFRS 16 raamat\-kohandatud kiht \-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-548">IFRS 16 raamat\-kohandatud kiht \-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-549">IFRS 16 raamat\-kohandatud kiht \-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91eda-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="91eda-550">Kohandatud kiht \+ Praegune kiht \- Tööriistad</span><span class="sxs-lookup"><span data-stu-id="91eda-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="91eda-551">1</span><span class="sxs-lookup"><span data-stu-id="91eda-551">1</span></span>          | <span data-ttu-id="91eda-552">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-552">Lease expense</span></span>            | <span data-ttu-id="91eda-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="91eda-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-554">1,000\.00</span></span>               |   | <span data-ttu-id="91eda-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="91eda-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="91eda-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-556">0\.00</span></span>                                   |
| <span data-ttu-id="91eda-557">2</span><span class="sxs-lookup"><span data-stu-id="91eda-557">2</span></span>          | <span data-ttu-id="91eda-558">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="91eda-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="91eda-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="91eda-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91eda-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-561">3\.00</span></span>                                   |
| <span data-ttu-id="91eda-562">3</span><span class="sxs-lookup"><span data-stu-id="91eda-562">3</span></span>          | <span data-ttu-id="91eda-563">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="91eda-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="91eda-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91eda-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-566">5\.00</span></span>                                   |
| <span data-ttu-id="91eda-567">4</span><span class="sxs-lookup"><span data-stu-id="91eda-567">4</span></span>          | <span data-ttu-id="91eda-568">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="91eda-568">Clearing account</span></span>         | <span data-ttu-id="91eda-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="91eda-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="91eda-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-571">0\.00</span></span>                   |   | <span data-ttu-id="91eda-572">1000</span><span class="sxs-lookup"><span data-stu-id="91eda-572">1,000</span></span>                                           |                                                | <span data-ttu-id="91eda-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="91eda-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="91eda-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-574">0\.00</span></span>                                   |
| <span data-ttu-id="91eda-575">5</span><span class="sxs-lookup"><span data-stu-id="91eda-575">5</span></span>          | <span data-ttu-id="91eda-576">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="91eda-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="91eda-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="91eda-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-578">1,008\.00</span></span>                                         | <span data-ttu-id="91eda-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91eda-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-580">0\.00</span></span>                                   |
| <span data-ttu-id="91eda-581">6</span><span class="sxs-lookup"><span data-stu-id="91eda-581">6</span></span>          | <span data-ttu-id="91eda-582">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="91eda-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="91eda-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="91eda-584">22,794</span><span class="sxs-lookup"><span data-stu-id="91eda-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="91eda-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="91eda-585">22,793\.90</span></span>                              |
| <span data-ttu-id="91eda-586">7</span><span class="sxs-lookup"><span data-stu-id="91eda-586">7</span></span>          | <span data-ttu-id="91eda-587">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="91eda-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="91eda-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="91eda-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="91eda-589">\-22,794</span></span>                                       | <span data-ttu-id="91eda-590">1000</span><span class="sxs-lookup"><span data-stu-id="91eda-590">1,000</span></span>                                          | <span data-ttu-id="91eda-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="91eda-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="91eda-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="91eda-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="91eda-593">8</span><span class="sxs-lookup"><span data-stu-id="91eda-593">8</span></span>          | <span data-ttu-id="91eda-594">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="91eda-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="91eda-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="91eda-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="91eda-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="91eda-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="91eda-597">94\.97</span></span>                                  |
| <span data-ttu-id="91eda-598">9</span><span class="sxs-lookup"><span data-stu-id="91eda-598">9</span></span>          | <span data-ttu-id="91eda-599">Sularaha</span><span class="sxs-lookup"><span data-stu-id="91eda-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="91eda-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="91eda-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91eda-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="91eda-603">10</span><span class="sxs-lookup"><span data-stu-id="91eda-603">10</span></span>         | <span data-ttu-id="91eda-604">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="91eda-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="91eda-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="91eda-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="91eda-606">949\.75</span></span>                                        | <span data-ttu-id="91eda-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="91eda-607">949\.75</span></span>                                 |
| <span data-ttu-id="91eda-608">11</span><span class="sxs-lookup"><span data-stu-id="91eda-608">11</span></span>         | <span data-ttu-id="91eda-609">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="91eda-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="91eda-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="91eda-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="91eda-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="91eda-611">\-949\.75</span></span>                                      | <span data-ttu-id="91eda-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="91eda-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]