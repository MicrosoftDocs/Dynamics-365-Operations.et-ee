--- 
title: "Saate häälestada käibemaksu tasakaalustusperioode."
description: "Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu."
author: twheeloc
manager: AnnBe
ms.date: 10/15/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 81214cc52b1488bb70ac5fd6ccc817f6f979163d
ms.openlocfilehash: 1087ed78e91b487ca7157bfdac1d72ae3f477875
ms.contentlocale: et-ee
ms.lasthandoff: 10/16/2018

---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="548a9-103">Saate häälestada käibemaksu tasakaalustusperioode.</span><span class="sxs-lookup"><span data-stu-id="548a9-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="548a9-104">Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="548a9-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="548a9-105">Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="548a9-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="548a9-106">Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="548a9-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="548a9-107">Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.</span><span class="sxs-lookup"><span data-stu-id="548a9-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="548a9-108">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="548a9-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="548a9-109">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid.</span><span class="sxs-lookup"><span data-stu-id="548a9-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="548a9-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="548a9-110">Click New.</span></span>
3. <span data-ttu-id="548a9-111">Sisestage väärtus väljale Tasakaalustusperiood.</span><span class="sxs-lookup"><span data-stu-id="548a9-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="548a9-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="548a9-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="548a9-113">Valige väljal Maksuhaldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.</span><span class="sxs-lookup"><span data-stu-id="548a9-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="548a9-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="548a9-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="548a9-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="548a9-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="548a9-116">Klõpsake väljal Maksetingimused otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="548a9-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="548a9-117">Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve.</span><span class="sxs-lookup"><span data-stu-id="548a9-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="548a9-118">Maksetingimused määratlevad avatud hankija arve maksetähtaja.</span><span class="sxs-lookup"><span data-stu-id="548a9-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="548a9-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="548a9-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="548a9-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="548a9-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="548a9-121">Valige tasakaalustusperioodi vahemike tüüp.</span><span class="sxs-lookup"><span data-stu-id="548a9-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="548a9-122">Sisestage perioodivahemiku ühikute arv perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="548a9-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="548a9-123">Näiteks kvartalis on 3 kuud.</span><span class="sxs-lookup"><span data-stu-id="548a9-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="548a9-124">Märkige või tühjendage ruut Kasuta käibemaksu tasakaalustamiseks pakktöötlust.</span><span class="sxs-lookup"><span data-stu-id="548a9-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="548a9-125">Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="548a9-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="548a9-126">See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.</span><span class="sxs-lookup"><span data-stu-id="548a9-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
14. <span data-ttu-id="548a9-127">Märkige või tühjendage Vastasmaksukannete loomise vältimise märkeruut.</span><span class="sxs-lookup"><span data-stu-id="548a9-127">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="548a9-128">Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid.</span><span class="sxs-lookup"><span data-stu-id="548a9-128">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="548a9-129">Märkige see märkeruut, et vältida vastasmaksukannete loomist.</span><span class="sxs-lookup"><span data-stu-id="548a9-129">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="548a9-130">Laiendage vahekaarti Perioodivahemikud.</span><span class="sxs-lookup"><span data-stu-id="548a9-130">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="548a9-131">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="548a9-131">Click Add.</span></span>
17. <span data-ttu-id="548a9-132">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="548a9-132">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="548a9-133">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="548a9-133">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="548a9-134">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="548a9-134">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="548a9-135">Klõpsake suvandit Uus perioodivahemik.</span><span class="sxs-lookup"><span data-stu-id="548a9-135">Click New period interval.</span></span>
    * <span data-ttu-id="548a9-136">Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="548a9-136">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="548a9-137">Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.</span><span class="sxs-lookup"><span data-stu-id="548a9-137">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="548a9-138">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="548a9-138">Close the page.</span></span>


