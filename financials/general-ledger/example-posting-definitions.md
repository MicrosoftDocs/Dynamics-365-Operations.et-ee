---
title: Sisestamisdefinitsioonid
description: "Selles artiklis on näited selle kohta, kuidas ostutellimuse pandiõiguse ja eelarve jaotamise puhul sisestamisdefinitsioone kasutatakse."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 004f3f24ec410d9f0e7d1e7264ec2730b9467410
ms.contentlocale: et-ee
ms.lasthandoff: 06/29/2017


---

# <a name="posting-definition-examples"></a><span data-ttu-id="e1b1f-103">Sisestamisdefinitsioonide näited</span><span class="sxs-lookup"><span data-stu-id="e1b1f-103">Posting definition examples</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e1b1f-104">Selles artiklis on näited selle kohta, kuidas ostutellimuse pandiõiguse ja eelarve jaotamise puhul sisestamisdefinitsioone kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="e1b1f-105">Enne selle teema lugemist peaksite olema kursis sisestamisdefinitsioonide ja kande sisestamisdefinitsioonidega.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="e1b1f-106">Lisateavet vaadake teemast [Sisestamisdefinitsioonid](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e1b1f-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="e1b1f-107">Lehel **Sisestamisdefinitsioonid** saate seadistada järgmised näited.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="e1b1f-108">Iga näide sisaldab järgmisi jaotisi.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="e1b1f-109">Sisestamisdefinitsioon – vastendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="e1b1f-110">Sisestamisdefinitsioon – loodud kanded</span><span class="sxs-lookup"><span data-stu-id="e1b1f-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="e1b1f-111">Kontode, dimensiooniväärtuste ja summadega kanded</span><span class="sxs-lookup"><span data-stu-id="e1b1f-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="e1b1f-112">Sisestamisdefinitsioonist loodud pearaamatukirjed</span><span class="sxs-lookup"><span data-stu-id="e1b1f-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="e1b1f-113">Kui sisestamisdefinitsiooni paanil **Vastendamiskriteeriumid** olevate kontode ja dimensiooniväärtuste ning kande kontode ja dimensiooniväärtuste vahel ilmneb vastendus, luuakse pearaamatukirjed sisestamisdefinitsiooni paani **Loodud kanded** alusel.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="e1b1f-114">Sisestamisdefinitsiooni saab seostada konkreetse kande tüübiga lehel **Kande sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="e1b1f-115">Pärast sisestamisdefinitsiooni seostamist kande tüübiga ja valiku **Kasuta sisestamisdefinitsioone** tegemist lehel **Pearaamatu parameetrid** peavad kõik valitud kande tüübiga kanded kasutama sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="e1b1f-116">Näide: ostutellimuse pandiõigus</span><span class="sxs-lookup"><span data-stu-id="e1b1f-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="e1b1f-117">Kui lubate pandiõiguse protsessi, valides lehel **Pearaamatu parameetrid** suvandi **Luba pandiõiguse protsess**, tuleb pandiõiguste pearaamatusse kandmiseks kasutada kõigi reserveeritavate kontode puhul sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="e1b1f-118">Enamasti reserveeritakse bilansis kõik kulukontod.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="e1b1f-119">Pandiõiguste sisestamisdefinitsioonid seadistatakse mooduli **Ostmine** jaoks lehel **Sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="e1b1f-120">Seejärel saate lehe **Kande sisestamisdefinitsioonid** alal **Ostmine** valida kandetüübi **Ostutellimus**, et seostada sisestamisdefinitsiooni ostutellimustega.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="e1b1f-121">Kõik ostutellimuse pandiõiguste pearaamatukanded peavad olema tasakaalus (st deebetid peavad võrduma kreedititega) kande igas kordumatus dimensioonis.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="e1b1f-122">Sisestamisdefinitsioon – vastendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="e1b1f-123">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="e1b1f-123">Account structure</span></span>       | <span data-ttu-id="e1b1f-124">Kattuva konto number</span><span class="sxs-lookup"><span data-stu-id="e1b1f-124">Match account number</span></span> | <span data-ttu-id="e1b1f-125">Prioriteet</span><span class="sxs-lookup"><span data-stu-id="e1b1f-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="e1b1f-126">Konto struktuur – kasum ja kahjum</span><span class="sxs-lookup"><span data-stu-id="e1b1f-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="e1b1f-127">1</span><span class="sxs-lookup"><span data-stu-id="e1b1f-127">1</span></span>        |

<span data-ttu-id="e1b1f-128">* Tühi väärtus väljal **Kattuva konto number** tähendab, et kõik kattuvad kontod määratletud kontostruktuuris on vastendusreegli osa.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-128">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="e1b1f-129">Sisestamisdefinitsioon – loodud kanded</span><span class="sxs-lookup"><span data-stu-id="e1b1f-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="e1b1f-130">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="e1b1f-130">Account structure</span></span> | <span data-ttu-id="e1b1f-131">Loodud konto number</span><span class="sxs-lookup"><span data-stu-id="e1b1f-131">Generated account number</span></span>                    | <span data-ttu-id="e1b1f-132">Loodud deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="e1b1f-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="e1b1f-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="e1b1f-133">Balance</span></span>           | <span data-ttu-id="e1b1f-134">300143 – (pandiõiguse konto)</span><span class="sxs-lookup"><span data-stu-id="e1b1f-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="e1b1f-135">Sama</span><span class="sxs-lookup"><span data-stu-id="e1b1f-135">Same</span></span>                   |
| <span data-ttu-id="e1b1f-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="e1b1f-136">Balance</span></span>           | <span data-ttu-id="e1b1f-137">300144 – (pandiõiguse konto reserveerimine)</span><span class="sxs-lookup"><span data-stu-id="e1b1f-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="e1b1f-138">Tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="e1b1f-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="e1b1f-139">Kontode, dimensiooniväärtuste ja summadega kanded</span><span class="sxs-lookup"><span data-stu-id="e1b1f-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="e1b1f-140">Kontod ja dimensiooniväärtused tulevad kas ostutellimuse reale sisestatud arvestuse jaotustelt või hankijate, kaupade, kategooriate ja dimensioonimallide vaikesätete põhjal automaatselt loodud kontodest ja dimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="e1b1f-141">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-141">Account + dimensions</span></span>           | <span data-ttu-id="e1b1f-142">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="e1b1f-142">Debit</span></span>  | <span data-ttu-id="e1b1f-143">Krediit</span><span class="sxs-lookup"><span data-stu-id="e1b1f-143">Credit</span></span> | <span data-ttu-id="e1b1f-144">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="e1b1f-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="e1b1f-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="e1b1f-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="e1b1f-146">250,00</span><span class="sxs-lookup"><span data-stu-id="e1b1f-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="e1b1f-147">Sisestamisdefinitsioonist loodud pearaamatukirjed</span><span class="sxs-lookup"><span data-stu-id="e1b1f-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="e1b1f-148">Genereeritud pearaamatukirjed luuakse pandiõiguste registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="e1b1f-149">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-149">Account + dimensions</span></span>           | <span data-ttu-id="e1b1f-150">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="e1b1f-150">Debit</span></span>  | <span data-ttu-id="e1b1f-151">Krediit</span><span class="sxs-lookup"><span data-stu-id="e1b1f-151">Credit</span></span> | <span data-ttu-id="e1b1f-152">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="e1b1f-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="e1b1f-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="e1b1f-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="e1b1f-154">250,00</span><span class="sxs-lookup"><span data-stu-id="e1b1f-154">250.00</span></span> |        |         |
| <span data-ttu-id="e1b1f-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="e1b1f-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="e1b1f-156">250,00</span><span class="sxs-lookup"><span data-stu-id="e1b1f-156">250.00</span></span> |         |

<span data-ttu-id="e1b1f-157">Selles näites vastab iga konto, mis on osa jaotisest Konto struktuur – kasum ja kahjum, sisestamisdefinitsiooni kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="e1b1f-158">Üksuse 606500-OU\_1-OU\_3566-Training hindamisel luuakse seega genereeritud kirjed kontode kohta, mis on määratletud sisestamisdefinitsiooni paanil **Loodud kirjed**.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="e1b1f-159">Näide: eelarveeraldised</span><span class="sxs-lookup"><span data-stu-id="e1b1f-159">Example: Budget appropriations</span></span>
<span data-ttu-id="e1b1f-160">Kui lubate eelarveeraldise, valides lehel **Pearaamatu parameetrid** suvandi **Luba eelarveeraldis**, tuleb eelarve registrikirjete registreerimiseks pearaamatusse kasutada sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="e1b1f-161">Kui eelarve juhtimise konfiguratsioon on aktiivne ja sisse lülitatud, saab sisestamisdefinitsioone ja kande sisestamisdefinitsioone kasutada eraldiste, paranduste, ülekannete, projektide, põhivarade ning tarne- ja nõudlusprognooside kirjete pearaamatusse registreerimise toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="e1b1f-162">Selleks et seadistada sisestamisdefinitsioon eelarve registrikannete jaoks, mille eelarvetüüp on **Algne eelarve** ja mille puhul on eraldised lubatud, valige lehel **Sisestamisdefinitsioonid** moodul **Eelarve**.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="e1b1f-163">Seejärel saate lehe **Kande sisestamisdefinitsioonid** alal **Eelarve** kasutada eelarvekoode, et seostada sisestamisdefinitsioonid eelarve registrikannetega, mille eelarvetüüp on **Algne eelarve**.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="e1b1f-164">Kui eelarveeraldised ja sisestamisdefinitsioonid on lubatud, registreeritakse eelarve registrikirjed eelarve juhtimisse ja pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="e1b1f-165">Sisestamisdefinitsioon – vastendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="e1b1f-166">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="e1b1f-166">Account structure</span></span>       | <span data-ttu-id="e1b1f-167">Kattuva konto number</span><span class="sxs-lookup"><span data-stu-id="e1b1f-167">Match account number</span></span> | <span data-ttu-id="e1b1f-168">Prioriteet</span><span class="sxs-lookup"><span data-stu-id="e1b1f-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="e1b1f-169">Konto struktuur – kasum ja kahjum</span><span class="sxs-lookup"><span data-stu-id="e1b1f-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="e1b1f-170">1</span><span class="sxs-lookup"><span data-stu-id="e1b1f-170">1</span></span>        |

<span data-ttu-id="e1b1f-171">* Tühi väärtus väljal **Kattuva konto number** tähendab, et kõik kattuvad kontod määratletud kontostruktuuris on vastendusreegli osa.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-171">*A blank value in the **Match account number** field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="e1b1f-172">Sisestamisdefinitsioon – loodud kanded</span><span class="sxs-lookup"><span data-stu-id="e1b1f-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="e1b1f-173">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="e1b1f-173">Account structure</span></span> | <span data-ttu-id="e1b1f-174">Loodud konto number</span><span class="sxs-lookup"><span data-stu-id="e1b1f-174">Generated account number</span></span>              | <span data-ttu-id="e1b1f-175">Loodud deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="e1b1f-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="e1b1f-176">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="e1b1f-176">Account structure</span></span> | <span data-ttu-id="e1b1f-177">300145 – (eeldatava tulu konto)</span><span class="sxs-lookup"><span data-stu-id="e1b1f-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="e1b1f-178">Sama</span><span class="sxs-lookup"><span data-stu-id="e1b1f-178">Same</span></span>                   |
| <span data-ttu-id="e1b1f-179">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="e1b1f-179">Account structure</span></span> | <span data-ttu-id="e1b1f-180">300146 – (eraldisekonto)</span><span class="sxs-lookup"><span data-stu-id="e1b1f-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="e1b1f-181">Tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="e1b1f-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="e1b1f-182">Kontode, dimensiooniväärtuste ja summadega kanded</span><span class="sxs-lookup"><span data-stu-id="e1b1f-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="e1b1f-183">Saate sisestada kontod, dimensiooniväärtused ja eelarve konto kirje summad lehel **Eelarve registrikirje**.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="e1b1f-184">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-184">Account + dimensions</span></span>           | <span data-ttu-id="e1b1f-185">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="e1b1f-185">Debit</span></span> | <span data-ttu-id="e1b1f-186">Krediit</span><span class="sxs-lookup"><span data-stu-id="e1b1f-186">Credit</span></span> | <span data-ttu-id="e1b1f-187">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="e1b1f-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="e1b1f-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="e1b1f-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="e1b1f-189">250,00</span><span class="sxs-lookup"><span data-stu-id="e1b1f-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="e1b1f-190">Sisestamisdefinitsioonist loodud pearaamatukirjed</span><span class="sxs-lookup"><span data-stu-id="e1b1f-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="e1b1f-191">Genereeritud pearaamatukirjed luuakse algse eelarve registreerimiseks igas dimensioonis.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="e1b1f-192">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="e1b1f-192">Account + dimensions</span></span>           | <span data-ttu-id="e1b1f-193">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="e1b1f-193">Debit</span></span>  | <span data-ttu-id="e1b1f-194">Krediit</span><span class="sxs-lookup"><span data-stu-id="e1b1f-194">Credit</span></span> | <span data-ttu-id="e1b1f-195">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="e1b1f-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="e1b1f-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="e1b1f-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="e1b1f-197">250,00</span><span class="sxs-lookup"><span data-stu-id="e1b1f-197">250.00</span></span> |         |
| <span data-ttu-id="e1b1f-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="e1b1f-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="e1b1f-199">250,00</span><span class="sxs-lookup"><span data-stu-id="e1b1f-199">250.00</span></span> |        |         |

<span data-ttu-id="e1b1f-200">Selles näites vastab iga konto, mis on osa jaotisest Konto struktuur – kasum ja kahjum, sisestamisdefinitsiooni kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="e1b1f-201">Üksuse 606400-OU\_1-OU\_3566-Training hindamisel luuakse seega genereeritud pearaamatukirjed.</span><span class="sxs-lookup"><span data-stu-id="e1b1f-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>






