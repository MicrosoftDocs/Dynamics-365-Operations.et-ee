---
title: Saate häälestada käibemaksu tasakaalustusperioode.
description: Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.
author: twheeloc
manager: AnnBe
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8304d9e8997a5d31740ee1203aa4bf0603014056
ms.sourcegitcommit: d0fa8d0140fa81029527edb317623c1a7737c593
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/05/2019
ms.locfileid: "1862984"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="a1e84-103">Saate häälestada käibemaksu tasakaalustusperioode.</span><span class="sxs-lookup"><span data-stu-id="a1e84-103">Set up sales tax settlement periods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a1e84-104">Käibemaksu tasakaalustusperioodid sisaldavad teavet perioodivahemike kohta, mille puhul tuleb esitada ja maksta käibemaksu.</span><span class="sxs-lookup"><span data-stu-id="a1e84-104">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="a1e84-105">Tasakaalustusprotsessi saab käitada konkreetse kuupäevavahemiku tasakaalustusperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="a1e84-105">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="a1e84-106">Kõik tasakaalustusperioodiga seotud maksukoodid tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="a1e84-106">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="a1e84-107">Seotud käibemaksuhalduri seadistamisest olenevalt sisestatakse maksukohustus kas hankija või pearaamatu kontole.</span><span class="sxs-lookup"><span data-stu-id="a1e84-107">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>



<span data-ttu-id="a1e84-108">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="a1e84-108">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="a1e84-109">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksu tasakaalustusperioodid.</span><span class="sxs-lookup"><span data-stu-id="a1e84-109">Go to Tax > Indirect taxes > Sales tax > Sales tax settlement periods.</span></span>
2. <span data-ttu-id="a1e84-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a1e84-110">Click New.</span></span>
3. <span data-ttu-id="a1e84-111">Sisestage väärtus väljale Tasakaalustusperiood.</span><span class="sxs-lookup"><span data-stu-id="a1e84-111">In the Settlement period field, type a value.</span></span>
4. <span data-ttu-id="a1e84-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="a1e84-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="a1e84-113">Valige väljal Maksuhaldur, kellele tasakaalustusperioodi puhul loodud aruanded ja maksed saadetakse.</span><span class="sxs-lookup"><span data-stu-id="a1e84-113">In the Authority field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="a1e84-114">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a1e84-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="a1e84-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a1e84-115">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a1e84-116">Klõpsake väljal Maksetingimused otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a1e84-116">In the Terms of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a1e84-117">Seotud käibemaksuhalduri saab seadistada kui hankija ja käibemaksu tasakaalustus loob avatud hankija arve.</span><span class="sxs-lookup"><span data-stu-id="a1e84-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="a1e84-118">Maksetingimused määratlevad avatud hankija arve maksetähtaja.</span><span class="sxs-lookup"><span data-stu-id="a1e84-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
9. <span data-ttu-id="a1e84-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a1e84-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="a1e84-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a1e84-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="a1e84-121">Valige tasakaalustusperioodi vahemike tüüp.</span><span class="sxs-lookup"><span data-stu-id="a1e84-121">Select a type for the settlement period intervals.</span></span>
12. <span data-ttu-id="a1e84-122">Sisestage perioodivahemiku ühikute arv perioodi kohta.</span><span class="sxs-lookup"><span data-stu-id="a1e84-122">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="a1e84-123">Näiteks kvartalis on 3 kuud.</span><span class="sxs-lookup"><span data-stu-id="a1e84-123">For example, a quarter has 3 months.</span></span>
13. <span data-ttu-id="a1e84-124">Märkige või tühjendage ruut Kasuta käibemaksu tasakaalustamiseks pakktöötlust.</span><span class="sxs-lookup"><span data-stu-id="a1e84-124">Select or clear the Use batch processing for sales tax settlement check box.</span></span>
    * <span data-ttu-id="a1e84-125">Tasakaalustusperioodi tasakaalustusprotsessi saab töödelda taustal pakett-tööna.</span><span class="sxs-lookup"><span data-stu-id="a1e84-125">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="a1e84-126">See on soovitatav suure hulga maksukannete puhul kuupäevavahemiku jooksul.</span><span class="sxs-lookup"><span data-stu-id="a1e84-126">This is recommended for a large number of tax transactions within a period interval.</span></span>  
    > [!NOTE]
    > <span data-ttu-id="a1e84-127">Praegu puudub selle tugi Austrias, Belgias, Hispaanias, Itaalias, Jaapanis ja Hollandis.</span><span class="sxs-lookup"><span data-stu-id="a1e84-127">Currently this is not supported in Austria, Belgium, Spain, Italy, Japan, and the Netherlands.</span></span>
14. <span data-ttu-id="a1e84-128">Märkige või tühjendage Vastasmaksukannete loomise vältimise märkeruut.</span><span class="sxs-lookup"><span data-stu-id="a1e84-128">Select or clear the Prevent generating offset tax transactions check box.</span></span>
    * <span data-ttu-id="a1e84-129">Süsteem loob tasakaalustusprotsessi ajal vaikimisi vastasmaksukandeid, mis põhjustavad jõudlusprobleeme, kui perioodivahemikul on suur hulk maksukandeid.</span><span class="sxs-lookup"><span data-stu-id="a1e84-129">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="a1e84-130">Märkige see märkeruut, et vältida vastasmaksukannete loomist.</span><span class="sxs-lookup"><span data-stu-id="a1e84-130">Select this check box to prevent generating offset tax transactions.</span></span>
15. <span data-ttu-id="a1e84-131">Laiendage vahekaarti Perioodivahemikud.</span><span class="sxs-lookup"><span data-stu-id="a1e84-131">Expand the Period intervals tab.</span></span>
16. <span data-ttu-id="a1e84-132">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a1e84-132">Click Add.</span></span>
17. <span data-ttu-id="a1e84-133">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a1e84-133">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a1e84-134">Sisestage kuupäev väljale Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="a1e84-134">In the From date field, enter a date.</span></span>
19. <span data-ttu-id="a1e84-135">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="a1e84-135">In the To date field, enter a date.</span></span>
20. <span data-ttu-id="a1e84-136">Klõpsake suvandit Uus perioodivahemik.</span><span class="sxs-lookup"><span data-stu-id="a1e84-136">Click New period interval.</span></span>
    * <span data-ttu-id="a1e84-137">Kui esimene perioodivahemik on sisestatud, saab uusi perioode luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="a1e84-137">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="a1e84-138">Vajaduse korral saate naasta ja uusi perioodivahemikke lisada.</span><span class="sxs-lookup"><span data-stu-id="a1e84-138">You can come back and add new period intervals as required.</span></span>  
21. <span data-ttu-id="a1e84-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a1e84-139">Close the page.</span></span>

