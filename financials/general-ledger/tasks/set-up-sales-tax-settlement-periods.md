--- 
title: "Saate häälestada käibemaksu tasakaalustusperioode."
description: "Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4d65dee3bd059966458cb9603807de85b704fc49
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="e103b-103">Saate häälestada käibemaksu tasakaalustusperioode.</span><span class="sxs-lookup"><span data-stu-id="e103b-103">Set up sales tax settlement periods</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e103b-104">Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="e103b-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="e103b-105">Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="e103b-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="e103b-106">Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="e103b-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="e103b-107">Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.</span><span class="sxs-lookup"><span data-stu-id="e103b-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="e103b-108">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="e103b-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="e103b-109">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid.</span><span class="sxs-lookup"><span data-stu-id="e103b-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="e103b-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e103b-110">Click New.</span></span>
3. <span data-ttu-id="e103b-111">Sisestage väärtus väljale Tasakaalustusperiood.</span><span class="sxs-lookup"><span data-stu-id="e103b-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="e103b-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e103b-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e103b-113">Valige väljal Maksuhaldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.</span><span class="sxs-lookup"><span data-stu-id="e103b-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="e103b-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e103b-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="e103b-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e103b-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="e103b-116">Klõpsake väljal Maksetingimused otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e103b-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e103b-117">Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve.</span><span class="sxs-lookup"><span data-stu-id="e103b-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="e103b-118">Maksetingimused määratlevad avatud hankija arve maksetähtaja.</span><span class="sxs-lookup"><span data-stu-id="e103b-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="e103b-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e103b-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="e103b-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e103b-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="e103b-121">Valige tasakaalustusperioodi vahemike tüüp.</span><span class="sxs-lookup"><span data-stu-id="e103b-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="e103b-122">Sisestage perioodivahemiku ühikute arv perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="e103b-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="e103b-123">Näiteks kvartalis on 3 kuud.</span><span class="sxs-lookup"><span data-stu-id="e103b-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="e103b-124">Märkige või tühjendage ruut Kasuta käibemaksu tasakaalustamiseks pakktöötlust.</span><span class="sxs-lookup"><span data-stu-id="e103b-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="e103b-125">Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="e103b-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="e103b-126">See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.</span><span class="sxs-lookup"><span data-stu-id="e103b-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="e103b-127">Laiendage vahekaarti Perioodivahemikud.</span><span class="sxs-lookup"><span data-stu-id="e103b-127">Expand the Period intervals tab.</span></span>
15. <span data-ttu-id="e103b-128">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e103b-128">Click Add.</span></span>
16. <span data-ttu-id="e103b-129">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e103b-129">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="e103b-130">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="e103b-130">In the From date field, enter a date.</span></span>
18. <span data-ttu-id="e103b-131">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="e103b-131">In the To date field, enter a date.</span></span>
19. <span data-ttu-id="e103b-132">Klõpsake suvandit Uus perioodivahemik.</span><span class="sxs-lookup"><span data-stu-id="e103b-132">Click New period interval.</span></span>
    * <span data-ttu-id="e103b-133">Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e103b-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="e103b-134">Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.</span><span class="sxs-lookup"><span data-stu-id="e103b-134">You can come back and add new period intervals as required.</span></span>  
20. <span data-ttu-id="e103b-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e103b-135">Close the page.</span></span>


