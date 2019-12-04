---
title: Edasilükkunud tulu tuvastamine
description: Sellest teemast leiate teavet tulu tuvastamise kohta tulu tuvastamise funktsiooni abil.
author: kweekley
manager: aolson
ms.date: 08/24/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: ace1d00ec25a57b26b1858369c32d9134a380977
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570352"
---
# <a name="recognize-deferred-revenue"></a><span data-ttu-id="c872f-103">Edasilükkunud tulu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="c872f-103">Recognize deferred revenue</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="c872f-104">Tulu tuvastamise funktsiooni ei saa funktsioonihalduse kaudu sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="c872f-104">The Revenue recognition feature can't be turned on through Feature management.</span></span> <span data-ttu-id="c872f-105">Praegu peate selle sisselülitamiseks kasutama konfiguratsioonivõtmeid.</span><span class="sxs-lookup"><span data-stu-id="c872f-105">Currently, you must use configuration keys to turn it on.</span></span>

<span data-ttu-id="c872f-106">Selles teemas kirjeldatakse tulu tuvastamise protsessi tulu tuvastamise graafikuga.</span><span class="sxs-lookup"><span data-stu-id="c872f-106">This topic describes the process of recognizing revenue in the revenue recognition schedule.</span></span> <span data-ttu-id="c872f-107">Pärast müügitellimuse arve sisestamist luuakse iga tulugraafikuga müügitellimuse rea jaoks tulu tuvastamise graafik.</span><span class="sxs-lookup"><span data-stu-id="c872f-107">After an invoice has been posted for a sales order, a revenue recognition schedule is created for each sales order line that has a revenue schedule.</span></span> <span data-ttu-id="c872f-108">Real olevat tulu graafikut kasutatakse selleks, et määrata, kas rea tulu tuleks edasi lükata.</span><span class="sxs-lookup"><span data-stu-id="c872f-108">The revenue schedule on a line is used to determine whether the line's revenue should be deferred.</span></span>

## <a name="view-revenue-recognition-schedule-details"></a><span data-ttu-id="c872f-109">Tulu tuvastamise graafiku üksikasjade kuvamine</span><span class="sxs-lookup"><span data-stu-id="c872f-109">View revenue recognition schedule details</span></span>

<span data-ttu-id="c872f-110">Tulu tuvastamise graafiku üksikasjade vaatamiseks on kaks võimalust.</span><span class="sxs-lookup"><span data-stu-id="c872f-110">There are two ways to access the details of the revenue recognition schedule.</span></span>

- <span data-ttu-id="c872f-111">Saate avada tulu tuvastamise graafiku otse arveldatud müügitellimusest.</span><span class="sxs-lookup"><span data-stu-id="c872f-111">You can open the revenue recognition schedule directly from an invoiced sales order.</span></span> <span data-ttu-id="c872f-112">Sel juhul filtreeritakse tulugraafikus olev teave nii, et kuvatakse ainult valitud müügitellimuse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="c872f-112">In this case, the information in the revenue schedule is filtered to show the details only for the selected sales order.</span></span> <span data-ttu-id="c872f-113">See variant on kasulik müügitellimuse graafiku üksikasjade kontrollimiseks.</span><span class="sxs-lookup"><span data-stu-id="c872f-113">This approach is useful when you're validating the schedule details for a sales order.</span></span>
- <span data-ttu-id="c872f-114">Saate avada tulu tuvastamise graafiku lehelt **Tulu tuvastamine \> Perioodilised ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="c872f-114">You can open the revenue recognition schedule from the **Revenue recognition \> Periodic tasks** page.</span></span> <span data-ttu-id="c872f-115">Seda varianti kasutatakse sageli siis, kui tulu tuvastatakse perioodi lõpus.</span><span class="sxs-lookup"><span data-stu-id="c872f-115">This approach is often used when revenue is recognized at the end of a period.</span></span> <span data-ttu-id="c872f-116">Lehe esmakordsel avamisel teavet ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="c872f-116">When the page is first opened, no information is shown.</span></span> <span data-ttu-id="c872f-117">Kasutage ruudustiku kohal olevaid filtreid, et määratleda graafiku kuvatavate üksikasjade kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="c872f-117">Use the filters above the grid to define criteria for the schedule details that should be shown.</span></span> <span data-ttu-id="c872f-118">Saate filtreerida arve kuupäevade alusel, sisestades kuupäevavahemiku, müügitellimuse, kliendi, projekti ID või oleku.</span><span class="sxs-lookup"><span data-stu-id="c872f-118">You can filter on the invoice dates by entering a date range, sales order, customer, project ID, or state.</span></span>

<span data-ttu-id="c872f-119">[![Tulugraafikute leht](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-119">[![Revenue schedules page](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)</span></span>

<span data-ttu-id="c872f-120">Ruudustiku all olev kiirkaart **Finantsdimensioon** kuvab müügitellimuse rea finantsdimensiooni.</span><span class="sxs-lookup"><span data-stu-id="c872f-120">The **Financial dimension** FastTab below the grid shows the financial dimensions of the sales order line.</span></span> <span data-ttu-id="c872f-121">Neid dimensioone arvestati edasilükatud tulu sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="c872f-121">These dimensions were considered during posting to deferred revenue.</span></span> <span data-ttu-id="c872f-122">Neid arvestatakse ka tulu tuvastamisel.</span><span class="sxs-lookup"><span data-stu-id="c872f-122">They are also considered when the revenue is recognized.</span></span> <span data-ttu-id="c872f-123">Kasutatavad dimensiooniväärtused sõltuvad tulu ja edasilükatud tulu põhikontodele omistatud konto struktuurist.</span><span class="sxs-lookup"><span data-stu-id="c872f-123">The dimension values that are used depend on the account structure that is assigned to the revenue and deferred revenue main accounts.</span></span>

## <a name="recognize-revenue"></a><span data-ttu-id="c872f-124">Tulu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="c872f-124">Recognize revenue</span></span>

<span data-ttu-id="c872f-125">Tulu tuvastamiseks käitatakse lehel **Tulu tuvastamine** protsess **Töölehe loomine**.</span><span class="sxs-lookup"><span data-stu-id="c872f-125">You recognize revenue by running the **Create journal** process from the **Recognize revenue** page.</span></span> <span data-ttu-id="c872f-126">Selle lehe saate avada kas müügitellimusest või lehelt **Perioodilised ülesanded**.</span><span class="sxs-lookup"><span data-stu-id="c872f-126">You can open this page from either the sales order or **Periodic tasks**.</span></span> <span data-ttu-id="c872f-127">Kui protsess käitatakse müügitellimusest, tuvastab see ainult valitud müügitellimuse tulu.</span><span class="sxs-lookup"><span data-stu-id="c872f-127">If the process is run from the sales order, it recognizes revenue only for the selected sales order.</span></span> <span data-ttu-id="c872f-128">Tavaliselt käivitatakse protsess lehel **Perioodilised ülesanded**, et tuvastada kõigi sisestatud müügitellimuste arvete tulu.</span><span class="sxs-lookup"><span data-stu-id="c872f-128">Typically, the process is run from **Periodic tasks** instead, so that it recognizes revenue for all posted sales order invoices.</span></span>

<span data-ttu-id="c872f-129">Tulu valimise ja sisestamise kriteeriumite määratlemiseks valige **Töölehe loomine**, et avada dialoogiboks **Loo tööleht**.</span><span class="sxs-lookup"><span data-stu-id="c872f-129">To define the criteria for selecting and posting revenue, select **Create journal** to open the **Create journal** dialog box.</span></span>

<span data-ttu-id="c872f-130">[![Töölehe loomise parameetrite suvandid](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-130">[![Create journal parameter options](./media/revenue-recognition-create-journal.png)](./media/revenue-recognition-create-journal.png)</span></span>

<span data-ttu-id="c872f-131">Dialoogiboksis kasutage väljagrupi **Töötlemise kuupäev** suvandeid, et määratleda tulu tuvastamisel kasutatav sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="c872f-131">In the dialog box, use the options in the **Processing date** field group to define the posting date that is used when revenue is recognized.</span></span> <span data-ttu-id="c872f-132">Kui valite **Valitud kuupäev**, saate sisestada sisestuskuupäeva väljale **Kande kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="c872f-132">If you select **Selected date**, you can enter a posting date in the **Transaction date** field.</span></span> <span data-ttu-id="c872f-133">Kui valite **Tulugraafiku kuupäev**, ei kasutata kande kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="c872f-133">If you select **Revenue schedule date**, the transaction date isn't used.</span></span> <span data-ttu-id="c872f-134">Selle asemel kasutatakse sisestuskuupäevana graafiku iga rea välja **Tuvastamise kuupäev** väärtust.</span><span class="sxs-lookup"><span data-stu-id="c872f-134">Instead, the value of the **Recognize date** field on each line of the schedule is used as the posting date.</span></span>

<span data-ttu-id="c872f-135">Järgmiseks sisestage väljal **Alates kuupäevast** tulu tuvastamise "alates"-kuupäev.</span><span class="sxs-lookup"><span data-stu-id="c872f-135">Next, in the **As of date** field, enter the "as-of" date for recognizing revenue.</span></span> <span data-ttu-id="c872f-136">Kõik graafiku read, millel tuvastamise kuupäev on "alates"-kuupäevaga võrdne või sellest varasem, tuvastatakse, eeldusel, et nad ei ole ootel.</span><span class="sxs-lookup"><span data-stu-id="c872f-136">Any lines of the schedule where the recognize date is on or before the "as-of" date will be recognized, provided that they aren't on hold.</span></span>

<span data-ttu-id="c872f-137">Kui olete kuupäevade määratlemise lõpetanud, klõpsake töölehe loomiseks dialoogiboksis nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="c872f-137">After you've finished defining the dates, select **OK** in the dialog box to create the journal.</span></span> <span data-ttu-id="c872f-138">Saate teate, mis näitab loodud kannete arvu ja töölehte, kus need loodi.</span><span class="sxs-lookup"><span data-stu-id="c872f-138">You receive an informational message that shows the number of transactions that have been created and the journal where they were created.</span></span> <span data-ttu-id="c872f-139">Töölehte ei sisestata automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c872f-139">The journal isn't automatically posted.</span></span> <span data-ttu-id="c872f-140">Seetõttu on tulu tuvastamise halduril aega, et kontrollida, milliseid graafiku ridu tuvastatakse.</span><span class="sxs-lookup"><span data-stu-id="c872f-140">Therefore, the revenue recognition manager has time to validate which lines of the schedule are being recognized.</span></span>

<span data-ttu-id="c872f-141">Pärast protsessi käitamist märgitakse töölehele üle kantud read olekusse **Töödeldud**.</span><span class="sxs-lookup"><span data-stu-id="c872f-141">After the process is run, the lines on the schedule that were transferred to the journal are marked as **Processed**.</span></span> <span data-ttu-id="c872f-142">Lipp **Töödeldud** näitab, et read on üle kantud töölehele, kuid neid saab sisestada või jätta sisestamata.</span><span class="sxs-lookup"><span data-stu-id="c872f-142">The **Processed** flag indicates that the lines have been transferred to the journal, but they can be posted or unposted.</span></span> <span data-ttu-id="c872f-143">Pärast tulu tuvastamise töölehe sisestamist jääb lipp **Töödeldud** alles.</span><span class="sxs-lookup"><span data-stu-id="c872f-143">After the revenue recognition journal is posted, the **Processed** flag remains.</span></span> <span data-ttu-id="c872f-144">Kui tulu tuvastamise tööleht kustutatakse või kui rida kustutatakse, eemaldatakse lipp **Töödeldud**.</span><span class="sxs-lookup"><span data-stu-id="c872f-144">If the revenue recognition journal is deleted, or if a line is deleted, the **Processed** flag is removed.</span></span> <span data-ttu-id="c872f-145">Sel viisil saab rida tuvastada, kui protsess **Loo tööleht** uuesti käitatakse.</span><span class="sxs-lookup"><span data-stu-id="c872f-145">In that way, the line can be recognized when the **Create journal** process is run again.</span></span>

<span data-ttu-id="c872f-146">[![Tulu tuvastamise graafikute leht](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-146">[![Revenue recognition schedules page](./media/revenue-recognition-rev-recog-schedule-02.png)](./media/revenue-recognition-rev-recog-schedule-02.png)</span></span>

<span data-ttu-id="c872f-147">Lehel **Tulu tuvastamise tööleht** (**Tulu tuvastamine \> Töölehe sisestused \> Tulu tuvastamise tööleht**) avage **Read**, et vaadata tuvastamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="c872f-147">On the **Revenue recognition journal** page (**Revenue recognition \> Journal entries \> Revenue recognition journal**), open **Lines** to view the details of what is being recognized.</span></span> <span data-ttu-id="c872f-148">Graafiku iga tuvastatud rea kohta luuakse alati eraldi kanne, isegi kui kõik read on sisestatud samal kuupäeval ja kasutades samu pearaamatukontosid.</span><span class="sxs-lookup"><span data-stu-id="c872f-148">A separate transaction is always created for each line of the schedule that is being recognized, even if all the lines are posted on the same date by using the same ledger accounts.</span></span>

<span data-ttu-id="c872f-149">[![Töölehe kande leht](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-149">[![Journal voucher page](./media/revenue-recognition-journal-voucher.png)](./media/revenue-recognition-journal-voucher.png)</span></span>

<span data-ttu-id="c872f-150">Veerus **Konto** kuvatakse edasilükkunud tulu pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="c872f-150">The **Account** column shows the deferred revenue ledger account.</span></span> <span data-ttu-id="c872f-151">Pearaamatukontot ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="c872f-151">This ledger account can't be edited.</span></span> <span data-ttu-id="c872f-152">See piirang aitab tagada, et väljastatakse õige edasilükkunud tulu pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="c872f-152">This restriction helps guarantee that the correct deferred revenue ledger account is relieved.</span></span> <span data-ttu-id="c872f-153">Seda pearaamatukontot ei kontrollita konto struktuuri suhtes, kuna see võib olla alates viidatud tulu pearaamatukontole sisestamisest muutunud.</span><span class="sxs-lookup"><span data-stu-id="c872f-153">This ledger account isn't validated against the account structure, because it might have changed since posting to the referred revenue ledger account last occurred.</span></span>

<span data-ttu-id="c872f-154">Veerus **Vastaskonto** kuvatakse tulu pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="c872f-154">The **Offset account** column shows the revenue ledger account.</span></span> <span data-ttu-id="c872f-155">Vaikimisi võetakse tulu pearaamatukonto varude sisestusprofiilidest ja finantsdimensioonid võetakse müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="c872f-155">By default, the revenue ledger account is taken from Inventory posting profiles, and the financial dimensions are taken from the sales order line.</span></span> <span data-ttu-id="c872f-156">Seda pearaamatukontot kontrollitakse praeguse konto struktuuri suhtes.</span><span class="sxs-lookup"><span data-stu-id="c872f-156">This ledger account is validated against the current account structure.</span></span> <span data-ttu-id="c872f-157">Kuid seda saab redigeerida, kui konto struktuur on muutunud ja nõuab täiendavaid finantsdimensioone.</span><span class="sxs-lookup"><span data-stu-id="c872f-157">However, it can be edited if the account structure has changed and requires additional financial dimensions.</span></span>

<span data-ttu-id="c872f-158">Vaikimisi summa on võetud graafiku vastavalt realt ja seda ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="c872f-158">The default amount is from the corresponding line of the schedule, and it can't be changed.</span></span>

<span data-ttu-id="c872f-159">Kui müügitellimus on mitme valuuta müügitellimus, siis määratakse vahetuskursiks vaikimisi arve vahetuskurss.</span><span class="sxs-lookup"><span data-stu-id="c872f-159">BY default, if the sales order is a multicurrency sales order, the exchange rate is set to the exchange rate from the invoice.</span></span> <span data-ttu-id="c872f-160">Selline käitumismudel aitab tagada, et arvestusvaluuta ja aruandlusvaluuta summad vabastatakse täielikult.</span><span class="sxs-lookup"><span data-stu-id="c872f-160">This behavior helps guarantee that the accounting currency and reporting currency amounts are fully relieved.</span></span> <span data-ttu-id="c872f-161">Ümardamise tõttu võib graafiku viimase rea vahetuskurss veidi erineda arve vahetuskursist.</span><span class="sxs-lookup"><span data-stu-id="c872f-161">Because of rounding, the exchange rate for the last line of the schedule might differ slightly from the rate on the invoice.</span></span>

<span data-ttu-id="c872f-162">Pärast tulu tuvastamise töölehe sisestamist sisestatakse kanne graafikule.</span><span class="sxs-lookup"><span data-stu-id="c872f-162">After the revenue recognition journal is posted, the voucher is entered on the schedule.</span></span> <span data-ttu-id="c872f-163">Kui graafiku sama rea kohta on rohkem kui üks kanne, kuvatakse real tärn (\*).</span><span class="sxs-lookup"><span data-stu-id="c872f-163">If there is more than one voucher for the same line of the schedule, an asterisk (\*) appears on the line.</span></span> <span data-ttu-id="c872f-164">Selle rea jaoks sisestatud kannete vaatamiseks valige **Kande kanded**.</span><span class="sxs-lookup"><span data-stu-id="c872f-164">To view the vouchers that were posted for that line, select **Voucher transactions**.</span></span>

## <a name="modify-the-revenue-recognition-schedule-details"></a><span data-ttu-id="c872f-165">Tulu tuvastamise graafiku üksikasjade muutmine</span><span class="sxs-lookup"><span data-stu-id="c872f-165">Modify the revenue recognition schedule details</span></span>

<span data-ttu-id="c872f-166">Enamikku tulu graafiku andmetest ei saa redigeerida.</span><span class="sxs-lookup"><span data-stu-id="c872f-166">Most of the data in the revenue schedule details can't be edited.</span></span> <span data-ttu-id="c872f-167">Graafikule ei saa lisada uusi ridu ja olemasolevaid ridu ei saa kustutada.</span><span class="sxs-lookup"><span data-stu-id="c872f-167">New lines can't be added to the schedule, and existing lines can't be deleted.</span></span> <span data-ttu-id="c872f-168">Iga müügitellimuse rea tulu graafiku üksikasju tuleb säilitada, et aidata tagada, et edaspidi tuvastaks organisatsioon sama summa, mis oli edasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="c872f-168">The revenue schedule details for each sales order line must be maintained to help guarantee that, over time, an organization recognizes the same amount that was deferred.</span></span>

### <a name="edit-schedule-lines"></a><span data-ttu-id="c872f-169">Graafiku ridade redigeerimine</span><span class="sxs-lookup"><span data-stu-id="c872f-169">Edit schedule lines</span></span>

<span data-ttu-id="c872f-170">Graafiku ridadel on lubatud mõned redigeerimised.</span><span class="sxs-lookup"><span data-stu-id="c872f-170">Some edits are allowed on the lines of the schedule.</span></span> <span data-ttu-id="c872f-171">Ridadel saab muuta järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="c872f-171">The following fields can be changed on the lines:</span></span>

- <span data-ttu-id="c872f-172">**Ootel** – selle lipu saab enne rea töötlemist määrata või eemaldada.</span><span class="sxs-lookup"><span data-stu-id="c872f-172">**On hold** – This flag can be set or cleared before the line is processed.</span></span> <span data-ttu-id="c872f-173">Lipu eemaldamiseks valige rida ja seejärel käsk **Eemalda ootelolek**.</span><span class="sxs-lookup"><span data-stu-id="c872f-173">To clear the flag, select the row, and then select **Remove hold**.</span></span> <span data-ttu-id="c872f-174">Ootel olevatel ridadel ei saa tulu tuvastada.</span><span class="sxs-lookup"><span data-stu-id="c872f-174">Revenue can't be recognized on lines that are on hold.</span></span> <span data-ttu-id="c872f-175">Ridu saab automaatselt ootele panna, kui tulu graafikul on automaatsed ootelepanekud seadistatud.</span><span class="sxs-lookup"><span data-stu-id="c872f-175">Lines can automatically be put on hold if the revenue schedule is set up for automatic holds.</span></span>

    <span data-ttu-id="c872f-176">[![Tulu graafikud – graafiku ridade redigeerimine](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-176">[![Revenue schedules - edit schedule lines](./media/revenue-recognition-rev-revenue-schedules.png)](./media/revenue-recognition-rev-revenue-schedules.png)</span></span>

- <span data-ttu-id="c872f-177">**Tuvastamise kuupäev** – tuvastamise kuupäeva saab enne rea töötlemist muuta.</span><span class="sxs-lookup"><span data-stu-id="c872f-177">**Recognize date** – The recognize date can be changed before the line is processed.</span></span> <span data-ttu-id="c872f-178">Kui käitatakse protsess, mis loob tulu tuvastamiseks töölehe, sisestatakse kuupäev väljale **Tulu tuvastamine alates kuupäevast**.</span><span class="sxs-lookup"><span data-stu-id="c872f-178">When the process that creates the journal for recognizing revenue is run, a date is entered in the **Recognize revenue as of date** field.</span></span> <span data-ttu-id="c872f-179">Seda kuupäeva võrreldakse väljal **Tuvastamise kuupäev** oleva kuupäevaga, et määrata, milliseid ridu tuleks tuvastada.</span><span class="sxs-lookup"><span data-stu-id="c872f-179">That date is compared to the date in the **Recognize date** field to determine which lines should be recognized.</span></span>
- <span data-ttu-id="c872f-180">**Vabastatav summa** – enne rea töötlemist saab vabastatavat summat muuta.</span><span class="sxs-lookup"><span data-stu-id="c872f-180">**Amount to release** – The amount that will be released can be changed before the line is processed.</span></span> <span data-ttu-id="c872f-181">Tuvastatud tulu summat saate vähendada, kuid mitte suurendada.</span><span class="sxs-lookup"><span data-stu-id="c872f-181">You can decrease the amount of revenue that is recognized, but you can't increase it.</span></span> <span data-ttu-id="c872f-182">See väli võimaldab organisatsioonil tuvastada osa tulust tuvastamise kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="c872f-182">This field lets an organization recognize part of the revenue on the recognize date.</span></span> <span data-ttu-id="c872f-183">Kui summat muudetakse, näitab summa väljal **Ülejäänud summa**, kui palju tulu tuleb veel tuvastada.</span><span class="sxs-lookup"><span data-stu-id="c872f-183">If the amount is changed, the amount in the **Remaining amount** field shows how much revenue must still be recognized.</span></span>
- <span data-ttu-id="c872f-184">**Väljastatav kogus** – kui tulu graafik on seadistatud ühe korra või ühe kuu kohta, näidatakse väljal **Väljastatav kogus** müügitellimuse rea kogust.</span><span class="sxs-lookup"><span data-stu-id="c872f-184">**Quantity to release** – If the revenue schedule is set up for one occurrence or one month, the **Quantity to release** field shows the quantity for the sales order line.</span></span> <span data-ttu-id="c872f-185">Seda välja saab samuti redigeerida ja see annab teise võimaluse tulu osa tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="c872f-185">This field can also be edited and provides another way to recognize part of the revenue.</span></span> <span data-ttu-id="c872f-186">Näiteks kui real olev kogus on 5, saate koguse alistada nii, et see on väiksem kui 5.</span><span class="sxs-lookup"><span data-stu-id="c872f-186">For example, if the quantity on the line is 5, you can override the quantity so that it's less than 5.</span></span> <span data-ttu-id="c872f-187">Summat väljal **Vabastatav summa** uuendatakse proportsionaalselt.</span><span class="sxs-lookup"><span data-stu-id="c872f-187">The amount in the **Amount to release** field is updated proportionately.</span></span>

### <a name="update-contract-terms"></a><span data-ttu-id="c872f-188">Lepingutingimuste uuendamine</span><span class="sxs-lookup"><span data-stu-id="c872f-188">Update contract terms</span></span>

<span data-ttu-id="c872f-189">Tulu graafiku üksikasjad luuakse arve sisestamisel müügitellimuse reale määratud tulu graafiku alusel.</span><span class="sxs-lookup"><span data-stu-id="c872f-189">The revenue schedule details are created based on the revenue schedule that is assigned to the sales order line when the invoice is posted.</span></span> <span data-ttu-id="c872f-190">Kui müügitellimuse rea tulu graafik on vale, ei saa seda müügitellimusel pärast müügitellimuse arveldamist muuta.</span><span class="sxs-lookup"><span data-stu-id="c872f-190">If the revenue schedule on the sales order line is incorrect, it can't be changed on the sales order after the sales order is invoiced.</span></span> <span data-ttu-id="c872f-191">Selle asemel peate tulu graafiku muutmiseks kasutama nuppu **Lepingutingimuste uuendamine**.</span><span class="sxs-lookup"><span data-stu-id="c872f-191">Instead, you must use the **Update contract terms** button to change the revenue schedule.</span></span> <span data-ttu-id="c872f-192">Tulu graafikut saab muuta kas enne või pärast tulu tuvastamist.</span><span class="sxs-lookup"><span data-stu-id="c872f-192">The revenue schedule can be changed either before or after revenue has been recognized.</span></span>

<span data-ttu-id="c872f-193">Graafiku muutmiseks valige muudetava üksuse mis tahes graafiku rida.</span><span class="sxs-lookup"><span data-stu-id="c872f-193">To change the schedule, select any schedule line for the item that you're changing.</span></span> <span data-ttu-id="c872f-194">Järgmisel joonisel on valitud 12-kuulise tulugraafikuga postitatud üksuse S0008 rida.</span><span class="sxs-lookup"><span data-stu-id="c872f-194">In the following illustration, the line for item S0008 that was posted by using a 12-month revenue schedule is selected.</span></span> <span data-ttu-id="c872f-195">Kui valite **Lepingutingimuste uuendamine**, kuvatakse dialoogiboksis lepingu algus- ja lõppkuupäevad ning tulu graafik.</span><span class="sxs-lookup"><span data-stu-id="c872f-195">When you select **Update contract terms**, a dialog box shows the contract start and end dates, and the revenue schedule.</span></span>

<span data-ttu-id="c872f-196">[![Lepingu algus- ja lõppkuupäevad](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-196">[![Contract start and end dates](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule.png)</span></span>

<span data-ttu-id="c872f-197">Muutke lepingu algus- ja lõppkuupäeva nii, et need kajastaksid õiget kuupäevavahemikku.</span><span class="sxs-lookup"><span data-stu-id="c872f-197">Change the contract start and end dates so that they reflect the correct date range.</span></span> <span data-ttu-id="c872f-198">Kuupäevavahemiku muutmisel peab välja **Juhtumite arv** väärtus kattuma süsteemis määratletud tulu graafikuga.</span><span class="sxs-lookup"><span data-stu-id="c872f-198">When you change the date range, the value in the **Number of occurrences** field must match a revenue schedule that has been defined in the system.</span></span> <span data-ttu-id="c872f-199">Selles näites, kuna leping muudeti 24-kuuliseks lepinguks, tuleb seadistada 24-kuuline tulugraafik.</span><span class="sxs-lookup"><span data-stu-id="c872f-199">In this example, because the contract was changed to a 24-month contract, a 24-month revenue schedule must be set up.</span></span> <span data-ttu-id="c872f-200">Kuna 24-kuuline tulugraafik on olemas, sisestatakse see vaikimisi ja lepingut saab muuta.</span><span class="sxs-lookup"><span data-stu-id="c872f-200">Because the 24-month revenue schedule exists, it's entered by default, and the contract can be changed.</span></span> <span data-ttu-id="c872f-201">Kui kattuva juhtumite arvuga tulugraafikut pole olemas, ei saa lepingut muuta.</span><span class="sxs-lookup"><span data-stu-id="c872f-201">If a revenue schedule that has a matching number of occurrences doesn't exist, the contract can't be changed.</span></span> <span data-ttu-id="c872f-202">Kui olete lepingutingimuste ja tulugraafiku uuendamise lõpetanud, valige muudatuste salvestamiseks dialoogiboksis nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="c872f-202">After you've finished updating the contract terms and revenue schedule as you require, select **OK** in the dialog box to save your changes.</span></span>

<span data-ttu-id="c872f-203">[![Uuendatud lepingu kuupäevavahemik](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-203">[![Updated contract date range](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)](./media/revenue-recognition-rev-revenue-schedule-update-cntrct-dates-schedule-02.png)</span></span>

<span data-ttu-id="c872f-204">Lepingu muudatused mõjutavad tulugraafiku üksikasju järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="c872f-204">The contract changes have the following effects on the revenue schedule details:</span></span>

- <span data-ttu-id="c872f-205">Kui toote kohta ei ole tulu tuvastatud, eemaldatakse kõik eelmise graafiku üksikasjad ja asendatakse uute tulugraafiku üksikasjadega.</span><span class="sxs-lookup"><span data-stu-id="c872f-205">If no revenue has been recognized for the product, all the previous schedule details are removed and replaced with the new revenue schedule details.</span></span> <span data-ttu-id="c872f-206">Näiteks oli üksuse S0008 graafiku üksikasjades algselt 12 rida.</span><span class="sxs-lookup"><span data-stu-id="c872f-206">For example, item S0008 originally had 12 lines in the schedule details.</span></span> <span data-ttu-id="c872f-207">Need 12 rida eemaldatakse ja asendatakse uue tulugraafiku 24 reaga.</span><span class="sxs-lookup"><span data-stu-id="c872f-207">Those 12 lines are removed and replaced with 24 lines, based on the new revenue schedule.</span></span>
- <span data-ttu-id="c872f-208">Kui toote kohta on tulu tuvastatud, siis tuvastati osa tulu valesti, sest tuvastamine põhines valel tulugraafikul.</span><span class="sxs-lookup"><span data-stu-id="c872f-208">If revenue has been recognized for the product, some revenue was incorrectly recognized because recognition was based on the incorrect revenue schedule.</span></span> <span data-ttu-id="c872f-209">Need read tuleb tühistada ja uue graafiku alusel uuesti tuvastada.</span><span class="sxs-lookup"><span data-stu-id="c872f-209">Those lines must be reversed and recognized again, based on the new schedule.</span></span> <span data-ttu-id="c872f-210">Selle stsenaariumi korral luuakse uued tulugraafiku read, millel on negatiivne summa algsel tuvastamise kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="c872f-210">In this scenario, new revenue schedule lines are created that have negative amounts on the original recognize date.</span></span> <span data-ttu-id="c872f-211">Seejärel luuakse uued read, et tuvastada summad uue tulugraafiku alusel.</span><span class="sxs-lookup"><span data-stu-id="c872f-211">New lines are then created to recognize the amounts based on the new revenue schedule.</span></span> <span data-ttu-id="c872f-212">Näiteks tuvastasite 8. augustil 2019 tulu 10,53 $.</span><span class="sxs-lookup"><span data-stu-id="c872f-212">For example, on August 8, 2019, you recognized revenue for $10.53.</span></span> <span data-ttu-id="c872f-213">8. septembril 2019 tuvastasite tulu 13,16 $.</span><span class="sxs-lookup"><span data-stu-id="c872f-213">On September 8, 2019, you recognized revenue for $13.16.</span></span> <span data-ttu-id="c872f-214">Seetõttu luuakse samade kuupäevadega kaks uut rida.</span><span class="sxs-lookup"><span data-stu-id="c872f-214">Therefore, two new lines are created on the same dates.</span></span> <span data-ttu-id="c872f-215">Üks rida on -10,53 $ ja teine rida on -13,16 $ jaoks.</span><span class="sxs-lookup"><span data-stu-id="c872f-215">One line is for -$10.53, and the other line is for -$13.16.</span></span> <span data-ttu-id="c872f-216">Seejärel luuakse kakskümmend neli uut rida ja neile eraldatakse kogu edasilükatud tulu 160,61 $.</span><span class="sxs-lookup"><span data-stu-id="c872f-216">Twenty-four new lines are then created, and the total deferred revenue of $160.61 is allocated across them.</span></span> <span data-ttu-id="c872f-217">Tühistamise ridu saate sisestada, käivitades protsessi **Loo tööleht**.</span><span class="sxs-lookup"><span data-stu-id="c872f-217">You can post the reversing lines by running the **Create journal** process.</span></span>

<span data-ttu-id="c872f-218">[![Tulu tuvastamise graafik](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)</span><span class="sxs-lookup"><span data-stu-id="c872f-218">[![Revenue recognition schedule](./media/revenue-recognition-rev-recog-schedule-03.png)](./media/revenue-recognition-rev-recog-schedule-03.png)</span></span>