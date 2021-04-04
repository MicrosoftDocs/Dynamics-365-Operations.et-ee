---
title: Protsesside kogumiskirjade näide
description: Käesolev teema peab läbima näite, mis näitab märgukirjade loomise, printimise ja sisestamise protsessi.
author: JodiChristiansen
manager: AnnBe
ms.date: 02/03/2021
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: df4252513f9e3a02632561b4e465c98edc888ea7
ms.sourcegitcommit: 4ecc1bf82fbb04882d7ef5e1994ef3c07ef953dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/08/2021
ms.locfileid: "5558307"
---
# <a name="process-collection-letters-example"></a><span data-ttu-id="8c0e0-103">Protsesside kogumiskirjade näide</span><span class="sxs-lookup"><span data-stu-id="8c0e0-103">Process collection letters example</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8c0e0-104">Käesolev teema peab läbima näite, mis näitab märgukirjade loomise, printimise ja sisestamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-104">This topic goes through an example that shows the process of creating, printing, and posting collection letters.</span></span> <span data-ttu-id="8c0e0-105">Näide põhineb **Krediit ja Sissenõuete märgukirjakoodi arvutamisel eira makseid** valikute krediiditeatisi.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-105">The example is based on the **Ignore payments and credit memos when calculating collection letter code** option in Credit and collections.</span></span> <span data-ttu-id="8c0e0-106">See kasutab andmeid USMF-i demoettevõttes ja uut klienti US-045.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-106">It uses data in the USMF demo company and a new customer, US-045.</span></span>

<span data-ttu-id="8c0e0-107">Et alustada, minge **Müügireskontro \> Kliendid \> Kõik kliendid**, valige **Uus** ja seejärel sisestage nõutav teave kliendi loomiseks US-045.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-107">To begin, go to **Accounts receivable \> Customers \> All customers**, select **New**, and then enter the required information to create customer US-045.</span></span>

<span data-ttu-id="8c0e0-108">Kui olete lõpetanud, järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-108">When you've finished, follow these steps.</span></span>

1. <span data-ttu-id="8c0e0-109">Minge moodulisse **Kreedit ja sissenõuded \> Märgukiri \> Märgukirjaseeria seadistus** ning seadistage märgukirjaseeria, nagu näidatud järgmises tabelis, mis on määratud kliendi sisestusreeglitele.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-109">Go to **Credit and collections \> Collection letter \> Setup collection letter sequence**, and set up the collection letter sequence as shown in the following table that is assigned to the customer posting profile.</span></span>

|     <span data-ttu-id="8c0e0-110">Märgukirja kood</span><span class="sxs-lookup"><span data-stu-id="8c0e0-110">Collection   letter code</span></span>      |     <span data-ttu-id="8c0e0-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c0e0-111">Description</span></span>                           |     <span data-ttu-id="8c0e0-112">Currency</span><span class="sxs-lookup"><span data-stu-id="8c0e0-112">Currency</span></span>      |     <span data-ttu-id="8c0e0-113">Põhikonto</span><span class="sxs-lookup"><span data-stu-id="8c0e0-113">Main   account</span></span>        |     <span data-ttu-id="8c0e0-114">Tasu valuutas</span><span class="sxs-lookup"><span data-stu-id="8c0e0-114">Fee   in currency</span></span>     |     <span data-ttu-id="8c0e0-115">Minimaalne üle</span><span class="sxs-lookup"><span data-stu-id="8c0e0-115">Minimum   over</span></span>        |     <span data-ttu-id="8c0e0-116">Blokeeri päevad</span><span class="sxs-lookup"><span data-stu-id="8c0e0-116">Days   Block</span></span>      |
|---------------------------------  |---------------------------------------    |-----------------  |-----------------------    |-------------------------- |-----------------------    |---------------------  |
|     <span data-ttu-id="8c0e0-117">1. märgukiri</span><span class="sxs-lookup"><span data-stu-id="8c0e0-117">Collection   letter 1</span></span>         |     <span data-ttu-id="8c0e0-118">Teine teatis tasuga</span><span class="sxs-lookup"><span data-stu-id="8c0e0-118">Second   notification with fee</span></span>        |     <span data-ttu-id="8c0e0-119">USA dollar</span><span class="sxs-lookup"><span data-stu-id="8c0e0-119">USD</span></span>           |                           |     <span data-ttu-id="8c0e0-120">0,00</span><span class="sxs-lookup"><span data-stu-id="8c0e0-120">0.00</span></span>                  |     <span data-ttu-id="8c0e0-121">0,00</span><span class="sxs-lookup"><span data-stu-id="8c0e0-121">0.00</span></span>                  |     <span data-ttu-id="8c0e0-122">2</span><span class="sxs-lookup"><span data-stu-id="8c0e0-122">2</span></span>                 |
|     <span data-ttu-id="8c0e0-123">2. märgukiri</span><span class="sxs-lookup"><span data-stu-id="8c0e0-123">Collection   letter 2</span></span>         |     <span data-ttu-id="8c0e0-124">Teine teatis tasuga</span><span class="sxs-lookup"><span data-stu-id="8c0e0-124">Second   notification with fee</span></span>        |     <span data-ttu-id="8c0e0-125">USC</span><span class="sxs-lookup"><span data-stu-id="8c0e0-125">USC</span></span>           |     <span data-ttu-id="8c0e0-126">403150</span><span class="sxs-lookup"><span data-stu-id="8c0e0-126">403150</span></span>                |     <span data-ttu-id="8c0e0-127">20.00</span><span class="sxs-lookup"><span data-stu-id="8c0e0-127">20.00</span></span>                 |     <span data-ttu-id="8c0e0-128">10.00</span><span class="sxs-lookup"><span data-stu-id="8c0e0-128">10.00</span></span>                 |     <span data-ttu-id="8c0e0-129">3</span><span class="sxs-lookup"><span data-stu-id="8c0e0-129">3</span></span>                 |
|     <span data-ttu-id="8c0e0-130">Kogum</span><span class="sxs-lookup"><span data-stu-id="8c0e0-130">Collection</span></span>                    |     <span data-ttu-id="8c0e0-131">Lõplik teatis tasuga</span><span class="sxs-lookup"><span data-stu-id="8c0e0-131">Final   notification with fee</span></span>         |     <span data-ttu-id="8c0e0-132">USA dollar</span><span class="sxs-lookup"><span data-stu-id="8c0e0-132">USD</span></span>           |     <span data-ttu-id="8c0e0-133">403150</span><span class="sxs-lookup"><span data-stu-id="8c0e0-133">403150</span></span>                |     <span data-ttu-id="8c0e0-134">50.00</span><span class="sxs-lookup"><span data-stu-id="8c0e0-134">50.00</span></span>                 |     <span data-ttu-id="8c0e0-135">100.00</span><span class="sxs-lookup"><span data-stu-id="8c0e0-135">100.00</span></span>                |     <span data-ttu-id="8c0e0-136">15</span><span class="sxs-lookup"><span data-stu-id="8c0e0-136">15</span></span>                |

<span data-ttu-id="8c0e0-137">Järgmine näide näitab teavet, mis on tabelis nii, nagu seda kuvataks **märgukirjade** lehel.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-137">The following illustration shows the information that's in the table as it would appear on the **Collection letters** page.</span></span> 

<span data-ttu-id="8c0e0-138">[![Märgukirjaseeria seadistamine](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-138">[![Setting up a collection letter sequence](./media/Ignore-payments-creditmemos-1.PNG)](./media/Ignore-payments-creditmemos-1.PNG)</span></span>

 <span data-ttu-id="8c0e0-139">Nüüd peate seadistama kaks selle näite puhul nõutavat parameetrit.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-139">You must now set the two parameters that are required for this example.</span></span>

2. <span data-ttu-id="8c0e0-140">Avage **Krediit ja sissenõudmine \> Seadistus \> Müügireskontro parameetrid**, ja järgige järgmisi samme:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-140">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-141">Kaardil **Sissenõudmine** märkige **Krediit ja sissenõuete märgukirjakoodi arvutamisel eira makseid valikute krediiditeatisi** valiku väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-141">On the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **Yes**.</span></span>
    2. <span data-ttu-id="8c0e0-142">Veenduge, et välja **Loo märgukiri** oleks seatud väärtusele **Klient**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-142">Make sure that the **Create collection letter per** field is set to **Customer**.</span></span>

    <span data-ttu-id="8c0e0-143">[![Sissenõuete müügireskontro parameetrite seadistamine](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-143">[![Setting Accounts receivable parameters for Credit collections](./media/Ignore-payments-creditmemos-2.PNG)](./media/Ignore-payments-creditmemos-2.PNG)</span></span>

3. <span data-ttu-id="8c0e0-144">Minge **müügireskontro \> Arved \> Kõik vabas vormis arved**, valige **Uus** ja seejärel järgige järgmisi samme:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-144">Go to **Accounts receivable \> Invoices \> All free text invoices**, select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-145">Valige **US-045** väljalt **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-145">In the **Customer account** field select **US-045**.</span></span>
    2. <span data-ttu-id="8c0e0-146">Sisestage **Arve kuupäev** väljale **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-146">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="8c0e0-147">Sisestage **Alates kuupäevast** väljale väärtus **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-147">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="8c0e0-148">Sisestage **Arve read** kiirkaardi väljale **Põhikonto** väärtus **401100**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-148">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="8c0e0-149">Sisestage väljale **Ühiku hind** väärtus **500.00**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-149">In the **Unit price** field, enter **500.00**.</span></span>
    6. <span data-ttu-id="8c0e0-150">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-150">Select **Post**.</span></span>

    <span data-ttu-id="8c0e0-151">Peate nüüd sisestama kliendile kaks kreeditarvet.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-151">You must now enter two credit notes for the customer.</span></span>

4. <span data-ttu-id="8c0e0-152">Valige käsk **Uus** ja tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-152">Select **New**, and then follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-153">Valige **US-045** väljalt **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-153">In the **Customer account** field, select **US-045**.</span></span>
    2. <span data-ttu-id="8c0e0-154">Sisestage **Arve kuupäev** väljale **1/15/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-154">In the **Invoice date** field, enter **1/15/2021**.</span></span>
    3. <span data-ttu-id="8c0e0-155">Sisestage **Alates kuupäevast** väljale väärtus **1/16/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-155">In the **Due date** field, enter **1/16/2021**.</span></span>
    4. <span data-ttu-id="8c0e0-156">Sisestage **Arve read** kiirkaardi väljale **Põhikonto** väärtus **401100**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-156">On the **Invoice lines** FastTab, in the **Main account** field, enter **401100**.</span></span>
    5. <span data-ttu-id="8c0e0-157">Sisestage **Ühiku hind** väljale **-100.00**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-157">In the **Unit price** field, enter **-100.00**.</span></span>
    6. <span data-ttu-id="8c0e0-158">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-158">Select **Post**.</span></span>

5. <span data-ttu-id="8c0e0-159">Korrake sammu 4, kuid sisestage **-200.00** väljal **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-159">Repeat step 4, but enter **-200.00** in the **Unit price** field.</span></span>
6. <span data-ttu-id="8c0e0-160">Minge **müügireskontro \> Kliendid \> Kõik kliendid** ja valige klient **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-160">Go to **Accounts receivable \> Customers \> All customers**, and select customer **US-045**.</span></span> <span data-ttu-id="8c0e0-161">Seejärel valige tegevuspaanil **Kanded \> Kanded** et vaadata kliendikandeid, mille sisestasite varem.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-161">Then, on the Action Pane, select **Transactions \> Transactions** to review the customer transactions that you posted earlier.</span></span>

    <span data-ttu-id="8c0e0-162">[![Sisestatud kliendikannete ülevaatamine](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-162">[![Reviewing the posted customer transactions](./media/Ignore-payments-creditmemos-3.PNG)](./media/Ignore-payments-creditmemos-3.PNG)</span></span>

    <span data-ttu-id="8c0e0-163">Teil on vaja nüüd kliendile US-045 märgukirjad koostada.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-163">You must now create collection letters for customer US-045.</span></span>

7. <span data-ttu-id="8c0e0-164">Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ja järgige järgmisi etappe:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-164">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-165">Seadke valiku **Arve** ja **Kreeditarve** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-165">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="8c0e0-166">Vaikimisi peaks välja **Märgukiri** väärtuseks olema määratud **Sissenõude märgukiri kliendi kohta**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-166">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="8c0e0-167">Sisestage **Arve kuupäev** väljale **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-167">In the **Collection letter date** field, enter **1/19/2021**.</span></span>
    3. <span data-ttu-id="8c0e0-168">**Kaasamiseks** kiirkaardil valige **Filter** ja siis lisage **Kliendikonto** väljale **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-168">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="8c0e0-169">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-169">Select **OK**.</span></span>
    5. <span data-ttu-id="8c0e0-170">Sissenõudekirja printimiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-170">Select **OK** to create collection letters.</span></span>

8. <span data-ttu-id="8c0e0-171">Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ning järgige järgmisi etappe:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-171">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-172">Pange tähele, et märgukirja kood nii päisel kui kanderidadel on **1. märgukiri**, sest see märgukiri on seeria esimene märgukiri.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-172">Notice that the collection letter code on both the header and the transaction lines is **Collection letter 1**, because this collection letter is the first collection letter in the sequence.</span></span> <span data-ttu-id="8c0e0-173">(Kanderidade vaatamiseks peate võib-olla valima **Kannete** kiirkaardi.)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-173">(To view the transaction lines, you might have to select the **Transactions** FastTab.)</span></span>

   <span data-ttu-id="8c0e0-174">[![Kontrollimine, et sama märgukirja kood ilmub päisele ja ridadele](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-174">[![Verifying that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-4.PNG)](./media/Ignore-payments-creditmemos-4.PNG)</span></span>

    2. <span data-ttu-id="8c0e0-175">Tehke toimingupaanil valik **Väljastamine**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-175">On the Action Pane, select **Post**.</span></span>
    3. <span data-ttu-id="8c0e0-176">Sisestage **Arve kuupäev** väljale **1/19/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-176">In the **Posting date** field, enter **1/19/2021**.</span></span>

    <span data-ttu-id="8c0e0-177">Teil on vaja nüüd kliendile US-045 märgukirjad koostada.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-177">You must now create collection letters again for customer US-045.</span></span>

9. <span data-ttu-id="8c0e0-178">Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ja järgige järgmisi etappe:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-178">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-179">Seadke valiku **Arve** ja **Kreeditarve** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-179">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="8c0e0-180">Vaikimisi peaks välja **Märgukiri** väärtuseks olema määratud **Sissenõude märgukiri kliendi kohta**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-180">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="8c0e0-181">Sisestage **Märgukirja kuupäev** väljale **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-181">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="8c0e0-182">**Kaasamiseks** kiirkaardil valige **Filter** ja siis lisage **Kliendikonto** väljale **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-182">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="8c0e0-183">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-183">Select **OK**.</span></span>
    5. <span data-ttu-id="8c0e0-184">Sissenõudekirja printimiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-184">Select **OK** to create collection letters.</span></span>

10. <span data-ttu-id="8c0e0-185">Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ning järgige järgmisi etappe:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-185">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-186">Pange tähele, et päises oleva märgukirja kood on **1. märgukiri**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-186">Notice that the collection letter code on the header is **Collection letter 1**.</span></span> <span data-ttu-id="8c0e0-187">Kanderidade kood on siiski **2. märgukiri**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-187">However, the code on the transaction lines is **Collection letter 2**.</span></span>

   <span data-ttu-id="8c0e0-188">[![Kontrollimine, et sama märgukirja kood ilmub päisele ja ridadele](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-188">[![Verifies that different collection letter codes appear on the header and the lines](./media/Ignore-payments-creditmemos-5.PNG)](./media/Ignore-payments-creditmemos-5.PNG)</span></span>

  <span data-ttu-id="8c0e0-189">Koodid erinevad, kuna **Sissemaksete koodi arvutamisel eira makseid ja krediiditeatisi** valiku väärtuseks on **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-189">The codes differ because the **Ignore payments and credit memos when calculating collection letter code** option is to **Yes**.</span></span>

  2. <span data-ttu-id="8c0e0-190">Ärge postitage seda märgukirja.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-190">Don't post this collection letter.</span></span>

11. <span data-ttu-id="8c0e0-191">Minge **Krediit ja sissenõueded \> Seadistamine \> Müügireskontro parameetritesse** ja siis **Sissenõuded** vahekaardil **Eira makseid ja krediiditeatisi märgukirjakoodi arvutamisel** suvandile **Ei**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-191">Go to **Credit and collections \> Setup \> Accounts receivable parameters**, and then, on the **Collections** tab, set the **Ignore payments and credit memos when calculating collection letter code** option to **No**.</span></span>

    <span data-ttu-id="8c0e0-192">[![Märgukirja koodi arvutamisel maksete ja kreeditarvete eiramiseks seadke väärtuseks Ei](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-192">[![Setting the Ignore payments and credit memos when calculating collection letter code option to No](./media/Ignore-payments-creditmemos-6.PNG)](./media/Ignore-payments-creditmemos-6.PNG)</span></span>

    <span data-ttu-id="8c0e0-193">Teil on vaja nüüd kliendile US-045 märgukirjad koostada.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-193">You must now create collection letters again for customer US-045.</span></span>

12. <span data-ttu-id="8c0e0-194">Minge **Krediit ja sissenõuded \> Sissenõudekiri \> Sissenõudekirja loomine** ja järgige järgmisi etappe:</span><span class="sxs-lookup"><span data-stu-id="8c0e0-194">Go to **Credit and collections \> Collection letter \> Create collection letters**, and follow these steps:</span></span>

    1. <span data-ttu-id="8c0e0-195">Seadke valiku **Arve** ja **Kreeditarve** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-195">Set the **Invoice** and **Credit note** options to **Yes**.</span></span>

        <span data-ttu-id="8c0e0-196">Vaikimisi peaks välja **Märgukiri** väärtuseks olema määratud **Sissenõude märgukiri kliendi kohta**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-196">By default, the **Collection letter** field should be set to **Collection per customer**.</span></span>

    2. <span data-ttu-id="8c0e0-197">Sisestage **Märgukirja kuupäev** väljale **1/23/2021**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-197">In the **Collection letter date** field, enter **1/23/2021**.</span></span>
    3. <span data-ttu-id="8c0e0-198">**Kaasamiseks** kiirkaardil valige **Filter** ja siis lisage **Kliendikonto** väljale **US-045**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-198">On the **Records to include** FastTab, select **Filter**, and then, in the **Customer account** field, add customer **US-045**.</span></span>
    4. <span data-ttu-id="8c0e0-199">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-199">Select **OK**.</span></span>
    5. <span data-ttu-id="8c0e0-200">Sissenõudekirja printimiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-200">Select **OK** to create collection letters.</span></span>

13. <span data-ttu-id="8c0e0-201">Minge **Krediit ja sissenõuded \> Märgukiri \> Vaadake üle ja koostage märgukiri** ja pange tähele, et märgukirja kood päisel ja kanderidadel on **2. märgukiri**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-201">Go to **Credit and collections \> Collection letter \> Review and process collection letters**, and notice that the collection letter code on both the header and the transaction lines is **Collection letter 2**.</span></span>

    <span data-ttu-id="8c0e0-202">[![Kontrollimine, et sama märgukirja kood ilmub päisele ja ridadele](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span><span class="sxs-lookup"><span data-stu-id="8c0e0-202">[![Showing again that the same collection letter code appears on the header and the lines](./media/Ignore-payments-creditmemos-7.PNG)](./media/Ignore-payments-creditmemos-7.PNG)</span></span>

    <span data-ttu-id="8c0e0-203">Koodid erinevad, kuna **Sissemaksete koodi arvutamisel eira makseid ja krediiditeatisi** valiku väärtuseks on **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c0e0-203">The same code appears in both places because the **Ignore payments and credit memos when calculating collection letter code** option is now set to **No**.</span></span>
