--- 
title: " Kassa loagruppide loomine"
description: "See protseduur näitab, kuidas kassalubade gruppi luua."
author: scott-tucker
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: bcda7c3a5c2cc97fbc6e4945e4d5f0ec42a7a478
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="create-pos-permission-groups"></a><span data-ttu-id="ffa62-103"> Kassa loagruppide loomine</span><span class="sxs-lookup"><span data-stu-id="ffa62-103">Create POS permission groups</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ffa62-104">See protseduur näitab, kuidas kassalubade gruppi luua.</span><span class="sxs-lookup"><span data-stu-id="ffa62-104">This procedure will show how to create a POS permission group.</span></span> <span data-ttu-id="ffa62-105">Selle tegevuse loomisel kasutati demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="ffa62-105">The demo data company used to create this task is USRT.</span></span> <span data-ttu-id="ffa62-106">See ülesanne on mõeldud Jaemüügitoimingute halduri rolli jaoks.</span><span class="sxs-lookup"><span data-stu-id="ffa62-106">This task is intended for the Retail operations manager role.</span></span>

1. <span data-ttu-id="ffa62-107">Tehke valik Permission groups (Lubade grupid).</span><span class="sxs-lookup"><span data-stu-id="ffa62-107">Go to Permission groups.</span></span>
2. <span data-ttu-id="ffa62-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ffa62-108">Click New.</span></span>
3. <span data-ttu-id="ffa62-109">Sisestage väärtus väljale POS permission group ID (Kassalubade grupi ID).</span><span class="sxs-lookup"><span data-stu-id="ffa62-109">In the POS permission group ID field, type a value.</span></span>
4. <span data-ttu-id="ffa62-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ffa62-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ffa62-111">Valige Yes (Jah) väljal View time clock entries (Vaata ajaarvesti kirjeid).</span><span class="sxs-lookup"><span data-stu-id="ffa62-111">Select Yes in the View time clock entries field.</span></span>
    * <span data-ttu-id="ffa62-112">Saate nüüd oma kassalubade grupile erinevaid lube anda või neid eemaldada.</span><span class="sxs-lookup"><span data-stu-id="ffa62-112">You can now enable or disable various permissions for your POS Permission group.</span></span> <span data-ttu-id="ffa62-113">Mõne loa jaoks saate määrata väärtuse, mida kasutatakse hindamiseks, kas kassa kasutaja saab seda toimingut teha.</span><span class="sxs-lookup"><span data-stu-id="ffa62-113">For some permission you can set a value that will be used to evaluate if the POS user can perform the action.</span></span>  <span data-ttu-id="ffa62-114">See tegevusjuhend annab mõned load, mida kassapidajale võidakse määrata.</span><span class="sxs-lookup"><span data-stu-id="ffa62-114">This task guide enables a few permission that might be given to a cashier.</span></span>  
6. <span data-ttu-id="ffa62-115">Valige Yes (Jah) väljal Allow create order (Luba tellimuse loomine).</span><span class="sxs-lookup"><span data-stu-id="ffa62-115">Select Yes in the Allow create order field.</span></span>
7. <span data-ttu-id="ffa62-116">Valige Yes (Jah) väljal Allow edit order field (Luba tellimuse redigeerimine).</span><span class="sxs-lookup"><span data-stu-id="ffa62-116">Select Yes in the Allow edit order field.</span></span>
8. <span data-ttu-id="ffa62-117">Valige Yes (Jah) väljal Allow retrieve order (Luba tellimuse väljaotsimine).</span><span class="sxs-lookup"><span data-stu-id="ffa62-117">Select Yes in the Allow retrieve order field.</span></span>
9. <span data-ttu-id="ffa62-118">Valige Yes (Jah) väljal Allow password change (Luba parooli muutmine).</span><span class="sxs-lookup"><span data-stu-id="ffa62-118">Select Yes in the Allow password change field.</span></span>
10. <span data-ttu-id="ffa62-119">Valige Yes (Jah) väljal Allow blind close (Luba pimesi sulgemine).</span><span class="sxs-lookup"><span data-stu-id="ffa62-119">Select Yes in the Allow blind close field.</span></span>
11. <span data-ttu-id="ffa62-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ffa62-120">Click Save.</span></span>
    * <span data-ttu-id="ffa62-121">Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused jaemüügikanalitesse edastada.</span><span class="sxs-lookup"><span data-stu-id="ffa62-121">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  
12. <span data-ttu-id="ffa62-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ffa62-122">Close the page.</span></span>
13. <span data-ttu-id="ffa62-123">Minge valikusse Jobs (Tööd).</span><span class="sxs-lookup"><span data-stu-id="ffa62-123">Go to Jobs.</span></span>
    * <span data-ttu-id="ffa62-124">Järgmisena määrame kassalubade grupi töö järgi.</span><span class="sxs-lookup"><span data-stu-id="ffa62-124">Next we will assign the POS permission group to a Job.</span></span>  
14. <span data-ttu-id="ffa62-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ffa62-125">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ffa62-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ffa62-126">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="ffa62-127">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="ffa62-127">Click Edit.</span></span>
17. <span data-ttu-id="ffa62-128">Laiendage jaotist Job classification (Tööde klassifikatsioon).</span><span class="sxs-lookup"><span data-stu-id="ffa62-128">Expand the Job classification section.</span></span>
18. <span data-ttu-id="ffa62-129">Sisestage või valige väärtus väljal POS permission group (Kassalubade grupp).</span><span class="sxs-lookup"><span data-stu-id="ffa62-129">In the POS permission group field, enter or select a value.</span></span>
    * <span data-ttu-id="ffa62-130">Kõik töötajad, kelle ametikohad sellele tööle vastavad, kasutavad selle kassalubade grupi sätteid, kui töötajate kassalube ei ole nende ametikoha tasemel tühistatud.</span><span class="sxs-lookup"><span data-stu-id="ffa62-130">All Workers in Positions for this Job will use this POS permission group’s settings unless the workers POS permissions have been overridden at their Position level.</span></span>  
19. <span data-ttu-id="ffa62-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ffa62-131">Click Save.</span></span>
    * <span data-ttu-id="ffa62-132">Pärast muudatuste salvestamist peate käivitama personali jaotusgraafiku, et muutused jaemüügikanalitesse edastada.</span><span class="sxs-lookup"><span data-stu-id="ffa62-132">After your changes are saved you need to run the Staff distribution schedule to push the changes to retail channels.</span></span>  


