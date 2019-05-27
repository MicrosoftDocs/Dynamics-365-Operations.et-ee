---
title: Pearaamatu tasakaalustused
description: Selles teemas kirjeldatakse, kuidas kasutada pearaamatu tasakaalustuste lehte pearaamatukannete tasakaalustamiseks ja taskaalustuste tühistamiseks.
author: mikefalkner
manager: aolson
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTransSettlement
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-11-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: b02a1a066913c9959e9a55e78789e5ff1a175c56
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1554686"
---
# <a name="ledger-settlements"></a><span data-ttu-id="a243b-103">Pearaamatu tasakaalustused</span><span class="sxs-lookup"><span data-stu-id="a243b-103">Ledger settlements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a243b-104">Pearaamatu tasakaalustustega saate sobitada deebet- ja krediitkandeid pearaamatus ning märkida need tasakaalustatuks.</span><span class="sxs-lookup"><span data-stu-id="a243b-104">Ledger settlements let you match debit and credit transactions in the general ledger, and mark them as settled.</span></span> <span data-ttu-id="a243b-105">Sel viisil saate veenduda, et seotud kanded on tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="a243b-105">In this way, you can make sure that related transactions have been cleared.</span></span> <span data-ttu-id="a243b-106">Saate ka tühistada ekslikult tehtud tasakaalustusi.</span><span class="sxs-lookup"><span data-stu-id="a243b-106">You can also reverse settlements if they were made by mistake.</span></span>

## <a name="enable-advanced-ledger-settlements"></a><span data-ttu-id="a243b-107">Luba laiendatud pearaamatu tasakaalustamised</span><span class="sxs-lookup"><span data-stu-id="a243b-107">Enable advanced ledger settlements</span></span>

<span data-ttu-id="a243b-108">Laiendatud pearaamatu tasakaalustuste leht pakub lisavõimalusi kannete filtreerimiseks ja valimiseks.</span><span class="sxs-lookup"><span data-stu-id="a243b-108">The advanced ledger settlements page provides additional capabilities for filtering and selecting transactions.</span></span> <span data-ttu-id="a243b-109">Laiendatud pearaamatu tasakaalustuste lehe lubamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a243b-109">To enable advanced ledger settlements page, follow these steps.</span></span>

1. <span data-ttu-id="a243b-110">Valige **Pearaamat** \> **Pearaamatu seadistamine** \> **Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="a243b-110">Select **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span> 
2. <span data-ttu-id="a243b-111">Laiendatud pearaamatu tasakaalustamise funktsiooni sisselülitamiseks määrake **Pearaamatu tasakaalustuste** vahekaardil **Laiendatud pearaamatu tasakaalustamised** suvandiks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a243b-111">On the **Ledger settlements** tab, set the **Advanced ledger settlement** option to **Yes** to turn on the advanced ledger settlement functionality.</span></span> <span data-ttu-id="a243b-112">Laiendatud **Pearaamatu tasakaalustuste** lehte kasutatakse, kui valite **Pearaamatu tasakaalustused** suvandis **Perioodilisi toiminguid**.</span><span class="sxs-lookup"><span data-stu-id="a243b-112">The advanced **Ledger settlements** page will be used when you select **Ledger settlements** in the **Periodic tasks**.</span></span> 
3. <span data-ttu-id="a243b-113">Peate iga kontoplaani jaoks sisestama pearaamatu tasakaalustamiseks kasutatavate kontode loendi.</span><span class="sxs-lookup"><span data-stu-id="a243b-113">You must enter the list of accounts to use for ledger settlements for each chart of accounts.</span></span> <span data-ttu-id="a243b-114">Seda loendit kasutatakse kannete loendi filtreerimiseks, mis kuvatakse **Pearaamatu tasakaalustuste** leheküljel.</span><span class="sxs-lookup"><span data-stu-id="a243b-114">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span> <span data-ttu-id="a243b-115">Valige **Kontoplaani** loendis kontoplaan ja seejärel valige uute kontode loendisse lisamiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a243b-115">In the **Chart of accounts** list, select a chart of accounts, and then select **New** to add new accounts to the list.</span></span>

## <a name="settle-transactions-by-using-the-advanced-ledger-settlements-page"></a><span data-ttu-id="a243b-116">Tasakaalustage kanded laiendatud pearaamatu tasakaalustuste lehega</span><span class="sxs-lookup"><span data-stu-id="a243b-116">Settle transactions by using the advanced ledger settlements page</span></span>

<span data-ttu-id="a243b-117">Pearaamatu kannete tasakaalustamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="a243b-117">To settle ledger transactions, follow these steps.</span></span>

1. <span data-ttu-id="a243b-118">Valige **Pearaamat** \> **Perioodilised ülesanded** \> **Pearaamatu tasakaalustused**.</span><span class="sxs-lookup"><span data-stu-id="a243b-118">Select **General ledger** \> **Periodic tasks** \> **Ledger settlements**.</span></span>
2. <span data-ttu-id="a243b-119">Seadke filtrid lehe ülaosas.</span><span class="sxs-lookup"><span data-stu-id="a243b-119">Set the filters at the top of the page:</span></span>

    - <span data-ttu-id="a243b-120">Valige kuupäevavahemik või **Kuupäevaintervalli kood** automaatseks kuupäevavahemiku täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="a243b-120">Select a date range, or select **Date interval code** to automatically fill in the date range.</span></span>
    - <span data-ttu-id="a243b-121">Muutke vajadusel sisestamiskihti.</span><span class="sxs-lookup"><span data-stu-id="a243b-121">Change the posting layer as you require.</span></span>
    - <span data-ttu-id="a243b-122">Pearaamatukonto ja dimensiooni eraldi kuvamiseks valige määratud finantsdimensioon.</span><span class="sxs-lookup"><span data-stu-id="a243b-122">To show the ledger account and dimensions separately, select a financial dimension set.</span></span>

3. <span data-ttu-id="a243b-123">Valige **Kuva kanded**, et kuvada kõik kanded, mis vastavad seatud filtritele ja eelmises jaotises kontoplaani loomisel määratud kontode loendile.</span><span class="sxs-lookup"><span data-stu-id="a243b-123">Select **Display transactions** to show all the transactions that match the filters that you set and the list of accounts that you specified when you set up the chart of accounts list in the previous section.</span></span> <span data-ttu-id="a243b-124">Filtrite või dimensioonikogumite muutmisel peate uuesti valima **Kuva kanded**.</span><span class="sxs-lookup"><span data-stu-id="a243b-124">If you change any of the filters or the dimension sets, you must select **Display transactions** again.</span></span>
4. <span data-ttu-id="a243b-125">Valige üks või mitu rida, mida soovite tasakaalustada.</span><span class="sxs-lookup"><span data-stu-id="a243b-125">Select one or more lines that you're considering for settlement.</span></span> <span data-ttu-id="a243b-126">Välja **Valitud summa** väärtus lehe ülaosas suureneb või kahaneb vastavalt valitud ridade kogusummale.</span><span class="sxs-lookup"><span data-stu-id="a243b-126">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
5. <span data-ttu-id="a243b-127">Pärast kannete valimise lõpetamist valige **Märgi valituks**.</span><span class="sxs-lookup"><span data-stu-id="a243b-127">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="a243b-128">Iga valitud kande eest ilmub **Märgistatud** veergu linnuke.</span><span class="sxs-lookup"><span data-stu-id="a243b-128">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="a243b-129">Lisaks, välja **Märgistatud summa** väärtus ruudustiku kohal suureneb või kahaneb vastavalt märgistatud ridade kogusummale.</span><span class="sxs-lookup"><span data-stu-id="a243b-129">Additionally, the value of the **Marked amount** field above the grid increases or decreases by the total amount on the lines that you marked.</span></span>
6. <span data-ttu-id="a243b-130">Kui **Märgistatud summa** väärtus on **0** (null), valige **Märgistatud kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="a243b-130">When the **Marked amount** value is **0** (zero), select **Settle marked transactions**.</span></span> <span data-ttu-id="a243b-131">Märgistatud kannete olek uuendatakse olekule **Tasakaalustatud**.</span><span class="sxs-lookup"><span data-stu-id="a243b-131">The status of the marked transactions is updated to **Settled**.</span></span>

## <a name="make-transactions-easier-to-find"></a><span data-ttu-id="a243b-132">Muudke kannete leidmine lihtsamaks</span><span class="sxs-lookup"><span data-stu-id="a243b-132">Make transactions easier to find</span></span>

<span data-ttu-id="a243b-133">**Pearaamatu tasakaalustuste** leht sisaldab funktsioone, mis hõlbustavad tasakaalustamist vajavate kannete nägemist.</span><span class="sxs-lookup"><span data-stu-id="a243b-133">The **Ledger settlements** page includes capabilities that make it easier to see the transactions that you need for settlement.</span></span>

- <span data-ttu-id="a243b-134">Nupp **Tühista valik** tühjendab **Märgistatud** välja kõigist valitud ridadest.</span><span class="sxs-lookup"><span data-stu-id="a243b-134">The **Unmark selected** button clears the **Marked** field for all lines that are selected.</span></span>
- <span data-ttu-id="a243b-135">**Märgistatud** filtri abil saate filtreerida kandeid vastavalt sellele, kas nende **Märgistatud** väli on valitud või tühjendatud.</span><span class="sxs-lookup"><span data-stu-id="a243b-135">The **Marked** filter lets you filter transactions based on whether the **Marked** field for them is selected or cleared.</span></span>
- <span data-ttu-id="a243b-136">**Oleku** filtri abil saate filtreerida kandeid vastavalt sellele, kas nende olek on **Tasakaalustatud** või **Tasakaalustamata**.</span><span class="sxs-lookup"><span data-stu-id="a243b-136">The **Status** filter lets you filter transactions based on whether their status is **Settled** or **Not settled**.</span></span>
- <span data-ttu-id="a243b-137">Nupp **Summa järgi sorteerimine** võimaldab sorteerida summasid absoluutväärtuse järgi, nii et saate grupeerida deebetid ja kreeditid, millel on sama summa.</span><span class="sxs-lookup"><span data-stu-id="a243b-137">The **Sort by absolute amount** button lets you sort the amounts by absolute value, so that you can group together debits and credits that have the same amount.</span></span>

## <a name="reverse-a-settlement"></a><span data-ttu-id="a243b-138">Tasakaalustuse tühistamine</span><span class="sxs-lookup"><span data-stu-id="a243b-138">Reverse a settlement</span></span>

<span data-ttu-id="a243b-139">Saate tühistada ekslikult tehtud tasakaalustuse.</span><span class="sxs-lookup"><span data-stu-id="a243b-139">You can reverse a settlement that was made by mistake.</span></span>

1. <span data-ttu-id="a243b-140">Otsitavate kannete kuvamiseks järgige jaotise "Kannete tasakaalustamine, kasutades laiendatud pearaamatu tasakaalustamise lehte" samme 1–3.</span><span class="sxs-lookup"><span data-stu-id="a243b-140">Follow steps 1 through 3 in the "Settle transactions by using advanced ledger settlements page" section to show the transactions that you're looking for.</span></span>
2. <span data-ttu-id="a243b-141">Valige **Oleku** filtris valik **Tasakaalustatud**.</span><span class="sxs-lookup"><span data-stu-id="a243b-141">In the **Status** filter, select **Settled**.</span></span>
3. <span data-ttu-id="a243b-142">Valige üks või mitu rida, mille tasakaalustamist soovite tühistada.</span><span class="sxs-lookup"><span data-stu-id="a243b-142">Select one or more lines that you're considering for reversal.</span></span> <span data-ttu-id="a243b-143">Välja **Valitud summa** väärtus lehe ülaosas suureneb või kahaneb vastavalt valitud ridade kogusummale.</span><span class="sxs-lookup"><span data-stu-id="a243b-143">The value of the **Selected amount** field at the top of the page increases or decreases by the total amount on the lines that you selected.</span></span>
4. <span data-ttu-id="a243b-144">Pärast kannete valimise lõpetamist valige **Märgi valituks**.</span><span class="sxs-lookup"><span data-stu-id="a243b-144">After you've finished selecting transactions, select **Mark selected**.</span></span> <span data-ttu-id="a243b-145">Iga valitud kande eest ilmub **Märgistatud** veergu linnuke.</span><span class="sxs-lookup"><span data-stu-id="a243b-145">A check mark appears in the **Marked** column for each transaction that you selected.</span></span> <span data-ttu-id="a243b-146">Lisaks, välja **Märgistatud summa** väärtus lehe ülaosas suureneb või kahaneb vastavalt märgistatud ridade kogusummale.</span><span class="sxs-lookup"><span data-stu-id="a243b-146">Additionally, the value of the **Marked amount** field at the top of the page increases or decreases by the total amount on the lines that you marked.</span></span>
5. <span data-ttu-id="a243b-147">Kui **Märgistatud summa** väärtus on **0** (null), valige **Märgistatud kannete tasakaalustamise tühistamine**.</span><span class="sxs-lookup"><span data-stu-id="a243b-147">When the **Marked amount** value is **0** (zero), select **Reverse marked transactions**.</span></span> <span data-ttu-id="a243b-148">Märgistatud kannete olek uuendatakse olekule **Tasakaalustamata**.</span><span class="sxs-lookup"><span data-stu-id="a243b-148">The status of the marked transactions is updated to **Not settled**.</span></span>

## <a name="update-the-list-of-accounts-that-are-included-in-the-list-of-transactions"></a><span data-ttu-id="a243b-149">Värskendage kannete loendisse kaasatud kontode loendit</span><span class="sxs-lookup"><span data-stu-id="a243b-149">Update the list of accounts that are included in the list of transactions</span></span>

<span data-ttu-id="a243b-150">Valige **Pearaamatu tasakaalustuskonto**, et avada dialoogiboks, kui saate redigeerida kannete loendisse kaasatud kontosid.</span><span class="sxs-lookup"><span data-stu-id="a243b-150">Select **Ledger settlement accounts** to open a dialog box where you can edit the accounts that are included in the list of transactions.</span></span> <span data-ttu-id="a243b-151">Valige loendisse uue konto lisamiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="a243b-151">Select **New** to add new accounts to the list.</span></span> <span data-ttu-id="a243b-152">Seda loendit kasutatakse kannete loendi filtreerimiseks, mis kuvatakse **Pearaamatu tasakaalustuste** leheküljel.</span><span class="sxs-lookup"><span data-stu-id="a243b-152">This list is used to filter the list of transactions that appears on the **Ledger settlements** page.</span></span>
