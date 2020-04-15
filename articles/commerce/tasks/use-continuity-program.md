---
title: Järjepidevusprogrammi kasutamine
description: See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2baf0127a35cc62952fd78daaf8204d35ec8d2b3
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141146"
---
# <a name="using-continuity-program"></a><span data-ttu-id="fca08-103">Järjepidevusprogrammi kasutamine</span><span class="sxs-lookup"><span data-stu-id="fca08-103">Using continuity program</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fca08-104">See protseduur selgitab järjepidevusprogrammi müüki ja seotud müügitellimuste töötlemist.</span><span class="sxs-lookup"><span data-stu-id="fca08-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="fca08-105">Protseduuri tegemiseks tuleb kasutaja seadistada kõnekeskuse kasutajaks.</span><span class="sxs-lookup"><span data-stu-id="fca08-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="fca08-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="fca08-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="fca08-107">Avage Jaemüük ja kaubandus > Kliendid > Klienditeenindus.</span><span class="sxs-lookup"><span data-stu-id="fca08-107">Go to Retail and Commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="fca08-108">Tippige väljale SearchText väärtus Karen ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="fca08-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="fca08-109">Avanema peaks täpsema otsingu dialoog.</span><span class="sxs-lookup"><span data-stu-id="fca08-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="fca08-110">Kui see ei avane, klõpsake nuppu Otsing sellest väljast paremal.</span><span class="sxs-lookup"><span data-stu-id="fca08-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="fca08-111">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="fca08-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fca08-112">Seal peaks olema ainult üks rida, milles on näha Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="fca08-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="fca08-113">Valige see rida, klõpsates linnukese veergu ruudustiku vasakus servas.</span><span class="sxs-lookup"><span data-stu-id="fca08-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="fca08-114">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="fca08-114">Click Select.</span></span>
5. <span data-ttu-id="fca08-115">Klõpsake valikul New sales order (Uus müügitellimus).</span><span class="sxs-lookup"><span data-stu-id="fca08-115">Click New sales order.</span></span>
    * <span data-ttu-id="fca08-116">Müügitellimuse number tuleks üles märkida.</span><span class="sxs-lookup"><span data-stu-id="fca08-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="fca08-117">Seda on protseduuris hiljem vaja.</span><span class="sxs-lookup"><span data-stu-id="fca08-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="fca08-118">Tippige väljale Kaubakood väärtus 88000 ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="fca08-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="fca08-119">See on demoettevõtte USRT puhul järjepidev kaup.</span><span class="sxs-lookup"><span data-stu-id="fca08-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="fca08-120">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="fca08-120">Click Complete.</span></span>
8. <span data-ttu-id="fca08-121">Sisestage väljale Makseviis väärtus Visa.</span><span class="sxs-lookup"><span data-stu-id="fca08-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="fca08-122">Klõpsake nuppu Lisa krediitkaart.</span><span class="sxs-lookup"><span data-stu-id="fca08-122">Click Add credit card.</span></span>
    * <span data-ttu-id="fca08-123">Sisestage sellele lehele vajalik krediitkaarditeave.</span><span class="sxs-lookup"><span data-stu-id="fca08-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="fca08-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fca08-124">Click OK.</span></span>
11. <span data-ttu-id="fca08-125">Laiendage jaotist Makse.</span><span class="sxs-lookup"><span data-stu-id="fca08-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="fca08-126">Kõnekeskuse tellimuse esitamiseks tuleb tellimusele sisestada maksed.</span><span class="sxs-lookup"><span data-stu-id="fca08-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="fca08-127">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fca08-127">Click OK.</span></span>
13. <span data-ttu-id="fca08-128">Klõpsake Edasta.</span><span class="sxs-lookup"><span data-stu-id="fca08-128">Click Submit.</span></span>
    * <span data-ttu-id="fca08-129">Uus järjepidev tellimus on valmis.</span><span class="sxs-lookup"><span data-stu-id="fca08-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="fca08-130">Järgmiseks tuleb käivitada kaks partiitöötlust, mida kasutatakse järjepidevate tellimuste töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="fca08-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="fca08-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="fca08-131">Close the page.</span></span>
15. <span data-ttu-id="fca08-132">Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevuse maksete töötlemine.</span><span class="sxs-lookup"><span data-stu-id="fca08-132">Go to Retail and Commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="fca08-133">Tippige väljale Järjepidev kaup väärtus 88000 ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="fca08-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="fca08-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fca08-134">Click OK.</span></span>
18. <span data-ttu-id="fca08-135">Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevuse tütartellimuste loomine.</span><span class="sxs-lookup"><span data-stu-id="fca08-135">Go to Retail and Commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="fca08-136">See protsess loob uued müügitellimused, mis põhinevad teie järjepidevusprogrammide sätetel.</span><span class="sxs-lookup"><span data-stu-id="fca08-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="fca08-137">Tippige väljale Järjepidev kaup väärtus 88000 ja vajutage siis tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="fca08-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="fca08-138">Kaup 88000 on demoettevõtte USRT puhul järjepidev kaup.</span><span class="sxs-lookup"><span data-stu-id="fca08-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="fca08-139">Valige või sisestage väärtus väljal Müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="fca08-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="fca08-140">Sisestage müügitellimuse number, mille protseduuris enne üles märkisite.</span><span class="sxs-lookup"><span data-stu-id="fca08-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="fca08-141">See tagab sellele protseduurile minimaalse töötlemisaja.</span><span class="sxs-lookup"><span data-stu-id="fca08-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="fca08-142">Müügitellimuse väli on valikuline – töödelda saab mis tahes programmi kõiki tellimusi.</span><span class="sxs-lookup"><span data-stu-id="fca08-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="fca08-143">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="fca08-143">Click OK.</span></span>

