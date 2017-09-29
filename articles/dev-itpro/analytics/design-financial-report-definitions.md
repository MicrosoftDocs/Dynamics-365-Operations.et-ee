---
title: Aruande definitsioonid finantsaruande koosturis
description: "See artikkel käsitleb aruande definitsioone. Aruande definitsioon on aruande komponent (koosteüksus), mis kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni. Aruande definitsioon annab valikud ja sätted ka aruande kohandamiseks."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 96090a3ae15294d98d6207c8eb4a1e58429ca9eb
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="a7d61-105">Aruande definitsioonid finantsaruande koosturis</span><span class="sxs-lookup"><span data-stu-id="a7d61-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a7d61-106">See artikkel käsitleb aruande definitsioone.</span><span class="sxs-lookup"><span data-stu-id="a7d61-106">This article provides information about report definitions.</span></span> <span data-ttu-id="a7d61-107">Aruande definitsioon on aruande komponent (koosteüksus), mis kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="a7d61-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a7d61-108">Aruande definitsioon annab valikud ja sätted ka aruande kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7d61-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="a7d61-109">Aruande definitsioon on aruande komponent (koosteüksus), mis kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="a7d61-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="a7d61-110">Aruande definitsioon sisaldab ka täiendavaid suvandeid ja sätteid, mida saab aruande kohandamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="a7d61-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="a7d61-111">Pärast rea ja veeru definitsioonide määratlemist peate need aruande definitsiooni kombineerima.</span><span class="sxs-lookup"><span data-stu-id="a7d61-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="a7d61-112">Saate määratleda ka definitsioonide muid aspekte, nagu üksikasjade tase ja aruande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="a7d61-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="a7d61-113">Seejärel saate salvestada ja aruande luua.</span><span class="sxs-lookup"><span data-stu-id="a7d61-113">You can then save and generate a report.</span></span> <span data-ttu-id="a7d61-114">Finantsaruandlus pakub järgmisi üksikasjade tasemeid.</span><span class="sxs-lookup"><span data-stu-id="a7d61-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="a7d61-115">Rahandus</span><span class="sxs-lookup"><span data-stu-id="a7d61-115">Financial</span></span>
-   <span data-ttu-id="a7d61-116">Rahaline ja Konto</span><span class="sxs-lookup"><span data-stu-id="a7d61-116">Financial and Account</span></span>
-   <span data-ttu-id="a7d61-117">Rahaline, Konto ja Kanne</span><span class="sxs-lookup"><span data-stu-id="a7d61-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="a7d61-118">Olenevalt sellest, kuidas andmed on Microsoft Dynamics ERP süsteemi salvestatud, ei pruugi kande üksikasjad aruannetes saadaval olla.</span><span class="sxs-lookup"><span data-stu-id="a7d61-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="a7d61-119">Aruande määratluse loomine</span><span class="sxs-lookup"><span data-stu-id="a7d61-119">Create a report definition</span></span>
1.  <span data-ttu-id="a7d61-120">Klõpsake aruande kujundaja menüüs **Fail** nuppu **Uus** ja seejärel valige **Aruande definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="a7d61-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="a7d61-121">Määrake sobiv teave vahekaartidel **Aruanne**, **Väljund ja jaotus**, **Päised ja jalused** ja **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="a7d61-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="a7d61-122">Aruande definitsiooni sisu</span><span class="sxs-lookup"><span data-stu-id="a7d61-122">Contents of a report definition</span></span>
<span data-ttu-id="a7d61-123">Järgmises tabelis kirjeldatakse aruande definitsiooni vahekaarte ja seda, kuidas teavet kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="a7d61-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a7d61-124">Vahekaart</span><span class="sxs-lookup"><span data-stu-id="a7d61-124">Tab</span></span></th>
<th><span data-ttu-id="a7d61-125">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a7d61-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a7d61-126">Aruanne</span><span class="sxs-lookup"><span data-stu-id="a7d61-126">Report</span></span></td>
<td><span data-ttu-id="a7d61-127">Aruande loomine, aruande seadistamine või olemasoleva aruande muutmine.</span><span class="sxs-lookup"><span data-stu-id="a7d61-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7d61-128">Väljund ja jaotus</span><span class="sxs-lookup"><span data-stu-id="a7d61-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="a7d61-129">Väljundi tüübi ja aruande sihtkoha muutmine.</span><span class="sxs-lookup"><span data-stu-id="a7d61-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a7d61-130">Päised ja jalused</span><span class="sxs-lookup"><span data-stu-id="a7d61-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="a7d61-131">Aruande päiste ja jaluste määratlemine ja vormindamine.</span><span class="sxs-lookup"><span data-stu-id="a7d61-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="a7d61-132">Näiteks saate lisada päisesse või jalusesse teksti või pilte.</span><span class="sxs-lookup"><span data-stu-id="a7d61-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="a7d61-133">Finantsaruandlus toetab piltide puhul failivorminguid .bmp, .jpg ja .png.</span><span class="sxs-lookup"><span data-stu-id="a7d61-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="a7d61-134">Võite sisestada ka automaatteksti koode muu teabe, näiteks ettevõtte nime, aruande nime või lehekülje numbri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="a7d61-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a7d61-135">Sätted</span><span class="sxs-lookup"><span data-stu-id="a7d61-135">Settings</span></span></td>
<td><span data-ttu-id="a7d61-136">Aruande definitsiooni sätete, näiteks järgmiste sätete määratlemine.</span><span class="sxs-lookup"><span data-stu-id="a7d61-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="a7d61-137">Summade vormindamine ja ümardamine</span><span class="sxs-lookup"><span data-stu-id="a7d61-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="a7d61-138">Üksikasjade aruannete vormindamine</span><span class="sxs-lookup"><span data-stu-id="a7d61-138">Format detail reports</span></span></li>
<li><span data-ttu-id="a7d61-139">Aruandluspuude vormindamine</span><span class="sxs-lookup"><span data-stu-id="a7d61-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="a7d61-140">Erandite aruande loomine</span><span class="sxs-lookup"><span data-stu-id="a7d61-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="a7d61-141">Valuuta konverteerimise määratlemine</span><span class="sxs-lookup"><span data-stu-id="a7d61-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="a7d61-142">Vahesumma ja konto üksikasjade filtrimine</span><span class="sxs-lookup"><span data-stu-id="a7d61-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="a7d61-143">Vt ka</span><span class="sxs-lookup"><span data-stu-id="a7d61-143">See also</span></span>
--------

[<span data-ttu-id="a7d61-144">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="a7d61-144">Financial reporting</span></span>](financial-reporting-intro.md)




