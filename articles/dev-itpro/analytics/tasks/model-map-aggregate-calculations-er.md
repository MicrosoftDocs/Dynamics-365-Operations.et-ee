---
title: Mudelivastenduse konfiguratsioonide kasutamine koondarvutusteks andmebaasi tasemel
description: See protseduur annab teavet selle kohta, kuidas kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a462a3997644a494b5cea89c9530ddba67c32450
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "313631"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="63222-103">Mudelivastenduse konfiguratsioonide kasutamine koondarvutusteks andmebaasi tasemel</span><span class="sxs-lookup"><span data-stu-id="63222-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63222-104">See protseduur annab teavet selle kohta, kuidas kujundada uue elektroonilise aruandluse (ER) mudeli vastendamise konfiguratsiooni ja kasutada sisseehitatud ER-i funktsioone tõhusate koondarvutuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="63222-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="63222-105">Selles protseduuris loote konfiguratsiooni näidisettevõttele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="63222-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="63222-106">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="63222-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="63222-107">Need etapid saab lõpule viia ükskõik millise andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="63222-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="63222-108">Toimingute tegemiseks tuleb esmalt lõpule viia protseduuri „ER parandab kogusumma arvutuste tõhusust, tehes neid andmebaasi tasemel (osa 1: konfiguratsioonide ettevalmistamine)” etapid.</span><span class="sxs-lookup"><span data-stu-id="63222-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="63222-109">Avage Organisatsiooni haldamine > Elektrooniline aruandlus > Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="63222-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="63222-110">Laiendage puul valikut Intrastati mudel.</span><span class="sxs-lookup"><span data-stu-id="63222-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="63222-111">Tehke puul valik „Intrastati mudel\Intrastati näidisvastendamine”.</span><span class="sxs-lookup"><span data-stu-id="63222-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="63222-112">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="63222-112">Click Designer.</span></span>
5. <span data-ttu-id="63222-113">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="63222-113">Click Designer.</span></span>
6. <span data-ttu-id="63222-114">Valige puul väärtus Dynamics 365 for Operations \ Tabeli kirjed.</span><span class="sxs-lookup"><span data-stu-id="63222-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="63222-115">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="63222-115">Click Add root.</span></span>
    * <span data-ttu-id="63222-116">Lisage uus andmeallikas, mis tähistab kirjeid, mille soovite grupeerida.</span><span class="sxs-lookup"><span data-stu-id="63222-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="63222-117">Sisestage väljale Nimi suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="63222-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="63222-118">Kanded</span><span class="sxs-lookup"><span data-stu-id="63222-118">Transactions</span></span>  
9. <span data-ttu-id="63222-119">Väljale Tabel tippige „Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="63222-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="63222-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="63222-120">Intrastat</span></span>  
10. <span data-ttu-id="63222-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="63222-121">Click OK.</span></span>
11. <span data-ttu-id="63222-122">Valige puul väärtus Funktsioonid\grupeerimisalus.</span><span class="sxs-lookup"><span data-stu-id="63222-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="63222-123">Seda tüüpi andmeallikat kasutatakse käitusajal uue andmeallika lisamiseks, et grupeerida kirjeid ja arvutada nõutavaid kogumeid.</span><span class="sxs-lookup"><span data-stu-id="63222-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="63222-124">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="63222-124">Click Add root.</span></span>
13. <span data-ttu-id="63222-125">Väljale Nimi tippige „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="63222-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="63222-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="63222-127">Klõpsake suvandit Grupi redigeerimise alus.</span><span class="sxs-lookup"><span data-stu-id="63222-127">Click Edit group by.</span></span>
15. <span data-ttu-id="63222-128">Valige puul suvand Kanded.</span><span class="sxs-lookup"><span data-stu-id="63222-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="63222-129">Valige lisatud andmeallikas tüübiga „Kirjete loend”, mis esindab kirjeid, mille soovite grupeerida.</span><span class="sxs-lookup"><span data-stu-id="63222-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="63222-130">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="63222-130">Click Add field to.</span></span>
17. <span data-ttu-id="63222-131">Klõpsake suvandit Mida grupeerida.</span><span class="sxs-lookup"><span data-stu-id="63222-131">Click What to group.</span></span>
18. <span data-ttu-id="63222-132">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="63222-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="63222-133">Valige puul suvand „Kanded\Suund”.</span><span class="sxs-lookup"><span data-stu-id="63222-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="63222-134">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="63222-134">Click Add field to.</span></span>
21. <span data-ttu-id="63222-135">Klõpsake suvandit Grupeeritud väljad.</span><span class="sxs-lookup"><span data-stu-id="63222-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="63222-136">Märkige väli, et määrata grupeerimise tase.</span><span class="sxs-lookup"><span data-stu-id="63222-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="63222-137">Selle valiku põhjal tagastab andmeallikas käitusajal sama palju kannete gruppe kui on suunakoode, mida Intrastati tabelis täidetakse.</span><span class="sxs-lookup"><span data-stu-id="63222-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="63222-138">Valige puul „Kanded\Arve summa (AmountMST)”.</span><span class="sxs-lookup"><span data-stu-id="63222-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="63222-139">Märkige ruut, et määrata kogumi arvutuse allikas.</span><span class="sxs-lookup"><span data-stu-id="63222-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="63222-140">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="63222-140">Click Add field to.</span></span>
24. <span data-ttu-id="63222-141">Klõpsake suvandit Kogumi väljad.</span><span class="sxs-lookup"><span data-stu-id="63222-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="63222-142">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="63222-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="63222-143">Valige väljal Meetod väärtus „Summa”.</span><span class="sxs-lookup"><span data-stu-id="63222-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="63222-144">Valige kogumi tüüp.</span><span class="sxs-lookup"><span data-stu-id="63222-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="63222-145">Väljale Nimi tippige „SumOfAmountMST”.</span><span class="sxs-lookup"><span data-stu-id="63222-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="63222-146">Määrake kogumi nimi konfigureeritud andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="63222-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="63222-147">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="63222-147">Click Save.</span></span>
    * <span data-ttu-id="63222-148">Pange tähele, et väli „Käivitamine:” näitab, et grupeerimine toimub SQL-i andmebaasis käitusajal.</span><span class="sxs-lookup"><span data-stu-id="63222-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="63222-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="63222-149">Close the page.</span></span>
30. <span data-ttu-id="63222-150">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="63222-150">Click OK.</span></span>
31. <span data-ttu-id="63222-151">Laiendage puul väärtust „Kogusummad”.</span><span class="sxs-lookup"><span data-stu-id="63222-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="63222-152">Laiendage puul väärtust „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="63222-153">Laiendage puus väärtust „TransactionsGroups\koondatud”.</span><span class="sxs-lookup"><span data-stu-id="63222-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="63222-154">Valige puul „TransactionsGroups\aggregated\SumOfAmountMST”.</span><span class="sxs-lookup"><span data-stu-id="63222-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="63222-155">Valige puul „Kogusummad\Arve kogusumma (TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')”.</span><span class="sxs-lookup"><span data-stu-id="63222-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="63222-156">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="63222-156">Click Bind.</span></span>
    * <span data-ttu-id="63222-157">Sätte alusel arvutab andmeallikas iga kannete grupi jaoks välja „AmountMST” väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="63222-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="63222-158">Kogumi arvutus on saadaval üksusena TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="63222-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="63222-159">Laiendage puul väärtust „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="63222-160">Valige puul väärtus „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="63222-161">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="63222-161">Click Edit.</span></span>
40. <span data-ttu-id="63222-162">Klõpsake suvandit Grupi redigeerimise alus.</span><span class="sxs-lookup"><span data-stu-id="63222-162">Click Edit group by.</span></span>
41. <span data-ttu-id="63222-163">Laiendage puul suvandit Kanded.</span><span class="sxs-lookup"><span data-stu-id="63222-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="63222-164">Valige puul „Kanded\Arve summa (AmountMST)”.</span><span class="sxs-lookup"><span data-stu-id="63222-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="63222-165">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="63222-165">Click Add field to.</span></span>
44. <span data-ttu-id="63222-166">Klõpsake suvandit Kogumi väljad.</span><span class="sxs-lookup"><span data-stu-id="63222-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="63222-167">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="63222-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="63222-168">Valige väljal Meetod väärtus „Max”.</span><span class="sxs-lookup"><span data-stu-id="63222-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="63222-169">Väljale Nimi tippige „MaxOfAmountMST”.</span><span class="sxs-lookup"><span data-stu-id="63222-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="63222-170">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="63222-170">Click Save.</span></span>
    * <span data-ttu-id="63222-171">Andmeallikate GROUPBY käivitamist saab praegu üle kanda SQL-i andmebaasi tasemele teatud piirangutega.</span><span class="sxs-lookup"><span data-stu-id="63222-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="63222-172">Ülekandmine on võimalik tüübiga „Kirjete loend” andmeallikate või avaldisena esitatud andmeallikate puhul, kasutades funktsiooni FILTER.</span><span class="sxs-lookup"><span data-stu-id="63222-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="63222-173">Seda saab teha ainult juhul, kui grupeeritavate kirjete ühe välja jaoks on konfigureeritud ainult üks kogum.</span><span class="sxs-lookup"><span data-stu-id="63222-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="63222-174">Pange tähele, et isegi juhul, kui väljal AmountMST konfigureeriti mitu kogumit, näitab väli „Käivitamine:” siiski, et grupeerimine toimub SQL-i andmebaasis käitusajal.</span><span class="sxs-lookup"><span data-stu-id="63222-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="63222-175">Selle põhjuseks on see, et andmemudeli üksusega on seotud ainult üks kogumik, mida kasutatakse käitusajal sellest andmeallikast andmete toomiseks.</span><span class="sxs-lookup"><span data-stu-id="63222-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="63222-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="63222-176">Close the page.</span></span>
50. <span data-ttu-id="63222-177">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="63222-177">Click OK.</span></span>
51. <span data-ttu-id="63222-178">Laiendage puul väärtust „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="63222-179">Laiendage puus väärtust „TransactionsGroups\koondatud”.</span><span class="sxs-lookup"><span data-stu-id="63222-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="63222-180">Valige puul „TransactionsGroups\aggregated\MaxOfAmountMST”.</span><span class="sxs-lookup"><span data-stu-id="63222-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="63222-181">Valige puul „Kogusummad\Statistiline väärtus kokku (TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')”.</span><span class="sxs-lookup"><span data-stu-id="63222-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="63222-182">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="63222-182">Click Bind.</span></span>
56. <span data-ttu-id="63222-183">Laiendage puul väärtust „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="63222-184">Valige puul väärtus „TransactionsGroups”.</span><span class="sxs-lookup"><span data-stu-id="63222-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="63222-185">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="63222-185">Click Edit.</span></span>
59. <span data-ttu-id="63222-186">Klõpsake suvandit Grupi redigeerimise alus.</span><span class="sxs-lookup"><span data-stu-id="63222-186">Click Edit group by.</span></span>
    * <span data-ttu-id="63222-187">Pange tähele, et väli „Käivitamine:” näitab, et grupeerimine toimub käitusajal mälus, kuna mõlemad sama välja kogumid on seotud andmemudeli üksustega.</span><span class="sxs-lookup"><span data-stu-id="63222-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="63222-188">Märkige või tühjendage loendis kõik read.</span><span class="sxs-lookup"><span data-stu-id="63222-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="63222-189">Klõpsake käsku Kustuta.</span><span class="sxs-lookup"><span data-stu-id="63222-189">Click Delete.</span></span>
62. <span data-ttu-id="63222-190">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="63222-190">Click Yes.</span></span>
63. <span data-ttu-id="63222-191">Klõpsake käsku Kustuta.</span><span class="sxs-lookup"><span data-stu-id="63222-191">Click Delete.</span></span>
64. <span data-ttu-id="63222-192">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="63222-192">Click Yes.</span></span>
65. <span data-ttu-id="63222-193">Klõpsake suvandit Lisa väli üksusele.</span><span class="sxs-lookup"><span data-stu-id="63222-193">Click Add field to.</span></span>
66. <span data-ttu-id="63222-194">Klõpsake suvandit Mida grupeerida.</span><span class="sxs-lookup"><span data-stu-id="63222-194">Click What to group.</span></span>
67. <span data-ttu-id="63222-195">Laiendage puul valikut „Kauba kirje (Intrastat)”.</span><span class="sxs-lookup"><span data-stu-id="63222-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="63222-196">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="63222-196">Click Save.</span></span>
    * <span data-ttu-id="63222-197">Pange tähele, et väli „Käivitamine:” näitab, et grupeerimine toimub käitusajal mälus, isegi kui ükski kogum ei ole määratud ja valitud andmeallikas tüübiga „Tabeli kirjed” viitab samale tabelile „Intrastat”.</span><span class="sxs-lookup"><span data-stu-id="63222-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="63222-198">Põhjuseks on see, et andmeallikas sisaldab mõningaid arvutatud välju, mida ei saa veel SQL-i andmebaasi tasemele üle kanda.</span><span class="sxs-lookup"><span data-stu-id="63222-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  

