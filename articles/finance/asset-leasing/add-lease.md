---
title: Rendikirjete lisamine või kopeerimine (eelversioon)
description: Selles teemas kirjeldatakse, kuidas luua uus rentimine, sisestades selle teabe vara rentimisest või kopeerides teabe olemasolevast rendikirjest.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b495c9a02a872d4b360b5f7216b1db3f7d366daf
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814148"
---
# <a name="add-or-copy-leases-preview"></a><span data-ttu-id="6f8ef-103">Rendikirjete lisamine või kopeerimine (eelversioon)</span><span class="sxs-lookup"><span data-stu-id="6f8ef-103">Add or copy leases (Preview)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6f8ef-104">See teema selgitab, kuidas luua rentimine vara rentimisel nullist ja samuti kuidas luua rentimist kopeerides olemasolevast rendikirjest.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-104">This topic explains how to create a lease from scratch in Asset leasing, and also how to create a lease by copying an existing lease.</span></span> <span data-ttu-id="6f8ef-105">Rendikirje nullist loomise toiming hõlmab teabe sisestamist uude rendikirjesse ja seejärel rentimise ajakava loomist.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-105">The process for creating a lease from scratch involves entering information for the new lease and then creating a lease schedule.</span></span> <span data-ttu-id="6f8ef-106">Pärast vähemalt ühe rendikirje häälestamist võib olla lihtsam kopeerida teave olemasolevast rendikirjest ja seejärel muuta seda teavet vastavalt vajadusele, et luua uus rendikirje.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-106">After at least one lease has been set up, you might find it easier to copy the information from an existing lease and then edit that information as you require to create a new lease.</span></span>

## <a name="create-a-lease"></a><span data-ttu-id="6f8ef-107">Rendi loomine</span><span class="sxs-lookup"><span data-stu-id="6f8ef-107">Create a lease</span></span>

<span data-ttu-id="6f8ef-108">Vara rentimises rendikirje loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-108">Follow these steps to create a lease in Asset leasing.</span></span>

1. <span data-ttu-id="6f8ef-109">Valige toimingupaani lehel **Rendi kokkuvõte** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-109">On the **Lease summary** page, on the Action Pane, select **New**.</span></span>
2. <span data-ttu-id="6f8ef-110">Sisestage rendi teave.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-110">Enter the lease information.</span></span> <span data-ttu-id="6f8ef-111">Nõutavatel väljadel on punased ääred.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-111">Fields that are required have red borders.</span></span>

## <a name="create-a-lease-schedule"></a><span data-ttu-id="6f8ef-112">Rendigraafiku loomine</span><span class="sxs-lookup"><span data-stu-id="6f8ef-112">Create a lease schedule</span></span>

<span data-ttu-id="6f8ef-113">Pärast rendikirje teabe sisestamist tehke rendiajakava loomiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-113">After you've finished entering information for the lease, follow these steps to create a lease schedule.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8ef-114">Finantsdimensioonid võivad mis tahes kohandatud finantsdimensiooni põhjal muutuda.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-114">The financial dimensions might change based on any custom financial dimensions.</span></span>

1. <span data-ttu-id="6f8ef-115">Rendiraamatute loomiseks valige **Loo graafikud**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-115">Select **Create schedules** to generate the lease books.</span></span> <span data-ttu-id="6f8ef-116">Rendiraamatute hulka kuuluvad makse, amortisatsiooni, kulumi ja kulude graafikud.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-116">The lease books include the payment, amortization, depreciation, and expense schedules.</span></span>
2. <span data-ttu-id="6f8ef-117">Rendiraamatutele juurdepääsuks vastloodud graafikute vaatamiseks valige vahekaart **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-117">To access the lease books and view the newly created schedules, select the **Books** tab.</span></span>

    <span data-ttu-id="6f8ef-118">Leht **Raamatu üksikasjad** näitab, kuidas renti sellele eraldatud raamatutega arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-118">The **Book details** page shows how the lease is accounted for by the books that have been allocated to it.</span></span> <span data-ttu-id="6f8ef-119">Siit saate vaadata rendigraafikuid.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-119">From here, you can view the lease schedules.</span></span>

    <span data-ttu-id="6f8ef-120">Maksegraafik sisaldab vahekaardi **Maksegraafiku read** sisendeid lehel **Rendi lisamine**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-120">The payment schedule contains the inputs from the **Payment schedule lines** tab on the **Add lease** page.</span></span> <span data-ttu-id="6f8ef-121">Saate iga makse summat ja muutuvat makset endiselt muuta.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-121">You can still change each payment amount and variable payment.</span></span> <span data-ttu-id="6f8ef-122">Rendikohustis arvutatakse muudetud maksegraafiku põhjal.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-122">The lease liability is calculated based on the modified payment schedule.</span></span>

4. <span data-ttu-id="6f8ef-123">Kui olete maksegraafiku läbivaatamise lõpetanud valige **Kinnita graafik**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-123">After you've finished reviewing the payment schedule, select **Confirm schedule**.</span></span> <span data-ttu-id="6f8ef-124">Pärast graafiku kinnitamist pole rendikirje redigeerimiseks enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-124">After the schedule is confirmed, the lease is no longer available for editing.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8ef-125">Süsteem arvutab rendiperioodi lehel **Rendi lisamine** maksegraafiku ridade põhjal automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-125">The system automatically calculates the lease term from the payment schedule lines on the **Add lease** page.</span></span>
    >
    > <span data-ttu-id="6f8ef-126">Rendiperioodi kuudes arvutamiseks leiab süsteem konkreetse maksegraafiku rea jaoks alguskuupäeva ja lõpukuupäeva erinevuse.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-126">To calculate the lease term in months, the system finds the difference between the start date and the end date for a specific payment schedule line.</span></span> <span data-ttu-id="6f8ef-127">Seejärel liigub see järgmisele maksegraafiku reale ja leiab erinevuse uuesti.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-127">It then moves to the next payment schedule line and finds the difference again.</span></span> <span data-ttu-id="6f8ef-128">Lõpuks liidab süsteem kõik summad, et määrata rendiperiood kuudes.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-128">Finally, the system sums all the amounts to determine the lease term in months.</span></span>

5. <span data-ttu-id="6f8ef-129">Arvutatud perioodi intressikulu vaatamiseks avage leht **Kohustise amortiseerimise graafik**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-129">To view the calculated period interest expenses, open the **Liability amortization schedule** page.</span></span> <span data-ttu-id="6f8ef-130">Arvutatud lineaarse kulumi vaatamiseks avage leht **Vara kulumigraafik**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-130">To view calculated straight-line depreciation, open the **Asset depreciation schedule** page.</span></span>
6. <span data-ttu-id="6f8ef-131">Kui olete arvutatud summa läbivaatamise lõpetanud, saate luua lehel **Esialgne tuvastamine** esialgse tuvastamise tööleje kirje.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-131">After you've finished reviewing the calculated amount, you can create the initial recognition journal entry on the **Initial recognition** page.</span></span> <span data-ttu-id="6f8ef-132">Teile kuvatakse teade, et tööleht on loodud.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-132">You receive a message that states that the journal has been created.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8ef-133">Töölehe kirjet ei sisestata pearaamatusse enne, kui sisestate kirje käsitsi.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-133">The journal entry isn't posted to General ledger until you manually post the entry.</span></span>

7. <span data-ttu-id="6f8ef-134">Kui soovite pakutud algse tuvastamise kirje enne sisestamist läbi vaadata, valige **Vara rentimise tööleht**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-134">To review the proposed initial recognition entry before you post it, select **Asset leasing journal**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8ef-135">Vara rentimise töölehte ei saa käsitsi luua.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-135">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="6f8ef-136">See luuakse rendiajakavade loomise ajal automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-136">It's automatically created when lease schedules are created.</span></span>

8. <span data-ttu-id="6f8ef-137">Kui olete algse tuvastamise töölehe kirje läbi vaadanud ja olete valmis selle sisestama, valige suvand **Sisesta**, et tuvastada kasutamisõiguse esemeks olev vara ja rendikohustis pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-137">When you've finished reviewing the initial recognition journal entry and are ready to post it, select **Post** to recognize the right-of-use (ROU) asset and lease liability in General ledger.</span></span>

## <a name="copy-a-lease"></a><span data-ttu-id="6f8ef-138">Rendi kopeerimine</span><span class="sxs-lookup"><span data-stu-id="6f8ef-138">Copy a lease</span></span>

<span data-ttu-id="6f8ef-139">Vara rentimine võimaldab teil kopeerida rendi üksikasjad, et luua uus rendikirje, millel on sama teave.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-139">Asset leasing lets you copy the details of a lease to create a new lease that has the same information.</span></span> <span data-ttu-id="6f8ef-140">Saate seejärel muuta rendikirje välju, enne kui loote kopeeritud rentimise graafiku.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-140">You can then change the lease fields before you create the schedules for the copied lease.</span></span>

1. <span data-ttu-id="6f8ef-141">Valige lehel **Rendikokkuvõte** kopeerimiseks rendikirje ja valige seejärel tegevuspaanil suvand **Kopeeri rendikirje**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-141">On the **Lease summary** page, select the lease to copy, and then, on the Action Pane, select **Copy lease**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6f8ef-142">Kui parameeter **Käsitsi** on rendi ID-de numbriseeria jaoks välja lülitatud, luuakse automaatselt kopeeritud rendikirje rendi ID automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-142">If the **Manual** parameter is turned off for the number sequence for lease IDs, the next number in the sequence is automatically generated as the lease ID of the copied lease.</span></span> <span data-ttu-id="6f8ef-143">Kui parameeter **Käsitsi** on sisse lülitatud, kuvatakse teade, mis palub teil enne müügikirje kopeerimist sisestada rendi ID.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-143">If the **Manual** parameter is turned on, you receive a message that prompts you to enter the lease ID before you proceed to copy the lease.</span></span>

2. <span data-ttu-id="6f8ef-144">Valige suvand **Kopeeri**.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-144">Select **Copy**.</span></span> <span data-ttu-id="6f8ef-145">Valitud rendikirje üksikasjad kopeeritakse uude rendikirjesse.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-145">The lease details from the selected lease are copied to a new lease.</span></span> <span data-ttu-id="6f8ef-146">Seejärel saate muuta uue rendikirje üksikasju, enne kui selle salvestate ja loote rendigraafikud.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-146">You can then edit the details of the new lease before you save it and create the lease schedules.</span></span>

## <a name="asset-leasing-journal"></a><span data-ttu-id="6f8ef-147">Vara rentimise tööleht</span><span class="sxs-lookup"><span data-stu-id="6f8ef-147">Asset leasing journal</span></span>

<span data-ttu-id="6f8ef-148">Kõik vara rentimises loodavad töölehe kanded sisalduvad vara rentimise töölehel.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-148">All journal entries that are created in Asset leasing are contained in the Asset leasing journal.</span></span> <span data-ttu-id="6f8ef-149">Lehel **Vara rentimise tööleht** (**Vara rentimine \> Töölehe kirjed \> Vara rentimise tööleht**) saate filtreerida, sisestades oleku, vaadates kindlaid töölehe kirjeid ja kandeid ning sisestada sisestamata töölehe kirjed.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-149">On the **Asset leasing journal** page (**Asset leasing \> Journal entries \> Asset leasing journal**), you can filter by posting status, view specific journal entries and the vouchers, and post unposted journal entries.</span></span>

> [!NOTE]
> <span data-ttu-id="6f8ef-150">Vara rentimise töölehte ei saa käsitsi luua.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-150">The Asset leasing journal can't be created manually.</span></span> <span data-ttu-id="6f8ef-151">See luuakse rendiajakavade loomise ajal automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6f8ef-151">It's automatically created when lease schedules are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]