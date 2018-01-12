---
title: Numbriseeriad
description: "Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid."
author: MargoC
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 15461
ms.assetid: 6e19bd1d-192b-4da2-8573-84f6e1ce98ef
ms.search.region: Global
ms.author: margoc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 63bf043124797b328116fd7951913eaeda6ff97b
ms.openlocfilehash: 8e3899e1ad5f4be754687c0e2d59348e7a773fd8
ms.contentlocale: et-ee
ms.lasthandoff: 01/12/2018

---

# <a name="number-sequences"></a><span data-ttu-id="0869f-103">Numbriseeriad</span><span class="sxs-lookup"><span data-stu-id="0869f-103">Number sequences</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0869f-104">Numbriseeriaid kasutatakse loetavate ainuidentifikaatorite loomiseks koondandmete ja kannete kirjete jaoks, mis nõuavad identifikaatoreid.</span><span class="sxs-lookup"><span data-stu-id="0869f-104">Number sequences are used to generate readable, unique identifiers for master data records and transaction records that require identifiers.</span></span> <span data-ttu-id="0869f-105">Koondandmete kirjet või kandekirjet, mis nõuab ID-d, nimetatakse *viiteks*.</span><span class="sxs-lookup"><span data-stu-id="0869f-105">A master data record or transaction record that requires an identifier is referred to as a *reference*.</span></span>

<span data-ttu-id="0869f-106">Enne kui saate viite jaoks uusi kirjeid luua, peate seadistama numbriseeria ja selle viitega siduma.</span><span class="sxs-lookup"><span data-stu-id="0869f-106">Before you can create new records for a reference, you must set up a number sequence and associate it with the reference.</span></span> <span data-ttu-id="0869f-107">Soovitame numbriseeriate häälestamiseks kasutada lehti jaotises **Organisatsiooni haldus**.</span><span class="sxs-lookup"><span data-stu-id="0869f-107">We recommend that you use the pages in **Organization administration** to set up number sequences.</span></span> <span data-ttu-id="0869f-108">Kui moodulipõhised sätted on nõutavad, saate mooduli parameetrite lehega määrata mooduli viidete numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="0869f-108">If module-specific settings are required, you can use the parameters page in a module to specify number sequences for the references in that module.</span></span> <span data-ttu-id="0869f-109">Näiteks jaotises **Müügireskontro** ja **Ostureskontro** saate häälestada numbriseeriate grupid, et eraldada numbriseeriad konkreetsetele klientidele või hankijatele.</span><span class="sxs-lookup"><span data-stu-id="0869f-109">For example, in **Accounts receivable** and **Accounts payable**, you can set up number sequence groups to allocate specific number sequences to specific customers or vendors.</span></span> 

<span data-ttu-id="0869f-110">Kui häälestate numbriseeria, tuleb teil määrata ulatus, mis määratleb, milline organisatsioon numbriseeriat kasutab.</span><span class="sxs-lookup"><span data-stu-id="0869f-110">When you set up a number sequence, you must specify a scope, which defines which organization uses the number sequence.</span></span> <span data-ttu-id="0869f-111">Ulatus võib olla **Jagatud**, **Ettevõte**, **Juriidiline isik** või **Tootmisüksus**.</span><span class="sxs-lookup"><span data-stu-id="0869f-111">The scope can be **Shared**, **Company**, **Legal entity**, or **Operating unit**.</span></span> <span data-ttu-id="0869f-112">Ulatused **Juriidiline isik** ja **Ettevõte** saab kombineerida atribuudiga **Rahanduskalendri periood** veelgi täpsemate numbriseeriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="0869f-112">**Legal entity** and **Company** scopes can be combined with **Fiscal calendar period** to create even more specific number sequences.</span></span> 

<span data-ttu-id="0869f-113">Numbriseeria vorming koosneb segmentidest.</span><span class="sxs-lookup"><span data-stu-id="0869f-113">Number sequence formats consist of segments.</span></span> <span data-ttu-id="0869f-114">Numbriseeriad, mille ulatus ei ole **Jagatud**, võivad sisaldada ulatusele vastavaid segmente.</span><span class="sxs-lookup"><span data-stu-id="0869f-114">Number sequences with a scope other than **Shared** can contain segments that correspond to the scope.</span></span> <span data-ttu-id="0869f-115">Näiteks numbriseeria, mille ulatus on **Juriidiline isik**, võib sisaldada juriidilise isiku segmenti.</span><span class="sxs-lookup"><span data-stu-id="0869f-115">For example, a number sequence with a scope of **Legal entity** can contain a legal entity segment.</span></span> <span data-ttu-id="0869f-116">Kui kaasate numbriseeria vormingus ulatuse segmendi, saate kirje numbri alusel määrata konkreetse kirje ulatuse.</span><span class="sxs-lookup"><span data-stu-id="0869f-116">By including a scope segment in the number sequence format, you can identify the scope of a particular record by looking at its number.</span></span> 

<span data-ttu-id="0869f-117">Peale ulatustele vastavate segmentide võivad numbriseeriate vormingud sisaldada segmente tüübiga **Konstantne** ja **Tähe- ja numbrimärkidest koosnevad segmendid**.</span><span class="sxs-lookup"><span data-stu-id="0869f-117">In addition to segments that correspond to scopes, number sequence formats can contain **Constant** and **Alphanumeric segments**.</span></span> <span data-ttu-id="0869f-118">Segment **Konstantne** sisaldab tähtede, numbrite või sümbolite muutumatut kogumit.</span><span class="sxs-lookup"><span data-stu-id="0869f-118">A **Constant** segment contains a set of letters, numbers, or symbols that does not change.</span></span> <span data-ttu-id="0869f-119">**Tähe- ja numbrimärkidest** koosnev segment sisaldab tähtede või numbrite kogumit, mis suureneb iga kord, kui numbrit kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="0869f-119">An **Alphanumeric** segment contains a set of letters or numbers that increment every time that a number is used.</span></span> <span data-ttu-id="0869f-120">Kasvavate numbrite tähistamiseks kasutage numbriosundit (\#), kasvavate tähtede jaoks ampersandi.</span><span class="sxs-lookup"><span data-stu-id="0869f-120">Use a number sign (\#) to represent incrementing numbers and an ampersand (&) to represent incrementing letters.</span></span> <span data-ttu-id="0869f-121">Näiteks vorming \#\#\#\#\#\_2017 loob seeria 00001\_2017, 00002\_2017 jne.</span><span class="sxs-lookup"><span data-stu-id="0869f-121">For example, the format \#\#\#\#\#\_2017 creates the sequence 00001\_2017, 00002\_2017, and so on.</span></span>

<a name="number-sequence-examples"></a><span data-ttu-id="0869f-122">Numbriseeriate näidised</span><span class="sxs-lookup"><span data-stu-id="0869f-122">Number sequence examples</span></span>
------------------------

<span data-ttu-id="0869f-123">Järgmised näited selgitavad, kuidas kasutada segmente numbriseeriate vormingute loomiseks.</span><span class="sxs-lookup"><span data-stu-id="0869f-123">The following examples show how to use segments to create number sequence formats.</span></span> <span data-ttu-id="0869f-124">Täpsemalt kajastavad näited ulatuse segmentide kasutamise mõju.</span><span class="sxs-lookup"><span data-stu-id="0869f-124">In particular, the examples demonstrate the effects of using scope segments.</span></span>

### <a name="expense-report-numbers"></a><span data-ttu-id="0869f-125">Kuluaruande numbrid</span><span class="sxs-lookup"><span data-stu-id="0869f-125">Expense report numbers</span></span>

<span data-ttu-id="0869f-126">Järgmises näites on kuluaruande numbrid häälestatud juriidilise isiku jaoks, mis kannab nime **CS**.</span><span class="sxs-lookup"><span data-stu-id="0869f-126">In the following example, expense report numbers are set up for the legal entity that is titled **CS**.</span></span> 

- <span data-ttu-id="0869f-127">**Ala:** Reisimine ja kulud</span><span class="sxs-lookup"><span data-stu-id="0869f-127">**Area:** Travel and expense</span></span> 
- <span data-ttu-id="0869f-128">**Viide:** kuluaruande number</span><span class="sxs-lookup"><span data-stu-id="0869f-128">**Reference:** Expense report number</span></span> 
- <span data-ttu-id="0869f-129">**Ulatus:** juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="0869f-129">**Scope:** Legal entity</span></span> 
- <span data-ttu-id="0869f-130">**Juriidiline isik:** CS</span><span class="sxs-lookup"><span data-stu-id="0869f-130">**Legal entity:** CS</span></span>

| <span data-ttu-id="0869f-131">Segmendid</span><span class="sxs-lookup"><span data-stu-id="0869f-131">Segments</span></span>  | <span data-ttu-id="0869f-132">Segmendi tüüp</span><span class="sxs-lookup"><span data-stu-id="0869f-132">Segment type</span></span> | <span data-ttu-id="0869f-133">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0869f-133">Value</span></span>     |
|-----------|--------------|-----------|
| <span data-ttu-id="0869f-134">1. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-134">Segment 1</span></span> | <span data-ttu-id="0869f-135">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="0869f-135">Legal entity</span></span> | <span data-ttu-id="0869f-136">CS</span><span class="sxs-lookup"><span data-stu-id="0869f-136">CS</span></span>        |
| <span data-ttu-id="0869f-137">2. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-137">Segment 2</span></span> | <span data-ttu-id="0869f-138">Konstant</span><span class="sxs-lookup"><span data-stu-id="0869f-138">Constant</span></span>     | <span data-ttu-id="0869f-139">-EXPENSE-</span><span class="sxs-lookup"><span data-stu-id="0869f-139">-EXPENSE-</span></span> |
| <span data-ttu-id="0869f-140">3. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-140">Segment 3</span></span> | <span data-ttu-id="0869f-141">Tärk</span><span class="sxs-lookup"><span data-stu-id="0869f-141">Alphanumeric</span></span> | \#\#\#\#  |

<span data-ttu-id="0869f-142">**Vormindatud numbri näide**: CS-EXPENSE-0039</span><span class="sxs-lookup"><span data-stu-id="0869f-142">**Example of formatted number**: CS-EXPENSE-0039</span></span> 

<span data-ttu-id="0869f-143">Saate häälestada sarnased numbriseeriavormingud muude juriidiliste isikute jaoks.</span><span class="sxs-lookup"><span data-stu-id="0869f-143">You can set up a similar number sequence format for other legal entities.</span></span> <span data-ttu-id="0869f-144">Näiteks kui muudate juriidilise isiku **RW** puhul ainult juriidilise isiku segmendi väärtust, on vormindatud number RW-EXPENSE-0039.</span><span class="sxs-lookup"><span data-stu-id="0869f-144">For example, for a legal entity that is named **RW**, if you change only the value of the legal entity segment, the formatted number is RW-EXPENSE-0039.</span></span> <span data-ttu-id="0869f-145">Samuti saate muuta tervet numbriseeriavormingut muude juriidiliste isikute jaoks.</span><span class="sxs-lookup"><span data-stu-id="0869f-145">You can also change the whole number sequence format for other legal entities.</span></span> <span data-ttu-id="0869f-146">Näiteks saate välistada juriidilise isiku ulatuse segmendi, et luua vormindatud number, näiteks Exp-0001.</span><span class="sxs-lookup"><span data-stu-id="0869f-146">For example, you can omit the legal entity scope segment to create a formatted number such as Exp-0001.</span></span>

### <a name="sales-order-numbers"></a><span data-ttu-id="0869f-147">Müügitellimuste numbrid</span><span class="sxs-lookup"><span data-stu-id="0869f-147">Sales order numbers</span></span>

<span data-ttu-id="0869f-148">Järgmises näites on müügitellimuse numbrid häälestatud ettevõttele, mille ID on **CEU**.</span><span class="sxs-lookup"><span data-stu-id="0869f-148">In the following example, sales order numbers are set up for the company ID **CEU**.</span></span> 

- <span data-ttu-id="0869f-149">**Ala:** müük</span><span class="sxs-lookup"><span data-stu-id="0869f-149">**Area:** Sales</span></span> 
- <span data-ttu-id="0869f-150">**Viide:** müügitellimus</span><span class="sxs-lookup"><span data-stu-id="0869f-150">**Reference:** Sales order</span></span> 
- <span data-ttu-id="0869f-151">**Ulatus:** ettevõte</span><span class="sxs-lookup"><span data-stu-id="0869f-151">**Scope:** Company</span></span> 
- <span data-ttu-id="0869f-152">**Ettevõte:** CEU</span><span class="sxs-lookup"><span data-stu-id="0869f-152">**Company:** CEU</span></span>

| <span data-ttu-id="0869f-153">Segmendid</span><span class="sxs-lookup"><span data-stu-id="0869f-153">Segments</span></span>  | <span data-ttu-id="0869f-154">Segmendi tüüp</span><span class="sxs-lookup"><span data-stu-id="0869f-154">Segment type</span></span> | <span data-ttu-id="0869f-155">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0869f-155">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="0869f-156">1. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-156">Segment 1</span></span> | <span data-ttu-id="0869f-157">Konstant</span><span class="sxs-lookup"><span data-stu-id="0869f-157">Constant</span></span>     | <span data-ttu-id="0869f-158">SO-</span><span class="sxs-lookup"><span data-stu-id="0869f-158">SO-</span></span>      |
| <span data-ttu-id="0869f-159">2. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-159">Segment 2</span></span> | <span data-ttu-id="0869f-160">Tärk</span><span class="sxs-lookup"><span data-stu-id="0869f-160">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="0869f-161">**Vormindatud numbri näide**: SO-0029</span><span class="sxs-lookup"><span data-stu-id="0869f-161">**Example of formatted number**: SO-0029</span></span> 

<span data-ttu-id="0869f-162">Kuigi vorming ei hõlma ulatuse segmenti, alustatakse nummerdamist uuesti iga ettevõtte ID puhul.</span><span class="sxs-lookup"><span data-stu-id="0869f-162">Even though a scope segment is not included in the format, numbering restarts for each company ID.</span></span> <span data-ttu-id="0869f-163">Kui kasutate sama vormingut kõikide ettevõtete ID-de puhul, kasutatakse iga ettevõtte jaoks samu numbreid.</span><span class="sxs-lookup"><span data-stu-id="0869f-163">If you use the same format for all company IDs, the same numbers are used in each company.</span></span> <span data-ttu-id="0869f-164">Näiteks müügitellimuse numbrit SO-0029 kasutatakse iga ettevõtte puhul.</span><span class="sxs-lookup"><span data-stu-id="0869f-164">For example, sales order number SO-0029 is used in each company.</span></span> <span data-ttu-id="0869f-165">Samuti saate muuta tervet numbriseeriavormingut muude ettevõtete ID-de jaoks.</span><span class="sxs-lookup"><span data-stu-id="0869f-165">You can also change the whole number sequence format for other company IDs.</span></span>

### <a name="purchase-requisition-numbers"></a><span data-ttu-id="0869f-166">Ostutaotluse numbrid</span><span class="sxs-lookup"><span data-stu-id="0869f-166">Purchase requisition numbers</span></span>

<span data-ttu-id="0869f-167">Järgmises näites kehtivad ostutaotluse numbrid kogu organisatsioonis.</span><span class="sxs-lookup"><span data-stu-id="0869f-167">In the following example, purchase requisition numbers are organization-wide.</span></span> 

- <span data-ttu-id="0869f-168">**Ala:** ost</span><span class="sxs-lookup"><span data-stu-id="0869f-168">**Area:** Purchase</span></span> 
- <span data-ttu-id="0869f-169">**Viide:** ostutaotlus</span><span class="sxs-lookup"><span data-stu-id="0869f-169">**Reference:** Purchase requisition</span></span> 
- <span data-ttu-id="0869f-170">**Ulatus:** ühiskasutatud</span><span class="sxs-lookup"><span data-stu-id="0869f-170">**Scope:** Shared</span></span>

| <span data-ttu-id="0869f-171">Segmendid</span><span class="sxs-lookup"><span data-stu-id="0869f-171">Segments</span></span>  | <span data-ttu-id="0869f-172">Segmendi tüüp</span><span class="sxs-lookup"><span data-stu-id="0869f-172">Segment type</span></span> | <span data-ttu-id="0869f-173">Väärtus</span><span class="sxs-lookup"><span data-stu-id="0869f-173">Value</span></span>    |
|-----------|--------------|----------|
| <span data-ttu-id="0869f-174">1. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-174">Segment 1</span></span> | <span data-ttu-id="0869f-175">Konstant</span><span class="sxs-lookup"><span data-stu-id="0869f-175">Constant</span></span>     | <span data-ttu-id="0869f-176">Req</span><span class="sxs-lookup"><span data-stu-id="0869f-176">Req</span></span>      |
| <span data-ttu-id="0869f-177">2. segment</span><span class="sxs-lookup"><span data-stu-id="0869f-177">Segment 2</span></span> | <span data-ttu-id="0869f-178">Tärk</span><span class="sxs-lookup"><span data-stu-id="0869f-178">Alphanumeric</span></span> | \#\#\#\# |

<span data-ttu-id="0869f-179">**Vormindatud numbri näide**: Req0052</span><span class="sxs-lookup"><span data-stu-id="0869f-179">**Example of formatted number**: Req0052</span></span> 

<span data-ttu-id="0869f-180">Kula ulatus on **Ühine**, kasutatakse numbriseeria vormingut kogu organisatsioonis.</span><span class="sxs-lookup"><span data-stu-id="0869f-180">Because the scope is **Shared**, the number sequence format is used across the organization.</span></span> <span data-ttu-id="0869f-181">Te ei saa organisatsiooni erinevate osade jaoks häälestada erinevaid numbriseeria vorminguid.</span><span class="sxs-lookup"><span data-stu-id="0869f-181">You cannot set up different number sequence formats for different parts of the organization.</span></span> 

<a name="performance-considerations-for-number-sequences"></a><span data-ttu-id="0869f-182">Numbriseeriate jõudluse kaalutlused</span><span class="sxs-lookup"><span data-stu-id="0869f-182">Performance considerations for number sequences</span></span>
-----------------------------------------------

<span data-ttu-id="0869f-183">Enne numbriseeriate häälestamist võtke arvesse järgmist teavet selle kohta, kuidas numbriseeriate konfiguratsioon võib mõjutada süsteemi jõudlust.</span><span class="sxs-lookup"><span data-stu-id="0869f-183">Consider the following information about how the configuration of number sequences can affect system performance before you set up number sequences.</span></span>

### <a name="continuous-and-non-continuous-number-sequences"></a><span data-ttu-id="0869f-184">Pidevad ja mittepidevad numbriseeriad</span><span class="sxs-lookup"><span data-stu-id="0869f-184">Continuous and non-continuous number sequences</span></span>

<span data-ttu-id="0869f-185">Numbriseeriad võivad olla pidevad ja mittepidevad.</span><span class="sxs-lookup"><span data-stu-id="0869f-185">Number sequences can be continuous or non-continuous.</span></span> <span data-ttu-id="0869f-186">Pidev numbriseeria ei jäta vahele ühtki numbrit, kuid numbreid ei saa kasutada järjest.</span><span class="sxs-lookup"><span data-stu-id="0869f-186">A continuous number sequence does not skip any numbers, but numbers may not be used sequentially.</span></span> <span data-ttu-id="0869f-187">Mittepideva numbriseeria numbreid kasutatakse järjest, kuid numbriseeria võib numbreid vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="0869f-187">Numbers from a non-continuous number sequence are used sequentially, but the number sequence may skip numbers.</span></span> <span data-ttu-id="0869f-188">Näiteks kui kasutaja tühistab kande, luuakse number, kuid seda ei kasutata.</span><span class="sxs-lookup"><span data-stu-id="0869f-188">For example, if a user cancels a transaction, a number is generated, but not used.</span></span> <span data-ttu-id="0869f-189">Pidevas numbriseerias kasutatakse numbrit hiljem.</span><span class="sxs-lookup"><span data-stu-id="0869f-189">In a continuous number sequence, that number is recycled later.</span></span> <span data-ttu-id="0869f-190">Mittepidevas numbriseerias ei kasutata numbrit.</span><span class="sxs-lookup"><span data-stu-id="0869f-190">In a non-continuous number sequence, the number is not used.</span></span> 

<span data-ttu-id="0869f-191">Pidevad numbriseeriad on tavaliselt nõutavad väliste dokumentide, näiteks ostutellimuste, müügitellimuste ja arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="0869f-191">Continuous number sequences are typically required for external documents, such as purchase orders, sales orders, and invoices.</span></span> <span data-ttu-id="0869f-192">Pidevad numbriseeriad võivad aga süsteemi reageerimist aeglustada, kuna süsteem peab taotlema numbrit andmebaasist iga kord, kui luuakse uus dokument või kirje.</span><span class="sxs-lookup"><span data-stu-id="0869f-192">However, continuous number sequences can adversely affect system response times because the system must request a number from the database every time that a new document or record is created.</span></span> 

<span data-ttu-id="0869f-193">Kui kasutate mittepidevat numbriseeriat, saate lubada valiku **Eelnev eraldamine** kiirkaardil **Jõudlus** lehel **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="0869f-193">If you use a non-continuous number sequence, you can enable **Preallocation** on the **Performance** FastTab of the **Number sequences** page.</span></span> <span data-ttu-id="0869f-194">Kui määrate eelnevalt eraldatavate numbrite koguse, valib süsteem numbrid ja talletab need mällu.</span><span class="sxs-lookup"><span data-stu-id="0869f-194">When you specify a quantity of numbers to preallocate, the system selects those numbers and stores them in memory.</span></span> <span data-ttu-id="0869f-195">Uusi numbreid taotletakse andmebaasist vaid pärast eelnevalt eraldatud koguse kasutamist.</span><span class="sxs-lookup"><span data-stu-id="0869f-195">New numbers are requested from the database only after the preallocated quantity has been used.</span></span> 

<span data-ttu-id="0869f-196">Kui te ei pea eeskirjade kohaselt kasutama pidevaid numbriseeriaid, soovitame parema jõudluse huvides kasutada mittepidevaid numbriseeriaid.</span><span class="sxs-lookup"><span data-stu-id="0869f-196">Unless there is a regulatory requirement that you use continuous number sequences, we recommend that you use non-continuous number sequences for better performance.</span></span>

### <a name="automatic-cleanup-of-number-sequences"></a><span data-ttu-id="0869f-197">Numbriseeriate automaatne puhastamine</span><span class="sxs-lookup"><span data-stu-id="0869f-197">Automatic cleanup of number sequences</span></span>

<span data-ttu-id="0869f-198">Toitekatkestuse, rakenduse tõrke või muu ootamatu vea puhul ei saa süsteem pidevate numbriseeriate numbreid automaatselt taaskasutada.</span><span class="sxs-lookup"><span data-stu-id="0869f-198">In case of a power failure, an application error, or other unexpected failure, the system cannot recycle numbers automatically for continuous number sequences.</span></span> <span data-ttu-id="0869f-199">Kaotsiläinud numbrite taastamiseks saate puhastamisprotsessi käsitsi või automaatselt käitada.</span><span class="sxs-lookup"><span data-stu-id="0869f-199">You can run the cleanup process manually or automatically to recover the lost numbers.</span></span> 

<span data-ttu-id="0869f-200">Puhastamisprotsessi plaanimisel võtke kindlasti arvesse serveri koormust.</span><span class="sxs-lookup"><span data-stu-id="0869f-200">Carefully consider server usage when you plan the cleanup process.</span></span> <span data-ttu-id="0869f-201">Soovitame puhastamist teha pakett-tööna tipptundidevälisel ajal.</span><span class="sxs-lookup"><span data-stu-id="0869f-201">We recommend that you perform the cleanup as a batch job during non-peak hours.</span></span>






