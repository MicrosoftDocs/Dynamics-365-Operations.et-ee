---
title: Põhivara väärtusmudeli ja kulumiraamatu ühendamine
description: 'Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.'
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 221564
ms.assetid: 7c68eb7c-8b1a-4dd9-afb8-04b4040e305e
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3225b214e729ff13d4ffe8ad1d8cf0f2d6baae49
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187195"
---
# <a name="fixed-asset-value-model-and-depreciation-book-merge"></a><span data-ttu-id="1e2fb-104">Põhivara väärtusmudeli ja kulumiraamatu ühendamine</span><span class="sxs-lookup"><span data-stu-id="1e2fb-104">Fixed asset value model and depreciation book merge</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1e2fb-105">Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-105">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="1e2fb-106">Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-106">In the Microsoft Dynamics 365 for Operations (1611) release, the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span>

<span data-ttu-id="1e2fb-107">Uued raamatu funktsioonid põhinevad varasema väärtusmudeli funktsioonidel, kui hõlmab ka kõiki funktsioone, mis olid varasemalt antud ainult kulumiraamatutes.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-107">The new book functionality is based on earlier value model functionality but also includes all functionality that was previously provided only in depreciation books.</span></span> <span data-ttu-id="1e2fb-108">[![Raamat väärtusmudeli ja kulumiraamatu funktsioonide ühendamisena](./media/fixed-assets.png)](./media/fixed-assets.png) Selle ühendamise tõttu saate nüüd kasutada lehtede, päringute ja aruannete üksikut kogumit kõikide teie põhivara protsesside jaoks.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-108">[![Book as a merging of value model and depreciation book functionality](./media/fixed-assets.png)](./media/fixed-assets.png) Because of this merge, you can now use a single set of pages, inquiries, and reports for all your fixed asset processes.</span></span> <span data-ttu-id="1e2fb-109">Selles teemas olevates tabelites kirjeldatakse kulumiraamatute ja väärtusmudelite varasemaid funktsioone koos raamatute uute funktsioonidega.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-109">The tables in this topic describe the earlier functionality for depreciation books and value models, together with the new functionality for books.</span></span>

## <a name="setup"></a><span data-ttu-id="1e2fb-110">Häälestus</span><span class="sxs-lookup"><span data-stu-id="1e2fb-110">Setup</span></span>
<span data-ttu-id="1e2fb-111">Vaikimisi sisestavad raamatud nii pearaamatusse (PR) kui ka põhivara alammoodulisse.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-111">By default, books post to both the general ledger (GL) and the fixed asset subledger.</span></span> <span data-ttu-id="1e2fb-112">Raamatutel on uus valik **Pearaamatusse sisestamine**, mis võimaldab teil keelata PR-sse sisestamise ja sisestada ainult põhivara alammoodulisse.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-112">Books have a new **Post to general ledger** option that lets you disable posting to the GL and post only to the fixed asset subledger.</span></span> <span data-ttu-id="1e2fb-113">See funktsioon sarnaneb kulumiraamatute varasemale sisestamise käitumisele.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-113">This functionality resembles the earlier posting behavior for depreciation books.</span></span> <span data-ttu-id="1e2fb-114">Töölehe nimede seadistusel on uus sisestamiskiht, mille nimetus on Pole.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-114">The journal names setup has a new posting layer that is named None.</span></span> <span data-ttu-id="1e2fb-115">Sisestamiskiht lisati spetsiifiliselt põhivara kannetele.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-115">This posting layer was added specifically for fixed asset transactions.</span></span> <span data-ttu-id="1e2fb-116">Sisestamaks kandeid raamatutele, mis ei sisesta pearaamatusse, peate kasutama töölehe nime, mille sisestamiskiht on määratud valikul **Pole**.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-116">To post transactions for books that don't post to the GL, you must use a journal name that has the posting layer set to **None**.</span></span>

|                                                  |                                 |                                 |                                                         |
|--------------------------------------------------|---------------------------------|---------------------------------|---------------------------------------------------------|
|                                                  | <span data-ttu-id="1e2fb-117">Kulumiraamat</span><span class="sxs-lookup"><span data-stu-id="1e2fb-117">Depreciation book</span></span>               | <span data-ttu-id="1e2fb-118">Väärtusmudel</span><span class="sxs-lookup"><span data-stu-id="1e2fb-118">Value model</span></span>                     | <span data-ttu-id="1e2fb-119">Raamat (Uus)</span><span class="sxs-lookup"><span data-stu-id="1e2fb-119">Book (New)</span></span>                                              |
| <span data-ttu-id="1e2fb-120">Pearaamatusse sisestamine</span><span class="sxs-lookup"><span data-stu-id="1e2fb-120">Post to the GL</span></span>                                   | <span data-ttu-id="1e2fb-121">Mitte kunagi</span><span class="sxs-lookup"><span data-stu-id="1e2fb-121">Never</span></span>                           | <span data-ttu-id="1e2fb-122">Alati</span><span class="sxs-lookup"><span data-stu-id="1e2fb-122">Always</span></span>                          | <span data-ttu-id="1e2fb-123">Valik pearaamatusse sisestamiseks</span><span class="sxs-lookup"><span data-stu-id="1e2fb-123">Option to post to the GL</span></span>                                |
| <span data-ttu-id="1e2fb-124">Sisestamiskihid</span><span class="sxs-lookup"><span data-stu-id="1e2fb-124">Posting layers</span></span>                                   | <span data-ttu-id="1e2fb-125">Pole kohaldatav</span><span class="sxs-lookup"><span data-stu-id="1e2fb-125">Not applicable</span></span>                  | <span data-ttu-id="1e2fb-126">3: Praegune, Toimingud ja Maks</span><span class="sxs-lookup"><span data-stu-id="1e2fb-126">3: Current, Operations, and Tax</span></span> | <span data-ttu-id="1e2fb-127">11: Praegune, Toimingud, Maks, 7 kohandatud kihti ja Pole</span><span class="sxs-lookup"><span data-stu-id="1e2fb-127">11: Current, Operations, Tax, 7 custom layers, and None</span></span> |
| <span data-ttu-id="1e2fb-128">Töölehe nimed</span><span class="sxs-lookup"><span data-stu-id="1e2fb-128">Journal names</span></span>                                    | <span data-ttu-id="1e2fb-129">Kulumiraamatu töölehtede nimed</span><span class="sxs-lookup"><span data-stu-id="1e2fb-129">Depreciation book journal names</span></span> | <span data-ttu-id="1e2fb-130">PR – töölehe nimed</span><span class="sxs-lookup"><span data-stu-id="1e2fb-130">GL - Journal names</span></span>              | <span data-ttu-id="1e2fb-131">PR – töölehe nimed</span><span class="sxs-lookup"><span data-stu-id="1e2fb-131">GL - Journal names</span></span>                                      |
| <span data-ttu-id="1e2fb-132">Tuletatud raamatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-132">Derived books</span></span>                                    | <span data-ttu-id="1e2fb-133">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-133">Not allowed</span></span>                     | <span data-ttu-id="1e2fb-134">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-134">Allowed</span></span>                         | <span data-ttu-id="1e2fb-135">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-135">Allowed</span></span>                                                 |
| <span data-ttu-id="1e2fb-136">Kulumireeglite alistamine vara tasandil</span><span class="sxs-lookup"><span data-stu-id="1e2fb-136">Depreciation profile override at the asset level</span></span> | <span data-ttu-id="1e2fb-137">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-137">Allowed</span></span>                         | <span data-ttu-id="1e2fb-138">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-138">Not allowed</span></span>                     | <span data-ttu-id="1e2fb-139">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-139">Allowed</span></span>                                                 |

## <a name="processes"></a><span data-ttu-id="1e2fb-140">Protsessid</span><span class="sxs-lookup"><span data-stu-id="1e2fb-140">Processes</span></span>
<span data-ttu-id="1e2fb-141">Protsessid kasutavad nüüd ühist lehte.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-141">Processes now use a common page.</span></span> <span data-ttu-id="1e2fb-142">Mõned protsessid on lubatud ainult juhul, kui valik **Pearaamatusse sisestamine** on raamatu seadistuses määratud valikule **Ei**.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-142">Some processes are allowed only if the **Post to general ledger** option is set to **No** in the book setup.</span></span>

|                                |                           |                     |                                          |
|--------------------------------|---------------------------|---------------------|------------------------------------------|
|                                | <span data-ttu-id="1e2fb-143">Kulumiraamat</span><span class="sxs-lookup"><span data-stu-id="1e2fb-143">Depreciation book</span></span>         | <span data-ttu-id="1e2fb-144">Väärtusmudel</span><span class="sxs-lookup"><span data-stu-id="1e2fb-144">Value model</span></span>         | <span data-ttu-id="1e2fb-145">Raamat (Uus)</span><span class="sxs-lookup"><span data-stu-id="1e2fb-145">Book (New)</span></span>                               |
| <span data-ttu-id="1e2fb-146">Kande kirje</span><span class="sxs-lookup"><span data-stu-id="1e2fb-146">Transaction entry</span></span>              | <span data-ttu-id="1e2fb-147">Kulumiraamatu tööleht</span><span class="sxs-lookup"><span data-stu-id="1e2fb-147">Depreciation book journal</span></span> | <span data-ttu-id="1e2fb-148">Põhivara tööleht</span><span class="sxs-lookup"><span data-stu-id="1e2fb-148">Fixed asset journal</span></span> | <span data-ttu-id="1e2fb-149">Põhivara tööleht</span><span class="sxs-lookup"><span data-stu-id="1e2fb-149">Fixed asset journal</span></span>                      |
| <span data-ttu-id="1e2fb-150">Lisakulum</span><span class="sxs-lookup"><span data-stu-id="1e2fb-150">Bonus depreciation</span></span>             | <span data-ttu-id="1e2fb-151">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-151">Allowed</span></span>                   | <span data-ttu-id="1e2fb-152">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-152">Not Allowed</span></span>         | <span data-ttu-id="1e2fb-153">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-153">Allowed</span></span>                                  |
| <span data-ttu-id="1e2fb-154">Kustuta kannete ajalugu</span><span class="sxs-lookup"><span data-stu-id="1e2fb-154">Delete historical transactions</span></span> | <span data-ttu-id="1e2fb-155">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-155">Allowed</span></span>                   | <span data-ttu-id="1e2fb-156">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-156">Not Allowed</span></span>         | <span data-ttu-id="1e2fb-157">Lubatud, kui te ei sisestata pearaamatusse</span><span class="sxs-lookup"><span data-stu-id="1e2fb-157">Allowed, unless you're posting to the GL</span></span> |
| <span data-ttu-id="1e2fb-158">Massvärskendus</span><span class="sxs-lookup"><span data-stu-id="1e2fb-158">Mass update</span></span>                    | <span data-ttu-id="1e2fb-159">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-159">Allowed</span></span>                   | <span data-ttu-id="1e2fb-160">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-160">Not Allowed</span></span>         | <span data-ttu-id="1e2fb-161">Lubatud, kui te ei sisestata pearaamatusse</span><span class="sxs-lookup"><span data-stu-id="1e2fb-161">Allowed, unless you're posting to the GL</span></span> |

## <a name="inquiries-and-reports"></a><span data-ttu-id="1e2fb-162">Päringud ja aruanded</span><span class="sxs-lookup"><span data-stu-id="1e2fb-162">Inquiries and reports</span></span>
<span data-ttu-id="1e2fb-163">Päringud ja aruanded toetavad kõiki raamatuid.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-163">Inquiries and reports support all books.</span></span> <span data-ttu-id="1e2fb-164">Aruanded, mis ei ole lisatud järgmisesse tabelisse, toetasid varasemalt nii kulumiraamatuid kui ka väärtusmudeleid ja toetavad nüüd jätkuvalt kõiki raamatu tüüpe.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-164">Reports that aren't included in the following table previously supported both depreciation books and value models, and will now continue to support all book types.</span></span> <span data-ttu-id="1e2fb-165">Väli **Sisestamiskiht** on lisatud ka aruannetesse, et saaksite hõlpsamalt tuvastada kande sisestused.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-165">The **Posting layer** field has also been added to reports, so that you can more easily identify the transaction postings.</span></span>

|                                       |                                |                          |                          |
|---------------------------------------|--------------------------------|--------------------------|--------------------------|
|                                       | <span data-ttu-id="1e2fb-166">Kulumiraamat</span><span class="sxs-lookup"><span data-stu-id="1e2fb-166">Depreciation book</span></span>              | <span data-ttu-id="1e2fb-167">Väärtusmudel</span><span class="sxs-lookup"><span data-stu-id="1e2fb-167">Value model</span></span>              | <span data-ttu-id="1e2fb-168">Raamat (Uus)</span><span class="sxs-lookup"><span data-stu-id="1e2fb-168">Book (New)</span></span>               |
| <span data-ttu-id="1e2fb-169">Päringud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-169">Inquiries</span></span>                             | <span data-ttu-id="1e2fb-170">Kulumiraamatu kanded</span><span class="sxs-lookup"><span data-stu-id="1e2fb-170">Depreciation book transactions</span></span> | <span data-ttu-id="1e2fb-171">Põhivarakanded</span><span class="sxs-lookup"><span data-stu-id="1e2fb-171">Fixed asset transactions</span></span> | <span data-ttu-id="1e2fb-172">Põhivarakanded</span><span class="sxs-lookup"><span data-stu-id="1e2fb-172">Fixed asset transactions</span></span> |
| <span data-ttu-id="1e2fb-173">Põhivara aruanne</span><span class="sxs-lookup"><span data-stu-id="1e2fb-173">Fixed asset statement</span></span>                 | <span data-ttu-id="1e2fb-174">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-174">Not allowed</span></span>                    | <span data-ttu-id="1e2fb-175">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-175">Allowed</span></span>                  | <span data-ttu-id="1e2fb-176">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-176">Allowed</span></span>                  |
| <span data-ttu-id="1e2fb-177">Põhivara alus</span><span class="sxs-lookup"><span data-stu-id="1e2fb-177">Fixed asset basis</span></span>                     | <span data-ttu-id="1e2fb-178">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-178">Allowed</span></span>                        | <span data-ttu-id="1e2fb-179">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-179">Not allowed</span></span>              | <span data-ttu-id="1e2fb-180">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-180">Allowed</span></span>                  |
| <span data-ttu-id="1e2fb-181">Põhivara seotavus kvartali keskel</span><span class="sxs-lookup"><span data-stu-id="1e2fb-181">Fixed asset mid-quarter applicability</span></span> | <span data-ttu-id="1e2fb-182">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-182">Allowed</span></span>                        | <span data-ttu-id="1e2fb-183">Pole lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-183">Not allowed</span></span>              | <span data-ttu-id="1e2fb-184">Lubatud</span><span class="sxs-lookup"><span data-stu-id="1e2fb-184">Allowed</span></span>                  |

## <a name="upgrade"></a><span data-ttu-id="1e2fb-185">Täiendamine</span><span class="sxs-lookup"><span data-stu-id="1e2fb-185">Upgrade</span></span>
<span data-ttu-id="1e2fb-186">Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-186">The upgrade process will move your existing setup and all your existing transactions to the new book structure.</span></span> <span data-ttu-id="1e2fb-187">Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-187">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="1e2fb-188">Siiski liigutatakse kulumiraamatud raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-188">However, depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="1e2fb-189">Kulumiraamatu töölehe nimed liigutatakse pearaamatu töölehele, mille nimel on sisestamiskiht määratud sättele **Pole**.</span><span class="sxs-lookup"><span data-stu-id="1e2fb-189">Depreciation book journal names will be moved to a general ledger journal name that has the posting layer set to **None**.</span></span>


