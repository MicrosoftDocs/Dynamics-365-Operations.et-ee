---
title: Aruande definitsioonid finantsaruande koosturis
description: See artikkel käsitleb aruande definitsioone.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 52322453328814b06bacefb4829bb10bf9953186
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755440"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="59742-103">Aruande definitsioonid finantsaruande koosturis</span><span class="sxs-lookup"><span data-stu-id="59742-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="59742-104">See artikkel käsitleb aruande definitsioone.</span><span class="sxs-lookup"><span data-stu-id="59742-104">This article provides information about report definitions.</span></span> <span data-ttu-id="59742-105">Aruande definitsioon on aruande komponent (koosteüksus), mis kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="59742-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="59742-106">Aruande definitsioon annab valikud ja sätted ka aruande kohandamiseks.</span><span class="sxs-lookup"><span data-stu-id="59742-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="59742-107">Aruande definitsioon on aruande komponent (koosteüksus), mis kasutab aruande loomiseks readefinitsiooni, veeru definitsiooni ja valikulist aruandluspuu definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="59742-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="59742-108">Aruande määratlus pakub suvandeid ja sätteid, mida saate aruande kohandamiseks kasutada.</span><span class="sxs-lookup"><span data-stu-id="59742-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="59742-109">Pärast rea ja veeru definitsioonide määratlemist peate need aruande definitsiooni kombineerima.</span><span class="sxs-lookup"><span data-stu-id="59742-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="59742-110">Saate määratleda ka definitsioonide muid aspekte, nagu üksikasjade tase ja aruande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="59742-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="59742-111">Seejärel saate salvestada ja aruande luua.</span><span class="sxs-lookup"><span data-stu-id="59742-111">You can then save and generate a report.</span></span> <span data-ttu-id="59742-112">Finantsaruandlus pakub järgmisi üksikasjade tasemeid.</span><span class="sxs-lookup"><span data-stu-id="59742-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="59742-113">Rahandus</span><span class="sxs-lookup"><span data-stu-id="59742-113">Financial</span></span>
- <span data-ttu-id="59742-114">Rahaline ja Konto</span><span class="sxs-lookup"><span data-stu-id="59742-114">Financial and Account</span></span>
- <span data-ttu-id="59742-115">Rahaline, Konto ja Kanne</span><span class="sxs-lookup"><span data-stu-id="59742-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="59742-116">Samas ei pruugi kande üksikasjad olenevalt andmete Microsoft Dynamics ERP süsteemis talletamise viisist aruannetes kättesaadavad olla.</span><span class="sxs-lookup"><span data-stu-id="59742-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="59742-117">Aruande määratluse loomine</span><span class="sxs-lookup"><span data-stu-id="59742-117">Create a report definition</span></span>
1. <span data-ttu-id="59742-118">Klõpsake aruande kujundaja menüüs **Fail** nuppu **Uus** ja seejärel valige **Aruande definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="59742-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="59742-119">Määrake sobiv teave vahekaartidel **Aruanne**, **Väljund ja jaotus**, **Päised ja jalused** ja **Sätted**.</span><span class="sxs-lookup"><span data-stu-id="59742-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="59742-120">Aruande definitsiooni sisu</span><span class="sxs-lookup"><span data-stu-id="59742-120">Contents of a report definition</span></span>
<span data-ttu-id="59742-121">Järgmises tabelis kirjeldatakse aruande definitsiooni vahekaarte ja seda, kuidas teavet kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="59742-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="59742-122">Väli</span><span class="sxs-lookup"><span data-stu-id="59742-122">Tab</span></span></th>
<th><span data-ttu-id="59742-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="59742-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="59742-124">Aruanne</span><span class="sxs-lookup"><span data-stu-id="59742-124">Report</span></span></td>
<td><span data-ttu-id="59742-125">Aruande loomine, aruande seadistamine või olemasoleva aruande muutmine.</span><span class="sxs-lookup"><span data-stu-id="59742-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59742-126">Väljund ja jaotus</span><span class="sxs-lookup"><span data-stu-id="59742-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="59742-127">Väljundi tüübi ja aruande sihtkoha muutmine.</span><span class="sxs-lookup"><span data-stu-id="59742-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59742-128">Päised ja jalused</span><span class="sxs-lookup"><span data-stu-id="59742-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="59742-129">Aruande päiste ja jaluste määratlemine ja vormindamine.</span><span class="sxs-lookup"><span data-stu-id="59742-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="59742-130">Näiteks saate lisada päisesse või jalusesse teksti või pilte.</span><span class="sxs-lookup"><span data-stu-id="59742-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="59742-131">Finantsaruandlus toetab piltide puhul failivorminguid .bmp, .jpg ja .png.</span><span class="sxs-lookup"><span data-stu-id="59742-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="59742-132">Võite sisestada ka automaatteksti koode muu teabe, näiteks ettevõtte nime, aruande nime või lehekülje numbri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="59742-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="59742-133">Sätted</span><span class="sxs-lookup"><span data-stu-id="59742-133">Settings</span></span></td>
<td><span data-ttu-id="59742-134">Aruande definitsiooni sätete, näiteks järgmiste sätete määratlemine.</span><span class="sxs-lookup"><span data-stu-id="59742-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="59742-135">Summade vormindamine ja ümardamine</span><span class="sxs-lookup"><span data-stu-id="59742-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="59742-136">Üksikasjade aruannete vormindamine</span><span class="sxs-lookup"><span data-stu-id="59742-136">Format detail reports</span></span></li>
<li><span data-ttu-id="59742-137">Aruandluspuude vormindamine</span><span class="sxs-lookup"><span data-stu-id="59742-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="59742-138">Erandite aruande loomine</span><span class="sxs-lookup"><span data-stu-id="59742-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="59742-139">Valuuta konverteerimise määratlemine</span><span class="sxs-lookup"><span data-stu-id="59742-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="59742-140">Vahesumma ja konto üksikasjade filtrimine</span><span class="sxs-lookup"><span data-stu-id="59742-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="59742-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="59742-141">Additional resources</span></span>

[<span data-ttu-id="59742-142">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="59742-142">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]