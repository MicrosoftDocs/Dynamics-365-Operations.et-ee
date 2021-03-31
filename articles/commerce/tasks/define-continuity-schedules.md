---
title: " Järjepidevuse graafikute määratlemine"
description: See teema selgitab järjepidevusprogrammi (teisisõnu korduvate tellimuste) seadistamist.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRContinuitySchedule, EcoResProductDetailsExtended
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f385d97ce8c458ada944609e165ebd0db500b546
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229932"
---
# <a name="define-continuity-schedules"></a><span data-ttu-id="61420-103"> Järjepidevuse graafikute määratlemine</span><span class="sxs-lookup"><span data-stu-id="61420-103">Define continuity schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61420-104">See teema selgitab järjepidevusprogrammi (teisisõnu korduvate tellimuste) seadistamist.</span><span class="sxs-lookup"><span data-stu-id="61420-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="61420-105">Selles teemas kasutatakse demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="61420-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="61420-106">Järjepidevusprogrammi loomine</span><span class="sxs-lookup"><span data-stu-id="61420-106">Create continuity program</span></span>
1. <span data-ttu-id="61420-107">Avage Jaemüük ja kaubandus > Järjepidevus > Järjepidevusprogrammid.</span><span class="sxs-lookup"><span data-stu-id="61420-107">Go to Retail and Commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="61420-108">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="61420-108">Click New.</span></span>
3. <span data-ttu-id="61420-109">Tippige väljale Graafiku ID järjepidevuse graafiku ID</span><span class="sxs-lookup"><span data-stu-id="61420-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="61420-110">Tehke väljal Tellimuse algus valik Esimene sündmus.</span><span class="sxs-lookup"><span data-stu-id="61420-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="61420-111">Kui klient esitab uue järjepidevusprogrammi tellimuse, on toote lähetamiseks kaks võimalust. 1.</span><span class="sxs-lookup"><span data-stu-id="61420-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="61420-112">Esimene sündmus: saadetakse järjepidevusprogrammi esimene toode.</span><span class="sxs-lookup"><span data-stu-id="61420-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="61420-113">2.</span><span class="sxs-lookup"><span data-stu-id="61420-113">2.</span></span> <span data-ttu-id="61420-114">Praegune sündmus: saadetakse praegune toode.</span><span class="sxs-lookup"><span data-stu-id="61420-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="61420-115">Näide.</span><span class="sxs-lookup"><span data-stu-id="61420-115">For example.</span></span> <span data-ttu-id="61420-116">Kolme kuu programm, klient saab programmi kolmanda toote.</span><span class="sxs-lookup"><span data-stu-id="61420-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="61420-117">Valige Jah, et küsitaks tellimuse alguskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="61420-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="61420-118">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="61420-118">Click Add line.</span></span>
7. <span data-ttu-id="61420-119">Tippige väljale Kaubakood esimese toote kaubakood (0013).</span><span class="sxs-lookup"><span data-stu-id="61420-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="61420-120">Tüüp PP.</span><span class="sxs-lookup"><span data-stu-id="61420-120">Type 'CP'.</span></span>
9. <span data-ttu-id="61420-121">Sisestage kuupäev, millal esimene toode on tellimiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="61420-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="61420-122">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="61420-122">Click Add line.</span></span>
11. <span data-ttu-id="61420-123">Sisestage väljale Kaubakood väärtus 0014.</span><span class="sxs-lookup"><span data-stu-id="61420-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="61420-124">Eemaldage väljalt Kuupäevaintervalli kood väärtus, et väli oleks tühi.</span><span class="sxs-lookup"><span data-stu-id="61420-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="61420-125">Selle protseduuri puhul kustutage kuupäevaintervall.</span><span class="sxs-lookup"><span data-stu-id="61420-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="61420-126">Kuupäev määratakse astmeliselt esimese kauba alguskuupäevast.</span><span class="sxs-lookup"><span data-stu-id="61420-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="61420-127">Siia saab sisestada toodete tarnimise intervalli.</span><span class="sxs-lookup"><span data-stu-id="61420-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="61420-128">Tippige 30.</span><span class="sxs-lookup"><span data-stu-id="61420-128">Type '30'.</span></span>
    * <span data-ttu-id="61420-129">Igakuise programmi puhul sisestatakse intervalliks 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="61420-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="61420-130">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="61420-130">Click Add line.</span></span>
15. <span data-ttu-id="61420-131">Sisestage väljale Kaubakood väärtus 0015.</span><span class="sxs-lookup"><span data-stu-id="61420-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="61420-132">Tippige Lõpp.</span><span class="sxs-lookup"><span data-stu-id="61420-132">Type 'End'.</span></span>
17. <span data-ttu-id="61420-133">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="61420-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="61420-134">Järjepidevale kaubale määramine</span><span class="sxs-lookup"><span data-stu-id="61420-134">Assign to continuity item</span></span>
1. <span data-ttu-id="61420-135">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="61420-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="61420-136">Valige kaup 0016.</span><span class="sxs-lookup"><span data-stu-id="61420-136">Select item '0016'.</span></span>
    * <span data-ttu-id="61420-137">Selle protseduuri puhul valige kauba number 0016.</span><span class="sxs-lookup"><span data-stu-id="61420-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="61420-138">Tavaliselt olete loonud väljastatud toote, millele on rakendatud järjepidevuse äriloogika, kui see pannakse kõnekeskuses müügitellimusse.</span><span class="sxs-lookup"><span data-stu-id="61420-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="61420-139">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="61420-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="61420-140">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="61420-140">Click Edit.</span></span>
5. <span data-ttu-id="61420-141">Laiendage või ahendage jaotist Müük.</span><span class="sxs-lookup"><span data-stu-id="61420-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="61420-142">Siia saate sisestada järjepidevusprogrammi, mida see kaup esindab.</span><span class="sxs-lookup"><span data-stu-id="61420-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="61420-143">Tippige varem loodud graafiku ID.</span><span class="sxs-lookup"><span data-stu-id="61420-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="61420-144">Kui see kaup kõnekeskuses müüakse, rakendatakse valitud järjepidevusprogrammist täiendav äriloogika.</span><span class="sxs-lookup"><span data-stu-id="61420-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="61420-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="61420-145">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]