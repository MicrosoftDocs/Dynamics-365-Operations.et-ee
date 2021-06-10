---
title: Tööjõu korraldamine osakondade, tööde ja ametikohtade abil
description: Osakonnad, tööd ja ametikohad on organisatsiooni elemendid, mida hallatakse inimressurssides. Selles artiklis kirjeldatakse nende elementide sisulist teavet.
author: andreabichsel
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmPosition, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 87933
ms.assetid: eb5dcacb-a5fe-451d-b30a-7ef14da65d81
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1279cd1eb0d495107515dd40f7d2e0f9dfd5e080
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058820"
---
# <a name="organize-your-workforce-by-using-departments-jobs-and-positions"></a><span data-ttu-id="d3ad8-104">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="d3ad8-104">Organize your workforce by using departments, jobs, and positions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d3ad8-105">Osakonnad, tööd ja ametikohad on organisatsiooni elemendid, mida hallatakse inimressurssides.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-105">Departments, jobs, and positions are organizational elements that are maintained within Human resources.</span></span> <span data-ttu-id="d3ad8-106">Selles artiklis kirjeldatakse nende elementide sisulist teavet.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-106">This article describes conceptual information about these elements.</span></span> 

<span data-ttu-id="d3ad8-107">Järgmise näite abil selgitatakse selles artiklis kirjeldatud põhimõtteid.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-107">The following example is used to illustrate the concepts described in this article.</span></span>

|<span data-ttu-id="d3ad8-108">**Osakond**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-108">**Department**</span></span>|<span data-ttu-id="d3ad8-109">**Ametikoht**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-109">**Position**</span></span>|<span data-ttu-id="d3ad8-110">**Töö**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-110">**Job**</span></span>|
|---|---|---|
|<span data-ttu-id="d3ad8-111">**Müük**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-111">**Sales**</span></span>|<span data-ttu-id="d3ad8-112">Müügijuht (Ida)</span><span class="sxs-lookup"><span data-stu-id="d3ad8-112">Sales manager (East)</span></span>|<span data-ttu-id="d3ad8-113">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-113">Sales manager</span></span>|
|<span data-ttu-id="d3ad8-114">**Müük**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-114">**Sales**</span></span>|<span data-ttu-id="d3ad8-115">Müügijuht (Lääs)</span><span class="sxs-lookup"><span data-stu-id="d3ad8-115">Sales manager (West)</span></span>|<span data-ttu-id="d3ad8-116">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-116">Sales manager</span></span>|
|<span data-ttu-id="d3ad8-117">**Müük**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-117">**Sales**</span></span>|<span data-ttu-id="d3ad8-118">Müügijuht (Kesk)</span><span class="sxs-lookup"><span data-stu-id="d3ad8-118">Sales manager (Central)</span></span>|<span data-ttu-id="d3ad8-119">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-119">Sales manager</span></span>|
|<span data-ttu-id="d3ad8-120">**Raamatupidamine**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-120">**Accounting**</span></span>|<span data-ttu-id="d3ad8-121">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="d3ad8-121">Accounting supervisor</span></span>|<span data-ttu-id="d3ad8-122">Pearaamatupidaja</span><span class="sxs-lookup"><span data-stu-id="d3ad8-122">Accounting manager</span></span>|
|<span data-ttu-id="d3ad8-123">**Raamatupidamine**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-123">**Accounting**</span></span>|<span data-ttu-id="d3ad8-124">Raamatupidamine A</span><span class="sxs-lookup"><span data-stu-id="d3ad8-124">Accounting-A</span></span>|<span data-ttu-id="d3ad8-125">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="d3ad8-125">Accountant</span></span>|
|<span data-ttu-id="d3ad8-126">**Inimressursid**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-126">**Human resources**</span></span>|<span data-ttu-id="d3ad8-127">Personalijuht (Ida)</span><span class="sxs-lookup"><span data-stu-id="d3ad8-127">HR manager (East)</span></span>|<span data-ttu-id="d3ad8-128">Personalijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-128">HR manager</span></span>|
|<span data-ttu-id="d3ad8-129">**Inimressursid**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-129">**Human resources**</span></span>|<span data-ttu-id="d3ad8-130">Personalijuht (Lääs)</span><span class="sxs-lookup"><span data-stu-id="d3ad8-130">HR manager (West)</span></span>|<span data-ttu-id="d3ad8-131">Personalijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-131">HR manager</span></span>|
|<span data-ttu-id="d3ad8-132">**Inimressursid**</span><span class="sxs-lookup"><span data-stu-id="d3ad8-132">**Human resources**</span></span>|<span data-ttu-id="d3ad8-133">Personalijuht (Kesk)</span><span class="sxs-lookup"><span data-stu-id="d3ad8-133">HR manager (Central)</span></span>|<span data-ttu-id="d3ad8-134">Personalijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-134">HR manager</span></span>|


 <a name="departments"></a><span data-ttu-id="d3ad8-135">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="d3ad8-135">Departments</span></span>
------------

<span data-ttu-id="d3ad8-136">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalala, mis vastutab organisatsiooni kindla valdkonna eest, nagu müük või raamatupidamine.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-136">A department is an operating unit that represents a category or functional area of an organization that is responsible for a specific area of the organization, such as sales or accounting.</span></span> <span data-ttu-id="d3ad8-137">Osakonda kasutatakse aruandluseks funktsionaalsete alade kohta ning sel võib olla kasumi ja kahjumi vastutus.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-137">A department is used to report on functional areas and may have profit and loss responsibility.</span></span> <span data-ttu-id="d3ad8-138">Osakond võib sisaldada ka, kulukeskuste gruppi.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-138">Also, a department might include a group of cost centers.</span></span> <span data-ttu-id="d3ad8-139">Organisatsiooni osakonnad on muu hulgas näiteks müük, raamatupidamine ja inimressursid.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-139">Sales, accounting, and human resources are some examples of departments in an organization.</span></span>

## <a name="jobs-and-positions"></a><span data-ttu-id="d3ad8-140"> Tööd ja ametikohad</span><span class="sxs-lookup"><span data-stu-id="d3ad8-140">Jobs and positions</span></span>
<span data-ttu-id="d3ad8-141">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-141">A job is a collection of tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d3ad8-142">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-142">A position is an individual instance of a job.</span></span> <span data-ttu-id="d3ad8-143">Töö jaoks nõutavad vastutusvaldkonnad, tööülesanded, oskused, haridusteave ja serdid on nõutavad ka selle tööga seostatud ametikohtade puhul.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-143">Areas of responsibility, job tasks, job functions, skills, education information, and certificates that are required for a job are also required for positions that are associated with a job.</span></span>
### <a name="job-tasks"></a><span data-ttu-id="d3ad8-144">Tööülesanded</span><span class="sxs-lookup"><span data-stu-id="d3ad8-144">Job tasks</span></span>

<span data-ttu-id="d3ad8-145">Saate luua tööülesandeid, mis kirjeldavad selle töö ametikohal tegutseva töötaja põhiülesandeid.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-145">You can create job tasks that describe the basic tasks that a worker in a position for that job must complete.</span></span> <span data-ttu-id="d3ad8-146">Sama tööülesande saab lisada mitmele tööle ja nende tööde ametikohad pärivad need tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-146">The same job task can be added to multiple jobs, and positions for those jobs will inherit those job tasks.</span></span> <span data-ttu-id="d3ad8-147">Tööülesannete näited on toodud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-147">Examples of job tasks are listed in the following table.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d3ad8-148">Töö</span><span class="sxs-lookup"><span data-stu-id="d3ad8-148">Job</span></span></th>
<th><span data-ttu-id="d3ad8-149">Tööülesanne</span><span class="sxs-lookup"><span data-stu-id="d3ad8-149">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3ad8-150">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-150">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="d3ad8-151"><span class="input">Jõudluse ülevaade</span> – iga müüja tööjõudluse ülevaade.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-151"><span class="input">Perf-review</span> – Review each salesperson’s job performance.</span></span></li>
<li><span data-ttu-id="d3ad8-152"><span class="input">Puudumiste ülevaade</span> – iga müüja puudumistaotluste või registreeringute kinnitamine või tagasilükkamine.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-152"><span class="input">Abs-review</span> – Approve or reject each salesperson’s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ad8-153">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="d3ad8-153">Accountant</span></span></td>
<td><span data-ttu-id="d3ad8-154"><span class="input">Finantsaruanne</span> – iganädalaste finantsaruannete esitamine pealaekurile.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-154"><span class="input">FIN-Report</span> – Present weekly financial reports to chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

### <a name="job-functions"></a><span data-ttu-id="d3ad8-155">Tööfunktsioonid</span><span class="sxs-lookup"><span data-stu-id="d3ad8-155">Job functions</span></span>

<span data-ttu-id="d3ad8-156">Tööfunktsioonid on nagu tööülesanded.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-156">Job functions are like job tasks.</span></span> <span data-ttu-id="d3ad8-157">Tööfunktsioon kirjeldab üht või mitut tööle määratud ülesannet, kohustust või vastutust.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-157">A job function describes one or more tasks, duties or responsibilities that are assigned to a job.</span></span> <span data-ttu-id="d3ad8-158">Tööfunktsioone saab määrata töödele ning kasutada hüvitusplaanide sobivusreeglite rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-158">Job functions can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="d3ad8-159">Tööfunktsioonide näited on toodud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-159">Examples of job functions are listed in the following table.</span></span>

| <span data-ttu-id="d3ad8-160">Töö</span><span class="sxs-lookup"><span data-stu-id="d3ad8-160">Job</span></span>           | <span data-ttu-id="d3ad8-161">Tööfunktsioon</span><span class="sxs-lookup"><span data-stu-id="d3ad8-161">Job function</span></span>                                                |
|---------------|-------------------------------------------------------------|
| <span data-ttu-id="d3ad8-162">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="d3ad8-162">Sales manager</span></span> | <span data-ttu-id="d3ad8-163">Alluvate haldus – teile aru andvate inimeste haldamine.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-163">Mng-people – Manage people who report to you.</span></span>               |
| <span data-ttu-id="d3ad8-164">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="d3ad8-164">Accountant</span></span>    | <span data-ttu-id="d3ad8-165">Finantsülevaade – kontokogumi finantsandmete haldamine.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-165">FIN-Review – Maintain financial data for a set of accounts.</span></span> |

### <a name="job-types"></a><span data-ttu-id="d3ad8-166">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="d3ad8-166">Job types</span></span>

<span data-ttu-id="d3ad8-167">Töötüüpide abil saate liigitada sarnaseid töid kategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-167">Use job types to classify similar jobs into categories.</span></span> <span data-ttu-id="d3ad8-168">Töötüüpe, nagu tööfunktsioonegi, saab määrata töödele ning kasutada hüvitusplaanide sobivusreeglite rakendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-168">Job types, just like job functions, can be assigned to jobs and used to set up and implement eligibility rules for compensation plans.</span></span> <span data-ttu-id="d3ad8-169">Mõni töötüüpide näide on toodud järgmises loendis.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-169">Some examples of job types are included in the following list:</span></span>
-   <span data-ttu-id="d3ad8-170">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="d3ad8-170">Full-time</span></span>
-   <span data-ttu-id="d3ad8-171">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="d3ad8-171">Part-time</span></span>
-   <span data-ttu-id="d3ad8-172">Töötasu</span><span class="sxs-lookup"><span data-stu-id="d3ad8-172">Salary</span></span>
-   <span data-ttu-id="d3ad8-173">Tunnitasu</span><span class="sxs-lookup"><span data-stu-id="d3ad8-173">Hourly pay</span></span>

### <a name="areas-of-responsibility"></a><span data-ttu-id="d3ad8-174">Vastutusalad</span><span class="sxs-lookup"><span data-stu-id="d3ad8-174">Areas of responsibility</span></span>

<span data-ttu-id="d3ad8-175">Vastutusalade abil saate näidata, milliste töörollide, protsesside ja toodete eest selle töö ametikohal tegutsev töötaja vastutab.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-175">Use areas of responsibility to indicate the work roles, processes, and products that a worker in a position for that job would be responsible for.</span></span> <span data-ttu-id="d3ad8-176">„Raamatupidaja” töö vastutusala näide võib olla „Toote A finantsaruandlus”.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-176">An example of an area of responsibility for a job titled “Accountant” might be “Financial reporting for Product A”.</span></span>

<a name="positions"></a><span data-ttu-id="d3ad8-177">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="d3ad8-177">Positions</span></span>
----------

<span data-ttu-id="d3ad8-178">Ametikohad on organisatsioonihierarhia madalama taseme oluline element.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-178">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="d3ad8-179">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-179">A position is an individual instance of a job.</span></span> <span data-ttu-id="d3ad8-180">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-180">For example, the position, “Sales manager (East),” is just one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="d3ad8-181">Ametikohad on osakonnas ja need määratakse töötajatele.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-181">Positions exist in a department and are assigned to workers.</span></span>
### <a name="position-creation-and-maintenance"></a><span data-ttu-id="d3ad8-182">Ametikoha loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="d3ad8-182">Position creation and maintenance</span></span>

-   <span data-ttu-id="d3ad8-183">Saate vaadata ametikohaga seotud süsteemimuudatusi hõlpsasti juurdepääsetaval loendilehel.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-183">You can view a history of position-related system changes in an easy-to-access list page.</span></span>
-   <span data-ttu-id="d3ad8-184">Saate luua põhjusekoode, mida teie kasutajad saavad ametikohti luues või muutes valida.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-184">You can create reason codes that your users can select when they create or modify positions.</span></span>
-   <span data-ttu-id="d3ad8-185">Saate luua personalitegevuste tüüpe ja määrata personalitegevustele numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-185">You can create personnel action types and assign a number sequence to personnel actions.</span></span>
-   <span data-ttu-id="d3ad8-186">Saate seadistada töövoo, nii et ametikoha täiendused ja muudatused nõuaksid kinnitamist.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-186">You can set up workflow so that position additions and changes can require approval.</span></span>

### <a name="position-duration"></a><span data-ttu-id="d3ad8-187">Positsiooni kestus</span><span class="sxs-lookup"><span data-stu-id="d3ad8-187">Position duration</span></span>

<span data-ttu-id="d3ad8-188">Igal ametikohal on kehtivusaeg.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-188">Every position has a length of time that the position is effective.</span></span> <span data-ttu-id="d3ad8-189">Seda ajaperioodi nimetatakse kestuseks.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-189">This length of time is referred to as duration.</span></span> <span data-ttu-id="d3ad8-190">Näiteks võib suviste ametikohtade kestus olla 1. maist 2015 kuni 31. augustini 2015.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-190">For example, summer positions might have duration of May 1, 2015 until August 31, 2015.</span></span>

### <a name="worker-assignments"></a><span data-ttu-id="d3ad8-191">Töötajate määramised</span><span class="sxs-lookup"><span data-stu-id="d3ad8-191">Worker assignments</span></span>

<span data-ttu-id="d3ad8-192">Kui määrate töötaja ametikohale, täidate selle ametikoha.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-192">When you assign a worker to a position, you fill that position.</span></span> <span data-ttu-id="d3ad8-193">Saate määrata töötajad mitmele ametikohale, kuid korraga saab olla ühele ametikohale määratud vaid üks töötaja.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-193">You can assign workers to multiple positions, but only one worker can be assigned to a position at the same time.</span></span>

### <a name="reporting-relationships"></a><span data-ttu-id="d3ad8-194">Aruandluse suhted</span><span class="sxs-lookup"><span data-stu-id="d3ad8-194">Reporting relationships</span></span>

<span data-ttu-id="d3ad8-195">Ametikohad on organisatsioonihierarhia madalama taseme olulised elemendid.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-195">Positions are important elements of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="d3ad8-196">Vormil Ametikoht saate määrata ametikoha, millele see ametikoht aru annab.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-196">In the Position form, you can specify the position that a position reports to.</span></span> <span data-ttu-id="d3ad8-197">Kui määrate töötaja ametikohale, mis annab aru teisele ametikohale, loote neile kahele ametikohale määratud töötajate vahel aruandlusseose.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-197">When you assign a worker to a position that reports to another position, you create a reporting relationship between the workers who are assigned to the two positions.</span></span> <span data-ttu-id="d3ad8-198">Näiteks annab ametikoht „raamatupidaja A” aru ametikohale „raamatupidamise ülevaataja”.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-198">For example, position “Accountant-A” reports to position “Accounting Supervisor”.</span></span> <span data-ttu-id="d3ad8-199">Kim Akers on määratud ametikohale „raamatupidamise ülevaataja” ja Sanjay Patel ametikohale „raamatupidaja A”.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-199">Kim Akers is assigned to position “Accounting Supervisor” and Sanjay Patel is assigned to position “Accountant-A”.</span></span> <span data-ttu-id="d3ad8-200">See tähendab, et Sanjay Patel annab aru Kim Akersile.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-200">This means that Sanjay Patel reports to Kim Akers.</span></span> 

<span data-ttu-id="d3ad8-201">Kui teie organisatsioon kasutab maatrikshierarhiat või mõnd muud kohandatud hierarhiat, saate seadistada ametikohahierarhia tüübid ja seejärel lisada iga seadistatud hierarhiatüübi puhul aruandlusseosed ametikohtadele.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-201">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span> <span data-ttu-id="d3ad8-202">Näiteks on Lori Penor Adventure Worksi üldjuhataja ja määratud ametikohale „üldjuht”.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-202">For example, Lori Penor is a general manager at Adventure Works and is assigned to the “General Manager” position.</span></span> <span data-ttu-id="d3ad8-203">Lori haldab tööriistade puhastamiseks kasutatava toote arendust.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-203">Lori manages the development of a product that is used to clean widgets.</span></span> <span data-ttu-id="d3ad8-204">Lori palub, et raamatupidaja aitaks teda toote arendusel finantsidega.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-204">Lori requires an accountant to help with the finances for developing the product.</span></span> <span data-ttu-id="d3ad8-205">Seetõttu palkaski ta Sanjay Pateli oma raamatupidajaks.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-205">Therefore, she has recruited Sanjay Patel to be the accountant.</span></span> <span data-ttu-id="d3ad8-206">Sanjay annab aru otse Kim Akersile, kuid ta töötab ka Lori Penorile seoses tööriistapuhasti arendusfinantsidega.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-206">Sanjay reports directly to Kim Akers, but also works with Lori Penor on his work related to the finances for developing the widget cleaner.</span></span> 

<span data-ttu-id="d3ad8-207">Eelmise näite puhul peate täitma järgmised ülesanded, et seadistada tööseos Sanjay Pateli ja Lori Penori vahel.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-207">For the previous example, you would complete the following tasks to set up the working relationship between Sanjay Patel and Lori Penor:</span></span>
1.  <span data-ttu-id="d3ad8-208">Looge kohandatud ametikohahierarhia tüüp nimega Tööriist, et luua hierarhia, mis sisaldab tööriistapuhastustootega seotud tööde eest vastutatavaid ametikohti.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-208">Create a custom position hierarchy type called “Widget” to create a hierarchy that includes positions responsible for working on the widget cleaner product.</span></span>
2.  <span data-ttu-id="d3ad8-209">Määrake üldjuhi ametikoht ametikohaks, millele ametikoht „raamatupidaja A” hierarhias Tööriist aru annab.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-209">Assign the General Manager position to be the position that the Accountant-A position reports to in the Widget hierarchy.</span></span>

<span data-ttu-id="d3ad8-210">Ametikohahierarhia abil saate vaadata ametikohtade aruandlusstruktuuri.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-210">Use the position hierarchy to view the reporting structure of positions.</span></span> <span data-ttu-id="d3ad8-211">Kui teil on mitu ametikohahierarhiat, saate vaadata ametikohahierarhia iga hierarhiatüübi hierarhiat.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-211">If you have multiple position hierarchies, you can view the hierarchy for each hierarchy type in the position hierarchy.</span></span> <span data-ttu-id="d3ad8-212">Samuti saate otsida ametikohta ametikoha ID või ametikohale määratud töötaja nime järgi.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-212">Also, you can search for a position by position ID or by the name of the worker who is assigned to the position.</span></span> <span data-ttu-id="d3ad8-213">Ametikohahierarhia on organisatsioonihierarhia.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-213">The position hierarchy is an organizational hierarchy.</span></span>

## <a name="date-effective-records"></a><span data-ttu-id="d3ad8-214">Kehtivuskuupäevade kirjed</span><span class="sxs-lookup"><span data-stu-id="d3ad8-214">Date effective records</span></span>
<span data-ttu-id="d3ad8-215">Mõne kirje puhul saate määrata kirje tulevased muudatused.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-215">For some records, you can specify future changes to the record.</span></span> <span data-ttu-id="d3ad8-216">Järgmine teave on jõustumiskuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-216">The following information is date effective.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d3ad8-217">Kirjed</span><span class="sxs-lookup"><span data-stu-id="d3ad8-217">Records</span></span></th>
<th><span data-ttu-id="d3ad8-218">Jõustumiskuupäeva teave</span><span class="sxs-lookup"><span data-stu-id="d3ad8-218">Date effective information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d3ad8-219">Tööd</span><span class="sxs-lookup"><span data-stu-id="d3ad8-219">Jobs</span></span></td>
<td><ul>
<li><span data-ttu-id="d3ad8-220">Töö üksikasjalik kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d3ad8-220">Some detailed job information</span></span></li>
<li><span data-ttu-id="d3ad8-221">Töö liigitusteave</span><span class="sxs-lookup"><span data-stu-id="d3ad8-221">Job classification information</span></span></li>
<li><span data-ttu-id="d3ad8-222">Hüvituseteave</span><span class="sxs-lookup"><span data-stu-id="d3ad8-222">Compensation information</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d3ad8-223">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="d3ad8-223">Positions</span></span></td>
<td><ul>
<li><span data-ttu-id="d3ad8-224">Ametikoha üksikasjalik kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d3ad8-224">Some detailed position information</span></span></li>
<li><span data-ttu-id="d3ad8-225">Töötajate määramised</span><span class="sxs-lookup"><span data-stu-id="d3ad8-225">Worker assignments</span></span></li>
<li><span data-ttu-id="d3ad8-226">Positsioonikestused</span><span class="sxs-lookup"><span data-stu-id="d3ad8-226">Position durations</span></span></li>
<li><span data-ttu-id="d3ad8-227">Positsioonihierarhiad</span><span class="sxs-lookup"><span data-stu-id="d3ad8-227">Position hierarchies</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d3ad8-228">Saate muuta eelmises tabelis nimetatud ametikoha- ja töö-teavet ning määrata kuupäeva, millal ametikoha või töö muudatused peavad jõustuma.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-228">You can modify the information mentioned in the previous table for a position or a job and specify a date when the modifications to the position or job should take effect.</span></span> <span data-ttu-id="d3ad8-229">Näiteks saab ametikoha määrata ainult ühele töötajale, kuid Sanjay Patel, kes on määratud ametikohale Raamatupidaja A, lahkub kahe nädala pärast.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-229">For example, a position can only be assigned to one worker, but Sanjay Patel, who is assigned to the position Accountant-A, will be leaving in two weeks.</span></span> <span data-ttu-id="d3ad8-230">Sanjay Pateli lahkumisel asendab teda Joe Healy.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-230">Joe Healy will replace Sanjay Patel when Sanjay leaves.</span></span> <span data-ttu-id="d3ad8-231">Kuigi Sanjay on veel oma ametikohale määratud, saate määrata Joe Healy samale ametikohale, nii et määramine jõustub alles pärast Sanjay viimast tööpäeva.</span><span class="sxs-lookup"><span data-stu-id="d3ad8-231">Even though Sanjay is still assigned to his position, you can assign Joe Healy to the same position so that the assignment is effective only after Sanjay’s last day.</span></span>







[!INCLUDE[footer-include](../includes/footer-banner.md)]