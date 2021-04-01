---
title: " Riistvarajaama loomine ja seostamine"
description: See protseduur selgitab uue riistvarajaama loomist.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailHardwareStation, RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d0c02246a20ef28c0f4f28b73dfe5ff56f38a68b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247040"
---
# <a name="create-and-associate-a-hardware-station"></a><span data-ttu-id="9648b-103"> Riistvarajaama loomine ja seostamine</span><span class="sxs-lookup"><span data-stu-id="9648b-103">Create and associate a hardware station</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9648b-104">See protseduur selgitab uue riistvarajaama loomist.</span><span class="sxs-lookup"><span data-stu-id="9648b-104">This procedure walks through how to create a new hardware station.</span></span> <span data-ttu-id="9648b-105">Luuakse uus riistvaraprofiil ja kasutatakse seda uute riistvarajaamade lisamiseks eelmääratletud kauplusse (kanalisse).</span><span class="sxs-lookup"><span data-stu-id="9648b-105">A new hardware profile will be created and used to add new hardware stations to a pre-defined store (channel).</span></span> <span data-ttu-id="9648b-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="9648b-106">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9648b-107">Avage Kaubanduse põhiandmed > Kanalid >...</span><span class="sxs-lookup"><span data-stu-id="9648b-107">Go to Commerce essentials > Channels > ..</span></span> <span data-ttu-id="9648b-108">> ..</span><span class="sxs-lookup"><span data-stu-id="9648b-108">> ..</span></span> <span data-ttu-id="9648b-109">> ..</span><span class="sxs-lookup"><span data-stu-id="9648b-109">> ..</span></span> <span data-ttu-id="9648b-110">> Riistvarajaamade profiilid.</span><span class="sxs-lookup"><span data-stu-id="9648b-110">> Hardware station profiles.</span></span>
2. <span data-ttu-id="9648b-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9648b-111">Click New.</span></span>
3. <span data-ttu-id="9648b-112">Sisestage väljale Riistvarajaama ID tekst „TestHWProfile”.</span><span class="sxs-lookup"><span data-stu-id="9648b-112">In the Hardware station ID field, type 'TestHWProfile'.</span></span>
4. <span data-ttu-id="9648b-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="9648b-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9648b-114">Sisestage number väljale Pordi number.</span><span class="sxs-lookup"><span data-stu-id="9648b-114">In the Port number field, enter a number.</span></span>
6. <span data-ttu-id="9648b-115">Klõpsake väljal Riistvaraprofiil otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9648b-115">In the Hardware profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="9648b-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9648b-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="9648b-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9648b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9648b-118">Klõpsake väljal Paketi nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9648b-118">In the Package name field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9648b-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9648b-119">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9648b-120">See on uue keskkonnaga kaasnev standardne pakett.</span><span class="sxs-lookup"><span data-stu-id="9648b-120">This is the standard package that comes with a new environment.</span></span> <span data-ttu-id="9648b-121">Versiooni seerianumber võib olla erinev.</span><span class="sxs-lookup"><span data-stu-id="9648b-121">The version number may vary.</span></span>  
11. <span data-ttu-id="9648b-122">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9648b-122">Click Save.</span></span>
12. <span data-ttu-id="9648b-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9648b-123">Close the page.</span></span>
13. <span data-ttu-id="9648b-124">Minge jaotisse Jaemüük ja kaubandus > Kanalid > Kõik kauplused.</span><span class="sxs-lookup"><span data-stu-id="9648b-124">Go to Retail and Commerce > Channels > All stores.</span></span>
14. <span data-ttu-id="9648b-125">Valige loendist rida 17.</span><span class="sxs-lookup"><span data-stu-id="9648b-125">In the list, select row 17.</span></span>
    * <span data-ttu-id="9648b-126">Kui kasutate demoettevõtet USRT, on tegemist Houstoni kauplusega.</span><span class="sxs-lookup"><span data-stu-id="9648b-126">If you are using the USRT demo data company, this is the Houston store.</span></span>  
15. <span data-ttu-id="9648b-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9648b-127">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="9648b-128">Laiendage jaotist Riistvarajaamad.</span><span class="sxs-lookup"><span data-stu-id="9648b-128">Toggle the expansion of the Hardware stations section.</span></span>
17. <span data-ttu-id="9648b-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9648b-129">Click Add.</span></span>
18. <span data-ttu-id="9648b-130">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9648b-130">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="9648b-131">Klõpsake väljal Profiili ID otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9648b-131">In the Profile ID field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="9648b-132">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9648b-132">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9648b-133">See peab olema eelmistes etappides loodud uue riistvarajaama profiil.</span><span class="sxs-lookup"><span data-stu-id="9648b-133">This must be the new hardware station profile that was created in the previous steps.</span></span>  
21. <span data-ttu-id="9648b-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9648b-134">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="9648b-135">Sisestage väärtus väljale Hosti nimi.</span><span class="sxs-lookup"><span data-stu-id="9648b-135">In the Host name field, type a value.</span></span>
23. <span data-ttu-id="9648b-136">Sisestage väärtus väljale EFT terminal.</span><span class="sxs-lookup"><span data-stu-id="9648b-136">In the EFT terminal ID field, type a value.</span></span>
24. <span data-ttu-id="9648b-137">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9648b-137">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]