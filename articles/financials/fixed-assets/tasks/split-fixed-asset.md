--- 
title: "Põhivara tükeldamine"
description: "See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 86d07f07bd15d8b2dbbc987027b2e6976001f554
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="3478b-103">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="3478b-103">Split a fixed asset</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3478b-104">See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse.</span><span class="sxs-lookup"><span data-stu-id="3478b-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="3478b-105">See kasutab raamatupidaja rolli ja USMF-i demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="3478b-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="3478b-106">Uue põhivara loomine</span><span class="sxs-lookup"><span data-stu-id="3478b-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="3478b-107">Minge jaotisse Põhivarad > Põhivarad > Põhivarad.</span><span class="sxs-lookup"><span data-stu-id="3478b-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="3478b-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3478b-108">Click New.</span></span>
3. <span data-ttu-id="3478b-109">Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="3478b-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="3478b-110">Märkige põhivara kood hilisemaks tükeldamisprotsessis kasutamiseks üles.</span><span class="sxs-lookup"><span data-stu-id="3478b-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="3478b-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="3478b-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="3478b-112">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="3478b-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="3478b-113">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="3478b-113">Split a fixed asset</span></span>
1. <span data-ttu-id="3478b-114">Leidke loendist tükeldatav põhivara ja valige see.</span><span class="sxs-lookup"><span data-stu-id="3478b-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="3478b-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3478b-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="3478b-116">Klõpsake valikut Raamatud.</span><span class="sxs-lookup"><span data-stu-id="3478b-116">Click Books.</span></span>
    * <span data-ttu-id="3478b-117">Valige uuele varale tükeldatav raamat.</span><span class="sxs-lookup"><span data-stu-id="3478b-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="3478b-118">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="3478b-118">Click Functions.</span></span>
5. <span data-ttu-id="3478b-119">Klõpsake suvandit Tükelda põhivara.</span><span class="sxs-lookup"><span data-stu-id="3478b-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="3478b-120">Sisestage väärtus väljale Põhivarasse või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="3478b-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="3478b-121">Klõpsake väljal Raamatusse otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3478b-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="3478b-122">Sisestage kuupäev väljale Kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="3478b-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="3478b-123">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="3478b-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="3478b-124">Valige või sisestage väärtus väljal Töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="3478b-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="3478b-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3478b-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="3478b-126">Töölehekande sisestamine</span><span class="sxs-lookup"><span data-stu-id="3478b-126">Post the journal transaction</span></span>
1. <span data-ttu-id="3478b-127">Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.</span><span class="sxs-lookup"><span data-stu-id="3478b-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="3478b-128">Valige loendist tükeldamise protsessis loodud tööleht.</span><span class="sxs-lookup"><span data-stu-id="3478b-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="3478b-129">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="3478b-129">Click Lines.</span></span>
    * <span data-ttu-id="3478b-130">Kontrollige loodud töölehe ridu.</span><span class="sxs-lookup"><span data-stu-id="3478b-130">Verify the journal lines created.</span></span>  <span data-ttu-id="3478b-131">Soetamise korrigeerimiskanne luuakse algse vara puhul väärtuse vähendamiseks tükeldamisprotsessis määratud protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="3478b-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="3478b-132">Soetamiskanne luuakse uue vara puhul samas summas.</span><span class="sxs-lookup"><span data-stu-id="3478b-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="3478b-133">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="3478b-133">Click Post.</span></span>


