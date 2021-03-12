---
title: Sisestamisdefinitsiooni näited
description: Selles artiklis on näited selle kohta, kuidas ostutellimuse pandiõiguse ja eelarve jaotamise puhul sisestamisdefinitsioone kasutatakse.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JournalizingDefinition, JournalizingDefinitionTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 15772
ms.assetid: 3864e4da-853f-403d-b906-79631d80b363
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 751be602b701ac7a5b593404bf655e1a9852f863
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990485"
---
# <a name="posting-definition-examples"></a><span data-ttu-id="7201d-103">Sisestamisdefinitsioonide näited</span><span class="sxs-lookup"><span data-stu-id="7201d-103">Posting definition examples</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7201d-104">Selles artiklis on näited selle kohta, kuidas ostutellimuse pandiõiguse ja eelarve jaotamise puhul sisestamisdefinitsioone kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="7201d-104">This article provides examples that show how posting definitions are used for purchase order encumbrances and budget appropriations.</span></span>

<span data-ttu-id="7201d-105">Enne selle teema lugemist peaksite olema kursis sisestamisdefinitsioonide ja kande sisestamisdefinitsioonidega.</span><span class="sxs-lookup"><span data-stu-id="7201d-105">Before you read this topic, you should be familiar with posting definitions and transaction posting definitions.</span></span> <span data-ttu-id="7201d-106">Lisateavet vaadake teemast [Sisestamisdefinitsioonid](posting-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="7201d-106">For information, see [Posting definitions](posting-definitions.md).</span></span> <span data-ttu-id="7201d-107">Lehel **Sisestamisdefinitsioonid** saate seadistada järgmised näited.</span><span class="sxs-lookup"><span data-stu-id="7201d-107">The following examples can be set up on the **Posting definitions** page.</span></span> <span data-ttu-id="7201d-108">Iga näide sisaldab järgmisi jaotisi.</span><span class="sxs-lookup"><span data-stu-id="7201d-108">Each example contains these sections:</span></span>

-   <span data-ttu-id="7201d-109">Sisestamisdefinitsioon – vastendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="7201d-109">Posting definition – Match criteria</span></span>
-   <span data-ttu-id="7201d-110">Sisestamisdefinitsioon – loodud kanded</span><span class="sxs-lookup"><span data-stu-id="7201d-110">Posting definition – Generated entries</span></span>
-   <span data-ttu-id="7201d-111">Kontode, dimensiooniväärtuste ja summadega kanded</span><span class="sxs-lookup"><span data-stu-id="7201d-111">Transactions with the accounts, dimension values, and amounts</span></span>
-   <span data-ttu-id="7201d-112">Sisestamisdefinitsioonist loodud pearaamatukirjed</span><span class="sxs-lookup"><span data-stu-id="7201d-112">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="7201d-113">Kui sisestamisdefinitsiooni paanil **Vastendamiskriteeriumid** olevate kontode ja dimensiooniväärtuste ning kande kontode ja dimensiooniväärtuste vahel ilmneb vastendus, luuakse pearaamatukirjed sisestamisdefinitsiooni paani **Loodud kanded** alusel.</span><span class="sxs-lookup"><span data-stu-id="7201d-113">When a match occurs between the accounts and dimension values in the **Match criteria** pane for the posting definition and the accounts and dimension values on the transaction, ledger entries are generated based on the **Generated entries** pane for the posting definition.</span></span> 
> [!NOTE]
> <span data-ttu-id="7201d-114">Sisestamisdefinitsiooni saab seostada konkreetse kande tüübiga lehel **Kande sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="7201d-114">To associate a posting definition with a specific transaction type, use the **Transaction posting definitions** page.</span></span> <span data-ttu-id="7201d-115">Pärast sisestamisdefinitsiooni seostamist kande tüübiga ja valiku **Kasuta sisestamisdefinitsioone** tegemist lehel **Pearaamatu parameetrid** peavad kõik valitud kande tüübiga kanded kasutama sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="7201d-115">After you associate a posting definition with a transaction type and select **Use posting definitions** on the **General ledger parameters** page, all transactions of the selected transaction type must use posting definitions.</span></span>

## <a name="example-purchase-order-encumbrances"></a><span data-ttu-id="7201d-116">Näide: ostutellimuse pandiõigus</span><span class="sxs-lookup"><span data-stu-id="7201d-116">Example: Purchase order encumbrances</span></span>
<span data-ttu-id="7201d-117">Kui lubate pandiõiguse protsessi, valides lehel **Pearaamatu parameetrid** suvandi **Luba pandiõiguse protsess**, tuleb pandiõiguste pearaamatusse kandmiseks kasutada kõigi reserveeritavate kontode puhul sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="7201d-117">When you enable encumbrance processing by selecting **Enable encumbrance process** on the **General ledger parameters** page, posting definitions must be used to record encumbrances to the general ledger for any accounts that should be reserved.</span></span> <span data-ttu-id="7201d-118">Enamasti reserveeritakse bilansis kõik kulukontod.</span><span class="sxs-lookup"><span data-stu-id="7201d-118">In most cases, all expense accounts are reserved on the balance sheet.</span></span> 

<span data-ttu-id="7201d-119">Pandiõiguste sisestamisdefinitsioonid seadistatakse mooduli **Ostmine** jaoks lehel **Sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="7201d-119">Posting definitions for encumbrances are set up for the **Purchasing** module on the **Posting definitions** page.</span></span> <span data-ttu-id="7201d-120">Seejärel saate lehe **Kande sisestamisdefinitsioonid** alal **Ostmine** valida kandetüübi **Ostutellimus**, et seostada sisestamisdefinitsiooni ostutellimustega.</span><span class="sxs-lookup"><span data-stu-id="7201d-120">Then, in the **Purchasing** area of the **Transaction posting definitions** page, you can select the **Purchase order** transaction type to associate the posting definition with purchase orders.</span></span> 

<span data-ttu-id="7201d-121">Kõik ostutellimuse pandiõiguste pearaamatukanded peavad olema tasakaalus (st deebetid peavad võrduma kreedititega) kande igas kordumatus dimensioonis.</span><span class="sxs-lookup"><span data-stu-id="7201d-121">All voucher transactions for purchase order encumbrances must balance (that is, debits must equal credits) in each unique dimension on a voucher.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="7201d-122">Sisestamisdefinitsioon – vastendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="7201d-122">Posting definition – Match criteria</span></span>

| <span data-ttu-id="7201d-123">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="7201d-123">Account structure</span></span>       | <span data-ttu-id="7201d-124">Kattuva konto number</span><span class="sxs-lookup"><span data-stu-id="7201d-124">Match account number</span></span> | <span data-ttu-id="7201d-125">Prioriteet </span><span class="sxs-lookup"><span data-stu-id="7201d-125">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="7201d-126">Konto struktuur – kasum ja kahjum</span><span class="sxs-lookup"><span data-stu-id="7201d-126">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="7201d-127">1</span><span class="sxs-lookup"><span data-stu-id="7201d-127">1</span></span>        |

<span data-ttu-id="7201d-128"><em>Tühi väärtus väljal \**Kattuva konto number</em>* tähendab, et kõik kattuvad kontod määratletud kontostruktuuris on vastendusreegli osa.</span><span class="sxs-lookup"><span data-stu-id="7201d-128"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="7201d-129">Sisestamisdefinitsioon – loodud kanded</span><span class="sxs-lookup"><span data-stu-id="7201d-129">Posting definition – Generated entries</span></span>

| <span data-ttu-id="7201d-130">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="7201d-130">Account structure</span></span> | <span data-ttu-id="7201d-131">Loodud konto number</span><span class="sxs-lookup"><span data-stu-id="7201d-131">Generated account number</span></span>                    | <span data-ttu-id="7201d-132">Loodud deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="7201d-132">Generated debit/credit</span></span> |
|-------------------|---------------------------------------------|------------------------|
| <span data-ttu-id="7201d-133">Saldo</span><span class="sxs-lookup"><span data-stu-id="7201d-133">Balance</span></span>           | <span data-ttu-id="7201d-134">300143 – (pandiõiguse konto)</span><span class="sxs-lookup"><span data-stu-id="7201d-134">300143 - -(Encumbrance account)</span></span>             | <span data-ttu-id="7201d-135">Sama</span><span class="sxs-lookup"><span data-stu-id="7201d-135">Same</span></span>                   |
| <span data-ttu-id="7201d-136">Saldo</span><span class="sxs-lookup"><span data-stu-id="7201d-136">Balance</span></span>           | <span data-ttu-id="7201d-137">300144 – (pandiõiguse konto reserveerimine)</span><span class="sxs-lookup"><span data-stu-id="7201d-137">300144 - -(Reserve for encumbrance account)</span></span> | <span data-ttu-id="7201d-138">Tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="7201d-138">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="7201d-139">Kontode, dimensiooniväärtuste ja summadega kanded</span><span class="sxs-lookup"><span data-stu-id="7201d-139">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="7201d-140">Kontod ja dimensiooniväärtused tulevad kas ostutellimuse reale sisestatud arvestuse jaotustelt või hankijate, kaupade, kategooriate ja dimensioonimallide vaikesätete põhjal automaatselt loodud kontodest ja dimensioonidest.</span><span class="sxs-lookup"><span data-stu-id="7201d-140">The accounts and dimension values come either from the accounting distributions that you enter for a purchase order line, or from the accounts and dimensions that are automatically generated based on the default settings for vendors, items, categories, and dimension templates.</span></span>

| <span data-ttu-id="7201d-141">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="7201d-141">Account + dimensions</span></span>           | <span data-ttu-id="7201d-142">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="7201d-142">Debit</span></span>  | <span data-ttu-id="7201d-143">Krediit</span><span class="sxs-lookup"><span data-stu-id="7201d-143">Credit</span></span> | <span data-ttu-id="7201d-144">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="7201d-144">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="7201d-145">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="7201d-145">606400-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="7201d-146">250,00</span><span class="sxs-lookup"><span data-stu-id="7201d-146">250.00</span></span> |        |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="7201d-147">Sisestamisdefinitsioonist loodud pearaamatukirjed</span><span class="sxs-lookup"><span data-stu-id="7201d-147">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="7201d-148">Genereeritud pearaamatukirjed luuakse pandiõiguste registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="7201d-148">Generated ledger entries are created to record the encumbrances.</span></span>

| <span data-ttu-id="7201d-149">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="7201d-149">Account + dimensions</span></span>           | <span data-ttu-id="7201d-150">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="7201d-150">Debit</span></span>  | <span data-ttu-id="7201d-151">Krediit</span><span class="sxs-lookup"><span data-stu-id="7201d-151">Credit</span></span> | <span data-ttu-id="7201d-152">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="7201d-152">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="7201d-153">300143-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="7201d-153">300143-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="7201d-154">250,00</span><span class="sxs-lookup"><span data-stu-id="7201d-154">250.00</span></span> |        |         |
| <span data-ttu-id="7201d-155">300144-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="7201d-155">300144-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="7201d-156">250,00</span><span class="sxs-lookup"><span data-stu-id="7201d-156">250.00</span></span> |         |

<span data-ttu-id="7201d-157">Selles näites vastab iga konto, mis on osa jaotisest Konto struktuur – kasum ja kahjum, sisestamisdefinitsiooni kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="7201d-157">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="7201d-158">Üksuse 606500-OU\_1-OU\_3566-Training hindamisel luuakse seega genereeritud kirjed kontode kohta, mis on määratletud sisestamisdefinitsiooni paanil **Loodud kirjed**.</span><span class="sxs-lookup"><span data-stu-id="7201d-158">Therefore, when 606500-OU\_1-OU\_3566-Training is evaluated, generated entries are created for the accounts that are defined in the **Generated entries** pane for the posting definition.</span></span>

## <a name="example-budget-appropriations"></a><span data-ttu-id="7201d-159">Näide: eelarveeraldised</span><span class="sxs-lookup"><span data-stu-id="7201d-159">Example: Budget appropriations</span></span>
<span data-ttu-id="7201d-160">Kui lubate eelarveeraldise, valides lehel **Pearaamatu parameetrid** suvandi **Luba eelarveeraldis**, tuleb eelarve registrikirjete registreerimiseks pearaamatusse kasutada sisestamisdefinitsioone.</span><span class="sxs-lookup"><span data-stu-id="7201d-160">When you enable budget appropriation by selecting **Enable budget appropriation** on the **General ledger parameters** page, posting definitions must be used to record budget register entries to the general ledger.</span></span> <span data-ttu-id="7201d-161">Kui eelarve juhtimise konfiguratsioon on aktiivne ja sisse lülitatud, saab sisestamisdefinitsioone ja kande sisestamisdefinitsioone kasutada eraldiste, paranduste, ülekannete, projektide, põhivarade ning tarne- ja nõudlusprognooside kirjete pearaamatusse registreerimise toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="7201d-161">When a budget control configuration is active and is turned on, posting definitions and transaction posting definitions can be used to support the recording of entries for appropriations, revisions, transfers, projects, fixed assets, and supply and demand forecasts to the general ledger.</span></span> 

<span data-ttu-id="7201d-162">Selleks et seadistada sisestamisdefinitsioon eelarve registrikannete jaoks, mille eelarvetüüp on **Algne eelarve** ja mille puhul on eraldised lubatud, valige lehel **Sisestamisdefinitsioonid** moodul **Eelarve**.</span><span class="sxs-lookup"><span data-stu-id="7201d-162">To set up a posting definition for budget register entries that has a budget type of **Original budget**, and that has appropriations enabled, select the **Budget** module on the **Posting definitions** page.</span></span> <span data-ttu-id="7201d-163">Seejärel saate lehe **Kande sisestamisdefinitsioonid** alal **Eelarve** kasutada eelarvekoode, et seostada sisestamisdefinitsioonid eelarve registrikannetega, mille eelarvetüüp on **Algne eelarve**.</span><span class="sxs-lookup"><span data-stu-id="7201d-163">Then, in the **Budget** area of the **Transaction posting definitions** page, you can use budget codes to associate the posting definition with budget register entries that have a budget type of **Original budget**.</span></span> 

<span data-ttu-id="7201d-164">Kui eelarveeraldised ja sisestamisdefinitsioonid on lubatud, registreeritakse eelarve registrikirjed eelarve juhtimisse ja pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="7201d-164">When budget appropriations and posting definitions are enabled, the budget register entries are recorded for budget control and in the general ledger.</span></span>

### <a name="posting-definition--match-criteria"></a><span data-ttu-id="7201d-165">Sisestamisdefinitsioon – vastendamise kriteeriumid</span><span class="sxs-lookup"><span data-stu-id="7201d-165">Posting definition – Match criteria</span></span>

| <span data-ttu-id="7201d-166">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="7201d-166">Account structure</span></span>       | <span data-ttu-id="7201d-167">Kattuva konto number</span><span class="sxs-lookup"><span data-stu-id="7201d-167">Match account number</span></span> | <span data-ttu-id="7201d-168">Prioriteet </span><span class="sxs-lookup"><span data-stu-id="7201d-168">Priority</span></span> |
|-------------------------|----------------------|----------|
| <span data-ttu-id="7201d-169">Konto struktuur – kasum ja kahjum</span><span class="sxs-lookup"><span data-stu-id="7201d-169">Account Structure - P&L</span></span> | \*                   | <span data-ttu-id="7201d-170">1</span><span class="sxs-lookup"><span data-stu-id="7201d-170">1</span></span>        |

<span data-ttu-id="7201d-171"><em>Tühi väärtus väljal \**Kattuva konto number</em>* tähendab, et kõik kattuvad kontod määratletud kontostruktuuris on vastendusreegli osa.</span><span class="sxs-lookup"><span data-stu-id="7201d-171"><em>A blank value in the \**Match account number</em>* field means that all matching accounts in the defined account structure are part of the matching rule.</span></span>

### <a name="posting-definition--generated-entries"></a><span data-ttu-id="7201d-172">Sisestamisdefinitsioon – loodud kanded</span><span class="sxs-lookup"><span data-stu-id="7201d-172">Posting definition – Generated entries</span></span>

| <span data-ttu-id="7201d-173">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="7201d-173">Account structure</span></span> | <span data-ttu-id="7201d-174">Loodud konto number</span><span class="sxs-lookup"><span data-stu-id="7201d-174">Generated account number</span></span>              | <span data-ttu-id="7201d-175">Loodud deebet/kreedit</span><span class="sxs-lookup"><span data-stu-id="7201d-175">Generated debit/credit</span></span> |
|-------------------|---------------------------------------|------------------------|
| <span data-ttu-id="7201d-176">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="7201d-176">Account structure</span></span> | <span data-ttu-id="7201d-177">300145 – (eeldatava tulu konto)</span><span class="sxs-lookup"><span data-stu-id="7201d-177">300145 - -(Estimated revenue account)</span></span> | <span data-ttu-id="7201d-178">Sama</span><span class="sxs-lookup"><span data-stu-id="7201d-178">Same</span></span>                   |
| <span data-ttu-id="7201d-179">Konto struktuur</span><span class="sxs-lookup"><span data-stu-id="7201d-179">Account structure</span></span> | <span data-ttu-id="7201d-180">300146 – (eraldisekonto)</span><span class="sxs-lookup"><span data-stu-id="7201d-180">300146 - -(Appropriation account)</span></span>     | <span data-ttu-id="7201d-181">Tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="7201d-181">Balancing</span></span>              |

### <a name="transactions-with-the-accounts-dimension-values-and-amounts"></a><span data-ttu-id="7201d-182">Kontode, dimensiooniväärtuste ja summadega kanded</span><span class="sxs-lookup"><span data-stu-id="7201d-182">Transactions with the accounts, dimension values, and amounts</span></span>

<span data-ttu-id="7201d-183">Saate sisestada kontod, dimensiooniväärtused ja eelarve konto kirje summad lehel **Eelarve registrikirje**.</span><span class="sxs-lookup"><span data-stu-id="7201d-183">You enter the accounts, dimension values, and amounts for the budget account entry on the **Budget register entry** page.</span></span>

| <span data-ttu-id="7201d-184">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="7201d-184">Account + dimensions</span></span>           | <span data-ttu-id="7201d-185">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="7201d-185">Debit</span></span> | <span data-ttu-id="7201d-186">Krediit</span><span class="sxs-lookup"><span data-stu-id="7201d-186">Credit</span></span> | <span data-ttu-id="7201d-187">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="7201d-187">Comment</span></span> |
|--------------------------------|-------|--------|---------|
| <span data-ttu-id="7201d-188">606400-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="7201d-188">606400-OU\_1-OU\_3566-Training</span></span> |       | <span data-ttu-id="7201d-189">250,00</span><span class="sxs-lookup"><span data-stu-id="7201d-189">250.00</span></span> |         |

### <a name="ledger-entries-generated-from-the-posting-definition"></a><span data-ttu-id="7201d-190">Sisestamisdefinitsioonist loodud pearaamatukirjed</span><span class="sxs-lookup"><span data-stu-id="7201d-190">Ledger entries generated from the posting definition</span></span>

<span data-ttu-id="7201d-191">Genereeritud pearaamatukirjed luuakse algse eelarve registreerimiseks igas dimensioonis.</span><span class="sxs-lookup"><span data-stu-id="7201d-191">Generated ledger entries are created to record the original budget in each dimension.</span></span>

| <span data-ttu-id="7201d-192">Konto + dimensioonid</span><span class="sxs-lookup"><span data-stu-id="7201d-192">Account + dimensions</span></span>           | <span data-ttu-id="7201d-193">Debiteeri</span><span class="sxs-lookup"><span data-stu-id="7201d-193">Debit</span></span>  | <span data-ttu-id="7201d-194">Krediit</span><span class="sxs-lookup"><span data-stu-id="7201d-194">Credit</span></span> | <span data-ttu-id="7201d-195">Kommentaar</span><span class="sxs-lookup"><span data-stu-id="7201d-195">Comment</span></span> |
|--------------------------------|--------|--------|---------|
| <span data-ttu-id="7201d-196">300145-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="7201d-196">300145-OU\_1-OU\_3566-Training</span></span> |        | <span data-ttu-id="7201d-197">250,00</span><span class="sxs-lookup"><span data-stu-id="7201d-197">250.00</span></span> |         |
| <span data-ttu-id="7201d-198">300146-OU\_1-OU\_3566-Training</span><span class="sxs-lookup"><span data-stu-id="7201d-198">300146-OU\_1-OU\_3566-Training</span></span> | <span data-ttu-id="7201d-199">250,00</span><span class="sxs-lookup"><span data-stu-id="7201d-199">250.00</span></span> |        |         |

<span data-ttu-id="7201d-200">Selles näites vastab iga konto, mis on osa jaotisest Konto struktuur – kasum ja kahjum, sisestamisdefinitsiooni kriteeriumitele.</span><span class="sxs-lookup"><span data-stu-id="7201d-200">In this example, any account that is part of Account Structure - P&L matches the posting definition criteria.</span></span> <span data-ttu-id="7201d-201">Üksuse 606400-OU\_1-OU\_3566-Training hindamisel luuakse seega genereeritud pearaamatukirjed.</span><span class="sxs-lookup"><span data-stu-id="7201d-201">Therefore, when 606400-OU\_1-OU\_3566-Training is evaluated, the generated ledger entries are created.</span></span>





