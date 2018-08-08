---
title: "Pearaamatu töölehe töötlemine"
description: "Selles artiklis kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi võimalusi, mis lihtsustavad üldise töölehe töötlemist ja mis aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud."
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 82d08a76c0d52719330960b85b3cca9b1440406b
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="general-journal-processing"></a><span data-ttu-id="fc652-103">Pearaamatu töölehe töötlemine</span><span class="sxs-lookup"><span data-stu-id="fc652-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc652-104">Selles artiklis kirjeldatakse Microsoft Dynamics 365 for Finance and Operationsi võimalusi, mis lihtsustavad üldise töölehe töötlemist ja mis aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud.</span><span class="sxs-lookup"><span data-stu-id="fc652-104">This articles describes capabilities in Microsoft Dynamics 365 for Finance and Operations that can help make general journal processing easier, and that can also help guarantee that correct data is captured and internal control isn't compromised.</span></span>  

<span data-ttu-id="fc652-105">Töölehe nimed</span><span class="sxs-lookup"><span data-stu-id="fc652-105">Journal names</span></span>

<span data-ttu-id="fc652-106">Üks tähtsaim seadistatav ala on töölehe nimed.</span><span class="sxs-lookup"><span data-stu-id="fc652-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="fc652-107">Soovitatav on määratleda konkreetsed töölehe nimed igaks eesmärgiks, nt kontsernisiseseks, viitvõlgade korrigeerimiseks ja vigade parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="fc652-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="fc652-108">Saate kohandada iga töölehe nime iga eesmärgi puhul andmete sisestamise lihtsaks ja turvaliseks muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="fc652-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="fc652-109">Lehel **Töölehe nimed** saate seadistada järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="fc652-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="fc652-110">**Töövoo kinnitamine** – sisekontrolli tõhustamiseks määratlege töölehe töövood, mis loovad ülevaatus- ja kinnitamisetappide materiaalsuspiirangud kriteeriumide, nagu deebeti kogusummade alusel.</span><span class="sxs-lookup"><span data-stu-id="fc652-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="fc652-111">Saate pearaamatute töövoogusid seadistada lehel **Pearaamatu töövood**.</span><span class="sxs-lookup"><span data-stu-id="fc652-111">You set up workflows for the general journals on the** General ledger workflows** page.</span></span>
-   <span data-ttu-id="fc652-112">**Vaikeväärtused** – valige vastaskontode, valuuta ja finantsdimensioonide vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="fc652-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="fc652-113">**Töölehe juhtimine** – saate seadistada ettevõtte ja kontotüübi piiranguid ja ka segmendi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="fc652-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="fc652-114">**Näited**</span><span class="sxs-lookup"><span data-stu-id="fc652-114">**Examples**</span></span>

<span data-ttu-id="fc652-115">Töölehe nime võib kasutada ainult korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="fc652-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="fc652-116">Sellisel juhul saate määrata, et kõigis ettevõtetes kehtib ainult konto tüüp **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="fc652-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> <span data-ttu-id="fc652-117">[![Töölehe juhtimise kontotüübid](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="fc652-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="fc652-118">Töölehe nime saab kasutada ainult kindla segmendi või põhikontode vahemiku puhul.</span><span class="sxs-lookup"><span data-stu-id="fc652-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> <span data-ttu-id="fc652-119">[![Töölehe juhtimise segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="fc652-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="fc652-120">Päevaraamatutes on saadaval suvand **Automaatne tühistamine**.</span><span class="sxs-lookup"><span data-stu-id="fc652-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="fc652-121">Näiteks viitvõlgade korrigeerimise puhul, kui tegelikku dokumenti pole veel töödeldud, nagu on näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="fc652-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="fc652-122">[![Pearaamatu ennistamine](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="fc652-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="fc652-123">Microsoft Exceli lisandmoodul pakub töölehe sisestuse puhul automatiseerimise täiendavat taset ja lihtsustab andmesisestust.</span><span class="sxs-lookup"><span data-stu-id="fc652-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="fc652-124">Tegevus **Ridade avamine Excelis** on saadaval lehtedel **Päevaraamat** ja **Töölehe kanne**.</span><span class="sxs-lookup"><span data-stu-id="fc652-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="fc652-125">Lehel **Perioodilised töölehed** saate töölehe töötlemise automatiseerimiseks seadistada korduvad töölehed.</span><span class="sxs-lookup"><span data-stu-id="fc652-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="fc652-126">Saate kande malle kasutada igal ajal.</span><span class="sxs-lookup"><span data-stu-id="fc652-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="fc652-127">Lehel **Päevaraamatud** on tegevused **Salvesta** ja **Vali kande mall** lehe **Töölehe kanne** kande ridade **Funktsioonid** all.</span><span class="sxs-lookup"><span data-stu-id="fc652-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="fc652-128">Seotud seadistus</span><span class="sxs-lookup"><span data-stu-id="fc652-128">Related setup</span></span>
<span data-ttu-id="fc652-129">Järgmine seadistus ei ole omane päevaraamatutele, kuid aitab tagada, et andmesisestus oleks õige ja lihtne.</span><span class="sxs-lookup"><span data-stu-id="fc652-129">The following setup isn't specific to general journals, but will help guarantee that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="fc652-130">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="fc652-130">Main account</span></span>

<span data-ttu-id="fc652-131">Põhikonto seadistus pakub päevaraamatu töötlemiseks mitmeid järgmisi suvandeid.</span><span class="sxs-lookup"><span data-stu-id="fc652-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="fc652-132">**DC/CR-i nõue** – kasutage seda suvandit, kui põhikonto on piiratud deebet- või kreeditkannetele.</span><span class="sxs-lookup"><span data-stu-id="fc652-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="fc652-133">Seadistus kinnitatakse töölehe kontrollimisel või sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="fc652-133">The setup is verified when a journal is validated or posted.</span></span>
-   <span data-ttu-id="fc652-134">**Vaikevastaskonto**</span><span class="sxs-lookup"><span data-stu-id="fc652-134">**Default offset account**</span></span>
-   <span data-ttu-id="fc652-135">**Peatatud** – põhikonto peatamine andmesisestuseks kõigis ettevõtetes või kindla ettevõtte/juriidiliste isikute puhul.</span><span class="sxs-lookup"><span data-stu-id="fc652-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entities.</span></span>
-   <span data-ttu-id="fc652-136">**Ära luba käsitsi sisestamist** – takistab kasutajatel töölehtede konto väärtuse käsitsi sisestamise.</span><span class="sxs-lookup"><span data-stu-id="fc652-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="fc652-137">**Vaikevaluuta/valuuta kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="fc652-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="fc652-138">**Juriidilise isiku alistamine** – see seadistus on omane määratud ettevõttele/juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="fc652-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="fc652-139">**Vaikimisi käibemaks/käibemaksu kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="fc652-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="fc652-140">**Vaikedimensioon** – **Pole fikseeritud** või **Fikseeritud väärtus**.</span><span class="sxs-lookup"><span data-stu-id="fc652-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="fc652-141">**Fikseeritud väärtus** aitab tagada, et kõigi selle põhikonto sisestuste puhul kasutatakse alati dimensiooniväärtust, mis on seadistatud kui **Fikseeritud**.</span><span class="sxs-lookup"><span data-stu-id="fc652-141">**Fixed value** will help guarantee that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="fc652-142">**Sisestuse kontrollimine**</span><span class="sxs-lookup"><span data-stu-id="fc652-142">**Posting validation**</span></span>
    -   <span data-ttu-id="fc652-143">**Kasutaja kinnitamine** – see suvand kontrollib, millised kasutajad võivad põhikontole sisestada.</span><span class="sxs-lookup"><span data-stu-id="fc652-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="fc652-144">**Sisestamistüübi kinnitamine** – see suvand kontrollib, millised sisestamistüübid on lubatud põhikonto puhul.</span><span class="sxs-lookup"><span data-stu-id="fc652-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="fc652-145">Arvestusstruktuurid ja täpsemate reeglite struktuurid</span><span class="sxs-lookup"><span data-stu-id="fc652-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="fc652-146">Arvestusstruktuurid ja täpsemate reeglite struktuurid on äärmiselt olulised, tagamaks andmete nõudmine finantsaruandluseks ja jõudluse jälgimise rakendamine päevaraamatu töötlemisel ja mis tahes dokumentide puhul.</span><span class="sxs-lookup"><span data-stu-id="fc652-146">Accounting structures and advanced rules structures are extremely important for guaranteeing that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="fc652-147">Arvestusstruktuurid ja täpsemate reeglite struktuurid võimaldavad teil andmete sisestamise kogemust kohandada.</span><span class="sxs-lookup"><span data-stu-id="fc652-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="fc652-148">Saate lubada andmesisestuse ainult igas olukorras asjakohaste finantsdimensioonide puhul ja rakendada alati kohustuslike ja õigete andmete hõivamise nõuet.</span><span class="sxs-lookup"><span data-stu-id="fc652-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that mandatory and correct data always be captured.</span></span>

<span data-ttu-id="fc652-149">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="fc652-149">For more information, see the following topics:</span></span>
- <span data-ttu-id="fc652-150">[Plaanimine: kontoplaan](plan-chart-of-accounts.md).</span><span class="sxs-lookup"><span data-stu-id="fc652-150">[Planning: Chart of accounts](plan-chart-of-accounts.md).</span></span> 
- [<span data-ttu-id="fc652-151">Täpsemate reeglite loomine töölehtede jaoks</span><span class="sxs-lookup"><span data-stu-id="fc652-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="fc652-152">Töölehe sisestuse loomine malli abil</span><span class="sxs-lookup"><span data-stu-id="fc652-152">Create a journal entry using a template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="fc652-153">Töölehtede loomine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="fc652-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="fc652-154">Perioodiliste töölehtede sisestamine</span><span class="sxs-lookup"><span data-stu-id="fc652-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="fc652-155">Pearaamatu eraldamistöölehe töötlemine</span><span class="sxs-lookup"><span data-stu-id="fc652-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)



