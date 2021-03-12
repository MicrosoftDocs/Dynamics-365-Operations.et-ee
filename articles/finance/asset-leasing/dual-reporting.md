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
ms.openlocfilehash: a7d9b3ea3d4f1d48b8a7326bd5a01d3119310c62
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003177"
---
# <a name="dual-reporting"></a><span data-ttu-id="3de81-103">Topeltaruandlus</span><span class="sxs-lookup"><span data-stu-id="3de81-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3de81-104">See teema juhendab teid läbi näite, mis näitab, kuidas saate täita nii rahvusvahelise finantsaruandluse standardi (IFRS) aruandlust kui ka vara rentimise kohustuslikku aruandlust.</span><span class="sxs-lookup"><span data-stu-id="3de81-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="3de81-105">Nõutav on rakenduses Microsoft Dynamics 365 Finance kihtide sisestamise kogemus ja see muudab näitest arusaamise lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="3de81-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="3de81-106">Näide</span><span class="sxs-lookup"><span data-stu-id="3de81-106">Example</span></span>

<span data-ttu-id="3de81-107">Järgmine näide kehtib rentimisele Itaalia seadusliku aruande korral, kasutades nii sularahapõhist meetodit kui ka IFRS-i aruandluse meetodeid.</span><span class="sxs-lookup"><span data-stu-id="3de81-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="3de81-108">Ettevõte peab looma kolm raamatut, et täita nii Itaalia seadusjärgsed nõuded kui ka IFRS 16 nõuded.</span><span class="sxs-lookup"><span data-stu-id="3de81-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="3de81-109">Üks raamat on vajalik IFRS 16 jaoks, üks raamat on nõutav kohustuslike nõuete jaoks ja üks raamat on nõutav seaduslike postituste automaatne tagasipööramine.</span><span class="sxs-lookup"><span data-stu-id="3de81-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="3de81-110">Raamatud häälestatakse, nagu järgmistes tabelites on näidatud.</span><span class="sxs-lookup"><span data-stu-id="3de81-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="3de81-111">**IFRS 16 raamat**</span><span class="sxs-lookup"><span data-stu-id="3de81-111">**IFRS 16 book**</span></span>

<span data-ttu-id="3de81-112">IFRS 16 raamat on häälestatud nii, et see vastab IFRS 16 raamatupidamise standardile.</span><span class="sxs-lookup"><span data-stu-id="3de81-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="3de81-113">Kõik sellesse raamatusse sisestatavad kirjed postitatakse kliendi kihis.</span><span class="sxs-lookup"><span data-stu-id="3de81-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="3de81-114">Nimi</span><span class="sxs-lookup"><span data-stu-id="3de81-114">Name</span></span>                                    | <span data-ttu-id="3de81-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="3de81-116">Žurnaali tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-116">Book type</span></span>                               | <span data-ttu-id="3de81-117">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="3de81-117">IFRS 16</span></span>        |
| <span data-ttu-id="3de81-118">Raamatu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-118">Book description</span></span>                        | <span data-ttu-id="3de81-119">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="3de81-119">IFRS 16</span></span>        |
| <span data-ttu-id="3de81-120">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="3de81-120">Posting Layer</span></span>                           | <span data-ttu-id="3de81-121">Kohandatud kiht 1</span><span class="sxs-lookup"><span data-stu-id="3de81-121">Custom layer 1</span></span> |
| <span data-ttu-id="3de81-122">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-122">Lease Type</span></span>                              | <span data-ttu-id="3de81-123">Finance</span><span class="sxs-lookup"><span data-stu-id="3de81-123">Finance</span></span>        |
| <span data-ttu-id="3de81-124">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="3de81-124">Accounting Framework</span></span>                    | <span data-ttu-id="3de81-125">IFRS 16</span><span class="sxs-lookup"><span data-stu-id="3de81-125">IFRS 16</span></span>        |
| <span data-ttu-id="3de81-126">Rendiperioodi / kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="3de81-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="3de81-127">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-127">0.00</span></span>           |
| <span data-ttu-id="3de81-128">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="3de81-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="3de81-129">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-129">0.00</span></span>           |
| <span data-ttu-id="3de81-130">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="3de81-130">Short-term threshold</span></span>                    | <span data-ttu-id="3de81-131">12</span><span class="sxs-lookup"><span data-stu-id="3de81-131">12</span></span>             |
| <span data-ttu-id="3de81-132">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="3de81-132">Low Value Threshold</span></span>                     | <span data-ttu-id="3de81-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-133">5,000.00</span></span>       |
| <span data-ttu-id="3de81-134">Hankijale tasumine</span><span class="sxs-lookup"><span data-stu-id="3de81-134">Pay to Vendor</span></span>                           | <span data-ttu-id="3de81-135">Ei</span><span class="sxs-lookup"><span data-stu-id="3de81-135">No</span></span>             |

<span data-ttu-id="3de81-136">**Kohustuslik raamat**</span><span class="sxs-lookup"><span data-stu-id="3de81-136">**Statutory book**</span></span>

<span data-ttu-id="3de81-137">Kohustuslik raamat on sularahal põhinev raamat, kus ettevõte arvestab rendikogemust kui sularaha summat, mis makstakse iga kuu rendiks.</span><span class="sxs-lookup"><span data-stu-id="3de81-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="3de81-138">See raamat ei tekita õiget kasutamisõiguse esemeks olevat vara või rendikohustist.</span><span class="sxs-lookup"><span data-stu-id="3de81-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="3de81-139">Nimi</span><span class="sxs-lookup"><span data-stu-id="3de81-139">Name</span></span>                                    | <span data-ttu-id="3de81-140">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="3de81-141">Žurnaali tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-141">Book type</span></span>                               | <span data-ttu-id="3de81-142">Seaduslik</span><span class="sxs-lookup"><span data-stu-id="3de81-142">Statutory</span></span>   |
| <span data-ttu-id="3de81-143">Raamatu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-143">Book description</span></span>                        | <span data-ttu-id="3de81-144">Kohalik GAAP</span><span class="sxs-lookup"><span data-stu-id="3de81-144">Local GAAP</span></span>  |
| <span data-ttu-id="3de81-145">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="3de81-145">Posting Layer</span></span>                           | <span data-ttu-id="3de81-146">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-146">Current</span></span>     |
| <span data-ttu-id="3de81-147">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-147">Lease Type</span></span>                              | <span data-ttu-id="3de81-148">Automaatne</span><span class="sxs-lookup"><span data-stu-id="3de81-148">Automatic</span></span>   |
| <span data-ttu-id="3de81-149">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="3de81-149">Accounting Framework</span></span>                    | <span data-ttu-id="3de81-150">Kassapõhine</span><span class="sxs-lookup"><span data-stu-id="3de81-150">Cash basis</span></span>  |
| <span data-ttu-id="3de81-151">Rendiperioodi / kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="3de81-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="3de81-152">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-152">0.00</span></span>        |
| <span data-ttu-id="3de81-153">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="3de81-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="3de81-154">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-154">0.00</span></span>        |
| <span data-ttu-id="3de81-155">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="3de81-155">Short-term threshold</span></span>                    | <span data-ttu-id="3de81-156">0</span><span class="sxs-lookup"><span data-stu-id="3de81-156">0</span></span>           |
| <span data-ttu-id="3de81-157">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="3de81-157">Low Value Threshold</span></span>                     | <span data-ttu-id="3de81-158">0</span><span class="sxs-lookup"><span data-stu-id="3de81-158">0</span></span>           |
| <span data-ttu-id="3de81-159">Hankijale tasumine</span><span class="sxs-lookup"><span data-stu-id="3de81-159">Pay to Vendor</span></span>                           | <span data-ttu-id="3de81-160">Ei</span><span class="sxs-lookup"><span data-stu-id="3de81-160">No</span></span>          |

<span data-ttu-id="3de81-161">**Kohustusliku tagasivõtmise raamat**</span><span class="sxs-lookup"><span data-stu-id="3de81-161">**Statutory reversal book**</span></span>

<span data-ttu-id="3de81-162">Kohustuslik tagasivõtmise raamat häälestatakse sarnaselt kohustuslikule raamatule.</span><span class="sxs-lookup"><span data-stu-id="3de81-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="3de81-163">Nimi</span><span class="sxs-lookup"><span data-stu-id="3de81-163">Name</span></span>                                    | <span data-ttu-id="3de81-164">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="3de81-165">Žurnaali tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-165">Book type</span></span>                               | <span data-ttu-id="3de81-166">Kohustuslik – tagasivõtmime</span><span class="sxs-lookup"><span data-stu-id="3de81-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="3de81-167">Raamatu kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-167">Book description</span></span>                        | <span data-ttu-id="3de81-168">Kohustustusliku raamatu tagasivõtmise raamat</span><span class="sxs-lookup"><span data-stu-id="3de81-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="3de81-169">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="3de81-169">Posting Layer</span></span>                           | <span data-ttu-id="3de81-170">Kohandatud kiht 1</span><span class="sxs-lookup"><span data-stu-id="3de81-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="3de81-171">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-171">Lease Type</span></span>                              | <span data-ttu-id="3de81-172">Automaatne</span><span class="sxs-lookup"><span data-stu-id="3de81-172">Automatic</span></span>                      |
| <span data-ttu-id="3de81-173">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="3de81-173">Accounting Framework</span></span>                    | <span data-ttu-id="3de81-174">Kassapõhine</span><span class="sxs-lookup"><span data-stu-id="3de81-174">Cash basis</span></span>                     |
| <span data-ttu-id="3de81-175">Rendiperioodi / kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="3de81-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="3de81-176">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-176">0.00</span></span>                           |
| <span data-ttu-id="3de81-177">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="3de81-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="3de81-178">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-178">0.00</span></span>                           |
| <span data-ttu-id="3de81-179">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="3de81-179">Short-term threshold</span></span>                    | <span data-ttu-id="3de81-180">0</span><span class="sxs-lookup"><span data-stu-id="3de81-180">0</span></span>                              |
| <span data-ttu-id="3de81-181">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="3de81-181">Low Value Threshold</span></span>                     | <span data-ttu-id="3de81-182">0</span><span class="sxs-lookup"><span data-stu-id="3de81-182">0</span></span>                              |
| <span data-ttu-id="3de81-183">Hankijale tasumine</span><span class="sxs-lookup"><span data-stu-id="3de81-183">Pay to Vendor</span></span>                           | <span data-ttu-id="3de81-184">Ei</span><span class="sxs-lookup"><span data-stu-id="3de81-184">No</span></span>                             |

<span data-ttu-id="3de81-185">Selle näite puhul on loodud rendikirje, millel on vahekaartidel **Üldine** ja **Maksegraafiku read** järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="3de81-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="3de81-186">**Vahekaart Üldine**</span><span class="sxs-lookup"><span data-stu-id="3de81-186">**General tab**</span></span>

| <span data-ttu-id="3de81-187">Field</span><span class="sxs-lookup"><span data-stu-id="3de81-187">Field</span></span>                      | <span data-ttu-id="3de81-188">Väärtus</span><span class="sxs-lookup"><span data-stu-id="3de81-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="3de81-189">Alternatiivne laenuintressimäär</span><span class="sxs-lookup"><span data-stu-id="3de81-189">Incremental borrowing rate</span></span> | <span data-ttu-id="3de81-190">5%</span><span class="sxs-lookup"><span data-stu-id="3de81-190">5%</span></span>               |
| <span data-ttu-id="3de81-191">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="3de81-191">Commencement date</span></span>          | <span data-ttu-id="3de81-192">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="3de81-192">1/1/2020</span></span>         |
| <span data-ttu-id="3de81-193">Rendigrupp</span><span class="sxs-lookup"><span data-stu-id="3de81-193">Lease group</span></span>                | <span data-ttu-id="3de81-194">Hooned</span><span class="sxs-lookup"><span data-stu-id="3de81-194">Buildings</span></span>        |
| <span data-ttu-id="3de81-195">Tarnija</span><span class="sxs-lookup"><span data-stu-id="3de81-195">Vendor</span></span>                     | <span data-ttu-id="3de81-196">1001</span><span class="sxs-lookup"><span data-stu-id="3de81-196">1001</span></span>             |
| <span data-ttu-id="3de81-197">Vara õiglane väärtus</span><span class="sxs-lookup"><span data-stu-id="3de81-197">Fair value of the asset</span></span>    | <span data-ttu-id="3de81-198">245,000</span><span class="sxs-lookup"><span data-stu-id="3de81-198">245,000</span></span>          |
| <span data-ttu-id="3de81-199">Vara kasulik tööiga</span><span class="sxs-lookup"><span data-stu-id="3de81-199">Asset useful life</span></span>          | <span data-ttu-id="3de81-200">120</span><span class="sxs-lookup"><span data-stu-id="3de81-200">120</span></span>              |
| <span data-ttu-id="3de81-201">Annuiteedi tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-201">Annuity type</span></span>               | <span data-ttu-id="3de81-202">Harilik annuiteet</span><span class="sxs-lookup"><span data-stu-id="3de81-202">Ordinary annuity</span></span> |
| <span data-ttu-id="3de81-203">Liitmisintervall</span><span class="sxs-lookup"><span data-stu-id="3de81-203">Compounding interval</span></span>       | <span data-ttu-id="3de81-204">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="3de81-204">Monthly</span></span>          |

<span data-ttu-id="3de81-205">**Maksegraafiku ridade vahekaart**</span><span class="sxs-lookup"><span data-stu-id="3de81-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="3de81-206">Field</span><span class="sxs-lookup"><span data-stu-id="3de81-206">Field</span></span>             | <span data-ttu-id="3de81-207">Väärtus</span><span class="sxs-lookup"><span data-stu-id="3de81-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="3de81-208">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="3de81-208">Start date</span></span>        | <span data-ttu-id="3de81-209">1.1.2020</span><span class="sxs-lookup"><span data-stu-id="3de81-209">1/1/2020</span></span>   |
| <span data-ttu-id="3de81-210">Perioodi intervall</span><span class="sxs-lookup"><span data-stu-id="3de81-210">Period interval</span></span>   | <span data-ttu-id="3de81-211">Kuud</span><span class="sxs-lookup"><span data-stu-id="3de81-211">Months</span></span>     |
| <span data-ttu-id="3de81-212">Perioodid</span><span class="sxs-lookup"><span data-stu-id="3de81-212">Periods</span></span>           | <span data-ttu-id="3de81-213">24</span><span class="sxs-lookup"><span data-stu-id="3de81-213">24</span></span>         |
| <span data-ttu-id="3de81-214">Lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="3de81-214">End date</span></span>          | <span data-ttu-id="3de81-215">31.12.2020</span><span class="sxs-lookup"><span data-stu-id="3de81-215">12/31/2020</span></span> |
| <span data-ttu-id="3de81-216">Makse sagedus</span><span class="sxs-lookup"><span data-stu-id="3de81-216">Payment frequency</span></span> | <span data-ttu-id="3de81-217">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="3de81-217">Monthly</span></span>    |
| <span data-ttu-id="3de81-218">Maksesumma</span><span class="sxs-lookup"><span data-stu-id="3de81-218">Payment amount</span></span>    | <span data-ttu-id="3de81-219">1000</span><span class="sxs-lookup"><span data-stu-id="3de81-219">1,000</span></span>      |

<span data-ttu-id="3de81-220">Selle rendikirje kahe raamistiku põhjal arvestamiseks kasutate praegust sisestamiskihti ja kohandatud sisestamiskihti.</span><span class="sxs-lookup"><span data-stu-id="3de81-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="3de81-221">Järgmises tabelis on toodud iga töölehe kirje näide, mis on nõutavad rahandusasjade õiglaseks kajastamiseks iga aruandlusstandardi põhjal.</span><span class="sxs-lookup"><span data-stu-id="3de81-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="3de81-222">Hiljem lisatakse rendiperioodi esimese kuu jaoks iga töölehe kirje üksikasjalik kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="3de81-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="3de81-223">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="3de81-224">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="3de81-225">Kohustuslik raamat (praegune kiht)</span><span class="sxs-lookup"><span data-stu-id="3de81-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="3de81-226">Praeguse kihi kogusumma</span><span class="sxs-lookup"><span data-stu-id="3de81-226">Current layer total</span></span></th>
<th><span data-ttu-id="3de81-227">Tühistamise raamat (kohandatud kiht)</span><span class="sxs-lookup"><span data-stu-id="3de81-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="3de81-228">IFRS 16 raamat (kohandatud kiht)</span><span class="sxs-lookup"><span data-stu-id="3de81-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="3de81-229">Praeguse kihi + kohandatud kiht kokku</span><span class="sxs-lookup"><span data-stu-id="3de81-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3de81-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="3de81-230">JE-100</span></span></th>
<th><span data-ttu-id="3de81-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="3de81-231">JE-110</span></span></th>
<th><span data-ttu-id="3de81-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="3de81-232">JE-120</span></span></th>
<th><span data-ttu-id="3de81-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="3de81-233">JE-130</span></span></th>
<th><span data-ttu-id="3de81-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="3de81-234">JE-140</span></span></th>
<th><span data-ttu-id="3de81-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="3de81-235">JE-150</span></span></th>
<th><span data-ttu-id="3de81-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="3de81-236">JE-160</span></span></th>
<th><span data-ttu-id="3de81-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="3de81-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3de81-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3de81-246">1</span><span class="sxs-lookup"><span data-stu-id="3de81-246">1</span></span></td>
<td><span data-ttu-id="3de81-247">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-247">Lease expense</span></span></td>
<td><span data-ttu-id="3de81-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-249">1,000.00</span></span></td>
<td><span data-ttu-id="3de81-250">–1000,00</span><span class="sxs-lookup"><span data-stu-id="3de81-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-251">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-252">2</span><span class="sxs-lookup"><span data-stu-id="3de81-252">2</span></span></td>
<td><span data-ttu-id="3de81-253">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="3de81-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-254">3.00</span><span class="sxs-lookup"><span data-stu-id="3de81-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-255">3.00</span><span class="sxs-lookup"><span data-stu-id="3de81-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-256">3.00</span><span class="sxs-lookup"><span data-stu-id="3de81-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-257">3</span><span class="sxs-lookup"><span data-stu-id="3de81-257">3</span></span></td>
<td><span data-ttu-id="3de81-258">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-259">5.00</span><span class="sxs-lookup"><span data-stu-id="3de81-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-260">5.00</span><span class="sxs-lookup"><span data-stu-id="3de81-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-261">5.00</span><span class="sxs-lookup"><span data-stu-id="3de81-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-262">4</span><span class="sxs-lookup"><span data-stu-id="3de81-262">4</span></span></td>
<td><span data-ttu-id="3de81-263">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-263">Clearing account</span></span></td>
<td><span data-ttu-id="3de81-264">–1000,00</span><span class="sxs-lookup"><span data-stu-id="3de81-264">-1,000.00</span></span></td>
<td><span data-ttu-id="3de81-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-266">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-266">0.00</span></span></td>
<td><span data-ttu-id="3de81-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-268">–1000,00</span><span class="sxs-lookup"><span data-stu-id="3de81-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-269">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-270">5</span><span class="sxs-lookup"><span data-stu-id="3de81-270">5</span></span></td>
<td><span data-ttu-id="3de81-271">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="3de81-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-272">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-272">-1,008.00</span></span></td>
<td><span data-ttu-id="3de81-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="3de81-273">1,008.00</span></span></td>
<td><span data-ttu-id="3de81-274">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-275">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-276">6</span><span class="sxs-lookup"><span data-stu-id="3de81-276">6</span></span></td>
<td><span data-ttu-id="3de81-277">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="3de81-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-278">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="3de81-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="3de81-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-281">7</span><span class="sxs-lookup"><span data-stu-id="3de81-281">7</span></span></td>
<td><span data-ttu-id="3de81-282">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="3de81-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-283">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-284">–22 794,00</span><span class="sxs-lookup"><span data-stu-id="3de81-284">-22,794.00</span></span></td>
<td><span data-ttu-id="3de81-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-285">1,000.00</span></span></td>
<td><span data-ttu-id="3de81-286">–94,97</span><span class="sxs-lookup"><span data-stu-id="3de81-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-287">–21 888,87</span><span class="sxs-lookup"><span data-stu-id="3de81-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-288">8</span><span class="sxs-lookup"><span data-stu-id="3de81-288">8</span></span></td>
<td><span data-ttu-id="3de81-289">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-290">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-291">94.97</span><span class="sxs-lookup"><span data-stu-id="3de81-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-292">94.97</span><span class="sxs-lookup"><span data-stu-id="3de81-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-293">9</span><span class="sxs-lookup"><span data-stu-id="3de81-293">9</span></span></td>
<td><span data-ttu-id="3de81-294">Sularaha</span><span class="sxs-lookup"><span data-stu-id="3de81-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-295">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-295">-1,008.00</span></span></td>
<td><span data-ttu-id="3de81-296">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-297">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-298">10</span><span class="sxs-lookup"><span data-stu-id="3de81-298">10</span></span></td>
<td><span data-ttu-id="3de81-299">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-300">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-301">949.75</span><span class="sxs-lookup"><span data-stu-id="3de81-301">949.75</span></span></td>
<td><span data-ttu-id="3de81-302">949.75</span><span class="sxs-lookup"><span data-stu-id="3de81-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-303">11</span><span class="sxs-lookup"><span data-stu-id="3de81-303">11</span></span></td>
<td><span data-ttu-id="3de81-304">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="3de81-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-305">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-306">–949,75</span><span class="sxs-lookup"><span data-stu-id="3de81-306">-949.75</span></span></td>
<td><span data-ttu-id="3de81-307">–949,75</span><span class="sxs-lookup"><span data-stu-id="3de81-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3de81-308">Nagu eelnev tabel näitab, tuleb nii kohustusliku aruandluse kui ka IFRS-i aruandluse põhjal esitada kolm raamatut.</span><span class="sxs-lookup"><span data-stu-id="3de81-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="3de81-309">Kohustuslik raamat kirjendab rendimaksed vastavalt sularahapõhise raamatupidamise praeguse kihi reeglitele.</span><span class="sxs-lookup"><span data-stu-id="3de81-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="3de81-310">Kohustuslik tagasivõtmise raamat pöörab kohustuslikud töölehe kanded ümber.</span><span class="sxs-lookup"><span data-stu-id="3de81-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="3de81-311">IFRS 16 raamat loob töölehe kirjed, mida nõutakse IFRS 16 alusel.</span><span class="sxs-lookup"><span data-stu-id="3de81-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="3de81-312">Peate sisestama rendi ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="3de81-312">You must enter a lease only one time.</span></span> <span data-ttu-id="3de81-313">Seejärel saate avada lehe **Raamatud**, et näha kõiki üürilepinguga seotud raamatuid.</span><span class="sxs-lookup"><span data-stu-id="3de81-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="3de81-314">Kui loote raamatud, peavad kõik kolm olema seotud sama rendikirjega.</span><span class="sxs-lookup"><span data-stu-id="3de81-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="3de81-315">Esimese töölehe kirje talletab kohustuslikku raamatusse rendikogemuse.</span><span class="sxs-lookup"><span data-stu-id="3de81-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="3de81-316">Makseid saate luua kas partiina või valides kohustuslikus raamatus maksegraafiku.</span><span class="sxs-lookup"><span data-stu-id="3de81-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="3de81-317">Käesolevas näites luuakse kohustusliku raamatu jaoks maksegraafikust järgmine töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="3de81-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="3de81-318">Rendimakse – 31.1.2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="3de81-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="3de81-319">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-319">Account type</span></span> | <span data-ttu-id="3de81-320">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-320">Account number</span></span> | <span data-ttu-id="3de81-321">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-321">Layer</span></span>   | <span data-ttu-id="3de81-322">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-322">Account description</span></span> | <span data-ttu-id="3de81-323">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-323">Debit</span></span>    | <span data-ttu-id="3de81-324">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="3de81-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-325">Ledger</span></span>       | <span data-ttu-id="3de81-326">1</span><span class="sxs-lookup"><span data-stu-id="3de81-326">1</span></span>              | <span data-ttu-id="3de81-327">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-327">Current</span></span> | <span data-ttu-id="3de81-328">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-328">Lease expense</span></span>       | <span data-ttu-id="3de81-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-329">1,000.00</span></span> |          |
| <span data-ttu-id="3de81-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-330">Ledger</span></span>       | <span data-ttu-id="3de81-331">4</span><span class="sxs-lookup"><span data-stu-id="3de81-331">4</span></span>              | <span data-ttu-id="3de81-332">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-332">Current</span></span> | <span data-ttu-id="3de81-333">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-333">Clearing account</span></span>    |          | <span data-ttu-id="3de81-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-334">1,000.00</span></span> |

<span data-ttu-id="3de81-335">Ostureskontro ametnik kasutab standardset Dynamics 365 funktsiooni, et luua arve rendi eest maksmiseks väljaspool vara rentimist.</span><span class="sxs-lookup"><span data-stu-id="3de81-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="3de81-336">Kuid selle asemel, et valida deebeti kontona **Rendikulu**, valib ostureskontro ametnik konto, et luua järgmine kirje.</span><span class="sxs-lookup"><span data-stu-id="3de81-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="3de81-337">AP protsess – 31.1./2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="3de81-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="3de81-338">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-338">Account type</span></span> | <span data-ttu-id="3de81-339">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-339">Account number</span></span> | <span data-ttu-id="3de81-340">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-340">Layer</span></span>   | <span data-ttu-id="3de81-341">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-341">Account description</span></span> | <span data-ttu-id="3de81-342">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-342">Debit</span></span>    | <span data-ttu-id="3de81-343">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="3de81-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-344">Ledger</span></span>       | <span data-ttu-id="3de81-345">4</span><span class="sxs-lookup"><span data-stu-id="3de81-345">4</span></span>              | <span data-ttu-id="3de81-346">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-346">Current</span></span> | <span data-ttu-id="3de81-347">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-347">Clearing account</span></span>    | <span data-ttu-id="3de81-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-348">1,000.00</span></span> |          |
| <span data-ttu-id="3de81-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-349">Ledger</span></span>       | <span data-ttu-id="3de81-350">2</span><span class="sxs-lookup"><span data-stu-id="3de81-350">2</span></span>              | <span data-ttu-id="3de81-351">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-351">Current</span></span> | <span data-ttu-id="3de81-352">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="3de81-352">Bank fee</span></span>            | <span data-ttu-id="3de81-353">3.00</span><span class="sxs-lookup"><span data-stu-id="3de81-353">3.00</span></span>     |          |
| <span data-ttu-id="3de81-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-354">Ledger</span></span>       | <span data-ttu-id="3de81-355">3</span><span class="sxs-lookup"><span data-stu-id="3de81-355">3</span></span>              | <span data-ttu-id="3de81-356">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-356">Current</span></span> | <span data-ttu-id="3de81-357">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-357">VAT expense</span></span>         | <span data-ttu-id="3de81-358">5.00</span><span class="sxs-lookup"><span data-stu-id="3de81-358">5.00</span></span>     |          |
| <span data-ttu-id="3de81-359">Tarnija</span><span class="sxs-lookup"><span data-stu-id="3de81-359">Vendor</span></span>       | <span data-ttu-id="3de81-360">5</span><span class="sxs-lookup"><span data-stu-id="3de81-360">5</span></span>              | <span data-ttu-id="3de81-361">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-361">Current</span></span> | <span data-ttu-id="3de81-362">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="3de81-362">Accounts payable</span></span>    |          | <span data-ttu-id="3de81-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="3de81-363">1,008.00</span></span> |

<span data-ttu-id="3de81-364">Kui hankijale edastatakse arve, järgite tavalist maksetoimingut.</span><span class="sxs-lookup"><span data-stu-id="3de81-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="3de81-365">Selle toimingu käigus luuakse järgmine töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="3de81-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="3de81-366">Sularahamakse – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="3de81-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="3de81-367">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-367">Account type</span></span> | <span data-ttu-id="3de81-368">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-368">Account number</span></span> | <span data-ttu-id="3de81-369">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-369">Layer</span></span>   | <span data-ttu-id="3de81-370">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-370">Account description</span></span> | <span data-ttu-id="3de81-371">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-371">Debit</span></span>    | <span data-ttu-id="3de81-372">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="3de81-373">Tarnija</span><span class="sxs-lookup"><span data-stu-id="3de81-373">Vendor</span></span>       | <span data-ttu-id="3de81-374">5</span><span class="sxs-lookup"><span data-stu-id="3de81-374">5</span></span>              | <span data-ttu-id="3de81-375">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-375">Current</span></span> | <span data-ttu-id="3de81-376">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="3de81-376">Accounts Payable</span></span>    | <span data-ttu-id="3de81-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="3de81-377">1,008.00</span></span> |          |
| <span data-ttu-id="3de81-378">Pank</span><span class="sxs-lookup"><span data-stu-id="3de81-378">Bank</span></span>         | <span data-ttu-id="3de81-379">9</span><span class="sxs-lookup"><span data-stu-id="3de81-379">9</span></span>              | <span data-ttu-id="3de81-380">Praegune</span><span class="sxs-lookup"><span data-stu-id="3de81-380">Current</span></span> | <span data-ttu-id="3de81-381">Sularaha</span><span class="sxs-lookup"><span data-stu-id="3de81-381">Cash</span></span>                |          | <span data-ttu-id="3de81-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="3de81-382">1,008.00</span></span> |

<span data-ttu-id="3de81-383">Selleks hetkeks on teil antud rendikirje kohustusliku aruandlusnõude alusel kõik raamatupidamistoimingud tehtud ja saate luua praegust kihti kasutades proovibilansi.</span><span class="sxs-lookup"><span data-stu-id="3de81-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="3de81-384">Süsteem tagastab proovibilansi, millel on järgmised arvud.</span><span class="sxs-lookup"><span data-stu-id="3de81-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="3de81-385">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="3de81-386">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="3de81-387">Kohustuslik raamat (praegune kiht)</span><span class="sxs-lookup"><span data-stu-id="3de81-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="3de81-388">Praeguse kihi kogusumma</span><span class="sxs-lookup"><span data-stu-id="3de81-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3de81-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="3de81-389">JE-100</span></span></th>
<th><span data-ttu-id="3de81-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="3de81-390">JE-110</span></span></th>
<th><span data-ttu-id="3de81-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="3de81-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3de81-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="3de81-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="3de81-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3de81-395">1</span><span class="sxs-lookup"><span data-stu-id="3de81-395">1</span></span></td>
<td><span data-ttu-id="3de81-396">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-396">Lease expense</span></span></td>
<td><span data-ttu-id="3de81-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-399">2</span><span class="sxs-lookup"><span data-stu-id="3de81-399">2</span></span></td>
<td><span data-ttu-id="3de81-400">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="3de81-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-401">3.00</span><span class="sxs-lookup"><span data-stu-id="3de81-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-402">3.00</span><span class="sxs-lookup"><span data-stu-id="3de81-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-403">3</span><span class="sxs-lookup"><span data-stu-id="3de81-403">3</span></span></td>
<td><span data-ttu-id="3de81-404">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-405">5.00</span><span class="sxs-lookup"><span data-stu-id="3de81-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-406">5.00</span><span class="sxs-lookup"><span data-stu-id="3de81-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-407">4</span><span class="sxs-lookup"><span data-stu-id="3de81-407">4</span></span></td>
<td><span data-ttu-id="3de81-408">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-408">Clearing account</span></span></td>
<td><span data-ttu-id="3de81-409">–1000,00</span><span class="sxs-lookup"><span data-stu-id="3de81-409">-1,000.00</span></span></td>
<td><span data-ttu-id="3de81-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-411">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-412">5</span><span class="sxs-lookup"><span data-stu-id="3de81-412">5</span></span></td>
<td><span data-ttu-id="3de81-413">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="3de81-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="3de81-414">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-414">-1,008.00</span></span></td>
<td><span data-ttu-id="3de81-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="3de81-415">1,008.00</span></span></td>
<td><span data-ttu-id="3de81-416">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-417">6</span><span class="sxs-lookup"><span data-stu-id="3de81-417">6</span></span></td>
<td><span data-ttu-id="3de81-418">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="3de81-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-419">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-420">7</span><span class="sxs-lookup"><span data-stu-id="3de81-420">7</span></span></td>
<td><span data-ttu-id="3de81-421">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="3de81-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-422">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-423">8</span><span class="sxs-lookup"><span data-stu-id="3de81-423">8</span></span></td>
<td><span data-ttu-id="3de81-424">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-425">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-426">9</span><span class="sxs-lookup"><span data-stu-id="3de81-426">9</span></span></td>
<td><span data-ttu-id="3de81-427">Sularaha</span><span class="sxs-lookup"><span data-stu-id="3de81-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-428">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-428">-1,008.00</span></span></td>
<td><span data-ttu-id="3de81-429">–1008,00</span><span class="sxs-lookup"><span data-stu-id="3de81-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-430">10</span><span class="sxs-lookup"><span data-stu-id="3de81-430">10</span></span></td>
<td><span data-ttu-id="3de81-431">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-432">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3de81-433">11</span><span class="sxs-lookup"><span data-stu-id="3de81-433">11</span></span></td>
<td><span data-ttu-id="3de81-434">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="3de81-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="3de81-435">0,00</span><span class="sxs-lookup"><span data-stu-id="3de81-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="3de81-436">Kui soovite kasutada sama proovibilansi käitamiseks kasutada IFRS 16 andmeid, tuleb kohustusliku raamatupidamise töölehe kanded tagasi võtta ja IFRS 16 töölehe kanded tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="3de81-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="3de81-437">Kohustusliku töölehe kirjete tühistamiseks sisaldab see näide seadusjärgset tagasivõtmise raamatut, millel on sama seadistus kui kohustuslik raamat, kuid vastupidine sisestusreegel.</span><span class="sxs-lookup"><span data-stu-id="3de81-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="3de81-438">Näiteks, kohustuslik raamat *debiteerib* rendikulu kontot, kuid tagasivõtmise konto *krediteerib* seda kontot.</span><span class="sxs-lookup"><span data-stu-id="3de81-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="3de81-439">Need seosed on lihtne määratleda vara rentimise sisestamise kontol lehel **Vara rentimise parameetrid**(**Vara rentimine \> Seadistus \> Vara rentimise parameetrid**).</span><span class="sxs-lookup"><span data-stu-id="3de81-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="3de81-440">Kui tagasivõtmise raamatu puhul kasutataks kohustusliku raamatuga sama protsessi, loodaks järgmine töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="3de81-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="3de81-441">Erinevus seisneb selles, et tagasivõtmise raamat kirjendab kohustusliku raamatu tagastamise kirjed.</span><span class="sxs-lookup"><span data-stu-id="3de81-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="3de81-442">Tagasivõtmise kirjed tehakse ka kliendi kihis.</span><span class="sxs-lookup"><span data-stu-id="3de81-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="3de81-443">Kui proovibilanssi käitatakse praeguses kihis, siis tagasivõtmise töölehe kirjeid ei kaasataks.</span><span class="sxs-lookup"><span data-stu-id="3de81-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="3de81-444">Rendimakse – 31.1.2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="3de81-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="3de81-445">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-445">Account type</span></span> | <span data-ttu-id="3de81-446">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-446">Account number</span></span> | <span data-ttu-id="3de81-447">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-447">Layer</span></span>  | <span data-ttu-id="3de81-448">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-448">Account description</span></span> | <span data-ttu-id="3de81-449">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-449">Debit</span></span>    | <span data-ttu-id="3de81-450">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="3de81-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-451">Ledger</span></span>       | <span data-ttu-id="3de81-452">4</span><span class="sxs-lookup"><span data-stu-id="3de81-452">4</span></span>              | <span data-ttu-id="3de81-453">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-453">Custom</span></span> | <span data-ttu-id="3de81-454">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-454">Clearing account</span></span>    | <span data-ttu-id="3de81-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-455">1,000.00</span></span> |          |
| <span data-ttu-id="3de81-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-456">Ledger</span></span>       | <span data-ttu-id="3de81-457">1</span><span class="sxs-lookup"><span data-stu-id="3de81-457">1</span></span>              | <span data-ttu-id="3de81-458">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-458">Custom</span></span> | <span data-ttu-id="3de81-459">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-459">Lease expense</span></span>       |          | <span data-ttu-id="3de81-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-460">1,000.00</span></span> |

<span data-ttu-id="3de81-461">Nüüd kui olete kohustusliku töölehe sisestused eemaldanud, kirjendate kõik töölehe kirjed, mida IFRS 16 nõuab, IFRS 16 raamatus.</span><span class="sxs-lookup"><span data-stu-id="3de81-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="3de81-462">Need kanded hõlmavad kasutamisõiguse esemeks oleva vara esialgset tunnustamist ning intressikirjet ja kulumi arvestust.</span><span class="sxs-lookup"><span data-stu-id="3de81-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="3de81-463">Esialgne tunnustamine – 1.1.2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="3de81-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="3de81-464">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-464">Account type</span></span> | <span data-ttu-id="3de81-465">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-465">Account number</span></span> | <span data-ttu-id="3de81-466">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-466">Layer</span></span>  | <span data-ttu-id="3de81-467">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-467">Account description</span></span>      | <span data-ttu-id="3de81-468">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-468">Debit</span></span>     | <span data-ttu-id="3de81-469">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="3de81-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-470">Ledger</span></span>       | <span data-ttu-id="3de81-471">6</span><span class="sxs-lookup"><span data-stu-id="3de81-471">6</span></span>              | <span data-ttu-id="3de81-472">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-472">Custom</span></span> | <span data-ttu-id="3de81-473">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="3de81-473">ROU Asset</span></span>                | <span data-ttu-id="3de81-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="3de81-474">22,793.90</span></span> |           |
| <span data-ttu-id="3de81-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-475">Ledger</span></span>       | <span data-ttu-id="3de81-476">7</span><span class="sxs-lookup"><span data-stu-id="3de81-476">7</span></span>              | <span data-ttu-id="3de81-477">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-477">Custom</span></span> | <span data-ttu-id="3de81-478">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="3de81-478">Finance lease obligation</span></span> |           | <span data-ttu-id="3de81-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="3de81-479">22,793.90</span></span> |

<span data-ttu-id="3de81-480">Rendimakse sisestatakse sarnaselt teistele rendimaksetele.</span><span class="sxs-lookup"><span data-stu-id="3de81-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="3de81-481">Tühjendamise konto kasutamise põhjus on tagada, et sularaha krediteeritakse ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="3de81-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="3de81-482">Rendimakse – 31.1.2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="3de81-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="3de81-483">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-483">Account type</span></span> | <span data-ttu-id="3de81-484">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-484">Account number</span></span> | <span data-ttu-id="3de81-485">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-485">Layer</span></span>  | <span data-ttu-id="3de81-486">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-486">Account description</span></span>      | <span data-ttu-id="3de81-487">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-487">Debit</span></span>    | <span data-ttu-id="3de81-488">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="3de81-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-489">Ledger</span></span>       | <span data-ttu-id="3de81-490">7</span><span class="sxs-lookup"><span data-stu-id="3de81-490">7</span></span>              | <span data-ttu-id="3de81-491">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-491">Custom</span></span> | <span data-ttu-id="3de81-492">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="3de81-492">Finance lease obligation</span></span> | <span data-ttu-id="3de81-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-493">1,000.00</span></span> |          |
| <span data-ttu-id="3de81-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-494">Ledger</span></span>       | <span data-ttu-id="3de81-495">4</span><span class="sxs-lookup"><span data-stu-id="3de81-495">4</span></span>              | <span data-ttu-id="3de81-496">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-496">Custom</span></span> | <span data-ttu-id="3de81-497">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-497">Clearing account</span></span>         |          | <span data-ttu-id="3de81-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="3de81-498">1,000.00</span></span> |

<span data-ttu-id="3de81-499">Intressikulu töölehe kirje luuakse kohustise amortiseerimise graafikust.</span><span class="sxs-lookup"><span data-stu-id="3de81-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="3de81-500">Intressikulu – 31.1.2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="3de81-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="3de81-501">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-501">Account type</span></span> | <span data-ttu-id="3de81-502">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-502">Account number</span></span> | <span data-ttu-id="3de81-503">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-503">Layer</span></span>  | <span data-ttu-id="3de81-504">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-504">Account description</span></span>      | <span data-ttu-id="3de81-505">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-505">Debit</span></span> | <span data-ttu-id="3de81-506">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="3de81-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-507">Ledger</span></span>       | <span data-ttu-id="3de81-508">8</span><span class="sxs-lookup"><span data-stu-id="3de81-508">8</span></span>              | <span data-ttu-id="3de81-509">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-509">Custom</span></span> | <span data-ttu-id="3de81-510">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-510">Interest expense</span></span>         | <span data-ttu-id="3de81-511">94.97</span><span class="sxs-lookup"><span data-stu-id="3de81-511">94.97</span></span> |        |
| <span data-ttu-id="3de81-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-512">Ledger</span></span>       | <span data-ttu-id="3de81-513">7</span><span class="sxs-lookup"><span data-stu-id="3de81-513">7</span></span>              | <span data-ttu-id="3de81-514">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-514">Custom</span></span> | <span data-ttu-id="3de81-515">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="3de81-515">Finance lease obligation</span></span> |       | <span data-ttu-id="3de81-516">94.97</span><span class="sxs-lookup"><span data-stu-id="3de81-516">94.97</span></span>  |

<span data-ttu-id="3de81-517">Kulumi kulu töölehe kirje luuakse vara kulumi graafikust.</span><span class="sxs-lookup"><span data-stu-id="3de81-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="3de81-518">Kulumi kulu – 31.1.2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="3de81-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="3de81-519">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="3de81-519">Account type</span></span> | <span data-ttu-id="3de81-520">Konto number</span><span class="sxs-lookup"><span data-stu-id="3de81-520">Account number</span></span> | <span data-ttu-id="3de81-521">Kiht</span><span class="sxs-lookup"><span data-stu-id="3de81-521">Layer</span></span>  | <span data-ttu-id="3de81-522">Konto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-522">Account description</span></span>      | <span data-ttu-id="3de81-523">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="3de81-523">Debit</span></span>  | <span data-ttu-id="3de81-524">Krediit</span><span class="sxs-lookup"><span data-stu-id="3de81-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="3de81-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-525">Ledger</span></span>       | <span data-ttu-id="3de81-526">10</span><span class="sxs-lookup"><span data-stu-id="3de81-526">10</span></span>             | <span data-ttu-id="3de81-527">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-527">Custom</span></span> | <span data-ttu-id="3de81-528">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-528">Depreciation expense</span></span>     | <span data-ttu-id="3de81-529">949.75</span><span class="sxs-lookup"><span data-stu-id="3de81-529">949.75</span></span> |        |
| <span data-ttu-id="3de81-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="3de81-530">Ledger</span></span>       | <span data-ttu-id="3de81-531">11</span><span class="sxs-lookup"><span data-stu-id="3de81-531">11</span></span>             | <span data-ttu-id="3de81-532">Kohandatud</span><span class="sxs-lookup"><span data-stu-id="3de81-532">Custom</span></span> | <span data-ttu-id="3de81-533">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="3de81-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="3de81-534">949.75</span><span class="sxs-lookup"><span data-stu-id="3de81-534">949.75</span></span> |

<span data-ttu-id="3de81-535">Pärast kõikide nende töölehe kirjete loomist ja sisestamist näete järgmist „kohandatud kiht 1” väärtuseid.</span><span class="sxs-lookup"><span data-stu-id="3de81-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="3de81-536">Pange tähele, et viimane veerg sisaldab pangatasu, käibemaksu (KM) kulu ja eelmise kihi sularaha vähendamist, kuid see ei sisalda kohustusliku aruandluse töölehe kandeid.</span><span class="sxs-lookup"><span data-stu-id="3de81-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="3de81-537">Seega saavutate tõelise topeltaruandluse võimalused.</span><span class="sxs-lookup"><span data-stu-id="3de81-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="3de81-538">Sel hetkel peab ettevõte lihtsalt käivitama oma proovibilansi ja kombineerima praeguse kihi ja kohandatud kihi, et luua IFRS-i prooviversioon.</span><span class="sxs-lookup"><span data-stu-id="3de81-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="3de81-539">Konto nr</span><span class="sxs-lookup"><span data-stu-id="3de81-539">Account No</span></span> | <span data-ttu-id="3de81-540">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3de81-540">Description</span></span>              | <span data-ttu-id="3de81-541">Kohustuslik raamat\-Praegune tase\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-542">Kohustuslik raamat\-Praegune tase\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-543">Kohustuslik raamat\-Praegune tase\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-544">Praegune kiht \- kogusummad</span><span class="sxs-lookup"><span data-stu-id="3de81-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="3de81-545">Tühistamise raamat\-Kohandatud kiht\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-546">IFRS 16 raamat\-kohandatud kiht \-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-547">IFRS 16 raamat\-kohandatud kiht \-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-548">IFRS 16 raamat\-kohandatud kiht \-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-549">IFRS 16 raamat\-kohandatud kiht \-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="3de81-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="3de81-550">Kohandatud kiht \+ Praegune kiht \- Tööriistad</span><span class="sxs-lookup"><span data-stu-id="3de81-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="3de81-551">1</span><span class="sxs-lookup"><span data-stu-id="3de81-551">1</span></span>          | <span data-ttu-id="3de81-552">Rendikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-552">Lease expense</span></span>            | <span data-ttu-id="3de81-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="3de81-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-554">1,000\.00</span></span>               |   | <span data-ttu-id="3de81-555">\-1000</span><span class="sxs-lookup"><span data-stu-id="3de81-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="3de81-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-556">0\.00</span></span>                                   |
| <span data-ttu-id="3de81-557">2</span><span class="sxs-lookup"><span data-stu-id="3de81-557">2</span></span>          | <span data-ttu-id="3de81-558">Pangatasu</span><span class="sxs-lookup"><span data-stu-id="3de81-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="3de81-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="3de81-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="3de81-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-561">3\.00</span></span>                                   |
| <span data-ttu-id="3de81-562">3</span><span class="sxs-lookup"><span data-stu-id="3de81-562">3</span></span>          | <span data-ttu-id="3de81-563">KM-kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="3de81-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="3de81-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="3de81-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-566">5\.00</span></span>                                   |
| <span data-ttu-id="3de81-567">4</span><span class="sxs-lookup"><span data-stu-id="3de81-567">4</span></span>          | <span data-ttu-id="3de81-568">Kliiringukonto</span><span class="sxs-lookup"><span data-stu-id="3de81-568">Clearing account</span></span>         | <span data-ttu-id="3de81-569">\-1000\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="3de81-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="3de81-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-571">0\.00</span></span>                   |   | <span data-ttu-id="3de81-572">1000</span><span class="sxs-lookup"><span data-stu-id="3de81-572">1,000</span></span>                                           |                                                | <span data-ttu-id="3de81-573">\-1000</span><span class="sxs-lookup"><span data-stu-id="3de81-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="3de81-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-574">0\.00</span></span>                                   |
| <span data-ttu-id="3de81-575">5</span><span class="sxs-lookup"><span data-stu-id="3de81-575">5</span></span>          | <span data-ttu-id="3de81-576">Ostureskontro</span><span class="sxs-lookup"><span data-stu-id="3de81-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="3de81-577">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="3de81-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-578">1,008\.00</span></span>                                         | <span data-ttu-id="3de81-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="3de81-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-580">0\.00</span></span>                                   |
| <span data-ttu-id="3de81-581">6</span><span class="sxs-lookup"><span data-stu-id="3de81-581">6</span></span>          | <span data-ttu-id="3de81-582">Kasutamisõiguse esemeks olev vara</span><span class="sxs-lookup"><span data-stu-id="3de81-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="3de81-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="3de81-584">22,794</span><span class="sxs-lookup"><span data-stu-id="3de81-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="3de81-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="3de81-585">22,793\.90</span></span>                              |
| <span data-ttu-id="3de81-586">7</span><span class="sxs-lookup"><span data-stu-id="3de81-586">7</span></span>          | <span data-ttu-id="3de81-587">Kapitalirendi kohustus</span><span class="sxs-lookup"><span data-stu-id="3de81-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="3de81-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="3de81-589">\-22 794</span><span class="sxs-lookup"><span data-stu-id="3de81-589">\-22,794</span></span>                                       | <span data-ttu-id="3de81-590">1000</span><span class="sxs-lookup"><span data-stu-id="3de81-590">1,000</span></span>                                          | <span data-ttu-id="3de81-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="3de81-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="3de81-592">\-21 888\.87</span><span class="sxs-lookup"><span data-stu-id="3de81-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="3de81-593">8</span><span class="sxs-lookup"><span data-stu-id="3de81-593">8</span></span>          | <span data-ttu-id="3de81-594">Intressikulu</span><span class="sxs-lookup"><span data-stu-id="3de81-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="3de81-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="3de81-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="3de81-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="3de81-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="3de81-597">94\.97</span></span>                                  |
| <span data-ttu-id="3de81-598">9</span><span class="sxs-lookup"><span data-stu-id="3de81-598">9</span></span>          | <span data-ttu-id="3de81-599">Sularaha</span><span class="sxs-lookup"><span data-stu-id="3de81-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="3de81-600">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="3de81-601">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="3de81-602">\-1008\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="3de81-603">10</span><span class="sxs-lookup"><span data-stu-id="3de81-603">10</span></span>         | <span data-ttu-id="3de81-604">Kulumi kulu</span><span class="sxs-lookup"><span data-stu-id="3de81-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="3de81-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="3de81-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="3de81-606">949\.75</span></span>                                        | <span data-ttu-id="3de81-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="3de81-607">949\.75</span></span>                                 |
| <span data-ttu-id="3de81-608">11</span><span class="sxs-lookup"><span data-stu-id="3de81-608">11</span></span>         | <span data-ttu-id="3de81-609">Akumuleeritud kulum</span><span class="sxs-lookup"><span data-stu-id="3de81-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="3de81-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="3de81-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="3de81-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="3de81-611">\-949\.75</span></span>                                      | <span data-ttu-id="3de81-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="3de81-612">\-949\.75</span></span>                               |


