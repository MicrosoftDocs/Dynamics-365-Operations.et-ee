---
title: Finantsaruandluse KKK
description: Sellesse teemasse on kogutud teiste kasutajate esitatud finantsaruandlusega seotud küsimused.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923021"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="5cf78-103">Finantsaruandluse KKK</span><span class="sxs-lookup"><span data-stu-id="5cf78-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="5cf78-104">Selles teemas antakse vastused korduma kippuvatele küsimustele finantsaruandluse kohta.</span><span class="sxs-lookup"><span data-stu-id="5cf78-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="5cf78-105">Kuidas piirata puuturbe abil juurdepääsu aruandele?</span><span class="sxs-lookup"><span data-stu-id="5cf78-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="5cf78-106">Järgmises näites kirjeldatakse aruandele juurdepääsu piiramist puuturbe abil.</span><span class="sxs-lookup"><span data-stu-id="5cf78-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="5cf78-107">Demoettevõttel USMF on bilansiaruanne, millele ei pea kõik finantsaruandluse kasutajad juurde pääsema.</span><span class="sxs-lookup"><span data-stu-id="5cf78-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="5cf78-108">Juurdepääsu piiramiseks saate kasutada puuturvet, et keelata juurdepääs ühele aruandele, nii et sellele pääseksid juurde ainult teatud kasutajad.</span><span class="sxs-lookup"><span data-stu-id="5cf78-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="5cf78-109">Juurdepääsu piiramiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="5cf78-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="5cf78-110">Logige sisse Financial Reporter Report Designerisse.</span><span class="sxs-lookup"><span data-stu-id="5cf78-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="5cf78-111">Looge uus puudefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="5cf78-111">Create a new tree definition.</span></span> <span data-ttu-id="5cf78-112">Avage **Fail > Uus > Puu definitsioon**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="5cf78-113">Topeltklõpsake veerus **Üksuse turve** rida **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="5cf78-114">Valige **Kasutajad ja grupid**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="5cf78-115">Valige kasutajad või grupid, kellele soovite anda juurdepääsu sellele aruandele.</span><span class="sxs-lookup"><span data-stu-id="5cf78-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="5cf78-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-116">Select **Save**.</span></span>
7. <span data-ttu-id="5cf78-117">Lisage aruandedefinitsioonis uus puudefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="5cf78-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="5cf78-118">Valige puudefinitsioonis **Säte**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="5cf78-119">Valige jaotises **Aruandlusüksuse valik** **Kaasa kõik üksused**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="5cf78-120">Kuidas tuvastada, millised kontod minu saldodele ei vasta?</span><span class="sxs-lookup"><span data-stu-id="5cf78-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="5cf78-121">Kui teil on aruanne, millel pole vastavaid saldosid, võivad järgmised tegevused aidata teil selliseid kontosid ja hälbeid tuvastada.</span><span class="sxs-lookup"><span data-stu-id="5cf78-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="5cf78-122">**Financial Reporter Report Designer**</span><span class="sxs-lookup"><span data-stu-id="5cf78-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="5cf78-123">Looge Financial Reporter Report Designeris uus readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="5cf78-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="5cf78-124">Valige **Redigeeri > Lisa read dimensioonidest**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="5cf78-125">Valige **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="5cf78-126">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-126">Select **OK**.</span></span>
5. <span data-ttu-id="5cf78-127">Salvestage readefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="5cf78-127">Save the row definition.</span></span>
6. <span data-ttu-id="5cf78-128">Uue veerudefinitsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="5cf78-128">Create a new column definition</span></span>
7. <span data-ttu-id="5cf78-129">Looge uus aruandedefinitsioon.</span><span class="sxs-lookup"><span data-stu-id="5cf78-129">Create a new report definition.</span></span>
8. <span data-ttu-id="5cf78-130">Valige **Sätted** ja tühjendage selle suvandi ruut.</span><span class="sxs-lookup"><span data-stu-id="5cf78-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="5cf78-131">Looge aruanne.</span><span class="sxs-lookup"><span data-stu-id="5cf78-131">Generate the report.</span></span> 
10. <span data-ttu-id="5cf78-132">Eksportige aruanne Microsoft Excelisse.</span><span class="sxs-lookup"><span data-stu-id="5cf78-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="5cf78-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="5cf78-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="5cf78-134">Avage Dynamics 365 Finance'is **Pearaamat > Päringud ja aruanded > Proovibilanss**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="5cf78-135">Saate määrata järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="5cf78-135">Set the following parameters:</span></span>
   - <span data-ttu-id="5cf78-136">**Alguskuupäev** – sisestage finantsaasta algus.</span><span class="sxs-lookup"><span data-stu-id="5cf78-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="5cf78-137">**Lõppkuupäev** – sisestage kuupäev, mille kohta aruande loote.</span><span class="sxs-lookup"><span data-stu-id="5cf78-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="5cf78-138">**Finantsdimensioon** – seadke selle välja väärtuseks **Põhikonto kogum**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="5cf78-139">Valige **Arvuta**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="5cf78-140">Eksportige aruanne Microsoft Excelisse.</span><span class="sxs-lookup"><span data-stu-id="5cf78-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="5cf78-141">Nüüd saate kopeerida andmeid Financial Reporteri Exceli aruandest proovibilansi aruandesse, et võrrelda veerge **Sulgemissaldo**.</span><span class="sxs-lookup"><span data-stu-id="5cf78-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]