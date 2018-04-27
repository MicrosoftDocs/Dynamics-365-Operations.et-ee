---
title: "Töö komponentide seadistamine"
description: "See teema kirjeldab töö võimalikke põhielemente ja toob näiteid, kuidas saate neid elemente oma organisatsioonis kasutada."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 88e8c1ae98ad5618feff3d2bb88d8f8cfe2ff9ba
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="679ea-103">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="679ea-103">Setting up the components of a job</span></span>

[!INCLUDE [banner](includes/banner.md)]

[!INCLUDE [retail name](includes/retail-name.md)]

<span data-ttu-id="679ea-104">See teema kirjeldab töö võimalikke põhielemente ja toob näiteid, kuidas saate neid elemente oma organisatsioonis kasutada.</span><span class="sxs-lookup"><span data-stu-id="679ea-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="679ea-105">Enne tööde loomist tuleb seadistada teatud viiteteave.</span><span class="sxs-lookup"><span data-stu-id="679ea-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="679ea-106">Saate luua töö, millel on ainult nimi.</span><span class="sxs-lookup"><span data-stu-id="679ea-106">You can create a job that has only a name.</span></span> <span data-ttu-id="679ea-107">Täiendava teabe, näiteks ametinimetuse, lisamisega pakute aga tööle määratud ametikohtade vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="679ea-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="679ea-108">Peale selle saab osa sisestatud teavet kasutada teatud töödele tasuplaanide filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="679ea-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="679ea-109">Kui soovite seadistada sobivuse, mida saate kasutada kindlale tööle tasuplaanide filtreerimiseks, peate enne tööde seadistamist seadistama tööfunktsioonid ja töötüübid.</span><span class="sxs-lookup"><span data-stu-id="679ea-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="679ea-110">Kui need vaikeväärtused on saadaval, hoiate tööle ametikohtade lisamisel aega kokku.</span><span class="sxs-lookup"><span data-stu-id="679ea-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="679ea-111">Mõned töö üksikasjad, nagu ametinimetus, töö tüüp ja funktsioon, on kuupäevaliselt jõustuvad.</span><span class="sxs-lookup"><span data-stu-id="679ea-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="679ea-112">Kui loote töö täna, kuid ei lisa nimetatud üksikasju kohe, ja otsite hiljem tööd loomiskuupäeva alusel, siis neid üksikasju ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="679ea-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="679ea-113">Seetõttu peate vajaliku viiteteabe enne selle otsimist looma.</span><span class="sxs-lookup"><span data-stu-id="679ea-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="679ea-114">Nii saate lisada teabe uutele töödele juba nende loomisel.</span><span class="sxs-lookup"><span data-stu-id="679ea-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="679ea-115">Ametinimetused</span><span class="sxs-lookup"><span data-stu-id="679ea-115">Job titles</span></span>
<span data-ttu-id="679ea-116">Enne tööde loomist peate seadistama tööde ametinimetused.</span><span class="sxs-lookup"><span data-stu-id="679ea-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="679ea-117">Ametikohtade ametinimetused tuletatakse töödest, millega ametikohad seotud on.</span><span class="sxs-lookup"><span data-stu-id="679ea-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="679ea-118">Ametinimetusi saate hallata lehel **Ametinimetused**, millele pääsete juurde otsingufunktsiooni abil.</span><span class="sxs-lookup"><span data-stu-id="679ea-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="679ea-119">Lehel **Ametinimetused** saate sisestada ametinimetused, mida kavatsete oma tööde jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="679ea-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="679ea-120">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="679ea-120">Job types</span></span>
<span data-ttu-id="679ea-121">Sarnaste tööde kategooriatesse grupeerimiseks saate kasutada töötüüpe.</span><span class="sxs-lookup"><span data-stu-id="679ea-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="679ea-122">Töötüübid ei ole nõutavad.</span><span class="sxs-lookup"><span data-stu-id="679ea-122">Job types aren't required.</span></span> <span data-ttu-id="679ea-123">Kuid kui te kavatsete kasutada töö tüüpe kompensatsioonihalduse sobivuse reeglite seadistamisel, peaksite seadistama töö tüübid enne tööde seadistamist.</span><span class="sxs-lookup"><span data-stu-id="679ea-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="679ea-124">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ja tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="679ea-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="679ea-125">Töötüüpe saate hallata lehel **Töötüübid**.</span><span class="sxs-lookup"><span data-stu-id="679ea-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="679ea-126">Sisestage lehel **Töötüübid** töötüübi nimi ja lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="679ea-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="679ea-127">Tehke väljal **Vabastatud olek** üks järgmistest valikutest, et näidata selle töötüübiga tööde õiglaste tööstandardite seaduse (FLSA) alusel vabastatud olekut.</span><span class="sxs-lookup"><span data-stu-id="679ea-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="679ea-128">**Vabastatud** – tööd on FLSA alusel ületunnitööst vabastatud.</span><span class="sxs-lookup"><span data-stu-id="679ea-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="679ea-129">**Mittevabastatud** – tööd ei ole FLSA alusel ületunnitööst vabastatud.</span><span class="sxs-lookup"><span data-stu-id="679ea-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="679ea-130">**Ei kohaldu** – FLSA kate ei kohaldu.</span><span class="sxs-lookup"><span data-stu-id="679ea-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="679ea-131">Tööfunktsioonid</span><span class="sxs-lookup"><span data-stu-id="679ea-131">Job functions</span></span>
<span data-ttu-id="679ea-132">Tööfunktsioonid kirjeldavad kõrgetasemelisi funktsioonikategooriaid ja seotud kõrgetasemelisi kohustusi.</span><span class="sxs-lookup"><span data-stu-id="679ea-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="679ea-133">Tööfunktsioonid ei ole nõutavad.</span><span class="sxs-lookup"><span data-stu-id="679ea-133">Job functions aren't required.</span></span> <span data-ttu-id="679ea-134">Saate kasutada tööfunktsioone koos töötüüpidega, et filtreerida konkreetsete tööde tasuplaane.</span><span class="sxs-lookup"><span data-stu-id="679ea-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="679ea-135">Seostage tööfunktsioonid ja töötüübid tasuplaanidega, seadistades sobivuse reeglid lehel **Sobivuse reeglid**.</span><span class="sxs-lookup"><span data-stu-id="679ea-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="679ea-136">Seejärel saate lisada tasuplaanile ka tasemete komplekti, mida rakendada töötüübi/tööfunktsiooni kindla kombinatsiooni korral, mille määratlesite sobivuse reeglitega.</span><span class="sxs-lookup"><span data-stu-id="679ea-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="679ea-137">(Need omadused kehtivad nii fikseeritud kui ka muutuvate tasuplaanide korral.) Kui te kavatsete siiski kasutada tööfunktsioone tasuhalduse jaoks sobivuse reeglite seadistamisel, peate seadistama tööfunktsioonid enne tööde seadistamist.</span><span class="sxs-lookup"><span data-stu-id="679ea-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="679ea-138">Järgmises tabelis on toodud mõned tööfunktsioonide näited.</span><span class="sxs-lookup"><span data-stu-id="679ea-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="679ea-139">Töö</span><span class="sxs-lookup"><span data-stu-id="679ea-139">Job</span></span>           | <span data-ttu-id="679ea-140">Tööfunktsioon</span><span class="sxs-lookup"><span data-stu-id="679ea-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="679ea-141">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="679ea-141">Sales manager</span></span> | <span data-ttu-id="679ea-142">Keskmise taseme haldur</span><span class="sxs-lookup"><span data-stu-id="679ea-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="679ea-143">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="679ea-143">Accountant</span></span>    | <span data-ttu-id="679ea-144">Professionaalid</span><span class="sxs-lookup"><span data-stu-id="679ea-144">Professionals</span></span>        |

<span data-ttu-id="679ea-145">Tööfunktsioone saate hallata lehel **Tööfunktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="679ea-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="679ea-146">Sisestage lehel **Tööfunktsioonid** tööfunktsiooni ID-kood ja lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="679ea-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="679ea-147">Tööülesanded</span><span class="sxs-lookup"><span data-stu-id="679ea-147">Job tasks</span></span>
<span data-ttu-id="679ea-148">Tööülesanded kirjeldavad teatud töö ametikohal tegutseva töötaja põhiülesandeid.</span><span class="sxs-lookup"><span data-stu-id="679ea-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="679ea-149">Sama tööülesande saab lisada mitmele tööle ja neid tööülesandeid kasutavate tööde ametikohtadele.</span><span class="sxs-lookup"><span data-stu-id="679ea-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="679ea-150">Järgmises tabelis on toodud mõned tööülesannete näited.</span><span class="sxs-lookup"><span data-stu-id="679ea-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="679ea-151">Töö</span><span class="sxs-lookup"><span data-stu-id="679ea-151">Job</span></span></th>
<th><span data-ttu-id="679ea-152">Tööülesanne</span><span class="sxs-lookup"><span data-stu-id="679ea-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="679ea-153">Müügijuht</span><span class="sxs-lookup"><span data-stu-id="679ea-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="679ea-154"><strong>Jõudluse ülevaade</strong> – iga müüja tööjõudluse ülevaade.</span><span class="sxs-lookup"><span data-stu-id="679ea-154"><strong>Perf-review</strong> – Review each salesperson&#39;s job performance.</span></span></li>
<li><span data-ttu-id="679ea-155"><strong>Puudumiste ülevaade</strong> – iga müüja puudumistaotluste või registreeringute kinnitamine või tagasilükkamine.</span><span class="sxs-lookup"><span data-stu-id="679ea-155"><strong>Abs-review</strong> – Approve or reject each salesperson&#39;s absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="679ea-156">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="679ea-156">Accountant</span></span></td>
<td><span data-ttu-id="679ea-157"><strong>Finantsaruanne</strong> – iganädalaste finantsaruannete esitamine pealaekurile.</span><span class="sxs-lookup"><span data-stu-id="679ea-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="679ea-158">Tööülesandeid saate hallata lehel **Tööülesanded**.</span><span class="sxs-lookup"><span data-stu-id="679ea-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="679ea-159">Sisestage lehel **Tööülesanded** tööülesande nimi ja lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="679ea-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="679ea-160">Väljale **Märkus** saate soovi korral sisestada ka lisateavet.</span><span class="sxs-lookup"><span data-stu-id="679ea-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="679ea-161">Märkusi saab kindla töö puhul värskendada ilma siia sisestatud märkusi muutmata.</span><span class="sxs-lookup"><span data-stu-id="679ea-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="679ea-162">Vastutusalad</span><span class="sxs-lookup"><span data-stu-id="679ea-162">Areas of responsibility</span></span>
<span data-ttu-id="679ea-163">Vastutusalade abil saate näidata, milliste töörollide, protsesside ja toodete eest selle töö ametikohal tegutsev töötaja vastutab.</span><span class="sxs-lookup"><span data-stu-id="679ea-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="679ea-164">Näiteks töö „Raamatupidaja” vastutusala võib olla „Toote A finantsaruandlus”.</span><span class="sxs-lookup"><span data-stu-id="679ea-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="679ea-165">Vastutusalasid saate hallata lehel **Vastutusalad**, millele pääsete juurde otsingufunktsiooni abil.</span><span class="sxs-lookup"><span data-stu-id="679ea-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="679ea-166">Sisestage lehel **Vastutusalad** vastutusala nimi ja lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="679ea-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="679ea-167">Väljale **Märkus** saate soovi korral sisestada ka lisateavet.</span><span class="sxs-lookup"><span data-stu-id="679ea-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="679ea-168">Märkusi saab kindla töö puhul värskendada ilma siia sisestatud märkusi muutmata.</span><span class="sxs-lookup"><span data-stu-id="679ea-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="steps-for-creating-a-job"></a><span data-ttu-id="679ea-169">Töö loomise juhised</span><span class="sxs-lookup"><span data-stu-id="679ea-169">Steps for creating a job</span></span>
<span data-ttu-id="679ea-170">Uue töö loomise etapiviisilise protseduuri leiate teemast [Uute tööde määratlemine](../fin-and-ops/hr/tasks/define-new-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="679ea-170">Refer to the [Define new jobs](../fin-and-ops/hr/tasks/define-new-jobs.md) topic for the step-by-step procedure for creating a new job.</span></span> 

