--- 
title: " Järjepidevusprogrammi kasutamine"
description: "See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist."
author: scott-tucker
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5d3b5690bfbd10b77e784d35d0c4f4518de58333
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="use-a-continuity-program"></a><span data-ttu-id="17c3a-103"> Järjepidevusprogrammi kasutamine</span><span class="sxs-lookup"><span data-stu-id="17c3a-103">Use a continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="17c3a-104">See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist.</span><span class="sxs-lookup"><span data-stu-id="17c3a-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="17c3a-105">Protseduuri tegemiseks tuleb kasutaja seadistada kõnekeskuse kasutajaks.</span><span class="sxs-lookup"><span data-stu-id="17c3a-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="17c3a-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="17c3a-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="17c3a-107">Avage Jaemüük ja kaubandus > Kliendid > Klienditeenindus.</span><span class="sxs-lookup"><span data-stu-id="17c3a-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="17c3a-108">Tippige väljale SearchText väärtus Karen ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="17c3a-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="17c3a-109">Avanema peaks täpsema otsingu dialoog.</span><span class="sxs-lookup"><span data-stu-id="17c3a-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="17c3a-110">Kui see ei avane, klõpsake nuppu Otsing sellest väljast paremal.</span><span class="sxs-lookup"><span data-stu-id="17c3a-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="17c3a-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="17c3a-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="17c3a-112">Seal peaks olema ainult üks rida, milles on näha Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="17c3a-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="17c3a-113">Valige see rida, klõpsates linnukese veergu ruudustiku vasakus servas.</span><span class="sxs-lookup"><span data-stu-id="17c3a-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="17c3a-114">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="17c3a-114">Click Select.</span></span>
5. <span data-ttu-id="17c3a-115">Klõpsake valikul New sales order (Uus müügitellimus).</span><span class="sxs-lookup"><span data-stu-id="17c3a-115">Click New sales order.</span></span>
    * <span data-ttu-id="17c3a-116">Müügitellimuse number tuleks üles märkida.</span><span class="sxs-lookup"><span data-stu-id="17c3a-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="17c3a-117">Seda on protseduuris hiljem vaja.</span><span class="sxs-lookup"><span data-stu-id="17c3a-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="17c3a-118">Tippige väljale Kaubakood väärtus 88000 ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="17c3a-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="17c3a-119">See on demoettevõtte USRT puhul järjepidev kaup.</span><span class="sxs-lookup"><span data-stu-id="17c3a-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="17c3a-120">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="17c3a-120">Click Complete.</span></span>
8. <span data-ttu-id="17c3a-121">Sisestage väljale Makseviis väärtus Visa.</span><span class="sxs-lookup"><span data-stu-id="17c3a-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="17c3a-122">Klõpsake nuppu Lisa krediitkaart.</span><span class="sxs-lookup"><span data-stu-id="17c3a-122">Click Add credit card.</span></span>
    * <span data-ttu-id="17c3a-123">Sisestage sellele lehele vajalik krediitkaarditeave.</span><span class="sxs-lookup"><span data-stu-id="17c3a-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="17c3a-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17c3a-124">Click OK.</span></span>
11. <span data-ttu-id="17c3a-125">Laiendage jaotist Makse.</span><span class="sxs-lookup"><span data-stu-id="17c3a-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="17c3a-126">Kõnekeskuse tellimuse esitamiseks tuleb tellimusele sisestada maksed.</span><span class="sxs-lookup"><span data-stu-id="17c3a-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="17c3a-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17c3a-127">Click OK.</span></span>
13. <span data-ttu-id="17c3a-128">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="17c3a-128">Click Submit.</span></span>
    * <span data-ttu-id="17c3a-129">Uus järjepidev tellimus on valmis.</span><span class="sxs-lookup"><span data-stu-id="17c3a-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="17c3a-130">Järgmiseks tuleb käivitada kaks partiitöötlust, mida kasutatakse järjepidevate tellimuste töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="17c3a-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="17c3a-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="17c3a-131">Close the page.</span></span>
15. <span data-ttu-id="17c3a-132">Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevuse maksete töötlemine.</span><span class="sxs-lookup"><span data-stu-id="17c3a-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="17c3a-133">Tippige väljale Järjepidev kaup väärtus 88000 ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="17c3a-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="17c3a-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17c3a-134">Click OK.</span></span>
18. <span data-ttu-id="17c3a-135">Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevuse tütartellimuste loomine.</span><span class="sxs-lookup"><span data-stu-id="17c3a-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="17c3a-136">See protsess loob uued müügitellimused, mis põhinevad teie järjepidevusprogrammide sätetel.</span><span class="sxs-lookup"><span data-stu-id="17c3a-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="17c3a-137">Tippige väljale Järjepidev kaup väärtus 88000 ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="17c3a-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="17c3a-138">Kaup 88000 on demoettevõtte USRT puhul järjepidev kaup.</span><span class="sxs-lookup"><span data-stu-id="17c3a-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="17c3a-139">Valige või sisestage väärtus väljal Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="17c3a-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="17c3a-140">Sisestage müügitellimuse number, mille protseduuris enne üles märkisite.</span><span class="sxs-lookup"><span data-stu-id="17c3a-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="17c3a-141">See tagab sellele protseduurile minimaalse töötlemisaja.</span><span class="sxs-lookup"><span data-stu-id="17c3a-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="17c3a-142">Müügitellimuse väli on valikuline – töödelda saab mis tahes programmi kõiki tellimusi.</span><span class="sxs-lookup"><span data-stu-id="17c3a-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="17c3a-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="17c3a-143">Click OK.</span></span>


