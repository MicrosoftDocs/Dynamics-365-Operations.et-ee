---
title: Projektilepingud
description: "Artikkel kirjeldab projektilepinguid ja toob näiteid lepingutest, mida saate erinevatele projektitüüpidele ja rahastamise allikatele luua, ning näitab, kuidas hallata Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis lepinguid ja arveprojekti kliente."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d13362acf70edc03a47662c4c3eff680cc04bd8f
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="project-contracts"></a><span data-ttu-id="5019d-103">Projektilepingud</span><span class="sxs-lookup"><span data-stu-id="5019d-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5019d-104">Artikkel kirjeldab projektilepinguid ja toob näiteid lepingutest, mida saate erinevatele projektitüüpidele ja rahastamise allikatele luua, ning näitab, kuidas hallata Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis lepinguid ja arveprojekti kliente.</span><span class="sxs-lookup"><span data-stu-id="5019d-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="5019d-105">Projektilepingu jaoks loodav projekti tüüp määratleb meetodi, mida kasutatakse projekti klientidele arvete esitamiseks.</span><span class="sxs-lookup"><span data-stu-id="5019d-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="5019d-106">Projekti lepingut ja seotud projekti saab muuta, kuid projekti tüüpi ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="5019d-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="5019d-107">Projektilepingu abil saate koostada samal ajal vähemalt ühe projekti arved.</span><span class="sxs-lookup"><span data-stu-id="5019d-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="5019d-108">Projektileping aitab tagada ka ühtse arveldusprotseduuri kasutamise projektistruktuuri iga alamprojekti puhul.</span><span class="sxs-lookup"><span data-stu-id="5019d-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="5019d-109">Iga projekt, mille kohta arve koostatakse, peab olema seotud projektilepinguga.</span><span class="sxs-lookup"><span data-stu-id="5019d-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="5019d-110">Projektilepingu sätted kehtivad kõigile projektidele ja alamprojektidele, mis on selle projektilepinguga seotud.</span><span class="sxs-lookup"><span data-stu-id="5019d-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="5019d-111">Projektilepingus saab määrata ühe või mitu rahastamisallikat.</span><span class="sxs-lookup"><span data-stu-id="5019d-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="5019d-112">Seetõttu saate jagada arveldamise mitme rahastaja vahel, seadistada rahastamise limiidid, nii et rahastamisallikatele esitatakse arved ainult teatud summa ulatuses, ja konfigureerida kulutuste rahastamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="5019d-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="5019d-113">Projektilepingute rahastamine</span><span class="sxs-lookup"><span data-stu-id="5019d-113">Funding for project contracts</span></span>
<span data-ttu-id="5019d-114">Mõned projektilepingud määravad, et projektikulude rahastamise eest vastutavad ühiselt mitu osapoolt.</span><span class="sxs-lookup"><span data-stu-id="5019d-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="5019d-115">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="5019d-115">Here are some examples:</span></span>

-   <span data-ttu-id="5019d-116">Suur mitme divisjoniga klient soovib jagada projekti rahastamise divisjonide kaupa.</span><span class="sxs-lookup"><span data-stu-id="5019d-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="5019d-117">Teie ettevõtte jagab suure projekti kulusid välise organisatsiooniga.</span><span class="sxs-lookup"><span data-stu-id="5019d-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="5019d-118">Teeprojekti rahastab ühiselt kaks valda.</span><span class="sxs-lookup"><span data-stu-id="5019d-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="5019d-119">Sillaprojekti rahastatakse riigi toetusest ja erakorporatsiooni vahenditest.</span><span class="sxs-lookup"><span data-stu-id="5019d-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="5019d-120">Finance and Operationsis saate jagada ühe kande või kogu projekti arveldused mitme kliendi, toetuse või organisatsiooni vahel.</span><span class="sxs-lookup"><span data-stu-id="5019d-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="5019d-121">Projektides, millel on mitu rahastajat, nimetatakse kõiki osapooli, kes panustavad keerukasse rahastusprojekti, rahastamise allikateks.</span><span class="sxs-lookup"><span data-stu-id="5019d-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="5019d-122">Pärast kliendi, organisatsiooni või toetuse määratlemist rahastamise allikana, saab selle määrata vähemalt ühele rahastamise reeglile.</span><span class="sxs-lookup"><span data-stu-id="5019d-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="5019d-123">Rahastamise reeglid sisaldavad kriteeriume, mis määravad, kuidas kulud projekti erinevate rahastamise allikate vahel jagatakse.</span><span class="sxs-lookup"><span data-stu-id="5019d-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="5019d-124">Kuna ladustatavaid kaupu (näiteks neid, mis on nimetatud ostutaotlustel ja ostutellimustel) ei saa jagada, ei saa kulusummat jaotamise ajal mitme rahastamise allika vahel jagada.</span><span class="sxs-lookup"><span data-stu-id="5019d-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="5019d-125">Seega jääb rahastamise allika väärtuseks 0 (null), kuni sisestatakse lao väljaminek.</span><span class="sxs-lookup"><span data-stu-id="5019d-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="5019d-126">Lao väljamineku sisestamisel jagatakse kulu summa projekti jaotusreeglite järgi.</span><span class="sxs-lookup"><span data-stu-id="5019d-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="5019d-127">Siin on mõned juhised, kuidas hõlbustada arvete jagamist mitme rahastamisallika vahel.</span><span class="sxs-lookup"><span data-stu-id="5019d-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="5019d-128">Määrake, et kõik projekti kohta sisestatud kanded kasutavad sama müügivaluutat, mida projektileping.</span><span class="sxs-lookup"><span data-stu-id="5019d-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="5019d-129">Seadistage rahastamise limiidid, nii et rahastamise allikale ei esitata suuremat arvet kui projektile määratud summa.</span><span class="sxs-lookup"><span data-stu-id="5019d-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="5019d-130">Saate konfigureerida rahastamise reegleid ja rahastamise limiite iga töötaja, kauba, kategooria, kategooriagrupi ja kande tüübi kohta (või kõigi kande tüüpide kohta).</span><span class="sxs-lookup"><span data-stu-id="5019d-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="5019d-131">Valige soovi korral algus- ja lõppkuupäevad, et määratleda iga rahastamise reegli kehtivusperiood.</span><span class="sxs-lookup"><span data-stu-id="5019d-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="5019d-132">Määrake protsent, mille eest iga rahastamise allikas vastutab.</span><span class="sxs-lookup"><span data-stu-id="5019d-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="5019d-133">Määrake milline rahastamise allikas vastutab rahastamise eraldamise arvutustest tekkinud ümarduserinevuste eest.</span><span class="sxs-lookup"><span data-stu-id="5019d-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="5019d-134">Saate seadistada reeglid, mis määravad, kuidas projektikulude eest välistele klientidele ja siseorganisatsioonidele arveid esitatakse.</span><span class="sxs-lookup"><span data-stu-id="5019d-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="5019d-135">Salvestage kanded ooteloleval rahastamise kontol, kuni saate täiendavat rahastamist või kuni otsustate kulud kanda ettevõttesiseselt.</span><span class="sxs-lookup"><span data-stu-id="5019d-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="5019d-136">Määramiseks, millist maksugruppi kandega seostada, otsitakse projektist maksugrupi määrangut.</span><span class="sxs-lookup"><span data-stu-id="5019d-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="5019d-137">Kui ühtegi maksugrupi määrangut projekti tasandil pole, otsitakse projektilepingust.</span><span class="sxs-lookup"><span data-stu-id="5019d-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="5019d-138">Näide: mitu rahastamise allikat (lihtne)</span><span class="sxs-lookup"><span data-stu-id="5019d-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="5019d-139">Järgmises tabelis pakutakse stsenaariume rahastamise mitmele rahastamise allikale eraldamise haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="5019d-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="5019d-140">Need stsenaariumid põhinevad järgmistel eeldustel.</span><span class="sxs-lookup"><span data-stu-id="5019d-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="5019d-141">Prioriteedisätteid arvestatakse vahendite eraldamises enne teiste rahastamise reegli kriteeriumide rakendamist.</span><span class="sxs-lookup"><span data-stu-id="5019d-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="5019d-142">Rahastamise reegli kehtivusperioodi määratlemiseks pole kuupäevavahemikku määratud.</span><span class="sxs-lookup"><span data-stu-id="5019d-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5019d-143"><strong>Stsenaarium</strong></span><span class="sxs-lookup"><span data-stu-id="5019d-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="5019d-144"><strong>Rahastamise allikas </strong></span><span class="sxs-lookup"><span data-stu-id="5019d-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="5019d-145"><strong>Eraldise % </strong></span><span class="sxs-lookup"><span data-stu-id="5019d-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="5019d-146"><strong>Eraldise prioriteet </strong></span><span class="sxs-lookup"><span data-stu-id="5019d-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5019d-147">Soovite määrata kulusid ühele rahastamise allikale, kuni selle vahendid on otsas, eraldada kulusid teisele rahastamise allikale, kuni selle vahendid on otsas ja eraldada lõpuks ülejäänud kulud kolmandale rahastamise allikale.</span><span class="sxs-lookup"><span data-stu-id="5019d-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-148">Rahastamise　allikas　1</span><span class="sxs-lookup"><span data-stu-id="5019d-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="5019d-149">Rahastamise　allikas　2</span><span class="sxs-lookup"><span data-stu-id="5019d-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="5019d-150">Rahastamise　allikas　3</span><span class="sxs-lookup"><span data-stu-id="5019d-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-151">1</span><span class="sxs-lookup"><span data-stu-id="5019d-151">100%</span></span></li>
<li><span data-ttu-id="5019d-152">1</span><span class="sxs-lookup"><span data-stu-id="5019d-152">100%</span></span></li>
<li><span data-ttu-id="5019d-153">1</span><span class="sxs-lookup"><span data-stu-id="5019d-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-154">1</span><span class="sxs-lookup"><span data-stu-id="5019d-154">1</span></span></li>
<li><span data-ttu-id="5019d-155">2</span><span class="sxs-lookup"><span data-stu-id="5019d-155">2</span></span></li>
<li><span data-ttu-id="5019d-156">3</span><span class="sxs-lookup"><span data-stu-id="5019d-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5019d-157">Soovite eraldada 75 protsenti kuludest ühele rahastamise allikale ja 25 protsenti teisele rahastamise allikale.</span><span class="sxs-lookup"><span data-stu-id="5019d-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5019d-158">Kui kumbki neist rahastamise allikatest ammendub, soovite maksta ülejäänud kulud kolmandast rahastamise allikast.</span><span class="sxs-lookup"><span data-stu-id="5019d-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-159">Rahastamise　allikas　1</span><span class="sxs-lookup"><span data-stu-id="5019d-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="5019d-160">Rahastamise　allikas　2</span><span class="sxs-lookup"><span data-stu-id="5019d-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="5019d-161">Rahastamise　allikas　3</span><span class="sxs-lookup"><span data-stu-id="5019d-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-162">75%</span><span class="sxs-lookup"><span data-stu-id="5019d-162">75%</span></span></li>
<li><span data-ttu-id="5019d-163">25%</span><span class="sxs-lookup"><span data-stu-id="5019d-163">25%</span></span></li>
<li><span data-ttu-id="5019d-164">1</span><span class="sxs-lookup"><span data-stu-id="5019d-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-165">1</span><span class="sxs-lookup"><span data-stu-id="5019d-165">1</span></span></li>
<li><span data-ttu-id="5019d-166">1</span><span class="sxs-lookup"><span data-stu-id="5019d-166">1</span></span></li>
<li><span data-ttu-id="5019d-167">2</span><span class="sxs-lookup"><span data-stu-id="5019d-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5019d-168">Soovite eraldada 75 protsenti kuludest ühele rahastamise allikale ja 25 protsenti teisele rahastamise allikale.</span><span class="sxs-lookup"><span data-stu-id="5019d-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5019d-169">Kui kumbki neist rahastamise allikatest ammendub, soovite jagada ülejäänud kulud kolmanda ja neljanda rahastamise allika vahel.</span><span class="sxs-lookup"><span data-stu-id="5019d-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-170">Rahastamise　allikas　1</span><span class="sxs-lookup"><span data-stu-id="5019d-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="5019d-171">Rahastamise　allikas　2</span><span class="sxs-lookup"><span data-stu-id="5019d-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="5019d-172">Rahastamise　allikas　3</span><span class="sxs-lookup"><span data-stu-id="5019d-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="5019d-173">Rahastamise　allikas　4</span><span class="sxs-lookup"><span data-stu-id="5019d-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-174">75%</span><span class="sxs-lookup"><span data-stu-id="5019d-174">75%</span></span></li>
<li><span data-ttu-id="5019d-175">25%</span><span class="sxs-lookup"><span data-stu-id="5019d-175">25%</span></span></li>
<li><span data-ttu-id="5019d-176">0,5</span><span class="sxs-lookup"><span data-stu-id="5019d-176">50%</span></span></li>
<li><span data-ttu-id="5019d-177">0,5</span><span class="sxs-lookup"><span data-stu-id="5019d-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-178">1</span><span class="sxs-lookup"><span data-stu-id="5019d-178">1</span></span></li>
<li><span data-ttu-id="5019d-179">1</span><span class="sxs-lookup"><span data-stu-id="5019d-179">1</span></span></li>
<li><span data-ttu-id="5019d-180">2</span><span class="sxs-lookup"><span data-stu-id="5019d-180">2</span></span></li>
<li><span data-ttu-id="5019d-181">2</span><span class="sxs-lookup"><span data-stu-id="5019d-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5019d-182">Soovite eraldada esimesed 25 protsenti kuludest ühele rahastamise allikale ja ülejäänu teisele rahastamise allikale.</span><span class="sxs-lookup"><span data-stu-id="5019d-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-183">Rahastamise　allikas　1</span><span class="sxs-lookup"><span data-stu-id="5019d-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="5019d-184">Rahastamise　allikas　2</span><span class="sxs-lookup"><span data-stu-id="5019d-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-185">25%</span><span class="sxs-lookup"><span data-stu-id="5019d-185">25%</span></span></li>
<li><span data-ttu-id="5019d-186">1</span><span class="sxs-lookup"><span data-stu-id="5019d-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5019d-187">1</span><span class="sxs-lookup"><span data-stu-id="5019d-187">1</span></span></li>
<li><span data-ttu-id="5019d-188">2</span><span class="sxs-lookup"><span data-stu-id="5019d-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="5019d-189">Näide: mitu rahastamise allikat (keerukas)</span><span class="sxs-lookup"><span data-stu-id="5019d-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="5019d-190">Teil on kolm rahastamise allikat, mida soovite kasutada järgmises järjekorras.</span><span class="sxs-lookup"><span data-stu-id="5019d-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="5019d-191">Kasutate rahastamise allikat 2 ja rahastamisallikat 3 võrdselt, kuni rahastamise allikas 2 on ammendatud.</span><span class="sxs-lookup"><span data-stu-id="5019d-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="5019d-192">Jätkate rahastamise allika 3 kasutamist, kuni see on ammendatud.</span><span class="sxs-lookup"><span data-stu-id="5019d-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="5019d-193">Kasutate rahastamise allikat 1 pärast rahastamise allika 3 ammendamist.</span><span class="sxs-lookup"><span data-stu-id="5019d-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="5019d-194">Selle eesmärgi saavutamiseks tuleb teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="5019d-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="5019d-195">Seadistage rahastamise limiidid rahastamise allikale 2 ja rahastamise allikale 3 nende vastavate summade ulatuses.</span><span class="sxs-lookup"><span data-stu-id="5019d-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="5019d-196">Looge järgmised rahastamise reeglid.</span><span class="sxs-lookup"><span data-stu-id="5019d-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="5019d-197">Reegel 1 (prioriteet 1): eraldate 50 protsenti kannetest rahastamise allikale 2 ja 50 protsenti rahastamise allikale 3.</span><span class="sxs-lookup"><span data-stu-id="5019d-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="5019d-198">Reegel 2 (prioriteet 2): eraldate 100 protsenti kannetest rahastamise allikale 3.</span><span class="sxs-lookup"><span data-stu-id="5019d-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="5019d-199">Reegel 3 (prioriteet 3): eraldate 100 protsenti kannetest rahastamise allikale 1.</span><span class="sxs-lookup"><span data-stu-id="5019d-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="5019d-200">See seadistus toimib, sest kandeid on reeglite ja piirangute suhtes kontrollitud, et määrata, kas neid rakendatakse kande puhul.</span><span class="sxs-lookup"><span data-stu-id="5019d-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="5019d-201">Kui kandele ei rakendata konkreetseid reegleid või piiranguid, kehtib kõigi kannete reegel.</span><span class="sxs-lookup"><span data-stu-id="5019d-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="5019d-202">Kõigi kannete reegel sobib kõigi kannetega.</span><span class="sxs-lookup"><span data-stu-id="5019d-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="5019d-203">Kui leitakse reegel, mis kandele sobib, rakendatakse esmalt selles reeglis eraldatud protsenti, kuid alles pärast seda, kui vastavusi on kontrollitud kõigi seadistatud limiitide suhtes.</span><span class="sxs-lookup"><span data-stu-id="5019d-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="5019d-204">Kui limiit on täis ja rahastamise allika vahendid on otsas, ignoreeritakse rahastamise limiidiga seotud rahastamise reeglit ja programm kontrollib järgmist reeglit, mida rakendatakse.</span><span class="sxs-lookup"><span data-stu-id="5019d-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="5019d-205">Mõnel juhul saab reegli alusel eraldada ainult osa kandest.</span><span class="sxs-lookup"><span data-stu-id="5019d-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="5019d-206">See võib juhtuda limiidi täitumise tõttu kande eraldamisel.</span><span class="sxs-lookup"><span data-stu-id="5019d-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="5019d-207">Sellisel juhul eraldatakse selle reegli alusel igale rahastamise allikale ainult teatud summa, näiteks 50 protsenti.</span><span class="sxs-lookup"><span data-stu-id="5019d-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="5019d-208">Selline on olukord reeglis 1, mida selles osas eelnevalt kirjeldati.</span><span class="sxs-lookup"><span data-stu-id="5019d-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="5019d-209">Jäägid eraldatakse jada järgmise reegli järgi.</span><span class="sxs-lookup"><span data-stu-id="5019d-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="5019d-210">Järgmises tabelis käsitletakse seda stsenaariumi täpsemalt.</span><span class="sxs-lookup"><span data-stu-id="5019d-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5019d-211"><strong>Fookus </strong></span><span class="sxs-lookup"><span data-stu-id="5019d-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="5019d-212"><strong>Üksikasjad</strong></span><span class="sxs-lookup"><span data-stu-id="5019d-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5019d-213">Rahastamisreeglid</span><span class="sxs-lookup"><span data-stu-id="5019d-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-214">Reegel 1 (prioriteet 1) – kõik kanded.</span><span class="sxs-lookup"><span data-stu-id="5019d-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="5019d-215">Eraldage rahastamise allikale 2 50% ja rahastamise allikale 3 50%.</span><span class="sxs-lookup"><span data-stu-id="5019d-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="5019d-216">Reegel 2 (prioriteet 2) – kõik kanded.</span><span class="sxs-lookup"><span data-stu-id="5019d-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="5019d-217">Eraldage rahastamise allikale 3 100%.</span><span class="sxs-lookup"><span data-stu-id="5019d-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="5019d-218">Reegel 3 (prioriteet 2) – kõik kanded.</span><span class="sxs-lookup"><span data-stu-id="5019d-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="5019d-219">Eraldage rahastamise allikale 1 100%.</span><span class="sxs-lookup"><span data-stu-id="5019d-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5019d-220">Rahastamise limiidid</span><span class="sxs-lookup"><span data-stu-id="5019d-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-221">Rahastamise allika 1 limiit = 10 000.00</span><span class="sxs-lookup"><span data-stu-id="5019d-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="5019d-222">Rahastamise allika 2 limiit = 500.00</span><span class="sxs-lookup"><span data-stu-id="5019d-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="5019d-223">Rahastamise allika 3 limiit = 750.00</span><span class="sxs-lookup"><span data-stu-id="5019d-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5019d-224">Kanne 1</span><span class="sxs-lookup"><span data-stu-id="5019d-224">Transaction 1</span></span></td>
<td><span data-ttu-id="5019d-225"><strong>Kande summa:</strong> 100.00<strong>Rahastamine:</strong> Kande eest tasutakse ainult reegli 1 alusel, kuna kanne on pärast reegli 1 rakendamist täielikult makstud.</span><span class="sxs-lookup"><span data-stu-id="5019d-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="5019d-226">Kanne rahastatakse võrdselt rahastamise allikast 2 ja rahastamise allikast 3.</span><span class="sxs-lookup"><span data-stu-id="5019d-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="5019d-227">Rahastamise allikas 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="5019d-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="5019d-228">Rahastamise allikas 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="5019d-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5019d-229">Kanne 2</span><span class="sxs-lookup"><span data-stu-id="5019d-229">Transaction 2</span></span></td>
<td><span data-ttu-id="5019d-230"><strong>Kande summa:</strong> 5000.00<strong>Rahastamine:</strong> Kande eest makstakse kõigi kolme reegli alusel.<strong>Reegel 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="5019d-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="5019d-231">Rahastamise allikas 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="5019d-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="5019d-232">Rahastamise allikas 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="5019d-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="5019d-233">
<strong>Reegel 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="5019d-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="5019d-234">Rahastamise allikas 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="5019d-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="5019d-235">
<strong>Reegel 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="5019d-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="5019d-236">Rahastamise allikas 1: 3850.00 (= 5000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="5019d-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5019d-237">Igale rahastamisallikale jaotatav vahendite koondsumma</span><span class="sxs-lookup"><span data-stu-id="5019d-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="5019d-238">Rahastamise allikas 1: 3850.00</span><span class="sxs-lookup"><span data-stu-id="5019d-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="5019d-239">Rahastamise allikas 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="5019d-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="5019d-240">Rahastamise allikas 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="5019d-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="5019d-241">Arveldusreeglid</span><span class="sxs-lookup"><span data-stu-id="5019d-241">Billing rules</span></span>
<span data-ttu-id="5019d-242">Kliendiga projektilepingu läbirääkimisi pidades saate määratleda, kuidas ja millal kliendile projekti raames tehtava töö eest arve esitate.</span><span class="sxs-lookup"><span data-stu-id="5019d-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="5019d-243">Pärast projektilepingu ja projekti seadistamist saate seadistada projekti arveldusreeglid.</span><span class="sxs-lookup"><span data-stu-id="5019d-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="5019d-244">Arveldusreeglid põhinevad projektilepingus määratud projekti tingimustel.</span><span class="sxs-lookup"><span data-stu-id="5019d-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="5019d-245">Arveldusreeglid, mida saate luua, sõltuvad projektilepingu tingimustest ja projekti tüübist (nt aeg ja materjal või fikseeritud hind), mille arveldusreegliga seostate.</span><span class="sxs-lookup"><span data-stu-id="5019d-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="5019d-246">Saate luua projekti lepingu jaoks rohkem kui ühe arveldusreegli.</span><span class="sxs-lookup"><span data-stu-id="5019d-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="5019d-247">Saate määrata arveldusreegli mitmele sama projektilepinguga seotud sarnaste maksetingimustega projektile.</span><span class="sxs-lookup"><span data-stu-id="5019d-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="5019d-248">Saate seadistada järgmist tüüpi arveldusreegleid.</span><span class="sxs-lookup"><span data-stu-id="5019d-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="5019d-249">**Tarneühik** – kliendile esitatakse arve, kui tarneühik on lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="5019d-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="5019d-250">Tarneühikud määratletakse lepingus.</span><span class="sxs-lookup"><span data-stu-id="5019d-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="5019d-251">**Edenemine** – kliendile esitatakse arve määratud projekti osa lõpetamisel.</span><span class="sxs-lookup"><span data-stu-id="5019d-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="5019d-252">Saate seadistada arveldusreegli lõpetatud töö protsendi automaatseks arvutamiseks või saate arvutada lõpetatud töö protsendi ja kliendi arvele lisatava summa käsitsi.</span><span class="sxs-lookup"><span data-stu-id="5019d-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="5019d-253">**Vahe-eesmärk** – kliendile esitatakse arve projekti vahe-eesmärgi kogu summa ulatuses, kui projekti vahe-eesmärk on saavutatud.</span><span class="sxs-lookup"><span data-stu-id="5019d-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="5019d-254">**Tasu**– kliendi arvele lisatakse tasu teenuste eest ja juhtimistasu, mis on tavaliselt protsent teenuste hinnast.</span><span class="sxs-lookup"><span data-stu-id="5019d-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="5019d-255">**Aeg ja materjal**– kliendile esitatakse arve projektis kasutatava aja- ja materjalikulu ulatuses.</span><span class="sxs-lookup"><span data-stu-id="5019d-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="5019d-256">Kõigi arveldusreeglite tüüpide puhul saate määrata kinnipeetava protsendimäära, mis arvestatakse kliendi arvetelt maha, kuni protsent jõuab kokkulepitud etappi.</span><span class="sxs-lookup"><span data-stu-id="5019d-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="5019d-257">Maksest kinnipeetav protsendimäär on määratud projektilepingus.</span><span class="sxs-lookup"><span data-stu-id="5019d-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="5019d-258">Summa arvutatakse ja lahutatakse kliendiarve ridade koguväärtusest.</span><span class="sxs-lookup"><span data-stu-id="5019d-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="5019d-259">Arveldusreeglite **Aeg ja materjal** ning **Edenemine** puhul saate määrata arveldatavad kategooriad.</span><span class="sxs-lookup"><span data-stu-id="5019d-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="5019d-260">Arveldatavad kategooriad näitavad kandeid, mis tuleb kliendiarvetele lisada.</span><span class="sxs-lookup"><span data-stu-id="5019d-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="5019d-261">Kui olete valmis kliendile arvet esitama, arvestatakse arveldusreeglite alusel projekti arve summa ja koostatakse projekti arvesoovitus.</span><span class="sxs-lookup"><span data-stu-id="5019d-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="5019d-262">Järgmistes jaotistes on näited projekti arveldusreeglite seadistamise ja haldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="5019d-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="5019d-263">Näide: tarnitud ühikutel põhineva arveldusreegli loomine</span><span class="sxs-lookup"><span data-stu-id="5019d-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="5019d-264">Teie organisatsioon sõlmib lepingu kokku viie koolituskursuse korraldamises kliendi töötajatele hinnaga 10 000 ühe koolituskursuse kohta.</span><span class="sxs-lookup"><span data-stu-id="5019d-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="5019d-265">Esitate pärast iga koolituskursust kliendile arve.</span><span class="sxs-lookup"><span data-stu-id="5019d-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="5019d-266">Lepingu arveldusreeglite seadistamisel kasutate järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="5019d-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="5019d-267">Tarneühik on üks koolituskursus.</span><span class="sxs-lookup"><span data-stu-id="5019d-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="5019d-268">Ühiku hind on 10 000 koolituskursuse kohta.</span><span class="sxs-lookup"><span data-stu-id="5019d-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="5019d-269">Ühikute arv on viis koolituskursust.</span><span class="sxs-lookup"><span data-stu-id="5019d-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="5019d-270">Kui olete ühe koolituskursuse lõpetanud, koostate esimese ühiku kohta arve summas 10 000 ja saadate arve kliendile.</span><span class="sxs-lookup"><span data-stu-id="5019d-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="5019d-271">Näide: projekti teatud (käsitsi arvutatud) osa valmimisel põhineva arveldusreegli loomine</span><span class="sxs-lookup"><span data-stu-id="5019d-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="5019d-272">Teie organisatsioon, tarkvarakonsultatsioone pakkuv firma, sõlmib kliendiga lepingu kliendi arendatava toote osa arendamiseks.</span><span class="sxs-lookup"><span data-stu-id="5019d-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="5019d-273">Teie organisatsioon nõustub edastama programmi kuue kuu jooksul.</span><span class="sxs-lookup"><span data-stu-id="5019d-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="5019d-274">Klient nõustub maksma teie organisatsioonile töö eest kokku 100 000.</span><span class="sxs-lookup"><span data-stu-id="5019d-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="5019d-275">Loote arveldusreegli kliendile arve esitamiseks projekti raames tehtud töö protsendi eest, vastavalt lepingu sätetele.</span><span class="sxs-lookup"><span data-stu-id="5019d-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="5019d-276">Esimese kuu lõpus saate kliendiga kokku, et määrata tehtud töö protsent.</span><span class="sxs-lookup"><span data-stu-id="5019d-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="5019d-277">Projekti ülevaatamisel leiate ühiselt, et projektist on valmis 15%.</span><span class="sxs-lookup"><span data-stu-id="5019d-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="5019d-278">Koostate arve summale 15 000 (15 protsenti summast 100 000) ja saadate selle kliendile.</span><span class="sxs-lookup"><span data-stu-id="5019d-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="5019d-279">Näide: projekti teatud (automaatselt arvutatud) osa valmimisel põhineva arveldusreegli loomine</span><span class="sxs-lookup"><span data-stu-id="5019d-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="5019d-280">Teie organisatsioon, tarkvaraarendusettevõte, nõustub töötama kliendile välja palgaarvestuse paketi tasu eest 30 000.</span><span class="sxs-lookup"><span data-stu-id="5019d-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="5019d-281">Klient nõustub maksma teie organisatsioonile valmis töö protsendi alusel.</span><span class="sxs-lookup"><span data-stu-id="5019d-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="5019d-282">Hindate projekti maksumuseks 20 000.</span><span class="sxs-lookup"><span data-stu-id="5019d-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="5019d-283">Projektilepingus on ära toodud töökategooriad, mida arveldusprotsessis kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="5019d-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="5019d-284">Saate seadistada arveldusreeglid, mis arvutavad automaatselt arvesummad iga kategooria lõpuleviidud töö protsendi jaoks.</span><span class="sxs-lookup"><span data-stu-id="5019d-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="5019d-285">Seadistate iga kategooria eelarve.</span><span class="sxs-lookup"><span data-stu-id="5019d-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="5019d-286">**Arendus** – kulu 15 000 ja tulu 20 000</span><span class="sxs-lookup"><span data-stu-id="5019d-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="5019d-287">**Paigaldus** – kulu 5000 ja tulu 10 000</span><span class="sxs-lookup"><span data-stu-id="5019d-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="5019d-288">Esmakordsel kliendiarve koostamisel arvutatakse arve summa automaatselt järgmiste andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="5019d-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="5019d-289">Ühe kuu pärast esitab projektiga seotud töötaja projekti ajatabeli.</span><span class="sxs-lookup"><span data-stu-id="5019d-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="5019d-290">Töötaja tundide maksumus on 5000 arenduse ja 1000 installimise eest.</span><span class="sxs-lookup"><span data-stu-id="5019d-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="5019d-291">Arendustööst on valminud 33 protsenti (5000 tegelik kulu / 15 000 eelarvekulu) ja installimistööst on valminud 20 protsenti (1000 tegelik kulu / 5000 eelarvekulu).</span><span class="sxs-lookup"><span data-stu-id="5019d-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="5019d-292">Arve summa 8667 arvutatakse automaatselt (33 protsenti summast 20 000 + 20 protsenti summast 10 000).</span><span class="sxs-lookup"><span data-stu-id="5019d-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="5019d-293">Koostate arve summale 8667 ja saadate selle kliendile.</span><span class="sxs-lookup"><span data-stu-id="5019d-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="5019d-294">Näide: kokkulepitud vahe-eesmärkidel põhineva arveldusreegli loomine</span><span class="sxs-lookup"><span data-stu-id="5019d-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="5019d-295">Teie organisatsioon, juhtimiskonsultatsioonide firma, nõustub viima läbi turu-uuringu tarbekauba kohta, mida klient müüa kavatseb.</span><span class="sxs-lookup"><span data-stu-id="5019d-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="5019d-296">Klient nõustub kasutama teie teenuseid kolme kuu jooksul, alates märtsist, ja nõustub tasuma teie organisatsioonile 50 000.</span><span class="sxs-lookup"><span data-stu-id="5019d-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="5019d-297">Projektil on kolm vahetähtaega.</span><span class="sxs-lookup"><span data-stu-id="5019d-297">The project has three milestones:</span></span>

-   <span data-ttu-id="5019d-298">Vahe-eesmärk 1: tarbijaandmete kogumine – 31. märts</span><span class="sxs-lookup"><span data-stu-id="5019d-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="5019d-299">Vahe-eesmärk 2: tarbijaandmete analüüsimine – 30. aprill</span><span class="sxs-lookup"><span data-stu-id="5019d-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="5019d-300">Vahe-eesmärk 3: toote elujõulisuse soovituse esitamine – 31. mai</span><span class="sxs-lookup"><span data-stu-id="5019d-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="5019d-301">Klient nõustub maksma teie organisatsioonile 10 000 esimese vahe-eesmärgi, 20 000 teise vahe-eesmärgi ja 20 000 kolmanda vahe-eesmärgi eest.</span><span class="sxs-lookup"><span data-stu-id="5019d-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="5019d-302">Projektilepingu seadistamisel lepite kokku, et esitate kliendile arveid saavutatud vahe-eesmärkide alusel.</span><span class="sxs-lookup"><span data-stu-id="5019d-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="5019d-303">Arveldusreegli seadistus koosneb järgmistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="5019d-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="5019d-304">Projekti vahe-eesmärkide määratlemine.</span><span class="sxs-lookup"><span data-stu-id="5019d-304">Define the project milestones.</span></span>
-   <span data-ttu-id="5019d-305">Määratlege summa, mille eest kliendile iga vahe-eesmärgi täitmise puhul arve esitatakse.</span><span class="sxs-lookup"><span data-stu-id="5019d-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="5019d-306">Esimese vahe-eesmärgi saavutamisel 31. märtsil märgite vahe-eesmärgi saavutatuks, koostate arve summas 10 000 ja saadate selle kliendile.</span><span class="sxs-lookup"><span data-stu-id="5019d-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="5019d-307">Vahe-eesmärgi kohta ei saa esitada arvet enne, kui olete vahe-eesmärgi saavutatuks märkinud.</span><span class="sxs-lookup"><span data-stu-id="5019d-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="5019d-308">Näide: arveldusreegli loomine teenuste ja juhtimistasu põhjal</span><span class="sxs-lookup"><span data-stu-id="5019d-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="5019d-309">Teie organisatsioon, juhtimiskonsultatsioonide firma, nõustub viima läbi turu-uuringu, et hinnata kliendi (jaemüügiettevõtte) arendatava toote elujõulisust.</span><span class="sxs-lookup"><span data-stu-id="5019d-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="5019d-310">Lepingu tingimustes on kirjas, et teenuseid osutavad teie kolm parimat juhtimiskonsultanti, kes viivad uuringu läbi aja- ja materjalikulu alusel.</span><span class="sxs-lookup"><span data-stu-id="5019d-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="5019d-311">Klient nõustub maksma tunni kohta 100 pluss 10 protsenti juhtimistasu projekti raames arvestatud konsulteerimistundide eest.</span><span class="sxs-lookup"><span data-stu-id="5019d-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5019d-312">Projektilepingu seadistamisel saate luua arveldusreegli 10 protsendi juhtimistasu lisamiseks projekti raames arvestatud konsulteerimistundidele.</span><span class="sxs-lookup"><span data-stu-id="5019d-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5019d-313">Kliendi arvele lisatakse 10 protsendi suurune juhtimistasu pluss konsulteerimistundide hind.</span><span class="sxs-lookup"><span data-stu-id="5019d-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="5019d-314">Näiteks kui kolm konsultanti töötas projektiga kokku 200 tundi, koostatakse arve summas 22 000, kasutades järgmist arvutust.</span><span class="sxs-lookup"><span data-stu-id="5019d-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="5019d-315">200 tundi tunnitasuga 100 = 20 000</span><span class="sxs-lookup"><span data-stu-id="5019d-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="5019d-316">10 protsenti juhtimistasu = 2000</span><span class="sxs-lookup"><span data-stu-id="5019d-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="5019d-317">Arve kogusumma = 22 000</span><span class="sxs-lookup"><span data-stu-id="5019d-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="5019d-318">Kui tasud on kliendi puhul maksustatavad ja valite projektilepingus käibemaksugrupi, sisestatakse käibemaksugrupp automaatselt tasude arveldusreeglisse.</span><span class="sxs-lookup"><span data-stu-id="5019d-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="5019d-319">Näide: arveldusreegli loomine aja ja materjali väärtuse kohta</span><span class="sxs-lookup"><span data-stu-id="5019d-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="5019d-320">Teie organisatsioon, tarkvarakonsultatsioonide firma, nõustub andma viis tehnilist konsultanti, kes töötavad kliendi tarkvara arendusprojektiga järgmise kuue kuu jooksul.</span><span class="sxs-lookup"><span data-stu-id="5019d-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="5019d-321">Klient nõustub maksma 150 iga nõustamistunni eest pluss kontoritarvete maksumuse.</span><span class="sxs-lookup"><span data-stu-id="5019d-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="5019d-322">Teie organisatsiooni saadab kliendile iga kuu lõpus arve.</span><span class="sxs-lookup"><span data-stu-id="5019d-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="5019d-323">Projektilepingu seadistamisel lepite kokku, et esitate kliendile arveid igakuiselt projekti aja- ja materjalikulu eest.</span><span class="sxs-lookup"><span data-stu-id="5019d-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="5019d-324">Saate luua arveldusreegli, mis sisaldab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="5019d-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="5019d-325">Lepingu kestus on kuus kuud.</span><span class="sxs-lookup"><span data-stu-id="5019d-325">The contract period is six months.</span></span>
-   <span data-ttu-id="5019d-326">Konsultatsiooniaja hind tunni kohta on 150.</span><span class="sxs-lookup"><span data-stu-id="5019d-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="5019d-327">Kontoritarvete eest küsitakse tasu tegeliku kulu alusel ja projekti kulu kokku ei tohi olla üle 10 000.</span><span class="sxs-lookup"><span data-stu-id="5019d-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="5019d-328">Koostate projekti vältel kliendile iga kalendrikuu lõpus arve.</span><span class="sxs-lookup"><span data-stu-id="5019d-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="5019d-329">Esimese kuu jooksul registreerivad konsultandid projektile kokku 800 tundi.</span><span class="sxs-lookup"><span data-stu-id="5019d-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="5019d-330">Projekti kontoritarvete kulu on 2000.</span><span class="sxs-lookup"><span data-stu-id="5019d-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="5019d-331">Seega koostate kuu lõpus arve summas 122 000, mis sisaldab 800 tundi hinnaga 150 tunni kohta pluss 2000 kontoritarvete eest.</span><span class="sxs-lookup"><span data-stu-id="5019d-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




