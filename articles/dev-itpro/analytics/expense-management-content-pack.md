---
title: Kulude halduse Power BI sisu
description: Selles teemas kirjeldatakse, mida hõlmab kulude halduse Power BI sisupakett.
author: RyanSand
manager: AnnBe
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: a07d9ed7e4c57c2444d1c2a017109509c153aad4
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1503123"
---
# <a name="expense-management-power-bi-content"></a><span data-ttu-id="66a53-103">Kulude halduse Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="66a53-103">Expense management Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66a53-104">Selles teemas kirjeldatakse, mida hõlmab kulude halduse Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="66a53-104">This topic describes what is included in the Expense management Power BI content.</span></span> 

## <a name="overview"></a><span data-ttu-id="66a53-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="66a53-105">Overview</span></span>
<span data-ttu-id="66a53-106">Versioonis 8.1 ja uuemates versioonides on koos kulude haldusega kasutamiseks saadaval kaks Power BI sisupaketti.</span><span class="sxs-lookup"><span data-stu-id="66a53-106">Two Power BI content packs are available for use with Expense management in version 8.1 and later.</span></span> 
- <span data-ttu-id="66a53-107">Kuluaruandeid esitavate töötajate jaoks on loodud isiklik armatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="66a53-107">There is a personal dashboard designed for employees who submit expense reports.</span></span> 

  <span data-ttu-id="66a53-108">Armatuurlaud on loodud nii, et see annab inimestele põhiteavet esitamata ja esitatud summade kohta ning näitab kulukannete ajalugu ja ülevaateid.</span><span class="sxs-lookup"><span data-stu-id="66a53-108">The dashboard is tailored to provide key information to individuals about unsubmitted and submitted amounts, as well as history and insights into expense transaction history.</span></span> <span data-ttu-id="66a53-109">Isiklik armatuurlaud on üks lehekülg, mis sisaldab kasutaja jaoks kõige olulisemat teavet.</span><span class="sxs-lookup"><span data-stu-id="66a53-109">The personal dashboard is a single page containing the most important information for the user.</span></span>

- <span data-ttu-id="66a53-110">Ostureskontro ametnike ja juhtide jaoks on loodud administraatori armatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="66a53-110">There is an admin dashboard designed for accounts payable clerks and managers.</span></span> <span data-ttu-id="66a53-111">Armatuurlaud on loodud töövõtja kulude jälgimiseks ja aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="66a53-111">The dashboard is tailored toward tracking and reporting on overall employee expenses.</span></span> <span data-ttu-id="66a53-112">See sisaldab peamisi kulude mõõdikuid, näiteks esitamata kulud, läbisõit ja keskmised kuluaruande summad.</span><span class="sxs-lookup"><span data-stu-id="66a53-112">It provides key expense metrics, such as unsubmitted expenses, mileage, and average expense report amounts.</span></span> <span data-ttu-id="66a53-113">See kasutab kandeandmeid ja annab koondvaated kulude haldusest kõigi ettevõtete lõikes.</span><span class="sxs-lookup"><span data-stu-id="66a53-113">It uses transactional data and provides aggregate views of expense management across all companies.</span></span> <span data-ttu-id="66a53-114">Peale selle esitab see jaotuse töövõtja kohta võimalusega lisada finantsdimensioonide andmeid.</span><span class="sxs-lookup"><span data-stu-id="66a53-114">It also provides a breakdown per employee, with the option to add financial dimension data.</span></span> <span data-ttu-id="66a53-115">Halduskulu analüüsi sisu sisaldab järgmist.</span><span class="sxs-lookup"><span data-stu-id="66a53-115">The Admin expense analytics content contains:</span></span> 
  - <span data-ttu-id="66a53-116">Ülevaate leht põhimõõdikutega kulusummade kohta ja ülevaadetega kuluaruannete mustanditest ning pooleliolevatest ja lõpetatud kuluaruannetest.</span><span class="sxs-lookup"><span data-stu-id="66a53-116">An overview page with key metrics about expense amounts and insights into draft, in process, and completed expense reports.</span></span> 
  - <span data-ttu-id="66a53-117">Töövõtja statistikaleht töövõtja individuaalsete üksikasjade ülevaatamiseks aja, kulutüübi ja statistikagrupi järgi.</span><span class="sxs-lookup"><span data-stu-id="66a53-117">An employee statistics page to review individual details about an employee by time, cost type, and statistics group.</span></span> 
  - <span data-ttu-id="66a53-118">Töövõtja võrdlusleht mitme töövõtja võrdlemiseks aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="66a53-118">An employee comparison page to compare multiple employees over time.</span></span> 

<span data-ttu-id="66a53-119">Kõik summad on näidatud ettevõtte valuutas.</span><span class="sxs-lookup"><span data-stu-id="66a53-119">All the amounts are shown in the company currency.</span></span> <span data-ttu-id="66a53-120">Näidatakse kõikide ettevõtete andmeid, aga vajaduse korral saab lisada ettevõtte filtri.</span><span class="sxs-lookup"><span data-stu-id="66a53-120">Data for all companies are shown, but if needed you can add a company filter.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="66a53-121">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="66a53-121">Accessing the Power BI content</span></span>
<span data-ttu-id="66a53-122">Kulude administraatori Dashboard.pbix-i ja kulude isikliku Dashboard.pbix-i Power BI sisu leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist.</span><span class="sxs-lookup"><span data-stu-id="66a53-122">You can find the Expense Admin Dashboard.pbix and Expense Personal Dashboard.pbix Power BI content in the Shared assets library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="66a53-123">Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).</span><span class="sxs-lookup"><span data-stu-id="66a53-123">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).</span></span>
<span data-ttu-id="66a53-124">Sisu on saadaval kulude halduse tööruumis Power Bi manussisuna.</span><span class="sxs-lookup"><span data-stu-id="66a53-124">The content is available from the Expense Management workspace as embedded Power Bi content.</span></span> <span data-ttu-id="66a53-125">Kulu omanik pääseb ligi enda isiklikele kuludele, kuid ainult ostureskontro ametnikel ja juhtidel on ligipääs administraatori sisule, et näha kõiki kasutaja kuluandmeid.</span><span class="sxs-lookup"><span data-stu-id="66a53-125">Any expense owner can access personal expenses for themselves, while only Accounts Payable clerks and managers have access to the Admin content to view all user's expense data.</span></span>

## <a name="refreshing-the-power-bi-content"></a><span data-ttu-id="66a53-126">Power BI sisu värskendamine</span><span class="sxs-lookup"><span data-stu-id="66a53-126">Refreshing the Power BI content</span></span>
<span data-ttu-id="66a53-127">Kulude halduse Power BI sisu jaoks on vaja üksuse kauplusest värskendada mõõdikuid TrvBiExpenseMeasurement ja BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="66a53-127">The Expense management Power BI content requires the TrvBiExpenseMeasurement measure and the BudgetActivityMeasure to be refreshed from the Entity Store.</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="66a53-128">Power BI sisusse kuuluvad mõõdikud</span><span class="sxs-lookup"><span data-stu-id="66a53-128">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="66a53-129">Sisu hõlmab aruandelehtede komplekti.</span><span class="sxs-lookup"><span data-stu-id="66a53-129">The content includes a set of report pages.</span></span> <span data-ttu-id="66a53-130">Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena.</span><span class="sxs-lookup"><span data-stu-id="66a53-130">Each page consists of a set of metrics that are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="66a53-131">Järgmine tabel annab ülevaate Power BI sisu visualiseerimistest.</span><span class="sxs-lookup"><span data-stu-id="66a53-131">The following table provides an overview of the visualizations in the Power BI content.</span></span>

<span data-ttu-id="66a53-132">**Isiklike kulude analüüs**</span><span class="sxs-lookup"><span data-stu-id="66a53-132">**Personal expenses analytics**</span></span>

| <span data-ttu-id="66a53-133">Aruandeleht</span><span class="sxs-lookup"><span data-stu-id="66a53-133">Report page</span></span> | <span data-ttu-id="66a53-134">Visualiseering</span><span class="sxs-lookup"><span data-stu-id="66a53-134">Visualization</span></span>                             |
|-------------|-------------------------------------------|
| <span data-ttu-id="66a53-135">Minu kulud</span><span class="sxs-lookup"><span data-stu-id="66a53-135">My expenses</span></span> | <span data-ttu-id="66a53-136">Läbisõidu summa</span><span class="sxs-lookup"><span data-stu-id="66a53-136">Amount of mileage</span></span>                         |
|             | <span data-ttu-id="66a53-137">Pooleliolevad kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="66a53-137">In process expense reports</span></span>                |
|             | <span data-ttu-id="66a53-138">Nr</span><span class="sxs-lookup"><span data-stu-id="66a53-138">No.</span></span> <span data-ttu-id="66a53-139">Esitamata kulude arv</span><span class="sxs-lookup"><span data-stu-id="66a53-139">of Unsubmitted expenses</span></span>               |
|             | <span data-ttu-id="66a53-140">Makstavad isiklikud kulud</span><span class="sxs-lookup"><span data-stu-id="66a53-140">Personal expenses to be paid</span></span>              |
|             | <span data-ttu-id="66a53-141">Esitamata summa</span><span class="sxs-lookup"><span data-stu-id="66a53-141">Amount unsubmitted</span></span>                        |
|             | <span data-ttu-id="66a53-142">Esitatud summa</span><span class="sxs-lookup"><span data-stu-id="66a53-142">Amount submitted</span></span>                          |
|             | <span data-ttu-id="66a53-143">Korvamist ootav summa</span><span class="sxs-lookup"><span data-stu-id="66a53-143">Amount awaiting reimbursement</span></span>             |
|             | <span data-ttu-id="66a53-144">Kuluaruanded summade ja olekuga</span><span class="sxs-lookup"><span data-stu-id="66a53-144">Expense reports with amounts and status</span></span>   |
|             | <span data-ttu-id="66a53-145">Esitatud, aga kinnitamata kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="66a53-145">Submitted but unapproved expense reports</span></span>  |
|             | <span data-ttu-id="66a53-146">Kulud kulutüübi järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-146">Expenses by cost type</span></span>                     |
|             | <span data-ttu-id="66a53-147">Kulud kaupmehe järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-147">Expenses by merchant</span></span>                      |
|             | <span data-ttu-id="66a53-148">Kulud töödeldud kulude järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-148">Expenses by processed expenses</span></span>            |
|             | <span data-ttu-id="66a53-149">Kulud projekti järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-149">Expenses by project</span></span>                       |
|             | <span data-ttu-id="66a53-150">Kande kogusumma aja jooksul</span><span class="sxs-lookup"><span data-stu-id="66a53-150">Total transaction amount over time</span></span>        |

<span data-ttu-id="66a53-151">**Halduskulude analüüs**</span><span class="sxs-lookup"><span data-stu-id="66a53-151">**Admin expenses analytics**</span></span>

| <span data-ttu-id="66a53-152">Aruandeleht</span><span class="sxs-lookup"><span data-stu-id="66a53-152">Report page</span></span>         | <span data-ttu-id="66a53-153">Visualiseering</span><span class="sxs-lookup"><span data-stu-id="66a53-153">Visualization</span></span>                           |           
|---------------------|-----------------------------------------|
| <span data-ttu-id="66a53-154">Kulude ülevaade</span><span class="sxs-lookup"><span data-stu-id="66a53-154">Expense Overview</span></span>    | <span data-ttu-id="66a53-155">Kulude mustandi summa</span><span class="sxs-lookup"><span data-stu-id="66a53-155">Draft expenses amount</span></span>                   |
|                     | <span data-ttu-id="66a53-156">Kulude mustandi ridade arv</span><span class="sxs-lookup"><span data-stu-id="66a53-156">Number of draft expense lines</span></span>           |
|                     | <span data-ttu-id="66a53-157">Kulude mustandi read</span><span class="sxs-lookup"><span data-stu-id="66a53-157">Draft expense lines</span></span>                     |
|                     | <span data-ttu-id="66a53-158">Kuluaruande poliitika rikkumised</span><span class="sxs-lookup"><span data-stu-id="66a53-158">Expense report policy violations</span></span>        |
|                     | <span data-ttu-id="66a53-159">Laekumata summa</span><span class="sxs-lookup"><span data-stu-id="66a53-159">Amount outstanding</span></span>                      |
|                     | <span data-ttu-id="66a53-160">Esitatud, aga kinnitamata kulud</span><span class="sxs-lookup"><span data-stu-id="66a53-160">Submitted but unapproved expenses</span></span>       |
|                     | <span data-ttu-id="66a53-161">Kinnitatud kulud</span><span class="sxs-lookup"><span data-stu-id="66a53-161">Approved expenses</span></span>                       |
|                     | <span data-ttu-id="66a53-162">Kulusumma kokku</span><span class="sxs-lookup"><span data-stu-id="66a53-162">Total expense amount</span></span>                    |
|                     | <span data-ttu-id="66a53-163">Kuluaruande kokkuvõtted</span><span class="sxs-lookup"><span data-stu-id="66a53-163">Expense report summaries</span></span>                |
|                     | <span data-ttu-id="66a53-164">Kulud kulutüübi järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-164">Expenses by cost type</span></span>                   |
|                     | <span data-ttu-id="66a53-165">Kulud kaupmehe järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-165">Expenses by merchant</span></span>                    |
|                     | <span data-ttu-id="66a53-166">Kulud töövõtjate järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-166">Expenses by employees</span></span>                   |
|                     | <span data-ttu-id="66a53-167">Kulud vs projekt</span><span class="sxs-lookup"><span data-stu-id="66a53-167">Expenses vs project</span></span>                     |
| <span data-ttu-id="66a53-168">Töövõtja võrdlus</span><span class="sxs-lookup"><span data-stu-id="66a53-168">Employee Comparison</span></span> | <span data-ttu-id="66a53-169">Kulusummad</span><span class="sxs-lookup"><span data-stu-id="66a53-169">Expense amounts</span></span>                         |
|                     | <span data-ttu-id="66a53-170">Kulusummad aja jooksul töövõtja järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-170">Expense amounts over time by employee</span></span>   |
| <span data-ttu-id="66a53-171">Töövõtja statistika</span><span class="sxs-lookup"><span data-stu-id="66a53-171">Employee Statistics</span></span> | <span data-ttu-id="66a53-172">Kuluaruanded kulutüübi järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-172">Expense reports by cost type</span></span>            |
|                     | <span data-ttu-id="66a53-173">Isiklikud kulud</span><span class="sxs-lookup"><span data-stu-id="66a53-173">Personal expenses</span></span>                       |
|                     | <span data-ttu-id="66a53-174">Kuluaruanded statistikagrupi järgi</span><span class="sxs-lookup"><span data-stu-id="66a53-174">Expense reports by statistics group</span></span>     |
