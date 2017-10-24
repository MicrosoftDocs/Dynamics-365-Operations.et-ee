--- 
title: "Laadimisaadressi määramine ühendusesisesele kandele"
description: "See protseduur näitab, kuidas määrata ühendusesisese kaubanduskande puhul laadimisaadressi."
author: v-oloski
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fc54b59f6cf8aec8d489955c57cbcf34c4e6be0a
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="specify-a-lading-address-for-an-intra-community-transaction"></a><span data-ttu-id="b1571-103">Laadimisaadressi määramine ühendusesisesele kandele</span><span class="sxs-lookup"><span data-stu-id="b1571-103">Specify a lading address for an intra-community transaction</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1571-104">See protseduur näitab, kuidas määrata ühendusesisese kaubanduskande puhul laadimisaadressi.</span><span class="sxs-lookup"><span data-stu-id="b1571-104">This procedure shows how to specify a lading address for an intra-community trade transaction.</span></span> <span data-ttu-id="b1571-105">Näiteks Saksamaa ettevõte tellib kaupu Saksamaa aadressiga hankijalt.</span><span class="sxs-lookup"><span data-stu-id="b1571-105">For example, a Germany company orders items from a vendor with a German business address.</span></span> <span data-ttu-id="b1571-106">Sellel hankijal on ladu Itaalias ja ta lähetab kaubad sealt.</span><span class="sxs-lookup"><span data-stu-id="b1571-106">This vendor has a warehouse in Italy and ships the items from there.</span></span> <span data-ttu-id="b1571-107">Tarne peab kajastuma intrastati aruandes.</span><span class="sxs-lookup"><span data-stu-id="b1571-107">This delivery must be reported in the Intrastat.</span></span> <span data-ttu-id="b1571-108">Sama kehtib klienditagastuste puhul.</span><span class="sxs-lookup"><span data-stu-id="b1571-108">The same behavior is valid for customer returns.</span></span>
<span data-ttu-id="b1571-109">See protseduur kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="b1571-109">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="b1571-110">Ülesande loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Saksamaa, andmeid.</span><span class="sxs-lookup"><span data-stu-id="b1571-110">The task was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="b1571-111">Enne selle protseduuri läbimist tuleb konfigureerida intrastati aruandlus.</span><span class="sxs-lookup"><span data-stu-id="b1571-111">Before you can complete this procedure, you must configure Intrastat reporting.</span></span> <span data-ttu-id="b1571-112">See protseduur on mõeldud raamatupidajatele.</span><span class="sxs-lookup"><span data-stu-id="b1571-112">This procedure is intended for accountants.</span></span> <span data-ttu-id="b1571-113">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="b1571-113">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="b1571-114">Avage Ostureskontro > Ostutellimused > Kõik ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="b1571-114">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="b1571-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b1571-115">Click New.</span></span>
3. <span data-ttu-id="b1571-116">Sisestage või valige väärtus</span><span class="sxs-lookup"><span data-stu-id="b1571-116">Enter or select a value</span></span>
    * <span data-ttu-id="b1571-117">Valige näiteks DE-001.</span><span class="sxs-lookup"><span data-stu-id="b1571-117">For example, select DE-001.</span></span> <span data-ttu-id="b1571-118">Sellel hankija ettevõttel on Saksamaa aadress.</span><span class="sxs-lookup"><span data-stu-id="b1571-118">This vendor has a German business address.</span></span>  
4. <span data-ttu-id="b1571-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b1571-119">Click OK.</span></span>
5. <span data-ttu-id="b1571-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b1571-120">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b1571-121">Sisestage või valige väärtus D0001 väljal Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="b1571-121">In the Item number field, enter or select a value D0001.</span></span>
7. <span data-ttu-id="b1571-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b1571-122">Click Save.</span></span>
8. <span data-ttu-id="b1571-123">Klõpsake toimingupaanil valikut Vastuvõtt.</span><span class="sxs-lookup"><span data-stu-id="b1571-123">On the Action Pane, click Receive.</span></span>
9. <span data-ttu-id="b1571-124">Klõpsake valikut Transpordi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b1571-124">Click Transportation details.</span></span>
10. <span data-ttu-id="b1571-125">Sisestage kuupäev ja kellaaeg väljale Laadimise kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="b1571-125">In the Loading date and time field, enter a date and time.</span></span>
11. <span data-ttu-id="b1571-126">Klõpsake valikut Lisa aadress.</span><span class="sxs-lookup"><span data-stu-id="b1571-126">Click Add address.</span></span>
12. <span data-ttu-id="b1571-127">Klõpsake nuppu Uus ja looge uus aadress eesmärgiga Laadimine.</span><span class="sxs-lookup"><span data-stu-id="b1571-127">Click New and create new address with purpose Lading.</span></span>
13. <span data-ttu-id="b1571-128">Tippige väljale Nimi või kirjeldus Itaalia.</span><span class="sxs-lookup"><span data-stu-id="b1571-128">In the Name or description field, type 'Italian'.</span></span>
14. <span data-ttu-id="b1571-129">Valige väärtuseks Laadimine.</span><span class="sxs-lookup"><span data-stu-id="b1571-129">Select Lading as the value.</span></span>
    * <span data-ttu-id="b1571-130">Pange tähele, et aadressi eesmärk peab olema Laadimine</span><span class="sxs-lookup"><span data-stu-id="b1571-130">Note that that address purpose must be Lading.</span></span>  
15. <span data-ttu-id="b1571-131">Sisestage või valige väärtus ITA väljal Riik/piirkond.</span><span class="sxs-lookup"><span data-stu-id="b1571-131">In the Country/region field, enter or select a value ITA.</span></span>
16. <span data-ttu-id="b1571-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b1571-132">Click Save.</span></span>
17. <span data-ttu-id="b1571-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b1571-133">Close the page.</span></span>
18. <span data-ttu-id="b1571-134">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b1571-134">Click Save.</span></span>
    * <span data-ttu-id="b1571-135">Kontrollige, et laadimisaadress oleks õige.</span><span class="sxs-lookup"><span data-stu-id="b1571-135">Verify that the lading address is correct.</span></span>  
19. <span data-ttu-id="b1571-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b1571-136">Close the page.</span></span>
20. <span data-ttu-id="b1571-137">Klõpsake toimingupaanil valikut Ost.</span><span class="sxs-lookup"><span data-stu-id="b1571-137">On the Action Pane, click Purchase.</span></span>
21. <span data-ttu-id="b1571-138">Klõpsake käsku Kinnita.</span><span class="sxs-lookup"><span data-stu-id="b1571-138">Click Confirm.</span></span>
22. <span data-ttu-id="b1571-139">Klõpsake toimingupaanil valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="b1571-139">On the Action Pane, click Invoice.</span></span>
23. <span data-ttu-id="b1571-140">Klõpsake valikut Arve.</span><span class="sxs-lookup"><span data-stu-id="b1571-140">Click Invoice.</span></span>
24. <span data-ttu-id="b1571-141">Sisestage väärtus väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="b1571-141">In the Number field, type a value.</span></span>
25. <span data-ttu-id="b1571-142">Sisestage kuupäev väljale Arve kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b1571-142">In the Invoice date field, enter a date.</span></span>
26. <span data-ttu-id="b1571-143">Rippdialoogi avamiseks klõpsake valikut Vaikimisi asukohast: toote sissetuleku kogus.</span><span class="sxs-lookup"><span data-stu-id="b1571-143">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
27. <span data-ttu-id="b1571-144">Valige Tellitud kogus väljal Ridade vaikekogus.</span><span class="sxs-lookup"><span data-stu-id="b1571-144">In the Default quantity for lines field, select 'Ordered quantity'.</span></span>
28. <span data-ttu-id="b1571-145">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b1571-145">Click OK.</span></span>
29. <span data-ttu-id="b1571-146">Klõpsake valikut Transpordi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b1571-146">Click Transportation details.</span></span>
    * <span data-ttu-id="b1571-147">Kontrollige, et kaubad lähetati Itaaliast.</span><span class="sxs-lookup"><span data-stu-id="b1571-147">Verify that goods were shipped from Italy.</span></span> <span data-ttu-id="b1571-148">Vajaduse korral saate laadimise üksikasju muuta.</span><span class="sxs-lookup"><span data-stu-id="b1571-148">If necessary, you can edit the lading details.</span></span>  
30. <span data-ttu-id="b1571-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b1571-149">Close the page.</span></span>
31. <span data-ttu-id="b1571-150">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="b1571-150">Click Post.</span></span>
32. <span data-ttu-id="b1571-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b1571-151">Close the page.</span></span>
33. <span data-ttu-id="b1571-152">Avage Maks > Deklaratsioonid > Väliskaubandus > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="b1571-152">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
34. <span data-ttu-id="b1571-153">Klõpsake käsku Ülekanne.</span><span class="sxs-lookup"><span data-stu-id="b1571-153">Click Transfer.</span></span>
35. <span data-ttu-id="b1571-154">Tehke väljal Hankija arve valik Jah.</span><span class="sxs-lookup"><span data-stu-id="b1571-154">Select Yes in the Vendor invoice field.</span></span>
36. <span data-ttu-id="b1571-155">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b1571-155">Click OK.</span></span>
37. <span data-ttu-id="b1571-156">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="b1571-156">Click the General tab.</span></span>
    * <span data-ttu-id="b1571-157">Otsige üles äsja loodud rida ja veenduge, et saatja saatis kaubad Itaaliast.</span><span class="sxs-lookup"><span data-stu-id="b1571-157">Find a newly created line and verify that the sender shipped the goods from Italy.</span></span>  


