---
title: Laokannete arhiivimine
description: Selles teema kirjeldatakse, kuidas arhiveerida laokannete andmeid süsteemi jõudluse parandamiseks.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 0526eb42a886817d50e1ecfd252a6e971875ba92
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956054"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="93cfb-103">Laokannete arhiivimine</span><span class="sxs-lookup"><span data-stu-id="93cfb-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93cfb-104">Laokannete tabel (`InventTrans`) kasvab aja jooksul pidevalt ja kasutab aina rohkem andmebaasiruumi.</span><span class="sxs-lookup"><span data-stu-id="93cfb-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="93cfb-105">Seetõttu muutuvad tabeli kohta tehtud päringud järk-järgult aeglasemaks.</span><span class="sxs-lookup"><span data-stu-id="93cfb-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="93cfb-106">Selles teemas kirjeldatakse, kuidas te saate kasutada *laokannete arhiivi* funktsiooni laokannete andmete arhiveerimiseks, et parandada süsteemi jõudlust.</span><span class="sxs-lookup"><span data-stu-id="93cfb-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="93cfb-107">Valitud suletud pearaamatu perioodi jooksul saab arhiveerida ainult finantsiliselt värskendatud laokandeid.</span><span class="sxs-lookup"><span data-stu-id="93cfb-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="93cfb-108">Arhiivimiseks peavad finantsiliselt uuendatud väljaminevate laokannete väljamineku olek olema *Müüdud* ja sissetulevate laokannete sissetuleku olek peab olema *Ostetud*.</span><span class="sxs-lookup"><span data-stu-id="93cfb-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="93cfb-109">Laokannete arhiivimisel teisaldatakse kõik seonduvad kanded tabelisse `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="93cfb-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="93cfb-110">Lao väljaminekukanded ja lao sissetulekukanded arhiveeritakse eraldi kauba ID (`itemId`) ja laodimensiooni ID (`inventDimId`) kombinatsiooni alusel ning pannakse summeeritud väljamineku ja summeeritud sissetuleku kannete hulka.</span><span class="sxs-lookup"><span data-stu-id="93cfb-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="93cfb-111">Kui üks `itemId` ja `inventDimId` kombinatsioon sisaldab ainult ühte sissetuleku- või väljaminekukannet, siis kannet ei arhiivita.</span><span class="sxs-lookup"><span data-stu-id="93cfb-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="93cfb-112">Funktsiooni sisselülitamine teie süsteemis</span><span class="sxs-lookup"><span data-stu-id="93cfb-112">Turn on the feature in your system</span></span>

<span data-ttu-id="93cfb-113">Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage funktsioon *Laokannete arhiiv* sisse.</span><span class="sxs-lookup"><span data-stu-id="93cfb-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span> <span data-ttu-id="93cfb-114">Pange tähele, et seda funktsiooni ei saa pärast lubamist enam keelata.</span><span class="sxs-lookup"><span data-stu-id="93cfb-114">Note that this feature cannot be disabled once it has been enabled.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="93cfb-115">Mida on vaja enne laokannete arhiivimist arvesse võtta</span><span class="sxs-lookup"><span data-stu-id="93cfb-115">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="93cfb-116">Enne laokannete arhiivimist peaksite arvestama järgmiste äristsenaariumiga, sest see toiming mõjutab neid:</span><span class="sxs-lookup"><span data-stu-id="93cfb-116">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="93cfb-117">Kui auditeerite laokandeid seonduvatest dokumentidest, nt ostutellimuse ridadest, kuvatakse need arhiivitud kannetena.</span><span class="sxs-lookup"><span data-stu-id="93cfb-117">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="93cfb-118">Arhiveeritud kannete ülevaatamiseks peate avama kausta **Laovarude haldus \> Perioodilised ülesanded \> Puhastamine \> Laokannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="93cfb-118">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="93cfb-119">Lao sulgemist ei saa arhiivitud perioodide puhul tühistada.</span><span class="sxs-lookup"><span data-stu-id="93cfb-119">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="93cfb-120">Enne, kui saate lao sulgemise tühistada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="93cfb-120">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="93cfb-121">Standardkulu teisendamist ei saa arhiivitud perioodideks teha.</span><span class="sxs-lookup"><span data-stu-id="93cfb-121">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="93cfb-122">Enne, kui saate standardkulu teisendada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="93cfb-122">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="93cfb-123">Laokannete arhiivimine mõjutab laokannetest hangitud laoaruandeid.</span><span class="sxs-lookup"><span data-stu-id="93cfb-123">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="93cfb-124">Need aruanded sisaldavad laovarude ajalise jaotuse aruannet ja laovarude väärtuse aruandeid.</span><span class="sxs-lookup"><span data-stu-id="93cfb-124">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="93cfb-125">Laovarude prognoose võib mõjutada nende käitamine arhiveeritud perioodide perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="93cfb-125">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="93cfb-126">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="93cfb-126">Prerequisites</span></span>

<span data-ttu-id="93cfb-127">Laokandeid saab arhiveerida ainult neil perioodidel, mille puhul on täidetud järgmised tingimused:</span><span class="sxs-lookup"><span data-stu-id="93cfb-127">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="93cfb-128">Pearaamatu periood peab olema suletud.</span><span class="sxs-lookup"><span data-stu-id="93cfb-128">The ledger period must be closed.</span></span>
- <span data-ttu-id="93cfb-129">Lao sulgemine peab olema käitatud arhiivi perioodi lõppkuupäeval või pärast seda.</span><span class="sxs-lookup"><span data-stu-id="93cfb-129">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="93cfb-130">Periood peab olema vähemalt üks aasta enne arhiivi perioodi alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="93cfb-130">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="93cfb-131">Varude ümberarvutusi ei tohi olla.</span><span class="sxs-lookup"><span data-stu-id="93cfb-131">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="93cfb-132">Laokannete arhiivimine</span><span class="sxs-lookup"><span data-stu-id="93cfb-132">Archive inventory transactions</span></span>

<span data-ttu-id="93cfb-133">Laokannete arhiivimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="93cfb-133">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="93cfb-134">Avage kaust **Varude haldus** \> **Perioodilised ülesanded** \> **Puhastamine** \> **Laokannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="93cfb-134">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="93cfb-135">Kuvatakse leht **Laokannete arhiiv** ja sellel kuvatakse arhiivitud protsessikirjete loend.</span><span class="sxs-lookup"><span data-stu-id="93cfb-135">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="93cfb-136">![Laokannete arhiivi leht](media/archive-inventory-empty.png "Laokannete arhiivi leht")</span><span class="sxs-lookup"><span data-stu-id="93cfb-136">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="93cfb-137">Valige tegevuspaanil laokannete arhiivi loomiseks **Laokannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="93cfb-137">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="93cfb-138">Seadke dialoogiboksis **Laokannete arhiiv** kiirkaardil **Parameetrid** järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="93cfb-138">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="93cfb-139">**Suletud pearaamatu perioodi alguskuupäev** – valige varaseim kande kuupäev arhiivi kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="93cfb-139">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="93cfb-140">**Suletud pearaamatu perioodi lõppkuupäev** – valige hiliseim kande kuupäev arhiivi kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="93cfb-140">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="93cfb-141">![Laokannete arhiivi dialoogiboks](media/archive-inventory-dates.png "Laokannete arhiivi dialoogiboks")</span><span class="sxs-lookup"><span data-stu-id="93cfb-141">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="93cfb-142">Valida saab ainult [eeltingimustele](#prerequisites) vastavad perioodid.</span><span class="sxs-lookup"><span data-stu-id="93cfb-142">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="93cfb-143">Seadistage kiirkaardil **Käivita taustal** pakett-töötluse üksikasjad vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="93cfb-143">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="93cfb-144">Järgige teenuse Microsoft Dynamics 365 Supply Chain Management tavalisi pakett-tööde etappe.</span><span class="sxs-lookup"><span data-stu-id="93cfb-144">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="93cfb-145">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="93cfb-145">Select **OK**.</span></span>
1. <span data-ttu-id="93cfb-146">Saate teate, mis palub teil kinnitada, et soovite jätkata.</span><span class="sxs-lookup"><span data-stu-id="93cfb-146">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="93cfb-147">Lugege teade hoolikalt läbi ja valige vastus **Jah**, kui soovite jätkata.</span><span class="sxs-lookup"><span data-stu-id="93cfb-147">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="93cfb-148">Saate teate, et teie laokannete arhiivitöö on lisatud pakett-töötluse järjekorda.</span><span class="sxs-lookup"><span data-stu-id="93cfb-148">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="93cfb-149">Töö alustab nüüd valitud perioodi laokannete arhiivimist.</span><span class="sxs-lookup"><span data-stu-id="93cfb-149">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="93cfb-150">Kuva arhiivitud varude kanded</span><span class="sxs-lookup"><span data-stu-id="93cfb-150">View archived inventory transactions</span></span>

<span data-ttu-id="93cfb-151">Lehel **Laokannete arhiiv** kuvatakse teie täielik arhiivimisajalugu.</span><span class="sxs-lookup"><span data-stu-id="93cfb-151">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="93cfb-152">Igal ruudustiku real kuvatakse selline teave nagu arhiivi loomise kuupäev, arhiivi loonud kasutaja ja selle olek.</span><span class="sxs-lookup"><span data-stu-id="93cfb-152">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="93cfb-153">![Arhiivimisajalugu lehel Laokannete arhiivimine](media/archive-inventory-full.png "Arhiivimisajalugu lehel Laokannete arhiivimine")</span><span class="sxs-lookup"><span data-stu-id="93cfb-153">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="93cfb-154">Valige ruudustikus kuvatavate arhiivide filtreerimiseks lehe ülaosas asuvast ripploendist üks järgmistest väärtustest:</span><span class="sxs-lookup"><span data-stu-id="93cfb-154">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="93cfb-155">**Aktiivne** – kuvatakse ainult aktiivsed arhiivid, mitte tagasipööratud arhiivid.</span><span class="sxs-lookup"><span data-stu-id="93cfb-155">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="93cfb-156">**Kõik** – kuvatakse kõik arhiivid, nii aktiivsed kui ka tagasipööratud.</span><span class="sxs-lookup"><span data-stu-id="93cfb-156">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="93cfb-157">Iga arhiivi kohta ruudustikus esitatakse järgmine teave:</span><span class="sxs-lookup"><span data-stu-id="93cfb-157">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="93cfb-158">**Aktiivne** – märge näitab, et arhiiv on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="93cfb-158">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="93cfb-159">**Alguskuupäev** – vanima kande kuupäev, mille saab arhiivi kaasata.</span><span class="sxs-lookup"><span data-stu-id="93cfb-159">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="93cfb-160">**Lõppkuupäev** – uusima kande kuupäev, mille saab arhiivi kaasata.</span><span class="sxs-lookup"><span data-stu-id="93cfb-160">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="93cfb-161">**Planeerija** – arhiivi loonud kasutajakonto.</span><span class="sxs-lookup"><span data-stu-id="93cfb-161">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="93cfb-162">**Teostatud** – arhiivi loomise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="93cfb-162">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="93cfb-163">**Tagasipööratud** – märge näitab, et arhiiv on tagasi pööratud.</span><span class="sxs-lookup"><span data-stu-id="93cfb-163">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="93cfb-164">**Peata praegune uuendus** – märge näitab, et arhiivimine on pooleli, kuid see on peatatud.</span><span class="sxs-lookup"><span data-stu-id="93cfb-164">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="93cfb-165">**Olek** – arhiivi töötlemise olek.</span><span class="sxs-lookup"><span data-stu-id="93cfb-165">**State** – The processing status of the archive.</span></span> <span data-ttu-id="93cfb-166">Võimalikud väärtused on *Ootel*, *Pooleli* ja *Lõpetatud*.</span><span class="sxs-lookup"><span data-stu-id="93cfb-166">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="93cfb-167">Ruudustiku kohal tööriistaribal on järgmised nupud, mida saate kasutada valitud arhiiviga töötamiseks:</span><span class="sxs-lookup"><span data-stu-id="93cfb-167">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="93cfb-168">**Arhiivitud kanded** – saate vaadata valitud arhiivi kõiki üksikasju.</span><span class="sxs-lookup"><span data-stu-id="93cfb-168">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="93cfb-169">Ilmuval lehel **Arhiivitud kanded** kuvatakse kõik arhiivis olevad kanded.</span><span class="sxs-lookup"><span data-stu-id="93cfb-169">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="93cfb-170">![Leht Arhiivitud kanded](media/archive-inventory-transactions.png "Leht Arhiivitud kanded")</span><span class="sxs-lookup"><span data-stu-id="93cfb-170">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="93cfb-171">Konkreetse kande kohta lisateabe vaatamiseks lehel **Arhiveeritud kanded** valige see ruudustikus ja seejärel valige tegevuspaanil **Arhiivitud kande üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="93cfb-171">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="93cfb-172">Ilmuval lehel **Arhiivitud kande üksikasjad** kuvatakse selline teave nagu pearaamatu sisestamine, seotud alammooduli viited ja finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="93cfb-172">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="93cfb-173">**Peata arhiivimine** – saate peatada praegu töödeldava valitud arhiivi.</span><span class="sxs-lookup"><span data-stu-id="93cfb-173">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="93cfb-174">Peatamine jõustub alles pärast arhiivimisülesande loomist.</span><span class="sxs-lookup"><span data-stu-id="93cfb-174">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="93cfb-175">Seega võib peatamise jõustumine toimuda viivitusega.</span><span class="sxs-lookup"><span data-stu-id="93cfb-175">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="93cfb-176">Kui arhiiv on peatatud, kuvatakse väljal **Peata praegune uuendus** märge.</span><span class="sxs-lookup"><span data-stu-id="93cfb-176">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="93cfb-177">**Jätka arhiivimist** – saate jätkata praegu peatatud valitud arhiivi töötlemist.</span><span class="sxs-lookup"><span data-stu-id="93cfb-177">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="93cfb-178">**Pööra tagasi** – saate valitud arhiivi tagasi pöörata.</span><span class="sxs-lookup"><span data-stu-id="93cfb-178">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="93cfb-179">Arhiivi saate tagasi pöörata ainult siis, kui selle välja **Olek** väärtuseks on seatud *Lõpetatud*.</span><span class="sxs-lookup"><span data-stu-id="93cfb-179">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="93cfb-180">Kui arhiiv on tagasi pööratud, kuvatakse väljal **Tagasipööratud** märge.</span><span class="sxs-lookup"><span data-stu-id="93cfb-180">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
