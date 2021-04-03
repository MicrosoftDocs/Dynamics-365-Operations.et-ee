---
title: Laokannete arhiivimine
description: Selles teema kirjeldatakse, kuidas arhiveerida laokannete andmeid süsteemi jõudluse parandamiseks.
author: sherry-zheng
manager: tfehr
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 3a0fa65eb728e4ce96bdfc3f7a0f04901551ccea
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556415"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="f42f2-103">Laokannete arhiivimine</span><span class="sxs-lookup"><span data-stu-id="f42f2-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f42f2-104">Laokannete tabel (`InventTrans`) kasvab aja jooksul pidevalt ja kasutab aina rohkem andmebaasiruumi.</span><span class="sxs-lookup"><span data-stu-id="f42f2-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="f42f2-105">Seetõttu muutuvad tabeli kohta tehtud päringud järk-järgult aeglasemaks.</span><span class="sxs-lookup"><span data-stu-id="f42f2-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="f42f2-106">Selles teemas kirjeldatakse, kuidas te saate kasutada *laokannete arhiivi* funktsiooni laokannete andmete arhiveerimiseks, et parandada süsteemi jõudlust.</span><span class="sxs-lookup"><span data-stu-id="f42f2-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="f42f2-107">Valitud suletud pearaamatu perioodi jooksul saab arhiveerida ainult finantsiliselt värskendatud laokandeid.</span><span class="sxs-lookup"><span data-stu-id="f42f2-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="f42f2-108">Arhiivimiseks peavad finantsiliselt uuendatud väljaminevate laokannete väljamineku olek olema *Müüdud* ja sissetulevate laokannete sissetuleku olek peab olema *Ostetud*.</span><span class="sxs-lookup"><span data-stu-id="f42f2-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="f42f2-109">Laokannete arhiivimisel teisaldatakse kõik seonduvad kanded tabelisse `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="f42f2-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="f42f2-110">Lao väljaminekukanded ja lao sissetulekukanded arhiveeritakse eraldi kauba ID (`itemId`) ja laodimensiooni ID (`inventDimId`) kombinatsiooni alusel ning pannakse summeeritud väljamineku ja summeeritud sissetuleku kannete hulka.</span><span class="sxs-lookup"><span data-stu-id="f42f2-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="f42f2-111">Kui üks `itemId` ja `inventDimId` kombinatsioon sisaldab ainult ühte sissetuleku- või väljaminekukannet, siis kannet ei arhiivita.</span><span class="sxs-lookup"><span data-stu-id="f42f2-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="f42f2-112">Funktsiooni sisselülitamine teie süsteemis</span><span class="sxs-lookup"><span data-stu-id="f42f2-112">Turn on the feature in your system</span></span>

<span data-ttu-id="f42f2-113">Kui teie süsteemis ei ole veel selles teemas kirjeldatud funktsioone, avage [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) ja lülitage funktsioon *Laokannete arhiiv* sisse.</span><span class="sxs-lookup"><span data-stu-id="f42f2-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="f42f2-114">Mida on vaja enne laokannete arhiivimist arvesse võtta</span><span class="sxs-lookup"><span data-stu-id="f42f2-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="f42f2-115">Enne laokannete arhiivimist peaksite arvestama järgmiste äristsenaariumiga, sest see toiming mõjutab neid:</span><span class="sxs-lookup"><span data-stu-id="f42f2-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="f42f2-116">Kui auditeerite laokandeid seonduvatest dokumentidest, nt ostutellimuse ridadest, kuvatakse need arhiivitud kannetena.</span><span class="sxs-lookup"><span data-stu-id="f42f2-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="f42f2-117">Arhiveeritud kannete ülevaatamiseks peate avama kausta **Laovarude haldus \> Perioodilised ülesanded \> Puhastamine \> Laokannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="f42f2-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="f42f2-118">Lao sulgemist ei saa arhiivitud perioodide puhul tühistada.</span><span class="sxs-lookup"><span data-stu-id="f42f2-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="f42f2-119">Enne, kui saate lao sulgemise tühistada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="f42f2-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="f42f2-120">Standardkulu teisendamist ei saa arhiivitud perioodideks teha.</span><span class="sxs-lookup"><span data-stu-id="f42f2-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="f42f2-121">Enne, kui saate standardkulu teisendada, peate tagasi pöörama laokannete arhiivi vastava perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="f42f2-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="f42f2-122">Laokannete arhiivimine mõjutab laokannetest hangitud laoaruandeid.</span><span class="sxs-lookup"><span data-stu-id="f42f2-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="f42f2-123">Need aruanded sisaldavad laovarude ajalise jaotuse aruannet ja laovarude väärtuse aruandeid.</span><span class="sxs-lookup"><span data-stu-id="f42f2-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="f42f2-124">Laovarude prognoose võib mõjutada nende käitamine arhiveeritud perioodide perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="f42f2-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f42f2-125">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="f42f2-125">Prerequisites</span></span>

<span data-ttu-id="f42f2-126">Laokandeid saab arhiveerida ainult neil perioodidel, mille puhul on täidetud järgmised tingimused:</span><span class="sxs-lookup"><span data-stu-id="f42f2-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="f42f2-127">Pearaamatu periood peab olema suletud.</span><span class="sxs-lookup"><span data-stu-id="f42f2-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="f42f2-128">Lao sulgemine peab olema käitatud arhiivi perioodi lõppkuupäeval või pärast seda.</span><span class="sxs-lookup"><span data-stu-id="f42f2-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="f42f2-129">Periood peab olema vähemalt üks aasta enne arhiivi perioodi alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="f42f2-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="f42f2-130">Varude ümberarvutusi ei tohi olla.</span><span class="sxs-lookup"><span data-stu-id="f42f2-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="f42f2-131">Laokannete arhiivimine</span><span class="sxs-lookup"><span data-stu-id="f42f2-131">Archive inventory transactions</span></span>

<span data-ttu-id="f42f2-132">Laokannete arhiivimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f42f2-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="f42f2-133">Avage kaust **Varude haldus** \> **Perioodilised ülesanded** \> **Puhastamine** \> **Laokannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="f42f2-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="f42f2-134">Kuvatakse leht **Laokannete arhiiv** ja sellel kuvatakse arhiivitud protsessikirjete loend.</span><span class="sxs-lookup"><span data-stu-id="f42f2-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="f42f2-135">![Laokannete arhiivi leht](media/archive-inventory-empty.png "Laokannete arhiivi leht")</span><span class="sxs-lookup"><span data-stu-id="f42f2-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="f42f2-136">Valige tegevuspaanil laokannete arhiivi loomiseks **Laokannete arhiiv**.</span><span class="sxs-lookup"><span data-stu-id="f42f2-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="f42f2-137">Seadke dialoogiboksis **Laokannete arhiiv** kiirkaardil **Parameetrid** järgmised väljad:</span><span class="sxs-lookup"><span data-stu-id="f42f2-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="f42f2-138">**Suletud pearaamatu perioodi alguskuupäev** – valige varaseim kande kuupäev arhiivi kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="f42f2-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="f42f2-139">**Suletud pearaamatu perioodi lõppkuupäev** – valige hiliseim kande kuupäev arhiivi kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="f42f2-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="f42f2-140">![Laokannete arhiivi dialoogiboks](media/archive-inventory-dates.png "Laokannete arhiivi dialoogiboks")</span><span class="sxs-lookup"><span data-stu-id="f42f2-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="f42f2-141">Valida saab ainult [eeltingimustele](#prerequisites) vastavad perioodid.</span><span class="sxs-lookup"><span data-stu-id="f42f2-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="f42f2-142">Seadistage kiirkaardil **Käivita taustal** pakett-töötluse üksikasjad vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="f42f2-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="f42f2-143">Järgige teenuse Microsoft Dynamics 365 Supply Chain Management tavalisi pakett-tööde etappe.</span><span class="sxs-lookup"><span data-stu-id="f42f2-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="f42f2-144">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f42f2-144">Select **OK**.</span></span>
1. <span data-ttu-id="f42f2-145">Saate teate, mis palub teil kinnitada, et soovite jätkata.</span><span class="sxs-lookup"><span data-stu-id="f42f2-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="f42f2-146">Lugege teade hoolikalt läbi ja valige vastus **Jah**, kui soovite jätkata.</span><span class="sxs-lookup"><span data-stu-id="f42f2-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="f42f2-147">Saate teate, et teie laokannete arhiivitöö on lisatud pakett-töötluse järjekorda.</span><span class="sxs-lookup"><span data-stu-id="f42f2-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="f42f2-148">Töö alustab nüüd valitud perioodi laokannete arhiivimist.</span><span class="sxs-lookup"><span data-stu-id="f42f2-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="f42f2-149">Kuva arhiivitud varude kanded</span><span class="sxs-lookup"><span data-stu-id="f42f2-149">View archived inventory transactions</span></span>

<span data-ttu-id="f42f2-150">Lehel **Laokannete arhiiv** kuvatakse teie täielik arhiivimisajalugu.</span><span class="sxs-lookup"><span data-stu-id="f42f2-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="f42f2-151">Igal ruudustiku real kuvatakse selline teave nagu arhiivi loomise kuupäev, arhiivi loonud kasutaja ja selle olek.</span><span class="sxs-lookup"><span data-stu-id="f42f2-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="f42f2-152">![Arhiivimisajalugu lehel Laokannete arhiivimine](media/archive-inventory-full.png "Arhiivimisajalugu lehel Laokannete arhiivimine")</span><span class="sxs-lookup"><span data-stu-id="f42f2-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="f42f2-153">Valige ruudustikus kuvatavate arhiivide filtreerimiseks lehe ülaosas asuvast ripploendist üks järgmistest väärtustest:</span><span class="sxs-lookup"><span data-stu-id="f42f2-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="f42f2-154">**Aktiivne** – kuvatakse ainult aktiivsed arhiivid, mitte tagasipööratud arhiivid.</span><span class="sxs-lookup"><span data-stu-id="f42f2-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="f42f2-155">**Kõik** – kuvatakse kõik arhiivid, nii aktiivsed kui ka tagasipööratud.</span><span class="sxs-lookup"><span data-stu-id="f42f2-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="f42f2-156">Iga arhiivi kohta ruudustikus esitatakse järgmine teave:</span><span class="sxs-lookup"><span data-stu-id="f42f2-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="f42f2-157">**Aktiivne** – märge näitab, et arhiiv on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="f42f2-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="f42f2-158">**Alguskuupäev** – vanima kande kuupäev, mille saab arhiivi kaasata.</span><span class="sxs-lookup"><span data-stu-id="f42f2-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="f42f2-159">**Lõppkuupäev** – uusima kande kuupäev, mille saab arhiivi kaasata.</span><span class="sxs-lookup"><span data-stu-id="f42f2-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="f42f2-160">**Planeerija** – arhiivi loonud kasutajakonto.</span><span class="sxs-lookup"><span data-stu-id="f42f2-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="f42f2-161">**Teostatud** – arhiivi loomise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="f42f2-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="f42f2-162">**Tagasipööratud** – märge näitab, et arhiiv on tagasi pööratud.</span><span class="sxs-lookup"><span data-stu-id="f42f2-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="f42f2-163">**Peata praegune uuendus** – märge näitab, et arhiivimine on pooleli, kuid see on peatatud.</span><span class="sxs-lookup"><span data-stu-id="f42f2-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="f42f2-164">**Olek** – arhiivi töötlemise olek.</span><span class="sxs-lookup"><span data-stu-id="f42f2-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="f42f2-165">Võimalikud väärtused on *Ootel*, *Pooleli* ja *Lõpetatud*.</span><span class="sxs-lookup"><span data-stu-id="f42f2-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="f42f2-166">Ruudustiku kohal tööriistaribal on järgmised nupud, mida saate kasutada valitud arhiiviga töötamiseks:</span><span class="sxs-lookup"><span data-stu-id="f42f2-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="f42f2-167">**Arhiivitud kanded** – saate vaadata valitud arhiivi kõiki üksikasju.</span><span class="sxs-lookup"><span data-stu-id="f42f2-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="f42f2-168">Ilmuval lehel **Arhiivitud kanded** kuvatakse kõik arhiivis olevad kanded.</span><span class="sxs-lookup"><span data-stu-id="f42f2-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="f42f2-169">![Leht Arhiivitud kanded](media/archive-inventory-transactions.png "Leht Arhiivitud kanded")</span><span class="sxs-lookup"><span data-stu-id="f42f2-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="f42f2-170">Konkreetse kande kohta lisateabe vaatamiseks lehel **Arhiveeritud kanded** valige see ruudustikus ja seejärel valige tegevuspaanil **Arhiivitud kande üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="f42f2-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="f42f2-171">Ilmuval lehel **Arhiivitud kande üksikasjad** kuvatakse selline teave nagu pearaamatu sisestamine, seotud alammooduli viited ja finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="f42f2-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="f42f2-172">**Peata arhiivimine** – saate peatada praegu töödeldava valitud arhiivi.</span><span class="sxs-lookup"><span data-stu-id="f42f2-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="f42f2-173">Peatamine jõustub alles pärast arhiivimisülesande loomist.</span><span class="sxs-lookup"><span data-stu-id="f42f2-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="f42f2-174">Seega võib peatamise jõustumine toimuda viivitusega.</span><span class="sxs-lookup"><span data-stu-id="f42f2-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="f42f2-175">Kui arhiiv on peatatud, kuvatakse väljal **Peata praegune uuendus** märge.</span><span class="sxs-lookup"><span data-stu-id="f42f2-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="f42f2-176">**Jätka arhiivimist** – saate jätkata praegu peatatud valitud arhiivi töötlemist.</span><span class="sxs-lookup"><span data-stu-id="f42f2-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="f42f2-177">**Pööra tagasi** – saate valitud arhiivi tagasi pöörata.</span><span class="sxs-lookup"><span data-stu-id="f42f2-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="f42f2-178">Arhiivi saate tagasi pöörata ainult siis, kui selle välja **Olek** väärtuseks on seatud *Lõpetatud*.</span><span class="sxs-lookup"><span data-stu-id="f42f2-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="f42f2-179">Kui arhiiv on tagasi pööratud, kuvatakse väljal **Tagasipööratud** märge.</span><span class="sxs-lookup"><span data-stu-id="f42f2-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
