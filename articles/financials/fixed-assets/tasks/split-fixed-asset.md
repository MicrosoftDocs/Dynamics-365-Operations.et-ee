---
title: Põhivara tükeldamine
description: See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6be9de64265a4d7b5c91af3ee8acfce80c78e0f1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333365"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="b8cc4-103">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="b8cc4-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b8cc4-104">See ülesande juhend tükeldab ühe vara raamatu protsendi uude vara raamatusse.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-104">This task guide will split a percentage of one asset book to a new asset book.</span></span>  <span data-ttu-id="b8cc4-105">See kasutab raamatupidaja rolli ja USMF-i demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="b8cc4-106">Uue põhivara loomine</span><span class="sxs-lookup"><span data-stu-id="b8cc4-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="b8cc4-107">Minge jaotisse Põhivarad > Põhivarad > Põhivarad.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-107">Go to Fixed assets > Fixed assets > Fixed assets.</span></span>
2. <span data-ttu-id="b8cc4-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-108">Click New.</span></span>
3. <span data-ttu-id="b8cc4-109">Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-109">In the Fixed asset group field, enter or select a value.</span></span>
4. <span data-ttu-id="b8cc4-110">Märkige põhivara kood hilisemaks tükeldamisprotsessis kasutamiseks üles.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-110">Note the fixed asset number to use in the split process later.</span></span>
5. <span data-ttu-id="b8cc4-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-111">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b8cc4-112">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="b8cc4-113">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="b8cc4-113">Split a fixed asset</span></span>
1. <span data-ttu-id="b8cc4-114">Leidke loendist tükeldatav põhivara ja valige see.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-114">In the list, find and select the fixed asset to split.</span></span>
2. <span data-ttu-id="b8cc4-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-115">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="b8cc4-116">Klõpsake valikut Raamatud.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-116">Click Books.</span></span>
    * <span data-ttu-id="b8cc4-117">Valige uuele varale tükeldatav raamat.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-117">Select the book to split to the new asset.</span></span>  
4. <span data-ttu-id="b8cc4-118">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-118">Click Functions.</span></span>
5. <span data-ttu-id="b8cc4-119">Klõpsake suvandit Tükelda põhivara.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-119">Click Split fixed asset.</span></span>
6. <span data-ttu-id="b8cc4-120">Sisestage väärtus väljale Põhivarasse või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-120">In the To fixed asset field, enter or select a value.</span></span>
7. <span data-ttu-id="b8cc4-121">Klõpsake väljal Raamatusse otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-121">In the To book field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="b8cc4-122">Sisestage kuupäev väljale Kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-122">In the Transaction date field, enter a date.</span></span>
9. <span data-ttu-id="b8cc4-123">Sisestage number väljale Protsent.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-123">In the Percent field, enter a number.</span></span>
10. <span data-ttu-id="b8cc4-124">Valige või sisestage väärtus väljal Töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-124">In the Journal name field, enter or select a value.</span></span>
11. <span data-ttu-id="b8cc4-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-125">Click OK.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="b8cc4-126">Töölehekande sisestamine</span><span class="sxs-lookup"><span data-stu-id="b8cc4-126">Post the journal transaction</span></span>
1. <span data-ttu-id="b8cc4-127">Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-127">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="b8cc4-128">Valige loendist tükeldamise protsessis loodud tööleht.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-128">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="b8cc4-129">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-129">Click Lines.</span></span>
    * <span data-ttu-id="b8cc4-130">Kontrollige loodud töölehe ridu.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-130">Verify the journal lines created.</span></span>  <span data-ttu-id="b8cc4-131">Soetamise korrigeerimiskanne luuakse algse vara puhul väärtuse vähendamiseks tükeldamisprotsessis määratud protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-131">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  <span data-ttu-id="b8cc4-132">Soetamiskanne luuakse uue vara puhul samas summas.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-132">An Acquisition transaction is created for the new asset for the same amount.</span></span>  
4. <span data-ttu-id="b8cc4-133">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="b8cc4-133">Click Post.</span></span>

