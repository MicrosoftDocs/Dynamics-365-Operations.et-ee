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
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 0dcb6114544b3817d8b80122a32759e67ad8dc94
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849655"
---
# <a name="expense-management-power-bi-content"></a><span data-ttu-id="8dd19-103">Kulude halduse Power BI sisu</span><span class="sxs-lookup"><span data-stu-id="8dd19-103">Expense management Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8dd19-104">Selles teemas kirjeldatakse, mida hõlmab kulude halduse Power BI sisu.</span><span class="sxs-lookup"><span data-stu-id="8dd19-104">This topic describes what is included in the Expense management Power BI content.</span></span> 

## <a name="overview"></a><span data-ttu-id="8dd19-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="8dd19-105">Overview</span></span>
<span data-ttu-id="8dd19-106">Versioonis 8.1 ja uuemates versioonides on koos kulude haldusega kasutamiseks saadaval kaks Power BI sisupaketti.</span><span class="sxs-lookup"><span data-stu-id="8dd19-106">Two Power BI content packs are available for use with Expense management in version 8.1 and later.</span></span> 
- <span data-ttu-id="8dd19-107">Kuluaruandeid esitavate töötajate jaoks on loodud isiklik armatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="8dd19-107">There is a personal dashboard designed for employees who submit expense reports.</span></span> 

  <span data-ttu-id="8dd19-108">Armatuurlaud on loodud nii, et see annab inimestele põhiteavet esitamata ja esitatud summade kohta ning näitab kulukannete ajalugu ja ülevaateid.</span><span class="sxs-lookup"><span data-stu-id="8dd19-108">The dashboard is tailored to provide key information to individuals about unsubmitted and submitted amounts, as well as history and insights into expense transaction history.</span></span> <span data-ttu-id="8dd19-109">Isiklik armatuurlaud on üks lehekülg, mis sisaldab kasutaja jaoks kõige olulisemat teavet.</span><span class="sxs-lookup"><span data-stu-id="8dd19-109">The personal dashboard is a single page containing the most important information for the user.</span></span>

- <span data-ttu-id="8dd19-110">Ostureskontro ametnike ja juhtide jaoks on loodud administraatori armatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="8dd19-110">There is an admin dashboard designed for accounts payable clerks and managers.</span></span> <span data-ttu-id="8dd19-111">Armatuurlaud on loodud töövõtja kulude jälgimiseks ja aruandluseks.</span><span class="sxs-lookup"><span data-stu-id="8dd19-111">The dashboard is tailored toward tracking and reporting on overall employee expenses.</span></span> <span data-ttu-id="8dd19-112">See sisaldab peamisi kulude mõõdikuid, näiteks esitamata kulud, läbisõit ja keskmised kuluaruande summad.</span><span class="sxs-lookup"><span data-stu-id="8dd19-112">It provides key expense metrics, such as unsubmitted expenses, mileage, and average expense report amounts.</span></span> <span data-ttu-id="8dd19-113">See kasutab kandeandmeid ja annab koondvaated kulude haldusest kõigi ettevõtete lõikes.</span><span class="sxs-lookup"><span data-stu-id="8dd19-113">It uses transactional data and provides aggregate views of expense management across all companies.</span></span> <span data-ttu-id="8dd19-114">Peale selle esitab see jaotuse töövõtja kohta võimalusega lisada finantsdimensioonide andmeid.</span><span class="sxs-lookup"><span data-stu-id="8dd19-114">It also provides a breakdown per employee, with the option to add financial dimension data.</span></span> <span data-ttu-id="8dd19-115">Halduskulu analüüsi sisu sisaldab järgmist.</span><span class="sxs-lookup"><span data-stu-id="8dd19-115">The Admin expense analytics content contains:</span></span> 
  - <span data-ttu-id="8dd19-116">Ülevaate leht põhimõõdikutega kulusummade kohta ja ülevaadetega kuluaruannete mustanditest ning pooleliolevatest ja lõpetatud kuluaruannetest.</span><span class="sxs-lookup"><span data-stu-id="8dd19-116">An overview page with key metrics about expense amounts and insights into draft, in process, and completed expense reports.</span></span> 
  - <span data-ttu-id="8dd19-117">Töövõtja statistikaleht töövõtja individuaalsete üksikasjade ülevaatamiseks aja, kulutüübi ja statistikagrupi järgi.</span><span class="sxs-lookup"><span data-stu-id="8dd19-117">An employee statistics page to review individual details about an employee by time, cost type, and statistics group.</span></span> 
  - <span data-ttu-id="8dd19-118">Töövõtja võrdlusleht mitme töövõtja võrdlemiseks aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="8dd19-118">An employee comparison page to compare multiple employees over time.</span></span> 

<span data-ttu-id="8dd19-119">Kõik summad on näidatud ettevõtte valuutas.</span><span class="sxs-lookup"><span data-stu-id="8dd19-119">All the amounts are shown in the company currency.</span></span> <span data-ttu-id="8dd19-120">Näidatakse kõikide ettevõtete andmeid, aga vajaduse korral saab lisada ettevõtte filtri.</span><span class="sxs-lookup"><span data-stu-id="8dd19-120">Data for all companies are shown, but if needed you can add a company filter.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="8dd19-121">Juurdepääs Power BI sisule</span><span class="sxs-lookup"><span data-stu-id="8dd19-121">Accessing the Power BI content</span></span>
<span data-ttu-id="8dd19-122">Kulude administraatori Dashboard.pbix-i ja kulude isikliku Dashboard.pbix-i Power BI sisu leiate teenuste Microsoft Dynamics Lifecycle Services (LCS) ühiste vahendite teegist.</span><span class="sxs-lookup"><span data-stu-id="8dd19-122">You can find the Expense Admin Dashboard.pbix and Expense Personal Dashboard.pbix Power BI content in the Shared assets library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="8dd19-123">Lisateavet sisu allalaadimise ja selle rakendamise kohta organisatsioonis vt jaotisest [Power BI sisu Microsoftilt ja teie partneritelt LCS-is](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).</span><span class="sxs-lookup"><span data-stu-id="8dd19-123">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/).</span></span>
<span data-ttu-id="8dd19-124">Sisu on saadaval kulude halduse tööruumis Power Bi manussisuna.</span><span class="sxs-lookup"><span data-stu-id="8dd19-124">The content is available from the Expense Management workspace as embedded Power Bi content.</span></span> <span data-ttu-id="8dd19-125">Kulu omanik pääseb ligi enda isiklikele kuludele, kuid ainult ostureskontro ametnikel ja juhtidel on ligipääs administraatori sisule, et näha kõiki kasutaja kuluandmeid.</span><span class="sxs-lookup"><span data-stu-id="8dd19-125">Any expense owner can access personal expenses for themselves, while only Accounts Payable clerks and managers have access to the Admin content to view all user's expense data.</span></span>

## <a name="refreshing-the-power-bi-content"></a><span data-ttu-id="8dd19-126">Power BI sisu värskendamine</span><span class="sxs-lookup"><span data-stu-id="8dd19-126">Refreshing the Power BI content</span></span>
<span data-ttu-id="8dd19-127">Kulude halduse Power BI sisu jaoks on vaja üksuse kauplusest värskendada mõõdikuid TrvBiExpenseMeasurement ja BudgetActivityMeasure.</span><span class="sxs-lookup"><span data-stu-id="8dd19-127">The Expense management Power BI content requires the TrvBiExpenseMeasurement measure and the BudgetActivityMeasure to be refreshed from the Entity Store.</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="8dd19-128">Power BI sisusse kuuluvad mõõdikud</span><span class="sxs-lookup"><span data-stu-id="8dd19-128">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="8dd19-129">Sisu hõlmab aruandelehtede komplekti.</span><span class="sxs-lookup"><span data-stu-id="8dd19-129">The content includes a set of report pages.</span></span> <span data-ttu-id="8dd19-130">Iga leht koosneb mõõdikute komplektist, mida visualiseeritakse diagrammide, paanide ja tabelitena.</span><span class="sxs-lookup"><span data-stu-id="8dd19-130">Each page consists of a set of metrics that are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="8dd19-131">Järgmine tabel annab ülevaate Power BI sisu visualiseerimistest.</span><span class="sxs-lookup"><span data-stu-id="8dd19-131">The following table provides an overview of the visualizations in the Power BI content.</span></span>

<span data-ttu-id="8dd19-132">**Isiklike kulude analüüs**</span><span class="sxs-lookup"><span data-stu-id="8dd19-132">**Personal expenses analytics**</span></span>

| <span data-ttu-id="8dd19-133">Aruandeleht</span><span class="sxs-lookup"><span data-stu-id="8dd19-133">Report page</span></span> | <span data-ttu-id="8dd19-134">Visualiseering</span><span class="sxs-lookup"><span data-stu-id="8dd19-134">Visualization</span></span>                             |
|-------------|-------------------------------------------|
| <span data-ttu-id="8dd19-135">Minu kulud</span><span class="sxs-lookup"><span data-stu-id="8dd19-135">My expenses</span></span> | <span data-ttu-id="8dd19-136">Läbisõidu summa</span><span class="sxs-lookup"><span data-stu-id="8dd19-136">Amount of mileage</span></span>                         |
|             | <span data-ttu-id="8dd19-137">Pooleliolevad kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="8dd19-137">In process expense reports</span></span>                |
|             | <span data-ttu-id="8dd19-138">Nr</span><span class="sxs-lookup"><span data-stu-id="8dd19-138">No.</span></span> <span data-ttu-id="8dd19-139">Esitamata kulude arv</span><span class="sxs-lookup"><span data-stu-id="8dd19-139">of Unsubmitted expenses</span></span>               |
|             | <span data-ttu-id="8dd19-140">Makstavad isiklikud kulud</span><span class="sxs-lookup"><span data-stu-id="8dd19-140">Personal expenses to be paid</span></span>              |
|             | <span data-ttu-id="8dd19-141">Esitamata summa</span><span class="sxs-lookup"><span data-stu-id="8dd19-141">Amount unsubmitted</span></span>                        |
|             | <span data-ttu-id="8dd19-142">Esitatud summa</span><span class="sxs-lookup"><span data-stu-id="8dd19-142">Amount submitted</span></span>                          |
|             | <span data-ttu-id="8dd19-143">Korvamist ootav summa</span><span class="sxs-lookup"><span data-stu-id="8dd19-143">Amount awaiting reimbursement</span></span>             |
|             | <span data-ttu-id="8dd19-144">Kuluaruanded summade ja olekuga</span><span class="sxs-lookup"><span data-stu-id="8dd19-144">Expense reports with amounts and status</span></span>   |
|             | <span data-ttu-id="8dd19-145">Esitatud, aga kinnitamata kuluaruanded</span><span class="sxs-lookup"><span data-stu-id="8dd19-145">Submitted but unapproved expense reports</span></span>  |
|             | <span data-ttu-id="8dd19-146">Kulud kulutüübi järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-146">Expenses by cost type</span></span>                     |
|             | <span data-ttu-id="8dd19-147">Kulud kaupmehe järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-147">Expenses by merchant</span></span>                      |
|             | <span data-ttu-id="8dd19-148">Kulud töödeldud kulude järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-148">Expenses by processed expenses</span></span>            |
|             | <span data-ttu-id="8dd19-149">Kulud projekti järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-149">Expenses by project</span></span>                       |
|             | <span data-ttu-id="8dd19-150">Kande kogusumma aja jooksul</span><span class="sxs-lookup"><span data-stu-id="8dd19-150">Total transaction amount over time</span></span>        |

<span data-ttu-id="8dd19-151">**Halduskulude analüüs**</span><span class="sxs-lookup"><span data-stu-id="8dd19-151">**Admin expenses analytics**</span></span>

| <span data-ttu-id="8dd19-152">Aruandeleht</span><span class="sxs-lookup"><span data-stu-id="8dd19-152">Report page</span></span>         | <span data-ttu-id="8dd19-153">Visualiseering</span><span class="sxs-lookup"><span data-stu-id="8dd19-153">Visualization</span></span>                           |           
|---------------------|-----------------------------------------|
| <span data-ttu-id="8dd19-154">Kulude ülevaade</span><span class="sxs-lookup"><span data-stu-id="8dd19-154">Expense Overview</span></span>    | <span data-ttu-id="8dd19-155">Kulude mustandi summa</span><span class="sxs-lookup"><span data-stu-id="8dd19-155">Draft expenses amount</span></span>                   |
|                     | <span data-ttu-id="8dd19-156">Kulude mustandi ridade arv</span><span class="sxs-lookup"><span data-stu-id="8dd19-156">Number of draft expense lines</span></span>           |
|                     | <span data-ttu-id="8dd19-157">Kulude mustandi read</span><span class="sxs-lookup"><span data-stu-id="8dd19-157">Draft expense lines</span></span>                     |
|                     | <span data-ttu-id="8dd19-158">Kuluaruande poliitika rikkumised</span><span class="sxs-lookup"><span data-stu-id="8dd19-158">Expense report policy violations</span></span>        |
|                     | <span data-ttu-id="8dd19-159">Laekumata summa</span><span class="sxs-lookup"><span data-stu-id="8dd19-159">Amount outstanding</span></span>                      |
|                     | <span data-ttu-id="8dd19-160">Esitatud, aga kinnitamata kulud</span><span class="sxs-lookup"><span data-stu-id="8dd19-160">Submitted but unapproved expenses</span></span>       |
|                     | <span data-ttu-id="8dd19-161">Kinnitatud kulud</span><span class="sxs-lookup"><span data-stu-id="8dd19-161">Approved expenses</span></span>                       |
|                     | <span data-ttu-id="8dd19-162">Kulusumma kokku</span><span class="sxs-lookup"><span data-stu-id="8dd19-162">Total expense amount</span></span>                    |
|                     | <span data-ttu-id="8dd19-163">Kuluaruande kokkuvõtted</span><span class="sxs-lookup"><span data-stu-id="8dd19-163">Expense report summaries</span></span>                |
|                     | <span data-ttu-id="8dd19-164">Kulud kulutüübi järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-164">Expenses by cost type</span></span>                   |
|                     | <span data-ttu-id="8dd19-165">Kulud kaupmehe järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-165">Expenses by merchant</span></span>                    |
|                     | <span data-ttu-id="8dd19-166">Kulud töövõtjate järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-166">Expenses by employees</span></span>                   |
|                     | <span data-ttu-id="8dd19-167">Kulud vs projekt</span><span class="sxs-lookup"><span data-stu-id="8dd19-167">Expenses vs project</span></span>                     |
| <span data-ttu-id="8dd19-168">Töövõtja võrdlus</span><span class="sxs-lookup"><span data-stu-id="8dd19-168">Employee Comparison</span></span> | <span data-ttu-id="8dd19-169">Kulusummad</span><span class="sxs-lookup"><span data-stu-id="8dd19-169">Expense amounts</span></span>                         |
|                     | <span data-ttu-id="8dd19-170">Kulusummad aja jooksul töövõtja järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-170">Expense amounts over time by employee</span></span>   |
| <span data-ttu-id="8dd19-171">Töövõtja statistika</span><span class="sxs-lookup"><span data-stu-id="8dd19-171">Employee Statistics</span></span> | <span data-ttu-id="8dd19-172">Kuluaruanded kulutüübi järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-172">Expense reports by cost type</span></span>            |
|                     | <span data-ttu-id="8dd19-173">Isiklikud kulud</span><span class="sxs-lookup"><span data-stu-id="8dd19-173">Personal expenses</span></span>                       |
|                     | <span data-ttu-id="8dd19-174">Kuluaruanded statistikagrupi järgi</span><span class="sxs-lookup"><span data-stu-id="8dd19-174">Expense reports by statistics group</span></span>     |
