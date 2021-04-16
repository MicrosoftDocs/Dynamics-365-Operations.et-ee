---
title: Üldtöölehe töötlemine
description: Selles teemas kirjeldatakse Microsoft Dynamics 365 Finance'i võimalusi, mis lihtsustavad üldise töölehe töötlemist ja aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud.
author: ShylaThompson
ms.date: 08/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76dbf5f8f2fc3b33077d559ffcef580a5295adb2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815568"
---
# <a name="general-journal-processing"></a><span data-ttu-id="ab79c-103">Üldtöölehe töötlemine</span><span class="sxs-lookup"><span data-stu-id="ab79c-103">General journal processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ab79c-104">Selles teemas kirjeldatakse võimalusi, mis lihtsustavad üldise töölehe töötlemist ja aitavad ühtlasi tagada, et jäädvustatakse õiged andmed ning sisekontrolli pole kahjustatud.</span><span class="sxs-lookup"><span data-stu-id="ab79c-104">This topic describes capabilities that can help make general journal processing easier, and that can also help ensure that correct data is captured and internal control isn't compromised.</span></span>  

## <a name="journal-names"></a><span data-ttu-id="ab79c-105">Töölehe nimed</span><span class="sxs-lookup"><span data-stu-id="ab79c-105">Journal names</span></span>

<span data-ttu-id="ab79c-106">Üks tähtsaim seadistatav ala on töölehe nimed.</span><span class="sxs-lookup"><span data-stu-id="ab79c-106">One of the most important areas to set up is journal names.</span></span> <span data-ttu-id="ab79c-107">Soovitatav on määratleda konkreetsed töölehe nimed igaks eesmärgiks, nt kontsernisiseseks, viitvõlgade korrigeerimiseks ja vigade parandamiseks.</span><span class="sxs-lookup"><span data-stu-id="ab79c-107">It's a good idea to define specific journal names for each purpose, such as intercompany, accrual adjustment, and error correction.</span></span> <span data-ttu-id="ab79c-108">Saate kohandada iga töölehe nime iga eesmärgi puhul andmete sisestamise lihtsaks ja turvaliseks muutmiseks.</span><span class="sxs-lookup"><span data-stu-id="ab79c-108">You can tailor each journal name to help make data entry for each purpose easy and secure.</span></span> 

<span data-ttu-id="ab79c-109">Lehel **Töölehe nimed** saate seadistada järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="ab79c-109">On the **Journal names** page, you can set up the following elements:</span></span>

-   <span data-ttu-id="ab79c-110">**Töövoo kinnitamine** – sisekontrolli tõhustamiseks määratlege töölehe töövood, mis loovad ülevaatus- ja kinnitamisetappide materiaalsuspiirangud kriteeriumide, nagu deebeti kogusummade alusel.</span><span class="sxs-lookup"><span data-stu-id="ab79c-110">**Workflow approval** – To increase internal control, define journal workflows that establish materiality limits for review and approval steps, based on criteria such as total debit amount.</span></span> <span data-ttu-id="ab79c-111">Saate pearaamatute töövoogusid seadistada lehel **Pearaamatu töövood**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-111">You set up workflows for the general journals on the **General ledger workflows** page.</span></span>
-   <span data-ttu-id="ab79c-112">**Vaikeväärtused** – valige vastaskontode, valuuta ja finantsdimensioonide vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="ab79c-112">**Default values** – Select default values for offset accounts, currency, and financial dimensions.</span></span>
-   <span data-ttu-id="ab79c-113">**Töölehe juhtimine** – saate seadistada ettevõtte ja kontotüübi piiranguid ja ka segmendi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ab79c-113">**Journal control** – You can set up restrictions on the company and account type, and also the segment values.</span></span> 

<span data-ttu-id="ab79c-114">**Näited**</span><span class="sxs-lookup"><span data-stu-id="ab79c-114">**Examples**</span></span>

<span data-ttu-id="ab79c-115">Töölehe nime võib kasutada ainult korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="ab79c-115">A journal name can be used only for adjustments.</span></span> <span data-ttu-id="ab79c-116">Sellisel juhul saate määrata, et kõigis ettevõtetes kehtib ainult konto tüüp **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-116">In this case, you can specify that only the **Ledger** account type is valid across all companies.</span></span> 

<span data-ttu-id="ab79c-117">[![Töölehe juhtimise kontotüübid](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span><span class="sxs-lookup"><span data-stu-id="ab79c-117">[![Journal control account types](./media/journal-control-account-types1.png)](./media/journal-control-account-types1.png)</span></span>

<span data-ttu-id="ab79c-118">Töölehe nime saab kasutada ainult kindla segmendi või põhikontode vahemiku puhul.</span><span class="sxs-lookup"><span data-stu-id="ab79c-118">A journal name can be used only for a specific segment or for a range for main accounts.</span></span> 

<span data-ttu-id="ab79c-119">[![Töölehe juhtimise segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span><span class="sxs-lookup"><span data-stu-id="ab79c-119">[![Journal control segment](./media/journal-control-segment1.png)](./media/journal-control-segment1.png)</span></span>

<span data-ttu-id="ab79c-120">Päevaraamatutes on saadaval suvand **Automaatne tühistamine**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-120">The **Automatic reversal** option is available in general journals.</span></span> <span data-ttu-id="ab79c-121">Näiteks viitvõlgade korrigeerimise puhul, kui tegelikku dokumenti pole veel töödeldud, nagu on näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="ab79c-121">For example, you have an accrual adjustment where the actual document hasn't yet been processed, as shown in the following illustration.</span></span>
<span data-ttu-id="ab79c-122">[![Pearaamatu ennistamine](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span><span class="sxs-lookup"><span data-stu-id="ab79c-122">[![General journal reversing](./media/general-journal-reversing1.png)](./media/general-journal-reversing1.png)</span></span> 

<span data-ttu-id="ab79c-123">Microsoft Exceli lisandmoodul pakub töölehe sisestuse puhul automatiseerimise täiendavat taset ja lihtsustab andmesisestust.</span><span class="sxs-lookup"><span data-stu-id="ab79c-123">The Microsoft Excel add-in for journal entry provides an additional level of automation and makes data entry easier.</span></span> <span data-ttu-id="ab79c-124">Tegevus **Ridade avamine Excelis** on saadaval lehtedel **Päevaraamat** ja **Töölehe kanne**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-124">The **Open lines in Excel** action is available on the **General journal** and **Journal voucher** pages.</span></span> 

<span data-ttu-id="ab79c-125">Lehel **Perioodilised töölehed** saate töölehe töötlemise automatiseerimiseks seadistada korduvad töölehed.</span><span class="sxs-lookup"><span data-stu-id="ab79c-125">On the **Periodic journals** page, you can set up recurring journals to automate journal processing.</span></span> 

<span data-ttu-id="ab79c-126">Saate kande malle kasutada igal ajal.</span><span class="sxs-lookup"><span data-stu-id="ab79c-126">You can use voucher templates at any time.</span></span> <span data-ttu-id="ab79c-127">Lehel **Päevaraamatud** on tegevused **Salvesta** ja **Vali kande mall** lehe **Töölehe kanne** kande ridade **Funktsioonid** all.</span><span class="sxs-lookup"><span data-stu-id="ab79c-127">On the **General journals** page, the **Save** and **Select voucher template** actions are found on the **Journal voucher** page, under **Functions** for the voucher lines.</span></span>

## <a name="related-setup"></a><span data-ttu-id="ab79c-128">Seotud seadistus</span><span class="sxs-lookup"><span data-stu-id="ab79c-128">Related setup</span></span>
<span data-ttu-id="ab79c-129">Järgmine seadistus ei ole omane pearaamatutele, kuid aitab tagada, et andmesisestus oleks õige ja lihtne.</span><span class="sxs-lookup"><span data-stu-id="ab79c-129">The following setup isn't specific to general journals, but will help ensure that data entry is correct data and easy.</span></span>

### <a name="main-account"></a><span data-ttu-id="ab79c-130">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="ab79c-130">Main account</span></span>

<span data-ttu-id="ab79c-131">Põhikonto seadistus pakub päevaraamatu töötlemiseks mitmeid järgmisi suvandeid.</span><span class="sxs-lookup"><span data-stu-id="ab79c-131">The main account setup provides many options for general journal processing:</span></span>

-   <span data-ttu-id="ab79c-132">**DC/CR-i nõue** – kasutage seda suvandit, kui põhikonto on piiratud deebet- või kreeditkannetele.</span><span class="sxs-lookup"><span data-stu-id="ab79c-132">**DC/CR requirement** – Use this option if a main account is limited to debit or credit transactions.</span></span> <span data-ttu-id="ab79c-133">Seadistus kinnitatakse töölehe kontrollimisel või sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="ab79c-133">The setup is verified when a journal is validated or posted.</span></span>

-   <span data-ttu-id="ab79c-134">**Vaikevastaskonto**</span><span class="sxs-lookup"><span data-stu-id="ab79c-134">**Default offset account**</span></span>
-   <span data-ttu-id="ab79c-135">**Peatatud** – põhikonto peatamine andmesisestuseks kõigis ettevõtetes või kindla ettevõtte / juriidilise isiku puhul.</span><span class="sxs-lookup"><span data-stu-id="ab79c-135">**Suspended** – Suspend a main account for data entry across all companies or for a specific company/legal entity.</span></span>
-   <span data-ttu-id="ab79c-136">**Ära luba käsitsi sisestamist** – takistab kasutajatel töölehtede konto väärtuse käsitsi sisestamise.</span><span class="sxs-lookup"><span data-stu-id="ab79c-136">**Do not allow manual entry** – Prevent users from manually entering a value for the account in journals.</span></span>
-   <span data-ttu-id="ab79c-137">**Vaikevaluuta/valuuta kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="ab79c-137">**Default/Validate currency**</span></span>
-   <span data-ttu-id="ab79c-138">**Juriidilise isiku alistamine** – see seadistus on omane määratud ettevõttele/juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="ab79c-138">**Legal entity override** – This setup is specific to the defined company/legal entity:</span></span>
    -   <span data-ttu-id="ab79c-139">**Vaikimisi käibemaks/käibemaksu kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="ab79c-139">**Default/Validate sales tax**</span></span>
    -   <span data-ttu-id="ab79c-140">**Vaikedimensioon** – **Pole fikseeritud** või **Fikseeritud väärtus**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-140">**Default dimension** – **Not fixed** or **Fixed value**.</span></span> <span data-ttu-id="ab79c-141">**Fikseeritud väärtus** aitab tagada, et kõigi selle põhikonto sisestuste puhul kasutatakse alati dimensiooniväärtust, mis on seadistatud kui **Fikseeritud**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-141">**Fixed value** will help ensure that all postings for this main account always use any dimension value that is set up as **Fixed**.</span></span>
-   <span data-ttu-id="ab79c-142">**Sisestuse kontrollimine**</span><span class="sxs-lookup"><span data-stu-id="ab79c-142">**Posting validation**</span></span>
    -   <span data-ttu-id="ab79c-143">**Kasutaja kinnitamine** – see suvand kontrollib, millised kasutajad võivad põhikontole sisestada.</span><span class="sxs-lookup"><span data-stu-id="ab79c-143">**User validation** – This option controls which users are allowed to post to a main account.</span></span>
    -   <span data-ttu-id="ab79c-144">**Sisestamistüübi kinnitamine** – see suvand kontrollib, millised sisestamistüübid on lubatud põhikonto puhul.</span><span class="sxs-lookup"><span data-stu-id="ab79c-144">**Posting type validation** – This option controls which posting types are allowed for a main account.</span></span>

### <a name="accounting-structures-and-advanced-rules-structures"></a><span data-ttu-id="ab79c-145">Arvestusstruktuurid ja täpsemate reeglite struktuurid</span><span class="sxs-lookup"><span data-stu-id="ab79c-145">Accounting structures and advanced rules structures</span></span>

<span data-ttu-id="ab79c-146">Arvestusstruktuurid ja täpsemate reeglite struktuurid on äärmiselt olulised tagamaks, et finantsaruandluseks ja jõudluse jälgimiseks vajalikud andmed hõivatakse pearaamatu töötlemisel ja mis tahes dokumentatsioonis.</span><span class="sxs-lookup"><span data-stu-id="ab79c-146">Accounting structures and advanced rules structures are extremely important for ensuring that the data that is required for financial reporting and performance tracking is captured during general journal processing and any documentation.</span></span> <span data-ttu-id="ab79c-147">Arvestusstruktuurid ja täpsemate reeglite struktuurid võimaldavad teil andmete sisestamise kogemust kohandada.</span><span class="sxs-lookup"><span data-stu-id="ab79c-147">Accounting structures and advanced rules structures let you tailor the data entry experience.</span></span> <span data-ttu-id="ab79c-148">Saate lubada andmesisestuse ainult igas olukorras asjakohaste finantsdimensioonide puhul ning rakendada alati kohustuslike ja õigete andmete hõivamise nõuet.</span><span class="sxs-lookup"><span data-stu-id="ab79c-148">You can allow data entry only for financial dimensions that are relevant in each situation, and can also enforce the requirement that required and accurate data always be captured.</span></span>

<span data-ttu-id="ab79c-149">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="ab79c-149">For more information, see the following topics:</span></span>
- [<span data-ttu-id="ab79c-150">Kontoplaanide plaanimine</span><span class="sxs-lookup"><span data-stu-id="ab79c-150">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md) 
- [<span data-ttu-id="ab79c-151">Täpsemate reeglite loomine töölehtede jaoks</span><span class="sxs-lookup"><span data-stu-id="ab79c-151">Create advanced rules for journals</span></span>](tasks/create-advanced-rules-journals.md)
- [<span data-ttu-id="ab79c-152">Töölehe sisestuse loomine malli abil</span><span class="sxs-lookup"><span data-stu-id="ab79c-152">Create a journal entry using template</span></span>](tasks/create-journal-entry-template.md)
- [<span data-ttu-id="ab79c-153">Töölehtede loomine ja kinnitamine</span><span class="sxs-lookup"><span data-stu-id="ab79c-153">Create and validate journals</span></span>](tasks/create-validate-journals.md)
- [<span data-ttu-id="ab79c-154">Perioodiliste töölehtede sisestamine</span><span class="sxs-lookup"><span data-stu-id="ab79c-154">Post periodic journals</span></span>](tasks/post-periodic-journals.md)
- [<span data-ttu-id="ab79c-155">Pearaamatu eraldamistöölehe töötlemine</span><span class="sxs-lookup"><span data-stu-id="ab79c-155">Process ledger allocation journal</span></span>](tasks/process-ledger-allocation-journal.md)

## <a name="simulate-posting"></a><span data-ttu-id="ab79c-156">Simuleeri sisestamist</span><span class="sxs-lookup"><span data-stu-id="ab79c-156">Simulate posting</span></span>
<span data-ttu-id="ab79c-157">Suvandi **Sisestamise simuleerimine** leiate enamiku töölehtede puhul menüüst **Kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-157">You can find **Simulate posting** on the **Validate** menu for most journals.</span></span> <span data-ttu-id="ab79c-158">Töölehe kinnitamisel funktsiooniga **Kinnitamine** kontrollib süsteemi töölehte konkreetsete tõrketingimuste suhtes.</span><span class="sxs-lookup"><span data-stu-id="ab79c-158">When you validate a journal using the **Validate** function, the system tests the journal for specific error conditions.</span></span> <span data-ttu-id="ab79c-159">Funktsiooni **Sisestamise simuleerimine** kasutamisel käitab süsteem samu protsesse mida sisestamise ajal, kuid töölehte tegelikult sisestamata.</span><span class="sxs-lookup"><span data-stu-id="ab79c-159">If you use the **Simulate posting** function, the system runs all of the same processes that are run during posting without actually posting the journal.</span></span> <span data-ttu-id="ab79c-160">Seejärel saate üle vaadata kuvatud sisestamisteated, paranda leitud tõrked ja seejärel avage töölehe sisestamiseks menüü **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-160">You can then review the posting messages that are displayed, fix any errors that you find, and then open the **Post** menu to post the journal.</span></span> 

<span data-ttu-id="ab79c-161">**Sisestamise simuleerimine** pole saadaval pakktöötluse puhul.</span><span class="sxs-lookup"><span data-stu-id="ab79c-161">**Simulate posting** is not available for batch processing.</span></span> <span data-ttu-id="ab79c-162">Siiski on saadaval kood sisestamise simuleerimiseks pakktöötluses ja arendajatel on võimalik koodi laiendada selle funktsionaalsuse lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="ab79c-162">However, there is code available to simulate posting in batch and developers can extend the code to add that functionality.</span></span>  

## <a name="journal-unlock"></a><span data-ttu-id="ab79c-163">Töölehe avamine</span><span class="sxs-lookup"><span data-stu-id="ab79c-163">Journal unlock</span></span>
<span data-ttu-id="ab79c-164">Töölehe lehel on saadaval nupp, et avada tööleht, mille oleku „Süsteemi poolt lukustatud” väärtuseks on seatud Jah.</span><span class="sxs-lookup"><span data-stu-id="ab79c-164">A button is available on the journal page to unlock a journal that has a status of "locked by system" set to Yes.</span></span> <span data-ttu-id="ab79c-165">Töölehe saab avada süsteemiadministraator, kes on analüüsinud kõiki pakett-tööde täitmisi ja kinnitanud, et pakett-töö ei töötle seda töölehte enam aktiivselt.</span><span class="sxs-lookup"><span data-stu-id="ab79c-165">This unlock can be performed by an administrator of the system who has analyzed any executing batch jobs and confirmed this journal is no longer actively being processed by a batch job.</span></span> <span data-ttu-id="ab79c-166">Selle nupu lubab lehe **Funktsioonihaldus** funktsioon **Töölehe avamise nupp**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-166">This button is enabled by the feature named **Journal Unlock button** on the **Feature management** page.</span></span> 

## <a name="workflow-recall"></a><span data-ttu-id="ab79c-167">Töövoo tagasi kutsumine</span><span class="sxs-lookup"><span data-stu-id="ab79c-167">Workflow recall</span></span> 
<span data-ttu-id="ab79c-168">Töölehe tagasivõtmise võimalus töövoos, mille olek on „taastamatu”, on lubatud töölehel ja lehel **Töövoo ajalugu** nupu **Töövoog** abil.</span><span class="sxs-lookup"><span data-stu-id="ab79c-168">The ability to recall a journal in a workflow that has a status of "unrecoverable" is enabled by using the **Workflow** button on a journal, and on the **Workflow history** page.</span></span> <span data-ttu-id="ab79c-169">Seda lubab funktsioon nimega **Töölehtede töövoo oleku lähtestamine** lehel **Funktsioonihaldus**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-169">This is enabled by the feature named **Resetting the workflow status for journals** on the **Feature management** page.</span></span>

## <a name="delete-journal-lines"></a><span data-ttu-id="ab79c-170">Kustuta töölehe read</span><span class="sxs-lookup"><span data-stu-id="ab79c-170">Delete Journal Lines</span></span>
<span data-ttu-id="ab79c-171">Kõigi töölehe ridade kiire kustutamise võimalus on lubatud töölehe jaotises **Funktsioonid** > **Kustuta töölehe read**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-171">The ability to delete all journal lines quickly is enabled in a journal under **Functions** > **Delete Journal Lines**.</span></span> <span data-ttu-id="ab79c-172">Selle funktsiooni lubamiseks valige lehel **Funktsioonihaldus** käsk **Kustuta töölehe jõudluse optimeerimised**.</span><span class="sxs-lookup"><span data-stu-id="ab79c-172">To enable this feature, on the **Feature management**, select **Delete journal performance optimizations**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]