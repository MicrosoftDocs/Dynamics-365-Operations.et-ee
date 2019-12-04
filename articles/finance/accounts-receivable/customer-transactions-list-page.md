---
title: Kliendi kannete loendi leht
description: See teema annab teavet rakenduse Microsoft Dynamics 365 Finance kliendi kannete loendilehe kohta.
author: mikefalkner
manager: aolson
ms.date: 08/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 8295c2bcdd2eb99290e1a955df84a092d8ae6adb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177399"
---
# <a name="customer-transactions-list-page"></a><span data-ttu-id="42355-103">Kliendi kannete loendi leht</span><span class="sxs-lookup"><span data-stu-id="42355-103">Customer transactions list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="42355-104">Kuva tasakaalustused</span><span class="sxs-lookup"><span data-stu-id="42355-104">View settlements</span></span>

<span data-ttu-id="42355-105">Nupp **Kuva tasakaalustused** toimingupaanil annab kiire juurdepääsu tasakaalustuste ajaloole ja üksikasjalikku lisateavet kogu tasakaalustuskande kohta.</span><span class="sxs-lookup"><span data-stu-id="42355-105">The **View settlements** button on the Action Pane provides quick access to the settlement history and detailed information about the settlement transaction.</span></span> <span data-ttu-id="42355-106">Saate ka kuvada lisakandeid, mis on seotud valitud kandega kas seetõttu, et need olid osa samast tasakaalustusest või kuna need on maksed, mis loodi samas makse töölehes.</span><span class="sxs-lookup"><span data-stu-id="42355-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="42355-107">Valige suvandid **Müügireskontro \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="42355-107">Select **Accounts receivable \> All customers**.</span></span>
2. <span data-ttu-id="42355-108">Valige klient, kellel on kanded, ja seejärel valige toimingupaani vahekaardil **Klient** suvand **Kanded**.</span><span class="sxs-lookup"><span data-stu-id="42355-108">Select a customer that has transactions, and then, on the Action Pane, on the **Customer** tab, select **Transactions**.</span></span>
3. <span data-ttu-id="42355-109">Valige uuritav kanne ja seejärel valige toimingupaanil suvand **Kuva tasakaalustused**.</span><span class="sxs-lookup"><span data-stu-id="42355-109">Select a transaction to research, and then, on the Action Pane, select **View settlements**.</span></span>

    <span data-ttu-id="42355-110">Avaneb dialoogiboks **Kuva tasakaalustused**, kus kuvatakse valitud kande ja kõik dokumendid, mis on selle suhtes tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="42355-110">The **View settlements** dialog box appears, and shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="42355-111">See dialoogiboks meenutab tasakaalustuste ajaloo vaadet, aga sisaldab kõiki seotud dokumente.</span><span class="sxs-lookup"><span data-stu-id="42355-111">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

4. <span data-ttu-id="42355-112">Selles dialoogiboksis saate teha mitmesuguseid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="42355-112">In the dialog box, you can perform various tasks.</span></span> <span data-ttu-id="42355-113">Valige üks või mitu kannet ja seejärel valige üks järgmistest nuppudest.</span><span class="sxs-lookup"><span data-stu-id="42355-113">Select one or more vouchers, and then select one of the following buttons:</span></span>

    - <span data-ttu-id="42355-114">**Kuva seotud** – kuvab kõik kliendi maksetöölehe kanded ja päevaraamatu kanded, mis loodi töölehtedes, milles loodi loendis kuvatud dokumendid.</span><span class="sxs-lookup"><span data-stu-id="42355-114">**View related** – Show all the payment journal transactions and general journal tranactions for the customer that were created in the journals in which the documents shown in the list were created.</span></span> <span data-ttu-id="42355-115">Näiteks makse kuvamisel kuvatakse kõik maksetöölehel, milles see loodi, olevad maksed.</span><span class="sxs-lookup"><span data-stu-id="42355-115">For example, if a payment is shown, then all of the payments in the payment journal in which it was created will be shown.</span></span> <span data-ttu-id="42355-116">Arve või makse kuvamisel, mis loodi päevaraamatus, kuvatakse kõik päevaraamatus, milles see loodi, olevad dokumendid.</span><span class="sxs-lookup"><span data-stu-id="42355-116">If an invoice or payment is shown and it was created in a general journal, then all of the documents in the general journal in which it was created will be shown.</span></span> <span data-ttu-id="42355-117">Peale selle kuvatakse kõik nende dokumendiloendiga seotud tasakaalustused.</span><span class="sxs-lookup"><span data-stu-id="42355-117">All the settlements that are related to list of documents are also shown.</span></span> <span data-ttu-id="42355-118">Seotud maksete vaatamise ajal muutub nupu sildiks **Kuva tasakaalustused**.</span><span class="sxs-lookup"><span data-stu-id="42355-118">While you're viewing related payments, the label of this button changes to **View settlements**.</span></span> <span data-ttu-id="42355-119">Valige suvand **Kuva tasakaalustused**, et kuvada ainult need kanded, mis kuvati dialoogiboksi **Kuva tasakaalustused** avamisel.</span><span class="sxs-lookup"><span data-stu-id="42355-119">Select **View settlements** to show only the transactions that were shown when you first opened the **View settlements** dialog box.</span></span>
    - <span data-ttu-id="42355-120">**Kuva ajalugu** – kuvatakse kannete tasakaalustamisajalugu.</span><span class="sxs-lookup"><span data-stu-id="42355-120">**View history** – Show the settlement history for the vouchers.</span></span> <span data-ttu-id="42355-121">Valige dialoogiboksi sulgemiseks suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="42355-121">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="42355-122">**Kuva raamatupidamine** – kuvatakse kõik valitud dokumentidega seotud kanded.</span><span class="sxs-lookup"><span data-stu-id="42355-122">**View accounting** – Show all vouchers that are related to the selected documents.</span></span> <span data-ttu-id="42355-123">Valige dialoogiboksi sulgemiseks suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="42355-123">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="42355-124">**Ekspordi** – valitud kanded eksporditakse Microsoft Excelisse.</span><span class="sxs-lookup"><span data-stu-id="42355-124">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
    - <span data-ttu-id="42355-125">**Kannete tasakaalustamine** – see nupp kuvatakse ainult siis, kui valitud algdokument ei olnud täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="42355-125">**Settle transactions** – This button appears only if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="42355-126">Selle nupu valimisel kuvatakse dialoogiboks **Kannete tasakaalustamine**, kus saate valida tasakaalustamiseks kanded.</span><span class="sxs-lookup"><span data-stu-id="42355-126">When you select this button, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="42355-127">**Tasakaalustamise tühistamine** – see nupp kuvatakse ainult siis, kui valitud algdokument oli täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="42355-127">**Undo settlements** – This button appears only if the original document that was selected was fully settled.</span></span> <span data-ttu-id="42355-128">Selle nupu valimisel kuvatakse dialoogiboks **Tasakaalustamise tühistamine**, kus saate selle dokumendi tasakaalustamised tühistada.</span><span class="sxs-lookup"><span data-stu-id="42355-128">When you select this button, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

## <a name="global-transactions"></a><span data-ttu-id="42355-129">Globaalsed kanded</span><span class="sxs-lookup"><span data-stu-id="42355-129">Global transactions</span></span>

<span data-ttu-id="42355-130">See **Globaalsete kannete** nupp kuvatakse ka loendilehel **Kliendi kanded**.</span><span class="sxs-lookup"><span data-stu-id="42355-130">The **Global transactions** button also displays on the **Customer transactions** list page.</span></span> <span data-ttu-id="42355-131">See nupp võimaldab kuvada kõik kliendi kanded kõigis juriidilistes isikutes.</span><span class="sxs-lookup"><span data-stu-id="42355-131">This button lets you view all transactions for a customer across all legal entities.</span></span> <span data-ttu-id="42355-132">Loendilehel **Kliendi kanded** kuvatakse kanded ainult nende juriidiliste isikute puhul, millele kasutajal on tema turbesätete alusel juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="42355-132">The **Customer transactions** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="42355-133">Loendilehel kuvatakse kõik nende klientide kanded, kellel on sama osapoole ID mis kliendil, kellega alustasite.</span><span class="sxs-lookup"><span data-stu-id="42355-133">The list page shows all transactions for customers that have the same party ID as the customer that you started with.</span></span> <span data-ttu-id="42355-134">Näiteks kui kliendil US-001 ühes juriidilises isikus on sama osapoole ID mis kliendil DE-001 teises juriidilises isikus, kuvatakse kõik kanded mõlema kliendi ID kohta.</span><span class="sxs-lookup"><span data-stu-id="42355-134">For example, if customer US-001 in one legal entity has the same party ID as customer DE-001 in another legal entity, all transactions for both customer IDs are shown.</span></span>

<span data-ttu-id="42355-135">Loendilehe **Kliendi kanded** menüüd erinevad olenevalt kande juriidilisest isikust.</span><span class="sxs-lookup"><span data-stu-id="42355-135">The menus on the **Customer transactions** list page vary, depending on the legal entity for the transaction.</span></span> <span data-ttu-id="42355-136">Näiteks kui mõni funktsioon on saadaval ainult Šveitsi juriidilistele isikutele, kuvatakse selle funktsiooni menüüsuvandid ainult Šveitsi kande valimisel.</span><span class="sxs-lookup"><span data-stu-id="42355-136">For example, if a feature is available only for Swiss legal entities, the menu options for that feature appear only when a Swiss transaction is selected.</span></span>

<span data-ttu-id="42355-137">Selle funktsiooni kasutamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="42355-137">To access the feature, follow these steps.</span></span>

1. <span data-ttu-id="42355-138">Valige suvandid **Müügireskontro \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="42355-138">Select **Accounts receivable \> All customers**.</span></span>
2. <span data-ttu-id="42355-139">Valige klient ja seejärel valige toimingupaani vahekaardil **Klient** grupis **Kanded** suvand **Globaalsed kanded**.</span><span class="sxs-lookup"><span data-stu-id="42355-139">Select a customer, and then, on the Action Pane, on the **Customer** tab, in the **Transactions** group, select **Global transactions**.</span></span>

## <a name="more-transaction-filters"></a><span data-ttu-id="42355-140">Rohkem kannetefiltreid</span><span class="sxs-lookup"><span data-stu-id="42355-140">More transaction filters</span></span> 

<span data-ttu-id="42355-141">Avatud kandeid kuvav filter on asendatud uue filtriga, mis võimaldab kuvada rohkem kannete kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="42355-141">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> <span data-ttu-id="42355-142">Väljal **Kuva** on saadaval järgmised suvandid.</span><span class="sxs-lookup"><span data-stu-id="42355-142">The following options are available in the **Show** field:</span></span>

- <span data-ttu-id="42355-143">**Kõik** – kuvatakse kõik valitud klientide kanded (avatud ja suletud).</span><span class="sxs-lookup"><span data-stu-id="42355-143">**All** – Show all transactions for the selected customers (open and closed).</span></span>
- <span data-ttu-id="42355-144">**Suletud** – kuvatakse ainult täielikult tasakaalustatud ja suletud kanded.</span><span class="sxs-lookup"><span data-stu-id="42355-144">**Closed** – Show only transactions that have been fully settled and closed.</span></span>
- <span data-ttu-id="42355-145">**Avatud** – kuvatakse ainult kanded, mis pole täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="42355-145">**Open** – Show only transactions that haven't been fully settled.</span></span>
- <span data-ttu-id="42355-146">**Avatud, sealhulgas sulgemise kuupäev või pärast kuupäeva** – kuvatakse ainult kanded, mis pole täielikult tasakaalustatud teie määratud kuupäeval või pärast seda.</span><span class="sxs-lookup"><span data-stu-id="42355-146">**Open including closed on or after date** – Show only transactions that haven't been fully settled on or after a date that you specify.</span></span> <span data-ttu-id="42355-147">Selle suvandi valimisel saate muuta filtri kõrval kuvatavat kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="42355-147">When you select this option, you can change the date that is shown next to the filter.</span></span> <span data-ttu-id="42355-148">Kanded, mille puhul on suvandi **Viimase tasakaalustuse kuupäev** väärtus teie määratud kuupäeval või pärast seda, kuvatakse loendis isegi siis, kui need kanded on tänase kuupäeva seisuga täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="42355-148">Transactions that have a **Last settlement date** value on or after the date that you specify are shown in the list, even if those transactions are fully settled as of the current date.</span></span> <span data-ttu-id="42355-149">Saldo näitab siiski saldot tänase, mitte valitud kuupäeva seisuga.</span><span class="sxs-lookup"><span data-stu-id="42355-149">However, the balance represents the balances as of the current date, not as of the selected date.</span></span>

<span data-ttu-id="42355-150">Valuutateisenduse kannete varjamiseks valige märkeruut **Peida valuuta ümberhindamised**.</span><span class="sxs-lookup"><span data-stu-id="42355-150">Select the **Hide currency revaluations** check box to hide currency translation transactions.</span></span>

## <a name="modify-due-dates-and-discount-dates"></a><span data-ttu-id="42355-151">Kuupäevade ja allahindluskuupäevade muutmine</span><span class="sxs-lookup"><span data-stu-id="42355-151">Modify due dates and discount dates</span></span>

<span data-ttu-id="42355-152">Saate värskendada avatud kliendikannete kuupäevi ja allahindluskuupäevi.</span><span class="sxs-lookup"><span data-stu-id="42355-152">You can update due dates and discount dates for open customer transactions.</span></span> <span data-ttu-id="42355-153">Väljaandes 8.1 saate lisada loendilehele **Kliendi kanded** tähtajad.</span><span class="sxs-lookup"><span data-stu-id="42355-153">In release 8.1, you can now add due dates to the **Customer transactions** list page.</span></span> <span data-ttu-id="42355-154">Klõpsates loendilehel **Kliendi kanded** tähtaega, saate muuta dialoogiboksis **Tähtaja ja skonto kuupäevade värskendamine** ka tähtaegu, allahindluskuupäevi, maksetingimusi ja skonto tingimusi.</span><span class="sxs-lookup"><span data-stu-id="42355-154">By clicking on the due date in the **Customer transactions** list page, you can also change due dates, discount dates, payment terms, and cash discount terms in the **Update due date and cash discount dates**  dialog box.</span></span>

### <a name="activate-the-feature"></a><span data-ttu-id="42355-155">Funktsiooni aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="42355-155">Activate the feature</span></span>

<span data-ttu-id="42355-156">Loendilehele **Kliendi kanded** tähtaegade lisamiseks ja kande maksesätete muutmiseks dialoogiboksi **Tähtaja ja skonto kuupäevade värskendamine** abil tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="42355-156">To add due dates to the **Customer transactions** list page and change payment settings for a transaction by using the **Update due date and cash discount dates** dialog box, follow these steps.</span></span>

1. <span data-ttu-id="42355-157">Valige suvandid **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="42355-157">Select **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="42355-158">Seadke vahekaardil **Tasakaalustused** suvandi **Kuva tähtaeg ja luba redigeerimine** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="42355-158">On the **Settlements** tab, set the **Show due date and allow edit** option to **Yes**.</span></span>
3. <span data-ttu-id="42355-159">Selle funktsiooni lubamiseks on kliendikannetele lisatud uued väljad.</span><span class="sxs-lookup"><span data-stu-id="42355-159">To enable this feature, new fields have been added to customer transactions.</span></span> <span data-ttu-id="42355-160">Need väljad täidetakse uue kande lõpuleviimisel.</span><span class="sxs-lookup"><span data-stu-id="42355-160">Those fields will be filled in when a new transaction is completed.</span></span> <span data-ttu-id="42355-161">Need täidetakse ka siis, kui avate dialoogiboksi **Tähtaja ja skonto kuupäevade värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="42355-161">They will also be filled in when you open the **Update due date and cash discount dates** dialog box.</span></span> <span data-ttu-id="42355-162">Kui seate suvandi **Kuva tähtaeg ja luba redigeerimine** sätteks **Ei**, kuvatakse dialoogiboks **Makseteabe värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="42355-162">When you set the **Show due date and allow edit** option to **Yes**, you will see the **Update payment information** dialog box.</span></span>  <span data-ttu-id="42355-163">Olemasolevate kannete kohe uuendamiseks valige suvand **Värskenda kõiki olemasolevaid kandeid**.</span><span class="sxs-lookup"><span data-stu-id="42355-163">To update existing transactions immediately, select **Update all existing transactions**.</span></span> <span data-ttu-id="42355-164">Teise võimalusena väljade täitmiseks ainult uute kannete puhul valige suvand **Jätka värskendamiseta**.</span><span class="sxs-lookup"><span data-stu-id="42355-164">Alternatively, to fill in the fields only for new transactions, select **Continue without update**.</span></span>

<span data-ttu-id="42355-165">Nüüd lisatakse tähtaeg loendilehele **Kliendi kanded**, nii et teil on kannete tähtaega ja skonto kuupäevi lihtsam muuta.</span><span class="sxs-lookup"><span data-stu-id="42355-165">The due date is now added to the **Customer transactions** list page, so you can easily modify the due date and cash discount dates for transactions.</span></span>

### <a name="modify-the-payment-settings"></a><span data-ttu-id="42355-166">Maksesätete muutmine</span><span class="sxs-lookup"><span data-stu-id="42355-166">Modify the payment settings</span></span>

<span data-ttu-id="42355-167">Loendilehel **Kliendi kanded** kuvatakse kõik kliendi kanded.</span><span class="sxs-lookup"><span data-stu-id="42355-167">The **Customer transactions** list page shows all transactions for a customer.</span></span> <span data-ttu-id="42355-168">Kui valite mõne kande tähtaja, avaneb dialoogiboks **Tähtaja ja skonto kuupäevade värskendamine**.</span><span class="sxs-lookup"><span data-stu-id="42355-168">When you select the due date for a transaction, the **Update due date and cash discount dates** dialog box appears.</span></span> <span data-ttu-id="42355-169">Selles dialoogiboksis kuvatakse tähtaja ja skonto arvutuste aluskuupäev, maksetingimused, skonto tingimused ja skonto kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="42355-169">This dialog box shows the base date for due date and discount calculations, due date, payment terms, cash discount terms, and cash discount dates.</span></span>

<span data-ttu-id="42355-170">Igal väljal on kandele selle redigeerimisel erinev mõju.</span><span class="sxs-lookup"><span data-stu-id="42355-170">Each field has a different effect on the transaction when you edit it:</span></span>

- <span data-ttu-id="42355-171">**Aluskuupäeva redigeerimine** – tähtaega ja allahindluskuupäevi muudetakse nii, et aluskuupäev on dokumendi kuupäev.</span><span class="sxs-lookup"><span data-stu-id="42355-171">**Edit the base date** - The due date and discount dates are changed as if the base date is the document date.</span></span>
- <span data-ttu-id="42355-172">**Tähtaja redigeerimine** – muudetakse ainult tähtaega.</span><span class="sxs-lookup"><span data-stu-id="42355-172">**Edit the due date** - Only the due date is changed.</span></span>
- <span data-ttu-id="42355-173">**Allahindluskuupäevade redigeerimine** – muudetakse ainult allahindluskuupäevi.</span><span class="sxs-lookup"><span data-stu-id="42355-173">**Edit the discount dates** - Only the discount dates are changed.</span></span>
- <span data-ttu-id="42355-174">**Maksetingimuste redigeerimine** – tähtaega muudetakse aluskuupäeva ja maksetingimuste alusel.</span><span class="sxs-lookup"><span data-stu-id="42355-174">**Edit the payment terms** - The due date is changed, based on the base date and the payment terms.</span></span>
- <span data-ttu-id="42355-175">**Skonto tingimuste redigeerimine** – skontosid muudetakse aluskuupäeva ja skonto tingimuste alusel.</span><span class="sxs-lookup"><span data-stu-id="42355-175">**Edit the cash discount terms** - The cash discounts are changed, based on the base date and the cash discount terms.</span></span>

<span data-ttu-id="42355-176">Kui olete maksesätete redigeerimise lõpetanud, valige muudatuste salvestamiseks käsk **Sule**.</span><span class="sxs-lookup"><span data-stu-id="42355-176">When you've finished editing the payment settings, select **Close** to save your changes.</span></span>