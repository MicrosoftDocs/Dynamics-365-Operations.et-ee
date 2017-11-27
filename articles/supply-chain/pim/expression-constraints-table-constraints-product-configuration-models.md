---
title: Avaldisepiirangud ja tabelipiirangud toote konfiguratsioonimudelites
description: "Selles teemas kirjeldatakse avaldise piirangute ja tabeli piirangute kasutamist. Piirangute abil kontrollitakse atribuutide väärtusi, mida saab valida toodete konfigureerimisel müügitellimuse, müügipakkumise, ostutellimuse või tootmistellimuse jaoks. Saate avaldise piiranguid või tabeli piiranguid kasutada sõltuvalt sellest, kuidas soovite piiranguid luua."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e4719ace2247eb95ed711b0c82e7d9bc8ec5c60c
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a><span data-ttu-id="6319c-105">Avaldisepiirangud ja tabelipiirangud toote konfiguratsioonimudelites</span><span class="sxs-lookup"><span data-stu-id="6319c-105">Expression constraints and table constraints in product configuration models</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6319c-106">Selles teemas kirjeldatakse avaldise piirangute ja tabeli piirangute kasutamist.</span><span class="sxs-lookup"><span data-stu-id="6319c-106">This topic describes the use of expression constraints and table constraints.</span></span> <span data-ttu-id="6319c-107">Piirangute abil kontrollitakse atribuutide väärtusi, mida saab valida toodete konfigureerimisel müügitellimuse, müügipakkumise, ostutellimuse või tootmistellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="6319c-107">Constraints control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="6319c-108">Saate avaldise piiranguid või tabeli piiranguid kasutada sõltuvalt sellest, kuidas soovite piiranguid luua.</span><span class="sxs-lookup"><span data-stu-id="6319c-108">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> 

<span data-ttu-id="6319c-109">Piirangute abil juhitakse atribuutide väärtusi, mida saab valida toodete konfigureerimisel müügitellimuse, müügipakkumise, ostutellimuse või tootmistellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="6319c-109">Constraints are used to control the attribute values that you can select when you configure products for a sales order, sales quotation, purchase order, or production order.</span></span> <span data-ttu-id="6319c-110">Saate avaldise piiranguid või tabeli piiranguid kasutada sõltuvalt sellest, kuidas soovite piiranguid luua.</span><span class="sxs-lookup"><span data-stu-id="6319c-110">You can use expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span>

## <a name="what-are-expression-constraints"></a><span data-ttu-id="6319c-111">Mis on avaldise piirangud?</span><span class="sxs-lookup"><span data-stu-id="6319c-111">What are expression constraints?</span></span>
<span data-ttu-id="6319c-112">Avaldise piiranguid iseloomustab avaldis, milles kasutatakse aritmeetilisi ja kahendmuutujaid ning funktsioone.</span><span class="sxs-lookup"><span data-stu-id="6319c-112">Expression constraints are characterized by an expression that uses arithmetic and Boolean operators and functions.</span></span> <span data-ttu-id="6319c-113">Avaldise piirang kirjutatakse konkreetsele toote konfiguratsioonimudeli komponendile.</span><span class="sxs-lookup"><span data-stu-id="6319c-113">An expression constraint is written for a specific component in a product configuration model.</span></span> <span data-ttu-id="6319c-114">Seda ei saa uuesti kasutada või teise komponendiga jagada.</span><span class="sxs-lookup"><span data-stu-id="6319c-114">It can't be reused by or shared with another component.</span></span> <span data-ttu-id="6319c-115">Kuid komponendi avaldise piirangud võivad viidata komponendi alamkomponentide atribuutidele.</span><span class="sxs-lookup"><span data-stu-id="6319c-115">However, the expression constraints for a component can reference attributes of the component's subcomponents.</span></span>

## <a name="what-are-table-constraints"></a><span data-ttu-id="6319c-116">Mis on tabeli piirangud?</span><span class="sxs-lookup"><span data-stu-id="6319c-116">What are table constraints?</span></span>
<span data-ttu-id="6319c-117">Tabeli piirangud loetlevad väärtuste kombinatsioonid, mis toote konfigureerimisel atribuutide puhul lubatud on.</span><span class="sxs-lookup"><span data-stu-id="6319c-117">Table constraints list the combinations of values that are allowed for attributes when you configure a product.</span></span> <span data-ttu-id="6319c-118">Tabeli piirangu definitsioone saab üldiselt kasutada.</span><span class="sxs-lookup"><span data-stu-id="6319c-118">Table constraint definitions can be used generically.</span></span> <span data-ttu-id="6319c-119">Komponendile toote konfiguratsioonimudelis tabeli piirangu loomisel tuleb valida tabeli piirangu definitsioon.</span><span class="sxs-lookup"><span data-stu-id="6319c-119">When you create a table constraint for a component in a product configuration model, you select a table constraint definition.</span></span> <span data-ttu-id="6319c-120">Lubatud kombinatsioonide loomiseks tuleb lisada komponentidele teatud tüüpi atribuudid.</span><span class="sxs-lookup"><span data-stu-id="6319c-120">To create the combinations that are allowed, you add attributes of specific types to the components.</span></span> <span data-ttu-id="6319c-121">Igal atribuudi tüübil on kindel väärtus.</span><span class="sxs-lookup"><span data-stu-id="6319c-121">Each attribute type has a specific value.</span></span>

### <a name="example-of-a-table-constraint"></a><span data-ttu-id="6319c-122">Tabeli piirangu näide</span><span class="sxs-lookup"><span data-stu-id="6319c-122">Example of a table constraint</span></span>

<span data-ttu-id="6319c-123">Selles näites selgitatakse, kuidas saate piirata kõlari konfiguratsiooni kindla korpuseviimistluse ja esiküljega.</span><span class="sxs-lookup"><span data-stu-id="6319c-123">This example shows how you can limit the configuration of a speaker to specific cabinet finishes and fronts.</span></span> <span data-ttu-id="6319c-124">Esimeses tabelis on üldkonfiguratsiooniks saadaolevad korpuseviimistlused ja esiküljed.</span><span class="sxs-lookup"><span data-stu-id="6319c-124">The first table shows the cabinet finishes and fronts that are generally available for configuration.</span></span> <span data-ttu-id="6319c-125">Atribuuditüüpidele **Korpuseviimistlus** ja **Esivõre** on väärtused määratletud.</span><span class="sxs-lookup"><span data-stu-id="6319c-125">The values are defined for the **Cabinet finish** and **Front grill** attribute types.</span></span>

| <span data-ttu-id="6319c-126">Atribuudi tüüp</span><span class="sxs-lookup"><span data-stu-id="6319c-126">Attribute type</span></span> | <span data-ttu-id="6319c-127">Väärtused</span><span class="sxs-lookup"><span data-stu-id="6319c-127">Values</span></span>                      |
|----------------|-----------------------------|
| <span data-ttu-id="6319c-128">Kabinetiviimistlus</span><span class="sxs-lookup"><span data-stu-id="6319c-128">Cabinet finish</span></span> | <span data-ttu-id="6319c-129">Must, tamm, roosipuu, valge</span><span class="sxs-lookup"><span data-stu-id="6319c-129">Black, Oak, Rosewood, White</span></span> |
| <span data-ttu-id="6319c-130">Esivõre</span><span class="sxs-lookup"><span data-stu-id="6319c-130">Front grill</span></span>    | <span data-ttu-id="6319c-131">Must, metall, valge</span><span class="sxs-lookup"><span data-stu-id="6319c-131">Black, Metal, White</span></span>         |

<span data-ttu-id="6319c-132">Järgmises tabelis on toodud kombinatsioonid, mis on määratletud tabelipiiranguga **Värv ja viimistlus**.</span><span class="sxs-lookup"><span data-stu-id="6319c-132">The next table shows the combinations that are defined by the **Color and finish** table constraint.</span></span> <span data-ttu-id="6319c-133">Selle tabelipiirangu abil saate konfigureerida tammeviimistluse ja musta võrega kõlari, roosipuust viimistluse ja valge võrega kõlari jne.</span><span class="sxs-lookup"><span data-stu-id="6319c-133">By using this table constraint, you can configure a speaker that has an oak finish and a black grill, a Rosewood finish and a white grill, and so on.</span></span>

| <span data-ttu-id="6319c-134">Valmis</span><span class="sxs-lookup"><span data-stu-id="6319c-134">Finish</span></span>         | <span data-ttu-id="6319c-135">Võre</span><span class="sxs-lookup"><span data-stu-id="6319c-135">Grill</span></span>                       |
|----------------|-----------------------------|
| <span data-ttu-id="6319c-136">Tamm</span><span class="sxs-lookup"><span data-stu-id="6319c-136">Oak</span></span>            | <span data-ttu-id="6319c-137">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-137">Black</span></span>                       |
| <span data-ttu-id="6319c-138">Roosipuu</span><span class="sxs-lookup"><span data-stu-id="6319c-138">Rosewood</span></span>       | <span data-ttu-id="6319c-139">Valge</span><span class="sxs-lookup"><span data-stu-id="6319c-139">White</span></span>                       |
| <span data-ttu-id="6319c-140">Valge</span><span class="sxs-lookup"><span data-stu-id="6319c-140">White</span></span>          | <span data-ttu-id="6319c-141">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-141">Black</span></span>                       |
| <span data-ttu-id="6319c-142">Valge</span><span class="sxs-lookup"><span data-stu-id="6319c-142">White</span></span>          | <span data-ttu-id="6319c-143">Valge</span><span class="sxs-lookup"><span data-stu-id="6319c-143">White</span></span>                       |
| <span data-ttu-id="6319c-144">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-144">Black</span></span>          | <span data-ttu-id="6319c-145">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-145">Black</span></span>                       |
| <span data-ttu-id="6319c-146">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-146">Black</span></span>          | <span data-ttu-id="6319c-147">Metall</span><span class="sxs-lookup"><span data-stu-id="6319c-147">Metal</span></span>                       | 

<span data-ttu-id="6319c-148">Saate luua süsteemi ja kasutaja määratletud tabeli piiranguid.</span><span class="sxs-lookup"><span data-stu-id="6319c-148">You can create system-defined and user-defined table constraints.</span></span> <span data-ttu-id="6319c-149">Lisateabe saamiseks vt jaotist [Süsteemi määratletud ja kasutaja määratletud tabelipiirangud](system-defined-user-defined-table-constraints.md).</span><span class="sxs-lookup"><span data-stu-id="6319c-149">For more information, see [System-defined and user-defined table constraints](system-defined-user-defined-table-constraints.md).</span></span>

## <a name="what-syntax-should-be-used-to-write-constraints"></a><span data-ttu-id="6319c-150">Millist süntaksit tuleks piirangute kirjutamisel kasutada?</span><span class="sxs-lookup"><span data-stu-id="6319c-150">What syntax should be used to write constraints?</span></span>
<span data-ttu-id="6319c-151">Piirangute kirjutamisel tuleb kasutada optimeerimise modelleerimiskeele (OML) süntaksit.</span><span class="sxs-lookup"><span data-stu-id="6319c-151">You must use Optimization Modeling Language (OML) syntax when you write constraints.</span></span> <span data-ttu-id="6319c-152">Süsteem kasutab piirangute lahendamiseks Microsoft Solver Foundationi piirangulahendajat.</span><span class="sxs-lookup"><span data-stu-id="6319c-152">The system uses Microsoft Solver Foundation constraint solver to solve the constraints.</span></span>

## <a name="should-i-use-table-constraints-or-expression-constraints"></a><span data-ttu-id="6319c-153">Kas peaksin kasutama tabeli või avaldise piiranguid?</span><span class="sxs-lookup"><span data-stu-id="6319c-153">Should I use table constraints or expression constraints?</span></span>
<span data-ttu-id="6319c-154">Saate kasutada avaldisepiiranguid või tabelipiiranguid olenevalt sellest, kuidas soovite piirangud koostada.</span><span class="sxs-lookup"><span data-stu-id="6319c-154">You can use either expression constraints or table constraints, depending on how you prefer to build the constraints.</span></span> <span data-ttu-id="6319c-155">Tabelipiirangu saate luua maatriksina, samas kui avaldisepiirang on eraldi lause.</span><span class="sxs-lookup"><span data-stu-id="6319c-155">You build a table constraint as a matrix, whereas an expression constraint is an individual statement.</span></span> <span data-ttu-id="6319c-156">Toote konfigureerimisel pole oluline, millist piirangut kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="6319c-156">When you configure a product, it doesn't matter what kind of constraint is used.</span></span> <span data-ttu-id="6319c-157">Järgmine näide selgitab kahe meetodi erinevust.</span><span class="sxs-lookup"><span data-stu-id="6319c-157">The following example shows how the two methods differ.</span></span>  

<span data-ttu-id="6319c-158">Toote konfigureerimisel järgmiste piiranguseadistuste abil on need kombinatsioonid lubatud.</span><span class="sxs-lookup"><span data-stu-id="6319c-158">When you configure a product by using the following constraint setups, these combinations are allowed:</span></span>

-   <span data-ttu-id="6319c-159">Toode, mille värv on must ja suurus 30 või 50.</span><span class="sxs-lookup"><span data-stu-id="6319c-159">A product in the color Black, and in size 30 or 50</span></span>
-   <span data-ttu-id="6319c-160">Toode, mille värv on punane ja suurus 20.</span><span class="sxs-lookup"><span data-stu-id="6319c-160">A product in the color Red and in size 20</span></span>

### <a name="table-constraint-setup"></a><span data-ttu-id="6319c-161">Tabeli piirangu seadistus</span><span class="sxs-lookup"><span data-stu-id="6319c-161">Table constraint setup</span></span>

| <span data-ttu-id="6319c-162">Värv</span><span class="sxs-lookup"><span data-stu-id="6319c-162">Color</span></span> | <span data-ttu-id="6319c-163">Suurus</span><span class="sxs-lookup"><span data-stu-id="6319c-163">Size</span></span> |
|-------|------|
| <span data-ttu-id="6319c-164">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-164">Black</span></span> | <span data-ttu-id="6319c-165">30</span><span class="sxs-lookup"><span data-stu-id="6319c-165">30</span></span>   |
| <span data-ttu-id="6319c-166">Must</span><span class="sxs-lookup"><span data-stu-id="6319c-166">Black</span></span> | <span data-ttu-id="6319c-167">50</span><span class="sxs-lookup"><span data-stu-id="6319c-167">50</span></span>   |
| <span data-ttu-id="6319c-168">Punane</span><span class="sxs-lookup"><span data-stu-id="6319c-168">Red</span></span>   | <span data-ttu-id="6319c-169">20</span><span class="sxs-lookup"><span data-stu-id="6319c-169">20</span></span>   |

### <a name="expression-constraint-setup"></a><span data-ttu-id="6319c-170">Avaldisepiirangu seadistus</span><span class="sxs-lookup"><span data-stu-id="6319c-170">Expression constraint setup</span></span>

<span data-ttu-id="6319c-171">(Värv == "Must" & (suurus == "30" | suurus == "50")) | (värv == "Punane" & suurus = "20")</span><span class="sxs-lookup"><span data-stu-id="6319c-171">(Color == "Black" & (size == "30" | size == "50")) | (color == "Red" & size = "20")</span></span>

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a><span data-ttu-id="6319c-172">Kas avaldise piirangute kirjutamisel tuleks kasutada tehtemärke või infix-märke?</span><span class="sxs-lookup"><span data-stu-id="6319c-172">Should I use operators or infix notation when I write expression constraints?</span></span>
<span data-ttu-id="6319c-173">Saate kirjutada avaldisepiirangu kas saadaolevaid tehtemärke või infix-märke kasutades.</span><span class="sxs-lookup"><span data-stu-id="6319c-173">You can write an expression constraint by using either the available prefix operators or infix notation.</span></span> <span data-ttu-id="6319c-174">Tehtemärkide **Min**, **Max** ja **Abs** puhul ei saa infix-märke kasutada.</span><span class="sxs-lookup"><span data-stu-id="6319c-174">For the **Min**, **Max**, and **Abs** operators, you can't use infix notation.</span></span> <span data-ttu-id="6319c-175">Need tehtemärgid sisalduvad standardina enamikus programmeerimiskeeltes.</span><span class="sxs-lookup"><span data-stu-id="6319c-175">These operators are included as standard operators in most programming languages.</span></span>

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a><span data-ttu-id="6319c-176">Milliseid tehtemärke ja infix-märke saan avaldisepiirangute kirjutamisel kasutada?</span><span class="sxs-lookup"><span data-stu-id="6319c-176">What operators and infix notation can I use when I write expression constraints?</span></span>
<span data-ttu-id="6319c-177">Järgmistes tabelites on tehtemärkide ja infix-märkide loend, mida saate toote konfiguratsioonimudeli komponendile avaldisepiirangu kirjutamisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="6319c-177">The following tables list the operators and infix notation that you can use when you write an expression constraint for a component in a product configuration model.</span></span> <span data-ttu-id="6319c-178">Esimeses tabelis toodud näited selgitavad, kuidas infix-märkide või tehtemärkide abil avaldist kirjutada.</span><span class="sxs-lookup"><span data-stu-id="6319c-178">The examples in the first table show how to write an expression by using either infix notation or operators.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6319c-179">Tehtemärk</span><span class="sxs-lookup"><span data-stu-id="6319c-179">Operator</span></span></th>
<th><span data-ttu-id="6319c-180">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6319c-180">Description</span></span></th>
<th><span data-ttu-id="6319c-181">Süntaks</span><span class="sxs-lookup"><span data-stu-id="6319c-181">Syntax</span></span></th>
<th><span data-ttu-id="6319c-182">Näited</span><span class="sxs-lookup"><span data-stu-id="6319c-182">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6319c-183">Tähendab</span><span class="sxs-lookup"><span data-stu-id="6319c-183">Implies</span></span></td>
<td><span data-ttu-id="6319c-184">See on tõene, kui esimene tingimus on väär, teine tingimus on tõene või mõlemad.</span><span class="sxs-lookup"><span data-stu-id="6319c-184">This is true if the first condition is false, the second condition is true, or both.</span></span></td>
<td><span data-ttu-id="6319c-185">Tähendab[a, b], infix: a -: b</span><span class="sxs-lookup"><span data-stu-id="6319c-185">Implies[a, b], infix: a -: b</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-186"><strong>Tehtemärk:</strong> Tähendab[x != 0, y &gt;= 0]</span><span class="sxs-lookup"><span data-stu-id="6319c-186"><strong>Operator:</strong> Implies[x != 0, y &gt;= 0]</span></span></li>
<li><span data-ttu-id="6319c-187"><strong>Infix-märk:</strong> x != 0 -: y &gt;= 0</span><span class="sxs-lookup"><span data-stu-id="6319c-187"><strong>Infix notation:</strong> x != 0 -: y &gt;= 0</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6319c-188">Ja</span><span class="sxs-lookup"><span data-stu-id="6319c-188">And</span></span></td>
<td><span data-ttu-id="6319c-189">See on tõene ainult juhul, kui kõik tingimused on tõesed.</span><span class="sxs-lookup"><span data-stu-id="6319c-189">This is true only if all conditions are true.</span></span> <span data-ttu-id="6319c-190">Kui tingimuste arv on 0 (null), on vastus <strong>Tõene</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-190">If the number of conditions is 0 (zero), it produces <strong>True</strong>.</span></span></td>
<td><span data-ttu-id="6319c-191">Ja[argumendid], infix: a &amp; b &amp; ... &amp; z</span><span class="sxs-lookup"><span data-stu-id="6319c-191">And[args], infix: a &amp; b &amp; ... &amp; z</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-192"><strong>Tehtemärk:</strong> And[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="6319c-192"><strong>Operator:</strong> And[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="6319c-193"><strong>Infix-märk:</strong> x == 2 &amp; y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="6319c-193"><strong>Infix notation:</strong> x == 2 &amp; y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6319c-194">Või</span><span class="sxs-lookup"><span data-stu-id="6319c-194">Or</span></span></td>
<td><span data-ttu-id="6319c-195">See on tõene, kui mis tahes tingimus on tõene.</span><span class="sxs-lookup"><span data-stu-id="6319c-195">This is true if any condition is true.</span></span> <span data-ttu-id="6319c-196">Kui tingimuste arv on 0 (null), on vastus <strong>Väär</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-196">If the number of conditions is 0 (zero), it produces <strong>False</strong>.</span></span></td>
<td><span data-ttu-id="6319c-197">Või[argumendid], infix: a | b | ... | z</span><span class="sxs-lookup"><span data-stu-id="6319c-197">Or[args], infix: a | b | ... | z</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-198"><strong>Tehtemärk:</strong> Või[x == 2, y &lt;= 2]</span><span class="sxs-lookup"><span data-stu-id="6319c-198"><strong>Operator:</strong> Or[x == 2, y &lt;= 2]</span></span></li>
<li><span data-ttu-id="6319c-199"><strong>Infix-märk:</strong> x == 2 | y &lt;= 2</span><span class="sxs-lookup"><span data-stu-id="6319c-199"><strong>Infix notation:</strong> x == 2 | y &lt;= 2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6319c-200">Pluss</span><span class="sxs-lookup"><span data-stu-id="6319c-200">Plus</span></span></td>
<td><span data-ttu-id="6319c-201">See summeerib tingimused.</span><span class="sxs-lookup"><span data-stu-id="6319c-201">This sums its conditions.</span></span> <span data-ttu-id="6319c-202">Kui tingimuste arv on 0 (null), on vastus <strong>0</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-202">If the number of conditions is 0 (zero), it produces <strong>0</strong>.</span></span></td>
<td><span data-ttu-id="6319c-203">Pluss[argumendid], infix: a + b + ... + z</span><span class="sxs-lookup"><span data-stu-id="6319c-203">Plus[args], infix: a + b + ... + z</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-204"><strong>Tehtemärk:</strong> Plus[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6319c-204"><strong>Operator:</strong> Plus[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="6319c-205"><strong>Infix-märk:</strong> x + y + 2 == z</span><span class="sxs-lookup"><span data-stu-id="6319c-205"><strong>Infix notation:</strong> x + y + 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6319c-206">Miinus</span><span class="sxs-lookup"><span data-stu-id="6319c-206">Minus</span></span></td>
<td><span data-ttu-id="6319c-207">See muudab argumendi negatiivseks.</span><span class="sxs-lookup"><span data-stu-id="6319c-207">This negates its argument.</span></span> <span data-ttu-id="6319c-208">Sel peab olema täpselt üks tingimus.</span><span class="sxs-lookup"><span data-stu-id="6319c-208">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="6319c-209">Miinus[avaldis], infix: –avaldis</span><span class="sxs-lookup"><span data-stu-id="6319c-209">Minus[expr], infix: -expr</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-210"><strong>Tehtemärk:</strong> Minus[x] == y</span><span class="sxs-lookup"><span data-stu-id="6319c-210"><strong>Operator:</strong> Minus[x] == y</span></span></li>
<li><span data-ttu-id="6319c-211"><strong>Infix-märk:</strong> -x == y</span><span class="sxs-lookup"><span data-stu-id="6319c-211"><strong>Infix notation:</strong> -x == y</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6319c-212">Abs</span><span class="sxs-lookup"><span data-stu-id="6319c-212">Abs</span></span></td>
<td><span data-ttu-id="6319c-213">See arvestab tingimuse absoluutväärtuse.</span><span class="sxs-lookup"><span data-stu-id="6319c-213">This takes the absolute value of its condition.</span></span> <span data-ttu-id="6319c-214">Sel peab olema täpselt üks tingimus.</span><span class="sxs-lookup"><span data-stu-id="6319c-214">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="6319c-215">Abs[avaldis]</span><span class="sxs-lookup"><span data-stu-id="6319c-215">Abs[expr]</span></span></td>
<td><span data-ttu-id="6319c-216"><strong>Tehtemärk:</strong> Abs[x]</span><span class="sxs-lookup"><span data-stu-id="6319c-216"><strong>Operator:</strong> Abs[x]</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6319c-217">Ajad</span><span class="sxs-lookup"><span data-stu-id="6319c-217">Times</span></span></td>
<td><span data-ttu-id="6319c-218">See arvestab tingimuste korrutise.</span><span class="sxs-lookup"><span data-stu-id="6319c-218">This takes the product of its conditions.</span></span> <span data-ttu-id="6319c-219">Kui tingimuste arv on 0 (null), on vastus <strong>1</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-219">If the number of conditions is 0 (zero), it produces <strong>1</strong>.</span></span></td>
<td><span data-ttu-id="6319c-220">Kordaja[argumendid], infix: a * b * ... * z</span><span class="sxs-lookup"><span data-stu-id="6319c-220">Times[args], infix: a * b * ... * z</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-221"><strong>Tehtemärk:</strong> Times[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6319c-221"><strong>Operator:</strong> Times[x, y, 2] == z</span></span></li>
<li><span data-ttu-id="6319c-222"><strong>Infix-märk:</strong> x * y * 2 == z</span><span class="sxs-lookup"><span data-stu-id="6319c-222"><strong>Infix notation:</strong> x * y * 2 == z</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6319c-223">Võimsus</span><span class="sxs-lookup"><span data-stu-id="6319c-223">Power</span></span></td>
<td><span data-ttu-id="6319c-224">See võtab astme.</span><span class="sxs-lookup"><span data-stu-id="6319c-224">This takes an exponential.</span></span> <span data-ttu-id="6319c-225">See rakendab paremalt vasakule astendamise.</span><span class="sxs-lookup"><span data-stu-id="6319c-225">It applies exponentiation from right to left.</span></span> <span data-ttu-id="6319c-226">(See tähendab parempoolset seost) Seega on avaldis <strong>Aste[a, b, c]</strong> võrdne avaldisega <strong>Aste[a, Aste[b, c]]</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-226">(In other words, it's right-associative.) Therefore, <strong>Power[a, b, c]</strong> is equivalent to <strong>Power[a, Power[b, c]]</strong>.</span></span> <span data-ttu-id="6319c-227"><strong>Astet</strong> saab kasutada ainult siis, kui aste on positiivne konstant.</span><span class="sxs-lookup"><span data-stu-id="6319c-227"><strong>Power</strong> can be used only if the exponent is a positive constant.</span></span></td>
<td><span data-ttu-id="6319c-228">Aste[argumendid], infix: a ^ b ^ ... ^ z</span><span class="sxs-lookup"><span data-stu-id="6319c-228">Power[args], infix: a ^ b ^ ... ^ z</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-229"><strong>Tehtemärk:</strong> Power[x, 2] == y</span><span class="sxs-lookup"><span data-stu-id="6319c-229"><strong>Operator:</strong> Power[x, 2] == y</span></span></li>
<li><span data-ttu-id="6319c-230"><strong>Infix-märk:</strong> x ^ 2 == y</span><span class="sxs-lookup"><span data-stu-id="6319c-230"><strong>Infix notation:</strong> x ^ 2 == y</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6319c-231">Suurim</span><span class="sxs-lookup"><span data-stu-id="6319c-231">Max</span></span></td>
<td><span data-ttu-id="6319c-232">See annab vastuseks suurima tingimuse.</span><span class="sxs-lookup"><span data-stu-id="6319c-232">This produces the largest condition.</span></span> <span data-ttu-id="6319c-233">Kui tingimuste arv on 0 (null), on vastus <strong>Lõpmatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-233">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="6319c-234">Max[argumendid]</span><span class="sxs-lookup"><span data-stu-id="6319c-234">Max[args]</span></span></td>
<td><span data-ttu-id="6319c-235"><strong>Tehtemärk:</strong> Max[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6319c-235"><strong>Operator:</strong> Max[x, y, 2] == z</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6319c-236">Väikseim</span><span class="sxs-lookup"><span data-stu-id="6319c-236">Min</span></span></td>
<td><span data-ttu-id="6319c-237">See annab vastuseks vähima tingimuse.</span><span class="sxs-lookup"><span data-stu-id="6319c-237">This produces the smallest condition.</span></span> <span data-ttu-id="6319c-238">Kui tingimuste arv on 0 (null), on vastus <strong>Lõpmatus</strong>.</span><span class="sxs-lookup"><span data-stu-id="6319c-238">If the number of conditions is 0 (zero), it produces <strong>Infinity</strong>.</span></span></td>
<td><span data-ttu-id="6319c-239">Min[argumendid]</span><span class="sxs-lookup"><span data-stu-id="6319c-239">Min[args]</span></span></td>
<td><span data-ttu-id="6319c-240"><strong>Tehtemärk:</strong> Min[x, y, 2] == z</span><span class="sxs-lookup"><span data-stu-id="6319c-240"><strong>Operator:</strong> Min[x, y, 2] == z</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6319c-241">Ei ole</span><span class="sxs-lookup"><span data-stu-id="6319c-241">Not</span></span></td>
<td><span data-ttu-id="6319c-242">See annab vastuseks tingimuse loogilise pöördväärtuse.</span><span class="sxs-lookup"><span data-stu-id="6319c-242">This produces the logical inverse of its condition.</span></span> <span data-ttu-id="6319c-243">Sel peab olema täpselt üks tingimus.</span><span class="sxs-lookup"><span data-stu-id="6319c-243">It must have exactly one condition.</span></span></td>
<td><span data-ttu-id="6319c-244">Pole[avaldis], infix: !avaldis</span><span class="sxs-lookup"><span data-stu-id="6319c-244">Not[expr], infix: !expr</span></span></td>
<td><ul>
<li><span data-ttu-id="6319c-245"><strong>Tehtemärk:</strong> Pole[x] &amp; Pole[y == 3]</span><span class="sxs-lookup"><span data-stu-id="6319c-245"><strong>Operator:</strong> Not[x] &amp; Not[y == 3]</span></span></li>
<li><span data-ttu-id="6319c-246"><strong>Infix-märk:</strong> !x!(y == 3)</span><span class="sxs-lookup"><span data-stu-id="6319c-246"><strong>Infix notation:</strong> !x!(y == 3)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6319c-247">Järgmise tabeli näited selgitavad, kuidas kirjutada infix-märke.</span><span class="sxs-lookup"><span data-stu-id="6319c-247">The examples in the next table show how to write infix notation.</span></span>

| <span data-ttu-id="6319c-248">Infix-märk</span><span class="sxs-lookup"><span data-stu-id="6319c-248">Infix notation</span></span>    | <span data-ttu-id="6319c-249">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6319c-249">Description</span></span>                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="6319c-250">x + y + z</span><span class="sxs-lookup"><span data-stu-id="6319c-250">x + y + z</span></span>         | <span data-ttu-id="6319c-251">Lisa</span><span class="sxs-lookup"><span data-stu-id="6319c-251">Addition</span></span>                                                                                      |
| <span data-ttu-id="6319c-252">x \* y \* z</span><span class="sxs-lookup"><span data-stu-id="6319c-252">x \* y \* z</span></span>       | <span data-ttu-id="6319c-253">Korrutamine</span><span class="sxs-lookup"><span data-stu-id="6319c-253">Multiplication</span></span>                                                                                |
| <span data-ttu-id="6319c-254">x - y</span><span class="sxs-lookup"><span data-stu-id="6319c-254">x - y</span></span>             | <span data-ttu-id="6319c-255">Binaarne lahutamine teisendatakse samamoodi nagu negatiivse teise liikmega binaarne liitmine.</span><span class="sxs-lookup"><span data-stu-id="6319c-255">Binary subtraction is translated the same as binary addition where there is a negated second.</span></span> |
| <span data-ttu-id="6319c-256">x ^ y ^ z</span><span class="sxs-lookup"><span data-stu-id="6319c-256">x ^ y ^ z</span></span>         | <span data-ttu-id="6319c-257">Parempoolse seosega astendamine</span><span class="sxs-lookup"><span data-stu-id="6319c-257">Exponentiation that has right associativity</span></span>                                                   |
| <span data-ttu-id="6319c-258">!x</span><span class="sxs-lookup"><span data-stu-id="6319c-258">!x</span></span>                | <span data-ttu-id="6319c-259">Kahendmuutuja pole</span><span class="sxs-lookup"><span data-stu-id="6319c-259">Boolean not</span></span>                                                                                   |
| <span data-ttu-id="6319c-260">x -: y</span><span class="sxs-lookup"><span data-stu-id="6319c-260">x -: y</span></span>            | <span data-ttu-id="6319c-261">Kahendmuutuja mõju</span><span class="sxs-lookup"><span data-stu-id="6319c-261">Boolean implication</span></span>                                                                           |
| <span data-ttu-id="6319c-262">x</span><span class="sxs-lookup"><span data-stu-id="6319c-262">x</span></span> | <span data-ttu-id="6319c-263">y</span><span class="sxs-lookup"><span data-stu-id="6319c-263">y</span></span> | <span data-ttu-id="6319c-264">z</span><span class="sxs-lookup"><span data-stu-id="6319c-264">z</span></span>         | <span data-ttu-id="6319c-265">Kahendmuutuja või</span><span class="sxs-lookup"><span data-stu-id="6319c-265">Boolean or</span></span>                                                                                    |
| <span data-ttu-id="6319c-266">x & y & z</span><span class="sxs-lookup"><span data-stu-id="6319c-266">x & y & z</span></span>         | <span data-ttu-id="6319c-267">Kahendmuutuja ja</span><span class="sxs-lookup"><span data-stu-id="6319c-267">Boolean and</span></span>                                                                                   |
| <span data-ttu-id="6319c-268">x == y == z</span><span class="sxs-lookup"><span data-stu-id="6319c-268">x == y == z</span></span>       | <span data-ttu-id="6319c-269">Võrdne</span><span class="sxs-lookup"><span data-stu-id="6319c-269">Equality</span></span>                                                                                      |
| <span data-ttu-id="6319c-270">x != y != z</span><span class="sxs-lookup"><span data-stu-id="6319c-270">x != y != z</span></span>       | <span data-ttu-id="6319c-271">Distinktne</span><span class="sxs-lookup"><span data-stu-id="6319c-271">Distinct</span></span>                                                                                      |
| <span data-ttu-id="6319c-272">x &lt; y &lt; z</span><span class="sxs-lookup"><span data-stu-id="6319c-272">x &lt; y &lt; z</span></span>   | <span data-ttu-id="6319c-273">Väiksem kui</span><span class="sxs-lookup"><span data-stu-id="6319c-273">Less than</span></span>                                                                                     |
| <span data-ttu-id="6319c-274">x &gt; y &gt; z</span><span class="sxs-lookup"><span data-stu-id="6319c-274">x &gt; y &gt; z</span></span>   | <span data-ttu-id="6319c-275">Suurem kui</span><span class="sxs-lookup"><span data-stu-id="6319c-275">Greater than</span></span>                                                                                  |
| <span data-ttu-id="6319c-276">x &lt;= y &lt;= z</span><span class="sxs-lookup"><span data-stu-id="6319c-276">x &lt;= y &lt;= z</span></span> | <span data-ttu-id="6319c-277">Väiksem kui või võrdne</span><span class="sxs-lookup"><span data-stu-id="6319c-277">Less than or equal to</span></span>                                                                         |
| <span data-ttu-id="6319c-278">x &gt;= y &gt;= z</span><span class="sxs-lookup"><span data-stu-id="6319c-278">x &gt;= y &gt;= z</span></span> | <span data-ttu-id="6319c-279">Suurem kui või võrdne</span><span class="sxs-lookup"><span data-stu-id="6319c-279">Greater than or equal to</span></span>                                                                      |
| <span data-ttu-id="6319c-280">(x)</span><span class="sxs-lookup"><span data-stu-id="6319c-280">(x)</span></span>               | <span data-ttu-id="6319c-281">Sulud alistavad vaikejärjestuse.</span><span class="sxs-lookup"><span data-stu-id="6319c-281">Parentheses override default precedence.</span></span>                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a><span data-ttu-id="6319c-282">Miks minu avaldisepiiranguid õigesti ei kinnitata?</span><span class="sxs-lookup"><span data-stu-id="6319c-282">Why aren't my expression constraints validated correctly?</span></span>
<span data-ttu-id="6319c-283">Toote konfiguratsioonimudelis ei saa kasutada atribuutide, komponentide või alamkomponentide nimena lahendaja nimena reserveeritud märksõnu.</span><span class="sxs-lookup"><span data-stu-id="6319c-283">You can't use reserved keywords as solver names for attributes, components, or subcomponents in a product configuration model.</span></span> <span data-ttu-id="6319c-284">Siin on loend, mis sisaldab reserveeritud märksõnu, mida ei saa kasutada.</span><span class="sxs-lookup"><span data-stu-id="6319c-284">Here is a list of the reserved keywords that you can't use:</span></span>

-   <span data-ttu-id="6319c-285">Ülempiir</span><span class="sxs-lookup"><span data-stu-id="6319c-285">Ceiling</span></span>
-   <span data-ttu-id="6319c-286">Element</span><span class="sxs-lookup"><span data-stu-id="6319c-286">Element</span></span>
-   <span data-ttu-id="6319c-287">Võrdne</span><span class="sxs-lookup"><span data-stu-id="6319c-287">Equal</span></span>
-   <span data-ttu-id="6319c-288">Põrand</span><span class="sxs-lookup"><span data-stu-id="6319c-288">Floor</span></span>
-   <span data-ttu-id="6319c-289">Kui</span><span class="sxs-lookup"><span data-stu-id="6319c-289">If</span></span>
-   <span data-ttu-id="6319c-290">Väiksem kui</span><span class="sxs-lookup"><span data-stu-id="6319c-290">Less</span></span>
-   <span data-ttu-id="6319c-291">Suurem</span><span class="sxs-lookup"><span data-stu-id="6319c-291">Greater</span></span>
-   <span data-ttu-id="6319c-292">Tähendab</span><span class="sxs-lookup"><span data-stu-id="6319c-292">Implies</span></span>
-   <span data-ttu-id="6319c-293">Logi</span><span class="sxs-lookup"><span data-stu-id="6319c-293">Log</span></span>
-   <span data-ttu-id="6319c-294">Suurim</span><span class="sxs-lookup"><span data-stu-id="6319c-294">Max</span></span>
-   <span data-ttu-id="6319c-295">Väikseim</span><span class="sxs-lookup"><span data-stu-id="6319c-295">Min</span></span>
-   <span data-ttu-id="6319c-296">Miinus</span><span class="sxs-lookup"><span data-stu-id="6319c-296">Minus</span></span>
-   <span data-ttu-id="6319c-297">Pluss</span><span class="sxs-lookup"><span data-stu-id="6319c-297">Plus</span></span>
-   <span data-ttu-id="6319c-298">Võimsus</span><span class="sxs-lookup"><span data-stu-id="6319c-298">Power</span></span>
-   <span data-ttu-id="6319c-299">Ajad</span><span class="sxs-lookup"><span data-stu-id="6319c-299">Times</span></span>
-   <span data-ttu-id="6319c-300">Pesa</span><span class="sxs-lookup"><span data-stu-id="6319c-300">Slot</span></span>
-   <span data-ttu-id="6319c-301">Mudel</span><span class="sxs-lookup"><span data-stu-id="6319c-301">Model</span></span>
-   <span data-ttu-id="6319c-302">Otsus</span><span class="sxs-lookup"><span data-stu-id="6319c-302">Decision</span></span>
-   <span data-ttu-id="6319c-303">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="6319c-303">Goal</span></span>


<a name="see-also"></a><span data-ttu-id="6319c-304">Vt ka</span><span class="sxs-lookup"><span data-stu-id="6319c-304">See also</span></span>
--------

<span data-ttu-id="6319c-305">[Avaldise piirangu loomine (tegevuse juhis)(tasks/add-expression-constraint-product-configuration-model.md)</span><span class="sxs-lookup"><span data-stu-id="6319c-305">[Create an expression constraint (Task guide)(tasks/add-expression-constraint-product-configuration-model.md)</span></span>

[<span data-ttu-id="6319c-306">Arvutuse lisamine toote konfiguratsioonimudelile (tegevuse juhis)</span><span class="sxs-lookup"><span data-stu-id="6319c-306">Add a calculation to a product configuration model (Task guide)</span></span>](tasks/add-calculation-product-configuration-model.md)




